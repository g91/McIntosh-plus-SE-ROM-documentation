# Memory Manager & Heap Architecture

## 1. Overview of the Macintosh Memory Architecture

The classic Macintosh Memory Manager (`plus/os/memory_mgr.s` and `se/os/memory_mgr.s`) provides dynamic memory allocation for the operating system and applications. Unlike simple linear allocators or modern paged virtual memory systems, the 68000 Macintosh lacked a memory management unit (MMU) in early models. To prevent memory fragmentation while running multiple resources, desk accessories, and application segments in a small physical RAM space (128 KB to 4 MB), Apple designed a sophisticated dual-allocation model:
1. **Non-relocatable blocks (Pointers)**: Fixed in memory at a specific physical address until explicitly freed.
2. **Relocatable blocks (Handles)**: Can be moved, compacted, or purged by the Memory Manager whenever free contiguous space is needed.

---

## 2. Heap Zone Data Structure (`Zone`)

Dynamic memory is divided into **Heap Zones**:
- **System Zone (`SysZone`)**: Created at startup at the lowest RAM addresses. Holds system globals, device driver control entries, VCBs, FCBs, and event queues.
- **Application Zone (`ApplZone`)**: Created when an application launches. Resides above the system heap and extends up toward the application stack.
- **Current Zone (`TheZone` / `CurZone`)**: Pointer in low memory (`$0118`) indicating the active zone for current allocations.

Each zone is governed by a 52-byte header structure (`Zone` record):

```
Offset  Field       Type      Description
------  ----------  --------  -------------------------------------------------------------
$00     bkLim       Ptr       Pointer to the first byte immediately following the zone
$04     purgePtr    Ptr       Pointer used internally during heap purging
$08     hFstFree    Ptr       Pointer to the first free Master Pointer in the zone's MP block
$0C     zcbFree     LongInt   Total number of free bytes currently available in the zone
$10     gzProc      ProcPtr   Address of GrowZone function (called when heap runs out of room)
$14     moreMast    Integer   Number of Master Pointers allocated per block (32 sys, 64 app)
$16     flags       Integer   Internal zone control flags (bit 4: fNSelCompct)
$18     cntRel      Integer   Count of relocatable blocks
$1A     maxRel      Integer   Maximum relocatable blocks seen
$1C     cntNRel     Integer   Count of non-relocatable blocks
$1E     maxNRel     Integer   Maximum non-relocatable blocks seen
$20     cntEmpty    Integer   Count of empty Master Pointers
$22     cntHandles  Integer   Count of allocated handles
$24     minCBFree   LongInt   Minimum contiguous free bytes threshold
$28     purgeProc   ProcPtr   Purge-warning callback procedure
$2C     sparePtr    Ptr       Internal pointer (system GrowZone procedure)
$30     allocPtr    Ptr       Roving allocation pointer for fast roving-fit allocation
$34     heapData    Integer   First byte of usable heap memory space
```

---

## 3. Physical Block Header Format (24-Bit Mode)

Every allocated or free block in a heap zone is prefixed by an 8-byte header:

```
Bytes 0 - 3 (tagBC):
+--------+--------+--------+--------+
| T1  T0 |  Corr  |   Physical Size |  (3 bytes: 24-bit physical size including header)
+--------+--------+--------+--------+
  Bits 7-6: Tag    Bits 3-0: Extra bytes

Bytes 4 - 7 (handle):
+-----------------------------------+
| Relative Handle Offset or Zone    |
+-----------------------------------+
```

### Tag Byte Breakdown (Byte 0)
- **Bits 7 - 6 (Block Type)**:
  - `00`: **Free Block** (Available memory in heap).
  - `01`: **Non-relocatable Block** (Pointer).
  - `10`: **Relocatable Block** (Handle).
- **Bits 3 - 0 (Size Correction)**:
  - Because 68000 word and longword alignment requires block sizes to be multiples of 4 or 8 bytes, this nibble indicates how many padding bytes sit at the end of the block.
- **Bytes 1 - 3 (Physical Block Size)**:
  - 24-bit integer representing total bytes including the 8-byte header. Minimum block size is 12 bytes.

### Second Longword (Byte 4 - 7)
- For **Relocatable blocks**: Contains the **Relative Handle Offset** (`MasterPointerAddress - ZoneAddress`). Storing relative offsets allowed heap zones to be relocated as a whole.
- For **Non-relocatable blocks**: Points back to the base address of the owning `Zone`.
- For **Free blocks**: Points to the next free block in the free list chain.

---

## 4. Handles and Master Pointers

Applications never reference the physical address of a relocatable block directly. Instead, they reference a **Handle** (`**Ptr`), which is a pointer to a **Master Pointer**:

```
Application Variable (Handle)
        |
        v
+-------------------------------+
| Master Pointer (in MP Table)  | ---> [ Flags Byte | 24-bit Physical Block Address ]
+-------------------------------+                                 |
                                                                  v
                                                 +---------------------------------+
                                                 | Block Header (8 bytes)          |
                                                 +---------------------------------+
                                                 | Block Data Contents             |
                                                 | (Can be moved during compaction)|
                                                 +---------------------------------+
```

### Master Pointer Flags (High Byte in 24-Bit Addressing)
The upper 8 bits of every 32-bit Master Pointer store state flags:
- **Bit 7 (`$80`) - Locked**: The block cannot be moved during compaction.
- **Bit 6 (`$40`) - Purgeable**: The Memory Manager may deallocate this block if heap space is exhausted. If purged, the Master Pointer is set to `NIL`, but the handle remains valid.
- **Bit 5 (`$20`) - Resource**: The block is managed by the Resource Manager.

---

## 5. Compaction, Purging, and Allocation Flow

When an allocation request arrives (`_NewHandle` or `_NewPtr`), the Memory Manager executes a multi-stage fallback strategy:

```
[ Allocation Request: NewHandle(N) ]
                 |
                 v
[ 1. Roving First-Fit Scan ] ---> Free block >= N found? ---> Allocate & Return
                 | (No)
                 v
[ 2. Compact Heap (CompactMem) ]
  - Slide unlocked relocatable blocks downward toward zone base.
  - Consolidate all fragmented free blocks into one large contiguous block at the top.
  - Large enough? ---> Allocate & Return
                 | (No)
                 v
[ 3. Purge Heap (PurgeMem) ]
  - Deallocate purgeable relocatable blocks (bit 6 set in MP).
  - Compact heap again.
  - Large enough? ---> Allocate & Return
                 | (No)
                 v
[ 4. Invoke GrowZone Procedure ]
  - Call application's gzProc callback (e.g., release caches, reduce document buffers).
  - Large enough? ---> Allocate & Return
                 | (No)
                 v
[ Failure ] ---> Return NIL and set MemErr = memFullErr (-108)
```

---

## 6. Labeled Function Directory

Every routine in `plus/os/memory_mgr.s` and `se/os/memory_mgr.s` is cataloged below:

### 6.1 Pointer Allocation Traps (Non-relocatable)
- **`NewPtr`** (`$A11E`):
  - *Prototype*: `FUNCTION NewPtr(logicalSize: Size): Ptr;`
  - *Entry*: `D0.L` = Size. Trap bit 9 (`$A31E`) = Zero-fill block. Trap bit 10 (`$A51E`) = Allocate in System Heap.
  - *Exit*: `A0` = Pointer (NIL on failure). `D0.W` = Result code (`noErr` or `memFullErr`).
  - *Details*: Calls `MakePtrSpc` to make room as low in the zone as possible, preserving high memory for relocatable blocks.
- **`DisposPtr`** (`$A01F`):
  - *Prototype*: `PROCEDURE DisposPtr(p: Ptr);`
  - *Entry*: `A0` = Pointer to free.
  - *Exit*: `D0.W` = Result code. Tags block as free and coalesces with adjacent free blocks.
- **`GetPtrSize`** (`$A021`):
  - *Prototype*: `FUNCTION GetPtrSize(p: Ptr): Size;`
  - *Entry*: `A0` = Pointer. *Exit*: `D0.L` = Logical size in bytes (physical size minus header and correction).
- **`SetPtrSize`** (`$A020`):
  - *Prototype*: `PROCEDURE SetPtrSize(p: Ptr; newSize: Size);`
  - *Entry*: `A0` = Pointer, `D0.L` = New size. Can expand only if adjacent forward block is free.

### 6.2 Handle Allocation Traps (Relocatable)
- **`NewHandle`** (`$A122`):
  - *Prototype*: `FUNCTION NewHandle(logicalSize: Size): Handle;`
  - *Entry*: `D0.L` = Size. Trap bit 9 (`$A322`) = Clear block. Trap bit 10 (`$A522`) = System Heap.
  - *Exit*: `A0` = Handle (pointer to Master Pointer).
  - *Details*: Allocates a Master Pointer from `hFstFree` (calling `MoreMasters` if empty), allocates block data in high zone space.
- **`DisposHandle`** (`$A023`):
  - *Prototype*: `PROCEDURE DisposHandle(h: Handle);`
  - *Entry*: `A0` = Handle. Marks block as free, clears physical address in Master Pointer, returns MP to free list.
- **`GetHandleSize`** (`$A025`) / **`SetHandleSize`** (`$A024`):
  - Get or dynamically resize a relocatable block. `SetHandleSize` can compact memory to grow the block.
- **`HandleZone`** (`$A126`):
  - *Prototype*: `FUNCTION HandleZone(h: Handle):牙Zone;`
  - *Entry*: `A0` = Handle. *Exit*: `A0` = Pointer to owning `Zone`.

### 6.3 Handle State Operations
- **`HLock`** (`$A029`) / **`HUnlock`** (`$A02A`):
  - Sets or clears bit 7 of the Master Pointer. Locked blocks cannot be relocated during compaction.
- **`HPurge`** (`$A04B`) / **`HNoPurge`** (`$A04A`):
  - Sets or clears bit 6 of the Master Pointer.
- **`MoveHHi`** (`$A064`):
  - Moves a relocatable block to the highest possible position in the heap zone before locking it, preventing heap fragmentation.

### 6.4 Heap Management & Maintenance
- **`CompactMem`** (`$A04C`):
  - *Prototype*: `FUNCTION CompactMem(cbNeeded: Size): Size;`
  - Slides unlocked relocatable blocks down without purging. Returns size of largest contiguous free block.
- **`PurgeMem`** (`$A04D`):
  - Purges all purgeable blocks in the zone until `cbNeeded` contiguous bytes are free.
- **`ResrvMem`** (`$A040`):
  - Reserves contiguous space at the bottom of the zone by moving relocatable blocks up.
- **`MaxMem`** (`$A11D`):
  - Compacts and purges the entire zone to determine the theoretical maximum single allocation possible.
- **`InitZone`** (`$A019`) / **`InitApplZone`** (`$A02C`):
  - Initializes zone structures, zeroes Master Pointer tables, and sets up zone boundary limits.
- **`SetApplLimit`** (`$A02D`) / **`SetApplBase`** (`$A057`):
  - Sets application heap boundaries and expansion ceiling.


---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

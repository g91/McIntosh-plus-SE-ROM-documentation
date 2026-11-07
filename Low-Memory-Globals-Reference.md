# Low-Memory Globals Reference Directory

## 1. Overview of Low-Memory Architecture

On the Motorola 68000, physical memory beginning at address `$000000` is dedicated to hardware exception vectors and system global variables. In classic Macintosh system software, the lowest memory pages (known collectively as **Low-Memory Globals**) store the foundational state of the entire operating system, including interrupt vectors, memory manager boundaries, screen buffers, trap dispatch tables, device driver queues, and font metrics.

This directory catalogs the primary low-memory globals defined in `include/lowmem.inc` (Mac Plus) and `include/lowmem_se.inc` (Mac SE).

---

## 2. 68000 Exception Vectors ($0000 - $00FF)

| Address | Symbol | Size | Description |
| :--- | :--- | :--- | :--- |
| **`$0000`** | `SSP_Init` | Long | Power-on initial Supervisor Stack Pointer (`$00400000`). |
| **`$0004`** | `PC_Init` | Long | Power-on initial Program Counter (`$0040002A`). |
| **`$0008`** | `BusErrorVector` | Long | Bus Error exception handler vector. |
| **`$000C`** | `AddressErrorVector` | Long | Address Error exception vector (unaligned word/long access). |
| **`$0010`** | `IllegalInstructionVector` | Long | Illegal Instruction exception vector. |
| **`$0014`** | `ZeroDivVector` | Long | Integer Zero Divide exception vector. |
| **`$0018`** | `ChkVector` | Long | `CHK` bounds-check instruction vector. |
| **`$001C`** | `TrapvVector` | Long | `TRAPV` overflow instruction vector. |
| **`$0020`** | `PrivilegeViolationVector` | Long | Privilege Violation exception vector. |
| **`$0024`** | `TraceVector` | Long | Single-step Trace exception vector. |
| **`$0028`** | `ATrapVector` | Long | **A-Line Trap Exception Vector (`EMT1010`)**. |
| **`$002C`** | `FTrapVector` | Long | F-Line Unimplemented instruction vector. |
| **`$0064`** | `Lev1AutoVector` | Long | Level 1 Interrupt: VIA 6522 autovector (VBL, 60Hz tick). |
| **`$0068`** | `Lev2AutoVector` | Long | Level 2 Interrupt: SCC 8530 autovector (Serial/LocalTalk). |
| **`$006C`** | `Lev3AutoVector` | Long | Level 3 Interrupt: Simultaneous VIA + SCC. |
| **`$0070`** | `Lev4AutoVector` | Long | Level 4 Interrupt: Programmer's Interrupt switch / NMI. |

---

## 3. System Sizing & Memory Manager Globals ($0100 - $01FF)

| Address | Symbol | Size | Description |
| :--- | :--- | :--- | :--- |
| **`$0106`** | `ScreenRow` | Word | Number of bytes per screen row (typically 64 bytes = 512 pixels). |
| **`$0108`** | `MemTop` | Long | Top of physical RAM detected during boot sizing (e.g. `$400000` for 4MB). |
| **`$010C`** | `BufPtr` | Long | Base address of high memory buffers (screen and sound). Application heap cannot grow above this. |
| **`$0110`** | `StackLowPoint`| Long | Lowest point reached by application stack (used for stack-overflow check). |
| **`$0114`** | `HeapEnd` | Long | Highest address currently reachable by the active heap zone. |
| **`$0118`** | `TheZone` / `CurZone` | Long | Pointer to the active `Zone` record for dynamic allocations. |
| **`$011C`** | `UTableBase` | Long | Pointer to the Device Manager Unit Table array. |
| **`$0120`** | `MacJmp` | Long | MacsBug debugger entry vector. |
| **`$012F`** | `CPUFlag` | Byte | CPU type: `0` = 68000, `1` = 68010, `2` = 68020, `3` = 68030. |
| **`$0130`** | `ApplLimit` | Long | Upper limit address of the Application Heap Zone. |
| **`$0144`** | `SysEvtMask` | Word | Mask of enabled system event types. |
| **`$0146`** | `SysEvtBuf` | Long | Pointer to the 20-element system event queue buffer. |
| **`$014A`** | `EventQueue` | 10 Bytes | Header of the system event queue (`QHdr`). |
| **`$0154`** | `EvtBufCnt` | Word | Number of events currently pending in the event queue. |
| **`$0156`** | `RndSeed` | Long | Random number generator seed. |
| **`$015A`** | `SysVersion` | Word | Operating system version word. |
| **`$0160`** | `VBLQueue` | 10 Bytes | Header of the Vertical Blanking task queue (`QHdr`). |
| **`$016A`** | `Ticks` | Long | Master system clock: increments every 1/60th of a second since startup. |
| **`$0172`** | `MBState` | Byte | Current state of mouse button (`$00` = pressed, `$80` = released). |
| **`$0174`** | `KeyMap` | 16 Bytes | 128-bit array reflecting current up/down state of all physical keys. |

---

## 4. Parameter RAM & Hardware Drivers ($0200 - $03FF)

| Address | Symbol | Size | Description |
| :--- | :--- | :--- | :--- |
| **`$0200`** | `SysParam` | 20 Bytes | Copy of 20-byte battery-backed PRAM read from RTC at boot. |
| **`$021A`** | `JKybdTask` | Long | Vector jumped to during VBL for keyboard task polling (ADB on SE). |
| **`$021E`** | `KbdType` | Byte | Detected keyboard hardware type (Apple standard, extended, ISO). |
| **`$0220`** | `MemErr` | Word | Result code returned by last Memory Manager trap (`noErr`, `memFullErr`). |
| **`$0252`** | `Time` | Long | Real-Time Clock: seconds elapsed since January 1, 1904. |
| **`$0262`** | `BootDrive` | Word | Working directory or drive number of startup boot volume. |
| **`$02A6`** | `WarmStart` | Long | Magic longword (`$5A4F656C` = 'ZOel') indicating warm reset vs cold boot. |
| **`$02BA`** | `DSAlertTab` | Long | Pointer to System Error Alert display parameter table. |
| **`$02F6`** | `ApplZone` | Long | Pointer to the Application Heap Zone record. |
| **`$02A0`** | `SysZone` | Long | Pointer to the System Heap Zone record. |
| **`$0308`** | `DrvQHdr` | 10 Bytes | Header of disk drive queue (`QHdr`). |
| **`$0352`** | `VCBQHdr` | 10 Bytes | Header of mounted Volume Control Block queue (`QHdr`). |
| **`$034E`** | `FCBSPtr` | Long | Pointer to File Control Block array for open files. |

---

## 5. Trap Dispatch Tables ($0400 - $15FF)

| Address | Symbol | Target | Description |
| :--- | :--- | :--- | :--- |
| **`$0400` - `$07FF`** | `DispatchTab` | Plus & SE | **OS Trap Dispatch Table**: 256 longword entries ($A000 - $A0FF). |
| **`$0C00` - `$13FF`** | `ToolDispTable` | **Mac Plus** | **Toolbox Trap Dispatch Table**: 512 longword entries ($A800 - $A9FF). |
| **`$0CF8`** | `ADBBase` | **Mac SE** | Pointer to Apple Desktop Bus manager globals and device table. |
| **`$0E00` - `$15FF`** | `ToolDispTable` | **Mac SE** | **Toolbox Trap Dispatch Table (Relocated in SE)**: 512 entries. |

---

## 6. QuickDraw & User Interface Globals ($0800 - $0FFF)

| Address | Symbol | Size | Description |
| :--- | :--- | :--- | :--- |
| **`$0824`** | `ScrnBase` | Long | Pointer to active video screen frame buffer in RAM. |
| **`$0828`** | `Mouse` | Point | Current global coordinates (v, h) of mouse cursor. |
| **`$0830`** | `CrsrPin` | Rect | Bounding rectangle constraining mouse cursor movements. |
| **`$0844`** | `CrsrState` | Word | Cursor visibility depth (`0` = visible, negative = hidden). |
| **`$0898`** | `JCrsrTask` | Long | Vector to cursor-drawing routine invoked during VBL. |
| **`$0904`** | `CurrentA5` | Long | Saved copy of current application `A5` register. |
| **`$0908`** | `CurStackBase`| Long | Base of application stack. |
| **`$0910`** | `CurApName` | 32 Bytes | Pascal string storing name of currently running application. |
| **`$0984`** | `WindowList` | Long | Pointer to frontmost window in Window Manager window list. |
| **`$0A1C`** | `MenuList` | Long | Handle to active desktop menu bar list. |
| **`$0A50`** | `TopMapHndl` | Long | Handle to resource map of frontmost open resource file. |
| **`$0A60`** | `SysMapHndl` | Long | Handle to resource map of `System` file. |
| **`$0A8C`** | `RestProc` | Long | Application restart/resume vector called by System Error Handler. |


---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

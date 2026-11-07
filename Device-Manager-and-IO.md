# Device Manager & I/O Subsystem

## 1. Overview of the Device Manager

The Macintosh **Device Manager** (`plus/os/device_mgr.s` and `se/os/device_mgr.s`) provides a unified, hardware-independent communication layer between applications, file systems, and hardware peripherals. It manages both ROM-resident drivers (such as the `.Sony` floppy driver and `.Sound` driver) and RAM-resident drivers (such as desk accessories and SCSI disc drivers).

Every peripheral driver is represented by a **Device Control Entry (DCE)** referenced through a global dispatch table known as the **Unit Table**.

---

## 2. The Unit Table & Driver References

The **Unit Table** is an array of handles or pointers to DCE records located in the System Heap.
- Base address is stored in low-memory global `UTableBase` (`$011C`).
- Total number of entries is stored in `UnitNtryCnt` (`$01D2`), defaulting to 128 slots.
- **Driver Reference Numbers**: Negative integers from `-1` to `-128`.
  - Formula: $\text{Unit Number} = -(\text{RefNum} + 1)$
  - RefNum `-1` $\rightarrow$ Unit 0 (`.Sound`)
  - RefNum `-2` $\rightarrow$ Unit 1 (`.Print` or serial)
  - RefNum `-3` $\rightarrow$ Unit 2 (`.Out` modem serial)
  - RefNum `-4` $\rightarrow$ Unit 3 (`.In` modem serial)
  - RefNum `-5` $\rightarrow$ Unit 4 (`.Sony` floppy driver)
  - RefNum `-9` $\rightarrow$ Unit 8 (`.MPP` AppleTalk driver)
  - RefNum `-10` $\rightarrow$ Unit 9 (`.ATP` AppleTalk Transaction)

---

## 3. Driver Header Structure

Every device driver contains a 20-byte standard header defining its capabilities and entry points:

```
Offset  Field       Type      Description
------  ----------  --------  -------------------------------------------------------------
$00     drvrFlags   Word      Bitmask defining driver capabilities and permissions
$02     drvrDelay   Word      Ticks between periodic actions (for desk accessories/polling)
$04     drvrEMask   Word      Event mask for Desk Accessories
$06     drvrMenu    Word      Menu ID associated with a Desk Accessory
$08     drvrOpen    Word      Offset from header base to Open routine
$0A     drvrPrime   Word      Offset from header base to Prime (Read / Write) routine
$0C     drvrCtl     Word      Offset from header base to Control routine
$0E     drvrStatus  Word      Offset from header base to Status routine
$10     drvrClose   Word      Offset from header base to Close routine
$12     drvrName    Str255    Pascal string naming the driver (e.g., "\x05.Sony")
```

### Driver Capability Flags (`drvrFlags`)
- **Bit 15 (`$8000`) - `dRAMBased`**: `0` = Driver resides in ROM, `1` = Driver is a relocatable handle in RAM.
- **Bit 14 (`$4000`) - `dReadEnable`**: Driver accepts `_Read` requests.
- **Bit 13 (`$2000`) - `dWritEnable`**: Driver accepts `_Write` requests.
- **Bit 12 (`$1000`) - `dCtlEnable`**: Driver accepts `_Control` commands.
- **Bit 11 (`$0800`) - `dStatEnable`**: Driver accepts `_Status` queries.
- **Bit 10 (`$0400`) - `dNeedGoodBye`**: Driver wants notification before application heap re-initialization.
- **Bit 9 (`$0200`) - `dNeedTime`**: Driver requests periodic execution via the VBL or system task loop.
- **Bit 8 (`$0100`) - `dNeedLock`**: Driver must be locked in memory upon opening.

---

## 4. Device Control Entry (`DCtlEntry` / DCE)

For every open driver, the Device Manager allocates a 40-byte DCE in the System Heap:

```
Offset  Field         Type        Description
------  ------------  ----------  -------------------------------------------------------------
$00     dCtlDriver    Ptr/Handle  Pointer (ROM) or Handle (RAM) to driver code
$04     dCtlFlags     Word        Current operational flags (open, active, in-progress)
$06     dCtlQHdr      QHdr        I/O Request Queue Header (10 bytes: QFlags, QHead, QTail)
$10     dCtlPosition  LongInt     Current byte offset position for read/write operations
$14     dCtlStorage   Handle      Driver's private work storage handle
$18     dCtlRefNum    Word        Driver reference number (-1 to -128)
$1A     dCtlCurTicks  LongInt     System tick count at last periodic call
$1E     dCtlWindow    GrafPtr     Window pointer (if driver is a desk accessory)
$22     dCtlDelay     Word        Number of ticks between periodic calls
$24     dCtlEMask     Word        Desk accessory event mask
$26     dCtlMenu      Word        Desk accessory menu ID
```

---

## 5. Synchronous vs Asynchronous I/O Execution

The Device Manager supports non-blocking I/O operations through parameter blocks:

```
[ Application issues PBRead(A0=IOParamPtr) ]
                     |
                     v
[ Trap Dispatcher EMT1010 ]
  - Reads Trap Word Bit 10: 0 = Synchronous, 1 = Asynchronous
                     |
                     v
[ Device Manager: Enqueue I/O Request ]
  - Inserts IOParam block into driver's dCtlQHdr queue.
  - Driver currently busy?
         /                      \
   (Yes) /                        \ (No)
        v                          v
  Return to caller           [ Invoke Driver's drvrPrime Routine ]
  (Request waits in queue)                 |
                                           v
                             [ Hardware performs transfer (DMA / IRQ) ]
                                           |
                                           v
                             [ Driver invokes IODone ]
                               - Remove request from queue.
                               - Set ioResult in parameter block.
                               - Invoke ioCompletion callback if non-nil.
                               - If synchronous: wake sleeping application.
```

### Parameter Block Layout (`IOParam`)
- `qLink` (`$00`): Pointer to next queued I/O request.
- `qType` (`$04`): Queue type.
- `ioTrap` (`$06`): Trap word causing the operation.
- `ioCmdAddr` (`$08`): Address of driver routine.
- `ioCompletion` (`$0C`): Pointer to asynchronous completion callback procedure.
- `ioResult` (`$10`): Result code (`noErr`, `readErr`, `writErr`, `abortErr`).
- `ioNamePtr` (`$12`): Driver or volume name string pointer.
- `ioVRefNum` (`$16`): Volume or driver reference number.
- `ioRefNum` (`$18`): Driver reference number.
- `ioBuffer` (`$20`): Data buffer pointer.
- `ioReqCount` (`$24`): Requested byte transfer count.
- `ioActCount` (`$28`): Actual byte transfer count achieved.
- `ioPosMode` (`$2C`): Seek mode (`fsAtMark`, `fsFromStart`, `fsFromLEOF`).
- `ioPosOffset` (`$2E`): Seek offset.

---

## 6. Labeled Function Directory

Routines defined in `plus/os/device_mgr.s` and `se/os/device_mgr.s`:

- **`Open` / `_Open`** (`$A000`):
  - *Entry*: `A0` = Pointer to `IOParam` block containing driver name string (e.g. `".Sony"`).
  - *Exit*: `D0.W` = Result code, `ioRefNum` set.
  - *Operation*: Scans Unit Table for existing driver; if not open, allocates a new DCE, reads driver from ROM or loads `'DRVR'` resource from disk, locks it in memory, and jumps to the driver's `drvrOpen` entry point.
- **`Close` / `_Close`** (`$A001`):
  - *Entry*: `A0` = Parameter block with `ioRefNum`.
  - *Operation*: Calls driver's `drvrClose` routine, flushes pending I/O requests, and frees DCE.
- **`Read` / `_Read`** (`$A002`) & **`Write` / `_Write`** (`$A003`):
  - *Entry*: `A0` = Parameter block (`ioBuffer`, `ioReqCount`, `ioPosMode`).
  - *Operation*: Validates permissions via `dReadEnable` / `dWritEnable`, queues request, and branches to `drvrPrime`.
- **`Control` / `_Control`** (`$A004`):
  - *Entry*: `A0` = `CntrlParam` pointer (`csCode` and parameters).
  - *Operation*: Sends control codes to driver (e.g. disk eject `$0007`, format track, serial baud rate selection).
- **`Status` / `_Status`** (`$A005`):
  - *Entry*: `A0` = `CntrlParam` pointer.
  - *Operation*: Queries driver internal states (e.g. floppy disk in drive, characters pending in serial buffer).
- **`KillIO` / `_KillIO`** (`$A006`):
  - *Operation*: Halts current I/O operation and purges all queued requests with `abortErr` (`-27`).
- **`Fetch`** (Vector at `$08F4`):
  - *Entry*: `A1` = DCE pointer. *Exit*: `D0.B` = Next byte from active I/O buffer. Bit 15 set when buffer exhausted.
- **`Stash`**:
  - *Entry*: `A1` = DCE pointer, `D0.B` = Byte to write. Writes byte into active I/O buffer and increments count.
- **`IODone`**:
  - *Entry*: `A1` = DCE pointer, `D0.W` = Result code. Core Device Manager completion routine.


---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

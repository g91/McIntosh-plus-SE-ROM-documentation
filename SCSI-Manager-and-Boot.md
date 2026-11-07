# SCSI Manager & SCSI Boot Architecture

## 1. Overview of the Macintosh SCSI Architecture

The Macintosh Plus was the first personal computer to include an **ANSI X3.131-1986 Small Computer System Interface (SCSI)** bus as standard equipment. Managed by an **NCR 5380 Asynchronous SCSI Interface Controller**, the SCSI bus allowed high-speed communication (up to ~1.25 MB/s theoretical burst) with external hard disks, tape drives, scanners, and CD-ROM drives.

The SCSI subsystem consists of two key kernel layers:
1. **SCSI Manager (`plus/os/scsi_mgr.s` / `se/os/scsi_mgr.s`)**: Provides the software protocol engine, bus arbitration, phase management, and data transfer instruction interpreter.
2. **SCSI Boot Engine (`plus/os/scsi_boot.s` / `se/os/scsi_boot.s`)**: Probes SCSI target IDs at startup, detects bootable partitions, reads block 0, and mounts the startup volume.

---

## 2. NCR 5380 Controller Registers & Memory Map

The NCR 5380 registers are mapped into the 68000 physical address space starting at `$580000`:

```
Address     Register Name  Direction  Description
----------  -------------  ---------  -------------------------------------------------
$580000     scsiCurrent    Read       Current SCSI Data Bus status
$580000     scsiOutput     Write      Output Data Register
$580002     scsiInitiator  R/W        Initiator Command Register (Assert RST, BSY, SEL, ATN)
$580004     scsiTarget     R/W        Mode Register (Arbitration, DMA, Target/Initiator mode)
$580006     scsiTargetCmd  R/W        Target Command Register
$580008     scsiStatus     Read       Current SCSI Bus Status (Phase match, BSY, REQ, MSG, C/D, I/O)
$580008     scsiSelect     Write      Select Enable Register
$58000A     scsiBusStatus  Read       Bus and Status Register (DMA request, phase match, error)
$58000C     scsiInDma      Read       Input Data Register with DMA handshake
$58000E     scsiReset      Read       Reset Parity / Interrupts
```

### SCSI Bus Phases
The NCR 5380 hardware tracks the three SCSI phase lines driven by the target:
- `MSG` (Message), `C/D` (Control / Data), `I/O` (Input / Output):
  - `000`: Data Out phase
  - `001`: Data In phase
  - `010`: Command phase
  - `011`: Status phase
  - `110`: Message Out phase
  - `111`: Message In phase

---

## 3. SCSI Manager API & Traps

The SCSI Manager is accessed via trap `_SCSIAtomic` (`$A015`), using selector routines:

### 3.1 Bus Arbitration & Selection
- **`SCSIReset`**:
  - Asserts the SCSI `RST` bus line for at least 25 microseconds, resetting all connected targets.
- **`SCSIGet`**:
  - Arbitrates for control of the SCSI bus. Waits for Bus Free phase, asserts Initiator ID bit (Mac is always SCSI ID 7), and asserts `BSY`.
- **`SCSISelect`**:
  - *Input*: Target ID (0 to 6).
  - *Operation*: Asserts `SEL` line and target's ID bit on data bus. Waits for target to respond by asserting `BSY`.

### 3.2 Command Execution & Completion
- **`SCSICmd`**:
  - *Input*: Pointer to 6, 10, or 12-byte SCSI Command Descriptor Block (CDB), and length.
  - *Operation*: Waits for Command Phase, transfers CDB bytes to target.
- **`SCSIComplete`**:
  - *Output*: `D0` = Status byte returned by target, `D1` = Message byte (e.g. `COMMAND COMPLETE` $00).
  - Releases bus to Bus Free phase.

---

## 4. The Transfer Instruction Block (TIB) Engine

For high-speed bulk data transfers (`_SCSIRead` and `_SCSIWrite`), the SCSI Manager does not take a simple memory buffer pointer. Instead, it interprets a compiled program known as a **Transfer Instruction Block (TIB)**. A TIB is an array of 10-byte instruction records:

```
TIB Record Format (10 bytes):
+--------------------+--------------------+--------------------+
| Opcode (2 bytes)   | Address (4 bytes)  | Count (4 bytes)    |
+--------------------+--------------------+--------------------+
```

### TIB Opcodes
- **`scLoop` (`$0001`)**: Decrements `Count`. If non-zero, jumps to offset in `Address`.
- **`scMove` (`$0002`)**: Transfers `Count` bytes between the SCSI data register and the memory buffer at `Address`.
- **`scNop` (`$0003`)**: No operation (used for padding).
- **`scStop` (`$0004`)**: Terminates TIB execution.

This mini-bytecode engine allows applications and drivers to execute scatter-gather I/O directly in kernel space without multiple trap calls!

---

## 5. Polled vs Blind Transfers: Plus vs SE Hardware

### The Mac Plus Timing Limitation
On the Macintosh Plus, the NCR 5380 was connected without direct hardware DMA or wait-state handshake lines (`DRQ` was not tied to CPU wait).
- **Polled Transfers (`_SCSIRBlind` / `_SCSIWBlind`)**:
  - If the kernel polled the `scsiBusStatus` register before reading every single byte, transfer speeds dropped to an abysmal ~150 KB/s.
- **Blind Transfers**:
  - To achieve acceptable throughput (~260 KB/s), Apple engineers wrote unrolled 68000 assembly loops that read consecutive bytes from the NCR 5380 data register every few clock cycles *without checking whether the drive was ready*.
  - If a hard drive paused momentarily to perform head settling or track buffering, the Mac Plus read corrupted data or caused a CPU bus timeout.

### The Mac Plus v3 ROM SCSI Patch (`extra.s`)
In early 1986, third-party hard drives frequently failed during boot on Mac Plus v1 and v2 ROMs. Apple released **Mac Plus ROM v3** (`$4D1F8172`), inserting a 32-byte emergency patch at the very end of the 128 KB ROM (`extra/extra.s` at offset `0x01FFC0`):
- Patches the SCSI handshake timing loop.
- Intercepts SCSI boot calls to introduce a small, calibrated delay between SCSI selections, allowing slow-spinning drives to achieve sync.

### The Mac SE Hardware Handshake Solution
On the Macintosh SE, Apple rectified the hardware deficiency:
- The logic board connects the NCR 5380 `DRQ` output pin directly to the 68000 bus timing and PAL circuitry.
- When the 68000 executes an instruction accessing `scsiInDma` (`$58000C`), the CPU clock automatically inserts hardware wait states until the NCR 5380 asserts `DRQ`.
- The SE achieves hardware pseudo-DMA speeds of **~650 KB/s to 1 MB/s** with zero risk of buffer underflow or corrupted bytes.

---

## 6. The SCSI Boot Sequence (`scsi_boot.s`)

During startup, if no boot floppy is inserted, the kernel activates `scsi_boot.s`:
1. Resets the SCSI bus via `SCSIReset`.
2. Iterates from Target ID 6 down to Target ID 0 (ID 7 is the Mac itself).
3. For each ID:
   - Issues `TEST UNIT READY` ($00).
   - If target responds, issues `READ` ($08) for Logical Block 0.
4. Inspects Block 0:
   - Checks for the classic Apple Partition Map signature (`$4552` = 'ER' / Driver Descriptor Record).
   - Reads the partition table to locate an Apple_HFS boot partition.
   - Loads the partition's physical SCSI device driver into the System Heap.
   - Installs the SCSI driver into the Device Manager's Unit Table.
   - Transfers control to the driver's `Open` routine to mount the root volume.


---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

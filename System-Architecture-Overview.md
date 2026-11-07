# Macintosh Plus & SE ROM Kernel: System Architecture

## 1. Overview of the Classic Macintosh ROM

The classic Macintosh operating system and user interface runtime are fundamentally anchored in Read-Only Memory (ROM). Unlike contemporary personal computers that relied on a minimal BIOS and loaded the entire operating system from disk, the Macintosh architecture integrated core components of the OS kernel, hardware drivers, memory management, file system, graphics engine (QuickDraw), and user interface toolkit (Toolbox) directly onto ROM silicon.

This wiki documents the reverse-engineered, bit-identical assembly source trees for:
- **Macintosh Plus (1986)**: 128 KB ROM (Targets: v1 `$4D1EEEE1`, v2 `$4D1EEAE1`, v3 `$4D1F8172`).
- **Macintosh SE (1987)**: 256 KB ROM (Target: `$B2E362A8`).
- **Macintosh SE FDHD / SuperDrive (1989)**: 256 KB ROM (Target: `$B306E171`).

The ROM acts as both the **operating system kernel** and the **application runtime framework**. When an application makes an OS or Toolbox call, it executes an illegal Motorola 68000 instruction starting with `$A` (an **A-line trap**), which is caught by the 68000 exception hardware and dispatched by the ROM kernel.

---

## 2. 68000 CPU Execution Model & Address Space

The Motorola 68000 microprocessor features a 32-bit internal architecture with a 24-bit external physical address bus, providing a flat physical address space of **16 Megabytes ($000000 to $FFFFFF)**.

```
+-----------------------------------+ $FFFFFF
| VIA (6522 Versatile Interface)    | $EFE1FE - $EFFFFE (Mirrored)
+-----------------------------------+ $DFE100
| IWM / SWIM (Floppy Controller)    | $DFE1FF / $C00000 - $DFFFFF
+-----------------------------------+ $9FFFFF
| SCC (8530 Serial Controller - Rd) | $900000 - $9FFFFF
+-----------------------------------+ $8FFFFF
| SCC (8530 Serial Controller - Wr) | $800000 - $8FFFFF
+-----------------------------------+ $5FFFFF
| SCSI Controller (NCR 5380)        | $580000 - $5FFFFF (Mac Plus & SE)
+-----------------------------------+ $43FFFF
| ROM Space (128 KB or 256 KB)      | $400000 - $41FFFF (Plus) / $43FFFF (SE)
+-----------------------------------+ $3FFFFF
| Sound / Screen Buffer (Top RAM)   | (e.g. $3FA700 Screen, $3FFD00 Sound on 4MB)
| Application Heap                  | Dynamic growth upward
| Application Stack                 | Dynamic growth downward from ApplLimit
| System Heap                       | Allocated at base of RAM
| Low-Memory Globals & Vectors      | $000000 - $000FFF (Mac Plus) / $001FFF (SE)
+-----------------------------------+ $000000
```

### The 24-Bit Addressing Trap
Because only the lower 24 bits (A0-A23) are connected to address decoding hardware, the upper 8 bits (bits 24-31) of address registers were ignored by the CPU during memory cycles. The Macintosh system software exploited this by utilizing the top 8 bits of master pointer addresses as **handle state flags**:
- **Bit 31 (Bit 7 of high byte)**: Lock status (`1` = Locked, cannot be moved during heap compaction).
- **Bit 30 (Bit 6 of high byte)**: Purgeable status (`1` = Block can be purged under memory pressure).
- **Bit 29 (Bit 5 of high byte)**: Resource status (`1` = Owned by the Resource Manager).

This design decision made the Mac Plus and SE ROMs strictly **24-bit "dirty"**, requiring the `_StripAddress` trap in later 32-bit systems to mask out the upper byte before pointer dereferencing.

---

## 3. Physical Memory Map & Hardware Overlays

### Boot-Time ROM Overlay Mechanism
At power-on or physical reset, the 68000 CPU reads the initial Supervisor Stack Pointer (`SSP`) from address `$000000` and the initial Program Counter (`PC`) from address `$000004`. Because RAM contents are uninitialized at power-on, the hardware employs a **ROM Overlay circuit** driven by VIA Port A, bit 4 (`vOverlay`):
1. **Overlay Asserted (Active)**: Address decoding maps the ROM chip to `$000000`. The 68000 reads its reset vectors directly from the start of the ROM (`vectors.s`).
2. **First Instruction Execution**: The reset PC directs execution into the true ROM address space at `$40002A` (`RESETENTRY` / `EBootStart`).
3. **De-asserting Overlay**: Once execution is safely occurring at `$400000+`, the boot routine clears VIA Port A bit 4. Address `$000000` reverts to physical RAM, allowing the kernel to initialize low-memory interrupt vectors and system globals.

### Screen & Sound Buffer Allocation
The classic Macintosh video display is a 1-bit monochrome bitmap of 512 x 342 pixels (21,888 bytes, padded to 32,768 bytes). The video and sound hardware continuously read scanlines directly from RAM via dedicated DMA cycles interleaved with 68000 bus cycles:
- **Main Screen Buffer**: Placed in top RAM (e.g., `$01A700` on 128K, `$07A700` on 512K, `$3FA700` on 4MB).
- **Alternate Screen Buffer**: Preceding the main buffer (used for page flipping in animation).
- **Main Sound Buffer**: Located at `$3FFD00` (on 4MB), fetched by sound hardware during horizontal blanking intervals.

---

## 4. Kernel Subsystems Architecture

The ROM is logically organized into distinct functional domains:

```
+---------------------------------------------------------------+
|                      Application Space                        |
+---------------------------------------------------------------+
|         Toolbox: Windows, Menus, Dialogs, Controls, TE        |
+---------------------------------------------------------------+
|            QuickDraw Graphics Engine & Font Manager           |
+---------------------------------------------------------------+
|                      Resource Manager                         |
+---------------------------------------------------------------+
|  Operating System Kernel:                                     |
|  - A-Line Trap Dispatcher (EMT1010)                           |
|  - Memory Manager (Heap Zones, Relocatable Handles)           |
|  - Device Manager & I/O Subsystem (Unit Table, DCE)           |
|  - File Manager (Hierarchical File System - HFS)              |
|  - SCSI Manager (NCR 5380 Protocol Engine)                    |
|  - ADB Manager (Mac SE Apple Desktop Bus Controller)          |
|  - Event Manager & VBL Queue Dispatcher                       |
|  - Segment Loader (CODE 0, Launch, Chain, Jump Table)         |
+---------------------------------------------------------------+
|  Hardware Drivers & Exception Vectors:                        |
|  - VIA 6522, SCC 8530 (LocalTalk/Serial), IWM/SWIM Floppy     |
|  - Level 1-7 Interrupt Autovectors, RTC/PRAM Interface       |
+---------------------------------------------------------------+
```

### Key Low-Memory Kernel Structures
The first 4 KB (Plus) to 8 KB (SE) of RAM are dedicated to low-memory system variables:
- `$0000 - $00FF`: 68000 Exception Vectors (Bus Error, Address Error, Traps, IRQs).
- `$0100 - $01FF`: Memory sizing, display pointers (`MemTop`, `BufPtr`, `HeapEnd`, `ScrnBase`).
- `$0200 - $03FF`: System event queue, VBL task queue, Real-Time Clock, Sound parameters.
- `$0400 - $07FF`: **OS Trap Dispatch Table** (256 longwords, one per `$A0xx` trap).
- `$0C00 - $13FF` (Plus) / `$0E00 - $15FF` (SE): **Toolbox Trap Dispatch Table** (512 longwords, `$A8xx - $A9xx`).
- `$0300 - $03FF`: File system volume and drive queues (`DrvQEl`, `VCB` heads).

---

## 5. Navigating This Wiki

This wiki provides comprehensive documentation on every kernel module, hardware driver, memory structure, and function label in the Mac Plus and SE ROMs:
- **[01. Mac Plus vs Mac SE Evolution](Mac-Plus-vs-Mac-SE-Evolution)**: Hardware and architectural changes between 128KB and 256KB ROMs.
- **[02. Boot Sequence & Diagnostics](Boot-Sequence-and-Diagnostics)**: Hardware reset, March RAM tests, and boot block execution.
- **[03. Trap Dispatcher](Trap-Dispatcher-EMT1010)**: EMT1010 Line 1010 exception dispatcher, auto-pop mechanism, and trap tables.
- **[04. Memory Manager](Memory-Manager-and-Heap)**: Heap zone structures, handle compaction, and block headers.
- **[05. Device Manager](Device-Manager-and-IO)**: Unit table, DCE records, and asynchronous I/O execution.
- **[06. File Manager (HFS)](File-Manager-HFS)**: Catalog B-Trees, extents allocation, and block caching.
- **[07. SCSI Manager & Boot](SCSI-Manager-and-Boot)**: NCR 5380 transfer engine and SCSI boot protocol.
- **[08. Apple Desktop Bus (ADB)](Apple-Desktop-Bus-ADB)**: Mac SE transceiver state machine and device enumeration.
- **[09. Interrupts & Hardware](Interrupts-and-Hardware)**: VIA, SCC, IWM, and exception autovectors.
- **[10. Event, VBL & Time Managers](Event-VBL-and-Time-Managers)**: 60Hz timing, tasks, and system events.
- **[11. Segment Loader & Runtime](Segment-Loader-and-Runtime)**: Application launching, jump table, and A5 world.
- **[12. System Error & Debugger](System-Errors-and-MacsBug)**: DSAlert bomb box and resident MicroBug debugger.
- **[13. ROM Resources & Drivers](ROM-Resources-and-Drivers)**: Built-in `.Sony`, `.Sound`, `.MPP`, and packages.
- **[14. Toolbox & QuickDraw](Toolbox-and-QuickDraw)**: QuickDraw graphics geometry, fonts, and window management.
- **[15. Low-Memory Globals Reference](Low-Memory-Globals-Reference)**: Complete address directory of system globals.
- **[16. Trap Reference Catalog](Trap-Reference-Catalog)**: Complete list of all 287+ A-line traps with hex codes and parameters.


---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

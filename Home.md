# Classic Macintosh Plus & SE ROM Kernel Wiki

Welcome to the definitive technical Wiki for the **Macintosh Plus (128 KB)** and **Macintosh SE / SE FDHD (256 KB)** ROM source trees, reverse-engineered and reconstructed from Apple's original MPW link maps and assembly source code.

> [!NOTE]
> This repository contains bit-identical assembly source code for seven classic Macintosh ROMs. This Wiki catalogs the operating system kernel, hardware drivers, memory architecture, trap dispatcher, and Toolbox.

---

## Quick Navigation

```
+-------------------------------------------------------------------------------+
|                             Macintosh ROM Kernel                              |
+-------------------------------------------------------------------------------+
|  Architecture & Boot      |  Memory & I/O              |  Storage & Drivers   |
|  - System Architecture    |  - Memory Manager & Heap   |  - File Manager HFS  |
|  - Plus vs SE Evolution   |  - Device Manager & I/O    |  - SCSI Manager      |
|  - Boot & Diagnostics     |  - Trap Dispatcher         |  - ADB Subsystem     |
+---------------------------+----------------------------+----------------------+
|  Runtime & UI Framework   |  Hardware & Low-Level      |  Reference Catalogs  |
|  - QuickDraw & Toolbox    |  - Interrupts & Autovectors|  - 287 A-Line Traps  |
|  - Segment Loader / A5    |  - VIA 6522, SCC, IWM/SWIM |  - 415 Low-Memory    |
|  - Event, VBL & Time Mgr  |  - Sound & Video DMA       |  - 10,963 Functions  |
+-------------------------------------------------------------------------------+
```

### 1. Architectural Foundations
- **[System Architecture Overview](System-Architecture-Overview)**: 68000 CPU memory map, 24-bit physical addressing, ROM overlay circuit, screen and sound DMA buffers.
- **[Mac Plus vs Mac SE Evolution](Mac-Plus-vs-Mac-SE-Evolution)**: Hardware comparison (ADB vs serial, SCSI handshake, SWIM 1.44M floppy controller), ROM expansion from 128 KB to 256 KB, and hidden team photo Easter eggs.
- **[Boot Sequence & Diagnostics](Boot-Sequence-and-Diagnostics)**: Reset vector (`$40002A`), March memory pattern testing, PRAM validation, VIA/SCC/IWM initialization, `BootBeep` audio synthesis, boot block loading, and Sad Mac diagnostics.
- **[Trap Dispatcher & EMT1010](Trap-Dispatcher-EMT1010)**: Line 1010 Emulator opcode bit layout, 68020+ stack fixup, `_GetTrapAddress` / `_SetTrapAddress`, and RAM patch mechanics.

### 2. Core Kernel Subsystems
- **[Memory Manager & Heap Zones](Memory-Manager-and-Heap)**: Zone records, 24-bit block headers, relocatable handles, master pointer flags (lock, purge, resource), compaction algorithms, and memory traps.
- **[Device Manager & I/O Subsystem](Device-Manager-and-IO)**: Unit Table (128 slots), DCE (Device Control Entry) structure, driver capability flags, synchronous and asynchronous I/O execution, and `IOParam` blocks.
- **[File Manager & HFS Architecture](File-Manager-HFS)**: Volume Control Blocks (VCB), File Control Blocks (FCB), Catalog Manager (CatKey, CNode records), extents allocation bitmap, and LRU block caching.
- **[HFS B*-Tree & Catalog Internals](HFS-BTree-and-Catalog-Internals)**: Deep dive into 512-byte node layouts, record offsets array, node splitting, tree balancing, and Catalog records.

### 3. Hardware Controllers & Bus Drivers
- **[SCSI Manager & SCSI Boot](SCSI-Manager-and-Boot)**: NCR 5380 controller registers, Transfer Instruction Block (TIB) bytecode interpreter, polled vs blind transfers, Mac Plus timing quirks and Plus v3 SCSI patch (`extra.s`).
- **[Apple Desktop Bus (ADB)](Apple-Desktop-Bus-ADB)**: Mac SE ADB transceiver architecture, PIC microcontroller state machine via VIA Port B (ST0/ST1) and shift register, Talk/Listen/SendReset/Flush commands, and collision detection.
- **[Interrupts & Hardware Subsystems](Interrupts-and-Hardware)**: 68000 exception autovectors (Levels 1-7), Synertek 6522 VIA registers and timers, Zilog 8530 SCC serial & LocalTalk DPLL, IWM/SWIM floppy controllers, and RTC/PRAM.
- **[Floppy Disk Driver & Controller Internals](Floppy-Disk-Driver-Internals)**: Detailed guide to `.Sony` driver, GCR 6-and-2 encoding/decoding, Zoned Constant Angular Velocity (ZCAV), PWM motor speed control, and SWIM SuperDrive mode switches.
- **[ROM Resources & Built-in Drivers](ROM-Resources-and-Drivers)**: ROM resource map architecture, `.Sony`, `.Sound`, `.Print`, AppleTalk (`.MPP`, `.ATP`, `.XPP`), SANE IEEE-754 (Pack 4), Transcendental Math (Pack 5), and standard definition procedures.

### 4. Application Runtime & Graphics
- **[Events, VBL & Time Managers](Event-VBL-and-Time-Managers)**: Circular system event queue, 60 Hz vertical blanking (VBL) queue, mouse tracking, and microsecond-accuracy Time Manager tasks.
- **[Segment Loader & Runtime](Segment-Loader-and-Runtime)**: `CODE` 0 Jump Table, unloaded-to-loaded transition, `_LoadSeg` / `_UnloadSeg`, application launching (`_Launch`), and the Application `A5` World layout.
- **[System Errors & MacsBug](System-Errors-and-MacsBug)**: DSAlert Bomb Box, raw frame buffer rendering without QuickDraw or heaps, fatal error IDs, and the resident MicroBug / MacsBug debugger.
- **[Toolbox & QuickDraw](Toolbox-and-QuickDraw)**: QuickDraw 2D vector/raster graphics engine, GrafPort, BitBlt 8 transfer modes, region inversion lists, shapes, Window Manager, Menu Manager, Control Manager, and TextEdit.

---

## Complete Reference Catalogs

| Catalog | Items | Description |
| :--- | :--- | :--- |
| **[A-Line Trap Catalog](Trap-Reference-Catalog)** | **287 Traps** | Complete reference of all OS ($A0xx) and Toolbox ($A8xx) A-line traps with hex codes, register conventions, and availability. |
| **[Low-Memory Globals](Low-Memory-Globals-Reference)** | **415 Globals** | Physical memory address directory of all system variables ($0000 - $1FFF) with Mac SE relocation details. |
| **[Hardware Registers Map](Hardware-Registers-Reference)** | **74 Registers** | Register addresses for Synertek 6522 VIA, Zilog 8530 SCC, NCR 5380 SCSI, and Floppy Disk controllers. |

---

## Subsystem Function Catalogs (10,963 Functions)

Every routine and label in the ROM source tree is indexed with ROM offsets, file locations, prototypes, and register calling conventions:

- **[OS Kernel Functions](Functions-OS-Kernel)** (3,043 routines)
- **[ROM Resources & Drivers Functions](Functions-ROM-Resources-and-Drivers)** (2,777 routines)
- **[Toolbox Functions](Functions-Toolbox)** (2,657 routines)
- **[QuickDraw Functions](Functions-QuickDraw)** (1,497 routines)
- **[Boot & Diagnostics Functions](Functions-Boot-and-Diagnostics)** (721 routines)
- **[Debugger Functions](Functions-Debugger)** (145 routines)
- **[Hardware & Interrupts Functions](Functions-Hardware-and-Interrupts)** (56 routines)
- **[Extra & Patches Functions](Functions-Extra-and-Patches)** (67 routines)

---

## Local Interactive Python Server

You can also run the full interactive Wiki locally with live search and dynamic symbol inspection:
```bash
python wiki.py
# or
python wiki.py serve --port 8080
```
Command-line search and inspection:
```bash
python wiki.py search NewPtr
python wiki.py symbol NewPtr
python wiki.py symbol INITADB
```

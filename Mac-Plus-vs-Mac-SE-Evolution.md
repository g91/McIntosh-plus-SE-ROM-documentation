# Mac Plus vs Mac SE: Architectural Evolution

## 1. Executive Summary

Between the release of the **Macintosh Plus** (January 1986) and the **Macintosh SE** (March 1987), Apple underwent a major overhaul of both the hardware design and ROM firmware. While the Mac Plus introduced double-density 800K floppy drives, SCSI support, and HFS in a 128 KB ROM, the Mac SE doubled the ROM capacity to **256 KB**, added the **Apple Desktop Bus (ADB)**, expanded the hardware SCSI interface with hardware handshaking, restructured the low-memory layout, and added built-in system resources directly into ROM.

In 1989, the **Macintosh SE FDHD** (later named SE/30 era sibling "Macintosh SE SuperDrive") updated the SE ROM with the **SWIM (Super Woz Integrated Machine)** controller, adding support for 1.44 MB high-density MFM floppy disks.

---

## 2. Comparative Specification Matrix

| Feature / Subsystem | Macintosh Plus (1986) | Macintosh SE (1987) | Macintosh SE FDHD (1989) |
| :--- | :--- | :--- | :--- |
| **ROM Size** | 128 KB ($20000 bytes) | 256 KB ($40000 bytes) | 256 KB ($40000 bytes) |
| **ROM Checksum** | `$4D1F8172` (v3) | `$B2E362A8` | `$B306E171` |
| **ROM Chips** | 2 x 64 KB EPROMs | 2 x 128 KB ROMs (High/Low byte) | 2 x 128 KB ROMs |
| **Reset PC** | `$40002A` | `$40002A` | `$40002A` |
| **Keyboard / Mouse** | Dedicated serial (VIA shift reg / interrupts) | Apple Desktop Bus (ADB) | Apple Desktop Bus (ADB) |
| **SCSI Interface** | NCR 5380 (Polled / Software loop) | NCR 5380 (Hardware handshake pseudo-DMA) | NCR 5380 (Hardware handshake pseudo-DMA) |
| **Floppy Controller** | IWM (Integrated Woz Machine - GCR 800K) | IWM (GCR 800K) | SWIM (Super Woz Integrated Machine - MFM 1.44M) |
| **Expansion Slot** | None | Processor Direct Slot (SE-PDS, 96-pin) | Processor Direct Slot (SE-PDS, 96-pin) |
| **Toolbox Dispatch Table** | `$0C00` (512 entries) | `$0E00` (512-1024 entries) | `$0E00` (512-1024 entries) |
| **OS Dispatch Table** | `$0400` (256 entries) | `$0400` (256 entries) | `$0400` (256 entries) |
| **Low-Memory Size** | 2.5 KB - 3 KB ($0000 - $0BFF) | Expanded up to `$1FFF` | Expanded up to `$1FFF` |
| **Internal Drives** | 1 internal 800K | Up to 2 internal drives (2x floppy or 1x floppy + 1x SCSI HD) | 2x FDHD or 1x FDHD + 1x SCSI HD |
| **B-Tree HFS Buffers** | Dynamic in heap | Enhanced caching in ROM | Enhanced caching in ROM |
| **Built-in Resources** | WDEF 0, MDEF 0, Pack 4,5,7, Chicago | CDEF 0,1, MBDF 0, WDEF 0,1, Fonts, Photos | CDEF 0,1, MBDF 0, WDEF 0,1, Fonts, Photos |

---

## 3. Hardware Differences and Their Impact on ROM

### 3.1 Apple Desktop Bus (ADB) Architecture
On the Macintosh Plus, the keyboard and mouse used separate physical connectors and distinct communication channels:
- Mouse: Quadrature signals wired directly to VIA port B and SCC handshake pins; mouse interrupts processed directly.
- Keyboard: 2-wire synchronous serial protocol driven through the VIA shift register (`VIA_SR` at `$EFF5FE`) and interrupt line.

On the Macintosh SE, Apple introduced **ADB**, a single-wire, multi-device multidrop serial bus managed by an 8-bit PIC1657 microcontroller:
- The 68000 communicates with the ADB microcontroller through VIA Port B (bits 4 and 5: state lines `ST0`, `ST1`) and the VIA Shift Register.
- A dedicated kernel module, `se/os/adb_mgr.s`, implements the transaction state machine, device scanning (polling all 16 ADB addresses), collision detection, and handler dispatching.
- Mouse and keyboard drivers in the SE are ADB handler procedures rather than dedicated interrupt loops.

### 3.2 SCSI Controller Improvements
The Mac Plus was the first Macintosh to include a SCSI port (NCR 5380 asynchronous SCSI controller). However, due to hardware design constraints:
- The Mac Plus lacked hardware handshaking lines connecting the 5380 `DRQ` (Data Request) signal to the CPU wait-state generator.
- Consequently, Mac Plus SCSI transfers required a tightly timed unrolled 68000 instruction loop (the "blind transfer" loop). If the drive could not keep up, bus errors or corrupted data occurred.
- In the Mac Plus v3 ROM (`rom_plus_v3.lst`), Apple added an emergency SCSI patch in `extra.s` (`0x01FFC0`) called by absolute address to work around SCSI drive timing bugs.
- In the Mac SE, the logic board hardware properly connects the NCR 5380 `DRQ` to the 68000 bus grant / wait generation logic. The SE ROM (`se/os/scsi_mgr.s`) takes full advantage of hardware handshaking, achieving transfer rates of ~650 KB/s compared to the Plus's ~260 KB/s.

### 3.3 IWM vs SWIM Floppy Controller
- **Mac Plus & Mac SE**: Use the **Integrated Woz Machine (IWM)** custom chip. The IWM only supports **GCR (Group Code Recording)** format, restricting floppy disk capacity to 400 KB (single-sided) and 800 KB (double-sided).
- **Mac SE FDHD**: Replaces the IWM with the **Super Woz Integrated Machine (SWIM)**. The SWIM can operate in two modes:
  1. *ISM Mode (IWM emulation)*: For reading/writing standard 400K/800K GCR disks.
  2. *SWIM Mode*: Enables **MFM (Modified Frequency Modulation)** encoding, supporting industry-standard 1.44 MB High Density (HD) floppies and MS-DOS / PC disks.
- In the SE FDHD ROM source tree, `res_drvr_sony_fdhd.s` replaces `res_drvr_sony.s` with a 339 KB driver assembly file incorporating the complete SWIM mode switching and MFM phase-locked loop tracking algorithms.

---

## 4. ROM Organization & Source Tree Differences

### 4.1 Master Include Comparison (`rom_plus.s` vs `rom_se.s`)
The entry point structure illustrates the modules added in the SE:

```
Mac Plus (rom_plus.s - 128 KB):
- boot/vectors.s
- boot/boot_install.s
- boot/boot_load.s
- boot/memtest.s
- boot/sad_mac.s
- debugger/debugger.s, microbug.s
- os/queue.s, sys_error.s
- hw/interrupts.s, rtc.s
- os/trap_dispatch.s, device_mgr.s
- os/keyboard.s                 <-- Classic serial keyboard driver
- os/file_mgr_* (8 modules)
- os/scsi_boot.s, scsi_mgr.s
- toolbox/quickdraw/* (28 modules)
- toolbox/font_mgr.s, resource_mgr.s, window_mgr.s, menu_mgr.s, control_mgr.s, dialog_mgr.s, textedit.s
- resources/res_drvr_sony.s     <-- IWM 800K driver only
- resources/res_pack_4, 5, 7
- extra/extra.s                 <-- Plus v3 SCSI patch ($1FFC0)

Mac SE (rom_se.s - 256 KB):
- boot/boot_search.s            <-- NEW: Multi-drive boot selection engine
- os/adb_mgr.s                  <-- NEW: Replaces os/keyboard.s with full ADB stack
- toolbox/print_glue.s          <-- NEW: Integrated printing glue
- resources/res_drvr_xpp.s      <-- NEW: AppleTalk Extended Protocol Package (.XPP)
- resources/res_cdef_0, 1.s     <-- NEW: Control definition procedures in ROM
- resources/res_mbdf.s          <-- NEW: Menu bar definition procedure in ROM
- resources/res_wdef_0, 1.s     <-- NEW: Window definition procedures in ROM
- resources/res_kchr.s, kmap.s  <-- NEW: International keyboard mapping in ROM
- resources/res_font_geneva.s   <-- NEW: Geneva font included in ROM
- resources/res_font_monaco.s   <-- NEW: Monaco font included in ROM
- resources/res_drvr_sony_fdhd.s<-- FDHD variant: SWIM 1.44M floppy driver
- resources/res_tcsl.s, res_bbmc.s <-- Easter Egg: Compressed Mac SE design team photos!
```

---

## 5. Low-Memory Relocations & New Symbols

In the Mac Plus, low-memory globals were tightly packed. The Toolbox trap table was located at `$0C00` (`ToolDispTable`).
In the Mac SE, with the inclusion of ADB, additional file system buffers, and expanded hardware tables, the memory layout was expanded:

1. **Toolbox Dispatch Table Shift**:
   - Mac Plus: `ToolDispTable` = `$0C00` - `$13FF` (512 entries).
   - Mac SE: `ToolDispTable` was relocated to **`$0E00` - `$15FF`**. Address `$0C00` was repurposed for ADB and AppleTalk communications buffers (`ADBBase` at `$0CF8`).
2. **New Low-Memory Globals in SE (`lowmem_se.inc`)**:
   - `ADBBase` (`$0CF8`): Base pointer to ADB manager globals and device table.
   - `JKybdTask` (`$021A`): Jump vector for the keyboard VBL polling routine.
   - `KbdType` (`$021E`): Detected keyboard hardware model byte.
   - `KeyRepThresh` (`$0214`) / `KeyThresh` (`$0216`): ADB keyboard repeat timings.
   - `FMSwitch` (`$0DE4`): Fast font-scaling switch.
   - `DTQueueHdr` (`$0D90`): Deferred Task Manager queue header.

---

## 6. The Easter Eggs: Mac SE Team Photos

The Mac SE 256 KB ROM includes two hidden compressed image resources:
- `res_tcsl.s` (`'tcsl'` resource 1): Contains the stylized typography and logo.
- `res_bbmc.s` (`'bbmc'` resource 1): Contains a high-resolution digitized group photograph of the Apple Mac SE engineering and design team (including Burrell Smith, Brian Berkeley, and others).

In the debugger or via memory poke, triggering the secret routine jumps to `res_bbmc.s`, which decodes the image using QuickDraw's `_UnpackBits` and displays the team on the built-in monitor!


---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

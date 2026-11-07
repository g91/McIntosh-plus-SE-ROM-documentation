# Boot Sequence & Diagnostics Subsystem

## 1. Overview of the Boot Pipeline

The boot process of the Macintosh Plus and Macintosh SE transitions the machine from uninitialized raw hardware into an interactive desktop environment. Because the early Macintosh hardware lacked a separate BIOS chip, the ROM itself performs power-on self-tests (POST), sizing and pattern testing of DRAM, hardware controller configuration (VIA, SCC, IWM, SCSI, RTC), audio chime synthesis, boot disk discovery, reading volume boot blocks (blocks 0 and 1), and launching the `System` file and `Finder`.

```
[ Power On / Hardware Reset ]
           |
           v
[ 68000 Reset Vector ] ---> Reads SSP ($000000) & PC ($000004) from ROM via Overlay
           |
           v
[ vectors.s: RESETENTRY ] ($40002A)
           |
           +--> Test Mode Switch Check (Diag mode vs Normal boot)
           |
           v
[ memtest.s: Memory Sizing & Diagnostics ]
           |
           +--> Sizing RAM: 128K, 512K, 1MB, 2MB, 2.5MB, 4MB
           +--> March Pattern Test & Bit-Fade Test
           +--> [Failure?] ---> [ sad_mac.s: CritErr / SADMAC_DRAW_CODE ]
           |
           v
[ boot_install.s: Hardware Initialization ]
           |
           +--> De-assert ROM Overlay (VIA Port A bit 4 = 0)
           +--> Initialize Synertek 6522 VIA (Timers, I/O directions)
           +--> Initialize Zilog 8530 SCC (Serial & LocalTalk timing)
           +--> Read & Validate Real-Time Clock (RTC) / PRAM
           +--> Generate Startup Chime (BootBeep via sound hardware)
           +--> Clear Video RAM & Set up Screen Display
           |
           v
[ Setup Heaps & Low-Memory Tables ]
           |
           +--> Initialize Exception Vectors ($0000 - $00FF)
           +--> Populate OS & Toolbox Trap Dispatch Tables ($0400 / $0C00 or $0E00)
           +--> InitZone: System Heap Zone & Application Heap Zone
           |
           v
[ boot_search.s / boot_load.s: Drive Polling & Boot Loader ]
           |
           +--> Poll Internal / External Floppy Drives (.Sony)
           +--> Poll SCSI Bus IDs (0 through 6)
           +--> Read Boot Blocks (Block 0 & 1 of boot volume)
           +--> Mount Boot Volume via HFS / MFS
           +--> Load 'boot' Resource or Execute Boot Code
           +--> Launch "System" file -> Load Finder
```

---

## 2. Reset Vectors and Initial Execution (`vectors.s`)

### Entry Point
At address `$400000`, the ROM defines the initial vectors:
- `$400000`: `BASEOFROM` - Initial Supervisor Stack Pointer (SSP) target.
- `$400004`: `STARTPC` - Initial Program Counter (`0x0040002A`).
- `$400008`: `ROMVERSION` - Word identifying the ROM version:
  - Mac Plus: `$0075`
  - Mac SE: `$0076`
- `$40002A`: `RESETENTRY` / `EBootStart` - First executable instruction.

```assembly
RESETENTRY:
        MOVE    #0x2700,SR              | Disable all interrupts (IPL 7)
        LEA.L   (0x00400000).L,A0       | Point A0 to base of ROM
        MOVEA.L A0,A6                   | A6 = ROM base reference register
        BRA.W   STARTBOOT               | Branch to startup sequence
```

### Warm Start vs Cold Start Detection
The kernel inspects low-memory location `WarmStart` (`$02A6`):
- If `WarmStart` contains the magic longword `$5A4F656C` ('ZOel') and the RAM checksum passes, the kernel preserves the current RAM contents and performs a soft reset (skipping destructive memory testing).
- Otherwise, it initiates a **Cold Start**, clearing memory and running full hardware self-tests.

---

## 3. Memory Sizing & March Testing (`memtest.s`)

Before dynamic memory allocation can begin, the kernel must determine how much RAM is physically installed on the logic board (from 128 KB up to 4 MB).

### Sizing Algorithm
The memory sizer writes test patterns to power-of-two address boundaries (`$020000`, `$040000`, `$080000`, `$100000`, `$200000`, `$400000`) and tests for address wrap-around:
- Because the 68000 address bus floating lines or open address lines mirror memory when unpopulated, writing a pattern to `$200000` on a 1MB machine alters the value at `$000000`.
- Once the boundary wraps, the maximum valid address is established and stored in `MemTop` (`$0108`).

### March Memory Test
If cold booting, the kernel runs a rigorous test on all data lines:
1. **Zero Fill**: Writes `$00000000` to all memory locations.
2. **Walking Ones Test**: Writes `$55555555`, `$AAAAAAAA`, `$FFFFFFFF` to verify that adjacent bits in RAM chips do not short-circuit.
3. **Address Line Test**: Writes the memory address itself as the data pattern at that address, then reads it back to ensure row and column address strobes (RAS/CAS) are functioning correctly.
4. **Bit-Fade Delay**: Pauses briefly to verify that dynamic RAM refresh cycles maintain charge across all memory cells.

---

## 4. Hardware Initialization (`boot_install.s`)

Once RAM is verified, the kernel configures the peripheral controllers:

### 4.1 VIA 6522 Configuration
- `VIA_DDRB` (`$EFE5FE`): Sets Port B data direction (RTC clock, serial data, mouse interrupt pins).
- `VIA_DDRA` (`$EFE7FE`): Sets Port A data direction.
- Port A bit 4 (`vOverlay`) is cleared, disabling the ROM overlay circuit so that physical RAM maps to `$000000`.
- VIA Timer 1 is configured to generate 60 Hz interrupt pulses for the VBL (Vertical Blanking) and cursor tracking subsystems.

### 4.2 Real-Time Clock & PRAM (`RTC_READ_PRAM_VOL`)
The Real-Time Clock (RTC) chip contains 20 bytes of battery-backed Parameter RAM (PRAM) on the Mac Plus, and 256 bytes on the Mac SE.
- The boot routine reads the PRAM bytes bit-by-bit through VIA Port B (`vRTCData`, `vRTCClk`, `vRTCEnb`).
- It verifies the PRAM validity bytes (`$A8` check pattern).
- If PRAM is corrupt (e.g., dead battery), it resets PRAM to factory defaults:
  - Default alarm time: 0.
  - Double-click time: 32 ticks (approx. 500 ms).
  - Key repeat rate: 6 ticks.
  - Startup volume: Level 3.
  - Boot device preference: Internal floppy / default SCSI ID.

### 4.3 Startup Audio Chime (`BootBeep`)
The classic Macintosh startup chime is synthesized entirely by software loop before the Sound Driver or interrupts are active!
- The routine `BootBeep` writes square wave or sine sample values into the sound buffer at the top of RAM (`$3FFD00`).
- It configures VIA Port A volume bits (bits 0-2) and toggles sound buffer enable (bit 3).
- The VIA Timer 1 is polled in a tight loop to modulate the pitch (approx. 440 Hz chord) for roughly 500 ms.

---

## 5. Boot Drive Discovery & Boot Blocks (`boot_search.s`, `boot_load.s`)

Once hardware is initialized, the system displays the "Happy Mac" or "Flashing Floppy" icon:

### Polling Sequence
1. **Floppy Drive Check**:
   - The `.Sony` driver polls the internal floppy drive (Drive 1).
   - If a 3.5" disk is inserted, the motor spins up, seeks to Track 0, and attempts to read Sectors 0 and 1.
2. **SCSI Bus Polling (Mac Plus & SE)**:
   - If no bootable floppy is found, the SCSI boot subsystem (`scsi_boot.s`) scans the SCSI bus starting from ID 6 down to ID 0.
   - For each SCSI ID, it executes `_SCSIGet`, `_SCSISelect`, and sends a `TEST UNIT READY` command ($00).
   - When a drive responds, it executes a `READ` command for Logical Block 0.

### Boot Blocks (Sectors 0 & 1)
Every bootable Macintosh volume contains a 1024-byte header across blocks 0 and 1:
- `bbID` (`$00`): Signature word (`$4C4B` = 'LK').
- `bbEntry` (`$02`): Offset to boot code execution entry point.
- `bbVersion` (`$06`): Boot block version.
- `bbPageFlags` (`$08`): Video and sound buffer flags.
- `bbSysName` (`$0A`): Pascal string naming the System file (default: `"System"`).
- `bbShellName` (`$1A`): Pascal string naming the shell (default: `"Finder"`).
- `bbDbg1Name`, `bbDbg2Name`: Names of low-level debuggers (e.g. `"MacsBug"`).

The boot loader loads the `System` file into the System Heap, reads the initial `boot` resource (ID 1), initializes the trap dispatcher, and transfers execution to the Finder.

---

## 6. Fatal Diagnostics & The Sad Mac (`sad_mac.s`)

If any fatal hardware or memory fault occurs before the OS is running, the kernel calls `CritErr` (`vectors.s:274`).

```assembly
CritErr:
        MOVEM.L D0-D7/A0-A7,(0x003FFC80).L      | Save all registers into SERegs
        MOVE.W  #0x2700,SR                      | Mask all interrupts
        BSR.W   SADMAC_SCRN_READY               | Clear display and draw Sad Mac icon
        BSR.W   SADMAC_DRAW_CODE                | Render hex error codes on screen
DEAD_MAC_BLINK:
        BSR.W   DEAD_MAC_CHIME                  | Play minor-chord death chime
        BRA.S   DEAD_MAC_BLINK                  | Loop indefinitely
```

### Hex Error Code Rendering Without QuickDraw
Because QuickDraw and font tables may not be loaded or RAM may be damaged, `sad_mac.s` contains its own raw 8x8 bitmap font table (`DT_HEX_FONT`):
- It directly calculates pixel offsets into the screen frame buffer at `$3FA700`.
- It draws the Sad Mac icon: a 32x32 bitmap depicting a classic Mac with X-eyes and a frowning mouth.
- Beneath the icon, it renders two lines of hexadecimal codes:
  - **Top Row (Class Code)**: `$000001` to `$00000F` indicates hardware subsystem:
    - `01`: ROM checksum failure.
    - `02`: RAM March test failure (Data bus bit error).
    - `03`: RAM addressing error (Row/Column strobe).
    - `04`: VIA controller failure.
    - `05`: SCC serial controller failure.
  - **Bottom Row (Sub-code)**:
    - For RAM errors: bits indicating exactly which SIMM or DRAM chip failed (e.g., `$0000FF00` = upper byte of bank A).


---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

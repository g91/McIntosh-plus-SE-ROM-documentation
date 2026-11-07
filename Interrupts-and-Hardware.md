# Interrupts & Hardware Subsystems Architecture

## 1. The Motorola 68000 Exception & Interrupt Model

The 68000 CPU features 7 levels of prioritized vectored interrupts (Level 1 through Level 7). On the Macintosh Plus and Macintosh SE, the interrupt lines ($\overline{\text{IPL0}}, \overline{\text{IPL1}}, \overline{\text{IPL2}}$) are driven by the peripheral controller chips:

```
Priority   Autovector  Vector Address  Interrupt Source / Function
---------  ----------  --------------  -------------------------------------------------
Level 1    $0064       $000064         VIA 6522 Interrupt (VBL 60Hz, Timers, Shift Reg, ADB)
Level 2    $0068       $000068         SCC 8530 Serial Controller (Data Rx/Tx, LocalTalk)
Level 3    $006C       $00006C         Simultaneous VIA (L1) and SCC (L2) Interrupts
Level 4    $0070       $000070         Programmer's Interrupt Switch (Debug break / NMI)
Level 5    $0074       $000074         (Reserved / Unused)
Level 6    $0078       $000078         (Reserved / Hardware diagnostics)
Level 7    $007C       $00007C         Non-Maskable Interrupt (NMI)
```

### The Interrupt Handling Dispatch Loop (`plus/hw/interrupts.s`)
When an autovector fires, the 68000 pushes the current Status Register (`SR`) and Program Counter (`PC`) onto the stack, sets the CPU interrupt priority mask in `SR` to the interrupt's level, and jumps to the vector:
- **Level 1 (VIA)**: The kernel handler inspects the VIA Interrupt Flag Register (`VIA_IFR` at `$EFFBFE`) to determine which sub-event occurred:
  - Bit 6: Timer 1 underflow (60 Hz clock tick).
  - Bit 5: Timer 2 underflow.
  - Bit 4: Keyboard/ADB shift register transfer complete.
  - Bit 3: Vertical Blanking signal (VBL).
  - Bit 1: Mouse button transition (on Plus).
- **Level 2 (SCC)**: The kernel checks SCC Read Register 0 (`RR0`) to process incoming serial characters or LocalTalk SDLC frame packets without dropping bytes.

---

## 2. Synertek 6522 Versatile Interface Adapter (VIA)

The 6522 VIA is mapped into physical memory at base `$EFE1FE` (`VBase`). It acts as the central peripheral routing hub:

```
Register   Address   Direction  Function
---------  --------  ---------  -------------------------------------------------------------
vBufB      $EFE1FE   R/W        Port B Data: RTC clock/data, mouse X/Y, ADB states
vBufA      $EFFFFE   R/W        Port A Data: Sound volume, floppy head sel, screen buffer
vDDRB      $EFE5FE   R/W        Port B Data Direction Register (1=Output, 0=Input)
vDDRA      $EFE7FE   R/W        Port A Data Direction Register
vT1CL      $EFE9FE   Read       Timer 1 Counter Low Byte
vT1CH      $EFEBFE   Read       Timer 1 Counter High Byte
vT1LL      $EFEDFE   R/W        Timer 1 Latch Low Byte
vT1LH      $EFEFFE   R/W        Timer 1 Latch High Byte (Sets 60 Hz VBL pulse rate)
vT2CL      $EFF1FE   Read       Timer 2 Counter Low Byte
vT2CH      $EFF3FE   Read       Timer 2 Counter High Byte
vSR        $EFF5FE   R/W        Shift Register (Serial keyboard on Plus; ADB on SE)
vACR       $EFF7FE   R/W        Auxiliary Control Register (Timer & shift modes)
vPCR       $EFF9FE   R/W        Peripheral Control Register (Handshake pin control)
vIFR       $EFFBFE   Read       Interrupt Flag Register
vIER       $EFFDFE   R/W        Interrupt Enable Register
```

### Port Bit Allocations
- **Port A (`vBufA` at `$EFFFFE`)**:
  - `Bit 0 - 2`: Sound volume control (0 to 7).
  - `Bit 3`: Sound buffer selector (`0` = alternate buffer, `1` = main buffer).
  - `Bit 4`: ROM Overlay control on Plus (`1` = ROM mapped at $000000; `0` = RAM); Drive select on SE.
  - `Bit 5`: Floppy Head Select (`SEL` line).
  - `Bit 6`: Screen buffer selector (`0` = alternate buffer, `1` = main buffer).
  - `Bit 7`: SCC Wait/Request input (`vSCCWrReq`) - polled during floppy data transfers.
- **Port B (`vBufB` at `$EFE1FE`)**:
  - `Bit 0`: RTC Serial Data in/out.
  - `Bit 1`: RTC Serial Clock line.
  - `Bit 2`: RTC Chip Enable line.
  - `Bit 3`: Mouse button switch (`0` = pressed, `1` = released).
  - `Bit 4 - 5`: On Plus: Mouse quadrature pulses; On SE: ADB state lines `ST0` and `ST1`.

---

## 3. Zilog 8530 Serial Communications Controller (SCC)

The Zilog 8530 SCC controls the two external serial ports: **Channel A (Modem Port)** and **Channel B (Printer Port / LocalTalk)**.

```
Address     Channel  Direction  Register
----------  -------  ---------  -------------------------------------------------------------
$800000     Chan B   Write      Channel B Control / Command Register
$800002     Chan A   Write      Channel A Control / Command Register
$800004     Chan B   Write      Channel B Transmit Data Register
$800006     Chan A   Write      Channel A Transmit Data Register
$900000     Chan B   Read       Channel B Status Register
$900002     Chan A   Read       Channel A Status Register
$900004     Chan B   Read       Channel B Receive Data Register
$900006     Chan A   Read       Channel A Receive Data Register
```

### LocalTalk Networking Physical Layer
Channel B is equipped with a flexible digital phase-locked loop (DPLL) supporting **AppleTalk / LocalTalk** network communications:
- Uses **FM0 (Bi-Phase Space)** encoding at a fixed clock rate of **230.4 kbps**.
- Implements SDLC (Synchronous Data Link Control) frame detection with automatic hardware CRC-16 generation and check.
- The ROM driver (`res_drvr_mpp.s`) implements carrier sensing and collision avoidance with random backoff (CSMA/CA).

---

## 4. Floppy Controllers: IWM & SWIM

The 3.5" floppy subsystem uses custom Apple silicon:

### 4.1 Integrated Woz Machine (IWM)
- Developed by Steve Wozniak for the Apple II and adapted for the Mac.
- Decodes **GCR (Group Code Recording)** 400K and 800K disks:
  - 800K disks use **Zoned Constant Angular Velocity (ZCAV)**: The disk spins faster on inner tracks (approx. 390 RPM) and slower on outer tracks (approx. 590 RPM) to maintain constant linear bit density.
  - Disk motor speed is dynamically adjusted via a pulse-width modulated (PWM) table stored in RAM (`PWMBuf1`/`PWMBuf2`).

### 4.2 Super Woz Integrated Machine (SWIM - SE FDHD)
- Introduced on the Mac SE FDHD to support **1.44 MB MFM (Modified Frequency Modulation)** High-Density floppy disks.
- Features dual-mode register banks:
  - Powers up in backward-compatible **IWM Mode**.
  - A magic byte sequence (`$57, $1B, $DB`) written to the control register switches the chip into **SWIM Mode**, enabling standard 500 kbps MFM clock recovery and double-density PC-compatible disk formatting.

---

## 5. Real-Time Clock & Parameter RAM (RTC / PRAM)

The RTC chip is an ultra-low-power custom CMOS circuit powered by a 4.5V lithium battery:
- Increments a 32-bit second counter representing the number of seconds elapsed since **Midnight, January 1, 1904**.
- Contains 20 bytes (Plus) or 256 bytes (SE) of non-volatile Parameter RAM (PRAM).
- Communicated with serially via VIA Port B (`vRTCData`, `vRTCClk`, `vRTCEnb`) using three-byte command packets (Read Sec, Write Sec, Read PRAM, Write PRAM).

---

## 6. Sound Synthesis Hardware

The classic Mac audio system produces 8-bit sound with zero CPU overhead during playback:
- A dedicated digital-to-analog converter (DAC) is wired to a 370-byte sound buffer in RAM (`$3FFD00`).
- During each horizontal blanking retrace (occurring 22,255 times per second), the video/sound scan hardware fetches one sample byte from RAM and feeds it to the DAC.
- The `.Sound` driver (`res_drvr_sound.s`) provides three synthesis modes:
  1. **Square Wave Synthesizer**: Generates up to 4 simultaneous square wave voices with pitch and volume envelopes.
  2. **Wave-Table Synthesizer**: Loops a 256-byte arbitrary waveform at varying frequency rates.
  3. **Free-Form Synthesizer**: Streams continuous speech, sampled sound, or complex audio directly from application memory.


---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

# Floppy Disk Driver & Controller Internals

## 1. Overview of the `.Sony` Floppy Driver

The 3.5" floppy disk subsystem on the classic Macintosh was engineered by Apple to achieve unprecedented capacity and reliability from standard Sony micro-floppy mechanisms. Implemented as the built-in device driver **`.Sony`** (`plus/resources/res_drvr_sony.s` for Mac Plus and SE, `se/resources/res_drvr_sony_fdhd.s` for SE FDHD), the driver interacts directly with custom Apple disk controller silicon:
- **IWM (Integrated Woz Machine)**: Used in the Mac Plus and base Mac SE. Supports 400 KB and 800 KB **GCR (Group Code Recording)** disks.
- **SWIM (Super Woz Integrated Machine)**: Used in the Mac SE FDHD. Adds hardware support for **1.44 MB MFM (Modified Frequency Modulation)** High-Density disks while retaining full backward compatibility with GCR disks.

---

## 2. GCR Encoding & The 6-and-2 Algorithm

Standard personal computer floppy drives (e.g. IBM PC) used Modified Frequency Modulation (MFM) to record bits. Apple utilized **Group Code Recording (GCR)**, an encoding scheme where nibbles of data are mapped to 8-bit disk bytes guaranteeing that no more than two consecutive `0` bits appear on the magnetic surface. This prevented magnetic flux collapse and clock sync loss without requiring dedicated clock bits.

### The 6-and-2 Byte Transformation
Because an 8-bit GCR disk byte can only represent 64 valid magnetic flux patterns ($2^6$), the driver maps three 8-bit data bytes (24 bits) into four 6-bit disk nibbles (24 bits):
1. **Buffer Setup**: A 512-byte sector is buffered into memory.
2. **Nibblizing**: The `.Sony` driver loops through the 512-byte buffer:
   - Takes 2 bits from each byte and packs them into a 175-byte auxiliary buffer.
   - The remaining 6 bits of each byte are stored in the main buffer.
3. **Table Encoding**: Each 6-bit value (0 to 63) is used as an index into the ROM **`GCR_EncodeTab`**, producing an 8-bit disk byte with bit 7 always set to `1`.
4. **Decoding & Checksum**: When reading from disk, the driver reads bytes from the IWM data register, translates them back using `GCR_DecodeTab`, reconstructs the original 512 bytes, and verifies a 3-byte running checksum.

---

## 3. Zoned Constant Angular Velocity (ZCAV)

Standard floppy drives spin at a constant speed of 300 RPM. Because the outer tracks of a disk have a much larger physical circumference than the inner tracks, recording at constant RPM wastes significant recording media on outer tracks.

Apple overcame this by implementing **Zoned Constant Angular Velocity (ZCAV)** on 800 KB double-sided drives:
- The disk mechanism dynamically varies motor speed across **5 distinct track zones**:

```
Zone   Track Range    Sectors / Track    Disk Motor Speed    Capacity / Track
----   -----------    ---------------    ----------------    ----------------
0      Tracks 0 - 15  12 sectors         approx. 394 RPM     12 KB (double-sided)
1      Tracks 16 - 31 11 sectors         approx. 429 RPM     11 KB
2      Tracks 32 - 47 10 sectors         approx. 472 RPM     10 KB
3      Tracks 48 - 63 9 sectors          approx. 525 RPM     9 KB
4      Tracks 64 - 79 8 sectors          approx. 590 RPM     8 KB
```

Total Capacity: 80 tracks $\times$ 2 heads = 1,600 sectors = **819,200 bytes (800 KB)**.

### Pulse-Width Modulation (PWM) Motor Speed Control
The Mac logic board does not use a tachometer feedback loop to set disk speed. Instead, the video/sound horizontal scan hardware continuously reads a byte from the **PWM sound buffer** in RAM (`PWMBuf1` / `PWMBuf2`).
- The PWM duty cycle directly controls the voltage fed to the floppy motor spindle.
- When the driver steps the drive heads to a new track, it calculates the track's zone and writes the appropriate PWM speed control value into the buffer.

---

## 4. Head Stepping & Track Navigation

The drive read/write head is positioned using a 4-phase bipolar stepper motor driven by VIA Port A (`vHeadSel`) and IWM phase lines `CA0`, `CA1`, `CA2`:

```
Phase Sequence:
Step Outward:  Phase 0 -> Phase 1 -> Phase 2 -> Phase 3 -> Phase 0
Step Inward:   Phase 3 -> Phase 2 -> Phase 1 -> Phase 0 -> Phase 3
```

### Motor Settling Timing
- Stepping pulse width: approx. 12 microseconds.
- Step settling delay: **12 milliseconds** per track step.
- Head load delay: **30 milliseconds** before read/write operations commence after seeking.

---

## 5. The SWIM Controller & High-Density MFM Support

The **Super Woz Integrated Machine (SWIM)** in the Mac SE FDHD (`se/resources/res_drvr_sony_fdhd.s`) represents the culmination of Apple's floppy technology:

### Mode Switching (`SWIM_MODE_SWITCH`)
The SWIM chip powers up in backward-compatible **ISM Mode** (mimicking an original IWM). To activate High-Density 1.44 MB MFM capabilities:
1. The driver writes the byte sequence `$57`, `$1B`, `$DB` to the mode register.
2. The internal logic resets the phase-locked loop (PLL) from 2 MHz to **4 MHz**.
3. In MFM mode, the disk mechanism spins at a constant **300 RPM** across all 80 tracks.
4. Each track contains **18 sectors** of 512 bytes each, providing:
   $$80 \text{ tracks} \times 2 \text{ heads} \times 18 \text{ sectors} \times 512 \text{ bytes} = 1,474,560 \text{ bytes} \text{ (1.44 MB)}$$
5. The driver automatically checks the High-Density sensor hole on 3.5" disk shells to determine whether to operate in GCR or MFM mode.


---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

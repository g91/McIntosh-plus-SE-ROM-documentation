# Hardware Registers Reference Map

This directory catalogs the physical hardware registers for the Synertek 6522 VIA, Zilog 8530 SCC, NCR 5380 SCSI, and Floppy Disk controllers, defined in `include/hwregs.inc`.

| Register Symbol | Address / Equation | Function & Details |
| :--- | :--- | :--- |
| **`AVBufA`** | `0xEFFFFE` | Port A data (sound, overlay, disk SEL, screen). |
| **`AVBufB`** | `0xEFE1FE` | Port B data (RTC, mouse, sound). |
| **`AVBufM`** | `0xEFE1FE` | Port B (mouse button bit). |
| **`AVIER`** | `0xEFFDFE` | Interrupt enable register. |
| **`AVIFR`** | `0xEFFBFE` | Interrupt flag register. |
| **`HiIntMask`** | `0x0300` | SR mask IPL 3: only the programmer's switch (MPW). |
| **`IWM_EXTDRV`** | `0xDFF7FF` | Drive-Sel = 1: /ENBL2, external drive. |
| **`IWM_INTDRV`** | `0xDFF5FF` | Drive-Sel = 0: /ENBL1, internal drive. |
| **`IWM_MTROFF`** | `0xDFF1FF` | Motor-On = 0: drive enables off (MPW: DMtrOff). |
| **`IWM_MTRON`** | `0xDFF3FF` | Motor-On = 1: enable the selected drive (MPW: DMtrOn). |
| **`IWM_PH0H`** | `0xDFE3FF` | PH0 = 1: drive CA0 high (MPW: DPh0H). |
| **`IWM_PH0L`** | `0xDFE1FF` | PH0 = 0: drive CA0 low (MPW: DBase, DPh0L). === IWM (Integrated Woz Machine - floppy disk controller) === The IWM is selected (/DEV) anywhere in 0xC00000-0xDFFFFF. Its register select inputs A0-A3 are CPU address lines A9-A12 and its data bus is the low byte (odd addresses), so its 16 locations are 0x200 apart, from DBase = 0xDFE1FF (MPW HardwareEqu.a; low-memory IWM holds the base, the offsets ph0L..q7H are in sysequ.inc). Any access (read or write) to a location sets ("H", odd location) or clears ("L", even location) one of eight state bits, selected by A3-A1 (IWM Design Spec, "State Register"): PH0-PH3    phase outputs = the drive's CA0, CA1, CA2 and LSTRB lines Motor-On   drive enable: the selected /ENBLx output goes low Drive-Sel  0 = /ENBL1 (internal drive), 1 = /ENBL2 (external port) L6, L7     register select ("Q6", "Q7") L7, L6 and Motor-On select the register that the same access reads or writes ("x" = either): L7 L6 Motor-On 0  0  0    read all ones 0  0  1    read the data register (read state) 0  1  x    read the status register: bit 7 = SENSE input, bit 5 = a drive enable is active, bits 0-4 = mode register bits 0-4 1  0  x    read the write-handshake register: bit 7 = 1: write buffer empty (ready for the next byte), bit 6 = 0: write underrun 1  1  0    write the mode register: bit 0 latch mode, bit 1 asynchronous handshake, bit 2 1-second motor-off timer disabled, bit 3 fast mode (2 us bit cells), bit 4 8 MHz clock, bit 5 test mode 1  1  1    write the data register (write load state) A register is read at an "L" location and written at an "H" location (IWM undoco features, "IWM Register Access"). The SENSE input and the read data input RDDATA are both wired to the drive's RD line. |
| **`IWM_PH1H`** | `0xDFE7FF` | PH1 = 1: drive CA1 high. |
| **`IWM_PH1L`** | `0xDFE5FF` | PH1 = 0: drive CA1 low. |
| **`IWM_PH2H`** | `0xDFEBFF` | PH2 = 1: drive CA2 high. |
| **`IWM_PH2L`** | `0xDFE9FF` | PH2 = 0: drive CA2 low. |
| **`IWM_PH3H`** | `0xDFEFFF` | PH3 = 1: drive LSTRB high (strobe a control register). |
| **`IWM_PH3L`** | `0xDFEDFF` | PH3 = 0: drive LSTRB low. |
| **`IWM_Q6H`** | `0xDFFBFF` | L6 = 1: status (L7 = 0), mode/data write (L7 = 1) (MPW: DiskQ6H). |
| **`IWM_Q6L`** | `0xDFF9FF` | L6 = 0: read data (L7 = 0) or handshake (L7 = 1) (MPW: DiskQ6L). |
| **`IWM_Q7H`** | `0xDFFFFF` | L7 = 1: write states (MPW: DiskQ7H). |
| **`IWM_Q7L`** | `0xDFFDFF` | L7 = 0: read states (MPW: DiskQ7L). |
| **`SCCEnblMask`** | `0xF9FF` | SR mask to enable SCC interrupts. |
| **`SCCRBase`** | `0x9FFFF8` | SCC base read address. === SCC (Zilog 8530 Serial Communications Controller) === MPW names: SCCRBase (read), SCCWBase (write) |
| **`SCCWBase`** | `0xBFFFF9` | SCC base write address. |
| **`SCC_RdCtlA`** | `SCCRBase` | Channel A control read. |
| **`SCC_RdCtlB`** | `SCCRBase` | Channel B control read. |
| **`SCC_RdDataA`** | `SCCRBase` | Channel A data read. |
| **`SCC_RdDataB`** | `SCCRBase` | Channel B data read. |
| **`SCC_WrCtlA`** | `SCCWBase` | Channel A control write. |
| **`SCC_WrCtlB`** | `SCCWBase` | Channel B control write. |
| **`SCC_WrDataA`** | `SCCWBase` | Channel A data write. |
| **`SCC_WrDataB`** | `SCCWBase` | Channel B data write. |
| **`SCSI_Base`** | `0x580000` | NCR 5380 base (MPW: scsiRd). === SCSI (NCR 5380) === MPW names: scsiRd, scsiWr |
| **`SERegs`** | `0x3FFC80` | Saved registers during system error. === System Error register save area (MPW HardwareEqu.a) === |
| **`SEScrnFace`** | `0x3FCCDF` | Screen addr for sad/happy Mac face. |
| **`SEScrnI2`** | `0x3FCF1F` | Screen addr for boot icon overlay. |
| **`SEScrnIcon`** | `0x3FCB5E` | Centered screen addr for boot icons. |
| **`SEScrnInc`** | `0x3FD5DF` | Screen addr for error blink animation. |
| **`SEScrnNum`** | `0x3FD3DD` | Screen addr for error number display. |
| **`ScreenLow`** | `0x3FA700` | Screen buffer base address. === Screen and Sound constants (MPW HardwareEqu.a) === |
| **`SoundLow`** | `0x3FFD00` | Sound buffer base address (370 words; see below). |
| **`TicksPr100`** | `78` | VIA timer cycles per 100 us (783.36 kHz: 99.6 us). |
| **`VBase`** | `0xEFE1FE` | VIA base address (= PortB). === VIA (6522 Versatile Interface Adapter) === MPW name: VBase. Registers spaced 0x200 apart, active on odd bytes. |
| **`VIAIntMask`** | `0x0100` | SR mask for VIA (level 1) interrupts. VIA interrupt constants: |
| **`VIA_ACR`** | `0xEFF7FE` | Auxiliary control reg = VBase + 0x1600. |
| **`VIA_DDRA`** | `0xEFE7FE` | Port A data direction = VBase + 0x0600. |
| **`VIA_DDRB`** | `0xEFE5FE` | Port B data direction = VBase + 0x0400. |
| **`VIA_IER`** | `AVIER` | Interrupt enable reg = VBase + 0x1C00. |
| **`VIA_IFR`** | `AVIFR` | Interrupt flag reg = VBase + 0x1A00. |
| **`VIA_PCR`** | `0xEFF9FE` | Peripheral control reg = VBase + 0x1800. |
| **`VIA_PortA`** | `AVBufA` | Port A = VBase + 0x1E00. |
| **`VIA_PortA2`** | `AVBufA` | Port A no handshake = VBase + 0x1E00. |
| **`VIA_PortB`** | `AVBufB` | Port B = VBase + 0x0000. Aliases using register-name convention: |
| **`VIA_SR`** | `0xEFF5FE` | Shift register (keyboard) = VBase + 0x1400. |
| **`VIA_T1CH`** | `0xEFEBFE` | Timer 1 counter high = VBase + 0x0A00. |
| **`VIA_T1CL`** | `0xEFE9FE` | Timer 1 counter low = VBase + 0x0800. |
| **`VIA_T1LH`** | `0xEFEFFE` | Timer 1 latch high = VBase + 0x0E00. |
| **`VIA_T1LL`** | `0xEFEDFE` | Timer 1 latch low = VBase + 0x0C00. |
| **`VIA_T2CH`** | `0xEFF3FE` | Timer 2 counter high = VBase + 0x1200. |
| **`VIA_T2CL`** | `0xEFF1FE` | Timer 2 counter low = VBase + 0x1000. |
| **`maxX`** | `512` | Screen width in pixels. |
| **`maxY`** | `342` | Screen height in pixels. |
| **`romStart`** | `0x400000` | ROM start address. |
| **`sBSR`** | `0x50` | Bus & Status Register (read) / DMA Tx Start (write). |
| **`sCDR`** | `0x00` | Current SCSI Data (read) / Output Data (write). NCR 5380 register offsets (from MPW HardwareEqu.a): |
| **`sCSR`** | `0x40` | Current SCSI Bus Status (read) / Select Enable (write). |
| **`sICR`** | `0x10` | Initiator Command Register. |
| **`sIDR`** | `0x60` | Input Data (read) / Target DMA Rx Start (write). |
| **`sMR`** | `0x20` | Mode Register. |
| **`sRESET`** | `0x70` | Reset Parity (read) / Initiator DMA Rx Start (write). |
| **`sTCR`** | `0x30` | Target Command Register. |
| **`scrnBytes`** | `21888` | Screen size: 512*342/8 = 21888 bytes. |
| **`scrnRowB`** | `64` | Screen row bytes (512/8). |

---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

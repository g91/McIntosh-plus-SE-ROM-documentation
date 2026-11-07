# Apple Desktop Bus (ADB) Manager

## 1. Overview of the Apple Desktop Bus Architecture

Introduced on the Apple IIgs and brought to the Macintosh line on the **Macintosh SE** (1987), the **Apple Desktop Bus (ADB)** (`se/os/adb_mgr.s`) replaced the separate, incompatible keyboard and mouse cables of earlier Macs with a standardized, daisy-chainable low-speed bidirectional serial bus.

Up to 16 input devices (keyboards, single-button mice, trackballs, numeric keypads, graphics tablets) can share a single 4-pin mini-DIN physical bus operating at ~10 to 125 kbps.

---

## 2. Hardware Architecture & The PIC Transceiver

On the Macintosh SE, the 68000 CPU does not drive the ADB serial wire directly. Instead, the logic board incorporates an 8-bit **PIC1657 microcontroller** that handles microsecond-level bus timing, bit encoding, and signal levels.

The 68000 CPU interfaces with the ADB transceiver through the **Synertek 6522 VIA**:
- **VIA Port B, Bits 4 and 5**: State lines `ST0` and `ST1`.
  - These two lines dictate the ADB transceiver transaction phase:
    - `00`: Idle / Start Transaction.
    - `01`: Command transfer (68000 sending command to ADB transceiver).
    - `10`: Data transfer (68000 sending/receiving data bytes via Shift Register).
    - `11`: End of transaction / Bus Reset.
- **VIA Shift Register (`VIA_SR` at `$EFF5FE`)**:
  - Transmits and receives serialized data bytes to and from the transceiver under external clock control (via VIA pin `CB1`).
- **VIA Interrupt (`VIA_IFR` bit 2)**:
  - The shift-register completion interrupt triggers `FDBSHIFTINT`, advancing the ADB transaction state machine.

---

## 3. ADB Command Structure & Protocols

Every transaction on the ADB bus begins with an 8-bit Command Byte sent by the host:

```
Bits 7 - 4: Device Address (0 to 15)
Bits 3 - 2: Command Type:
            00: SendReset  (Resets all devices on bus)
            01: Flush      (Purges internal device buffer)
            10: Listen     (Host writes data into device register 0-3)
            11: Talk       (Host requests data from device register 0-3)
Bits 1 - 0: Register Number (0 to 3)
```

### Standard ADB Device Registers
- **Register 0**: Primary input data (e.g. keyboard scancodes, mouse X/Y deltas).
- **Register 1**: Reserved / Device configuration.
- **Register 2**: Modifier key status or secondary control.
- **Register 3**: Device Identification & Handler ID (used during bus enumeration).

### Default ADB Device Addresses
- Address `0`: Reserved.
- Address `1`: Software protection dongle / security device.
- Address `2`: Standard Apple Keyboard.
- Address `3`: Apple Desktop Bus Mouse.
- Address `4`: Absolute positioning device (graphics tablet).
- Address `5` - `15`: Unassigned / expansion peripherals.

---

## 4. Bus Enumeration & Collision Detection

When multiple identical devices (e.g., two keyboards or two mice) are connected to the daisy chain, they both power up listening to the same default address (e.g. Address 2). The ADB Manager resolves this via **Bus Arbitration**:

```
[ INITADB / ADBReInit ]
           |
           v
[ SendReset ($00) ] ---> Resets all connected peripherals to default addresses
           |
           v
[ Scan Loop: Address 0 to 15 ]
  - Send "Talk Register 3" to each address.
  - Does a device respond?
         /                   \
   (No) /                     \ (Yes)
       v                       v
  Next address          Read 16-bit Device ID & Handler ID
                               |
                               v
                        [ Check for Collision ]
                        - Both devices pull line low.
                        - Device with lowest random address wins.
                        - Manager moves responding device to a free
                          unassigned address (e.g. from 2 to 8)
                          via "Listen Register 3" command.
                               |
                               v
                        Repeat until all devices occupy unique addresses!
```

---

## 5. The ADB Manager Device Table (`ADBBase`)

The ADB Manager maintains its global state and device directory in memory pointed to by low-memory global `ADBBase` (`$0CF8`).
The **Device Table** holds up to 16 entries (12 bytes per entry):

```
Offset  Field         Type     Description
------  ------------  -------  -------------------------------------------------------------
$00     devAddress    Byte     Current active ADB bus address (1 to 15)
$01     origAddress   Byte     Default factory address (2=Keyboard, 3=Mouse)
$02     handlerID     Byte     Device handler ID (e.g., $01 = standard mouse, $02 = keyboard)
$03     flags         Byte     Device status flags
$04     dbServiceRt   ProcPtr  Pointer to device service routine (invoked on Talk Reg 0)
$08     dbDataArea    Ptr      Pointer to device's private workspace/buffers
```

---

## 6. ADB Traps and API Reference

- **`ADBReInit`** (`$A07B`):
  - *Operation*: Completely re-initializes the ADB subsystem. Resets bus, clears device table, re-enumerates all connected devices, and loads default drivers.
- **`ADBOp`** (`$A07C`):
  - *Prototype*: `FUNCTION ADBOp(data: Ptr; compRout: ProcPtr; buffer: Ptr; commandNum: Integer): OSErr;`
  - *Entry*: `A0` = Pointer to parameter block, `D0.W` = ADB command byte.
  - *Operation*: Asynchronously queues a raw ADB command (Talk, Listen, Flush) for bus transmission.
- **`CountADBs`** (`$A077`):
  - *Exit*: `D0.W` = Total number of active devices currently enumerated in the ADB table.
- **`GetIndADB`** (`$A078`):
  - *Entry*: `D0.W` = Index (1 to Count). *Exit*: `D0.B` = ADB address, `A0` = Pointer to `ADBDataBlock`.
- **`GetADBInfo`** (`$A079`) & **`SetADBInfo`** (`$A07A`):
  - Reads or reassigns the service routine pointer and data area for a specific ADB address.
- **`KeyTranslate`** (`$A9C3`):
  - *Prototype*: `FUNCTION KeyTranslate(transData: Ptr; keycode: Integer; VAR state: LongInt): LongInt;`
  - *Operation*: Translates raw ADB 7-bit keyboard scancodes and modifier keys into ASCII characters using the ROM-resident or system `'KCHR'` resource table (`res_kchr.s`).


---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

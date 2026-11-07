# Boot & Diagnostics Function & Routine Directory

This catalog lists all **721** routines, functions, exception vectors, and labels belonging to the **Boot & Diagnostics** subsystem across the Macintosh Plus (128 KB) and Macintosh SE (256 KB) ROMs.

| Symbol / Routine | Mac Plus Offset | Mac SE Offset | Source File : Line | Description / Prototype |
| :--- | :--- | :--- | :--- | :--- |
| **`ADDRLINE_FAIL`** | `0x000DBE` | — | `memtest.s:54` | — |
| **`ADDRLINE_TEST`** | `0x000DA8` | — | `memtest.s:43` | Address line stuck-at-fault test: write 0xFFFF to each power-of-2 offset, check whether it bleeds through to address 0 (stuck address line = alias). |
| **`ADDRTEST_CHK_STACK`** | — | `0x00293E` | `memtest.s:1914` | — |
| **`ADDRTEST_LINES`** | — | `0x002928` | `memtest.s:1908` | **Regs:** `Entry: SP = RAM top (from memory sizing) Exit: D6 = 0 if pass, non-zero if address line fault`<br>ADDRTEST_LINES - address line stuck-at test Writes unique values at power-of-2 addresses (4, 8, 16, ..., up to half of RAM) then reads back to verify no aliasing. Tests all address lines for stuck-at ... |
| **`ADDRTEST_PHASE1`** | — | `0x002948` | `memtest.s:1921` | Phase 1: write unique values at power-of-2 addresses (ascending) |
| **`ADDRTEST_RETURN`** | — | `0x00299A` | `memtest.s:1970` | — |
| **`ADDRTEST_REVERSE_VERIFY`** | — | `0x00298A` | `memtest.s:1961` | Phase 6: verify markers after reverse write |
| **`ADDRTEST_REVERSE_WRITE`** | — | `0x002972` | `memtest.s:1947` | Phase 4: reverse-write markers (descending power-of-2 addresses) |
| **`ADDRTEST_VERIFY_LOOP`** | — | `0x002960` | `memtest.s:1936` | Phase 2: verify address 0 not corrupted (no stuck address lines) Phase 3: verify each power-of-2 address still holds its marker |
| **`ADDRTEST_VERIFY_REF`** | — | `0x002982` | `memtest.s:1955` | Phase 5: verify address 0 not corrupted (reverse-order check) |
| **`ADDRTEST_WRITE_LOOP`** | — | `0x00294E` | `memtest.s:1924` | — |
| **`ADRERROR`** | — | `0x001AFA` | `memtest.s:166` | — |
| **`ALARM_FLASH_LOOP`** | `0x000926` | `0x0006BA` | `boot_install.s:186`<br>`boot_install.s:755` | Flash the Apple menu bar area (alarm indicator) by XORing scanlines. A1 = AlarmState low-memory address (set by caller). XOR Apple menu area (alarm flash) |
| **`ALLOC_BOOT_BUF`** | — | `0x000AFC` | `boot_load.s:350` | ALLOC_BOOT_BUF - D3 > 0: read into boot block buffer area |
| **`ALLOC_CAT_CACHE`** | `0x000D34` | — | `boot_load.s:483` | Allocate catalog cache |
| **`ALLOC_CTL_CACHE`** | — | `0x000C48` | `boot_load.s:490` | — |
| **`ALLOC_FILE_BUFFER`** | `0x000C40` | — | `boot_load.s:372` | ALLOC_FILE_BUFFER - D3 < 0: allocate buffer with _NewPtr for file contents Called during boot. |
| **`ALLOC_SYS_PTR`** | — | `0x000B06` | `boot_load.s:356` | ALLOC_SYS_PTR - D3 < 0: allocate system heap block for file data |
| **`ALLOC_VOL_CACHE`** | `0x000D1C` | `0x000C30` | `boot_load.s:474`<br>`boot_load.s:482` | Allocate volume cache |
| **`ANIM_DELAY_LOOP`** | `0x0007BA` | — | `vectors.s:1145` | Busy-wait animation delay |
| **`ANIMATE_DISK_ICON`** | `0x0007A6` | — | `vectors.s:1133` | ANIMATE_DISK_ICON - animate disk icon: alternate between drawing and erasing D4 counts frames, D7 = icon address (0 = erase, nonzero = draw icon) |
| **`BADDISK`** | — | `0x00000E` | `vectors.s:65` | +$0A, +$0E: restart entries (Apple: StBoot, "jump to start code for a restart", and BadDisk, "eject disk, and reboot"). In the SE both restart at STARTBOOT; the Plus branches to its eject-and-try-next... |
| **`BANK_ALIAS_CHECK`** | `0x000DE6` | — | `memtest.s:90` | Verify no bank-to-bank address aliasing: each bank should hold its unique sequence number (D3) written during previous iterations. |
| **`BANK_PATTERN_TEST`** | `0x000DD4` | — | `memtest.s:78` | Per-bank data pattern verification: write alternating patterns to each bank, then read back to confirm data bus integrity across all banks. |
| **`BANK_TOGGLE_LOOP`** | `0x000DD6` | — | `memtest.s:80` | Per-bank data pattern verification: write alternating patterns to each bank, then read back to confirm data bus integrity across all banks. |
| **`BASEOFROM`** | `0x000000` | `0x000000` | `vectors.s:41`<br>`vectors.s:27` | Macintosh Plus ROM Boot Code - Vectors, Hardware Init, Startup This file contains the ROM header, exception vectors, hardware initialization (VIA, IWM, SCC, RTC), and the startup sequence that leads t... |
| **`BEEP_DMA_DELAY`** | `0x0002C2` | `0x002A24` | `vectors.s:525`<br>`memtest.s:2055` | Sound DMA settling delay |
| **`BEEP_DONE`** | `0x0000F8` | — | `vectors.s:229` | BEEP_DONE - startup beep complete, now initialize disk controller Trace: beep has sounded, A5 = VIA base. Called during boot. |
| **`BEEP_DURATION_CHECK`** | `0x00033C` | `0x002A9E` | `vectors.s:596`<br>`memtest.s:2118` | BEEP_DURATION_CHECK - decrement duration; if done, fill buffer with silence and return |
| **`BEEP_EXTEND_LOOP`** | `0x000310` | `0x002A72` | `vectors.s:573`<br>`memtest.s:2098` | Extend smoothed data: copy samples to fill remaining buffer Sound extend: copy filtered data to fill buffer |
| **`BEEP_FILL_BUFFER`** | `0x0002BE` | `0x002A20` | `vectors.s:522`<br>`memtest.s:2053` | BEEP_FILL_BUFFER - fill sound buffer with square wave pattern Uses 4-byte pattern 0xC0,0x06,0xFA,0x40 repeated to fill 370 bytes. The pattern creates a ~3 kHz square wave through the PWM DAC. |
| **`BEEP_FILL_CYCLE`** | `0x0002CE` | `0x002A30` | `vectors.s:532`<br>`memtest.s:2060` | Sound fill: cycle 4 pattern bytes |
| **`BEEP_FILL_REPEAT`** | `0x0002C8` | `0x002A2A` | `vectors.s:529`<br>`memtest.s:2058` | Sound fill: repeat pattern 5 times |
| **`BEEP_FIR_LOOP`** | `0x0002F0` | `0x002A52` | `vectors.s:556`<br>`memtest.s:2082` | Sound smoothing: 1:2:1 FIR filter |
| **`BEEP_POLL_T1_LOOP`** | `0x0002AE` | — | `vectors.s:515` | BootBeep: poll VIA IFR for vertical blanking (CA1) |
| **`BEEP_POLL_TIMER_LOOP`** | — | `0x002A10` | `memtest.s:2046` | — |
| **`BEEP_POLL_VIA`** | `0x0002AC` | `0x002A0E` | `vectors.s:512`<br>`memtest.s:2044` | BEEP_POLL_VIA - VBL polling path (interrupts disabled during early boot) Poll VIA IFR bit 1 (CA1: vertical blanking) since no VBL interrupt handler yet. Called during boot. |
| **`BEEP_SILENCE_LOOP`** | `0x000348` | `0x002AAA` | `vectors.s:603`<br>`memtest.s:2124` | Beep duration expired: fill buffer with silence ($80 = zero level) Fill sound buffer with silence (0x80) |
| **`BEEP_SMOOTH_FILTER`** | `0x0002E8` | `0x002A4A` | `vectors.s:551`<br>`memtest.s:2078` | BEEP_SMOOTH_FILTER - smooth the sound buffer using weighted average filter Applies a 1:2:1 FIR filter to the sound samples to reduce aliasing. Then extends the smoothed data to fill the entire buffer.... |
| **`BEEP_TICK_WAIT`** | `0x000324` | `0x002A86` | `vectors.s:584`<br>`memtest.s:2108` | BootBeep: wait for next tick |
| **`BEEP_VBL_POLL`** | `0x00032C` | — | `vectors.s:591` | BEEP_VBL_POLL - VBL poll: wait for Timer 1 interrupt flag (early boot path) Called during boot (2,388,671 times in 30s trace). |
| **`BEEP_VIA_POLL_LOOP`** | — | `0x002A8E` | `memtest.s:2113` | VIA polling path (interrupts disabled) |
| **`BEEP_WAIT_TICK`** | `0x0002A4` | `0x002A06` | `vectors.s:504`<br>`memtest.s:2038` | Interrupts enabled: sync to VBL using Ticks global BootBeep: wait for Ticks change |
| **`BEEP_WAIT_VBL`** | `0x00031A` | `0x002A7C` | `vectors.s:578`<br>`memtest.s:2103` | BEEP_WAIT_VBL - wait for one VBL tick, then loop back to smooth and refill |
| **`BEEP_WRITE_SAMPLE`** | `0x0002D0` | `0x002A32` | `vectors.s:535`<br>`memtest.s:2062` | Sound fill: write 20 samples per byte |
| **`BOOT_DEVICE_FOUND`** | — | `0x000CC4` | `boot_search.s:42` | — |
| **`BOOT_FAIL`** | — | `0x000A4C` | `boot_load.s:253` | — |
| **`BOOT_FINDNEXT_DONE`** | — | `0x000DB6` | `boot_search.s:182` | — |
| **`BOOT_MEMTEST_RET`** | `0x000132` | — | `vectors.s:268` | BOOT_MEMTEST_RET - return from ChecksumRomAndTestMemory Z flag = 1: all tests passed -> continue boot. Z flag = 0: test failed -> show sad Mac (CritErr). Called during boot. |
| **`BootBeep`** | `0x00028A` | `0x0029EA` | `vectors.s:494` | Startup beep: fills the sound buffer with a square wave. SoundLow (0x3FFD00) is the main sound buffer: 370 words, one fetched per scan line (22.25 kHz); the high byte of each word is the sound sample.... |
| **`BOOTBEEP`** | `0x00028A` | `0x0029EA` | `memtest.s:2024` | **Regs:** `Entry: D0 = beep duration in ticks`<br>BOOTBEEP - generate square wave beep tone Fills the sound buffer with a ~3 kHz square wave pattern, then smooths it with a FIR filter. The tone plays through the PWM DAC for D3 ticks. Code continues i... |
| **`BootFromDisk`** | `0x000986` | — | `boot_load.s:29` | Startup: boot from the startup disk (BootFromDisk) Corresponds to Apple's StartBoot.a (BOOTME in the SE link map). BootFromDisk is the top of the system-loading sequence: heap sizing, mounting the sta... |
| **`BOOTME`** | — | `0x00080A` | `boot_load.s:26` | Startup: boot from the startup disk (StartBoot) Apple source: StartBoot.a. BOOTME (MYBOOT in MacSEROM.lst) mounts the startup volume found by boot_search.s, reads the boot blocks, opens the System fil... |
| **`BootPart2`** | `0x000352` | — | `vectors.s:613` | At this point: A3 = start of usable RAM, D0 = end of RAM (from memtest), A5 = top of RAM (MemTop). Screen is white, beep has sounded. Called during boot. |
| **`BOOTRETRY`** | — | `0x0000D2` | `boot_install.s:88` | — |
| **`BUSERROR`** | — | `0x001AE8` | `memtest.s:157` | Exception handlers of the startup tests, reached through MEMTEST (Apple source: the handlers after TMVectors in USTStartUp.a; the labels are Apple's names). Each stores $FF00 plus the exception number... |
| **`BUSERROR_UNEXPECTED`** | — | `0x001AF2` | `memtest.s:163` | The other handlers follow in vector order. |
| **`CALL_SECONDARY_BOOT`** | — | `0x000822` | `boot_load.s:34` | — |
| **`CAP_APPL_BASE`** | — | `0x000868` | `boot_load.s:61` | — |
| **`CHECK_BOOT_ERROR`** | `0x000BB2` | `0x000A84` | `boot_load.s:274`<br>`boot_load.s:279` | CHECK_BOOT_ERROR - Conditional system error - show error if D7 is nonzero Called during boot. |
| **`CHECK_BOOT_ERROR_RTS`** | — | `0x000A8A` | `boot_load.s:283` | — |
| **`CHECK_BOOT_MASK`** | `0x00078C` | — | `vectors.s:1118` | CHECK_BOOT_MASK - check if this drive is in the boot mask (eligible for boot) |
| **`CHECK_DIAG_ROM`** | `0x000368` | — | `vectors.s:631` | Initialize system error handler (creates exception vectors, MicroBug entry) CHECK_DIAG_ROM - check for diagnostic ROM at 0xF80080 A second checkpoint for external test hardware (alternate ROM socket).... |
| **`CHECK_FILE_EXISTS`** | `0x000BC6` | `0x000A8C` | `boot_load.s:297`<br>`boot_load.s:290` | CHECK_FILE_EXISTS - File existence check - call _GetFileInfo on file named by A3 Called during boot. |
| **`CHECK_TEST_SW`** | `0x000042` | — | `vectors.s:106` | CHECK_TEST_SW - check for external test software at TestSoftware ($0680) Trace: D0=0, A0=0 (no test software installed), falls through to COLD_START. Called during boot. |
| **`CHECKMOUSE_RTS`** | — | `0x000DF2` | `boot_search.s:218` | — |
| **`CHECKMOUSEEJECT`** | — | `0x000DE8` | `boot_search.s:214` | CHECKMOUSEEJECT - if mouse button is down, eject the disk Returns Z=0 if disk was NOT ejected (boot can proceed). |
| **`ChecksumRomAndTestMemory`** | `0x000D76` | — | `memtest.s:19` | ROM Checksum Verification and Memory Test Verifies the ROM checksum (sum of 16-bit words from offset 4), then tests RAM with multiple passes (bus test, address line test, byte-write test). Called duri... |
| **`CHKERROR`** | — | `0x001B12` | `memtest.s:175` | — |
| **`CKSUM_LOOP`** | `0x000D8A` | `0x0026DA` | `memtest.s:27`<br>`memtest.s:1580` | — |
| **`CLEAR_APPACKS_LOOP`** | `0x00066A` | — | `vectors.s:988` | Clear all 8 package handle slots (PACK 0-7) Clear AppPacks[0..7] |
| **`CLEAR_BOOT_MASK`** | — | `0x000A76` | `boot_load.s:271` | — |
| **`CLEAR_CKDDB_LOOP`** | `0x000C8E` | `0x000B8E` | `boot_load.s:423`<br>`boot_load.s:424` | Clear checked disk block table |
| **`CLEAR_QD_GLOBALS`** | `0x000466` | — | `vectors.s:723` | Read initial mouse button state from VIA port B bit 3 Clear QuickDraw and cursor globals (JHideCursor through WWExist) Clear QD/cursor globals loop |
| **`ClkNoMem`** | `0x0001F8` | `0x00A2C0` | `vectors.s:378` | RTC serial protocol: sends a command byte, receives a response byte. Uses VIA PortB bits: PB0=data, PB1=clock, PB2=enable (active low). Protocol: enable RTC (PB2=0), clock out 8 command bits on PB0/PB... |
| **`CLOSE_FILE`** | `0x000C2C` | `0x000AF2` | `boot_load.s:349`<br>`boot_load.s:343` | Close file (after read or error) |
| **`CLR_CRSRVARS_LOOP`** | — | `0x0005EE` | `boot_install.s:676` | — |
| **`COLD_START`** | `0x000062` | — | `vectors.s:129` | COLD_START - begin cold start: disable interrupts, sample bus timing Reached via the entry-table BRA at $000A, or after a failed test-software signature check. Masks all interrupts, samples bus timing... |
| **`COLDSTART_ADDRLINE_DONE`** | — | `0x001CF0` | `memtest.s:381` | — |
| **`COLDSTART_CHECKSUM_DONE`** | — | `0x001C6C` | `memtest.s:322` | — |
| **`COLDSTART_DIAG_TIMER_INIT`** | — | `0x001D2C` | `memtest.s:411` | — |
| **`COLDSTART_INIT_RAM_DONE`** | — | `0x001CC8` | `memtest.s:367` | Check first 1K of RAM with pattern fill/verify |
| **`COLDSTART_LOOPBACK_PATH`** | — | `0x001D1A` | `memtest.s:405` | Loopback jumper (factory test fixture) found: queue the boot message for the host (D7 bit 16, MsgQ), repeated about once a second (bit 22, timer: 12 runs of VIA timer 2), and enter the Test Manager, w... |
| **`COLDSTART_MEMSIZE_DONE`** | — | `0x001CE0` | `memtest.s:375` | — |
| **`COLDSTART_MEMTEST_COPYLOOP`** | — | `0x001D10` | `memtest.s:396` | Normal start: install MEMTEST as the exception vector table by copying its 64 vectors to address 0 (a 68000 takes its vectors from there), then continue at STARTINIT1 with A6 = top of RAM. |
| **`COLDSTART_NO_TEST_SW`** | — | `0x001C04` | `memtest.s:288` | — |
| **`COLDSTART_RUN_CHECKSUM`** | — | `0x001C60` | `memtest.s:318` | — |
| **`COLDSTART_RUN_TM`** | — | `0x001D3A` | `memtest.s:416` | — |
| **`COMPBOOTSTACK`** | — | `0x00018E` | `boot_install.s:164` | COMPBOOTSTACK - compute boot stack position = MemTop/2 - 1K Returns A0 = boot stack address. Places stack at midpoint of RAM minus a 1K safety margin. |
| **`COPY_SYSRES_NAME`** | `0x0009F2` | `0x0008B0` | `boot_load.s:70`<br>`boot_load.s:87` | Initialize Event Manager and File System from boot block parameters Mount the boot volume Get volume info to find the Finder info (blessing) Copy System name, open Finder |
| **`COPY_ZONE_PARAMS`** | `0x00096C` | — | `boot_install.s:218` | Copy InitZone parameter words |
| **`CPPROTOCOL`** | — | `0x001B4A` | `memtest.s:196` | — |
| **`CPU_DETECTED`** | `0x0005A6` | — | `vectors.s:898` | CPU detected - restore SP, set CPUFlag |
| **`CritErr`** | `0x000136` | `0x001092` | `vectors.s:274` | Saves all registers to the system error save area (0x3FFC80 = SERegs) then shows the sad Mac icon with the error code. |
| **`CRITERR`** | `0x000136` | `0x001092` | `sad_mac.s:15` | Startup failure: Sad Mac / Happy Mac (StartFail) Apple source: StartFail.a. CRITERR shows the Sad Mac with the error code after a failed startup test; HAPPYMAC/SADMAC draw the Mac icon with the face, ... |
| **`CRITERR_DEADLOOP`** | — | `0x001106` | `sad_mac.s:58` | — |
| **`CRITERR_DRAW_LOW`** | — | `0x0010E6` | `sad_mac.s:45` | Draw sad Mac icon: high 8 hex digits of error code |
| **`CRITERR_ERASE`** | — | `0x0010C8` | `sad_mac.s:31` | — |
| **`CRITERR_SHOW_ICON`** | — | `0x0010FE` | `sad_mac.s:55` | — |
| **`CRITICAL`** | — | `0x000026` | `vectors.s:82` | +$26: critical-error entry: the sad Mac (CRITERR, boot/sad_mac.s). |
| **`DEAD_MAC_BLINK`** | `0x0001AC` | — | `vectors.s:333` | DEAD_MAC_BLINK - infinite loop: flash the error code on screen Writes a counter value to screen memory at SEScrnInc to create a blinking effect. The Mac is dead; only power cycle can recover. Dead Mac... |
| **`Debugger`** | `0x000806` | `0x0012C6` | `vectors.s:1247` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`DECODE_ABS_LOOP`** | — | `0x00073E` | `boot_install.s:825` | — |
| **`DECODE_ABSOLUTE`** | — | `0x00073C` | `boot_install.s:823` | — |
| **`DECODE_DISP_LOOP`** | `0x000548` | — | `vectors.s:826` | Decode compressed dispatch table from ROM into the trap tables. TrapDispatchTbl contains delta-encoded ROM offsets for each implemented trap. A0 = compressed data, A1 = current table entry, A2 = ROM b... |
| **`DECODE_DISPATCH`** | — | `0x000710` | `boot_install.s:798` | Decode compressed dispatch table from ROM |
| **`DECODE_DONE`** | — | `0x00074C` | `boot_install.s:834` | DECODE_DONE - dispatch table fully decoded; install A-line handler Selects between 68000 and 68010+ A-line trap handler based on CPU. |
| **`DECODE_NEXT`** | — | `0x000722` | `boot_install.s:809` | — |
| **`DECODE_SHORT`** | — | `0x000730` | `boot_install.s:816` | — |
| **`DETECT_CPU_TYPE`** | `0x000580` | — | `vectors.s:877` | All trap handler addresses are now installed in the OS and Toolbox dispatch tables. Next: detect CPU type (68000 vs 68020). Called during boot. Tries executing a 68020-only MOVEC instruction. If it ca... |
| **`DEVICE_LOOP_RETURN`** | `0x0007EC` | — | `vectors.s:1178` | DEVICE_LOOP_RETURN - Return from PutIcon - check if icon overlay is needed Called during boot. |
| **`DFAC_BEEP_TONE`** | — | `0x0024FE` | `memtest.s:1334` | DFAC_BEEP_TONE - beep tone generation via DFAC (Apple Sound Chip) Generates a multi-tone beep by programming the DFAC sound attenuator through the VIA shift register. Encodes D7 (4 bytes), D6 (4 bytes... |
| **`DFAC_D6_NEXT`** | — | `0x002530` | `memtest.s:1359` | — |
| **`DFAC_D7_NEXT`** | — | `0x00251A` | `memtest.s:1348` | — |
| **`DFAC_DH_NEXT`** | — | `0x00254E` | `memtest.s:1372` | — |
| **`DFAC_ENCODE_D6`** | — | `0x002522` | `memtest.s:1353` | Encode D6 error code as 4 DFAC commands (bytes 4-7) |
| **`DFAC_ENCODE_D7`** | — | `0x00250C` | `memtest.s:1342` | Encode D7 flags as 4 DFAC commands (bytes 0-3) |
| **`DFAC_ENCODE_DH`** | — | `0x002540` | `memtest.s:1366` | Encode "DH" prefix + checksum as 4 DFAC commands (bytes 8-11) |
| **`DFAC_INIT`** | — | `0x0025CC` | `memtest.s:1435` | DFAC_INIT - initialize DFAC sound attenuator Sends initial volume/mode bytes to DFAC via VIA shift register. Sets up DFAC for tone generation. |
| **`DFAC_INIT_BYTE2`** | — | `0x0025E4` | `memtest.s:1443` | — |
| **`DFAC_INIT_DESELECT`** | — | `0x0025EE` | `memtest.s:1447` | — |
| **`DFAC_SEND_CMD`** | — | `0x00257E` | `memtest.s:1405` | **Regs:** `Entry: D1 = channel (0-15), D2 = data byte`<br>DFAC_SEND_CMD - send one DFAC command (channel + data) Programs the DFAC sound attenuator with channel D1 and data D2. Builds a 3-byte command: channel address, channel address (repeated), then data b... |
| **`DFAC_SEND_DESELECT`** | — | `0x0025C0` | `memtest.s:1427` | — |
| **`DFAC_SEND_LOWBYTE`** | — | `0x0025A8` | `memtest.s:1418` | — |
| **`DFAC_TONE_INIT`** | — | `0x002508` | `memtest.s:1338` | — |
| **`DISABLEDYNWAIT`** | — | `0x001028` | `boot_search.s:495` | DISABLEDYNWAIT - disable dynamic boot wait (set bit 7) |
| **`DISABLEPERMWAIT`** | — | `0x00104C` | `boot_search.s:511` | DISABLEPERMWAIT - disable permanent boot wait (set bit 6) |
| **`DISK_NOT_BOOTABLE`** | `0x000760` | — | `vectors.s:1093` | DISK_NOT_BOOTABLE - disk not bootable or read error: eject and try next |
| **`DISK_READ_ERROR`** | `0x000754` | — | `vectors.s:1087` | DISK_READ_ERROR - disk read error: check if drive is offline or missing |
| **`DISP_ADD_DELTA`** | `0x000556` | `0x00071E` | `vectors.s:837`<br>`boot_install.s:806` | Dispatch: add delta to ROM ptr, store in table |
| **`DISP_DOUBLE_DELTA`** | `0x000550` | — | `vectors.s:832` | Dispatch: double delta for byte offset |
| **`DISP_NEXT_ENTRY`** | `0x00055A` | — | `vectors.s:841` | Dispatch: advance to next table entry |
| **`DISP_PACKED_ENTRY`** | `0x000568` | — | `vectors.s:854` | Toolbox table done (D0 reaches 0). Switch to OS table: DISP_PACKED_ENTRY - 1-byte packed dispatch entry (high bit was set) Low 7 bits: 0 = skip, 0x7F = absolute, other = short delta. Called during boo... |
| **`DISP_READ_ABSOLUTE`** | `0x000572` | — | `vectors.s:862` | 0x7F = absolute 4-byte ROM offset follows Dispatch: read 4-byte absolute offset |
| **`DISPOFF`** | — | `0x000022` | `vectors.s:79` | +$1E: eject entry (Apple: Eject; the label EJECT is the _Eject trap). DOEJECT ejects a disk, first asking the EjectNotify hook. +$22: offset of the compressed trap dispatch table; INITDISPATCHER (boot... |
| **`DRAW_FACE_OVERLAY`** | `0x000F16` | — | `sad_mac.s:90` | DRAW_FACE_OVERLAY - overlay the face expression onto the Mac icon Called during boot. |
| **`DRAW_MAC_FACE`** | — | `0x001196` | `sad_mac.s:122` | — |
| **`DRAW_MAC_ICON`** | `0x000F04` | `0x001180` | `sad_mac.s:78`<br>`sad_mac.s:115` | DRAW_MAC_ICON - common icon drawing: decode Macintosh outline + overlay face |
| **`DRAW_MAC_RETURN`** | — | `0x0011A8` | `sad_mac.s:128` | — |
| **`DRAW_OR_ERASE_ICON`** | `0x0007B0` | — | `vectors.s:1139` | Draw or erase icon (toggle on D4 bit) |
| **`DRAWBEEPSCREEN`** | — | `0x0001DA` | `boot_install.s:203` | DRAWBEEPSCREEN - draw the startup rounded-rectangle screen Uses QuickDraw to draw a 3-pixel rounded-rect border inset from the screen edge, with a filled rounded-rect pattern inside. A5 = QD globals w... |
| **`DRIVE_FAILED`** | `0x000772` | — | `vectors.s:1104` | DRIVE_FAILED - drive failed: remove from boot mask and try next |
| **`DSAT_NOT_FOUND`** | `0x000BAC` | — | `boot_load.s:265` | DSAT_NOT_FOUND - DSAT not found - continue boot without alert table |
| **`DT_HEX_FONT`** | `0x0001BA` | `0x001146` | `vectors.s:345`<br>`sad_mac.s:97` | DT_HEX_FONT - Hex digit font table - 16 glyphs x 3 bytes each for error code display |
| **`DT_INITZONE_PARAMS`** | `0x000946` | — | `boot_install.s:204` | DT_INITZONE_PARAMS - InitZone parameter block (28 bytes) Configures the initial system heap zone: start, limit, grow proc, master count. Fields: Lo3Bytes mask, startPtr, limitPtr, cMoreMasters, pGrowZ... |
| **`DT_mHappyMac`** | `0x000FD2` | `0x00125C` | `sad_mac.s:157`<br>`sad_mac.s:208` | — |
| **`DT_mQMark`** | `0x000FFA` | — | `sad_mac.s:169` | — |
| **`DT_mSadMac`** | `0x000FE6` | `0x001270` | `sad_mac.s:163`<br>`sad_mac.s:214` | — |
| **`DT_mXMark`** | `0x001018` | — | `sad_mac.s:176` | — |
| **`DT_SCC_INIT_DATA`** | `0x00080C` | `0x000578` | `boot_install.s:31`<br>`boot_install.s:622` | Boot-time I/O and manager setup (SCC reset, jump-table setup, driver install, GNEFilter, system zone) Corresponds to the end of Apple's StartInit.a (the SE link map's INITSCC ... INITMEMMGR). Reached ... |
| **`DT_SONY_NAME`** | `0x00086E` | `0x0007BC` | `boot_install.s:90`<br>`boot_install.s:886` | DT_SONY_NAME - Pascal string ".Sony" - Sony disk driver name |
| **`DT_SOUND_NAME`** | `0x000874` | `0x0007C2` | `boot_install.s:95`<br>`boot_install.s:890` | Pascal string: ".Sound" driver name |
| **`DT_SWITCHER_PARAMS`** | `0x000672` | — | `vectors.s:996` | DT_SWITCHER_PARAMS - default Switcher parameter table (32 bytes) Copied to SwitcherTPtr at boot. Controls task switching behavior. |
| **`DTAB_INITZONE`** | — | `0x0001CC` | `boot_install.s:193` | DTAB_INITZONE - InitZone parameter block (14 bytes) startPtr=$1600, limitPtr=$2E00, cGrowZone=$400000, cMoreMasters=0 |
| **`DTAB_INTERNALWAIT`** | — | `0x000CF4` | `boot_search.s:73` | DTAB_INTERNALWAIT - jump table for _InternalWait selectors 0-9 Each entry is a word offset from the table base to the handler. |
| **`DTAB_MICKEY`** | — | `0x00065E` | `boot_install.s:718` | Install cursor J-vectors (JHideCursor..JInitCrsr) DTAB_MICKEY - default mouse acceleration table data (8 bytes) |
| **`E_SoftReset`** | `0x0003A8` | — | `vectors.s:662` | Also reached via reset button (ROM entry table at offset +E). Sets up the system stack and initializes critical low-memory globals. |
| **`EBootStart`** | `0x00002A` | — | `vectors.s:73` | The initial SP value (checksum) is an invalid address - real SP is set up later after RAM sizing. It doubles as the ROM checksum word. ROM entry points table (addresses relative to ROM base): State: a... |
| **`EJECT_DISK`** | `0x000762` | — | `vectors.s:1096` | EJECT_DISK - eject disk (also used when mouse button held down) |
| **`EJECT_WARM_RESTART`** | `0x000BA8` | — | `boot_load.s:258` | Eject OK - warm restart |
| **`EJECTME`** | — | `0x000E86` | `boot_search.s:300` | EJECTME - eject disk from currently selected drive |
| **`EMBARK_SAVE_TIME`** | — | `0x000D1C` | `boot_search.s:94` | — |
| **`EMBARKONSEARCH`** | — | `0x000D04` | `boot_search.s:83` | EMBARKONSEARCH - initialize boot device search state Reads default startup device from XPRAM, sets up the candidate filter function (ISITFLOPORDEF for specific device, ISITANYTHING for any bootable de... |
| **`ENABLE_INTERRUPTS`** | `0x00063E` | — | `vectors.s:975` | Initialize Drive Queue and I/O Manager Third diagnostic ROM checkpoint at 0xF80088 ENABLE_INTERRUPTS All hardware is initialized, drivers installed, Resource Manager open. Now enable interrupts, init ... |
| **`ENABLEDYNWAIT`** | — | `0x00103A` | `boot_search.s:503` | ENABLEDYNWAIT - enable dynamic boot wait (clear bit 7) |
| **`ENABLEPERMWAIT`** | — | `0x00105E` | `boot_search.s:519` | ENABLEPERMWAIT - enable permanent boot wait (clear bit 6) |
| **`ENABLEXFLASH`** | — | `0x000E6C` | `boot_search.s:285` | ENABLEXFLASH - enable the X-flash animation on next cycle |
| **`ERASE_SCRN_LOOP`** | `0x0001F0` | — | `vectors.s:364` | Screen erase loop body |
| **`EraseScrnBuff`** | `0x0001EA` | — | `vectors.s:360` | EraseScrnBuff - fill screen buffer with all 1s (white) A2 = screen buffer start address (0x3FA700 = ScreenLow) A6 = return address (callee-saves pattern, no stack available yet) Fills 0x1560 longwords... |
| **`ERRORBEEP1`** | — | `0x002AB4` | `memtest.s:2131` | ERRORBEEP3 - error beep return stub (used by boot error paths) |
| **`ERRORBEEP2`** | — | `0x002AB4` | `memtest.s:2130` | ERRORBEEP3 - error beep return stub (used by boot error paths) |
| **`ERRORBEEP3`** | — | `0x002AB4` | `memtest.s:2132` | ERRORBEEP3 - error beep return stub (used by boot error paths) |
| **`EXCEPTIONHANDLER`** | — | `0x001BCA` | `memtest.s:266` | EXCEPTIONHANDLER - common exit of the handlers (Apple: ExceptionHandler; the 1992 version goes to CritErr instead). Sets D7 bit 24 (STEqu.a: excp, "unexpected exception received"). After an NMI (D7 bi... |
| **`EXCEPTIONHANDLER_RTE`** | — | `0x001BDC` | `memtest.s:272` | — |
| **`EXEC_PATCH1`** | — | `0x000962` | `boot_load.s:158` | Load and execute boot code patches from boot block names |
| **`FCB_COUNT_READY`** | `0x000CA4` | — | `boot_load.s:431` | FCB count ready - allocate arrays |
| **`FDHD_ColdStartPatchHook`** | — | — | `memtest.s:350` | — |
| **`FDHD_RAMTEST_OFFSET`** | — | — | `memtest.s:353` | — |
| **`FILE_LOAD_RETURN`** | `0x000C32` | `0x000AF8` | `boot_load.s:353`<br>`boot_load.s:346` | Return result code from file load |
| **`FILL_EVTBUF_LOOP`** | `0x000D66` | `0x000C7E` | `boot_load.s:513`<br>`boot_load.s:522` | Fill event buffer with 0xFFFF (free markers) |
| **`FILL_LOOP`** | `0x000E82` | `0x000186` | `memtest.s:197`<br>`boot_install.s:155` | Fill loop: writes pattern from both ends simultaneously A0 ascends writing D2-D4 (12 bytes), A1 descends writing D4-D6 (12 bytes) |
| **`FILL_LVL1DT`** | — | `0x0003A2` | `boot_install.s:390` | — |
| **`FILL_LVL1DT_LOOP`** | `0x0004C8` | — | `vectors.s:759` | Fill Lvl1DT with default RTS handler |
| **`FILL_OS_DISP`** | `0x000530` | `0x0006F4` | `vectors.s:808`<br>`boot_install.s:788` | Fill OS dispatch table loop |
| **`FILL_TOOL_DISP`** | `0x000522` | `0x0006E6` | `vectors.s:802`<br>`boot_install.s:783` | Fill Toolbox dispatch table loop |
| **`FILLWITHONES`** | — | `0x00017E` | `boot_install.s:150` | FILLWITHONES - fill memory range [A0..A1) with 0xFFFFFFFF A0 = start address, A1 = end address Used during boot to clear low memory before globals are set up. |
| **`FINDNEXTCANDIDATE`** | — | `0x000DA6` | `boot_search.s:175` | FINDNEXTCANDIDATE - find next bootable device in drive queue Walks drive queue via NEXTDQENTRY, skipping rejected drives (ISREJECT) and drives that don't match the filter (A3 callback). Returns Z=1 if... |
| **`FINDSTARTUPDEVICE`** | — | `0x000C8E` | `boot_search.s:22` | Startup: choosing the startup device (StartSearch) Apple source: StartSearch.a. FINDSTARTUPDEVICE walks the drive queue in the order set by the startup-device preference in extended parameter RAM (GET... |
| **`FORMATX`** | — | `0x001B50` | `memtest.s:199` | — |
| **`FPCP1`** | — | `0x001B90` | `memtest.s:230` | — |
| **`FPCP2`** | — | `0x001B96` | `memtest.s:233` | — |
| **`FPCP3`** | — | `0x001B9C` | `memtest.s:236` | — |
| **`FPCP4`** | — | `0x001BA2` | `memtest.s:239` | — |
| **`FPCP5`** | — | `0x001BA8` | `memtest.s:242` | — |
| **`FPCP6`** | — | `0x001BAE` | `memtest.s:245` | — |
| **`FPCP7`** | — | `0x001BB4` | `memtest.s:248` | — |
| **`GETDEFAULTSTARTUP`** | — | `0x000CC8` | `boot_search.s:47` | GETDEFAULTSTARTUP - read default startup device from XPRAM Reads 4 bytes from XPRAM offset $78 (startup device record). |
| **`GETPRAM`** | — | `0x000358` | `boot_install.s:344` | GETPRAM - read PRAM settings for keyboard and mouse timing Reads SPKbd (key repeat speed) and SPClikCaret (double-click and caret blink rate) from PRAM, decodes packed nibble fields, and sets KeyRepTh... |
| **`GETRAWTIMEOUT`** | — | `0x001070` | `boot_search.s:528` | GETRAWTIMEOUT - read raw timeout byte from XPRAM offset $01 |
| **`GETSTARTUP_RTS`** | — | `0x000E12` | `boot_search.s:233` | — |
| **`GETSTARTUPINFO`** | — | `0x000DF4` | `boot_search.s:225` | GETSTARTUPINFO - read boot blocks (1K) from selected device Reads 1024 bytes from sector 0 into A6 buffer. Checks for boot signature 'LK' ($4C4B) at start of boot blocks. Returns Z=1 if valid boot blo... |
| **`GETTIMEOUT`** | — | `0x000FE2` | `boot_search.s:460` | GETTIMEOUT - get boot wait timeout (low 5 bits of raw timeout) |
| **`GETWAITFLAGS`** | — | `0x001008` | `boot_search.s:479` | GETWAITFLAGS - get boot wait flags (high 3 bits of raw timeout) |
| **`GLYPH_DRAW_LOOP`** | `0x00017E` | `0x00111E` | `vectors.s:313`<br>`sad_mac.s:73` | GLYPH_DRAW_LOOP - draw one glyph byte as two scanlines |
| **`GNE_FILTER_DONE`** | `0x000944` | `0x0006D8` | `boot_install.s:198`<br>`boot_install.s:767` | Return from GNEFilter |
| **`GNEFILTER`** | — | `0x000666` | `boot_install.s:728` | GNEFILTER - GetNextEvent filter (alarm menu flash + beep) Installed in GNEFilter low-mem vector. Called on every GetNextEvent. Checks if alarm is armed and ready to flash the Apple menu bar area. If s... |
| **`GOT_DSAT`** | — | `0x000922` | `boot_load.s:134` | — |
| **`HAPPYMAC`** | — | `0x001176` | `sad_mac.s:110` | HAPPYMAC / SADMAC (sad Mac) - draw Mac icon with face HAPPYMAC draws happy face, SADMAC draws sad face. Both draw ICON_MAC_OUTLINE first, then overlay face bitmap. |
| **`HAPPYMAC_SHOWN`** | `0x00074C` | — | `vectors.s:1081` | HAPPYMAC_SHOWN - Happy Mac shown, now boot from the disk Called during boot. |
| **`HEX_DIGIT_LOOP`** | `0x00016A` | `0x00110A` | `vectors.s:304`<br>`sad_mac.s:65` | HEX_DIGIT_LOOP - hex digit rendering loop: draw one digit per iteration |
| **`ICON_BIT_LOOP`** | `0x000ED0` | — | `sad_mac.s:35` | — |
| **`ICON_BYTE_COUNT`** | `0x000EDC` | — | `sad_mac.s:49` | — |
| **`ICON_COPY_BYTE`** | `0x000EDA` | — | `sad_mac.s:47` | ICON_COPY_BYTE - copy one data byte from icon source to screen Called during boot. |
| **`ICON_DISK`** | `0x000FA2` | `0x000FB2` | `sad_mac.s:147`<br>`boot_search.s:449` | ICON_DISK - floppy disk icon bitmap (used during boot search) ICON_DISK bitmap data (26 bytes, floppy disk icon) |
| **`ICON_DRAW_DONE`** | `0x000802` | — | `vectors.s:1193` | ICON_DRAW_DONE ICON_DRAW_DONE - icon drawing complete, show cursor and return Called during boot. |
| **`ICON_DRAW_RETURN`** | `0x000F26` | — | `sad_mac.s:101` | ICON_DRAW_RETURN - return from icon drawing chain Called during boot. |
| **`ICON_MAC_OUTLINE`** | `0x000F3E` | `0x0011F8` | `sad_mac.s:128`<br>`sad_mac.s:182` | ICON_MAC_OUTLINE - compressed Macintosh computer outline icon (32x32, delta-encoded) Decoded by PutIcon into a 32-pixel-wide icon at SEScrnIcon. |
| **`ICON_NEXT_ROW`** | `0x000EE8` | — | `sad_mac.s:60` | ICON_NEXT_ROW - advance to next icon row; after all rows, XOR-propagate Called during boot. |
| **`ICON_ROW_LOOP`** | `0x000ECA` | — | `sad_mac.s:32` | — |
| **`ICON_XOR_PROPAGATE`** | `0x000EF0` | `0x0011E8` | `sad_mac.s:65`<br>`sad_mac.s:171` | XOR each row with the previous to reconstruct delta-encoded image |
| **`ILLEGAL_INSN_TRAP`** | `0x00059A` | — | `vectors.s:892` | ILLEGAL_INSN_TRAP - illegal instruction handler (MOVEC failed = not 68020) Check exception frame format to distinguish 68000 from 68010. Called during boot. |
| **`ILLERROR`** | — | `0x001B02` | `memtest.s:169` | — |
| **`INBOOTMASK`** | — | `0x000EF4` | `boot_search.s:367` | INBOOTMASK - check if drive type is tracked in BootMask Returns Z=1 if floppy/HD20/SCSI with drive# <= 15, NZ otherwise. |
| **`INBOOTMASK_CHK`** | — | `0x000F06` | `boot_search.s:374` | — |
| **`INBOOTMASK_RTS`** | — | `0x000F10` | `boot_search.s:378` | — |
| **`INIT_FONTS`** | — | `0x000928` | `boot_load.s:137` | — |
| **`INIT_FONTS_BUFS`** | `0x000A5C` | — | `boot_load.s:114` | Load the system error alert table ('DSAT' resource ID 0) Initialize Font Manager and allocate system buffers |
| **`INIT_HW_GLOBALS`** | `0x0003F8` | — | `vectors.s:687` | Detect SCSI: compare ROM at two mirror addresses. If 0x420000 = 0x440000, ROM mirrors (no SCSI chip present). Store HW base addresses, init I/O and globals |
| **`INIT_IOMGR_DONE`** | `0x0008D0` | `0x0007BA` | `boot_install.s:149`<br>`boot_install.s:883` | Load and execute the serial driver resource ('SERD' 0) This installs the .AIn/.AOut/.BIn/.BOut serial port drivers. Return from InitIOMgr |
| **`INIT_LOAD_DONE`** | — | `0x0009CA` | `boot_load.s:205` | INIT not found for this ID: restore regs, try next ID |
| **`INIT_LOAD_LOOP`** | `0x000AD0` | `0x0009A4` | `boot_load.s:169`<br>`boot_load.s:189` | Load and execute 'INIT' resources 0 through 35 ($24). These are startup code from the System file and extensions. INIT load/execute loop (IDs 0-35) |
| **`INIT_MANAGERS`** | — | `0x0000CE` | `boot_install.s:86` | INIT_MANAGERS - initialize high-memory globals, then all system managers |
| **`INIT_MEMORY_MAP`** | `0x00037E` | — | `vectors.s:647` | INIT_MEMORY_MAP - set up memory map: MemTop, sound buffers, screen buffer A5 = top of RAM (from memory test). Memory layout from top down: MemTop (A5) MemTop - 0x2FF: PWM sound buffer (767 bytes) MemT... |
| **`INIT_NEXT`** | `0x000AF6` | — | `boot_load.s:184` | Restore globals after INIT, try next |
| **`INIT_NOT_FOUND`** | `0x000B7C` | — | `boot_load.s:241` | INIT_NOT_FOUND - INIT resource not found: skip and try next ID |
| **`INIT_QUICKDRAW`** | `0x000692` | — | `vectors.s:1006` | This is where the screen first shows something other than white. |
| **`INIT_SYS_ZONE`** | `0x000962` | — | `boot_install.s:213` | INIT_SYS_ZONE - initialize system heap zone from DT_INITZONE_PARAMS parameters Copies DT_INITZONE_PARAMS data to low-memory zone config area, then calls _InitZone. |
| **`INIT_VIA_PORT_A`** | `0x0000BC` | — | `vectors.s:195` | INIT_VIA_PORT_A - configure VIA port A with volume and system flags Trace: D2 = speaker volume (bits 0-2) from PRAM or default. D4 = volume bits extracted from D2. Called during boot. |
| **`INITADBVARS`** | — | `0x000228` | `boot_install.s:233` | INITADBVARS - initialize Apple Desktop Bus manager variables Allocates 370 bytes ($172) for ADB data structures and installs the FDB shift-register interrupt handler into VIA level-1 dispatch. |
| **`INITCRSRMGR`** | — | `0x0005F6` | `boot_install.s:685` | INITCRSRMGR - initialize Cursor Manager Sets up mouse position, screen bounds, mickey-to-pixel table, and installs cursor J-vectors for QuickDraw. |
| **`INITCRSRVARS`** | — | `0x0005E6` | `boot_install.s:673` | INITCRSRVARS - clear QuickDraw cursor globals Zeros the range from JHideCursor through WWExist-1. |
| **`INITDISPATCHER`** | — | `0x0006DA` | `boot_install.s:779` | INITDISPATCHER - build A-line trap dispatch tables Fills ToolTable (512 entries) and DispatchTab (256 entries) with P_tUnimplemented, then decodes the compressed dispatch table from ROM to populate ac... |
| **`InitEvents`** | `0x000D4C` | `0x000C64` | `boot_load.s:499` | _InitEvents ($A06D) Called during boot. |
| **`INITEVENTS`** | `0x000D4C` | `0x000C64` | `boot_load.s:508` | INITEVENTS - initialize Event Manager (create event queue) D0 = number of event buffer slots (from boot block). Allocates D0 * 22 bytes, fills with $FFFF (free markers), and sets up the event queue he... |
| **`InitFS`** | `0x000C7A` | `0x000B7A` | `boot_load.s:416` | _InitFS ($A06C) Called during boot. |
| **`INITFS`** | `0x000C7A` | `0x000B7A` | `boot_load.s:418` | INITFS - initialize File System (HFS boot-time setup) Allocates FCB table, WDCB table, HFS stack, block cache buffers. D0 = number of file buffers (from boot block). Called via _InitFS trap during boo... |
| **`INITFS_ALLOC_FAIL`** | `0x000C76` | — | `boot_load.s:407` | INITFS_ALLOC_FAIL - _InitFS allocation failed - return -1 |
| **`INITFS_ALLOC_FCB`** | — | `0x000BA4` | `boot_load.s:431` | — |
| **`INITFS_DONE`** | `0x000D48` | — | `boot_load.s:490` | InitFS complete - return noErr |
| **`INITFS_FAIL`** | — | `0x000C60` | `boot_load.s:500` | Called by: INITFS_ALLOC_FCB, ALLOC_VOL_CACHE, ALLOC_CTL_CACHE |
| **`INITFS_OK`** | — | `0x000C5C` | `boot_load.s:496` | — |
| **`INITGLOBALVARS`** | — | `0x000262` | `boot_install.s:262` | INITGLOBALVARS - initialize low-memory global variables Sets ROMBase, hardware flags, I/O vectors, initializes all hardware-specific globals, clears system state variables. HWCfgFlags $C400 = bit 15 (... |
| **`INITHIMEMGLOBALS`** | — | `0x00023C` | `boot_install.s:245` | INITHIMEMGLOBALS - set up high-memory globals (sound buffers, BufPtr) Allocates sound buffers just below MemTop, then sets BufPtr below the sound area. Memory layout (top down): MemTop -> [767 bytes P... |
| **`InitIOMgr`** | `0x00087C` | `0x00076E` | `boot_install.s:100` | Allocate Unit Table, open .Sony/.Sound, load SERD |
| **`INITIOMGR`** | `0x00087C` | `0x00076E` | `boot_install.s:856` | INITIOMGR - allocate Unit Table, open ROM drivers, load SERD Allocates a 64-entry Unit Table, opens .Sony and .Sound drivers, then loads and executes the SERD 0 resource (serial drivers). |
| **`INITIWM`** | — | `0x0004F0` | `boot_install.s:544` | INITIWM - initialize the floppy disk controller (Apple's InitIWM): set the IWM mode register to $17 (IWMInitMode in Apple's HardwarePrivateEqu.a) = latch mode, asynchronous handshake, 1-second timer o... |
| **`INITIWMGLOBALS`** | — | `0x0004E6` | `boot_install.s:529` | INITIWMGLOBALS - set the low-memory pointer IWM to the floppy disk controller (the IWM; the SWIM of the SE FDHD sits at the same place). It is on the low data byte (odd addresses); its address lines A... |
| **`INITMEMMGR`** | — | `0x0007CA` | `boot_install.s:895` | INITMEMMGR - initialize Memory Manager low-memory globals |
| **`INITRSRCMGR`** | — | `0x0007E8` | `boot_install.s:903` | INITRSRCMGR - initialize Resource Manager (ROM resource map) |
| **`InitSCC`** | `0x00082C` | `0x000598` | `boot_install.s:43` | Writes 17 register bytes from DT_SCC_INIT_DATA to each channel (B then A). Configures: async mode, 8-bit data, 1 stop bit, no parity, external/status interrupts enabled (for mouse DCD tracking). |
| **`INITSCC`** | `0x00082C` | `0x000598` | `boot_install.s:636` | INITSCC - reset and configure the Zilog 8530 SCC Writes 17 register bytes to each channel (B then A) from DT_SCC_INIT_DATA. Configures: async mode, 8-bit data, 1 stop bit, external/status interrupts e... |
| **`INITSCCGLOBALS`** | — | `0x000562` | `boot_install.s:588` | INITSCCGLOBALS - set SCC base addresses and clear poll proc |
| **`INITSCSI`** | — | `0x0004CE` | `boot_install.s:517` | INITSCSI - reset NCR 5380 SCSI controller Clears the four control registers (ICR, MR, TCR, SER) by writing 0 to offsets $10, $20, $30, $40 from base + 1. |
| **`INITSCSIGLOBALS`** | — | `0x0004B4` | `boot_install.s:508` | INITSCSIGLOBALS - set SCSI controller base addresses in low memory NCR 5380 at $5FF000 (base), $5FF200 (DMA/handshake). |
| **`INITSWITCHERTABLE`** | — | `0x000344` | `boot_install.s:330` | INITSWITCHERTABLE - allocate and init Switcher context table Copies 52-byte SWITCHGOODIES template to a system heap block and stores the pointer in SwitcherTPtr low-mem global. |
| **`INITTIMERMGR`** | — | `0x0007F8` | `boot_install.s:913` | INITTIMERMGR - initialize Time Manager Allocates 18 bytes for timer variables, inits the timer queue. |
| **`INITVIA`** | — | `0x00052A` | `boot_install.s:571` | INITVIA - initialize VIA 6522 peripheral interface Sets port A output (volume, overlay, drive select), port B direction (RTC, sound, mouse), clears pending interrupts. |
| **`INITVIAGLOBALS`** | — | `0x000520` | `boot_install.s:564` | INITVIAGLOBALS - set VIA base address in low memory |
| **`INITVIDGLOBALS`** | — | `0x0005CA` | `boot_install.s:664` | INITVIDGLOBALS - initialize video/screen globals SE FDHD: 512x342 built-in display, 64 bytes/row, 60 Hz. |
| **`INITXVECTTABLES`** | — | `0x000396` | `boot_install.s:385` | INITXVECTTABLES - install interrupt dispatch vector tables Sets up three vector tables in low memory: Lvl1DT[0..15] - VIA interrupt dispatch (16 slots) slot 0 = ONESECINT (one-second timer) slot 1 = V... |
| **`INSTALL_ALINE`** | — | `0x000762` | `boot_install.s:842` | — |
| **`INSTALL_ATRAP`** | `0x0005B8` | — | `vectors.s:909` | Install A-line trap dispatcher based on CPU type. 68020 uses a faster dispatch path with cache instructions. Install A-line handler, begin manager init |
| **`INTERNALWAIT`** | — | `0x000CDC` | `boot_search.s:61` | INTERNALWAIT - dispatch to boot-time wait subroutine by selector A0 = selector (0-9). Dispatches through DTAB_INTERNALWAIT jump table. Used by _InternalWait trap during boot. |
| **`INTERNALWAIT_RTS`** | — | `0x000CF2` | `boot_search.s:69` | — |
| **`INTLEVEL1`** | — | `0x001B62` | `memtest.s:208` | — |
| **`INTLEVEL2`** | — | `0x001B68` | `memtest.s:211` | — |
| **`INTLEVEL3`** | — | `0x001B6E` | `memtest.s:214` | — |
| **`INTLEVEL4`** | — | `0x001B74` | `memtest.s:217` | — |
| **`INTLEVEL5`** | — | `0x001B7A` | `memtest.s:220` | — |
| **`INTLEVEL6`** | — | `0x001B80` | `memtest.s:223` | — |
| **`INTLEVEL7`** | — | `0x001B86` | `memtest.s:226` | — |
| **`ISITANYTHING`** | — | `0x000EDE` | `boot_search.s:350` | ISITANYTHING - filter: accept any drive (always returns Z=1) |
| **`ISITFLOPDEF_RTS`** | — | `0x000EB8` | `boot_search.s:328` | — |
| **`ISITFLOPORDEF`** | — | `0x000EA6` | `boot_search.s:321` | ISITFLOPORDEF - filter: is this the default device or a floppy? Checks if drive matches XPRAM default (D4=refNum, D3=driveNum) or is the internal floppy ($FFFB). |
| **`ISITFLOPPY`** | — | `0x000EBA` | `boot_search.s:332` | ISITFLOPPY - filter: is this a floppy drive? (refNum $FFFB) |
| **`ISITHD20`** | — | `0x000EC2` | `boot_search.s:336` | ISITHD20 - filter: is this an HD20? (refNum $FFFE) |
| **`ISITSCSI`** | — | `0x000ECA` | `boot_search.s:340` | ISITSCSI - filter: is this a SCSI device? (refNum $FFD8-$FFDF) |
| **`ISITSCSI_NO`** | — | `0x000EDC` | `boot_search.s:347` | — |
| **`ISREJECT`** | — | `0x000E94` | `boot_search.s:309` | ISREJECT - check if drive should be rejected from boot search Returns Z=0 if drive is OK, Z=1 if rejected (not in BootMask or already tried and failed). |
| **`ISREJECT_RTS`** | — | `0x000EA4` | `boot_search.s:315` | — |
| **`IWM_INIT_DONE`** | `0x000126` | `0x00051A` | `vectors.s:258`<br>`boot_install.s:559` | IWM_INIT_DONE - IWM initialized, now checksum ROM and test RAM This is the main memory test call. On success (Z flag set), continues to BootPart2. On failure, falls through to CritErr (sad Mac icon). ... |
| **`IWM_INIT_LOOP`** | `0x000104` | `0x0004F8` | `vectors.s:240`<br>`boot_install.s:547` | motor off; mode bits 0-4 read back in the status; write only with motor off |
| **`JMPTBL2`** | — | `0x000170` | `boot_install.s:139` | — |
| **`JmpTblInit`** | `0x00085E` | `0x00016E` | `boot_install.s:75` | A0 = source table (word offsets relative to table start) A1 = destination (longword addresses to fill) D1 = number of entries - 1 Called during boot. |
| **`JMPTBLINIT`** | `0x00085E` | `0x00016E` | `boot_install.s:137` | JMPTBLINIT - convert ROM-relative offset table to absolute addresses A0 = source table (word offsets relative to table start) A1 = destination (longword addresses to fill) D1 = number of entries - 1 |
| **`L_mJmpTbl2`** | `0x000860` | — | `boot_install.s:78` | Offset-to-address conversion loop |
| **`LAUNCH_APP`** | `0x000B5E` | `0x000A42` | `boot_load.s:225`<br>`boot_load.s:247` | Set speaker volume from PRAM via .Sound driver control call Set up Scrap Manager (clipboard) and copy Finder name from boot block Try the startup application first (boot block +$5A), fall back to Find... |
| **`LAUNCH_FAILED`** | `0x000B76` | — | `boot_load.s:236` | If we get here, _Launch returned - that means it failed. |
| **`LAUNCH_FINDER`** | — | `0x00098A` | `boot_load.s:177` | LAUNCH_FINDER - final boot: init ADB driver, mouse, launch app |
| **`LINEA`** | — | `0x001B32` | `memtest.s:187` | — |
| **`LINEF`** | — | `0x001B3A` | `memtest.s:190` | — |
| **`LOAD_DSAT_RESOURCE`** | — | `0x00090E` | `boot_load.s:125` | LOAD_DSAT_RESOURCE - load system error alert table ('DSAT' 0) |
| **`LOAD_MCKY_RSRC`** | — | `0x000B58` | `boot_load.s:398` | — |
| **`LOAD_TO_BOOTBUF`** | `0x000C36` | — | `boot_load.s:361` | LOAD_TO_BOOTBUF - D3 > 0: load into boot block buffer area (+$800) |
| **`LOADDRIVERS`** | — | `0x000D86` | `boot_search.s:151` | LOADDRIVERS - load SCSI device drivers Checks keyboard for Cmd-Opt-Shift-Delete to skip SCSI drivers. D0 = -2 if skip requested, -1 for normal load. |
| **`LOADDRVR_CALL`** | — | `0x000D94` | `boot_search.s:157` | — |
| **`MEMSIZE_BUS_DONE`** | — | `0x002678` | `memtest.s:1526` | — |
| **`MEMSIZE_BUS_LOOP`** | — | `0x002644` | `memtest.s:1501` | — |
| **`MEMSIZE_BUS_OK`** | — | `0x002670` | `memtest.s:1522` | — |
| **`MEMSIZE_DO_PROBE`** | — | `0x002616` | `memtest.s:1471` | — |
| **`MEMSIZE_PROBE_BUS`** | — | `0x002628` | `memtest.s:1486` | MEMSIZE_PROBE_BUS - RAM probe subroutine: write pattern, verify readback Writes rotating patterns at the probe address (D0 << 16) and checks all 4 byte lanes for data bus integrity. Address A4 is a re... |
| **`MEMSIZE_PROBE_NEXT`** | — | `0x002602` | `memtest.s:1461` | — |
| **`MEMSIZE_PROBE_RESULT`** | — | `0x002620` | `memtest.s:1475` | — |
| **`MEMSIZE_PROBE_TBL`** | — | `0x00267A` | `memtest.s:1532` | MEMSIZE_PROBE_TBL - RAM size probe table Each byte is a RAM size code (shifted left 16 to form address). Table: 0x08, 0x10, 0x20, 0x28, 0x40, terminated by 0xFF. Corresponds to sizes: 512K, 1M, 2M, 2.... |
| **`MEMSIZE_REF_TBL`** | — | `0x002680` | `memtest.s:1537` | MEMSIZE_REF_TBL - reference addresses for mirror detection Each longword is the RAM address to monitor for aliasing. |
| **`MEMSIZE_RETURN`** | — | `0x002626` | `memtest.s:1479` | — |
| **`MEMTEST`** | — | `0x0019E8` | `memtest.s:80` | Startup tests: RAM test, Test Manager, SysBeep/BootBeep Apple sources: the startup test code (System 7.1: USTStartUp.a, USTTestMgr.a and their includes; MacSEROM.lst lists these routines in the SYSTEM... |
| **`MEMTEST0_FILL_INIT`** | — | `0x002712` | `memtest.s:1616` | Calculate iteration counts for 12-byte MOVEM fill (64K outer x inner) |
| **`MEMTEST0_FILL_LOOP`** | — | `0x00271C` | `memtest.s:1621` | Fill loop: write 12 bytes at a time using MOVEM |
| **`MEMTEST0_VERIFY_LOOP_F1`** | — | `0x002750` | `memtest.s:1646` | — |
| **`MEMTEST0_VERIFY_LOOP_F2`** | — | `0x002762` | `memtest.s:1655` | Verify phase: cascading XOR propagation (forward pass 2) |
| **`MEMTEST0_VERIFY_PASS1`** | — | `0x00273C` | `memtest.s:1637` | Handle tail bytes (range not multiple of 12): write remaining 4 or 8 Verify phase: cascading XOR propagation (forward pass 1) |
| **`MEMTEST_LOOP`** | `0x000030` | — | `vectors.s:85` | MEMTEST_LOOP - repeated memory test loop (not used on Mac Plus) Loops SP times: each iteration checksums ROM and tests RAM. |
| **`MEMTEST_LOOP_RET`** | `0x000038` | — | `vectors.s:96` | MEMTEST_LOOP_RET - return from memory test; loop or continue boot Z=0 on failure (bad RAM or ROM checksum mismatch). SP doubles as an iteration counter: decrement on each successful pass, loop back to... |
| **`MEMTEST_RAM_RET`** | — | `0x001CA8` | `memtest.s:356` | — |
| **`MEMTEST_RETURN`** | `0x000E36` | — | `memtest.s:147` | — |
| **`MEMTEST_REV_FILL_INIT`** | — | `0x0027C8` | `memtest.s:1707` | Calculate iteration counts (same as P_TestMemory0) |
| **`MEMTEST_REV_FILL_LOOP`** | — | `0x0027D2` | `memtest.s:1712` | Reverse fill: write 12 bytes at a time descending from end |
| **`MEMTEST_REV_PATTERN`** | — | `0x002846` | `memtest.s:1766` | Compare first 12 bytes against expected pattern MEMTEST_REV_PATTERN - 12-byte test pattern for MEMTEST_REVERSE (reverse test) |
| **`MEMTEST_REV_VERIFY_INIT`** | — | `0x0027F0` | `memtest.s:1727` | Handle head tail bytes (if range not multiple of 12) Reverse verify: cascading XOR propagation (backward pass 1) |
| **`MEMTEST_REV_VERIFY_LOOP_B1`** | — | `0x002804` | `memtest.s:1736` | — |
| **`MEMTEST_REV_VERIFY_LOOP_B2`** | — | `0x002818` | `memtest.s:1746` | Reverse verify: cascading XOR propagation (backward pass 2) |
| **`MEMTEST_REVERSE`** | — | `0x0027A6` | `memtest.s:1690` | **Regs:** `Entry: A0 = start, A1 = end Exit: D6 = error bits (0 = pass)`<br>MEMTEST_REVERSE - reverse-direction memory test (pattern fill + XOR verify) Same algorithm as P_TestMemory0 but fills from end to start using MOVEM -(A3) and verifies backwards. Tests for direction-se... |
| **`MEMTEST_ZEROONES`** | — | `0x0028CA` | `memtest.s:1840` | **Regs:** `Entry: A0 = start, A1 = end Exit: D6 = error bits (0 = pass)`<br>MEMTEST_ZEROONES - multi-pass zero/ones RAM test Five-pass test: fill with 0, verify 0, XOR to all-1s, verify all-1s (forward+backward), then verify zeros again. Tests for stuck bits, coupling faults,... |
| **`MEMTEST_ZO_FAULT`** | — | `0x002918` | `memtest.s:1894` | MEMTEST_ZO_FAULT - test failure: accumulate error bits Called by: MEMTEST_ZO_PASS2, MEMTEST_ZO_REVERIFY_BACK, MEMTEST_ZO_PASS4, MEMTEST_ZO_PASS5, MEMTEST_ZO_FINAL_VERIFY |
| **`MEMTEST_ZO_FILL_LOOP`** | — | `0x0028D8` | `memtest.s:1849` | Pass 1: fill entire range with zeros (forward) |
| **`MEMTEST_ZO_FINAL_VERIFY`** | — | `0x00290E` | `memtest.s:1886` | Pass 6: final verify zeros (forward) |
| **`MEMTEST_ZO_PASS2`** | — | `0x0028E2` | `memtest.s:1856` | Pass 2: verify zeros, then XOR to all-1s (forward) |
| **`MEMTEST_ZO_PASS4`** | — | `0x0028F8` | `memtest.s:1871` | Pass 4: verify zeros, XOR to all-1s again (forward) |
| **`MEMTEST_ZO_PASS5`** | — | `0x002904` | `memtest.s:1879` | Pass 5: verify all-1s, XOR back to zeros (backward) |
| **`MEMTEST_ZO_REVERIFY_BACK`** | — | `0x0028EE` | `memtest.s:1864` | Pass 3: verify all-1s, XOR back to zeros (backward) |
| **`MOUNT_FAILED_EJECT`** | `0x000B82` | `0x000A52` | `boot_load.s:246`<br>`boot_load.s:261` | MOUNT_FAILED_EJECT - disk mount failed: eject and return to WaitForBootDisk |
| **`MOUSEINIT`** | — | `0x000B34` | `boot_load.s:385` | MOUSEINIT - initialize mouse acceleration from PRAM and resources Reads mouse speed from SPVolCtl bits 5-3. If > 4, clamps to 2 and updates PRAM. Loads 'mcky' resource for acceleration table. |
| **`MOUSEINIT_DONE`** | — | `0x000B78` | `boot_load.s:411` | — |
| **`MYBOOT`** | — | `0x00080A` | `boot_load.s:25` | Startup: boot from the startup disk (StartBoot) Apple source: StartBoot.a. BOOTME (MYBOOT in MacSEROM.lst) mounts the startup volume found by boot_search.s, reads the boot blocks, opens the System fil... |
| **`MYFIRSTPROC`** | — | `0x000000` | `vectors.s:25` | ROM header ($00-$3F): checksum, reset vectors, ROM version, entry points Apple source: StartInit.a (System 7.1: OS/StartMgr/StartInit.a, "START OF ROM"); BASEOFROM is defined in StartTop.a (MacSEROM.l... |
| **`MYROM`** | — | `0x000000` | `vectors.s:26` | ROM header ($00-$3F): checksum, reset vectors, ROM version, entry points Apple source: StartInit.a (System 7.1: OS/StartMgr/StartInit.a, "START OF ROM"); BASEOFROM is defined in StartTop.a (MacSEROM.l... |
| **`NEVERAGAIN`** | — | `0x000EE2` | `boot_search.s:356` | NEVERAGAIN - mark drive as rejected in BootMask Clears the drive's bit in BootMask so it won't be tried again. |
| **`NEVERAGAIN_RTS`** | — | `0x000EF2` | `boot_search.s:362` | — |
| **`NEXT_BOOT_ATTEMPT`** | `0x0007CA` | — | `vectors.s:1154` | Return to WaitForBootDisk |
| **`NEXTDQ_FOLLOW`** | — | `0x000DC4` | `boot_search.s:194` | — |
| **`NEXTDQ_TEST`** | — | `0x000DC6` | `boot_search.s:196` | — |
| **`NEXTDQENTRY`** | — | `0x000DBA` | `boot_search.s:189` | NEXTDQENTRY - advance to next entry in drive queue A2 = current entry (nil = start from head). Returns next in A2. Z=1 if end of queue reached (A2=nil). |
| **`NO_BOOT_ERROR`** | `0x000BB8` | — | `boot_load.s:279` | Return (no error) |
| **`NOTASS`** | — | `0x001B42` | `memtest.s:193` | — |
| **`OPEN_AND_READ_FILE`** | `0x000BDC` | `0x000AA2` | `boot_load.s:313`<br>`boot_load.s:305` | Open file, read contents (D3 = alloc mode) |
| **`OPEN_BOOT_PATCH`** | `0x000BDA` | `0x000AA0` | `boot_load.s:310`<br>`boot_load.s:302` | OPEN_BOOT_PATCH - Open and read file (D3=0: from BufPtr) - entry for boot patch loading Called during boot. |
| **`OPEN_SYSRES`** | — | `0x00097C` | `boot_load.s:169` | Open the System resource file |
| **`OPEN_SYSTEM_FILE`** | — | `0x0008F4` | `boot_load.s:113` | Draw startup bitmap from Finder icon to screen via CopyBits OPEN_SYSTEM_FILE - re-init resources, open System file |
| **`OPEN_SYSTEM_RSRC`** | `0x000AA8` | — | `boot_load.s:147` | Execute boot block patch code entries (offsets +$2A and +$3A) These are optional patches applied during boot before launching the System. Open the System file as a resource file |
| **`P_CheckRamFirst8`** | — | `0x002694` | `memtest.s:1549` | **Regs:** `Entry: D6 = running error accumulator Exit: D6 = updated error bits (0 = all lanes OK)`<br>P_CheckRamFirst8 - data bus walking-ones test on first 8 bytes Writes rotating 1/0 patterns to addresses 0-7, then verifies readback matches. Tests all 32 data bus lines with 256 rotations. Entry: D6 ... |
| **`P_CheckRamFirst8_Loop`** | — | `0x0026A2` | `memtest.s:1556` | — |
| **`P_ChecksumRom`** | — | `0x0026C8` | `memtest.s:1574` | P_ChecksumRom - verify 256 KB ROM checksum Sums all 16-bit words from ROM offset 4 through 0x3FFFF. XORs result with stored checksum at offset 0. D6 = 0 if match. |
| **`P_FindMemorySize`** | — | `0x0025FA` | `memtest.s:1458` | **Regs:** `Exit: D6 = detected RAM top address (0 = probe failed)`<br>P_FindMemorySize - detect installed RAM size Probes RAM at various sizes from the MEMSIZE_PROBE_TBL table. For each entry, writes a pattern at the probed address and checks if the reference address (f... |
| **`P_mGNEFilter`** | `0x0008D2` | — | `boot_install.s:156` | P_m GNE Filter Called during boot (3,695 times in 30s trace). |
| **`P_SadMac`** | — | `0x001DA2` | `memtest.s:471` | P_SadMac - error handler Normally: jumps to CRITERR to display Sad Mac screen. With the factory loopback jumper (D7 bit 26): restarts the diagnostic test manager so the manufacturing test station can ... |
| **`P_SADMAC_TESTMGR`** | — | `0x001DAC` | `memtest.s:475` | P_SadMac - error handler Normally: jumps to CRITERR to display Sad Mac screen. With the factory loopback jumper (D7 bit 26): restarts the diagnostic test manager so the manufacturing test station can ... |
| **`P_TestMemory0`** | — | `0x0026F0` | `memtest.s:1599` | **Regs:** `Entry: A0 = start, A1 = end Exit: D6 = error bits (0 = pass)`<br>P_TestMemory0 - forward-direction memory test (pattern fill + XOR verify) Fills RAM range (A0..A1) with 12-byte repeating pattern from PAT_6DB6, then verifies using cascading XOR propagation. Any mism... |
| **`P_tUnimplemented`** | — | `0x000768` | `boot_install.s:849` | P_tUnimplemented - handler for unimplemented A-line traps Called when an application uses a trap not in this ROM. Generates system error #12 (dsNoPk = unimplemented trap). |
| **`PAT_6DB6`** | `0x000EB0` | `0x002792` | `memtest.s:232`<br>`memtest.s:1676` | Compare final 12 bytes against expected pattern (verify complete) PAT_6DB6 - 12-byte test pattern for P_TestMemory0 Repeating 3-bit sequence (110, 101, 011) exercises every data bit. |
| **`PAT_B6DB`** | `0x000EAE` | — | `memtest.s:229` | — |
| **`PAT_DB6D`** | `0x000EAC` | — | `memtest.s:226` | PAT_DB6D/PAT_B6DB/PAT_6DB6 - three complementary DRAM test patterns Each pattern uses the repeating 3-bit sequence (110, 101, 011) shifted by one bit, so together all three patterns test every bit as ... |
| **`PATCH_LOAD_FAILED`** | `0x000BBA` | — | `boot_load.s:287` | PATCH_LOAD_FAILED - Boot block patch load failed - restore BufPtr and continue Called during boot. |
| **`PATTERN_FILL_VERIFY`** | `0x000E3C` | — | `memtest.s:163` | **Regs:** `Entry: A0 = pattern data (12 bytes), A3 = RAM base, A2 = RAM end Exit: D0 = updated error accumulator (0 = no new errors)`<br>PATTERN_FILL_VERIFY - pattern fill/verify subroutine Fills verified RAM (A3..A2) with a repeating 12-byte pattern from (A0), then reads back and XORs against expected values. Any mismatched bits are a... |
| **`PATTERN_PASS_2`** | `0x000E18` | — | `memtest.s:119` | PATTERN_PASS_2 - second pattern pass: uses PAT_6DB6 (0x6DB6DB... walking-ones) Called during boot. |
| **`PATTERN_PASS_3`** | `0x000E22` | — | `memtest.s:131` | PATTERN_PASS_3 - third pattern pass: uses PAT_B6DB (0xB6DB = 1011_0110...) The three patterns (DB6D, 6DB6, B6DB) together exercise every bit position as both 0 and 1, ensuring no stuck data bits in DR... |
| **`PATTERN_TESTS_DONE`** | `0x000E2C` | — | `memtest.s:141` | PATTERN_TESTS_DONE - all pattern tests complete, assemble final results Called during boot. |
| **`PHASE_TIMING_INIT`** | `0x00006C` | — | `vectors.s:142` | PHASE_TIMING_INIT Called during boot. Trace: D0-D2 = phase read results, D7=1, A6=SCC read base, SR=2700. Examines the low bit of each phase read word to determine SCC timing. On Mac Plus, all three p... |
| **`PLANSTRATEGY`** | — | `0x000D9A` | `boot_search.s:164` | PLANSTRATEGY - adjust boot device search filter If default device is floppy ($FFFB), keep current filter. Otherwise, broaden to accept any bootable device. |
| **`PLANSTRATEGY_RTS`** | — | `0x000DA4` | `boot_search.s:168` | — |
| **`PlotDisk`** | `0x0007CE` | `0x000F34` | `vectors.s:1161` | D7 = icon data address (or 0 to erase). Uses ICON_DISK icon template. Draws at screen address 0x3FCB5E (= SEScrnIcon, centered). Called during boot. |
| **`PLOTDISK`** | `0x0007CE` | `0x000F34` | `boot_search.s:408` | PLOTDISK - draw disk icon with optional overlay to screen A0 = overlay bitmap (nil = none, QMARK or XMARK). Draws the disk icon at screen position $3FCB5E, then overlays the symbol (if any) at $3FCF1F... |
| **`PLOTDISK_DONE`** | — | `0x000F6E` | `boot_search.s:429` | — |
| **`PLOTDISK_OVERLAY`** | — | `0x000F58` | `boot_search.s:421` | PLOTDISK_OVERLAY - overlay symbol on top of disk icon if needed |
| **`PLOTDISK_SYNC`** | — | `0x000F40` | `boot_search.s:413` | — |
| **`PLOTDISK_VBL_WAIT`** | `0x0007D4` | — | `vectors.s:1165` | Wait one VBL tick before drawing |
| **`PMMUACCESS`** | — | `0x001BC6` | `memtest.s:257` | — |
| **`PMMUCONFIG`** | — | `0x001BBA` | `memtest.s:251` | — |
| **`PMMUILLEGAL`** | — | `0x001BC0` | `memtest.s:254` | — |
| **`PMSPSWOS`** | — | `0x000342` | `boot_install.s:324` | — |
| **`POST_DEBUGGER_INIT`** | — | `0x0000B0` | `boot_install.s:76` | POST_DEBUGGER_INIT - continue boot after debugger/SysError vectors installed Calibrates timing loops, checks for external test software, then initializes all system managers in sequence. |
| **`PRAM_GOT_DELAY`** | — | `0x000376` | `boot_install.s:358` | — |
| **`PRAM_GOT_REPEAT`** | — | `0x000368` | `boot_install.s:352` | — |
| **`PREPARE_LAUNCH`** | `0x000AB8` | — | `boot_load.s:154` | Prepare to launch the Finder application |
| **`PRIVERROR`** | — | `0x001B22` | `memtest.s:181` | — |
| **`PutIcon`** | `0x000EC4` | `0x0011BA` | `sad_mac.s:28` | **Regs:** `Entry: A2 = screen destination, A4 = compressed icon data`<br>Sad Mac Icon Display and Boot-Screen Icon Drawing Contains the RLE icon decoder (PutIcon), Sad Mac / Happy Mac entry points, and compressed icon templates for the Macintosh outline, floppy disk, and t... |
| **`PUTICON`** | `0x000EC4` | `0x0011BA` | `sad_mac.s:145` | PUTICON - draw RLE-compressed icon to screen (32x32 delta-encoded) A4 = icon data, A2 = screen destination. Control byte: bit=1 means clear (black), bit=0 means copy source. After all rows decoded, XO... |
| **`PUTICON_ADVANCE`** | — | `0x0011D2` | `sad_mac.s:160` | — |
| **`PUTICON_BYTE`** | — | `0x0011C6` | `sad_mac.s:152` | — |
| **`PUTICON_COPY`** | — | `0x0011D0` | `sad_mac.s:158` | — |
| **`PUTICON_NEXTROW`** | — | `0x0011E0` | `sad_mac.s:166` | — |
| **`PUTICON_ROW`** | — | `0x0011C0` | `sad_mac.s:149` | — |
| **`PutSymbol`** | `0x000F2E` | `0x0011AA` | `sad_mac.s:115` | **Regs:** `Entry: A4 = bitmap data (20 bytes: 10 rows x 2 bytes), A2 = screen dest`<br>PutSymbol - draw a 10-row, 2-byte-wide bitmap at screen position A2 Entry: A4 = bitmap data (20 bytes: 10 rows x 2 bytes), A2 = screen dest A6 = return address Called during boot. |
| **`PUTSYMBOL`** | `0x000F2E` | `0x0011AA` | `sad_mac.s:133` | PUTSYMBOL - draw a 2-byte-wide bitmap to screen A4 = bitmap data, A2 = screen destination, D2 = row count - 1. |
| **`PUTSYMBOL_LOOP`** | `0x000F30` | — | `sad_mac.s:117` | **Regs:** `Entry: A4 = bitmap data (20 bytes: 10 rows x 2 bytes), A2 = screen dest`<br>PutSymbol - draw a 10-row, 2-byte-wide bitmap at screen position A2 Entry: A4 = bitmap data (20 bytes: 10 rows x 2 bytes), A2 = screen dest A6 = return address Called during boot. |
| **`QMARK`** | — | `0x000F76` | `boot_search.s:434` | QMARK - question mark bitmap (16x16, 30 bytes) |
| **`RAM_FILL_LOOP`** | `0x00035A` | — | `vectors.s:619` | RAM fill loop: write 0xFFFFFFFF |
| **`RAM_SIZE_DETECT`** | `0x000DC2` | — | `memtest.s:66` | RAM_SIZE_DETECT - RAM size detection via address mirror test Walks up in power-of-2 steps from the last address-line-test offset. When a write aliases back to address 0, that offset is the RAM size. T... |
| **`RAM_SIZE_DONE`** | `0x000DFC` | — | `memtest.s:102` | RAM_SIZE_DONE - RAM sizing complete, A2 = top of verified RAM |
| **`RAMTEST`** | — | `0x001D3E` | `memtest.s:424` | **Regs:** `Entry: A0 = start address, A1 = end address, A6 = RAM end Exit: D6 = error code (0 = pass), registers preserved`<br>RAMTEST - callable RAM test routine Tests a RAM range by splitting at the 512K or 2MB boundary and testing each segment with P_TestMemory0 (pattern fill/verify). Entry: A0 = start address, A1 = end ad... |
| **`RAMTEST_FIRST_HALF_DONE`** | — | `0x001D80` | `memtest.s:447` | — |
| **`RAMTEST_RETURN`** | — | `0x001D9A` | `memtest.s:460` | — |
| **`RAMTEST_RUN_SEGMENT`** | — | `0x001D8E` | `memtest.s:454` | — |
| **`RAMTEST_SECOND_HALF`** | — | `0x001D8A` | `memtest.s:452` | — |
| **`RAMTEST_SEGMENT_DONE`** | — | `0x001D96` | `memtest.s:457` | — |
| **`RAMTEST_USE_512K_SPLIT`** | — | `0x001D60` | `memtest.s:434` | — |
| **`REACTFAIL_MARK`** | — | `0x000E26` | `boot_search.s:247` | — |
| **`REACTFAIL_RTS`** | — | `0x000E2E` | `boot_search.s:251` | — |
| **`REACTFAIL_SHOW`** | — | `0x000E2A` | `boot_search.s:249` | — |
| **`REACTTOFAILURE`** | — | `0x000E14` | `boot_search.s:240` | REACTTOFAILURE - handle boot block read failure Error -65 ($FFBF): no disk in drive -- just return. Error -64 ($FFC0): offline -- mark as never-try-again. Other: eject disk, show failure icon. |
| **`READ_PHASE_LINES`** | `0x000058` | — | `vectors.s:119` | READ_PHASE_LINES - read hardware phase lines to sample bus timing signals Reads 3 words from the phase-read address (0xF00000) into D0-D2. Used by PHASE_TIMING_INIT below to detect SCC-clock phase. Ca... |
| **`READ_RTC_BIT_LOOP`** | `0x000274` | `0x00A33C` | `vectors.s:474`<br>`rtc.s:150` | ReadRTCByte bit-clock loop |
| **`ReadRTCByte`** | `0x000266` | `0x00A32E` | `vectors.s:468`<br>`rtc.s:144` | Read 8 bits from RTC via VIA PortB bit-bang serial. Switches PB0 to input, clocks PB1, reads data from PB0 into D2. return address in A6 Called during boot. |
| **`REINIT_SYS_ZONE`** | `0x00097C` | — | `boot_install.s:226` | REINIT_SYS_ZONE - alternate zone init entry (used during warm restart) |
| **`REOPEN_RESOURCES`** | `0x000A36` | — | `boot_load.s:98` | Copy System file name from boot block to SysResName low-memory Open the shell application (Finder) specified in boot block Draw "Welcome to Macintosh" bitmap from boot block The bitmap is at boot bloc... |
| **`REPLAN_SEARCH`** | — | `0x000C9C` | `boot_search.s:27` | — |
| **`RESERVE_PRINT_BUF`** | `0x000A76` | `0x000942` | `boot_load.s:126`<br>`boot_load.s:148` | Allocate printer buffer space from BufPtr based on boot block config Subtract printer buffer from BufPtr |
| **`RESERVE_STACK_BUF`** | — | `0x000946` | `boot_load.s:150` | — |
| **`RESERVE_TAG_BUF`** | `0x000A7A` | — | `boot_load.s:129` | Reserve tag buffer, run boot patches |
| **`RESETENTRY`** | — | `0x00002A` | `vectors.s:86` | +$2A: reset entry; the initial PC at +$04 points here (EBootStart in the Plus and 128K trees). |
| **`RETRY_BOOT`** | — | `0x000A80` | `boot_load.s:275` | — |
| **`RETRY_CANDIDATE`** | — | `0x000CA4` | `boot_search.s:30` | — |
| **`ROM_CKSUM_CHK_3`** | — | `0x0028B4` | `memtest.s:1821` | — |
| **`ROM_CKSUM_CHK_4`** | — | `0x0028BE` | `memtest.s:1826` | — |
| **`ROM_CKSUM_CHK_ODD`** | — | `0x0028AA` | `memtest.s:1816` | Verify: compare computed sums against expected (4 longwords at 0x30) |
| **`ROM_CKSUM_DONE`** | — | `0x0028C8` | `memtest.s:1831` | — |
| **`ROM_CKSUM_OK`** | — | `0x0026EE` | `memtest.s:1590` | — |
| **`ROM_CKSUM_PER_BYTE`** | — | `0x00285A` | `memtest.s:1778` | ROM_CKSUM_PER_BYTE - per-byte ROM checksum verification Computes separate even-byte and odd-byte sums over the 256 KB ROM, then compares each against expected values stored at ROM offset 0x30. Sets D6... |
| **`ROM_CKSUM_SEC1_LOOP`** | — | `0x002876` | `memtest.s:1790` | Sum first section: ROM offset 4 through 0x30 |
| **`ROM_CKSUM_SEC2_LOOP`** | — | `0x002890` | `memtest.s:1802` | Sum second section: ROM offset 0x40 through end |
| **`ROMRSRC`** | — | `0x00001A` | `vectors.s:72` | +$1A: offset of the ROM resources: the two words in front of the resource map (number of ROM resources, map size; resources/res_map.s). InitResources adds it to ROMBase. |
| **`ROMVERSION`** | — | `0x000008` | `vectors.s:56` | +$08: the ROM version word ($0276). Apple's StartInit.a calls the high byte the machine number. Software tests the low byte, the ROM version proper ($75 Mac Plus, $76 SE): the .ATP and .MPP drivers co... |
| **`RTC_DISABLE_CHIP`** | `0x00024E` | `0x00A316` | `vectors.s:444`<br>`rtc.s:122` | RTC_DISABLE_CHIP - RTC transaction complete; disable chip and return Called during boot. |
| **`RTC_EXT_CMD_SENT`** | `0x000220` | `0x00A2E8` | `vectors.s:398`<br>`rtc.s:98` | Decode the RTC command type from D1: Bits 6-3 of D1 determine the command class. If bits 6-3 = 0b0111 ($38), this is an extended (2-byte) command. Extended command: send first byte, then handle second... |
| **`RTC_READ_CMD`** | `0x00023E` | — | `vectors.s:432` | RTC_READ_CMD RTC_READ_CMD - read command: send command byte, then read response Called during boot. |
| **`RTC_READ_CMD_SENT`** | `0x000246` | — | `vectors.s:438` | RTC_READ_CMD_SENT - command sent; now clock in the response byte Called during boot. |
| **`RTC_READ_OR_WRITE`** | `0x000228` | `0x00A2F0` | `vectors.s:408`<br>`rtc.s:104` | Check D1 sign: negative = read, positive = write |
| **`RTC_READ_PRAM_VOL`** | `0x0000B2` | — | `vectors.s:185` | RTC_READ_PRAM_VOL - RTC is valid: read PRAM byte containing speaker volume Sends command 0xA1 (= -0x5F) to read PRAM byte with volume setting. Called during boot. |
| **`RTC_READ_RETURN`** | `0x0000A8` | — | `vectors.s:175` | Init VIA port B: set bits 0-2,7 as output (RTC data/clock/enable + sound disable) Trace: A5 = VIA_PortB (0xEFE1FE) Read initial RTC state: send command byte 0xC1 (= -0x3F = read seconds byte 0) RTC_RE... |
| **`RTC_SINGLE_CMD`** | `0x000226` | `0x00A2EE` | `vectors.s:405`<br>`rtc.s:102` | RTC_SINGLE_CMD - single-byte RTC command: check if read or write Called during boot. |
| **`RTC_WRITE_CMD_SENT`** | `0x000232` | `0x0025B6` | `vectors.s:416`<br>`memtest.s:1423` | Write command: send the command byte, then send data byte (D2) RTC_WRITE_CMD_SENT - command byte sent for write; now send the data byte Called during boot. |
| **`RTC_WRITE_DONE`** | `0x00023C` | `0x00A304` | `vectors.s:423`<br>`rtc.s:112` | RTC_WRITE_DONE - write complete; disable RTC and return Called during boot. |
| **`SADMAC`** | — | `0x00117C` | `sad_mac.s:113` | — |
| **`SADMAC_DRAW_CODE`** | `0x00015C` | — | `vectors.s:297` | SADMAC_DRAW_CODE - draw 6-digit hex error code below the sad Mac icon D0.W = high part of error code, D1.W = low part. Renders each hex digit as a 3x6 pixel glyph from the DT_HEX_FONT font table. Scre... |
| **`SADMAC_SCRN_READY`** | `0x000152` | — | `vectors.s:288` | SADMAC_SCRN_READY SADMAC_SCRN_READY - prepare to display the error code below the sad Mac icon A4 = error code from the failed operation. |
| **`SCAN_CANDIDATES`** | — | `0x000CA8` | `boot_search.s:32` | — |
| **`SCC_INIT`** | — | `0x002450` | `memtest.s:1263` | SCC_INIT - initialize SCC serial port (channel B, modem port) Programs SCC channel B registers from SCC_INIT_REGS table for 9600 baud, 8N1 serial communication. Flushes receive buffer, enables sound o... |
| **`SCC_INIT_FLUSH`** | — | `0x00246A` | `memtest.s:1273` | — |
| **`SCC_INIT_LOOP`** | — | `0x00245C` | `memtest.s:1267` | — |
| **`SCC_INIT_REGS`** | — | `0x002492` | `memtest.s:1286` | SCC_INIT_REGS - SCC channel B init register table Format: pairs of (register_number, value), terminated by 0xFF. Configures 9600 baud, 8N1 for manufacturing test serial link. |
| **`SCC_RECV_CHAR`** | — | `0x0022EC` | `memtest.s:1092` | **Regs:** `Entry: D7 bit 17 = SCC initialized Exit: D5 = received character (bit 15 set if no data available)`<br>SCC_RECV_CHAR - read one character from SCC serial port (channel B) Entry: D7 bit 17 = SCC initialized Exit: D5 = received character (bit 15 set if no data available) D5 high word = char saved for com... |
| **`SCC_RECV_DONE`** | — | `0x00234E` | `memtest.s:1120` | — |
| **`SCC_RECV_NO_DATA`** | — | `0x002350` | `memtest.s:1124` | SCC_RECV_NO_DATA - no character: return the no-data value, after two NOPs if D7 bit 18 is set |
| **`SCC_RECV_RETURN`** | — | `0x00235A` | `memtest.s:1129` | — |
| **`SCC_RECV_STORE`** | — | `0x00232E` | `memtest.s:1108` | — |
| **`SCC_SEND_CHAR`** | — | `0x002422` | `memtest.s:1246` | **Regs:** `Entry: D0 = character to send`<br>SCC_SEND_CHAR - write one character to SCC serial port (channel B) Entry: D0 = character to send Waits for TX buffer ready before returning. Called by: TM_CMD_G_ECHO_STAR, TM_CMD_G_ECHO_G, TM_CMD_UNKN... |
| **`SCC_SEND_WAIT`** | — | `0x002432` | `memtest.s:1250` | — |
| **`SCC_TIMING_DONE`** | `0x000086` | — | `vectors.s:155` | SCC timing complete - init VIA and screen buffer |
| **`SCC_WRITE_ENTER`** | `0x000858` | `0x0005C4` | `boot_install.s:66`<br>`boot_install.s:658` | SCC register write loop |
| **`SCC_WRITE_LOOP`** | `0x000852` | `0x0005BE` | `boot_install.s:61`<br>`boot_install.s:654` | SCC_WRITE_LOOP - SCC register write loop with settling delay Called during boot. |
| **`SCC_WRITE_REGS`** | `0x00084E` | — | `boot_install.s:56` | SCC_WRITE_REGS - write D1+1 bytes from (A2) to SCC write register (A0) Includes delay loops (MOVE.L (SP),(SP)) for SCC register settling time. |
| **`SCRN_ERASED`** | `0x0000EE` | — | `vectors.s:220` | Writing VIA Port A clears bit 4 (MemOverlay). This remaps address 0x000000 from ROM back to RAM. From this point, the ROM is only at 0x400000. Erase screen buffer to all white (0xFF = white pixels) A2... |
| **`ScrnAddress`** | `0x000806` | `0x018F8C` | `vectors.s:1231` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`ScrnSize`** | `0x000806` | `0x018F94` | `vectors.s:1226` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`SELECT_HEAP_SIZE`** | `0x0009A2` | `0x000826` | `boot_load.s:40`<br>`boot_load.s:36` | Select system heap size based on installed RAM |
| **`SELECTDEVICE`** | — | `0x000DCA` | `boot_search.s:202` | SELECTDEVICE - set boot drive from selected drive queue entry A2 = drive queue entry. Sets ioRefNum, ioVRefNum, BtDskRfn, BootDrive. |
| **`SET_APPL_BASE`** | `0x0009B2` | — | `boot_load.s:46` | Set app base, init events/FS, mount volume |
| **`SET_APPL_BASE2`** | — | `0x000874` | `boot_load.s:67` | — |
| **`SET_APPL_LIMIT`** | — | `0x0001C4` | `boot_install.s:187` | — |
| **`SET_BLESSED_DONE`** | `0x000C74` | — | `boot_load.s:400` | Return from SET_BLESSED_VOLUME |
| **`SET_BLESSED_VOLUME`** | `0x000C4C` | — | `boot_load.s:385` | SET_BLESSED_VOLUME - Set default volume to blessed folder using HFS _OpenWD + _SetVol Called during boot. |
| **`SET_BOOT_STACK`** | — | `0x00008A` | `boot_install.s:61` | SET_BOOT_STACK - set up initial stack pointer and fill low memory A1 = stack top (min of 256K, MemTop). Saves WarmStart across the low-memory fill so it survives the wipe. |
| **`SetAppBase__MAP`** | — | — | `vectors.s:1227` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`SETDEFAULTSTARTUP`** | — | `0x000CD2` | `boot_search.s:53` | SETDEFAULTSTARTUP - write default startup device to XPRAM |
| **`SETRAWTIMEOUT`** | — | `0x001082` | `boot_search.s:538` | SETRAWTIMEOUT - write raw timeout byte to XPRAM offset $01 |
| **`SETTIMEOUT`** | — | `0x000FEC` | `boot_search.s:466` | SETTIMEOUT - set boot wait timeout (low 5 bits, max 31) |
| **`SETTIMEOUT_MERGE`** | — | `0x000FFE` | `boot_search.s:473` | — |
| **`SETUP_BOOT_ENV`** | — | `0x000122` | `boot_install.s:112` | Full RAM test (skipped on warm restart) SETUP_BOOT_ENV - set up boot environment: stack, drive queue, I/O |
| **`SETUP_READ_PARAMS`** | `0x000C12` | `0x000AD8` | `boot_load.s:337`<br>`boot_load.s:332` | Set up IOParam and read file data |
| **`SETUPSYSAPPZONE`** | — | `0x00019C` | `boot_install.s:174` | SETUPSYSAPPZONE - create system and application heap zones Uses DTAB_INITZONE parameter block to call _InitZone. Sets SysZone, RAMBase, ApplZone, HeapEnd, ApplLimit. |
| **`SETUPTIMEK`** | — | `0x00041C` | `boot_install.s:453` | SETUPTIMEK - calibrate TimeDBRA and TimeSCCDB timing constants Measures how many DBF loop iterations fit in one VIA Timer 1 interrupt period. Two measurements: 1. TimeDBRA: plain DBF loop (used by _De... |
| **`SETVOL_BLESSED_FOLDER`** | — | `0x000B12` | `boot_load.s:368` | SETVOL_BLESSED_FOLDER - set default volume to blessed folder D0 = blessed folder DirID. If zero, returns immediately. Uses HFSDispatch selector 1 (SetVol by DirID) with the magic signature 'ERIK' to r... |
| **`SETVOL_BLESSED_FOLDER_RTS`** | — | `0x000B32` | `boot_load.s:379` | — |
| **`SETWAITFLAGS`** | — | `0x001012` | `boot_search.s:485` | SETWAITFLAGS - set boot wait flags (high 3 bits) |
| **`SHOW_XMARK_ICON`** | `0x00079E` | — | `vectors.s:1127` | SHOW_XMARK_ICON - disk was ejected: show X mark icon briefly, then question mark |
| **`SHOWDEVFAIL_RTS`** | — | `0x000F1C` | `boot_search.s:387` | — |
| **`SHOWDEVICEFAIL`** | — | `0x000F12` | `boot_search.s:383` | SHOWDEVICEFAIL - show failure indicator for failed boot device If it's a floppy, enable the X-flash animation. |
| **`SHOWDISKQ`** | — | `0x000F24` | `boot_search.s:397` | — |
| **`SHOWDISKX`** | — | `0x000F2C` | `boot_search.s:400` | — |
| **`ShowHappyMac`** | `0x000F28` | — | `sad_mac.s:107` | ShowHappyMac - draw Happy Mac icon (all tests passed) return address in A5 Called during boot. |
| **`SHOWPLAINDISK`** | — | `0x000F1E` | `boot_search.s:394` | SHOWPLAINDISK / SHOWDISKQ / SHOWDISKX - draw boot disk icons SHOWPLAINDISK: draw plain disk (no overlay) SHOWDISKQ: draw disk with question mark overlay SHOWDISKX: draw disk with X mark overlay |
| **`ShowSadMac`** | `0x000F00` | — | `sad_mac.s:75` | ShowSadMac - draw Sad Mac icon on boot screen (test failure) return address in A5 |
| **`SHOWSUCCESS`** | — | `0x000E72` | `boot_search.s:290` | SHOWSUCCESS - display happy Mac icon (bootable disk found) |
| **`SHOWSUCCESS_RET`** | — | `0x000E80` | `boot_search.s:295` | — |
| **`SKIP_SECONDARY_BOOT`** | `0x000992` | — | `boot_load.s:34` | Select 128K or 512K heap size |
| **`SPURINTERRUPT`** | — | `0x001B56` | `memtest.s:202` | — |
| **`STARTBOOT`** | — | `0x000040` | `boot_install.s:25` | Startup: hardware and manager initialization (StartInit) Apple source: StartInit.a (System 7.1: OS/StartMgr/StartInit.a). Reset entry (STARTBOOT, STARTINIT1, BOOTRETRY) and the initialization chain: J... |
| **`STARTINIT1`** | — | `0x000048` | `boot_install.s:32` | STARTINIT1 - hardware initialization after initial RAM test passes STARTTEST1 returns here with A6 = top of RAM. D7 = CPU type from WHICHCPU (0=68000, 1=68010, 2=68020). |
| **`STARTPC`** | — | `0x000004` | `vectors.s:50` | +$04: the initial PC. It lies in the ROM's own address range: the first access to $400000-$4FFFFF switches the overlay off, so RAM is at address 0 from the first instruction on. (The Plus switches the... |
| **`STARTTEST1`** | — | `0x001BDE` | `memtest.s:277` | — |
| **`STBOOT`** | — | `0x00000A` | `vectors.s:63` | +$0A, +$0E: restart entries (Apple: StBoot, "jump to start code for a restart", and BadDisk, "eject disk, and reboot"). In the SE both restart at STARTBOOT; the Plus branches to its eject-and-try-next... |
| **`SWITCHGOODIES`** | — | `0x00030C` | `boot_install.s:307` | SWITCHGOODIES - Switcher/MultiFinder context table template (52 bytes) Copied to a heap block during INITSWITCHERTABLE. Contains default context-switch parameters: stack sizes, buffer sizes, and confi... |
| **`SYSTEMBEEP`** | — | `0x0029B4` | `memtest.s:1992` | SYSTEMBEEP - _SysBeep trap handler Called by the Toolbox _SysBeep trap. If sound is active, flashes the menu bar instead. Otherwise generates a square-wave beep tone via the VIA sound hardware using B... |
| **`TEST_ALWAYS_PASS`** | — | `0x00299E` | `memtest.s:1974` | TEST_ALWAYS_PASS - success return (unconditional pass) |
| **`TEST_DISPATCH_TBL`** | — | `0x0029A4` | `memtest.s:1982` | TEST_DISPATCH_TBL - test dispatch table (8 PC-relative offsets) Each word is a signed offset from TEST_DISPATCH_TBL to a test routine. |
| **`TEST_MODE_ENTRY`** | `0x00002E` | — | `vectors.s:80` | TEST_MODE_ENTRY - test mode entry (stores D0 to memory pointed by A0) |
| **`TEST_TABLE_COUNT`** | — | `0x0029A2` | `memtest.s:1978` | TEST_TABLE_COUNT - test dispatch table entry count |
| **`TESTMANAGER`** | — | `0x001DB0` | `memtest.s:490` | TESTMANAGER - hardware test dispatcher Callable entry point for the manufacturing test infrastructure. D0 selects the function: 0 = init from param block at (A0), dispatch by test number 1 = return (d... |
| **`TIMEK_DBRA_BODY`** | — | `0x00044C` | `boot_install.s:467` | — |
| **`TIMEK_DBRA_DONE`** | — | `0x000460` | `boot_install.s:475` | — |
| **`TIMEK_DBRA_LOOP`** | — | `0x000458` | `boot_install.s:470` | — |
| **`TIMEK_DBRA_START`** | — | `0x00045E` | `boot_install.s:473` | — |
| **`TIMEK_SCC_BODY`** | — | `0x000482` | `boot_install.s:487` | — |
| **`TIMEK_SCC_DONE`** | — | `0x00049A` | `boot_install.s:496` | — |
| **`TIMEK_SCC_LOOP`** | — | `0x00048E` | `boot_install.s:490` | — |
| **`TIMEK_SCC_START`** | — | `0x000498` | `boot_install.s:494` | — |
| **`TM_BEEP_CHECK`** | — | `0x002264` | `memtest.s:1028` | TM_BEEP_CHECK - send the queued boot message: with D7 bit 16 (MsgQ) set, send it now, or with bit 22 (timer) also set each time VIA timer 2 has run out 12 times (about once a second); then read the ne... |
| **`TM_BEEP_PREFIX_LOOP`** | — | `0x002288` | `memtest.s:1044` | — |
| **`TM_BEEP_PREFIX_NEXT`** | — | `0x002292` | `memtest.s:1048` | — |
| **`TM_BEEP_PREFIX_STR`** | — | `0x0022DE` | `memtest.s:1078` | TM_BEEP_PREFIX_STR - boot message header "*APPLE*" (count - 1, chars) |
| **`TM_BEEP_PRINT_D7`** | — | `0x0022AA` | `memtest.s:1056` | — |
| **`TM_BEEP_SEND_STATUS`** | — | `0x002280` | `memtest.s:1040` | Send the boot message: "*APPLE*", D6, D7.W, "*2*" CR LF (2 = Mac SE) |
| **`TM_BEEP_SUFFIX_INIT`** | — | `0x0022B6` | `memtest.s:1061` | — |
| **`TM_BEEP_SUFFIX_LOOP`** | — | `0x0022C2` | `memtest.s:1066` | — |
| **`TM_BEEP_SUFFIX_NEXT`** | — | `0x0022CC` | `memtest.s:1070` | — |
| **`TM_BEEP_SUFFIX_STR`** | — | `0x0022E6` | `memtest.s:1084` | TM_BEEP_SUFFIX_STR - boot message trailer "*2*" CR LF; Apple: "The *2* part identifies the system as a Mac SE" |
| **`TM_BEEP_TIMER_CHECK`** | — | `0x00227C` | `memtest.s:1036` | — |
| **`TM_BIT0_RESULT`** | — | `0x001E64` | `memtest.s:571` | — |
| **`TM_BIT1_CHECK`** | — | `0x001E6A` | `memtest.s:574` | — |
| **`TM_BIT1_RESULT`** | — | `0x001E78` | `memtest.s:580` | — |
| **`TM_BIT2_CHECK`** | — | `0x001E7E` | `memtest.s:583` | — |
| **`TM_BIT2_RESULT`** | — | `0x001E8C` | `memtest.s:589` | — |
| **`TM_BIT3_CHECK`** | — | `0x001E92` | `memtest.s:592` | — |
| **`TM_BIT3_RESULT`** | — | `0x001EA0` | `memtest.s:598` | — |
| **`TM_BIT4_CHECK`** | — | `0x001EA6` | `memtest.s:601` | — |
| **`TM_BIT4_RESULT`** | — | `0x001EB4` | `memtest.s:607` | — |
| **`TM_BIT5_CHECK`** | — | `0x001EBA` | `memtest.s:610` | — |
| **`TM_BIT5_RESULT`** | — | `0x001EC8` | `memtest.s:616` | — |
| **`TM_BIT6_CHECK`** | — | `0x001ECE` | `memtest.s:619` | — |
| **`TM_BIT6_RESULT`** | — | `0x001EDC` | `memtest.s:625` | — |
| **`TM_BIT7_CHECK`** | — | `0x001EE2` | `memtest.s:628` | — |
| **`TM_BIT7_RESULT`** | — | `0x001EF0` | `memtest.s:634` | — |
| **`TM_CHK_RESET`** | — | `0x001E38` | `memtest.s:549` | — |
| **`TM_CMD_0_ECHO`** | — | `0x002082` | `memtest.s:813` | — |
| **`TM_CMD_1_ECHO`** | — | `0x0020AC` | `memtest.s:829` | — |
| **`TM_CMD_B_ECHO`** | — | `0x001FC2` | `memtest.s:736` | — |
| **`TM_CMD_C_COMPARE`** | — | `0x002016` | `memtest.s:771` | — |
| **`TM_CMD_D_BYTELOOP`** | — | `0x001FEA` | `memtest.s:753` | — |
| **`TM_CMD_D_STORE`** | — | `0x001FF6` | `memtest.s:757` | — |
| **`TM_CMD_G_ECHO_CRLF`** | — | `0x00205A` | `memtest.s:797` | — |
| **`TM_CMD_G_ECHO_G`** | — | `0x00204E` | `memtest.s:793` | — |
| **`TM_CMD_G_ECHO_STAR`** | — | `0x002040` | `memtest.s:788` | — |
| **`TM_CMD_G_JUMP`** | — | `0x002068` | `memtest.s:802` | — |
| **`TM_CMD_L_ECHO`** | — | `0x001F98` | `memtest.s:720` | — |
| **`TM_CMD_M_LOOP`** | — | `0x002158` | `memtest.s:903` | — |
| **`TM_CMD_M_NEXT`** | — | `0x002164` | `memtest.s:908` | — |
| **`TM_CMD_M_PRELOOP`** | — | `0x002154` | `memtest.s:901` | — |
| **`TM_CMD_R_PRINT_FLAGS`** | — | `0x002136` | `memtest.s:887` | — |
| **`TM_CMD_T_CHK_ABORT`** | — | `0x002220` | `memtest.s:993` | — |
| **`TM_CMD_T_CHK_LOOP_ON_ERR`** | — | `0x002204` | `memtest.s:979` | — |
| **`TM_CMD_T_DEC_ITER`** | — | `0x00220A` | `memtest.s:983` | Test passed or no error flags: decrement iteration counter |
| **`TM_CMD_T_DONE`** | — | `0x002224` | `memtest.s:997` | '*T' complete: set status to 'T' and return to prompt |
| **`TM_CMD_T_ECHO_FLAGS`** | — | `0x0021C2` | `memtest.s:951` | — |
| **`TM_CMD_T_GOT_ADDR`** | — | `0x002196` | `memtest.s:933` | — |
| **`TM_CMD_T_GOT_FLAGS`** | — | `0x0021A4` | `memtest.s:939` | — |
| **`TM_CMD_T_REPEAT_FOREVER`** | — | `0x0021FE` | `memtest.s:976` | — |
| **`TM_CMD_T_RESULT`** | — | `0x0021F4` | `memtest.s:971` | — |
| **`TM_CMD_T_RUN`** | — | `0x0021CE` | `memtest.s:957` | '*T' test execution: dispatch test and iterate |
| **`TM_CMD_TRY_0`** | — | `0x002072` | `memtest.s:807` | Command '*0' (0x30) - set A0 (test start address) |
| **`TM_CMD_TRY_1`** | — | `0x00209C` | `memtest.s:823` | Command '*1' (0x31) - set A1 (test end address) |
| **`TM_CMD_TRY_2`** | — | `0x0020C6` | `memtest.s:839` | Command '*2' (0x32) - reserved (no-op) |
| **`TM_CMD_TRY_3`** | — | `0x0020D0` | `memtest.s:844` | Command '*3' (0x33) - reserved (no-op) |
| **`TM_CMD_TRY_4`** | — | `0x0020DA` | `memtest.s:849` | Command '*4' (0x34) - clear the result registers D6 and D7.W |
| **`TM_CMD_TRY_5`** | — | `0x0020E8` | `memtest.s:857` | Command '*5' (0x35) - queue the boot message for the host, repeated about once a second |
| **`TM_CMD_TRY_A`** | — | `0x002104` | `memtest.s:867` | Command '*A' (0x41) - enable hex digit display mode |
| **`TM_CMD_TRY_B`** | — | `0x001FB2` | `memtest.s:730` | Command '*B' (0x42) - Byte count: read 4 hex digits into D4 |
| **`TM_CMD_TRY_C`** | — | `0x002006` | `memtest.s:765` | Command '*C' (0x43) - Checksum: compare expected vs accumulated |
| **`TM_CMD_TRY_D`** | — | `0x001FDC` | `memtest.s:746` | Command '*D' (0x44) - Data: read D4 bytes into memory at (A4)+ |
| **`TM_CMD_TRY_E`** | — | `0x00216C` | `memtest.s:912` | Command '*E' (0x45) - Echo: enable serial echo mode |
| **`TM_CMD_TRY_G`** | — | `0x002030` | `memtest.s:782` | Command '*G' (0x47) - Go: read address, echo "*G", jump to address |
| **`TM_CMD_TRY_H`** | — | `0x002112` | `memtest.s:873` | Command '*H' (0x48) - disable hex digit display mode |
| **`TM_CMD_TRY_I`** | — | `0x00217A` | `memtest.s:918` | Command '*I' (0x49) - Init: full cold restart |
| **`TM_CMD_TRY_L`** | — | `0x001F88` | `memtest.s:714` | Command '*S' (0x53) - service mode request (Apple's USTTestMgr.a): drop the queued boot message and stop its timer Command '*L' (0x4C) - Load address: read 8 hex digits into A4 |
| **`TM_CMD_TRY_M`** | — | `0x002146` | `memtest.s:894` | Command '*M' (0x4D) - Memory dump: print longwords from (A4) |
| **`TM_CMD_TRY_R`** | — | `0x002120` | `memtest.s:879` | Command '*R' (0x52) - Report: print D6 (error) and D7 (flags) |
| **`TM_CMD_TRY_T`** | — | `0x002184` | `memtest.s:927` | Command '*T' (0x54) - Test: read test params and run test by number Reads 8 hex digits for test address, then 4 hex digits for flags. Flags are shifted into D7 bits 28-31 (stop, loop, pram, boot), the... |
| **`TM_CMD_UNKNOWN`** | — | `0x00222C` | `memtest.s:1001` | Unknown command: echo the received character |
| **`TM_DISPATCH_BY_INDEX`** | — | `0x001EF6` | `memtest.s:640` | TM_DISPATCH_BY_INDEX - test dispatch: look up test D1 in TEST_DISPATCH_TBL and jump Called by: TM_SEL6_BITMASK_LOOP, TM_BIT1_CHECK, TM_BIT2_CHECK, TM_BIT3_CHECK, TM_BIT4_CHECK (and 3 more) |
| **`TM_ERROR_CHK_LOOP`** | — | `0x001F12` | `memtest.s:655` | — |
| **`TM_ERROR_REPEAT_FOREVER`** | — | `0x001F0C` | `memtest.s:652` | TM_TEST_ERROR - after a failed test: loop on it (D7 bit 29, loop), stop (bit 28, stop) or go on Called by: TM_BIT0_RESULT, TM_BIT1_RESULT, TM_BIT2_RESULT, TM_BIT3_RESULT, TM_BIT4_RESULT (and 3 more) |
| **`TM_HEX_DIGIT`** | — | `0x00235C` | `memtest.s:1135` | **Regs:** `Entry: D0 = ASCII character Exit: D0 = 0-15 (valid hex digit) or 0 (invalid)`<br>TM_HEX_DIGIT - parse ASCII hex digit to binary nibble Entry: D0 = ASCII character Exit: D0 = 0-15 (valid hex digit) or 0 (invalid) |
| **`TM_HEX_DIGIT_BAD`** | — | `0x002376` | `memtest.s:1146` | — |
| **`TM_HEX_DIGIT_OK`** | — | `0x002374` | `memtest.s:1144` | — |
| **`TM_HEX_PRINT`** | — | `0x0023B4` | `memtest.s:1192` | **Regs:** `Entry: D0 = value, D2 = byte count, A6 = return address (saved to A5)`<br>TM_HEX_PRINT - print hex value to SCC serial port Prints D0 as hex (D2 bytes). With D7 bit 20 (aski) set, prints nibbles with ASCII hex conversion. In byte mode, sends raw bytes. With D7 bit 23 (crlf)... |
| **`TM_HEX_PRINT_CHK_CRLF`** | — | `0x002402` | `memtest.s:1229` | — |
| **`TM_HEX_PRINT_DIGIT`** | — | `0x0023F2` | `memtest.s:1222` | — |
| **`TM_HEX_PRINT_DONE`** | — | `0x002420` | `memtest.s:1239` | — |
| **`TM_HEX_PRINT_LF`** | — | `0x002414` | `memtest.s:1235` | — |
| **`TM_HEX_PRINT_LOOP`** | — | `0x0023D6` | `memtest.s:1209` | — |
| **`TM_HEX_PRINT_LOOP_INIT`** | — | `0x0023D4` | `memtest.s:1207` | — |
| **`TM_HEX_PRINT_NEXT`** | — | `0x0023FE` | `memtest.s:1227` | — |
| **`TM_HEX_PRINT_NIBBLE`** | — | `0x0023E2` | `memtest.s:1215` | — |
| **`TM_HEX_PRINT_SEND`** | — | `0x0023F6` | `memtest.s:1224` | — |
| **`TM_HEX_READ`** | — | `0x00237A` | `memtest.s:1156` | **Regs:** `Entry: D2 = byte count, A6 = return address (saved to A5) Exit: D1 = parsed hex value`<br>TM_HEX_READ - read hex value from serial port Reads D2 bytes from serial; with D7 bit 20 (aski) set, as D2*2 ASCII hex digits. Accumulates into D1. Entry: D2 = byte count, A6 = return address (saved t... |
| **`TM_HEX_READ_BYTE`** | — | `0x0023AA` | `memtest.s:1179` | — |
| **`TM_HEX_READ_GOT_CHAR`** | — | `0x002390` | `memtest.s:1167` | — |
| **`TM_HEX_READ_LOOP`** | — | `0x002388` | `memtest.s:1164` | — |
| **`TM_HEX_READ_LOOP_INIT`** | — | `0x002386` | `memtest.s:1162` | — |
| **`TM_HEX_READ_NEXT`** | — | `0x0023AE` | `memtest.s:1182` | — |
| **`TM_HEX_READ_NIBBLE`** | — | `0x0023A4` | `memtest.s:1175` | — |
| **`TM_ITER_CHK_LOOP_ON_ERR`** | — | `0x001E20` | `memtest.s:537` | — |
| **`TM_ITER_DEC`** | — | `0x001E26` | `memtest.s:540` | — |
| **`TM_ITER_LOOP`** | — | `0x001E0A` | `memtest.s:526` | Test iteration loop: run test via A5, check result, repeat per D7 |
| **`TM_ITER_REPEAT_FOREVER`** | — | `0x001E1A` | `memtest.s:534` | — |
| **`TM_ITER_RESULT`** | — | `0x001E10` | `memtest.s:529` | — |
| **`TM_JUMP_RESET_VEC`** | — | `0x001E42` | `memtest.s:553` | — |
| **`TM_LOOP_NEXT_CHAR`** | — | `0x0022DA` | `memtest.s:1075` | — |
| **`TM_NEXT_ITER`** | — | `0x001F1A` | `memtest.s:659` | TM_NEXT_ITER - advance to next test in bit mask |
| **`TM_POP_AND_RETURN`** | — | `0x001F2E` | `memtest.s:668` | — |
| **`TM_PROMPT`** | — | `0x002238` | `memtest.s:1008` | TM_PROMPT - command prompt: send "*<status>" with CR/LF, then loop Called by: TM_CMD_C_COMPARE, TMRESTART_CHK_PREFIX, TM_CMD_L_ECHO, TM_CMD_B_ECHO, TM_CMD_D_STORE (and 10 more) |
| **`TM_PROMPT_CRLF`** | — | `0x002252` | `memtest.s:1018` | — |
| **`TM_PROMPT_DONE`** | — | `0x002260` | `memtest.s:1023` | — |
| **`TM_PROMPT_STATUS`** | — | `0x002244` | `memtest.s:1012` | — |
| **`TM_RETURN`** | — | `0x001F2C` | `memtest.s:666` | TESTMANAGER return paths |
| **`TM_SEL0_INIT`** | — | `0x001DE4` | `memtest.s:510` | Selector 0: init from parameter block at (A0) |
| **`TM_SEL2_RETURN_NO_SR`** | — | `0x001F34` | `memtest.s:672` | Selector 2: return, discard saved SR (pop SR as data, not to SR) |
| **`TM_SEL3_RESET_STATE`** | — | `0x001F38` | `memtest.s:676` | Selector 3: reset state |
| **`TM_SEL4_DISPATCH_TEST`** | — | `0x001DF0` | `memtest.s:516` | Selector 4: dispatch single test by test number in D7 bits 8-15 |
| **`TM_SEL5_INIT_BITMASK`** | — | `0x001E48` | `memtest.s:557` | Selector 5: init from param block, then run tests by bit mask |
| **`TM_SEL6_BITMASK_LOOP`** | — | `0x001E54` | `memtest.s:565` | Selector 6: run tests by D7 bit mask (bits 8-15 = tests 0-7) Each bit selects a test routine via TEST_DISPATCH_TBL. Tests run in order from bit 8 (test 0) through bit 15 (test 7), skipping unset bits. |
| **`TM_TEST_COMPLETE`** | — | `0x001E2A` | `memtest.s:544` | All iterations done, or stopped on an error (D7 bit 28) |
| **`TM_TEST_ERROR`** | — | `0x001F06` | `memtest.s:649` | TM_TEST_ERROR - after a failed test: loop on it (D7 bit 29, loop), stop (bit 28, stop) or go on Called by: TM_BIT0_RESULT, TM_BIT1_RESULT, TM_BIT2_RESULT, TM_BIT3_RESULT, TM_BIT4_RESULT (and 3 more) |
| **`TMENTRY1`** | — | `0x001F3C` | `memtest.s:684` | TMRESTART - diagnostic test manager main loop Initializes SCC serial port, then enters an infinite loop reading commands via serial. Commands are single ASCII characters prefixed by '*'. The loop: ini... |
| **`TMRESTART`** | — | `0x001F3C` | `memtest.s:685` | TMRESTART - diagnostic test manager main loop Initializes SCC serial port, then enters an infinite loop reading commands via serial. Commands are single ASCII characters prefixed by '*'. The loop: ini... |
| **`TMRESTART_CHK_PREFIX`** | — | `0x001F6A` | `memtest.s:702` | — |
| **`TMRESTART_PARSE_CHAR`** | — | `0x001F52` | `memtest.s:694` | Command parser: D5 = received character |
| **`TMRESTART_SCC_INIT_DONE`** | — | `0x001F4A` | `memtest.s:690` | — |
| **`TRACE`** | — | `0x001B2A` | `memtest.s:184` | — |
| **`Trap0_53`** | `0x0001F8` | — | `vectors.s:377` | RTC serial protocol: sends a command byte, receives a response byte. Uses VIA PortB bits: PB0=data, PB1=clock, PB2=enable (active low). Protocol: enable RTC (PB2=0), clock out 8 command bits on PB0/PB... |
| **`Trap0_55`** | `0x000806` | — | `vectors.s:1216` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap0_56`** | `0x000806` | — | `vectors.s:1213` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap0_5B`** | `0x000806` | — | `vectors.s:1215` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap0_5C`** | `0x000806` | — | `vectors.s:1217` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap0_5D`** | `0x000806` | — | `vectors.s:1219` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap0_5E`** | `0x000806` | — | `vectors.s:1218` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap0_5F`** | `0x000806` | — | `vectors.s:1214` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap0_6B`** | `0x000806` | — | `vectors.s:1212` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_0`** | `0x000806` | — | `vectors.s:1236` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_1`** | `0x000806` | — | `vectors.s:1237` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_14`** | `0x000806` | — | `vectors.s:1224` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_1C3`** | `0x000806` | — | `vectors.s:1246` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_2`** | `0x000806` | — | `vectors.s:1238` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_3`** | `0x000806` | — | `vectors.s:1233` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_3C`** | `0x000806` | — | `vectors.s:1221` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_3D`** | `0x000806` | — | `vectors.s:1222` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_3E`** | `0x000806` | — | `vectors.s:1229` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_4`** | `0x000806` | — | `vectors.s:1234` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_5`** | `0x000806` | — | `vectors.s:1235` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_6`** | `0x000806` | — | `vectors.s:1242` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_60`** | `0x000806` | — | `vectors.s:1228` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_7`** | `0x000806` | — | `vectors.s:1243` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_8`** | `0x000806` | — | `vectors.s:1244` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_8F`** | `0x000806` | — | `vectors.s:1230` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_9`** | `0x000806` | — | `vectors.s:1239` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_95`** | `0x000806` | — | `vectors.s:1220` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_9F`** | `0x000806` | — | `vectors.s:1225` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_A`** | `0x000806` | — | `vectors.s:1240` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_B`** | `0x000806` | — | `vectors.s:1241` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_B5`** | `0x000806` | — | `vectors.s:1223` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_C`** | `0x000806` | — | `vectors.s:1232` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_D7`** | `0x000806` | — | `vectors.s:1245` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_F7`** | `0x000806` | — | `vectors.s:1248` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`Trap1_FD`** | `0x000806` | — | `vectors.s:1249` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`TRAPN`** | — | `0x001B5C` | `memtest.s:205` | — |
| **`TRY_NEXT_DRIVE`** | `0x00077C` | — | `vectors.s:1109` | TRY_NEXT_DRIVE - advance to next drive in queue; check SCSI if available |
| **`Unimplemented`** | `0x000806` | — | `vectors.s:1250` | Shows the "unimplemented trap" error icon (ID=12) and halts. Every trap slot the ROM leaves empty points here; trap $A89F is _Unimplemented itself. MacPlusROM.lst lists those slots at this address: OS... |
| **`USE_BOOT_HEAP`** | — | `0x00085E` | `boot_load.s:56` | Fractional heap: size = SysZone + base + (MemTop * fraction) |
| **`USE_FIXED_HEAP`** | — | `0x000862` | `boot_load.s:58` | — |
| **`VERIFY_LOOP`** | `0x000E96` | — | `memtest.s:206` | Verify loop: reads back 12 bytes at a time, XORs with expected pattern |
| **`VIA_BITBANG_8BITS`** | — | `0x002558` | `memtest.s:1383` | VIA_BITBANG_8BITS - shift 8 bits out via VIA port A bit-bang Sends D1 (8 bits) to the DFAC sound attenuator via VIA port A, bit-banging the serial data through the shift register protocol. Bit 1 of VI... |
| **`VIA_BITBANG_LOOP`** | — | `0x002560` | `memtest.s:1386` | — |
| **`VIA_T1_CHECK_RELOAD`** | — | `0x0024CA` | `memtest.s:1311` | **Regs:** `Entry: D0 = reload count (used when countdown reaches 0) Exit: D0 bit 15 set if countdown expired`<br>VIA_T1_CHECK_RELOAD - check/reload VIA Timer 1 for beep countdown Checks if Timer 1 has expired (IFR bit 5). If expired, reloads timer and decrements the beep countdown in D4 high word. Entry: D0 = re... |
| **`VIA_T1_INIT_BEEP`** | — | `0x0024AC` | `memtest.s:1298` | VIA_T1_INIT_BEEP - init VIA Timer 1 for periodic beep Configures Timer 1 in free-run mode with maximum interval (0xFFFF). The timer generates periodic interrupts used for boot beep timing. |
| **`VIA_T1_RESTORE_D4`** | — | `0x0024FA` | `memtest.s:1324` | — |
| **`VIA_T1_RETURN`** | — | `0x0024FC` | `memtest.s:1326` | — |
| **`VIATIMERENABLES`** | — | `0x00054E` | `boot_install.s:581` | VIATIMERENABLES - enable VIA Timer 1 and Timer 2 interrupts |
| **`VISUALUPDATE`** | — | `0x000E30` | `boot_search.s:258` | VISUALUPDATE - animate boot disk icon during device search Alternates between plain disk, disk-with-X (bad), and disk-with-? icons every 60 ticks (1 second) during the boot search loop. D6 bits: 8=ini... |
| **`VISUPD_FLASH`** | — | `0x000E5A` | `boot_search.s:273` | — |
| **`VISUPD_QUESTION`** | — | `0x000E66` | `boot_search.s:279` | — |
| **`VISUPD_RTS`** | — | `0x000E6A` | `boot_search.s:281` | — |
| **`VISUPD_TOGGLE`** | — | `0x000E4E` | `boot_search.s:268` | — |
| **`WAIT_DRIVE_READY`** | `0x0006E8` | — | `vectors.s:1040` | Initialize QuickDraw graphics system A5 = QuickDraw globals pointer (above current SP) Draw the Happy Mac icon with startup disk icon Draw question-mark disk icon (waiting for boot disk) Wait until Dr... |
| **`WaitForBootDisk`** | `0x0006F4` | — | `vectors.s:1050` | Uses the stack as an IOParam block (A0 = SP). Reads the first 1024 bytes from each drive and checks for the boot block signature 0x4C4B ("LK") at offset 0. Called during boot. |
| **`WAITFORINTERNAL`** | — | `0x000D24` | `boot_search.s:103` | WAITFORINTERNAL - wait for internal floppy disk to become ready Polls drive queue for floppy insertion. Checks keyboard for Cmd-Opt-Shift-Delete (skip internal drive, $8805 in KeyMap). Times out after... |
| **`WAITINT_CHECK_TIME`** | — | `0x000D6E` | `boot_search.s:136` | — |
| **`WAITINT_CLEANUP`** | — | `0x000D7A` | `boot_search.s:141` | — |
| **`WAITINT_DONE`** | — | `0x000D80` | `boot_search.s:144` | — |
| **`WAITINT_GOT_TIMEOUT`** | — | `0x000D3E` | `boot_search.s:117` | — |
| **`WAITINT_POLL`** | — | `0x000D4A` | `boot_search.s:122` | — |
| **`WAITINT_SCAN_DQ`** | — | `0x000D5E` | `boot_search.s:130` | — |
| **`WARMSTART_CHECK`** | — | `0x00007C` | `boot_install.s:53` | WARMSTART_CHECK - check for warm-start signature before RAM test If WarmStart == 'WLSC' ($574C5343), the machine was warm-restarted and RAM contents are presumed good; skip the destructive RAM test. |
| **`WDCBSWOS`** | — | `0x000340` | `boot_install.s:322` | WDCBSWOS/PMSPSWOS - context switch parameter sizes |
| **`WHICHCPU`** | — | `0x0003EE` | `boot_install.s:423` | WHICHCPU - detect CPU type (68000 vs 68010 vs 68020+) Attempts to execute MOVEC D0,CACR (68020+ instruction). If it causes an illegal instruction exception: 68010 or 68000. Distinguishes 68010 from 68... |
| **`WHICHCPU_DONE`** | — | `0x000414` | `boot_install.s:440` | — |
| **`WHICHCPU_TRAP`** | — | `0x000408` | `boot_install.s:435` | Illegal instruction trap handler: MOVEC caused exception |
| **`WRITE_RTC_BIT_LOOP`** | `0x000256` | `0x00A31E` | `vectors.s:455`<br>`rtc.s:132` | WriteRTCByte bit-shift loop |
| **`WriteRTCByte`** | `0x000254` | `0x00A31C` | `vectors.s:452`<br>`rtc.s:129` | Write 8 bits to RTC via VIA PortB bit-bang serial. Shifts D1 MSB-first out through PB0 (data), clocking PB1 (clock) for each bit. return address in A6 Called during boot. |
| **`WRITESCC`** | — | `0x0005BA` | `boot_install.s:651` | WRITESCC - write D1+1 bytes from (A2) to SCC register (A0) Includes delay loops (MOVE.L (SP),(SP)) for SCC register settling. |
| **`XMARK`** | — | `0x000F94` | `boot_search.s:441` | XMARK - X mark bitmap (16x16, 30 bytes) |
| **`XTRAPX`** | — | `0x001B1A` | `memtest.s:178` | — |
| **`ZERERROR`** | — | `0x001B0A` | `memtest.s:172` | — |

---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

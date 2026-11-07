# Hardware & Interrupts Function & Routine Directory

This catalog lists all **56** routines, functions, exception vectors, and labels belonging to the **Hardware & Interrupts** subsystem across the Macintosh Plus (128 KB) and Macintosh SE (256 KB) ROMs.

| Symbol / Routine | Mac Plus Offset | Mac SE Offset | Source File : Line | Description / Prototype |
| :--- | :--- | :--- | :--- | :--- |
| **`CLKNOMEM`** | `0x0001F8` | `0x00A2C0` | `rtc.s:85` | — |
| **`ClkRW`** | `0x00FDF2` | `0x00A23C` | `rtc.s:19` | Clock chip (RTC) access -- ClkRW, _ReadXPRam, _WriteXPRam Apple source: Clock.a (MacSEROM.lst module CLOCK). The real-time clock is a serial device on VIA port B (data, clock and enable lines; vRTCDat... |
| **`CLKRW`** | `0x00FDF2` | `0x00A23C` | `rtc.s:15` | Clock chip (RTC) access -- ClkRW, _ReadXPRam, _WriteXPRam, ClkNoMem Apple source: Clock.a (MacSEROM.lst module CLOCK). The real-time clock is a serial device on VIA port B (data, clock and enable line... |
| **`CLKRW_CONT`** | `0x00FE0A` | `0x00A254` | `rtc.s:41`<br>`rtc.s:35` | CLKRW_CONT Called during boot. |
| **`CLKRW_EXIT`** | `0x00FE02` | `0x00A24C` | `rtc.s:31`<br>`rtc.s:26` | CLKRW_EXIT Called during boot. |
| **`CLOCK`** | — | `0x00A23C` | `rtc.s:14` | Clock chip (RTC) access -- ClkRW, _ReadXPRam, _WriteXPRam, ClkNoMem Apple source: Clock.a (MacSEROM.lst module CLOCK). The real-time clock is a serial device on VIA port B (data, clock and enable line... |
| **`EXTAINT`** | — | `0x002B94` | `interrupts.s:72` | EXTAINT - SCC channel A external/status change interrupt |
| **`ExtAInt_StatusChngSCC`** | `0x001AC2` | — | `interrupts.s:141` | ExtAInt_StatusChngSCC - SCC channel A external/status change Handles DCD transitions on channel A (mouse X1 quadrature). |
| **`EXTBINT`** | — | `0x002B88` | `interrupts.s:66` | EXTBINT - SCC channel B external/status change interrupt Reads RR0, compares with saved status to detect DCD transitions (used for mouse quadrature input via SCC DCD pins). |
| **`ExtBInt_StatusChngSCC`** | `0x001AB6` | — | `interrupts.s:129` | ExtBInt_StatusChngSCC - SCC channel B external/status change Handles DCD transitions on channel B (mouse Y1 quadrature). Compares old vs new RR0 to detect which ext/status bit changed, then dispatches... |
| **`EXTSTATUS_DISPATCH`** | `0x001ACC` | `0x002B9E` | `interrupts.s:154`<br>`interrupts.s:81` | EXTSTATUS_DISPATCH - Common ext/status dispatch for both SCC channels Reads WR15 (ext/status interrupt enable mask), XORs old and new RR0 to find changed bits, ANDs with WR15 to isolate enabled change... |
| **`EXTSTATUS_RESET`** | `0x001AE0` | `0x002BB2` | `interrupts.s:163`<br>`interrupts.s:90` | — |
| **`INTHND`** | — | `0x002B2E` | `interrupts.s:20` | Interrupt handlers (VIA, SCC) Apple source: InterruptHandlers.a (MacSEROM.lst module INTHND): LVL1INT (VIA: one-second interrupt, VBL, the ADB shift register, timer 2 of the Time Manager, ... dispatch... |
| **`LVL1_RETURN`** | `0x001A7E` | — | `interrupts.s:85` | — |
| **`LVL1INT`** | — | `0x002B2E` | `interrupts.s:21` | Interrupt handlers (VIA, SCC) Apple source: InterruptHandlers.a (MacSEROM.lst module INTHND): LVL1INT (VIA: one-second interrupt, VBL, the ADB shift register, timer 2 of the Time Manager, ... dispatch... |
| **`Lvl1Int_VIA`** | `0x001A42` | — | `interrupts.s:31` | Interrupt Handlers (VIA, SCC, Keyboard, Mouse) 68000 auto-vector interrupts: Level 1 (VIA): timer 1 (sound/VBL), timer 2, keyboard shift register, one-second tick, VBL (via timer 1) Level 2 (SCC): ser... |
| **`LVL1RTS`** | — | `0x002BE2` | `interrupts.s:109` | — |
| **`LVL2INT`** | — | `0x002B56` | `interrupts.s:42` | LVL2INT - Level 2 interrupt handler (SCC) 68000 auto-vector level 2 (vector $68). Reads SCC RR2B modified vector to identify source (bits [3:1] = interrupt type). Channel A sources use offsets >= 8, c... |
| **`Lvl2Int_SCC`** | `0x001A84` | — | `interrupts.s:100` | Level 2 Interrupt: SCC (vector $68) SCC interrupt flags = SCCBControl[3:1] Reads RR2B to identify interrupt source, dispatches via Lvl2DT. RR2B modified vector bits [3:1] encode the source: 0x0=Ch B T... |
| **`LVL2RTS`** | — | `0x002BE2` | `interrupts.s:110` | — |
| **`MOUSE_MOVE_DOWN`** | `0x001C1E` | — | `interrupts.s:327` | MOUSE_MOVE_DOWN - Mouse move down |
| **`MOUSE_MOVE_LEFT`** | `0x001BF4` | — | `interrupts.s:301` | MOUSE_MOVE_LEFT - Mouse move left |
| **`ONESEC_DONE`** | `0x001B10` | — | `interrupts.s:187` | — |
| **`ONESECINT`** | — | `0x002BBA` | `interrupts.s:98` | ONESECINT - one-second interrupt handler (VIA CA1) Increments the system clock (Time global), checks alarm state. If alarm time has passed, signals the alarm by clearing AlarmState bit 1. |
| **`OneSecInt_VIA`** | `0x001AE8` | — | `interrupts.s:176` | OneSecInt_VIA - One-second interrupt handler Called during boot. Triggered by VIA CA1 every second. Increments global time counter (seconds since 1/1/1904), clears the one-second IFR flag, and checks ... |
| **`ReadXPRam`** | `0x00FE18` | `0x00A262` | `rtc.s:55` | _ReadXPRam ($A051) Called during boot. |
| **`READXPRAM`** | `0x00FE18` | `0x00A262` | `rtc.s:43` | — |
| **`RTC_READ_DATA_BYTE`** | — | `0x00A30E` | `rtc.s:117` | — |
| **`RTC_READ_PATH`** | — | `0x00A306` | `rtc.s:114` | — |
| **`RTC_SEND_DATA_BYTE`** | — | `0x00A2FA` | `rtc.s:108` | — |
| **`SCC_DISPATCH_JMP`** | `0x001AA8` | `0x002B7A` | `interrupts.s:113`<br>`interrupts.s:55` | — |
| **`SCCInt_AChng_MouseH`** | `0x001BD8` | — | `interrupts.s:287` | Mouse quadrature interrupt handlers on entry, D0 = newest channel A/B RR0 value. Bit 3 = X1 or Y1. Mouse horizontal tracking: SCC channel A DCD transitions = X1 quadrature. X2 comes from VIA PortB bit... |
| **`SCCInt_BChng_MouseV`** | `0x001C00` | — | `interrupts.s:312` | SCCInt_BChng_MouseV - Mouse vertical quadrature handler Mouse vertical tracking: SCC channel B DCD transitions = Y1 quadrature. Y2 comes from VIA PortB bit 5. Direction = Y1 XOR Y2. |
| **`SCSI_INT_CHECK`** | `0x001A4C` | — | `interrupts.s:57` | SCSI_INT_CHECK SCSI pseudo-DMA interrupt check (Mac Plus only). If NCR 5380 has a pending interrupt, acknowledge it and return from the level-1 handler without VIA dispatch. |
| **`SPURIOUS`** | — | `0x002B86` | `interrupts.s:60` | — |
| **`Spurious_IntVIAandSCC`** | `0x001AB4` | — | `interrupts.s:118` | — |
| **`VBL_BTN_DONE`** | `0x001B92` | — | `interrupts.s:240` | — |
| **`VBL_CHECK_BTN_CHG`** | `0x001B62` | `0x003A5E` | `interrupts.s:225`<br>`adb_mgr.s:792` | — |
| **`VBL_CHECK_HEAP`** | `0x001B38` | `0x002C08` | `interrupts.s:209`<br>`interrupts.s:128` | Stack overflow detection |
| **`VBL_CURSOR_TASK`** | `0x001B46` | `0x002C14` | `interrupts.s:215`<br>`interrupts.s:135` | Cursor task and VBL task queue processing |
| **`VBL_TASK_LOOP`** | `0x001BAC` | `0x002C24` | `interrupts.s:261`<br>`interrupts.s:148` | — |
| **`VBL_TASK_NEXT`** | `0x001BCC` | `0x002C44` | `interrupts.s:273`<br>`interrupts.s:160` | — |
| **`VBL_TASK_QUEUE`** | `0x001BA6` | `0x002C1E` | `interrupts.s:258`<br>`interrupts.s:145` | VBL task queue processing Walks the VBL queue (linked list at VBLQueueHdr). For each task, decrements vblCount. When count reaches zero, calls the task's vblAddr routine. If vblCount is still zero aft... |
| **`VBL_TASKS_DONE`** | `0x001BD0` | `0x002C48` | `interrupts.s:276`<br>`interrupts.s:163` | — |
| **`VBLINT`** | — | `0x002BE4` | `interrupts.s:116` | VBLINT - vertical blanking interrupt handler (VIA Timer 1) Called 60.15 times per second. Increments Ticks, processes the VBL task queue, checks stack overflow, and calls the cursor task. |
| **`VBLInt_VIA`** | `0x001B12` | — | `interrupts.s:198` | VBLInt_VIA - Vertical blanking interrupt handler (60.15 Hz) Called during boot. VIA Timer 1 fires at 60.15 Hz (every vertical blank interval). Increments Ticks, processes mouse button via VIA PortB bi... |
| **`VIA_DISPATCH`** | `0x001A60` | — | `interrupts.s:73` | VIA_DISPATCH - VIA interrupt source identification and dispatch Reads IFR ANDed with IER to find which VIA interrupt fired. Scans bits 0-6 (Timer2, Timer1, CB1/keyboard, CB2, SR, CA1/1sec, CA2/VBL) vi... |
| **`VIA_SCAN_NEXT`** | `0x001A74` | `0x002B46` | `interrupts.s:79`<br>`interrupts.s:28` | — |
| **`WriteXPRam`** | `0x00FE22` | `0x00A26C` | `rtc.s:66` | WriteXPRam -- trap handler for _WriteXPRam ($A052). _WriteXPRam ($A052) |
| **`WRITEXPRAM`** | `0x00FE22` | `0x00A26C` | `rtc.s:48` | — |
| **`WRITEXPRAM_CONT`** | `0x00FE2E` | `0x00A278` | `rtc.s:71`<br>`rtc.s:53` | — |
| **`WRITEXPRAM_ERR`** | `0x00FE72` | `0x00A2BC` | `rtc.s:105`<br>`rtc.s:82` | WRITEXPRAM_ERR |
| **`WRITEXPRAM_EXIT`** | `0x00FE6C` | `0x00A2B6` | `rtc.s:97`<br>`rtc.s:79` | — |
| **`WRITEXPRAM_LOOP`** | `0x00FE36` | `0x00A280` | `rtc.s:74`<br>`rtc.s:56` | — |
| **`WRITEXPRAM_LOOP_2`** | `0x00FE42` | `0x00A28C` | `rtc.s:80`<br>`rtc.s:62` | — |
| **`WRITEXPRAM_LOOP_3`** | `0x00FE4A` | `0x00A294` | `rtc.s:84`<br>`rtc.s:66` | — |

---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

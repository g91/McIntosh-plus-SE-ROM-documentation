# OS Kernel Function & Routine Directory

This catalog lists all **3,043** routines, functions, exception vectors, and labels belonging to the **OS Kernel** subsystem across the Macintosh Plus (128 KB) and Macintosh SE (256 KB) ROMs.

| Symbol / Routine | Mac Plus Offset | Mac SE Offset | Source File : Line | Description / Prototype |
| :--- | :--- | :--- | :--- | :--- |
| **`Actuals`** | `0x0108CC` | `0x00AE8A` | `memory_mgr.s:2207` | Actuals - convert a logical size to a physical block size D0.L = D0 + 8 (header), rounded up to even, at least 12. Called during boot (34,515 times in 30s trace). |
| **`ACTUALS`** | `0x0108CC` | `0x00AE8A` | `memory_mgr.s:1599` | Called by: MAXBLOCK_OR_COMPACT, PURGEMEM, ALLOCBK, SETSIZE, MAKEPTRSPC |
| **`ACTUALS_OK`** | `0x0108DE` | `0x00AE9C` | `memory_mgr.s:2214`<br>`memory_mgr.s:1606` | — |
| **`ADB_AFTER_SEND`** | — | `0x00366E` | `adb_mgr.s:388` | ADB_AFTER_SEND - PIC INT received: process response after send |
| **`ADB_BEGIN_SEND`** | — | `0x003648` | `adb_mgr.s:377` | ADB_BEGIN_SEND - start new send transaction (no prior state) |
| **`ADB_BEGIN_TXN`** | — | `0x0036DA` | `adb_mgr.s:426` | ADB_BEGIN_TXN - start fresh ADB transaction |
| **`ADB_BUS_SCAN`** | — | `0x003334` | `adb_mgr.s:34` | ADB_BUS_SCAN - ADB bus scan and device initialization |
| **`ADB_CALL_COMPLETION`** | — | `0x003682` | `adb_mgr.s:395` | ADB_CALL_COMPLETION/03686 - call completion callback |
| **`ADB_CALL_COMPLETION_DO`** | — | `0x003686` | `adb_mgr.s:397` | — |
| **`ADB_CHK_SRQ`** | — | `0x00370A` | `adb_mgr.s:443` | ADB_CHK_SRQ - check for SRQ or scan-in-progress |
| **`ADB_COPY_DEVTBL`** | — | `0x003D28` | `adb_mgr.s:1144` | ADB_COPY_DEVTBL - copy device table entry to ADBDataBlock |
| **`ADB_COPY_DEVTBL_RTS`** | — | `0x003D4A` | `adb_mgr.s:1167` | — |
| **`ADB_DEQUEUE_INVALIDATE`** | — | `0x003FF8` | `event_mgr.s:180` | ADB_DEQUEUE_INVALIDATE (DequeueAndInvalidate) -- unlink + mark slot free |
| **`ADB_DEQUEUE_RTS`** | — | `0x003FF6` | `event_mgr.s:177` | — |
| **`ADB_DONE_CLR_PENDING`** | — | `0x003C78` | `adb_mgr.s:1055` | ADB_DONE_CLR_PENDING - simple ADB completion: clear pending flag |
| **`ADB_DONE_RTS`** | — | `0x003C8C` | `adb_mgr.s:1067` | — |
| **`ADB_ENSURE_MOUSE`** | — | `0x003D6E` | `adb_mgr.s:1196` | ADB_ENSURE_MOUSE - ensure keyboard and mouse entries exist in device table If no device at address 2 (keyboard), creates a default entry. If no device at address 3 (mouse), creates a default entry. Us... |
| **`ADB_ENSURE_MOUSE_LOOP`** | — | `0x003D8E` | `adb_mgr.s:1207` | No keyboard found: create default entry |
| **`ADB_ENSURE_MOUSE_RTS`** | — | `0x003DAC` | `adb_mgr.s:1217` | No mouse found: create default entry |
| **`ADB_EXEC_COMMAND`** | — | `0x0037D2` | `adb_mgr.s:513` | ADB_EXEC_COMMAND - set up ADB poll/command cycle Prepares for an ADB Talk command by looking up the device's handler and data pointers in the device table, building the command byte, and initiating th... |
| **`ADB_EXEC_FALLBACK`** | — | `0x003808` | `adb_mgr.s:528` | Device not found at this address: fall back to address 3 (mouse) |
| **`ADB_EXEC_NOW`** | — | `0x0038DA` | `adb_mgr.s:612` | Execute ADB command immediately |
| **`ADB_EXEC_NOW_RTS`** | — | `0x0038F6` | `adb_mgr.s:621` | — |
| **`ADB_FIND_DEVICE`** | — | `0x003D4C` | `adb_mgr.s:1174` | **Regs:** `Entry: D0 = ADB address to find Exit: A1 = device entry pointer, D0 = 0 if found, -1 if not`<br>ADB_FIND_DEVICE - find device table entry by ADB address Entry: D0 = ADB address to find Exit: A1 = device entry pointer, D0 = 0 if found, -1 if not Called by: ADB_EXEC_COMMAND, GETADBINFO, SETADBINFO... |
| **`ADB_FIND_DEVICE_FOUND`** | — | `0x0034D8` | `adb_mgr.s:215` | — |
| **`ADB_FIND_DEVICE_LOOP`** | — | `0x0034CC` | `adb_mgr.s:210` | Search device table for entry with matching current address |
| **`ADB_FIND_DEVICE_LOOP2`** | — | `0x003D54` | `adb_mgr.s:1178` | — |
| **`ADB_FIND_DEVICE_NEXT`** | — | `0x003D58` | `adb_mgr.s:1180` | — |
| **`ADB_FIND_DEVICE_OK`** | — | `0x003D6A` | `adb_mgr.s:1188` | — |
| **`ADB_FIND_DEVICE_RTS`** | — | `0x003D66` | `adb_mgr.s:1185` | — |
| **`ADB_FIND_FREE_FWD`** | — | `0x003552` | `adb_mgr.s:266` | ADB_FIND_FREE_FWD - find next free ADB address for device relocation Scans the device present bitmap for an address that's not yet used. Returns: D0 = free address (N clear), or N set if none free |
| **`ADB_FIND_FREE_FWD_LOOP`** | — | `0x00355E` | `adb_mgr.s:272` | Scan bitmap starting from current address |
| **`ADB_FIND_FREE_FWD_RTS`** | — | `0x00356E` | `adb_mgr.s:280` | — |
| **`ADB_FIND_OCCUPIED_REV`** | — | `0x003574` | `adb_mgr.s:287` | ADB_FIND_OCCUPIED_REV - find highest occupied ADB address (for conflict scan) Scans bitmap from address 15 downward to find the first occupied slot. Returns: D0 = address (N clear if found), N set if ... |
| **`ADB_FIND_OCCUPIED_REV_LOOP`** | — | `0x00357C` | `adb_mgr.s:291` | — |
| **`ADB_FIND_OCCUPIED_REV_RTS`** | — | `0x003584` | `adb_mgr.s:296` | — |
| **`ADB_HANDLER_KBD`** | — | `0x003AC0` | `adb_mgr.s:838` | ADB_HANDLER_KBD - ADB keyboard handler (device address 2) Processes keyboard data from ADB Talk Reg 0 response. ADB keyboard register 0: 2 bytes, each containing a keycode. Bit 7 = key state (0 = down... |
| **`ADB_HANDLER_MOUSE`** | — | `0x003A54` | `adb_mgr.s:787` | ADB_HANDLER_MOUSE - ADB mouse handler (device address 3) Processes mouse data from ADB Talk Reg 0 response. ADB mouse register 0: byte 0 = button + Y delta, byte 1 = X delta. Bit 7 of byte 0: button s... |
| **`ADB_IDLE`** | — | `0x0037BC` | `adb_mgr.s:501` | ADB_IDLE - idle: no pending ADB work, run explicit command if any |
| **`ADB_INIT_WAIT`** | — | `0x00335E` | `adb_mgr.s:45` | — |
| **`ADB_INSTALL_BODY`** | — | `0x003CE8` | `adb_mgr.s:1109` | — |
| **`ADB_INSTALL_FOUND`** | — | `0x003CFC` | `adb_mgr.s:1122` | — |
| **`ADB_INSTALL_LOOP`** | — | `0x003CF0` | `adb_mgr.s:1114` | — |
| **`ADB_INTERNAL_DISPATCH`** | — | `0x003890` | `adb_mgr.s:586` | ADB_INTERNAL_DISPATCH - internal ADB command dispatch (registers pre-loaded) |
| **`ADB_INTERNAL_DISPATCH_BUSY`** | — | `0x003894` | `adb_mgr.s:588` | — |
| **`ADB_INTERNAL_DISPATCH_PEND`** | — | `0x0038B6` | `adb_mgr.s:597` | — |
| **`ADB_INTERNAL_DISPATCH_PUSH`** | — | `0x0038D2` | `adb_mgr.s:607` | — |
| **`ADB_INTERNAL_DISPATCH_QUEUE`** | — | `0x0038C6` | `adb_mgr.s:602` | — |
| **`ADB_KICK_PIC`** | — | `0x00396C` | `adb_mgr.s:686` | ADB_KICK_PIC - initiate ADB transaction: set active flag + trigger PIC Called by: ADB_SCAN_DEVICE, ADB_TALK_REG3, ADB_LISTEN_REG3, ADB_POLL_DEVICES, ADB_POLL_KBD (and 2 more) |
| **`ADB_LISTEN_REG3`** | — | `0x003524` | `adb_mgr.s:250` | **Regs:** `Entry: D0 = device address, D1 = new address data, A0 = callback`<br>ADB_LISTEN_REG3 - issue ADB Listen Register 3 command (Move device) Sends Listen Reg 3 with 2-byte data (new_addr, 0xFE) to relocate an ADB device from its current address to a new one. Entry: D0 = de... |
| **`ADB_MOVE_COMPLETE`** | — | `0x003468` | `adb_mgr.s:169` | ADB_MOVE_COMPLETE - ADB Move command completion: verify move succeeded After moving a device to a new address, Talk the new address to confirm the device responds there. If successful, update device t... |
| **`ADB_MOVE_NEXT_ADDR`** | — | `0x003496` | `adb_mgr.s:185` | — |
| **`ADB_MOVE_RESCAN`** | — | `0x0034A0` | `adb_mgr.s:189` | — |
| **`ADB_MOVE_RESCAN_RTS`** | — | `0x0034B0` | `adb_mgr.s:194` | — |
| **`ADB_MOVE_RETRY`** | — | `0x003486` | `adb_mgr.s:180` | Move failed: retry with different target address |
| **`ADB_MOVE_TALK_NEW`** | — | `0x003474` | `adb_mgr.s:173` | — |
| **`ADB_NEXT_ADDRESS`** | — | `0x00339C` | `adb_mgr.s:89` | ADB_NEXT_ADDRESS - ADB scan callback: issue Talk Reg 0 to next address Called by the VIA shift interrupt after PIC completes a Talk command. Advances to next ADB address, issues Talk Reg 0 via ADB_TAL... |
| **`ADB_NEXT_BYTE`** | — | `0x00383E` | `adb_mgr.s:548` | ADB_NEXT_BYTE - read ADB response byte from VIA SR into buffer Reads the byte from VIA shift register (if in input mode) and stores it at the current buffer position. Advances the byte counter. Return... |
| **`ADB_NEXT_BYTE_IN`** | — | `0x003870` | `adb_mgr.s:565` | — |
| **`ADB_NEXT_BYTE_OUT`** | — | `0x00385E` | `adb_mgr.s:559` | SR output mode: write next data byte to PIC via VIA SR |
| **`ADB_NEXT_BYTE_RTS`** | — | `0x003876` | `adb_mgr.s:568` | — |
| **`ADB_NEXT_POLL`** | — | `0x003700` | `adb_mgr.s:439` | ADB_NEXT_POLL - start next ADB idle poll |
| **`ADB_PHASE_DISPATCH`** | — | `0x003610` | `adb_mgr.s:357` | ADB_PHASE_DISPATCH - send phase: write or read VIA SR based on cmd direction |
| **`ADB_POLL_DEVICES`** | — | `0x003722` | `adb_mgr.s:455` | ADB_POLL_DEVICES - ADB auto-poll: walk device table, poll next device Iterates through the device table (12 bytes/entry at +$C0) and issues Talk Reg 0 to each registered device's current address. Uses... |
| **`ADB_POLL_DEVICES_RTS`** | — | `0x003770` | `adb_mgr.s:476` | — |
| **`ADB_POLL_KBD`** | — | `0x003778` | `adb_mgr.s:484` | ADB_POLL_KBD - handle Service Request (SRQ) from ADB device An ADB device asserted SRQ during the last transaction. Poll the first device in the table (keyboard at address 2) to service the request. S... |
| **`ADB_QUEUE_POP`** | — | `0x003A16` | `adb_mgr.s:757` | ADB_QUEUE_POP - dequeue ADB command from circular buffer Reads next pending command from the queue into registers. Returns with D0 = cmd, A0 = data, A1 = completion, A2 = refCon. Sets bit 2 of +$15D (... |
| **`ADB_QUEUE_POP_EMPTY`** | — | `0x003A40` | `adb_mgr.s:770` | — |
| **`ADB_QUEUE_POP_HAVE`** | — | `0x003A50` | `adb_mgr.s:776` | — |
| **`ADB_QUEUE_POP_RTS`** | — | `0x003A4C` | `adb_mgr.s:774` | — |
| **`ADB_QUEUE_PREEMPT`** | — | `0x003994` | `adb_mgr.s:702` | ADB_QUEUE_PREEMPT - save current ADB state and queue for later Saves the current command/completion/data to the ADB queue so the current transaction can be preempted by a higher-priority one. |
| **`ADB_QUEUE_PUSH`** | — | `0x0039D2` | `adb_mgr.s:729` | ADB_QUEUE_PUSH - enqueue ADB command into circular buffer ADB command queue is a circular buffer of 14-byte entries at +$C0. Each entry: +0 = cmd byte, +2 = data ptr, +6 = completion, +A = refCon. +$1... |
| **`ADB_QUEUE_PUSH_FULL`** | — | `0x003A0E` | `adb_mgr.s:747` | — |
| **`ADB_QUEUE_PUSH_RTS`** | — | `0x003A12` | `adb_mgr.s:749` | — |
| **`ADB_QUEUE_RESTORE`** | — | `0x0039B2` | `adb_mgr.s:716` | ADB_QUEUE_RESTORE - restore saved ADB poll state after preemption Restores command, length, buffer, completion, and data pointers from the saved poll state ($16E-$16F, $158, $150, $154). |
| **`ADB_RECORD_AFTER_HANDLER`** | — | `0x0033E8` | `adb_mgr.s:118` | — |
| **`ADB_RECORD_DEVICE`** | — | `0x0033AA` | `adb_mgr.s:99` | ADB_RECORD_DEVICE - process Talk Reg 0 response during scan If device responded (no error), records it in the device table: handler_id, original address, current address, and installs the appropriate ... |
| **`ADB_RECORD_NOT_KBD`** | — | `0x0033DA` | `adb_mgr.s:113` | — |
| **`ADB_RECV_BYTE`** | — | `0x0035E2` | `adb_mgr.s:345` | PIC not ready: send next command byte PIC asserted INT: read response byte from VIA SR |
| **`ADB_RECV_DO_READ`** | — | `0x0036B6` | `adb_mgr.s:413` | PIC has data: read and process |
| **`ADB_RECV_DONE`** | — | `0x0036D4` | `adb_mgr.s:422` | — |
| **`ADB_RECV_PATH`** | — | `0x00368C` | `adb_mgr.s:401` | ADB_RECV_PATH - receive path: PIC sending data to 68000 |
| **`ADB_RECV_VIA_SR`** | — | `0x003618` | `adb_mgr.s:361` | Read byte from PIC via VIA SR (Talk response) |
| **`ADB_RESOLVE_CONFLICTS`** | — | `0x003414` | `adb_mgr.s:136` | All addresses scanned: begin address conflict resolution Address conflict resolution: move colliding devices to free addresses |
| **`ADB_RESOLVE_DO_MOVE`** | — | `0x003434` | `adb_mgr.s:148` | — |
| **`ADB_RESOLVE_LOOP`** | — | `0x003418` | `adb_mgr.s:138` | — |
| **`ADB_SCAN_DEVICE`** | — | `0x003370` | `adb_mgr.s:73` | ADB_SCAN_DEVICE - start ADB bus scan (Talk Reg 0 to all 16 addresses) Initializes the ADB command block and begins scanning all 16 ADB addresses with Talk Register 0 commands. The PIC microcontroller ... |
| **`ADB_SCAN_DONE`** | — | `0x00344E` | `adb_mgr.s:158` | ADB_SCAN_DONE - scan complete: set up idle polling |
| **`ADB_SCAN_NEXT_ADDR`** | — | `0x0033FA` | `adb_mgr.s:125` | Advance to next ADB address (0 through 15) |
| **`ADB_SEND_BYTE`** | — | `0x0035BC` | `adb_mgr.s:333` | Receive path: PIC is sending data to 68000 via VIA SR Send path: 68000 sends command/data byte to PIC via VIA SR |
| **`ADB_SEND_VIA_SR`** | — | `0x003628` | `adb_mgr.s:367` | Write command/data byte to PIC via VIA SR |
| **`ADB_SEND_VIA_SR_GO`** | — | `0x003636` | `adb_mgr.s:371` | — |
| **`ADB_STATE0_IDLE`** | — | `0x003928` | `adb_mgr.s:655` | ADB_STATE0_IDLE/03930/03938/03940 - set VIA port B ST0/ST1 state bits These four entry points set the 2-bit state code (ST1:ST0) on VIA port B bits 4-5, which tells the PIC ADB controller what phase t... |
| **`ADB_STATE1_BUSY`** | — | `0x003930` | `adb_mgr.s:659` | — |
| **`ADB_STATE2_RECV`** | — | `0x003938` | `adb_mgr.s:663` | — |
| **`ADB_STATE3_NULL`** | — | `0x003940` | `adb_mgr.s:667` | — |
| **`ADB_TALK_REG3`** | — | `0x003500` | `adb_mgr.s:234` | **Regs:** `Entry: D0 = ADB device address (0-15), A0 = completion callback`<br>ADB_TALK_REG3 - issue ADB Talk Register 0 command Builds Talk Reg 0 command byte (addr << 4 \| 0x0F = Talk Reg 3), sets up completion callback, and initiates ADB transaction via PIC. Entry: D0 = ADB de... |
| **`ADB_UPDATE_DEVTBL`** | — | `0x0034B4` | `adb_mgr.s:200` | ADB_UPDATE_DEVTBL - update device table after successful ADB Move Marks new address as present in bitmap, finds device entry by source address, copies entry to new slot, updates current address. |
| **`ADBINIT_BODY`** | — | `0x003CAA` | `adb_mgr.s:1084` | — |
| **`ADBOP`** | — | `0x003880` | `adb_mgr.s:579` | ADBOP - _ADBOp trap handler (Inside Mac: Devices, Ch 5) Sends an explicit ADB command. Entry via trap or internal call. Entry (trap): A0 = param block: +0 = data ptr, +4 = completion, +8 = refCon D0 =... |
| **`ADBOP_RTS`** | — | `0x003922` | `adb_mgr.s:642` | — |
| **`ADBOP_TRAP`** | — | `0x0038FC` | `adb_mgr.s:629` | ADBOP_TRAP - call ADB completion routine after transaction Prepares the response buffer header (byte count at buf[-1]), then calls the completion routine with D0 = command, A0 = buffer, A2 = refCon. P... |
| **`ADBREINIT`** | — | `0x003C7E` | `adb_mgr.s:1062` | ADBREINIT - reinitialize ADB subsystem (_ADBReInit trap) Clears all ADB globals, rescans the bus, and loads ADBS device driver resources for each discovered device. |
| **`ADBREINIT_TAIL`** | — | `0x003CD2` | `adb_mgr.s:1100` | Try to load 'ADBS' resource for this device's handler ID |
| **`AddDrive`** | `0x002558` | `0x0032F6` | `device_mgr.s:878` | _AddDrive ($A04E) D0 = drvNum, D1 = refNum, A0 = DQE (drive queue element) -> D0 = noErr Stores drive number and driver refNum in the DQE, then enqueues it on the system drive queue (DrvQHdr) for File... |
| **`ADDDRIVE`** | `0x002558` | `0x0032F6` | `device_mgr.s:753` | **Regs:** `Entry: A0 = drive queue element, D0 = driver refNum`<br>ADDDRIVE - _AddDrive trap: add a drive to the drive queue Entry: A0 = drive queue element, D0 = driver refNum Stores refNum at element+6, enqueues in DrvQHdr. |
| **`AdjEof`** | `0x005536` | — | `file_mgr_io.s:914` | Adj Eof Called during boot. AdjEOF: adjust EOF in other open FCBs for this file copies LEOF/PEOF from current FCB to all other FCBs with same file number |
| **`ADJEOF_CONT`** | `0x005592` | `0x007044` | `file_mgr_io.s:967`<br>`file_mgr_io.s:821` | MFS SetEOF shrink: walk chain to truncation point ADJEOF_CONT Called during boot. |
| **`ADJEOF_CONT_2`** | `0x005594` | `0x007046` | `file_mgr_io.s:970`<br>`file_mgr_io.s:823` | MFS SetEOF shrink: walk chain to new PEOF and truncate |
| **`ADJEOF_CONT_3`** | `0x0055B0` | — | `file_mgr_io.s:982` | reached the new PEOF: truncate the chain |
| **`ADJEOF_CONT_4`** | `0x0055BE` | — | `file_mgr_io.s:993` | ADJEOF_CONT_4 ADJEOF_CONT_4/Alloc: allocate disk space for file (MFS/HFS dispatch) |
| **`ADJEOF_CONT_5`** | `0x0055CE` | — | `file_mgr_io.s:1005` | ADJEOF_CONT_5 |
| **`ADJEOF_CONT_6`** | `0x0055D4` | — | `file_mgr_io.s:1009` | — |
| **`ADJEOF_FOUND`** | `0x005558` | `0x00700A` | `file_mgr_io.s:928`<br>`file_mgr_io.s:791` | extract file info from current FCB scan all FCBs for matching file number |
| **`ADJEOF_FOUND_2`** | `0x005578` | `0x00702A` | `file_mgr_io.s:943`<br>`file_mgr_io.s:805` | — |
| **`AdjEOF_Impl`** | — | `0x006FB2` | `file_mgr_io.s:751` | — |
| **`ADJEOF_NO`** | `0x00557E` | `0x007030` | `file_mgr_io.s:952`<br>`file_mgr_io.s:813` | ADJEOF_NO Called during boot. |
| **`ADJEOF_SKIP`** | `0x005572` | `0x007024` | `file_mgr_io.s:940`<br>`file_mgr_io.s:802` | same fork: update EOF/PEOF from current FCB |
| **`AdjustFree`** | `0x010A7C` | `0x00B03A` | `memory_mgr.s:2482` | AdjustFree - zcbFree += D0 (A6 = zone); system error 33 if it goes negative Called during boot (56,518 times in 30s trace). |
| **`ADJUSTFREE`** | `0x010A7C` | `0x00B03A` | `memory_mgr.s:1834` | Called by: EH_CONT_2, ALLOCBK_CONT_5, ZONEADJUSTEND, SETSIZE_CONT_3, SETSIZE_CONT_4 (and 3 more) |
| **`ADJUSTFREE_ERR`** | `0x010A84` | `0x00B042` | `memory_mgr.s:2491`<br>`memory_mgr.s:1842` | ADJUSTFREE_ERR |
| **`ALLOC_COMMIT`** | `0x006EAE` | `0x00896E` | `file_mgr_btree.s:1048`<br>`file_mgr_btree.s:903` | calculate node number for the selected node check for end of map ANAlloc: allocate the node |
| **`ALLOC_EXIT`** | `0x006EC4` | `0x008984` | `file_mgr_btree.s:1056`<br>`file_mgr_btree.s:911` | — |
| **`ALLOC_FOUNDBIT`** | `0x006E82` | `0x008942` | `file_mgr_btree.s:1027`<br>`file_mgr_btree.s:883` | — |
| **`ALLOC_FOUNDLW`** | `0x006E76` | `0x008936` | `file_mgr_btree.s:1021`<br>`file_mgr_btree.s:877` | ANFound: found a long word with free blocks, locate 1st one |
| **`ALLOC_FREE_REMAINING`** | — | `0x007062` | `file_mgr_io.s:834` | — |
| **`ALLOC_GETMAP`** | `0x006E48` | `0x008908` | `file_mgr_btree.s:998`<br>`file_mgr_btree.s:854` | ANGetMap: get next map record |
| **`ALLOC_SCANBIT`** | `0x006E7A` | `0x00893A` | `file_mgr_btree.s:1023`<br>`file_mgr_btree.s:879` | — |
| **`ALLOC_SCANLW`** | `0x006E60` | `0x008920` | `file_mgr_btree.s:1011`<br>`file_mgr_btree.s:867` | — |
| **`ALLOC_SEARCH`** | `0x006E58` | `0x008918` | `file_mgr_btree.s:1006`<br>`file_mgr_btree.s:862` | ANSearch: search map record for a free node (zero bit) |
| **`Allocate`** | `0x00548E` | — | `file_mgr_io.s:822` | _Allocate ($A010) _Allocate ($A010): pre-allocate disk space for a file |
| **`ALLOCATE_EMPTY`** | `0x0054AA` | `0x006F64` | `file_mgr_io.s:833`<br>`file_mgr_io.s:718` | — |
| **`ALLOCATE_ERR`** | `0x0054BC` | — | `file_mgr_io.s:840` | — |
| **`AllocBK`** | `0x0106FE` | `0x00ACB4` | `memory_mgr.s:1855` | AllocBK - allocate a block of D0 logical bytes D0 = requested size -> A0 = block data ptr (or nil), Z set if failed A1 = master pointer (relocatable block; set to point to the block) or nil (nonreloca... |
| **`ALLOCBK`** | `0x0106FE` | `0x00ACB4` | `memory_mgr.s:1319` | AllocBK: carve block from free space at A0 D0 = actual size needed, A0 = free block, A1 = master pointer or nil Called by: NEWPTR, NEWHANDLE_ALLOC, REALLOCHANDLE_OK, HMAKEMOREMASTERS_CONT, MAKEPTRSPC_... |
| **`ALLOCBK_CONT`** | `0x01072E` | `0x00ACE4` | `memory_mgr.s:1890`<br>`memory_mgr.s:1345` | build the block header and split free space |
| **`ALLOCBK_CONT_2`** | `0x010748` | `0x00ACFE` | `memory_mgr.s:1910`<br>`memory_mgr.s:1363` | ALLOCBK_CONT_2 Called during boot (34,443 times in 30s trace). |
| **`ALLOCBK_CONT_3`** | `0x010762` | `0x00AD18` | `memory_mgr.s:1927`<br>`memory_mgr.s:1379` | ALLOCBK_CONT_3 Called during boot (15,878 times in 30s trace). |
| **`ALLOCBK_CONT_4`** | `0x010784` | `0x00AD3A` | `memory_mgr.s:1948`<br>`memory_mgr.s:1399` | — |
| **`ALLOCBK_CONT_5`** | `0x01078C` | `0x00AD42` | `memory_mgr.s:1959`<br>`memory_mgr.s:1404` | — |
| **`ALLOCBK_CONT_6`** | `0x0107A2` | `0x00AD58` | `memory_mgr.s:1975`<br>`memory_mgr.s:1419` | ALLOCBK_CONT_6 Called during boot (1,397 times in 30s trace). |
| **`ALLOCBK_EMPTY`** | `0x010728` | `0x00ACDE` | `memory_mgr.s:1885`<br>`memory_mgr.s:1340` | relocatable block: store relative handle in block header non-relocatable block: no handle |
| **`ALLOCBK_ERR`** | `0x010740` | `0x00ACF6` | `memory_mgr.s:1900`<br>`memory_mgr.s:1354` | update master pointer to point to block data |
| **`ALLOCBK_FOUND`** | `0x010718` | `0x00ACCE` | `memory_mgr.s:1874`<br>`memory_mgr.s:1330` | no block found: compact heap and try again ALLOCBK_FOUND - AllocBK found a free block: carve the block from the free space at A0 D0 = actual size needed, A0 = free block, A1 = master pointer or nil |
| **`ALLOCBK_NO`** | `0x010782` | `0x00AD38` | `memory_mgr.s:1946`<br>`memory_mgr.s:1397` | ALLOCBK_NO Called during boot (15,867 times in 30s trace). |
| **`ALLOCBK_NO_2`** | `0x01078A` | `0x00AD40` | `memory_mgr.s:1957`<br>`memory_mgr.s:1402` | ALLOCBK_NO_2 Called during boot. |
| **`ALLOCEXTEND_HFS_BEGIN`** | — | `0x00707A` | `file_mgr_io.s:843` | — |
| **`AllocFakeRgns`** | `0x0011AC` | `0x0013F4` | `sys_error.s:79` | AllocFakeRgns - set up fake visRgn/clipRgn for DS GrafPort The DS error handler creates a minimal GrafPort on the stack. A6 points to the port; offsets +0x18/+0x1C are visRgn/clipRgn handles. This all... |
| **`ALLOCFAKERGNS`** | `0x0011AC` | `0x0013F4` | `sys_error.s:75` | Handler returned 0: resume from error ALLOCFAKERGNS - called from 2 places ALLOCFAKERGNS - set up fake visRgn/clipRgn for DS alert GrafPort Points the GrafPort's visRgn and clipRgn handles to stack-al... |
| **`ALLOCFILE_DEFAULT`** | — | `0x006F44` | `file_mgr_io.s:705` | — |
| **`ALLOCFILE_DONE`** | — | `0x006F74` | `file_mgr_io.s:725` | — |
| **`AllocFile_OrAllocContig`** | — | `0x006F32` | `file_mgr_io.s:698` | — |
| **`AllocNode`** | `0x006E3E` | `0x0088F8` | `file_mgr_btree.s:992` | Alloc Node |
| **`ALLOCNODE`** | `0x006E3E` | `0x0088F8` | `file_mgr_btree.s:845` | — |
| **`AllocOrExtendFile`** | — | `0x007070` | `file_mgr_io.s:839` | — |
| **`APPHEAP_TEST`** | — | `0x009960` | `segment_loader.s:101` | — |
| **`APPHEAP_TEST_RTS`** | — | `0x009970` | `segment_loader.s:108` | — |
| **`ASYNCPATCH`** | — | `0x009BD8` | `os_utilities.s:22` | Operating System Utilities Apple source: SysUtil.a (MacSEROM.lst module SYSUTIL). In ROM order: ASYNCPATCH                 - (an RTS: patch point) ReadParam, WriteParam      - parameter RAM: low-memor... |
| **`ATRAP68010`** | — | `0x002CCE` | `trap_dispatch.s:30` | 68020+ cache flush: MOVEC CACR,D1 / BSET #3 / MOVEC D1,CACR Raw bytes because m68000 assembler cannot encode MOVEC. ATRAP68010 - A-line trap entry for 68010+ (different stack frame) |
| **`ATRAP68020`** | — | `0x002CB6` | `trap_dispatch.s:20` | A-line trap dispatcher -- ATRAP68020/68010, EMT1010, _SetTrapAddress, _GetTrapAddress Apple source: Dispatch.a (MacSEROM.lst module DSPATCH). Dispatches A-line instructions ($Axxx) to the OS or Toolbo... |
| **`BAD_UNIT_ERR`** | `0x0021EE` | `0x002F7C` | `device_mgr.s:371`<br>`device_mgr.s:326` | BAD_UNIT_ERR - Return badUnitErr for re-opened device |
| **`BasicIO`** | `0x007C1A` | — | `file_mgr_cache.s:839` | Basic IO Called during boot. |
| **`BASICIO_ACHK`** | `0x007C48` | `0x00979C` | `file_mgr_cache.s:876`<br>`file_mgr_cache.s:722` | — |
| **`BASICIO_ASYNC`** | `0x007C30` | `0x009784` | `file_mgr_cache.s:861`<br>`file_mgr_cache.s:708` | BASICIO_ASYNC - async I/O path |
| **`BASICIO_AWRITE`** | `0x007C46` | `0x00979A` | `file_mgr_cache.s:874`<br>`file_mgr_cache.s:720` | BASICIO_AWRITE - async write |
| **`BASICIO_COMPRET`** | `0x007C86` | `0x0097DC` | `file_mgr_cache.s:913`<br>`file_mgr_cache.s:754` | BASICIO_COMPRET - completion return: restore interrupted context |
| **`BASICIO_DONE`** | — | `0x0097D8` | `file_mgr_cache.s:747` | — |
| **`BASICIO_ERRCHK`** | `0x007C84` | — | `file_mgr_cache.s:906` | — |
| **`BASICIO_IOCOMP`** | `0x007C5A` | `0x0097AE` | `file_mgr_cache.s:890`<br>`file_mgr_cache.s:731` | BASICIO_IOCOMP - async I/O completion routine |
| **`BASICIO_QUEUED`** | — | `0x0097A4` | `file_mgr_cache.s:726` | — |
| **`BASICIO_RECOVER`** | `0x007C6A` | `0x0097BE` | `file_mgr_cache.s:896`<br>`file_mgr_cache.s:737` | — |
| **`BASICIO_RESUME`** | `0x007C62` | `0x0097B6` | `file_mgr_cache.s:893`<br>`file_mgr_cache.s:734` | — |
| **`BASICIO_RTS`** | `0x007C58` | `0x0097AC` | `file_mgr_cache.s:883`<br>`file_mgr_cache.s:729` | — |
| **`BASICIO_SETFLAG`** | `0x007C50` | — | `file_mgr_cache.s:880` | — |
| **`BASICIO_SETUP`** | `0x007BE2` | `0x009736` | `file_mgr_cache.s:817`<br>`file_mgr_cache.s:673` | — |
| **`BASICIO_VOLBLK`** | — | `0x009730` | `file_mgr_cache.s:670` | — |
| **`BASICIO_WRITE`** | `0x007C2C` | `0x009780` | `file_mgr_cache.s:853`<br>`file_mgr_cache.s:701` | BASICIO_WRITE - synchronous write Called during boot. |
| **`BCPY_BT1`** | `0x010F28` | `0x00B4F4` | `memory_mgr.s:3687`<br>`memory_mgr.s:2659` | — |
| **`BCPY_BT2`** | `0x010F26` | `0x00B4F2` | `memory_mgr.s:3685`<br>`memory_mgr.s:2657` | — |
| **`BCPY_BT3`** | `0x010F24` | `0x00B4F0` | `memory_mgr.s:3683`<br>`memory_mgr.s:2655` | — |
| **`BCPY_BT4`** | `0x010F22` | `0x00B4EE` | `memory_mgr.s:3681`<br>`memory_mgr.s:2653` | — |
| **`BCPY_BT5`** | `0x010F20` | `0x00B4EC` | `memory_mgr.s:3679`<br>`memory_mgr.s:2651` | — |
| **`BCPY_BT6`** | `0x010F1E` | `0x00B4EA` | `memory_mgr.s:3677`<br>`memory_mgr.s:2649` | — |
| **`BCPY_BT7`** | `0x010F1C` | `0x00B4E8` | `memory_mgr.s:3675`<br>`memory_mgr.s:2647` | Variant C: copy N longwords + 1 byte, predecrement |
| **`BCPY_DISPATCH_0`** | — | `0x00B47E` | `memory_mgr.s:2536` | — |
| **`BCPY_DISPATCH_0_RTS`** | — | `0x00B47A` | `memory_mgr.s:2533` | — |
| **`BCPY_DISPATCH_1`** | — | `0x00B484` | `memory_mgr.s:2542` | — |
| **`BCPY_DISPATCH_10`** | — | `0x00B492` | `memory_mgr.s:2556` | — |
| **`BCPY_DISPATCH_11`** | — | `0x00B490` | `memory_mgr.s:2554` | — |
| **`BCPY_DISPATCH_12`** | — | `0x00B496` | `memory_mgr.s:2560` | — |
| **`BCPY_DISPATCH_13`** | — | `0x00B49C` | `memory_mgr.s:2566` | — |
| **`BCPY_DISPATCH_14`** | — | `0x00B49A` | `memory_mgr.s:2564` | — |
| **`BCPY_DISPATCH_15`** | — | `0x00B498` | `memory_mgr.s:2562` | — |
| **`BCPY_DISPATCH_16`** | — | `0x00B49E` | `memory_mgr.s:2568` | — |
| **`BCPY_DISPATCH_17`** | — | `0x00B4A4` | `memory_mgr.s:2574` | — |
| **`BCPY_DISPATCH_18`** | — | `0x00B4A2` | `memory_mgr.s:2572` | — |
| **`BCPY_DISPATCH_19`** | — | `0x00B4A0` | `memory_mgr.s:2570` | — |
| **`BCPY_DISPATCH_2`** | — | `0x00B482` | `memory_mgr.s:2540` | — |
| **`BCPY_DISPATCH_20`** | — | `0x00B4A6` | `memory_mgr.s:2576` | — |
| **`BCPY_DISPATCH_21`** | — | `0x00B4AC` | `memory_mgr.s:2582` | — |
| **`BCPY_DISPATCH_22`** | — | `0x00B4AA` | `memory_mgr.s:2580` | — |
| **`BCPY_DISPATCH_23`** | — | `0x00B4A8` | `memory_mgr.s:2578` | — |
| **`BCPY_DISPATCH_24`** | — | `0x00B4AE` | `memory_mgr.s:2584` | — |
| **`BCPY_DISPATCH_3`** | — | `0x00B480` | `memory_mgr.s:2538` | — |
| **`BCPY_DISPATCH_4`** | — | `0x00B486` | `memory_mgr.s:2544` | — |
| **`BCPY_DISPATCH_5`** | — | `0x00B48C` | `memory_mgr.s:2550` | — |
| **`BCPY_DISPATCH_6`** | — | `0x00B48A` | `memory_mgr.s:2548` | — |
| **`BCPY_DISPATCH_7`** | — | `0x00B488` | `memory_mgr.s:2546` | — |
| **`BCPY_DISPATCH_8`** | — | `0x00B48E` | `memory_mgr.s:2552` | — |
| **`BCPY_DISPATCH_9`** | — | `0x00B494` | `memory_mgr.s:2558` | — |
| **`BCPY_ENT_BT13`** | `0x010EDC` | — | `memory_mgr.s:3585` | **Regs:** `Entry: copy 3 longs + 1 byte (29 bytes total)`<br>Entry: copy 3 longs + 1 byte (29 bytes total) |
| **`BCPY_ENT_BT29`** | `0x010ED4` | — | `memory_mgr.s:3569` | **Regs:** `Entry: copy 4 longs + 1 byte (29 bytes total)`<br>Unrolled block-copy routines (continuation of Memory Manager) Three variants for different remainder classes after longword alignment: BCPY_WD7: N longs + 1 word (even-byte remainder = 2) BCPY_WDB7: N... |
| **`BCPY_ENT_BT5`** | `0x010EEC` | `0x00B4B8` | `memory_mgr.s:3617`<br>`memory_mgr.s:2599` | **Regs:** `Entry: copy 1 long + 1 byte (5 bytes total)`<br>Entry: copy 1 long + 1 byte (5 bytes total) |
| **`BCPY_ENT_BT9`** | `0x010EE4` | `0x00B4B0` | `memory_mgr.s:3601`<br>`memory_mgr.s:2587` | **Regs:** `Entry: copy 2 longs + 1 byte (9 bytes total)`<br>Entry: copy 2 longs + 1 byte (9 bytes total) |
| **`BCPY_ENT_WD10`** | `0x010EE6` | `0x00B4B2` | `memory_mgr.s:3605`<br>`memory_mgr.s:2590` | **Regs:** `Entry: copy 2 longs + 1 word (10 bytes total)`<br>Entry: copy 2 longs + 1 word (10 bytes total) |
| **`BCPY_ENT_WD14`** | `0x010EDE` | — | `memory_mgr.s:3589` | **Regs:** `Entry: copy 3 longs + 1 word (30 bytes total)`<br>Entry: copy 3 longs + 1 word (30 bytes total) |
| **`BCPY_ENT_WD18`** | `0x010ED6` | — | `memory_mgr.s:3573` | **Regs:** `Entry: copy 4 longs + 1 word (30 bytes total)`<br>Entry: copy 4 longs + 1 word (30 bytes total) |
| **`BCPY_ENT_WD22`** | `0x010EEA` | `0x00B4B6` | `memory_mgr.s:3613`<br>`memory_mgr.s:2596` | **Regs:** `Entry: copy 5 longs + 1 word (22 bytes total)`<br>Entry: copy 5 longs + 1 word (22 bytes total) |
| **`BCPY_ENT_WD26`** | `0x010EE2` | — | `memory_mgr.s:3597` | **Regs:** `Entry: copy 6 longs + 1 word (26 bytes total)`<br>Entry: copy 6 longs + 1 word (26 bytes total) |
| **`BCPY_ENT_WD30`** | `0x010EDA` | — | `memory_mgr.s:3581` | **Regs:** `Entry: copy 7 longs + 1 word (30 bytes total)`<br>Entry: copy 7 longs + 1 word (30 bytes total) |
| **`BCPY_ENT_WD6`** | `0x010EEE` | `0x00B4BA` | `memory_mgr.s:3621`<br>`memory_mgr.s:2602` | **Regs:** `Entry: copy 1 long + 1 word (6 bytes total)`<br>Entry: copy 1 long + 1 word (6 bytes total) |
| **`BCPY_ENT_WDB11`** | `0x010EE8` | `0x00B4B4` | `memory_mgr.s:3609`<br>`memory_mgr.s:2593` | **Regs:** `Entry: copy 2 longs + 1 word + 1 byte (11 bytes total)`<br>Entry: copy 2 longs + 1 word + 1 byte (11 bytes total) |
| **`BCPY_ENT_WDB15`** | `0x010EE0` | — | `memory_mgr.s:3593` | **Regs:** `Entry: copy 3 longs + 1 word + 1 byte (31 bytes total)`<br>Entry: copy 3 longs + 1 word + 1 byte (31 bytes total) |
| **`BCPY_ENT_WDB19`** | `0x010ED8` | — | `memory_mgr.s:3577` | **Regs:** `Entry: copy 4 longs + 1 word + 1 byte (31 bytes total)`<br>Entry: copy 4 longs + 1 word + 1 byte (31 bytes total) |
| **`BCPY_ENT_WDB7`** | `0x010EF0` | `0x00B4BC` | `memory_mgr.s:3625`<br>`memory_mgr.s:2605` | **Regs:** `Entry: copy 1 long + 1 word + 1 byte (7 bytes total)`<br>Entry: copy 1 long + 1 word + 1 byte (7 bytes total) |
| **`BCPY_WD1`** | `0x010EFE` | `0x00B4CA` | `memory_mgr.s:3643`<br>`memory_mgr.s:2619` | — |
| **`BCPY_WD2`** | `0x010EFC` | `0x00B4C8` | `memory_mgr.s:3641`<br>`memory_mgr.s:2617` | — |
| **`BCPY_WD3`** | `0x010EFA` | `0x00B4C6` | `memory_mgr.s:3639`<br>`memory_mgr.s:2615` | — |
| **`BCPY_WD4`** | `0x010EF8` | `0x00B4C4` | `memory_mgr.s:3637`<br>`memory_mgr.s:2613` | — |
| **`BCPY_WD5`** | `0x010EF6` | `0x00B4C2` | `memory_mgr.s:3635`<br>`memory_mgr.s:2611` | — |
| **`BCPY_WD6`** | `0x010EF4` | `0x00B4C0` | `memory_mgr.s:3633`<br>`memory_mgr.s:2609` | — |
| **`BCPY_WD7`** | `0x010EF2` | — | `memory_mgr.s:3631` | Variant A: copy N longwords + 1 word, predecrement Entered at BCPY_WD7..BCPY_WD_TAIL depending on count needed. |
| **`BCPY_WD8`** | — | `0x00B4BE` | `memory_mgr.s:2607` | — |
| **`BCPY_WD_TAIL`** | `0x010F00` | `0x00B4CC` | `memory_mgr.s:3645`<br>`memory_mgr.s:2621` | — |
| **`BCPY_WDB1`** | `0x010F12` | `0x00B4DE` | `memory_mgr.s:3664`<br>`memory_mgr.s:2637` | — |
| **`BCPY_WDB2`** | `0x010F10` | `0x00B4DC` | `memory_mgr.s:3662`<br>`memory_mgr.s:2635` | — |
| **`BCPY_WDB3`** | `0x010F0E` | `0x00B4DA` | `memory_mgr.s:3660`<br>`memory_mgr.s:2633` | — |
| **`BCPY_WDB4`** | `0x010F0C` | `0x00B4D8` | `memory_mgr.s:3658`<br>`memory_mgr.s:2631` | — |
| **`BCPY_WDB5`** | `0x010F0A` | `0x00B4D6` | `memory_mgr.s:3656`<br>`memory_mgr.s:2629` | — |
| **`BCPY_WDB6`** | `0x010F08` | `0x00B4D4` | `memory_mgr.s:3654`<br>`memory_mgr.s:2627` | — |
| **`BCPY_WDB7`** | `0x010F06` | — | `memory_mgr.s:3652` | Variant B: copy N longwords + 1 word + 1 byte, predecrement |
| **`BCPY_WDB8`** | — | `0x00B4D2` | `memory_mgr.s:2625` | — |
| **`BCPY_WDB_TAIL`** | `0x010F16` | `0x00B4E2` | `memory_mgr.s:3668`<br>`memory_mgr.s:2641` | — |
| **`BCPY_WDB_WORD`** | `0x010F14` | `0x00B4E0` | `memory_mgr.s:3666`<br>`memory_mgr.s:2639` | — |
| **`BCPYB_ALIGNED`** | — | `0x00B412` | `memory_mgr.s:2483` | — |
| **`BCPYF_RTS`** | — | `0x00B388` | `memory_mgr.s:2316` | — |
| **`BCPYF_T0_0`** | — | `0x00B38C` | `memory_mgr.s:2319` | — |
| **`BCPYF_T0_1`** | — | `0x00B392` | `memory_mgr.s:2325` | — |
| **`BCPYF_T0_2`** | — | `0x00B390` | `memory_mgr.s:2323` | — |
| **`BCPYF_T0_3`** | — | `0x00B38E` | `memory_mgr.s:2321` | — |
| **`BCPYF_T2_0`** | — | `0x00B3BC` | `memory_mgr.s:2367` | — |
| **`BCPYF_T3_0`** | — | `0x00B3B4` | `memory_mgr.s:2359` | — |
| **`BCPYF_T3_1`** | — | `0x00B3BA` | `memory_mgr.s:2365` | — |
| **`BCPYF_T3_2`** | — | `0x00B3B8` | `memory_mgr.s:2363` | — |
| **`BCPYF_T3_3`** | — | `0x00B3B6` | `memory_mgr.s:2361` | — |
| **`BCPYF_T4_0`** | — | `0x00B3AC` | `memory_mgr.s:2351` | — |
| **`BCPYF_T4_1`** | — | `0x00B3B2` | `memory_mgr.s:2357` | — |
| **`BCPYF_T4_2`** | — | `0x00B3B0` | `memory_mgr.s:2355` | — |
| **`BCPYF_T4_3`** | — | `0x00B3AE` | `memory_mgr.s:2353` | — |
| **`BCPYF_T5_0`** | — | `0x00B3A4` | `memory_mgr.s:2343` | — |
| **`BCPYF_T5_1`** | — | `0x00B3AA` | `memory_mgr.s:2349` | — |
| **`BCPYF_T5_2`** | — | `0x00B3A8` | `memory_mgr.s:2347` | — |
| **`BCPYF_T5_3`** | — | `0x00B3A6` | `memory_mgr.s:2345` | — |
| **`BCPYF_T6_0`** | — | `0x00B39C` | `memory_mgr.s:2335` | — |
| **`BCPYF_T6_1`** | — | `0x00B3A2` | `memory_mgr.s:2341` | — |
| **`BCPYF_T6_2`** | — | `0x00B3A0` | `memory_mgr.s:2339` | — |
| **`BCPYF_T6_3`** | — | `0x00B39E` | `memory_mgr.s:2337` | — |
| **`BCPYF_T7_0`** | — | `0x00B394` | `memory_mgr.s:2327` | — |
| **`BCPYF_T7_1`** | — | `0x00B39A` | `memory_mgr.s:2333` | — |
| **`BCPYF_T7_2`** | — | `0x00B398` | `memory_mgr.s:2331` | — |
| **`BCPYF_T7_3`** | — | `0x00B396` | `memory_mgr.s:2329` | — |
| **`BCPYF_WD8`** | — | `0x00B3CC` | `memory_mgr.s:2414` | — |
| **`BCPYF_WDB8`** | — | `0x00B3E0` | `memory_mgr.s:2432` | — |
| **`BDFREE`** | — | `0x008282` | `file_mgr_btree.s:119` | BDFree: free the empty node |
| **`BDNXTLEV`** | — | `0x0082AA` | `file_mgr_btree.s:133` | BDNxtLev: move to next level up |
| **`BFindS`** | `0x0106A2` | — | `memory_mgr.s:1774` | **Regs:** `Entry: D0.L = physical size needed, A6 = zone Exit:  A0 = free block (header) or nil, Z set accordingly; allocPtr = A0`<br>BFindS - find a free block of at least D0 bytes Entry: D0.L = physical size needed, A6 = zone Exit:  A0 = free block (header) or nil, Z set accordingly; allocPtr = A0 Searches from the allocation rove... |
| **`BFINDS_EMPTY`** | `0x0106C2` | `0x00AC78` | `memory_mgr.s:1786`<br>`memory_mgr.s:1257` | — |
| **`BFINDS_ERR`** | `0x0106EC` | `0x00ACA2` | `memory_mgr.s:1829`<br>`memory_mgr.s:1297` | BFINDS_ERR Called during boot. |
| **`BFINDS_ERR_2`** | `0x0106F4` | `0x00ACAA` | `memory_mgr.s:1840`<br>`memory_mgr.s:1307` | BFINDS_ERR_2 Called during boot. |
| **`BFINDS_EXIT`** | `0x0106F6` | `0x00ACAC` | `memory_mgr.s:1842`<br>`memory_mgr.s:1309` | — |
| **`BFINDS_NO`** | `0x0106CC` | `0x00AC82` | `memory_mgr.s:1792`<br>`memory_mgr.s:1263` | — |
| **`BFINDS_NO_2`** | `0x0106E4` | `0x00AC9A` | `memory_mgr.s:1818`<br>`memory_mgr.s:1287` | BFINDS_NO_2 Called during boot (15,988 times in 30s trace). |
| **`BFINDS_OK`** | `0x0106D2` | `0x00AC88` | `memory_mgr.s:1802`<br>`memory_mgr.s:1272` | BFINDS_OK Called during boot (30,345 times in 30s trace). |
| **`BFINDS_RETRY`** | `0x0106B8` | `0x00AC6E` | `memory_mgr.s:1781`<br>`memory_mgr.s:1252` | — |
| **`BKALLOCEXIT`** | `0x005922` | `0x0073CC` | `file_mgr_alloc.s:169`<br>`file_mgr_alloc.s:150` | BkAllocExit |
| **`BKALLOCOK`** | `0x005900` | `0x0073AA` | `file_mgr_alloc.s:153`<br>`file_mgr_alloc.s:134` | BkAllocOK: allocation is done |
| **`BKCompacts`** | `0x010662` | `0x00AC18` | `memory_mgr.s:1732` | **Regs:** `Entry: D0.L = physical size needed, D2 = tryGrow (0 = only compact and Exit:  A0 = free block or nil (Z set accordingly), D1 = largest free block`<br>BKCompacts - make a free block of D0 bytes by compacting, growing and purging the zone Entry: D0.L = physical size needed, D2 = tryGrow (0 = only compact and purge, as for MaxMem), A6 = zone Exit:  A0... |
| **`BKCOMPACTS`** | `0x010662` | `0x00AC18` | `memory_mgr.s:1213` | — |
| **`BKCOMPACTS_DONE`** | `0x01069A` | `0x00AC50` | `memory_mgr.s:1759`<br>`memory_mgr.s:1241` | Called by: BKCOMPACTS, BKCOMPACTS_SKIP, BKCOMPACTS_RETRY |
| **`BKCOMPACTS_RETRY`** | `0x01068C` | `0x00AC42` | `memory_mgr.s:1751`<br>`memory_mgr.s:1232` | — |
| **`BKCOMPACTS_SKIP`** | `0x010680` | `0x00AC36` | `memory_mgr.s:1745`<br>`memory_mgr.s:1226` | — |
| **`BLDKEY_DONE`** | `0x006600` | `0x0080C8` | `file_mgr_catalog.s:688`<br>`file_mgr_catalog.s:620` | — |
| **`BlkAlloc`** | `0x0057DC` | `0x007282` | `file_mgr_alloc.s:25` | Blk Alloc |
| **`BLKALLOC`** | `0x0057DC` | `0x007282` | `file_mgr_alloc.s:13` | File Manager -- allocation: volume bitmap and file extents Apple sources: VSM.a, the Volume Space Manager (MacSEROM.lst module VSM: BlkAlloc, BlkDealloc, BlkChk, UpdateFree, ReadBM -- allocation block... |
| **`BLKALLOC_CONT`** | `0x005812` | `0x0072BE` | `file_mgr_alloc.s:47`<br>`file_mgr_alloc.s:36` | look for free fragment at or beyond starting block |
| **`BLKALLOC_CONT_2`** | `0x00583A` | `0x0072E6` | `file_mgr_alloc.s:69`<br>`file_mgr_alloc.s:52` | BLKALLOC_CONT_2 bkAlFree: found a free fragment, check if big enough |
| **`BLKALLOC_CONT_3`** | `0x00585C` | `0x007306` | `file_mgr_alloc.s:81`<br>`file_mgr_alloc.s:64` | — |
| **`BLKALLOC_CONT_4`** | `0x0058A8` | `0x007352` | `file_mgr_alloc.s:116`<br>`file_mgr_alloc.s:98` | contiguous fragment big enough |
| **`BLKALLOC_EXIT`** | `0x00589E` | `0x007348` | `file_mgr_alloc.s:111`<br>`file_mgr_alloc.s:94` | — |
| **`BLKALLOC_EXIT_2`** | `0x00592C` | `0x0073D6` | `file_mgr_alloc.s:175`<br>`file_mgr_alloc.s:156` | bkAllocFull |
| **`BLKALLOC_LOOP`** | — | `0x0072B0` | `file_mgr_alloc.s:31` | — |
| **`BLKALLOC_NEXT`** | `0x00588A` | `0x007334` | `file_mgr_alloc.s:103`<br>`file_mgr_alloc.s:86` | — |
| **`BLKALLOC_NO`** | `0x005804` | — | `file_mgr_alloc.s:41` | blkLoop |
| **`BLKALLOC_NO_2`** | `0x00582A` | `0x0072D6` | `file_mgr_alloc.s:56`<br>`file_mgr_alloc.s:45` | — |
| **`BLKALLOC_NO_3`** | `0x005876` | `0x007320` | `file_mgr_alloc.s:94`<br>`file_mgr_alloc.s:77` | fragment too small |
| **`BLKALLOC_NO_4`** | `0x0058BA` | `0x007364` | `file_mgr_alloc.s:124`<br>`file_mgr_alloc.s:105` | bkAllocDoIt: round request to clump size and start allocating |
| **`BLKALLOC_NO_5`** | `0x005914` | `0x0073BE` | `file_mgr_alloc.s:162`<br>`file_mgr_alloc.s:143` | — |
| **`BLKALLOC_OK`** | `0x0057FA` | `0x0072A6` | `file_mgr_alloc.s:35`<br>`file_mgr_alloc.s:26` | — |
| **`BLKALLOC_OK_2`** | `0x0058D0` | `0x00737A` | `file_mgr_alloc.s:133`<br>`file_mgr_alloc.s:114` | mark blocks allocated from the starting block |
| **`BLKALLOC_OK_3`** | `0x005910` | `0x0073BA` | `file_mgr_alloc.s:160`<br>`file_mgr_alloc.s:141` | — |
| **`BlkChk`** | `0x005978` | `0x007422` | `file_mgr_alloc.s:226` | Blk Chk BlkChk: check and fix bitmap for extent record blocks |
| **`BLKCHK`** | `0x005978` | `0x007422` | `file_mgr_alloc.s:190` | — |
| **`BLKCHK_CONT`** | `0x0059B0` | `0x00745A` | `file_mgr_alloc.s:252`<br>`file_mgr_alloc.s:216` | — |
| **`BLKCHK_DONE`** | `0x0059C6` | `0x007470` | `file_mgr_alloc.s:262`<br>`file_mgr_alloc.s:226` | — |
| **`BLKCHK_ERR`** | `0x0059C8` | `0x007472` | `file_mgr_alloc.s:264`<br>`file_mgr_alloc.s:228` | — |
| **`BLKCHK_LOOP`** | `0x005994` | `0x00743E` | `file_mgr_alloc.s:239`<br>`file_mgr_alloc.s:203` | — |
| **`BLKCHK_NEXT`** | `0x005984` | `0x00742E` | `file_mgr_alloc.s:232`<br>`file_mgr_alloc.s:196` | — |
| **`BLKCHK_NO`** | `0x0059BA` | `0x007464` | `file_mgr_alloc.s:257`<br>`file_mgr_alloc.s:221` | — |
| **`BLKCHK_OK`** | `0x0059A0` | `0x00744A` | `file_mgr_alloc.s:244`<br>`file_mgr_alloc.s:208` | — |
| **`BlkDealloc`** | `0x005938` | `0x0073DC` | `file_mgr_alloc.s:193` | Blk Dealloc |
| **`BLKDEALLOC`** | `0x005938` | `0x0073DC` | `file_mgr_alloc.s:160` | — |
| **`BLKDEALLOC_CONT`** | `0x005948` | `0x0073F2` | `file_mgr_alloc.s:200`<br>`file_mgr_alloc.s:170` | — |
| **`BLKDEALLOC_DONE`** | `0x00596E` | `0x007418` | `file_mgr_alloc.s:215`<br>`file_mgr_alloc.s:185` | — |
| **`BLKDEALLOC_OK`** | `0x005966` | `0x007410` | `file_mgr_alloc.s:211`<br>`file_mgr_alloc.s:181` | — |
| **`BLOCK2`** | — | `0x00B28C` | `memory_mgr.s:2156` | — |
| **`BlockMove`** | `0x010CC0` | `0x00B28C` | `memory_mgr.s:2869` | _BlockMove ($A02E) A0 = src, A1 = dst, D0.L = count -> (copied) Called during boot (5,329 times in 30s trace). |
| **`BLOCKMOVE`** | `0x010CC0` | `0x00B28C` | `memory_mgr.s:2157` | — |
| **`BLOCKMOVE_CONT`** | `0x010CD8` | `0x00B2A4` | `memory_mgr.s:2880`<br>`memory_mgr.s:2168` | — |
| **`BLOCKMOVE_CONT_10`** | `0x010DB8` | `0x00B384` | `memory_mgr.s:3031`<br>`memory_mgr.s:2312` | — |
| **`BLOCKMOVE_CONT_11`** | `0x010DBA` | `0x00B386` | `memory_mgr.s:3033`<br>`memory_mgr.s:2314` | — |
| **`BLOCKMOVE_CONT_12`** | `0x010DBC` | — | `memory_mgr.s:3035` | — |
| **`BLOCKMOVE_CONT_13`** | `0x010DC0` | — | `memory_mgr.s:3044` | BLOCKMOVE_CONT_13 Called during boot. |
| **`BLOCKMOVE_CONT_14`** | `0x010DC2` | — | `memory_mgr.s:3052` | BLOCKMOVE_CONT_14 Called during boot. |
| **`BLOCKMOVE_CONT_15`** | `0x010DC4` | — | `memory_mgr.s:3060` | BLOCKMOVE_CONT_15 Called during boot. |
| **`BLOCKMOVE_CONT_16`** | `0x010DC6` | — | `memory_mgr.s:3068` | BLOCKMOVE_CONT_16 Called during boot. |
| **`BLOCKMOVE_CONT_17`** | `0x010DC8` | — | `memory_mgr.s:3076` | BLOCKMOVE_CONT_17 Called during boot. |
| **`BLOCKMOVE_CONT_18`** | `0x010DCA` | — | `memory_mgr.s:3084` | BLOCKMOVE_CONT_18 Called during boot. |
| **`BLOCKMOVE_CONT_19`** | `0x010DCC` | — | `memory_mgr.s:3092` | BLOCKMOVE_CONT_19 Called during boot. |
| **`BLOCKMOVE_CONT_2`** | `0x010CFE` | `0x00B2CA` | `memory_mgr.s:2913`<br>`memory_mgr.s:2199` | BLOCKMOVE_CONT_2 Called during boot. |
| **`BLOCKMOVE_CONT_20`** | `0x010DCE` | — | `memory_mgr.s:3100` | BLOCKMOVE_CONT_20 Called during boot. |
| **`BLOCKMOVE_CONT_21`** | `0x010DD0` | — | `memory_mgr.s:3108` | BLOCKMOVE_CONT_21 Called during boot. |
| **`BLOCKMOVE_CONT_22`** | `0x010DD2` | — | `memory_mgr.s:3116` | BLOCKMOVE_CONT_22 Called during boot. |
| **`BLOCKMOVE_CONT_23`** | `0x010DD4` | — | `memory_mgr.s:3124` | BLOCKMOVE_CONT_23 Called during boot. |
| **`BLOCKMOVE_CONT_24`** | `0x010DD6` | — | `memory_mgr.s:3132` | BLOCKMOVE_CONT_24 Called during boot. |
| **`BLOCKMOVE_CONT_25`** | `0x010DD8` | — | `memory_mgr.s:3140` | BLOCKMOVE_CONT_25 Called during boot. |
| **`BLOCKMOVE_CONT_26`** | `0x010DDA` | — | `memory_mgr.s:3148` | BLOCKMOVE_CONT_26 Called during boot. |
| **`BLOCKMOVE_CONT_27`** | `0x010DDC` | — | `memory_mgr.s:3156` | BLOCKMOVE_CONT_27 Called during boot. |
| **`BLOCKMOVE_CONT_28`** | `0x010DDE` | — | `memory_mgr.s:3164` | BLOCKMOVE_CONT_28 Called during boot. |
| **`BLOCKMOVE_CONT_29`** | `0x010DE0` | — | `memory_mgr.s:3172` | BLOCKMOVE_CONT_29 Called during boot. |
| **`BLOCKMOVE_CONT_3`** | `0x010D30` | `0x00B2FC` | `memory_mgr.s:2959`<br>`memory_mgr.s:2242` | BLOCKMOVE_CONT_3 Called during boot. |
| **`BLOCKMOVE_CONT_30`** | `0x010DE2` | — | `memory_mgr.s:3179` | BLOCKMOVE_CONT_30 |
| **`BLOCKMOVE_CONT_31`** | `0x010DE4` | — | `memory_mgr.s:3187` | BLOCKMOVE_CONT_31 Called during boot. |
| **`BLOCKMOVE_CONT_32`** | `0x010DE6` | — | `memory_mgr.s:3194` | BLOCKMOVE_CONT_32 |
| **`BLOCKMOVE_CONT_33`** | `0x010DE8` | — | `memory_mgr.s:3202` | BLOCKMOVE_CONT_33 Called during boot. |
| **`BLOCKMOVE_CONT_34`** | `0x010DEA` | — | `memory_mgr.s:3209` | BLOCKMOVE_CONT_34 |
| **`BLOCKMOVE_CONT_35`** | `0x010DEC` | — | `memory_mgr.s:3216` | BLOCKMOVE_CONT_35 |
| **`BLOCKMOVE_CONT_36`** | `0x010DEE` | — | `memory_mgr.s:3223` | BLOCKMOVE_CONT_36 |
| **`BLOCKMOVE_CONT_37`** | `0x010DF0` | — | `memory_mgr.s:3231` | BLOCKMOVE_CONT_37 Called during boot. |
| **`BLOCKMOVE_CONT_38`** | `0x010DF2` | `0x00B3BE` | `memory_mgr.s:3238`<br>`memory_mgr.s:2373` | BLOCKMOVE_CONT_38 |
| **`BLOCKMOVE_CONT_39`** | `0x010DF4` | `0x00B3C0` | `memory_mgr.s:3246`<br>`memory_mgr.s:2380` | BLOCKMOVE_CONT_39 Called during boot. |
| **`BLOCKMOVE_CONT_4`** | `0x010DA8` | `0x00B374` | `memory_mgr.s:3012`<br>`memory_mgr.s:2294` | — |
| **`BLOCKMOVE_CONT_40`** | `0x010DF6` | `0x00B3C2` | `memory_mgr.s:3253`<br>`memory_mgr.s:2386` | BLOCKMOVE_CONT_40 |
| **`BLOCKMOVE_CONT_41`** | `0x010DF8` | `0x00B3C4` | `memory_mgr.s:3261`<br>`memory_mgr.s:2393` | BLOCKMOVE_CONT_41 Called during boot. |
| **`BLOCKMOVE_CONT_42`** | `0x010DFA` | `0x00B3C6` | `memory_mgr.s:3268`<br>`memory_mgr.s:2399` | BLOCKMOVE_CONT_42 |
| **`BLOCKMOVE_CONT_43`** | `0x010DFC` | `0x00B3C8` | `memory_mgr.s:3276`<br>`memory_mgr.s:2406` | BLOCKMOVE_CONT_43 Called during boot. |
| **`BLOCKMOVE_CONT_44`** | `0x010DFE` | `0x00B3CA` | `memory_mgr.s:3283`<br>`memory_mgr.s:2412` | BLOCKMOVE_CONT_44 |
| **`BLOCKMOVE_CONT_45`** | `0x010E00` | — | `memory_mgr.s:3291` | BLOCKMOVE_CONT_45 Called during boot. |
| **`BLOCKMOVE_CONT_46`** | `0x010E02` | `0x00B3CE` | `memory_mgr.s:3293`<br>`memory_mgr.s:2416` | — |
| **`BLOCKMOVE_CONT_47`** | `0x010E04` | `0x00B3D0` | `memory_mgr.s:3295`<br>`memory_mgr.s:2418` | — |
| **`BLOCKMOVE_CONT_48`** | `0x010E06` | `0x00B3D2` | `memory_mgr.s:3297`<br>`memory_mgr.s:2420` | — |
| **`BLOCKMOVE_CONT_49`** | `0x010E08` | `0x00B3D4` | `memory_mgr.s:3299`<br>`memory_mgr.s:2422` | — |
| **`BLOCKMOVE_CONT_5`** | `0x010DAE` | `0x00B37A` | `memory_mgr.s:3021`<br>`memory_mgr.s:2302` | BLOCKMOVE_CONT_5 Called during boot. |
| **`BLOCKMOVE_CONT_50`** | `0x010E0A` | `0x00B3D6` | `memory_mgr.s:3301`<br>`memory_mgr.s:2424` | — |
| **`BLOCKMOVE_CONT_51`** | `0x010E0C` | `0x00B3D8` | `memory_mgr.s:3303`<br>`memory_mgr.s:2426` | — |
| **`BLOCKMOVE_CONT_52`** | `0x010E0E` | `0x00B3DA` | `memory_mgr.s:3305`<br>`memory_mgr.s:2428` | — |
| **`BLOCKMOVE_CONT_53`** | `0x010E14` | — | `memory_mgr.s:3314` | BLOCKMOVE_CONT_53 |
| **`BLOCKMOVE_CONT_54`** | `0x010E16` | `0x00B3E2` | `memory_mgr.s:3316`<br>`memory_mgr.s:2434` | — |
| **`BLOCKMOVE_CONT_55`** | `0x010E18` | `0x00B3E4` | `memory_mgr.s:3318`<br>`memory_mgr.s:2436` | — |
| **`BLOCKMOVE_CONT_56`** | `0x010E1A` | `0x00B3E6` | `memory_mgr.s:3320`<br>`memory_mgr.s:2438` | — |
| **`BLOCKMOVE_CONT_57`** | `0x010E1C` | `0x00B3E8` | `memory_mgr.s:3322`<br>`memory_mgr.s:2440` | — |
| **`BLOCKMOVE_CONT_58`** | `0x010E1E` | `0x00B3EA` | `memory_mgr.s:3324`<br>`memory_mgr.s:2442` | — |
| **`BLOCKMOVE_CONT_59`** | `0x010E20` | `0x00B3EC` | `memory_mgr.s:3326`<br>`memory_mgr.s:2444` | — |
| **`BLOCKMOVE_CONT_6`** | `0x010DB0` | `0x00B37C` | `memory_mgr.s:3023`<br>`memory_mgr.s:2304` | — |
| **`BLOCKMOVE_CONT_60`** | `0x010E22` | `0x00B3EE` | `memory_mgr.s:3328`<br>`memory_mgr.s:2446` | — |
| **`BLOCKMOVE_CONT_61`** | `0x010E24` | `0x00B3F0` | `memory_mgr.s:3330`<br>`memory_mgr.s:2448` | — |
| **`BLOCKMOVE_CONT_62`** | `0x010E2A` | `0x00B3F6` | `memory_mgr.s:3339`<br>`memory_mgr.s:2456` | BLOCKMOVE_CONT_62 |
| **`BLOCKMOVE_CONT_63`** | `0x010E2C` | `0x00B3F8` | `memory_mgr.s:3341`<br>`memory_mgr.s:2458` | — |
| **`BLOCKMOVE_CONT_64`** | `0x010E2E` | `0x00B3FA` | `memory_mgr.s:3343`<br>`memory_mgr.s:2460` | — |
| **`BLOCKMOVE_CONT_65`** | `0x010E30` | `0x00B3FC` | `memory_mgr.s:3345`<br>`memory_mgr.s:2462` | — |
| **`BLOCKMOVE_CONT_66`** | `0x010E32` | `0x00B3FE` | `memory_mgr.s:3347`<br>`memory_mgr.s:2464` | — |
| **`BLOCKMOVE_CONT_67`** | `0x010E34` | `0x00B400` | `memory_mgr.s:3349`<br>`memory_mgr.s:2466` | — |
| **`BLOCKMOVE_CONT_68`** | `0x010E36` | `0x00B402` | `memory_mgr.s:3351`<br>`memory_mgr.s:2468` | — |
| **`BLOCKMOVE_CONT_69`** | `0x010E3E` | `0x00B40A` | `memory_mgr.s:3362`<br>`memory_mgr.s:2478` | BLOCKMOVE_CONT_69 Called during boot (3,684 times in 30s trace). |
| **`BLOCKMOVE_CONT_7`** | `0x010DB2` | `0x00B37E` | `memory_mgr.s:3025`<br>`memory_mgr.s:2306` | — |
| **`BLOCKMOVE_CONT_70`** | `0x010E9A` | `0x00B466` | `memory_mgr.s:3395`<br>`memory_mgr.s:2511` | — |
| **`BLOCKMOVE_CONT_71`** | `0x010EA6` | `0x00B472` | `memory_mgr.s:3410`<br>`memory_mgr.s:2525` | — |
| **`BLOCKMOVE_CONT_72`** | `0x010EA8` | `0x00B474` | `memory_mgr.s:3412`<br>`memory_mgr.s:2527` | — |
| **`BLOCKMOVE_CONT_73`** | `0x010EAA` | `0x00B476` | `memory_mgr.s:3414`<br>`memory_mgr.s:2529` | — |
| **`BLOCKMOVE_CONT_74`** | `0x010EAC` | `0x00B478` | `memory_mgr.s:3416`<br>`memory_mgr.s:2531` | — |
| **`BLOCKMOVE_CONT_75`** | `0x010EAE` | — | `memory_mgr.s:3418` | — |
| **`BLOCKMOVE_CONT_76`** | `0x010EB2` | — | `memory_mgr.s:3427` | BLOCKMOVE_CONT_76 Called during boot. |
| **`BLOCKMOVE_CONT_77`** | `0x010EB4` | — | `memory_mgr.s:3435` | BLOCKMOVE_CONT_77 Called during boot. |
| **`BLOCKMOVE_CONT_78`** | `0x010EB6` | — | `memory_mgr.s:3443` | BLOCKMOVE_CONT_78 Called during boot. |
| **`BLOCKMOVE_CONT_79`** | `0x010EB8` | — | `memory_mgr.s:3451` | BLOCKMOVE_CONT_79 Called during boot. |
| **`BLOCKMOVE_CONT_8`** | `0x010DB4` | `0x00B380` | `memory_mgr.s:3027`<br>`memory_mgr.s:2308` | — |
| **`BLOCKMOVE_CONT_80`** | `0x010EBA` | — | `memory_mgr.s:3459` | BLOCKMOVE_CONT_80 Called during boot. |
| **`BLOCKMOVE_CONT_81`** | `0x010EBC` | — | `memory_mgr.s:3467` | BLOCKMOVE_CONT_81 Called during boot. |
| **`BLOCKMOVE_CONT_82`** | `0x010EBE` | — | `memory_mgr.s:3475` | BLOCKMOVE_CONT_82 Called during boot (1,364 times in 30s trace). |
| **`BLOCKMOVE_CONT_83`** | `0x010EC0` | — | `memory_mgr.s:3482` | BLOCKMOVE_CONT_83 |
| **`BLOCKMOVE_CONT_84`** | `0x010EC2` | — | `memory_mgr.s:3490` | BLOCKMOVE_CONT_84 Called during boot. |
| **`BLOCKMOVE_CONT_85`** | `0x010EC4` | — | `memory_mgr.s:3498` | BLOCKMOVE_CONT_85 Called during boot. |
| **`BLOCKMOVE_CONT_86`** | `0x010EC6` | — | `memory_mgr.s:3506` | BLOCKMOVE_CONT_86 Called during boot (1,065 times in 30s trace). |
| **`BLOCKMOVE_CONT_87`** | `0x010EC8` | — | `memory_mgr.s:3514` | BLOCKMOVE_CONT_87 Called during boot. |
| **`BLOCKMOVE_CONT_88`** | `0x010ECA` | — | `memory_mgr.s:3522` | BLOCKMOVE_CONT_88 Called during boot. |
| **`BLOCKMOVE_CONT_89`** | `0x010ECC` | — | `memory_mgr.s:3529` | BLOCKMOVE_CONT_89 |
| **`BLOCKMOVE_CONT_9`** | `0x010DB6` | `0x00B382` | `memory_mgr.s:3029`<br>`memory_mgr.s:2310` | — |
| **`BLOCKMOVE_CONT_90`** | `0x010ECE` | — | `memory_mgr.s:3537` | BLOCKMOVE_CONT_90 Called during boot. |
| **`BLOCKMOVE_CONT_91`** | `0x010ED0` | — | `memory_mgr.s:3545` | BLOCKMOVE_CONT_91 Called during boot. |
| **`BLOCKMOVE_CONT_92`** | `0x010ED2` | — | `memory_mgr.s:3553` | BLOCKMOVE_CONT_92 Called during boot. |
| **`BLOCKMOVE_EXIT`** | `0x010D0E` | `0x00B2DA` | `memory_mgr.s:2922`<br>`memory_mgr.s:2208` | — |
| **`BLOCKMOVE_FWD_ALIGNED`** | — | `0x00B320` | `memory_mgr.s:2266` | — |
| **`BLOCKMOVE_LOOP`** | `0x010CE0` | `0x00B2AC` | `memory_mgr.s:2885`<br>`memory_mgr.s:2173` | — |
| **`BLOCKMOVE_LOOP_2`** | `0x010D12` | `0x00B2DE` | `memory_mgr.s:2931`<br>`memory_mgr.s:2216` | BLOCKMOVE_LOOP_2 Called during boot (3,452 times in 30s trace). |
| **`BLOCKMOVE_LOOP_3`** | `0x010D72` | `0x00B33E` | `memory_mgr.s:2992`<br>`memory_mgr.s:2274` | — |
| **`BLOCKMOVE_LOOP_4`** | `0x010D92` | `0x00B35E` | `memory_mgr.s:3001`<br>`memory_mgr.s:2283` | — |
| **`BLOCKMOVE_LOOP_5`** | `0x010E64` | `0x00B430` | `memory_mgr.s:3375`<br>`memory_mgr.s:2491` | — |
| **`BLOCKMOVE_LOOP_6`** | `0x010E84` | `0x00B450` | `memory_mgr.s:3384`<br>`memory_mgr.s:2500` | — |
| **`BLOCKMOVE_LOOP_7`** | `0x010EA0` | `0x00B46C` | `memory_mgr.s:3404`<br>`memory_mgr.s:2519` | BLOCKMOVE_LOOP_7 Called during boot. |
| **`BLOCKMOVE_LOOP_8`** | `0x010EA2` | `0x00B46E` | `memory_mgr.s:3406`<br>`memory_mgr.s:2521` | — |
| **`BLOCKMOVE_LOOP_9`** | `0x010EA4` | `0x00B470` | `memory_mgr.s:3408`<br>`memory_mgr.s:2523` | — |
| **`BLOCKMOVE_NO`** | `0x010CF6` | `0x00B2C2` | `memory_mgr.s:2903`<br>`memory_mgr.s:2190` | BLOCKMOVE_NO Called during boot. |
| **`BLOCKMOVE_NO_2`** | `0x010D28` | `0x00B2F4` | `memory_mgr.s:2949`<br>`memory_mgr.s:2233` | BLOCKMOVE_NO_2 Called during boot (1,485 times in 30s trace). |
| **`BLOCKMOVE_NO_3`** | `0x010D44` | `0x00B310` | `memory_mgr.s:2976`<br>`memory_mgr.s:2258` | BLOCKMOVE_NO_3 Called during boot (3,821 times in 30s trace). |
| **`BLOCKMOVE_NO_4`** | `0x010D54` | — | `memory_mgr.s:2984` | — |
| **`BLOCKMOVE_NO_5`** | `0x010E46` | — | `memory_mgr.s:3367` | — |
| **`BMChk`** | `0x003332` | — | `file_mgr_vol.s:924` | BM Chk BMChk: wrapper for BlkChk that checks write-protect first |
| **`BMCHK_CONT`** | `0x00334C` | `0x004DD2` | `file_mgr_vol.s:940`<br>`file_mgr_vol.s:907` | BMCHK_CONT - close extent and catalog B-tree FCBs (mark as free) |
| **`BMCHK_CONT_2`** | `0x00336E` | `0x004DF4` | `file_mgr_vol.s:958`<br>`file_mgr_vol.s:921` | BMCHK_CONT_2 - dequeue and dispose VCB, close all open FCBs for this volume |
| **`BMCHK_CONT_3`** | `0x003374` | `0x004DFA` | `file_mgr_vol.s:961`<br>`file_mgr_vol.s:924` | — |
| **`BMCHK_CONT_4`** | `0x0033A2` | `0x004E28` | `file_mgr_vol.s:984`<br>`file_mgr_vol.s:943` | BMCHK_CONT_4 - trash all cached blocks for the volume being unmounted |
| **`BMCHK_CONT_5`** | `0x0033C0` | — | `file_mgr_vol.s:999` | BMCHK_CONT_5 - FindFCB: find a free FCB entry |
| **`BMCHK_CONT_6`** | `0x0033C6` | `0x004E4C` | `file_mgr_vol.s:1002`<br>`file_mgr_vol.s:958` | — |
| **`BMCHK_CONT_7`** | `0x0033DE` | `0x004E64` | `file_mgr_vol.s:1013`<br>`file_mgr_vol.s:969` | — |
| **`BMCHK_CONT_8`** | `0x0033E0` | `0x004E66` | `file_mgr_vol.s:1021`<br>`file_mgr_vol.s:976` | BMCHK_CONT_8 - AccessBT: set up access to a B*-Tree file D0=refnum, D1=file ID, D2=clump size, A1=cache, A3=key compare routine |
| **`BMCHK_EMPTY`** | `0x00335E` | `0x004DE4` | `file_mgr_vol.s:946`<br>`file_mgr_vol.s:913` | — |
| **`BMCHK_EMPTY_2`** | `0x003368` | `0x004DEE` | `file_mgr_vol.s:950`<br>`file_mgr_vol.s:917` | — |
| **`BMCHK_NEXT`** | `0x0033D6` | — | `file_mgr_vol.s:1009` | — |
| **`BMCHK_NO`** | `0x003384` | `0x004E0A` | `file_mgr_vol.s:967`<br>`file_mgr_vol.s:930` | — |
| **`BMCHK_NO_2`** | `0x00339C` | `0x004E22` | `file_mgr_vol.s:975`<br>`file_mgr_vol.s:938` | — |
| **`BMCHK_SKIP`** | `0x003348` | `0x004DCE` | `file_mgr_vol.s:932`<br>`file_mgr_vol.s:900` | — |
| **`BOOT_SCSI_DISPOSE_BUF`** | — | `0x004116` | `scsi_boot.s:132` | BOOT_SCSI_DISPOSE_BUF -- error path: dispose driver buffer, return -1 |
| **`BOOT_SCSI_DRIVE_OK`** | — | `0x004060` | `scsi_boot.s:33` | — |
| **`BOOT_SCSI_DRVR_INSTALL`** | — | `0x004282` | `scsi_boot.s:308` | — |
| **`BOOT_SCSI_DRVR_OK`** | — | `0x004288` | `scsi_boot.s:312` | — |
| **`BOOT_SCSI_DRVR_REFNUM`** | — | `0x00427C` | `scsi_boot.s:304` | BOOT_SCSI_DRVR_REFNUM -- 16-bit rotating-add checksum A0 -> data, D1 = byte count - 1.  For each byte: D0 = ROL16(D0 + byte) Result in D0; if the natural result would be 0, returns -1 instead so calle... |
| **`BOOT_SCSI_DRVR_RTS`** | — | `0x004292` | `scsi_boot.s:317` | — |
| **`BOOT_SCSI_FIND_HFS`** | — | `0x004194` | `scsi_boot.s:190` | Called by: BOOT_SCSI_FIND_HFS |
| **`BOOT_SCSI_HFS_FOUND`** | — | `0x00423C` | `scsi_boot.s:271` | — |
| **`BOOT_SCSI_NEXT_PM_ENTRY`** | — | `0x00416E` | `scsi_boot.s:173` | BOOT_SCSI_NEXT_PM_ENTRY -- next PM entry (search continues for Apple_Driver) Called by: BOOT_SCSI_PMAP_LOOP, BOOT_SCSI_NEXT_PM_ENTRY |
| **`BOOT_SCSI_NO_DRIVE`** | — | `0x004070` | `scsi_boot.s:41` | — |
| **`BOOT_SCSI_NO_PMAP`** | — | `0x00410E` | `scsi_boot.s:125` | BOOT_SCSI_NO_PMAP -- no partition map, just run the driver-init code |
| **`BOOT_SCSI_PMAP_LOOP`** | — | `0x004120` | `scsi_boot.s:150` | BOOT_SCSI_PMAP_LOOP -- check current PM entry for "Apple_Driver" partition. Partition entry layout (Apple Partition Map, 512 bytes): +0x00 W  pmSig 0x504D ('PM') +0x04 L  pmMapBlkCnt +0x08 L  pmPyPart... |
| **`BOOT_SCSI_RDBLOCKS`** | — | `0x004270` | `scsi_boot.s:289` | Called by: BOOT_SCSI_HFS_FOUND, SCSIREADBLOCKS_RETRY |
| **`BOOT_SCSI_RESCAN`** | — | `0x00418E` | `scsi_boot.s:186` | BOOT_SCSI_RESCAN -- restart PM scan from block 1, look for Apple_HFS |
| **`BOOT_SCSI_RTS`** | — | `0x00411C` | `scsi_boot.s:137` | — |
| **`BOOT_SCSI_RTS_ERR`** | — | `0x00411A` | `scsi_boot.s:135` | — |
| **`BOOT_SCSI_RUN_DRIVER`** | — | `0x004112` | `scsi_boot.s:128` | — |
| **`BOOT_SCSI_SCAN_PMAP`** | — | `0x004080` | `scsi_boot.s:71` | BOOT_SCSI_SCAN_PMAP -- scan one SCSI device for a partition driver D5 = SCSI ID being probed.  Returns Z if a driver was loaded. Flow: 1. Read block 0 (Driver Descriptor Map). Check for "ER" signature... |
| **`BOOT_SCSI_TRY_DRIVE`** | — | `0x004058` | `scsi_boot.s:29` | — |
| **`BT_CLEANUP`** | `0x006E02` | `0x0088C2` | `file_mgr_btree.s:946`<br>`file_mgr_btree.s:820` | BT_CLEANUP BTCleanUp: cleans up after a BTree service call |
| **`BT_SETUP`** | `0x006E10` | `0x0088D0` | `file_mgr_btree.s:958`<br>`file_mgr_btree.s:828` | BT_SETUP - BTSetUp: sets up for a BTree service call |
| **`BTALLOC`** | — | `0x0088F8` | `file_mgr_btree.s:844` | — |
| **`BTClose`** | `0x0066E2` | `0x0081A6` | `file_mgr_btree.s:40` | BT Close |
| **`BTCLOSE`** | `0x0066E2` | `0x0081A6` | `file_mgr_btree.s:28` | File Manager - B-tree Engine Generic B-tree implementation used by HFS for both the catalog file and the extents overflow file. Supports search, insert, delete, and node splitting/rotation for balance... |
| **`BTCLOSE_EXIT`** | `0x006712` | `0x0081DC` | `file_mgr_btree.s:58`<br>`file_mgr_btree.s:49` | — |
| **`BTDEL_CHKFLINK`** | `0x0067B2` | `0x008278` | `file_mgr_btree.s:131`<br>`file_mgr_btree.s:114` | — |
| **`BTDEL_CHKLEAF`** | `0x006758` | `0x008220` | `file_mgr_btree.s:98`<br>`file_mgr_btree.s:79` | — |
| **`BTDEL_CHKRECS`** | `0x006764` | `0x00822C` | `file_mgr_btree.s:102`<br>`file_mgr_btree.s:84` | BTDelChkRecs: check if node is empty |
| **`BTDEL_CHKUPD`** | `0x006852` | `0x00831A` | `file_mgr_btree.s:197`<br>`file_mgr_btree.s:179` | check if done BTDEL_CHKUPD |
| **`BTDEL_CLEANUP`** | `0x0068A8` | `0x00837E` | `file_mgr_btree.s:241`<br>`file_mgr_btree.s:223` | BTDelCleanup: release node and exit Called by: VBTDELETE, BTDEL_CHKRECS, BTDEL_GETRSIB, BTDEL_GETPAR, BTDEL_UPDDEPTH |
| **`BTDEL_DELREC`** | `0x006740` | `0x00820A` | `file_mgr_btree.s:89`<br>`file_mgr_btree.s:70` | BTDelRec: delete record from current node |
| **`BTDEL_DONE`** | `0x0068A2` | `0x008378` | `file_mgr_btree.s:238`<br>`file_mgr_btree.s:218` | **Regs:** `BDExit: release last node and exit`<br>release the previous root node BDExit: release last node and exit |
| **`BTDEL_FREENODE`** | `0x0067BC` | — | `file_mgr_btree.s:136` | BDFree: free the empty node |
| **`BTDEL_GETPAR`** | `0x0067FA` | `0x0082BE` | `file_mgr_btree.s:157`<br>`file_mgr_btree.s:141` | BTDelGetPar: get parent node |
| **`BTDEL_GETRSIB`** | `0x006784` | `0x00824A` | `file_mgr_btree.s:114`<br>`file_mgr_btree.s:97` | node empty: update sibling links |
| **`BTDEL_NXTLEV`** | `0x0067E4` | — | `file_mgr_btree.s:150` | BDNxtLev: move to next level up |
| **`BTDEL_RELCHILD`** | `0x00683C` | `0x008304` | `file_mgr_btree.s:182`<br>`file_mgr_btree.s:169` | BDUpdKey: update parent key |
| **`BTDEL_ROOT`** | `0x00685A` | `0x008322` | `file_mgr_btree.s:206`<br>`file_mgr_btree.s:184` | BTDEL_ROOT - BDRoot: up to root, check for empty tree |
| **`BTDEL_UPDDEPTH`** | `0x006868` | `0x008330` | `file_mgr_btree.s:218`<br>`file_mgr_btree.s:191` | BTDEL_UPDDEPTH BDUpdDepth: update tree depth if root has only 1 index record |
| **`BTDEL_UPDPTRS`** | `0x0067A0` | `0x008266` | `file_mgr_btree.s:125`<br>`file_mgr_btree.s:108` | BDUpdPtrs: update 1st and last node pointers |
| **`BTDelete`** | `0x006722` | `0x0081E6` | `file_mgr_btree.s:78` | BT Delete |
| **`BTDELETE`** | `0x006722` | `0x0081E6` | `file_mgr_btree.s:55` | Called by: CMDELETECN_DODELETE, DEALLOCFILE_NO_2, TRUNCATEFILE_OK, CC_CLR_THD_LOOP, MC_UPD_DEST (and 1 more) |
| **`BTFlush`** | `0x0068C8` | `0x008398` | `file_mgr_btree.s:266` | BT Flush |
| **`BTFLUSH`** | `0x0068C8` | `0x008398` | `file_mgr_btree.s:234` | — |
| **`BTFLUSH_CACHE`** | `0x006910` | `0x0083E6` | `file_mgr_btree.s:296`<br>`file_mgr_btree.s:265` | release cache buffer BFFlush: flush the cache for this file |
| **`BTFLUSH_CPYLOOP`** | `0x006900` | `0x0083D6` | `file_mgr_btree.s:287`<br>`file_mgr_btree.s:257` | get BTH from disk update BTH from BTCB info |
| **`BTFLUSH_EXIT`** | `0x00691E` | `0x0083F2` | `file_mgr_btree.s:303`<br>`file_mgr_btree.s:271` | BFExit |
| **`BTGetRecord`** | `0x00692E` | `0x0083FC` | `file_mgr_btree.s:322` | BT Get Record |
| **`BTGETRECORD`** | `0x00692E` | `0x0083FC` | `file_mgr_btree.s:276` | — |
| **`BTINS_CHKERR`** | `0x006A5E` | `0x008528` | `file_mgr_btree.s:509`<br>`file_mgr_btree.s:428` | build BTree record: input key with junk data record BISearch: search tree for key BTINS_CHKERR |
| **`BTINS_CKDONE`** | `0x006B2C` | `0x0085F8` | `file_mgr_btree.s:604`<br>`file_mgr_btree.s:511` | BICkDone: check if all done |
| **`BTINS_CLEANUP`** | `0x006C5A` | `0x008724` | `file_mgr_btree.s:717`<br>`file_mgr_btree.s:628` | BICleanup: release all nodes and exit Called by: BTINS_CHKERR, BTINS_NEWROOT, BTINS_INIT, BTINS_TRY_ROTLT, BTINS_DOSPLIT (and 1 more) |
| **`BTINS_DONE`** | `0x006C54` | `0x00871E` | `file_mgr_btree.s:714`<br>`file_mgr_btree.s:623` | insert left child index record into new root insert right child index record into new root BIDone: insert complete |
| **`BTINS_DOSPLIT`** | — | `0x0085AC` | `file_mgr_btree.s:479` | BISplit: rotation failed, must split the node |
| **`BTINS_EXIT`** | `0x006C80` | `0x00874A` | `file_mgr_btree.s:731`<br>`file_mgr_btree.s:642` | — |
| **`BTINS_EXTEND`** | `0x006A0C` | — | `file_mgr_btree.s:469` | make sure there is enough file space for worst case split |
| **`BTINS_EXTEND_RETRY`** | — | `0x0084D6` | `file_mgr_btree.s:389` | ensure file space for worst-case split |
| **`BTINS_INIT`** | `0x006A1A` | `0x0084E4` | `file_mgr_btree.s:475`<br>`file_mgr_btree.s:395` | BIInit: initialize some things |
| **`BTINS_INSDONE`** | `0x006B02` | `0x0085CE` | `file_mgr_btree.s:588`<br>`file_mgr_btree.s:495` | BIInsDone: completed the record insert |
| **`BTINS_INSERT`** | `0x006AA8` | `0x008574` | `file_mgr_btree.s:532`<br>`file_mgr_btree.s:452` | if tree is empty, add 1st leaf node BIInsert: try a simple insert first |
| **`BTINS_KEYUPD`** | `0x006AF6` | `0x0085C2` | `file_mgr_btree.s:582`<br>`file_mgr_btree.s:489` | — |
| **`BTINS_NEWIREC`** | `0x006AF2` | `0x0085BE` | `file_mgr_btree.s:580`<br>`file_mgr_btree.s:487` | BTINS_NEWIREC - BISplit1: new index record required after split |
| **`BTINS_NEWROOT`** | `0x006BD4` | `0x0086A0` | `file_mgr_btree.s:674`<br>`file_mgr_btree.s:579` | set up for insert of new index record BTINS_NEWROOT |
| **`BTINS_NXTLEV`** | `0x006B3A` | `0x008606` | `file_mgr_btree.s:610`<br>`file_mgr_btree.s:517` | BINxtLev: move to next level |
| **`BTINS_RELLEFT`** | `0x006BA8` | `0x008674` | `file_mgr_btree.s:653`<br>`file_mgr_btree.s:562` | BINewRec: build new index record pointing at new left node |
| **`BTINS_RELRIGHT`** | `0x006B8E` | `0x00865A` | `file_mgr_btree.s:641`<br>`file_mgr_btree.s:549` | BIUpdKey: update parent key |
| **`BTINS_ROTATE`** | `0x006AC0` | — | `file_mgr_btree.s:548` | BTINS_ROTATE - BIRotate: try rotation into left sibling |
| **`BTINS_SAVEMARK`** | `0x006B28` | `0x0085F4` | `file_mgr_btree.s:601`<br>`file_mgr_btree.s:508` | — |
| **`BTINS_SPLIT`** | `0x006AE0` | — | `file_mgr_btree.s:567` | BTINS_SPLIT - BISplit: rotate didn't work, got to split |
| **`BTINS_TRY_ROTLT`** | — | `0x00858C` | `file_mgr_btree.s:464` | BIRotate: try rotation into left sibling |
| **`BTInsert`** | `0x0069F0` | `0x0084B4` | `file_mgr_btree.s:457` | BT Insert |
| **`BTINSERT`** | `0x0069F0` | `0x0084B4` | `file_mgr_btree.s:374` | Called by: EXTENDFILE_LOOP, CC_ADD_REC, CC_CLR_THD_LOOP, MC_INSERT_DST, CMRENAMECN |
| **`BTMAINT1`** | — | `0x008BC8` | `file_mgr_btree.s:1163` | RotateLT: rotate records from right node to left sibling |
| **`BTMAINT2`** | — | `0x008E00` | `file_mgr_btree.s:1445` | BuildIRec: build index record (key + child node ptr) |
| **`BTN_INVERT`** | `0x001446` | `0x00164E` | `sys_error.s:499`<br>`sys_error.s:453` | BTN_INVERT - invert (highlight/unhighlight) button at A3 |
| **`BTN_PT_IN_RECT`** | `0x001438` | `0x001640` | `sys_error.s:487`<br>`sys_error.s:442` | BTN_PT_IN_RECT - test if mouse is inside button rect at A3 Returns D0 nonzero if mouse point is inside the rect. |
| **`BTOpen`** | `0x006C90` | `0x008754` | `file_mgr_btree.s:750` | BT Open |
| **`BTOPEN`** | `0x006C90` | `0x008754` | `file_mgr_btree.s:647` | — |
| **`BTOPEN_BADHDR`** | `0x006D16` | `0x0087D8` | `file_mgr_btree.s:800`<br>`file_mgr_btree.s:700` | allocate and initialize a BTCB get BTH from disk BOChkHdr: make sure the BTree header node is ok BOBadHdr |
| **`BTOPEN_CPYBTH`** | `0x006D1A` | `0x0087DC` | `file_mgr_btree.s:809`<br>`file_mgr_btree.s:708` | BTOPEN_CPYBTH BOCpyBTH: copy BTH into BTCB |
| **`BTOPEN_CPYLOOP`** | `0x006D26` | `0x0087E8` | `file_mgr_btree.s:813`<br>`file_mgr_btree.s:712` | — |
| **`BTOPEN_EXIT`** | `0x006D40` | `0x008802` | `file_mgr_btree.s:828`<br>`file_mgr_btree.s:726` | — |
| **`BTOPEN_RELBLK`** | `0x006D2E` | `0x0087F0` | `file_mgr_btree.s:818`<br>`file_mgr_btree.s:716` | **Regs:** `BOExit: release header block and exit`<br>BOExit: release header block and exit |
| **`BTOPEN_RESULT`** | `0x006D3E` | `0x008800` | `file_mgr_btree.s:826`<br>`file_mgr_btree.s:724` | — |
| **`BTREC_ATBEGIN`** | `0x006982` | `0x008452` | `file_mgr_btree.s:381`<br>`file_mgr_btree.s:324` | BTREC_ATBEGIN - at beginning of leaf chain |
| **`BTREC_ATEND`** | `0x006968` | `0x00843A` | `file_mgr_btree.s:359`<br>`file_mgr_btree.s:310` | BTREC_ATEND - at end of leaf chain, use last record as mark |
| **`BTREC_CHKINDX`** | `0x006952` | `0x008424` | `file_mgr_btree.s:343`<br>`file_mgr_btree.s:298` | GRChkIndx: check index bounds |
| **`BTREC_EXIT`** | `0x0069A4` | `0x008472` | `file_mgr_btree.s:401`<br>`file_mgr_btree.s:340` | GRExit |
| **`BTREC_FOUND`** | `0x006992` | `0x008460` | `file_mgr_btree.s:393`<br>`file_mgr_btree.s:332` | BTREC_FOUND - GRGotIt: found the record |
| **`BTREC_GETNODE`** | `0x00694C` | — | `file_mgr_btree.s:340` | — |
| **`BTREC_GETPREV`** | `0x00696E` | `0x008440` | `file_mgr_btree.s:368`<br>`file_mgr_btree.s:315` | BTREC_GETPREV - get previous node |
| **`BTREC_GRGETNODE`** | — | `0x008420` | `file_mgr_btree.s:294` | GRGetNode: release current, get node D3 |
| **`BTREC_LOCATE`** | `0x00694A` | `0x00841E` | `file_mgr_btree.s:338`<br>`file_mgr_btree.s:291` | BTREC_LOCATE - GRLocate: locate record relative to starting position |
| **`BTREC_SETMARK`** | `0x006984` | `0x008454` | `file_mgr_btree.s:383`<br>`file_mgr_btree.s:326` | — |
| **`BTSearch`** | `0x006D50` | `0x00880C` | `file_mgr_btree.s:848` | BT Search |
| **`BTSEARCH`** | `0x006D50` | `0x00880C` | `file_mgr_btree.s:732` | Called by: MOUNTVOL_OK_9, DEALLOCFILE_NEXT, TRUNCATEFILE_RELEASE_EXTENT, VXFSEARCH, XFSEARCH_NO_2 (and 1 more) |
| **`BTSEARCH_CLEANUP`** | — | `0x00888A` | `file_mgr_btree.s:789` | — |
| **`BTSRCH_EXIT`** | `0x006DC8` | — | `file_mgr_btree.s:903` | — |
| **`BTSRCH_FOUND`** | `0x006D9E` | `0x008860` | `file_mgr_btree.s:883`<br>`file_mgr_btree.s:771` | BSGotIt: found or not-found with valid position |
| **`BTSRCH_RELHINT`** | `0x006D84` | `0x008846` | `file_mgr_btree.s:870`<br>`file_mgr_btree.s:757` | initialize some things go directly to the leaf node if hint is given |
| **`BTSRCH_RELNODE`** | `0x006DB6` | `0x008878` | `file_mgr_btree.s:896`<br>`file_mgr_btree.s:782` | **Regs:** `BSExit: release node buffer and exit`<br>update current markers in BTCB set up pointers to key and data record BSExit: release node buffer and exit |
| **`BTSRCH_TREE`** | `0x006D8E` | `0x008850` | `file_mgr_btree.s:876`<br>`file_mgr_btree.s:763` | BSTSrch: search tree for key |
| **`BTSVCS`** | — | `0x0081A6` | `file_mgr_btree.s:27` | File Manager - B-tree Engine Generic B-tree implementation used by HFS for both the catalog file and the extents overflow file. Supports search, insert, delete, and node splitting/rotation for balance... |
| **`BTUPD_EXIT`** | `0x006DF8` | `0x0088B8` | `file_mgr_btree.s:935`<br>`file_mgr_btree.s:810` | — |
| **`BTUpdate`** | `0x006DDC` | `0x008896` | `file_mgr_btree.s:924` | BT Update |
| **`BTUPDATE`** | `0x006DDC` | `0x008896` | `file_mgr_btree.s:796` | Called by: MC_UPD_DEST, XFSEARCH_LOOP_3, CC_UPD_PAR, DC_UPD_PAR, MC_UPD_SRC (and 3 more) |
| **`BuildIRec`** | `0x0072A0` | `0x008E00` | `file_mgr_btree.s:1613` | BuildIRec -- build index record. Build I Rec |
| **`BUILDIREC`** | `0x0072A0` | `0x008E00` | `file_mgr_btree.s:1446` | BuildIRec: build index record (key + child node ptr) |
| **`BuildKey`** | `0x0065D8` | `0x0080A0` | `file_mgr_catalog.s:674` | BuildKey -- build the key record. Build Key Called by: CMCreateCN, CC_BLD_THD, CC_CLR_THD_LOOP, DC_DELETE, CMRenameCN (and 1 more) |
| **`BUILDKEY`** | `0x0065D8` | `0x0080A0` | `file_mgr_catalog.s:606` | BuildKey: build a catalog key record Called by: CMCREATECN, CC_BLD_THD, CC_CLR_THD_LOOP, CMDELETECN_DODELETE, CMRENAMECN (and 1 more) |
| **`Cache`** | `0x00769A` | `0x0091EE` | `file_mgr_cache.s:26` | File Manager - Block Cache Caches disk blocks in memory for the B-tree and catalog operations. Each cached block is tagged with its volume, file, and block number. Dirty blocks are written back on Flu... |
| **`CACHE`** | `0x00769A` | `0x0091EE` | `file_mgr_cache.s:23` | File Manager - Block Cache Caches disk blocks in memory for the B-tree and catalog operations. Each cached block is tagged with its volume, file, and block number. Dirty blocks are written back on Flu... |
| **`CACHE_DONE`** | `0x0076A6` | `0x0091FA` | `file_mgr_cache.s:31`<br>`file_mgr_cache.s:28` | — |
| **`CACHEIO`** | — | `0x009702` | `file_mgr_cache.s:649` | — |
| **`CacheRDIP`** | `0x007B30` | `0x00967E` | `file_mgr_cache.s:703` | Cache RDIP Called during boot. |
| **`CACHERDIP`** | `0x007B30` | `0x00967E` | `file_mgr_cache.s:584` | — |
| **`CacheWRIP`** | `0x007B5C` | `0x0096AA` | `file_mgr_cache.s:732` | Cache WRIP |
| **`CACHEWRIP`** | `0x007B5C` | `0x0096AA` | `file_mgr_cache.s:602` | — |
| **`CACHEWRIP_EXIT`** | `0x007B7C` | `0x0096D0` | `file_mgr_cache.s:744`<br>`file_mgr_cache.s:617` | — |
| **`CAL_BTVARS`** | `0x006E2E` | — | `file_mgr_btree.s:974` | CAL_BTVARS - CalBTVars: calculate size of BTVars |
| **`CALL_DRV_ENTRY`** | `0x002152` | `0x002EDE` | `device_mgr.s:269`<br>`device_mgr.s:249` | CALL_DRV_ENTRY - Call driver entry point A1 = DCE pointer, A0 = IOParam block, D1 = entry point offset in driver header (drvrOpen=$08, drvrPrime=$0A, drvrCtl=$0C, drvrStatus=$0E). Loads and locks RAM-... |
| **`CALL_DRV_EXEC`** | `0x002190` | `0x002F1E` | `device_mgr.s:301`<br>`device_mgr.s:278` | Execute driver entry point |
| **`CALL_DRV_EXIT`** | `0x0021A0` | `0x002F2E` | `device_mgr.s:313`<br>`device_mgr.s:286` | — |
| **`CALL_DRV_LOADFAIL`** | `0x00219C` | `0x002F2A` | `device_mgr.s:311`<br>`device_mgr.s:284` | CALL_DRV_LOADFAIL - _LoadResource failed for RAM-based driver |
| **`CALL_DRV_LOCK`** | `0x00215E` | `0x002EEA` | `device_mgr.s:282`<br>`device_mgr.s:255` | CALL_DRV_LOCK - Lock driver resource and dispatch to entry point For RAM-based drivers (dRAMBased=1), lock the resource handle and load it if purged. Then call the driver entry point. |
| **`CALL_DRV_LOCK_HDL`** | `0x002186` | — | `device_mgr.s:296` | — |
| **`CALL_DS_DRAWPROC`** | `0x00133A` | `0x00154A` | `sys_error.s:344`<br>`sys_error.s:303` | CALL_DS_DRAWPROC - call DSDrawProc if installed If DSDrawProc is a valid pointer (positive nonzero), calls it to draw custom DS content. Sets bit 7 to prevent re-entrancy. |
| **`CATMOVE_BAD_NAME_RTS`** | — | `0x006102` | `file_mgr_dir.s:828` | Called by: CATMOVE_HFS_PATH, TFMOVE, HFSCATMOVE_NO, HFSCATMOVE_ERR_3, CATMOVE_NEXT_FCB |
| **`CATMOVE_HFS_PATH`** | — | `0x006106` | `file_mgr_dir.s:831` | check write protect and find source file |
| **`CATMOVE_NEXT_FCB`** | — | `0x0061CC` | `file_mgr_dir.s:915` | — |
| **`CATMOVE_NO_CROSSVOL`** | — | `0x006100` | `file_mgr_dir.s:825` | determine destination directory determine source directory |
| **`CC_ADD_REC`** | `0x0060BE` | `0x007B8C` | `file_mgr_catalog.s:78`<br>`file_mgr_catalog.s:68` | CCAddRec: add new directory/file record to catalog BTree |
| **`CC_BLD_THD`** | `0x0060D8` | `0x007BA6` | `file_mgr_catalog.s:93`<br>`file_mgr_catalog.s:82` | CC_BLD_THD CCBldThd: build thread record for new directory CNode |
| **`CC_CLR_CDR_LOOP`** | `0x006078` | `0x007B46` | `file_mgr_catalog.s:49`<br>`file_mgr_catalog.s:41` | set up some initial stuff make sure parent exists build key for new CNode initialize catalog data record (cdr) for directory or file |
| **`CC_CLR_THD_LOOP`** | `0x0060F2` | `0x007BC0` | `file_mgr_catalog.s:103`<br>`file_mgr_catalog.s:92` | — |
| **`CC_EXIT`** | `0x00617C` | `0x007C4A` | `file_mgr_catalog.s:156`<br>`file_mgr_catalog.s:142` | update VCB directory and file counts CCExit |
| **`CC_INIT_FILE`** | `0x0060A2` | `0x007B70` | `file_mgr_catalog.s:68`<br>`file_mgr_catalog.s:59` | CC_INIT_FILE |
| **`CC_UPD_PAR`** | `0x006144` | `0x007C12` | `file_mgr_catalog.s:134`<br>`file_mgr_catalog.s:121` | add thread record to catalog BTree couldn't add thread record, delete newly created directory record CCUpdPar: update parent directory |
| **`Chain`** | `0x00F556` | `0x00999C` | `segment_loader.s:171` | _Chain ($A9F3) _Chain ($A9F3): launch next app without full cleanup |
| **`CHAIN`** | `0x00F556` | `0x00999C` | `segment_loader.s:129` | — |
| **`CHECK_FORK_ALREADY_OPEN_DONE`** | — | `0x005C00` | `file_mgr_dir.s:190` | — |
| **`CHECKREMOUNT`** | `0x003008` | `0x004A5A` | `file_mgr_vol.s:570`<br>`file_mgr_vol.s:535` | find two free FCBs for the volume control B*-Trees set up volume caches finish setting up FCBs for extent and catalog B*-Trees mark disk as inconsistent from now until unmount CheckRemount: scan VCB q... |
| **`CheckSCSI`** | `0x007D40` | — | `scsi_boot.s:19` | SCSI boot support -- CheckSCSI, SCSIProbeDevice, SCSIReadBlocks Apple source: SCSIBoot.a (MacSEROM.lst module SCSIBOOTS). Called while the system starts up: probes SCSI IDs 6 down to 0, reads each dev... |
| **`ChkNode`** | `0x0072C2` | `0x008E22` | `file_mgr_btree.s:1631` | ChkNode -- validate node structure. Chk Node |
| **`CHKNODE`** | `0x0072C2` | `0x008E22` | `file_mgr_btree.s:1459` | ChkNode: validate a B-tree node's structure |
| **`CHKNODE_BAD`** | `0x007340` | `0x008E98` | `file_mgr_btree.s:1680`<br>`file_mgr_btree.s:1504` | CNBadNode |
| **`CHKNODE_EXIT`** | `0x007346` | `0x008E9E` | `file_mgr_btree.s:1686`<br>`file_mgr_btree.s:1509` | — |
| **`CHKNODE_OFFLOOP`** | `0x007322` | `0x008E7E` | `file_mgr_btree.s:1668`<br>`file_mgr_btree.s:1492` | validate offset table entries |
| **`CHKNODE_OK`** | `0x007344` | `0x008E9C` | `file_mgr_btree.s:1684`<br>`file_mgr_btree.s:1507` | CNExit |
| **`CHKVOL`** | `0x004048` | `0x005AE2` | `file_mgr_dir.s:81`<br>`file_mgr_dir.s:62` | ChkVol: search directory for the file to open |
| **`CKExtFS`** | `0x003638` | — | `file_mgr_vol.s:1340` | CKExtFS: check for external file system Called during boot. |
| **`CkExtFS_AndOnline`** | — | `0x006560` | `file_mgr_dir.s:1359` | CkExtFS + volume online check Called by: GETVOLINFO_CONT_6, SETVOLINFO, RENAME_VOL_VERIFY_ONLINE, CATMOVE_HFS_PATH, FNDFILNAME_NO_3 (and 2 more) |
| **`CKEXTFS_NO`** | `0x003640` | — | `file_mgr_vol.s:1344` | — |
| **`CKEXTFS_RTS`** | — | `0x0050CC` | `file_mgr_vol.s:1250` | — |
| **`CKFILERFN`** | `0x00537A` | `0x006E2C` | `file_mgr_io.s:657`<br>`file_mgr_io.s:583` | CKFILERFN Called during boot. CkFileRfn: check that refnum points to a valid open file |
| **`CkFileRfn_RTS`** | — | `0x006E4A` | `file_mgr_io.s:597` | — |
| **`CLEAR_DRV_BUSY`** | `0x0020A2` | `0x002E2E` | `device_mgr.s:168`<br>`device_mgr.s:153` | CLEAR_DRV_BUSY - Clear driver busy flag and unlock driver resource A1 = DCE pointer. Clears the "busy" bit (bit 7) of dCtlFlags+1 and, unless dNeedLock is set, unlocks the driver handle in both the ha... |
| **`ClearGZStuff`** | `0x0108F8` | `0x00AEB6` | `memory_mgr.s:2244` | ClearGZStuff - clear GZRootHnd and GZRootPtr (the block being sized or reallocated no longer needs protection from the grow-zone function). Called by SetSize and ReallocHandle. Called during boot (7,4... |
| **`CLEARGZSTUFF`** | `0x0108F8` | `0x00AEB6` | `memory_mgr.s:1621` | — |
| **`Close`** | `0x002386` | `0x003124` | `device_mgr.s:578` | _Close ($A001) A0 = paramBlock -> D0 = error Positive ioRefNum -> file close (File Manager); negative -> device close. Called during boot. |
| **`CLOSE`** | `0x002386` | `0x003124` | `device_mgr.s:523` | **Regs:** `Entry: A0 = IOParam, ioRefNum (+0x18) identifies driver`<br>CLOSE - _Close trap: close a device driver Entry: A0 = IOParam, ioRefNum (+0x18) identifies driver Negative refNum = device driver; positive = file (dispatch to FS) |
| **`CLOSE_DEVICE`** | `0x002390` | `0x00312E` | `device_mgr.s:587`<br>`device_mgr.s:527` | CLOSE_DEVICE - device driver close path |
| **`CLOSE_WAIT_BUSY`** | `0x0023A2` | `0x003140` | `device_mgr.s:593`<br>`device_mgr.s:533` | — |
| **`CLOSEFILE_FLUSH_MDB`** | — | `0x0079C2` | `file_mgr_alloc.s:817` | — |
| **`CLOSEFILE_NOERR_RESTORE`** | — | `0x0079C4` | `file_mgr_alloc.s:819` | — |
| **`CLOSEWD`** | — | `0x0056AA` | `file_mgr_vol.s:1949` | _CloseWD: close a working directory |
| **`CloseWD_hfs`** | `0x003C1E` | — | `file_mgr_vol.s:2137` | Close WD_hfs _CloseWD (HFS): close a working directory |
| **`CLOSEWD_HFS_CONT`** | `0x003C36` | `0x0056C2` | `file_mgr_vol.s:2147`<br>`file_mgr_vol.s:1959` | close the working directory |
| **`CLOSEWD_HFS_CONT_2`** | `0x003C54` | — | `file_mgr_vol.s:2165` | — |
| **`CLOSEWD_HFS_EXIT`** | `0x003C52` | — | `file_mgr_vol.s:2163` | — |
| **`CLOSEWD_HFS_OK`** | `0x003C4E` | `0x0056DA` | `file_mgr_vol.s:2161`<br>`file_mgr_vol.s:1968` | CLOSEWD_HFS_OK |
| **`CLOSEWD_OK_DONE`** | — | `0x0056DE` | `file_mgr_vol.s:1970` | — |
| **`ClrNode`** | `0x00734E` | `0x008EA6` | `file_mgr_btree.s:1696` | ClrNode -- zero out the node buffer. Clr Node |
| **`CLRNODE`** | `0x00734E` | `0x008EA6` | `file_mgr_btree.s:1514` | ClrNode: zero out a node buffer |
| **`CLRNODE_LOOP`** | `0x00735E` | `0x008EB6` | `file_mgr_btree.s:1703`<br>`file_mgr_btree.s:1521` | — |
| **`CM_EPILOGUE`** | — | `0x007F20` | `file_mgr_catalog.s:433` | Called by: MC_UPD_DEST, MC_CHK_DEST, MC_INSERT_DST, MC_UPD_SRC, CMMOVECN (and 3 more) |
| **`CMCreateCN`** | `0x006044` | `0x007B12` | `file_mgr_catalog.s:26` | File Manager - HFS Catalog Operations Implements HFS catalog B-tree record operations. The catalog file is a B-tree that maps (parentID, name) to file/directory info. Catalog Manager (CM) routines: CM... |
| **`CMCREATECN`** | `0x006044` | `0x007B12` | `file_mgr_catalog.s:22` | File Manager - HFS Catalog Operations Implements HFS catalog B-tree record operations. The catalog file is a B-tree that maps (parentID, name) to file/directory info. Catalog Manager (CM) routines: CM... |
| **`CMDeleteCN`** | `0x00618A` | `0x007C58` | `file_mgr_catalog.s:168` | CMDeleteCN -- delete catalog entry. CM Delete CN |
| **`CMDELETECN`** | `0x00618A` | `0x007C58` | `file_mgr_catalog.s:148` | — |
| **`CMDELETECN_DODELETE`** | — | `0x007C9A` | `file_mgr_catalog.s:173` | DCDelete: delete catalog records for CNode |
| **`CMFlush`** | `0x006606` | `0x0080CE` | `file_mgr_catalog.s:698` | CMFlush -- flush the catalog. CM Flush Called by: CC_UPD_PAR, DC_UPD_PAR, MC_EXIT, RC_EXIT, UC_FLUSH |
| **`CMFLUSH`** | `0x006606` | `0x0080CE` | `file_mgr_catalog.s:624` | Called by: CC_UPD_PAR, DC_UPD_PAR, CMMOVECN_EXIT, CMRENAMECN_EXIT, UC_FLUSH |
| **`CMFLUSH_EXIT`** | `0x006630` | `0x0080F8` | `file_mgr_catalog.s:713`<br>`file_mgr_catalog.s:639` | — |
| **`CMFLUSH_OK`** | `0x00662E` | `0x0080F6` | `file_mgr_catalog.s:711`<br>`file_mgr_catalog.s:637` | — |
| **`CMGetCN`** | `0x006238` | `0x007D04` | `file_mgr_catalog.s:246` | CMGetCN -- locate catalog record. CM Get CN Called by: FNDFILNAME_CONT_3, MOUNTVOL_OK_3, MTCHECK, MOUNTVOL_FOUND_3, GETVOLINFO_CONT_6 (and 4 more) |
| **`CMGETCN`** | `0x006238` | `0x007D04` | `file_mgr_catalog.s:216` | Called by: FNDFILNAME_CONT_3, MOUNTVOL_OK_3, MTCHECK, MOUNTVOL_FOUND_3, GETVOLINFO_CONT_6 (and 4 more) |
| **`CMGetOff`** | `0x006258` | `0x007D24` | `file_mgr_catalog.s:265` | locate directory/file BTree record for the CNode GCExit CMGetOff -- get Nth offspring record. CM Get Off |
| **`CMGETOFF`** | `0x006258` | `0x007D24` | `file_mgr_catalog.s:227` | — |
| **`CMKeyCmp`** | `0x00663A` | `0x008102` | `file_mgr_catalog.s:723` | CM Key Cmp |
| **`CMKEYCMP`** | `0x00663A` | `0x008102` | `file_mgr_catalog.s:644` | — |
| **`CMMAINT`** | — | `0x0080A0` | `file_mgr_catalog.s:605` | BuildKey: build a catalog key record Called by: CMCREATECN, CC_BLD_THD, CC_CLR_THD_LOOP, CMDELETECN_DODELETE, CMRENAMECN (and 1 more) |
| **`CMMoveCN`** | `0x0062BC` | `0x007D88` | `file_mgr_catalog.s:314` | CMMoveCN -- move the catalog entry. CM Move CN |
| **`CMMOVECN`** | `0x0062BC` | `0x007D88` | `file_mgr_catalog.s:271` | — |
| **`CMMOVECN_EXIT`** | — | `0x007F14` | `file_mgr_catalog.s:427` | update VCB counts for source MCExit |
| **`CmpString`** | `0x00F7EE` | `0x009C38` | `os_utilities.s:110` | _CmpString ($A03C) _CmpString ($A03C): compare two strings (case-insensitive) D0.hi = length1, D0.lo = length2, A0 = str1, A1 = str2 Returns D0 = 0 if equal, nonzero if different |
| **`CMPSTRING`** | `0x00F7EE` | `0x009C38` | `os_utilities.s:79` | CMPSTRING -- _CmpString ($A03C): compare two strings for equality (D0 high/low = lengths, A0/A1 = the strings); D0 = 0 if equal, 1 if not |
| **`CMPSTRING_CONT`** | `0x00F7FE` | `0x009C48` | `os_utilities.s:119`<br>`os_utilities.s:88` | — |
| **`CMPSTRING_LENDIFF`** | `0x00F800` | — | `os_utilities.s:127` | CMPSTRING_LENDIFF CmpString: lengths differ -> not equal |
| **`CMPSTRING_NOTEQUAL`** | — | `0x009C4A` | `os_utilities.s:90` | — |
| **`CMRenameCN`** | `0x006462` | `0x007F2E` | `file_mgr_catalog.s:486` | CMRenameCN -- rename the root directory. CM Rename CN |
| **`CMRENAMECN`** | `0x006462` | `0x007F2E` | `file_mgr_catalog.s:439` | — |
| **`CMRENAMECN_EPILOGUE`** | — | `0x008028` | `file_mgr_catalog.s:541` | Called by: CMRENAMECN, RC_DEL_OLD, RC_EXISTS_ERR, RC_UPD_THD |
| **`CMRENAMECN_EXIT`** | — | `0x00801C` | `file_mgr_catalog.s:535` | RCExit |
| **`CMSetUp`** | `0x0065A6` | — | `file_mgr_catalog.s:639` | CM Set Up - allocate CM vars on A6 stack |
| **`CMSVCS`** | — | `0x007B12` | `file_mgr_catalog.s:21` | File Manager - HFS Catalog Operations Implements HFS catalog B-tree record operations. The catalog file is a B-tree that maps (parentID, name) to file/directory info. Catalog Manager (CM) routines: CM... |
| **`CMUpdateCN`** | `0x00656C` | `0x008036` | `file_mgr_catalog.s:599` | CMUpdateCN -- call helper. CM Update CN |
| **`CMUPDATECN`** | `0x00656C` | `0x008036` | `file_mgr_catalog.s:547` | — |
| **`CompactHp`** | `0x0107B2` | `0x00AD68` | `memory_mgr.s:1995` | **Regs:** `Entry: D0.L = physical size needed, A6 = zone Exit:  A0 = free block of at least D0 bytes or nil (also stored in`<br>CompactHp - compact the zone until a free block of D0 bytes exists Entry: D0.L = physical size needed, A6 = zone Exit:  A0 = free block of at least D0 bytes or nil (also stored in allocPtr), D1 = larg... |
| **`COMPACTHP`** | `0x0107B2` | `0x00AD68` | `memory_mgr.s:1425` | — |
| **`COMPACTHP_CONT`** | `0x0107CC` | `0x00AD82` | `memory_mgr.s:2013`<br>`memory_mgr.s:1442` | — |
| **`COMPACTHP_CONT_2`** | `0x0107DA` | `0x00AD90` | `memory_mgr.s:2020`<br>`memory_mgr.s:1449` | — |
| **`COMPACTHP_CONT_3`** | `0x0107DE` | `0x00AD94` | `memory_mgr.s:2023`<br>`memory_mgr.s:1452` | — |
| **`COMPACTHP_CONT_4`** | `0x010836` | `0x00ADEC` | `memory_mgr.s:2098`<br>`memory_mgr.s:1522` | COMPACTHP_CONT_4 Called during boot. |
| **`COMPACTHP_DONE`** | `0x010846` | `0x00ADFC` | `memory_mgr.s:2108`<br>`memory_mgr.s:1532` | — |
| **`COMPACTHP_OK`** | `0x0107D0` | `0x00AD86` | `memory_mgr.s:2016`<br>`memory_mgr.s:1445` | — |
| **`COMPACTHP_OK_2`** | `0x01080C` | `0x00ADC2` | `memory_mgr.s:2050`<br>`memory_mgr.s:1478` | COMPACTHP_OK_2 Called during boot. |
| **`COMPACTHP_OK_3`** | `0x010822` | `0x00ADD8` | `memory_mgr.s:2075`<br>`memory_mgr.s:1501` | COMPACTHP_OK_3 Called during boot. |
| **`COMPACTHP_OK_4`** | `0x010826` | `0x00ADDC` | `memory_mgr.s:2084`<br>`memory_mgr.s:1509` | COMPACTHP_OK_4 Called during boot. |
| **`COMPACTHP_OK_5`** | `0x010828` | `0x00ADDE` | `memory_mgr.s:2086`<br>`memory_mgr.s:1511` | — |
| **`COMPACTHP_SKIP`** | `0x0107C0` | `0x00AD76` | `memory_mgr.s:2007`<br>`memory_mgr.s:1436` | COMPACTHP_SKIP Called during boot. |
| **`COMPACTHP_SKIP_2`** | `0x01081E` | `0x00ADD4` | `memory_mgr.s:2066`<br>`memory_mgr.s:1493` | COMPACTHP_SKIP_2 Called during boot. |
| **`COMPACTHP_SKIP_3`** | `0x010840` | `0x00ADF6` | `memory_mgr.s:2104`<br>`memory_mgr.s:1528` | — |
| **`CompactMem`** | `0x00FFBE` | `0x00A4CE` | `memory_mgr.s:283` | **Proto:** `Pascal: FUNCTION CompactMem(cbNeeded: Size): Size;`<br>**Regs:** `Entry: D0.L = cbNeeded; trap bit 10 ($A44C) = use the system heap Exit:  D0.L = logical size of the largest contiguous free block found;`<br>_CompactMem ($A04C): compact the current heap zone Pascal: FUNCTION CompactMem(cbNeeded: Size): Size; Entry: D0.L = cbNeeded; trap bit 10 ($A44C) = use the system heap Exit:  D0.L = logical size of th... |
| **`COMPACTMEM`** | `0x00FFBE` | `0x00A4CE` | `memory_mgr.s:200` | — |
| **`COMPACTMEM_CONT`** | `0x00FFC4` | — | `memory_mgr.s:286` | — |
| **`COMPACTMEM_CONT_2`** | `0x00FFDC` | — | `memory_mgr.s:301` | COMPACTMEM_NO - MaxBlock: clear fNSelCompct, so CompactHp only measures |
| **`COMPACTMEM_NO`** | `0x00FFD8` | `0x00A4E8` | `memory_mgr.s:299`<br>`memory_mgr.s:211` | COMPACTMEM_NO - MaxBlock: clear fNSelCompct, so CompactHp only measures |
| **`Compressed_ALine_Dispatch_Table`** | — | `0x01AA9C` | `dispatch_table.s:14` | Compressed trap dispatch table Apple source: DispTable.a (MacSEROM.lst modules RESTOP and DSPTABLE). Read once at startup by INITDISPATCHER (boot_install.s), which fills the Toolbox dispatch table (51... |
| **`Control`** | `0x002442` | `0x0031E0` | `device_mgr.s:689` | _Control ($A004) A0 = paramBlock (CntrlParam) -> D0 = error D0 = -17 (controlErr default), D4 = 2 (dCtlEnable bit position) Called during boot. |
| **`CONTROL__MAP`** | — | — | `device_mgr.s:601` | P_tControl - _Control trap handler |
| **`CONVERSION_TBL`** | `0x00F98A` | — | `os_utilities.s:311` | — |
| **`COPY_ALERT_RECT`** | `0x001216` | `0x001424` | `sys_error.s:160`<br>`sys_error.s:110` | COPY_ALERT_RECT - copy DSAlertRect and offset to GrafPort origin Copies the 8-byte alert rectangle to Scratch20_2, clears the high bit (used as "rect initialized" flag), then offsets the rect by the G... |
| **`CORESTUB`** | — | `0x002CB4` | `vbl_mgr.s:69` | — |
| **`COUNTADBS`** | — | `0x003CF2` | `adb_mgr.s:1117` | COUNTADBS - _CountADBs trap: count ADB devices with non-zero address |
| **`COUNTADBS_TEST`** | — | `0x003D00` | `adb_mgr.s:1124` | — |
| **`Create`** | `0x0041E2` | — | `file_mgr_dir.s:291` | **Proto:** `Create -- _Create ($A008): FUNCTION Create (fileName: Str255; vRefNum: INTEGER; creator:`<br>Create -- _Create ($A008): FUNCTION Create (fileName: Str255; vRefNum: INTEGER; creator: _Create ($A008) |
| **`CREATE_BAD_NAME_RTS`** | — | `0x005D92` | `file_mgr_dir.s:407` | name has colon or is empty: bad name for MFS |
| **`CREATE_CONT`** | `0x0041EC` | — | `file_mgr_dir.s:294` | — |
| **`CREATE_CONT_10`** | `0x004366` | `0x005E00` | `file_mgr_dir.s:525`<br>`file_mgr_dir.s:463` | — |
| **`CREATE_CONT_11`** | `0x0043A0` | `0x005E3A` | `file_mgr_dir.s:562`<br>`file_mgr_dir.s:498` | CREATE_CONT_11 CREATE_CONT_11: get WDCB array base and initial offset |
| **`CREATE_CONT_12`** | `0x0043B0` | `0x005E4A` | `file_mgr_dir.s:581`<br>`file_mgr_dir.s:515` | CREATE_CONT_12: find first WDCB belonging to volume A2 |
| **`CREATE_CONT_13`** | `0x0043B2` | `0x005E4C` | `file_mgr_dir.s:583`<br>`file_mgr_dir.s:517` | — |
| **`CREATE_CONT_14`** | `0x0043C2` | `0x005E5C` | `file_mgr_dir.s:599`<br>`file_mgr_dir.s:532` | CREATE_CONT_14 CREATE_CONT_14: CkDirBusy - check if any files in directory D6 are open |
| **`CREATE_CONT_15`** | `0x0043CC` | `0x005E66` | `file_mgr_dir.s:603`<br>`file_mgr_dir.s:536` | — |
| **`CREATE_CONT_16`** | `0x0043DA` | `0x005E74` | `file_mgr_dir.s:616`<br>`file_mgr_dir.s:548` | CREATE_ERR_6 |
| **`CREATE_CONT_17`** | `0x004400` | `0x005E9A` | `file_mgr_dir.s:644`<br>`file_mgr_dir.s:570` | — |
| **`CREATE_CONT_2`** | `0x004288` | `0x005D28` | `file_mgr_dir.s:386`<br>`file_mgr_dir.s:347` | CREATE_CONT_2 - PopCName: restore CName from A6 stack |
| **`CREATE_CONT_3`** | `0x0042D6` | — | `file_mgr_dir.s:432` | CREATE_CONT_3 |
| **`CREATE_CONT_4`** | `0x0042DA` | — | `file_mgr_dir.s:434` | — |
| **`CREATE_CONT_5`** | `0x0042F6` | — | `file_mgr_dir.s:460` | CREATE_CONT_5 MFS Create: check write protect and find space in directory |
| **`CREATE_CONT_6`** | `0x004304` | `0x005D9E` | `file_mgr_dir.s:468`<br>`file_mgr_dir.s:416` | MFS Create: initialize new directory entry |
| **`CREATE_CONT_7`** | `0x004340` | `0x005DDA` | `file_mgr_dir.s:501`<br>`file_mgr_dir.s:444` | CREATE_CONT_7 Called during boot. CREATE_CONT_7: MFS directory flush - flush the system control cache for this volume |
| **`CREATE_CONT_8`** | `0x00434E` | `0x005DE8` | `file_mgr_dir.s:512`<br>`file_mgr_dir.s:450` | CREATE_CONT_8 CREATE_CONT_8: find space in MFS directory for a new entry |
| **`CREATE_CONT_9`** | `0x004362` | `0x005DFC` | `file_mgr_dir.s:522`<br>`file_mgr_dir.s:460` | — |
| **`CREATE_DONE`** | — | `0x005CF4` | `file_mgr_dir.s:310` | Called by: CREATE_NAME_NOT_FOUND, CREATE_NO, CREATE_TRY_RESOLVE |
| **`CREATE_EMPTY`** | `0x004332` | — | `file_mgr_dir.s:488` | — |
| **`CREATE_ERR`** | `0x0041F6` | — | `file_mgr_dir.s:305` | CREATE_ERR Create/CreateDir: check if file already exists |
| **`CREATE_ERR_2`** | `0x004254` | — | `file_mgr_dir.s:348` | — |
| **`CREATE_ERR_3`** | `0x0042E4` | `0x005D84` | `file_mgr_dir.s:445`<br>`file_mgr_dir.s:399` | — |
| **`CREATE_ERR_4`** | `0x0042F2` | — | `file_mgr_dir.s:452` | — |
| **`CREATE_ERR_5`** | `0x004388` | `0x005E22` | `file_mgr_dir.s:540`<br>`file_mgr_dir.s:478` | — |
| **`CREATE_ERR_6`** | `0x0043D8` | `0x005E72` | `file_mgr_dir.s:614`<br>`file_mgr_dir.s:546` | CREATE_ERR_6 |
| **`CREATE_FOUND`** | `0x004370` | `0x005E0A` | `file_mgr_dir.s:531`<br>`file_mgr_dir.s:469` | MFS Create: insert new entry in directory block |
| **`CREATE_FOUND_2`** | `0x0043C0` | `0x005E5A` | `file_mgr_dir.s:591`<br>`file_mgr_dir.s:525` | — |
| **`CREATE_FOUND_3`** | `0x004404` | `0x005E9E` | `file_mgr_dir.s:652`<br>`file_mgr_dir.s:573` | CREATE_FOUND_3 |
| **`CREATE_LOOP`** | `0x00432C` | `0x005DC6` | `file_mgr_dir.s:484`<br>`file_mgr_dir.s:432` | fill in MFS directory entry fields set creation and modification dates copy filename into entry |
| **`CREATE_MFS_BUMP_NMFLS`** | — | `0x005DCC` | `file_mgr_dir.s:436` | — |
| **`CREATE_MFS_PATH`** | — | `0x005D96` | `file_mgr_dir.s:410` | MFS create: check write protect and find directory space |
| **`CREATE_NAME_NOT_FOUND`** | — | `0x005C90` | `file_mgr_dir.s:265` | name not found: check error and volume type |
| **`CREATE_NEXT`** | `0x00438A` | `0x005E24` | `file_mgr_dir.s:548`<br>`file_mgr_dir.s:485` | CREATE_NEXT: advance to next MFS directory entry Called during boot. |
| **`CREATE_NEXT_2`** | `0x0043B8` | `0x005E52` | `file_mgr_dir.s:587`<br>`file_mgr_dir.s:521` | CREATE_NEXT_2: advance to next WDCB and continue scanning |
| **`CREATE_NO`** | `0x004226` | `0x005CC6` | `file_mgr_dir.s:327`<br>`file_mgr_dir.s:288` | — |
| **`CREATE_NO_2`** | `0x004252` | — | `file_mgr_dir.s:346` | — |
| **`CREATE_NO_3`** | `0x004282` | `0x005D22` | `file_mgr_dir.s:378`<br>`file_mgr_dir.s:339` | copy CName to A6 stack as Pascal string |
| **`CREATE_NO_4`** | `0x004292` | `0x005D32` | `file_mgr_dir.s:392`<br>`file_mgr_dir.s:353` | — |
| **`CREATE_NO_5`** | `0x004294` | `0x005D34` | `file_mgr_dir.s:401`<br>`file_mgr_dir.s:361` | CREATE_NO_5 Called during boot. MFSOpen: MFS file open path |
| **`CREATE_NO_6`** | `0x0042AA` | `0x005D4A` | `file_mgr_dir.s:409`<br>`file_mgr_dir.s:369` | — |
| **`CREATE_NO_7`** | `0x0042DE` | `0x005D7E` | `file_mgr_dir.s:441`<br>`file_mgr_dir.s:395` | CREATE_NO_7 |
| **`CREATE_NO_8`** | `0x00435E` | `0x005DF8` | `file_mgr_dir.s:520`<br>`file_mgr_dir.s:458` | scan directory blocks for free space |
| **`CREATE_NO_DIRID`** | — | `0x005CF2` | `file_mgr_dir.s:307` | — |
| **`CREATE_OK`** | `0x004246` | `0x005CE6` | `file_mgr_dir.s:342`<br>`file_mgr_dir.s:303` | — |
| **`CREATE_OK_2`** | `0x0042CC` | — | `file_mgr_dir.s:423` | load fork info from MFS directory entry |
| **`CREATE_OK_3`** | `0x0042F0` | `0x005D90` | `file_mgr_dir.s:450`<br>`file_mgr_dir.s:405` | name has colon or is empty: bad name for MFS |
| **`CREATE_OK_4`** | `0x0043E0` | `0x005E7A` | `file_mgr_dir.s:624`<br>`file_mgr_dir.s:555` | CREATE_OK_4 |
| **`CREATE_OK_5`** | `0x0043E8` | `0x005E82` | `file_mgr_dir.s:634`<br>`file_mgr_dir.s:560` | CREATE_OK_5 CREATE_OK_5: CkFileBusy - check if file is open (has any FCBs) |
| **`CREATE_OK_6`** | `0x0043F8` | `0x005E92` | `file_mgr_dir.s:640`<br>`file_mgr_dir.s:566` | — |
| **`CREATE_SKIP`** | `0x0043A8` | `0x005E42` | `file_mgr_dir.s:572`<br>`file_mgr_dir.s:507` | CREATE_SKIP: advance to next WDCB entry (16 bytes each) Called by: OPENWD_HFS_CONT_3, OPENWD_HFS_OK, GETWDINFO_HFS_NO, GETWDINFO_HFS_SKIP, CREATE_NEXT_2 |
| **`CREATE_TRY_RESOLVE`** | — | `0x005C86` | `file_mgr_dir.s:259` | — |
| **`CREATECN`** | `0x004210` | `0x005CB0` | `file_mgr_dir.s:320`<br>`file_mgr_dir.s:281` | CREATECN CreateCN: create the catalog record |
| **`CREATEDIR`** | — | `0x005C70` | `file_mgr_dir.s:252` | — |
| **`CreateDir_hfs`** | `0x0041D6` | — | `file_mgr_dir.s:281` | Create Dir_hfs |
| **`D2S_IN_JAN_FEB`** | `0x017112` | `0x01A182` | `date_utils.s:131`<br>`date_utils.s:117` | — |
| **`D2S_NOT_LEAP`** | `0x017110` | `0x01A180` | `date_utils.s:129`<br>`date_utils.s:115` | — |
| **`Date2Secs`** | `0x0170CA` | `0x01A13A` | `date_utils.s:95` | **Regs:** `Entry: A0 = pointer to 14-byte DateTimeRec Exit: D0.L = seconds since epoch`<br>_Date2Secs ($A9C7) - Date2Secs Converts a DateTimeRec to seconds since midnight Jan 1 1904. Entry: A0 = pointer to 14-byte DateTimeRec Exit: D0.L = seconds since epoch Reads fields in reverse order (d... |
| **`DATE2SECS`** | `0x0170CA` | `0x01A13A` | `date_utils.s:84` | **Proto:** `Pascal: procedure Date2Secs(d: DateTimeRec; var secs: LongInt);`<br>_Date2Secs ($A9C7) - convert date components to seconds. Pascal: procedure Date2Secs(d: DateTimeRec; var secs: LongInt); In: A0 = DateTimeRec ptr (year/month/day/hour/min/sec). Out: D0 = seconds since... |
| **`DBG_CALL_HANDLER`** | `0x00118A` | — | `sys_error.s:60` | — |
| **`DBG_SKIP_SP_SAVE`** | `0x00116A` | `0x0013AE` | `sys_error.s:42`<br>`sys_error.s:42` | — |
| **`DBG_USE_DS_HANDLER`** | `0x001186` | — | `sys_error.s:58` | DBG_USE_DS_HANDLER - default: use built-in DS error handler |
| **`DC_CHK_EMPTY`** | `0x0061C4` | `0x007C90` | `file_mgr_catalog.s:190`<br>`file_mgr_catalog.s:167` | set up some common stuff locate subject CNode DCCkDir: if directory, make sure it's not root and is empty |
| **`DC_DELETE`** | `0x0061CE` | — | `file_mgr_catalog.s:196` | DCDelete: delete catalog records for CNode |
| **`DC_EXIT`** | `0x00622A` | `0x007CF6` | `file_mgr_catalog.s:233`<br>`file_mgr_catalog.s:209` | update VCB directory and file counts DCExit |
| **`DC_UPD_PAR`** | `0x0061F6` | `0x007CC2` | `file_mgr_catalog.s:213`<br>`file_mgr_catalog.s:190` | DCDelThd: delete thread record (directories only) DCUpdPar: update parent directory |
| **`DeallocFile`** | `0x005AAE` | `0x007550` | `file_mgr_alloc.s:420` | Dealloc File |
| **`DEALLOCFILE`** | `0x005AAE` | `0x007550` | `file_mgr_alloc.s:354` | — |
| **`DEALLOCFILE_CONT`** | `0x005ABE` | `0x007566` | `file_mgr_alloc.s:428`<br>`file_mgr_alloc.s:364` | DFFkLoop: locate catalog record for file |
| **`DEALLOCFILE_DONE`** | `0x005B62` | `0x00760A` | `file_mgr_alloc.s:497`<br>`file_mgr_alloc.s:430` | DFNxtFork: check for another fork |
| **`DEALLOCFILE_ERR`** | `0x005B6E` | `0x007616` | `file_mgr_alloc.s:503`<br>`file_mgr_alloc.s:436` | DFExit |
| **`DEALLOCFILE_FOUND`** | `0x005B1E` | `0x0075C6` | `file_mgr_alloc.s:466`<br>`file_mgr_alloc.s:401` | get the next extent record DFCopyRec: copy extent data to FXM buffer |
| **`DEALLOCFILE_LOOP`** | `0x005B24` | `0x0075CC` | `file_mgr_alloc.s:469`<br>`file_mgr_alloc.s:404` | — |
| **`DEALLOCFILE_NEXT`** | `0x005AF6` | `0x00759E` | `file_mgr_alloc.s:451`<br>`file_mgr_alloc.s:387` | DFRecLoop: set up key for next extent file record |
| **`DEALLOCFILE_NEXT_2`** | `0x005B30` | `0x0075D8` | `file_mgr_alloc.s:475`<br>`file_mgr_alloc.s:409` | DFRelExt: release extents for this record |
| **`DEALLOCFILE_NO`** | `0x005AF0` | `0x007598` | `file_mgr_alloc.s:447`<br>`file_mgr_alloc.s:383` | — |
| **`DEALLOCFILE_NO_2`** | `0x005B4A` | `0x0075F2` | `file_mgr_alloc.s:486`<br>`file_mgr_alloc.s:420` | DFDelRec: delete extent record |
| **`DEALLOCFILE_OK`** | `0x005ADA` | `0x007582` | `file_mgr_alloc.s:439`<br>`file_mgr_alloc.s:375` | — |
| **`DEALLOCFILE_OK_2`** | `0x005B5E` | `0x007606` | `file_mgr_alloc.s:493`<br>`file_mgr_alloc.s:427` | — |
| **`Delay`** | `0x00F7DC` | `0x009C26` | `os_utilities.s:94` | _Delay ($A03B): delay for specified number of ticks (1/60 sec) A0 = tick count to delay |
| **`DELAY`** | `0x00F7DC` | `0x009C26` | `os_utilities.s:66` | — |
| **`DELAY_LOOP`** | `0x00F7E6` | `0x009C30` | `os_utilities.s:98`<br>`os_utilities.s:70` | — |
| **`Delete`** | `0x00440C` | — | `file_mgr_dir.s:662` | _Delete ($A009) _Delete ($A009) |
| **`DELETE_CONT`** | `0x00444A` | `0x005EE4` | `file_mgr_dir.s:686`<br>`file_mgr_dir.s:601` | — |
| **`DELETE_DIR_NOT_EMPTY`** | — | `0x005F18` | `file_mgr_dir.s:624` | — |
| **`DELETE_ERR`** | `0x00447E` | — | `file_mgr_dir.s:709` | — |
| **`DELETE_FILE`** | — | `0x005EE6` | `file_mgr_dir.s:604` | deallocate file's disk space and delete catalog entry |
| **`DELETE_MFS_DONE`** | — | `0x006208` | `file_mgr_dir.s:937` | delete MFS file: deallocate blocks and remove entry |
| **`DELETE_NO`** | `0x00443C` | `0x005ED6` | `file_mgr_dir.s:679`<br>`file_mgr_dir.s:594` | check if file is locked determine record type: directory or file file record: check if file is open |
| **`DELETE_NO_2`** | `0x00446A` | `0x005F04` | `file_mgr_dir.s:701`<br>`file_mgr_dir.s:616` | file: deallocate disk space first |
| **`DELETE_SKIP`** | `0x00444C` | — | `file_mgr_dir.s:689` | deallocate file's disk space and delete catalog entry |
| **`DeleteRec`** | `0x00736A` | `0x008EC2` | `file_mgr_btree.s:1714` | DeleteRec -- deleteRec: remove record at index D1 from node A3. Delete Rec |
| **`DELETEREC`** | `0x00736A` | `0x008EC2` | `file_mgr_btree.s:1527` | DeleteRec: remove record at index D1 from node A1 |
| **`DEQ_RETURN`** | `0x001A22` | `0x002B0E` | `queue.s:92`<br>`queue.s:80` | — |
| **`DEQ_SEARCH_LOOP`** | `0x001A00` | `0x002AEC` | `queue.s:70`<br>`queue.s:62` | — |
| **`DEQ_SUCCESS`** | `0x001A20` | `0x002B0C` | `queue.s:90`<br>`queue.s:78` | — |
| **`DEQ_UNLINK`** | `0x001A12` | `0x002AFE` | `queue.s:84`<br>`queue.s:72` | DEQ_UNLINK - unlink element from queue |
| **`DEQ_UNLINK_MID`** | `0x001A2A` | `0x002B16` | `queue.s:101`<br>`queue.s:85` | DEQ_UNLINK_MID - unlink element from middle or end of queue |
| **`Dequeue`** | `0x0019F0` | `0x002ADC` | `queue.s:64` | _Dequeue ($A96E) - remove element from OS queue A0 = ptr to QElem to remove. A1 = ptr to QHdr (flags, qHead, qTail). Returns D0: 0 = success, -1 = element not found. Called by: VBL_TASK_LOOP, VRemove,... |
| **`DEQUEUE`** | `0x0019F0` | `0x002ADC` | `queue.s:56` | DEQUEUE - remove element A0 from queue at A1 Searches queue for element A0, unlinks it from the chain. Returns D0 = 0 if found and removed, D0 = -1 if not found. Called by: VBL_TASK_LOOP, VREMOVE, ADB... |
| **`DEQUEUE_CHK_COMPL`** | `0x0020E6` | `0x002E72` | `device_mgr.s:200`<br>`device_mgr.s:182` | — |
| **`DEQUEUE_DONE`** | `0x0020F6` | `0x002E82` | `device_mgr.s:208`<br>`device_mgr.s:190` | — |
| **`DEQUEUE_INVALIDATE`** | `0x0027FE` | — | `event_mgr.s:196` | DequeueAndInvalidate - remove EvQEl from queue, mark slot free A0 = EvQEl entry to remove, A1 = queue header (EventQueue). After Dequeue, sets evtQWhat to -1 to mark the slot as unused so PostEvent ca... |
| **`DEQUEUE_IOREQ`** | `0x0020C4` | `0x002E50` | `device_mgr.s:188`<br>`device_mgr.s:170` | DEQUEUE_IOREQ - Dequeue completed request and call completion routine A1 = DCE pointer, D0 = result code, D1 = saved SR. Removes the head of the driver's I/O queue (dCtlQHead), stores the result in io... |
| **`DEQUEUE_RESTORE_SR`** | `0x0020DA` | `0x002E66` | `device_mgr.s:195`<br>`device_mgr.s:177` | — |
| **`DerefHandle`** | `0x01045E` | — | `memory_mgr.s:1267` | **Regs:** `Entry: A0 = handle Exit:  A1 = masked handle; A0 = D0 = master pointer contents (0 if the`<br>DerefHandle - mask a handle and fetch its master pointer Entry: A0 = handle Exit:  A1 = masked handle; A0 = D0 = master pointer contents (0 if the handle is nil); Z set if the handle or its master poi... |
| **`DEREFHANDLE_CONT`** | `0x010470` | `0x00A9CA` | `memory_mgr.s:1289`<br>`memory_mgr.s:868` | **Regs:** `Entry: A0 = block data pointer, A1 = handle (nil for a pointer block) Exit:  A0 = masked data pointer; A6 = zone (nonrelocatable: the header's`<br>DEREFHANDLE_CONT - find the zone a block belongs to Entry: A0 = block data pointer, A1 = handle (nil for a pointer block) Exit:  A0 = masked data pointer; A6 = zone (nonrelocatable: the header's zone ... |
| **`DEREFHANDLE_CONT_2`** | `0x010486` | `0x00A9E0` | `memory_mgr.s:1305`<br>`memory_mgr.s:883` | DEREFHANDLE_CONT_2 Called during boot (39,521 times in 30s trace). |
| **`DEREFHANDLE_CONT_3`** | `0x01048C` | `0x00A9E6` | `memory_mgr.s:1308`<br>`memory_mgr.s:886` | — |
| **`DEREFHANDLE_CONT_4`** | `0x010492` | `0x00A9EC` | `memory_mgr.s:1318`<br>`memory_mgr.s:895` | DEREFHANDLE_CONT_4 |
| **`DEREFHANDLE_CONT_5`** | `0x010496` | `0x00A9F0` | `memory_mgr.s:1331`<br>`memory_mgr.s:903` | **Regs:** `Exit: D0 = 0 (N clear) if they match, else memAZErr (-113); A0 preserved.`<br>DEREFHANDLE_CONT_5 - check that A6 points to a valid heap zone Masks A6 to 24 bits and compares it with the zone field in the header of the zone's first block (the master pointer block, a nonrelocatab... |
| **`DEREFHANDLE_EXIT`** | `0x01046E` | `0x00A9C8` | `memory_mgr.s:1275`<br>`memory_mgr.s:861` | — |
| **`DEREFHANDLE_EXIT_2`** | `0x01048E` | `0x00A9E8` | `memory_mgr.s:1310`<br>`memory_mgr.s:888` | — |
| **`DEREFHANDLE_FOUND`** | `0x0104AE` | `0x00AA08` | `memory_mgr.s:1341`<br>`memory_mgr.s:913` | — |
| **`DETECT_DONE`** | `0x002004` | `0x002D88` | `trap_dispatch.s:138`<br>`trap_dispatch.s:127` | — |
| **`DETECT_OS_TABLE`** | `0x002000` | `0x002D84` | `trap_dispatch.s:136`<br>`trap_dispatch.s:125` | — |
| **`DETECT_TRAP_TABLE`** | `0x001FE4` | `0x002D68` | `trap_dispatch.s:126`<br>`trap_dispatch.s:115` | **Regs:** `Entry: D0 = trap number (will be masked to 9 bits) Exit: A1 = correct dispatch table, D0 = masked trap number`<br>DETECT_TRAP_TABLE - Old-style OS/Toolbox auto-detect Pre-System 7 trap API: without the "new" bit, the system must guess whether a trap number belongs to the OS or Toolbox table. Traps $50-$53 and $55... |
| **`DEVIO_COMMON`** | `0x0023D0` | `0x00316E` | `device_mgr.s:625`<br>`device_mgr.s:557` | DEVIO_COMMON - common Read/Write/Control/Status dispatch D0 = default error code, D4 = permission bit to test |
| **`DEVIO_POLL_RESULT`** | `0x002420` | `0x0031BE` | `device_mgr.s:650`<br>`device_mgr.s:583` | Dispatch based on trap word bits 9-10 Synchronous I/O: enqueue, then poll ioResult until complete |
| **`DEVIO_SET_INPROGRESS`** | `0x0023E0` | `0x00317E` | `device_mgr.s:632`<br>`device_mgr.s:563` | Common entry for Read/Write/Control - D0=default error, D4=enable bit |
| **`DEVIO_STORE_RESULT`** | `0x002428` | `0x0031C6` | `device_mgr.s:654`<br>`device_mgr.s:587` | — |
| **`DEVMGR_OPEN_DISP`** | `0x0021D8` | `0x002F66` | `device_mgr.s:359`<br>`device_mgr.s:319` | DEVMGR_OPEN_DISP - Device Manager Open dispatch After looking up the driver, decides whether this is a file open (goes to File Manager) or a device open (returns badUnitErr). |
| **`DIAC_STRIP_TBL`** | — | `0x009CD4` | `os_utilities.s:213` | DIAC_STRIP_TBL (= DIAC_STRIP_TBL): 256-byte diacritical-stripping table indexed by char code. ASCII portion (0x00..0x7F) is identity (case preserved). High-bit chars (0x80..0xFF) collapse accented Mac... |
| **`Dispatch`** | `0x001F4A` | — | `trap_dispatch.s:20` | A-line trap dispatcher -- EMT1010, _GetTrapAddress, _SetTrapAddress Apple source: Dispatch.a (MacSEROM.lst module DSPATCH). The 68000 Line 1010 Emulator exception handler dispatches A-line instruction... |
| **`DISPATCH_NEXT_REQ`** | `0x00210A` | `0x002E96` | `device_mgr.s:225`<br>`device_mgr.s:205` | DISPATCH_NEXT_REQ - try to start next I/O request |
| **`DISPOSE_LOCKED_EMPTY`** | — | `0x00A6A4` | `memory_mgr.s:425` | — |
| **`DISPOSE_RELEASE_MP`** | — | `0x00A69C` | `memory_mgr.s:420` | — |
| **`DISPOSEPTR`** | — | `0x00A60A` | `memory_mgr.s:343` | — |
| **`DisposHandle`** | `0x010170` | — | `memory_mgr.s:694` | **Proto:** `Pascal: PROCEDURE DisposHandle(h: Handle);`<br>**Regs:** `Entry: A0 = h Exit:  D0.W = noErr, memROZErr, memWZErr or memAZErr; MemErr set`<br>_DisposHandle ($A023): release a relocatable block and its master pointer Pascal: PROCEDURE DisposHandle(h: Handle); Entry: A0 = h Exit:  D0.W = noErr, memROZErr, memWZErr or memAZErr; MemErr set Bloc... |
| **`DISPOSHANDLE_CONT`** | `0x010184` | — | `memory_mgr.s:702` | — |
| **`DISPOSHANDLE_EXIT`** | `0x010188` | `0x00A6A0` | `memory_mgr.s:704`<br>`memory_mgr.s:422` | — |
| **`DISPOSHANDLE_ROZONE`** | `0x01018C` | — | `memory_mgr.s:713` | DISPOSHANDLE_ROZONE - DisposHandle: empty handle in a read-only zone; clear the master pointer but do not return it to the free list |
| **`DisposPtr`** | `0x0100F2` | — | `memory_mgr.s:542` | **Proto:** `Pascal: PROCEDURE DisposPtr(p: Ptr);`<br>**Regs:** `Entry: A0 = p Exit:  D0.W = noErr, memROZErr (block in a read-only zone, not freed),`<br>_DisposPtr ($A01F): release a nonrelocatable block Pascal: PROCEDURE DisposPtr(p: Ptr); Entry: A0 = p Exit:  D0.W = noErr, memROZErr (block in a read-only zone, not freed), or memWZErr/memAZErr from M... |
| **`DISPOSPTR_CONT`** | `0x0100F6` | `0x00A60E` | `memory_mgr.s:544`<br>`memory_mgr.s:345` | — |
| **`DISPOSPTR_EXIT`** | `0x010104` | `0x00A61C` | `memory_mgr.s:554`<br>`memory_mgr.s:350` | DISPOSPTR_EXIT - DisposPtr/DisposHandle: block is in a read-only zone |
| **`DISPTABLE`** | — | `0x01AA9C` | `dispatch_table.s:16` | Data table decoded by InitDispatcher. |
| **`DivUp`** | `0x002C50` | `0x004698` | `file_mgr_vol.s:95` | DivUp - unsigned divide D0/D1 with round-up (ceiling division) Returns ceil(D0/D1) in D0.W. Used for allocation block calculations. Called by: RoundAlloc, FlushMDB, MOUNTVOL_CONT_6, MOUNTVOL_FOUND_3, ... |
| **`DIVUP`** | `0x002C50` | `0x004698` | `file_mgr_vol.s:96` | **Regs:** `Entry: D0 = dividend, D1 = divisor Exit: D0 = ceiling quotient`<br>DIVUP - unsigned divide with round-up Returns ceil(D0 / D1). Used for allocation block calculations. Entry: D0 = dividend, D1 = divisor Exit: D0 = ceiling quotient Called by: ROUNDALLOC, FLUSHMDB, MOU... |
| **`DIVUP_EXACT`** | `0x002C60` | `0x0046A8` | `file_mgr_vol.s:109`<br>`file_mgr_vol.s:106` | DIVUP_EXACT - exact division, no rounding needed |
| **`DIVUP_RET`** | `0x002C62` | `0x0046AA` | `file_mgr_vol.s:111`<br>`file_mgr_vol.s:108` | — |
| **`DOEJECT`** | — | `0x004664` | `file_mgr_vol.s:68` | **Regs:** `Entry: D1 = drive number, D2 = volume refNum`<br>File Manager -- common subroutines and volume calls Apple sources, included by TFS.a (MacSEROM.lst module TURBOFS): TFSCommon.a (DOEJECT, DIVUP, ROUNDALLOC, GETVCBRFN, MARKVCB, MARKVCBTIME, FLUSHMDB, ... |
| **`DOPART`** | `0x0050B4` | `0x006B5A` | `file_mgr_io.s:265`<br>`file_mgr_io.s:256` | DOPART Called during boot. DoPart: copy partial block to/from user buffer D0: 0=read, 1=write, $FF=verify-read |
| **`DQCBuf`** | `0x007B84` | `0x0096D8` | `file_mgr_cache.s:755`<br>`file_mgr_cache.s:627` | DQCBuf - DQCBuf: dequeue cache buffer from circular list Called during boot. |
| **`DRAW_ALERT_FRAME`** | `0x001378` | `0x001588` | `sys_error.s:388`<br>`sys_error.s:344` | DRAW_ALERT_FRAME - draw DS alert box frame (double-bordered rectangle) Draws the standard system error alert box: erase, frame, then inset by 3 pixels and draw a thicker (2x2) inner frame. |
| **`DRAW_ALERT_TEXT`** | `0x001300` | `0x001510` | `sys_error.s:307`<br>`sys_error.s:265` | DRAW_ALERT_TEXT - draw text string from alert table entry Reads text ID from A3, looks it up in the alert table, then draws the text at position D3. Text is split on '/' (0x2F) into multiple lines, ad... |
| **`DRAW_BTN_LOOP`** | `0x0013B0` | `0x0015C0` | `sys_error.s:420`<br>`sys_error.s:381` | Draw each button: label text + rounded-rect frame |
| **`DRAW_FRAME_RTS`** | `0x0013A2` | `0x0015B2` | `sys_error.s:404`<br>`sys_error.s:360` | — |
| **`DRAWTEXT_DONE`** | `0x001338` | `0x001548` | `sys_error.s:335`<br>`sys_error.s:295` | — |
| **`DRAWTEXT_SCAN`** | `0x00130C` | `0x00151C` | `sys_error.s:314`<br>`sys_error.s:273` | Scan text for '/' (line separator) or NUL (end of string) |
| **`DRAWTEXT_SEGMENT`** | `0x001316` | `0x001526` | `sys_error.s:319`<br>`sys_error.s:279` | Draw one line segment from A2 to A0-1 |
| **`DRVRINST_ALLOC_NORM`** | `0x0024E2` | — | `device_mgr.s:784` | — |
| **`DRVRINST_BAD_REFNUM`** | `0x002524` | `0x0032C2` | `device_mgr.s:831`<br>`device_mgr.s:719` | DRVRINST_BAD_REFNUM - invalid refNum: return unitEmptyErr (-21) |
| **`DRVRINST_EXIT`** | `0x002502` | — | `device_mgr.s:801` | — |
| **`DRVRINST_RET_NOERR`** | `0x002500` | — | `device_mgr.s:799` | — |
| **`DRVRINST_ZERO_DCE`** | `0x0024E8` | — | `device_mgr.s:788` | — |
| **`DRVRINST_ZERO_LOOP`** | `0x0024EC` | `0x00328A` | `device_mgr.s:792`<br>`device_mgr.s:686` | Zero-fill the 40-byte DCE and install it in the unit table |
| **`DrvrInstall`** | `0x0024CA` | `0x003268` | `device_mgr.s:773` | _DrvrInstall ($A03D) D0 = refNum -> D0 = error Allocates a 40-byte DCE in the system heap and installs it in the unit table. Trap word bit 10 (_DrvrInstallResrvMem variant) reserves memory first. Call... |
| **`DRVRINSTALL`** | `0x0024CA` | `0x003268` | `device_mgr.s:666` | **Regs:** `Entry: D0 = refNum, A0 = driver handle (unused for slot alloc)`<br>DRVRINSTALL - _DrvrInstall trap: allocate DCE for a driver Entry: D0 = refNum, A0 = driver handle (unused for slot alloc) Allocates a 50-byte (0x32) DCE handle in system heap, zeros it, installs in un... |
| **`DRVRINSTALL_DO_ALLOC`** | — | `0x003280` | `device_mgr.s:678` | Slot empty: allocate new DCE handle (50 bytes) |
| **`DRVRINSTALL_OK`** | — | `0x00329E` | `device_mgr.s:693` | — |
| **`DRVRINSTALL_RTS`** | — | `0x0032A0` | `device_mgr.s:695` | — |
| **`DRVRINSTALL_ZERO_DCE`** | — | `0x003286` | `device_mgr.s:683` | Zero-fill DCE and install in unit table |
| **`DrvrRemove`** | `0x002528` | `0x0032C6` | `device_mgr.s:842` | _DrvrRemove ($A03E) D0 = refNum -> D0 = error Removes a closed driver from the unit table and frees its DCE. Cannot remove an open driver (returns dRemovErr -25). |
| **`DRVRREMOVE`** | `0x002528` | `0x0032C6` | `device_mgr.s:727` | **Regs:** `Entry: D0 = refNum`<br>DRVRREMOVE - _DrvrRemove trap: remove a driver from unit table Entry: D0 = refNum Releases driver resource if RAM-based, disposes DCE handle, clears unit table slot. Returns error if driver is still o... |
| **`DRVRREMOVE_DISPOSE`** | — | `0x0032EA` | `device_mgr.s:741` | — |
| **`DRVRREMOVE_FREE_DCE`** | `0x00254C` | — | `device_mgr.s:856` | — |
| **`DRVRREMOVE_STILL_OPEN`** | `0x002554` | `0x0032F2` | `device_mgr.s:866`<br>`device_mgr.s:746` | DRVRREMOVE_STILL_OPEN - driver is still open, cannot remove |
| **`DSERR_BTN_CLICKED`** | `0x0012DC` | — | `sys_error.s:259` | DSERR_BTN_CLICKED - button was clicked, clean up and return via button handler |
| **`DSERR_DISPATCH`** | `0x001278` | — | `sys_error.s:207` | DSERR_DISPATCH - dispatch on error code using alert table |
| **`DSERR_DRAW_ALERT`** | `0x001294` | `0x0014A4` | `sys_error.s:220`<br>`sys_error.s:163` | — |
| **`DSERR_HAS_TABLE`** | — | `0x001488` | `sys_error.s:150` | No DSAT resource loaded: show raw error via boot-time sad Mac |
| **`DSERR_RESTART`** | — | `0x0014EC` | `sys_error.s:197` | — |
| **`DSERR_RESUME`** | `0x0012CC` | `0x0014DC` | `sys_error.s:248`<br>`sys_error.s:191` | — |
| **`DSERR_SETUP_RECT`** | `0x001288` | `0x001498` | `sys_error.s:213`<br>`sys_error.s:156` | — |
| **`DSERR_SHOW_BTNS`** | `0x0012C6` | `0x0014D6` | `sys_error.s:245`<br>`sys_error.s:188` | — |
| **`DSERR_SKIP_ICON`** | `0x0012B0` | `0x0014C0` | `sys_error.s:233`<br>`sys_error.s:176` | — |
| **`DSERR_SKIP_PROC`** | `0x0012BA` | `0x0014CA` | `sys_error.s:239`<br>`sys_error.s:182` | — |
| **`DSErrorHandler`** | `0x001234` | `0x001442` | `sys_error.s:181` | DSErrorHandler - system error alert display Creates a temporary GrafPort on the stack, initializes QuickDraw, and displays the system error dialog using the alert table pointed to by DSAlertTab. If no... |
| **`DSERRORHANDLER`** | `0x001234` | `0x001442` | `sys_error.s:127` | DSERRORHANDLER - built-in DS alert (system error dialog) Draws the system error alert box with error text, Restart and Resume buttons. Uses QuickDraw for rendering. D0 = error code on entry. |
| **`DSHook`** | `0x002A86` | `0x0044C8` | `file_mgr_queue.s:317` | DSHook - disk-switch hook, handles "please insert disk" dialog Called when a volume is needed but not mounted. Saves state, shows the disk-switch alert (dsErrCode=30), and polls for disk-insert events... |
| **`DSHOOK`** | `0x002A86` | `0x0044C8` | `file_mgr_queue.s:335` | DSHOOK -- Disk-Switch Hook Posts the "Please insert the disk:" dialog when an FS call hits nsDrvErr (-43) and the requested volume can't be found online. First tries to silently re-mount via _MountVol... |
| **`DSHOOK_CALL_KBDTASK`** | — | `0x0045DA` | `file_mgr_queue.s:459` | — |
| **`DSHOOK_CHK_CMDPER`** | `0x002B9E` | `0x0045E6` | `file_mgr_queue.s:442`<br>`file_mgr_queue.s:465` | DSHOOK_CHK_CMDPER - check for Cmd-. (cancel disk-switch) |
| **`DSHOOK_CLEANUP`** | `0x002BE8` | `0x004630` | `file_mgr_queue.s:487`<br>`file_mgr_queue.s:508` | — |
| **`DSHOOK_DISK_INSERT`** | `0x002BA6` | `0x0045EE` | `file_mgr_queue.s:451`<br>`file_mgr_queue.s:473` | DSHOOK_DISK_INSERT - disk inserted, try to mount it |
| **`DSHOOK_DISMISS`** | `0x002BBA` | `0x004602` | `file_mgr_queue.s:460`<br>`file_mgr_queue.s:482` | — |
| **`DSHOOK_DO_EJECT`** | `0x002B54` | `0x004596` | `file_mgr_queue.s:406`<br>`file_mgr_queue.s:421` | — |
| **`DSHOOK_EJECT_DRV`** | `0x002B52` | `0x004594` | `file_mgr_queue.s:404`<br>`file_mgr_queue.s:419` | — |
| **`DSHOOK_EVT_LOOP`** | `0x002B5A` | `0x00459C` | `file_mgr_queue.s:409`<br>`file_mgr_queue.s:433` | DSHOOK_EVT_LOOP / DSHOOK_POLL_EVT -- main wait loop Mask 0x88 = diskEvt (bit 7) \| keyDownEvt (bit 3). Polls until either a disk insertion (sysEvt code 7) or a Cmd-period (key 0x2E with cmdKey modifier... |
| **`DSHOOK_FIX_ALINE`** | `0x002C08` | `0x004650` | `file_mgr_queue.s:511`<br>`file_mgr_queue.s:531` | DSHOOK_FIX_ALINE - convert trap number to A-line instruction and re-execute |
| **`DSHOOK_FOUND_DRV`** | `0x002B42` | `0x004584` | `file_mgr_queue.s:398`<br>`file_mgr_queue.s:413` | DSHOOK_FOUND_DRV - found drive in queue, eject if it's a floppy (type 1 or 2) |
| **`DSHOOK_NO_PORT`** | `0x002BDC` | `0x004624` | `file_mgr_queue.s:480`<br>`file_mgr_queue.s:501` | DSHOOK_NO_PORT - no temp port: flag windows need updating |
| **`DSHOOK_POLL_EVT`** | `0x002B5E` | `0x0045A0` | `file_mgr_queue.s:411`<br>`file_mgr_queue.s:435` | — |
| **`DSHOOK_RETRY_TRAP`** | `0x002BFE` | `0x004646` | `file_mgr_queue.s:502`<br>`file_mgr_queue.s:522` | DSHOOK_RETRY_TRAP - disk-switch succeeded, re-execute the original FS call The ioTrap word was saved in TrapAgain earlier. We jump to it to re-execute the trap that originally caused the disk-switch. |
| **`DSHOOK_SCAN_DRV`** | `0x002B34` | `0x004576` | `file_mgr_queue.s:386`<br>`file_mgr_queue.s:402` | Walk the drive queue looking for the failed drive (drvNum in D3). |
| **`DSHOOK_SETPORT`** | `0x002BE4` | `0x00462C` | `file_mgr_queue.s:484`<br>`file_mgr_queue.s:505` | — |
| **`DSHOOK_SHOW_DLG`** | `0x002AB6` | `0x0044F8` | `file_mgr_queue.s:341`<br>`file_mgr_queue.s:358` | DSHOOK_SHOW_DLG - set up and show the disk-switch dialog Sets up the alert rectangle, optionally creates a temporary QD port to save/restore screen contents behind the dialog, then calls _SysError wit... |
| **`DSHOOK_SYSERROR`** | `0x002B2C` | `0x00456E` | `file_mgr_queue.s:382`<br>`file_mgr_queue.s:397` | — |
| **`DSPATCH`** | — | `0x002CB6` | `trap_dispatch.s:19` | A-line trap dispatcher -- ATRAP68020/68010, EMT1010, _SetTrapAddress, _GetTrapAddress Apple source: Dispatch.a (MacSEROM.lst module DSPATCH). Dispatches A-line instructions ($Axxx) to the OS or Toolbo... |
| **`DSPOSEHANDLE`** | — | `0x00A688` | `memory_mgr.s:412` | — |
| **`DSPTABLE`** | — | `0x01AA9C` | `dispatch_table.s:13` | Compressed trap dispatch table Apple source: DispTable.a (MacSEROM.lst modules RESTOP and DSPTABLE). Read once at startup by INITDISPATCHER (boot_install.s), which fills the Toolbox dispatch table (51... |
| **`DT_INF_RGN`** | — | `0x00141A` | `sys_error.s:99` | DT_INF_RGN - infinite bounding region (10 bytes) rgnSize=10, rgnBBox = (-32767,-32767,32767,32767) |
| **`DT_mFSIODNETbl`** | `0x002030` | — | `device_mgr.s:70` | Device Manager Handles communication between applications and device drivers. High-level: OpenDriver, CloseDriver, FSRead, FSWrite, Control, Status, KillIO Low-level: PBOpen, PBClose, PBRead, PBWrite,... |
| **`DTRMV1`** | `0x003656` | — | `file_mgr_vol.s:1370` | DTRMV1 Called during boot. DTRMV1: determine volume from ioVRefNum (no filename) |
| **`DTRMV1_CONT`** | `0x003668` | `0x0050FA` | `file_mgr_vol.s:1379`<br>`file_mgr_vol.s:1276` | negative reference: VRefNum or WDCB |
| **`DTRMV1_CONT_10`** | `0x0037F2` | `0x005280` | `file_mgr_vol.s:1607`<br>`file_mgr_vol.s:1485` | — |
| **`DTRMV1_CONT_2`** | `0x003678` | `0x00510A` | `file_mgr_vol.s:1387`<br>`file_mgr_vol.s:1283` | — |
| **`DTRMV1_CONT_3`** | `0x0036E6` | `0x005178` | `file_mgr_vol.s:1452`<br>`file_mgr_vol.s:1343` | DTRMV1_CONT_3: HFS InitFS patch table processing (build param block entries) |
| **`DTRMV1_CONT_4`** | `0x003756` | `0x0051E8` | `file_mgr_vol.s:1503`<br>`file_mgr_vol.s:1393` | DTRMV1_CONT_4 Called during boot. |
| **`DTRMV1_CONT_5`** | `0x00375A` | `0x0051EC` | `file_mgr_vol.s:1506`<br>`file_mgr_vol.s:1396` | — |
| **`DTRMV1_CONT_6`** | `0x003772` | `0x005204` | `file_mgr_vol.s:1519`<br>`file_mgr_vol.s:1409` | — |
| **`DTRMV1_CONT_7`** | `0x003788` | `0x00521A` | `file_mgr_vol.s:1538`<br>`file_mgr_vol.s:1421` | DTRMV1_CONT_7: parse pathname into volume name and file name components D2 = ptr to pathname string, returns A4=filename, D2=name length, A3=vol prefix |
| **`DTRMV1_CONT_8`** | `0x0037C4` | `0x005252` | `file_mgr_vol.s:1572`<br>`file_mgr_vol.s:1452` | no volume name: resolve by ioVRefNum only |
| **`DTRMV1_CONT_9`** | `0x0037D4` | `0x005262` | `file_mgr_vol.s:1592`<br>`file_mgr_vol.s:1470` | — |
| **`DTRMV1_EMPTY`** | `0x00367E` | `0x005110` | `file_mgr_vol.s:1399`<br>`file_mgr_vol.s:1294` | DTRMV1_EMPTY Called during boot. use default volume |
| **`DTRMV1_EMPTY_2`** | `0x0037CC` | `0x00525A` | `file_mgr_vol.s:1581`<br>`file_mgr_vol.s:1460` | DTRMV1_EMPTY_2 |
| **`DTRMV1_ERR`** | `0x0036A2` | `0x005134` | `file_mgr_vol.s:1412`<br>`file_mgr_vol.s:1307` | — |
| **`DTRMV1_ERR_2`** | `0x0036B4` | `0x005146` | `file_mgr_vol.s:1421`<br>`file_mgr_vol.s:1316` | — |
| **`DTRMV1_ERR_3`** | `0x00370C` | `0x00519E` | `file_mgr_vol.s:1467`<br>`file_mgr_vol.s:1357` | check if boot volume has a default directory |
| **`DTRMV1_ERR_4`** | `0x00376A` | `0x0051FC` | `file_mgr_vol.s:1513`<br>`file_mgr_vol.s:1403` | — |
| **`DTRMV1_FOUND`** | `0x00368C` | `0x00511E` | `file_mgr_vol.s:1405`<br>`file_mgr_vol.s:1300` | — |
| **`DTRMV1_FOUND_2`** | `0x003750` | `0x0051E2` | `file_mgr_vol.s:1494`<br>`file_mgr_vol.s:1383` | — |
| **`DTRMV1_FOUND_3`** | `0x0037AE` | `0x005240` | `file_mgr_vol.s:1562`<br>`file_mgr_vol.s:1441` | DTRMV1_FOUND_3 |
| **`DTRMV1_FOUND_4`** | `0x0037C0` | — | `file_mgr_vol.s:1570` | — |
| **`DTRMV1_FOUND_5`** | `0x0037EE` | `0x00527C` | `file_mgr_vol.s:1604`<br>`file_mgr_vol.s:1482` | — |
| **`DTRMV1_LOOP`** | `0x0036AC` | `0x00513E` | `file_mgr_vol.s:1417`<br>`file_mgr_vol.s:1312` | — |
| **`DTRMV1_NO`** | `0x00367A` | `0x00510C` | `file_mgr_vol.s:1389`<br>`file_mgr_vol.s:1285` | — |
| **`DTRMV1_NO_2`** | `0x0036E4` | `0x005176` | `file_mgr_vol.s:1449`<br>`file_mgr_vol.s:1341` | first call: build PMSP table from current volume/directory no WDCB: use root directory |
| **`DTRMV1_NO_3`** | `0x003718` | `0x0051AA` | `file_mgr_vol.s:1473`<br>`file_mgr_vol.s:1363` | terminate the param block table |
| **`DTRMV1_NO_4`** | `0x003784` | `0x005216` | `file_mgr_vol.s:1534`<br>`file_mgr_vol.s:1419` | DTRMV1_NO_4 Called during boot. |
| **`DTRMV1_NO_5`** | `0x00379C` | `0x00522E` | `file_mgr_vol.s:1549`<br>`file_mgr_vol.s:1432` | scan for colon separator |
| **`DTRMV1_OK`** | `0x003674` | — | `file_mgr_vol.s:1385` | working directory reference |
| **`DTRMV1_OK_2`** | `0x0036B8` | `0x00514A` | `file_mgr_vol.s:1430`<br>`file_mgr_vol.s:1324` | DTRMV1_OK_2 Called during boot. |
| **`DTRMV1_OK_3`** | `0x0036C6` | `0x005158` | `file_mgr_vol.s:1436`<br>`file_mgr_vol.s:1330` | DTRMV1_OK_3: HFS InitFS - build param block table for PMSP (Param Manager) |
| **`DTRMV1_OK_4`** | `0x00372C` | `0x0051BE` | `file_mgr_vol.s:1483`<br>`file_mgr_vol.s:1372` | call the dispatch vector if set set up default WDCB from result |
| **`DTRMV1_OK_5`** | `0x003770` | `0x005202` | `file_mgr_vol.s:1517`<br>`file_mgr_vol.s:1407` | — |
| **`DTRMV1_OK_6`** | `0x003782` | `0x005214` | `file_mgr_vol.s:1526`<br>`file_mgr_vol.s:1416` | — |
| **`DTRMV1_OK_7`** | `0x0037D0` | `0x00525E` | `file_mgr_vol.s:1590`<br>`file_mgr_vol.s:1468` | DTRMV1_OK_7 scan VCB queue for volume by name |
| **`DTRMV1_TRY_WD`** | — | `0x005106` | `file_mgr_vol.s:1281` | — |
| **`DTRMV3`** | `0x003642` | — | `file_mgr_vol.s:1352` | DTRMV3: determine volume from param block (with filename check) Called during boot. |
| **`DTRMV3_REFNUM_ONLY`** | — | `0x00524E` | `file_mgr_vol.s:1450` | no volume name: resolve by ioVRefNum only |
| **`E_1056_LOOP_LOOP_3`** | — | `0x003A02` | `adb_mgr.s:743` | — |
| **`EH`** | `0x010522` | `0x00AAD8` | `memory_mgr.s:1483`<br>`memory_mgr.s:1019` | **Regs:** `Entry: A0 = data pointer, A1 = handle, A6 = zone Exit:  D0 = noErr, or memPurErr (-112) if the block is locked`<br>EH - empty a handle: purge its block Entry: A0 = data pointer, A1 = handle, A6 = zone Exit:  D0 = noErr, or memPurErr (-112) if the block is locked In a read-only zone only the master pointer is clear... |
| **`EH_CONT`** | `0x010542` | `0x00AAF8` | `memory_mgr.s:1518`<br>`memory_mgr.s:1050` | EH_CONT - call the zone's purge-warning proc (purgeProc) for handle A1 Apple source name: CallPurgeProc (System 7.1 MemoryMgrInternal.a) Called during boot. |
| **`EH_CONT_2`** | `0x01055A` | `0x00AB10` | `memory_mgr.s:1537`<br>`memory_mgr.s:1065` | **Regs:** `Entry: A0 = block header, A1 = handle, A6 = zone`<br>EH_CONT_2 - purge a block: purge warning, master pointer := nil, free it Entry: A0 = block header, A1 = handle, A6 = zone Called by EH, PurgeHeap and MAKEPTRSPC_CONT_2. Apple source name: PurgeBlock (... |
| **`EH_EXIT`** | `0x010536` | `0x00AAEC` | `memory_mgr.s:1491`<br>`memory_mgr.s:1027` | — |
| **`EH_EXIT_2`** | `0x010538` | `0x00AAEE` | `memory_mgr.s:1493`<br>`memory_mgr.s:1029` | — |
| **`EH_EXIT_3`** | `0x01053A` | `0x00AAF0` | `memory_mgr.s:1500`<br>`memory_mgr.s:1035` | EH_EXIT_3 |
| **`EH_EXIT_4`** | `0x010558` | `0x00AB0E` | `memory_mgr.s:1526`<br>`memory_mgr.s:1058` | — |
| **`EH_OK`** | `0x01053E` | `0x00AAF4` | `memory_mgr.s:1508`<br>`memory_mgr.s:1042` | EH_OK |
| **`Eject`** | `0x0034E0` | `0x004F66` | `file_mgr_vol.s:1151` | _Eject ($A017) _Eject ($A017) |
| **`EJECT`** | `0x0034E0` | `0x004F66` | `file_mgr_vol.s:1079` | _Eject: eject disk and take volume offline |
| **`EJECT_CONT`** | `0x0034E4` | — | `file_mgr_vol.s:1153` | — |
| **`EJECT_CONT_2`** | `0x0034FA` | `0x004F80` | `file_mgr_vol.s:1167`<br>`file_mgr_vol.s:1095` | — |
| **`EJECT_CONT_3`** | `0x003570` | `0x004FF6` | `file_mgr_vol.s:1224`<br>`file_mgr_vol.s:1148` | mark volume as offline |
| **`EJECT_DONE`** | `0x003508` | `0x004F8E` | `file_mgr_vol.s:1172`<br>`file_mgr_vol.s:1101` | Called by: EJECT_FOUND_2, EJECT_OFFLINE_JOIN, EJECT_CONT_2, EJECT_OK, EJECT_NO_2 |
| **`EJECT_FOUND`** | `0x0034F6` | `0x004F7C` | `file_mgr_vol.s:1165`<br>`file_mgr_vol.s:1093` | EJECT_FOUND |
| **`EJECT_FOUND_2`** | `0x00350C` | `0x004F92` | `file_mgr_vol.s:1180`<br>`file_mgr_vol.s:1108` | EJECT_FOUND_2 volume found: get drive number from VCB |
| **`EJECT_MFS_PATH`** | — | `0x004FEA` | `file_mgr_vol.s:1143` | — |
| **`EJECT_NO`** | `0x003564` | — | `file_mgr_vol.s:1219` | MFS flush/offline |
| **`EJECT_NO_2`** | `0x00357A` | `0x005000` | `file_mgr_vol.s:1229`<br>`file_mgr_vol.s:1153` | — |
| **`EJECT_NO_3`** | `0x003598` | `0x00501E` | `file_mgr_vol.s:1241`<br>`file_mgr_vol.s:1164` | if offline only, dequeue and re-enqueue VCB (move to end of queue) EJECT_NO_3: send eject/offline control call to disk driver |
| **`EJECT_OFFLINE_JOIN`** | — | `0x004F6A` | `file_mgr_vol.s:1081` | — |
| **`EJECT_OK`** | `0x003528` | `0x004FAE` | `file_mgr_vol.s:1197`<br>`file_mgr_vol.s:1124` | EJECT_OK volume is online: check drive type and flush |
| **`EJECT_OK_2`** | `0x00354E` | `0x004FD4` | `file_mgr_vol.s:1210`<br>`file_mgr_vol.s:1135` | determine eject behavior based on drive type flush all open files for this volume |
| **`EmptyHandle`** | `0x0101DC` | `0x00A6F4` | `memory_mgr.s:806` | _EmptyHandle ($A02B) A0 = handle -> (master ptr set to NIL) Called during boot. |
| **`EMPTYHANDLE`** | `0x0101DC` | `0x00A6F4` | `memory_mgr.s:468` | — |
| **`EMPTYHANDLE_CONT`** | `0x0101E6` | — | `memory_mgr.s:817` | EMPTYHANDLE_CONT Called during boot. |
| **`EMPTYHANDLE_DO`** | — | `0x00A6FE` | `memory_mgr.s:473` | — |
| **`EMPTYHANDLE_EXIT`** | `0x0101EA` | `0x00A702` | `memory_mgr.s:819`<br>`memory_mgr.s:475` | — |
| **`EMT1010`** | — | `0x002CD6` | `trap_dispatch.s:34` | EMT1010 - 1010 emulator trap entry (F-line) |
| **`EMT1010_TrapDispatch`** | `0x001F52` | — | `trap_dispatch.s:30` | EMT1010 - 68000 Line 1010 Emulator (trap dispatcher) 68000 A-line exception pushes SR (word) + PC (long) onto stack. This is the main entry point for all A-line trap dispatch. |
| **`ENQ_APPEND_TAIL`** | `0x0019DE` | `0x002ACA` | `queue.s:44`<br>`queue.s:40` | ENQ_APPEND_TAIL - queue not empty: link new element after current tail |
| **`ENQ_DONE`** | `0x0019EA` | `0x002AD6` | `queue.s:51`<br>`queue.s:47` | — |
| **`Enqueue`** | `0x0019CA` | `0x002AB6` | `queue.s:29` | OS Queue Primitives -- Enqueue / Dequeue / InitQueuePrim Three core list-manipulation routines used by the Device Manager (I/O queue), Event Manager (event queue), and VBL task manager. Routines: Enqu... |
| **`ENQUEUE`** | `0x0019CA` | `0x002AB6` | `queue.s:29` | OS Queue Primitives -- Enqueue / Dequeue / InitQueuePrim Three core list-manipulation routines used by the Device Manager (I/O queue), Event Manager (event queue), and VBL task manager. Routines: Enqu... |
| **`ENQUEUE_IOREQ`** | `0x0020F8` | `0x002E84` | `device_mgr.s:218`<br>`device_mgr.s:197` | ENQUEUE_IOREQ - Enqueue an I/O request into a driver's queue A1 = DCE pointer, A0 = IOParam block to enqueue. Enqueues the request at dCtlQueue (offset 6 in DCE), then attempts to start it if driver i... |
| **`EVENTS`** | — | `0x003EE6` | `event_mgr.s:27` | **Regs:** `Entry: A0 = event code (mouseDown=1, mouseUp=2, keyDown=3, etc.)`<br>Operating System Event Manager -- _PostEvent, _OSEventAvail, _GetOSEvent, _FlushEvents Apple source: OSEventMgr.a (MacSEROM.lst module EVENTS). The event queue (EventQueue) is kept in a fixed circular... |
| **`ExitToShell`** | `0x00F6D8` | `0x009B24` | `segment_loader.s:348` | initialize app A5 globals area set heap limit (stack reserve) clear all data registers for clean app entry set address registers to safe "odd" values (trap on dereference) _ExitToShell ($A9F4): quit c... |
| **`EXITTOSHELL`** | `0x00F6D8` | `0x009B24` | `segment_loader.s:281` | — |
| **`EXITTOSHELL_ERR`** | `0x00F70A` | `0x009B54` | `segment_loader.s:376`<br>`segment_loader.s:306` | launch Finder EXITTOSHELL_ERR Launch failed: dsFinderErr (error 26) |
| **`EXITTOSHELL_LOOP`** | `0x00F6E4` | `0x009B30` | `segment_loader.s:356`<br>`segment_loader.s:288` | build SetVol param block to restore boot volume |
| **`EXTBT_ADDMAP`** | `0x006F36` | — | `file_mgr_btree.s:1120` | EXTBT_ADDMAP EFAddMap: must extend the map |
| **`EXTBT_CALRANGE`** | `0x006F00` | `0x0089C0` | `file_mgr_btree.s:1091`<br>`file_mgr_btree.s:934` | extend the BTree file space (data fork) EFCalRange: calculate node number range for new space |
| **`EXTBT_EXIT`** | `0x006FAA` | `0x008A72` | `file_mgr_btree.s:1167`<br>`file_mgr_btree.s:1009` | EFExit |
| **`EXTBT_GETMAP`** | `0x006F1E` | — | `file_mgr_btree.s:1104` | locate map positions for beginning and end of new space |
| **`EXTBT_INITMAP`** | — | `0x008A14` | `file_mgr_btree.s:974` | mark new map node as allocated in current map |
| **`EXTBT_MARKDIRTY`** | — | `0x008A54` | `file_mgr_btree.s:996` | EFInitMap: create new map node |
| **`EXTBT_MARKMAP`** | — | `0x0089F4` | `file_mgr_btree.s:958` | EFMarkMap: mark map node in existing map, then create new map node |
| **`EXTBT_MARKNEW`** | `0x006F94` | — | `file_mgr_btree.s:1156` | EFNewMap: initialize a new map node |
| **`EXTBT_MARKOLD`** | `0x006F56` | — | `file_mgr_btree.s:1135` | — |
| **`EXTBT_SCANMAP`** | — | `0x0089DE` | `file_mgr_btree.s:947` | EFScanMap: find map record covering new nodes |
| **`EXTBT_UPDFREE`** | `0x006F9A` | `0x008A5A` | `file_mgr_btree.s:1160`<br>`file_mgr_btree.s:1000` | EFUpdFree: update free node count |
| **`ExtBTFile`** | `0x006ED4` | `0x00898E` | `file_mgr_btree.s:1075` | Ext BT File |
| **`EXTBTFILE`** | `0x006ED4` | `0x00898E` | `file_mgr_btree.s:916` | — |
| **`ExtendFile`** | `0x005B82` | `0x007624` | `file_mgr_alloc.s:524` | Extend File ExtendFile: extend the disk space allocated to a file |
| **`EXTENDFILE`** | `0x005B82` | `0x007624` | `file_mgr_alloc.s:442` | — |
| **`EXTENDFILE_CONT`** | `0x005BC8` | `0x00768A` | `file_mgr_alloc.s:550`<br>`file_mgr_alloc.s:478` | round # of bytes requested up to next alloc blk EFLocExt: locate extent mapping new PEOF - 1 (last byte) |
| **`EXTENDFILE_CONT_2`** | `0x005BF4` | `0x0076B6` | `file_mgr_alloc.s:567`<br>`file_mgr_alloc.s:494` | — |
| **`EXTENDFILE_CONT_3`** | `0x005C1C` | `0x0076DE` | `file_mgr_alloc.s:581`<br>`file_mgr_alloc.s:508` | EFExtExt: see if current extent can be extended |
| **`EXTENDFILE_CONT_4`** | `0x005C3C` | `0x0076FE` | `file_mgr_alloc.s:602`<br>`file_mgr_alloc.s:527` | EFUpdExt: update the extent record |
| **`EXTENDFILE_CONT_5`** | `0x005CA8` | `0x00776A` | `file_mgr_alloc.s:652`<br>`file_mgr_alloc.s:574` | EFUpdFCB: update FCB and see if more space is needed |
| **`EXTENDFILE_DONE`** | `0x005CC2` | `0x007784` | `file_mgr_alloc.s:661`<br>`file_mgr_alloc.s:582` | EFExit |
| **`EXTENDFILE_ERR`** | `0x005CC8` | `0x00778A` | `file_mgr_alloc.s:664`<br>`file_mgr_alloc.s:586` | Called by: EXTENDFILE_CONT_2, VEXTENDFILE, EXTENDFILE_CONT, EXTENDFILE_CONT_4, EXTENDFILE_OK_2 (and 1 more) |
| **`EXTENDFILE_FORCED_CONTIG`** | — | `0x007662` | `file_mgr_alloc.s:464` | — |
| **`EXTENDFILE_LOOP`** | `0x005C7E` | `0x007740` | `file_mgr_alloc.s:636`<br>`file_mgr_alloc.s:558` | clear new extent record |
| **`EXTENDFILE_NO`** | `0x005B98` | — | `file_mgr_alloc.s:532` | — |
| **`EXTENDFILE_NO_2`** | `0x005C26` | `0x0076E8` | `file_mgr_alloc.s:592`<br>`file_mgr_alloc.s:518` | EXTENDFILE_NO_2 EFAddExt: add a new extent entry |
| **`EXTENDFILE_NO_3`** | `0x005C58` | `0x00771A` | `file_mgr_alloc.s:625`<br>`file_mgr_alloc.s:548` | EXTENDFILE_NO_3 |
| **`EXTENDFILE_OK`** | `0x005C34` | `0x0076F6` | `file_mgr_alloc.s:598`<br>`file_mgr_alloc.s:524` | — |
| **`EXTENDFILE_OK_2`** | `0x005C4A` | `0x00770C` | `file_mgr_alloc.s:614`<br>`file_mgr_alloc.s:538` | EXTENDFILE_OK_2 EFNewRec: add a new extent record |
| **`EXTENDFILE_RETRY`** | `0x005BEC` | `0x0076AE` | `file_mgr_alloc.s:564`<br>`file_mgr_alloc.s:491` | adjust PEOF to end of extent EFAddSpace: allocate additional disk space |
| **`EXTENDFILE_TRY_CONTIG`** | — | `0x007654` | `file_mgr_alloc.s:459` | — |
| **`FDBSHIFTINT`** | — | `0x003588` | `adb_mgr.s:317` | FDBSHIFTINT - VIA shift register interrupt handler (ADB protocol) Called when the PIC microcontroller clocks a byte via CB1/CB2. This is the core ADB state machine that manages byte-level transactions... |
| **`Fetch`** | `0x002036` | `0x002DBA` | `device_mgr.s:81` | Fetch - read a byte from the driver's I/O buffer Called via JFetch vector ($08F4). Used by serial drivers and others to read one byte from the active I/O request's buffer. A1 = DCE pointer. Returns by... |
| **`FETCH`** | `0x002036` | `0x002DBA` | `device_mgr.s:79` | **Regs:** `Entry: D0 bit 15 = 0 (fetch mode) Exit: D0 = byte read (bit 15 set if buffer exhausted)`<br>FETCH - read next byte from serial input buffer (SCC driver) Entry: D0 bit 15 = 0 (fetch mode) A1 = DCE pointer -> dCtlQHead -> serial buffer Exit: D0 = byte read (bit 15 set if buffer exhausted) |
| **`FETCH_STASH_ADVANCE`** | `0x00205E` | `0x002DE2` | `device_mgr.s:101`<br>`device_mgr.s:95` | Stash continuation - write byte to buffer |
| **`FETCH_STASH_COMMON`** | `0x00203A` | `0x002DBE` | `device_mgr.s:83`<br>`device_mgr.s:81` | — |
| **`FETCH_STASH_EXIT`** | `0x00206E` | `0x002DF2` | `device_mgr.s:107`<br>`device_mgr.s:101` | — |
| **`FETCH_STASH_WRITE`** | `0x00205A` | `0x002DDE` | `device_mgr.s:99`<br>`device_mgr.s:93` | Stash continuation - write byte to buffer |
| **`FILEALLOC`** | — | `0x006F48` | `file_mgr_io.s:707` | — |
| **`FileClose`** | `0x00514E` | `0x006BF4` | `file_mgr_io.s:376` | FileClose |
| **`FILECLOSE`** | `0x00514E` | `0x006BF4` | `file_mgr_io.s:356` | — |
| **`FILECLOSE_BEGIN`** | — | `0x006BFC` | `file_mgr_io.s:359` | — |
| **`FILECLOSE_BT_FLUSH`** | — | `0x006C3E` | `file_mgr_io.s:384` | — |
| **`FILECLOSE_CONT`** | `0x005156` | — | `file_mgr_io.s:379` | — |
| **`FILECLOSE_CONT_2`** | `0x005162` | `0x006C08` | `file_mgr_io.s:384`<br>`file_mgr_io.s:364` | — |
| **`FILECLOSE_CONT_3`** | `0x005168` | `0x006C0E` | `file_mgr_io.s:395`<br>`file_mgr_io.s:368` | FILECLOSE_CONT_3 Called during boot. FClose: do the actual flush/close for TFS files |
| **`FILECLOSE_CONT_4`** | `0x00518E` | — | `file_mgr_io.s:415` | — |
| **`FILECLOSE_CONT_5`** | `0x005304` | — | `file_mgr_io.s:566` | find the file's MFS directory entry |
| **`FILECLOSE_CONT_6`** | `0x005326` | `0x006DD8` | `file_mgr_io.s:594`<br>`file_mgr_io.s:536` | FILECLOSE_CONT_6 Called during boot. FILECLOSE_CONT_6/UpdFlNtry: update file lengths in catalog from FCB A3 = ptr to file length fields in catalog, (A1,D1) = FCB |
| **`FILECLOSE_CONT_7`** | `0x005336` | `0x006DE8` | `file_mgr_io.s:601`<br>`file_mgr_io.s:543` | — |
| **`FILECLOSE_DONE`** | `0x0052A8` | `0x006D5A` | `file_mgr_io.s:518`<br>`file_mgr_io.s:476` | Called by: FILECLOSE_NO_2, FILECLOSE_NO, FILECLOSE_NO_3, FILECLOSE_OK_4 |
| **`FILECLOSE_ERR`** | `0x005164` | `0x006C0A` | `file_mgr_io.s:386`<br>`file_mgr_io.s:366` | — |
| **`FILECLOSE_ERR_2`** | `0x0052A4` | `0x006D56` | `file_mgr_io.s:516`<br>`file_mgr_io.s:473` | update file info in catalog record if resource fork with LEOF >= 128, update rsrc fork block 0 in volume cache read resource fork block 0 from volume cache and update it copy catalog info into resourc... |
| **`FILECLOSE_ERR_3`** | `0x0052AA` | `0x006D5C` | `file_mgr_io.s:521`<br>`file_mgr_io.s:479` | FClose exit: flush volume cache for this file |
| **`FILECLOSE_ERR_4`** | `0x0052E2` | `0x006D94` | `file_mgr_io.s:545`<br>`file_mgr_io.s:503` | — |
| **`FILECLOSE_LOOP`** | `0x0052DC` | `0x006D8E` | `file_mgr_io.s:542`<br>`file_mgr_io.s:500` | — |
| **`FILECLOSE_MFS_DIR_LOOP`** | — | `0x006DB6` | `file_mgr_io.s:516` | — |
| **`FILECLOSE_NO`** | `0x005192` | `0x006C42` | `file_mgr_io.s:418`<br>`file_mgr_io.s:386` | FClose TFS path: flush/close a single TFS file |
| **`FILECLOSE_NO_2`** | `0x00521C` | `0x006CCE` | `file_mgr_io.s:465`<br>`file_mgr_io.s:427` | copy FCB extent record back to catalog |
| **`FILECLOSE_NO_3`** | `0x0052EC` | `0x006D9E` | `file_mgr_io.s:557`<br>`file_mgr_io.s:508` | FILECLOSE_NO_3 Called during boot. MFS FClose path |
| **`FILECLOSE_OK`** | `0x00518A` | `0x006C3A` | `file_mgr_io.s:413`<br>`file_mgr_io.s:382` | check if file has a B-tree open FILECLOSE_OK |
| **`FILECLOSE_OK_2`** | `0x0052BA` | `0x006D6C` | `file_mgr_io.s:528`<br>`file_mgr_io.s:486` | — |
| **`FILECLOSE_OK_3`** | `0x0052CC` | `0x006D7E` | `file_mgr_io.s:534`<br>`file_mgr_io.s:492` | — |
| **`FILECLOSE_OK_4`** | `0x005314` | `0x006DC6` | `file_mgr_io.s:580`<br>`file_mgr_io.s:523` | FILECLOSE_OK_4 Called during boot. MFS FClose: update directory entry from FCB data |
| **`FILECLOSE_SKIP`** | `0x0051E4` | — | `file_mgr_io.s:445` | check if FCB is dirty FCB was dirty: check if we should/can flush truncate to clump-rounded PEOF on close |
| **`FILECLOSE_SKIP_2`** | `0x0052D0` | `0x006D82` | `file_mgr_io.s:537`<br>`file_mgr_io.s:495` | if closing (not just flushing), clear the FCB |
| **`FILECLOSE_TRUNCATE`** | — | `0x006C8E` | `file_mgr_io.s:407` | — |
| **`FILECREATE`** | — | `0x005C7C` | `file_mgr_dir.s:256` | — |
| **`FILEDELETE`** | — | `0x005EA6` | `file_mgr_dir.s:577` | — |
| **`FileFileTFSetCatInfo_hfs`** | `0x004908` | — | `file_mgr_dir.s:1275` | copy Finder info from param block to catalog record File File TF Set Cat Info_hfs _SetCatInfo (HFS): set file or directory info |
| **`FILEFILETFSETCATINFO_HFS_CONT`** | `0x004974` | `0x00641A` | `file_mgr_dir.s:1302`<br>`file_mgr_dir.s:1168` | — |
| **`FILEFILETFSETCATINFO_HFS_CONT_2`** | `0x00497A` | `0x006420` | `file_mgr_dir.s:1312`<br>`file_mgr_dir.s:1174` | FILEFILETFSETCATINFO_HFS_CONT_2: find file and check write protect (shared by Set calls) Called by: Delete, SETFILTYPE_NO, RSTFILLOCK_CONT, SetFileInfo, FileFileTFSetCatInfo_hfs |
| **`FILEFILETFSETCATINFO_HFS_ERR`** | `0x004976` | `0x00641C` | `file_mgr_dir.s:1304`<br>`file_mgr_dir.s:1170` | — |
| **`FILEFILETFSETCATINFO_HFS_ERR_2`** | `0x00498A` | `0x006430` | `file_mgr_dir.s:1320`<br>`file_mgr_dir.s:1182` | — |
| **`FILEFILETFSETCATINFO_HFS_NO`** | `0x004948` | `0x0063EE` | `file_mgr_dir.s:1292`<br>`file_mgr_dir.s:1158` | file record: copy all Finder info + dates directory record: copy directory info + dates |
| **`FileOpen`** | `0x00402A` | `0x005ABE` | `file_mgr_dir.s:64` | File Open Called during boot. FileOpen (vFileOpen) |
| **`FILEOPEN`** | `0x00402A` | `0x005ABE` | `file_mgr_dir.s:42` | _Open: open data fork (vectored through $784) |
| **`FILEOPEN_CONT`** | `0x004032` | `0x005ACC` | `file_mgr_dir.s:68`<br>`file_mgr_dir.s:49` | first, make sure we have an open FCB |
| **`FILEOPEN_CONT_2`** | `0x004034` | `0x005ACE` | `file_mgr_dir.s:70`<br>`file_mgr_dir.s:51` | first, make sure we have an open FCB |
| **`FILEOPEN_CONT_3`** | `0x004040` | — | `file_mgr_dir.s:76` | — |
| **`FILEOPEN_CONT_4`** | `0x0040A2` | `0x005B3C` | `file_mgr_dir.s:115`<br>`file_mgr_dir.s:98` | — |
| **`FILEOPEN_CONT_5`** | `0x0040BA` | `0x005B54` | `file_mgr_dir.s:124`<br>`file_mgr_dir.s:107` | copy extent record from catalog to FCB |
| **`FILEOPEN_CONT_6`** | `0x0040FE` | `0x005B98` | `file_mgr_dir.s:154`<br>`file_mgr_dir.s:137` | load fork info from catalog record |
| **`FILEOPEN_CONT_7`** | `0x00415E` | `0x005BF8` | `file_mgr_dir.s:204`<br>`file_mgr_dir.s:187` | found another FCB for same file: adjust EOF |
| **`FILEOPEN_EMPTY`** | `0x004098` | `0x005B32` | `file_mgr_dir.s:112`<br>`file_mgr_dir.s:95` | handle an open for a TFS volume set up clump size |
| **`FILEOPEN_ERR`** | `0x004044` | — | `file_mgr_dir.s:78` | — |
| **`FILEOPEN_EXIT`** | — | `0x005ADE` | `file_mgr_dir.s:59` | — |
| **`FILEOPEN_FOUND`** | `0x004146` | `0x005BE0` | `file_mgr_dir.s:191`<br>`file_mgr_dir.s:174` | scan for other open forks of same file to adjust permissions |
| **`FILEOPEN_FOUND_2`** | `0x004166` | — | `file_mgr_dir.s:207` | — |
| **`FILEOPEN_LOOP`** | `0x00405A` | `0x005AF4` | `file_mgr_dir.s:90`<br>`file_mgr_dir.s:71` | zero the newly found FCB before use |
| **`FILEOPEN_LOOP_2`** | `0x004104` | `0x005B9E` | `file_mgr_dir.s:160`<br>`file_mgr_dir.s:143` | check file permissions permission denied: zero the FCB and exit |
| **`FILEOPEN_NO`** | `0x0040E2` | `0x005B7C` | `file_mgr_dir.s:141`<br>`file_mgr_dir.s:124` | copy CName into FCB set up file info from catalog record |
| **`FILEOPEN_NO_2`** | `0x004130` | `0x005BCA` | `file_mgr_dir.s:182`<br>`file_mgr_dir.s:165` | set up user's own buffer as cache entry |
| **`FILEOPEN_PERMSSNCHK`** | — | `0x005D6C` | `file_mgr_dir.s:383` | load fork info from MFS directory entry |
| **`FILEOPEN_RFN_DONE`** | — | `0x005D7A` | `file_mgr_dir.s:388` | — |
| **`FILEOPEN_SKIP`** | `0x004156` | `0x005BF0` | `file_mgr_dir.s:199`<br>`file_mgr_dir.s:182` | — |
| **`FILEOPEN_TOO_MANY_FILES`** | — | `0x005ADA` | `file_mgr_dir.s:57` | find a free FCB for the file |
| **`FILEREAD`** | — | `0x0069BA` | `file_mgr_io.s:20` | _Read ($A002): read bytes from file |
| **`FileWrite`** | `0x00502A` | `0x006AD0` | `file_mgr_io.s:182` | L_MFILEREAD_CONT_6: read file block into cache (PreRdFileBlk helper) only reads if block is within current LEOF File Write Called during boot. |
| **`FILEWRITE`** | `0x00502A` | `0x006AD0` | `file_mgr_io.s:176` | _Write ($A003): write bytes to file |
| **`FILEWRITE_CONT`** | `0x005060` | `0x006B06` | `file_mgr_io.s:206`<br>`file_mgr_io.s:199` | see if file has to be made physically longer ran off physical end: allocate more blocks |
| **`FILEWRITE_CONT_2`** | `0x0050AA` | `0x006B50` | `file_mgr_io.s:252`<br>`file_mgr_io.s:244` | FILEWRITE_CONT_2 - UpdteCntPos: update byte count, actual count, and file position Called during boot. |
| **`FILEWRITE_CONT_3`** | `0x0050EE` | `0x006B94` | `file_mgr_io.s:294`<br>`file_mgr_io.s:286` | verify mode: compare bytes |
| **`FILEWRITE_CONT_4`** | `0x0050FC` | `0x006BA2` | `file_mgr_io.s:308`<br>`file_mgr_io.s:299` | FILEWRITE_CONT_4 Called during boot. |
| **`FILEWRITE_CONT_5`** | `0x005130` | `0x006BD6` | `file_mgr_io.s:355`<br>`file_mgr_io.s:342` | FILEWRITE_CONT_5 FILEWRITE_CONT_5: read MFS directory block D3 into volume cache |
| **`FILEWRITE_CONT_6`** | `0x005136` | `0x006BDC` | `file_mgr_io.s:358`<br>`file_mgr_io.s:345` | — |
| **`FILEWRITE_CONT_7`** | `0x00513A` | `0x006BE0` | `file_mgr_io.s:360`<br>`file_mgr_io.s:347` | — |
| **`FILEWRITE_DONE`** | `0x005096` | `0x006B3C` | `file_mgr_io.s:237`<br>`file_mgr_io.s:230` | FWrOK |
| **`FILEWRITE_ERR`** | `0x005098` | — | `file_mgr_io.s:239` | — |
| **`FILEWRITE_ERR_2`** | `0x0050E6` | `0x006B8C` | `file_mgr_io.s:288`<br>`file_mgr_io.s:280` | — |
| **`FILEWRITE_EXIT`** | `0x0050A0` | `0x006B46` | `file_mgr_io.s:242`<br>`file_mgr_io.s:235` | — |
| **`FILEWRITE_EXIT_2`** | `0x0050E8` | `0x006B8E` | `file_mgr_io.s:290`<br>`file_mgr_io.s:282` | — |
| **`FILEWRITE_LOOP`** | `0x0050F2` | `0x006B98` | `file_mgr_io.s:297`<br>`file_mgr_io.s:289` | — |
| **`FILEWRITE_NEXT`** | `0x00510C` | `0x006BB2` | `file_mgr_io.s:321`<br>`file_mgr_io.s:311` | FILEWRITE_NEXT Called during boot. FILEWRITE_NEXT: read next MFS directory block (advance CkdDB) |
| **`FILEWRITE_NEXT_2`** | `0x00512A` | `0x006BD0` | `file_mgr_io.s:346`<br>`file_mgr_io.s:334` | FILEWRITE_NEXT_2 -- read next block. FILEWRITE_NEXT_2 |
| **`FILEWRITE_NO`** | `0x005040` | `0x006AE6` | `file_mgr_io.s:193`<br>`file_mgr_io.s:187` | FileWrite (vFileWrite) set up D3 so PreRdFileBlk knows when block must actually be read |
| **`FILEWRITE_NO_2`** | `0x005062` | `0x006B08` | `file_mgr_io.s:209`<br>`file_mgr_io.s:202` | update logical length |
| **`FILEWRITE_NO_3`** | `0x0050A6` | `0x006B4C` | `file_mgr_io.s:244`<br>`file_mgr_io.s:237` | — |
| **`FILEWRITE_NO_4`** | `0x00511C` | `0x006BC2` | `file_mgr_io.s:335`<br>`file_mgr_io.s:324` | FILEWRITE_NO_4 Called during boot. FILEWRITE_NO_4: read MFS directory block D3 into cache |
| **`FILEWRITE_OK`** | `0x0050C2` | `0x006B68` | `file_mgr_io.s:272`<br>`file_mgr_io.s:263` | — |
| **`FILEWRITE_OK_2`** | `0x0050DE` | `0x006B84` | `file_mgr_io.s:284`<br>`file_mgr_io.s:276` | dispatch by mode: D0>0=write, D0=0=read, D0<0=verify |
| **`FILEWRITE_PEOF_DONE`** | — | `0x006B3E` | `file_mgr_io.s:232` | — |
| **`FILL_EVENT_FIELDS`** | `0x002746` | `0x003F40` | `event_mgr.s:88`<br>`event_mgr.s:85` | Fill in the event record FILL_EVENT_FIELDS - Fill event record timestamp and modifier fields A0 points to evtNum field (event record + 6 bytes past queue header). Fills evtTicks, evtMouse (v,h), evtMe... |
| **`FindDrive`** | `0x003414` | `0x004E9A` | `file_mgr_vol.s:1046` | Find Drive Called during boot. FindDrive: find drive queue entry for drive number D2 Returns: D1=driver refnum, A3=drive queue entry, D0=0 or error |
| **`FINDDRIVE`** | `0x003414` | `0x004E9A` | `file_mgr_vol.s:995` | FindDrive: find drive queue entry by drive number D2=drive number, returns A3=drive entry, D1=driver refNum, D0=error |
| **`FINDDRIVE_EMPTY`** | `0x003432` | `0x004EB8` | `file_mgr_vol.s:1058`<br>`file_mgr_vol.s:1007` | — |
| **`FINDDRIVE_FOUND`** | `0x003436` | `0x004EBC` | `file_mgr_vol.s:1061`<br>`file_mgr_vol.s:1010` | — |
| **`FindFCB`** | — | `0x004E46` | `file_mgr_vol.s:955` | FindFCB: find a free FCB and reserve it Returns: D1=FCB offset, A1=FCB array base, D0=0 on success |
| **`FindFCB_NEXT`** | — | `0x004E5C` | `file_mgr_vol.s:965` | — |
| **`FINDVCB_FOUND`** | `0x002CE8` | `0x004730` | `file_mgr_vol.s:230`<br>`file_mgr_vol.s:200` | FINDVCB_FOUND - VCB found |
| **`FINDVCB_LOOP`** | `0x002CCE` | `0x004716` | `file_mgr_vol.s:213`<br>`file_mgr_vol.s:188` | — |
| **`FINDVCB_NEXT`** | `0x002CE4` | `0x00472C` | `file_mgr_vol.s:222`<br>`file_mgr_vol.s:197` | — |
| **`FINDVCB_NSVERR`** | `0x002CF0` | `0x004738` | `file_mgr_vol.s:240`<br>`file_mgr_vol.s:209` | FINDVCB_NSVERR - VCB not found, return nsvErr |
| **`FINDVCB_RET`** | `0x002CEA` | `0x004732` | `file_mgr_vol.s:232`<br>`file_mgr_vol.s:202` | — |
| **`FindVCBDrv`** | `0x002CC0` | `0x004708` | `file_mgr_vol.s:207`<br>`file_mgr_vol.s:182` | **Regs:** `Entry: D0 = drive number (positive) Exit: A2 = VCB, D0 = 0 if found, D0 = nsvErr (-35) if not`<br>FindVCBDrv - find VCB by drive number (D0) or negative volume refnum Searches VCB queue for a volume whose vcbDrvNum (offset 0x48=72) matches D0, or whose vcbVRefNum (offset 0x4A=78) matches -D0 (for ... |
| **`FINITQ_DONE`** | `0x002A80` | `0x0044C2` | `file_mgr_queue.s:304`<br>`file_mgr_queue.s:318` | — |
| **`FINITQUEUE`** | — | `0x0044AE` | `file_mgr_queue.s:310` | FINITQUEUE -- truncate FS queue to single head entry Used during disk-switch dialog so completion callbacks for stale entries in the queue don't fire while the user fumbles for the right disk. Atomica... |
| **`FLUSH_CHK_CLEAN`** | `0x007706` | `0x00925A` | `file_mgr_cache.s:94`<br>`file_mgr_cache.s:78` | FLUSH_CHK_CLEAN - check if more than 25% of control cache buffers are clean Called during boot. |
| **`FLUSH_CHK_MATCH`** | `0x007748` | `0x00929C` | `file_mgr_cache.s:130`<br>`file_mgr_cache.s:114` | FLUSH_CHK_MATCH - FlushCache: check if buffer matches flush criteria Called during boot. |
| **`FLUSH_CHK_ORDER`** | `0x007770` | `0x0092C4` | `file_mgr_cache.s:146`<br>`file_mgr_cache.s:130` | — |
| **`FLUSH_CHK_TRASH`** | `0x007790` | `0x0092E4` | `file_mgr_cache.s:163`<br>`file_mgr_cache.s:146` | — |
| **`FLUSH_COUNT_CLEAN`** | `0x007702` | `0x009256` | `file_mgr_cache.s:85`<br>`file_mgr_cache.s:70` | — |
| **`FLUSH_DIRTY`** | `0x0076A8` | `0x0091FC` | `file_mgr_cache.s:39`<br>`file_mgr_cache.s:34` | FLUSH_DIRTY Called during boot. |
| **`FLUSH_EXIT`** | `0x002846` | `0x004040` | `event_mgr.s:242`<br>`event_mgr.s:219` | — |
| **`FLUSH_EXIT_OK`** | `0x0077A4` | `0x0092F8` | `file_mgr_cache.s:176`<br>`file_mgr_cache.s:158` | FLUSH_EXIT_OK - FlushCache exit: no error Called during boot. |
| **`FLUSH_MAIN`** | `0x007712` | `0x009266` | `file_mgr_cache.s:99`<br>`file_mgr_cache.s:83` | — |
| **`FLUSH_NEXT_ENTRY`** | `0x002840` | `0x00403A` | `event_mgr.s:237`<br>`event_mgr.s:214` | — |
| **`FLUSH_QUEUE_EMPTY`** | `0x002844` | `0x00403E` | `event_mgr.s:240`<br>`event_mgr.s:217` | — |
| **`FLUSH_RESTART`** | `0x007732` | `0x009286` | `file_mgr_cache.s:112`<br>`file_mgr_cache.s:96` | — |
| **`FLUSH_SCAN_NEXT`** | `0x0076E4` | `0x009238` | `file_mgr_cache.s:75`<br>`file_mgr_cache.s:60` | — |
| **`FLUSH_SEARCH_NEXT`** | `0x007736` | `0x00928A` | `file_mgr_cache.s:115`<br>`file_mgr_cache.s:100` | Called by: FLUSH_CHK_MATCH, FLUSH_CHK_ORDER, FLUSH_VOL_MATCH |
| **`FLUSH_VOL_MATCH`** | `0x007766` | `0x0092BA` | `file_mgr_cache.s:141`<br>`file_mgr_cache.s:125` | — |
| **`FLUSH_WALK_LOOP`** | `0x00282E` | `0x004028` | `event_mgr.s:228`<br>`event_mgr.s:205` | — |
| **`FLUSH_WRITE_BUF`** | `0x00777E` | `0x0092D2` | `file_mgr_cache.s:158`<br>`file_mgr_cache.s:141` | FLUSH_WRITE_BUF - FlushCache: flush next matching buffer in disk order Called during boot. |
| **`FLUSH_ZERO_MATCH`** | `0x007730` | `0x009284` | `file_mgr_cache.s:110`<br>`file_mgr_cache.s:94` | — |
| **`FlushCache`** | `0x0076CC` | `0x00921A` | `file_mgr_cache.s:65` | Flush Cache Called during boot. |
| **`FLUSHCACHE`** | `0x0076CC` | `0x00921A` | `file_mgr_cache.s:47` | Called by: OFFLINE_SKIP_2, CREATE_CONT_7, L_MFILEREAD_CONT, FILECLOSE_OK_2, VBTCLOSE (and 3 more) |
| **`FLUSHDIRTY_EXIT`** | `0x0076C4` | `0x009218` | `file_mgr_cache.s:49`<br>`file_mgr_cache.s:44` | — |
| **`FlushEvents`** | `0x00280A` | `0x004004` | `event_mgr.s:215` | _FlushEvents ($A032) - remove events matching a mask D0.W = eventMask (low word): bits for event types to flush D0.W = stopMask (high word, swapped into D1): if an event matches this mask, stop flushi... |
| **`FLUSHEVENTS`** | `0x00280A` | `0x004004` | `event_mgr.s:192` | _FlushEvents ($A032) -- remove events matching mask D0.W = eventMask, swapped high word = stopMask. Walks EventQueue: dequeue+invalidate any entry whose evtNum is in eventMask. Stop early if entry's e... |
| **`FlushFile`** | `0x005144` | `0x006BEA` | `file_mgr_io.s:371` | _FlushFile ($A045) _FlushFile ($A045) |
| **`FLUSHFILE`** | `0x005144` | `0x006BEA` | `file_mgr_io.s:352` | — |
| **`FlushMDB`** | `0x002D2E` | `0x004776` | `file_mgr_vol.s:300` | FlushMDB - write the master directory block (MDB) to disk Copies VCB fields back into the cached MDB block, updates extent B-tree and catalog B-tree file size info from their FCB entries, then release... |
| **`FLUSHMDB`** | `0x002D2E` | `0x004776` | `file_mgr_vol.s:262` | **Regs:** `Entry: A2 = VCB pointer`<br>FLUSHMDB - flush Master Directory Block to disk Writes the in-memory VCB data back to the on-disk MDB (block 2). Copies VCB fields to the block buffer, including catalog and extent overflow file exten... |
| **`FLUSHMDB_CPYEXT`** | — | `0x008BAC` | `file_mgr_btree.s:1150` | — |
| **`FLUSHMDB_DONE`** | `0x002DDC` | `0x00482E` | `file_mgr_vol.s:350`<br>`file_mgr_vol.s:319` | — |
| **`FLUSHMDB_EXIT`** | — | `0x008BBE` | `file_mgr_btree.s:1157` | — |
| **`FLUSHMDB_GETBLK`** | — | `0x008B74` | `file_mgr_btree.s:1127` | — |
| **`FLUSHMDB_RELBLK`** | — | `0x008BBA` | `file_mgr_btree.s:1155` | — |
| **`FLUSHMDB_UPDEXT`** | — | `0x008BA2` | `file_mgr_btree.s:1146` | update extent info in alt MDB |
| **`FLUSHMDB_USESIZE`** | — | `0x008B68` | `file_mgr_btree.s:1122` | calculate last block number for alt MDB |
| **`FlushVol`** | `0x0035FC` | `0x005082` | `file_mgr_vol.s:1300` | _FlushVol ($A013) Called during boot. |
| **`FLUSHVOL`** | `0x0035FC` | `0x005082` | `file_mgr_vol.s:1207` | _FlushVol: flush volume buffers to disk |
| **`FLUSHVOL_CONT`** | `0x003604` | `0x008A8C` | `file_mgr_vol.s:1304`<br>`file_mgr_btree.s:1023` | common entry for FlushVol/UnmountVol |
| **`FLUSHVOL_DONE`** | `0x003632` | `0x0050BA` | `file_mgr_vol.s:1330`<br>`file_mgr_vol.s:1239` | Called by: FLUSHVOL_UNMOUNTVOL_SHARED, FLUSHVOL_OK |
| **`FLUSHVOL_ERR`** | `0x003634` | — | `file_mgr_vol.s:1332` | — |
| **`FLUSHVOL_NO_DISPOSE`** | — | `0x0050B8` | `file_mgr_vol.s:1236` | — |
| **`FLUSHVOL_OK`** | `0x00361C` | `0x0050A2` | `file_mgr_vol.s:1321`<br>`file_mgr_vol.s:1227` | FLUSHVOL_OK TFS FlushVol/UnmountVol path |
| **`FLUSHVOL_SKIP`** | `0x003628` | `0x0050AE` | `file_mgr_vol.s:1326`<br>`file_mgr_vol.s:1232` | — |
| **`FLUSHVOL_UNMOUNTVOL_SHARED`** | — | `0x00508A` | `file_mgr_vol.s:1211` | shared FlushVol/UnmountVol entry |
| **`FNDFCB`** | `0x005406` | `0x006EBE` | `file_mgr_io.s:736`<br>`file_mgr_io.s:649` | FNDFCB FndFCB: find an FCB by refnum or by index (for GetFCBInfo) |
| **`FNDFCB_NOT_FOUND_ERR`** | — | `0x006F16` | `file_mgr_io.s:685` | — |
| **`FNDFCB_RTS_WITH_VCB`** | — | `0x006F1E` | `file_mgr_io.s:688` | — |
| **`FndFilName`** | `0x004996` | — | `file_mgr_dir.s:1338` | Fnd Fil Name Called during boot. |
| **`FNDFILNAME_CONT`** | `0x00499C` | `0x006442` | `file_mgr_dir.s:1341`<br>`file_mgr_dir.s:1197` | FndFilName: resolve pathname to volume, directory, and catalog record |
| **`FNDFILNAME_CONT_2`** | `0x0049E6` | `0x00648C` | `file_mgr_dir.s:1386`<br>`file_mgr_dir.s:1241` | TFS FndFilName: parse pathname component by component |
| **`FNDFILNAME_CONT_3`** | `0x004A1A` | `0x0064C0` | `file_mgr_dir.s:1422`<br>`file_mgr_dir.s:1276` | FNDFILNAME_CONT_3: parse pathname component and look up in catalog (FndFilName helper) |
| **`FNDFILNAME_CONT_4`** | `0x004ABA` | — | `file_mgr_dir.s:1512` | FNDFILNAME_CONT_4 Called during boot. FNDFILNAME_CONT_4: check for external FS and dispatch if so |
| **`FNDFILNAME_ERR`** | `0x004AA2` | `0x006548` | `file_mgr_dir.s:1492`<br>`file_mgr_dir.s:1344` | TFS FndFilName: catalog lookup error |
| **`FNDFILNAME_ERR_2`** | `0x004AAA` | `0x006550` | `file_mgr_dir.s:1497`<br>`file_mgr_dir.s:1349` | TFS FndFilName exit |
| **`FNDFILNAME_ERR_3`** | `0x004AC8` | `0x00656E` | `file_mgr_dir.s:1518`<br>`file_mgr_dir.s:1365` | — |
| **`FNDFILNAME_EXIT`** | `0x004AB0` | `0x006556` | `file_mgr_dir.s:1500`<br>`file_mgr_dir.s:1352` | — |
| **`FNDFILNAME_NEXT`** | `0x0049E2` | `0x006488` | `file_mgr_dir.s:1382`<br>`file_mgr_dir.s:1237` | TFS: use catalog instead (fall through to TFS FndFilName) |
| **`FNDFILNAME_NO`** | `0x0049AC` | `0x006452` | `file_mgr_dir.s:1356`<br>`file_mgr_dir.s:1211` | — |
| **`FNDFILNAME_NO_2`** | `0x0049B8` | `0x00645E` | `file_mgr_dir.s:1363`<br>`file_mgr_dir.s:1218` | check if caller provided a pathname with content |
| **`FNDFILNAME_NO_3`** | `0x0049CA` | `0x006470` | `file_mgr_dir.s:1372`<br>`file_mgr_dir.s:1227` | check for HFS DirID override FNDFILNAME_NO_3: MFS FndFilName - look up file in MFS directory |
| **`FNDFILNAME_NO_4`** | `0x004A00` | `0x0064A6` | `file_mgr_dir.s:1401`<br>`file_mgr_dir.s:1255` | FNDFILNAME_NO_4 |
| **`FNDFILNAME_NO_5`** | `0x004A7E` | `0x006524` | `file_mgr_dir.s:1469`<br>`file_mgr_dir.s:1322` | copy current pathname component to A6 stack as Pascal string look up this pathname component in the catalog deallocate stack buffer if pathname had a directory prefix, follow thread to get actual dire... |
| **`FNDFILNAME_OK`** | `0x00499E` | `0x006444` | `file_mgr_dir.s:1350`<br>`file_mgr_dir.s:1205` | FNDFILNAME_OK Called during boot. FndFilName common entry: get DirID from WDCB and check for DirID override |
| **`FNDFILNAME_OK_2`** | `0x004A04` | `0x0064AA` | `file_mgr_dir.s:1410`<br>`file_mgr_dir.s:1264` | FNDFILNAME_OK_2 found colon: this component is a directory prefix |
| **`FNDFILNAME_OK_3`** | `0x004A18` | `0x0064BE` | `file_mgr_dir.s:1419`<br>`file_mgr_dir.s:1273` | — |
| **`FNDFILNAME_OK_4`** | `0x004A98` | `0x00653E` | `file_mgr_dir.s:1486`<br>`file_mgr_dir.s:1338` | component was a directory: advance to next component FNDFILNAME_OK_4 TFS FndFilName: found the file/directory |
| **`FreeBk`** | `0x010C40` | `0x00B20C` | `memory_mgr.s:2787` | FreeBk - free the block whose data pointer is A0 (zone A6) A relocatable block's master pointer is put back on the free list (ReleaseMP); the block becomes free and zcbFree grows. A block that is alre... |
| **`FREEBK`** | `0x010C40` | `0x00B20C` | `memory_mgr.s:2093` | — |
| **`FREEBK_NO`** | `0x010C5E` | — | `memory_mgr.s:2799` | — |
| **`FREEBK_NORELOC`** | — | `0x00B22A` | `memory_mgr.s:2105` | — |
| **`FREEBK_SKIP`** | `0x010C66` | `0x00B232` | `memory_mgr.s:2802`<br>`memory_mgr.s:2108` | — |
| **`FreeMem`** | `0x010014` | `0x00A524` | `memory_mgr.s:358` | _FreeMem ($A01C) -> D0.L = total free bytes |
| **`FREEMEM`** | `0x010014` | `0x00A524` | `memory_mgr.s:242` | — |
| **`FreeNode`** | `0x006FBA` | `0x008A7C` | `file_mgr_btree.s:1186` | Free Node |
| **`FREENODE`** | `0x006FBA` | `0x008A7C` | `file_mgr_btree.s:1014` | — |
| **`FREENODE_EXIT`** | `0x006FFC` | `0x008AC0` | `file_mgr_btree.s:1215`<br>`file_mgr_btree.s:1046` | FNFound: found map record, mark node free |
| **`FREENODE_GETMAP`** | `0x006FC4` | — | `file_mgr_btree.s:1192` | locate map record for target node |
| **`FSDispatch`** | `0x002852` | — | `file_mgr_queue.s:33` | File Manager -- trap dispatch, file system queue, disk-switch hook Apple source: TFS.a, the head of the TurboFS module (MacSEROM.lst module TURBOFS): _FSDispatch ($A060, the HFS selector dispatcher wi... |
| **`FSDISPATCH_BAD_SEL`** | `0x00285C` | `0x00429E` | `file_mgr_queue.s:38`<br>`file_mgr_queue.s:36` | — |
| **`FSDISPATCH_VALID`** | `0x002864` | `0x0042A6` | `file_mgr_queue.s:47`<br>`file_mgr_queue.s:44` | HFS dispatch - index into HFS_DISPATCH_TABLE and jump to handler |
| **`FSIODNETBL`** | — | `0x002DB4` | `device_mgr.s:71` | Device Manager Apple source: DeviceMgr.a (MacSEROM.lst module IOCORE): the jump offsets FSIODNETBL (JFetch, JStash, JIODone), FETCH, STASH, IODONE, the request queueing and the traps Open ... KillIO, ... |
| **`FSQUEUE_CALL_EXTFS`** | `0x002A24` | `0x004466` | `file_mgr_queue.s:262`<br>`file_mgr_queue.s:274` | — |
| **`FSQUEUE_CHK_EXTFS`** | `0x0029F2` | `0x004434` | `file_mgr_queue.s:247`<br>`file_mgr_queue.s:259` | — |
| **`FSQUEUE_CHK_MORE`** | `0x002A5A` | `0x00449C` | `file_mgr_queue.s:282`<br>`file_mgr_queue.s:294` | — |
| **`FSQUEUE_CLR_OFFLINE`** | `0x0029E2` | `0x004424` | `file_mgr_queue.s:241`<br>`file_mgr_queue.s:253` | — |
| **`FSQUEUE_DEQUEUE`** | `0x002A26` | `0x004468` | `file_mgr_queue.s:264`<br>`file_mgr_queue.s:276` | — |
| **`FSQUEUE_DONE`** | `0x00295E` | `0x0043A0` | `file_mgr_queue.s:188`<br>`file_mgr_queue.s:200` | FS queue completion - called after an FS call finishes Checks for disk-switch errors and retries with alternate volumes. Called by: FSDISPATCH_BAD_SEL, HFS_MOUNTVOL, HFSC_OK, FILEOPEN_FOUND_2, FILEFIL... |
| **`FSQUEUE_ENQUEUE`** | `0x002912` | `0x004354` | `file_mgr_queue.s:143`<br>`file_mgr_queue.s:145` | FSQUEUE_ENQUEUE - enqueue param block into FS queue and start server Adds the param block at A0 into the FS queue (FSQHdr). If the queue was idle (qFlags bit 0 clear), starts the FS queue server to pr... |
| **`FSQUEUE_NO_DRIVE`** | `0x0029E0` | `0x004422` | `file_mgr_queue.s:239`<br>`file_mgr_queue.s:251` | FSQUEUE_NO_DRIVE - no alternate drive found, report nsDrvErr |
| **`FSQUEUE_NO_HOOK`** | `0x0028B4` | `0x0042F6` | `file_mgr_queue.s:95`<br>`file_mgr_queue.s:98` | — |
| **`FSQUEUE_RESTORED_SR`** | `0x002A48` | `0x00448A` | `file_mgr_queue.s:274`<br>`file_mgr_queue.s:286` | — |
| **`FSQUEUE_RETURN`** | `0x002910` | `0x004352` | `file_mgr_queue.s:132`<br>`file_mgr_queue.s:134` | — |
| **`FSQUEUE_SCAN_END`** | `0x0029C0` | `0x004402` | `file_mgr_queue.s:222`<br>`file_mgr_queue.s:235` | — |
| **`FSQUEUE_SCAN_NEXT`** | `0x0029A8` | `0x0043EA` | `file_mgr_queue.s:212`<br>`file_mgr_queue.s:225` | FSQUEUE_SCAN_NEXT -- walk PMSP looking for an online VCB drive |
| **`FSQUEUE_SERVER`** | `0x00292E` | `0x004370` | `file_mgr_queue.s:162`<br>`file_mgr_queue.s:163` | FS queue server - dequeue and execute pending FS calls Processes the head entry of the FS queue. Sets up the PMSP (Permission State Machine Pointer) and HFS stack, then calls the routine address store... |
| **`FSQUEUE_SETUP`** | `0x0028AA` | `0x0042EC` | `file_mgr_queue.s:90`<br>`file_mgr_queue.s:93` | FSQUEUE_SETUP -- fSQueue: wait our turn. Called by: FSDISPATCH_BAD_SEL, HFS_MOUNTVOL, FlushVol, hfsC, GetVolInfo (and 32 more) |
| **`FSQUEUE_SETUP_SYNC`** | `0x0028A6` | `0x0042E8` | `file_mgr_queue.s:86`<br>`file_mgr_queue.s:89` | FSQUEUE_SETUP_SYNC - FS param block setup (clear async bit) FSQUEUE_SETUP - FS param block setup (preserve async bit) Prepares the I/O parameter block at A0 for FS queue submission. Sets ioResult=1 (p... |
| **`FSQUEUE_SPIN_WAIT`** | `0x0028F0` | `0x004332` | `file_mgr_queue.s:121`<br>`file_mgr_queue.s:123` | — |
| **`FSQUEUE_STORE_CMD`** | `0x0028CE` | `0x004310` | `file_mgr_queue.s:102`<br>`file_mgr_queue.s:105` | — |
| **`FSQUEUE_STORE_ERR`** | `0x00296C` | `0x0043AE` | `file_mgr_queue.s:194`<br>`file_mgr_queue.s:206` | — |
| **`FSQUEUE_SYNC_PATH`** | `0x0028E6` | `0x004328` | `file_mgr_queue.s:115`<br>`file_mgr_queue.s:117` | Synchronous FS call path - enqueue, wait for completion |
| **`FSQUEUE_SYNC_WAIT`** | `0x0028EA` | `0x00432C` | `file_mgr_queue.s:117`<br>`file_mgr_queue.s:119` | — |
| **`FSQUEUE_TRY_LOCK`** | `0x002920` | `0x004362` | `file_mgr_queue.s:148`<br>`file_mgr_queue.s:150` | — |
| **`FSQUEUE_TRY_SWITCH`** | `0x00298C` | `0x0043CE` | `file_mgr_queue.s:204`<br>`file_mgr_queue.s:216` | — |
| **`FXM`** | — | `0x007550` | `file_mgr_alloc.s:353` | — |
| **`FXMKeyCmp`** | `0x005CDE` | `0x0077A0` | `file_mgr_alloc.s:679` | FXM Key Cmp FXMKeyCmp: compare two extent file keys |
| **`FXMKEYCMP`** | `0x005CDE` | `0x0077A0` | `file_mgr_alloc.s:595` | — |
| **`FXMKEYCMP_CONT`** | `0x005D0A` | `0x0077CC` | `file_mgr_alloc.s:700`<br>`file_mgr_alloc.s:612` | compare file ID's file ID's equal, compare fork types fork types equal, compare starting block numbers KCIsEQ KCIsLT |
| **`FXMKEYCMP_CONT_2`** | `0x005D10` | `0x0077D2` | `file_mgr_alloc.s:704`<br>`file_mgr_alloc.s:615` | KCIsGT |
| **`FXMKEYCMP_EXIT`** | `0x005D14` | `0x0077D6` | `file_mgr_alloc.s:706`<br>`file_mgr_alloc.s:617` | — |
| **`GB_ASSIGN`** | `0x007908` | `0x00945C` | `file_mgr_cache.s:366`<br>`file_mgr_cache.s:331` | GBAssign: assign buffer to new block, read it from disk |
| **`GB_CACHE_SEARCH`** | `0x00786C` | `0x0093C0` | `file_mgr_cache.s:272`<br>`file_mgr_cache.s:242` | — |
| **`GB_CHK_INUSE`** | `0x007898` | `0x0093EC` | `file_mgr_cache.s:298`<br>`file_mgr_cache.s:267` | — |
| **`GB_CHK_NONEMPTY`** | `0x007886` | `0x0093DA` | `file_mgr_cache.s:291`<br>`file_mgr_cache.s:260` | GB_CHK_NONEMPTY - GetBlock: non-empty buffer, check if it's the one we want Called during boot. |
| **`GB_CHK_OWNBUF`** | `0x007806` | `0x00935A` | `file_mgr_cache.s:231`<br>`file_mgr_cache.s:202` | GB_CHK_OWNBUF - GetBlock: file block not in cache, check OwnBuf Called during boot. |
| **`GB_CHK_REREAD`** | `0x00796E` | `0x0094C2` | `file_mgr_cache.s:417`<br>`file_mgr_cache.s:377` | GB_CHK_REREAD - GetBlock: check for forced re-read (GBread flag) Called during boot. |
| **`GB_EVICT_DIRTY`** | `0x0078D4` | `0x009428` | `file_mgr_cache.s:348`<br>`file_mgr_cache.s:313` | GB_EVICT_DIRTY - GetBlock: must evict dirty buffer (flush all blocks of same file first) |
| **`GB_EXIT`** | `0x007990` | `0x0094E4` | `file_mgr_cache.s:432`<br>`file_mgr_cache.s:392` | Called by: GB_MAP_BLOCK, GB_SELECT, GB_PICK_BUFFER, GB_READ_ERR, GB_FOUND_IT |
| **`GB_EXIT_OK`** | `0x00798A` | `0x0094DE` | `file_mgr_cache.s:428`<br>`file_mgr_cache.s:388` | — |
| **`GB_FILE_SEARCH`** | `0x0077DC` | `0x009330` | `file_mgr_cache.s:210`<br>`file_mgr_cache.s:182` | Called by: GB_FILE_SEARCH |
| **`GB_FLUSH_VREF`** | `0x0078F2` | `0x009446` | `file_mgr_cache.s:358`<br>`file_mgr_cache.s:323` | — |
| **`GB_FOUND_IT`** | `0x007962` | `0x0094B6` | `file_mgr_cache.s:406`<br>`file_mgr_cache.s:367` | GB_FOUND_IT - GetBlock: found requested buffer (GBFoundIt) Called during boot. |
| **`GB_MAP_BLOCK`** | `0x00781C` | `0x009370` | `file_mgr_cache.s:238`<br>`file_mgr_cache.s:209` | — |
| **`GB_PICK_BUFFER`** | `0x0078BC` | `0x009410` | `file_mgr_cache.s:331`<br>`file_mgr_cache.s:297` | GB_PICK_BUFFER - GetBlock: select best available buffer (empty > clean > dirty) Called during boot. |
| **`GB_READ_BLK`** | `0x007938` | `0x00948C` | `file_mgr_cache.s:379`<br>`file_mgr_cache.s:343` | GBReadBlk: read block from disk into cache buffer |
| **`GB_READ_ERR`** | `0x007958` | `0x0094AC` | `file_mgr_cache.s:396`<br>`file_mgr_cache.s:358` | scavenge VCB write count from tag data whenever we read a block GB_READ_ERR - GetBlock: read error, mark buffer empty |
| **`GB_REQUEUE`** | `0x007974` | `0x0094C8` | `file_mgr_cache.s:421`<br>`file_mgr_cache.s:381` | GBReQueue: re-queue buffer for LRU |
| **`GB_SAVE_CLEAN`** | `0x0078AC` | `0x009400` | `file_mgr_cache.s:311`<br>`file_mgr_cache.s:279` | GB_SAVE_CLEAN - GetBlock: found a clean (not dirty) non-in-use buffer Called during boot. |
| **`GB_SCAN_NEXT`** | `0x007874` | `0x0093C8` | `file_mgr_cache.s:277`<br>`file_mgr_cache.s:247` | — |
| **`GB_SELECT`** | `0x0078B0` | `0x009404` | `file_mgr_cache.s:320`<br>`file_mgr_cache.s:287` | GB_SELECT - GetBlock: block not found, select a buffer to use (GBSelect) Called during boot. |
| **`GB_VOL_REF`** | `0x007864` | `0x0093B8` | `file_mgr_cache.s:267`<br>`file_mgr_cache.s:237` | GB_VOL_REF - GetBlock: logical block on volume was requested (GBVolRef) Called during boot. |
| **`GET_MAP`** | `0x007006` | `0x008ACA` | `file_mgr_btree.s:1226`<br>`file_mgr_btree.s:1053` | GET_MAP GetMap: gets next allocation map record |
| **`GET_OFFA`** | `0x00745C` | `0x008FB0` | `file_mgr_btree.s:1870`<br>`file_mgr_btree.s:1649` | GET_OFFA - GetOffA: get offset address |
| **`GET_TRAP_OLD`** | `0x002006` | `0x002D8A` | `trap_dispatch.s:146`<br>`trap_dispatch.s:130` | Old-style GetTrapAddress (bit 9 = 0) Auto-detects OS vs Toolbox via DETECT_TRAP_TABLE, then reads address. |
| **`GET_TRAP_READ`** | `0x002026` | `0x002DAA` | `trap_dispatch.s:167`<br>`trap_dispatch.s:148` | — |
| **`GETADBINFO`** | — | `0x003D38` | `adb_mgr.s:1154` | **Regs:** `Entry: D0 = ADB address, A0 = ADBDataBlock pointer Exit: D0 = 0 if found, -1 if not`<br>GETADBINFO - _GetADBInfo trap: get device info by address Entry: D0 = ADB address, A0 = ADBDataBlock pointer Exit: D0 = 0 if found, -1 if not |
| **`GetAppParms`** | `0x00F710` | `0x009B5A` | `segment_loader.s:382` | **Proto:** `Pascal: procedure GetAppParms(VAR apName: Str255; VAR apRefNum: INTEGER; VAR apParam: Handle);`<br>_GetAppParms ($A9F5): get current application info Pascal: procedure GetAppParms(VAR apName: Str255; VAR apRefNum: INTEGER; VAR apParam: Handle); |
| **`GETAPPPARMS`** | `0x00F710` | `0x009B5A` | `segment_loader.s:310` | — |
| **`GetBlock`** | `0x0077B6` | `0x009304` | `file_mgr_cache.s:197` | Get Block Called during boot. |
| **`GETBLOCK`** | `0x0077B6` | `0x009304` | `file_mgr_cache.s:165` | Called by: FLUSHMDB, MOUNTVOL_SKIP_2, L_MFILEREAD_CONT_6, FILECLOSE_NO_2, READBM_NEXT_3 (and 4 more) |
| **`GETBTVARSIZE`** | — | `0x0088EE` | `file_mgr_btree.s:840` | GetBTVarSize: calculate B-tree variable block size |
| **`GETCATINFO`** | — | `0x006576` | `file_mgr_dir.s:1370` | _GetCatInfo: get catalog info for file or directory |
| **`GetCatInfo_hfs`** | `0x004AD0` | — | `file_mgr_dir.s:1527` | Get Cat Info_hfs |
| **`GETCATINFO_OFFSPRING`** | — | `0x0066D8` | `file_mgr_dir.s:1520` | GetCatInfo mode: get offspring directly (includes directories) |
| **`GETCODERSRC`** | — | `0x00990A` | `segment_loader.s:65` | — |
| **`GETDIR`** | — | `0x0055DA` | `file_mgr_vol.s:1851` | _HGetVol with ioDirFlg: get default working directory info |
| **`GetDir_hfs4`** | `0x003B4E` | — | `file_mgr_vol.s:2023` | Get Dir_hfs4 _GetVol (HFS): get default directory info |
| **`GETDIR_HFS4_NO`** | `0x003B6E` | — | `file_mgr_vol.s:2033` | — |
| **`GetEOF`** | `0x005340` | `0x006DF2` | `file_mgr_io.s:614` | _GetEOF ($A011) Called during boot. _GetEOF ($A011) |
| **`GETEOF`** | `0x005340` | `0x006DF2` | `file_mgr_io.s:549` | — |
| **`GETEOF_NO`** | `0x00534E` | — | `file_mgr_io.s:619` | — |
| **`GETFCBINFO`** | — | `0x006E6A` | `file_mgr_io.s:614` | — |
| **`GetFCBInfo_hfs`** | `0x0053B2` | — | `file_mgr_io.s:696` | Get FCB Info_hfs _GetFCBInfo (HFS): return info about an open FCB |
| **`GETFCBINFO_HFS_CONT`** | `0x00542E` | `0x006EE6` | `file_mgr_io.s:752`<br>`file_mgr_io.s:664` | — |
| **`GETFCBINFO_HFS_ERR`** | `0x005402` | `0x006E00` | `file_mgr_io.s:728`<br>`file_mgr_io.s:554` | — |
| **`GETFCBINFO_HFS_ERR_2`** | `0x005462` | — | `file_mgr_io.s:780` | — |
| **`GETFCBINFO_HFS_FOUND`** | `0x00545E` | — | `file_mgr_io.s:778` | GETFCBINFO_HFS_FOUND |
| **`GETFCBINFO_HFS_NO`** | `0x0053F8` | `0x006EB0` | `file_mgr_io.s:724`<br>`file_mgr_io.s:638` | copy first 20 bytes of FCB to param block copy additional FCB fields copy FCB CName to caller's buffer GetFCBInfo exit: set requested volume and check external FS |
| **`GETFCBINFO_HFS_NO_2`** | `0x00542A` | — | `file_mgr_io.s:750` | indexed search: find Nth user-open FCB |
| **`GETFCBINFO_HFS_NO_3`** | `0x005450` | `0x006F08` | `file_mgr_io.s:765`<br>`file_mgr_io.s:677` | — |
| **`GETFCBINFO_HFS_OK`** | `0x005446` | `0x006EFE` | `file_mgr_io.s:760`<br>`file_mgr_io.s:672` | — |
| **`GETFCBINFO_HFS_SKIP`** | `0x005454` | — | `file_mgr_io.s:768` | — |
| **`GETFCBINFO_INDEXED_BEGIN`** | — | `0x006EE2` | `file_mgr_io.s:662` | — |
| **`GETFCBINFO_NEXT_FCB`** | — | `0x006F0C` | `file_mgr_io.s:680` | — |
| **`GetFileInfo`** | `0x004AE2` | `0x006588` | `file_mgr_dir.s:1539` | _GetFileInfo ($A00C) Called during boot. |
| **`GETFILEINFO`** | `0x004AE2` | `0x006588` | `file_mgr_dir.s:1377` | _GetFileInfo ($A00C): get file info by name or index |
| **`GETFILEINFO_BEGIN`** | — | `0x006592` | `file_mgr_dir.s:1380` | — |
| **`GETFILEINFO_CONT`** | `0x004B1C` | `0x0065BC` | `file_mgr_dir.s:1566`<br>`file_mgr_dir.s:1397` | GETFILEINFO_CONT |
| **`GETFILEINFO_CONT_10`** | `0x004E32` | `0x0068D6` | `file_mgr_dir.s:1955`<br>`file_mgr_dir.s:1768` | MFS GetFileInfo indexed: resume from cached position or start fresh |
| **`GETFILEINFO_CONT_11`** | `0x004E46` | `0x0068EA` | `file_mgr_dir.s:1963`<br>`file_mgr_dir.s:1776` | — |
| **`GETFILEINFO_CONT_12`** | `0x004E76` | `0x00691A` | `file_mgr_dir.s:1997`<br>`file_mgr_dir.s:1806` | copy filename to caller's buffer |
| **`GETFILEINFO_CONT_2`** | `0x004B1E` | `0x0065BE` | `file_mgr_dir.s:1568`<br>`file_mgr_dir.s:1399` | — |
| **`GETFILEINFO_CONT_3`** | `0x004BDC` | `0x00667A` | `file_mgr_dir.s:1648`<br>`file_mgr_dir.s:1476` | index == 0: get by name (thread lookup) index > 0: get Nth offspring of directory |
| **`GETFILEINFO_CONT_4`** | `0x004C0A` | — | `file_mgr_dir.s:1667` | — |
| **`GETFILEINFO_CONT_5`** | `0x004C4A` | `0x0066EE` | `file_mgr_dir.s:1699`<br>`file_mgr_dir.s:1530` | GETFILEINFO_CONT_5: format result from catalog record into param block |
| **`GETFILEINFO_CONT_6`** | `0x004CC0` | `0x006764` | `file_mgr_dir.s:1750`<br>`file_mgr_dir.s:1581` | — |
| **`GETFILEINFO_CONT_7`** | `0x004D82` | — | `file_mgr_dir.s:1838` | MFS SetFileInfo/SetFilLock: mark dirty and flush |
| **`GETFILEINFO_CONT_8`** | `0x004DC0` | `0x006864` | `file_mgr_dir.s:1878`<br>`file_mgr_dir.s:1691` | — |
| **`GETFILEINFO_CONT_9`** | `0x004DD0` | `0x006874` | `file_mgr_dir.s:1895`<br>`file_mgr_dir.s:1707` | MFS directory search: scan entries for matching filename |
| **`GETFILEINFO_DIR_LOOP`** | — | `0x0066A8` | `file_mgr_dir.s:1495` | — |
| **`GETFILEINFO_DONE`** | — | `0x0066D4` | `file_mgr_dir.s:1517` | Called by: GETFILEINFO_BEGIN, GETFILEINFO_CONT_2, GETFILEINFO_INDEXED, GETFILEINFO_VOLNAME_DONE, GETFILEINFO_ERR (and 2 more) |
| **`GETFILEINFO_ERR`** | `0x004C2A` | `0x0066C8` | `file_mgr_dir.s:1682`<br>`file_mgr_dir.s:1510` | catalog error exit |
| **`GETFILEINFO_ERR_2`** | `0x004C36` | — | `file_mgr_dir.s:1688` | — |
| **`GETFILEINFO_ERR_3`** | `0x004CCC` | `0x006770` | `file_mgr_dir.s:1755`<br>`file_mgr_dir.s:1585` | update this FCB's fork lengths from catalog |
| **`GETFILEINFO_ERR_4`** | `0x004D12` | `0x0067B6` | `file_mgr_dir.s:1792`<br>`file_mgr_dir.s:1617` | compute clump size from catalog entry GETFILEINFO_ERR_4 GetCatInfo directory record: copy directory info to param block |
| **`GETFILEINFO_ERR_5`** | `0x004D8C` | `0x006830` | `file_mgr_dir.s:1842`<br>`file_mgr_dir.s:1661` | — |
| **`GETFILEINFO_ERR_6`** | `0x004DB6` | `0x00685A` | `file_mgr_dir.s:1874`<br>`file_mgr_dir.s:1687` | GETFILEINFO_ERR_6 Called during boot. |
| **`GETFILEINFO_ERR_7`** | `0x004E0E` | `0x0068B2` | `file_mgr_dir.s:1926`<br>`file_mgr_dir.s:1738` | — |
| **`GETFILEINFO_ERR_8`** | `0x004E5E` | `0x006902` | `file_mgr_dir.s:1980`<br>`file_mgr_dir.s:1788` | GETFILEINFO_ERR_8 |
| **`GETFILEINFO_EXIT`** | `0x004B6C` | `0x00660C` | `file_mgr_dir.s:1599`<br>`file_mgr_dir.s:1429` | MFS GetFileInfo: only supports root directory MFS root directory info (synthetic) |
| **`GETFILEINFO_EXIT_2`** | `0x004C8C` | `0x006730` | `file_mgr_dir.s:1727`<br>`file_mgr_dir.s:1559` | set file attributes and scan for open FCBs |
| **`GETFILEINFO_FCB_DONE`** | — | `0x00677E` | `file_mgr_dir.s:1590` | — |
| **`GETFILEINFO_FNF_TRANSLATE`** | — | `0x0066D2` | `file_mgr_dir.s:1514` | — |
| **`GETFILEINFO_FOUND`** | `0x004B08` | — | `file_mgr_dir.s:1554` | found file: check TFS or MFS |
| **`GETFILEINFO_FOUND_2`** | `0x004CDA` | — | `file_mgr_dir.s:1760` | — |
| **`GETFILEINFO_FOUND_3`** | `0x004E08` | `0x0068AC` | `file_mgr_dir.s:1923`<br>`file_mgr_dir.s:1735` | match found |
| **`GETFILEINFO_HFS_FILENUM`** | — | `0x006748` | `file_mgr_dir.s:1566` | — |
| **`GETFILEINFO_HFS_OR_MFS`** | — | `0x0065AE` | `file_mgr_dir.s:1391` | name-based lookup |
| **`GETFILEINFO_INDEXED`** | — | `0x0065F4` | `file_mgr_dir.s:1419` | check for HFS DirID override |
| **`GETFILEINFO_LOOKUP`** | `0x004AEC` | — | `file_mgr_dir.s:1543` | GetFileInfo: lookup by name or use ioFDirIndex |
| **`GETFILEINFO_LOOP`** | `0x004B72` | `0x006612` | `file_mgr_dir.s:1602`<br>`file_mgr_dir.s:1432` | — |
| **`GETFILEINFO_LOOP_2`** | `0x004C0E` | `0x0066AC` | `file_mgr_dir.s:1669`<br>`file_mgr_dir.s:1497` | — |
| **`GETFILEINFO_LOOP_3`** | `0x004C62` | `0x006706` | `file_mgr_dir.s:1709`<br>`file_mgr_dir.s:1540` | copy filename to caller's buffer |
| **`GETFILEINFO_LOOP_4`** | `0x004C80` | `0x006724` | `file_mgr_dir.s:1723`<br>`file_mgr_dir.s:1554` | check record type: file or directory? copy file record fields to param block |
| **`GETFILEINFO_LOOP_5`** | `0x004CF0` | `0x006794` | `file_mgr_dir.s:1775`<br>`file_mgr_dir.s:1605` | TFS GetFileInfo: copy file record to param block |
| **`GETFILEINFO_LOOP_6`** | `0x004E84` | `0x006928` | `file_mgr_dir.s:2006`<br>`file_mgr_dir.s:1815` | — |
| **`GETFILEINFO_LOOP_7`** | `0x004EAC` | `0x006950` | `file_mgr_dir.s:2019`<br>`file_mgr_dir.s:1827` | for HFS-aware callers: add extended info |
| **`GETFILEINFO_NO`** | `0x004B40` | `0x0065E0` | `file_mgr_dir.s:1581`<br>`file_mgr_dir.s:1411` | GetFileInfo/GetCatInfo common setup determine parent DirID from WDCB |
| **`GETFILEINFO_NO_10`** | `0x004E7C` | `0x006920` | `file_mgr_dir.s:2002`<br>`file_mgr_dir.s:1811` | MFS GetFileInfo: copy MFS directory entry to param block |
| **`GETFILEINFO_NO_11`** | `0x004EB4` | `0x006958` | `file_mgr_dir.s:2023`<br>`file_mgr_dir.s:1831` | — |
| **`GETFILEINFO_NO_2`** | `0x004B54` | — | `file_mgr_dir.s:1589` | check if caller specified a DirID directly |
| **`GETFILEINFO_NO_3`** | `0x004C02` | `0x0066A0` | `file_mgr_dir.s:1663`<br>`file_mgr_dir.s:1491` | check if we can resume from cached position start enumeration from beginning of directory |
| **`GETFILEINFO_NO_4`** | `0x004C68` | `0x00670C` | `file_mgr_dir.s:1713`<br>`file_mgr_dir.s:1545` | check record type: file or directory? |
| **`GETFILEINFO_NO_5`** | `0x004D66` | `0x00680A` | `file_mgr_dir.s:1815`<br>`file_mgr_dir.s:1639` | copy directory fields to param block GETFILEINFO_NO_5 |
| **`GETFILEINFO_NO_6`** | `0x004D6E` | `0x006812` | `file_mgr_dir.s:1823`<br>`file_mgr_dir.s:1647` | GETFILEINFO_NO_6 |
| **`GETFILEINFO_NO_7`** | `0x004D92` | `0x006836` | `file_mgr_dir.s:1850`<br>`file_mgr_dir.s:1669` | GETFILEINFO_NO_7 |
| **`GETFILEINFO_NO_8`** | `0x004DAC` | `0x006850` | `file_mgr_dir.s:1862`<br>`file_mgr_dir.s:1681` | GETFILEINFO_NO_8 Called during boot. |
| **`GETFILEINFO_NO_9`** | `0x004E02` | — | `file_mgr_dir.s:1919` | — |
| **`GETFILEINFO_OK`** | `0x004BBE` | `0x00665C` | `file_mgr_dir.s:1632`<br>`file_mgr_dir.s:1460` | GETFILEINFO_OK TFS GetFileInfo/GetCatInfo path |
| **`GETFILEINFO_OK_10`** | `0x004E10` | `0x0068B4` | `file_mgr_dir.s:1934`<br>`file_mgr_dir.s:1746` | GETFILEINFO_OK_10 Called during boot. |
| **`GETFILEINFO_OK_11`** | `0x004E30` | `0x0068D4` | `file_mgr_dir.s:1952`<br>`file_mgr_dir.s:1765` | GETFILEINFO_OK_11 Called during boot. |
| **`GETFILEINFO_OK_12`** | `0x004E5A` | `0x0068FE` | `file_mgr_dir.s:1972`<br>`file_mgr_dir.s:1785` | — |
| **`GETFILEINFO_OK_13`** | `0x004E64` | `0x006908` | `file_mgr_dir.s:1990`<br>`file_mgr_dir.s:1798` | GETFILEINFO_OK_13 Called during boot. found the Nth MFS file: copy name and info to param block |
| **`GETFILEINFO_OK_14`** | `0x004EB8` | — | `file_mgr_dir.s:2031` | GETFILEINFO_OK_14 Called during boot. |
| **`GETFILEINFO_OK_15`** | `0x004EC2` | `0x006964` | `file_mgr_dir.s:2041`<br>`file_mgr_dir.s:1843` | GETFILEINFO_OK_15 Called during boot. |
| **`GETFILEINFO_OK_2`** | `0x004C3A` | — | `file_mgr_dir.s:1691` | MFS compatibility mode: get offspring directly |
| **`GETFILEINFO_OK_3`** | `0x004CA4` | — | `file_mgr_dir.s:1735` | set file attributes and scan for open FCBs |
| **`GETFILEINFO_OK_4`** | `0x004CAA` | `0x00674E` | `file_mgr_dir.s:1738`<br>`file_mgr_dir.s:1570` | scan open FCBs for attribute bits |
| **`GETFILEINFO_OK_5`** | `0x004CBA` | `0x00675E` | `file_mgr_dir.s:1748`<br>`file_mgr_dir.s:1579` | GETFILEINFO_OK_5 |
| **`GETFILEINFO_OK_6`** | `0x004CE0` | `0x006784` | `file_mgr_dir.s:1768`<br>`file_mgr_dir.s:1598` | GETFILEINFO_OK_6 |
| **`GETFILEINFO_OK_7`** | `0x004D7C` | `0x006820` | `file_mgr_dir.s:1834`<br>`file_mgr_dir.s:1653` | GETFILEINFO_OK_7 |
| **`GETFILEINFO_OK_8`** | `0x004DC8` | `0x00686C` | `file_mgr_dir.s:1882`<br>`file_mgr_dir.s:1695` | — |
| **`GETFILEINFO_OK_9`** | `0x004DCC` | `0x006870` | `file_mgr_dir.s:1891`<br>`file_mgr_dir.s:1703` | GETFILEINFO_OK_9 Called during boot. |
| **`GETFILEINFO_SKIP`** | `0x004BB8` | — | `file_mgr_dir.s:1623` | copy volume name to caller's buffer |
| **`GETFILEINFO_SKIP_2`** | `0x004C34` | — | `file_mgr_dir.s:1686` | — |
| **`GETFILEINFO_SKIP_3`** | `0x004DF6` | `0x00689A` | `file_mgr_dir.s:1913`<br>`file_mgr_dir.s:1725` | check drive number and filename compare filename using _CmpString |
| **`GETFILEINFO_VOLNAME_DONE`** | — | `0x006658` | `file_mgr_dir.s:1452` | fill in synthetic root directory record copy volume name to caller's buffer if provided |
| **`GetFPos`** | `0x004F10` | `0x0069B2` | `file_mgr_io.s:18` | **Proto:** `GetFPos -- _GetFPos ($A018): FUNCTION GetFPos (refNum: INTEGER; VAR filePos: LONGINT) OSErr;`<br>File Manager -- calls on open files (refnum-based) Apple sources: TFSRFN1.a ... TFSRFN3.a and MFSRFN1.a ... MFSRFN3.a, included by TFS.a (MacSEROM.lst module TURBOFS): GetFPos, SetFPos, FileRead and F... |
| **`GETFPOS`** | `0x004F10` | `0x0069B2` | `file_mgr_io.s:14` | File Manager -- calls on open files (refnum-based) Apple sources: TFSRFN1.a ... TFSRFN3.a and MFSRFN1.a ... MFSRFN3.a, included by TFS.a (MacSEROM.lst module TURBOFS): GetFPos, SetFPos, FileRead and F... |
| **`GetHandleSize`** | `0x010190` | `0x00A6A8` | `memory_mgr.s:730` | **Proto:** `Pascal: FUNCTION GetHandleSize(h: Handle): Size;`<br>**Regs:** `Entry: A0 = h Exit:  D0.L = logical size (>= 0) and MemErr = noErr, or D0 =`<br>_GetHandleSize ($A025): return the logical size of a relocatable block Pascal: FUNCTION GetHandleSize(h: Handle): Size; Entry: A0 = h Exit:  D0.L = logical size (>= 0) and MemErr = noErr, or D0 = nilH... |
| **`GETHANDLESIZE`** | `0x010190` | `0x00A6A8` | `memory_mgr.s:428` | — |
| **`GETINDADB`** | — | `0x003D0C` | `adb_mgr.s:1133` | **Regs:** `Entry: D0 = index (1-based), A0 = ADBDataBlock pointer Exit: D0 = device address, ADBDataBlock filled`<br>GETINDADB - _GetIndADB trap: get Nth ADB device info Entry: D0 = index (1-based), A0 = ADBDataBlock pointer Exit: D0 = device address, ADBDataBlock filled |
| **`GetKeyboardModelNumber`** | `0x002590` | — | `keyboard.s:35` | GetKeyboardModelNumber -- re-send Model command to detect keyboard. |
| **`GetLTSib`** | `0x0073BA` | `0x008F12` | `file_mgr_btree.s:1752` | set up some common stuff compress remaining records adjust the offsets GetLTSib -- getLTSib: get left sibling to update its forward link. Get LT Sib |
| **`GETLTSIB`** | `0x0073BA` | `0x008F12` | `file_mgr_btree.s:1559` | close gap in record data area adjust offset table entries GetLTSib: get left sibling node |
| **`GETMAP_EXIT`** | `0x00704C` | `0x008B0E` | `file_mgr_btree.s:1260`<br>`file_mgr_btree.s:1084` | — |
| **`GETMAP_GETNODE`** | `0x00701E` | `0x008AE0` | `file_mgr_btree.s:1240`<br>`file_mgr_btree.s:1065` | release current map node GMGetNode: get next map node |
| **`GETMAP_LOCREC`** | `0x007034` | `0x008AF6` | `file_mgr_btree.s:1250`<br>`file_mgr_btree.s:1074` | locate map record and calculate its size |
| **`GetMaxKey`** | `0x0073F6` | `0x008F4C` | `file_mgr_btree.s:1797` | GetMaxKey -- max key length + 4. Get Max Key |
| **`GETMAXKEY`** | `0x0073F6` | `0x008F4C` | `file_mgr_btree.s:1595` | GetMaxKey: return max key length rounded to even Called by: BTINS_NEWROOT, BTINS_RELLEFT, GETBTVARSIZE, BUILDIREC |
| **`GetNode`** | `0x007408` | `0x008F58` | `file_mgr_btree.s:1818` | Get Node |
| **`GETNODE`** | `0x007408` | `0x008F58` | `file_mgr_btree.s:1603` | GetNode: read a B-tree node from cache with validation Called by: BTDEL_GETPAR, BTDEL_UPDDEPTH, VBTFLUSH, GR_GETNODE, BTINS_NXTLEV (and 5 more) |
| **`GETNODE_EXIT`** | `0x007432` | `0x008F88` | `file_mgr_btree.s:1833`<br>`file_mgr_btree.s:1622` | invalid node: release block and return error |
| **`GetNodeSiz`** | `0x00743C` | `0x008F92` | `file_mgr_btree.s:1844` | GetNodeSiz -- get its size. Get Node Siz |
| **`GETNODESIZ`** | `0x00743C` | `0x008F92` | `file_mgr_btree.s:1628` | GetNodeSiz: return total data size of node (records + offsets) |
| **`GetOffset`** | `0x007454` | `0x008FAA` | `file_mgr_btree.s:1861` | GetOffset -- get offset for record D0. Get Offset Called by: DeleteRec, GetRecA, InsertRec, ChkNode, GetNodeSiz |
| **`GETOFFSET`** | `0x007454` | `0x008FAA` | `file_mgr_btree.s:1640` | GetOffset: get offset value for record index D0 in node A1 Called by: DELETEREC, GETRECA, INSERTREC, CHKNODE, GETNODESIZ |
| **`GetOSEvent`** | `0x0027EC` | `0x003FE6` | `event_mgr.s:179` | _GetOSEvent ($A031) Dequeues the highest-priority event matching the mask in D0. Calls OSEventAvail to find a match, then removes it from the queue. On exit: D0 = 0 if event found (Z set), event recor... |
| **`GETOSEVENT`** | `0x0027EC` | `0x003FE6` | `event_mgr.s:170` | _GetOSEvent ($A031) -- dequeue + return matching event D0 = mask. Calls OSEVENTAVAIL to find a matching event, then dequeues and invalidates the slot via ADB_DEQUEUE_INVALIDATE. |
| **`GETOSEVENT_DONE`** | `0x0027FC` | — | `event_mgr.s:186` | — |
| **`GetPtrSize`** | `0x010108` | `0x00A620` | `memory_mgr.s:563` | _GetPtrSize ($A021) A0 = ptr -> D0.L = size |
| **`GETPTRSIZE`** | `0x010108` | `0x00A620` | `memory_mgr.s:353` | — |
| **`GetRecA`** | `0x00746E` | `0x008FC2` | `file_mgr_btree.s:1885` | GetRecA -- parent index record. Get Rec A Called by: BTDEL_GETPAR, BTINS_NXTLEV, GETMAP_LOCREC, LocRec, ROTLT_ADJINDX (and 3 more) |
| **`GETRECA`** | `0x00746E` | `0x008FC2` | `file_mgr_btree.s:1660` | GetRecA: get record address and size for index D0 in node A1 Returns: A0=record ptr, D0=record size Called by: BTDEL_GETPAR, BTINS_NXTLEV, GETMAP_LOCREC, LOCREC, ROTLT_SKIPADJ (and 3 more) |
| **`GetRTSib`** | `0x0073C4` | `0x008F1C` | `file_mgr_btree.s:1763` | GetRTSib -- getRTSib: get right sibling node. Get RT Sib |
| **`GETRTSIB`** | `0x0073C4` | `0x008F1C` | `file_mgr_btree.s:1565` | GetRTSib: get right sibling node |
| **`GETSIB_COMMON`** | `0x0073CC` | `0x008F24` | `file_mgr_btree.s:1767`<br>`file_mgr_btree.s:1569` | — |
| **`GETSIB_DOREAD`** | — | `0x008F36` | `file_mgr_btree.s:1580` | — |
| **`GETSIB_EXIT`** | `0x0073EC` | `0x008F42` | `file_mgr_btree.s:1786`<br>`file_mgr_btree.s:1588` | — |
| **`GETSIB_GETNODE`** | `0x0073D8` | — | `file_mgr_btree.s:1774` | — |
| **`GETSIB_NOERR`** | `0x0073EA` | `0x008F40` | `file_mgr_btree.s:1784`<br>`file_mgr_btree.s:1586` | — |
| **`GETSIB_READ`** | `0x0073DE` | — | `file_mgr_btree.s:1778` | — |
| **`GETSIB_RIGHT`** | `0x0073D6` | `0x008F2E` | `file_mgr_btree.s:1772`<br>`file_mgr_btree.s:1574` | — |
| **`GETSIB_TEST`** | — | `0x008F30` | `file_mgr_btree.s:1576` | — |
| **`GetSize`** | `0x0108E0` | `0x00AE9E` | `memory_mgr.s:2224` | **Regs:** `Entry: A0 = block data pointer Exit:  D0.L = physical size - 8 - size correction; A0 and D1 preserved`<br>GetSize - logical size of a block Entry: A0 = block data pointer Exit:  D0.L = physical size - 8 - size correction; A0 and D1 preserved Called during boot (24,078 times in 30s trace). |
| **`GETSIZE`** | `0x0108E0` | `0x00AE9E` | `memory_mgr.s:1609` | Called by: GETPTRSIZE, GETHANDLESIZE, REALLOCHANDLE_LOCKED, SETSIZE, MAKEPTRSPC_SKIP_3 (and 1 more) |
| **`GetTrapAddress`** | `0x00200A` | `0x002D8E` | `trap_dispatch.s:158` | _GetTrapAddress ($A146) - NGetTrapAddress On entry: D0 = trap word, D1 = trap word On exit: A0 = handler address from dispatch table Bit 9 of D1: 1 = "new" interface (bit 10 selects OS vs Toolbox) 0 =... |
| **`GETTRAPADDRESS`** | `0x00200A` | `0x002D8E` | `trap_dispatch.s:139` | **Regs:** `Entry: D0 = trap number Exit: A0 = handler address`<br>GETTRAPADDRESS - _GetTrapAddress trap handler Returns the dispatch table entry for trap D0 in A0. D1 bit 9: new-style, D1 bit 10: 1 = Toolbox, 0 = OS Entry: D0 = trap number Exit: A0 = handler address |
| **`GetVCBRFN`** | `0x002CA6` | `0x0046EE` | `file_mgr_vol.s:181` | GetVCBRFN - find VCB by drive refnum in D0 Searches the VCB queue for a volume whose vcbDRefNum (offset 0x4E=78) matches D0. Returns A2 -> VCB if found (Z=1), or nsvErr (-35) if not. |
| **`GETVCBRFN`** | `0x002CA6` | `0x0046EE` | `file_mgr_vol.s:163` | **Regs:** `Entry: D0 = volume refNum Exit: A2 = VCB pointer if found, D0 = nsvErr (-35) if not`<br>GETVCBRFN - find VCB by volume reference number Searches VCB queue for vcbVRefNum (offset 0x4E = 78) == D0. Entry: D0 = volume refNum Exit: A2 = VCB pointer if found, D0 = nsvErr (-35) if not |
| **`GETVCBRFN_NSVERR`** | `0x002CBC` | `0x004704` | `file_mgr_vol.s:196`<br>`file_mgr_vol.s:173` | GETVCBRFN_NSVERR - VCB not found, return nsvErr (-35) |
| **`GETVCBRFN_RET`** | `0x002CB6` | `0x0046FE` | `file_mgr_vol.s:188`<br>`file_mgr_vol.s:170` | — |
| **`GetVol`** | `0x003A8A` | `0x005516` | `file_mgr_vol.s:1908` | _GetVol ($A014) Called during boot. |
| **`GETVOL`** | `0x003A8A` | `0x005516` | `file_mgr_vol.s:1754` | _GetVol / _HGetVol: get current default volume |
| **`GETVOL_CONT`** | `0x003AA6` | — | `file_mgr_vol.s:1917` | — |
| **`GETVOL_CONT_2`** | `0x003AAE` | `0x00553A` | `file_mgr_vol.s:1934`<br>`file_mgr_vol.s:1778` | GETVOL_CONT_2 Called during boot. GETVOL_CONT_2: copy volume name to caller's buffer (for GetVol) |
| **`GETVOL_DEFAULT_DONE`** | — | `0x005532` | `file_mgr_vol.s:1763` | — |
| **`GETVOL_LOOP`** | `0x003ACC` | `0x005558` | `file_mgr_vol.s:1945`<br>`file_mgr_vol.s:1789` | — |
| **`GETVOL_NO`** | `0x003AAA` | `0x005536` | `file_mgr_vol.s:1924`<br>`file_mgr_vol.s:1769` | GETVOL_NO |
| **`GETVOL_SKIP`** | `0x003AD2` | `0x00555E` | `file_mgr_vol.s:1948`<br>`file_mgr_vol.s:1792` | — |
| **`GetVolInfo`** | `0x003824` | `0x0052B2` | `file_mgr_vol.s:1639` | _GetVolInfo ($A007) A0 = paramBlock -> D0 = error; returns volume info Called during boot. _GetVolInfo ($A007): return volume information |
| **`GETVOLINFO`** | `0x003824` | `0x0052B2` | `file_mgr_vol.s:1505` | _GetVolInfo / PBHGetVInfo: get volume information |
| **`GETVOLINFO_BY_REFNUM`** | — | `0x0052C8` | `file_mgr_vol.s:1514` | — |
| **`GETVOLINFO_CONT`** | `0x00383A` | — | `file_mgr_vol.s:1649` | use ioVRefNum to find volume |
| **`GETVOLINFO_CONT_2`** | `0x003840` | `0x0052CE` | `file_mgr_vol.s:1653`<br>`file_mgr_vol.s:1518` | index into VCB queue |
| **`GETVOLINFO_CONT_3`** | `0x00384A` | — | `file_mgr_vol.s:1658` | scan VCB queue by index |
| **`GETVOLINFO_CONT_4`** | `0x00386E` | `0x0052FC` | `file_mgr_vol.s:1675`<br>`file_mgr_vol.s:1539` | check if volume has open files (set ioVAtrb bit 6) |
| **`GETVOLINFO_CONT_5`** | `0x0038BE` | `0x00534A` | `file_mgr_vol.s:1706`<br>`file_mgr_vol.s:1570` | check if it's a WD reference |
| **`GETVOLINFO_CONT_6`** | `0x0038C8` | `0x005354` | `file_mgr_vol.s:1710`<br>`file_mgr_vol.s:1574` | — |
| **`GETVOLINFO_CONT_7`** | `0x003916` | `0x0053A2` | `file_mgr_vol.s:1744`<br>`file_mgr_vol.s:1607` | — |
| **`GETVOLINFO_CONT_8`** | `0x0039B8` | `0x005444` | `file_mgr_vol.s:1797`<br>`file_mgr_vol.s:1659` | copy Finder info (32 bytes) |
| **`GETVOLINFO_DONE`** | — | `0x005456` | `file_mgr_vol.s:1667` | — |
| **`GETVOLINFO_EMPTY`** | `0x003836` | — | `file_mgr_vol.s:1647` | use ioVRefNum to find volume |
| **`GETVOLINFO_ERR`** | `0x003902` | `0x00538E` | `file_mgr_vol.s:1734`<br>`file_mgr_vol.s:1597` | look up directory valence from catalog GETVOLINFO_ERR |
| **`GETVOLINFO_ERR_2`** | `0x0039CA` | — | `file_mgr_vol.s:1805` | — |
| **`GETVOLINFO_EXIT`** | `0x003858` | `0x0052E6` | `file_mgr_vol.s:1666`<br>`file_mgr_vol.s:1530` | GETVOLINFO_EXIT: copy VCB info to param block |
| **`GETVOLINFO_EXIT_2`** | `0x003952` | `0x0053DE` | `file_mgr_vol.s:1773`<br>`file_mgr_vol.s:1634` | GETVOLINFO_EXIT_2 Called during boot. GETVOLINFO_EXIT_2: return extended HFS volume info (for HFS-aware callers) |
| **`GETVOLINFO_FOUND`** | `0x003894` | `0x005320` | `file_mgr_vol.s:1688`<br>`file_mgr_vol.s:1552` | check if this is the default volume |
| **`GETVOLINFO_INDEX_LOOP`** | — | `0x0052D8` | `file_mgr_vol.s:1522` | — |
| **`GETVOLINFO_LOOP`** | `0x00385A` | `0x0052E8` | `file_mgr_vol.s:1668`<br>`file_mgr_vol.s:1532` | — |
| **`GETVOLINFO_NEXT_FCB`** | — | `0x005314` | `file_mgr_vol.s:1547` | — |
| **`GETVOLINFO_NO`** | `0x003888` | — | `file_mgr_vol.s:1683` | — |
| **`GETVOLINFO_NO_2`** | `0x0038A6` | `0x005332` | `file_mgr_vol.s:1694`<br>`file_mgr_vol.s:1558` | determine WDCB for directory info |
| **`GETVOLINFO_NO_3`** | `0x003930` | `0x0053BC` | `file_mgr_vol.s:1753`<br>`file_mgr_vol.s:1615` | for TFS: subtract extent/catalog B-tree blocks from free count |
| **`GETVOLINFO_NO_4`** | `0x003950` | `0x0053DC` | `file_mgr_vol.s:1764`<br>`file_mgr_vol.s:1626` | for MFS compatibility: cap at 31KB max |
| **`GETVOLINFO_OK`** | `0x003910` | `0x00539C` | `file_mgr_vol.s:1742`<br>`file_mgr_vol.s:1605` | — |
| **`GETVOLINFO_RESOLVE`** | — | `0x0052C4` | `file_mgr_vol.s:1512` | — |
| **`GETVOLINFO_SKIP`** | `0x003906` | `0x005392` | `file_mgr_vol.s:1737`<br>`file_mgr_vol.s:1600` | set return VRefNum |
| **`GETVOLINFO_SKIP_2`** | `0x0039C8` | `0x005454` | `file_mgr_vol.s:1803`<br>`file_mgr_vol.s:1665` | — |
| **`GETWDINFO`** | — | `0x0056E4` | `file_mgr_vol.s:1975` | _GetWDInfo: get working directory information |
| **`GETWDINFO_DONE`** | — | `0x0056FC` | `file_mgr_vol.s:1985` | — |
| **`GETWDINFO_FOUND_FILL`** | — | `0x00578A` | `file_mgr_vol.s:2050` | — |
| **`GetWDInfo_hfs`** | `0x003C58` | — | `file_mgr_vol.s:2173` | Get WD Info_hfs _GetWDInfo (HFS): return working directory info |
| **`GETWDINFO_HFS_CONT`** | `0x003C74` | `0x005700` | `file_mgr_vol.s:2191`<br>`file_mgr_vol.s:1988` | GETWDINFO_HFS_CONT GETWDINFO_HFS_CONT/GetWDInfo common: get WD info by refnum or index |
| **`GETWDINFO_HFS_CONT_2`** | `0x003CA4` | `0x005732` | `file_mgr_vol.s:2209`<br>`file_mgr_vol.s:2007` | get by VRefNum not a WD: return root directory info valid WD reference: get WDCB info |
| **`GETWDINFO_HFS_CONT_3`** | `0x003CFA` | `0x005788` | `file_mgr_vol.s:2255`<br>`file_mgr_vol.s:2048` | found the Nth matching WDCB: fill param block |
| **`GETWDINFO_HFS_CONT_4`** | `0x003CFC` | — | `file_mgr_vol.s:2257` | — |
| **`GETWDINFO_HFS_ERR`** | `0x003C70` | `0x0056E0` | `file_mgr_vol.s:2183`<br>`file_mgr_vol.s:1972` | — |
| **`GETWDINFO_HFS_ERR_2`** | `0x003D00` | `0x00578E` | `file_mgr_vol.s:2259`<br>`file_mgr_vol.s:2052` | — |
| **`GETWDINFO_HFS_NO`** | `0x003CC4` | `0x005752` | `file_mgr_vol.s:2230`<br>`file_mgr_vol.s:2022` | GetWDInfo indexed: scan WDCBs by index, with procID and volume filters |
| **`GETWDINFO_HFS_NO_2`** | `0x003CEC` | `0x00577A` | `file_mgr_vol.s:2247`<br>`file_mgr_vol.s:2039` | filter by procID filter by volume |
| **`GETWDINFO_HFS_NO_3`** | `0x003CF6` | `0x005784` | `file_mgr_vol.s:2252`<br>`file_mgr_vol.s:2044` | — |
| **`GETWDINFO_HFS_OK`** | `0x003CB2` | `0x005740` | `file_mgr_vol.s:2221`<br>`file_mgr_vol.s:2014` | GETWDINFO_HFS_OK GetWDInfo by index: determine volume filter first |
| **`GETWDINFO_HFS_SKIP`** | `0x003CD6` | — | `file_mgr_vol.s:2236` | — |
| **`GETWDINFO_INDEX_LOOP`** | — | `0x005764` | `file_mgr_vol.s:2029` | scan WDCB array matching procID and volume filters |
| **`GetZone`** | `0x00FFA4` | `0x00A4B4` | `memory_mgr.s:231` | **Proto:** `Pascal: FUNCTION GetZone: THz;`<br>**Regs:** `Exit:  A0 = TheZone; D0.W = noErr, MemErr cleared (INITZONE_EXIT)`<br>_GetZone ($A11A): return a pointer to the current heap zone Pascal: FUNCTION GetZone: THz; Exit:  A0 = TheZone; D0.W = noErr, MemErr cleared (INITZONE_EXIT) Toolbox trap $A81A dispatches here as well ... |
| **`GETZONE`** | `0x00FFA4` | `0x00A4B4` | `memory_mgr.s:189` | — |
| **`GO_CHK_PARENT`** | `0x0062A4` | `0x007D70` | `file_mgr_catalog.s:297`<br>`file_mgr_catalog.s:260` | — |
| **`GO_EXIT`** | `0x0062AE` | `0x007D7A` | `file_mgr_catalog.s:302`<br>`file_mgr_catalog.s:265` | GOExit |
| **`GO_GET_OFF`** | `0x006286` | `0x007D52` | `file_mgr_catalog.s:284`<br>`file_mgr_catalog.s:247` | GOGetOff: get offspring record |
| **`GO_INVAL_EXIT`** | `0x00629E` | `0x007D6A` | `file_mgr_catalog.s:294`<br>`file_mgr_catalog.s:257` | — |
| **`GO_LOCATE_THD`** | `0x006270` | `0x007D3C` | `file_mgr_catalog.s:275`<br>`file_mgr_catalog.s:238` | GOLocateThd: locate thread record to establish position |
| **`GO_NOT_FOUND`** | `0x00629C` | `0x007D68` | `file_mgr_catalog.s:292`<br>`file_mgr_catalog.s:255` | — |
| **`GR_GETNODE`** | `0x0069C0` | `0x00848C` | `file_mgr_btree.s:416`<br>`file_mgr_btree.s:351` | GR_GETNODE - GRGetNode: releases current node and gets next |
| **`GR_RELNODE`** | `0x0069D8` | `0x0084A2` | `file_mgr_btree.s:433`<br>`file_mgr_btree.s:364` | GR_RELNODE - GRRelNode: releases current node buffer |
| **`GRGETNODE_EXIT`** | `0x0069D2` | `0x00849C` | `file_mgr_btree.s:424`<br>`file_mgr_btree.s:359` | — |
| **`HandleZone`** | `0x0101AE` | `0x00A6C6` | `memory_mgr.s:773` | _HandleZone ($A126): return zone containing handle's block A0 = handle -> A0 = zone pointer |
| **`HANDLEZONE`** | `0x0101AE` | `0x00A6C6` | `memory_mgr.s:449` | — |
| **`HEAP`** | — | `0x00A352` | `memory_mgr.s:49` | Memory Manager Apple sources: MemoryMgr.a and MemoryMgrInternal.a (MacSEROM.lst modules HEAP, HEAPGUTS) and BlockMove.a (module BLOCK2). Manages heap zones for dynamic memory allocation. Provides NewH... |
| **`HEAPGUTS`** | — | `0x00A9B8` | `memory_mgr.s:853` | HEAPGUTS -- dereference a handle: A1 = handle A0 masked to 24 bits, A0 = D0 = its master pointer (0 for a nil handle); Z set if the handle or the master pointer is nil. (Apple module HEAPGUTS starts h... |
| **`HFLAGS_SET_MEMERR`** | — | `0x00A774` | `memory_mgr.s:530` | — |
| **`HFS_DISPATCH_TABLE`** | `0x002872` | `0x0042B4` | `file_mgr_queue.s:60`<br>`file_mgr_queue.s:56` | HFS_DISPATCH_TABLE - HFS dispatch relative offset table (18 word entries) Each word is a signed offset from the start of HFS_DISPATCH_TABLE to the corresponding HFS routine. Selector 0 -> HFS_MOUNTVOL... |
| **`HFS_MOUNTVOL`** | `0x002896` | — | `file_mgr_queue.s:69` | HFS selector 0: MountVol - stamp ioMisc with version string |
| **`hfsC`** | `0x0037F6` | — | `file_mgr_vol.s:1616` | hfs C hfsC: _HSetFLock / _SetFLock HFS dispatch (set HFS flags) |
| **`HFSC_OK`** | `0x00381E` | — | `file_mgr_vol.s:1628` | — |
| **`HFSC_SKIP`** | `0x003808` | `0x005296` | `file_mgr_vol.s:1622`<br>`file_mgr_vol.s:1495` | — |
| **`hfsCatMove`** | `0x004630` | — | `file_mgr_dir.s:895` | copy new name to VCB volume name if TFS volume, also rename root directory in catalog hfs Cat Move _CatMove (HFS): move a file/directory to a different parent |
| **`HFSCATMOVE_CONT`** | `0x004718` | `0x0061BE` | `file_mgr_dir.s:1001`<br>`file_mgr_dir.s:910` | — |
| **`HFSCATMOVE_CONT_2`** | `0x004766` | `0x00620C` | `file_mgr_dir.s:1040`<br>`file_mgr_dir.s:943` | HFSCATMOVE_CONT_2 - MFS: compute directory entry size from name length |
| **`HFSCATMOVE_CONT_3`** | `0x004776` | `0x00621C` | `file_mgr_dir.s:1051`<br>`file_mgr_dir.s:949` | **Regs:** `HFSCATMOVE_CONT_3 - MFSDeleteEntry: remove entry by compressing directory`<br>HFSCATMOVE_CONT_3 - MFSDeleteEntry: remove entry by compressing directory |
| **`HFSCATMOVE_CONT_4`** | `0x00478E` | `0x006234` | `file_mgr_dir.s:1061`<br>`file_mgr_dir.s:959` | compress directory: shift entries after deleted one |
| **`HFSCATMOVE_CONT_5`** | `0x0047C8` | `0x00626E` | `file_mgr_dir.s:1103`<br>`file_mgr_dir.s:1000` | do the rename |
| **`HFSCATMOVE_CONT_6`** | `0x004838` | `0x0062DE` | `file_mgr_dir.s:1167`<br>`file_mgr_dir.s:1059` | HFSCATMOVE_CONT_6 HFSCATMOVE_CONT_6: find all FCBs for this MFS file and update them |
| **`HFSCATMOVE_DONE`** | `0x004796` | `0x00623C` | `file_mgr_dir.s:1072`<br>`file_mgr_dir.s:969` | HFSCATMOVE_DONE clear remaining words in directory block |
| **`HFSCATMOVE_ERR`** | `0x004658` | — | `file_mgr_dir.s:911` | determine destination directory determine source directory |
| **`HFSCATMOVE_ERR_2`** | `0x00465A` | — | `file_mgr_dir.s:913` | determine destination directory determine source directory |
| **`HFSCATMOVE_ERR_3`** | `0x004708` | `0x0061B0` | `file_mgr_dir.s:993`<br>`file_mgr_dir.s:902` | call CMMoveCN to move the catalog entry |
| **`HFSCATMOVE_ERR_4`** | `0x004816` | — | `file_mgr_dir.s:1141` | — |
| **`HFSCATMOVE_ERR_5`** | `0x00481A` | `0x0062C0` | `file_mgr_dir.s:1144`<br>`file_mgr_dir.s:1041` | MFS Rename: entry moved - need to re-insert at new position |
| **`HFSCATMOVE_ERR_6`** | `0x004850` | — | `file_mgr_dir.s:1176` | — |
| **`HFSCATMOVE_FOUND`** | `0x0047C2` | `0x006268` | `file_mgr_dir.s:1099`<br>`file_mgr_dir.s:995` | different name: check if new name already exists |
| **`HFSCATMOVE_FOUND_2`** | `0x00482A` | `0x0062D0` | `file_mgr_dir.s:1152`<br>`file_mgr_dir.s:1049` | copy saved entry to new position |
| **`HFSCATMOVE_LOOP`** | `0x0047DC` | `0x006282` | `file_mgr_dir.s:1113`<br>`file_mgr_dir.s:1010` | save old directory entry on A6 stack |
| **`HFSCATMOVE_LOOP_2`** | `0x0047F4` | `0x00629A` | `file_mgr_dir.s:1126`<br>`file_mgr_dir.s:1022` | delete old entry and insert with new name copy saved entry data to new location copy saved entry data back to new location |
| **`HFSCATMOVE_NO`** | `0x004684` | `0x00612C` | `file_mgr_dir.s:937`<br>`file_mgr_dir.s:847` | find source file in catalog find destination directory |
| **`HFSCATMOVE_NO_2`** | `0x0046D2` | `0x00617A` | `file_mgr_dir.s:970`<br>`file_mgr_dir.s:879` | hfsCatMove: move a catalog entry to a different directory |
| **`HFSCATMOVE_NO_3`** | `0x00472C` | `0x0061D2` | `file_mgr_dir.s:1015`<br>`file_mgr_dir.s:919` | HFSCATMOVE_NO_3 MFS Delete path |
| **`HFSCATMOVE_NO_4`** | `0x0047A2` | `0x006248` | `file_mgr_dir.s:1084`<br>`file_mgr_dir.s:980` | HFSCATMOVE_NO_4 MFS Rename: compare old and new names, then rename |
| **`HFSCATMOVE_NO_5`** | `0x00482C` | `0x0062D2` | `file_mgr_dir.s:1154`<br>`file_mgr_dir.s:1051` | — |
| **`HFSCATMOVE_OK`** | `0x00465E` | — | `file_mgr_dir.s:921` | HFSCATMOVE_OK check write protect and find source file |
| **`HFSCATMOVE_OK_2`** | `0x0046C6` | `0x00616E` | `file_mgr_dir.s:964`<br>`file_mgr_dir.s:873` | temporarily swap to dest name for lookup HFSCATMOVE_OK_2 hfsCatMove: check dest is a directory and get its DirID |
| **`HFSCATMOVE_OK_3`** | `0x00470C` | `0x0061B4` | `file_mgr_dir.s:996`<br>`file_mgr_dir.s:905` | update open FCBs with new parent DirID and hint |
| **`HFSCATMOVE_OK_4`** | `0x004726` | — | `file_mgr_dir.s:1006` | — |
| **`HFSCATMOVE_OK_5`** | `0x004762` | — | `file_mgr_dir.s:1033` | delete MFS file: deallocate blocks and remove directory entry |
| **`HFSCATMOVE_OK_6`** | `0x004804` | `0x0062AA` | `file_mgr_dir.s:1133`<br>`file_mgr_dir.s:1029` | MFS Rename: copy new name bytes into directory entry |
| **`HFSCATMOVE_OK_7`** | `0x004846` | `0x0062EC` | `file_mgr_dir.s:1172`<br>`file_mgr_dir.s:1064` | — |
| **`hfsD`** | `0x003D60` | — | `file_mgr_vol.s:2320` | hfs D hfsD: _OpenWD HFS dispatch (open a working directory) |
| **`HFSD_CONT`** | `0x003D7E` | `0x005818` | `file_mgr_vol.s:2330`<br>`file_mgr_vol.s:2112` | — |
| **`HFSD_ERR`** | `0x003D80` | `0x00581A` | `file_mgr_vol.s:2332`<br>`file_mgr_vol.s:2114` | — |
| **`hfsE`** | `0x003D8A` | — | `file_mgr_vol.s:2341` | hfsE: _SetVol HFS dispatch (set default directory) |
| **`HFSE_CONT`** | `0x003DAA` | `0x005844` | `file_mgr_vol.s:2358`<br>`file_mgr_vol.s:2136` | HFSE_CONT Called during boot. MV_GetMFSMap: set up MFS volume - allocate alloc map and read it from disk |
| **`HFSE_CONT_10`** | `0x003F9A` | — | `file_mgr_vol.s:2644` | HFSE_CONT_10 |
| **`HFSE_CONT_11`** | `0x003FB0` | `0x005A4A` | `file_mgr_vol.s:2658`<br>`file_mgr_vol.s:2404` | — |
| **`HFSE_CONT_12`** | `0x003FB8` | `0x005A52` | `file_mgr_vol.s:2668`<br>`file_mgr_vol.s:2410` | — |
| **`HFSE_CONT_13`** | `0x003FCE` | `0x005A68` | `file_mgr_vol.s:2683`<br>`file_mgr_vol.s:2425` | — |
| **`HFSE_CONT_14`** | `0x003FF2` | `0x005A8C` | `file_mgr_vol.s:2704`<br>`file_mgr_vol.s:2448` | HFSE_CONT_14 Called during boot. |
| **`HFSE_CONT_15`** | `0x004002` | `0x005A9C` | `file_mgr_vol.s:2724`<br>`file_mgr_vol.s:2471` | HFSE_CONT_15 Called during boot. |
| **`HFSE_CONT_16`** | `0x004004` | `0x005A9E` | `file_mgr_vol.s:2726`<br>`file_mgr_vol.s:2473` | HFSE_CONT_15 HFSE_CONT_15: find FCB by file number + volume D2 = file number, A2 = VCB Returns: D1 = FCB offset, Z set if found Called during boot. |
| **`HFSE_CONT_2`** | `0x003DF6` | `0x005890` | `file_mgr_vol.s:2409`<br>`file_mgr_vol.s:2181` | HFSE_CONT_2 HFSE_CONT_2: dispose MFS alloc map memory |
| **`HFSE_CONT_3`** | `0x003E0A` | `0x0058A4` | `file_mgr_vol.s:2422`<br>`file_mgr_vol.s:2189` | HFSE_CONT_3: MFS consistency check - count free blocks in alloc map Called during boot. |
| **`HFSE_CONT_4`** | `0x003E0E` | `0x0058A8` | `file_mgr_vol.s:2425`<br>`file_mgr_vol.s:2192` | — |
| **`HFSE_CONT_5`** | `0x003E44` | `0x0058DE` | `file_mgr_vol.s:2465`<br>`file_mgr_vol.s:2222` | scan MFS directory entries in this block |
| **`HFSE_CONT_6`** | `0x003E88` | `0x005922` | `file_mgr_vol.s:2493`<br>`file_mgr_vol.s:2252` | directory scan complete: update VCB counters |
| **`HFSE_CONT_7`** | `0x003EAA` | `0x005944` | `file_mgr_vol.s:2514`<br>`file_mgr_vol.s:2273` | HFSE_CONT_7 Called during boot. HFSE_CONT_7: MFS alloc chain walk - compute PEOF from chain and update directory |
| **`HFSE_CONT_8`** | `0x003EE0` | `0x00597A` | `file_mgr_vol.s:2541`<br>`file_mgr_vol.s:2300` | — |
| **`HFSE_CONT_9`** | `0x003F00` | `0x00599A` | `file_mgr_vol.s:2564`<br>`file_mgr_vol.s:2322` | HFSE_CONT_9 Called during boot. HFSE_CONT_9: MFS FlushVol - flush VCB info back to MDB on disk |
| **`HFSE_COPY_VOLNAME_DONE`** | — | `0x005A88` | `file_mgr_vol.s:2439` | — |
| **`HFSE_DEALLOC_THEN_DEQUEUE`** | — | `0x005A24` | `file_mgr_vol.s:2386` | — |
| **`HFSE_ERR`** | `0x003DEE` | `0x005888` | `file_mgr_vol.s:2398`<br>`file_mgr_vol.s:2171` | — |
| **`HFSE_ERR_2`** | `0x003DF0` | `0x00588A` | `file_mgr_vol.s:2400`<br>`file_mgr_vol.s:2173` | — |
| **`HFSE_ERR_3`** | `0x003E42` | `0x0058DC` | `file_mgr_vol.s:2463`<br>`file_mgr_vol.s:2219` | — |
| **`HFSE_ERR_4`** | `0x003EA2` | `0x00593C` | `file_mgr_vol.s:2504`<br>`file_mgr_vol.s:2263` | — |
| **`HFSE_ERR_5`** | `0x003EBC` | `0x005956` | `file_mgr_vol.s:2522`<br>`file_mgr_vol.s:2281` | walk the alloc chain |
| **`HFSE_ERR_6`** | `0x003F8E` | `0x005A28` | `file_mgr_vol.s:2632`<br>`file_mgr_vol.s:2388` | — |
| **`HFSE_ERR_7`** | `0x003F90` | — | `file_mgr_vol.s:2634` | — |
| **`HFSE_ERR_8`** | `0x003FEE` | — | `file_mgr_vol.s:2696` | — |
| **`HFSE_ERR_9`** | `0x004010` | `0x005AAA` | `file_mgr_vol.s:2733`<br>`file_mgr_vol.s:2479` | HFSE_ERR_9 -- gtNxtMatch: find next matching FCB. Called by: FILEOPEN_SKIP, PERMSSNCHK_NO_2, RENAME_CONT_2, HFSCATMOVE_CONT, HFSCATMOVE_OK_7 (and 2 more) |
| **`HFSE_ERR_RESTORE`** | — | `0x005A2A` | `file_mgr_vol.s:2390` | — |
| **`HFSE_FLUSH_VOL_CACHES`** | — | `0x005A0A` | `file_mgr_vol.s:2375` | flush caches for this volume |
| **`HFSE_LOOP`** | `0x003F32` | `0x0059CC` | `file_mgr_vol.s:2583`<br>`file_mgr_vol.s:2342` | write-protect check and read MDB block copy VCB info to MDB |
| **`HFSE_NEXT`** | `0x003FFA` | `0x005A94` | `file_mgr_vol.s:2714`<br>`file_mgr_vol.s:2459` | HFSE_NEXT Called during boot (1,205 times in 30s trace). |
| **`HFSE_NO`** | `0x003DCE` | `0x005868` | `file_mgr_vol.s:2376`<br>`file_mgr_vol.s:2154` | compute alloc map size: (NmAlBlks * 1.5 + 1) / 2 bytes (12 bits per entry) allocate alloc map and read it from MDB copy alloc map from MDB block(s) to memory |
| **`HFSE_NO_2`** | `0x003DEA` | `0x005884` | `file_mgr_vol.s:2395`<br>`file_mgr_vol.s:2168` | need next disk block for more alloc map data HFSE_NO_2 Called during boot. |
| **`HFSE_NO_3`** | `0x003E16` | `0x0058B0` | `file_mgr_vol.s:2429`<br>`file_mgr_vol.s:2196` | — |
| **`HFSE_NO_4`** | `0x003E56` | `0x0058F0` | `file_mgr_vol.s:2474`<br>`file_mgr_vol.s:2231` | track max file number for VCBNxtCNID verify alloc map entries for data and resource forks |
| **`HFSE_NO_5`** | `0x003ED0` | `0x00596A` | `file_mgr_vol.s:2532`<br>`file_mgr_vol.s:2291` | MFS FClose: update directory entry from FCB |
| **`HFSE_NO_6`** | `0x003EE6` | `0x005980` | `file_mgr_vol.s:2545`<br>`file_mgr_vol.s:2304` | — |
| **`HFSE_NO_7`** | `0x003F42` | `0x0059DC` | `file_mgr_vol.s:2590`<br>`file_mgr_vol.s:2349` | copy alloc map to MDB (offset $40 in MDB block) |
| **`HFSE_NO_8`** | `0x003F62` | `0x0059FC` | `file_mgr_vol.s:2608`<br>`file_mgr_vol.s:2368` | HFSE_NO_8 |
| **`HFSE_NO_9`** | `0x003F76` | `0x005A10` | `file_mgr_vol.s:2623`<br>`file_mgr_vol.s:2379` | MFS unmount path |
| **`HFSE_NO_OPEN_FILES`** | — | `0x005A78` | `file_mgr_vol.s:2431` | — |
| **`HFSE_OK`** | `0x003E20` | `0x0058BA` | `file_mgr_vol.s:2440`<br>`file_mgr_vol.s:2201` | HFSE_OK: compare counted free blocks with VCB Called during boot. |
| **`HFSE_OK_10`** | `0x003FB4` | `0x005A4E` | `file_mgr_vol.s:2666`<br>`file_mgr_vol.s:2408` | HFSE_OK_10 |
| **`HFSE_OK_11`** | `0x003FC6` | `0x005A60` | `file_mgr_vol.s:2680`<br>`file_mgr_vol.s:2422` | HFSE_OK_11 |
| **`HFSE_OK_12`** | `0x003FDE` | — | `file_mgr_vol.s:2689` | — |
| **`HFSE_OK_13`** | `0x003FE0` | `0x005A7A` | `file_mgr_vol.s:2691`<br>`file_mgr_vol.s:2434` | copy VCB info to param block |
| **`HFSE_OK_14`** | `0x004018` | `0x005AB2` | `file_mgr_vol.s:2737`<br>`file_mgr_vol.s:2483` | — |
| **`HFSE_OK_2`** | `0x003E26` | `0x0058C0` | `file_mgr_vol.s:2449`<br>`file_mgr_vol.s:2205` | HFSE_OK_2: MFS mount - initialize directory scan counters Called during boot. |
| **`HFSE_OK_3`** | `0x003E32` | `0x0058CC` | `file_mgr_vol.s:2455`<br>`file_mgr_vol.s:2211` | — |
| **`HFSE_OK_4`** | `0x003E6C` | `0x005906` | `file_mgr_vol.s:2483`<br>`file_mgr_vol.s:2241` | end of block: read next directory block |
| **`HFSE_OK_5`** | `0x003E94` | `0x00592E` | `file_mgr_vol.s:2498`<br>`file_mgr_vol.s:2257` | — |
| **`HFSE_OK_6`** | `0x003EF8` | `0x005992` | `file_mgr_vol.s:2552`<br>`file_mgr_vol.s:2311` | — |
| **`HFSE_OK_7`** | `0x003EFA` | `0x005994` | `file_mgr_vol.s:2554`<br>`file_mgr_vol.s:2313` | — |
| **`HFSE_OK_8`** | `0x003F8A` | — | `file_mgr_vol.s:2630` | — |
| **`HFSE_OK_9`** | `0x003FAC` | — | `file_mgr_vol.s:2656` | HFSE_OK_9 |
| **`HFSE_RESOLVE_BY_REFNUM`** | — | `0x005A46` | `file_mgr_vol.s:2402` | SetVolInfo_hfs: indexed volume info (same structure as GetVolInfo) |
| **`HFSE_SKIP`** | `0x003F70` | — | `file_mgr_vol.s:2620` | HFSE_SKIP Called during boot. |
| **`hfsF`** | `0x003D04` | — | `file_mgr_vol.s:2267` | hfs F |
| **`HFSF_CONT`** | `0x003D1A` | `0x0057A8` | `file_mgr_vol.s:2280`<br>`file_mgr_vol.s:2067` | hfsF: _GetWDInfo HFS dispatch HFSF_CONT: copy WDCB info + procID to param block |
| **`HFSF_CONT_2`** | `0x003D20` | `0x0057AE` | `file_mgr_vol.s:2283`<br>`file_mgr_vol.s:2070` | HFSF_CONT_2: copy WDCB VCB/DirID to param block |
| **`HFSF_CONT_3`** | `0x003D3C` | `0x0057CA` | `file_mgr_vol.s:2297`<br>`file_mgr_vol.s:2080` | HFSF_CONT_3 HFSF_CONT_3: validate that D1 is a valid WD refnum |
| **`HFSF_OK`** | `0x003D5A` | `0x0057F4` | `file_mgr_vol.s:2310`<br>`file_mgr_vol.s:2097` | — |
| **`hfsUn_LockRange`** | `0x005466` | — | `file_mgr_io.s:789` | hfs Un_Lock Range _LockRng / _UnlockRng (HFS): stub - always succeeds |
| **`HFSUN_LOCKRANGE_CONT`** | `0x005476` | — | `file_mgr_io.s:802` | HFSUN_LOCKRANGE_CONT HFSUN_LOCKRANGE_CONT/FileAlloc: allocate space for file (MFS/HFS dispatch) |
| **`HFSUN_LOCKRANGE_ERR`** | `0x005472` | — | `file_mgr_io.s:794` | — |
| **`HFSUN_LOCKRANGE_NO`** | `0x005488` | — | `file_mgr_io.s:813` | HFSUN_LOCKRANGE_NO |
| **`HGETFLAGS`** | — | `0x00A7A0` | `memory_mgr.s:560` | — |
| **`HGETVOL_DEFAULT_DONE`** | — | `0x0055FA` | `file_mgr_vol.s:1861` | — |
| **`HITTEST_BTN_LOOP`** | `0x001402` | `0x00160E` | `sys_error.s:449`<br>`sys_error.s:412` | Mouse down: find which button was clicked |
| **`HLock`** | `0x010230` | `0x00A748` | `memory_mgr.s:878` | **Proto:** `Pascal: PROCEDURE HLock(h: Handle);`<br>**Regs:** `Entry: A0 = h Exit:  D0.W = noErr, or nilHandleErr if the master pointer is nil;`<br>_HLock ($A029): lock a relocatable block Pascal: PROCEDURE HLock(h: Handle); Entry: A0 = h Exit:  D0.W = noErr, or nilHandleErr if the master pointer is nil; MemErr set Sets the lock bit (bit 7) in th... |
| **`HLOCK`** | `0x010230` | `0x00A748` | `memory_mgr.s:504` | — |
| **`HMakeMoreMasters`** | `0x010AA4` | `0x00B062` | `memory_mgr.s:2519` | **Regs:** `zone's free list. Exit: A1 = head of the free list (the last new master`<br>HMakeMoreMasters - allocate a block of master pointers for zone A6 Allocates zone.mAllocCnt (32 if not positive) master pointers as one nonrelocatable block (MakePtrSpc + AllocBK) and links them all o... |
| **`HMAKEMOREMASTERS`** | `0x010AA4` | `0x00B062` | `memory_mgr.s:1858` | — |
| **`HMAKEMOREMASTERS_CONT`** | `0x010AB2` | `0x00B070` | `memory_mgr.s:2525`<br>`memory_mgr.s:1864` | — |
| **`HMAKEMOREMASTERS_CONT_2`** | `0x010AC2` | `0x00B080` | `memory_mgr.s:2533`<br>`memory_mgr.s:1872` | — |
| **`HMAKEMOREMASTERS_ERR`** | `0x010ACC` | `0x00B08A` | `memory_mgr.s:2539`<br>`memory_mgr.s:1878` | — |
| **`HNoPurge`** | `0x01024E` | `0x00A766` | `memory_mgr.s:931` | **Proto:** `Pascal: PROCEDURE HNoPurge(h: Handle);`<br>**Regs:** `Entry: A0 = h Exit:  D0.W = noErr, or nilHandleErr if the master pointer is nil;`<br>_HNoPurge ($A04A): mark a relocatable block unpurgeable Pascal: PROCEDURE HNoPurge(h: Handle); Entry: A0 = h Exit:  D0.W = noErr, or nilHandleErr if the master pointer is nil; MemErr set (h = nil: ret... |
| **`HNOPURGE`** | `0x01024E` | `0x00A766` | `memory_mgr.s:519` | — |
| **`HNOPURGE_CONT`** | `0x010262` | `0x00A78E` | `memory_mgr.s:958`<br>`memory_mgr.s:550` | **Regs:** `Entry: A0 = handle Exit:  A1 = masked handle (master pointer address), D0 = master pointer,`<br>HNOPURGE_CONT - common entry of HLock, HUnlock, HPurge and HNoPurge Entry: A0 = handle Exit:  A1 = masked handle (master pointer address), D0 = master pointer, Z set if the master pointer is nil If th... |
| **`HNOPURGE_EMPTY`** | `0x01026E` | `0x00A79A` | `memory_mgr.s:965`<br>`memory_mgr.s:556` | handle is non-nil |
| **`HNOPURGE_EXIT`** | `0x010256` | `0x00A76E` | `memory_mgr.s:935`<br>`memory_mgr.s:524` | Called by: HLOCK, HUNLOCK, HPURGE, HRSRC, HNORSRC (and 1 more) |
| **`HNOPURGE_EXIT_2`** | `0x01025A` | `0x00A772` | `memory_mgr.s:944`<br>`memory_mgr.s:528` | HNOPURGE_EXIT_2 - HLock/HUnlock/HPurge/HNoPurge: master pointer is nil Called during boot. |
| **`HNOPURGE_EXIT_3`** | `0x01025C` | — | `memory_mgr.s:946` | — |
| **`HNORSRC`** | — | `0x00A784` | `memory_mgr.s:538` | — |
| **`HPurge`** | `0x010244` | `0x00A75C` | `memory_mgr.s:914` | **Proto:** `Pascal: PROCEDURE HPurge(h: Handle);`<br>**Regs:** `Entry: A0 = h Exit:  D0.W = noErr, or nilHandleErr if the master pointer is nil;`<br>_HPurge ($A049): mark a relocatable block purgeable Pascal: PROCEDURE HPurge(h: Handle); Entry: A0 = h Exit:  D0.W = noErr, or nilHandleErr if the master pointer is nil; MemErr set (h = nil: returns a... |
| **`HPURGE`** | `0x010244` | `0x00A75C` | `memory_mgr.s:514` | — |
| **`HRSRC`** | — | `0x00A77A` | `memory_mgr.s:533` | — |
| **`HSETFLAGS`** | — | `0x00A7AE` | `memory_mgr.s:567` | — |
| **`HSETVOL_DEFAULT_WDCB_DONE`** | — | `0x0055D6` | `file_mgr_vol.s:1848` | — |
| **`HUnlock`** | `0x01023A` | `0x00A752` | `memory_mgr.s:898` | **Proto:** `Pascal: PROCEDURE HUnlock(h: Handle);`<br>**Regs:** `Entry: A0 = h Exit:  D0.W = noErr, or nilHandleErr if the master pointer is nil;`<br>_HUnlock ($A02A): unlock a relocatable block Pascal: PROCEDURE HUnlock(h: Handle); Entry: A0 = h Exit:  D0.W = noErr, or nilHandleErr if the master pointer is nil; MemErr set (h = nil: returns at once... |
| **`HUNLOCK`** | `0x01023A` | `0x00A752` | `memory_mgr.s:509` | — |
| **`ICDISP_NO_DEBUGGER`** | `0x00117C` | — | `sys_error.s:48` | — |
| **`INF_RGN_TEMPLATE`** | `0x0011D2` | — | `sys_error.s:107` | INF_RGN_TEMPLATE - infinite region template (10 bytes) Region: size=10, rgnBBox=(-32767,-32767,32767,32767) |
| **`INIT_ALERT_RECT`** | `0x00134A` | `0x00155A` | `sys_error.s:355`<br>`sys_error.s:313` | INIT_ALERT_RECT - initialize DS alert rectangle if not already set |
| **`INITADB`** | — | `0x003306` | `adb_mgr.s:21` | Apple Desktop Bus Manager and keyboard Apple source: ADBMgr.a (MacSEROM.lst module KBDMNGR; System 7.1: OS/ADBMgr/ADBMgr.a). The SE talks to the keyboard and the mouse over ADB through the VIA shift r... |
| **`INITADBDRVR`** | — | `0x003C9E` | `adb_mgr.s:1078` | INITADBDRVR - load ADBS (ADB Service) resources for each device For each ADB device found, looks up an 'ADBS' resource by handler ID. If found, calls its init routine (per Inside Mac: Devices). |
| **`InitApplZone`** | `0x00FEE4` | `0x00A3CA` | `memory_mgr.s:127` | _InitApplZone ($A02C) Called during boot. |
| **`INITAPPLZONE`** | `0x00FEE4` | `0x00A3CA` | `memory_mgr.s:95` | — |
| **`INITAPPLZONE_DONE`** | `0x00FF26` | `0x00A408` | `memory_mgr.s:159`<br>`memory_mgr.s:120` | INITAPPLZONE_DONE Called during boot. |
| **`INITAPPLZONE_LOOP`** | `0x00FF08` | `0x00A3EA` | `memory_mgr.s:139`<br>`memory_mgr.s:106` | — |
| **`INITAPPLZONE_LOOP_2`** | `0x00FF14` | `0x00A3F6` | `memory_mgr.s:144`<br>`memory_mgr.s:111` | — |
| **`INITAPPLZONE_SKIP`** | `0x00FEEE` | `0x00A3D4` | `memory_mgr.s:132`<br>`memory_mgr.s:100` | — |
| **`INITAPPLZONE_SKIP_2`** | `0x00FF22` | `0x00A404` | `memory_mgr.s:150`<br>`memory_mgr.s:117` | — |
| **`INITC_EXIT`** | `0x0079DE` | `0x009532` | `file_mgr_cache.s:471`<br>`file_mgr_cache.s:424` | — |
| **`INITC_LOOP`** | `0x0079CE` | `0x009522` | `file_mgr_cache.s:464`<br>`file_mgr_cache.s:417` | allocate memory for cache queue initialize the cache queue |
| **`InitCache`** | `0x00799A` | `0x0094EE` | `file_mgr_cache.s:443` | Init Cache Called during boot. |
| **`INITCACHE`** | `0x00799A` | `0x0094EE` | `file_mgr_cache.s:397` | — |
| **`InitKeyboard`** | `0x002568` | — | `keyboard.s:23` | Keyboard driver -- InitKeyboard, keyboard interrupt, KybdTask Apple module KBDMNGR (the SE has the ADB Manager in its place). Talks to the keyboard through the VIA shift register: Model/Inquiry comman... |
| **`InitNode`** | `0x00748A` | `0x008FDE` | `file_mgr_btree.s:1903` | InitNode -- get an initialized node. Init Node |
| **`INITNODE`** | `0x00748A` | `0x008FDE` | `file_mgr_btree.s:1673` | InitNode: allocate and initialize an empty node |
| **`INITNODE_EXIT`** | `0x0074B2` | `0x009006` | `file_mgr_btree.s:1918`<br>`file_mgr_btree.s:1686` | get cache buffer for new node initialize the node |
| **`InitQueue`** | `0x002A6C` | `0x002B24` | `file_mgr_queue.s:296` | _FInitQueue ($A016) - reset FS queue to single-element state Clears the FS queue so only the currently executing request remains. Called during system initialization to reset file system state. |
| **`INITQUEUE`** | `0x002A6C` | `0x002B24` | `queue.s:94` | INITQUEUE - initialize an empty queue header Clears the 10-byte queue header: flags (word), qHead (long), qTail (long) |
| **`InitQueuePrim`** | `0x001A38` | — | `queue.s:114` | InitQueuePrim - zero a 10-byte queue header (flags + head + tail) A1 = queue header ptr. Stores zeros at (A1), (A1)+2, (A1)+6; leaves A1 pointing to start of header on return. |
| **`INITSCSIMGR`** | — | `0x01A19C` | `scsi_mgr.s:71` | SCSI Manager Apple sources: SCSIMgrInit.a and SCSIMgr.a (MacSEROM.lst module SCSISTUFF): INITSCSIMGR and the SCSI Manager trap (_SCSIDispatch $A815) for the NCR 5380 SCSI controller. Public routines (... |
| **`InitUtil`** | `0x00FCC2` | `0x00A10C` | `os_utilities.s:482` | _InitUtil ($A03F): initialize Parameter RAM from RTC Reads PRAM, validates it, reinitializes if invalid Called during boot before most other managers |
| **`INITUTIL`** | `0x00FCC2` | `0x00A10C` | `os_utilities.s:527` | — |
| **`INITUTIL_CONT`** | `0x00FD46` | `0x00A190` | `os_utilities.s:546`<br>`os_utilities.s:586` | INITUTIL_CONT Called during boot. INITUTIL_CONT: read date/time from RTC chip (4 bytes, read twice for consistency) RTC stores seconds since midnight Jan 1, 1904 as 4 bytes Reads twice and compares to... |
| **`INITUTIL_CONT_2`** | `0x00FD7C` | `0x00A1C6` | `os_utilities.s:575`<br>`os_utilities.s:613` | INITUTIL_CONT_2: write date/time to RTC chip (for SetDateTime) Writes 4 bytes, reads back to verify |
| **`INITUTIL_DONE`** | `0x00FD26` | `0x00A170` | `os_utilities.s:521`<br>`os_utilities.s:562` | — |
| **`INITUTIL_ERR`** | `0x00FD42` | `0x00A18C` | `os_utilities.s:534`<br>`os_utilities.s:575` | — |
| **`INITUTIL_ERR_2`** | `0x00FDAA` | `0x00A1F4` | `os_utilities.s:596`<br>`os_utilities.s:633` | verify: read back and compare |
| **`INITUTIL_FOUND`** | `0x00FD6E` | `0x00A1B8` | `os_utilities.s:565`<br>`os_utilities.s:604` | verify: first 4 bytes should match second 4 bytes |
| **`INITUTIL_LOOP`** | `0x00FCEE` | `0x00A138` | `os_utilities.s:502`<br>`os_utilities.s:543` | reset RTC test register read PRAM and date/time validate PRAM magic byte invalid PRAM: initialize with defaults from READPRAM_CONT |
| **`INITUTIL_LOOP_2`** | `0x00FD4E` | `0x00A198` | `os_utilities.s:550`<br>`os_utilities.s:590` | — |
| **`INITUTIL_LOOP_3`** | `0x00FD58` | `0x00A1A2` | `os_utilities.s:555`<br>`os_utilities.s:595` | — |
| **`INITUTIL_LOOP_4`** | `0x00FD88` | `0x00A1D2` | `os_utilities.s:580`<br>`os_utilities.s:618` | — |
| **`INITUTIL_LOOP_5`** | `0x00FD8E` | `0x00A1D8` | `os_utilities.s:584`<br>`os_utilities.s:622` | — |
| **`INITUTIL_NO`** | `0x00FD38` | `0x00A182` | `os_utilities.s:530`<br>`os_utilities.s:571` | — |
| **`INITUTIL_OK`** | `0x00FCF8` | `0x00A142` | `os_utilities.s:507`<br>`os_utilities.s:548` | check for extended PRAM (Mac Plus has 256 bytes) |
| **`InitZone`** | `0x00FF38` | `0x00A41A` | `memory_mgr.s:170` | Called during boot. _InitZone ($A019): initialize a heap zone from parameter block A0 = ptr to: startPtr, limitPtr, cMoreMasters, pGrowZone |
| **`INITZONE`** | `0x00FF38` | `0x00A41A` | `memory_mgr.s:127` | — |
| **`INITZONE_ERR`** | `0x00FF6C` | `0x00A452` | `memory_mgr.s:195`<br>`memory_mgr.s:150` | set zone limit (bkLim) update HighHeapMark if this zone extends higher create the trailing free block (sentinel) at end of zone |
| **`INITZONE_EXIT`** | `0x00FF9C` | `0x00A4AC` | `memory_mgr.s:216`<br>`memory_mgr.s:185` | initialize zone header fields create the initial free block and master pointer block |
| **`INITZONE_LOOP`** | `0x00FF4A` | `0x00A42C` | `memory_mgr.s:179`<br>`memory_mgr.s:135` | zero the zone header (13 longwords = 52 bytes) |
| **`InsertRec`** | `0x0074BC` | `0x009010` | `file_mgr_btree.s:1930` | InsertRec -- try to insert it. Insert Rec Called by: BTINS_NEWROOT, BTINS_INSERT, ROTLT_LOOP, ROTLT_CHKRT2, ROT_RECLT |
| **`INSERTREC`** | `0x0074BC` | `0x009010` | `file_mgr_btree.s:1694` | InsertRec: insert record at index D1 in node A1 Input: A0=record data, D0=record size, A1=node, D1=insert index Called by: BTINS_NEWROOT, BTINS_INSERT, ROTLT_LOOP, ROTLT_CHKRT2, ROT_RECLT |
| **`INSREC_EXIT`** | `0x007526` | `0x00907A` | `file_mgr_btree.s:1982`<br>`file_mgr_btree.s:1744` | adjust offsets for moved records move in the new record |
| **`INSREC_FIT`** | `0x0074F0` | `0x009044` | `file_mgr_btree.s:1961`<br>`file_mgr_btree.s:1723` | set up some common stuff see if new record will fit INSREC_FIT IRInsert: make hole for new record |
| **`INSTALL_INF_RGN`** | `0x0011C4` | `0x00140C` | `sys_error.s:95`<br>`sys_error.s:91` | INSTALL_INF_RGN - install infinite bounding region into Scratch20 Copies 10-byte region struct (size=10, bbox=0x8001..0x7FFF) to Scratch20. Both visRgn and clipRgn point here. |
| **`INSTALL_KCHR_KMAP`** | — | `0x003DAE` | `adb_mgr.s:1225` | INSTALL_KCHR_KMAP - configure keyboard: load KCHR and KMAP resources For each keyboard device (orig_addr = 2), allocates a 50-byte key handler data block, loads 'KCHR' (key character mapping) and 'KMA... |
| **`INSTALL_KCHR_LOOP`** | — | `0x003DB6` | `adb_mgr.s:1229` | — |
| **`INSTALL_KCHR_NEXT`** | — | `0x003DBA` | `adb_mgr.s:1231` | — |
| **`INSTALLRDRIVERS`** | — | `0x009B76` | `segment_loader.s:322` | — |
| **`InsTime`** | `0x0175D2` | `0x01A95C` | `time_mgr.s:39` | **Proto:** `Pascal: PROCEDURE InsTime(tmTaskPtr: QElemPtr);`<br>**Regs:** `Entry: A0 = ptr to TMTask (qLink, qType, tmAddr, tmCount) Exit:  D0 = noErr`<br>Time Manager Manages asynchronous timer tasks using VIA Timer 2. Provides the _InsTime ($A058), _RmvTime ($A059), _PrimeTime ($A05A) traps. Timer 2 runs in one-shot mode. When a timer fires, VIAInt5_T... |
| **`INSTIME`** | `0x0175D2` | `0x01A95C` | `time_mgr.s:60` | **Proto:** `Pascal: PROCEDURE InsTime(tmTaskPtr: QElemPtr);`<br>**Regs:** `Entry: A0 = ptr to TMTask (qLink, qType, tmAddr, tmCount) Exit:  D0 = noErr`<br>Time Manager Manages asynchronous timer tasks using VIA Timer 2. Provides the _InsTime ($A058), _RmvTime ($A059), _PrimeTime ($A05A) traps. Timer 2 runs in one-shot mode. When a timer fires, VIAInt5_T... |
| **`IO_CORE_ERR`** | `0x002076` | `0x002DFA` | `device_mgr.s:116`<br>`device_mgr.s:105` | No active I/O request - fatal system error |
| **`IO_PRIME_ENTRY`** | `0x002150` | `0x002EDC` | `device_mgr.s:259`<br>`device_mgr.s:239` | — |
| **`IO_SET_POSITION`** | `0x00214C` | `0x002ED8` | `device_mgr.s:257`<br>`device_mgr.s:237` | Read/Write Prime path: set file position before calling driver |
| **`IOCORE`** | — | `0x002DB4` | `device_mgr.s:70` | Device Manager Apple source: DeviceMgr.a (MacSEROM.lst module IOCORE): the jump offsets FSIODNETBL (JFetch, JStash, JIODone), FETCH, STASH, IODONE, the request queueing and the traps Open ... KillIO, ... |
| **`IODone`** | `0x002082` | `0x002E06` | `device_mgr.s:147` | IODone - complete an asynchronous I/O request Called via JIODone vector ($08FC) when a driver finishes an I/O operation. A1 = DCE pointer, D0 = result code. Dequeues the completed request, calls its c... |
| **`IODONE`** | `0x002082` | `0x002E06` | `device_mgr.s:120` | IODONE (Apple's IODone) - since <13Jan86> it preserves D0 around the completion, which its local label @1 (IODONE_1) does |
| **`IODONE_1`** | — | `0x002E0E` | `device_mgr.s:133` | IODONE_1 (IODone's @1) - complete an asynchronous I/O request Called via JIODone vector ($08FC) when a driver finishes an I/O operation. A1 = DCE pointer, D0 = result code. Dequeues the completed requ... |
| **`IOOK`** | `0x002080` | `0x002E04` | `device_mgr.s:136`<br>`device_mgr.s:116` | IOOK (Apple's name) - complete the I/O request with noErr: falls into IODone |
| **`KBD_BUILD_MESSAGE`** | — | `0x003B3C` | `adb_mgr.s:896` | — |
| **`KBD_CHK_KEY_UP`** | `0x002652` | — | `keyboard.s:148` | — |
| **`KBD_CHK_KEYPAD`** | `0x00262E` | — | `keyboard.s:117` | KBD_CHK_KEYPAD - check if byte is keypad prefix ($79) Mac Plus keyboard sends $79 before each numeric keypad key code. |
| **`KBD_COMPLETION`** | — | `0x003B76` | `adb_mgr.s:924` | KBD_COMPLETION - build and post keyboard event D0 = translated character, D3 = keycode + up/down flag Builds event message: char in bits 0-7, keycode in bits 8-15, ADB address in bits 16-23. Posts key... |
| **`KBD_COMPLETION_NEXT`** | — | `0x003BB6` | `adb_mgr.s:956` | Toggle key: check if currently down in key map |
| **`KBD_COMPLETION_NORMAL`** | — | `0x003B98` | `adb_mgr.s:938` | Key down: record timing and post keyDown event |
| **`KBD_DATA_RECEIVED`** | `0x00260E` | — | `keyboard.s:100` | KBD_DATA_RECEIVED - Keyboard response byte received via VIA SR input Processes the raw byte: model number, keypad prefix, or key transition. Key encoding: bit 7 = transition (0=down, 1=up), bits [6:1]... |
| **`KBD_DO_POST`** | `0x002694` | — | `keyboard.s:179` | Post the key event |
| **`KBD_KEYUP_AUTO`** | — | `0x003B34` | `adb_mgr.s:893` | — |
| **`KBD_LED_PATH`** | — | `0x003BD6` | `adb_mgr.s:970` | Special key processing: modifier keys, LED control, etc. D2 = special key type, A0 = special key data table entry |
| **`KBD_POST_EVENT`** | `0x00267C` | `0x003AEC` | `keyboard.s:170`<br>`adb_mgr.s:863` | Translate raw key code through Key1Trans/Key2Trans procedure Translation returned 0: check screen dump (Cmd-Shift-3) state |
| **`KBD_POST_EVENT_RTS`** | — | `0x003B72` | `adb_mgr.s:916` | Call _KeyTranslate to convert keycode to character |
| **`KBD_POST_KEYUP`** | — | `0x003B9A` | `adb_mgr.s:941` | Post keyUp event |
| **`KBD_POST_NOT_FF`** | — | `0x003B12` | `adb_mgr.s:878` | Look up keycode in KCHR key-code-to-modifier mapping table |
| **`KBD_PROCESS_KEY`** | `0x002642` | — | `keyboard.s:141` | KBD_PROCESS_KEY - Process a key transition byte from keyboard Raw byte format: bit 7=transition (0=down,1=up), bits[6:1]=keyCode, bit 0=pair Extracts 7-bit virtual key code, applies keypad offset, tra... |
| **`KBD_QUEUE_DRAIN_LOOP`** | — | `0x003C1E` | `adb_mgr.s:1003` | — |
| **`KBD_QUEUE_DRAIN_RTS`** | — | `0x003C28` | `adb_mgr.s:1007` | — |
| **`KBD_QUEUE_FILL`** | — | `0x003BF2` | `adb_mgr.s:984` | Found free slot: fill with ADB command data |
| **`KBD_QUEUE_FREE_SLOT`** | — | `0x003BE4` | `adb_mgr.s:977` | — |
| **`KBD_QUEUE_FULL`** | — | `0x003C08` | `adb_mgr.s:992` | — |
| **`KBD_QUEUE_LED_UPDATE`** | — | `0x003BDA` | `adb_mgr.s:972` | — |
| **`KBD_RESET_KEYMAP`** | — | `0x003EDA` | `adb_mgr.s:1376` | — |
| **`KBD_SEND_CMD`** | `0x0025A4` | `0x003946` | `keyboard.s:47`<br>`adb_mgr.s:670` | Send command byte D0 to keyboard via VIA shift register Protocol: disable SR -> send sync pulse (0x00) -> load command byte VIA ACR bits [4:2]: 000=disabled, 011=shift out under ext CB1 clock, 111=shi... |
| **`KBD_SEND_CMD_JMP`** | `0x00263E` | — | `keyboard.s:131` | — |
| **`KBD_SEND_DELAY`** | `0x0025FE` | — | `keyboard.s:86` | Command byte just finished transmitting; wait ~330us for keyboard to prepare |
| **`KBD_SEND_INQUIRY`** | `0x00263C` | — | `keyboard.s:129` | KBD_SEND_INQUIRY - send Inquiry command to poll keyboard for next key event Called during boot. |
| **`KBD_SET_LED`** | — | `0x003C30` | `adb_mgr.s:1016` | KBD_SET_LED - LED update completion: apply LED mask to key state Merges or clears LED bits in the keyboard register data based on key down/up state. Then sends a Listen command to update the keyboard'... |
| **`KBD_SET_LED_AFTER_CAPS`** | — | `0x003C56` | `adb_mgr.s:1038` | — |
| **`KBD_SET_LED_AFTER_NUM`** | — | `0x003C4A` | `adb_mgr.s:1031` | — |
| **`KBD_SET_LED_CALC`** | — | `0x003C3E` | `adb_mgr.s:1024` | — |
| **`KBD_SET_LED_CAPSLOCK`** | — | `0x003C50` | `adb_mgr.s:1034` | — |
| **`KBD_SET_LED_DO_LISTEN`** | — | `0x003C5A` | `adb_mgr.s:1041` | Send updated LED state back to keyboard via Listen command |
| **`KBD_SET_LED_NUMLOCK`** | — | `0x003C46` | `adb_mgr.s:1028` | — |
| **`KBD_SET_LED_RTS`** | — | `0x003C72` | `adb_mgr.s:1051` | — |
| **`KBD_SPECIAL_KEY`** | — | `0x003BA6` | `adb_mgr.s:947` | KBD_SPECIAL_KEY - special key table match: check key state and dispatch |
| **`KBD_TRANSLATE`** | `0x002664` | — | `keyboard.s:157` | If key-up and matches last key-down, clear auto-repeat state |
| **`KBD_UPDATE_KEYMAP`** | — | `0x003B24` | `adb_mgr.s:885` | KBD_UPDATE_KEYMAP - update key map and post keyboard event |
| **`KBDMNGR`** | — | `0x003306` | `adb_mgr.s:20` | Apple Desktop Bus Manager and keyboard Apple source: ADBMgr.a (MacSEROM.lst module KBDMNGR; System 7.1: OS/ADBMgr/ADBMgr.a). The SE talks to the keyboard and the mouse over ADB through the VIA shift r... |
| **`KC_EXIT`** | `0x006670` | `0x008136` | `file_mgr_catalog.s:753`<br>`file_mgr_catalog.s:674` | — |
| **`KC_IS_EQ`** | `0x00666A` | `0x008130` | `file_mgr_catalog.s:747`<br>`file_mgr_catalog.s:668` | KCIsEQ |
| **`KC_IS_GT`** | `0x00666E` | `0x008134` | `file_mgr_catalog.s:751`<br>`file_mgr_catalog.s:672` | KCIsGT |
| **`KC_IS_LT`** | `0x006666` | `0x00812C` | `file_mgr_catalog.s:743`<br>`file_mgr_catalog.s:664` | compare DirID's first ParID's are equal, compare the CNames KCIsLT |
| **`KEYMAP_CALL_TRANS`** | `0x0026CA` | — | `keyboard.s:214` | — |
| **`KEYMAP_CHK_DIRECTION`** | `0x0026AE` | — | `keyboard.s:202` | — |
| **`KEYMAP_SEL_TRANS`** | `0x0026C0` | — | `keyboard.s:209` | Select translation procedure: Key2Trans for keypad, Key1Trans for main kbd |
| **`KEYMAP_ZERO_LOOP`** | `0x0026E0` | — | `keyboard.s:237` | Zero the 18-byte KeyMap bitmap (9 words = 128 key bits + padding) |
| **`KEYTRANS`** | — | `0x003E18` | `adb_mgr.s:1273` | KEYTRANS - _KeyTranslate trap: translate keycode to character(s) Per Inside Mac: Text, the KCHR resource defines a keycode-to-char mapping. This routine looks up the keycode in the KCHR tables, handle... |
| **`KEYTRANS_BODY`** | — | `0x003E12` | `adb_mgr.s:1263` | Allocate key handler data block (50 bytes, cleared) Load 'KCHR' resource (key character mapping, ID 0) Load 'KMAP' resource (key layout mapping, ID 0) |
| **`KEYTRANS_DEAD_CHK`** | — | `0x003E74` | `adb_mgr.s:1321` | KEYTRANS_DEAD_CHK - zero char from table: check dead-key sequence table |
| **`KEYTRANS_DEAD_DONE`** | — | `0x003EB4` | `adb_mgr.s:1353` | Completing a dead-key sequence: look up completion char |
| **`KEYTRANS_DEAD_LOOKUP`** | — | `0x003E84` | `adb_mgr.s:1328` | — |
| **`KEYTRANS_DEAD_MATCH`** | — | `0x003E9E` | `adb_mgr.s:1342` | KEYTRANS_DEAD_MATCH - dead-key sequence matched |
| **`KEYTRANS_DEAD_NEXT`** | — | `0x003ECA` | `adb_mgr.s:1365` | — |
| **`KEYTRANS_DEAD_NOMATCH`** | — | `0x003EC0` | `adb_mgr.s:1360` | — |
| **`KEYTRANS_DEFAULT_CHAR`** | — | `0x003E68` | `adb_mgr.s:1312` | Dead-key not matched: return default completion char |
| **`KEYTRANS_HAVE_DEAD`** | — | `0x003E5E` | `adb_mgr.s:1306` | Look up modifier-to-table-number mapping Non-zero character: check for dead-key completion |
| **`KEYTRANS_NORMAL_CHAR`** | — | `0x003E70` | `adb_mgr.s:1317` | — |
| **`KEYTRANS_RETURN`** | — | `0x003E94` | `adb_mgr.s:1337` | KEYTRANS_RETURN - KeyTranslate return: store result and return Called by: KEYTRANS, KEYTRANS_DEFAULT_CHAR, KEYTRANS_NORMAL_CHAR, KEYTRANS_DEAD_CHK, KEYTRANS_DEAD_DONE (and 2 more) |
| **`KillIO`** | `0x002476` | `0x003214` | `device_mgr.s:727` | _KillIO ($A006) A0 = paramBlock -> D0 = error; aborts pending I/O Sends killCode control call, then dequeues and aborts all pending requests. |
| **`KILLIO`** | `0x002476` | `0x003214` | `device_mgr.s:629` | KILLIO - _KillIO trap: abort pending I/O on a driver Sends a Control call (csCode=1) to kill pending requests, then drains the driver's I/O queue by completing each with abortErr. |
| **`KILLIO_DONE`** | `0x0024BE` | `0x00325C` | `device_mgr.s:758`<br>`device_mgr.s:655` | Drain the driver's I/O queue: dequeue and abort each pending request KILLIO_DONE - queue drained, clear drvrActive, return noErr |
| **`KILLIO_DRAIN_QUEUE`** | `0x0024AC` | `0x00324A` | `device_mgr.s:745`<br>`device_mgr.s:648` | KillIO queue drain: complete all pending requests with abortErr |
| **`KILLIO_RESTORE_SR`** | `0x0024C4` | `0x003262` | `device_mgr.s:761`<br>`device_mgr.s:658` | — |
| **`KybdTask`** | `0x0026CC` | — | `keyboard.s:226` | KybdTask - Keyboard VBL polling task Called every VBL (~16.6ms). If keyboard hasn't responded since last poll (KbdVers=0), assumes keyboard was disconnected: re-queries model number and resets KeyMap.... |
| **`KYBDTASK_CLEAR_FLAG`** | `0x0026E6` | — | `keyboard.s:240` | — |
| **`L_BasicIO`** | `0x007C14` | `0x009768` | `file_mgr_cache.s:830`<br>`file_mgr_cache.s:685` | — |
| **`L_mFileRead`** | `0x004F18` | — | `file_mgr_io.s:24` | FileRead (vFileRead) |
| **`L_MFILEREAD_CONT`** | `0x004F32` | `0x0069D4` | `file_mgr_io.s:36`<br>`file_mgr_io.s:32` | figure min(requested count, distance to EOF) |
| **`L_MFILEREAD_CONT_2`** | `0x004F9E` | `0x006A44` | `file_mgr_io.s:83`<br>`file_mgr_io.s:85` | FRdEOFXit |
| **`L_MFILEREAD_CONT_3`** | `0x004FAC` | `0x006A52` | `file_mgr_io.s:96`<br>`file_mgr_io.s:99` | L_MFILEREAD_CONT_3 FRNewLine: reading while looking for end of line characters |
| **`L_MFILEREAD_CONT_4`** | `0x004FE4` | `0x006A8A` | `file_mgr_io.s:128`<br>`file_mgr_io.s:130` | L_MFILEREAD_CONT_4 Called during boot. L_MFILEREAD_CONT_4/PreRdFileBlk: read file block, but only if within current LEOF |
| **`L_MFILEREAD_CONT_5`** | `0x004FEE` | `0x006A94` | `file_mgr_io.s:141`<br>`file_mgr_io.s:142` | L_MFILEREAD_CONT_5 Called during boot. L_MFILEREAD_CONT_5/RdFileBlk: read a file block into volume cache |
| **`L_MFILEREAD_CONT_6`** | `0x005006` | `0x006AAC` | `file_mgr_io.s:158`<br>`file_mgr_io.s:159` | L_MFILEREAD_CONT_6 Called during boot. |
| **`L_MFILEREAD_DONE`** | `0x004F8E` | `0x006A34` | `file_mgr_io.s:74`<br>`file_mgr_io.s:76` | FRdOK |
| **`L_MFILEREAD_EXIT`** | `0x004F90` | `0x006A36` | `file_mgr_io.s:76`<br>`file_mgr_io.s:78` | — |
| **`L_MFILEREAD_EXIT_2`** | `0x004FA0` | `0x006A46` | `file_mgr_io.s:85`<br>`file_mgr_io.s:88` | FRdEOFXit |
| **`L_MFILEREAD_EXIT_3`** | `0x004FA8` | `0x006A4E` | `file_mgr_io.s:88`<br>`file_mgr_io.s:91` | — |
| **`L_MFILEREAD_LOOP`** | `0x004FBE` | `0x006A64` | `file_mgr_io.s:104`<br>`file_mgr_io.s:107` | newline byte-by-byte scan loop |
| **`L_MFILEREAD_NO`** | `0x004F5A` | `0x006A00` | `file_mgr_io.s:50`<br>`file_mgr_io.s:50` | check for no-cache and newline-mode flags check if caller wants cache bypass flush cache for this file first |
| **`L_MFILEREAD_NO_2`** | `0x004FDA` | `0x006A80` | `file_mgr_io.s:115`<br>`file_mgr_io.s:118` | — |
| **`L_MFILEREAD_OK`** | `0x004FFA` | `0x006AA0` | `file_mgr_io.s:146`<br>`file_mgr_io.s:147` | — |
| **`L_mMMNoErrEpilogue`** | `0x010516` | — | `memory_mgr.s:1457` | — |
| **`L_SegStack`** | `0x00F674` | `0x009AC0` | `segment_loader.s:296`<br>`segment_loader.s:242` | — |
| **`L_TrashBlocks`** | `0x007AE2` | `0x009636` | `file_mgr_cache.s:647`<br>`file_mgr_cache.s:548` | Called by: TB_CVT_END_BLK, TRASHFBLOCKS |
| **`Launch`** | `0x00F55C` | `0x0099A2` | `segment_loader.s:180` | _Launch ($A9F2): launch an application Closes all DA drivers, reinitializes app heap, loads CODE 0 |
| **`LAUNCH`** | `0x00F55C` | `0x0099A2` | `segment_loader.s:132` | — |
| **`LAUNCH_CONT`** | `0x00F59C` | `0x0099E2` | `segment_loader.s:205`<br>`segment_loader.s:156` | LAUNCH_CONT: common launch/chain entry point A0 = ptr to launch parameter block: [filename ptr, pageOption, app name...] |
| **`LAUNCH_CONT_2`** | `0x00F66E` | `0x009ABA` | `segment_loader.s:292`<br>`segment_loader.s:238` | load CODE resource 0 (jump table segment) configure stack based on CurPageOption negative: reserve 55K for sound/screen buffers |
| **`LAUNCH_EMPTY`** | `0x00F590` | `0x0099D6` | `segment_loader.s:198`<br>`segment_loader.s:149` | — |
| **`LAUNCH_EMPTY_2`** | `0x00F5BA` | `0x009A0C` | `segment_loader.s:218`<br>`segment_loader.s:174` | close previous app's resource file |
| **`LAUNCH_LOOP`** | `0x00F576` | `0x0099BC` | `segment_loader.s:188`<br>`segment_loader.s:139` | close all open desk accessories |
| **`LAUNCH_NO`** | `0x00F5E2` | `0x009A34` | `segment_loader.s:236`<br>`segment_loader.s:190` | full launch: save desk scrap, reinitialize app heap copy scrap data to stack temporarily (heap will be destroyed) |
| **`LAUNCH_NO_2`** | `0x00F624` | `0x009A76` | `segment_loader.s:262`<br>`segment_loader.s:214` | clear all hook vectors and system state before reinit restore desk scrap from stack into new heap |
| **`LAUNCH_NO_3`** | `0x00F640` | — | `segment_loader.s:275` | check for 'LC' launch control signature in param block |
| **`LAUNCH_NO_LC`** | — | `0x0099FE` | `segment_loader.s:168` | — |
| **`LAUNCH_OPEN_RFORK`** | — | `0x009A78` | `segment_loader.s:216` | — |
| **`LAUNCH_SET_PERM`** | — | `0x009A88` | `segment_loader.s:223` | — |
| **`LAUNCH_SKIP`** | `0x00F626` | — | `segment_loader.s:265` | LAUNCH_SKIP: open application resource file and load CODE 0 |
| **`Lg2Phys`** | `0x0055E6` | `0x00708C` | `file_mgr_io.s:1030` | Lg2Phys Called during boot. |
| **`LG2PHYS`** | `0x0055E6` | `0x00708C` | `file_mgr_io.s:852` | — |
| **`LG2PHYS_CONT`** | `0x005616` | `0x0070C2` | `file_mgr_io.s:1065`<br>`file_mgr_io.s:888` | — |
| **`LG2PHYS_CONT_10`** | `0x0057B6` | `0x007262` | `file_mgr_io.s:1315`<br>`file_mgr_io.s:1127` | LG2PHYS_CONT_10 LG2PHYS_CONT_10/MFSDealloc: free an MFS allocation chain starting at block D3 |
| **`LG2PHYS_CONT_11`** | `0x0057D4` | `0x007280` | `file_mgr_io.s:1328`<br>`file_mgr_io.s:1140` | — |
| **`LG2PHYS_CONT_2`** | `0x00569C` | `0x007148` | `file_mgr_io.s:1142`<br>`file_mgr_io.s:962` | — |
| **`LG2PHYS_CONT_3`** | `0x0056DA` | `0x007186` | `file_mgr_io.s:1177`<br>`file_mgr_io.s:995` | — |
| **`LG2PHYS_CONT_4`** | `0x0056F6` | `0x0071A2` | `file_mgr_io.s:1192`<br>`file_mgr_io.s:1009` | found free block: link it into the chain |
| **`LG2PHYS_CONT_5`** | `0x005700` | `0x0071AC` | `file_mgr_io.s:1198`<br>`file_mgr_io.s:1015` | update counts |
| **`LG2PHYS_CONT_6`** | `0x005758` | `0x007204` | `file_mgr_io.s:1253`<br>`file_mgr_io.s:1067` | MFS Alloc scan: check if this block is free (entry = 0) |
| **`LG2PHYS_CONT_7`** | `0x005772` | `0x00721E` | `file_mgr_io.s:1274`<br>`file_mgr_io.s:1087` | — |
| **`LG2PHYS_CONT_8`** | `0x005776` | `0x007222` | `file_mgr_io.s:1277`<br>`file_mgr_io.s:1090` | — |
| **`LG2PHYS_CONT_9`** | `0x00577E` | `0x00722A` | `file_mgr_io.s:1288`<br>`file_mgr_io.s:1101` | LG2PHYS_CONT_9 LG2PHYS_CONT_9: MFS alloc map write - set 12-bit entry in alloc map D3 = alloc block number, D5 = value to store (12-bit next block) |
| **`LG2PHYS_DONE`** | `0x00563C` | `0x0070E8` | `file_mgr_io.s:1088`<br>`file_mgr_io.s:910` | validate result and convert to byte count |
| **`LG2PHYS_ERR`** | `0x005664` | `0x007110` | `file_mgr_io.s:1107`<br>`file_mgr_io.s:929` | — |
| **`LG2PHYS_ERR_2`** | `0x0056D8` | `0x007184` | `file_mgr_io.s:1175`<br>`file_mgr_io.s:993` | first allocation: get a new start block LG2PHYS_ERR_2 |
| **`LG2PHYS_ERR_3`** | `0x005752` | `0x0071FE` | `file_mgr_io.s:1249`<br>`file_mgr_io.s:1063` | LG2PHYS_ERR_3 |
| **`LG2PHYS_EXIT`** | `0x0056B6` | `0x007162` | `file_mgr_io.s:1154`<br>`file_mgr_io.s:974` | — |
| **`LG2PHYS_NEXT`** | `0x00560E` | `0x0070BA` | `file_mgr_io.s:1060`<br>`file_mgr_io.s:883` | LG2PHYS_NEXT Called during boot (3,127 times in 30s trace). walk MFS extent chain |
| **`LG2PHYS_NEXT_2`** | `0x00566E` | `0x00711A` | `file_mgr_io.s:1119`<br>`file_mgr_io.s:940` | LG2PHYS_NEXT_2 Called during boot (3,700 times in 30s trace). LG2PHYS_NEXT_2: MFS alloc map lookup - get next alloc block from 12-bit map D3 = current alloc block, returns D5 = next alloc block |
| **`LG2PHYS_NEXT_3`** | `0x00571C` | `0x0071C8` | `file_mgr_io.s:1219`<br>`file_mgr_io.s:1034` | LG2PHYS_NEXT_3 LG2PHYS_NEXT_3: MFS find free block - scan alloc map for best free run |
| **`LG2PHYS_NO`** | `0x0055F0` | `0x00709C` | `file_mgr_io.s:1040`<br>`file_mgr_io.s:864` | LG2PHYS_NO - MFS Lg2Phys: simple linear extent mapping Called during boot. |
| **`LG2PHYS_NO_2`** | `0x005660` | `0x00710C` | `file_mgr_io.s:1104`<br>`file_mgr_io.s:926` | — |
| **`LG2PHYS_NO_3`** | `0x00569A` | `0x007146` | `file_mgr_io.s:1140`<br>`file_mgr_io.s:960` | LG2PHYS_NO_3 - MFS Alloc: allocate space for file (Alloc entry for MFS) |
| **`LG2PHYS_NO_4`** | `0x0056B0` | `0x00715C` | `file_mgr_io.s:1150`<br>`file_mgr_io.s:970` | — |
| **`LG2PHYS_NO_5`** | `0x0056E2` | `0x00718E` | `file_mgr_io.s:1181`<br>`file_mgr_io.s:999` | — |
| **`LG2PHYS_NO_6`** | `0x005742` | `0x0071EE` | `file_mgr_io.s:1236`<br>`file_mgr_io.s:1051` | — |
| **`LG2PHYS_NO_7`** | `0x005768` | `0x007214` | `file_mgr_io.s:1262`<br>`file_mgr_io.s:1076` | — |
| **`LG2PHYS_NO_8`** | `0x00576C` | `0x007218` | `file_mgr_io.s:1270`<br>`file_mgr_io.s:1083` | LG2PHYS_NO_8 |
| **`LG2PHYS_NO_9`** | `0x0057BA` | `0x007266` | `file_mgr_io.s:1318`<br>`file_mgr_io.s:1130` | — |
| **`LG2PHYS_OK`** | `0x005628` | `0x0070D4` | `file_mgr_io.s:1076`<br>`file_mgr_io.s:898` | found the right extent: compute disk block count contiguous blocks from this extent |
| **`LG2PHYS_OK_2`** | `0x0056BC` | `0x007168` | `file_mgr_io.s:1158`<br>`file_mgr_io.s:978` | MFS Alloc: extend file by allocating blocks from alloc map |
| **`LG2PHYS_OK_3`** | `0x005718` | `0x0071C4` | `file_mgr_io.s:1210`<br>`file_mgr_io.s:1026` | done: update FCB PEOF next block is occupied: find a free one |
| **`LG2PHYS_OK_4`** | `0x00572C` | `0x0071D8` | `file_mgr_io.s:1226`<br>`file_mgr_io.s:1041` | MFS Alloc: scan entire alloc map for best-fit free chain |
| **`LOADER`** | — | `0x009896` | `segment_loader.s:15` | Segment Loader -- _LoadSeg, _UnLoadSeg, _Chain, _Launch, _ExitToShell, _GetAppParms Apple source: SegmentLoader.a (MacSEROM.lst module LOADER). LoadSeg loads a CODE resource and patches its jump-table... |
| **`LOADER_LOCKED`** | — | `0x0098B4` | `segment_loader.s:29` | — |
| **`LOADER_NO_MOVEHHI`** | — | `0x0098B2` | `segment_loader.s:27` | — |
| **`LoadSeg`** | `0x00F456` | `0x009896` | `segment_loader.s:23` | Segment Loader -- _LoadSeg, _UnLoadSeg, _Chain, _Launch, _ExitToShell, _GetAppParms Apple source: SegmentLoader.a (MacSEROM.lst module LOADER). LoadSeg loads a CODE resource and patches its jump-table... |
| **`LOADSEG`** | `0x00F456` | `0x009896` | `segment_loader.s:16` | Segment Loader -- _LoadSeg, _UnLoadSeg, _Chain, _Launch, _ExitToShell, _GetAppParms Apple source: SegmentLoader.a (MacSEROM.lst module LOADER). LoadSeg loads a CODE resource and patches its jump-table... |
| **`LOADSEG_CONT`** | `0x00F4CA` | — | `segment_loader.s:82` | LOADSEG_CONT -- load CODE resource -> A0 = handle. |
| **`LOADSEG_EMPTY`** | `0x00F4AA` | `0x0098EA` | `segment_loader.s:61`<br>`segment_loader.s:50` | — |
| **`LOADSEG_ERR`** | `0x00F4C4` | `0x009904` | `segment_loader.s:77`<br>`segment_loader.s:61` | LOADSEG_ERR |
| **`LOADSEG_EXIT`** | `0x00F4C2` | `0x009902` | `segment_loader.s:70`<br>`segment_loader.s:59` | — |
| **`LOADSEG_LOOP`** | `0x00F496` | `0x0098D6` | `segment_loader.s:53`<br>`segment_loader.s:42` | A0+0 = first jump table offset, A0+2 = entry count check if already patched (JMP = $4EF9) patch each jump table entry: replace stub with JMP to loaded code |
| **`LOADSEG_NO`** | `0x00F470` | — | `segment_loader.s:34` | lock the segment in memory |
| **`LOADSEG_OK`** | `0x00F474` | — | `segment_loader.s:37` | dereference and patch jump table entries |
| **`LocBTCB`** | `0x00752E` | `0x009082` | `file_mgr_btree.s:1993` | LocBTCB -- locate the BTCB. Loc BTCB Called by: BTClose, BTFlush, BTInsert, BTUpdate, BT_SETUP |
| **`LOCBTCB`** | `0x00752E` | `0x009082` | `file_mgr_btree.s:1750` | LocBTCB: locate BTCB from FCB extension pointer Called by: VBTCLOSE, VBTFLUSH, VBTINSERT, VBTUPDATE, BT_SETUP |
| **`LocCNode`** | `0x006678` | `0x00813E` | `file_mgr_catalog.s:764` | LocCNode -- locate source CNode. Loc C Node Called by: MC_UPD_DEST, CMRenameCN, CC_UPD_PAR, CMDeleteCN, DC_UPD_PAR (and 7 more) |
| **`LOCCNODE`** | `0x006678` | `0x00813E` | `file_mgr_catalog.s:679` | Called by: MC_UPD_DEST, CMRENAMECN, CC_UPD_PAR, CMDELETECN, DC_UPD_PAR (and 7 more) |
| **`LOCCNODE_EXIT`** | `0x006692` | — | `file_mgr_catalog.s:775` | locate catalog record using given CNode specification thread record found, locate corresponding directory record |
| **`LOCCNODE_RETURN`** | — | `0x008158` | `file_mgr_catalog.s:689` | thread found: follow it to the directory record |
| **`LocCRec`** | `0x006698` | `0x00815E` | `file_mgr_catalog.s:786` | LocCRec -- locate thread record. Loc C Rec Called by: LocCNode, CMCreateCN, GO_LOCATE_THD, MC_UPD_DEST, RC_UPD_THD |
| **`LOCCREC`** | `0x006698` | `0x00815E` | `file_mgr_catalog.s:694` | Called by: LOCCNODE, CMCREATECN, GO_LOCATE_THD, MC_UPD_DEST, RC_UPD_THD |
| **`LOCCREC_EXIT`** | `0x0066BC` | `0x008186` | `file_mgr_catalog.s:802`<br>`file_mgr_catalog.s:712` | — |
| **`LOCCREC_SEARCH`** | `0x0066A6` | — | `file_mgr_catalog.s:793` | — |
| **`LocRec`** | `0x007538` | `0x00908C` | `file_mgr_btree.s:2004` | LocRec -- in node. Loc Rec Called by: BTDEL_UPDDEPTH, BTREC_FOUND, BTSRCH_FOUND, TSRCH_SETINDX, UpdDRec |
| **`LOCREC`** | `0x007538` | `0x00908C` | `file_mgr_btree.s:1756` | LocRec: locate record, returning key ptr (A0) and data ptr (A1) Called by: BTDEL_UPDDEPTH, BTREC_FOUND, BTSRCH_FOUND, TSRCH_SETINDX, UPDDREC |
| **`LocTPR`** | `0x00756A` | `0x0090BE` | `file_mgr_btree.s:2033` | LocTPR -- for this level. Loc TPR Called by: BTDEL_FREENODE, BTDEL_GETPAR, BTINS_NXTLEV, BTINS_NEWROOT, SplitLT (and 1 more) |
| **`LOCTPR`** | `0x00756A` | `0x0090BE` | `file_mgr_btree.s:1781` | LocTPR: locate Tree Path Record for level D0 Returns: A0 = TPR entry (6 bytes: nodeN + rIndx + reserved) Called by: BDFREE, BTDEL_GETPAR, BTINS_NXTLEV, BTINS_NEWROOT, SPLITLT (and 1 more) |
| **`LOOKUP_ALERT_ID`** | `0x0012E4` | `0x0014F4` | `sys_error.s:272`<br>`sys_error.s:213` | LOOKUP_ALERT_ID - look up ID in DS alert table Searches the alert table (pointed to by D7) for entry matching D0. Returns Z=0 and A0=entry data if found, Z=1 and A0=0 if not found. Called by: DSERR_SE... |
| **`LOOKUP_FOUND`** | `0x0012FA` | `0x00150A` | `sys_error.s:295`<br>`sys_error.s:230` | LOOKUP_FOUND - alert table entry found |
| **`LOOKUP_LOOP`** | `0x0012EA` | `0x0014FA` | `sys_error.s:281`<br>`sys_error.s:217` | LOOKUP_LOOP - alert table search loop |
| **`LOOKUP_NEXT`** | `0x0012F0` | `0x001500` | `sys_error.s:285`<br>`sys_error.s:221` | — |
| **`LOOKUP_UNIT`** | `0x0021A8` | `0x002F36` | `device_mgr.s:326`<br>`device_mgr.s:298` | LOOKUP_UNIT - Look up a driver in the unit table D2 = driver refNum (negated unit number - 1). Converts to unit number, bounds-checks, and returns DCE pointer in A1. On failure, branches to UNIT_EMPTY... |
| **`LOOKUP_UNIT_SLOT`** | `0x002508` | `0x0032A6` | `device_mgr.s:814`<br>`device_mgr.s:707` | LOOKUP_UNIT_SLOT - Look up unit table slot by refNum In: D0 = refNum (negative), D1 = trap word Out: A2 = pointer to unit table slot, A0 = DCE handle (may be nil) D0 = DCE handle (masked 24-bit), Z se... |
| **`MakeBKF`** | `0x01051C` | `0x00AAD2` | `memory_mgr.s:1468` | **Regs:** `Entry: A0 = block header, D0.L = physical size (including the header)`<br>MakeBKF - make the block at A0 a free block of D0 bytes Entry: A0 = block header, D0.L = physical size (including the header) Writes D0 to the header and clears the tag byte. Called during boot (46,44... |
| **`MAKEBKF`** | `0x01051C` | `0x00AAD2` | `memory_mgr.s:1010` | Called by: INITZONE_ERR, EH_CONT_2, ALLOCBK_CONT_4, ZONEADJUSTEND, SETSIZE_CONT_4 (and 1 more) |
| **`MakePtrSpc`** | `0x010ADE` | `0x00B09C` | `memory_mgr.s:2566` | **Regs:** `Entry: D0.L = logical size, A6 = zone Exit:  A2 = free block (header) or nil`<br>MakePtrSpc - make a free block of D0 bytes as low in the zone as possible Entry: D0.L = logical size, A6 = zone Exit:  A2 = free block (header) or nil Finds the first region of free and unlocked reloc... |
| **`MAKEPTRSPC`** | `0x010ADE` | `0x00B09C` | `memory_mgr.s:1886` | — |
| **`MAKEPTRSPC_CONT`** | `0x010B3C` | `0x00B108` | `memory_mgr.s:2619`<br>`memory_mgr.s:1941` | — |
| **`MAKEPTRSPC_CONT_2`** | `0x010B56` | `0x00B122` | `memory_mgr.s:2645`<br>`memory_mgr.s:1965` | MAKEPTRSPC_CONT_2 Called during boot (7,495 times in 30s trace). |
| **`MAKEPTRSPC_CONT_3`** | `0x010B60` | `0x00B12C` | `memory_mgr.s:2650`<br>`memory_mgr.s:1970` | — |
| **`MAKEPTRSPC_CONT_4`** | `0x010BB6` | `0x00B182` | `memory_mgr.s:2703`<br>`memory_mgr.s:2021` | MAKEPTRSPC_CONT_4 Called during boot (1,336 times in 30s trace). |
| **`MAKEPTRSPC_CONT_5`** | `0x010BE8` | `0x00B1B4` | `memory_mgr.s:2731`<br>`memory_mgr.s:2048` | MAKEPTRSPC_CONT_5 Called during boot (1,340 times in 30s trace). |
| **`MAKEPTRSPC_CONTINUE`** | — | `0x00B0F8` | `memory_mgr.s:1929` | — |
| **`MAKEPTRSPC_ERR`** | `0x010BAC` | `0x00B178` | `memory_mgr.s:2693`<br>`memory_mgr.s:2012` | — |
| **`MAKEPTRSPC_ERR_2`** | `0x010C30` | `0x00B1FC` | `memory_mgr.s:2764`<br>`memory_mgr.s:2081` | — |
| **`MAKEPTRSPC_ERR_3`** | `0x010C3A` | `0x00B206` | `memory_mgr.s:2773`<br>`memory_mgr.s:2089` | MAKEPTRSPC_ERR_3 |
| **`MAKEPTRSPC_EXIT`** | `0x010B34` | `0x00B100` | `memory_mgr.s:2607`<br>`memory_mgr.s:1935` | — |
| **`MAKEPTRSPC_EXIT_2`** | `0x010B50` | `0x00B11C` | `memory_mgr.s:2636`<br>`memory_mgr.s:1957` | — |
| **`MAKEPTRSPC_NO`** | `0x010AF8` | — | `memory_mgr.s:2577` | — |
| **`MAKEPTRSPC_NO_2`** | `0x010B20` | `0x00B0DE` | `memory_mgr.s:2596`<br>`memory_mgr.s:1916` | — |
| **`MAKEPTRSPC_NO_3`** | `0x010B40` | `0x00B10C` | `memory_mgr.s:2622`<br>`memory_mgr.s:1944` | — |
| **`MAKEPTRSPC_NO_4`** | `0x010C2C` | `0x00B1F8` | `memory_mgr.s:2761`<br>`memory_mgr.s:2078` | — |
| **`MAKEPTRSPC_OK`** | `0x010B0E` | `0x00B0CC` | `memory_mgr.s:2587`<br>`memory_mgr.s:1907` | — |
| **`MAKEPTRSPC_OK_2`** | `0x010B30` | `0x00B0FC` | `memory_mgr.s:2604`<br>`memory_mgr.s:1932` | — |
| **`MAKEPTRSPC_OK_3`** | `0x010B3A` | `0x00B106` | `memory_mgr.s:2617`<br>`memory_mgr.s:1939` | MAKEPTRSPC_OK_3 Called during boot. |
| **`MAKEPTRSPC_OK_4`** | `0x010B8A` | `0x00B156` | `memory_mgr.s:2669`<br>`memory_mgr.s:1989` | — |
| **`MAKEPTRSPC_OK_5`** | `0x010B9E` | `0x00B16A` | `memory_mgr.s:2685`<br>`memory_mgr.s:2004` | MAKEPTRSPC_OK_5 Called during boot (7,495 times in 30s trace). |
| **`MAKEPTRSPC_PAST_FREED`** | — | `0x00B0F4` | `memory_mgr.s:1926` | — |
| **`MAKEPTRSPC_RETRY`** | `0x010AEE` | `0x00B0AC` | `memory_mgr.s:2572`<br>`memory_mgr.s:1892` | — |
| **`MAKEPTRSPC_RETRY_2`** | `0x010B4E` | `0x00B11A` | `memory_mgr.s:2634`<br>`memory_mgr.s:1955` | MAKEPTRSPC_RETRY_2 |
| **`MAKEPTRSPC_SCAN_LOOP`** | — | `0x00B0B6` | `memory_mgr.s:1897` | — |
| **`MAKEPTRSPC_SKIP`** | `0x010B98` | `0x00B164` | `memory_mgr.s:2675`<br>`memory_mgr.s:1995` | — |
| **`MAKEPTRSPC_SKIP_2`** | `0x010BA6` | `0x00B172` | `memory_mgr.s:2689`<br>`memory_mgr.s:2008` | — |
| **`MAKEPTRSPC_SKIP_3`** | `0x010BCE` | `0x00B19A` | `memory_mgr.s:2712`<br>`memory_mgr.s:2030` | — |
| **`MAKEPTRSPC_SKIP_4`** | `0x010BE2` | `0x00B1AE` | `memory_mgr.s:2721`<br>`memory_mgr.s:2039` | — |
| **`MakeStkPB`** | `0x002DE6` | `0x004838` | `file_mgr_vol.s:362` | MakeStkPB - allocate a zeroed 64-byte IOParam block on the stack Pops the return address, pushes 32 zero words (64 bytes) onto SP, then returns with A0 -> the param block (just above return addr). |
| **`MAKESTKPB`** | `0x002DE6` | `0x004838` | `file_mgr_vol.s:329` | MAKESTKPB - build a zeroed IOParam block on the stack Allocates 64 bytes (32 words) on the stack, clears them, pushes the return address below, and returns A0 -> the IOParam block. Used for building t... |
| **`MAKESTKPB_CLRLOOP`** | `0x002DEA` | `0x00483C` | `file_mgr_vol.s:365`<br>`file_mgr_vol.s:332` | — |
| **`MapFBlock`** | `0x005D1C` | `0x0077DE` | `file_mgr_alloc.s:716` | Map F Block MapFBlock: maps file position to physical disk address (HFS) |
| **`MAPFBLOCK`** | `0x005D1C` | `0x0077DE` | `file_mgr_alloc.s:621` | — |
| **`MAPFBLOCK_CONT`** | `0x005D88` | `0x007850` | `file_mgr_alloc.s:763`<br>`file_mgr_alloc.s:666` | set up some constants calculate physical start block calculate number of available bytes |
| **`MAPFBLOCK_EXIT`** | `0x005D8A` | `0x007852` | `file_mgr_alloc.s:766`<br>`file_mgr_alloc.s:669` | MFExit |
| **`MAPFBLOCK_NO`** | `0x005D4C` | `0x007814` | `file_mgr_alloc.s:735`<br>`file_mgr_alloc.s:641` | locate the extent mapping the desired file position determine end of available space (PEOF or end of extent) |
| **`MarkA5Block`** | `0x007A02` | `0x009556` | `file_mgr_cache.s:510` | Mark A5Block Called during boot. |
| **`MARKA5BLOCK`** | `0x007A02` | `0x009556` | `file_mgr_cache.s:446` | Called by: HFSE_NO_6, HFSE_CONT_9, HFSE_NO_7, CREATE_FOUND, WRPART (and 1 more) |
| **`MarkBlock`** | `0x0079FA` | `0x009548` | `file_mgr_cache.s:501` | Mark Block Called during boot. |
| **`MARKBLOCK`** | `0x0079FA` | `0x009548` | `file_mgr_cache.s:439` | Called by: HFSCATMOVE_CONT_3, SETFILEINFO_MFS_FLUSH, BLKALLOC_OK_2, BLKALLOC_NO_5, BLKDEALLOC_CONT (and 12 more) |
| **`MarkEmpty`** | `0x0079E8` | `0x00953C` | `file_mgr_cache.s:482`<br>`file_mgr_cache.s:434` | MarkEmpty - MarkEmpty: mark buffer empty and zero disk block Called during boot. |
| **`MarkVCB`** | `0x002D1E` | `0x004766` | `file_mgr_vol.s:276` | MarkVCB - mark VCB dirty and update last-modification time Sets the dirty flag (vcbFlags byte, offset 6) and stores the current system time in vcbLsMod (offset 0xE=14). |
| **`MARKVCB`** | `0x002D1E` | `0x004766` | `file_mgr_vol.s:240` | MARKVCB - mark volume dirty and update modification time Called by: SETVOLINFO_RENAME_DONE, SETVOLINFO_HFS_OK, HFSE_OK_5, CREATE_MFS_BUMP_NMFLS, HFSCATMOVE_NO_3 (and 6 more) |
| **`MarkVCBTime`** | `0x002D20` | `0x004768` | `file_mgr_vol.s:280` | MarkVCBTime -- mark the VCB dirty. Called by: HFSCATMOVE_OK_6, CC_UPD_PAR, DC_UPD_PAR, MC_EXIT, RC_EXIT (and 1 more) |
| **`MARKVCBTIME`** | `0x002D20` | `0x004768` | `file_mgr_vol.s:244` | MARKVCBTIME - update volume modification timestamp Called by: HFSCATMOVE_OK_6, CC_UPD_PAR, DC_UPD_PAR, CMMOVECN_EXIT, CMRENAMECN_EXIT (and 1 more) |
| **`MaxApplZone`** | `0x0100AE` | `0x00A5C2` | `memory_mgr.s:472` | _MaxApplZone ($A063) -> (grows app zone to maximum) |
| **`MAXAPPLZONE`** | `0x0100AE` | `0x00A5C2` | `memory_mgr.s:306` | — |
| **`MAXAPPLZONE_NO_ROOM`** | — | `0x00A5EC` | `memory_mgr.s:323` | — |
| **`MAXAPPLZONE_SKIP`** | `0x0100D4` | — | `memory_mgr.s:488` | — |
| **`MaxBlock`** | `0x00FFB0` | `0x00A4C0` | `memory_mgr.s:261` | **Proto:** `Pascal: FUNCTION MaxBlock: LONGINT;`<br>**Regs:** `Entry: trap bit 10 ($A461) = use the system heap Exit:  D0.L = logical size of the largest contiguous free space that`<br>_MaxBlock ($A061): largest block that compacting the zone could make Pascal: FUNCTION MaxBlock: LONGINT; Entry: trap bit 10 ($A461) = use the system heap Exit:  D0.L = logical size of the largest cont... |
| **`MAXBLOCK`** | `0x00FFB0` | `0x00A4C0` | `memory_mgr.s:195` | — |
| **`MAXBLOCK_DO_COMPACT`** | — | `0x00A4EC` | `memory_mgr.s:213` | — |
| **`MAXBLOCK_OR_COMPACT`** | — | `0x00A4D4` | `memory_mgr.s:203` | — |
| **`MaxLimit`** | `0x010850` | `0x00AE06` | `memory_mgr.s:2124` | MaxLimit -- compute max growable limit. |
| **`MAXLIMIT`** | `0x010850` | `0x00AE06` | `memory_mgr.s:1537` | — |
| **`MAXLIMIT_OK`** | `0x010860` | `0x00AE1E` | `memory_mgr.s:2131`<br>`memory_mgr.s:1546` | — |
| **`MaxMem`** | `0x01003C` | `0x00A54C` | `memory_mgr.s:400` | **Proto:** `Pascal: FUNCTION MaxMem(VAR grow: Size): Size;`<br>**Regs:** `Entry: trap bit 10 ($A51D) = use the system heap Exit:  D0.L = logical size of the largest contiguous free block;`<br>_MaxMem ($A11D): compact and purge the zone, return its largest free block Pascal: FUNCTION MaxMem(VAR grow: Size): Size; Entry: trap bit 10 ($A51D) = use the system heap Exit:  D0.L = logical size of... |
| **`MAXMEM`** | `0x01003C` | `0x00A54C` | `memory_mgr.s:259` | — |
| **`MAXMEM_CONT`** | `0x010052` | `0x00A562` | `memory_mgr.s:408`<br>`memory_mgr.s:267` | — |
| **`MAXMEM_DONE`** | — | `0x00A57C` | `memory_mgr.s:276` | — |
| **`MAXMEM_SKIP`** | `0x01006C` | — | `memory_mgr.s:417` | — |
| **`MC_BAD_MOVE`** | `0x006336` | `0x007E02` | `file_mgr_catalog.s:363`<br>`file_mgr_catalog.s:320` | MCChkAncestors: check moving into own descendant |
| **`MC_CHK_ANCESTOR`** | `0x006318` | `0x007DE4` | `file_mgr_catalog.s:351`<br>`file_mgr_catalog.s:309` | MCChkAncestor: prevent moving directory into its own descendant |
| **`MC_CHK_DEST`** | `0x0062E8` | `0x007DB4` | `file_mgr_catalog.s:332`<br>`file_mgr_catalog.s:289` | MCChkSrc: make sure source CNode exists MCChkDest: make sure destination exists and is a directory |
| **`MC_CHK_DST_DIR`** | `0x006304` | `0x007DD0` | `file_mgr_catalog.s:343`<br>`file_mgr_catalog.s:300` | MCChkDst: check for invalid move operation |
| **`MC_COPY_SRC`** | `0x006358` | `0x007E24` | `file_mgr_catalog.s:378`<br>`file_mgr_catalog.s:335` | MCCopySrc: save source record data |
| **`MC_ERR_EXIT`** | `0x006454` | — | `file_mgr_catalog.s:474` | — |
| **`MC_EXIT`** | `0x006448` | — | `file_mgr_catalog.s:469` | update VCB counts for source MCExit |
| **`MC_INSERT_DST`** | `0x00638C` | `0x007E58` | `file_mgr_catalog.s:399`<br>`file_mgr_catalog.s:357` | MCBldDst: build destination key and insert |
| **`MC_LOC_SRC`** | `0x00633E` | `0x007E0A` | `file_mgr_catalog.s:367`<br>`file_mgr_catalog.s:324` | MCLocSrc: locate source CNode record |
| **`MC_UPD_DEST`** | `0x0063A4` | `0x007E70` | `file_mgr_catalog.s:408`<br>`file_mgr_catalog.s:366` | MCUpdDest: update destination parent directory |
| **`MC_UPD_SRC`** | `0x00641A` | `0x007EE6` | `file_mgr_catalog.s:451`<br>`file_mgr_catalog.s:409` | update VCB counts for destination MCDelSrc: delete source record MCUpdThd: update thread record if directory MCUpdSrc: update source parent directory |
| **`MEMINIT_DONE`** | — | `0x00A4A8` | `memory_mgr.s:183` | — |
| **`MEMMGREND`** | — | `0x00B28C` | `memory_mgr.s:2155` | — |
| **`MM_CLEAR_BLOCK_RTS`** | — | `0x00A650` | `memory_mgr.s:382` | — |
| **`MM_HANDLE_EPILOGUE`** | — | `0x00A680` | `memory_mgr.s:407` | — |
| **`MM_HANDLE_NOERR`** | — | `0x00A67E` | `memory_mgr.s:405` | — |
| **`MM_PTR_EPILOGUE`** | — | `0x00A602` | `memory_mgr.s:338` | — |
| **`MMEpilogue`** | `0x01050A` | `0x00AAC0` | `memory_mgr.s:1451` | MMEpilogue - standard exit of the Memory Manager traps MemErr := 0 if D0.L >= 0 (noErr, or a size returned in D0), else MemErr := D0.W; then restores D3-D7/A2-A6 and returns to the trap dispatcher. MM... |
| **`MMEPILOGUE`** | `0x01050A` | `0x00AAC0` | `memory_mgr.s:1000` | Called by: PURGEMEM_ERR, MAXMEM_DONE, MM_PTR_EPILOGUE, NEWEMPTYHANDLE, MM_HANDLE_EPILOGUE (and 2 more) |
| **`MMEPILOGUE_ERR`** | `0x010512` | `0x00AAC8` | `memory_mgr.s:1455`<br>`memory_mgr.s:1004` | — |
| **`MMHPrologue`** | `0x0104C6` | `0x00AA20` | `memory_mgr.s:1383` | **Regs:** `Entry: A0 = handle, D0 = trap argument Exit:  A0 = masked data pointer (nil if empty), A1 = masked handle,`<br>MMHPrologue - standard entry of the handle traps Saves D3-D7/A2-A6 (MMEpilogue restores them) and dereferences the handle in A0 (DerefHandle). If the master pointer is non-nil, the zone is found from ... |
| **`MMHPROLOGUE`** | `0x0104C6` | `0x00AA20` | `memory_mgr.s:927` | Called by: DSPOSEHANDLE, GETHANDLESIZE, SETHANDLESIZE, HANDLEZONE, EMPTYHANDLE (and 2 more) |
| **`MMHPROLOGUE_CHECK`** | — | `0x00AA34` | `memory_mgr.s:936` | — |
| **`MMHPROLOGUE_CONT`** | `0x0104DA` | — | `memory_mgr.s:1392` | — |
| **`MMHPROLOGUE_EMPTY`** | `0x0104E2` | — | `memory_mgr.s:1403` | MMHPROLOGUE_EMPTY Called during boot. |
| **`MMHPROLOGUE_ERR`** | `0x0104E6` | `0x00AA5C` | `memory_mgr.s:1411`<br>`memory_mgr.s:956` | MMHPROLOGUE_ERR |
| **`MMHPROLOGUE_FIND_ZONE`** | — | `0x00AA3C` | `memory_mgr.s:941` | — |
| **`MMHPROLOGUE_TRY_SYS`** | — | `0x00AA50` | `memory_mgr.s:949` | — |
| **`MMHPROLOGUE_VALIDATE`** | — | `0x00AA58` | `memory_mgr.s:953` | — |
| **`MMNOERREPILOGUE`** | — | `0x00AACC` | `memory_mgr.s:1006` | — |
| **`MMPPrologue`** | `0x0104B2` | `0x00AA0C` | `memory_mgr.s:1356` | **Regs:** `Entry: A0 = pointer, D0 = trap argument Exit:  A0 = masked pointer, A1 = nil, A6 = zone, D0 preserved (copy in D2)`<br>MMPPrologue - standard entry of the pointer traps Saves D3-D7/A2-A6 (MMEpilogue restores them), sets A1 = nil and finds the zone of the block at A0 (DEREFHANDLE_CONT). On memWZErr/memAZErr the trap is... |
| **`MMPPROLOGUE`** | `0x0104B2` | `0x00AA0C` | `memory_mgr.s:916` | — |
| **`MMPrologue`** | `0x0104EA` | `0x00AA60` | `memory_mgr.s:1427` | **Regs:** `Entry: D0 = trap argument, D1 = trap word Exit:  A6 = zone, D0 preserved (copy in D2)`<br>MMPrologue - standard entry of the traps that work on a whole zone Saves D3-D7/A2-A6 (MMEpilogue restores them) and sets A6 = TheZone, or SysZone if trap bit 10 (SYS) is set in D1; the trap is abandon... |
| **`MMPROLOGUE`** | `0x0104EA` | `0x00AA60` | `memory_mgr.s:960` | Called by: MAXBLOCK, COMPACTMEM, PURGEMEM, PURGESPACE, FREEMEM (and 5 more) |
| **`MMPROLOGUE_NO`** | `0x010502` | — | `memory_mgr.s:1436` | — |
| **`MMPROLOGUE_ZONE`** | — | `0x00AA78` | `memory_mgr.s:969` | — |
| **`MMRHPROLOGUE`** | — | `0x00AA82` | `memory_mgr.s:974` | — |
| **`MMRHPROLOGUE_CHK_LOC`** | — | `0x00AAA6` | `memory_mgr.s:988` | — |
| **`MMRHPROLOGUE_TRY_SYS`** | — | `0x00AAA2` | `memory_mgr.s:986` | — |
| **`MMRHPROLOGUE_VALIDATE`** | — | `0x00AAB6` | `memory_mgr.s:994` | — |
| **`MoreMasters`** | `0x010274` | `0x00A7B8` | `memory_mgr.s:976` | _MoreMasters ($A036) -> (allocates 32 more master pointers) Called during boot. |
| **`MOREMASTERS`** | `0x010274` | `0x00A7B8` | `memory_mgr.s:573` | — |
| **`MOREMASTERS_SKIP`** | `0x010284` | `0x00A7C8` | `memory_mgr.s:983`<br>`memory_mgr.s:580` | — |
| **`MountVol`** | `0x002DF8` | `0x00484A` | `file_mgr_vol.s:375` | Called during boot. _MountVol: mount a volume from disk |
| **`MOUNTVOL`** | `0x002DF8` | `0x00484A` | `file_mgr_vol.s:344` | **Regs:** `Entry: A0 = IOParam, ioVRefNum (+$16) = drive number`<br>MOUNTVOL - _MountVol trap: mount a volume on a drive Entry: A0 = IOParam, ioVRefNum (+$16) = drive number Attempts to mount. On volOnLinErr (-42) or extFSErr (-58), offlines stale volumes and retries. |
| **`MOUNTVOL_ALLOC_VCB`** | — | `0x0048BE` | `file_mgr_vol.s:405` | Find drive and allocate VCB |
| **`MOUNTVOL_CONT`** | `0x002E1C` | `0x00486E` | `file_mgr_vol.s:390`<br>`file_mgr_vol.s:360` | — |
| **`MOUNTVOL_CONT_10`** | `0x003170` | `0x004BBE` | `file_mgr_vol.s:723`<br>`file_mgr_vol.s:680` | — |
| **`MOUNTVOL_CONT_11`** | `0x00330A` | `0x004D8A` | `file_mgr_vol.s:902`<br>`file_mgr_vol.s:871` | position to start of extent file extent file scan loop |
| **`MOUNTVOL_CONT_12`** | `0x003322` | — | `file_mgr_vol.s:913` | extent scan done: recount free blocks and finish |
| **`MOUNTVOL_CONT_2`** | `0x002E44` | `0x004896` | `file_mgr_vol.s:410`<br>`file_mgr_vol.s:380` | — |
| **`MOUNTVOL_CONT_3`** | `0x002E48` | — | `file_mgr_vol.s:420` | MOUNTVOL_CONT_3 Called during boot. MOUNTVOL_CONT_3: main mount path (called from MountVol) |
| **`MOUNTVOL_CONT_4`** | `0x002E50` | `0x0048A2` | `file_mgr_vol.s:423`<br>`file_mgr_vol.s:392` | Validate drive number and check for existing mount |
| **`MOUNTVOL_CONT_5`** | `0x002EBE` | `0x004910` | `file_mgr_vol.s:465`<br>`file_mgr_vol.s:431` | assign a refNum to this new volume |
| **`MOUNTVOL_CONT_6`** | `0x002F00` | `0x004952` | `file_mgr_vol.s:491`<br>`file_mgr_vol.s:455` | check what manner of animal we have before us mv_GotMDB: now do a little more checking |
| **`MOUNTVOL_CONT_7`** | `0x00300C` | `0x004A5E` | `file_mgr_vol.s:572`<br>`file_mgr_vol.s:537` | — |
| **`MOUNTVOL_CONT_8`** | `0x003048` | `0x004A9A` | `file_mgr_vol.s:604`<br>`file_mgr_vol.s:565` | MOUNTVOL_FOUND remount found: verify all open FCBs still match catalog |
| **`MOUNTVOL_CONT_9`** | `0x003068` | — | `file_mgr_vol.s:615` | MFS verification: check file entry in MFS directory |
| **`MOUNTVOL_CORE`** | — | `0x00489A` | `file_mgr_vol.s:388` | MOUNTVOL_CORE - core mount procedure Validates drive, allocates VCB (178 bytes), reads MDB (block 2), validates signature, copies MDB fields to VCB, opens catalog and extent B-tree files. Per Inside M... |
| **`MOUNTVOL_DEQUEUE_NEW_VCB`** | — | `0x004B6A` | `file_mgr_vol.s:640` | update B-tree FCB volume pointers for HFS dequeue and dispose the new VCB (keep old one) |
| **`MOUNTVOL_ENQUEUE_VCB`** | — | `0x0048F8` | `file_mgr_vol.s:423` | — |
| **`MOUNTVOL_ERR_BRA`** | — | `0x0048BA` | `file_mgr_vol.s:402` | — |
| **`MOUNTVOL_EXIT`** | `0x002E68` | — | `file_mgr_vol.s:434` | mv_Start: see if the disk is already mounted |
| **`MOUNTVOL_FOUND`** | `0x003044` | — | `file_mgr_vol.s:602` | MOUNTVOL_FOUND remount found: verify all open FCBs still match catalog |
| **`MOUNTVOL_FOUND_2`** | `0x003078` | `0x004AC6` | `file_mgr_vol.s:621`<br>`file_mgr_vol.s:582` | — |
| **`MOUNTVOL_FOUND_3`** | `0x0031C0` | `0x004C40` | `file_mgr_vol.s:768`<br>`file_mgr_vol.s:745` | check if volume name in catalog matches VCB volume name changed: rename root directory to match VCB verify bitmap for extent and catalog B-tree files |
| **`MOUNTVOL_LOOP`** | `0x003034` | `0x004A86` | `file_mgr_vol.s:587`<br>`file_mgr_vol.s:552` | compare the volume names |
| **`MOUNTVOL_MFS_DIR_LOOP`** | — | `0x004AB8` | `file_mgr_vol.s:576` | MFS remount verification: check file in MFS directory |
| **`MOUNTVOL_NO`** | `0x002E6C` | — | `file_mgr_vol.s:437` | mv_getDrive: find drive queue entry and allocate a VCB |
| **`MOUNTVOL_NO_10`** | `0x003242` | `0x004CC2` | `file_mgr_vol.s:821`<br>`file_mgr_vol.s:797` | file record |
| **`MOUNTVOL_NO_11`** | `0x003256` | `0x004CD6` | `file_mgr_vol.s:829`<br>`file_mgr_vol.s:804` | — |
| **`MOUNTVOL_NO_12`** | `0x003260` | `0x004CE0` | `file_mgr_vol.s:833`<br>`file_mgr_vol.s:808` | — |
| **`MOUNTVOL_NO_2`** | `0x002EA6` | — | `file_mgr_vol.s:456` | first VCB: set up as default |
| **`MOUNTVOL_NO_3`** | `0x003040` | `0x004A92` | `file_mgr_vol.s:593`<br>`file_mgr_vol.s:559` | Called by: MOUNTVOL_CONT_7, MOUNTVOL_OK_3, MOUNTVOL_LOOP, MOUNTVOL_CONT_8, MOUNTVOL_MFS_DIR_LOOP (and 2 more) |
| **`MOUNTVOL_NO_4`** | `0x003088` | `0x004AD6` | `file_mgr_vol.s:626`<br>`file_mgr_vol.s:587` | — |
| **`MOUNTVOL_NO_5`** | `0x0030D2` | `0x004B1E` | `file_mgr_vol.s:651`<br>`file_mgr_vol.s:612` | — |
| **`MOUNTVOL_NO_6`** | `0x0030FC` | `0x004B4A` | `file_mgr_vol.s:667`<br>`file_mgr_vol.s:628` | all FCBs verified: this is a valid remount copy new VCB data into old VCB (transfer mount to existing VCB) |
| **`MOUNTVOL_NO_7`** | `0x00311C` | — | `file_mgr_vol.s:678` | update B-tree FCB VCB pointers for TFS volumes |
| **`MOUNTVOL_NO_8`** | `0x00317E` | `0x004BCC` | `file_mgr_vol.s:729`<br>`file_mgr_vol.s:686` | remount error: clean up the remounted VCB's TFS-specific fields |
| **`MOUNTVOL_NO_9`** | `0x003236` | `0x004CB6` | `file_mgr_vol.s:815`<br>`file_mgr_vol.s:791` | check record type: directory or file? |
| **`MOUNTVOL_OK`** | `0x002E18` | `0x00486A` | `file_mgr_vol.s:388`<br>`file_mgr_vol.s:358` | Scan VCB queue for offline-but-mounted volumes to force offline |
| **`MOUNTVOL_OK_2`** | `0x002E30` | `0x004882` | `file_mgr_vol.s:401`<br>`file_mgr_vol.s:371` | offline the stale volume and retry mount |
| **`MOUNTVOL_OK_3`** | `0x003096` | `0x004AE2` | `file_mgr_vol.s:633`<br>`file_mgr_vol.s:594` | TFS verification: look up catalog record |
| **`MOUNTVOL_OK_4`** | `0x003272` | — | `file_mgr_vol.s:846` | verify bitmap for file's extents MOUNTVOL_OK_4 scan complete (end of catalog): update VCB counters |
| **`MOUNTVOL_OK_5`** | `0x00328E` | `0x004D0E` | `file_mgr_vol.s:857`<br>`file_mgr_vol.s:826` | fix up VCBNxtCNID if needed compare counted values against VCB |
| **`MOUNTVOL_OK_6`** | `0x0032A0` | `0x004D20` | `file_mgr_vol.s:863`<br>`file_mgr_vol.s:832` | — |
| **`MOUNTVOL_OK_7`** | `0x0032B2` | `0x004D32` | `file_mgr_vol.s:869`<br>`file_mgr_vol.s:838` | — |
| **`MOUNTVOL_OK_8`** | `0x0032C4` | `0x004D44` | `file_mgr_vol.s:875`<br>`file_mgr_vol.s:844` | — |
| **`MOUNTVOL_OK_9`** | `0x0032D8` | `0x004D58` | `file_mgr_vol.s:883`<br>`file_mgr_vol.s:852` | now scan extent overflow file to verify those bitmaps too |
| **`MOUNTVOL_REMOUNT_NEXT_FCB`** | — | `0x004B26` | `file_mgr_vol.s:615` | — |
| **`MOUNTVOL_REMOUNT_VERIFY`** | — | `0x004A96` | `file_mgr_vol.s:563` | remount found: verify all open FCBs still match catalog |
| **`MOUNTVOL_RETRY`** | `0x002E14` | `0x004866` | `file_mgr_vol.s:386`<br>`file_mgr_vol.s:355` | retry: offline any stale offline-but-mounted volumes and try again |
| **`MOUNTVOL_SKIP`** | `0x002E2C` | `0x00487E` | `file_mgr_vol.s:397`<br>`file_mgr_vol.s:367` | — |
| **`MOUNTVOL_SKIP_2`** | `0x002EDC` | `0x00492E` | `file_mgr_vol.s:476`<br>`file_mgr_vol.s:441` | mv_GetMDB: read the master directory block |
| **`MOUNTVOL_SKIP_3`** | `0x0030D8` | — | `file_mgr_vol.s:654` | — |
| **`MOUNTVOL_SKIP_4`** | `0x003154` | — | `file_mgr_vol.s:701` | — |
| **`MOUNTVOL_SKIP_5`** | `0x003206` | `0x004C86` | `file_mgr_vol.s:795`<br>`file_mgr_vol.s:772` | scan entire catalog to recount files and directories calculate total number of catalog leaf records initialize counters for consistency check catalog scan loop: count files, directories, verify bitmap... |
| **`MOUSE_PROCESS_RTS`** | — | `0x003ABE` | `adb_mgr.s:828` | — |
| **`MOUSE_PROCESS_X`** | — | `0x003AA6` | `adb_mgr.s:819` | Process X delta (horizontal mouse movement) |
| **`MOUSE_PROCESS_Y`** | — | `0x003A8E` | `adb_mgr.s:809` | Button state changed: post mouse event Process Y delta (vertical mouse movement) |
| **`MoveHHi`** | `0x01028C` | `0x00A7D6` | `memory_mgr.s:995` | _MoveHHi ($A064) A0 = handle -> (moved to top of heap) Called during boot (3,693 times in 30s trace). _MoveHHi ($A064): move relocatable block to top of heap |
| **`MOVEHHI`** | `0x01028C` | `0x00A7D6` | `memory_mgr.s:602` | MOVEHHI -- _MoveHHi ($A064): move the relocatable block of handle A0 as high as possible in its heap zone (A6, found by MMHPROLOGUE): into the free block at the top of the zone if the data fits, other... |
| **`MOVEHHI_CONT`** | `0x010298` | `0x00A7E2` | `memory_mgr.s:1002`<br>`memory_mgr.s:609` | check if block is locked (can't move locked blocks) |
| **`MOVEHHI_CONT_2`** | `0x010334` | `0x00A888` | `memory_mgr.s:1067`<br>`memory_mgr.s:676` | — |
| **`MOVEHHI_CONT_3`** | `0x01033A` | `0x00A88E` | `memory_mgr.s:1071`<br>`memory_mgr.s:680` | — |
| **`MOVEHHI_CONT_4`** | `0x01038A` | `0x00A8DE` | `memory_mgr.s:1112`<br>`memory_mgr.s:716` | — |
| **`MOVEHHI_CONT_5`** | `0x0103DC` | `0x00A936` | `memory_mgr.s:1166`<br>`memory_mgr.s:768` | MOVEHHI_CONT_5 Called during boot. |
| **`MOVEHHI_CONT_6`** | `0x010416` | `0x00A970` | `memory_mgr.s:1212`<br>`memory_mgr.s:806` | MOVEHHI_CONT_6 -- copy chunk to stack buffer. MOVEHHI_CONT_6 |
| **`MOVEHHI_CONT_7`** | `0x01043E` | `0x00A998` | `memory_mgr.s:1236`<br>`memory_mgr.s:829` | MOVEHHI_CONT_7 |
| **`MOVEHHI_CONT_8`** | `0x010454` | `0x00A9AE` | `memory_mgr.s:1253`<br>`memory_mgr.s:845` | MOVEHHI_CONT_8 -- compact heap. MOVEHHI_CONT_8 |
| **`MOVEHHI_DONE`** | `0x010414` | `0x00A96E` | `memory_mgr.s:1204`<br>`memory_mgr.s:804` | — |
| **`MOVEHHI_EMPTY`** | `0x0103EA` | `0x00A944` | `memory_mgr.s:1178`<br>`memory_mgr.s:779` | MOVEHHI_EMPTY |
| **`MOVEHHI_EPILOGUE`** | — | `0x00A932` | `memory_mgr.s:761` | — |
| **`MOVEHHI_ERR`** | `0x010294` | — | `memory_mgr.s:999` | — |
| **`MOVEHHI_EXIT`** | `0x0103D8` | — | `memory_mgr.s:1158` | — |
| **`MOVEHHI_NEXT`** | `0x010358` | `0x00A8AC` | `memory_mgr.s:1089`<br>`memory_mgr.s:693` | — |
| **`MOVEHHI_NEXT_2`** | `0x010390` | `0x00A8E4` | `memory_mgr.s:1122`<br>`memory_mgr.s:725` | — |
| **`MOVEHHI_NO`** | `0x0102A2` | `0x00A7EC` | `memory_mgr.s:1009`<br>`memory_mgr.s:616` | scan from block to bkLim, measuring free space above |
| **`MOVEHHI_NO_2`** | `0x0102E8` | `0x00A832` | `memory_mgr.s:1037`<br>`memory_mgr.s:644` | — |
| **`MOVEHHI_NO_3`** | `0x01034A` | `0x00A89E` | `memory_mgr.s:1084`<br>`memory_mgr.s:688` | MOVEHHI_NO_3 |
| **`MOVEHHI_NO_4`** | `0x01038E` | `0x00A8E2` | `memory_mgr.s:1120`<br>`memory_mgr.s:723` | MOVEHHI_NO_4 |
| **`MOVEHHI_NO_5`** | `0x0103EE` | `0x00A948` | `memory_mgr.s:1180`<br>`memory_mgr.s:781` | — |
| **`MOVEHHI_NO_6`** | `0x010420` | `0x00A97A` | `memory_mgr.s:1217`<br>`memory_mgr.s:811` | — |
| **`MOVEHHI_OK`** | `0x0102CE` | `0x00A818` | `memory_mgr.s:1027`<br>`memory_mgr.s:634` | — |
| **`MOVEHHI_OK_2`** | `0x0103B0` | `0x00A904` | `memory_mgr.s:1140`<br>`memory_mgr.s:742` | MOVEHHI_OK_2 Called during boot. |
| **`MOVEHHI_OK_3`** | `0x010404` | `0x00A95E` | `memory_mgr.s:1190`<br>`memory_mgr.s:791` | — |
| **`MOVEHHI_OK_4`** | `0x01040E` | `0x00A968` | `memory_mgr.s:1201`<br>`memory_mgr.s:801` | MOVEHHI_OK_4 |
| **`MOVEHHI_RETURN`** | — | `0x00A7DE` | `memory_mgr.s:606` | — |
| **`MOVEHHI_SKIP`** | `0x0103BE` | `0x00A912` | `memory_mgr.s:1147`<br>`memory_mgr.s:749` | — |
| **`MOVOFF_RETURN`** | `0x00759A` | `0x0090EE` | `file_mgr_btree.s:2065`<br>`file_mgr_btree.s:1805` | — |
| **`MovOffLT`** | `0x00757A` | `0x0090CE` | `file_mgr_btree.s:2044` | Mov Off LT - move offsets left within a single node |
| **`MOVOFFLT`** | `0x00757A` | `0x0090CE` | `file_mgr_btree.s:1788` | MovOffLT: shift D0+1 offset entries left, adding D1 to each |
| **`MOVOFFLT_LOOP`** | `0x00757E` | `0x0090D2` | `file_mgr_btree.s:2046`<br>`file_mgr_btree.s:1790` | — |
| **`MovOffRT`** | `0x00758A` | `0x0090DE` | `file_mgr_btree.s:2057` | Mov Off RT - move offsets right within a single node |
| **`MOVOFFRT`** | `0x00758A` | `0x0090DE` | `file_mgr_btree.s:1797` | MovOffRT: shift D0+1 offset entries right, adding D1 to each |
| **`MOVOFFRT_LOOP`** | `0x007590` | `0x0090E4` | `file_mgr_btree.s:2060`<br>`file_mgr_btree.s:1800` | — |
| **`MovRecLT`** | `0x0075A0` | `0x0090F4` | `file_mgr_btree.s:2074` | Mov Rec LT MovRecLt: move records left within a single node |
| **`MOVRECLT`** | `0x0075A0` | `0x0090F4` | `file_mgr_btree.s:1809` | MovRecLT: copy D0 bytes forward (A0)+ -> (A1)+ |
| **`MOVRECLT_EXIT`** | `0x0075B0` | `0x009104` | `file_mgr_btree.s:2082`<br>`file_mgr_btree.s:1817` | — |
| **`MOVRECLT_LOOP`** | `0x0075AA` | `0x0090FE` | `file_mgr_btree.s:2079`<br>`file_mgr_btree.s:1814` | — |
| **`MovRecRT`** | `0x0075B6` | `0x00910A` | `file_mgr_btree.s:2090` | Mov Rec RT - move records right within a single node |
| **`MOVRECRT`** | `0x0075B6` | `0x00910A` | `file_mgr_btree.s:1821` | MovRecRT: copy D0 bytes backward -(A0) -> -(A1) |
| **`MOVRECRT_EXIT`** | `0x0075CA` | `0x00911E` | `file_mgr_btree.s:2100`<br>`file_mgr_btree.s:1831` | — |
| **`MOVRECRT_LOOP`** | `0x0075C4` | `0x009118` | `file_mgr_btree.s:2097`<br>`file_mgr_btree.s:1828` | — |
| **`MTCHECK`** | `0x003190` | `0x004BDE` | `file_mgr_vol.s:744`<br>`file_mgr_vol.s:696` | MTCHECK MtCheck: disk consistency check (runs on first mount after unclean shutdown) |
| **`MTCHECK_COPY_NAME_LOOP`** | — | `0x004C3A` | `file_mgr_vol.s:741` | — |
| **`MTCHECK_EXT_SCAN_DONE`** | — | `0x004DA2` | `file_mgr_vol.s:882` | extent scan done: recount free blocks |
| **`MTCHECK_NAME_TRUNC_OK`** | — | `0x004C34` | `file_mgr_vol.s:737` | — |
| **`MTCHECK_RENAME_FROM_CAT`** | — | `0x004C24` | `file_mgr_vol.s:730` | VCB name empty: use catalog name to rename |
| **`MTCHECK_RENAME_FROM_VCB`** | — | `0x004C14` | `file_mgr_vol.s:721` | check if volume name in catalog matches VCB volume name changed: rename root directory to match VCB |
| **`MTCHECK_SCAN_DONE`** | — | `0x004CF2` | `file_mgr_vol.s:815` | scan complete: update VCB counters if needed |
| **`MTCHKERR`** | `0x003158` | `0x004BA6` | `file_mgr_vol.s:709`<br>`file_mgr_vol.s:666` | MTCHKERR MtChkErr: B-tree open errors during mount |
| **`MTVOLDONE`** | `0x00313A` | `0x004B88` | `file_mgr_vol.s:692`<br>`file_mgr_vol.s:653` | MtVolDone |
| **`MTVOLDONE_EXIT`** | — | `0x004BA2` | `file_mgr_vol.s:662` | — |
| **`MTVOLER1`** | `0x003162` | — | `file_mgr_vol.s:716` | MtVolEr1: shared MFS/TFS error exit |
| **`MTVOLER1_FLUSH_CACHES`** | — | `0x004BB0` | `file_mgr_vol.s:673` | MtVolEr1: flush and trash volume caches |
| **`MTVOLER2`** | `0x003166` | `0x004BB4` | `file_mgr_vol.s:719`<br>`file_mgr_vol.s:676` | MtVolEr2: release VCB and exit |
| **`MTVOLERR`** | `0x00315E` | — | `file_mgr_vol.s:713` | MtVolErr: close any opened B-tree files |
| **`MTVOLERR_CLOSE_BT`** | — | `0x004BAC` | `file_mgr_vol.s:670` | MtVolErr: close any opened B-tree files |
| **`MTVOLOK`** | `0x003138` | `0x004B86` | `file_mgr_vol.s:689`<br>`file_mgr_vol.s:650` | dequeue and dispose the new VCB (keep the old one) MtVolOK |
| **`NewEmptyHandle`** | `0x01013A` | `0x00A652` | `memory_mgr.s:616` | _NewEmptyHandle ($A066): allocate a master pointer with nil handle |
| **`NEWEMPTYHANDLE`** | `0x01013A` | `0x00A652` | `memory_mgr.s:384` | — |
| **`NewHandle`** | `0x01014E` | `0x012EBA` | `memory_mgr.s:643` | **Proto:** `Pascal: FUNCTION NewHandle(logicalSize: Size): Handle;`<br>**Regs:** `Entry: D0.L = logicalSize; trap bit 9 ($A322) = clear the block, Exit:  A0 = handle (nil on failure), D0.W = noErr or memFullErr;`<br>_NewHandle ($A122): allocate a relocatable block Pascal: FUNCTION NewHandle(logicalSize: Size): Handle; Entry: D0.L = logicalSize; trap bit 9 ($A322) = clear the block, bit 10 ($A522) = allocate in th... |
| **`NEWHANDLE_2`** | `0x01016C` | `0x00A684` | `memory_mgr.s:672`<br>`memory_mgr.s:409` | NEWHANDLE_2 - NewHandle: no room for the block; free the master pointer |
| **`NEWHANDLE_ALLOC`** | `0x01015C` | `0x00A674` | `memory_mgr.s:657`<br>`memory_mgr.s:399` | NEWHANDLE_ALLOC - NewHandle: got master pointer A1, now allocate the block NEWHANDLE_CONT is also ReallocHandle's success path; NEWHANDLE_EXIT and NEWHANDLE_EXIT_2 are common exits of the handle traps... |
| **`NEWHANDLE_CONT`** | `0x010162` | `0x00A67A` | `memory_mgr.s:660`<br>`memory_mgr.s:402` | — |
| **`NEWHANDLE_EMPTY`** | `0x010158` | `0x00A670` | `memory_mgr.s:647`<br>`memory_mgr.s:396` | — |
| **`NEWHANDLE_EXIT`** | `0x010166` | — | `memory_mgr.s:663` | — |
| **`NEWHANDLE_EXIT_2`** | `0x010168` | — | `memory_mgr.s:665` | — |
| **`NewPtr`** | `0x0100D6` | `0x00A5EE` | `memory_mgr.s:509` | **Proto:** `Pascal: FUNCTION NewPtr(logicalSize: Size): Ptr;`<br>**Regs:** `Entry: D0.L = logicalSize; trap bit 9 ($A31E) = clear the block, Exit:  A0 = pointer to the block (nil on failure), D0.W = result code`<br>_NewPtr ($A11E): allocate a nonrelocatable block Pascal: FUNCTION NewPtr(logicalSize: Size): Ptr; Entry: D0.L = logicalSize; trap bit 9 ($A31E) = clear the block, bit 10 ($A51E) = allocate in the syst... |
| **`NEWPTR`** | `0x0100D6` | `0x00A5EE` | `memory_mgr.s:329` | NewPtr: zone locked, allocate directly |
| **`NEWPTR_ERR`** | `0x0100EA` | — | `memory_mgr.s:518` | — |
| **`NEWPTR_ERR_2`** | `0x0100EE` | `0x00A606` | `memory_mgr.s:525`<br>`memory_mgr.s:340` | NEWPTR_ERR_2 - NewPtr: no room; return memFullErr (A0 = nil from AllocBK) |
| **`NEWPTR_EXIT`** | `0x0100E8` | `0x00A600` | `memory_mgr.s:516`<br>`memory_mgr.s:336` | — |
| **`NextMaster`** | `0x010A88` | `0x00B046` | `memory_mgr.s:2495` | NextMaster -- get free master pointer -> A1. |
| **`NEXTMASTER`** | `0x010A88` | `0x00B046` | `memory_mgr.s:1845` | ADJUSTFREE_ERR |
| **`NEXTMASTER_CONT`** | `0x010A98` | `0x00B056` | `memory_mgr.s:2502`<br>`memory_mgr.s:1852` | — |
| **`NEXTMASTER_ERR`** | `0x010A9E` | `0x00B05C` | `memory_mgr.s:2505`<br>`memory_mgr.s:1855` | — |
| **`NOPKG_SYSERROR`** | `0x00295A` | `0x00439C` | `file_mgr_queue.s:182`<br>`file_mgr_queue.s:182` | NOPKG_SYSERROR - fatal error: no packages loaded (dsNoPk = 27) Called when a required package (e.g., Standard File) is not available. Triggers a system error with ID 27 (dsNoPk). |
| **`NQCBuf`** | `0x007B9A` | `0x0096EE` | `file_mgr_cache.s:769`<br>`file_mgr_cache.s:640` | NQCBuf - NQCBuf: enqueue cache buffer after A0 in circular list Called during boot. |
| **`NWHANDLE`** | — | `0x00A666` | `memory_mgr.s:392` | — |
| **`Offline`** | `0x00343A` | `0x004EC0` | `file_mgr_vol.s:1070` | _OffLine ($A035) _OffLine ($A035): take volume offline (don't eject media) |
| **`OFFLINE`** | `0x00343A` | `0x004EC0` | `file_mgr_vol.s:1014` | _OffLine: take volume offline without ejecting disk |
| **`OFFLINE_CONT`** | `0x003442` | `0x004EC8` | `file_mgr_vol.s:1079`<br>`file_mgr_vol.s:1022` | OFFLINE_CONT close B-tree files on the VCB (unmount path) |
| **`OFFLINE_CONT_2`** | `0x00344E` | `0x004ED4` | `file_mgr_vol.s:1091`<br>`file_mgr_vol.s:1028` | OFFLINE_CONT_2 Called during boot. FlushVol/UnmountVol: flush or close all files on volume |
| **`OFFLINE_CONT_3`** | `0x00348C` | `0x004F12` | `file_mgr_vol.s:1113`<br>`file_mgr_vol.s:1048` | flush/close catalog B-tree |
| **`OFFLINE_ERR`** | `0x0034D6` | `0x004F5C` | `file_mgr_vol.s:1140`<br>`file_mgr_vol.s:1073` | — |
| **`OFFLINE_OK`** | `0x0034D4` | `0x004F5A` | `file_mgr_vol.s:1138`<br>`file_mgr_vol.s:1071` | if unmounting, trash all cached blocks |
| **`OFFLINE_SKIP`** | `0x003470` | `0x004EF6` | `file_mgr_vol.s:1103`<br>`file_mgr_vol.s:1039` | flush TFS volume: set consistency bit, flush MDB and B-trees |
| **`OFFLINE_SKIP_2`** | `0x0034A0` | `0x004F26` | `file_mgr_vol.s:1122`<br>`file_mgr_vol.s:1056` | flush/close extent B-tree flush all volume caches |
| **`Open`** | `0x0021F4` | `0x002F82` | `device_mgr.s:382` | _Open ($A000) A0 = paramBlock (IOParam) -> D0 = error Opens a driver by name: searches unit table, then tries 'DRVR' resource. refNum = -(unitNum+1), returned in ioRefNum of the paramBlock. Called dur... |
| **`OPEN`** | `0x0021F4` | `0x002F82` | `device_mgr.s:335` | **Regs:** `Entry: A0 = IOParam, D1 = trap word Exit: D0 = result, IOParam.ioRefNum (+0x18) = driver refNum`<br>OPEN - _Open trap: open a device driver by name or refNum Entry: A0 = IOParam, D1 = trap word IOParam.ioNamePtr (+0x12) = driver name (Pascal string) IOParam.ioPermssn (+0x1B) = permission Exit: D0 = ... |
| **`OPEN_AFTER_INSTALL`** | — | `0x00304E` | `device_mgr.s:426` | — |
| **`OPEN_CALL_DRIVER`** | `0x00233E` | `0x0030D4` | `device_mgr.s:527`<br>`device_mgr.s:480` | Check read/write permission compatibility |
| **`OPEN_CHECK_DRVR_PTR`** | `0x00223C` | `0x002FCC` | `device_mgr.s:412`<br>`device_mgr.s:365` | — |
| **`OPEN_CHK_INSTALL`** | `0x0022BE` | — | `device_mgr.s:477` | — |
| **`OPEN_CHK_LOCK`** | — | `0x0030EC` | `device_mgr.s:491` | OPEN_CHK_LOCK - check if driver needs unlocking after close/open |
| **`OPEN_CHK_NEEDLOCK`** | `0x002354` | — | `device_mgr.s:543` | Call the driver's open routine (offset 8 in DRVR header) Open failed -- clean up OPEN_CHK_NEEDLOCK - open succeeded; check if driver needs GoodBye kiss Called during boot. |
| **`OPEN_CHK_PERM`** | `0x002314` | `0x0030A8` | `device_mgr.s:512`<br>`device_mgr.s:465` | Check open permission compatibility |
| **`OPEN_CLOSE_EXIT`** | — | `0x003114` | `device_mgr.s:510` | OPEN_CLOSE_EXIT - Open/Close common exit: restore regs, set ioResult Called by: OPEN_UNLOCK_RAM, OPEN_SCAN_NEXT, OPEN_GOT_RESOURCE, OPEN_AFTER_INSTALL, OPEN_CHK_PERM (and 3 more) |
| **`OPEN_COPY_DRVR_HDR`** | `0x0022E6` | `0x00307C` | `device_mgr.s:494`<br>`device_mgr.s:446` | DCE exists (or just created); initialize it from DRVR header fields |
| **`OPEN_DCE_FAIL`** | — | `0x0030EA` | `device_mgr.s:488` | — |
| **`OPEN_EXIT`** | `0x002376` | — | `device_mgr.s:555` | Unlock RAM-based driver if it was locked during open |
| **`OPEN_GOT_RESOURCE`** | `0x002288` | `0x003018` | `device_mgr.s:447`<br>`device_mgr.s:401` | Driver not found in unit table -- try loading as 'DRVR' resource by name OPEN_GOT_RESOURCE - DRVR resource found, get its resource ID to derive unit number Called during boot. |
| **`OPEN_INIT_DCE`** | `0x0022C2` | `0x003052` | `device_mgr.s:479`<br>`device_mgr.s:429` | OPEN_INIT_DCE - DCE slot allocated, set up driver header fields |
| **`OPEN_LOCK_DCE`** | `0x002310` | `0x0030A4` | `device_mgr.s:510`<br>`device_mgr.s:461` | Lock driver in memory if dNeedLock set and RAM-based |
| **`OPEN_LOCK_DRIVER`** | `0x0022F8` | `0x00308E` | `device_mgr.s:501`<br>`device_mgr.s:453` | Copy DRVR header fields into DCE |
| **`OPEN_LOCK_DRVR`** | — | `0x002F12` | `device_mgr.s:270` | RAM-based driver: lock handle and load if purged |
| **`OPEN_LOOKUP_RTS`** | — | `0x002F58` | `device_mgr.s:312` | — |
| **`OPEN_RET_NOERR`** | `0x002382` | `0x003120` | `device_mgr.s:567`<br>`device_mgr.s:516` | OPEN_RET_NOERR - return noErr (driver already open, no action needed) |
| **`OPEN_SCAN_NEXT`** | `0x002254` | `0x002FE4` | `device_mgr.s:423`<br>`device_mgr.s:377` | Called by: OPEN_SCAN_UNIT_TBL, OPEN_CHECK_DRVR_PTR |
| **`OPEN_SCAN_UNIT_TBL`** | `0x002220` | `0x002FB0` | `device_mgr.s:399`<br>`device_mgr.s:352` | Search unit table for an installed driver matching the requested name |
| **`OPEN_SEARCH_BY_NAME`** | `0x002216` | `0x002FA6` | `device_mgr.s:394`<br>`device_mgr.s:348` | Search unit table for a driver matching the given name |
| **`OPEN_STD_INSTALL`** | `0x0022BC` | `0x00304C` | `device_mgr.s:475`<br>`device_mgr.s:424` | No DCE at this unit number -- install a new one OPEN_STD_INSTALL - standard driver install (no reserved memory needed) |
| **`OPEN_STORE_RESULT`** | `0x00237C` | `0x00311A` | `device_mgr.s:559`<br>`device_mgr.s:513` | Common exit: restore regs, store result, return |
| **`OPEN_UNLOCK_RAM`** | `0x00235C` | `0x0030F4` | `device_mgr.s:546`<br>`device_mgr.s:495` | OPEN_UNLOCK_RAM - unlock RAM driver and DCE handles |
| **`OpenRF`** | `0x00401A` | `0x005AB4` | `file_mgr_dir.s:44` | File Manager -- calls by file name (directory level) Apple sources, included by TFS.a (MacSEROM.lst module TURBOFS): TFSDir1.a ... TFSDir3.a and MFSDir1.a ... MFSDir3.a: OpenRF/FileOpen (open a fork: ... |
| **`OPENRF`** | `0x00401A` | `0x005AB4` | `file_mgr_dir.s:37` | File Manager -- calls by file name (directory level) Apple sources, included by TFS.a (MacSEROM.lst module TURBOFS): TFSDir1.a ... TFSDir3.a and MFSDir1.a ... MFSDir3.a: OpenRF/FileOpen (open a fork: ... |
| **`OPENWD`** | — | `0x0055FE` | `file_mgr_vol.s:1864` | _OpenWD: open a working directory |
| **`OPENWD_DONE`** | — | `0x005636` | `file_mgr_vol.s:1887` | — |
| **`OpenWD_hfs`** | `0x003B72` | — | `file_mgr_vol.s:2042` | Open WD_hfs Called during boot. _OpenWD (HFS): open a working directory |
| **`OPENWD_HFS_CONT`** | `0x003BAE` | `0x00563A` | `file_mgr_vol.s:2074`<br>`file_mgr_vol.s:1894` | OPENWD_HFS_CONT: set default volume and directory Called during boot. |
| **`OPENWD_HFS_CONT_2`** | `0x003BB4` | `0x005640` | `file_mgr_vol.s:2078`<br>`file_mgr_vol.s:1899` | OPENWD_HFS_CONT_2: fill in a WDCB entry at offset D1 |
| **`OPENWD_HFS_CONT_3`** | `0x003BD2` | `0x00565E` | `file_mgr_vol.s:2093`<br>`file_mgr_vol.s:1910` | OPENWD_HFS_CONT_3 OPENWD_HFS_CONT_3: allocate or find existing WDCB for DirID D6 on volume A2 |
| **`OPENWD_HFS_CONT_4`** | `0x003C0C` | `0x005698` | `file_mgr_vol.s:2120`<br>`file_mgr_vol.s:1937` | found existing WDCB: return its WD refnum no existing match: allocate the free slot |
| **`OPENWD_HFS_CONT_5`** | `0x003C12` | `0x00569E` | `file_mgr_vol.s:2124`<br>`file_mgr_vol.s:1941` | — |
| **`OPENWD_HFS_ERR`** | `0x003BAA` | — | `file_mgr_vol.s:2066` | — |
| **`OPENWD_HFS_FOUND`** | `0x003B88` | `0x005614` | `file_mgr_vol.s:2052`<br>`file_mgr_vol.s:1874` | check that it's a directory |
| **`OPENWD_HFS_FOUND_2`** | `0x003BF4` | `0x005680` | `file_mgr_vol.s:2109`<br>`file_mgr_vol.s:1927` | check if this WDCB matches our volume/DirID/procID |
| **`OPENWD_HFS_NO`** | `0x003BA2` | `0x00562E` | `file_mgr_vol.s:2063`<br>`file_mgr_vol.s:1884` | root directory: just return VRefNum |
| **`OPENWD_HFS_NO_2`** | `0x003C1A` | `0x0056A6` | `file_mgr_vol.s:2128`<br>`file_mgr_vol.s:1945` | — |
| **`OPENWD_HFS_OK`** | `0x003BE0` | — | `file_mgr_vol.s:2099` | scan WDCBs for existing match or free slot |
| **`OPENWD_SCAN_LOOP`** | — | `0x00566C` | `file_mgr_vol.s:1917` | scan WDCB array for existing match or free slot Called by: OPENWD_HFS_FOUND_2, OPENWD_SCAN_LOOP |
| **`OSEventAvail`** | `0x002764` | `0x003F5E` | `event_mgr.s:106` | _OSEventAvail ($A030) D0 = event mask (bit per event type), A0 = event record buffer -> D0 = 0 if event found (copied to buffer), D0 = -1 if no matching event. Peeks at the event queue without dequeui... |
| **`OSEVENTAVAIL`** | `0x002764` | `0x003F5E` | `event_mgr.s:104` | _OSEventAvail ($A030) -- check for an event matching D0 mask Walks the EventQueue looking for an event whose evtNum bit is set in the caller's mask in D0. If found, copies it to A0 and returns D0=0 (Z... |
| **`OSEVTAVAIL_CHK_AUTOKEY`** | `0x002782` | `0x003F7C` | `event_mgr.s:120`<br>`event_mgr.s:118` | Walk the event queue looking for an event matching the caller's mask |
| **`OSEVTAVAIL_COPY_LOOP`** | `0x0027D0` | `0x003FCA` | `event_mgr.s:150`<br>`event_mgr.s:145` | Found (or generated) a matching event; copy 16-byte event record to buffer |
| **`OSEVTAVAIL_FOUND`** | `0x0027C6` | `0x003FC0` | `event_mgr.s:144`<br>`event_mgr.s:140` | No matching event found; check if auto-key repeat should fire Generate auto-key repeat event |
| **`OSEVTAVAIL_NO_EVENT`** | `0x0027DC` | `0x003FD6` | `event_mgr.s:162`<br>`event_mgr.s:156` | OSEVTAVAIL_NO_EVENT - no matching event: fill buffer with null event, return -1 Called during boot (32,476 times in 30s trace). |
| **`OSEVTAVAIL_WALK`** | `0x002774` | `0x003F6E` | `event_mgr.s:112`<br>`event_mgr.s:110` | — |
| **`P_AdjEof`** | `0x005530` | `0x006FE2` | `file_mgr_io.s:903`<br>`file_mgr_io.s:776` | P_Adj Eof Called during boot. |
| **`P_BFindS`** | — | `0x00AC58` | `memory_mgr.s:1245` | — |
| **`P_BMChk`** | — | `0x004DB2` | `file_mgr_vol.s:889` | BMChk: wrapper for BlkChk that checks write-protect first Called by: MOUNTVOL_FOUND_3, MOUNTVOL_NO_12, MOUNTVOL_CONT_11 |
| **`P_CKExtFS`** | — | `0x0050BE` | `file_mgr_vol.s:1243` | CkExtFS: check if volume uses an external file system Called by: EJECT_OFFLINE_JOIN, FLUSHVOL_UNMOUNTVOL_SHARED, GETVOLINFO_CONT_8, GETWDINFO, CkExtFS_AndOnline (and 1 more) |
| **`P_CMSetUp`** | `0x0065A0` | `0x008068` | `file_mgr_catalog.s:631`<br>`file_mgr_catalog.s:573` | P_CMSetUp -- common set up routine. P_CM Set Up Called by: CMCreateCN, CMDeleteCN, CMGetCN, CMGetOff, CMMoveCN (and 2 more) |
| **`P_DTRMV1`** | `0x003650` | `0x0050E2` | `file_mgr_vol.s:1360`<br>`file_mgr_vol.s:1265` | P_DTRMV1 -- dTRMV1: determine volume. Called by: SetVolInfo_hfs, GETWDINFO_HFS_CONT, hfsD, hfsE, GETFILEINFO_CONT_2 (and 1 more) |
| **`P_DTRMV3`** | — | `0x0050CE` | `file_mgr_vol.s:1254` | DTRMV3: determine volume from param block (by name, refnum, or default) Called by: TFMOVE, EJECT_OFFLINE_JOIN, FLUSHVOL_UNMOUNTVOL_SHARED, GETVOLINFO, SETVOL (and 5 more) |
| **`P_FndFilName`** | `0x004990` | `0x006436` | `file_mgr_dir.s:1329`<br>`file_mgr_dir.s:1190` | P_Fnd Fil Name Called during boot. |
| **`P_hfs0`** | — | `0x0042D8` | `file_mgr_queue.s:74` | P_hfs0 -- HFS selector 0: GetVolName (placeholder) Stores ASCII "A2.1" into the version slot at 0x20(A0) of the param block and returns success. The "A2.1" version stamp is the SE FDHD HFS version ide... |
| **`P_hfsC`** | — | `0x005284` | `file_mgr_vol.s:1489` | HFS selector C: set PMSP callback and HFS flags |
| **`P_hfsD`** | — | `0x0057FA` | `file_mgr_vol.s:2102` | HFS selector D: OpenWD (by dirID, full HFS stack) |
| **`P_hfsE`** | — | `0x005824` | `file_mgr_vol.s:2119` | HFS selector E: SetVol (by dirID, full HFS stack) |
| **`P_hfsF`** | — | `0x005792` | `file_mgr_vol.s:2056` | HFS selector F: GetWDInfo (full HFS stack frame) |
| **`P_hfsUn_LockRange`** | — | `0x006F22` | `file_mgr_io.s:691` | — |
| **`P_KybdTask`** | — | `0x003586` | `adb_mgr.s:299` | P_KybdTask - keyboard VBL task (stub, actual processing via ADB) |
| **`P_mAllocNode`** | `0x006E38` | — | `file_mgr_btree.s:984` | P_mAllocNode -- allocate the node. P_m Alloc Node |
| **`P_mBlkAlloc`** | `0x0057D6` | — | `file_mgr_alloc.s:17` | File Manager -- allocation: volume bitmap and file extents Apple sources: VSM.a, the Volume Space Manager (MacSEROM.lst module VSM: BlkAlloc, BlkDealloc, BlkChk, UpdateFree, ReadBM -- allocation block... |
| **`P_mBlkDealloc`** | `0x005932` | — | `file_mgr_alloc.s:185` | P_mBlkDealloc -- deallocate the space. P_m Blk Dealloc |
| **`P_mBTClose`** | `0x0066DC` | — | `file_mgr_btree.s:32` | File Manager - B-tree Engine Generic B-tree implementation used by HFS for both the catalog file and the extents overflow file. Supports search, insert, delete, and node splitting/rotation for balance... |
| **`P_mBTDelete`** | `0x00671C` | — | `file_mgr_btree.s:70` | P_mBTDelete -- delete the record. P_m BT Delete Called by: DC_DELETE, DEALLOCFILE_NO_2, TRUNCATEFILE_OK, CC_CLR_THD_LOOP, MC_UPD_DEST (and 1 more) |
| **`P_mBTFlush`** | `0x0068C2` | — | `file_mgr_btree.s:258` | P_mBTFlush -- flush B-tree header (BTH) to disk node 0. P_m BT Flush |
| **`P_mBTGetRecord`** | `0x006928` | — | `file_mgr_btree.s:314` | P_mBTGetRecord -- get next catalog record. P_m BT Get Record |
| **`P_mBTInsert`** | `0x0069EA` | — | `file_mgr_btree.s:449` | P_mBTInsert -- insert the record. P_m BT Insert Called by: EXTENDFILE_LOOP, CC_ADD_REC, CC_CLR_THD_LOOP, MC_INSERT_DST, CMRenameCN |
| **`P_mBTOpen`** | `0x006C8A` | — | `file_mgr_btree.s:742` | P_mBTOpen -- bTOpen: open the B*-Tree file. P_m BT Open |
| **`P_mBTSearch`** | `0x006D4A` | — | `file_mgr_btree.s:840` | P_mBTSearch -- find the record. P_m BT Search Called by: MOUNTVOL_OK_9, DEALLOCFILE_NEXT, TRUNCATEFILE_NEXT, XFSearch, XFSEARCH_NO_2 (and 1 more) |
| **`P_mBTUpdate`** | `0x006DD6` | — | `file_mgr_btree.s:916` | P_mBTUpdate -- update the BTree record. P_m BT Update Called by: MC_UPD_DEST, XFSEARCH_LOOP_3, CC_UPD_PAR, DC_UPD_PAR, MC_UPD_SRC (and 3 more) |
| **`P_mCacheRDIP`** | `0x007B2A` | — | `file_mgr_cache.s:694` | P_m Cache RDIP Called during boot. |
| **`P_mCacheWRIP`** | `0x007B56` | — | `file_mgr_cache.s:724` | P_mCacheWRIP -- cacheWrIP: write blocks from user buffer. P_m Cache WRIP |
| **`P_mDeallocFile`** | `0x005AA8` | — | `file_mgr_alloc.s:412` | P_mDeallocFile -- deallocate all file extents. P_m Dealloc File |
| **`P_mExtBTFile`** | `0x006ECE` | — | `file_mgr_btree.s:1067` | P_mExtBTFile -- extend the file. P_m Ext BT File |
| **`P_mExtendFile`** | `0x005B7C` | — | `file_mgr_alloc.s:515` | P_mExtendFile -- extend the file. P_m Extend File |
| **`P_mFileOpen`** | `0x004024` | — | `file_mgr_dir.s:54` | P_m File Open Called during boot. |
| **`P_mFlushCache`** | `0x0076C6` | — | `file_mgr_cache.s:56` | P_m Flush Cache Called during boot. |
| **`P_mFreeNode`** | `0x006FB4` | — | `file_mgr_btree.s:1178` | P_mFreeNode -- the disk node. P_m Free Node |
| **`P_mGetBlock`** | `0x0077B0` | — | `file_mgr_cache.s:188` | P_m Get Block Called during boot. |
| **`P_mGetNode`** | `0x007402` | — | `file_mgr_btree.s:1810` | P_mGetNode -- get the node. P_m Get Node Called by: BTDEL_GETPAR, BTFlush, GR_GETNODE, BTINS_NXTLEV, BTSearch (and 4 more) |
| **`P_mLg2Phys`** | `0x0055E0` | — | `file_mgr_io.s:1021` | P_m Lg2Phys Called during boot. |
| **`P_mMarkBlock`** | `0x0079F4` | — | `file_mgr_cache.s:492` | P_m Mark Block Called during boot. |
| **`P_mRdBlocks`** | `0x007C8C` | — | `file_mgr_cache.s:922` | P_m Rd Blocks Called during boot. |
| **`P_mRelBlock`** | `0x007A0A` | — | `file_mgr_cache.s:521` | P_m Rel Block Called during boot. |
| **`P_mRelNode`** | `0x0075D0` | — | `file_mgr_btree.s:2110` | P_mRelNode -- release the node. P_m Rel Node Called by: BTINS_CLEANUP, BTDEL_CHKRECS, BTDEL_GETRSIB, BTDEL_FREENODE, BTDEL_RELCHILD (and 12 more) |
| **`P_mTrashBlocks`** | `0x007A94` | — | `file_mgr_cache.s:617` | P_mTrashBlocks -- trash cached blocks in the written range (now stale). P_m Trash Blocks |
| **`P_mTrashVBlks`** | `0x007A5C` | — | `file_mgr_cache.s:570` | P_mTrashVBlks -- trash bitmap blocks for this volume. P_m Trash V Blks |
| **`P_mTruncateFile`** | `0x005D98` | — | `file_mgr_alloc.s:778` | P_mTruncateFile -- truncateFile: truncate to rounded length. P_m Truncate File |
| **`P_mWrBlocks`** | `0x007CDA` | — | `file_mgr_cache.s:959` | P_mWrBlocks -- write data directly to disk (bypasses cache). P_m Wr Blocks |
| **`P_PermssnChk`** | `0x00416C` | `0x005C06` | `file_mgr_dir.s:216`<br>`file_mgr_dir.s:198` | P_Permssn Chk Called during boot. |
| **`P_ReadBM`** | — | `0x0074AA` | `file_mgr_alloc.s:258` | Called by: BLKALLOC_LOOP, BLKALLOC_CONT, BLKALLOC_CONT_4, VBLKDEALLOC, BLKCHK_NEXT (and 1 more) |
| **`P_RFNCall`** | `0x005352` | `0x006E04` | `file_mgr_io.s:627`<br>`file_mgr_io.s:561` | P_RFN Call Called during boot. |
| **`P_SCSI_scAdd`** | — | `0x01A350` | `scsi_mgr.s:287` | scAdd - *(long*)scParam1 += scParam2 |
| **`P_SCSI_scComp`** | — | `0x01A36A` | `scsi_mgr.s:307` | scComp - set compare-mode flag and fall into scInc |
| **`P_SCSI_scInc`** | — | `0x01A33C` | `scsi_mgr.s:276` | scInc - transfer D2 bytes, advance scParam1 pointer by D2 |
| **`P_SCSI_scLoop`** | — | `0x01A35A` | `scsi_mgr.s:296` | scLoop - decrement scParam2; if >0, jump back by scParam1 offset |
| **`P_SCSI_scMove`** | — | `0x01A354` | `scsi_mgr.s:291` | scMove - *(long*)scParam2 = *(long*)scParam1 |
| **`P_SCSI_scNoInc`** | — | `0x01A348` | `scsi_mgr.s:282` | scNoInc - transfer D2 bytes without advancing scParam1 |
| **`P_SCSI_scNOp`** | — | `0x01A370` | `scsi_mgr.s:312` | scNOp - advance A1 past current 10-byte TIB entry Called by: SCSI_TIB_LOOP, P_SCSI_scInc, P_SCSI_scNoInc, P_SCSI_scAdd, P_SCSI_scMove |
| **`P_SCSI_scStop`** | — | `0x01A366` | `scsi_mgr.s:303` | scStop - terminate TIB execution, return noErr |
| **`P_SCSICmd`** | — | `0x01A2D8` | `scsi_mgr.s:225` | Selector 3: CMP_COPY_FROM_DISK - send a SCSI command descriptor block Params: 0xA(A6) = ptr to CDB, 0x8(A6) = CDB length; result: 0xE(A6) |
| **`P_SCSIComplete`** | — | `0x01A388` | `scsi_mgr.s:326` | Selector 4: SCSIComplete - finish a transaction (status + msg-in) Params: 0x8(A6) timeout, 0xC(A6) ptr to message word, 0x10(A6) ptr to status word; result: 0x14(A6). |
| **`P_SCSIGet`** | — | `0x01A27C` | `scsi_mgr.s:183` | Selector 1: SCSIGet - arbitrate for the SCSI bus Wait while another driver owns the bus (busy flag), then mark ourselves busy and run the NCR 5380 arbitration sequence. |
| **`P_SCSIInstall`** | — | `0x01A256` | `scsi_mgr.s:161` | Selector 7: SCSIInstall - on SE FDHD this is a no-op stub (interrupt-driven SCSI handler is wired into VIA2; nothing to do). |
| **`P_SCSIMsgIn`** | — | `0x01A3DE` | `scsi_mgr.s:364` | Selector 12: SCSIMsgIn - read one message-in byte from target Param: 0x8(A6) = ptr to caller's message word; result: 0xC(A6). |
| **`P_SCSIMsgOut`** | — | `0x01A3F2` | `scsi_mgr.s:376` | Selector 13: SCSIMsgOut - send one message-out byte to target Param: 0x8(A6) = message byte; result: 0xA(A6). |
| **`P_SCSIRead`** | — | `0x01A2F6` | `scsi_mgr.s:242` | Selectors 5 (SCSIRead), 6 (SCSIWrite), 8 (SCSIRBlind), 9 (SCSIWBlind) Run the TIB (transfer-instruction-block) interpreter. D4: 0xFF (write), 0x00 (read); bit 15 = blind/pseudo-DMA mode. Param: 0x8(A6... |
| **`P_SCSIReset`** | — | `0x01A266` | `scsi_mgr.s:171` | Selector 0: SCSIReset - assert SCSI bus reset, clear busy flag |
| **`P_SCSISelect_SelAtn`** | — | `0x01A2B0` | `scsi_mgr.s:207` | Selectors 2 (SCSISelect) and 11 (SCSISelAtn) - select target For SelAtn, set bit 31 of D0 to flag attention-assert mode to SCSI_DO_SELECT. Param: 0x8(A6) target SCSI ID; result: 0xA(A6). |
| **`P_SCSIStat`** | — | `0x01A258` | `scsi_mgr.s:165` | Selector 10: SCSIStat - return NCR 5380 sBSR/sCSR as result word |
| **`P_SCSIunimplemented`** | — | `0x01A250` | `scsi_mgr.s:153` | P_SCSIunimplemented - called from 1 place Selectors 14..23: any caller using a reserved selector lands here. |
| **`P_SCSIWrite`** | — | `0x01A2F4` | `scsi_mgr.s:240` | Selectors 5 (SCSIRead), 6 (SCSIWrite), 8 (SCSIRBlind), 9 (SCSIWBlind) Run the TIB (transfer-instruction-block) interpreter. D4: 0xFF (write), 0x00 (read); bit 15 = blind/pseudo-DMA mode. Param: 0x8(A6... |
| **`P_SetUpTags`** | `0x007CEC` | `0x009842` | `file_mgr_cache.s:980`<br>`file_mgr_cache.s:797` | P_Set Up Tags Called during boot. |
| **`P_tControl`** | — | `0x0031E0` | `device_mgr.s:602` | P_tControl - _Control trap handler |
| **`P_tStatus`** | — | `0x0031EE` | `device_mgr.s:612` | P_tStatus - _Status trap handler Special case: csCode = 1 returns DCE handle in csParam. |
| **`P_TstMod`** | — | `0x006E4E` | `file_mgr_io.s:600` | — |
| **`P_VIAint5_Timer2`** | — | `0x01AA4A` | `time_mgr.s:178` | P_VIAint5_Timer2 - VIA Timer 2 interrupt handler Called when T2 counts down to 0. Subtracts last-programmed ms from every primed task's tmCount, queues expired-task callbacks onto the supervisor stack... |
| **`P_XFSearch`** | — | `0x0079CE` | `file_mgr_alloc.s:824` | — |
| **`PACKMGREND`** | — | `0x01A0C2` | `date_utils.s:22` | Date conversion -- _Secs2Date / _Date2Secs Apple source: SexyDate.a (MacSEROM.lst module SEXYDATE). Convert between the clock's seconds since midnight, January 1, 1904 and a DateTimeRec (year, month, ... |
| **`PermssnChk`** | `0x004172` | — | `file_mgr_dir.s:226` | Permssn Chk Called during boot. PermssnChk: check file access permissions |
| **`PERMSSNCHK_CONT`** | `0x0041A4` | `0x005C3E` | `file_mgr_dir.s:251`<br>`file_mgr_dir.s:227` | FCBScan: check for permission conflicts with other open FCBs |
| **`PERMSSNCHK_CONT_2`** | `0x0041A8` | `0x005C42` | `file_mgr_dir.s:253`<br>`file_mgr_dir.s:229` | FCBScan: check for permission conflicts with other open FCBs |
| **`PERMSSNCHK_EXIT`** | `0x0041A2` | `0x005C3C` | `file_mgr_dir.s:248`<br>`file_mgr_dir.s:224` | — |
| **`PERMSSNCHK_EXIT_2`** | `0x0041D4` | `0x005C6E` | `file_mgr_dir.s:274`<br>`file_mgr_dir.s:250` | — |
| **`PERMSSNCHK_FOUND`** | `0x0041D2` | — | `file_mgr_dir.s:272` | no conflicts |
| **`PERMSSNCHK_NO`** | `0x00419A` | `0x005C34` | `file_mgr_dir.s:242`<br>`file_mgr_dir.s:218` | — |
| **`PERMSSNCHK_NO_2`** | `0x0041C4` | `0x005C5E` | `file_mgr_dir.s:263`<br>`file_mgr_dir.s:239` | — |
| **`PERMSSNCHK_NO_3`** | `0x0041CA` | `0x005C64` | `file_mgr_dir.s:267`<br>`file_mgr_dir.s:243` | conflict found: file already open |
| **`PERMSSNCHK_NO_CONFLICT`** | — | `0x005C6C` | `file_mgr_dir.s:248` | no conflicts found |
| **`PERMSSNCHK_OK`** | `0x00418E` | `0x005C28` | `file_mgr_dir.s:238`<br>`file_mgr_dir.s:214` | file already open with write permission first open with write permission |
| **`PERMSSNCHK_OK_2`** | `0x00419C` | `0x005C36` | `file_mgr_dir.s:245`<br>`file_mgr_dir.s:221` | read-only or downgraded access |
| **`PostEvent`** | `0x0026EC` | `0x003EE6` | `event_mgr.s:30` | Operating System Event Manager -- _PostEvent, _OSEventAvail, _GetOSEvent, _FlushEvents Apple source: OSEventMgr.a (MacSEROM.lst module EVENTS). The event queue (EventQueue) is kept in a fixed circular... |
| **`POSTEVENT`** | `0x0026EC` | `0x003EE6` | `event_mgr.s:28` | **Regs:** `Entry: A0 = event code (mouseDown=1, mouseUp=2, keyDown=3, etc.)`<br>Operating System Event Manager -- _PostEvent, _OSEventAvail, _GetOSEvent, _FlushEvents Apple source: OSEventMgr.a (MacSEROM.lst module EVENTS). The event queue (EventQueue) is kept in a fixed circular... |
| **`POSTEVENT_ENABLED`** | `0x0026FA` | `0x003EF4` | `event_mgr.s:48`<br>`event_mgr.s:45` | POSTEVENT_ENABLED - event is enabled, find a free event record and enqueue it Event records are in a circular buffer (SysEvtBuf). Each record is 22 bytes: 6-byte queue header + 16-byte event data (evt... |
| **`POSTEVENT_FILL`** | `0x00272C` | `0x003F26` | `event_mgr.s:69`<br>`event_mgr.s:68` | No free slot: steal oldest event from queue head |
| **`POSTEVENT_SCAN_LOOP`** | `0x002714` | `0x003F0E` | `event_mgr.s:59`<br>`event_mgr.s:57` | Scan for free event record (evtNum == -1) |
| **`PRIME_NO_ACTIVE`** | `0x017634` | `0x01A9C8` | `time_mgr.s:93`<br>`time_mgr.s:106` | PRIME_NO_ACTIVE -- no task was active; scan queue and start T2 |
| **`PRIME_PEEL`** | — | `0x01A9CA` | `time_mgr.s:108` | — |
| **`PRIME_RESTORE_SR`** | `0x017636` | `0x01A9CC` | `time_mgr.s:95`<br>`time_mgr.s:110` | — |
| **`PrimeTime`** | `0x0175FA` | `0x01A984` | `time_mgr.s:68` | PrimeTime -- trap handler for _PrimeTime ($A05A). _PrimeTime ($A05A) |
| **`PRIMETIME`** | `0x0175FA` | `0x01A984` | `time_mgr.s:82` | _PrimeTime ($A05A) - set tmCount on a TMTask and start T2 Inputs: A0 -> TMTask, D0.L = delay in milliseconds. |
| **`PROGRAM_T2`** | `0x01767A` | `0x01AA10` | `time_mgr.s:136`<br>`time_mgr.s:150` | PROGRAM_T2 -- Program VIA Timer 2 for soonest task D1 = pointer to soonest TMTask (or nil if none). Clamps delay to 84 ms max (T2 is 16-bit: 84*780 < 65536). Writes T2CL/T2CH and enables T2 interrupt ... |
| **`PtrZone`** | `0x01011C` | `0x00A634` | `memory_mgr.s:586` | **Proto:** `Pascal: FUNCTION PtrZone(p: Ptr): THz;`<br>**Regs:** `Entry: A0 = p Exit:  A0 = zone found by MMPPrologue, D0.W = noErr (or memWZErr/memAZErr)`<br>_PtrZone ($A148): return the heap zone containing a nonrelocatable block Pascal: FUNCTION PtrZone(p: Ptr): THz; Entry: A0 = p Exit:  A0 = zone found by MMPPrologue, D0.W = noErr (or memWZErr/memAZErr) |
| **`PTRZONE`** | `0x01011C` | `0x00A634` | `memory_mgr.s:361` | — |
| **`PTRZONE_CONT`** | `0x010124` | `0x00A63C` | `memory_mgr.s:598`<br>`memory_mgr.s:371` | **Regs:** `Entry: D1 = trap word (bit 9 = CLEAR), A0 = block data, D0.L = logical size`<br>PTRZONE_CONT - clear a newly allocated block if the trap's CLEAR bit is set Entry: D1 = trap word (bit 9 = CLEAR), A0 = block data, D0.L = logical size Clears (D0 + 1) / 2 words; A0 is preserved. Call... |
| **`PTRZONE_CONT_2`** | `0x010130` | `0x00A648` | `memory_mgr.s:604`<br>`memory_mgr.s:377` | — |
| **`PTRZONE_NO`** | `0x010138` | — | `memory_mgr.s:609` | — |
| **`PurgeHeap`** | `0x010570` | `0x00AB26` | `memory_mgr.s:1561` | **Regs:** `Entry: D0.L = physical size needed, A6 = zone Exit:  A0 = free block of at least D0 bytes or nil, D1 = largest free`<br>PurgeHeap - purge blocks until D0 contiguous bytes can be made free Entry: D0.L = physical size needed, A6 = zone Exit:  A0 = free block of at least D0 bytes or nil, D1 = largest free block (both from... |
| **`PURGEHEAP`** | `0x010570` | `0x00AB26` | `memory_mgr.s:1075` | — |
| **`PURGEHEAP_CONT`** | `0x010574` | `0x00AB2A` | `memory_mgr.s:1563`<br>`memory_mgr.s:1077` | — |
| **`PURGEHEAP_CONT_2`** | `0x0105AC` | `0x00AB62` | `memory_mgr.s:1586`<br>`memory_mgr.s:1100` | — |
| **`PURGEHEAP_DONE`** | `0x0105FA` | `0x00ABB0` | `memory_mgr.s:1636`<br>`memory_mgr.s:1148` | — |
| **`PURGEHEAP_NO`** | `0x010586` | `0x00AB3C` | `memory_mgr.s:1570`<br>`memory_mgr.s:1084` | — |
| **`PURGEHEAP_NO_2`** | `0x0105B8` | `0x00AB6E` | `memory_mgr.s:1601`<br>`memory_mgr.s:1114` | — |
| **`PURGEHEAP_OK`** | `0x0105B4` | `0x00AB6A` | `memory_mgr.s:1597`<br>`memory_mgr.s:1110` | PURGEHEAP_OK Called during boot. |
| **`PURGEHEAP_OK_2`** | `0x0105CC` | `0x00AB82` | `memory_mgr.s:1615`<br>`memory_mgr.s:1127` | PURGEHEAP_OK_2 Called during boot. |
| **`PURGEHEAP_OK_3`** | `0x0105CE` | `0x00AB84` | `memory_mgr.s:1617`<br>`memory_mgr.s:1129` | — |
| **`PURGEHEAP_SKIP`** | `0x0105B6` | `0x00AB6C` | `memory_mgr.s:1599`<br>`memory_mgr.s:1112` | PURGEHEAP_OK Called during boot. |
| **`PURGEHEAP_SKIP_2`** | `0x0105F0` | `0x00ABA6` | `memory_mgr.s:1631`<br>`memory_mgr.s:1143` | — |
| **`PurgeMem`** | `0x00FFEE` | `0x00A4FE` | `memory_mgr.s:317` | _PurgeMem ($A04D) D0.L = needed -> (purges until space available) Called during boot. |
| **`PURGEMEM`** | `0x00FFEE` | `0x00A4FE` | `memory_mgr.s:222` | — |
| **`PURGEMEM_CONT`** | `0x00FFFA` | `0x00A50A` | `memory_mgr.s:321`<br>`memory_mgr.s:226` | — |
| **`PURGEMEM_ERR`** | `0x010006` | `0x00A516` | `memory_mgr.s:336`<br>`memory_mgr.s:236` | Called by: MAXBLOCK_DO_COMPACT, PURGEMEM_CONT, PURGESPACE, FREEMEM |
| **`PURGEMEM_EXIT`** | `0x010002` | `0x00A512` | `memory_mgr.s:332`<br>`memory_mgr.s:231` | PURGEMEM_EXIT Called during boot. |
| **`PURGEMEM_EXIT_2`** | `0x010004` | `0x00A514` | `memory_mgr.s:334`<br>`memory_mgr.s:233` | — |
| **`PurgeSpace`** | `0x01000A` | `0x00A51A` | `memory_mgr.s:348` | **Proto:** `Pascal: PROCEDURE PurgeSpace(VAR total, contig: LONGINT);`<br>**Regs:** `Entry: trap bit 10 ($A562) = use the system heap Exit:  D0.L = total free + purgeable bytes in the zone, A0 = largest`<br>_PurgeSpace ($A162): how much space purging the zone could free Pascal: PROCEDURE PurgeSpace(VAR total, contig: LONGINT); Entry: trap bit 10 ($A562) = use the system heap Exit:  D0.L = total free + pu... |
| **`PURGESPACE`** | `0x01000A` | `0x00A51A` | `memory_mgr.s:238` | — |
| **`PUSHCNAME`** | `0x004258` | `0x005CF8` | `file_mgr_dir.s:357`<br>`file_mgr_dir.s:318` | PUSHCNAME PushCName: save CName on A6 stack, return Pascal string in A0 Called by: RENAME_OK_2, CREATE_NO, DELETE_SKIP, RENAME_NO_2, HFSCATMOVE_NO_2 |
| **`QSEARCH_FOUND`** | `0x002C9A` | `0x0046E2` | `file_mgr_vol.s:160`<br>`file_mgr_vol.s:149` | QSEARCH_FOUND - queue search: element found |
| **`QSEARCH_LOOP`** | `0x002C8C` | `0x0046D4` | `file_mgr_vol.s:148`<br>`file_mgr_vol.s:142` | — |
| **`QSEARCH_NOTFOUND`** | `0x002CA2` | `0x0046EA` | `file_mgr_vol.s:171`<br>`file_mgr_vol.s:155` | QSEARCH_NOTFOUND - queue search: element not found |
| **`QSEARCH_RET`** | `0x002C9C` | `0x0046E4` | `file_mgr_vol.s:162`<br>`file_mgr_vol.s:151` | — |
| **`QSTUFF`** | — | `0x002AB6` | `queue.s:28` | OS Queue Primitives -- Enqueue / Dequeue / InitQueuePrim Three core list-manipulation routines used by the Device Manager (I/O queue), Event Manager (event queue), and VBL task manager. Routines: Enqu... |
| **`QueueSearch`** | `0x002C86` | `0x0046CE` | `file_mgr_vol.s:145`<br>`file_mgr_vol.s:139` | **Regs:** `Entry: A0 -> queue header, D0 = key to match, D1 = field offset Exit: Z=1 if found (A0 -> matching element), Z=0 if not found`<br>QueueSearch - search a queue for element with word at offset D1 == D0 Entry: A0 -> queue header, D0 = key to match, D1 = field offset Exit: Z=1 if found (A0 -> matching element), Z=0 if not found |
| **`RB_CHK_DIRTY`** | `0x007A30` | `0x009584` | `file_mgr_cache.s:545`<br>`file_mgr_cache.s:469` | RB_CHK_DIRTY - RelBlock: check dirty/write options |
| **`RB_CHK_WRITE`** | `0x007A3C` | `0x009590` | `file_mgr_cache.s:549`<br>`file_mgr_cache.s:473` | — |
| **`RB_EXIT`** | `0x007A52` | `0x0095A6` | `file_mgr_cache.s:559`<br>`file_mgr_cache.s:483` | — |
| **`RB_EXIT_OK`** | `0x007A50` | `0x0095A4` | `file_mgr_cache.s:557`<br>`file_mgr_cache.s:481` | RBExit |
| **`RC_CASE_RENAME`** | `0x0064F4` | `0x007FC0` | `file_mgr_catalog.s:545`<br>`file_mgr_catalog.s:498` | case-only rename: just update the name in place |
| **`RC_CHK_FILNUM`** | `0x0064E6` | `0x007FB2` | `file_mgr_catalog.s:537`<br>`file_mgr_catalog.s:490` | locate source CNode save catalog data record build new key and insert renamed record "already exists": check if it's really a case-only rename |
| **`RC_DEL_OLD`** | `0x00650A` | `0x007FD6` | `file_mgr_catalog.s:554`<br>`file_mgr_catalog.s:507` | RCDelOld: normal rename - delete old record |
| **`RC_ERR_EXIT`** | `0x00655E` | — | `file_mgr_catalog.s:587` | — |
| **`RC_EXISTS_ERR`** | `0x0064F0` | `0x007FBC` | `file_mgr_catalog.s:541`<br>`file_mgr_catalog.s:494` | — |
| **`RC_EXIT`** | `0x006552` | — | `file_mgr_catalog.s:582` | RCExit |
| **`RC_UPD_THD`** | `0x006528` | `0x007FF2` | `file_mgr_catalog.s:567`<br>`file_mgr_catalog.s:520` | RCUpdThd: update thread record with new name |
| **`RDBLK_ENTRY`** | `0x007C94` | `0x0097EA` | `file_mgr_cache.s:933`<br>`file_mgr_cache.s:762` | — |
| **`RdBlocks`** | `0x007C92` | `0x0097E2` | `file_mgr_cache.s:931` | Rd Blocks Called during boot. |
| **`RDBLOCKS`** | `0x007C92` | `0x0097E2` | `file_mgr_cache.s:757` | — |
| **`RDIP_DONE`** | `0x007B54` | `0x0096A8` | `file_mgr_cache.s:716`<br>`file_mgr_cache.s:600` | — |
| **`RDMAIN`** | `0x004F76` | `0x006A1C` | `file_mgr_io.s:63`<br>`file_mgr_io.s:65` | RdMain: read multiple blocks into place in user's buffer |
| **`RDPART`** | `0x004F62` | `0x006A08` | `file_mgr_io.s:55`<br>`file_mgr_io.s:57` | RdPart: must read a partial block first |
| **`RDrvrInstall`** | `0x00F72C` | — | `segment_loader.s:402` | _RDrvrInstall ($A04F) _RDrvrInstall: reinitialize desk accessory DCEs for new application Clears DCEs whose drivers lived in the app heap (now destroyed) Called during boot. |
| **`RDRVRINSTALL_CONT`** | `0x00F73A` | — | `segment_loader.s:407` | — |
| **`RDRVRINSTALL_LOOP`** | `0x00F760` | `0x009BAA` | `segment_loader.s:424`<br>`segment_loader.s:343` | driver was in app heap: zero out DCE (40 bytes) |
| **`RDRVRINSTALL_LOOP_TOP`** | — | `0x009B84` | `segment_loader.s:327` | — |
| **`RDRVRINSTALL_NO`** | `0x00F770` | `0x009BBA` | `segment_loader.s:429`<br>`segment_loader.s:348` | — |
| **`RDRVRINSTALL_NO_2`** | `0x00F780` | `0x009BC8` | `segment_loader.s:435`<br>`segment_loader.s:354` | — |
| **`RDRVRINSTALL_SKIP`** | `0x00F784` | `0x009BCC` | `segment_loader.s:437`<br>`segment_loader.s:356` | — |
| **`Read`** | `0x0023BE` | `0x00315C` | `device_mgr.s:610` | _Read ($A002) A0 = paramBlock -> D0 = error; reads ioReqCount bytes Positive ioRefNum -> file read; negative -> device driver read. Called during boot. |
| **`READ`** | `0x0023BE` | `0x00315C` | `device_mgr.s:546` | READ - _Read trap: read from device or file Negative ioRefNum = device, positive = file. D4 = 0 = dCtlFlags bit to test for read permission (bit 0). |
| **`READ_DEVICE`** | `0x0023C8` | `0x003166` | `device_mgr.s:621`<br>`device_mgr.s:550` | READ_DEVICE - device driver read path D0 = -19 (readErr default), D4 = 0 (dReadEnable bit position) Called during boot. |
| **`READBLOCK`** | — | `0x009702` | `file_mgr_cache.s:650` | — |
| **`ReadBM`** | `0x005A04` | — | `file_mgr_alloc.s:305` | ReadBM -- pick up the bitmap block of interest. Read BM Called by: BLKALLOC_NO, BLKALLOC_CONT, BLKALLOC_CONT_4, BlkDealloc, BLKCHK_NEXT (and 1 more) |
| **`READBM_CONT`** | `0x005A30` | `0x0074DA` | `file_mgr_alloc.s:325`<br>`file_mgr_alloc.s:280` | — |
| **`READBM_CONT_2`** | `0x005A42` | `0x0074EC` | `file_mgr_alloc.s:348`<br>`file_mgr_alloc.s:301` | READBM_CONT_2 - FrBitScan: scan for next free bit, skipping $FFFFFFFF words |
| **`READBM_CONT_3`** | `0x005A48` | `0x0074F2` | `file_mgr_alloc.s:352`<br>`file_mgr_alloc.s:305` | — |
| **`READBM_CONT_4`** | `0x005A7E` | `0x007526` | `file_mgr_alloc.s:384`<br>`file_mgr_alloc.s:332` | — |
| **`READBM_EXIT`** | `0x005A3E` | `0x0074E8` | `file_mgr_alloc.s:340`<br>`file_mgr_alloc.s:294` | — |
| **`READBM_NEXT`** | `0x005A34` | `0x0074DE` | `file_mgr_alloc.s:334`<br>`file_mgr_alloc.s:288` | READBM_NEXT - NextBit: advance to next bit in bitmap Called by: BLKALLOC_CONT_3, BLKALLOC_OK_2, BLKDEALLOC_CONT, UPDATEFREE_NO, READBM_CONT_2 |
| **`READBM_NEXT_2`** | `0x005A5C` | `0x007506` | `file_mgr_alloc.s:368`<br>`file_mgr_alloc.s:316` | READBM_NEXT_2 - NextWord: get next longword from bitmap buffer |
| **`READBM_NEXT_3`** | `0x005A82` | `0x00752A` | `file_mgr_alloc.s:392`<br>`file_mgr_alloc.s:339` | READBM_NEXT_3 - GetBMBlk: read a volume bitmap block from cache |
| **`READBM_NO`** | `0x005A78` | `0x007520` | `file_mgr_alloc.s:381`<br>`file_mgr_alloc.s:329` | — |
| **`READBM_OK`** | `0x005A24` | `0x0074CE` | `file_mgr_alloc.s:320`<br>`file_mgr_alloc.s:275` | ReadBM: read bitmap block for allocation block D2 |
| **`READBM_OK_2`** | `0x005A58` | `0x007502` | `file_mgr_alloc.s:360`<br>`file_mgr_alloc.s:313` | — |
| **`READBM_OK_3`** | `0x005A76` | `0x00751E` | `file_mgr_alloc.s:379`<br>`file_mgr_alloc.s:327` | — |
| **`ReadDateTime`** | `0x00F7CA` | `0x009C14` | `os_utilities.s:75` | _ReadDateTime ($A039) _ReadDateTime ($A039): read date/time from RTC into Time global |
| **`READDATETIME`** | `0x00F7CA` | `0x009C14` | `os_utilities.s:59` | — |
| **`ReadOwnBuf`** | `0x007BAE` | `0x009702` | `file_mgr_cache.s:784` | Read Own Buf Called during boot. |
| **`READOWNBUF`** | `0x007BAE` | `0x009702` | `file_mgr_cache.s:651` | — |
| **`ReadParam`** | `0x00F790` | `0x009BDA` | `os_utilities.s:25` | Operating System Utilities Apple source: SysUtil.a (MacSEROM.lst module SYSUTIL). In ROM order: ReadParam, WriteParam      - parameter RAM: low-memory copy SysParam <-> clock chip ReadDateTime, SetDat... |
| **`READPARAM`** | `0x00F790` | `0x009BDA` | `os_utilities.s:24` | — |
| **`READPARAM_CONT`** | `0x00F79A` | `0x009BE4` | `os_utilities.s:37`<br>`os_utilities.s:35` | READPARAM_CONT READPARAM_CONT: copy selected bytes from A1 to A0 based on D0 bitmask Iterates 20 bytes; if corresponding bit in D0 is set, copies byte |
| **`READPARAM_LOOP`** | `0x00F79C` | `0x009BE6` | `os_utilities.s:39`<br>`os_utilities.s:37` | — |
| **`READPARAM_SKIP`** | `0x00F7A2` | `0x009BEC` | `os_utilities.s:43`<br>`os_utilities.s:41` | — |
| **`ReadPRAM`** | `0x00FC8A` | `0x00A0D4` | `os_utilities.s:445` | ReadPRAM: read 20 bytes from RTC PRAM into buffer at A1 PRAM is split: 16 bytes at RTC registers $C1-$FC, 4 bytes at $A1-$AC |
| **`READPRAM`** | `0x00FC8A` | `0x00A0D4` | `os_utilities.s:495` | STRIP_TBL (continued): entries $96-$FF READPRAM - called from 2 places |
| **`READPRAM_CONT`** | `0x00FCAE` | `0x00A0F8` | `os_utilities.s:473`<br>`os_utilities.s:521` | READPRAM_CONT |
| **`READPRAM_LOOP`** | `0x00FCA0` | `0x00A0EA` | `os_utilities.s:462`<br>`os_utilities.s:511` | READPRAM_LOOP: read consecutive RTC registers into buffer at A1 D1 = starting RTC command, D5 = byte count - 1 Called during boot. |
| **`ReallocHandle`** | `0x0101EC` | `0x00A704` | `memory_mgr.s:828` | _ReallocHandle ($A027) A0 = handle, D0.L = size -> (reallocated) Called during boot. |
| **`REALLOCHANDLE`** | `0x0101EC` | `0x00A704` | `memory_mgr.s:477` | — |
| **`REALLOCHANDLE_ERR`** | `0x01021E` | — | `memory_mgr.s:851` | REALLOCHANDLE_ERR |
| **`REALLOCHANDLE_ERR_2`** | `0x01022A` | `0x00A742` | `memory_mgr.s:857`<br>`memory_mgr.s:501` | — |
| **`REALLOCHANDLE_LOCKED`** | — | `0x00A736` | `memory_mgr.s:495` | — |
| **`REALLOCHANDLE_OK`** | `0x010204` | `0x00A71C` | `memory_mgr.s:837`<br>`memory_mgr.s:486` | — |
| **`RecoverHandle`** | `0x0101B6` | `0x00A6CE` | `memory_mgr.s:783` | _RecoverHandle ($A128): given a pointer, find its handle A0 = pointer -> A0 = handle |
| **`RECOVERHANDLE`** | `0x0101B6` | `0x00A6CE` | `memory_mgr.s:453` | — |
| **`RECOVERHANDLE_FOUND`** | `0x0101D2` | `0x00A6EA` | `memory_mgr.s:795`<br>`memory_mgr.s:464` | verify the master pointer actually points back to this block |
| **`REL_MAP`** | `0x007052` | `0x008B14` | `file_mgr_btree.s:1271`<br>`file_mgr_btree.s:1090` | REL_MAP -- relMap: release map node. REL_MAP Called by: ALLOC_FOUNDBIT, ALLOC_COMMIT, EXTBT_MARKOLD, EXTBT_UPDFREE, FREENODE_GETMAP (and 1 more) |
| **`RelBlock`** | `0x007A10` | `0x00955E` | `file_mgr_cache.s:530` | Rel Block Called during boot. |
| **`RELBLOCK`** | `0x007A10` | `0x00955E` | `file_mgr_cache.s:452` | Called by: FLUSHMDB, MOUNTVOL_SKIP_2, HFSE_OK_3, FILECLOSE_NO_2, BTOPEN_RELBLK (and 3 more) |
| **`ReleaseMP`** | `0x010AD4` | `0x00B092` | `memory_mgr.s:2549` | ReleaseMP - put master pointer A1 at the head of the zone's free list Called during boot (14,917 times in 30s trace). |
| **`RELEASEMP`** | `0x010AD4` | `0x00B092` | `memory_mgr.s:1882` | — |
| **`RelNode`** | `0x0075D6` | `0x009124` | `file_mgr_btree.s:2118` | Rel Node |
| **`RELNODE`** | `0x0075D6` | `0x009124` | `file_mgr_btree.s:1836` | RelNode: release a B-tree node via block cache Called by: BTINS_CLEANUP, BTDEL_CHKRECS, BTDEL_GETRSIB, BDFREE, BTDEL_RELCHILD (and 12 more) |
| **`RELNODE_SKIP`** | `0x0075E2` | `0x009136` | `file_mgr_btree.s:2124`<br>`file_mgr_btree.s:1845` | — |
| **`RelString`** | `0x00F804` | `0x009C4E` | `os_utilities.s:137` | _RelString ($A050): compare two strings, returning ordering D0.hi=len1, D0.lo=len2, A0=str1, A1=str2, D1=case/marks flags Returns: D0<0 if str1<str2, D0=0 if equal, D0>0 if str1>str2 |
| **`RELSTRING`** | `0x00F804` | `0x009C4E` | `os_utilities.s:93` | — |
| **`RELSTRING_CONT`** | `0x00F84A` | `0x009C94` | `os_utilities.s:200`<br>`os_utilities.s:152` | RELSTRING_CONT Called during boot. |
| **`RELSTRING_CONT_2`** | `0x00F852` | `0x009C9C` | `os_utilities.s:204`<br>`os_utilities.s:156` | — |
| **`RELSTRING_CONT_3`** | `0x00F85A` | `0x009CA4` | `os_utilities.s:208`<br>`os_utilities.s:160` | — |
| **`RELSTRING_CONT_4`** | `0x00F85C` | `0x009CA6` | `os_utilities.s:218`<br>`os_utilities.s:169` | RELSTRING_CONT_4 RELSTRING_CONT_4: set up character comparison tables for string operations D1 encodes case/marks sensitivity flags A2 = uppercase table (CONVERSION_TBL), A3 = diacritical stripping ta... |
| **`RELSTRING_EXIT`** | `0x00F844` | `0x009C8E` | `os_utilities.s:188`<br>`os_utilities.s:141` | RELSTRING_EXIT Called during boot. |
| **`RELSTRING_EXIT_2`** | `0x00F846` | `0x009C90` | `os_utilities.s:190`<br>`os_utilities.s:143` | — |
| **`RELSTRING_EXIT_3`** | `0x00F848` | `0x009C92` | `os_utilities.s:192`<br>`os_utilities.s:145` | — |
| **`RELSTRING_EXIT_4`** | `0x00F872` | `0x009CBC` | `os_utilities.s:233`<br>`os_utilities.s:183` | RELSTRING_EXIT_4 RelString/CmpString exit: restore regs |
| **`RELSTRING_LOOP`** | `0x00F820` | `0x009C6A` | `os_utilities.s:165`<br>`os_utilities.s:119` | RELSTRING_LOOP Called during boot. |
| **`RELSTRING_LOOP_2`** | `0x00F838` | `0x009C82` | `os_utilities.s:176`<br>`os_utilities.s:130` | — |
| **`RELSTRING_OK`** | `0x00F81A` | `0x009C64` | `os_utilities.s:155`<br>`os_utilities.s:110` | RELSTRING_OK Called during boot. |
| **`Rename`** | `0x004482` | `0x005F1C` | `file_mgr_dir.s:717` | _Rename ($A00B) _Rename ($A00B) |
| **`RENAME`** | `0x004482` | `0x005F1C` | `file_mgr_dir.s:626` | — |
| **`RENAME_CONT`** | `0x00452A` | `0x005FC4` | `file_mgr_dir.s:782`<br>`file_mgr_dir.s:692` | locate source file in catalog locate destination (new name) in catalog check if new name already exists (or is same file) |
| **`RENAME_CONT_2`** | `0x0045CC` | `0x006066` | `file_mgr_dir.s:844`<br>`file_mgr_dir.s:755` | update FCBs for renamed file: new CName and catalog hint update all open FCBs for this file with new name |
| **`RENAME_DO_CATALOG`** | — | `0x005FD2` | `file_mgr_dir.s:700` | do the catalog rename |
| **`RENAME_DUPFN_TRANSLATE`** | — | `0x005F54` | `file_mgr_dir.s:650` | — |
| **`RENAME_ERR`** | `0x0044B0` | `0x005F4A` | `file_mgr_dir.s:734`<br>`file_mgr_dir.s:643` | check if rename crosses volumes (HFS move-rename) |
| **`RENAME_ERR_2`** | `0x0044B2` | `0x005F4C` | `file_mgr_dir.s:736`<br>`file_mgr_dir.s:646` | Called by: RENAME_NO_2, RENAME_HFS_PATH, RENAME, RENAME_ERR_3, RENAME_ERR_4 (and 1 more) |
| **`RENAME_ERR_3`** | `0x00452C` | `0x005FC6` | `file_mgr_dir.s:784`<br>`file_mgr_dir.s:694` | locate source file in catalog locate destination (new name) in catalog check if new name already exists (or is same file) |
| **`RENAME_ERR_4`** | `0x0045E8` | `0x006082` | `file_mgr_dir.s:855`<br>`file_mgr_dir.s:768` | Called by: RENAME_NO_3, RENAME_ERR_5, RENAME_VOL_VERIFY_ONLINE |
| **`RENAME_ERR_5`** | `0x0045EC` | `0x006086` | `file_mgr_dir.s:862`<br>`file_mgr_dir.s:774` | RENAME_ERR_5 |
| **`RENAME_HFS_PATH`** | — | `0x005F58` | `file_mgr_dir.s:653` | HFS Rename: check write protect and find source |
| **`RENAME_NEXT_FCB_FOR_FILE`** | — | `0x006080` | `file_mgr_dir.s:765` | — |
| **`RENAME_NO`** | `0x0044BA` | — | `file_mgr_dir.s:740` | — |
| **`RENAME_NO_2`** | `0x00457C` | `0x006016` | `file_mgr_dir.s:816`<br>`file_mgr_dir.s:727` | cleanup: pop both CNames from FS stack |
| **`RENAME_NO_3`** | `0x0045F8` | `0x006092` | `file_mgr_dir.s:868`<br>`file_mgr_dir.s:780` | MFS Rename path: rename on MFS volume (including volume name) |
| **`RENAME_OK`** | `0x0044BE` | — | `file_mgr_dir.s:743` | TFS Rename: find source and dest on same volume |
| **`RENAME_OK_2`** | `0x004538` | — | `file_mgr_dir.s:790` | do the catalog rename |
| **`RENAME_OK_3`** | `0x004574` | — | `file_mgr_dir.s:812` | if renamed in root, update VCB volume name |
| **`RENAME_UPDATE_VOL_NAME`** | — | `0x00600E` | `file_mgr_dir.s:722` | check if root dir or volume renamed (update volume name) |
| **`RENAME_VOL_COPY_NAME`** | — | `0x0060B8` | `file_mgr_dir.s:796` | copy new name to VCB volume name |
| **`RENAME_VOL_VERIFY_ONLINE`** | — | `0x0060B2` | `file_mgr_dir.s:792` | — |
| **`REPOS_ALERT_PORT`** | `0x00136E` | `0x00157E` | `sys_error.s:376`<br>`sys_error.s:333` | REPOS_ALERT_PORT - reposition port to existing alert rect |
| **`ResolveWDVCB`** | `0x002CF4` | `0x00473C` | `file_mgr_vol.s:251`<br>`file_mgr_vol.s:220` | ResolveWDVCB - resolve working directory refnum (D0) to its VCB WD refnums range from -32767..-4096 (WDRfnMin..WDRfnMax). Each maps to an entry in the WDCB array. The WDCB contains a pointer to the VC... |
| **`ResrvMem`** | `0x01001E` | `0x00A52E` | `memory_mgr.s:369` | _ResrvMem ($A040) D0.L = needed -> (reserves space) Called during boot. |
| **`RESRVMEM`** | `0x01001E` | `0x00A52E` | `memory_mgr.s:246` | — |
| **`RESRVMEM_MAKESPC`** | — | `0x00A544` | `memory_mgr.s:255` | — |
| **`RESRVMEM_SKIP`** | `0x010034` | — | `memory_mgr.s:378` | — |
| **`RESTOP`** | — | `0x01AA9C` | `dispatch_table.s:12` | Compressed trap dispatch table Apple source: DispTable.a (MacSEROM.lst modules RESTOP and DSPTABLE). Read once at startup by INITDISPATCHER (boot_install.s), which fills the Toolbox dispatch table (51... |
| **`RFNCall`** | `0x005358` | — | `file_mgr_io.s:637` | RFN Call Called during boot. RFNCall: map a reference number to FCB/VCB pointers |
| **`RFNCALL_CONT`** | `0x005376` | `0x006E28` | `file_mgr_io.s:647`<br>`file_mgr_io.s:574` | — |
| **`RFNCALL_OK`** | `0x005398` | — | `file_mgr_io.s:671` | — |
| **`RmvTime`** | `0x0175E0` | `0x01A96A` | `time_mgr.s:51` | RmvTime -- trap handler for _RmvTime ($A059). _RmvTime ($A059) |
| **`RMVTIME`** | `0x0175E0` | `0x01A96A` | `time_mgr.s:68` | _RmvTime ($A059) - dequeue TMTask (A0) and reschedule if needed |
| **`RMVTIME_DONE`** | `0x0175F8` | `0x01A982` | `time_mgr.s:60`<br>`time_mgr.s:77` | — |
| **`ROT_RECLT`** | `0x00726C` | `0x008DCC` | `file_mgr_btree.s:1584`<br>`file_mgr_btree.s:1422` | ROT_RECLT RotRecLt: rotates one record from right node into left node |
| **`RotateLT`** | `0x00706C` | `0x008BC8` | `file_mgr_btree.s:1288` | RotateLT -- try rotating left. Rotate LT |
| **`ROTATELT`** | `0x00706C` | `0x008BC8` | `file_mgr_btree.s:1164` | RotateLT: rotate records from right node to left sibling |
| **`ROTLT_ADJINDX`** | `0x0070AA` | — | `file_mgr_btree.s:1325` | — |
| **`ROTLT_CHKFIT`** | `0x0070DE` | `0x008C3A` | `file_mgr_btree.s:1358`<br>`file_mgr_btree.s:1225` | — |
| **`ROTLT_CHKRT`** | `0x0070CA` | `0x008C26` | `file_mgr_btree.s:1345`<br>`file_mgr_btree.s:1212` | RLChkFit: check for a fit after simulated rotation ROTLT_CHKRT |
| **`ROTLT_CHKRT2`** | `0x007130` | `0x008C8C` | `file_mgr_btree.s:1410`<br>`file_mgr_btree.s:1271` | RLCheckRt: check if new record goes in right node |
| **`ROTLT_CHKSPLIT`** | `0x007128` | `0x008C84` | `file_mgr_btree.s:1404`<br>`file_mgr_btree.s:1265` | — |
| **`ROTLT_CKSPLIT`** | `0x0070D6` | `0x008C32` | `file_mgr_btree.s:1353`<br>`file_mgr_btree.s:1220` | RLCkSplit: select best fit |
| **`ROTLT_DOROT`** | `0x007100` | `0x008C5C` | `file_mgr_btree.s:1380`<br>`file_mgr_btree.s:1246` | ROTLT_DOROT RLRotate: we have a fit, do the actual rotation |
| **`ROTLT_EXIT`** | `0x007154` | `0x008CB0` | `file_mgr_btree.s:1436`<br>`file_mgr_btree.s:1296` | — |
| **`ROTLT_FATAL`** | `0x00714A` | `0x008CA6` | `file_mgr_btree.s:1428`<br>`file_mgr_btree.s:1288` | ROTLT_FATAL |
| **`ROTLT_FITLOOP`** | `0x007096` | `0x008BF2` | `file_mgr_btree.s:1309`<br>`file_mgr_btree.s:1183` | calculate split point simulate left rotation to determine best fit RLFitLoop |
| **`ROTLT_GETREC`** | `0x00709E` | `0x008BFA` | `file_mgr_btree.s:1319`<br>`file_mgr_btree.s:1188` | ROTLT_GETREC |
| **`ROTLT_INCLOFF`** | `0x0070B0` | `0x008C0C` | `file_mgr_btree.s:1328`<br>`file_mgr_btree.s:1197` | — |
| **`ROTLT_LOOP`** | `0x007104` | `0x008C60` | `file_mgr_btree.s:1382`<br>`file_mgr_btree.s:1248` | — |
| **`ROTLT_NEXTFIT`** | `0x0070E8` | `0x008C44` | `file_mgr_btree.s:1364`<br>`file_mgr_btree.s:1231` | — |
| **`ROTLT_OK`** | `0x00714E` | `0x008CAA` | `file_mgr_btree.s:1432`<br>`file_mgr_btree.s:1292` | RLExit |
| **`ROTLT_ROTREC`** | `0x00711E` | `0x008C7A` | `file_mgr_btree.s:1399`<br>`file_mgr_btree.s:1260` | ROTLT_ROTREC |
| **`ROTLT_SKIPADJ`** | — | `0x008C06` | `file_mgr_btree.s:1194` | — |
| **`ROTRECLT_DEL`** | `0x007290` | `0x008DF0` | `file_mgr_btree.s:1599`<br>`file_mgr_btree.s:1436` | RRLDelete: delete record from right node |
| **`ROTRECLT_EXIT`** | `0x007298` | `0x008DF8` | `file_mgr_btree.s:1603`<br>`file_mgr_btree.s:1440` | — |
| **`RoundAlloc`** | `0x002C64` | `0x0046AC` | `file_mgr_vol.s:122` | RoundAlloc - round byte count D0 up to D1 allocation-block-aligned Given D0=current byte count, D1=requested bytes, A2->VCB: Returns D0 = number of allocation blocks needed, rounded up to the nearest ... |
| **`ROUNDALLOC`** | `0x002C64` | `0x0046AC` | `file_mgr_vol.s:117` | **Regs:** `Entry: D0 = existing value, D1 = byte count to convert Exit: stacked allocation block count`<br>ROUNDALLOC - round byte count to allocation blocks Converts a byte count (D1) to allocation block count using the volume's block size from the VCB at (A2). Entry: D0 = existing value, D1 = byte count ... |
| **`RstFilLock`** | `0x004894` | `0x00633A` | `file_mgr_dir.s:1212` | RstFilLock -- trap handler for _RstFilLock ($A042). _RstFilLock ($A042) |
| **`RSTFILLOCK`** | `0x004894` | `0x00633A` | `file_mgr_dir.s:1097` | _RstFilLock ($A042): unlock a file |
| **`RSTFILLOCK_CONT`** | `0x00489C` | — | `file_mgr_dir.s:1216` | SetFilLock/RstFilLock: TFS path |
| **`RSTFILLOCK_CONT_2`** | `0x0048C0` | `0x006366` | `file_mgr_dir.s:1233`<br>`file_mgr_dir.s:1113` | RSTFILLOCK_CONT_2 |
| **`RSTFILLOCK_CONT_3`** | `0x0048C8` | `0x00636E` | `file_mgr_dir.s:1236`<br>`file_mgr_dir.s:1116` | — |
| **`RSTFILLOCK_ERR`** | `0x0048D2` | `0x0062BC` | `file_mgr_dir.s:1247`<br>`file_mgr_dir.s:1038` | Called by: HFSCATMOVE_CONT_5, HFSCATMOVE_FOUND, HFSCATMOVE_ERR_5, HFSCATMOVE_NO_5 |
| **`RSTFILLOCK_OK`** | `0x0048D0` | `0x006376` | `file_mgr_dir.s:1245`<br>`file_mgr_dir.s:1120` | RSTFILLOCK_OK |
| **`S2D_NOT_LEAP`** | `0x017082` | `0x01A0F2` | `date_utils.s:47`<br>`date_utils.s:44` | — |
| **`S2D_PAST_FEB`** | `0x017092` | `0x01A102` | `date_utils.s:57`<br>`date_utils.s:53` | — |
| **`SAMELEN`** | `0x00506A` | `0x006B10` | `file_mgr_io.s:214`<br>`file_mgr_io.s:207` | SameLen: data will fit, start writing |
| **`SCAN_DONE`** | `0x017670` | `0x01AA06` | `time_mgr.s:125`<br>`time_mgr.s:139` | — |
| **`SCAN_NEXT_TASK`** | `0x017658` | `0x01A9EE` | `time_mgr.s:114`<br>`time_mgr.s:128` | — |
| **`SCAN_SKIP_TASK`** | `0x01766C` | `0x01AA02` | `time_mgr.s:122`<br>`time_mgr.s:136` | — |
| **`SCAN_TIMER_QUEUE`** | `0x01763A` | `0x01A9D0` | `time_mgr.s:104`<br>`time_mgr.s:118` | SCAN_TIMER_QUEUE -- Scan timer queue, find soonest task, program VIA Timer 2 Walks the linked list of TMTasks starting from the queue head. Finds the task with the smallest positive tmCount, stores it... |
| **`SCSI_ARB_DELAY`** | — | `0x01A816` | `scsi_mgr.s:901` | SCSI_ARB_DELAY - short busy-wait delay (~50 cycles) Used as the SCSI bus-settling delay after assertions. Called by: SCSI_SEL_NO_ATN, SCSI_ARB_GOT_AIP, SCSI_DO_SELECT, SCSI_BAD_PHASE_HANDSHAKE |
| **`SCSI_ARB_DELAY_LOOP`** | — | `0x01A818` | `scsi_mgr.s:903` | — |
| **`SCSI_ARB_FAIL`** | `0x0172FC` | — | `scsi_mgr.s:378` | SCSI_ARB_FAIL - arbitration failed: clear mode register and return scCommErr |
| **`SCSI_ARB_GOT_AIP`** | — | `0x01A460` | `scsi_mgr.s:432` | — |
| **`SCSI_ARB_TRY`** | — | `0x01A430` | `scsi_mgr.s:415` | — |
| **`SCSI_ARB_WAIT_AIP`** | — | `0x01A44A` | `scsi_mgr.s:424` | — |
| **`SCSI_ARBITRATE`** | `0x0172BC` | `0x01A426` | `scsi_mgr.s:356`<br>`scsi_mgr.s:412` | SCSI_ARBITRATE - SCSIGet: arbitrate for the SCSI bus using NCR 5380 Returns D0=0 if arbitration won, D0=2 (scCommErr) if lost/timeout |
| **`SCSI_ASSERT_RST`** | `0x0174E6` | `0x01A81E` | `scsi_mgr.s:633`<br>`scsi_mgr.s:911` | SCSI_ASSERT_RST - SCSI bus reset: assert RST for ~200 usec, then release Per SCSI spec, RST must be held at least 25 usec |
| **`SCSI_BAD_PHASE_DONE`** | — | `0x01A948` | `scsi_mgr.s:1047` | — |
| **`SCSI_BAD_PHASE_DRAIN`** | — | `0x01A8F4` | `scsi_mgr.s:1023` | — |
| **`SCSI_BAD_PHASE_EXIT`** | `0x0175C0` | — | `scsi_mgr.s:753` | — |
| **`SCSI_BAD_PHASE_HANDSHAKE`** | — | `0x01A92A` | `scsi_mgr.s:1038` | — |
| **`SCSI_BAD_PHASE_HAVE_REQ`** | — | `0x01A8EA` | `scsi_mgr.s:1019` | — |
| **`SCSI_BAD_PHASE_LOOP`** | — | `0x01A8E2` | `scsi_mgr.s:1014` | — |
| **`SCSI_BAD_PHASE_OK`** | `0x0175BE` | — | `scsi_mgr.s:751` | — |
| **`SCSI_BAD_PHASE_OUT`** | — | `0x01A918` | `scsi_mgr.s:1034` | — |
| **`SCSI_BAD_PHASE_WAIT`** | `0x0175A6` | — | `scsi_mgr.s:743` | I/O=1 (data-in): bit-bucket incoming byte SCSI_PAD_BYTE_OUT - pad byte to target (data-out phase during cleanup) |
| **`SCSI_BFREE_POLL_DONE`** | `0x017536` | — | `scsi_mgr.s:677` | — |
| **`SCSI_BFREE_POLL_LOOP`** | `0x017526` | — | `scsi_mgr.s:671` | — |
| **`SCSI_BLIND_CMP_LOOP`** | `0x017432` | `0x01A642` | `scsi_mgr.s:531`<br>`scsi_mgr.s:664` | Blind compare loop (no per-byte DRQ check after first byte) |
| **`SCSI_BLIND_CMP_NEXT`** | `0x01743A` | — | `scsi_mgr.s:536` | — |
| **`SCSI_BLIND_COMPARE`** | — | `0x01A64A` | `scsi_mgr.s:669` | — |
| **`SCSI_BLIND_FIRST_DRQ`** | `0x017426` | — | `scsi_mgr.s:524` | SCSI_BLIND_FIRST_DRQ - blind transfer: first byte uses DRQ poll, rest are blind Blind: no DRQ check after the first byte - relies on device speed |
| **`SCSI_BLIND_RD_LOOP`** | `0x017440` | — | `scsi_mgr.s:543` | SCSI_BLIND_RD_LOOP - blind read loop (no per-byte DRQ check) |
| **`SCSI_BLIND_READ`** | — | `0x01A654` | `scsi_mgr.s:683` | SCSI_BLIND_READ -- pseudo-DMA fast read into A2 D2 = byte count, D3 = stride shift, D7 = alignment bit. Reads 1 byte for alignment if needed, then unrolls MoveP.L instructions (16 longs = 64 bytes per... |
| **`SCSI_BLIND_READ_ALIGNED`** | — | `0x01A65E` | `scsi_mgr.s:689` | — |
| **`SCSI_BLIND_READ_LOOP`** | — | `0x01A66E` | `scsi_mgr.s:698` | — |
| **`SCSI_BLIND_READ_TAIL_BODY`** | — | `0x01A6D8` | `scsi_mgr.s:744` | Tail-byte loop: copy 1 byte at a time for the leftover (D2 + 1) bytes that didn't fit in a 64-byte unrolled chunk. |
| **`SCSI_BLIND_READ_TAIL_LOOP`** | — | `0x01A6DA` | `scsi_mgr.s:746` | — |
| **`SCSI_BLIND_WR_LOOP`** | `0x017448` | — | `scsi_mgr.s:551` | SCSI_BLIND_WR_LOOP - blind write loop (no per-byte DRQ check) |
| **`SCSI_BLIND_WRITE`** | — | `0x01A6E0` | `scsi_mgr.s:758` | SCSI_BLIND_WRITE -- pseudo-DMA fast write from A2 to A1 D2 = byte count, D3 = stride shift, D7 = alignment bit. Symmetric to SCSI_BLIND_READ but writes A2-resident data to the NCR 5380 data port (A1) ... |
| **`SCSI_BLIND_WRITE_ALIGNED`** | — | `0x01A6EA` | `scsi_mgr.s:764` | — |
| **`SCSI_BLIND_WRITE_LOOP`** | — | `0x01A6FA` | `scsi_mgr.s:779` | SCSI_BLIND_WRITE_LOOP inner-loop body: 16 unrolled (MOVE.L (A2)+,D5; MoveP.L D5,$0(A1)) pairs send 16 long-words = 64 bytes from the buffer at (A2)+ to the NCR 5380 data port (A1, accessed via MoveP.L... |
| **`SCSI_BLIND_WRITE_TAIL_BODY`** | — | `0x01A764` | `scsi_mgr.s:816` | Tail-byte loop for SCSI_BLIND_WRITE. |
| **`SCSI_BLIND_WRITE_TAIL_LOOP`** | — | `0x01A766` | `scsi_mgr.s:818` | — |
| **`SCSI_BSY_POLL_DONE`** | `0x017520` | — | `scsi_mgr.s:661` | — |
| **`SCSI_BSY_POLL_LOOP`** | `0x017512` | — | `scsi_mgr.s:655` | — |
| **`SCSI_BUS_SETTLE`** | `0x0174DE` | — | `scsi_mgr.s:624` | SCSI_BUS_SETTLE - short bus-settle delay (~50 iterations, ~20 usec) Used after signal changes to allow SCSI bus signals to stabilize |
| **`SCSI_BUSERR_HANDLER`** | — | `0x01A630` | `scsi_mgr.s:649` | SCSI_BUSERR_HANDLER - bus-error trampoline installed during xfer If the inner loop touches a faulting address, the 68000 bus-error exception lands here. We unwind to the saved SP, set scBusError (9) o... |
| **`SCSI_CDB_BYTE_LOOP`** | `0x017366` | — | `scsi_mgr.s:425` | Send each CDB byte with REQ/ACK handshake |
| **`SCSI_CDB_DONE`** | `0x01739A` | `0x01A51A` | `scsi_mgr.s:438`<br>`scsi_mgr.s:509` | — |
| **`SCSI_CDB_LOOP`** | — | `0x01A4F4` | `scsi_mgr.s:498` | — |
| **`SCSI_CHECK_BLIND`** | `0x0171CC` | — | `scsi_mgr.s:189` | — |
| **`SCSI_CHECK_PHASE`** | — | `0x01A94C` | `scsi_mgr.s:1053` | SCSI_CHECK_PHASE - verify sBSR phase-match bit (bit 3) Output: D0 = 0 (match) or 5 (scPhaseErr) |
| **`SCSI_CHECK_PHASE_DONE`** | — | `0x01A958` | `scsi_mgr.s:1058` | — |
| **`SCSI_CMD_DONE`** | — | `0x01A2EA` | `scsi_mgr.s:231` | — |
| **`SCSI_CMPL_CHKTMO`** | `0x017272` | `0x01A3AC` | `scsi_mgr.s:310`<br>`scsi_mgr.s:340` | — |
| **`SCSI_CMPL_GOT_MSG`** | — | `0x01A3C6` | `scsi_mgr.s:352` | — |
| **`SCSI_CMPL_GOT_STATUS`** | `0x01727A` | `0x01A3B6` | `scsi_mgr.s:317`<br>`scsi_mgr.s:345` | SCSI_CMPL_GOT_STATUS - status byte received; now read message-in byte |
| **`SCSI_CMPL_POLL`** | `0x017260` | `0x01A396` | `scsi_mgr.s:303`<br>`scsi_mgr.s:331` | Poll loop: wait for status phase or handle unexpected phases |
| **`SCSI_CMPL_RESULT`** | — | `0x01A3CC` | `scsi_mgr.s:355` | — |
| **`SCSI_CMPL_STORE`** | `0x01728C` | — | `scsi_mgr.s:324` | — |
| **`SCSI_DISPATCH_OFFSETS`** | — | `0x01A220` | `scsi_mgr.s:137` | Dispatch offset table - 24 word offsets relative to SCSI_DISPATCH_OFFSETS INITSCSIMGR converts these to absolute longs in SCSIGlobals[0..23]. sel 0=SCSIReset(+0x46), 1=SCSIGet(+0x5C), 2=SCSISelect(+0x... |
| **`SCSI_DO_SELECT`** | `0x017306` | `0x01A484` | `scsi_mgr.s:387`<br>`scsi_mgr.s:452` | SCSI_DO_SELECT - SCSISelect: select target device after winning arbitration D0 = target SCSI ID (0-6) on entry Returns D0=0 if target responded, D0=2 (scCommErr) if timeout |
| **`SCSI_DT_CMD`** | `0x01714A` | — | `scsi_mgr.s:85` | Selector 3: SCSICmd (send command descriptor block) |
| **`SCSI_DT_COMPLETE`** | `0x01714E` | — | `scsi_mgr.s:90` | Selector 4: SCSIComplete (get status + message, release bus) |
| **`SCSI_DT_GET`** | `0x017142` | — | `scsi_mgr.s:75` | Selector 1: SCSIGet (arbitrate for SCSI bus) |
| **`SCSI_DT_INSTALL`** | `0x01715A` | — | `scsi_mgr.s:105` | Selector 7: SCSIInstall (install interrupt handler - stub) |
| **`SCSI_DT_RBLIND`** | `0x01715E` | — | `scsi_mgr.s:111` | Selector 8: SCSIRBlind (blind/pseudo-DMA read via TIB) D1=8 signals blind mode to SCSIRead (checked at SCSI_CHECK_BLIND) |
| **`SCSI_DT_READ`** | `0x017152` | — | `scsi_mgr.s:95` | Selector 5: SCSIRead (polled read via TIB) |
| **`SCSI_DT_RESET`** | `0x01713E` | — | `scsi_mgr.s:70` | _SCSIDispatch branch table - one BRA.W per selector Selector 0: SCSIReset |
| **`SCSI_DT_SELECT`** | `0x017146` | — | `scsi_mgr.s:80` | Selector 2: SCSISelect (select target device) |
| **`SCSI_DT_STAT`** | `0x017166` | — | `scsi_mgr.s:121` | Selector 10: SCSIStat (return bus status registers) |
| **`SCSI_DT_WBLIND`** | `0x017162` | — | `scsi_mgr.s:116` | Selector 9: SCSIWBlind (blind/pseudo-DMA write via TIB) |
| **`SCSI_DT_WRITE`** | `0x017156` | — | `scsi_mgr.s:100` | Selector 6: SCSIWrite (polled write via TIB) |
| **`SCSI_EPILOGUE`** | `0x0172B0` | `0x01A41A` | `scsi_mgr.s:346`<br>`scsi_mgr.s:400` | SCSI_EPILOGUE - epilogue for all SCSIDispatch handlers D0 = number of parameter bytes to remove from caller's stack |
| **`SCSI_EXIT`** | `0x007D60` | — | `scsi_boot.s:56` | — |
| **`SCSI_FIND_DRVR`** | `0x007D8C` | `0x0040AE` | `scsi_boot.s:78`<br>`scsi_boot.s:87` | Walk DDM driver entries (8 bytes each: ddBlock,ddSize,ddType) |
| **`SCSI_GET_STORE`** | — | `0x01A2AA` | `scsi_mgr.s:200` | — |
| **`SCSI_GET_TRY`** | — | `0x01A29A` | `scsi_mgr.s:195` | — |
| **`SCSI_GET_WAIT`** | — | `0x01A288` | `scsi_mgr.s:188` | — |
| **`SCSI_HANDLE_BAD_PHASE`** | `0x017566` | `0x01A8E0` | `scsi_mgr.s:720`<br>`scsi_mgr.s:1012` | SCSI_HANDLE_BAD_PHASE - handle unexpected bus phase during SCSIComplete If target is not in status phase, bit-bucket data or pad bytes to force bus through to status phase. Loops until phase changes t... |
| **`SCSI_INIT_LOOP`** | — | `0x01A1B6` | `scsi_mgr.s:82` | — |
| **`SCSI_INIT_RTS`** | — | `0x01A204` | `scsi_mgr.s:111` | — |
| **`SCSI_LOAD_DRVR`** | `0x007D9C` | `0x0040BE` | `scsi_boot.s:90`<br>`scsi_boot.s:95` | SCSI_LOAD_DRVR |
| **`SCSI_LOAD_TIB`** | `0x0171D6` | — | `scsi_mgr.s:193` | — |
| **`SCSI_MSGIN_DONE`** | — | `0x01A3EA` | `scsi_mgr.s:369` | — |
| **`SCSI_NEXT_ID`** | `0x007D58` | — | `scsi_boot.s:52` | — |
| **`SCSI_PAD_BYTE_OUT`** | `0x017596` | — | `scsi_mgr.s:739` | I/O=1 (data-in): bit-bucket incoming byte SCSI_PAD_BYTE_OUT - pad byte to target (data-out phase during cleanup) |
| **`SCSI_PMATCH_POLL_DONE`** | `0x017562` | — | `scsi_mgr.s:710` | — |
| **`SCSI_PMATCH_POLL_LOOP`** | `0x017552` | — | `scsi_mgr.s:704` | — |
| **`SCSI_POLL_CMP_LOOP`** | `0x0173F6` | — | `scsi_mgr.s:489` | Polled transfer: check D4.B for direction Polled compare loop: read each byte and compare against buffer |
| **`SCSI_POLL_CMP_NEXT`** | `0x017404` | — | `scsi_mgr.s:496` | — |
| **`SCSI_POLL_RD_LOOP`** | `0x01740A` | — | `scsi_mgr.s:503` | SCSI_POLL_RD_LOOP - polled read loop: read bytes with DRQ polling |
| **`SCSI_POLL_WR_LOOP`** | `0x017418` | — | `scsi_mgr.s:513` | SCSI_POLL_WR_LOOP - polled write loop: write bytes with DRQ polling |
| **`SCSI_PRAM_OK`** | — | `0x01A1E8` | `scsi_mgr.s:100` | — |
| **`SCSI_PREP_PHASE`** | — | `0x01A774` | `scsi_mgr.s:831` | — |
| **`SCSI_PREP_READ`** | — | `0x01A76C` | `scsi_mgr.s:826` | SCSI_PREP_READ - prepare DMA mode for the next transfer Called from SCSI_XFER_ENGINE before write loops, and from blind paths before read/write. Sets sTCR phase, enables DMA mode in sMR, and primes ei... |
| **`SCSI_PREP_WRITE`** | — | `0x01A788` | `scsi_mgr.s:838` | — |
| **`SCSI_PROBE_EXIT`** | `0x007DC6` | — | `scsi_boot.s:109` | — |
| **`SCSI_PROBE_LOOP`** | `0x007D50` | — | `scsi_boot.s:48` | — |
| **`SCSI_PROLOGUE`** | `0x017294` | `0x01A402` | `scsi_mgr.s:333`<br>`scsi_mgr.s:387` | SCSI_PROLOGUE - prologue for all SCSIDispatch handlers Sets up stack frame, saves registers, initializes NCR 5380 pointers Called by: SCSIStat, SCSIReset, SCSIGet, SCSISelect, SCSICmd (and 2 more) |
| **`SCSI_RDMSG_DONE`** | `0x0174D2` | — | `scsi_mgr.s:609` | — |
| **`SCSI_RDSTAT_DONE`** | `0x017498` | — | `scsi_mgr.s:587` | — |
| **`SCSI_READ_BUS_PHASE`** | `0x0174D4` | — | `scsi_mgr.s:616` | SCSI_READ_BUS_PHASE - read current bus phase from sCSR Returns phase bits (I/O + C/D) in D0, masked to 0x0C Used to detect which information transfer phase the target is in |
| **`SCSI_READ_ERR`** | `0x007E4E` | — | `scsi_boot.s:172` | SCSI_READ_ERR Called during boot. |
| **`SCSI_READ_LOAD_TIB`** | — | `0x01A302` | `scsi_mgr.s:247` | — |
| **`SCSI_READ_MSGIN`** | `0x01749A` | `0x01A7BC` | `scsi_mgr.s:594`<br>`scsi_mgr.s:864` | SCSI_READ_MSGIN - read message-in byte from target (message-in phase) Sets TCR to message-in phase (C/D=1, I/O=1, MSG=1 => $07), reads one byte Returns: D0=0 and message byte in D2, or D0=2/5 on error |
| **`SCSI_READ_MSGIN_DONE`** | — | `0x01A7E4` | `scsi_mgr.s:877` | — |
| **`SCSI_READ_STATUS`** | `0x017464` | `0x01A794` | `scsi_mgr.s:573`<br>`scsi_mgr.s:847` | SCSI_READ_STATUS - read status byte from target (status phase) Sets TCR to status phase (C/D=1, I/O=1, MSG=0 => $03), reads one byte Returns: D0=0 and status byte in D2 on success, D0=2 on timeout, D0... |
| **`SCSI_READ_STATUS_DONE`** | — | `0x01A7BA` | `scsi_mgr.s:859` | — |
| **`SCSI_REQCLR_POLL_DONE`** | `0x01754C` | — | `scsi_mgr.s:693` | — |
| **`SCSI_REQCLR_POLL_LOOP`** | `0x01753C` | — | `scsi_mgr.s:687` | — |
| **`SCSI_RETURN_OK`** | `0x017184` | `0x01A276` | `scsi_mgr.s:145`<br>`scsi_mgr.s:176` | — |
| **`SCSI_RST_HOLD`** | — | `0x01A830` | `scsi_mgr.s:917` | — |
| **`SCSI_RST_HOLD_LOOP`** | `0x0174F6` | — | `scsi_mgr.s:638` | — |
| **`SCSI_RST_RECOVER`** | — | `0x01A84A` | `scsi_mgr.s:926` | — |
| **`SCSI_RST_RECOVER_LOOP`** | `0x017506` | — | `scsi_mgr.s:643` | — |
| **`SCSI_scAdd`** | `0x01721C` | — | `scsi_mgr.s:237` | scAdd - add scParam2 long value to the long at address scParam1 |
| **`SCSI_scComp`** | `0x017236` | — | `scsi_mgr.s:266` | scComp - compare SCSI data against memory buffer (verify mode) Sets D4 bit 0 to flag compare mode, then falls into scInc transfer |
| **`SCSI_scInc`** | `0x017208` | — | `scsi_mgr.s:222` | scInc - transfer D2 bytes, then advance scParam1 pointer by D2 |
| **`SCSI_scLoop`** | `0x017226` | — | `scsi_mgr.s:250` | scLoop - decrement scParam2 counter; if >0, jump back by scParam1 offset |
| **`SCSI_scMove`** | `0x017220` | — | `scsi_mgr.s:243` | scMove - copy long from address scParam1 to address scParam2 |
| **`SCSI_scNoInc`** | `0x017214` | — | `scsi_mgr.s:230` | scNoInc - transfer D2 bytes without advancing buffer pointer |
| **`SCSI_scNOp`** | `0x01723C` | — | `scsi_mgr.s:272` | scNop - skip this TIB entry (advance A1 by 10 bytes = sizeof(SCSIInstr)) |
| **`SCSI_scStop`** | `0x017232` | — | `scsi_mgr.s:259` | scStop - terminate TIB execution, return noErr |
| **`SCSI_SEL_DONE`** | — | `0x01A2CE` | `scsi_mgr.s:218` | — |
| **`SCSI_SEL_FAIL`** | — | `0x01A4DA` | `scsi_mgr.s:482` | — |
| **`SCSI_SEL_GO`** | — | `0x01A2BC` | `scsi_mgr.s:212` | — |
| **`SCSI_SEL_NO_ATN`** | — | `0x01A4B0` | `scsi_mgr.s:467` | — |
| **`SCSI_SEL_RELEASE`** | `0x017346` | — | `scsi_mgr.s:406` | — |
| **`SCSI_SEND_CDB`** | `0x01734C` | `0x01A4E0` | `scsi_mgr.s:416`<br>`scsi_mgr.s:491` | SCSI_SEND_CDB - send SCSI command descriptor block (command phase) A2 -> CDB bytes, D2 = CDB length Sets TCR to command phase (C/D=1, I/O=0 => $02), then sends each byte with REQ/ACK handshake Returns... |
| **`SCSI_SEND_MSGOUT`** | — | `0x01A7E6` | `scsi_mgr.s:882` | SCSI_SEND_MSGOUT - send one message-out byte to the target Input: D2 = byte to send; Output: D0 = result. |
| **`SCSI_SEND_MSGOUT_DONE`** | — | `0x01A814` | `scsi_mgr.s:895` | — |
| **`SCSI_SETTLE_LOOP`** | `0x0174E0` | — | `scsi_mgr.s:626` | SCSI_BUS_SETTLE - short bus-settle delay (~50 iterations, ~20 usec) Used after signal changes to allow SCSI bus signals to stabilize |
| **`SCSI_TIB_EXIT`** | `0x017242` | `0x01A376` | `scsi_mgr.s:278`<br>`scsi_mgr.s:316` | SCSI_TIB_EXIT - TIB interpreter exit: store result and return |
| **`SCSI_TIB_LOOP`** | `0x0171DA` | `0x01A30E` | `scsi_mgr.s:197`<br>`scsi_mgr.s:253` | TIB interpreter loop - fetch and dispatch each TIB instruction TIB entry: word opcode at (A1), long scParam1 at 2(A1), long scParam2 at 6(A1) |
| **`SCSI_UNIMPL_HANG`** | — | `0x01A254` | `scsi_mgr.s:156` | — |
| **`SCSI_VERIFY_PHASE`** | `0x0175C2` | — | `scsi_mgr.s:760` | SCSI_VERIFY_PHASE - verify bus is in expected phase (sBSR phase-match bit only; REQ is not tested) Checks sBSR bit 3 (phase match): if set, target phase matches TCR Returns D0=0 if phase correct, D0=5... |
| **`SCSI_VPHASE_DONE`** | `0x0175CE` | — | `scsi_mgr.s:765` | — |
| **`SCSI_WAIT_BSY`** | `0x017510` | `0x01A858` | `scsi_mgr.s:653`<br>`scsi_mgr.s:935` | SCSI_WAIT_BSY - wait for target BSY asserted (selection response) Polls sCSR bit 6 (BSY) until set or D1 timeout expires Returns D0=0 if BSY detected, D0=2 (scCommErr) on timeout |
| **`SCSI_WAIT_BSY_CLEAR`** | `0x017524` | — | `scsi_mgr.s:669` | SCSI_WAIT_BSY_CLEAR - wait for BSY deasserted (bus free detection) Polls sCSR bit 6 (BSY) until clear or D1 timeout expires Returns D0=0 if bus free, D0=2 (scCommErr) on timeout |
| **`SCSI_WAIT_BSY_DONE`** | — | `0x01A874` | `scsi_mgr.s:946` | — |
| **`SCSI_WAIT_BSY_DROP_DONE`** | — | `0x01A894` | `scsi_mgr.s:963` | — |
| **`SCSI_WAIT_BSY_DROP_LOOP`** | — | `0x01A882` | `scsi_mgr.s:957` | SCSI_WAIT_BSY_DROP (unlabeled fallthrough copy in original ROM) Mirror of SCSI_WAIT_BSY but waits for BSY to drop instead of rise. Currently dead code (no callers) but preserved for byte-identity. |
| **`SCSI_WAIT_BSY_LOOP`** | — | `0x01A862` | `scsi_mgr.s:940` | — |
| **`SCSI_WAIT_PHASE_MATCH`** | `0x017550` | — | `scsi_mgr.s:702` | SCSI_WAIT_PHASE_MATCH - wait for REQ (despite the label: no phase test) Polls sCSR bit 5 (REQ) until set or D1 timeout; phase match (sBSR bit 3) is tested separately by SCSI_VERIFY_PHASE Returns D0=0 ... |
| **`SCSI_WAIT_REQ`** | — | `0x01A8BC` | `scsi_mgr.s:990` | SCSI_WAIT_REQ - wait for target REQ (sBSR bit 5) to assert Output: D0 = 0 (REQ seen) or 2 (timeout) Called by: SCSI_SEND_CDB, SCSI_CDB_LOOP, SCSI_READ_STATUS, SCSI_READ_MSGIN, SCSI_SEND_MSGOUT (and 1 ... |
| **`SCSI_WAIT_REQ_CLEAR`** | `0x01753A` | — | `scsi_mgr.s:685` | SCSI_WAIT_REQ_CLEAR - wait for REQ deasserted (handshake complete) Polls sCSR bit 5 (REQ) until clear or D1 timeout Returns D0=0 on success, D0=2 (scCommErr) on timeout |
| **`SCSI_WAIT_REQ_DONE`** | — | `0x01A8DC` | `scsi_mgr.s:1003` | — |
| **`SCSI_WAIT_REQ_DROP`** | — | `0x01A898` | `scsi_mgr.s:970` | SCSI_WAIT_REQ_DROP - wait for target REQ (sBSR bit 5) to drop Output: D0 = 0 (drop seen) or 2 (timeout) Called by: SCSI_CDB_LOOP, SCSI_READ_STATUS, SCSI_READ_MSGIN, SCSI_SEND_MSGOUT, SCSI_BAD_PHASE_HA... |
| **`SCSI_WAIT_REQ_DROP_DONE`** | — | `0x01A8B8` | `scsi_mgr.s:983` | — |
| **`SCSI_WAIT_REQ_DROP_LOOP`** | — | `0x01A8A6` | `scsi_mgr.s:977` | — |
| **`SCSI_WAIT_REQ_LOOP`** | — | `0x01A8CA` | `scsi_mgr.s:997` | — |
| **`SCSI_WR_FINAL_DRQ`** | `0x01744E` | — | `scsi_mgr.s:556` | SCSI_WR_FINAL_DRQ - after write: wait for final DRQ (last byte accepted by 5380) |
| **`SCSI_XFER_BLIND`** | — | `0x01A5E2` | `scsi_mgr.s:605` | — |
| **`SCSI_XFER_BLIND_R`** | — | `0x01A5FA` | `scsi_mgr.s:616` | — |
| **`SCSI_XFER_BLIND_W`** | — | `0x01A5FE` | `scsi_mgr.s:619` | — |
| **`SCSI_XFER_BLIND_WAIT`** | — | `0x01A5EA` | `scsi_mgr.s:608` | — |
| **`SCSI_XFER_C_LOOP`** | — | `0x01A582` | `scsi_mgr.s:563` | — |
| **`SCSI_XFER_C_NEXT`** | — | `0x01A590` | `scsi_mgr.s:570` | — |
| **`SCSI_XFER_C_PHCHK`** | — | `0x01A59C` | `scsi_mgr.s:574` | — |
| **`SCSI_XFER_CLR`** | — | `0x01A61A` | `scsi_mgr.s:632` | Bus-error trampoline target re-enters here too. Called by: SCSI_XFER_DRAIN_LOOP, SCSI_BUSERR_HANDLER, SCSI_XFER_W_PHCHK |
| **`SCSI_XFER_DISPATCH`** | — | `0x01A566` | `scsi_mgr.s:549` | — |
| **`SCSI_XFER_DONE`** | — | `0x01A62E` | `scsi_mgr.s:641` | — |
| **`SCSI_XFER_DRAIN`** | — | `0x01A602` | `scsi_mgr.s:621` | — |
| **`SCSI_XFER_DRAIN_LOOP`** | — | `0x01A606` | `scsi_mgr.s:623` | — |
| **`SCSI_XFER_ENGINE`** | `0x01739C` | `0x01A51C` | `scsi_mgr.s:447`<br>`scsi_mgr.s:524` | SCSI_XFER_ENGINE - SCSI data transfer engine (used by scInc, scNoInc, scComp) A2 -> buffer, D2 = byte count D4 flags: bit 15 = blind mode, byte = 0xFF write, byte = 0x01 compare, byte = 0 read Both mo... |
| **`SCSI_XFER_EXIT_DMA`** | `0x017454` | — | `scsi_mgr.s:560` | SCSI_XFER_EXIT_DMA - transfer complete: exit DMA mode |
| **`SCSI_XFER_MODE_SEL`** | `0x0173DC` | — | `scsi_mgr.s:474` | SCSI_XFER_MODE_SEL - select polled vs blind transfer, then dispatch by direction Pseudo-DMA: access NCR 5380 at base+$200 for handshake-free byte I/O |
| **`SCSI_XFER_PHASE_CHK`** | — | `0x01A558` | `scsi_mgr.s:544` | — |
| **`SCSI_XFER_R_LOOP`** | — | `0x01A5A6` | `scsi_mgr.s:578` | — |
| **`SCSI_XFER_R_NEXT`** | — | `0x01A5AE` | `scsi_mgr.s:582` | — |
| **`SCSI_XFER_R_PHCHK`** | — | `0x01A5B8` | `scsi_mgr.s:586` | — |
| **`SCSI_XFER_R_PHERR`** | — | `0x01A5C0` | `scsi_mgr.s:589` | — |
| **`SCSI_XFER_RESTORE`** | — | `0x01A622` | `scsi_mgr.s:637` | Common exit: restore bus-error vector + saved regs, return D0 Called by: SCSI_XFER_PHASE_CHK, SCSI_XFER_C_NEXT, SCSI_XFER_R_NEXT, SCSI_XFER_R_PHERR, SCSI_XFER_BLIND_WAIT (and 1 more) |
| **`SCSI_XFER_RETURN`** | `0x01745C` | — | `scsi_mgr.s:563` | SCSI_XFER_EXIT_DMA - transfer complete: exit DMA mode |
| **`SCSI_XFER_RW_DEC`** | — | `0x01A57A` | `scsi_mgr.s:559` | — |
| **`SCSI_XFER_SET_TCR`** | `0x0173A8` | — | `scsi_mgr.s:453` | — |
| **`SCSI_XFER_W_LOOP`** | — | `0x01A5C4` | `scsi_mgr.s:592` | — |
| **`SCSI_XFER_W_NEXT`** | — | `0x01A5CC` | `scsi_mgr.s:596` | — |
| **`SCSI_XFER_W_PHCHK`** | — | `0x01A5D6` | `scsi_mgr.s:600` | — |
| **`SCSI_XFER_WAIT_REQ`** | — | `0x01A54A` | `scsi_mgr.s:539` | — |
| **`SCSI_XFER_WR_SETUP`** | `0x0173D2` | — | `scsi_mgr.s:469` | Read/compare setup: start DMA receive SCSI_XFER_WR_SETUP - write mode DMA setup |
| **`SCSI_XFER_WRITE_WAIT`** | — | `0x01A53C` | `scsi_mgr.s:534` | — |
| **`SCSIBOOTS`** | — | `0x00404C` | `scsi_boot.s:23` | SCSI boot support -- SCSILOAD Apple source: SCSIBoot.a (MacSEROM.lst module SCSIBOOTS). Called while the system starts up: probes the SCSI IDs, reads each device's driver descriptor map and partition ... |
| **`SCSICmd`** | `0x0171AE` | — | `scsi_mgr.s:174` | SCSICmd - send a SCSI command descriptor block to target Params: 0xA(A6) = pointer to CDB, 8(A6) = CDB length |
| **`SCSIComplete`** | `0x017256` | — | `scsi_mgr.s:298` | SCSIComplete - complete SCSI transaction: read status + message bytes Params: 8(A6) = timeout (ticks), 0xC(A6) = ptr to message word, 0x10(A6) = ptr to status word Waits for target to enter status pha... |
| **`SCSIDispatch`** | `0x01712C` | — | `scsi_mgr.s:58` | SCSI Manager Implements the SCSI Manager trap (_SCSIDispatch $A815) for the Mac Plus NCR 5380 SCSI controller at SCSI_Base (0x580000). Public routines (sub-selectors of _SCSIDispatch): SCSIReset - res... |
| **`SCSIGet`** | `0x01718A` | — | `scsi_mgr.s:153` | SCSIGet - arbitrate for the SCSI bus Calls SCSI_ARBITRATE to perform NCR 5380 arbitration sequence Result in D0: 0=won arbitration, 2=lost/timeout |
| **`SCSIInstall`** | `0x017168` | — | `scsi_mgr.s:127` | SCSIInstall - install SCSI interrupt handler Mac Plus has no SCSI interrupt wired, so this is a no-op stub |
| **`SCSILOAD`** | — | `0x00404C` | `scsi_boot.s:24` | SCSI boot support -- SCSILOAD Apple source: SCSIBoot.a (MacSEROM.lst module SCSIBOOTS). Called while the system starts up: probes the SCSI IDs, reads each device's driver descriptor map and partition ... |
| **`SCSIMGR`** | — | `0x01A206` | `scsi_mgr.s:118` | _SCSIDispatch ($A815) trap entry - SE FDHD SCSI Manager Stack on entry: ... params ... selectorWord(W) returnAddr(L) 24 selectors total (vs 11 on Plus); SE adds SelAtn/MsgIn/MsgOut and reserves 14..23... |
| **`SCSIProbeDevice`** | `0x007D62` | — | `scsi_boot.s:64` | SCSIProbeDevice Called during boot. |
| **`SCSIRead`** | `0x0171C8` | — | `scsi_mgr.s:187` | SCSIRead - read data from target using TIB instructions Also handles SCSIRBlind (selector 8) when D1 >= 8 Param: 8(A6) = pointer to TIB array |
| **`SCSIReadBlocks`** | `0x007DCC` | `0x0041D4` | `scsi_boot.s:118` | SCSIReadBlocks Called during boot. |
| **`SCSIREADBLOCKS`** | `0x007DCC` | `0x0041D4` | `scsi_boot.s:224` | SCSIREADBLOCKS -- read N blocks from a SCSI device D2 = block count, D3 = starting LBA, D4 = block size (bytes), D5 = SCSI ID, A2 -> destination buffer. Builds a 6-byte READ(6) command in (scratch8) a... |
| **`SCSIREADBLOCKS_RETRY`** | — | `0x0041D8` | `scsi_boot.s:233` | SCSIREADBLOCKS_RETRY -- build and send the READ(6) command; entered again once after a unit attention (CHECK CONDITION) Called during boot. |
| **`SCSIReset`** | `0x01717C` | — | `scsi_mgr.s:142` | SCSIReset - assert RST on SCSI bus for >25 usec, then release |
| **`SCSISelect`** | `0x017198` | — | `scsi_mgr.s:163` | SCSISelect - select a SCSI target device Param: 8(A6) = target SCSI ID (0-6) Result: 0xA(A6) = result code from selection |
| **`SCSIStat`** | `0x01716A` | — | `scsi_mgr.s:134` | SCSIStat - reads sBSR and sCSR but stores them at 8(SP)/9(SP): after SCSI_PROLOGUE (LINK + MOVEM.L of 9 regs) those are the high word of the saved D4 (restored by SCSI_EPILOGUE); the result at 8(A6) i... |
| **`SCSISTUFF`** | — | `0x01A19C` | `scsi_mgr.s:70` | SCSI Manager Apple sources: SCSIMgrInit.a and SCSIMgr.a (MacSEROM.lst module SCSISTUFF): INITSCSIMGR and the SCSI Manager trap (_SCSIDispatch $A815) for the NCR 5380 SCSI controller. Public routines (... |
| **`SCSIWrite`** | `0x01724C` | — | `scsi_mgr.s:287` | SCSIWrite - write data to target using TIB instructions Also handles SCSIWBlind (selector 9) via same blind mode flag Param: 8(A6) = pointer to TIB array |
| **`SearchNode`** | `0x0075EA` | `0x00913E` | `file_mgr_btree.s:2135` | SearchNode -- binary search within node. Search Node |
| **`SEARCHNODE`** | `0x0075EA` | `0x00913E` | `file_mgr_btree.s:1853` | SearchNode: binary search within a B-tree node Input: A0=search key, A1=node buffer Returns: D0=0 if found, D0=BTnotfound if not; D1=record index |
| **`Secs2Date`** | `0x017052` | `0x01A0C2` | `date_utils.s:25` | **Regs:** `Entry: D0.L = seconds since epoch Exit: DateTimeRec filled with year/month/day/hour/min/sec/dayOfWeek`<br>Date conversion -- _Secs2Date / _Date2Secs Apple source: SexyDate.a (MacSEROM.lst module SEXYDATE). Convert between the clock's seconds since midnight, January 1, 1904 and a DateTimeRec (year, month, ... |
| **`SECS2DATE`** | `0x017052` | `0x01A0C2` | `date_utils.s:24` | Date conversion -- _Secs2Date / _Date2Secs Apple source: SexyDate.a (MacSEROM.lst module SEXYDATE). Convert between the clock's seconds since midnight, January 1, 1904 and a DateTimeRec (year, month, ... |
| **`SEEK`** | `0x004ECE` | `0x006970` | `file_mgr_dir.s:2055`<br>`file_mgr_dir.s:1856` | SEEK Called during boot. Seek: position within file, set up D5=cur pos, D7=IOReqCount |
| **`SegStack`** | `0x00F67A` | — | `segment_loader.s:307` | Seg Stack SegStack: set up application memory layout from CODE 0 header CODE 0 format: [aboveA5 size, belowA5 size, JT length, JT offset] Called during boot. |
| **`SET_DEFAULT_RECT`** | `0x001356` | `0x001566` | `sys_error.s:364`<br>`sys_error.s:322` | SET_DEFAULT_RECT - set default DS alert rect and draw frame Default rect: top=64, left=32, bottom=190, right=480 |
| **`SET_TRAP_OLD`** | `0x001FE0` | `0x002D64` | `trap_dispatch.s:113`<br>`trap_dispatch.s:106` | Old-style SetTrapAddress (bit 9 = 0) Auto-detects OS vs Toolbox via DETECT_TRAP_TABLE heuristic, then stores address. |
| **`SET_TRAP_STORE`** | `0x001FD6` | `0x002D5A` | `trap_dispatch.s:102`<br>`trap_dispatch.s:100` | — |
| **`SETADBINFO`** | — | `0x003D3E` | `adb_mgr.s:1162` | **Regs:** `Entry: D0 = ADB address, A0 = ADBSetInfoBlock (+0=handler, +4=data)`<br>SETADBINFO - _SetADBInfo trap: set device handler and data Entry: D0 = ADB address, A0 = ADBSetInfoBlock (+0=handler, +4=data) Sets the device's service routine and data area pointers. |
| **`SetAppBase`** | `0x00FE76` | — | `memory_mgr.s:67` | **Proto:** `Pascal: PROCEDURE SetApplBase(startPtr: Ptr);`<br>**Regs:** `Entry: A0 = startPtr Exit:  D0.W = noErr, MemErr cleared`<br>Memory Manager Manages heap zones for dynamic memory allocation. Provides NewHandle, NewPtr, DisposeHandle, DisposePtr, SetHandleSize, CompactMem, PurgeMem, and other routines. Zone record (Inside Mac... |
| **`SETAPPBASE_CONT`** | `0x00FE92` | `0x00A378` | `memory_mgr.s:91`<br>`memory_mgr.s:65` | **Regs:** `Sets ApplZone and HeapEnd. Exit: D0 = 0, MemErr cleared.`<br>SETAPPBASE_CONT - (re)initialize the application heap zone Calls _RsrcZoneInit, sets ApplLimit = HighHeapMark = BufPtr - DefltStack (ToMaxLimit's D2) and runs _InitZone for a zone that starts right af... |
| **`SETAPPBASE_OK`** | `0x00FEBC` | `0x00A3A2` | `memory_mgr.s:106`<br>`memory_mgr.s:80` | — |
| **`SETAPPBASE_SKIP`** | `0x00FE8A` | `0x00A370` | `memory_mgr.s:74`<br>`memory_mgr.s:61` | — |
| **`SETAPPLBASE`** | — | `0x00A352` | `memory_mgr.s:50` | Memory Manager Apple sources: MemoryMgr.a and MemoryMgrInternal.a (MacSEROM.lst modules HEAP, HEAPGUTS) and BlockMove.a (module BLOCK2). Manages heap zones for dynamic memory allocation. Provides NewH... |
| **`SetApplLimit`** | `0x01007A` | `0x00A58A` | `memory_mgr.s:437` | _SetApplLimit ($A02D) A0 = limit -> (sets application heap limit) Called during boot. |
| **`SETAPPLLIMIT`** | `0x01007A` | `0x00A58A` | `memory_mgr.s:282` | — |
| **`SETAPPLLIMIT_EXIT`** | `0x010096` | `0x00A5A6` | `memory_mgr.s:448`<br>`memory_mgr.s:293` | — |
| **`SETAPPLLIMIT_EXIT_2`** | `0x010098` | `0x00A5A8` | `memory_mgr.s:450`<br>`memory_mgr.s:295` | — |
| **`SETCATINFO`** | — | `0x0063AE` | `file_mgr_dir.s:1141` | copy Finder info and dates from param block to catalog _SetCatInfo: set catalog info (HFS extended) |
| **`SetDateTime`** | `0x00F7D4` | `0x009C1E` | `os_utilities.s:85` | _SetDateTime ($A03A) _SetDateTime ($A03A): set date/time in RTC |
| **`SETDATETIME`** | `0x00F7D4` | `0x009C1E` | `os_utilities.s:63` | — |
| **`SETDIR`** | — | `0x0055A6` | `file_mgr_vol.s:1824` | _HSetVol with ioDirFlg: set default working directory |
| **`SetDir_hfs3`** | `0x003B1A` | — | `file_mgr_vol.s:1990` | Set Dir_hfs3 _SetVol (HFS SetDir): set default directory by pathname |
| **`SETDIR_HFS3_CONT`** | `0x003B3E` | `0x0055CA` | `file_mgr_vol.s:2010`<br>`file_mgr_vol.s:1843` | — |
| **`SETDIR_HFS3_ERR`** | `0x003B4A` | — | `file_mgr_vol.s:2015` | — |
| **`SETDIR_HFS3_FOUND`** | `0x003B32` | `0x0055BE` | `file_mgr_vol.s:2005`<br>`file_mgr_vol.s:1838` | SETDIR_HFS3_FOUND |
| **`SetEOF`** | `0x0054C0` | `0x006F78` | `file_mgr_io.s:849` | _SetEOF ($A012) Called during boot. _SetEOF ($A012) |
| **`SETEOF`** | `0x0054C0` | `0x006F78` | `file_mgr_io.s:727` | — |
| **`SETEOF_CONT`** | `0x0054FC` | — | `file_mgr_io.s:875` | shrtnFil: shorten the file |
| **`SETEOF_CONT_2`** | `0x005512` | `0x006FC4` | `file_mgr_io.s:884`<br>`file_mgr_io.s:759` | truncate the file space beyond the new PEOF |
| **`SETEOF_CONT_3`** | `0x005528` | `0x006FDA` | `file_mgr_io.s:893`<br>`file_mgr_io.s:767` | lngthnFil: lengthen the file |
| **`SETEOF_DONE`** | — | `0x006FAE` | `file_mgr_io.s:749` | — |
| **`SETEOF_EXIT`** | `0x0054F8` | — | `file_mgr_io.s:872` | — |
| **`SETEOF_NO`** | `0x0054E4` | `0x006F9C` | `file_mgr_io.s:864`<br>`file_mgr_io.s:741` | — |
| **`SETEOF_OK`** | `0x0054D8` | — | `file_mgr_io.s:859` | SEOFOK: same length or file adjusted |
| **`SETEOF_OK_2`** | `0x0054F2` | — | `file_mgr_io.s:869` | — |
| **`SETEOF_PIN_POSITION`** | — | `0x006FAA` | `file_mgr_io.s:746` | — |
| **`SETEOF_SHRINK`** | — | `0x006F90` | `file_mgr_io.s:736` | — |
| **`SETFCBINFO_DONE`** | — | `0x006EBA` | `file_mgr_io.s:642` | — |
| **`SetFileInfo`** | `0x0048D6` | `0x00637C` | `file_mgr_dir.s:1255` | _SetFileInfo ($A00D) _SetFileInfo ($A00D) |
| **`SETFILEINFO`** | `0x0048D6` | `0x00637C` | `file_mgr_dir.s:1126` | _SetFileInfo ($A00D): set file info from param block |
| **`SETFILEINFO_MFS_FLUSH`** | — | `0x006826` | `file_mgr_dir.s:1657` | MFS SetFileInfo/SetFilLock: mark dirty and flush |
| **`SETFILEINFO_MFS_NEXT_BLOCK`** | — | `0x0068A6` | `file_mgr_dir.s:1731` | — |
| **`SETFILEINFO_NEXT_FCB_RTS`** | — | `0x0062F6` | `file_mgr_dir.s:1068` | — |
| **`SetFilLock`** | `0x00488A` | `0x006330` | `file_mgr_dir.s:1206` | SetFilLock -- trap handler for _SetFilLock ($A041). _SetFilLock ($A041) |
| **`SETFILLOCK`** | `0x00488A` | `0x006330` | `file_mgr_dir.s:1092` | _SetFilLock ($A041): lock a file |
| **`SETFILLOCK_DONE`** | — | `0x006378` | `file_mgr_dir.s:1123` | Called by: SETFILTYPE_NO, SETFILTYPE_OK, SETFILLOCK_HFS_PATH, RSTFILLOCK_CONT_3, SETFILEINFO |
| **`SETFILLOCK_HFS_PATH`** | — | `0x006342` | `file_mgr_dir.s:1101` | SetFilLock/RstFilLock: HFS path |
| **`SetFilType`** | `0x004852` | `0x0062F8` | `file_mgr_dir.s:1184` | _SetFilType ($A043) _SetFilType: set file type (MFS-only trap, fails on HFS) |
| **`SETFILTYPE`** | `0x004852` | `0x0062F8` | `file_mgr_dir.s:1071` | _SetFilType ($A043): set MFS file type (fails on HFS) |
| **`SETFILTYPE_NO`** | `0x004874` | `0x00631A` | `file_mgr_dir.s:1195`<br>`file_mgr_dir.s:1082` | — |
| **`SETFILTYPE_OK`** | `0x004886` | `0x00632C` | `file_mgr_dir.s:1201`<br>`file_mgr_dir.s:1088` | — |
| **`SETFLOCK_RTS`** | — | `0x006F2E` | `file_mgr_io.s:696` | — |
| **`SetFPos`** | `0x004F14` | `0x0069B6` | `file_mgr_io.s:21` | **Proto:** `SetFPos -- _SetFPos ($A044): FUNCTION SetFPos (refNum: INTEGER; posMode: INTEGER; posOff:`<br>SetFPos -- _SetFPos ($A044): FUNCTION SetFPos (refNum: INTEGER; posMode: INTEGER; posOff: |
| **`SETFPOS`** | `0x004F14` | `0x0069B6` | `file_mgr_io.s:17` | _SetFPos ($A044): set file position (Seek with count=0) |
| **`SetGrowZone`** | `0x010070` | `0x00A580` | `memory_mgr.s:426` | _SetGrowZone ($A04B) A0 = proc -> (installs grow-zone function) Called during boot. |
| **`SETGROWZONE`** | `0x010070` | `0x00A580` | `memory_mgr.s:278` | — |
| **`SetHandleSize`** | `0x01019C` | `0x00A6B4` | `memory_mgr.s:751` | **Proto:** `Pascal: PROCEDURE SetHandleSize(h: Handle; newSize: Size);`<br>**Regs:** `Entry: A0 = h, D0.L = newSize Exit:  D0.W = noErr, memFullErr, memROZErr (cannot shrink a block in a`<br>_SetHandleSize ($A024): change the logical size of a relocatable block Pascal: PROCEDURE SetHandleSize(h: Handle; newSize: Size); Entry: A0 = h, D0.L = newSize Exit:  D0.W = noErr, memFullErr, memROZE... |
| **`SETHANDLESIZE`** | `0x01019C` | `0x00A6B4` | `memory_mgr.s:437` | SetHandleSize: do the resize |
| **`SETHANDLESIZE_DO`** | `0x0101A6` | `0x00A6BE` | `memory_mgr.s:762`<br>`memory_mgr.s:443` | SETHANDLESIZE_DO - SetHandleSize: block present, resize it |
| **`SETHANDLESIZE_EMPTY`** | `0x0101A2` | `0x00A6BA` | `memory_mgr.s:754`<br>`memory_mgr.s:440` | — |
| **`SETHANDLESIZE_ERR`** | `0x0101AA` | `0x00A6C2` | `memory_mgr.s:764`<br>`memory_mgr.s:446` | Called by: GETHANDLESIZE, SETHANDLESIZE_EMPTY, EMPTYHANDLE_EXIT, REALLOCHANDLE, REALLOCHANDLE_OK (and 2 more) |
| **`SetPtrSize`** | `0x010112` | `0x00A62A` | `memory_mgr.s:574` | _SetPtrSize ($A020) A0 = ptr, D0.L = newSize -> D0 = error Called during boot. |
| **`SETPTRSIZE`** | `0x010112` | `0x00A62A` | `memory_mgr.s:357` | — |
| **`SetSize`** | `0x010902` | `0x00AEC0` | `memory_mgr.s:2262` | **Regs:** `Entry: A0 = data pointer, A1 = handle (nil for a nonrelocatable block), Exit:  D0 = noErr, memFullErr, or memROZErr (would shrink a block in a`<br>SetSize - change the logical size of a block (SetPtrSize, SetHandleSize) Entry: A0 = data pointer, A1 = handle (nil for a nonrelocatable block), D0.L = new logical size, A6 = zone Exit:  D0 = noErr, m... |
| **`SETSIZE`** | `0x010902` | `0x00AEC0` | `memory_mgr.s:1625` | — |
| **`SETSIZE_CONT`** | `0x01093E` | `0x00AEFC` | `memory_mgr.s:2286`<br>`memory_mgr.s:1649` | — |
| **`SETSIZE_CONT_2`** | `0x010962` | `0x00AF20` | `memory_mgr.s:2308`<br>`memory_mgr.s:1670` | — |
| **`SETSIZE_CONT_3`** | `0x010A2C` | `0x00AFEA` | `memory_mgr.s:2433`<br>`memory_mgr.s:1791` | SETSIZE_CONT_3 Called during boot (7,436 times in 30s trace). |
| **`SETSIZE_CONT_4`** | `0x010A42` | `0x00B000` | `memory_mgr.s:2444`<br>`memory_mgr.s:1802` | — |
| **`SETSIZE_EMPTY`** | `0x0109F2` | `0x00AFB0` | `memory_mgr.s:2397`<br>`memory_mgr.s:1757` | Called by: SETSIZE_OK, SETSIZE_SKIP_2, SETSIZE_NO_3 |
| **`SETSIZE_EMPTY_2`** | `0x010A24` | `0x00AFE2` | `memory_mgr.s:2423`<br>`memory_mgr.s:1782` | SETSIZE_EMPTY_2 |
| **`SETSIZE_ERR`** | `0x010A70` | `0x00B02E` | `memory_mgr.s:2464`<br>`memory_mgr.s:1822` | — |
| **`SETSIZE_ERR_2`** | `0x010A78` | `0x00B036` | `memory_mgr.s:2473`<br>`memory_mgr.s:1830` | SETSIZE_ERR_2 |
| **`SETSIZE_NO`** | `0x0109A0` | `0x00AF5E` | `memory_mgr.s:2353`<br>`memory_mgr.s:1713` | — |
| **`SETSIZE_NO_2`** | `0x0109B0` | `0x00AF6E` | `memory_mgr.s:2362`<br>`memory_mgr.s:1722` | — |
| **`SETSIZE_NO_3`** | `0x0109E0` | `0x00AF9E` | `memory_mgr.s:2388`<br>`memory_mgr.s:1747` | SETSIZE_NO_3 Called during boot. |
| **`SETSIZE_NO_4`** | `0x010A0A` | `0x00AFC8` | `memory_mgr.s:2407`<br>`memory_mgr.s:1767` | — |
| **`SETSIZE_NO_5`** | `0x010A66` | `0x00B024` | `memory_mgr.s:2458`<br>`memory_mgr.s:1816` | — |
| **`SETSIZE_OK`** | `0x01094C` | `0x00AF0A` | `memory_mgr.s:2300`<br>`memory_mgr.s:1662` | SETSIZE_OK Called during boot (7,440 times in 30s trace). |
| **`SETSIZE_OK_2`** | `0x010976` | `0x00AF34` | `memory_mgr.s:2324`<br>`memory_mgr.s:1685` | SETSIZE_OK_2 Called during boot. |
| **`SETSIZE_OK_3`** | `0x01097A` | `0x00AF38` | `memory_mgr.s:2327`<br>`memory_mgr.s:1688` | — |
| **`SETSIZE_OK_4`** | `0x010990` | `0x00AF4E` | `memory_mgr.s:2344`<br>`memory_mgr.s:1704` | SETSIZE_OK_4 Called during boot. |
| **`SETSIZE_OK_5`** | `0x010A6E` | `0x00B02C` | `memory_mgr.s:2462`<br>`memory_mgr.s:1820` | — |
| **`SETSIZE_SKIP`** | `0x010984` | `0x00AF42` | `memory_mgr.s:2331`<br>`memory_mgr.s:1692` | — |
| **`SETSIZE_SKIP_2`** | `0x0109C4` | `0x00AF82` | `memory_mgr.s:2370`<br>`memory_mgr.s:1730` | — |
| **`SetTrapAddress`** | `0x001FBA` | `0x002D3E` | `trap_dispatch.s:93` | _SetTrapAddress ($A047) - NSetTrapAddress On entry: A0 = new handler address, D0 = trap word, D1 = trap word Bit 9 of D1: 1 = "new" interface (bit 10 selects OS vs Toolbox) 0 = "old" interface (auto-d... |
| **`SETTRAPADDRESS`** | `0x001FBA` | `0x002D3E` | `trap_dispatch.s:91` | **Regs:** `Entry: D0 = trap number, A0 = new handler address`<br>SETTRAPADDRESS - _SetTrapAddress trap handler Sets the dispatch table entry for trap D0 to address A0. D1 bit 9: new-style (explicit OS/Toolbox select) D1 bit 10: 1 = Toolbox table, 0 = OS table Entry... |
| **`SETUPFCB`** | `0x00410E` | `0x005BA8` | `file_mgr_dir.s:165`<br>`file_mgr_dir.s:148` | SetupFCB: fill in the FCB fields |
| **`SetUpTags`** | `0x007CF2` | — | `file_mgr_cache.s:989` | Set Up Tags Called during boot. |
| **`SETUPTAGS_DATE`** | — | `0x009868` | `file_mgr_cache.s:808` | — |
| **`SetVCBDirty`** | `0x002D28` | `0x004770` | `file_mgr_vol.s:288`<br>`file_mgr_vol.s:251` | SetVCBDirty - set VCB dirty flag |
| **`SetVol`** | `0x003ADA` | `0x005566` | `file_mgr_vol.s:1958` | _SetVol ($A015) Called during boot. |
| **`SETVOL`** | `0x003ADA` | `0x005566` | `file_mgr_vol.s:1797` | _SetVol / _HSetVol: set current default volume |
| **`SETVOL_DEFAULT_WDCB_DONE`** | — | `0x0055A2` | `file_mgr_vol.s:1821` | — |
| **`SETVOL_ERR`** | `0x003B16` | — | `file_mgr_vol.s:1982` | — |
| **`SETVOL_NO`** | `0x003B10` | `0x00559C` | `file_mgr_vol.s:1979`<br>`file_mgr_vol.s:1818` | — |
| **`SETVOL_OK`** | `0x003AFE` | `0x00558A` | `file_mgr_vol.s:1971`<br>`file_mgr_vol.s:1810` | — |
| **`SETVOL_PMSP_FLAG_SET`** | — | `0x0052AC` | `file_mgr_vol.s:1501` | — |
| **`SETVOL_SKIP`** | `0x003B02` | `0x00558E` | `file_mgr_vol.s:1973`<br>`file_mgr_vol.s:1812` | — |
| **`SETVOLINFO`** | — | `0x00545A` | `file_mgr_vol.s:1670` | _SetVolInfo / PBSetVInfo: set volume information |
| **`SETVOLINFO_DONE`** | — | `0x0054CA` | `file_mgr_vol.s:1707` | — |
| **`SetVolInfo_hfs`** | `0x0039CE` | — | `file_mgr_vol.s:1813` | Set Vol Info_hfs _SetVolInfo (HFS): set volume info from param block |
| **`SETVOLINFO_HFS_CONT`** | `0x003A42` | `0x0054CE` | `file_mgr_vol.s:1860`<br>`file_mgr_vol.s:1716` | SETVOLINFO_HFS_CONT -- update VCB volume name. SETVOLINFO_HFS_CONT |
| **`SETVOLINFO_HFS_CONT_2`** | `0x003A4C` | `0x0054D8` | `file_mgr_vol.s:1864`<br>`file_mgr_vol.s:1720` | — |
| **`SETVOLINFO_HFS_CONT_3`** | `0x003A76` | `0x005502` | `file_mgr_vol.s:1892`<br>`file_mgr_vol.s:1743` | SETVOLINFO_HFS_CONT_3: check volume write protect status Called during boot. |
| **`SETVOLINFO_HFS_ERR`** | `0x003A3E` | — | `file_mgr_vol.s:1852` | — |
| **`SETVOLINFO_HFS_NO`** | `0x003A2E` | `0x0054BA` | `file_mgr_vol.s:1844`<br>`file_mgr_vol.s:1699` | copy volume dates and attributes from param block copy TFS-specific fields copy Finder info (32 bytes) update volume name if specified |
| **`SETVOLINFO_HFS_NO_2`** | `0x003A38` | — | `file_mgr_vol.s:1849` | — |
| **`SETVOLINFO_HFS_OK`** | `0x003A68` | `0x0054F4` | `file_mgr_vol.s:1880`<br>`file_mgr_vol.s:1730` | SETVOLINFO_HFS_OK finish name copy: set length byte and mark VCB dirty |
| **`SETVOLINFO_HFS_OK_2`** | `0x003A88` | `0x005514` | `file_mgr_vol.s:1900`<br>`file_mgr_vol.s:1751` | SETVOLINFO_HFS_CONT_3: check volume write protect status check volume write-protect status Returns D0=0 if writable, error code if locked Called during boot. |
| **`SETVOLINFO_RENAME_DONE`** | — | `0x0054C4` | `file_mgr_vol.s:1704` | — |
| **`SetZone`** | `0x00FFAA` | `0x00A4BA` | `memory_mgr.s:246` | **Proto:** `Pascal: PROCEDURE SetZone(hz: THz);`<br>**Regs:** `Entry: A0 = hz (stored in TheZone without any check) Exit:  D0.W = noErr, MemErr cleared (INITZONE_EXIT)`<br>_SetZone ($A01B): make hz the current heap zone Pascal: PROCEDURE SetZone(hz: THz); Entry: A0 = hz (stored in TheZone without any check) Exit:  D0.W = noErr, MemErr cleared (INITZONE_EXIT) Toolbox tra... |
| **`SETZONE`** | `0x00FFAA` | `0x00A4BA` | `memory_mgr.s:192` | — |
| **`SEXYDATE`** | — | `0x01A0C2` | `date_utils.s:23` | Date conversion -- _Secs2Date / _Date2Secs Apple source: SexyDate.a (MacSEROM.lst module SEXYDATE). Convert between the clock's seconds since midnight, January 1, 1904 and a DateTimeRec (year, month, ... |
| **`SGLDREND`** | — | `0x009BD8` | `os_utilities.s:20` | Operating System Utilities Apple source: SysUtil.a (MacSEROM.lst module SYSUTIL). In ROM order: ASYNCPATCH                 - (an RTS: patch point) ReadParam, WriteParam      - parameter RAM: low-memor... |
| **`SHOW_ALERT_BTNS`** | `0x0013A4` | `0x0015B4` | `sys_error.s:414`<br>`sys_error.s:374` | SHOW_ALERT_BTNS - display DS alert buttons and wait for mouse click Looks up button definition in alert table, draws rounded-rect buttons with labels, then waits for mouse click on a button. Returns Z... |
| **`SplitLT`** | `0x00715C` | `0x008CB8` | `file_mgr_btree.s:1446` | SplitLT -- split left. Split LT |
| **`SPLITLT`** | `0x00715C` | `0x008CB8` | `file_mgr_btree.s:1300` | — |
| **`SPLITLT_DONE`** | `0x0071D6` | `0x008D34` | `file_mgr_btree.s:1496`<br>`file_mgr_btree.s:1345` | SLExit |
| **`SPLITLT_DOROTATE`** | — | `0x008D26` | `file_mgr_btree.s:1338` | — |
| **`SPLITLT_EXIT`** | `0x0071DA` | `0x008D38` | `file_mgr_btree.s:1499`<br>`file_mgr_btree.s:1348` | — |
| **`SPLITLT_INIT`** | `0x00718E` | `0x008CEA` | `file_mgr_btree.s:1470`<br>`file_mgr_btree.s:1320` | set up some common stuff allocate a new disk node update forward link in original left node and release it SLInit: initialize a new left node |
| **`SPLITLT_ROTATE`** | `0x0071C8` | — | `file_mgr_btree.s:1488` | SLRotate: insert new record via rotate left |
| **`SRCHNODE_EQ`** | `0x00762C` | `0x009180` | `file_mgr_btree.s:2171`<br>`file_mgr_btree.s:1887` | SrchLT: search key < trial key SrchEQ |
| **`SRCHNODE_EXIT`** | `0x00763C` | `0x009190` | `file_mgr_btree.s:2190`<br>`file_mgr_btree.s:1904` | SrchRet |
| **`SRCHNODE_GT`** | `0x007630` | `0x009184` | `file_mgr_btree.s:2180`<br>`file_mgr_btree.s:1895` | SRCHNODE_GT SrchGT: search key > trial key |
| **`SRCHNODE_LOOP`** | `0x007602` | `0x009156` | `file_mgr_btree.s:2148`<br>`file_mgr_btree.s:1864` | set up some common stuff search node for key using a binary search SrchLoop |
| **`SRCHNODE_NOTFND`** | `0x007638` | `0x00918C` | `file_mgr_btree.s:2186`<br>`file_mgr_btree.s:1901` | SrchExit |
| **`StackSpace`** | `0x01009E` | `0x00A5AE` | `memory_mgr.s:459` | _StackSpace ($A065) -> D0.L = bytes between SP and heap end |
| **`STACKSPACE`** | `0x01009E` | `0x00A5AE` | `memory_mgr.s:298` | — |
| **`START_HEAD_IOPARAM`** | `0x00211E` | `0x002EAA` | `device_mgr.s:242`<br>`device_mgr.s:221` | — |
| **`START_HEAD_REQ`** | `0x002118` | `0x002EA4` | `device_mgr.s:239`<br>`device_mgr.s:218` | START_HEAD_REQ - Start processing the head I/O request Driver was not busy. Determine which driver entry point to call based on the ioTrap field of the IOParam block: _Control (4), _Status (5), or _Re... |
| **`Stash`** | `0x00207A` | `0x002DFE` | `device_mgr.s:127` | Stash - write a byte to the driver's I/O buffer Called via JStash vector ($08F8). Writes byte in D0.B to the active I/O request's buffer. A1 = DCE pointer. Bit 15 of D0 set on return if buffer is full... |
| **`STASH`** | `0x00207A` | `0x002DFE` | `device_mgr.s:111` | **Regs:** `Entry: D0 = byte to write (bit 15 will be set as write indicator)`<br>STASH - write byte to serial output buffer Entry: D0 = byte to write (bit 15 will be set as write indicator) |
| **`Status`** | `0x002450` | `0x0031EE` | `device_mgr.s:702` | _Status ($A005) A0 = paramBlock (CntrlParam) -> D0 = error csCode=1 is special: returns DCE handle in ioMisc without calling driver. |
| **`STATUS__MAP`** | — | — | `device_mgr.s:611` | P_tStatus - _Status trap handler Special case: csCode = 1 returns DCE handle in csParam. |
| **`STATUS_DEVICE`** | — | `0x003208` | `device_mgr.s:621` | — |
| **`STATUS_GET_DCE`** | `0x00246A` | — | `device_mgr.s:716` | STATUS_GET_DCE - Status csCode=1: return DCE handle in ioMisc |
| **`StdGZ`** | `0x010C6C` | `0x00B238` | `memory_mgr.s:2816` | **Proto:** `FUNCTION StdGZ(cbNeeded: Size): Size, called by TOTEPURGEABLES_CONT_3.`<br>StdGZ - standard grow-zone function (installed in zone.spare1 by InitZone) FUNCTION StdGZ(cbNeeded: Size): Size, called by TOTEPURGEABLES_CONT_3. Critical case (GZMoveHnd nil or = GZRootHnd): unless f... |
| **`STDGZ`** | `0x010C6C` | `0x00B238` | `memory_mgr.s:2111` | — |
| **`STDGZ_NO`** | `0x010C7E` | `0x00B24A` | `memory_mgr.s:2824`<br>`memory_mgr.s:2119` | — |
| **`STDGZ_NO_2`** | `0x010CA8` | `0x00B274` | `memory_mgr.s:2845`<br>`memory_mgr.s:2139` | STDGZ_NO_2 |
| **`STDGZ_NO_3`** | `0x010CB0` | `0x00B27C` | `memory_mgr.s:2848`<br>`memory_mgr.s:2142` | — |
| **`STDGZ_OK`** | `0x010CB4` | `0x00B280` | `memory_mgr.s:2856`<br>`memory_mgr.s:2149` | STDGZ_OK |
| **`STRIP_TBL`** | `0x00FA8A` | `0x009ED4` | `os_utilities.s:356`<br>`os_utilities.s:363` | STRIP_TBL: 256-entry x 16-bit international-collation weight table. Each entry packs (primary_char << 8) \| diacritic_weight, where primary_char is the base ASCII letter for collation and diacritic_wei... |
| **`STRIPADDRESS`** | — | `0x00A7D0` | `memory_mgr.s:584` | — |
| **`SysBeep`** | `0x0011DC` | — | `sys_error.s:117` | SysBeep - _SysBeep trap handler Plays the system alert sound if available, or flashes the menu bar if sound is busy or volume is zero. |
| **`SYSBEEP_AUDIBLE`** | `0x001200` | `0x0029D8` | `sys_error.s:138`<br>`memtest.s:2010` | SYSBEEP_AUDIBLE - audible beep via BootBeep square wave |
| **`SYSBEEP_EPILOG`** | `0x00120C` | `0x0029E0` | `sys_error.s:147`<br>`memtest.s:2013` | SYSBEEP_EPILOG - SysBeep epilogue, pops duration param and returns |
| **`SYSBEEP_FLASH`** | `0x0011EC` | `0x0029C4` | `sys_error.s:123`<br>`memtest.s:1999` | No sound hardware available: flash menu bar as visual alert |
| **`SysErr2`** | `0x00115E` | `0x0013A2` | `sys_error.s:38` | — |
| **`SYSERR2`** | `0x00115E` | `0x0013A2` | `sys_error.s:38` | SYSERR2 - system error dispatch: save SP, check debugger, call handler D0 = error code. Tries external debugger first, falls back to built-in DSErrorHandler. If handler returns 0, resume from error. |
| **`SYSERR_DISPATCH`** | — | `0x0013CE` | `sys_error.s:56` | — |
| **`SYSERR_TRY_DEBUGGER`** | — | `0x0013C0` | `sys_error.s:49` | No debugger or debugger not ready |
| **`SYSERR_USE_DS`** | — | `0x0013CA` | `sys_error.s:54` | — |
| **`SysError`** | `0x001142` | — | `sys_error.s:30` | System Error Handler -- _SysError, the system error alert, _SysBeep Apple source: SysErr.a (System 7.1: StartErr.a and StartAlert.a; MacSEROM.lst module SYSTEMERROR). In ROM order: SysError ($A9C9), S... |
| **`SYSTEMERROR`** | — | `0x001386` | `sys_error.s:27` | System Error Handler -- _SysError, the system error alert, _SysBeep Apple sources: StartErr.a and StartAlert.a (MacSEROM.lst module SYSTEMERROR). In ROM order (the SE has SysBeep with the startup test... |
| **`SYSUTIL`** | — | `0x009BD8` | `os_utilities.s:21` | Operating System Utilities Apple source: SysUtil.a (MacSEROM.lst module SYSUTIL). In ROM order: ASYNCPATCH                 - (an RTS: patch point) ReadParam, WriteParam      - parameter RAM: low-memor... |
| **`T2_DELAY_OK`** | `0x01768C` | `0x01AA22` | `time_mgr.s:145`<br>`time_mgr.s:159` | — |
| **`T2_NO_TASK`** | `0x0176B4` | `0x01AA48` | `time_mgr.s:157`<br>`time_mgr.s:170` | — |
| **`T2ISR_DISPATCH`** | — | `0x01AA82` | `time_mgr.s:200` | — |
| **`T2ISR_DONE`** | `0x0176F2` | `0x01AA96` | `time_mgr.s:191`<br>`time_mgr.s:210` | — |
| **`T2ISR_NEXT_TASK`** | `0x0176C6` | `0x01AA62` | `time_mgr.s:174`<br>`time_mgr.s:187` | — |
| **`T2ISR_RESTORE`** | — | `0x01AA94` | `time_mgr.s:208` | — |
| **`T2ISR_SKIP_TASK`** | `0x0176D2` | `0x01AA78` | `time_mgr.s:179`<br>`time_mgr.s:195` | — |
| **`TAGS_CHK_TFS`** | `0x007D12` | — | `file_mgr_cache.s:997` | — |
| **`TAGS_MFS_DATE`** | `0x007D38` | `0x00988E` | `file_mgr_cache.s:1022`<br>`file_mgr_cache.s:826` | TAGS_MFS_DATE - MFS tag: use current time instead of write count Called during boot. |
| **`TAGS_VOL_BLOCK`** | `0x007D24` | `0x00987A` | `file_mgr_cache.s:1009`<br>`file_mgr_cache.s:819` | TAGS_VOL_BLOCK - set up tags for non-file (volume) block Called during boot. |
| **`TB_CVT_END_BLK`** | `0x007AAA` | `0x0095FE` | `file_mgr_cache.s:628`<br>`file_mgr_cache.s:528` | — |
| **`TB_EXIT`** | `0x007B24` | `0x009678` | `file_mgr_cache.s:685`<br>`file_mgr_cache.s:581` | TB_EXIT |
| **`TB_INVALIDATE`** | `0x007B1E` | `0x009672` | `file_mgr_cache.s:677`<br>`file_mgr_cache.s:574` | — |
| **`TB_SCAN_NEXT`** | `0x007AEE` | `0x009642` | `file_mgr_cache.s:658`<br>`file_mgr_cache.s:555` | Called by: TB_SCAN_NEXT, TB_INVALIDATE |
| **`TFMOVE`** | — | `0x0060D8` | `file_mgr_dir.s:809` | if HFS, also rename root directory in catalog _CatMove: move a file/directory to a different parent |
| **`TFSBitTst`** | — | `0x00695C` | `file_mgr_dir.s:1834` | helper: test ioDirFlg bit |
| **`TFSDISPATCH`** | — | `0x004294` | `file_mgr_queue.s:31` | File Manager -- trap dispatch, file system queue, disk-switch hook Apple source: TFS.a, the head of the TurboFS module (MacSEROM.lst module TURBOFS): TFSDISPATCH (_FSDispatch $A060, the HFS selector d... |
| **`TFSVCBTst`** | `0x004EC6` | `0x006968` | `file_mgr_dir.s:2045` | TFSVCBTst -- tFS volume?. Called by: MOUNTVOL_CONT_6, MOUNTVOL_CONT_8, MOUNTVOL_SKIP_3, MOUNTVOL_NO_6, MTVOLDONE (and 32 more) |
| **`TFSVCBTST`** | `0x004EC6` | `0x006968` | `file_mgr_dir.s:1847` | TFSVCBTst: check if volume is HFS (signature = 'BD' = 0x4244) Called by: MOUNTVOL_CONT_6, MOUNTVOL_CONT_8, MOUNTVOL_REMOUNT_NEXT_FCB, MOUNTVOL_NO_6, MTVOLDONE (and 32 more) |
| **`TFSVCBTST_CONT`** | `0x004EF2` | `0x006994` | `file_mgr_dir.s:2069`<br>`file_mgr_dir.s:1870` | relative to end of file (mode 2) |
| **`TFSVCBTST_CONT_2`** | `0x004EF6` | `0x006998` | `file_mgr_dir.s:2073`<br>`file_mgr_dir.s:1874` | PM01: mode 0 or 1 |
| **`TFSVCBTST_ERR`** | `0x004F0E` | `0x0069B0` | `file_mgr_dir.s:2089`<br>`file_mgr_dir.s:1890` | — |
| **`TFSVCBTST_OK`** | `0x004EFA` | `0x00699C` | `file_mgr_dir.s:2076`<br>`file_mgr_dir.s:1877` | PM01: mode 0 or 1 |
| **`TFSVCBTST_OK_2`** | `0x004F00` | `0x0069A2` | `file_mgr_dir.s:2081`<br>`file_mgr_dir.s:1882` | check position vs EOF |
| **`TFSVCBTST_OK_3`** | `0x004F08` | `0x0069AA` | `file_mgr_dir.s:2086`<br>`file_mgr_dir.s:1887` | — |
| **`TIMEMGR`** | — | `0x01A95C` | `time_mgr.s:59` | **Proto:** `Pascal: PROCEDURE InsTime(tmTaskPtr: QElemPtr);`<br>**Regs:** `Entry: A0 = ptr to TMTask (qLink, qType, tmAddr, tmCount) Exit:  D0 = noErr`<br>Time Manager Manages asynchronous timer tasks using VIA Timer 2. Provides the _InsTime ($A058), _RmvTime ($A059), _PrimeTime ($A05A) traps. Timer 2 runs in one-shot mode. When a timer fires, VIAInt5_T... |
| **`ToMaxLimit`** | `0x010848` | `0x00ADFE` | `memory_mgr.s:2120` | ToMaxLimit - D2 = BufPtr - DefltStack, then fall into MaxLimit MaxLimit   - D1 = lower of D2 and SP - MinStack: the highest end allowed for the application zone ToMaxLimit is called by SETAPPBASE_CONT... |
| **`TOMAXLIMIT`** | `0x010848` | `0x00ADFE` | `memory_mgr.s:1534` | — |
| **`TotEPurgeables`** | `0x010602` | `0x00ABB8` | `memory_mgr.s:1650` | **Regs:** `Entry: A6 = zone Exit:  D0.L = bytes in free and purgeable blocks; A0 = largest such total`<br>TotEPurgeables - total the free and purgeable space of the zone Entry: A6 = zone Exit:  D0.L = bytes in free and purgeable blocks; A0 = largest such total within one region (regions end at nonrelocata... |
| **`TOTEPURGEABLES`** | `0x010602` | `0x00ABB8` | `memory_mgr.s:1152` | — |
| **`TOTEPURGEABLES_CONT`** | `0x01060C` | `0x00ABC2` | `memory_mgr.s:1655`<br>`memory_mgr.s:1157` | — |
| **`TOTEPURGEABLES_CONT_2`** | `0x010632` | `0x00ABE8` | `memory_mgr.s:1679`<br>`memory_mgr.s:1180` | TOTEPURGEABLES_CONT_2 |
| **`TOTEPURGEABLES_CONT_3`** | `0x010642` | `0x00ABF8` | `memory_mgr.s:1698`<br>`memory_mgr.s:1194` | **Regs:** `Exit: D2 = bytes added to the zone (0 if none or no proc); other`<br>TOTEPURGEABLES_CONT_3 - call the zone's system grow-zone proc Calls zone.spare1 ($2C, set to StdGZ by InitZone) with D0 = bytes needed. Exit: D2 = bytes added to the zone (0 if none or no proc); other... |
| **`TOTEPURGEABLES_EXIT`** | `0x01062E` | `0x00ABE4` | `memory_mgr.s:1671`<br>`memory_mgr.s:1173` | — |
| **`TOTEPURGEABLES_EXIT_2`** | `0x01065C` | `0x00AC12` | `memory_mgr.s:1708`<br>`memory_mgr.s:1204` | — |
| **`TOTEPURGEABLES_OK`** | `0x01062C` | `0x00ABE2` | `memory_mgr.s:1669`<br>`memory_mgr.s:1171` | — |
| **`TOTEPURGEABLES_OK_2`** | `0x010636` | `0x00ABEC` | `memory_mgr.s:1681`<br>`memory_mgr.s:1182` | — |
| **`TOTEPURGEABLES_OK_3`** | `0x01063E` | `0x00ABF4` | `memory_mgr.s:1686`<br>`memory_mgr.s:1187` | — |
| **`TOTEPURGEABLES_RETRY`** | `0x01065E` | `0x00AC14` | `memory_mgr.s:1716`<br>`memory_mgr.s:1211` | TOTEPURGEABLES_RETRY Called during boot. |
| **`TRACK_BTN_CHECK`** | `0x001420` | `0x00162C` | `sys_error.s:472`<br>`sys_error.s:429` | — |
| **`TRACK_BTN_DOWN`** | — | `0x00161C` | `sys_error.s:420` | Mouse is on a button: highlight it and track while held |
| **`TRACK_BTN_LOOP`** | — | `0x001620` | `sys_error.s:423` | — |
| **`TRACK_BTN_MOUSE`** | `0x001410` | — | `sys_error.s:463` | TRACK_BTN_MOUSE - track mouse while button is held down Highlights the button under the mouse (invert), and tracks mouse movement in/out of the button rect until mouse-up. |
| **`TRACK_BTN_POLL`** | `0x001414` | — | `sys_error.s:466` | — |
| **`Trap0_37`** | `0x00F790` | — | `os_utilities.s:24` | Operating System Utilities Apple source: SysUtil.a (MacSEROM.lst module SYSUTIL). In ROM order: ReadParam, WriteParam      - parameter RAM: low-memory copy SysParam <-> clock chip ReadDateTime, SetDat... |
| **`Trap1_1A`** | `0x00FFA4` | — | `memory_mgr.s:230` | **Proto:** `Pascal: FUNCTION GetZone: THz;`<br>**Regs:** `Exit:  A0 = TheZone; D0.W = noErr, MemErr cleared (INITZONE_EXIT)`<br>_GetZone ($A11A): return a pointer to the current heap zone Pascal: FUNCTION GetZone: THz; Exit:  A0 = TheZone; D0.W = noErr, MemErr cleared (INITZONE_EXIT) Toolbox trap $A81A dispatches here as well ... |
| **`Trap1_1B`** | `0x00FFAA` | — | `memory_mgr.s:245` | **Proto:** `Pascal: PROCEDURE SetZone(hz: THz);`<br>**Regs:** `Entry: A0 = hz (stored in TheZone without any check) Exit:  D0.W = noErr, MemErr cleared (INITZONE_EXIT)`<br>_SetZone ($A01B): make hz the current heap zone Pascal: PROCEDURE SetZone(hz: THz); Entry: A0 = hz (stored in TheZone without any check) Exit:  D0.W = noErr, MemErr cleared (INITZONE_EXIT) Toolbox tra... |
| **`Trap1_1D`** | `0x01003C` | — | `memory_mgr.s:399` | **Proto:** `Pascal: FUNCTION MaxMem(VAR grow: Size): Size;`<br>**Regs:** `Entry: trap bit 10 ($A51D) = use the system heap Exit:  D0.L = logical size of the largest contiguous free block;`<br>_MaxMem ($A11D): compact and purge the zone, return its largest free block Pascal: FUNCTION MaxMem(VAR grow: Size): Size; Entry: trap bit 10 ($A51D) = use the system heap Exit:  D0.L = logical size of... |
| **`Trap1_1E`** | `0x0100D6` | — | `memory_mgr.s:508` | **Proto:** `Pascal: FUNCTION NewPtr(logicalSize: Size): Ptr;`<br>**Regs:** `Entry: D0.L = logicalSize; trap bit 9 ($A31E) = clear the block, Exit:  A0 = pointer to the block (nil on failure), D0.W = result code`<br>_NewPtr ($A11E): allocate a nonrelocatable block Pascal: FUNCTION NewPtr(logicalSize: Size): Ptr; Entry: D0.L = logicalSize; trap bit 9 ($A31E) = clear the block, bit 10 ($A51E) = allocate in the syst... |
| **`Trap1_22`** | `0x01014E` | — | `memory_mgr.s:642` | **Proto:** `Pascal: FUNCTION NewHandle(logicalSize: Size): Handle;`<br>**Regs:** `Entry: D0.L = logicalSize; trap bit 9 ($A322) = clear the block, Exit:  A0 = handle (nil on failure), D0.W = noErr or memFullErr;`<br>_NewHandle ($A122): allocate a relocatable block Pascal: FUNCTION NewHandle(logicalSize: Size): Handle; Entry: D0.L = logicalSize; trap bit 9 ($A322) = clear the block, bit 10 ($A522) = allocate in th... |
| **`Trap1_23`** | `0x010170` | — | `memory_mgr.s:693` | **Proto:** `Pascal: PROCEDURE DisposHandle(h: Handle);`<br>**Regs:** `Entry: A0 = h Exit:  D0.W = noErr, memROZErr, memWZErr or memAZErr; MemErr set`<br>_DisposHandle ($A023): release a relocatable block and its master pointer Pascal: PROCEDURE DisposHandle(h: Handle); Entry: A0 = h Exit:  D0.W = noErr, memROZErr, memWZErr or memAZErr; MemErr set Bloc... |
| **`Trap1_24`** | `0x01019C` | — | `memory_mgr.s:750` | **Proto:** `Pascal: PROCEDURE SetHandleSize(h: Handle; newSize: Size);`<br>**Regs:** `Entry: A0 = h, D0.L = newSize Exit:  D0.W = noErr, memFullErr, memROZErr (cannot shrink a block in a`<br>_SetHandleSize ($A024): change the logical size of a relocatable block Pascal: PROCEDURE SetHandleSize(h: Handle; newSize: Size); Entry: A0 = h, D0.L = newSize Exit:  D0.W = noErr, memFullErr, memROZE... |
| **`Trap1_25`** | `0x010190` | — | `memory_mgr.s:729` | **Proto:** `Pascal: FUNCTION GetHandleSize(h: Handle): Size;`<br>**Regs:** `Entry: A0 = h Exit:  D0.L = logical size (>= 0) and MemErr = noErr, or D0 =`<br>_GetHandleSize ($A025): return the logical size of a relocatable block Pascal: FUNCTION GetHandleSize(h: Handle): Size; Entry: A0 = h Exit:  D0.L = logical size (>= 0) and MemErr = noErr, or D0 = nilH... |
| **`Trap1_29`** | `0x010230` | — | `memory_mgr.s:877` | **Proto:** `Pascal: PROCEDURE HLock(h: Handle);`<br>**Regs:** `Entry: A0 = h Exit:  D0.W = noErr, or nilHandleErr if the master pointer is nil;`<br>_HLock ($A029): lock a relocatable block Pascal: PROCEDURE HLock(h: Handle); Entry: A0 = h Exit:  D0.W = noErr, or nilHandleErr if the master pointer is nil; MemErr set Sets the lock bit (bit 7) in th... |
| **`Trap1_2A`** | `0x01023A` | — | `memory_mgr.s:897` | **Proto:** `Pascal: PROCEDURE HUnlock(h: Handle);`<br>**Regs:** `Entry: A0 = h Exit:  D0.W = noErr, or nilHandleErr if the master pointer is nil;`<br>_HUnlock ($A02A): unlock a relocatable block Pascal: PROCEDURE HUnlock(h: Handle); Entry: A0 = h Exit:  D0.W = noErr, or nilHandleErr if the master pointer is nil; MemErr set (h = nil: returns at once... |
| **`Trap1_32`** | `0x00280A` | — | `event_mgr.s:214` | _FlushEvents ($A032) - remove events matching a mask D0.W = eventMask (low word): bits for event types to flush D0.W = stopMask (high word, swapped into D1): if an event matches this mask, stop flushi... |
| **`Trap1_4C`** | `0x00FFBE` | — | `memory_mgr.s:282` | **Proto:** `Pascal: FUNCTION CompactMem(cbNeeded: Size): Size;`<br>**Regs:** `Entry: D0.L = cbNeeded; trap bit 10 ($A44C) = use the system heap Exit:  D0.L = logical size of the largest contiguous free block found;`<br>_CompactMem ($A04C): compact the current heap zone Pascal: FUNCTION CompactMem(cbNeeded: Size): Size; Entry: D0.L = cbNeeded; trap bit 10 ($A44C) = use the system heap Exit:  D0.L = logical size of th... |
| **`Trap1_54`** | `0x00F878` | — | `os_utilities.s:244` | _UpperString ($A054): convert string to uppercase in place D0 = string length, A0 = string ptr, D1 = case/marks flags Toolbox trap $A854, UprString's trap number in the 64K ROM, dispatches here as wel... |
| **`TRAP_COMMON`** | `0x001F54` | `0x002CD8` | `trap_dispatch.s:32`<br>`trap_dispatch.s:36` | EMT1010 - 68000 Line 1010 Emulator (trap dispatcher) 68000 A-line exception pushes SR (word) + PC (long) onto stack. This is the main entry point for all A-line trap dispatch. |
| **`TRAP_DECODE`** | — | `0x002CDC` | `trap_dispatch.s:39` | Common A-line dispatch: fetch trap word, decode OS vs Toolbox |
| **`TRAP_OS_NOSAVEREG`** | `0x001FAC` | `0x002D30` | `trap_dispatch.s:77`<br>`trap_dispatch.s:78` | OS trap dispatch - bit 8 set (A0 returns a result) Only A1 is saved/restored; A0 passes through to return result. |
| **`TRAP_OS_PATH`** | `0x001F88` | `0x002D0C` | `trap_dispatch.s:57`<br>`trap_dispatch.s:61` | OS trap dispatch path OS trap word: bit 8 = 1 means do NOT save/restore A0 (result in A0). D2 has 9-bit trap number; bit 8 is the save-A0 flag, bits 0-7 = index. |
| **`TRAP_OS_RETURN`** | `0x001FA2` | `0x002D26` | `trap_dispatch.s:66`<br>`trap_dispatch.s:70` | — |
| **`TRAP_TBOX_DISPATCH`** | `0x001F86` | `0x002D0A` | `trap_dispatch.s:48`<br>`trap_dispatch.s:55` | Toolbox trap dispatch: look up in ToolTable |
| **`TrapDispatchTbl`** | `0x007E58` | — | `dispatch_table.s:30` | Compressed trap dispatch table Apple source: DispTable.a. Read once at startup by the decoder in vectors.s (DECODE_DISP_LOOP), which fills the Toolbox dispatch table (512 entries at ToolDispTable) and... |
| **`TrashBlocks`** | `0x007AE8` | `0x0095E8` | `file_mgr_cache.s:655` | Trash Blocks |
| **`TRASHBLOCKS`** | `0x007AE8` | `0x0095E8` | `file_mgr_cache.s:517` | — |
| **`TrashFBlocks`** | `0x007A8A` | `0x0095DE` | `file_mgr_cache.s:606` | TrashFBlocks -- trash cached blocks for this file. Trash F Blocks |
| **`TRASHFBLOCKS`** | `0x007A8A` | `0x0095DE` | `file_mgr_cache.s:512` | — |
| **`TrashVBlks`** | `0x007A62` | `0x0095B0` | `file_mgr_cache.s:578` | Trash V Blks |
| **`TRASHVBLKS`** | `0x007A62` | `0x0095B0` | `file_mgr_cache.s:488` | — |
| **`TreeSearch`** | `0x0071E4` | `0x008D42` | `file_mgr_btree.s:1510` | TreeSearch -- treeSearch: descend B-tree from root to leaf for this key. Tree Search |
| **`TREESEARCH`** | `0x0071E4` | `0x008D42` | `file_mgr_btree.s:1353` | — |
| **`TruncateFile`** | `0x005D9E` | `0x007860` | `file_mgr_alloc.s:786` | Truncate File |
| **`TRUNCATEFILE`** | `0x005D9E` | `0x007860` | `file_mgr_alloc.s:675` | — |
| **`TRUNCATEFILE_CONT`** | `0x005DE0` | — | `file_mgr_alloc.s:811` | TFLocExt: locate extent mapping last byte of truncated file truncating to zero: release all extents |
| **`TRUNCATEFILE_CONT_2`** | `0x005E24` | `0x0078E6` | `file_mgr_alloc.s:835`<br>`file_mgr_alloc.s:724` | — |
| **`TRUNCATEFILE_CONT_3`** | `0x005E74` | `0x00793C` | `file_mgr_alloc.s:867`<br>`file_mgr_alloc.s:754` | TFRelExt: release extents for this record |
| **`TRUNCATEFILE_CONT_4`** | `0x005EC6` | `0x007990` | `file_mgr_alloc.s:918`<br>`file_mgr_alloc.s:799` | TRUNCATEFILE_CONT_4 - FXSetUp: allocate FXM vars on A6 stack |
| **`TRUNCATEFILE_CONT_5`** | `0x005ED0` | `0x00799A` | `file_mgr_alloc.s:929`<br>`file_mgr_alloc.s:804` | TRUNCATEFILE_CONT_5 XFFlush: flush the extent file for a specified volume |
| **`TRUNCATEFILE_DELETE_REC`** | — | `0x007978` | `file_mgr_alloc.s:781` | — |
| **`TRUNCATEFILE_DONE`** | `0x005EB4` | `0x00797E` | `file_mgr_alloc.s:904`<br>`file_mgr_alloc.s:785` | TFExit |
| **`TRUNCATEFILE_DONE_2`** | `0x005EF8` | — | `file_mgr_alloc.s:942` | — |
| **`TRUNCATEFILE_EMPTY`** | `0x005E8C` | `0x007954` | `file_mgr_alloc.s:878`<br>`file_mgr_alloc.s:765` | TFRelRExt |
| **`TRUNCATEFILE_ERR`** | `0x005EB8` | `0x007982` | `file_mgr_alloc.s:907`<br>`file_mgr_alloc.s:789` | Called by: TRUNCATEFILE_FIND_EXTENT, TRUNCATEFILE_NO, TRUNCATEFILE_RELEASE_EXTENT, TRUNCATEFILE_NEXT_2, TRUNCATEFILE_OK |
| **`TRUNCATEFILE_ERR_2`** | `0x005EFA` | — | `file_mgr_alloc.s:944` | — |
| **`TRUNCATEFILE_FIND_EXTENT`** | — | `0x0078A2` | `file_mgr_alloc.s:700` | — |
| **`TRUNCATEFILE_FOUND`** | `0x005E5E` | `0x007926` | `file_mgr_alloc.s:856`<br>`file_mgr_alloc.s:745` | — |
| **`TRUNCATEFILE_LOOP`** | `0x005E66` | `0x00792E` | `file_mgr_alloc.s:861`<br>`file_mgr_alloc.s:749` | copy extent data to FXM buffer |
| **`TRUNCATEFILE_NEXT`** | `0x005E36` | — | `file_mgr_alloc.s:843` | TFLoop: get next extent record in BTree |
| **`TRUNCATEFILE_NEXT_2`** | `0x005E76` | `0x00793E` | `file_mgr_alloc.s:869`<br>`file_mgr_alloc.s:756` | — |
| **`TRUNCATEFILE_NO`** | `0x005E04` | `0x0078C6` | `file_mgr_alloc.s:823`<br>`file_mgr_alloc.s:712` | TFTrunPEOF: truncate extent containing new PEOF |
| **`TRUNCATEFILE_NO_2`** | `0x005E94` | `0x00795C` | `file_mgr_alloc.s:883`<br>`file_mgr_alloc.s:769` | TFUpdRec: update extent record |
| **`TRUNCATEFILE_OK`** | `0x005EA2` | `0x00796A` | `file_mgr_alloc.s:894`<br>`file_mgr_alloc.s:775` | TRUNCATEFILE_OK |
| **`TRUNCATEFILE_OK_2`** | `0x005EB0` | — | `file_mgr_alloc.s:900` | — |
| **`TRUNCATEFILE_RELEASE_EXTENT`** | — | `0x0078F8` | `file_mgr_alloc.s:731` | — |
| **`TSRCH_EXIT`** | `0x007262` | `0x008DC2` | `file_mgr_btree.s:1573`<br>`file_mgr_btree.s:1416` | — |
| **`TSRCH_LEAF`** | `0x007258` | `0x008DB8` | `file_mgr_btree.s:1568`<br>`file_mgr_btree.s:1411` | TSNxtLev: move to next level down TSDone: at leaf level, set up return info |
| **`TSRCH_LOOP`** | `0x007208` | `0x008D6A` | `file_mgr_btree.s:1531`<br>`file_mgr_btree.s:1374` | TSLoop: get the node and search for key |
| **`TSRCH_SETINDX`** | `0x007236` | `0x008D96` | `file_mgr_btree.s:1552`<br>`file_mgr_btree.s:1395` | TSUpdTPR: update TPR info |
| **`TSRCH_START`** | `0x007202` | `0x008D64` | `file_mgr_btree.s:1527`<br>`file_mgr_btree.s:1370` | TSRCH_START |
| **`TstMod`** | `0x00539C` | — | `file_mgr_io.s:680` | TstMod: test if we may modify this file Called during boot. |
| **`TSTMOD_EXIT`** | `0x0053AE` | — | `file_mgr_io.s:687` | — |
| **`TstMod_Impl`** | — | `0x006E58` | `file_mgr_io.s:606` | — |
| **`TstMod_VOL_CHECK`** | — | `0x006E66` | `file_mgr_io.s:611` | — |
| **`TURBOFS`** | — | `0x004294` | `file_mgr_queue.s:30` | File Manager -- trap dispatch, file system queue, disk-switch hook Apple source: TFS.a, the head of the TurboFS module (MacSEROM.lst module TURBOFS): TFSDISPATCH (_FSDispatch $A060, the HFS selector d... |
| **`TV_EXIT`** | `0x007A84` | `0x0095D8` | `file_mgr_cache.s:597`<br>`file_mgr_cache.s:509` | TV_EXIT |
| **`TV_SCAN_NEXT`** | `0x007A6A` | `0x0095BE` | `file_mgr_cache.s:582`<br>`file_mgr_cache.s:495` | — |
| **`UC_EXIT`** | `0x006592` | `0x00805A` | `file_mgr_catalog.s:618`<br>`file_mgr_catalog.s:561` | — |
| **`UC_FLUSH`** | `0x00658A` | `0x008052` | `file_mgr_catalog.s:615`<br>`file_mgr_catalog.s:558` | UC_FLUSH |
| **`UNIT_EMPTY_ERR`** | `0x0021CA` | — | `device_mgr.s:346` | UNIT_EMPTY_ERR - Driver not found error Returns unitEmptyErr (-21) in ioResult. |
| **`UnloadSeg`** | `0x00F4E0` | `0x009920` | `segment_loader.s:98` | _UnLoadSeg ($A9F1) _UnLoadSeg ($A9F1): mark a CODE segment as unlocked (purgeable) Reverts jump table entries from JMP to LoadSeg stubs |
| **`UNLOADSEG`** | `0x00F4E0` | `0x009920` | `segment_loader.s:74` | — |
| **`UNLOADSEG_CONT`** | `0x00F522` | `0x009974` | `segment_loader.s:132`<br>`segment_loader.s:111` | UNLOADSEG_CONT Called during boot. |
| **`UNLOADSEG_CONT_2`** | `0x00F548` | `0x00998E` | `segment_loader.s:161`<br>`segment_loader.s:125` | UNLOADSEG_CONT_2 UNLOADSEG_CONT_2: CurPageOption > 0: reserve 24K for sound/screen buffer |
| **`UNLOADSEG_DONE`** | — | `0x00995C` | `segment_loader.s:98` | — |
| **`UNLOADSEG_EMPTY`** | `0x00F51E` | — | `segment_loader.s:123` | — |
| **`UNLOADSEG_LOOP`** | `0x00F504` | `0x009942` | `segment_loader.s:112`<br>`segment_loader.s:87` | restore jump table stubs: MOVE.W #seg,-(SP); _LoadSeg |
| **`UNLOADSEG_OK`** | `0x00F546` | `0x00998C` | `segment_loader.s:153`<br>`segment_loader.s:123` | UNLOADSEG_OK Called during boot. |
| **`UNLOADSEG_SKIP`** | `0x00F526` | — | `segment_loader.s:134` | — |
| **`UNLOCK_DRV_CHECK`** | `0x0020A8` | `0x002E34` | `device_mgr.s:170`<br>`device_mgr.s:155` | — |
| **`UNLOCK_DRV_DONE`** | `0x0020C2` | `0x002E4E` | `device_mgr.s:178`<br>`device_mgr.s:163` | — |
| **`UnmountVol`** | `0x0035B4` | `0x00503A` | `file_mgr_vol.s:1257` | _UnmountVol ($A00E) _UnmountVol ($A00E) |
| **`UNMOUNTVOL`** | `0x0035B4` | `0x00503A` | `file_mgr_vol.s:1175` | _UnmountVol: unmount a volume |
| **`UNMOUNTVOL_CONT`** | `0x0035BE` | `0x005044` | `file_mgr_vol.s:1268`<br>`file_mgr_vol.s:1181` | UNMOUNTVOL_CONT Called during boot. UNMOUNTVOL_CONT: flush/close all open user files for this volume |
| **`UNMOUNTVOL_CONT_2`** | `0x0035C8` | `0x00504E` | `file_mgr_vol.s:1272`<br>`file_mgr_vol.s:1185` | — |
| **`UNMOUNTVOL_ERR`** | `0x0035F2` | — | `file_mgr_vol.s:1289` | — |
| **`UNMOUNTVOL_EXIT`** | — | `0x005078` | `file_mgr_vol.s:1201` | — |
| **`UNMOUNTVOL_NEXT`** | — | `0x005070` | `file_mgr_vol.s:1197` | — |
| **`UNMOUNTVOL_NO`** | `0x0035E4` | `0x00506A` | `file_mgr_vol.s:1282`<br>`file_mgr_vol.s:1194` | — |
| **`UNMOUNTVOL_SKIP`** | `0x0035EA` | — | `file_mgr_vol.s:1285` | — |
| **`UPD_ROOT_CNTS`** | `0x0065BE` | `0x008086` | `file_mgr_catalog.s:656`<br>`file_mgr_catalog.s:592` | UPD_ROOT_CNTS: update root counts if in root directory |
| **`UPD_ROOT_FILES`** | `0x0065D2` | `0x00809A` | `file_mgr_catalog.s:663`<br>`file_mgr_catalog.s:599` | — |
| **`UPD_VCNTS`** | `0x0065AE` | `0x008076` | `file_mgr_catalog.s:648`<br>`file_mgr_catalog.s:584` | UPD_VCNTS - UpdVCnts: update VCB directory and file counts |
| **`UPD_VCNTS_DONE`** | `0x0065D6` | `0x00809E` | `file_mgr_catalog.s:665`<br>`file_mgr_catalog.s:601` | — |
| **`UPD_VCNTS_FILE`** | `0x0065BA` | `0x008082` | `file_mgr_catalog.s:653`<br>`file_mgr_catalog.s:589` | — |
| **`UPDALTMDB`** | — | `0x008B2E` | `file_mgr_btree.s:1103` | UPDALTMDB (Apple's UpdAltMDB, vector JUpdAltMDB of BTAlloc.a): update the alternate MDB on disk |
| **`UPDATE_KEYMAP`** | `0x00269C` | — | `keyboard.s:193` | UPDATE_KEYMAP - Update KeyMap bitmap and call key translation procedure In: D2 = virtual key code (0-127), D3 = raw byte (bit 7 = up/down) Out: D0 = translated ASCII character (0 if no translation pro... |
| **`UpdateFree`** | `0x0059D2` | `0x00747C` | `file_mgr_alloc.s:274` | UpdateFree: recount free blocks by scanning entire bitmap |
| **`UPDATEFREE`** | `0x0059D2` | `0x00747C` | `file_mgr_alloc.s:233` | — |
| **`UPDATEFREE_CONT`** | `0x0059E4` | — | `file_mgr_alloc.s:281` | — |
| **`UPDATEFREE_DONE`** | `0x0059F8` | `0x00749E` | `file_mgr_alloc.s:292`<br>`file_mgr_alloc.s:251` | — |
| **`UPDATEFREE_ERR`** | `0x0059FC` | `0x0074A2` | `file_mgr_alloc.s:294`<br>`file_mgr_alloc.s:253` | — |
| **`UPDATEFREE_LOOP`** | — | `0x00748C` | `file_mgr_alloc.s:240` | — |
| **`UPDATEFREE_NO`** | `0x0059EE` | `0x007496` | `file_mgr_alloc.s:287`<br>`file_mgr_alloc.s:246` | — |
| **`UpdCName`** | `0x0066C2` | `0x00818C` | `file_mgr_catalog.s:812` | UpdCName -- move in the CName. Upd C Name |
| **`UPDCNAME`** | `0x0066C2` | `0x00818C` | `file_mgr_catalog.s:716` | — |
| **`UPDCNAME_COPY`** | `0x0066D2` | `0x00819C` | `file_mgr_catalog.s:820`<br>`file_mgr_catalog.s:724` | — |
| **`UpdDRec`** | `0x007646` | `0x00919A` | `file_mgr_btree.s:2201` | UpdDRec -- replace the junk data record. Upd D Rec |
| **`UPDDREC`** | `0x007646` | `0x00919A` | `file_mgr_btree.s:1911` | UpdDRec: replace junk data record with real data after BTInsert Input: A0=source data (or nil to clear), D0=data size |
| **`UPDDREC_CLR`** | `0x00765E` | `0x0091B2` | `file_mgr_btree.s:2213`<br>`file_mgr_btree.s:1923` | — |
| **`UPDDREC_CLRLOOP`** | `0x00765C` | `0x0091B0` | `file_mgr_btree.s:2211`<br>`file_mgr_btree.s:1921` | — |
| **`UPDDREC_EXIT`** | `0x007662` | `0x0091B6` | `file_mgr_btree.s:2215`<br>`file_mgr_btree.s:1925` | — |
| **`UpdIKey`** | `0x007668` | `0x0091BC` | `file_mgr_btree.s:2223` | Upd I Key - update key portion of an index record |
| **`UPDIKEY`** | `0x007668` | `0x0091BC` | `file_mgr_btree.s:1930` | UpdIKey: update index key to max key length with padding Input: A0=source key, A1=dest key buffer |
| **`UPDIKEY_CPYLOOP`** | `0x007682` | `0x0091D6` | `file_mgr_btree.s:2235`<br>`file_mgr_btree.s:1942` | — |
| **`UPDIKEY_CPYTEST`** | `0x007684` | `0x0091D8` | `file_mgr_btree.s:2237`<br>`file_mgr_btree.s:1944` | — |
| **`UPDIKEY_EXIT`** | `0x007694` | `0x0091E8` | `file_mgr_btree.s:2246`<br>`file_mgr_btree.s:1953` | — |
| **`UPDIKEY_PADLOOP`** | `0x00768E` | `0x0091E2` | `file_mgr_btree.s:2242`<br>`file_mgr_btree.s:1949` | — |
| **`UPDIKEY_PADTEST`** | `0x007690` | `0x0091E4` | `file_mgr_btree.s:2244`<br>`file_mgr_btree.s:1951` | — |
| **`UPDTECNTPOS`** | `0x0051EC` | `0x006C9E` | `file_mgr_io.s:449`<br>`file_mgr_io.s:412` | UpdteCntPos: update catalog record from FCB |
| **`UPPER_FOLD_TBL`** | — | `0x009DD4` | `os_utilities.s:286` | UPPER_FOLD_TBL (= UPPER_FOLD_TBL): 256-byte case-folding table indexed by char code. Folds ASCII a-z (0x61..0x7A) to A-Z (0x41..0x5A) and high-bit Mac chars to their case-folded equivalent for the cas... |
| **`UPPERSTRING_LOOP`** | — | `0x009CC6` | `os_utilities.s:193` | UPPERSTRING_LOOP |
| **`UPPERSTRING_LOOP_2`** | — | `0x009CCC` | `os_utilities.s:197` | — |
| **`UprString`** | `0x00F878` | `0x009CC2` | `os_utilities.s:245` | _UpperString ($A054): convert string to uppercase in place D0 = string length, A0 = string ptr, D1 = case/marks flags Toolbox trap $A854, UprString's trap number in the 64K ROM, dispatches here as wel... |
| **`UPRSTRING`** | `0x00F878` | `0x009CC2` | `os_utilities.s:186` | — |
| **`UPRSTRING_CONT`** | `0x00F88A` | — | `os_utilities.s:266` | UPRSTRING_CONT |
| **`UPRSTRING_LOOP`** | `0x00F87C` | — | `os_utilities.s:253` | UPRSTRING_LOOP |
| **`UPRSTRING_LOOP_2`** | `0x00F882` | — | `os_utilities.s:257` | — |
| **`VADJEOF`** | — | `0x006FE8` | `file_mgr_io.s:779` | — |
| **`VALLOCNODE`** | — | `0x0088FE` | `file_mgr_btree.s:848` | — |
| **`VBASICIO`** | — | `0x00976E` | `file_mgr_cache.s:688` | — |
| **`VBL_SCAN_LOOP`** | — | `0x009978` | `segment_loader.s:113` | — |
| **`VBLCORE`** | — | `0x002C50` | `vbl_mgr.s:21` | **Regs:** `Entry: A0 = VBLTask record pointer`<br>Vertical Retrace Manager -- _VInstall / _VRemove Apple source: VerticalRetraceMgr.a (MacSEROM.lst module VBLCORE). The VBL interrupt handler itself, which runs the VBL task queue every tick, is VBLINT... |
| **`VBLKALLOC`** | — | `0x007288` | `file_mgr_alloc.s:16` | — |
| **`VBLKDEALLOC`** | — | `0x0073E2` | `file_mgr_alloc.s:163` | — |
| **`VBMCHK`** | — | `0x004DB8` | `file_mgr_vol.s:892` | — |
| **`VBTCLOSE`** | — | `0x0081AC` | `file_mgr_btree.s:31` | — |
| **`VBTDELETE`** | — | `0x0081EC` | `file_mgr_btree.s:58` | — |
| **`VBTFLUSH`** | — | `0x00839E` | `file_mgr_btree.s:237` | — |
| **`VBTGETRECORD`** | — | `0x008402` | `file_mgr_btree.s:279` | — |
| **`VBTINSERT`** | — | `0x0084BA` | `file_mgr_btree.s:377` | — |
| **`VBTOPEN`** | — | `0x00875A` | `file_mgr_btree.s:650` | — |
| **`VBTSEARCH`** | — | `0x008812` | `file_mgr_btree.s:735` | — |
| **`VBTUPDATE`** | — | `0x00889C` | `file_mgr_btree.s:799` | — |
| **`VCACHERDIP`** | — | `0x009684` | `file_mgr_cache.s:587` | — |
| **`VCACHEWRIP`** | — | `0x0096B0` | `file_mgr_cache.s:605` | — |
| **`VCKEXTFS`** | — | `0x0050C4` | `file_mgr_vol.s:1246` | — |
| **`VCMSETUP`** | — | `0x00806E` | `file_mgr_catalog.s:576` | — |
| **`VDEALLOCFILE`** | — | `0x007556` | `file_mgr_alloc.s:357` | — |
| **`vDoEject`** | `0x002C1C` | `0x004664` | `file_mgr_vol.s:66` | File Manager -- common subroutines and volume calls Apple sources, included by TFS.a (MacSEROM.lst module TURBOFS): TFSCommon.a (vDoEject, DivUp, RoundAlloc, QueueSearch, GetVCBRFN, FindVCBDrv, Resolv... |
| **`VDOEJECT`** | `0x002C1C` | `0x004664` | `file_mgr_vol.s:67` | **Regs:** `Entry: D1 = drive number, D2 = volume refNum`<br>File Manager -- common subroutines and volume calls Apple sources, included by TFS.a (MacSEROM.lst module TURBOFS): TFSCommon.a (DOEJECT, DIVUP, ROUNDALLOC, GETVCBRFN, MARKVCB, MARKVCBTIME, FLUSHMDB, ... |
| **`VDOEJECT_DO_EJECT`** | `0x002C40` | `0x004688` | `file_mgr_vol.s:80`<br>`file_mgr_vol.s:82` | — |
| **`VDOEJECT_DONE`** | `0x002C4A` | `0x004692` | `file_mgr_vol.s:85`<br>`file_mgr_vol.s:87` | — |
| **`VDTRMV1`** | — | `0x0050E8` | `file_mgr_vol.s:1268` | — |
| **`VDTRMV3`** | — | `0x0050D4` | `file_mgr_vol.s:1257` | — |
| **`VEXTBTFILE`** | — | `0x008994` | `file_mgr_btree.s:919` | — |
| **`VEXTENDFILE`** | — | `0x00762A` | `file_mgr_alloc.s:445` | — |
| **`VFILEOPEN`** | — | `0x005AC4` | `file_mgr_dir.s:45` | — |
| **`VFLUSHCACHE`** | — | `0x009220` | `file_mgr_cache.s:50` | — |
| **`VFNDFILNAME`** | — | `0x00643C` | `file_mgr_dir.s:1194` | FndFilName: resolve pathname to volume, directory, and catalog record |
| **`VFREENODE`** | — | `0x008A82` | `file_mgr_btree.s:1017` | — |
| **`VGETBLOCK`** | — | `0x00930A` | `file_mgr_cache.s:168` | — |
| **`VGETNODE`** | — | `0x008F5E` | `file_mgr_btree.s:1606` | — |
| **`VIAInt5_Timer2`** | `0x0176B6` | — | `time_mgr.s:168` | VIAInt5_Timer2 -- Timer 2 interrupt handler Called when T2 counts down to zero. Subtracts the elapsed interval from every primed task's tmCount, then fires the soonest task if its tmCount has reached ... |
| **`VIAInt_KeyDataReady`** | `0x0025E4` | `0x0036F4` | `keyboard.s:77`<br>`adb_mgr.s:434` | VIAInt_KeyDataReady - VIA SR interrupt: keyboard sent response data Called when VIA shift register completes a byte transfer. If Mac was transmitting (ACR bit 4 set), this is command-done; wait for ke... |
| **`VInstall`** | `0x001C2A` | `0x002C50` | `vbl_mgr.s:24` | Vertical Retrace Manager -- _VInstall / _VRemove Apple source: VerticalRetraceMgr.a (MacSEROM.lst module VBLCORE). The VBL interrupt handler itself, which runs the VBL task queue every tick, is VBLInt... |
| **`VINSTALL`** | `0x001C2A` | `0x002C50` | `vbl_mgr.s:22` | **Regs:** `Entry: A0 = VBLTask record pointer`<br>Vertical Retrace Manager -- _VInstall / _VRemove Apple source: VerticalRetraceMgr.a (MacSEROM.lst module VBLCORE). The VBL interrupt handler itself, which runs the VBL task queue every tick, is VBLINT... |
| **`VINSTALL_ENQUEUE`** | `0x001C68` | `0x002C94` | `vbl_mgr.s:58`<br>`vbl_mgr.s:53` | — |
| **`VINSTALL_PHASE_OK`** | `0x001C62` | `0x002C8E` | `vbl_mgr.s:55`<br>`vbl_mgr.s:50` | Phase-align first fire: compute (Ticks mod vblCount) offset |
| **`VINSTALL_SYNC`** | `0x001C36` | `0x002C5C` | `vbl_mgr.s:36`<br>`vbl_mgr.s:28` | VINSTALL_SYNC - VInstall phase synchronization and enqueue Called during boot. |
| **`VINSTALL_TYPERR`** | `0x001C32` | `0x002C58` | `vbl_mgr.s:27`<br>`vbl_mgr.s:25` | — |
| **`VLG2PHYS`** | — | `0x007092` | `file_mgr_io.s:855` | — |
| **`VLOCCREC`** | — | `0x008164` | `file_mgr_catalog.s:697` | — |
| **`VLOCCREC_SEARCH`** | — | `0x008172` | `file_mgr_catalog.s:704` | — |
| **`VMAPFBLOCK`** | — | `0x0077E4` | `file_mgr_alloc.s:624` | — |
| **`VMARKBLOCK`** | — | `0x00954E` | `file_mgr_cache.s:442` | — |
| **`VPERMSSNCHK`** | — | `0x005C0C` | `file_mgr_dir.s:202` | PermssnChk: check file access permissions |
| **`VRDBLOCKS`** | — | `0x0097E8` | `file_mgr_cache.s:760` | — |
| **`VREADBM`** | — | `0x0074B0` | `file_mgr_alloc.s:261` | — |
| **`VRELBLOCK`** | — | `0x009564` | `file_mgr_cache.s:455` | — |
| **`VRELNODE`** | — | `0x00912A` | `file_mgr_btree.s:1839` | — |
| **`VRemove`** | `0x001C74` | `0x002CA0` | `vbl_mgr.s:71` | _VRemove ($A034) - Remove a VBL task from the VBL queue A0 = pointer to VBL task element. Returns D0 from Dequeue (0=success, qErr if not found). |
| **`VREMOVE`** | `0x001C74` | `0x002CA0` | `vbl_mgr.s:62` | **Regs:** `Entry: A0 = VBLTask record pointer`<br>VREMOVE - _VRemove trap: remove a VBL task from the queue Entry: A0 = VBLTask record pointer Returns D0 = 0 (success) or D0 = -2 (bad qType) |
| **`VRFNCALL`** | — | `0x006E0A` | `file_mgr_io.s:564` | — |
| **`VSEGSTACK`** | — | `0x009AC6` | `segment_loader.s:245` | — |
| **`VSETUPTAGS`** | — | `0x009848` | `file_mgr_cache.s:800` | — |
| **`VSM`** | — | `0x007282` | `file_mgr_alloc.s:12` | File Manager -- allocation: volume bitmap and file extents Apple sources: VSM.a, the Volume Space Manager (MacSEROM.lst module VSM: BlkAlloc, BlkDealloc, BlkChk, UpdateFree, ReadBM -- allocation block... |
| **`VTRASHBLOCKS`** | — | `0x00963C` | `file_mgr_cache.s:551` | — |
| **`VTRASHVBLKS`** | — | `0x0095B6` | `file_mgr_cache.s:491` | — |
| **`VTREESEARCH`** | — | `0x008D48` | `file_mgr_btree.s:1357` | TreeSearch: descend B-tree from root to leaf |
| **`VTRUNCATEFILE`** | — | `0x007866` | `file_mgr_alloc.s:678` | — |
| **`VTSTMOD`** | — | `0x006E54` | `file_mgr_io.s:603` | — |
| **`VWRBLOCKS`** | — | `0x009836` | `file_mgr_cache.s:785` | — |
| **`VXFSEARCH`** | — | `0x0079D4` | `file_mgr_alloc.s:827` | — |
| **`WAIT_MOUSE_DOWN`** | `0x0013F2` | `0x001602` | `sys_error.s:442`<br>`sys_error.s:405` | All buttons drawn: show cursor and wait for mouse click Wait for mouse button down |
| **`WBLK_SETUP_TAGS`** | `0x007BD4` | `0x009728` | `file_mgr_cache.s:812`<br>`file_mgr_cache.s:667` | — |
| **`WDLOOKUP_RET`** | `0x002D16` | `0x00475E` | `file_mgr_vol.s:265`<br>`file_mgr_vol.s:234` | — |
| **`WPOff`** | `0x00FDBA` | `0x00A204` | `os_utilities.s:615` | WPOff: disable RTC write protect (write $55 to WP register) |
| **`WPOFF`** | `0x00FDBA` | `0x00A204` | `os_utilities.s:641` | — |
| **`WPOFF_CONT`** | `0x00FDC2` | `0x00A20C` | `os_utilities.s:624`<br>`os_utilities.s:649` | WPOFF_CONT: write SysParam (20 bytes) to RTC PRAM |
| **`WPOFF_LOOP`** | `0x00FDE4` | `0x00A22E` | `os_utilities.s:643`<br>`os_utilities.s:667` | WPOFF_LOOP: write consecutive bytes from A2 to RTC registers D1 = starting RTC command, D3 = byte count - 1 |
| **`WPOn`** | `0x00FDB2` | `0x00A1FC` | `os_utilities.s:606` | WP On WPOn: enable RTC write protect (write $D5 to WP register) |
| **`WPON`** | `0x00FDB2` | `0x00A1FC` | `os_utilities.s:637` | — |
| **`WrBlocks`** | `0x007CE0` | `0x009830` | `file_mgr_cache.s:967` | Wr Blocks |
| **`WRBLOCKS`** | `0x007CE0` | `0x009830` | `file_mgr_cache.s:782` | — |
| **`Write`** | `0x00242E` | `0x0031CC` | `device_mgr.s:665` | _Write ($A003) A0 = paramBlock -> D0 = error; writes ioReqCount bytes Positive ioRefNum -> file write; negative -> device driver write. Called during boot. |
| **`WRITE`** | `0x00242E` | `0x0031CC` | `device_mgr.s:591` | WRITE - _Write trap: write to device or file |
| **`WRITE_DEVICE`** | `0x002438` | `0x0031D6` | `device_mgr.s:676`<br>`device_mgr.s:595` | WRITE_DEVICE - device driver write path D0 = -20 (writErr default), D4 = 1 (dWritEnable bit position) Called during boot. |
| **`WriteBlock`** | `0x007BC0` | `0x009714` | `file_mgr_cache.s:805` | Write Block Called during boot. |
| **`WRITEBLOCK`** | `0x007BC0` | `0x009714` | `file_mgr_cache.s:660` | — |
| **`WriteOwnBuf`** | `0x007BB8` | `0x00970C` | `file_mgr_cache.s:795` | WriteOwnBuf -- call. Write Own Buf |
| **`WRITEOWNBUF`** | `0x007BB8` | `0x00970C` | `file_mgr_cache.s:656` | — |
| **`WriteParam`** | `0x00F7AA` | `0x009BF4` | `os_utilities.s:54` | _WriteParam ($A038) _WriteParam ($A038): write SysParam block to RTC PRAM Writes the 20-byte parameter block, then verifies by reading back |
| **`WRITEPARAM`** | `0x00F7AA` | `0x009BF4` | `os_utilities.s:45` | — |
| **`WRITEPARAM_ERR`** | `0x00F7C8` | `0x009C12` | `os_utilities.s:67`<br>`os_utilities.s:57` | — |
| **`WRITEPARAM_LOOP`** | `0x00F7BE` | `0x009C08` | `os_utilities.s:62`<br>`os_utilities.s:52` | verify: read back and compare |
| **`WRMAIN`** | `0x005080` | `0x006B26` | `file_mgr_io.s:226`<br>`file_mgr_io.s:219` | WrMain: write entire blocks |
| **`WRPART`** | `0x005072` | `0x006B18` | `file_mgr_io.s:219`<br>`file_mgr_io.s:212` | WrPart: must write a partial block first |
| **`XFSearch`** | `0x005F04` | — | `file_mgr_alloc.s:955` | XF Search XFSearch: search extent file for extent mapping a file position |
| **`XFSEARCH_CONT`** | `0x005F82` | `0x007A52` | `file_mgr_alloc.s:996`<br>`file_mgr_alloc.s:866` | FSSchFCB: search FCB extent record first FSSchFile: locate desired record in extents file |
| **`XFSEARCH_CONT_2`** | `0x005FDA` | `0x007AA8` | `file_mgr_alloc.s:1050`<br>`file_mgr_alloc.s:917` | XFSEARCH_CONT_2 XRSearch: search extent record for extent mapping a given FABN D0=desired FABN, A1=ptr to xdr, D3=beginning FABN for record |
| **`XFSEARCH_CONT_3`** | `0x005FFA` | `0x007AC8` | `file_mgr_alloc.s:1067`<br>`file_mgr_alloc.s:934` | — |
| **`XFSEARCH_CONT_4`** | `0x006006` | `0x007AD4` | `file_mgr_alloc.s:1082`<br>`file_mgr_alloc.s:948` | XFSEARCH_CONT_4 - XRUpdate: update the current extent record |
| **`XFSEARCH_DONE`** | `0x005FFE` | `0x007ACC` | `file_mgr_alloc.s:1071`<br>`file_mgr_alloc.s:938` | RSExit |
| **`XFSEARCH_DONE_2`** | `0x006038` | `0x007B06` | `file_mgr_alloc.s:1102`<br>`file_mgr_alloc.s:968` | — |
| **`XFSEARCH_EMPTY`** | `0x005FF4` | `0x007AC2` | `file_mgr_alloc.s:1063`<br>`file_mgr_alloc.s:930` | — |
| **`XFSEARCH_ERR`** | `0x005FD0` | `0x007A9E` | `file_mgr_alloc.s:1038`<br>`file_mgr_alloc.s:906` | Called by: VXFSEARCH, XFSEARCH_OK, XFSEARCH_LOOP_2 |
| **`XFSEARCH_ERR_2`** | `0x00603A` | `0x007B08` | `file_mgr_alloc.s:1104`<br>`file_mgr_alloc.s:970` | — |
| **`XFSEARCH_EXIT`** | `0x006000` | `0x007ACE` | `file_mgr_alloc.s:1073`<br>`file_mgr_alloc.s:940` | — |
| **`XFSEARCH_FOUND`** | `0x005F9E` | `0x007A6E` | `file_mgr_alloc.s:1015`<br>`file_mgr_alloc.s:883` | XFSEARCH_FOUND FSCopyRec: found extent record, copy key and data into FXM vars |
| **`XFSEARCH_FOUND_2`** | `0x005FCE` | `0x007A9C` | `file_mgr_alloc.s:1036`<br>`file_mgr_alloc.s:903` | FSSchRec: search record for desired extent entry FSExit |
| **`XFSEARCH_LOOP`** | `0x005FA6` | `0x007A76` | `file_mgr_alloc.s:1019`<br>`file_mgr_alloc.s:887` | — |
| **`XFSEARCH_LOOP_2`** | `0x005FB4` | `0x007A84` | `file_mgr_alloc.s:1025`<br>`file_mgr_alloc.s:893` | — |
| **`XFSEARCH_LOOP_3`** | `0x006028` | `0x007AF6` | `file_mgr_alloc.s:1096`<br>`file_mgr_alloc.s:961` | — |
| **`XFSEARCH_NO`** | `0x005FE0` | `0x007AAE` | `file_mgr_alloc.s:1054`<br>`file_mgr_alloc.s:921` | — |
| **`XFSEARCH_NO_2`** | `0x006018` | `0x007AE6` | `file_mgr_alloc.s:1090`<br>`file_mgr_alloc.s:955` | RUUpdFile: re-locate and update extent file record |
| **`XFSEARCH_OK`** | `0x005F8E` | `0x007A5E` | `file_mgr_alloc.s:1002`<br>`file_mgr_alloc.s:871` | FSMissed: didn't find extent record, return pointing to last extent in FCB |
| **`ZERO_KEYMAP`** | `0x0026DA` | `0x003ED4` | `keyboard.s:233`<br>`adb_mgr.s:1373` | Keyboard timeout -- re-initialize and re-query model number ZERO_KEYMAP -- zero the 18-byte KeyMap bitmap. |
| **`ZoneAdjustEnd`** | `0x010862` | `0x00AE20` | `memory_mgr.s:2143` | **Regs:** `Entry: A0 = new end (address of the new 12-byte end block), A6 = zone`<br>ZoneAdjustEnd - move the end of zone A6 up to A0 Entry: A0 = new end (address of the new 12-byte end block), A6 = zone Writes the new end block, turns the old end block and the gap into one free block... |
| **`ZONEADJUSTEND`** | `0x010862` | `0x00AE20` | `memory_mgr.s:1548` | — |
| **`ZONEADJUSTEND_CONT`** | `0x010884` | `0x00AE42` | `memory_mgr.s:2166`<br>`memory_mgr.s:1565` | ZONEADJUSTEND_CONT - grow the application zone by about D0 bytes Rounds D0 up to a multiple of 1K and moves HeapEnd (and the zone end) up by that much, or only up to MaxLimit(ApplLimit) if less room i... |
| **`ZONEADJUSTEND_CONT_2`** | `0x0108BE` | `0x00AE7C` | `memory_mgr.s:2193`<br>`memory_mgr.s:1591` | — |
| **`ZONEADJUSTEND_NO`** | `0x0108B0` | `0x00AE6E` | `memory_mgr.s:2188`<br>`memory_mgr.s:1586` | ZONEADJUSTEND_NO |
| **`ZONEADJUSTEND_OK`** | `0x0108C6` | `0x00AE84` | `memory_mgr.s:2197`<br>`memory_mgr.s:1595` | — |

---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

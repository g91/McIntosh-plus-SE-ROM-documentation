# Debugger Function & Routine Directory

This catalog lists all **145** routines, functions, exception vectors, and labels belonging to the **Debugger** subsystem across the Macintosh Plus (128 KB) and Macintosh SE (256 KB) ROMs.

| Symbol / Routine | Mac Plus Offset | Mac SE Offset | Source File : Line | Description / Prototype |
| :--- | :--- | :--- | :--- | :--- |
| **`ASCII_TO_NIBBLE`** | `0x0016A8` | `0x0018B0` | `microbug.s:423`<br>`microbug.s:391` | ASCII_TO_NIBBLE - convert ASCII hex character in D0 to 0-15 Same algorithm as TN1136's StringToNumber: if > '9', subtract 7 to map 'A'-'F' to 10-15, then mask low nibble. |
| **`CLEAR_SEREGS`** | `0x00106C` | `0x0012BA` | `debugger.s:70`<br>`debugger.s:69` | Zero the register save area used by system error handler |
| **`DBG_CLEANUP`** | `0x0010AE` | `0x0012F2` | `debugger.s:107`<br>`debugger.s:96` | DBG_NO_DEBUGGER - no debugger installed, return error |
| **`DBG_NO_DEBUGGER`** | `0x0010AC` | `0x0012F0` | `debugger.s:105`<br>`debugger.s:94` | DBG_NO_DEBUGGER - no debugger installed, return error |
| **`DbgCmd_AAt`** | `0x001654` | — | `microbug.s:353` | DbgCmd_AAt - Ax command: display/set address register "Ax" displays saved address register x. "Ax expr" sets it. |
| **`DbgCmd_DAt`** | `0x00164C` | — | `microbug.s:344` | DbgCmd_DAt - Dx command: display/set data register "Dx" displays saved data register x. "Dx expr" sets it. Register number extracted from second command char. |
| **`DbgCmd_DM`** | `0x001592` | — | `microbug.s:224` | DbgCmd_DM - Dump Memory command Displays 6 rows of 8 words (96 bytes) starting at the parsed address or the DM continuation address. Format: address followed by 8 hex words per line. |
| **`DbgCmd_FS`** | `0x001612` | — | `microbug.s:308` | DbgCmd_FS - SM (Set Memory) command "SM addr expr..." stores expression values into memory at addr, sizing each store (byte/word/long) based on the expression size (D1 from EVAL_EXPR). After all value... |
| **`DbgCmd_G`** | `0x00156E` | — | `microbug.s:187` | DbgCmd_G - Go command: resume execution at address "G addr" resumes at addr. "G" alone resumes from saved PC. |
| **`DBGCMD_G_RESUME`** | `0x00157C` | `0x001784` | `microbug.s:198`<br>`microbug.s:201` | DBGCMD_G_RESUME - G with no argument: resume from exception point |
| **`DbgCmd_PC`** | `0x00165C` | — | `microbug.s:362` | DbgCmd_PC - PC command: display/set program counter "PC" displays saved PC. "PC expr" sets it. |
| **`DbgCmd_SR`** | `0x001664` | — | `microbug.s:371` | DbgCmd_SR - SR command: display/set status register "SR" displays saved SR. "SR expr" sets it (word-sized). |
| **`DbgCmd_TD`** | `0x00163E` | — | `microbug.s:333` | DbgCmd_TD - Total Display: dump all saved registers Sets DM continuation to SEVarBase (0x3FFC80) so that DM displays the 16 saved registers (D0-D7, A0-A7) plus SP/PC/SR. |
| **`DBGREG_DISPLAY`** | `0x001682` | `0x00188A` | `microbug.s:402`<br>`microbug.s:371` | DBGREG_DISPLAY - display register value from save area |
| **`DBGREG_PARSE_NUM`** | `0x001672` | `0x00187A` | `microbug.s:382`<br>`microbug.s:351` | DBGREG_PARSE_NUM - parse register number and optional value for Dx/Ax |
| **`DBGREG_PARSE_VAL`** | `0x001678` | `0x001880` | `microbug.s:386`<br>`microbug.s:355` | — |
| **`DBGREG_PRINT_LOW`** | `0x0016A2` | `0x0018AA` | `microbug.s:413`<br>`microbug.s:382` | — |
| **`DBGREG_SHOW_WORD`** | `0x001680` | `0x001888` | `microbug.s:396`<br>`microbug.s:364` | DBGREG_SHOW_WORD - SR display: flag for word-sized display |
| **`DEBUGGER`** | `0x000806` | `0x0012C6` | `debugger.s:80` | DEBUGGER - ROM debugger entry point (called via _Debugger trap) Saves all registers to SERegs, checks if external debugger (MacsBug) is installed via MacJmp, dispatches to it. If no debugger, returns ... |
| **`DebugProlog`** | `0x0010CA` | `0x00130E` | `debugger.s:127` | DebugProlog - extract debugger address and status from MacJmp MacJmp is a 32-bit value where the low 24 bits are the debugger entry address and the high byte holds flags (bit 7=active, bit 6=installed... |
| **`DEBUGPROLOG`** | `0x0010CA` | `0x00130E` | `debugger.s:108` | DEBUGPROLOG - extract debugger address and status from MacJmp MacJmp low 24 bits = debugger address, high byte = flags. Returns A1 = debugger entry, CC from flag byte (Z=none, N=active). |
| **`DM_ROW_LOOP`** | `0x0015B0` | `0x0017B8` | `microbug.s:234`<br>`microbug.s:236` | — |
| **`DM_WORD_LOOP`** | `0x0015C4` | `0x0017CC` | `microbug.s:243`<br>`microbug.s:245` | — |
| **`DT_DbgCmdTab`** | `0x00154C` | `0x001754` | `microbug.s:174`<br>`microbug.s:181` | DT_DbgCmdTab - MicroBug command dispatch table Each entry: 2-byte command code, 2-byte offset from table base. '@' (0x40) in low byte = register command (D0-D7 or A0-A7). "G " = Go, "DM" = Dump Memory... |
| **`ERASE_STACK_RECT`** | `0x001588` | `0x001790` | `microbug.s:210`<br>`microbug.s:216` | ERASE_STACK_RECT - erase rectangle area on stack The caller pushes a rect (8 bytes) before calling. ERASE_STACK_RECT pops the return address, calls EraseRect on the stacked rect, then cleans up and ju... |
| **`EVAL_EXPR`** | `0x0016C8` | `0x0018D0` | `microbug.s:465`<br>`microbug.s:431` | EVAL_EXPR - MicroBug expression evaluator Parses the input buffer (A4..A6) and evaluates the expression. Returns: D0 = value, D1 = expression size (1/2/4 bytes), Z=1 if no expression found, Z=0 if val... |
| **`EXCPT_ADDR_ERR`** | `0x00112A` | `0x00136E` | `debugger.s:187`<br>`debugger.s:155` | GenExcps - exception vector dispatch table Each entry is a 2-byte BSR.B to ToDeepShit. The BSR pushes a return address that encodes the exception number (offset / 2 from GenExcps). Vector 2=bus error ... |
| **`EXCPT_CHK`** | `0x001130` | `0x001374` | `debugger.s:193`<br>`debugger.s:161` | GenExcps - exception vector dispatch table Each entry is a 2-byte BSR.B to ToDeepShit. The BSR pushes a return address that encodes the exception number (offset / 2 from GenExcps). Vector 2=bus error ... |
| **`EXCPT_DISCARD_FRAME`** | `0x001124` | `0x001368` | `debugger.s:173`<br>`debugger.s:146` | EXCPT_DISCARD_FRAME - debugger was active when exception occurred, discard frame |
| **`EXCPT_ILLEGAL`** | — | `0x001370` | `debugger.s:157` | GENEXCPS - exception vector dispatch table (2-byte BSR entries) Each BSR pushes a return address that encodes the exception ID. |
| **`EXCPT_ILLEGAL_INST`** | `0x00112C` | — | `debugger.s:189` | GenExcps - exception vector dispatch table Each entry is a 2-byte BSR.B to ToDeepShit. The BSR pushes a return address that encodes the exception number (offset / 2 from GenExcps). Vector 2=bus error ... |
| **`EXCPT_LINE_1010`** | `0x001138` | `0x00137C` | `debugger.s:201`<br>`debugger.s:169` | GenExcps - exception vector dispatch table Each entry is a 2-byte BSR.B to ToDeepShit. The BSR pushes a return address that encodes the exception number (offset / 2 from GenExcps). Vector 2=bus error ... |
| **`EXCPT_LINE_1111`** | `0x00113A` | `0x00137E` | `debugger.s:203`<br>`debugger.s:171` | GenExcps - exception vector dispatch table Each entry is a 2-byte BSR.B to ToDeepShit. The BSR pushes a return address that encodes the exception number (offset / 2 from GenExcps). Vector 2=bus error ... |
| **`EXCPT_PRIVILEGE`** | `0x001134` | `0x001378` | `debugger.s:197`<br>`debugger.s:165` | GenExcps - exception vector dispatch table Each entry is a 2-byte BSR.B to ToDeepShit. The BSR pushes a return address that encodes the exception number (offset / 2 from GenExcps). Vector 2=bus error ... |
| **`EXCPT_REGS_SAVED`** | `0x0010EE` | `0x001332` | `debugger.s:152`<br>`debugger.s:127` | — |
| **`EXCPT_SHARED`** | `0x00113E` | — | `debugger.s:207` | GenExcps - exception vector dispatch table Each entry is a 2-byte BSR.B to ToDeepShit. The BSR pushes a return address that encodes the exception number (offset / 2 from GenExcps). Vector 2=bus error ... |
| **`EXCPT_STD_FRAME`** | `0x001110` | `0x001354` | `debugger.s:163`<br>`debugger.s:138` | — |
| **`EXCPT_TO_SYSERR`** | `0x001126` | `0x00136A` | `debugger.s:175`<br>`debugger.s:148` | — |
| **`EXCPT_TRACE`** | `0x001136` | `0x00137A` | `debugger.s:199`<br>`debugger.s:167` | GenExcps - exception vector dispatch table Each entry is a 2-byte BSR.B to ToDeepShit. The BSR pushes a return address that encodes the exception number (offset / 2 from GenExcps). Vector 2=bus error ... |
| **`EXCPT_TRAPV`** | `0x001132` | `0x001376` | `debugger.s:195`<br>`debugger.s:163` | GenExcps - exception vector dispatch table Each entry is a 2-byte BSR.B to ToDeepShit. The BSR pushes a return address that encodes the exception number (offset / 2 from GenExcps). Vector 2=bus error ... |
| **`EXCPT_UNASSIGNED`** | `0x00113C` | `0x001380` | `debugger.s:205`<br>`debugger.s:173` | GenExcps - exception vector dispatch table Each entry is a 2-byte BSR.B to ToDeepShit. The BSR pushes a return address that encodes the exception number (offset / 2 from GenExcps). Vector 2=bus error ... |
| **`EXCPT_ZERO_DIV`** | — | `0x001372` | `debugger.s:159` | GENEXCPS - exception vector dispatch table (2-byte BSR entries) Each BSR pushes a return address that encodes the exception ID. |
| **`EXCPT_ZERO_DIVIDE`** | `0x00112E` | — | `debugger.s:191` | GenExcps - exception vector dispatch table Each entry is a 2-byte BSR.B to ToDeepShit. The BSR pushes a return address that encodes the exception number (offset / 2 from GenExcps). Vector 2=bus error ... |
| **`EXPR_ACCUMULATE`** | `0x001742` | `0x00194A` | `microbug.s:550`<br>`microbug.s:516` | — |
| **`EXPR_CHECK_DOT`** | `0x00176E` | `0x001976` | `microbug.s:583`<br>`microbug.s:548` | EXPR_CHECK_DOT - check for '.' (dot address) or register tokens |
| **`EXPR_CHECK_HEX`** | `0x001706` | `0x00190E` | `microbug.s:510`<br>`microbug.s:474` | EXPR_CHECK_HEX - check for '$' hex prefix or bare hex number |
| **`EXPR_CHECK_NEG`** | `0x001738` | `0x001940` | `microbug.s:546`<br>`microbug.s:512` | — |
| **`EXPR_CHECK_NEXT`** | `0x001756` | `0x00195E` | `microbug.s:561`<br>`microbug.s:528` | — |
| **`EXPR_CHECK_OP`** | `0x0016F2` | `0x0018FA` | `microbug.s:498`<br>`microbug.s:463` | EXPR_CHECK_OP - check for +/- operators between terms |
| **`EXPR_CHECK_PC`** | `0x001786` | `0x00198E` | `microbug.s:605`<br>`microbug.s:569` | EXPR_CHECK_PC - check for "PC" (program counter) token |
| **`EXPR_CHECK_RD`** | `0x0017D0` | `0x0019D8` | `microbug.s:645`<br>`microbug.s:607` | EXPR_CHECK_RD - check for "RDx" (data register) token |
| **`EXPR_CHECK_REG`** | `0x00179C` | `0x0019A4` | `microbug.s:619`<br>`microbug.s:582` | EXPR_CHECK_REG - check for "RAx" or "RDx" register tokens |
| **`EXPR_CHECK_SIZE`** | `0x001750` | `0x001958` | `microbug.s:557`<br>`microbug.s:524` | Compute expression size from digit count |
| **`EXPR_DEREF_LOOP`** | `0x00172C` | `0x001934` | `microbug.s:540`<br>`microbug.s:506` | — |
| **`EXPR_FINALIZE`** | `0x001726` | `0x00192E` | `microbug.s:536`<br>`microbug.s:502` | EXPR_FINALIZE - finalize current term: apply indirection and negate |
| **`EXPR_HEX_LOOP`** | `0x001712` | `0x00191A` | `microbug.s:522`<br>`microbug.s:487` | EXPR_HEX_LOOP - hex digit accumulation loop Converts each ASCII char to 0-15 via ASCII_TO_NIBBLE (forgiving: any char that isn't a digit just contributes its low nibble, which is why "G FINDER" evalua... |
| **`EXPR_NEW_TERM`** | `0x0016CC` | `0x0018D4` | `microbug.s:472`<br>`microbug.s:438` | EXPR_NEW_TERM - start parsing a new term in the expression |
| **`EXPR_NEXT_TERM`** | `0x001762` | `0x00196A` | `microbug.s:566`<br>`microbug.s:533` | — |
| **`EXPR_READ_REGNUM`** | `0x0017B0` | `0x0019B8` | `microbug.s:629`<br>`microbug.s:592` | EXPR_READ_REGNUM - read register number and fetch saved value |
| **`EXPR_RETURN`** | `0x001768` | `0x001970` | `microbug.s:574`<br>`microbug.s:540` | EXPR_RETURN - expression complete: return value and size |
| **`EXPR_SCAN_PREFIX`** | `0x0016E0` | `0x0018E8` | `microbug.s:485`<br>`microbug.s:451` | — |
| **`EXPR_SKIP_CHARS`** | `0x00177E` | `0x001986` | `microbug.s:595`<br>`microbug.s:560` | — |
| **`EXPR_SKIP_SPACE`** | `0x0016DA` | `0x0018E2` | `microbug.s:482`<br>`microbug.s:448` | EXPR_SKIP_SPACE - skip whitespace and control chars in input |
| **`EXPR_TOKEN_DONE`** | `0x00177C` | `0x001984` | `microbug.s:593`<br>`microbug.s:558` | EXPR_TOKEN_DONE - common path for '.', PC, and register tokens D1 = value, D2 = chars to consume from input buffer. |
| **`GenExcps`** | `0x001128` | `0x00136C` | `debugger.s:185` | GenExcps - exception vector dispatch table Each entry is a 2-byte BSR.B to ToDeepShit. The BSR pushes a return address that encodes the exception number (offset / 2 from GenExcps). Vector 2=bus error ... |
| **`GENEXCPS`** | `0x001128` | `0x00136C` | `debugger.s:153` | GENEXCPS - exception vector dispatch table (2-byte BSR entries) Each BSR pushes a return address that encodes the exception ID. |
| **`HEX_DIGIT_OK`** | `0x001608` | `0x001810` | `microbug.s:292`<br>`microbug.s:293` | — |
| **`IRQexception`** | `0x001140` | `0x001384` | `debugger.s:209` | — |
| **`IRQEXCEPTION`** | `0x001140` | `0x001384` | `debugger.s:178` | IRQEXCEPTION - autovector interrupt exception (fatal: shouldn't happen) |
| **`MICROBUG_CHECK_KEY`** | `0x0014C4` | `0x0016CC` | `microbug.s:88`<br>`microbug.s:93` | — |
| **`MICROBUG_CMD_CMP`** | `0x00153C` | `0x001744` | `microbug.s:157`<br>`microbug.s:162` | — |
| **`MICROBUG_CMD_DONE`** | `0x001548` | `0x001750` | `microbug.s:162`<br>`microbug.s:167` | — |
| **`MICROBUG_CMD_LOOP`** | `0x001522` | `0x00172A` | `microbug.s:146`<br>`microbug.s:151` | — |
| **`MICROBUG_ENTRY`** | `0x001452` | `0x00165A` | `microbug.s:38`<br>`microbug.s:37` | MicroBug -- the built-in ROM debugger Entered from SysErr2 (os/sys_error.s) when no external debugger (MacsBug) is installed and the programmer's switch is pressed. Provides a hex expression parser an... |
| **`MICROBUG_EXEC_CMD`** | `0x001516` | `0x00171E` | `microbug.s:139`<br>`microbug.s:144` | MICROBUG_EXEC_CMD - Return pressed: parse and dispatch command If input is empty, re-submit the previous command (D7). Otherwise read the first two chars as command code and look up in DT_DbgCmdTab fo... |
| **`MICROBUG_FILL_BUF`** | `0x00148E` | `0x001696` | `microbug.s:59`<br>`microbug.s:62` | Fill input buffer with spaces (34 bytes, top-down) |
| **`MICROBUG_KEY_LOOP`** | `0x0014AA` | `0x0016B2` | `microbug.s:78`<br>`microbug.s:83` | MICROBUG_KEY_LOOP - keyboard input loop: read characters into buffer Polls for keyboard events, converts lowercase to uppercase, handles Return (execute), Backspace (delete), and printable chars. Inpu... |
| **`MICROBUG_PARSE_CMD`** | `0x00151C` | `0x001724` | `microbug.s:143`<br>`microbug.s:148` | — |
| **`MICROBUG_PROMPT`** | `0x00147A` | `0x001682` | `microbug.s:53`<br>`microbug.s:55` | MICROBUG_PROMPT - MicroBug prompt: clear input line, draw ">" prompt |
| **`MICROBUG_STORE_CH`** | `0x001508` | `0x001710` | `microbug.s:123`<br>`microbug.s:128` | MICROBUG_STORE_CH - store printable character in buffer and echo it |
| **`NIBBLE_IS_DIGIT`** | `0x0016B6` | `0x0018BE` | `microbug.s:428`<br>`microbug.s:396` | — |
| **`P_DbgCmd_DM`** | — | `0x00179A` | `microbug.s:226` | P_DbgCmd_DM - "DM" (Dump Memory): display hex memory dump Shows 6 rows of 8 words each, starting at parsed address or continuation from last DM command. |
| **`P_DbgCmd_FS`** | — | `0x00181A` | `microbug.s:304` | P_DbgCmd_FS (SM) - "SM" (Set Memory): write values to memory Parses address, then reads hex values separated by spaces and stores them byte-by-byte at the target address. After all values are written,... |
| **`P_DbgCmd_G`** | — | `0x001776` | `microbug.s:195` | P_DbgCmd_G - "G " (Go): resume execution at address If expression given, jumps to that address. If empty, resumes from the saved exception PC. |
| **`P_DbgCmd_PC`** | — | `0x001864` | `microbug.s:336` | P_DbgCmd_Dn - "D0"-"D7": display/set data register P_DbgCmd_An - "A0"-"A7": display/set address register P_DbgCmd_PC - "PC" (Program Counter): display or set saved PC |
| **`P_DbgCmd_SR`** | — | `0x00186C` | `microbug.s:341` | P_DbgCmd_SR - "SR" (Status Register): display or set saved SR |
| **`P_DbgCmd_TD`** | — | `0x001846` | `microbug.s:325` | P_DbgCmd_TD - "TD" (Total Display): dump all saved registers Sets continuation to SERegs ($3FFC80) and falls into DM. |
| **`P_Debugger`** | `0x001082` | — | `debugger.s:88` | P_Debugger - ROM debugger entry point (called via _Debugger trap or NMI) (MacSEROM.lst names this code DEBUGGER; MacPlusROM.lst lists Debugger at the unimplemented-trap handler, where that name is a l... |
| **`PARSE_ADDR_OR_CONT`** | `0x0016BC` | `0x0018C4` | `microbug.s:438`<br>`microbug.s:405` | PARSE_ADDR_OR_CONT - parse address, defaulting to DM continuation address If the user typed an expression, returns it in D0. Otherwise returns the DM continuation address (for "DM" alone). |
| **`PARSE_ADDR_RTS`** | `0x0016C6` | `0x0018CE` | `microbug.s:442`<br>`microbug.s:409` | — |
| **`PRINT_HEX_BYTE`** | `0x0015F0` | `0x0017F8` | `microbug.s:277`<br>`microbug.s:278` | PRINT_HEX_BYTE - print 8-bit hex value (2 digits) |
| **`PRINT_HEX_LONG`** | `0x0015E2` | `0x0017EA` | `microbug.s:260`<br>`microbug.s:261` | PRINT_HEX_LONG - print 32-bit hex value (8 digits) Prints D0 as 8 hex digits by printing high word then low word. |
| **`PRINT_HEX_NIBBLE`** | `0x0015F8` | `0x001800` | `microbug.s:286`<br>`microbug.s:287` | PRINT_HEX_NIBBLE - print single hex nibble (low 4 bits of D0) |
| **`PRINT_HEX_WORD`** | `0x0015E8` | `0x0017F0` | `microbug.s:268`<br>`microbug.s:269` | PRINT_HEX_WORD - print 16-bit hex value (4 digits) |
| **`SCC_INIT_PARAMS`** | `0x0018B8` | — | `microbug.s:840` | SCC_INIT_PARAMS - SCC initialization parameters for serial debugger 8 register/value pairs for Zilog 8530 SCC setup: WR4=0x4C (x16 clock, 2 stop bits), WR14=0x00 (BRG off), WR11=0x50 (RxC=BRG, TxC=BRG... |
| **`SERIAL_CHK_INUSE`** | `0x0018E6` | — | `microbug.s:869` | SERIAL_CHK_INUSE - check if serial port is currently in use |
| **`SERIAL_CHK_NIBBLE`** | `0x0018D8` | — | `microbug.s:857` | — |
| **`SERIAL_CMD_EXEC`** | `0x001898` | — | `microbug.s:802` | SERIAL_CMD_EXEC - serial execute: jump to address received from remote |
| **`SERIAL_CMD_LOOP`** | `0x001832` | — | `microbug.s:715` | SERIAL_CMD_LOOP - serial command receive loop Waits for a command byte from the remote debugger, dispatches via SERIAL_CMD_TABLE jump table. Commands: 0=nop, 1=ack, 2=send mem, 3=read mem, 4=write mem... |
| **`SERIAL_CMD_NOP`** | `0x001852` | — | `microbug.s:740` | SERIAL_CMD_NOP - serial NOP/ping: send 0 byte back |
| **`SERIAL_CMD_READ`** | `0x001858` | — | `microbug.s:750` | SERIAL_CMD_READ - serial read memory: send block to remote debugger Receives: 4-byte address, 4-byte count from serial. Sends: command 3, count as long, then count bytes of memory. |
| **`SERIAL_CMD_TABLE`** | `0x001846` | — | `microbug.s:732` | SERIAL_CMD_TABLE - serial command dispatch table (6 word offsets) Entries are PC-relative offsets from SERIAL_CMD_TABLE to handlers: [0] SERIAL_CMD_NOP (nop/ping), [1] SERIAL_CMD_READ (send memory blo... |
| **`SERIAL_CMD_WATCH`** | `0x0018A0` | — | `microbug.s:814` | SERIAL_CMD_WATCH - install A-line trap watcher for serial debugger Saves the current A-line trap vector and installs TRAP_WATCHER as a filter that intercepts traps in a specified number range. The rem... |
| **`SERIAL_CMD_WRITE`** | `0x00187E` | — | `microbug.s:779` | SERIAL_CMD_WRITE - serial write memory: receive block from remote debugger Receives: 4-byte address, 4-byte count, then count data bytes. Writes received bytes into memory at the specified address. |
| **`SERIAL_DBG_ENTRY`** | `0x0017E0` | — | `microbug.s:658` | SERIAL_DBG_ENTRY - serial debugger entry point (external debugger protocol) Called when MicroBug hands off to an external serial debugger. D0 encodes the operation: bit 15 set = specific request, bit ... |
| **`SERIAL_INIT_DELAY`** | `0x001914` | — | `microbug.s:895` | — |
| **`SERIAL_INIT_ERR`** | `0x0018FC` | — | `microbug.s:877` | — |
| **`SERIAL_INIT_PORT`** | `0x0018C8` | — | `microbug.s:851` | SERIAL_INIT_PORT - initialize serial port for debugger communication D0 = port number (1=modem, 2=printer). Checks SPConfig to verify port is configured for serial, and checks PortAUse/PortBUse to ver... |
| **`SERIAL_PORT_RTS`** | `0x001960` | — | `microbug.s:954` | — |
| **`SERIAL_READ_DONE`** | `0x00187C` | — | `microbug.s:770` | SERIAL_READ_DONE - return from serial command handler |
| **`SERIAL_READ_LOOP`** | `0x001870` | — | `microbug.s:759` | — |
| **`SERIAL_RECV_BYTE`** | `0x001970` | — | `microbug.s:979` | SERIAL_RECV_BYTE - receive one byte from SCC serial port Polls SCC RR0 bit 0 (Rx char available). If D1 != 0, a timeout applies (D1 is decremented until negative). Returns received byte in D0.B. N fla... |
| **`SERIAL_RECV_LONG`** | `0x001962` | — | `microbug.s:961` | SERIAL_RECV_LONG - receive 32-bit value from serial (MSB first) |
| **`SERIAL_RECV_WORD`** | `0x00196A` | — | `microbug.s:969` | SERIAL_RECV_WORD - receive 16-bit value from serial (high byte first) |
| **`SERIAL_RX_POLL`** | `0x001972` | — | `microbug.s:981` | — |
| **`SERIAL_RX_READ`** | `0x00197E` | — | `microbug.s:992` | SERIAL_RX_READ - read received byte from SCC data register |
| **`SERIAL_SEND_ACK`** | `0x001828` | — | `microbug.s:703` | SERIAL_SEND_ACK - send acknowledgment, enter serial command loop |
| **`SERIAL_SEND_BLOCK`** | `0x00180A` | — | `microbug.s:685` | SERIAL_SEND_BLOCK - send memory block over serial (response to request) |
| **`SERIAL_SEND_BYTE`** | `0x001936` | — | `microbug.s:930` | SERIAL_SEND_BYTE - send one byte (D0.B) over SCC serial port Waits for transmit buffer empty (SCC RR0 bit 2), then writes byte to SCC data register (control base + 4). Called by: SERIAL_SEND_CMD16, SE... |
| **`SERIAL_SEND_CMD16`** | `0x0017FC` | — | `microbug.s:674` | SERIAL_SEND_CMD16 - send command byte D1 then 16-bit value D0 over serial |
| **`SERIAL_SEND_LONG`** | `0x001924` | — | `microbug.s:908` | SERIAL_SEND_LONG - send 32-bit value over serial (MSB first) |
| **`SERIAL_SEND_LOOP`** | `0x00181C` | — | `microbug.s:692` | — |
| **`SERIAL_SEND_WORD`** | `0x00192E` | — | `microbug.s:918` | SERIAL_SEND_WORD - send 16-bit value over serial (high byte first) |
| **`SERIAL_SET_ACTIVE`** | `0x00182C` | — | `microbug.s:706` | — |
| **`SERIAL_SET_PORT`** | `0x00194A` | — | `microbug.s:946` | SERIAL_SET_PORT - set up SCC register pointers for selected port Returns A0 = SCC write control, A1 = SCC read control. Port 1 (modem) = channel A (+2), port 2 (printer) = channel B. |
| **`SERIAL_SETUP_SCC`** | `0x001900` | — | `microbug.s:887` | SERIAL_SETUP_SCC - configure SCC and establish serial link Programs the SCC with SCC_INIT_PARAMS init params, sends sync byte, waits for response. If no response, returns timeout error. |
| **`SERIAL_TX_POLL`** | `0x00193C` | — | `microbug.s:933` | — |
| **`SERIAL_UNWATCH`** | `0x0018B2` | — | `microbug.s:825` | SERIAL_UNWATCH - uninstall trap watcher (called from TRAP_WATCHER filter) |
| **`SERIAL_USE_MODEM`** | `0x0017F8` | — | `microbug.s:667` | — |
| **`SERIAL_WRITE_DONE`** | `0x001896` | — | `microbug.s:795` | SERIAL_WRITE_DONE - return from serial write handler |
| **`SERIAL_WRITE_LOOP`** | `0x00188A` | — | `microbug.s:784` | — |
| **`SM_PARSE_LOOP`** | `0x001626` | `0x00182E` | `microbug.s:315`<br>`microbug.s:311` | — |
| **`SM_STORE_LOOP`** | `0x001630` | `0x001838` | `microbug.s:319`<br>`microbug.s:315` | — |
| **`SysErrInit`** | `0x001036` | `0x001284` | `debugger.s:40` | 68000 exception handling and the _Debugger trap Apple source: the system error code (System 7.1: StartErr.a; MacSEROM.lst modules SYSERRINIT, DEBUGGER, TODEEPSHIT, GENEXCPS). In ROM order: 1. SysErrIn... |
| **`SYSERRINIT`** | `0x001036` | `0x001284` | `debugger.s:39` | 68000 exception handling and the _Debugger trap Apple source: StartErr.a (MacSEROM.lst modules SYSERRINIT, DEBUGGER, TODEEPSHIT, GENEXCPS). In ROM order: 1. SysErrInit - boot-time install of exception... |
| **`ToDeepShit`** | `0x0010DC` | `0x001320` | `debugger.s:146` | ToDeepShit - fatal exception handler entry point Called via BSR from GenExcps entries. The BSR return address on the stack encodes which exception occurred (offset from GenExcps base / 2 = error ID). ... |
| **`TODEEPSHIT`** | `0x0010DC` | `0x001320` | `debugger.s:122` | TODEEPSHIT - fatal exception handler entry point Called via BSR from GenExcps entries. The BSR return address encodes which exception occurred (offset from GenExcps / 2). Saves registers, extracts exc... |
| **`TRAP_WATCHER`** | `0x001986` | — | `microbug.s:1005` | TRAP_WATCHER - A-line trap watcher (installed by SERIAL_CMD_WATCH) Intercepts A-line traps. If the trap number falls within the watched range (0x3FFCDE..0x3FFCE0), triggers a system error (via GenExcp... |
| **`TRAPWATCH_CHAIN`** | `0x0019BE` | — | `microbug.s:1034` | TRAPWATCH_CHAIN - trap not in watch range: chain to original handler |
| **`TRAPWATCH_CHECK`** | `0x0019A0` | — | `microbug.s:1020` | TRAPWATCH_OS - OS trap: extract 8-bit trap number |
| **`TRAPWATCH_OS`** | `0x00199C` | — | `microbug.s:1018` | TRAPWATCH_OS - OS trap: extract 8-bit trap number |
| **`VECLOOP_IRQ`** | `0x001056` | `0x0012A4` | `debugger.s:59`<br>`debugger.s:58` | Install vectors 25-31: autovector interrupts (levels 1-7) |
| **`VECLOOP_TRAP`** | `0x00105E` | `0x0012AC` | `debugger.s:64`<br>`debugger.s:63` | Install vectors 32-63: TRAP instructions + reserved vectors |
| **`VECLOOP_UNASSIGNED`** | `0x00104A` | `0x001298` | `debugger.s:53`<br>`debugger.s:52` | Install vectors 12-24: all point to same unassigned exception handler |
| **`VECLOOP_UNIQUE`** | `0x001040` | `0x00128E` | `debugger.s:47`<br>`debugger.s:46` | Install vectors 2-11: each GenExcps entry is 2 bytes apart (BSR.B ToDeepShit) so the BSR offset encodes which exception triggered the error. |

---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

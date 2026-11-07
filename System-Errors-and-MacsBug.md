# System Error Handler & Resident Debugger

## 1. Overview of System Error Handling

When the classic Macintosh experiences an unrecoverable hardware exception or fatal software fault (such as a bus error, zero divide, stack overflow, or memory exhaustion), normal user interface subsystems cannot be trusted to handle the condition. The application heap may be corrupted, the stack may have collided with the heap, or the Window Manager may be in an invalid state.

The **System Error Handler** (`plus/os/sys_error.s` and `se/os/sys_error.s`) provides an emergency crash-reporting mechanism designed to run under absolute worst-case conditions. Known affectionately in early Apple internal documentation as **DSAlert** ("Deep Shit Alert"), it displays the iconic **Macintosh Bomb Box** and error identification codes.

---

## 2. Emergency Screen Display: The Bomb Box

When `_SysError` (`$A9C9`) is called, it bypasses the entire user interface stack:
- It **does not allocate memory** from any heap zone.
- It **does not rely on QuickDraw** or the Window Manager.
- It uses its own minimal 1-bit line and font rendering routines directly targeting the screen frame buffer at `ScrnBase` (`$0824`).

```
+-------------------------------------------------------------+
|                                                             |
|   +----+                                                    |
|   | ** |   Sorry, a system error occurred.                  |
|   | || |                                                    |
|   +----+   "Application Name"                               |
|   (BOMB)   unimplemented trap error                         |
|                                                             |
|            +---------+                  +---------+         |
|            | Restart |                  | Resume  |         |
|            +---------+                  +---------+         |
+-------------------------------------------------------------+
```

### The System Error Alert Table
The error text strings and layout specifications are stored in low memory and ROM in the System Error Alert Table (`DSAlertTab` at `$02BA`):
- Each entry defines:
  - Alert box dimensions (centered on 512 x 342 display).
  - Icon to display (Bomb icon, Note icon, Stop icon).
  - Primary text string or error ID number.
  - Buttons enabled: "Restart" (always available) and "Resume" (enabled only if the application provided a resume vector at `RestProc` `$0A8C`).

---

## 3. System Error Codes Directory

| Error ID | Symbol | Name & Cause |
| :--- | :--- | :--- |
| **`1`** | `dsBusError` | **Bus Error**: Attempted memory access to non-existent physical address. |
| **`2`** | `dsAddressErr` | **Address Error**: Attempted 16-bit word or 32-bit longword access on an odd byte boundary (strict 68000 hardware limitation). |
| **`3`** | `dsIllInst` | **Illegal Instruction**: CPU encountered an invalid opcode byte. |
| **`4`** | `dsZeroDiv` | **Zero Divide**: Integer division by zero attempted in assembly or runtime. |
| **`5`** | `dsChkErr` | **Check Instruction**: 68000 `CHK` instruction bounds check failed. |
| **`6`** | `dsOvflowErr` | **Trapv Instruction**: 68000 `TRAPV` overflow condition trapped. |
| **`7`** | `dsPrivErr` | **Privilege Violation**: Attempted execution of supervisor-only opcode in user mode. |
| **`8`** | `dsTraceErr` | **Trace Exception**: CPU trace bit set without active debugger. |
| **`9`** | `dsLine1010` | **Line 1010 Trap**: EMT1010 trap failed or reached corrupt vector. |
| **`10`** | `dsLine1111` | **Line 1111 Trap**: Unimplemented F-line opcode (often FPU instructions on 68000). |
| **`11`** | `dsMiscErr` | **Miscellaneous Hardware Exception**: Unassigned exception vector. |
| **`12`** | `dsUnimpTrap` | **Core Trap Not Available**: Executed unassigned A-line trap word. |
| **`13`** | `dsSpuriousInt` | **Spurious Interrupt**: Bus error during interrupt acknowledge cycle. |
| **`15`** | `dsLoadErr` | **Segment Loader Error**: Failed to read required `'CODE'` resource from disk. |
| **`25`** | `dsMemFullErr` | **Out of Memory**: Heap compaction and purging failed to satisfy allocation. |
| **`26`** | `dsDirNFErr` | **Directory Not Found**: Catalog search failed on critical system path. |
| **`27`** | `dsBadHdrErr` | **Menu Bar Damaged**: Menu list or MBDF handle corrupted. |
| **`28`** | `dsStkNFloErr` | **Stack Overflow**: Stack collided with Application Heap ceiling (`ApplLimit`). |

---

## 4. Resident Debugger: MicroBug & MacsBug

The ROM includes a built-in resident low-level machine language debugger known as **MicroBug** (`plus/debugger/microbug.s` and `se/debugger/microbug.s`):
- If the full disk-based **MacsBug** debugger is installed in the System Folder, the boot loader hooks the debug vector `MacJmp` (`$0120`) to point to MacsBug.
- If no disk debugger is present, hitting the **Programmer's Interrupt Switch** on the side of the Macintosh case (or calling `_Debugger` `$A9FF` / `_DebugStr` `$ABFF`) drops directly into **MicroBug**.

### MicroBug Capabilities
MicroBug runs with all interrupts masked, directly writing text onto the screen:
- **`DM <address> [count]`**: Dump Memory in hexadecimal and ASCII.
- **`SM <address> <val> ...`**: Set Memory bytes.
- **`DR`**: Display all CPU registers (D0-D7, A0-A7, SR, PC, USP, SSP).
- **`SR <reg> <val>`**: Set Register contents.
- **`IL <address>`**: Disassemble 68000 instructions into mnemonic assembly.
- **`G [address]`**: Go (Resume execution at address).
- **`ES`**: Exit to Shell (recover control by launching Finder).
- **`RB`**: Reboot system.


---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

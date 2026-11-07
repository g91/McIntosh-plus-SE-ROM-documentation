# The A-Line Trap Dispatcher & Exception Architecture

## 1. Overview of the Trap Dispatch Mechanism

The central nervous system of the Macintosh operating system is the **A-Line Trap Dispatcher**. The Motorola 68000 architecture reserves opcodes with the upper 4 bits set to binary `1010` (`$Axxx`) and `1111` (`$Fxxx`) as unimplemented instructions. When the CPU encounters an instruction starting with nibble `$A`, it generates an **EMT1010 (Line 1010 Emulator)** exception and branches to the vector at address `$000028` (`ATrapVector`).

The ROM kernel uses this mechanism to provide an extensible, table-driven Application Binary Interface (ABI) for all operating system and user interface calls.

```
+-------------------------------------------------------------+
| 68000 Application Code executes:                            |
| $A11E   (_NewPtr)                                           |
+-------------------------------------------------------------+
                              |
                              v  (Hardware Exception)
+-------------------------------------------------------------+
| CPU saves SR and PC onto stack; vectors to $000028          |
+-------------------------------------------------------------+
                              |
                              v
+-------------------------------------------------------------+
| EMT1010_TrapDispatch (plus/os/trap_dispatch.s:30)            |
| 1. Read trap word from PC location                          |
| 2. Inspect Bit 11: OS Trap (0) vs Toolbox Trap (1)          |
| 3. Mask trap number                                         |
| 4. Fetch routine address from RAM Dispatch Table            |
| 5. Handle register saving or auto-pop                       |
| 6. Jump to target handler                                   |
+-------------------------------------------------------------+
          /                                         \
         / (Bit 11 = 0)                              \ (Bit 11 = 1)
        v                                             v
+-------------------------------+             +-------------------------------+
| OS Trap Handler               |             | Toolbox Trap Handler          |
| - DispatchTab at $0400        |             | - ToolDispTable at $0C00 (Plus)|
| - 256 entries                 |             |   or $0E00 (SE) - 512 entries |
| - Preserves D1-D2, A1-A2      |             | - Pascal stack conventions    |
| - Returns result in D0 / A0   |             | - Evaluates Auto-Pop (Bit 10) |
+-------------------------------+             +-------------------------------+
```

---

## 2. Trap Word Bit Encoding

Every A-line instruction is a 16-bit word encoded according to Inside Macintosh:

```
 15  14  13  12  11  10   9   8   7   6   5   4   3   2   1   0
+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+
| 1 | 0 | 1 | 0 | T |   Flags   |          Trap Number          |
+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+---+
```

### 2.1 OS Traps (`Bit 11 = 0`)
OS traps manage kernel services like memory allocation, file I/O, device drivers, and resources.
- **Bit 11 = 0**: Identifies an OS trap.
- **Bit 10**: Asynchronous / System Heap flag.
  - In I/O calls: `0` = Synchronous (wait for completion), `1` = Asynchronous (return immediately).
  - In Memory Manager calls: `1` = Allocate in System Heap rather than Application Heap.
- **Bit 9**: Clear memory / reserved flag.
  - In `_NewPtr` / `_NewHandle`: `1` = Zero-fill allocated memory block.
- **Bit 8**: Don't preserve register `A0`.
  - `0`: Register `A0` is preserved across the trap call.
  - `1`: Routine returns a pointer in register `A0` (e.g. `_NewPtr`, `_NewHandle`).
- **Bits 0 - 7**: 8-bit trap index (0 to 255), indexing the **OS Dispatch Table** at `$0400`.

### 2.2 Toolbox Traps (`Bit 11 = 1`)
Toolbox traps provide user interface functions (Windows, Menus, Dialogs, QuickDraw).
- **Bit 11 = 1**: Identifies a Toolbox trap.
- **Bit 10**: **Auto-Pop Bit**.
  - If set to `1`, the dispatcher discards (pops) the return address of the glue routine from the stack before calling the handler, allowing direct return to the caller.
- **Bits 0 - 8**: 9-bit trap index (0 to 511), indexing the **Toolbox Dispatch Table** at `$0C00` (Plus) or `$0E00` (SE).

---

## 3. Dissecting `EMT1010_TrapDispatch`

The actual assembly implementation from `plus/os/trap_dispatch.s`:

```assembly
| EMT1010 - 68000 Line 1010 Emulator (trap dispatcher)
EMT1010_TrapDispatch:
        SUBQ.L  #0x2,SP                         | Align stack to match 68020 frame
TRAP_COMMON:
        MOVEM.L D1-D2/A2,-(SP)                  | Save working registers
        MOVE.L  0x10(SP),A2                     | A2 = PC from exception frame (points past trap)
        MOVE    (A2)+,D2                        | D2 = trap word; advance PC past it
        MOVE.L  A2,0x10(SP)                     | Store updated PC as return address
        MOVE    D2,D1                           | D1 = copy of trap word
        ANDI    #0x1FF,D2                       | D2 = trap number (bits 0-8 masked)
        CMPI    #-0x5800,D1                     | Test bit 11: $A800 unsigned
        BCS.B   TRAP_OS_PATH                    | Branch if OS trap (bit 11 = 0)

| Toolbox Dispatch Path
        LEA.L   (ToolDispTable).w,A2            | A2 = base of Toolbox dispatch table
        LSL     #0x2,D2                         | D2 = trap number * 4 (longword index)
        MOVE.L  0x0(A2,D2.W),0xC(SP)            | Store handler address on stack
        CMPI    #-0x5400,D1                     | Test bit 10 (auto-pop)
        MOVEM.L (SP)+,D1-D2/A2                  | Restore working registers
        BCS.B   TRAP_TBOX_DISPATCH              | Branch if auto-pop bit is clear
        MOVE.L  (SP)+,(SP)                      | Auto-pop: discard return address
TRAP_TBOX_DISPATCH:
        RTS                                     | Jump to Toolbox handler

| OS Trap Dispatch Path
TRAP_OS_PATH:
        LEA.L   (DispatchTab).w,A2              | A2 = base of OS dispatch table ($0400)
        BCLR    #0x8,D2                         | Test and clear bit 8: save A0?
        BNE.B   TRAP_OS_NOSAVEREG               | If set, don't save A0
        MOVEM.L D3-D7/A3-A6,-(SP)               | Save full register set
        ...
```

### 68020+ Architecture Compatibility
Notice the first instruction:
```assembly
Dispatch:
        MOVE.L  0x2(SP),0x4(SP)                 | Shift PC down over format/vector word
        BRA.B   TRAP_COMMON
EMT1010_TrapDispatch:
        SUBQ.L  #0x2,SP                         | Adjust stack for 68000 4-byte frame
```
On a Motorola 68000, an exception pushes a 6-byte stack frame: Status Register (word) + Program Counter (longword). On the 68010/68020/68030, an additional 2-byte vector offset / format word is pushed. The dispatcher transparently adjusts the stack pointer so that the same ROM code executes identically on 68000 and 68020/030 accelerator cards!

---

## 4. RAM Dispatch Tables & Trap Patching

A fundamental design requirement of the Macintosh operating system was the ability to fix bugs or extend ROM functionality using software disk patches without burning new ROM chips.

### Table Locations in Low Memory
- **`DispatchTab`** (`$0400` - `$07FF`): 256 longword entries for OS traps `$A000` through `$A0FF`.
- **`ToolDispTable`**:
  - Mac Plus: `$0C00` - `$13FF` (512 longword entries for Toolbox traps `$A800` through `$A9FF`).
  - Mac SE: `$0E00` - `$15FF` (512 longword entries).

### Initialization at Startup
During boot (`os/dispatch_table.s`), the kernel reads a compressed table of relative offsets stored in ROM (`DT_DispatchTbl`) and expands it into the RAM tables at `$0400` and `$0C00`/`$0E00`.

### Trap Patching via `_GetTrapAddress` & `_SetTrapAddress`
System software patches ROM routines by modifying the entry in the RAM dispatch table:
- **`_GetTrapAddress`** (`$A146`):
  - Input: `D0.W` = Trap number.
  - Output: `A0` = Pointer to current handler routine in RAM or ROM.
- **`_SetTrapAddress`** (`$A047`):
  - Input: `D0.W` = Trap number, `A0` = Pointer to replacement handler in RAM.
  - Operation: Overwrites the table slot. When application software executes the trap, control flows to the patch. The patch can either completely replace the routine or "chain" back to the original ROM address.

---

## 5. Unimplemented Trap Handling

If an application invokes an unassigned trap number, the dispatch table points to `UnimpTrap` (`sys_error.s`).
- `UnimpTrap` calls `_SysError` with System Error code `12` (`dsUnimpTrap`).
- The system halts and presents the classic Bomb Box: *"An error occurred: Unimplemented trap instruction."*


---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

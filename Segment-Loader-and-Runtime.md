# Segment Loader & Application Runtime Environment

## 1. Overview of the Segment Loader

The classic Macintosh operating system operates on a segmented code model. Because early Macintosh computers had very limited RAM (128 KB or 512 KB), application code could not be loaded into memory all at once. Instead, the compiler and linker divided programs into discrete **`CODE` resources** (numbered 1, 2, 3...).

The **Segment Loader** (`plus/os/segment_loader.s` and `se/os/segment_loader.s`) manages dynamic loading, execution, and purging of executable code segments, and governs application launching and teardown.

---

## 2. The Application `A5` World

Every running Macintosh application is centered around the contents of CPU register **`A5`**. When an application launches, the Segment Loader establishes the **A5 World**:

```
High Memory (Top of Application Space)
+---------------------------------------------------------------+
| Application Dynamic Stack (Grows Downward)                    |
+---------------------------------------------------------------+
                                |
                                v
                   [ Heap / Stack Boundary ]
                                ^
                                |
+---------------------------------------------------------------+
| Application Global Variables                                  |
| (Referenced as Positive Offsets from A5: e.g. 8(A5), 12(A5))  |
+---------------------------------------------------------------+
| Jump Table (Compiled CODE 0 header)                           |
| (Referenced as Positive Offsets: 0(A5) to jumpTableSize(A5))  |
+---------------------------------------------------------------+ <--- A5 Register
| Application Parameters (32 bytes)                             |
+---------------------------------------------------------------+
| QuickDraw Globals (206 bytes):                                |
| - thePort    (-4(A5)): Pointer to current GrafPort            |
| - white      (-8(A5)): Standard white pattern                 |
| - black      (-16(A5)): Standard black pattern                |
| - gray       (-24(A5)): 50% gray pattern                      |
| - ltGray     (-32(A5)): Light gray pattern                    |
| - dkGray     (-40(A5)): Dark gray pattern                     |
| - arrow      (-108(A5)): Standard mouse arrow cursor          |
| - screenBits (-122(A5)): Display screen bitmap descriptor     |
| - randSeed   (-126(A5)): Pseudo-random number generator seed  |
+---------------------------------------------------------------+
Low Memory
```

Register `CurrentA5` (`$0904`) stores the base pointer of the current A5 world. When interrupt handlers or desk accessories run, they must save and restore `A5` before calling Toolbox routines.

---

## 3. The Jump Table & Dynamic Segment Loading

The application's `CODE` resource 0 is never executed directly; instead, it defines the **Jump Table**. Every cross-segment function call compiles to a `JSR` into an 8-byte entry in the Jump Table:

```
Unloaded State Entry (8 bytes):
+--------------------+--------------------+--------------------+
| Segment # (Word)   | Trap Word: $A9F0   | Offset in Segment  |
+--------------------+--------------------+--------------------+
                      (_LoadSeg)
```

### The `_LoadSeg` Transition
1. When code calls a routine residing in an unloaded segment, execution hits the `_LoadSeg` trap instruction (`$A9F0`).
2. The Segment Loader intercepts the call, reads the segment number from the Jump Table entry, and calls `_GetResource('CODE', segNum)`.
3. It locks the segment handle in memory via `_HLock`.
4. **Patching the Jump Table**: The loader rewrites the 8-byte Jump Table entry from the unloaded state into a loaded state:
```
Loaded State Entry (8 bytes):
+--------------------+--------------------+--------------------+
| Segment # (Word)   | JMP Opcode: $4EF9  | Absolute Address   |
+--------------------+--------------------+--------------------+
```
5. It executes the newly patched `JMP`, transferring control to the target routine. Subsequent calls jump directly to the code with **zero loader overhead**!

### Unloading Segments (`_UnloadSeg`)
To reclaim memory under memory pressure, applications call `_UnloadSeg`:
```pascal
UnloadSeg(@MyRoutine);
```
The loader reads the Jump Table entry, restores the original `_LoadSeg` trap instruction, unlocks the `'CODE'` resource handle, and marks it purgeable.

---

## 4. Application Launch & Termination API

- **`Launch` / `_Launch`** (`$A9F2`):
  - *Entry*: `A0` = Pointer to `LaunchParamBlock` (specifying file name and volume).
  - *Operation*:
    1. Closes all open disk resource files (preserving ROM and System file).
    2. Purges the Application Heap Zone and resets `ApplLimit` (`$0130`).
    3. Opens the application's resource fork.
    4. Loads `CODE` 0 into the bottom of the Application Heap to build the Jump Table.
    5. Sets up the A5 register.
    6. Loads `CODE` 1 (the main entry point).
    7. Sets up the stack pointer and jumps to the application's starting instruction.
- **`Chain` / `_Chain`** (`$A9F3`):
  - Similar to `_Launch`, but preserves the current resource map and application global variables, allowing multi-application chaining.
- **`ExitToShell`** (`$A9F4`):
  - Terminates the current application. Frees all allocated memory, purges pending events, unmounts temporary working directories, and launches the default shell (typically the Finder).


---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

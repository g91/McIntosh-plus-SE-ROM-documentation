# A-Line Trap Reference Catalog

## 1. Overview of the Trap Reference

This catalog lists the core Operating System and Toolbox A-line traps implemented in the Macintosh Plus (128 KB) and Macintosh SE (256 KB) ROMs.

- **OS Traps (`$A000` - `$A7FF`)**: Bit 11 = 0. Handled via `DispatchTab` at `$0400`. Pass parameters in 68000 registers (`A0` for pointers/blocks, `D0` for sizes/selectors). Return result codes in `D0.W`.
- **Toolbox Traps (`$A800` - `$AFFF`)**: Bit 11 = 1. Handled via `ToolDispTable` at `$0C00` (Plus) or `$0E00` (SE). Use Pascal stack-based calling conventions (parameters pushed before call, return value returned on stack).

---

## 2. Memory Manager Traps

| Trap | Code | Macro | Type | Parameters / Registers | Description |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **`$A019`** | `0xA019` | `_InitZone` | OS | `(startPtr, limitPtr, cMoreMasters, pGrowZone)` | Initializes a new heap zone. |
| **`$A02C`** | `0xA02C` | `_InitApplZone` | OS | None | Initializes the Application Heap Zone. |
| **`$A057`** | `0xA057` | `_SetApplBase` | OS | `A0` = startPtr | Sets lower boundary of Application Heap. |
| **`$A02D`** | `0xA02D` | `_SetApplLimit` | OS | `A0` = limitPtr | Sets maximum growth ceiling of Application Heap. |
| **`$A11E`** | `0xA11E` | `_NewPtr` | OS | `D0` = size $\rightarrow$ `A0` = Ptr, `D0` = err | Allocates a non-relocatable block. |
| **`$A01F`** | `0xA01F` | `_DisposPtr` | OS | `A0` = Ptr $\rightarrow$ `D0` = err | Deallocates a non-relocatable block. |
| **`$A020`** | `0xA020` | `_SetPtrSize` | OS | `A0` = Ptr, `D0` = newSize $\rightarrow$ `D0` = err | Resizes a non-relocatable block. |
| **`$A021`** | `0xA021` | `_GetPtrSize` | OS | `A0` = Ptr $\rightarrow$ `D0` = size | Returns logical byte size of a pointer block. |
| **`$A122`** | `0xA122` | `_NewHandle` | OS | `D0` = size $\rightarrow$ `A0` = Handle, `D0` = err | Allocates a relocatable block and Master Pointer. |
| **`$A023`** | `0xA023` | `_DisposHandle` | OS | `A0` = Handle $\rightarrow$ `D0` = err | Deallocates a relocatable block. |
| **`$A024`** | `0xA024` | `_SetHandleSize` | OS | `A0` = Handle, `D0` = newSize $\rightarrow$ `D0` = err | Resizes a relocatable block (may compact heap). |
| **`$A025`** | `0xA025` | `_GetHandleSize` | OS | `A0` = Handle $\rightarrow$ `D0` = size | Returns logical size of a handle block. |
| **`$A126`** | `0xA126` | `_HandleZone` | OS | `A0` = Handle $\rightarrow$ `A0` = ZonePtr | Returns pointer to zone owning the handle. |
| **`$A027`** | `0xA027` | `_ReallocHandle` | OS | `A0` = Handle, `D0` = size $\rightarrow$ `D0` = err | Reallocates a purged handle block. |
| **`$A028`** | `0xA028` | `_RecoverHandle` | OS | `A0` = Ptr $\rightarrow$ `A0` = Handle | Derives handle from block pointer. |
| **`$A029`** | `0xA029` | `_HLock` | OS | `A0` = Handle $\rightarrow$ `D0` = err | Locks relocatable block in memory. |
| **`$A02A`** | `0xA02A` | `_HUnlock` | OS | `A0` = Handle $\rightarrow$ `D0` = err | Unlocks relocatable block (can move during compaction). |
| **`$A04A`** | `0xA04A` | `_HNoPurge` | OS | `A0` = Handle $\rightarrow$ `D0` = err | Marks block non-purgeable. |
| **`$A04B`** | `0xA04B` | `_HPurge` | OS | `A0` = Handle $\rightarrow$ `D0` = err | Marks block purgeable under memory pressure. |
| **`$A04C`** | `0xA04C` | `_CompactMem` | OS | `D0` = cbNeeded $\rightarrow$ `D0` = maxContig | Compacts heap zone by sliding relocatable blocks. |
| **`$A04D`** | `0xA04D` | `_PurgeMem` | OS | `D0` = cbNeeded | Purges purgeable blocks until room is available. |
| **`$A040`** | `0xA040` | `_ResrvMem` | OS | `D0` = cbNeeded | Reserves contiguous space at bottom of heap. |
| **`$A11D`** | `0xA11D` | `_MaxMem` | OS | None $\rightarrow$ `D0` = maxBytes, `A0` = growBytes | Calculates absolute maximum single allocation. |
| **`$A064`** | `0xA064` | `_MoveHHi` | OS | `A0` = Handle $\rightarrow$ `D0` = err | Moves relocatable block to top of zone before locking. |

---

## 3. Device Manager Traps

| Trap | Code | Macro | Type | Parameters | Description |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **`$A000`** | `0xA000` | `_Open` | OS | `A0` = ParmBlkPtr $\rightarrow$ `D0` = err | Opens a device driver by name string. |
| **`$A001`** | `0xA001` | `_Close` | OS | `A0` = ParmBlkPtr $\rightarrow$ `D0` = err | Closes an open device driver. |
| **`$A002`** | `0xA002` | `_Read` | OS | `A0` = ParmBlkPtr $\rightarrow$ `D0` = err | Reads data bytes from a device. |
| **`$A003`** | `0xA003` | `_Write` | OS | `A0` = ParmBlkPtr $\rightarrow$ `D0` = err | Writes data bytes to a device. |
| **`$A004`** | `0xA004` | `_Control` | OS | `A0` = ParmBlkPtr $\rightarrow$ `D0` = err | Sends control command to driver (`csCode`). |
| **`$A005`** | `0xA005` | `_Status` | OS | `A0` = ParmBlkPtr $\rightarrow$ `D0` = err | Queries driver status information. |
| **`$A006`** | `0xA006` | `_KillIO` | OS | `A0` = ParmBlkPtr $\rightarrow$ `D0` = err | Terminates pending and active I/O requests. |

---

## 4. File Manager Traps

| Trap | Code | Macro | Type | Parameters | Description |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **`$A008`** | `0xA008` | `_Create` | OS | `A0` = ParmBlkPtr $\rightarrow$ `D0` = err | Creates an empty file in catalog. |
| **`$A009`** | `0xA009` | `_Delete` | OS | `A0` = ParmBlkPtr $\rightarrow$ `D0` = err | Deletes a closed file or empty directory. |
| **`$A00A`** | `0xA00A` | `_OpenRF` | OS | `A0` = ParmBlkPtr $\rightarrow$ `D0` = err | Opens the Resource Fork of a file. |
| **`$A00C`** | `0xA00C` | `_GetFileInfo` | OS | `A0` = ParmBlkPtr $\rightarrow$ `D0` = err | Reads file attributes, Type, Creator, dates. |
| **`$A00D`** | `0xA00D` | `_SetFileInfo` | OS | `A0` = ParmBlkPtr $\rightarrow$ `D0` = err | Writes updated Finder attributes. |
| **`$A00F`** | `0xA00F` | `_MountVol` | OS | `A0` = ParmBlkPtr $\rightarrow$ `D0` = err | Mounts an inserted disk volume. |
| **`$A010`** | `0xA010` | `_Allocate` | OS | `A0` = ParmBlkPtr $\rightarrow$ `D0` = err | Allocates contiguous blocks to open file. |
| **`$A011`** | `0xA011` | `_GetEOF` | OS | `A0` = ParmBlkPtr $\rightarrow$ `D0` = err | Gets logical file length. |
| **`$A012`** | `0xA012` | `_SetEOF` | OS | `A0` = ParmBlkPtr $\rightarrow$ `D0` = err | Sets logical file length. |
| **`$A014`** | `0xA014` | `_GetVolInfo` | OS | `A0` = ParmBlkPtr $\rightarrow$ `D0` = err | Returns volume size and free block metrics. |
| **`$A200`** | `0xA200` | `_OpenWD` | OS | `A0` = WDPBPtr $\rightarrow$ `D0` = err | Opens an HFS Working Directory. |
| **`$A201`** | `0xA201` | `_CloseWD` | OS | `A0` = WDPBPtr $\rightarrow$ `D0` = err | Closes an HFS Working Directory. |
| **`$A205`** | `0xA205` | `_CatMove` | OS | `A0` = CMovePBPtr $\rightarrow$ `D0` = err | Moves a file/folder across directories. |

---

## 5. Apple Desktop Bus (ADB) Traps (Mac SE Exclusive)

| Trap | Code | Macro | Type | Parameters | Description |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **`$A077`** | `0xA077` | `_CountADBs` | OS | None $\rightarrow$ `D0.W` = count | Returns number of active ADB devices on bus. |
| **`$A078`** | `0xA078` | `_GetIndADB` | OS | `D0` = index $\rightarrow$ `D0` = addr, `A0` = info | Gets ADB device table entry by index. |
| **`$A079`** | `0xA079` | `_GetADBInfo` | OS | `D0` = addr, `A0` = info $\rightarrow$ `D0` = err | Gets device handler and service routine address. |
| **`$A07A`** | `0xA07A` | `_SetADBInfo` | OS | `D0` = addr, `A0` = info $\rightarrow$ `D0` = err | Installs custom ADB device handler. |
| **`$A07B`** | `0xA07B` | `_ADBReInit` | OS | None | Resets bus and re-enumerates all ADB devices. |
| **`$A07C`** | `0xA07C` | `_ADBOp` | OS | `A0` = parm, `D0` = cmd $\rightarrow$ `D0` = err | Sends raw asynchronous Talk/Listen/Reset command. |
| **`$A9C3`** | `0xA9C3` | `_KeyTranslate`| TB | Pascal stack | Translates ADB scancode to ASCII via `'KCHR'`. |

---

## 6. Toolbox Window & Menu Traps

| Trap | Code | Macro | Type | Parameters | Description |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **`$A912`** | `0xA912` | `_InitWindows` | TB | Stack | Initializes Window Manager and desktop port. |
| **`$A913`** | `0xA913` | `_NewWindow` | TB | Stack $\rightarrow$ `WindowPtr` | Creates an on-screen or off-screen window. |
| **`$A914`** | `0xA914` | `_DisposeWindow`| TB | Stack | Closes and frees a window record. |
| **`$A915`** | `0xA915` | `_ShowWindow` | TB | Stack | Makes a window visible on screen. |
| **`$A916`** | `0xA916` | `_HideWindow` | TB | Stack | Hides a window from view. |
| **`$A91F`** | `0xA91F` | `_SelectWindow` | TB | Stack | Brings window to front and highlights title bar. |
| **`$A92C`** | `0xA92C` | `_FindWindow` | TB | Stack $\rightarrow$ partCode | Hit-tests screen coordinate against window parts. |
| **`$A930`** | `0xA930` | `_InitMenus` | TB | Stack | Initializes Menu Manager and desktop menu bar. |
| **`$A931`** | `0xA931` | `_NewMenu` | TB | Stack $\rightarrow$ `MenuHandle` | Allocates a new empty menu record. |
| **`$A935`** | `0xA935` | `_InsertMenu` | TB | Stack | Inserts menu into global menu bar list. |
| **`$A937`** | `0xA937` | `_DrawMenuBar` | TB | Stack | Redraws desktop menu bar at top of screen. |
| **`$A93D`** | `0xA93D` | `_MenuSelect` | TB | Stack $\rightarrow$ menuResult | Tracks mouse pulling down menus; returns Choice. |


---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

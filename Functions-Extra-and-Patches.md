# Extra & Patches Function & Routine Directory

This catalog lists all **67** routines, functions, exception vectors, and labels belonging to the **Extra & Patches** subsystem across the Macintosh Plus (128 KB) and Macintosh SE (256 KB) ROMs.

| Symbol / Routine | Mac Plus Offset | Mac SE Offset | Source File : Line | Description / Prototype |
| :--- | :--- | :--- | :--- | :--- |
| **`DRVTBL`** | — | `0x03561C` | `res_drvr_sony.s:2337` | DrvTbl -- icon and drive information for physical drives 1-5 (the 1987 SE driver's table): offset of the media icon, offset of the drive icon and the drive info word returned by csCode 23 (Inside Maci... |
| **`EXTRA_CONT`** | `0x01FFC0` | — | `extra.s:33` | Plus v1/v2: opening of the developer-initials easter egg (16 bytes). Plus v3: SCSI-patch subroutine (16 bytes) -- overwrites the 16-char prefix of the easter egg. Invoked via `JSR (0x41FFC0).l` from I... |
| **`FDHD_RAMTestPatch`** | — | — | `rom_tail.s:1554` | RAM-test patch (entry 13, $43D034), not part of the driver: the cold start code in boot/memtest.s jumps here instead of running the RAM test (test phase 14) directly, with A6 pointing to a word that h... |
| **`FDHD_RAMTESTPATCH_LOOP`** | — | — | `rom_tail.s:1559` | — |
| **`FDHD_ResourceTailPatchCode`** | — | — | `rom_tail.s:44` | — |
| **`ICON_DISKETTE`** | — | `0x0356B8` | `res_drvr_sony.s:2431` | Icons -- 32x32 icon and mask, followed by an empty Pascal string (the "Where:" string of the Finder's Get Info window) and a pad byte, the same four icons as in the 1987 SE driver: the 3.5-inch disket... |
| **`ICON_EXTDRIVE`** | — | `0x0357BA` | `res_drvr_sony.s:2501` | 3.5-inch diskette (media icon of all drives): mask external drive (drive 3): icon |
| **`ICON_LOWERDRIVE`** | — | `0x0358BC` | `res_drvr_sony.s:2570` | external drive (drive 3): mask lower internal drive of the Macintosh SE (drive 1): icon |
| **`ICON_UPPERDRIVE`** | — | `0x0359BE` | `res_drvr_sony.s:2639` | lower internal drive of the Macintosh SE (drive 1): mask upper internal drive of the Macintosh SE (drive 2): icon |
| **`MacSEFDHD_ROM_End`** | — | — | `rom_tail.s:1579` | — |
| **`ROMTail_BuildDate_Thu_Nov_20_1986`** | — | `0x03FFEE` | `rom_tail.s:27` | The date at a fixed place: if the ROM resources grow into the tail, the .org stops the assembly ("attempt to move .org backwards"; shorten the initials above to make room); if they shrink, it pads wit... |
| **`ROMTail_BuildDate_Tue_Oct_11_1988`** | — | — | `rom_tail.s:1574` | — |
| **`ROMTail_Initials_FDHD`** | — | — | `rom_tail.s:32` | SE FDHD: the initials string from $3CBA8 up to the patch code at $3D000 |
| **`ROMTail_Initials_FDHD_2`** | — | — | `rom_tail.s:1567` | the initials string again from $3DD52 (in phase with the copy at $3CBA8: the patch code was written over the filled tail) up to $3FFED |
| **`ROMTail_Initials_SE`** | — | `0x03CBA8` | `rom_tail.s:18` | — |
| **`SONY_CTL_DRIVEICON`** | — | `0x035648` | `res_drvr_sony.s:2375` | — |
| **`SONY_CTL_DRIVEICON_ADD`** | — | — | `rom_tail.s:1494` | — |
| **`SONY_CTL_DRVINFO`** | — | `0x035658` | `res_drvr_sony.s:2382` | — |
| **`SONY_CTL_DRVINFO_NEW`** | — | — | `rom_tail.s:1507` | — |
| **`SONY_CTL_ICONRET`** | — | `0x03567A` | `res_drvr_sony.s:2395` | — |
| **`SONY_CTL_MEDIAICON`** | — | `0x03563A` | `res_drvr_sony.s:2368` | upper internal drive of the Macintosh SE (drive 2): mask ctlLogIcon (csCode 22), ctlPhysIcon (csCode 21), ctlDrvInfo (csCode 23) for floppy drives (csCode 23 also for HD20s), entered from the control ... |
| **`SONY_CTL_MEDIAICON_ADD`** | — | — | `rom_tail.s:1483` | — |
| **`SONY_CTL_PARAM`** | — | `0x035674` | `res_drvr_sony.s:2392` | Branch from: SONY_CTL_MEDIAICON_ADD, SONY_CTL_DRIVEICON_ADD, SONY_CTL_DRVINFO, SONY_CTL_DRVINFO_NEW |
| **`SONY_CTLFORMAT_BUILD`** | — | — | `rom_tail.s:686` | — |
| **`SONY_CTLFORMAT_CHKFMT`** | — | — | `rom_tail.s:652` | — |
| **`SONY_CTLFORMAT_GCR`** | — | — | `rom_tail.s:708` | — |
| **`SONY_CTLFORMAT_NEXT`** | — | — | `rom_tail.s:710` | — |
| **`SONY_CTLFORMAT_SELECT`** | — | — | `rom_tail.s:665` | — |
| **`SONY_CTLFORMAT_SETCHIP`** | — | — | `rom_tail.s:660` | — |
| **`SONY_CTLVERIFY_GCR`** | — | — | `rom_tail.s:1051` | — |
| **`SONY_CTLVERIFY_NEXT`** | — | — | `rom_tail.s:1053` | — |
| **`SONY_CTLVERIFY_START`** | — | — | `rom_tail.s:1031` | — |
| **`SONY_GETDRVTBL`** | — | `0x03567E` | `res_drvr_sony.s:2400` | getDrvTbl -- A3 -> DrvTbl entry (in the table drvTblPtr points to) of the physical drive behind the current logical drive (the drive number was checked by the dispatcher) |
| **`SONY_RDADDR_GCR`** | — | — | `rom_tail.s:193` | — |
| **`SONY_RDADDRXIT`** | — | `0x035BB0` | `res_drvr_sony.s:2863` | Branch from: SONY_RDADDR_CONT, SONY_RDADDR_SKIP_2, SONY_RDADDR_ERR_2, SONY_RDADDR_ERR_3, SONY_RDDATA_SKIP |
| **`SONY_RDDATA_GCR`** | — | — | `rom_tail.s:322` | — |
| **`SONY_SETDRVTBL`** | — | — | `rom_tail.s:1535` | SetDrvTbl -- drvTblPtr (SonyVars+$178) = DRVTBL; called by DiskOpen with A0 = SonyVars |
| **`SONY_TAIL_DISKDONE`** | — | — | `rom_tail.s:1540` | complete the request: jump to DiskDone in the driver |
| **`TAIL_DRV_ADRANDSENSE`** | — | — | `rom_tail.s:123` | — |
| **`TAIL_DRV_ADRDISK`** | — | — | `rom_tail.s:108` | Jump table into the driver: absolute jumps to the driver's entry table SONY_DRVENT_* (one per routine the tail code calls) |
| **`TAIL_DRV_DISKSELECT`** | — | — | `rom_tail.s:121` | — |
| **`TAIL_DRV_DSKRTN`** | — | — | `rom_tail.s:115` | — |
| **`TAIL_DRV_DSKRWOFF`** | — | — | `rom_tail.s:127` | — |
| **`TAIL_DRV_EMPTYPD`** | — | — | `rom_tail.s:131` | — |
| **`TAIL_DRV_GETDRV1`** | — | — | `rom_tail.s:111` | Called by: E_Sony_RdAddr, E_Sony_RdData, SONY_CTLFORMAT_MARKS_2, SONY_CTLFORMAT_TRACKLOOP, SONY_CTLFORMAT_NEXT (and 5 more) |
| **`TAIL_DRV_GETFREQ1`** | — | — | `rom_tail.s:137` | — |
| **`TAIL_DRV_MFMTTRACK`** | — | — | `rom_tail.s:125` | — |
| **`TAIL_DRV_MRDADDR`** | — | — | `rom_tail.s:113` | — |
| **`TAIL_DRV_MRDDATA`** | — | — | `rom_tail.s:117` | — |
| **`TAIL_DRV_MVERTRACK`** | — | — | `rom_tail.s:129` | — |
| **`TAIL_DRV_RWPOWERUP`** | — | — | `rom_tail.s:135` | — |
| **`TAIL_DRV_SEEK`** | — | — | `rom_tail.s:133` | — |
| **`TAIL_DRV_SETCHIPMODE`** | — | — | `rom_tail.s:119` | — |
| **`TAILENT_CTLFORMAT`** | — | — | `rom_tail.s:81` | SE FDHD .Sony driver, part 2: code in the free space at the end of the ROM ($3D000-$3DD51) The SuperDrive driver (part 1: resources/res_drvr_sony_fdhd.s) did not fit into the $2610-byte resource slot ... |
| **`TAILENT_CTLVERIFY`** | — | — | `rom_tail.s:83` | SE FDHD .Sony driver, part 2: code in the free space at the end of the ROM ($3D000-$3DD51) The SuperDrive driver (part 1: resources/res_drvr_sony_fdhd.s) did not fit into the $2610-byte resource slot ... |
| **`TAILENT_DRIVEICON`** | — | — | `rom_tail.s:93` | SE FDHD .Sony driver, part 2: code in the free space at the end of the ROM ($3D000-$3DD51) The SuperDrive driver (part 1: resources/res_drvr_sony_fdhd.s) did not fit into the $2610-byte resource slot ... |
| **`TAILENT_DRVINFO`** | — | — | `rom_tail.s:97` | SE FDHD .Sony driver, part 2: code in the free space at the end of the ROM ($3D000-$3DD51) The SuperDrive driver (part 1: resources/res_drvr_sony_fdhd.s) did not fit into the $2610-byte resource slot ... |
| **`TAILENT_E_SETUPPOLL`** | — | — | `rom_tail.s:91` | SE FDHD .Sony driver, part 2: code in the free space at the end of the ROM ($3D000-$3DD51) The SuperDrive driver (part 1: resources/res_drvr_sony_fdhd.s) did not fit into the $2610-byte resource slot ... |
| **`TAILENT_MEDIAICON`** | — | — | `rom_tail.s:95` | SE FDHD .Sony driver, part 2: code in the free space at the end of the ROM ($3D000-$3DD51) The SuperDrive driver (part 1: resources/res_drvr_sony_fdhd.s) did not fit into the $2610-byte resource slot ... |
| **`TAILENT_RAMTEST`** | — | — | `rom_tail.s:101` | SE FDHD .Sony driver, part 2: code in the free space at the end of the ROM ($3D000-$3DD51) The SuperDrive driver (part 1: resources/res_drvr_sony_fdhd.s) did not fit into the $2610-byte resource slot ... |
| **`TAILENT_RDADDR`** | — | — | `rom_tail.s:75` | SE FDHD .Sony driver, part 2: code in the free space at the end of the ROM ($3D000-$3DD51) The SuperDrive driver (part 1: resources/res_drvr_sony_fdhd.s) did not fit into the $2610-byte resource slot ... |
| **`TAILENT_RDADDRSETUP`** | — | — | `rom_tail.s:85` | SE FDHD .Sony driver, part 2: code in the free space at the end of the ROM ($3D000-$3DD51) The SuperDrive driver (part 1: resources/res_drvr_sony_fdhd.s) did not fit into the $2610-byte resource slot ... |
| **`TAILENT_RDDATA`** | — | — | `rom_tail.s:77` | SE FDHD .Sony driver, part 2: code in the free space at the end of the ROM ($3D000-$3DD51) The SuperDrive driver (part 1: resources/res_drvr_sony_fdhd.s) did not fit into the $2610-byte resource slot ... |
| **`TAILENT_READDATA`** | — | — | `rom_tail.s:87` | SE FDHD .Sony driver, part 2: code in the free space at the end of the ROM ($3D000-$3DD51) The SuperDrive driver (part 1: resources/res_drvr_sony_fdhd.s) did not fit into the $2610-byte resource slot ... |
| **`TAILENT_SETDRVTBL`** | — | — | `rom_tail.s:99` | SE FDHD .Sony driver, part 2: code in the free space at the end of the ROM ($3D000-$3DD51) The SuperDrive driver (part 1: resources/res_drvr_sony_fdhd.s) did not fit into the $2610-byte resource slot ... |
| **`TAILENT_SETUPPOLL`** | — | — | `rom_tail.s:79` | SE FDHD .Sony driver, part 2: code in the free space at the end of the ROM ($3D000-$3DD51) The SuperDrive driver (part 1: resources/res_drvr_sony_fdhd.s) did not fit into the $2610-byte resource slot ... |
| **`TAILENT_TOEMPTYPD`** | — | — | `rom_tail.s:89` | SE FDHD .Sony driver, part 2: code in the free space at the end of the ROM ($3D000-$3DD51) The SuperDrive driver (part 1: resources/res_drvr_sony_fdhd.s) did not fit into the $2610-byte resource slot ... |

---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

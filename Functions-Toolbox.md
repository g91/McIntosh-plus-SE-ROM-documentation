# Toolbox Function & Routine Directory

This catalog lists all **2,657** routines, functions, exception vectors, and labels belonging to the **Toolbox** subsystem across the Macintosh Plus (128 KB) and Macintosh SE (256 KB) ROMs.

| Symbol / Routine | Mac Plus Offset | Mac SE Offset | Source File : Line | Description / Prototype |
| :--- | :--- | :--- | :--- | :--- |
| **`AddReference`** | `0x01451E` | `0x00EB42` | `resource_mgr.s:3023` | **Proto:** `PROCEDURE AddReference(theResource: Handle; theID: INTEGER; name: Str255)`<br>_AddReference ($A9AC): obsolete trap, kept as a stub that always fails PROCEDURE AddReference(theResource: Handle; theID: INTEGER; name: Str255) (signature as given in System 7.1 ResourceMgr.a) Pops i... |
| **`ADDREFERENCE`** | `0x01451E` | `0x00EB42` | `resource_mgr.s:2873` | _AddReference ($A9CB) -- vestigial, returns addRefFailed (-195). |
| **`AddResMenu`** | `0x012C20` | `0x00D24C` | `menu_mgr.s:1753` | **Proto:** `Pascal: PROCEDURE AddResMenu(theMenu: MenuHandle; theType: ResType);`<br>_AddResMenu ($A94D): append the names of all resources of a type to a menu Pascal: PROCEDURE AddResMenu(theMenu: MenuHandle; theType: ResType); Inserts afterItem = 999 below the return address and fal... |
| **`ADDRESMENU`** | `0x012C20` | `0x00D24C` | `menu_mgr.s:1423` | **Proto:** `Pascal: procedure AddResMenu(theMenu: MenuHandle; theType: ResType);`<br>_AddResMenu ($A94D): append all resources of a type to a menu. Pascal: procedure AddResMenu(theMenu: MenuHandle; theType: ResType); |
| **`AddResource`** | `0x01460E` | `0x00EC32` | `resource_mgr.s:3178` | _AddResource ($A9AB) stack: handle, type, id, name -> (adds to current file) Called during boot. |
| **`ADDRESOURCE`** | `0x01460E` | `0x00EC32` | `resource_mgr.s:3016` | _AddResource ($A9AB) -- attach a handle as a new resource. Stack: handle(L), type(L), id(W), name(L). Pre-flight checks: handle is non-nil, not already a resource. Allocates ref entry (ADDRESOURCE_CON... |
| **`ADDRESOURCE_CONT`** | `0x014662` | `0x00EC84` | `resource_mgr.s:3210`<br>`resource_mgr.s:3052` | ADDRESOURCE_CONT Called during boot. |
| **`ADDRESOURCE_CONT_2`** | `0x0146AA` | `0x00ECCC` | `resource_mgr.s:3244`<br>`resource_mgr.s:3085` | ADDRESOURCE_CONT_2 Called during boot. |
| **`ADDRESOURCE_CONT_3`** | `0x0146E0` | `0x00ED02` | `resource_mgr.s:3271`<br>`resource_mgr.s:3107` | — |
| **`ADDRESOURCE_EMPTY`** | `0x01467E` | `0x00ECA0` | `resource_mgr.s:3219`<br>`resource_mgr.s:3061` | — |
| **`ADDRESOURCE_ERR`** | `0x01465C` | `0x00EC7E` | `resource_mgr.s:3201`<br>`resource_mgr.s:3039` | — |
| **`ADDRESOURCE_LOOP`** | `0x0146DC` | `0x00ECFE` | `resource_mgr.s:3269`<br>`resource_mgr.s:3105` | ADDRESOURCE_LOOP - adjust ref list offsets after type/ref insertion Called during boot. |
| **`AdjustRunPositions`** | — | `0x0121F6` | `textedit.s:3727` | AdjustRunPositions - adjust char positions in StyleRec from A0+4 onward. In: A0 = first run entry, D0 = run index, D5 = adjustment. Adds D5 to each charPos field in entries from A0+4 to end. Used afte... |
| **`AdjustRunPositions_DONE`** | — | `0x01220A` | `textedit.s:3738` | — |
| **`AdjustRunPositions_LOOP`** | — | `0x012202` | `textedit.s:3733` | — |
| **`Alert`** | `0x014974` | `0x00EF96` | `dialog_mgr.s:153` | **Proto:** `Alert -- _Alert ($A985): FUNCTION Alert (alertID: INTEGER; fi lterPro c : ProcPtr) : INTEGER;`<br>Alert -- _Alert ($A985): FUNCTION Alert (alertID: INTEGER; fi lterPro c : ProcPtr) : INTEGER; _Alert ($A985) |
| **`ALERT`** | `0x014974` | `0x00EF96` | `dialog_mgr.s:145` | _Alert ($A985) -- show plain alert (no icon). |
| **`ALERT_CONT`** | `0x014976` | `0x00EF98` | `dialog_mgr.s:155`<br>`dialog_mgr.s:148` | **Proto:** `Alert -- _Alert ($A985): FUNCTION Alert (alertID: INTEGER; fi lterPro c : ProcPtr) : INTEGER;`<br>Alert -- _Alert ($A985): FUNCTION Alert (alertID: INTEGER; fi lterPro c : ProcPtr) : INTEGER; _Alert ($A985) |
| **`ALERT_CONT_2`** | `0x0149A0` | `0x00EFC2` | `dialog_mgr.s:169`<br>`dialog_mgr.s:162` | — |
| **`ALERT_CONT_3`** | `0x0149A8` | `0x00EFCA` | `dialog_mgr.s:179`<br>`dialog_mgr.s:171` | ALERT_CONT_3 - process alert stage nibble |
| **`ALERT_CONT_4`** | `0x0149C6` | `0x00EFE8` | `dialog_mgr.s:193`<br>`dialog_mgr.s:184` | ALERT_CONT_4 - create and show alert dialog |
| **`ALERT_CONT_5`** | `0x014A68` | `0x00F08A` | `dialog_mgr.s:263`<br>`dialog_mgr.s:256` | ALERT_CONT_5 Called during boot. |
| **`ALERT_CONT_6`** | `0x014A7A` | `0x00F09C` | `dialog_mgr.s:277`<br>`dialog_mgr.s:270` | ALERT_CONT_6 Called during boot. |
| **`ALERT_DISPOSE_UNLOCK`** | — | `0x00F070` | `dialog_mgr.s:237` | — |
| **`ALERT_OK`** | `0x014998` | `0x00EFBA` | `dialog_mgr.s:166`<br>`dialog_mgr.s:159` | — |
| **`ALERT_OK_2`** | `0x014A60` | `0x00F082` | `dialog_mgr.s:253`<br>`dialog_mgr.s:245` | — |
| **`ALERT_SKIP`** | `0x014A14` | `0x00F036` | `dialog_mgr.s:224`<br>`dialog_mgr.s:215` | — |
| **`ALERT_SKIP_2`** | `0x014A4E` | — | `dialog_mgr.s:246` | — |
| **`ALERT_SKIP_3`** | `0x014A8A` | `0x00F0AC` | `dialog_mgr.s:284`<br>`dialog_mgr.s:277` | — |
| **`ALGORITHM`** | `0x01580E` | `0x00FE50` | `fixmath.s:131`<br>`fixmath.s:103` | ALGORITHM - Full unsigned 32x32 multiply using four 16x16 MULUs. Produces 64-bit result in D0 (high) : D4 (low). Algorithm: (D1h:D1l) * (D2h:D2l) using schoolbook multiply. Both operands are magnitude... |
| **`AppendMenu`** | `0x012A1A` | `0x00D046` | `menu_mgr.s:1370` | **Proto:** `Pascal: PROCEDURE AppendMenu(theMenu: MenuHandle; data: Str255);`<br>_AppendMenu ($A933): append one or more items to a menu Pascal: PROCEDURE AppendMenu(theMenu: MenuHandle; data: Str255); Inserts afterItem = 999 below the return address and falls into InsMenuItem: Ap... |
| **`APPENDMENU`** | `0x012A1A` | `0x00D046` | `menu_mgr.s:1089` | **Proto:** `Pascal: procedure AppendMenu(theMenu: MenuHandle; data: Str255);`<br>_AppendMenu ($A933): append items parsed from a Pascal string to a menu. Pascal: procedure AppendMenu(theMenu: MenuHandle; data: Str255); Same metachar parser as InsMenuItem; insertion position = end ... |
| **`ATAN_ABS_DIVIDEND`** | — | `0x0100B8` | `fixmath.s:496` | — |
| **`ATAN_CHK_DVND`** | `0x015AF4` | `0x010130` | `fixmath.s:730`<br>`fixmath.s:553` | — |
| **`ATAN_CHK_DVSR`** | `0x015AE8` | `0x010124` | `fixmath.s:724`<br>`fixmath.s:547` | — |
| **`ATAN_COEFF_TBL`** | `0x015B00` | `0x01013C` | `fixmath.s:744`<br>`fixmath.s:563` | ATAN_COEFF_TBL - arctangent polynomial coefficients at0..at5 (Fract): $3FFFA073 (0.99998), $EAB64EBE (-0.33262), $0C62F72C (0.19354), $F88C77F2 (-0.11643), $035E92FE (0.05265), $FF3FFE62 (-0.01172) Ap... |
| **`ATAN_DEALLOC_RTS`** | — | `0x0100CE` | `fixmath.s:509` | — |
| **`ATAN_DO_DIVIDE`** | `0x015A9E` | — | `fixmath.s:693` | — |
| **`ATAN_DO_FRACDIV`** | — | `0x0100DA` | `fixmath.s:517` | — |
| **`ATAN_DVND_ABS`** | `0x015A78` | — | `fixmath.s:658` | ATAN_DVND_ABS -- rejoin point of Apple's FixTypoInFixAtan2 patch (Plus $15A78) |
| **`ATAN_DVSR_ABS`** | `0x015A6A` | `0x0100AA` | `fixmath.s:650`<br>`fixmath.s:489` | — |
| **`ATAN_DVSR_ZERO`** | `0x015A8E` | `0x0100CC` | `fixmath.s:676`<br>`fixmath.s:507` | ATAN_DVSR_ZERO - x = 0 (with \|y\| > 0): t = 0, so a = 0 and the fix-up gives +-pi/2. ATAN_RESULT_ZERO: also y = 0 (or 0/0) with a = 0. Both drop the reserved area and the pushed value and skip the poly... |
| **`ATAN_NO_SWAP`** | `0x015A98` | `0x0100D4` | `fixmath.s:689`<br>`fixmath.s:513` | ATAN_NO_SWAP - \|y\| <= \|x\|: t = \|y\|/\|x\|. ATAN_DO_DIVIDE: t = FracDiv, t2 = FracMul(t,t), then Horner evaluation from at5 (5 steps) and a final multiply by t; each result replaces the accumulator on the... |
| **`ATAN_POLY_LOOP`** | `0x015AB6` | `0x0100F2` | `fixmath.s:702`<br>`fixmath.s:526` | — |
| **`ATAN_RESTORE_A2`** | `0x015AD6` | `0x010112` | `fixmath.s:717`<br>`fixmath.s:540` | ATAN_RESTORE_A2 (Apple: bypass) -- quadrant fix-up of a = atan(t) in D0 |
| **`ATAN_RESULT_ZERO`** | `0x015A90` | — | `fixmath.s:678` | — |
| **`ATAN_RETURN`** | `0x015AFC` | — | `fixmath.s:734` | — |
| **`ATAN_SIGN_RESULT`** | — | `0x010138` | `fixmath.s:557` | — |
| **`AUTOSCROLL_APPLY`** | `0x016D9E` | `0x012162` | `textedit.s:2117`<br>`textedit.s:3624` | TEPinScroll(dh = D4, dv = D5, hTE) |
| **`AUTOSCROLL_CHECK_BOUNDS`** | — | `0x012142` | `textedit.s:3603` | — |
| **`AUTOSCROLL_DOWN`** | `0x016D96` | `0x01215A` | `textedit.s:2104`<br>`textedit.s:3616` | mouse below: dv = -lineHeight (text moves up) |
| **`AUTOSCROLL_GET_LINE`** | — | `0x012138` | `textedit.s:3599` | — |
| **`AUTOSCROLL_LEFT`** | `0x016D9C` | `0x012160` | `textedit.s:2114`<br>`textedit.s:3622` | mouse left of the view: dh = +lineHeight |
| **`AUTOSCROLL_NONE`** | `0x016D8E` | `0x012152` | `textedit.s:2098`<br>`textedit.s:3612` | TempRect = viewRect grown by 8 pixels (h) and lineHeight/2 (v) InsetRect(TempRect, -8, -(lineHeight/2)) get current mouse position compare the mouse with TempRect: top, left, bottom, right mouse insid... |
| **`AUTOSCROLL_RIGHT`** | `0x016D9A` | `0x01215E` | `textedit.s:2111`<br>`textedit.s:3620` | mouse right of the view: dh = -lineHeight |
| **`AUTOSCROLL_UP`** | `0x016D98` | `0x01215C` | `textedit.s:2107`<br>`textedit.s:3618` | mouse above: dv = +lineHeight (text moves down) |
| **`AUTOVIEW_EXIT`** | `0x016D42` | — | `textedit.s:2045` | — |
| **`AUTOVIEW_OFF`** | `0x016D3C` | `0x0120F8` | `textedit.s:2043`<br>`textedit.s:3567` | — |
| **`AUXLIST_SEARCH`** | — | `0x00C91A` | `window_mgr.s:2560` | SEARCH_AUX_LIST: walk an aux-record list looking for key match. In:  A1 = list head handle stack: result-handle-ptr (long), found-flag-byte (low half of 4-byte slot), key (long), return addr (long) Ou... |
| **`AUXLIST_SEARCH_LOOP`** | — | `0x00C924` | `window_mgr.s:2563` | — |
| **`AUXLIST_SEARCH_STORE`** | — | `0x00C93E` | `window_mgr.s:2575` | — |
| **`BeginUpdate`** | `0x011D16` | `0x00C3B6` | `window_mgr.s:1873` | remove target and reinsert behind specified window _BeginUpDate ($A922) stack: window -> (sets visRgn to updateRgn) Called during boot. _BeginUpdate ($A922): set up for redrawing a window's update reg... |
| **`BEGINUPDATE`** | `0x011D16` | `0x00C3B6` | `window_mgr.s:1748` | remove target and reinsert behind specified window _BeginUpdate ($A922): set up for redrawing a window's update region Saves current visRgn, replaces it with intersection of visRgn and updateRgn. Clea... |
| **`BLITMENUICON_EXIT`** | — | `0x00D37E` | `menu_mgr.s:1565` | — |
| **`BringToFront`** | `0x011C24` | `0x00C2BE` | `window_mgr.s:1740` | **Proto:** `Pascal: procedure BringToFront(theWindow: WindowPtr);`<br>_BringToFront ($A920) stack: window -> (moves in front of all) _BringToFront ($A920): move a window to front of window list Pascal: procedure BringToFront(theWindow: WindowPtr); Accumulates obscured a... |
| **`BRINGTOFRONT`** | `0x011C24` | `0x00C2BE` | `window_mgr.s:1620` | **Proto:** `Pascal: procedure BringToFront(theWindow: WindowPtr);`<br>_BringToFront ($A920): move a window to front of window list Pascal: procedure BringToFront(theWindow: WindowPtr); Accumulates obscured areas from windows above, removes from list, inserts at front, a... |
| **`BRINGTOFRONT_CONT`** | `0x011C28` | `0x00C2C2` | `window_mgr.s:1743`<br>`window_mgr.s:1624` | BRINGTOFRONT_CONT -- bringToFront. |
| **`BRINGTOFRONT_CONT_2`** | `0x011CB6` | `0x00C356` | `window_mgr.s:1815`<br>`window_mgr.s:1697` | BRINGTOFRONT_CONT_2 - negate a point on the stack (reverse an offset) Negates the v and h components of a point at SP+4. Called during boot. |
| **`BRINGTOFRONT_DONE`** | `0x011C80` | — | `window_mgr.s:1782` | — |
| **`BRINGTOFRONT_NEXT`** | — | `0x00C318` | `window_mgr.s:1661` | compute this window's visRgn that overlaps target, in global coords accumulate the overlap into D3 |
| **`BRINGTOFRONT_NO`** | `0x011C44` | `0x00C2DE` | `window_mgr.s:1754`<br>`window_mgr.s:1635` | walk windows above target, accumulating areas that overlap target |
| **`BRINGTOFRONT_OK`** | `0x011CAA` | — | `window_mgr.s:1803` | — |
| **`BRINGTOFRONT_SKIP`** | `0x011C78` | — | `window_mgr.s:1778` | compute this window's visRgn that overlaps target, in global coords accumulate the overlap into D3 |
| **`BRINGTOFRONT_SKIP_2`** | `0x011CA2` | `0x00C342` | `window_mgr.s:1798`<br>`window_mgr.s:1681` | remove target from current position and insert at front repaint newly visible area (unless dragging, which handles it) |
| **`BRINGTOFRONT_UNLINK`** | — | `0x00C320` | `window_mgr.s:1665` | — |
| **`BTN_DONE`** | `0x010F5A` | `0x00B526` | `toolbox_event.s:53`<br>`toolbox_event.s:52` | — |
| **`BUILDBBOX_ALREADY_DONE`** | — | `0x019F1C` | `font_mgr.s:1709` | — |
| **`BUILDBBOX_BODY`** | — | `0x019ED6` | `font_mgr.s:1676` | BUILDBBOX_BODY (= INVERTCOLOR_CONT_3 in Plus): build per-glyph bounding box table appended to the font strike. Scans the strike's bitmap to find the top/bottom ink row of each glyph. Used by QuickDraw... |
| **`BUILDBBOX_BOTTOM_FOUND`** | — | `0x019FDE` | `font_mgr.s:1814` | — |
| **`BUILDBBOX_RESIZE`** | — | `0x019F16` | `font_mgr.s:1705` | — |
| **`BUILDBBOX_WIDE_GLYPH`** | — | `0x019F7C` | `font_mgr.s:1760` | — |
| **`BuildCharTable`** | `0x00F30A` | — | `font_mgr.s:1885` | **Regs:** `Entry: A0 = font handle. Not part of FontMetrics; called by SwapFont`<br>BuildCharTable - build the image height table of a FONT Entry: A0 = font handle. Not part of FontMetrics; called by SwapFont (SWAPFONT_FOUND_3, and SWAPFONT_EXIT after reloading a purged font). Return... |
| **`BUILDCHARTABLE_CONT_4`** | `0x00F350` | `0x019F22` | `font_mgr.s:1926`<br>`font_mgr.s:1718` | BUILDCHARTABLE_CONT_4 - font grown: set fontType bit 0 and fill the image height table, one entry per glyph Called during boot. |
| **`BUILDCHARTABLE_CONT_5`** | `0x00F3AE` | — | `font_mgr.s:1975` | glyph ends inside this word - clear mask bits right of its end BUILDCHARTABLE_CONT_5 - mask table: entry n (n = 0..16) = $FFFF >> n |
| **`BUILDCHARTABLE_CONT_6`** | `0x00F3D0` | — | `font_mgr.s:1983` | BUILDCHARTABLE_CONT_6: glyph continues - extend mask into D0.lo |
| **`BUILDCHARTABLE_CONT_7`** | `0x00F3E8` | `0x019F90` | `font_mgr.s:1997`<br>`font_mgr.s:1771` | BUILDCHARTABLE_CONT_7: scan bitmap rows from top, looking for first ink row |
| **`BUILDCHARTABLE_EMPTY`** | `0x00F40A` | `0x019FB2` | `font_mgr.s:2014`<br>`font_mgr.s:1788` | — |
| **`BUILDCHARTABLE_EXIT`** | `0x00F34A` | — | `font_mgr.s:1916` | — |
| **`BUILDCHARTABLE_FOUND`** | `0x00F40E` | `0x019FB6` | `font_mgr.s:2023`<br>`font_mgr.s:1791` | BUILDCHARTABLE_FOUND: found top ink row - record it, then scan from bottom for last row Called during boot. |
| **`BUILDCHARTABLE_FOUND_2`** | `0x00F438` | — | `font_mgr.s:2053` | BUILDCHARTABLE_FOUND_2 BUILDCHARTABLE_FOUND_2: compute glyph height (bottom - top) and update max Called during boot. |
| **`BUILDCHARTABLE_LOOP`** | `0x00F3F8` | `0x019FA0` | `font_mgr.s:2005`<br>`font_mgr.s:1779` | — |
| **`BUILDCHARTABLE_LOOP_2`** | `0x00F428` | `0x019FCE` | `font_mgr.s:2038`<br>`font_mgr.s:1806` | — |
| **`BUILDCHARTABLE_NEXT`** | `0x00F362` | `0x019F34` | `font_mgr.s:1935`<br>`font_mgr.s:1726` | BUILDCHARTABLE_NEXT: next glyph - init its entry, get image width |
| **`BUILDCHARTABLE_NEXT_2`** | `0x00F370` | `0x019F40` | `font_mgr.s:1942`<br>`font_mgr.s:1733` | BUILDCHARTABLE_NEXT_2: next 16-pixel band - column mask in D0.hi |
| **`BUILDCHARTABLE_NEXT_3`** | `0x00F442` | `0x019FE8` | `font_mgr.s:2058`<br>`font_mgr.s:1819` | — |
| **`BUILDCHARTABLE_NO_2`** | `0x00F346` | — | `font_mgr.s:1913` | compute table offsets and the new font size |
| **`BUILDCHARTABLE_NO_3`** | `0x00F3DA` | `0x019F84` | `font_mgr.s:1989`<br>`font_mgr.s:1765` | — |
| **`BUILDCHARTABLE_NO_4`** | `0x00F416` | `0x019FBC` | `font_mgr.s:2028`<br>`font_mgr.s:1796` | BUILDCHARTABLE_NO_4: scan bitmap rows from bottom up for last ink row |
| **`BuildHilitePattern`** | — | `0x0125C8` | `textedit.s:4289` | BuildHilitePattern - install txMode-derived ASCII pattern at *(A7+4). Used by TextEdit setup (TE_PROLOGUE_NODISP) to build a 6-byte glyph substitution pattern from the GrafPort's source-mode bits (por... |
| **`BuildHilitePattern_Align`** | — | `0x0125DE` | `textedit.s:4297` | — |
| **`BuildHilitePattern_LeaveZero`** | — | `0x0125EA` | `textedit.s:4305` | — |
| **`BuildHilitePattern_LOOP`** | — | `0x0125E2` | `textedit.s:4300` | — |
| **`Button`** | `0x010F4C` | `0x00B518` | `toolbox_event.s:47` | **Proto:** `Pascal: FUNCTION Button: BOOLEAN`<br>_Button ($A974) Pascal: FUNCTION Button: BOOLEAN Returns TRUE if the mouse button is currently down. MBState bit 7 = 1 means button up (hardware active-low); bit 7 = 0 (positive or zero) means button ... |
| **`BUTTON`** | `0x010F4C` | `0x00B518` | `toolbox_event.s:46` | **Proto:** `Pascal: FUNCTION Button: BOOLEAN`<br>_Button ($A974) Pascal: FUNCTION Button: BOOLEAN Returns TRUE if the mouse button is currently down. MBState bit 7 = 1 means button up (hardware active-low); bit 7 = 0 (positive or zero) means button ... |
| **`BYTES`** | — | `0x00FBB6` | `toolbox_utils.s:27` | Toolbox Utilities: byte-string munger, handle/pointer copying and MacApp method dispatch Routines, in physical ROM order: _Munger ($A9E0), _XMunger ($A819)  search/replace/insert/delete bytes in a han... |
| **`CalcMBHeight`** | `0x0121BE` | `0x00C9D6` | `menu_mgr.s:50` | Calc MB Height Called during boot. |
| **`CALCMBHEIGHT`** | `0x0121BE` | `0x00C9D6` | `menu_mgr.s:105` | CalcMBHeight: compute menu bar height from system font ascent+descent. MBarHeight = ascent + descent + 5 (baseline padding) Called during boot. |
| **`CALCMBHEIGHT_CONT`** | `0x0121CE` | — | `menu_mgr.s:64` | CALCMBHEIGHT_CONT Called during boot. |
| **`CALCMBHEIGHT_EMPTY`** | `0x0121E6` | `0x00C9FE` | `menu_mgr.s:81`<br>`menu_mgr.s:134` | CALCMBHEIGHT_EMPTY Called during boot. |
| **`CALCMBHEIGHT_EMPTY_2`** | `0x0121EA` | `0x00CA02` | `menu_mgr.s:85`<br>`menu_mgr.s:138` | CALCMBHEIGHT_EMPTY_2 -- reinitialize to empty list. |
| **`CALCMBHEIGHT_LOOP`** | `0x0121F6` | `0x00CA0E` | `menu_mgr.s:91`<br>`menu_mgr.s:144` | — |
| **`CalcMenuSize`** | `0x012994` | `0x00CFC0` | `menu_mgr.s:1290` | _CalcMenuSize ($A948) _CalcMenuSize ($A948): calculate menu dimensions via MDEF Sends mSizeMsg (2) to the menu's MDEF to compute width/height |
| **`CALCMENUSIZE`** | `0x012994` | `0x00CFC0` | `menu_mgr.s:1023` | **Proto:** `Pascal: procedure CalcMenuSize(theMenu: MenuHandle);`<br>_CalcMenuSize ($A948): force a menu's width/height to be recomputed by calling MDEF msg=2 (calcSize). Standard MDEF then walks the items and stores total dimensions back into the MenuInfo header. Pasc... |
| **`CALCMENUSIZE_EXIT`** | `0x0129B6` | `0x00CFE2` | `menu_mgr.s:1303`<br>`menu_mgr.s:1036` | — |
| **`CALCMENUSIZE_EXIT_2`** | `0x0129C8` | `0x00CFF4` | `menu_mgr.s:1320`<br>`menu_mgr.s:1046` | Tail of an enable-flag check helper (DisableItem-style branch in test). Reads enableFlags long at offset 0xA of MenuInfo. |
| **`CalcVBehind`** | `0x011290` | — | `window_mgr.s:226` | **Proto:** `Pascal: procedure CalcVisBehind(window: WindowPeek; clobberedRgn: RgnHandle);`<br>_CalcVBehind ($A90A) Called during boot. _CalcVBehind ($A90A): recalculate visRgn for window and all behind it Pascal: procedure CalcVisBehind(window: WindowPeek; clobberedRgn: RgnHandle); |
| **`CALCVBEHIND_EMPTY`** | `0x0112CE` | `0x00B91C` | `window_mgr.s:260`<br>`window_mgr.s:257` | optimization: only recalc if clobbered region intersects this window CALCVBEHIND_EMPTY - CalcVBehind epilogue: restore A2 and strip stack params Called during boot. |
| **`CALCVBEHIND_NEXT`** | `0x01129A` | `0x00B8E8` | `window_mgr.s:231`<br>`window_mgr.s:232` | — |
| **`CALCVBEHIND_SKIP`** | `0x01129E` | `0x00B8EC` | `window_mgr.s:235`<br>`window_mgr.s:236` | walk window list behind this one |
| **`CalcVis`** | `0x011238` | `0x00B880` | `window_mgr.s:164` | **Proto:** `Pascal: procedure CalcVis(whichWindow: WindowPeek);`<br>_CalcVis ($A909) _CalcVis ($A909): recalculate a window's visRgn Pascal: procedure CalcVis(whichWindow: WindowPeek); visRgn = intersection of contRgn with desktop minus obscuring windows |
| **`CALCVIS`** | `0x011238` | `0x00B880` | `window_mgr.s:172` | **Proto:** `Pascal: procedure CalcVis(whichWindow: WindowPeek);`<br>_CalcVis ($A909): recalculate a window's visRgn Pascal: procedure CalcVis(whichWindow: WindowPeek); visRgn = intersection of contRgn with desktop minus obscuring windows |
| **`CALCVIS_CONT`** | `0x011272` | `0x00B8C0` | `window_mgr.s:204`<br>`window_mgr.s:208` | CALCVIS_CONT - subtract structure regions of all windows above A2 from D4 Walks the window list front-to-back, subtracting each visible window's strucRgn from D4 until reaching the target window A2. C... |
| **`CALCVIS_DONE`** | `0x011258` | `0x00B8A0` | `window_mgr.s:179`<br>`window_mgr.s:187` | — |
| **`CALCVIS_EXIT`** | `0x011252` | `0x00B89A` | `window_mgr.s:175`<br>`window_mgr.s:183` | invisible window: set visRgn to empty |
| **`CALCVIS_EXIT_2`** | `0x011256` | `0x00B89E` | `window_mgr.s:177`<br>`window_mgr.s:185` | — |
| **`CALCVIS_LOOP`** | `0x011276` | — | `window_mgr.s:206` | — |
| **`CALCVIS_SKIP`** | `0x01128A` | `0x00B8D8` | `window_mgr.s:215`<br>`window_mgr.s:219` | — |
| **`CALCVIS_SUBTRACT_LOOP`** | — | `0x00B8C4` | `window_mgr.s:210` | — |
| **`CALCVIS_VISIBLE`** | `0x01125A` | `0x00B8A2` | `window_mgr.s:186`<br>`window_mgr.s:191` | CalcVis: visible window - compute visRgn from content and desktop |
| **`CALCVISBEHIND`** | — | `0x00B8DE` | `window_mgr.s:227` | **Proto:** `Pascal: procedure CalcVisBehind(window: WindowPeek; clobberedRgn: RgnHandle);`<br>_CalcVBehind ($A90A): recalculate visRgn for window and all behind it Pascal: procedure CalcVisBehind(window: WindowPeek; clobberedRgn: RgnHandle); |
| **`CautionAlert`** | `0x014970` | `0x00EF92` | `dialog_mgr.s:144` | _CautionAlert ($A988) |
| **`CAUTIONALERT`** | `0x014970` | `0x00EF92` | `dialog_mgr.s:139` | _CautionAlert ($A988) -- show caution-icon alert dialog. |
| **`ChangedResource`** | `0x01444C` | `0x00EA68` | `resource_mgr.s:2858` | _ChangedResource ($A9AA) Called during boot. |
| **`CHANGEDRESOURCE`** | `0x01444C` | `0x00EA68` | `resource_mgr.s:2738` | _ChangedResource ($A9AA) -- mark resource as modified. Sets the resChanged bit in the ref entry. If the resource doesn't have its on-disk space reserved (resReserved clear), grows the map handle by 28... |
| **`CHANGEDRESOURCE_AFTER_WRITE`** | — | `0x00EAB8` | `resource_mgr.s:2773` | — |
| **`CHANGEDRESOURCE_CONT`** | `0x014476` | — | `resource_mgr.s:2876` | CHANGEDRESOURCE_CONT - resource is protected, cannot mark changed |
| **`CHANGEDRESOURCE_ERR`** | `0x01447C` | — | `resource_mgr.s:2878` | CHANGEDRESOURCE_CONT - resource is protected, cannot mark changed |
| **`CheckItem`** | `0x0128C4` | `0x00CEF0` | `menu_mgr.s:1140` | _CheckItem ($A945): set/clear checkmark on a menu item |
| **`CHECKITEM`** | `0x0128C4` | `0x00CEF0` | `menu_mgr.s:897` | **Proto:** `Pascal: procedure CheckItem(theMenu: MenuHandle; item: INTEGER; checked: BOOLEAN);`<br>_CheckItem ($A945): set/clear the check mark on a menu item. Pascal: procedure CheckItem(theMenu: MenuHandle; item: INTEGER; checked: BOOLEAN); Implements check-mark by overlaying SetItemMark with mar... |
| **`CHECKITEM_CONT`** | `0x0128D8` | `0x00CF04` | `menu_mgr.s:1161`<br>`menu_mgr.s:911` | CHECKITEM_CONT CHECKITEM_CONT: uppercase a single character in D0 Uses _UprString with length=1 on a temp stack byte |
| **`CHECKITEM_NO`** | `0x0128D2` | `0x00CEFE` | `menu_mgr.s:1151`<br>`menu_mgr.s:903` | CHECKITEM_NO Called during boot (18,470 times in 30s trace). |
| **`CheckLoad`** | `0x014136` | — | `resource_mgr.s:2309` | Check Load Called during boot (22,904 times in 30s trace). |
| **`CHECKLOAD_ALLOC_HANDLE`** | — | `0x00E778` | `resource_mgr.s:2211` | CHECKLOAD_ALLOC_HANDLE: helper -- compute resource data size + reserve memory if locked. |
| **`CHECKLOAD_CONT`** | `0x014168` | — | `resource_mgr.s:2334` | CHECKLOAD_CONT Called during boot. |
| **`CHECKLOAD_CONT_10`** | `0x01424A` | `0x00E85E` | `resource_mgr.s:2506`<br>`resource_mgr.s:2388` | CHECKLOAD_CONT_10 Called during boot. |
| **`CHECKLOAD_CONT_11`** | `0x014252` | `0x00E866` | `resource_mgr.s:2517`<br>`resource_mgr.s:2398` | CHECKLOAD_CONT_11 Called during boot. |
| **`CHECKLOAD_CONT_12`** | `0x01428E` | `0x00E8A2` | `resource_mgr.s:2566`<br>`resource_mgr.s:2453` | CHECKLOAD_CONT_12 Called during boot. |
| **`CHECKLOAD_CONT_13`** | `0x0142A2` | `0x00E8B6` | `resource_mgr.s:2576`<br>`resource_mgr.s:2463` | — |
| **`CHECKLOAD_CONT_14`** | `0x0142A8` | `0x00E8BC` | `resource_mgr.s:2585`<br>`resource_mgr.s:2473` | CHECKLOAD_CONT_14 Called during boot. |
| **`CHECKLOAD_CONT_15`** | `0x0142E8` | `0x00E8FC` | `resource_mgr.s:2625`<br>`resource_mgr.s:2510` | — |
| **`CHECKLOAD_CONT_16`** | `0x0142F6` | `0x00E90A` | `resource_mgr.s:2646`<br>`resource_mgr.s:2531` | CHECKLOAD_CONT_16 Called during boot. |
| **`CHECKLOAD_CONT_17`** | `0x014300` | `0x00E914` | `resource_mgr.s:2652`<br>`resource_mgr.s:2537` | CHECKLOAD_CONT_17 -- place the resource data at the end of the data area. |
| **`CHECKLOAD_CONT_18`** | `0x01432E` | `0x00E942` | `resource_mgr.s:2680`<br>`resource_mgr.s:2568` | CHECKLOAD_CONT_18 Called during boot. |
| **`CHECKLOAD_CONT_19`** | `0x014372` | `0x00E986` | `resource_mgr.s:2719`<br>`resource_mgr.s:2610` | CHECKLOAD_CONT_19 Called during boot. |
| **`CHECKLOAD_CONT_2`** | `0x014184` | `0x00E794` | `resource_mgr.s:2356`<br>`resource_mgr.s:2232` | — |
| **`CHECKLOAD_CONT_20`** | `0x0143B6` | `0x00E9D2` | `resource_mgr.s:2752`<br>`resource_mgr.s:2644` | CHECKLOAD_CONT_20 - validate name list offset against computed position Called during boot. |
| **`CHECKLOAD_CONT_3`** | `0x0141B8` | `0x00E7C8` | `resource_mgr.s:2395`<br>`resource_mgr.s:2273` | CHECKLOAD_CONT_3 - SetPL: master pointer flags of handle A0 from rAttr D1 Called during boot. |
| **`CHECKLOAD_CONT_4`** | `0x0141C2` | `0x00E7D2` | `resource_mgr.s:2408`<br>`resource_mgr.s:2280` | CHECKLOAD_NO_2 - set handle flags for a resource that is not locked Called during boot. |
| **`CHECKLOAD_CONT_5`** | `0x0141CC` | `0x00E7E0` | `resource_mgr.s:2419`<br>`resource_mgr.s:2294` | CHECKLOAD_CONT_5 Called during boot. |
| **`CHECKLOAD_CONT_6`** | `0x0141E2` | `0x00E7F6` | `resource_mgr.s:2435`<br>`resource_mgr.s:2311` | CHECKLOAD_CONT_6 Called during boot. |
| **`CHECKLOAD_CONT_7`** | `0x0141F6` | `0x00E80A` | `resource_mgr.s:2451`<br>`resource_mgr.s:2330` | CHECKLOAD_CONT_7 Called during boot. |
| **`CHECKLOAD_CONT_8`** | `0x01420E` | `0x00E822` | `resource_mgr.s:2465`<br>`resource_mgr.s:2343` | CHECKLOAD_CONT_8 Called during boot. |
| **`CHECKLOAD_CONT_9`** | `0x014230` | `0x00E844` | `resource_mgr.s:2489`<br>`resource_mgr.s:2369` | CHECKLOAD_CONT_9 Called during boot. |
| **`CHECKLOAD_EMPTY`** | `0x01419E` | `0x00E7AE` | `resource_mgr.s:2374`<br>`resource_mgr.s:2249` | CHECKLOAD_EMPTY Called during boot. |
| **`CHECKLOAD_EMPTY_2`** | `0x014254` | `0x00E868` | `resource_mgr.s:2521`<br>`resource_mgr.s:2402` | CHECKLOAD_EMPTY_2 -- write null map at offset 256. Called by: CHECKLOAD_OK_2, CREATERES_CHKEOF, CMP_NEXT_RES, CMP_WRITE_MAP, CMP_FLUSH_BUF |
| **`CHECKLOAD_ERR`** | `0x014196` | `0x00E7A6` | `resource_mgr.s:2364`<br>`resource_mgr.s:2240` | — |
| **`CHECKLOAD_ERR_2`** | `0x0141A8` | `0x00E7B8` | `resource_mgr.s:2381`<br>`resource_mgr.s:2256` | — |
| **`CHECKLOAD_ERR_3`** | `0x01425A` | `0x00E86E` | `resource_mgr.s:2525`<br>`resource_mgr.s:2406` | — |
| **`CHECKLOAD_ERR_4`** | `0x01436C` | `0x00E980` | `resource_mgr.s:2710`<br>`resource_mgr.s:2598` | — |
| **`CHECKLOAD_ERR_5`** | `0x0143C0` | `0x00E9DC` | `resource_mgr.s:2764`<br>`resource_mgr.s:2655` | CHECKLOAD_ERR_5 - map validation failed |
| **`CHECKLOAD_EXIT`** | `0x0141A6` | `0x00E7B6` | `resource_mgr.s:2379`<br>`resource_mgr.s:2254` | — |
| **`CHECKLOAD_EXIT_2`** | `0x0141F0` | `0x00E804` | `resource_mgr.s:2442`<br>`resource_mgr.s:2318` | — |
| **`CHECKLOAD_EXIT_3`** | `0x01425E` | `0x00E872` | `resource_mgr.s:2527`<br>`resource_mgr.s:2408` | — |
| **`CHECKLOAD_EXIT_4`** | `0x014268` | `0x00E87C` | `resource_mgr.s:2538`<br>`resource_mgr.s:2421` | CHECKLOAD_EXIT_4 Called during boot. |
| **`CHECKLOAD_EXIT_5`** | `0x0142F0` | `0x00E904` | `resource_mgr.s:2637`<br>`resource_mgr.s:2521` | — |
| **`CHECKLOAD_EXIT_6`** | `0x0143C6` | `0x00E9E2` | `resource_mgr.s:2766`<br>`resource_mgr.s:2657` | — |
| **`CHECKLOAD_FIND_NEXT`** | — | `0x00E8F2` | `resource_mgr.s:2505` | — |
| **`CHECKLOAD_LOOP`** | `0x01438E` | `0x00E9AA` | `resource_mgr.s:2730`<br>`resource_mgr.s:2623` | — |
| **`CHECKLOAD_NEXT`** | `0x0142DA` | `0x00E8EE` | `resource_mgr.s:2612`<br>`resource_mgr.s:2502` | — |
| **`CHECKLOAD_NEXT_2`** | `0x0142EE` | `0x00E902` | `resource_mgr.s:2635`<br>`resource_mgr.s:2519` | CHECKLOAD_NEXT_2 Called during boot. |
| **`CHECKLOAD_NO`** | `0x014150` | `0x00E760` | `resource_mgr.s:2317`<br>`resource_mgr.s:2199` | — |
| **`CHECKLOAD_NO_2`** | `0x0141C0` | `0x00E7D0` | `resource_mgr.s:2406`<br>`resource_mgr.s:2278` | CHECKLOAD_NO_2 - set handle flags for a resource that is not locked Called during boot. |
| **`CHECKLOAD_NO_3`** | `0x0142B4` | `0x00E8C8` | `resource_mgr.s:2597`<br>`resource_mgr.s:2487` | CHECKLOAD_NO_3 Called during boot. |
| **`CHECKLOAD_NO_4`** | `0x0142DE` | — | `resource_mgr.s:2620` | CHECKLOAD_NO_4 |
| **`CHECKLOAD_OK`** | `0x01417A` | `0x00E78A` | `resource_mgr.s:2350`<br>`resource_mgr.s:2226` | CHECKLOAD_OK Called during boot (22,312 times in 30s trace). |
| **`CHECKLOAD_OK_2`** | `0x01421E` | `0x00E832` | `resource_mgr.s:2473`<br>`resource_mgr.s:2351` | — |
| **`CHECKLOAD_OK_3`** | `0x01427A` | `0x00E88E` | `resource_mgr.s:2551`<br>`resource_mgr.s:2436` | CHECKLOAD_OK_3 Called during boot. |
| **`CHECKLOAD_OK_4`** | `0x014324` | `0x00E938` | `resource_mgr.s:2670`<br>`resource_mgr.s:2555` | CHECKLOAD_OK_4 Called during boot. |
| **`CHECKLOAD_OK_5`** | `0x0143BC` | `0x00E9D8` | `resource_mgr.s:2756`<br>`resource_mgr.s:2648` | — |
| **`CHECKLOAD_SKIP`** | `0x014176` | `0x00E786` | `resource_mgr.s:2341`<br>`resource_mgr.s:2218` | — |
| **`CHECKLOAD_SKIP_2`** | `0x0141B0` | `0x00E7C0` | `resource_mgr.s:2385`<br>`resource_mgr.s:2260` | — |
| **`CHECKLOAD_SKIP_3`** | `0x01435C` | `0x00E970` | `resource_mgr.s:2703`<br>`resource_mgr.s:2591` | — |
| **`CHECKLOAD_SKIP_4`** | `0x0143A0` | `0x00E9BC` | `resource_mgr.s:2737`<br>`resource_mgr.s:2630` | — |
| **`CheckUpdate`** | `0x0114E8` | `0x00BB46` | `window_mgr.s:629` | _CheckUpDate ($A911) _CheckUpdate ($A911): find window needing update (for GetNextEvent) Scans window list front-to-back for first window with non-empty updateRgn Returns: true + event filled if updat... |
| **`CHECKUPDATE`** | `0x0114E8` | `0x00BB46` | `window_mgr.s:586` | _CheckUpdate ($A911): find window needing update (for GetNextEvent) Scans window list front-to-back for first window with non-empty updateRgn. Returns: true + event filled if update needed, false othe... |
| **`CHECKUPDATE_CONT`** | `0x0114FE` | `0x00BB5C` | `window_mgr.s:639`<br>`window_mgr.s:596` | scan window list for pending updates |
| **`CHECKUPDATE_CONT_2`** | `0x011570` | `0x00BBCE` | `window_mgr.s:705`<br>`window_mgr.s:657` | CHECKUPDATE_CONT_2 - allocate a GrafPort-sized block (108 bytes) and open it CHECKUPDATE_EMPTY entry: allocate D0 bytes and open as port. CHECKUPDATE_CONT_3 entry: open pre-allocated A0 as port. Retur... |
| **`CHECKUPDATE_CONT_3`** | `0x011574` | `0x00BBD2` | `window_mgr.s:711`<br>`window_mgr.s:661` | CHECKUPDATE_CONT_3 -- open it as GrafPort (A3 = port). |
| **`CHECKUPDATE_EMPTY`** | `0x011572` | `0x00BBD0` | `window_mgr.s:708`<br>`window_mgr.s:659` | CHECKUPDATE_EMPTY -- allocate and zero. |
| **`CHECKUPDATE_EXIT`** | `0x011556` | `0x00BBB4` | `window_mgr.s:677`<br>`window_mgr.s:634` | — |
| **`CHECKUPDATE_NO`** | `0x011560` | `0x00BBBE` | `window_mgr.s:690`<br>`window_mgr.s:646` | CHECKUPDATE_NO - fill update event for window with non-empty updateRgn Builds an EventRecord: what=updateEvt(6), message=windowPtr Called during boot. |
| **`CHECKUPDATE_SKIP`** | `0x011550` | `0x00BBAE` | `window_mgr.s:674`<br>`window_mgr.s:631` | check if this window has a non-empty update region auto-draw window picture (no update event needed) |
| **`ClearMenuBar`** | `0x0121FE` | `0x00CA16` | `menu_mgr.s:101` | _ClearMenuBar ($A934) Called during boot. |
| **`CLEARMENUBAR`** | `0x0121FE` | `0x00CA16` | `menu_mgr.s:152` | **Proto:** `Pascal: procedure ClearMenuBar;`<br>_ClearMenuBar ($A934): empty the menu bar. Pascal: procedure ClearMenuBar; |
| **`ClipAbove`** | `0x0112D4` | `0x00B922` | `window_mgr.s:270` | _ClipAbove ($A90B) _ClipAbove ($A90B): set WMgrPort clip to visible area above a window Clips to desktop minus all windows above the given one |
| **`CLIPABOVE`** | `0x0112D4` | `0x00B922` | `window_mgr.s:265` | _ClipAbove ($A90B): set WMgrPort clip to visible area above a window Clips to desktop minus all windows above the given one |
| **`CloseDeskAcc`** | `0x015EB2` | `0x010506` | `desk_mgr.s:436` | _CloseDeskAcc ($A9B7) |
| **`CLOSEDESKACC`** | `0x015EB2` | `0x010506` | `desk_mgr.s:445` | _CloseDeskAcc ($A9B7) - close DA by refNum. Calls _Close on a minimal IOParam block. |
| **`CLOSEDESKACC_EXIT`** | `0x015EC6` | `0x01051A` | `desk_mgr.s:443`<br>`desk_mgr.s:452` | — |
| **`CloseDialog`** | `0x014C9E` | `0x00F2C0` | `dialog_mgr.s:575` | _CloseDialog ($A982) Called during boot. |
| **`CLOSEDIALOG`** | `0x014C9E` | `0x00F2C0` | `dialog_mgr.s:581` | _CloseDialog ($A982) -- close dialog window, dispose item handles. Stack: theDialog(L). Empties contRgn (so window doesn't update), disposes all item Pascal-string storage via FINDDITEM_CONT op=2, dis... |
| **`CLOSEDIALOG_CONT`** | `0x014CC4` | `0x00F2E6` | `dialog_mgr.s:590`<br>`dialog_mgr.s:596` | — |
| **`CLOSEDIALOG_CONT_2`** | `0x014CC6` | `0x00F2E8` | `dialog_mgr.s:592`<br>`dialog_mgr.s:598` | — |
| **`CLOSEDIALOG_CONT_3`** | `0x014CC8` | `0x00F2EA` | `dialog_mgr.s:600`<br>`dialog_mgr.s:605` | CLOSEDIALOG_CONT_3 Called during boot. |
| **`CLOSEDIALOG_CONT_4`** | `0x014CDA` | `0x00F2FC` | `dialog_mgr.s:615`<br>`dialog_mgr.s:623` | CLOSEDIALOG_CONT_4 Called during boot. |
| **`CLOSEDIALOG_CONT_5`** | `0x014CF2` | `0x00F314` | `dialog_mgr.s:633`<br>`dialog_mgr.s:642` | CLOSEDIALOG_CONT_5 Called during boot. |
| **`CLOSEDIALOG_CONT_6`** | `0x014D18` | `0x00F33A` | `dialog_mgr.s:663`<br>`dialog_mgr.s:666` | CLOSEDIALOG_CONT_6 Called during boot. |
| **`CLOSEDIALOG_EXIT`** | `0x014D16` | `0x00F338` | `dialog_mgr.s:655`<br>`dialog_mgr.s:658` | — |
| **`CLOSEDIALOG_FOUND`** | `0x014D14` | `0x00F336` | `dialog_mgr.s:653`<br>`dialog_mgr.s:656` | — |
| **`CLOSEDIALOG_LOOP`** | — | `0x00F322` | `dialog_mgr.s:649` | — |
| **`CLOSEDIALOG_NO`** | `0x014CFE` | `0x00F320` | `dialog_mgr.s:644`<br>`dialog_mgr.s:647` | CLOSEDIALOG_NO - search for first editText item Called during boot. |
| **`CLOSEDIALOG_NO_2`** | `0x014D00` | — | `dialog_mgr.s:646` | — |
| **`CLOSEDIALOG_SKIP`** | `0x014CD4` | — | `dialog_mgr.s:606` | — |
| **`CLOSEDIALOG_SKIP_2`** | `0x014CEE` | `0x00F310` | `dialog_mgr.s:624`<br>`dialog_mgr.s:632` | — |
| **`CLOSERES_CHK_ALL`** | `0x013BEA` | `0x00E1F4` | `resource_mgr.s:1323`<br>`resource_mgr.s:1255` | — |
| **`CLOSERES_CHK_SYS`** | `0x013C32` | `0x00E23C` | `resource_mgr.s:1361`<br>`resource_mgr.s:1292` | — |
| **`CLOSERES_DISP_LP`** | `0x013C0A` | `0x00E214` | `resource_mgr.s:1337`<br>`resource_mgr.s:1269` | — |
| **`CLOSERES_DISP_NXT`** | `0x013C12` | `0x00E21C` | `resource_mgr.s:1342`<br>`resource_mgr.s:1274` | — |
| **`CLOSERES_DISPOSE`** | `0x013C6E` | `0x00E278` | `resource_mgr.s:1388`<br>`resource_mgr.s:1320` | — |
| **`CLOSERES_FILE`** | `0x013C62` | — | `resource_mgr.s:1383` | — |
| **`CLOSERES_FINDMAP`** | `0x013BF4` | — | `resource_mgr.s:1327` | — |
| **`CLOSERES_PRED_LNK`** | `0x013C2A` | `0x00E234` | `resource_mgr.s:1357`<br>`resource_mgr.s:1288` | CLOSERES_PRED_LNK - unlink map from chain via predecessor |
| **`CLOSERES_UNLINK`** | `0x013C18` | `0x00E222` | `resource_mgr.s:1345`<br>`resource_mgr.s:1277` | — |
| **`CLOSERES_UPD_CUR`** | `0x013C54` | `0x00E25E` | `resource_mgr.s:1378`<br>`resource_mgr.s:1310` | CLOSERES_UPD_CUR - update CurMap if closing the current resource file Called during boot. |
| **`CloseResFile`** | `0x013BD2` | `0x00E1E0` | `resource_mgr.s:1316` | _CloseResFile ($A99A) Closes a resource file: updates it, disposes all resource handles, unlinks its map from the chain, and closes the file. Called during boot. |
| **`CLOSERESFILE`** | `0x013BD2` | `0x00E1E0` | `resource_mgr.s:1249` | _CloseResFile ($A99A) -- close a resource file and unlink its map. Flushes any pending updates to disk via _UpdateResFile, then walks the map's reference list disposing every loaded resource handle vi... |
| **`CLOSERESFILE_DO_CLOSE`** | — | `0x00E26C` | `resource_mgr.s:1315` | — |
| **`CloseWindow`** | `0x011776` | `0x00BDDC` | `window_mgr.s:968` | **Proto:** `Pascal: procedure CloseWindow(theWindow: WindowPtr);`<br>_CloseWindow ($A92D) stack: window -> (disposes of window) _CloseWindow ($A92D): close and dispose a window's data structures Pascal: procedure CloseWindow(theWindow: WindowPtr); Hides window, kills c... |
| **`CLOSEWINDOW`** | `0x011776` | `0x00BDDC` | `window_mgr.s:907` | **Proto:** `Pascal: procedure CloseWindow(theWindow: WindowPtr);`<br>_CloseWindow ($A92D): close and dispose a window's data structures Pascal: procedure CloseWindow(theWindow: WindowPtr); Hides window, kills controls, sends wDispose to WDEF, frees regions. |
| **`CLOSEWINDOW_CONT`** | `0x0117E6` | `0x00BE4C` | `window_mgr.s:1022`<br>`window_mgr.s:960` | CLOSEWINDOW_CONT - deactivate a window: unhighlight it and schedule deactivate event D0 = window to deactivate on entry. Called during boot. |
| **`CLOSEWINDOW_NO`** | `0x0117D6` | `0x00BE3C` | `window_mgr.s:1007`<br>`window_mgr.s:946` | check if this was the front window (saved FrontWindow result on stack) |
| **`CLOSEWINDOW_SKIP`** | `0x0117C4` | `0x00BE2A` | `window_mgr.s:999`<br>`window_mgr.s:938` | dispose window's allocated structures |
| **`CLOSEWINDOW_SKIP_2`** | `0x0117DE` | `0x00BE44` | `window_mgr.s:1011`<br>`window_mgr.s:950` | — |
| **`CLOSEWINDOW_SKIP_3`** | `0x011802` | `0x00BE68` | `window_mgr.s:1033`<br>`window_mgr.s:971` | — |
| **`CMGR`** | — | `0x00D382` | `control_mgr.s:18` | Control Manager Apple source: ControlMgr.a (MacSEROM.lst module CMGR). The Control Manager traps with their local helpers, in physical ROM order: NewControl, DisposControl, KillControls, Draw1Control,... |
| **`CMGREND`** | — | `0x00D958` | `resource_mgr.s:85` | **Proto:** `The "1" variants (Count1Resources, Get1IxResource (Pascal:`<br>Resource Manager Apple source: ResourceMgr.a (MacSEROM.lst module RMGR). In ROM order: InitResources, SuperLoad, NewMap, CLOSEDIALOG_LOOP; the file calls (CreateResFile, OpenResFile, OpenRFPerm, UseRe... |
| **`CMP_ADD_LEN_PFX`** | `0x01399A` | `0x00DF86` | `resource_mgr.s:975`<br>`resource_mgr.s:902` | — |
| **`CMP_ADD_TO_BUF`** | — | `0x00E04E` | `resource_mgr.s:1006` | CMP_ADD_TO_BUF (CMP_COPY_CHANGED) -- copy changed resource to compaction buffer. Reads the resource handle's data and copies it to the compaction buffer, flushing the buffer to disk when full. Writes ... |
| **`CMP_ADV_WRITEPTR`** | `0x013A8A` | `0x00E09C` | `resource_mgr.s:1103`<br>`resource_mgr.s:1054` | CMP_ADV_WRITEPTR -- advance write pointer, update limit. |
| **`CMP_AFTER_FREE`** | — | `0x00E01E` | `resource_mgr.s:979` | — |
| **`CMP_ALLOC_HEAP_BUF`** | — | `0x00DFC8` | `resource_mgr.s:930` | — |
| **`CMP_BEGIN`** | — | `0x00DF6A` | `resource_mgr.s:889` | — |
| **`CMP_BLOCKMOVE`** | `0x013A80` | `0x00E092` | `resource_mgr.s:1096`<br>`resource_mgr.s:1047` | CMP_BLOCKMOVE -- copy 4-byte length prefix within buffer. |
| **`CMP_BUF_SIZE_OK`** | — | `0x00DFB6` | `resource_mgr.s:921` | — |
| **`CMP_CHG_CHUNK`** | `0x013A5E` | `0x00E070` | `resource_mgr.s:1071`<br>`resource_mgr.s:1022` | CMP_CHG_CHUNK: chunked copy loop (data > buffer capacity). |
| **`CMP_CHG_FINAL`** | `0x013A7A` | `0x00E08C` | `resource_mgr.s:1089`<br>`resource_mgr.s:1039` | CMP_CHG_FINAL - final chunk: copy remaining bytes to buffer |
| **`CMP_COPY_CHANGED`** | `0x013A3C` | — | `resource_mgr.s:1056` | CMP_COPY_CHANGED - copy changed resource from memory to compaction buffer Reads the resource handle's data and copies it into the compaction buffer, flushing the buffer to disk when full. Writes the 4... |
| **`CMP_COPY_CHUNK`** | `0x013A7C` | `0x00E08E` | `resource_mgr.s:1092`<br>`resource_mgr.s:1043` | CMP_COPY_CHUNK -- copy chunk to buffer and flush. |
| **`CMP_COPY_FROM_DISK`** | — | `0x00DFF2` | `resource_mgr.s:958` | — |
| **`CMP_COPY_FROM_DSK`** | `0x0139E8` | — | `resource_mgr.s:1015` | — |
| **`CMP_COPY_UNCHANGE`** | `0x013AC6` | `0x00E0D8` | `resource_mgr.s:1162`<br>`resource_mgr.s:1110` | CMP_COPY_UNCHANGE - copy unchanged resource from file to compaction buffer Reads the resource data directly from the file into the buffer. If the resource's file offset is behind the current write pos... |
| **`CMP_DISK_LEN`** | — | `0x00DF82` | `resource_mgr.s:900` | — |
| **`CMP_FLUSH_BUF`** | `0x013B8E` | `0x00E19C` | `resource_mgr.s:1278`<br>`resource_mgr.s:1209` | CMP_FLUSH_BUF -- flush buffer if needed, update file pos. CMP_FLUSH_BUF Called by: CMP_COPY_CHANGED, CMP_CHG_CHUNK, CMP_COPY_UNCHANGE, CMP_READ_INTACT, CMP_READ_LOOP |
| **`CMP_FLUSH_RET`** | `0x013BCC` | `0x00E1DA` | `resource_mgr.s:1305`<br>`resource_mgr.s:1236` | — |
| **`CMP_GAP_CHECK`** | `0x0139AC` | `0x00DF9A` | `resource_mgr.s:982`<br>`resource_mgr.s:909` | — |
| **`CMP_LOOP_ENTRY`** | — | `0x00DFD0` | `resource_mgr.s:935` | — |
| **`CMP_MAP_EXIT`** | `0x013A38` | `0x00E04A` | `resource_mgr.s:1046`<br>`resource_mgr.s:996` | — |
| **`CMP_NEXT_RES`** | `0x0139EC` | `0x00DFF6` | `resource_mgr.s:1017`<br>`resource_mgr.s:960` | — |
| **`CMP_RDLIMIT_OK`** | `0x013A94` | `0x00E0A6` | `resource_mgr.s:1110`<br>`resource_mgr.s:1061` | — |
| **`CMP_READ_ERROR`** | `0x013B4E` | `0x00E15C` | `resource_mgr.s:1237`<br>`resource_mgr.s:1168` | CMP_READ_ERROR - read error during compaction |
| **`CMP_READ_FILE`** | `0x013B58` | `0x00E166` | `resource_mgr.s:1248`<br>`resource_mgr.s:1178` | CMP_READ_FILE - read resource data from file into compaction buffer Computes how many bytes remain in the file between the current read position (D5) and EOF, clamps to available buffer space, then re... |
| **`CMP_READ_FINAL`** | `0x013B46` | `0x00E154` | `resource_mgr.s:1228`<br>`resource_mgr.s:1164` | CMP_READ_FINAL - final chunk fits in buffer |
| **`CMP_READ_INTACT`** | `0x013ADA` | `0x00E0EC` | `resource_mgr.s:1178`<br>`resource_mgr.s:1118` | CMP_READ_INTACT - read unchanged resource from file into buffer The resource data is still at its original file position. Reads the 4-byte length prefix first, then the data body. Handles the case whe... |
| **`CMP_READ_LOOP`** | `0x013B2C` | `0x00E13A` | `resource_mgr.s:1210`<br>`resource_mgr.s:1151` | CMP_READ_LOOP: chunked read loop for resources larger than buffer. |
| **`CMP_READ_SIZE`** | `0x013996` | — | `resource_mgr.s:973` | CMP_READ_SIZE - read existing resource size from file |
| **`CMP_READ_UPD_OFS`** | `0x013AF2` | `0x00E104` | `resource_mgr.s:1188`<br>`resource_mgr.s:1128` | — |
| **`CMP_READF_CLAMP`** | `0x013B74` | `0x00E182` | `resource_mgr.s:1260`<br>`resource_mgr.s:1190` | — |
| **`CMP_STORE_DATALEN`** | `0x013A0E` | `0x00E020` | `resource_mgr.s:1032`<br>`resource_mgr.s:982` | CMP_STORE_DATALEN: store final data fork length in map header. |
| **`CMP_UNLK_A3`** | — | `0x00E01C` | `resource_mgr.s:977` | — |
| **`CMP_UPD_RDLIMIT`** | `0x013A8E` | `0x00E0A0` | `resource_mgr.s:1106`<br>`resource_mgr.s:1057` | — |
| **`CMP_UPD_REF_OFS`** | `0x013A96` | `0x00E0A8` | `resource_mgr.s:1120`<br>`resource_mgr.s:1070` | CMP_UPD_REF_OFS - update ref entry's data offset to reflect new position Computes the new data offset from the buffer write pointer relative to buffer base, plus the cumulative file write offset. Pres... |
| **`CMP_WLONG_LOOP`** | `0x013AB8` | `0x00E0CA` | `resource_mgr.s:1146`<br>`resource_mgr.s:1095` | — |
| **`CMP_WRITE_LONG`** | `0x013AB4` | `0x00E0C6` | `resource_mgr.s:1143`<br>`resource_mgr.s:1092` | CMP_WRITE_LONG -- write 4-byte length prefix to buffer. |
| **`CMP_WRITE_MAP`** | `0x013A12` | `0x00E024` | `resource_mgr.s:1034`<br>`resource_mgr.s:984` | — |
| **`CMP_WRITE_RES`** | `0x013982` | `0x00DF6E` | `resource_mgr.s:961`<br>`resource_mgr.s:893` | CMP_WRITE_RES - compaction loop: write current resource If the resChanged bit is set, writes the in-memory resource data to disk (CHECKLOAD_CONT_8) and gets its handle size. Otherwise reads the existi... |
| **`CMP_WRITE_ZERO`** | `0x013AB2` | `0x00E0C4` | `resource_mgr.s:1140`<br>`resource_mgr.s:1089` | CMP_WRITE_ZERO - write zero length prefix to buffer Entry at CMP_WRITE_ZERO writes a zero-length resource (D0=0). Entry at CMP_WRITE_LONG writes D0 as a 4-byte big-endian value into the compaction buf... |
| **`CmpFrm`** | `0x0139DC` | — | `resource_mgr.s:1010` | CmpFrm - compaction frame: copy resources to close gaps For each resource in file order, either copies from memory (changed) or from disk (unchanged) into the compaction buffer, then flushes the buffe... |
| **`CNTTYPE_ADD_NEW`** | `0x013D74` | `0x00E37E` | `resource_mgr.s:1579`<br>`resource_mgr.s:1485` | — |
| **`CNTTYPE_CMP_LOOP`** | `0x013D6C` | `0x00E376` | `resource_mgr.s:1575`<br>`resource_mgr.s:1481` | — |
| **`CNTTYPE_ENTRY_LP`** | `0x013D62` | `0x00E36C` | `resource_mgr.s:1569`<br>`resource_mgr.s:1475` | — |
| **`CNTTYPE_MAP_LOOP`** | `0x013D5C` | `0x00E366` | `resource_mgr.s:1566`<br>`resource_mgr.s:1472` | — |
| **`CNTTYPE_NEXT_ENT`** | `0x013D78` | `0x00E382` | `resource_mgr.s:1582`<br>`resource_mgr.s:1488` | — |
| **`CNTTYPE_NEXTMAP`** | `0x013D7E` | `0x00E388` | `resource_mgr.s:1585`<br>`resource_mgr.s:1491` | — |
| **`CouldAlert`** | `0x014D68` | `0x00F38A` | `dialog_mgr.s:737` | **Proto:** `CouldAlert -- _CouldAlert ($A989): PROCEDURE CouldAlert (a l ertID: I NTEGER);`<br>CouldAlert -- _CouldAlert ($A989): PROCEDURE CouldAlert (a l ertID: I NTEGER); _CouldAlert ($A989) |
| **`COULDALERT`** | `0x014D68` | `0x00F38A` | `dialog_mgr.s:730` | _CouldAlert ($A989) -- preload an ALRT resource and its sub-resources. |
| **`COULDALERT_CONT`** | `0x014D74` | — | `dialog_mgr.s:741` | — |
| **`COULDALERT_CONT_2`** | `0x014D92` | `0x00F3B6` | `dialog_mgr.s:759`<br>`dialog_mgr.s:754` | COULDALERT_CONT_2 -- load ALRT resource template. COULDALERT_CONT_2 |
| **`COULDALERT_CONT_3`** | `0x014D9A` | `0x00F3BE` | `dialog_mgr.s:768`<br>`dialog_mgr.s:760` | COULDALERT_CONT_3 Called during boot. |
| **`COULDALERT_CONT_4`** | `0x014DA0` | `0x00F3C4` | `dialog_mgr.s:770`<br>`dialog_mgr.s:762` | — |
| **`CouldDialog`** | `0x014D5A` | `0x00F37C` | `dialog_mgr.s:726` | _CouldDialog ($A979) |
| **`COULDDIALOG`** | `0x014D5A` | `0x00F37C` | `dialog_mgr.s:722` | _CouldDialog ($A979) -- preload a DLOG resource and its sub-resources. Stack: dialogID(W). Loads DLOG, makes it non-purgeable, loads its DITL, walks items preloading any embedded sub-resources, loads ... |
| **`Count1Resources`** | `0x013C76` | `0x00E280` | `resource_mgr.s:1404` | **Proto:** `Pascal: FUNCTION Count1Resources(theType: ResType): INTEGER;`<br>**Regs:** `Entry: 4(SP).L = theType, 8(SP).W = space for the function result Exit:  function result = number of resources of theType; 4 bytes popped`<br>_Count1Resources ($A80D): count the resources of a given type in the current resource file only (Mac Plus addition, Inside Macintosh IV) Pascal: FUNCTION Count1Resources(theType: ResType): INTEGER; En... |
| **`COUNT1RESOURCES`** | `0x013C76` | `0x00E280` | `resource_mgr.s:1331` | _Count1Resources ($A80D), _CountResources ($A99C) -- count resources of type. _Count1Resources searches only the current map (sets RMgrCurOnly=true). _CountResources searches all maps in the chain. St... |
| **`Count1Types`** | `0x013D3C` | `0x00E346` | `resource_mgr.s:1540` | **Proto:** `Pascal: FUNCTION Count1Types: INTEGER;`<br>**Regs:** `Entry: 4(SP).W = space for the function result (no parameters) Exit:  function result = number of distinct resource types`<br>_Count1Types ($A81C): count the distinct resource types in the current resource file only (Mac Plus addition, Inside Macintosh IV) Pascal: FUNCTION Count1Types: INTEGER; Entry: 4(SP).W = space for the... |
| **`COUNT1TYPES`** | `0x013D3C` | `0x00E346` | `resource_mgr.s:1449` | _Count1Types ($A81C), _CountTypes ($A99E) -- count distinct resource types. _Count1Types restricts to current map (sets RMgrCurOnly). _CountTypes counts distinct types across the entire map chain. Ret... |
| **`COUNT_UNIQ_TYPES`** | `0x013D50` | `0x00E35A` | `resource_mgr.s:1561`<br>`resource_mgr.s:1467` | COUNT_UNIQ_TYPES - collect the distinct resource types on the stack Walks the maps from RETURNS_20 (all open maps, or only CurMap when RMgrCurOnly is set) and pushes each type not already on the stack... |
| **`CountMItems`** | `0x012CFC` | `0x00D32A` | `menu_mgr.s:1879` | **Proto:** `Pascal: function CountMItems(theMenu: MenuHandle): INTEGER;`<br>_CountMItems ($A950) _CountMItems ($A950): count items in a menu Pascal: function CountMItems(theMenu: MenuHandle): INTEGER; |
| **`COUNTMITEMS`** | `0x012CFC` | `0x00D32A` | `menu_mgr.s:1526` | **Proto:** `Pascal: function CountMItems(theMenu: MenuHandle): INTEGER;`<br>_CountMItems ($A950): count items in a menu. Pascal: function CountMItems(theMenu: MenuHandle): INTEGER; |
| **`COUNTMITEMS_NEXT`** | `0x012CFE` | `0x00D32C` | `menu_mgr.s:1881`<br>`menu_mgr.s:1528` | — |
| **`COUNTRES_LOOP`** | `0x013C86` | `0x00E290` | `resource_mgr.s:1414`<br>`resource_mgr.s:1338` | — |
| **`COUNTRES_NEXTMAP`** | `0x013C92` | `0x00E29C` | `resource_mgr.s:1419`<br>`resource_mgr.s:1343` | — |
| **`CountResources`** | `0x013C7A` | `0x00E284` | `resource_mgr.s:1409` | **Proto:** `Pascal: FUNCTION CountResources(theType: ResType): INTEGER;`<br>CountResources -- _CountResources ($A99C): same count over all open files. Pascal: FUNCTION CountResources(theType: ResType): INTEGER; Called 3,781 times during 30s boot-to-Finder. |
| **`COUNTRESOURCES`** | `0x013C7A` | `0x00E284` | `resource_mgr.s:1333` | — |
| **`CountRunsBefore`** | — | `0x0121BC` | `textedit.s:3685` | CountRunsBefore - count style runs from A0 up to char D1. In: A0 = run entry ptr, D1 = end char. Out: D0 = number of runs covering range. Called by: TE_LOCATE_STYLERUNS, XTRIMMEASURE_PLAIN, TE_PUT_STY... |
| **`CountRunsBefore_DONE`** | — | `0x0121DE` | `textedit.s:3702` | — |
| **`CountRunsBefore_LOOP`** | — | `0x0121D2` | `textedit.s:3695` | — |
| **`CountTypes`** | `0x013D40` | `0x00E34A` | `resource_mgr.s:1543` | **Proto:** `CountTypes -- _CountTypes ($A99E): FUNCTION CountTypes: Integer;`<br>CountTypes -- _CountTypes ($A99E): FUNCTION CountTypes: Integer; |
| **`COUNTTYPES`** | `0x013D40` | `0x00E34A` | `resource_mgr.s:1451` | — |
| **`CREATERES_CHKEOF`** | `0x0137C6` | `0x00DDC2` | `resource_mgr.s:662`<br>`resource_mgr.s:661` | — |
| **`CREATERES_CLOSE`** | `0x0137EA` | `0x00DDE6` | `resource_mgr.s:675`<br>`resource_mgr.s:674` | — |
| **`CREATERES_EXIT`** | `0x0137EC` | `0x00DDE8` | `resource_mgr.s:677`<br>`resource_mgr.s:676` | — |
| **`CreateResFile`** | `0x0137A6` | `0x00DDA2` | `resource_mgr.s:649` | _CreateResFile ($A9B1) Creates a new resource file. If the file does not exist, creates it first with _Create. Writes an empty resource map (16-byte header + 30-byte null map) to the resource fork. |
| **`CREATERESFILE`** | `0x0137A6` | `0x00DDA2` | `resource_mgr.s:648` | _CreateResFile ($A9B1) -- create a new resource file. Creates a new resource file. If the file does not exist, creates it first with _Create. Writes an empty resource map (16-byte header + 30-byte nul... |
| **`CurResFile`** | `0x01450E` | `0x00EB32` | `resource_mgr.s:2999` | _CurResFile ($A994) Called during boot. |
| **`CURRESFILE`** | `0x01450E` | `0x00EB32` | `resource_mgr.s:2865` | _CurResFile ($A994) -- return the current resource file's refnum. |
| **`DateToSeconds`** | — | `0x01216E` | `textedit.s:3639` | DateToSeconds - binary search StyleRec for run containing D0. In: D0 = char offset. Out: A0 = ptr to entry whose charPos <= D0+1 < next.charPos, D0 = entry index. StyleRec layout: (nRuns:W) (elementHa... |
| **`DateToSeconds_AT_ZERO`** | — | `0x0121A8` | `textedit.s:3668` | — |
| **`DateToSeconds_FOUND`** | — | `0x0121A6` | `textedit.s:3666` | — |
| **`DateToSeconds_GO_LOWER`** | — | `0x0121A2` | `textedit.s:3663` | — |
| **`DateToSeconds_LOOP`** | — | `0x012184` | `textedit.s:3648` | — |
| **`DateToSeconds_RETURN`** | — | `0x0121AE` | `textedit.s:3672` | — |
| **`DefClikProc`** | `0x016D46` | `0x012102` | `textedit.s:2063`<br>`textedit.s:3579` | DefClikProc - default click loop routine (DefClikProc) TENew stores its address in teClikProc; TEClick calls it (JSR) while the mouse button is down, with A3 = TERec and A6 = TEClick's frame (8(A6) = ... |
| **`DeleteMenu`** | `0x0122AE` | `0x00CAA2` | `menu_mgr.s:204` | **Proto:** `DeleteMenu -- _DeleteMenu ($A936): PROCEDURE DeleteMenu (menuID: Integer);`<br>DeleteMenu -- _DeleteMenu ($A936): PROCEDURE DeleteMenu (menuID: Integer); _DeleteMenu ($A936) |
| **`DELETEMENU`** | `0x0122AE` | `0x00CAA2` | `menu_mgr.s:235` | **Proto:** `Pascal: procedure DeleteMenu(menuID: INTEGER);`<br>_DeleteMenu ($A936): remove a menu from the menu bar. Pascal: procedure DeleteMenu(menuID: INTEGER); |
| **`DELETEMENU_CONT`** | `0x0122E8` | `0x00CADC` | `menu_mgr.s:229`<br>`menu_mgr.s:258` | — |
| **`DELETEMENU_CONT_2`** | `0x0122F0` | — | `menu_mgr.s:241` | DELETEMENU_CONT_2 Called during boot. |
| **`DELETEMENU_CONT_3`** | `0x012314` | — | `menu_mgr.s:261` | — |
| **`DELETEMENU_CONT_4`** | `0x012318` | — | `menu_mgr.s:270` | DELETEMENU_CONT_4 Called during boot. |
| **`DELETEMENU_EXIT`** | `0x0122EA` | — | `menu_mgr.s:231` | — |
| **`DELETEMENU_NO`** | `0x0122C6` | `0x00CABA` | `menu_mgr.s:218`<br>`menu_mgr.s:247` | DELETEMENU_NO |
| **`DELETEMENU_NO_2`** | `0x0122D2` | `0x00CAC6` | `menu_mgr.s:222`<br>`menu_mgr.s:251` | — |
| **`DELETEMENU_OK`** | `0x012310` | — | `menu_mgr.s:259` | DELETEMENU_OK Called during boot. |
| **`DeleteWindow`** | `0x011220` | `0x00B868` | `window_mgr.s:146` | DeleteWindow - Remove a window from the window list Unlinks the window at 0x4(SP) from the WindowList chain. If the target is the first window (no predecessor), patches WindowList itself via ChooserBi... |
| **`DELETEWINDOW`** | `0x011220` | `0x00B868` | `window_mgr.s:156` | DeleteWindow - Remove a window from the window list Unlinks the window at 0x4(SP) from the WindowList chain. If the target is the first window (no predecessor), patches WindowList itself via PrFlags (... |
| **`DelMenuItem`** | `0x012B9E` | `0x00D1CA` | `menu_mgr.s:1672` | **Proto:** `Pascal: PROCEDURE DelMenuItem(theMenu: MenuHandle; item: INTEGER);`<br>_DelMenuItem ($A952): delete an item from a menu Pascal: PROCEDURE DelMenuItem(theMenu: MenuHandle; item: INTEGER); Pushes a copy of the return address as a dummy third parameter so that the stack loo... |
| **`DELMENUITEM`** | `0x012B9E` | `0x00D1CA` | `menu_mgr.s:1357` | **Proto:** `Pascal: procedure DelMenuItem(theMenu: MenuHandle; item: INTEGER);`<br>_DelMenuItem ($A952): delete a menu item. Pascal: procedure DelMenuItem(theMenu: MenuHandle; item: INTEGER); Removes item via _Munger; also rotates enableFlags to remove the deleted bit. |
| **`DeltaPoint`** | `0x011924` | `0x00BF8A` | `window_mgr.s:1263` | _DeltaPoint ($A94F) _DeltaPoint ($A94F): compute difference between two points on stack Stack: retAddr, pt1(4 bytes), pt2(4 bytes) -> result overwrites pt2 result.v = pt2.v - pt1.v, result.h = pt2.h -... |
| **`DELTAPOINT`** | `0x011924` | `0x00BF8A` | `window_mgr.s:1174` | DELTAPOINT - compute Point delta: result = (pt2 - pt1) Stack on entry: pt1, pt2, result-space, return-addr. Called by: DELTAPOINT_CONT, NEWWINDOW_CONT, GROWWINDOW, GROWWINDOW_OK, GROWWINDOW_CONT_2 (an... |
| **`DELTAPOINT_CONT`** | `0x01193E` | `0x00BFA4` | `window_mgr.s:1279`<br>`window_mgr.s:1190` | DELTAPOINT_CONT - move window to new position D0 (packed point) Computes offset from current portRect origin to new position, then offsets strucRgn, contRgn, updateRgn, and portBounds by delta. D0 = n... |
| **`DELWIN_UNLINK`** | `0x01122E` | `0x00B876` | `window_mgr.s:152`<br>`window_mgr.s:162` | — |
| **`DESKMGR`** | — | `0x01021C` | `desk_mgr.s:22` | **Proto:** `FUNCTION SystemEvent(theEvent: EventRecord): BOOLEAN`<br>Desk Manager -- desk accessories Apple source: DeskMgr.a (MacSEROM.lst module DESKMGR): SystemEvent ($A9B2), SystemClick ($A9B3), SystemTask ($A9B4), SystemMenu ($A9B5), SysEdit ($A9C2), OpenDeskAcc (... |
| **`DetachResource`** | `0x014434` | `0x00EA50` | `resource_mgr.s:2838` | _DetachResource ($A992) Called during boot. |
| **`DETACHRESOURCE`** | `0x014434` | `0x00EA50` | `resource_mgr.s:2720` | _DetachResource ($A992) -- detach handle from resource map. Clears the resource bit in the handle's master flags, then nulls the ref entry so subsequent GetResource reloads from disk. Caller takes own... |
| **`DETACHRESOURCE_ERR`** | `0x014444` | `0x00EA60` | `resource_mgr.s:2849`<br>`resource_mgr.s:2727` | DETACHRESOURCE_ERR - can't detach changed resource |
| **`DialogSelect`** | `0x014B9A` | `0x00F1BC` | `dialog_mgr.s:426` | _DialogSelect ($A980) Called during boot. |
| **`DIALOGSELECT`** | `0x014B9A` | `0x00F1BC` | `dialog_mgr.s:428` | _DialogSelect ($A980) -- dispatch a dialog event to its handler. Stack: eventPtr(L), theDialog(L), itemHit(L) -> handled(B). Calls RETURNS_15 to dispatch the event (key/click on items, etc). Returns h... |
| **`DIALOGSELECT_CONT`** | `0x014BD8` | `0x00F1FA` | `dialog_mgr.s:448`<br>`dialog_mgr.s:450` | — |
| **`DIALOGSELECT_NO`** | `0x014BCC` | `0x00F1EE` | `dialog_mgr.s:443`<br>`dialog_mgr.s:445` | — |
| **`DisableItem`** | `0x012420` | `0x00CB66` | `menu_mgr.s:415` | _DisableItem ($A93A) Called during boot (96,044 times in 30s trace). |
| **`DISABLEITEM`** | `0x012420` | `0x00CB66` | `menu_mgr.s:348` | **Proto:** `Pascal: procedure DisableItem(theMenu: MenuHandle; item: INTEGER);`<br>_DisableItem ($A93B): disable a menu item. Pascal: procedure DisableItem(theMenu: MenuHandle; item: INTEGER); |
| **`DISABLEITEM_CONT`** | `0x012434` | `0x00CB7A` | `menu_mgr.s:439`<br>`menu_mgr.s:370` | DISABLEITEM_CONT Called during boot (63,856 times in 30s trace). |
| **`DISABLEITEM_CONT_2`** | `0x012438` | `0x00CB7E` | `menu_mgr.s:442`<br>`menu_mgr.s:373` | DISABLEITEM_CONT_2 -- a0 = dereferenced source data. |
| **`DISABLEITEM_CONT_3`** | `0x012440` | `0x00CB86` | `menu_mgr.s:453`<br>`menu_mgr.s:382` | DISABLEITEM_CONT_3 Called during boot. |
| **`DISABLEITEM_CONT_4`** | `0x012450` | — | `menu_mgr.s:468` | DISABLEITEM_CONT_4 -- toggle old highlighted menu (unhighlight). |
| **`DISABLEITEM_CONT_5`** | `0x012456` | — | `menu_mgr.s:472` | DISABLEITEM_CONT_5 -- invert menu title (highlight it). |
| **`DISABLEITEM_ERR`** | `0x01244C` | `0x00CB92` | `menu_mgr.s:464`<br>`menu_mgr.s:388` | DISABLEITEM_ERR |
| **`DISABLEITEM_EXIT`** | `0x012432` | — | `menu_mgr.s:431` | — |
| **`DISABLEITEM_NEXT`** | `0x012426` | `0x00CB6C` | `menu_mgr.s:425`<br>`menu_mgr.s:358` | DISABLEITEM_NEXT Called during boot (57,585 times in 30s trace). |
| **`DISABLEITEM_SKIP`** | `0x01246C` | — | `menu_mgr.s:481` | — |
| **`DISKINSERT_ENTRY`** | — | `0x0102C4` | `desk_mgr.s:153` | DISKINSERT_ENTRY - disk-inserted path. If high word non-zero call disk-inserted vector at $7DC; else mount the volume via _MountVol. |
| **`DisposControl`** | `0x012E96` | — | `control_mgr.s:181` | _DisposeControl ($A955) Called during boot. |
| **`DisposDialog`** | `0x014D24` | `0x00F346` | `dialog_mgr.s:679` | **Proto:** `Pascal: PROCEDURE DisposDialog(theDialog: DialogPtr);`<br>**Regs:** `Entry: 0x4(SP) = theDialog. Pushes the item list handle (items, offset $9C),`<br>_DisposDialog ($A983): close a dialog, dispose of its item list and record Pascal: PROCEDURE DisposDialog(theDialog: DialogPtr); Entry: 0x4(SP) = theDialog. Pushes the item list handle (items, offset ... |
| **`DISPOSDIALOG`** | `0x014D24` | `0x00F346` | `dialog_mgr.s:679` | _DisposDialog ($A983) -- dispose dialog including item list and storage. Closes the dialog (which disposes individual item Pascal strings), disposes the item list handle itself, then disposes the dSto... |
| **`DISPOSECONTROL`** | — | `0x00D49A` | `control_mgr.s:162` | **Proto:** `Pascal: procedure DisposeControl(theControl: ControlHandle);`<br>_DisposeControl ($A955): erase, unlink, dispose a control. Pascal: procedure DisposeControl(theControl: ControlHandle); |
| **`DISPOSEDIALOG_CONT`** | `0x014D3C` | `0x00F35E` | `dialog_mgr.s:699`<br>`dialog_mgr.s:695` | DISPOSEDIALOG_CONT - get the DITL of a DLOG template (not part of DisposDialog) Apple source name: GetLstD2 (System 7.1 DialogMgr.a) Called during boot. A2 = DLOG handle -> A2 = DITL handle (GetResour... |
| **`DISPOSEDIALOG_CONT_2`** | `0x014D44` | `0x00F366` | `dialog_mgr.s:710`<br>`dialog_mgr.s:703` | DISPOSEDIALOG_CONT_2 - get the DITL of an ALRT template (itemsID at offset 8) for CouldAlert/FreeAlert (Apple: GetLstA2). DISPOSEDIALOG_EXIT is also used by FREEALERT_CONT_3 to get WDEF 0. |
| **`DISPOSEDIALOG_CONT_3`** | `0x014D4A` | `0x00F36C` | `dialog_mgr.s:713`<br>`dialog_mgr.s:706` | — |
| **`DISPOSEDIALOG_EXIT`** | `0x014D54` | `0x00F376` | `dialog_mgr.s:717`<br>`dialog_mgr.s:710` | — |
| **`DISPOSEMENU`** | — | `0x00CDB8` | `menu_mgr.s:686` | **Proto:** `Pascal: procedure DisposeMenu(theMenu: MenuHandle);`<br>_DisposeMenu ($A932): free a menu handle. Pascal: procedure DisposeMenu(theMenu: MenuHandle); Uses TE_APPLY_JUST_MEASURE if it came from a resource file (bit 5 of menuFlags), else plain DisposeHandle. |
| **`DISPOSEMENU_EXIT`** | `0x0127D4` | `0x00CDCA` | `menu_mgr.s:963`<br>`menu_mgr.s:696` | — |
| **`DISPOSEMENU_NO`** | `0x0127D2` | `0x00CDC8` | `menu_mgr.s:961`<br>`menu_mgr.s:694` | DISPOSEMENU_NO - dispose plain (non-resource) menu handle |
| **`DISPOSEWINDOW`** | — | `0x00BE6A` | `window_mgr.s:978` | **Proto:** `Pascal: procedure DisposeWindow(theWindow: WindowPtr);`<br>_DisposeWindow ($A914): close window and free its storage Pascal: procedure DisposeWindow(theWindow: WindowPtr); |
| **`DisposMenu`** | `0x0127C2` | — | `menu_mgr.s:949` | _DisposeMenu ($A932) |
| **`DisposWindow`** | `0x011804` | — | `window_mgr.s:1045` | **Proto:** `Pascal: procedure DisposeWindow(theWindow: WindowPtr);`<br>_DisposeWindow ($A914) stack: window -> (disposes of window and its storage) _DisposeWindow ($A914): close window and free its storage Pascal: procedure DisposeWindow(theWindow: WindowPtr); Calls Clos... |
| **`DLG_FrameRoundOuter`** | — | `0x00FB36` | `dialog_mgr.s:1871` | **Regs:** `Entry: A0 = ptr to rect, D0 = pen width, D1 = pen height,`<br>DLG_FrameRoundOuter - Draw a rounded-rect frame around an item rect. Entry: A0 = ptr to rect, D0 = pen width, D1 = pen height, D2 = outward inset (positive = expand outward). Expands rect outward by D... |
| **`DLG_NewStringHandle`** | — | `0x00FB58` | `dialog_mgr.s:1896` | **Regs:** `Entry: A0 = ptr to Pascal string. Exit: A0 = new string handle. Preserves D1-D2, A1-A2.`<br>DLG_NewStringHandle - Create a new string handle from a Pascal string. Entry: A0 = ptr to Pascal string. Exit: A0 = new string handle. Preserves D1-D2, A1-A2. Note: saves D0-D2/A1-A2 but restores D1-D... |
| **`DLG_SwitchActiveField`** | — | `0x00FA76` | `dialog_mgr.s:1770` | **Regs:** `Entry: D3 = new field index (0-based), D2 = selection range.`<br>DLG_SwitchActiveField - Switch active edit field. Deactivates current TE (scrolling it back to origin), calls DLGMGR_CONT_33 to install new field's text into TE, then activates TE. Entry: D3 = new fie... |
| **`DLG_SwitchOrEditField`** | — | `0x00FAAA` | `dialog_mgr.s:1796` | **Regs:** `Entry: D3 = target field index, D2 = selection range.`<br>DLG_SwitchOrEditField - Check if edit field changed, then install new field. Entry: D3 = target field index, D2 = selection range. Falls through to DLGMGR_CONT_33 if field is different. |
| **`DLGMGR_CONT`** | `0x0150DA` | `0x00F70A` | `dialog_mgr.s:1251`<br>`dialog_mgr.s:1246` | Load resource handle for a control item (ctrlItem) Determines CNTL vs CDEF resource type from control subtype bits. |
| **`DLGMGR_CONT_10`** | `0x015154` | `0x00F784` | `dialog_mgr.s:1339`<br>`dialog_mgr.s:1326` | Initialize statText or editText: copy inline text from DITL to a handle DITL item data: length byte at +13(A2), text bytes follow |
| **`DLGMGR_CONT_11`** | `0x015162` | `0x00F792` | `dialog_mgr.s:1350`<br>`dialog_mgr.s:1336` | Initialize iconItem: load ICON resource by ID from DITL data |
| **`DLGMGR_CONT_12`** | `0x01516A` | `0x00F79A` | `dialog_mgr.s:1357`<br>`dialog_mgr.s:1342` | Initialize picItem: load PICT resource by ID from DITL data |
| **`DLGMGR_CONT_13`** | `0x015170` | `0x00F7A0` | `dialog_mgr.s:1359`<br>`dialog_mgr.s:1344` | — |
| **`DLGMGR_CONT_14`** | `0x01517C` | `0x00F7AC` | `dialog_mgr.s:1370`<br>`dialog_mgr.s:1354` | Initialize ctrlItem: create control from resource or inline data. D0 bits 0-1 = subtype: btnCtrl(0), chkCtrl(1), radCtrl(2), resCtrl(3) |
| **`DLGMGR_CONT_15`** | `0x0151B4` | `0x00F7E4` | `dialog_mgr.s:1399`<br>`dialog_mgr.s:1382` | — |
| **`DLGMGR_CONT_16`** | `0x0151BA` | `0x00F7EA` | `dialog_mgr.s:1402`<br>`dialog_mgr.s:1385` | — |
| **`DLGMGR_CONT_17`** | `0x0151E4` | `0x00F814` | `dialog_mgr.s:1433`<br>`dialog_mgr.s:1414` | DLGMGR_CONT_17 - Draw a single dialog item (D4=1) Dispatches by item type to draw controls, text, icons, pictures, or call userItem drawing procedure. |
| **`DLGMGR_CONT_18`** | `0x0151F4` | `0x00F824` | `dialog_mgr.s:1439`<br>`dialog_mgr.s:1420` | — |
| **`DLGMGR_CONT_19`** | `0x01520A` | `0x00F83A` | `dialog_mgr.s:1449`<br>`dialog_mgr.s:1430` | — |
| **`DLGMGR_CONT_2`** | `0x0150F0` | `0x00F720` | `dialog_mgr.s:1262`<br>`dialog_mgr.s:1256` | DLGMGR_CONT_2 - callback for resCtrl: extract CDEF proc ID from CNTL resource |
| **`DLGMGR_CONT_20`** | `0x01521A` | `0x00F84A` | `dialog_mgr.s:1463`<br>`dialog_mgr.s:1443` | Draw iconItem: load and plot icon in item's display rect |
| **`DLGMGR_CONT_21`** | `0x015228` | `0x00F858` | `dialog_mgr.s:1474`<br>`dialog_mgr.s:1453` | Draw picItem: load and draw picture in item's display rect |
| **`DLGMGR_CONT_22`** | `0x015236` | `0x00F866` | `dialog_mgr.s:1489`<br>`dialog_mgr.s:1467` | Draw statText or editText item. If this is the active editText field, erase and TEUpdate. Otherwise, perform ParamText substitution (^0..^3) then TextBox. After drawing, if editText, draw 3-pixel fram... |
| **`DLGMGR_CONT_23`** | `0x01524C` | `0x00F87C` | `dialog_mgr.s:1498`<br>`dialog_mgr.s:1476` | — |
| **`DLGMGR_CONT_24`** | `0x0152EA` | `0x00F918` | `dialog_mgr.s:1597`<br>`dialog_mgr.s:1572` | Dispose item resources (D4=2). Frees handles for text/icon/picture items, disposes controls. Item type dispatch: userItem=RTS, ctrlItem=DisposControl, statText/editText=DisposeHandle, iconItem/picItem... |
| **`DLGMGR_CONT_25`** | `0x0152F6` | `0x00F924` | `dialog_mgr.s:1603`<br>`dialog_mgr.s:1578` | — |
| **`DLGMGR_CONT_26`** | `0x0152FA` | `0x00F928` | `dialog_mgr.s:1610`<br>`dialog_mgr.s:1584` | Dispose text or icon/picture handle |
| **`DLGMGR_CONT_27`** | `0x0152FE` | — | `dialog_mgr.s:1617` | DLGMGR_CONT_27 - Dispose a control item (called from CloseDialog's item loop) |
| **`DLGMGR_CONT_28`** | `0x015304` | `0x00F932` | `dialog_mgr.s:1627`<br>`dialog_mgr.s:1598` | Handle activate/deactivate event for dialog's TextEdit field. Switches port to target dialog, activates/deactivates its TE, then restores original port. Event modifiers bit 0 = activeFlag. |
| **`DLGMGR_CONT_29`** | `0x015354` | `0x00F982` | `dialog_mgr.s:1678`<br>`dialog_mgr.s:1647` | Handle updateEvt: redraw entire dialog within update region |
| **`DLGMGR_CONT_3`** | `0x0150F6` | `0x00F726` | `dialog_mgr.s:1265`<br>`dialog_mgr.s:1259` | — |
| **`DLGMGR_CONT_30`** | `0x015362` | `0x00F990` | `dialog_mgr.s:1691`<br>`dialog_mgr.s:1659` | Handle keyDown/autoKey: dispatch to TEKey or Tab-to-next-field. event.message low byte at -0x47(A6) = character code. |
| **`DLGMGR_CONT_31`** | `0x0153AC` | `0x00F9DA` | `dialog_mgr.s:1728`<br>`dialog_mgr.s:1694` | Reached end of DITL during Tab scan - wrap to beginning. Only wraps once (D5 tracks whether we already wrapped). |
| **`DLGMGR_CONT_32`** | `0x0153BC` | `0x00F9EA` | `dialog_mgr.s:1742`<br>`dialog_mgr.s:1707` | Handle mouseDown: convert click to local coords, find which DITL item was clicked, then dispatch by item type. |
| **`DLGMGR_CONT_33`** | `0x015482` | `0x00FAB0` | `dialog_mgr.s:1838`<br>`dialog_mgr.s:1800` | DLGMGR_CONT_33 -- install new field's text into shared TERec. |
| **`DLGMGR_CONT_34`** | `0x0154DE` | `0x00FB0C` | `dialog_mgr.s:1889`<br>`dialog_mgr.s:1849` | DLGMGR_CONT_34 - Test if item rect (expanded by 4 pixels) intersects portRect. Used during drawing to skip off-screen items. Returns Z=1 if no intersection. |
| **`DLGMGR_CONT_35`** | `0x0154E4` | `0x00FB12` | `dialog_mgr.s:1891`<br>`dialog_mgr.s:1851` | — |
| **`DLGMGR_CONT_36`** | `0x01557A` | `0x00FBA8` | `dialog_mgr.s:2007`<br>`dialog_mgr.s:1961` | DLGMGR_CONT_36 - Copy item's display rect to local frame variable. Copies 8 bytes from item+4 (display rect) to -0x28(A6). |
| **`DLGMGR_CONT_4`** | `0x0150FE` | `0x00F72E` | `dialog_mgr.s:1272`<br>`dialog_mgr.s:1265` | Load ICON resource for an iconItem |
| **`DLGMGR_CONT_5`** | `0x015106` | `0x00F736` | `dialog_mgr.s:1279`<br>`dialog_mgr.s:1271` | Load PICT resource for a picItem |
| **`DLGMGR_CONT_6`** | `0x01510C` | `0x00F73C` | `dialog_mgr.s:1281`<br>`dialog_mgr.s:1273` | — |
| **`DLGMGR_CONT_7`** | `0x015110` | `0x00F740` | `dialog_mgr.s:1283`<br>`dialog_mgr.s:1275` | — |
| **`DLGMGR_CONT_8`** | `0x015126` | `0x00F756` | `dialog_mgr.s:1298`<br>`dialog_mgr.s:1287` | DLGMGR_CONT_8 - mark handle purgeable if the resource itself is purgeable Called with D4=-1 during pre-load to preserve resource's purgeable attr. |
| **`DLGMGR_CONT_9`** | `0x01513A` | `0x00F76A` | `dialog_mgr.s:1314`<br>`dialog_mgr.s:1303` | Initialize item from DITL data (D4=0) A0 = item handle from DITL entry, D0 = item type byte If handle already set (non-nil), item was pre-initialized - skip. |
| **`DLGMGR_EMPTY`** | `0x015140` | `0x00F770` | `dialog_mgr.s:1324`<br>`dialog_mgr.s:1312` | Create item handle/control from DITL data based on item type. Dispatches by testing type bits: ctrlItem, iconItem, picItem, statText/editText. |
| **`DLGMGR_EMPTY_2`** | `0x01526C` | `0x00F89C` | `dialog_mgr.s:1520`<br>`dialog_mgr.s:1497` | — |
| **`DLGMGR_EMPTY_3`** | `0x0152CA` | `0x00F8F8` | `dialog_mgr.s:1575`<br>`dialog_mgr.s:1551` | — |
| **`DLGMGR_EXIT`** | `0x015350` | `0x00F97E` | `dialog_mgr.s:1671`<br>`dialog_mgr.s:1641` | Called by: DLGMGR_CONT_28, DLGMGR_SKIP_5, RETURNS_15, DLGMGR_CONT_29, DLGMGR_CONT_30 (and 3 more) |
| **`DLGMGR_EXIT_2`** | `0x0153AA` | `0x00F9D8` | `dialog_mgr.s:1721`<br>`dialog_mgr.s:1688` | — |
| **`DLGMGR_EXIT_3`** | `0x0153BA` | `0x00F9E8` | `dialog_mgr.s:1735`<br>`dialog_mgr.s:1701` | — |
| **`DLGMGR_EXIT_4`** | `0x01540E` | `0x00FA3C` | `dialog_mgr.s:1772`<br>`dialog_mgr.s:1737` | — |
| **`DLGMGR_EXIT_5`** | `0x01543A` | `0x00FA68` | `dialog_mgr.s:1794`<br>`dialog_mgr.s:1758` | — |
| **`DLGMGR_EXIT_6`** | `0x0154D8` | `0x00FB06` | `dialog_mgr.s:1872`<br>`dialog_mgr.s:1834` | — |
| **`DLGMGR_EXIT_7`** | `0x01555A` | `0x00FB88` | `dialog_mgr.s:1980`<br>`dialog_mgr.s:1936` | — |
| **`DLGMGR_EXIT_8`** | `0x015574` | `0x00FBA2` | `dialog_mgr.s:1998`<br>`dialog_mgr.s:1953` | — |
| **`DLGMGR_FOUND`** | `0x0151BE` | `0x00F7EE` | `dialog_mgr.s:1413`<br>`dialog_mgr.s:1395` | Hit test: check if item rect intersects update region (D4>2) Builds a temp rect from item's display rect, insets by -4 pixels (to include the 3-pixel frame around editText items), then tests intersect... |
| **`DLGMGR_FOUND_2`** | `0x0152A4` | `0x00F8D4` | `dialog_mgr.s:1558`<br>`dialog_mgr.s:1534` | Found '^' marker - look up which DAStrings[] entry to substitute. DAStrings (at DABeeper+4) holds 4 handles for ^0..^3 replacement text. D6 scans ASCII '0'..'3' (0x30..0x33) to match char after '^'. |
| **`DLGMGR_LOOP`** | `0x01527A` | `0x00F8AA` | `dialog_mgr.s:1533`<br>`dialog_mgr.s:1509` | Scan for '^' (0x5E) character - ParamText substitution marker. Text format: ^0, ^1, ^2, ^3 replaced by DAStrings[0..3]. |
| **`DLGMGR_LOOP_2`** | `0x015282` | `0x00F8B2` | `dialog_mgr.s:1538`<br>`dialog_mgr.s:1514` | — |
| **`DLGMGR_LOOP_3`** | `0x01555E` | `0x00FB8C` | `dialog_mgr.s:1989`<br>`dialog_mgr.s:1944` | DLGMGR_LOOP_3 - Skip one DITL item entry (variable-length). Each item: 4-byte handle + 8-byte rect + 1-byte type + 1-byte data length + data (padded to even boundary). |
| **`DLGMGR_NEXT`** | `0x0152AC` | `0x00F8DC` | `dialog_mgr.s:1561`<br>`dialog_mgr.s:1537` | — |
| **`DLGMGR_NEXT_2`** | `0x01537C` | `0x00F9AA` | `dialog_mgr.s:1706`<br>`dialog_mgr.s:1673` | Tab key: find next editText item in DITL and switch to it. Wraps around from last editText to first editText. |
| **`DLGMGR_NEXT_3`** | `0x0153CA` | `0x00F9F8` | `dialog_mgr.s:1747`<br>`dialog_mgr.s:1712` | — |
| **`DLGMGR_NEXT_4`** | `0x01553A` | `0x00FB68` | `dialog_mgr.s:1953`<br>`dialog_mgr.s:1910` | DLGMGR_NEXT_4 - Advance to the next DITL item. Increments D3 (item index), then positions A2 at next item. If D3 was -1 (no current item), falls into DLGMGR_OK_3 to start from the beginning. Returns Z... |
| **`DLGMGR_NO`** | `0x015138` | `0x00F768` | `dialog_mgr.s:1306`<br>`dialog_mgr.s:1296` | — |
| **`DLGMGR_NO_2`** | `0x01519A` | `0x00F7CA` | `dialog_mgr.s:1388`<br>`dialog_mgr.s:1371` | Create standard button/checkbox/radio control from DITL inline data. Builds NewControl params: owner, rect, title, visible, value=1, min=0, procID=subtype*16, refCon=0. |
| **`DLGMGR_NO_3`** | `0x015260` | `0x00F890` | `dialog_mgr.s:1514`<br>`dialog_mgr.s:1491` | Draw statText/editText with ParamText (^0..^3) substitution. Makes a copy of the text handle, scans for '^' markers, substitutes from DAStrings[0..3], then draws via TextBox. |
| **`DLGMGR_NO_4`** | `0x015322` | `0x00F950` | `dialog_mgr.s:1640`<br>`dialog_mgr.s:1610` | — |
| **`DLGMGR_NO_5`** | `0x015410` | `0x00FA3E` | `dialog_mgr.s:1779`<br>`dialog_mgr.s:1743` | Click was in a non-control item: check if editText. If editText, switch edit field and pass click to TEClick. |
| **`DLGMGR_OK`** | `0x015422` | `0x00FA50` | `dialog_mgr.s:1786`<br>`dialog_mgr.s:1750` | — |
| **`DLGMGR_OK_2`** | `0x0154DA` | `0x00FB08` | `dialog_mgr.s:1880`<br>`dialog_mgr.s:1841` | DLGMGR_OK_2 - Test if item display rect is within dialog's portRect. Returns Z=1 if no intersection (item not visible). Uses inset=0 (exact rect bounds). |
| **`DLGMGR_OK_3`** | `0x015544` | `0x00FB72` | `dialog_mgr.s:1967`<br>`dialog_mgr.s:1923` | DLGMGR_OK_3 - Position A2 at DITL item number D3. Walks the variable-length DITL item list from the beginning, skipping D3 items to reach the target. D7 accumulates byte offset. Returns A2 = ptr to it... |
| **`DLGMGR_OK_4`** | `0x01556C` | `0x00FB9A` | `dialog_mgr.s:1994`<br>`dialog_mgr.s:1949` | — |
| **`DLGMGR_SKIP`** | `0x015218` | `0x00F848` | `dialog_mgr.s:1457`<br>`dialog_mgr.s:1438` | — |
| **`DLGMGR_SKIP_10`** | `0x0154CA` | `0x00FAF8` | `dialog_mgr.s:1866`<br>`dialog_mgr.s:1828` | — |
| **`DLGMGR_SKIP_11`** | `0x01554C` | `0x00FB7A` | `dialog_mgr.s:1972`<br>`dialog_mgr.s:1928` | — |
| **`DLGMGR_SKIP_2`** | `0x015234` | `0x00F864` | `dialog_mgr.s:1480`<br>`dialog_mgr.s:1459` | — |
| **`DLGMGR_SKIP_3`** | `0x01525E` | `0x00F88E` | `dialog_mgr.s:1506`<br>`dialog_mgr.s:1484` | — |
| **`DLGMGR_SKIP_4`** | `0x015280` | `0x00F8B0` | `dialog_mgr.s:1536`<br>`dialog_mgr.s:1512` | — |
| **`DLGMGR_SKIP_5`** | `0x015324` | `0x00F952` | `dialog_mgr.s:1642`<br>`dialog_mgr.s:1612` | — |
| **`DLGMGR_SKIP_6`** | `0x015386` | `0x00F9B4` | `dialog_mgr.s:1710`<br>`dialog_mgr.s:1677` | — |
| **`DLGMGR_SKIP_7`** | `0x01546C` | `0x00FA9A` | `dialog_mgr.s:1820`<br>`dialog_mgr.s:1783` | — |
| **`DLGMGR_SKIP_8`** | `0x01547A` | `0x00FAA8` | `dialog_mgr.s:1826`<br>`dialog_mgr.s:1789` | — |
| **`DLGMGR_SKIP_9`** | `0x0154A0` | `0x00FACE` | `dialog_mgr.s:1850`<br>`dialog_mgr.s:1812` | — |
| **`DMGR`** | — | `0x00EECA` | `dialog_mgr.s:21` | Dialog Manager Apple source: DialogMgr.a (MacSEROM.lst module DMGR). The public traps come first, in physical ROM order: InitDialogs                                     (initialization) StopAlert, Not... |
| **`DMGREND`** | — | `0x00FBB6` | `toolbox_utils.s:26` | Toolbox Utilities: byte-string munger, handle/pointer copying and MacApp method dispatch Routines, in physical ROM order: _Munger ($A9E0), _XMunger ($A819)  search/replace/insert/delete bytes in a han... |
| **`DragControl`** | `0x0130AE` | `0x00D6B2` | `control_mgr.s:563` | _DragControl ($A967) |
| **`DRAGCONTROL`** | `0x0130AE` | `0x00D6B2` | `control_mgr.s:477` | **Proto:** `Pascal: procedure DragControl(theControl: ControlHandle; startPt: Point;`<br>_DragControl ($A967): drag a control by its outline (XOR rect). Pascal: procedure DragControl(theControl: ControlHandle; startPt: Point; limitRect: Rect; slopRect: Rect; axis: INTEGER); Sets DragFlag ... |
| **`DRAGCONTROL_CONT`** | `0x0130B2` | `0x00D6B6` | `control_mgr.s:566`<br>`control_mgr.s:481` | DRAGCONTROL_CONT -- drag the thumb region. |
| **`DRAGCONTROL_CONT_2`** | `0x013142` | `0x00D746` | `control_mgr.s:636`<br>`control_mgr.s:550` | DRAGCONTROL_CONT_2 Called during boot. DRAGCONTROL_CONT_2: save current port, then set port to control's owner window Leaves saved port on stack for later _SetPort restore |
| **`DRAGCONTROL_DONE`** | `0x013130` | `0x00D734` | `control_mgr.s:620`<br>`control_mgr.s:536` | Common drag exit: restore port, return delta in D1. |
| **`DRAGCONTROL_EXIT`** | `0x013110` | `0x00D714` | `control_mgr.s:599`<br>`control_mgr.s:514` | — |
| **`DRAGCONTROL_NO`** | `0x013114` | `0x00D718` | `control_mgr.s:607`<br>`control_mgr.s:522` | DRAGCONTROL_NO: apply drag movement to control position |
| **`DRAGCONTROL_OK`** | `0x013100` | `0x00D704` | `control_mgr.s:591`<br>`control_mgr.s:506` | — |
| **`DRAGGRAY_RATE_LIMIT`** | — | `0x00C5C2` | `window_mgr.s:2035` | — |
| **`DragGrayRgn`** | `0x011E5A` | `0x00C50A` | `window_mgr.s:2066` | _DragGrayRgn ($A905): drag a gray outline region tracking the mouse Sets up gray pattern, falls into DragTheRgn. |
| **`DRAGGRAYRGN`** | `0x011E5A` | `0x00C50A` | `window_mgr.s:1935` | _DragGrayRgn ($A905): drag a gray outline region tracking the mouse Sets up gray pattern, falls into DragTheRgn. |
| **`DragTheRgn`** | `0x011E66` | `0x00C516` | `window_mgr.s:2072` | _DragTheRgn ($A926): generic region-dragging loop Stack params: region, startPt, limitRect, slopRect, axis, actionProc Returns: packed dv:dh offset (0x80008000 if cancelled) |
| **`DRAGTHERGN`** | `0x011E66` | `0x00C516` | `window_mgr.s:1944` | _DragTheRgn ($A926): generic region-dragging loop Stack params: region, startPt, limitRect, slopRect, axis, actionProc Returns: packed dv:dh offset (0x80008000 if cancelled). |
| **`DRAGTHERGN_CONT`** | `0x011EC4` | `0x00C574` | `window_mgr.s:2116`<br>`window_mgr.s:1988` | mouse inside limit rect: compute delta and move outline |
| **`DRAGTHERGN_CONT_2`** | `0x011EE4` | `0x00C594` | `window_mgr.s:2139`<br>`window_mgr.s:2010` | apply axis constraint DRAGTHERGN_NO - horizontal only: zero vertical delta |
| **`DRAGTHERGN_CONT_3`** | `0x011F50` | `0x00C600` | `window_mgr.s:2201`<br>`window_mgr.s:2069` | DRAGTHERGN_CONT_3 DRAGTHERGN_CONT_3 - call DragHook if installed; DRAGTHERGN_EMPTY - call proc in D0 if non-nil Called during boot. |
| **`DRAGTHERGN_CONT_4`** | `0x011F5C` | `0x00C60C` | `window_mgr.s:2215`<br>`window_mgr.s:2082` | DRAGTHERGN_CONT_4 - mouse outside limitRect: check slopRect and toggle outline |
| **`DRAGTHERGN_CONT_5`** | `0x011F70` | `0x00C620` | `window_mgr.s:2226`<br>`window_mgr.s:2093` | outside slop rect: erase outline if drawn |
| **`DRAGTHERGN_EMPTY`** | `0x011F54` | `0x00C604` | `window_mgr.s:2204`<br>`window_mgr.s:2072` | DRAGTHERGN_EMPTY -- call actionProc if non-nil. |
| **`DRAGTHERGN_NO`** | `0x011EE2` | `0x00C592` | `window_mgr.s:2137`<br>`window_mgr.s:2008` | apply axis constraint DRAGTHERGN_NO - horizontal only: zero vertical delta |
| **`DRAGTHERGN_NO_2`** | `0x011F12` | — | `window_mgr.s:2164` | — |
| **`DRAGTHERGN_OK`** | `0x011EB0` | `0x00C560` | `window_mgr.s:2106`<br>`window_mgr.s:1978` | set up XOR pen for gray outline drawing create outline: region minus inset copy (hollow frame) draw initial outline main tracking loop |
| **`DRAGTHERGN_OK_2`** | `0x011F42` | `0x00C5F2` | `window_mgr.s:2188`<br>`window_mgr.s:2058` | check if release point is inside slopRect (cancel if outside) |
| **`DRAGTHERGN_OK_3`** | `0x011F76` | `0x00C626` | `window_mgr.s:2235`<br>`window_mgr.s:2101` | DRAGTHERGN_OK_3 - mouse in slopRect but outside limitRect: redraw outline if needed |
| **`DRAGTHERGN_OK_4`** | `0x011F7E` | `0x00C62E` | `window_mgr.s:2245`<br>`window_mgr.s:2110` | DRAGTHERGN_OK_4 - pin mouse to limitRect edge (clamp to nearest boundary) |
| **`DRAGTHERGN_SKIP`** | `0x011EFA` | `0x00C5AA` | `window_mgr.s:2151`<br>`window_mgr.s:2022` | accumulate deltas into result erase old outline and draw new one at offset position |
| **`DRAGTHERGN_SKIP_2`** | `0x011F04` | `0x00C5B4` | `window_mgr.s:2158`<br>`window_mgr.s:2029` | call actionProc and DragHook, then wait |
| **`DRAGTHERGN_SKIP_3`** | `0x011F28` | `0x00C5D8` | `window_mgr.s:2176`<br>`window_mgr.s:2047` | mouse released: erase final outline and return result |
| **`DRAGTHERGN_SKIP_4`** | `0x011F5A` | `0x00C60A` | `window_mgr.s:2208`<br>`window_mgr.s:2076` | — |
| **`DragWindow`** | `0x011D9C` | `0x00C448` | `window_mgr.s:1970` | **Proto:** `Pascal: procedure DragWindow(theWindow: WindowPtr; startPt: Point;`<br>_DragWindow ($A925) stack: window, startPt, boundsRect -> (handles drag) _DragWindow ($A925): drag a window to a new position Draws gray outline while tracking mouse, moves window on release Pascal: p... |
| **`DRAGWINDOW`** | `0x011D9C` | `0x00C448` | `window_mgr.s:1835` | **Proto:** `Pascal: procedure DragWindow(theWindow: WindowPtr; startPt: Point;`<br>_DragWindow ($A925): drag a window to a new position Pascal: procedure DragWindow(theWindow: WindowPtr; startPt: Point; boundsRect: Rect); Draws gray outline while tracking mouse, moves window on rele... |
| **`DRAGWINDOW_BEGIN_GRAY`** | — | `0x00C498` | `window_mgr.s:1867` | build local drag bounds rect check if Command key held (for "bring to front" behavior) |
| **`DRAGWINDOW_EMPTY`** | `0x011E48` | `0x00C4F8` | `window_mgr.s:2048`<br>`window_mgr.s:1914` | DRAGWINDOW_EMPTY - zero drag offset: window not moved, select if Cmd not held |
| **`DRAGWINDOW_NO`** | `0x011E3E` | `0x00C4EE` | `window_mgr.s:2039`<br>`window_mgr.s:1906` | — |
| **`DRAGWINDOW_OK`** | `0x011DC2` | `0x00C46C` | `window_mgr.s:1985`<br>`window_mgr.s:1850` | clamp drag bounds to keep title bar visible |
| **`DRAGWINDOW_SKIP`** | `0x011DEE` | — | `window_mgr.s:2002` | build local drag bounds rect check if Command key held (for "bring to front" behavior) |
| **`DRAGWINDOW_SKIP_2`** | `0x011E36` | `0x00C4E6` | `window_mgr.s:2035`<br>`window_mgr.s:1902` | copy strucRgn and initiate gray drag tracking evaluate drag result compute new window position from drag offset |
| **`Draw1Control`** | `0x012ECC` | — | `control_mgr.s:224` | **Proto:** `Pascal: PROCEDURE Draw1Control(theControl: ControlHandle);`<br>**Regs:** `Entry: 0x4(SP) = theControl. Saves A3 and joins ShowControl at`<br>_Draw1Control ($A96D): draw one control if it is visible Pascal: PROCEDURE Draw1Control(theControl: ControlHandle); Apple source name: DrawOneControl (System 7.1 ControlMgr.a; MacSEROM.lst DRAWONECONT... |
| **`DrawControls`** | `0x01325E` | `0x00D862` | `control_mgr.s:796` | _DrawControls ($A969) Called during boot. |
| **`DRAWCONTROLS`** | `0x01325E` | `0x00D862` | `control_mgr.s:703` | **Proto:** `Pascal: procedure DrawControls(theWindow: WindowPtr);`<br>_DrawControls ($A969): redraw all visible controls in a window. Pascal: procedure DrawControls(theWindow: WindowPtr); |
| **`DRAWCONTROLS_CONT`** | `0x013286` | `0x00D88A` | `control_mgr.s:814`<br>`control_mgr.s:721` | DRAWCONTROLS_CONT: walk control list and draw each |
| **`DRAWCONTROLS_CONT_2`** | `0x0132BE` | `0x00D8C2` | `control_mgr.s:850`<br>`control_mgr.s:754` | DRAWCONTROLS_CONT_2 Called during boot. DRAWCONTROLS_CONT_2: unlink handle A0 from linked list headed at (A1) Each node: handle -> [nextHandle, ...], list head at (A1) Returns D0=0 if found, D0=-1 if ... |
| **`DRAWCONTROLS_CONT_3`** | `0x0132D6` | `0x00D8DA` | `control_mgr.s:868`<br>`control_mgr.s:768` | — |
| **`DRAWCONTROLS_DONE`** | `0x0132AC` | `0x00D8B0` | `control_mgr.s:832`<br>`control_mgr.s:739` | — |
| **`DRAWCONTROLS_FOUND`** | `0x0132E0` | `0x00D8E4` | `control_mgr.s:874`<br>`control_mgr.s:774` | — |
| **`DRAWCONTROLS_LOOP`** | `0x01326C` | `0x00D870` | `control_mgr.s:801`<br>`control_mgr.s:708` | — |
| **`DRAWCONTROLS_NEXT`** | `0x0132CE` | `0x00D8D2` | `control_mgr.s:863`<br>`control_mgr.s:763` | DRAWCONTROLS_NEXT: advance to next node in linked list |
| **`DRAWCONTROLS_NO`** | `0x0132A0` | `0x00D8A4` | `control_mgr.s:825`<br>`control_mgr.s:732` | — |
| **`DRAWCONTROLS_SKIP`** | `0x0132A6` | `0x00D8AA` | `control_mgr.s:828`<br>`control_mgr.s:735` | — |
| **`DrawDialog`** | `0x014C68` | `0x00F28A` | `dialog_mgr.s:542` | _DrawDialog ($A981) Called during boot. |
| **`DRAWDIALOG`** | `0x014C68` | `0x00F28A` | `dialog_mgr.s:547` | _DrawDialog ($A981) -- redraw a dialog window's items. Stack: theDialog(L). Draws controls and items via FINDDITEM_CONT with operation = 1 (draw all items). |
| **`DrawGrowIcon`** | `0x01217A` | `0x00C836` | `window_mgr.s:2609` | **Proto:** `Pascal: procedure DrawGrowIcon(theWindow: WindowPtr);`<br>_DrawGrowIcon ($A904) stack: window -> (draws size box) _DrawGrowIcon ($A904): draw the size box in a window's lower-right corner Pascal: procedure DrawGrowIcon(theWindow: WindowPtr); Sends wGrow+1=6 ... |
| **`DRAWGROWICON`** | `0x01217A` | `0x00C836` | `window_mgr.s:2433` | **Proto:** `Pascal: procedure DrawGrowIcon(theWindow: WindowPtr);`<br>_DrawGrowIcon ($A904): draw the size box in a window's lower-right corner Pascal: procedure DrawGrowIcon(theWindow: WindowPtr); Sends wGrowIcon=6 message to WDEF. |
| **`DRAWMBAR`** | — | `0x00CAE4` | `menu_mgr.s:269` | DrawMBar (MBDF helper): force MBDF redraw with no flash flag. param = -1 means "internal redraw" (skip alarm-bit reset). |
| **`DrawMenuBar`** | `0x012350` | `0x00CAEE` | `menu_mgr.s:297` | _DrawMenuBar ($A937) -> (redraws menu bar) Called during boot. |
| **`DRAWMENUBAR`** | `0x012350` | `0x00CAEE` | `menu_mgr.s:279` | **Proto:** `Pascal: procedure DrawMenuBar;`<br>_DrawMenuBar ($A937): redraw the entire menu bar. Pascal: procedure DrawMenuBar; Sets AlarmState bit 7 (alarm acknowledged) so the apple icon won't flash. |
| **`DRAWMENUBAR_CONT`** | `0x0123AA` | — | `menu_mgr.s:335` | DRAWMENUBAR_CONT - dim disabled menu title with gray pattern |
| **`DRAWMENUBAR_CONT_2`** | `0x0123C4` | — | `menu_mgr.s:354` | DRAWMENUBAR_CONT_2 -- paint gray over title (dim effect). DRAWMENUBAR_CONT_2 |
| **`DRAWMENUBAR_DONE`** | `0x0123BA` | — | `menu_mgr.s:344` | — |
| **`DRAWMENUBAR_NEXT`** | `0x01237A` | — | `menu_mgr.s:312` | — |
| **`DRAWMENUBAR_NEXT_2`** | `0x0123B4` | — | `menu_mgr.s:340` | — |
| **`DrawNew`** | `0x01143C` | `0x00BA90` | `window_mgr.s:516` | **Proto:** `Pascal: procedure DrawNew(theWindow: WindowPeek; fUpdate: BOOLEAN);`<br>_DrawNew ($A90F) _DrawNew ($A90F): repaint changed areas after window modification Pascal: procedure DrawNew(theWindow: WindowPeek; fUpdate: BOOLEAN); Compares current regions with SaveOld snapshots v... |
| **`DRAWNEW`** | `0x01143C` | `0x00BA90` | `window_mgr.s:478` | **Proto:** `Pascal: procedure DrawNew(theWindow: WindowPeek; fUpdate: BOOLEAN);`<br>_DrawNew ($A90F): repaint changed areas after window modification Pascal: procedure DrawNew(theWindow: WindowPeek; fUpdate: BOOLEAN); Compares current regions with SaveOld snapshots via XOR to find ch... |
| **`DRAWNEW_EXIT`** | `0x011496` | `0x00BAEA` | `window_mgr.s:552`<br>`window_mgr.s:514` | DRAWNEW_EXIT - strip 6 bytes of params (window + fUpdate) and return |
| **`DRAWNEW_SKIP`** | `0x011464` | `0x00BAB8` | `window_mgr.s:530`<br>`window_mgr.s:492` | — |
| **`DRAWONECONTROL`** | — | `0x00D4D0` | `control_mgr.s:193` | **Proto:** `Pascal: procedure Draw1Control(theControl: ControlHandle);`<br>_Draw1Control ($A96D): redraw one control unconditionally. Pascal: procedure Draw1Control(theControl: ControlHandle); |
| **`DT_mMaxIAppend`** | `0x0148A8` | — | `dialog_mgr.s:28` | Dialog Manager Apple source: DialogMgr.a (MacSEROM.lst module DMGR). The public traps come first, in physical ROM order: InitDialogs                                     (initialization) StopAlert, Not... |
| **`DT_MMAXIAPPEND_EMPTY`** | `0x0148B0` | `0x00EED2` | `dialog_mgr.s:33`<br>`dialog_mgr.s:26` | DT_MMAXIAPPEND_EMPTY: empty Pascal string (length=0), used as dialog title |
| **`DT_mWMgrGray`** | `0x011E52` | — | `window_mgr.s:2059` | Window Manager gray pattern (50% checkerboard, same as QD gray): #.#.#.#. 0xAA Used for window drag outlines .#.#.#.# 0x55 and desktop background pattern (repeats) |
| **`DT_mWMgrGray_4`** | `0x011E56` | `0x00C506` | `window_mgr.s:2061`<br>`window_mgr.s:1927` | — |
| **`EnableItem`** | `0x012404` | `0x00CB4A` | `menu_mgr.s:391` | _EnableItem ($A939) Called during boot (60,959 times in 30s trace). |
| **`ENABLEITEM`** | `0x012404` | `0x00CB4A` | `menu_mgr.s:326` | **Proto:** `Pascal: procedure EnableItem(theMenu: MenuHandle; item: INTEGER);`<br>_EnableItem ($A93A): enable a menu item. Pascal: procedure EnableItem(theMenu: MenuHandle; item: INTEGER); item=0 enables the entire menu (item-0 = title flag). |
| **`ENABLEITEM_CONT`** | `0x012410` | `0x00CB56` | `menu_mgr.s:403`<br>`menu_mgr.s:338` | ENABLEITEM_CONT Called during boot (157,003 times in 30s trace). |
| **`ENABLEITEM_EXIT`** | `0x012408` | `0x00CB4E` | `menu_mgr.s:394`<br>`menu_mgr.s:329` | — |
| **`EndUpdate`** | `0x011D50` | `0x00C3F6` | `window_mgr.s:1911` | **Proto:** `Pascal: procedure EndUpdate(theWindow: WindowPtr);`<br>_EndUpDate ($A923) stack: window -> (restores visRgn) _EndUpdate ($A923): restore visRgn after update drawing is complete Pascal: procedure EndUpdate(theWindow: WindowPtr); Converts SaveVisRgn back to... |
| **`ENDUPDATE`** | `0x011D50` | `0x00C3F6` | `window_mgr.s:1782` | **Proto:** `Pascal: procedure EndUpdate(theWindow: WindowPtr);`<br>_EndUpdate ($A923): restore visRgn after update drawing is complete Pascal: procedure EndUpdate(theWindow: WindowPtr); |
| **`ENSUREINIT_RTS`** | `0x016F48` | `0x012792` | `scrap_mgr.s:367`<br>`scrap_mgr.s:300` | scrap uninitialized: create empty scrap |
| **`ENTRY`** | `0x0150B2` | `0x00F6E2` | `dialog_mgr.s:1231`<br>`dialog_mgr.s:1227` | **Regs:** `Entry: A2 = ptr to DITL item entry, D4 = mode (0=init, 1=draw, 2=hitTest)`<br>Dialog Manager -- internal routines The subroutines called by the public traps above: item initialization from the DITL, item drawing and disposal, event dispatch, edit-field switching, hit testing, P... |
| **`ENTRY_2`** | `0x015448` | — | `dialog_mgr.s:1807` | **Regs:** `Entry: D3 = new field index (0-based), D2 = selection range.`<br>ENTRY_2 - Switch active edit field. Deactivates current TE (scrolling it back to origin), calls DLGMGR_CONT_33 to install new field's text into TE, then activates TE. Entry: D3 = new field index (0-ba... |
| **`ENTRY_3`** | `0x01547C` | — | `dialog_mgr.s:1834` | **Regs:** `Entry: D3 = target field index, D2 = selection range.`<br>ENTRY_3 - Check if edit field changed, then install new field. Entry: D3 = target field index, D2 = selection range. Falls through to DLGMGR_CONT_33 if field is different. |
| **`ENTRY_4`** | `0x015508` | — | `dialog_mgr.s:1912` | **Regs:** `Entry: A0 = ptr to rect, D0 = pen width, D1 = pen height,`<br>ENTRY_4 - Draw a rounded-rect frame around an item rect. Entry: A0 = ptr to rect, D0 = pen width, D1 = pen height, D2 = outward inset (positive = expand outward). Expands rect outward by D2, frames it... |
| **`ENTRY_5`** | `0x01552A` | — | `dialog_mgr.s:1938` | **Regs:** `Entry: A0 = ptr to Pascal string. Exit: A0 = new string handle. Preserves D1-D2, A1-A2.`<br>ENTRY_5 - Create a new string handle from a Pascal string. Entry: A0 = ptr to Pascal string. Exit: A0 = new string handle. Preserves D1-D2, A1-A2. Note: saves D0-D2/A1-A2 but restores D1-D2/A1-A2 only... |
| **`ErrorSound`** | `0x014E32` | `0x00F462` | `dialog_mgr.s:861` | **Proto:** `ErrorSound -- _ErrorSound ($A98C): PROCEDURE ErrorSound (soundProc: ProcPtr);`<br>ErrorSound -- _ErrorSound ($A98C): PROCEDURE ErrorSound (soundProc: ProcPtr); _ErrorSound ($A98C) |
| **`ERRORSOUND`** | `0x014E32` | `0x00F462` | `dialog_mgr.s:854` | _ErrorSound ($A98C) -- install custom beep procedure. Stack: soundProc(L). Stores caller's procptr in DABeeper. Used by ALERT_CONT_6 to play stage-encoded beep sequences. |
| **`EventAvail`** | `0x010FFC` | `0x00B5C8` | `toolbox_event.s:185` | **Proto:** `Pascal: FUNCTION EventAvail(eventMask: INTEGER; VAR theEvent: EventRecord): BOOLEAN`<br>_EventAvail ($A971) Pascal: FUNCTION EventAvail(eventMask: INTEGER; VAR theEvent: EventRecord): BOOLEAN Peeks at the event queue without removing any event. Sets D0 = -1 as flag so TBOX_GET_EVENT call... |
| **`EVENTAVAIL`** | `0x010FFC` | `0x00B5C8` | `toolbox_event.s:166` | _EventAvail ($A971) Sets D0 = -1 so TBOX_GET_EVENT calls OSEventAvail (peek). |
| **`FIND_PREV_WINDOW`** | `0x0111CE` | `0x00B816` | `window_mgr.s:87`<br>`window_mgr.s:100` | FIND_PREV_WINDOW - Find predecessor of a window in the window list Walks WindowList (linked via nextWindow at offset 0x90) to find the window whose nextWindow field points to D0. Returns A0 = predeces... |
| **`FindControl`** | `0x0132E6` | `0x00D8EA` | `control_mgr.s:886` | **Proto:** `Pascal: function FindControl(thePoint: Point; theWindow: WindowPtr;`<br>_FindControl ($A96C) Called during boot. _FindControl ($A96C): find which control contains a point Pascal: function FindControl(thePoint: Point; theWindow: WindowPtr; VAR whichControl: ControlHandle):... |
| **`FINDCONTROL`** | `0x0132E6` | `0x00D8EA` | `control_mgr.s:783` | **Proto:** `Pascal: function FindControl(thePoint: Point; theWindow: WindowPtr;`<br>_FindControl ($A96C): which control (if any) contains the point? Pascal: function FindControl(thePoint: Point; theWindow: WindowPtr; var whichControl: ControlHandle): INTEGER; Returns part code (0 if ... |
| **`FINDCONTROL_FOUND`** | `0x013348` | `0x00D94C` | `control_mgr.s:934`<br>`control_mgr.s:826` | FINDCONTROL_FOUND: found a hit -- store result and continue searching (last hit wins, so deeper controls take priority) Called during boot. |
| **`FINDCONTROL_NEXT`** | `0x013326` | `0x00D92A` | `control_mgr.s:911`<br>`control_mgr.s:808` | FINDCONTROL_NEXT: walk control list testing each |
| **`FINDCONTROL_SKIP`** | `0x01333C` | `0x00D940` | `control_mgr.s:921`<br>`control_mgr.s:818` | — |
| **`FindDItem`** | `0x015064` | `0x00F694` | `dialog_mgr.s:1155` | Find D Item |
| **`FINDDITEM`** | `0x015064` | `0x00F694` | `dialog_mgr.s:1145` | _FindDItem ($A984) -- find dialog item containing a point. Stack: theDialog(L), pt(L) -> itemIndex(W). Walks all items testing _PtInRect against the point. Returns 0-based item index or -1 if not in a... |
| **`FINDDITEM_CONT`** | `0x015098` | `0x00F6C8` | `dialog_mgr.s:1180`<br>`dialog_mgr.s:1173` | FINDDITEM_CONT Called during boot. |
| **`FINDDITEM_CONT_2`** | `0x0150AA` | `0x00F6DA` | `dialog_mgr.s:1194`<br>`dialog_mgr.s:1187` | FINDDITEM_CONT_2 - get item handle and type from item entry Called during boot. |
| **`FINDDITEM_EXIT`** | `0x015090` | — | `dialog_mgr.s:1171` | — |
| **`FINDDITEM_EXIT_2`** | `0x01509E` | — | `dialog_mgr.s:1183` | — |
| **`FINDDITEM_INNER_LOOP`** | — | `0x00F6CE` | `dialog_mgr.s:1176` | — |
| **`FINDDITEM_NEXT`** | `0x015076` | — | `dialog_mgr.s:1161` | — |
| **`FINDDITEM_UNLOCK`** | — | `0x00F6C0` | `dialog_mgr.s:1161` | — |
| **`FINDDITEM_WALK`** | — | `0x00F6A6` | `dialog_mgr.s:1151` | — |
| **`FINDNEXT_ALL`** | `0x01387A` | `0x00DE7C` | `resource_mgr.s:791`<br>`resource_mgr.s:769` | FINDNEXT_ALL - FindNext (from beginning of all maps) Searches all resource maps for the next reference entry whose data offset is greater than the current position. Used by UpdateResFile to iterate re... |
| **`FINDNEXT_ALL_LOOP`** | `0x0138CA` | `0x00DECC` | `resource_mgr.s:847`<br>`resource_mgr.s:823` | FINDNEXT_ALL_LOOP - FindNext inner loop (all entries, no flag check) Scans all reference entries for the one with the smallest data offset that is still greater than the minimum in D2. Called during b... |
| **`FINDNEXT_ALL_SKIP`** | `0x0138DE` | `0x00DEE0` | `resource_mgr.s:856`<br>`resource_mgr.s:832` | — |
| **`FINDNEXT_CUR_OFS`** | `0x013882` | `0x00DE84` | `resource_mgr.s:809`<br>`resource_mgr.s:786` | FINDNEXT_CUR_OFS -- find next changed entry after current. |
| **`FINDNEXT_DONE`** | `0x0138E6` | `0x00DEE8` | `resource_mgr.s:859`<br>`resource_mgr.s:835` | — |
| **`FINDNEXT_ENTER`** | `0x01388A` | `0x00DE8C` | `resource_mgr.s:812`<br>`resource_mgr.s:789` | — |
| **`FINDNEXT_FLAG_LOOP`** | `0x0138A6` | `0x00DEA8` | `resource_mgr.s:824`<br>`resource_mgr.s:801` | — |
| **`FINDNEXT_FLAG_SKIP`** | `0x0138C0` | `0x00DEC2` | `resource_mgr.s:835`<br>`resource_mgr.s:812` | — |
| **`FINDNEXT_FROM_CUR`** | `0x013880` | `0x00DE82` | `resource_mgr.s:806`<br>`resource_mgr.s:783` | FINDNEXT_FROM_CUR - FindNext (from current entry's offset) Searches for the next resource entry whose data offset is greater than the current entry's offset. Used during UpdateResFile compaction to pr... |
| **`FINDNEXT_FROM_START`** | `0x01387C` | `0x00DE7E` | `resource_mgr.s:794`<br>`resource_mgr.s:772` | FINDNEXT_FROM_START -- findNext from beginning, changed only. |
| **`FINDNEXT_RET`** | `0x0138F4` | `0x00DEF6` | `resource_mgr.s:865`<br>`resource_mgr.s:841` | — |
| **`FINDRESHANDLE`** | — | `0x00EB94` | `resource_mgr.s:2923` | FINDRESHANDLE -- find ref entry by handle, set ResErr on failure. Wrapper around RESMGR_CONT_12 that sets ResErr=resNotFound (-192) if the handle isn't in any map. Returns Z=1 on found, Z=0 on miss. C... |
| **`FINDRESHANDLE_RTS`** | — | `0x00EBA0` | `resource_mgr.s:2927` | — |
| **`FindWindow`** | `0x0120F6` | `0x00C7B2` | `window_mgr.s:2491` | _FindWindow ($A92C) stack: pt -> stack: partCode, WindowPtr Called during boot (3,695 times in 30s trace). _FindWindow ($A92C): determine which window part contains a point Returns: inDesk=0, inMenuBa... |
| **`FINDWINDOW`** | `0x0120F6` | `0x00C7B2` | `window_mgr.s:2336` | **Proto:** `Pascal: function FindWindow(thePoint: Point; VAR theWindow: WindowPtr): INTEGER;`<br>_FindWindow ($A92C): determine which window part contains a point Pascal: function FindWindow(thePoint: Point; VAR theWindow: WindowPtr): INTEGER; Returns: inDesk=0, inMenuBar=1, inSysWindow=2, inCont... |
| **`FINDWINDOW_CONT`** | `0x012152` | `0x00C80E` | `window_mgr.s:2559`<br>`window_mgr.s:2397` | FINDWINDOW_CONT - translate WDEF hit code to FindWindow partCode WDEF returns: 1=content, 2=drag, 3+=grow/goAway/zoom FindWindow returns: 3=inContent, 4=inDrag, 5+=inGrow/inGoAway/inZoom Called during... |
| **`FINDWINDOW_CONT_2`** | `0x01215E` | `0x00C81A` | `window_mgr.s:2571`<br>`window_mgr.s:2408` | FINDWINDOW_CONT_2 - WDEF code > 2: add 2 to get FindWindow code (3->5, 4->6, etc.) Called during boot. |
| **`FINDWINDOW_CONT_3`** | `0x012162` | `0x00C81E` | `window_mgr.s:2581`<br>`window_mgr.s:2411` | FINDWINDOW_CONT_3 FINDWINDOW_CONT_3 - WDEF code 1 = content area Called during boot (1,018 times in 30s trace). |
| **`FINDWINDOW_EXIT`** | `0x012150` | `0x00C80C` | `window_mgr.s:2549`<br>`window_mgr.s:2388` | — |
| **`FINDWINDOW_EXIT_2`** | `0x012164` | `0x00C820` | `window_mgr.s:2583`<br>`window_mgr.s:2414` | Called by: FINDWINDOW_OK_2, FINDWINDOW_EXIT, FINDWINDOW_CONT, FINDWINDOW_CONT_2 |
| **`FINDWINDOW_LOOP`** | `0x01211A` | `0x00C7D6` | `window_mgr.s:2515`<br>`window_mgr.s:2357` | — |
| **`FINDWINDOW_NO`** | `0x012116` | `0x00C7D2` | `window_mgr.s:2513`<br>`window_mgr.s:2355` | check if point is in menu bar FINDWINDOW_NO FINDWINDOW_NO - scan window list for window containing the point Called during boot (2,682 times in 30s trace). |
| **`FINDWINDOW_OK`** | `0x012142` | `0x00C7FE` | `window_mgr.s:2543`<br>`window_mgr.s:2382` | FINDWINDOW_OK FINDWINDOW_OK - point hit a window: translate WDEF result to FindWindow code WDEF wHit returns: 0=miss, 1=content, 2=drag, 3=grow, 4+=go-away/zoom Called during boot (1,323 times in 30s ... |
| **`FINDWINDOW_OK_2`** | `0x012170` | `0x00C82C` | `window_mgr.s:2594`<br>`window_mgr.s:2422` | FINDWINDOW_OK_2 FINDWINDOW_OK_2 - no window hit: check if DeskHook claims clicks Called during boot (1,359 times in 30s trace). |
| **`FINDWINDOW_SKIP`** | `0x01213C` | `0x00C7F8` | `window_mgr.s:2532`<br>`window_mgr.s:2374` | test if point is in this window's structure region point hit this window: ask WDEF which part |
| **`Fix2Frac`** | `0x015BD0` | `0x01020C` | `fixmath.s:962` | **Proto:** `Pascal: FUNCTION Fix2Frac(x: Fixed): Fract;`<br>_Fix2Frac ($A841): convert Fixed (16.16) to Fract (2.30) Pascal: FUNCTION Fix2Frac(x: Fixed): Fract; As Long2Fix, with a shift of 14 bits; pinned to $7FFFFFFF / $80000000 on overflow. LONG2FIX_SHIFT (... |
| **`FIX2FRAC`** | `0x015BD0` | `0x01020C` | `fixmath.s:724` | _Fix2Frac ($A841) - convert Fixed (16.16) to Fract (2.30) Left-shifts by 14 to convert 16.16 -> 2.30 format. Clamps on overflow. |
| **`Fix2Long`** | `0x015BAC` | `0x0101E8` | `fixmath.s:906` | **Proto:** `Pascal: FUNCTION Fix2Long(x: Fixed): LONGINT;`<br>**Regs:** `Entry: 4(SP) = x, 8(SP) = result slot (no frame; uses D0-D1/A0) Exit:  result = x rounded to an integer, halves away from zero`<br>_Fix2Long ($A840): convert Fixed (16.16) to LongInt Pascal: FUNCTION Fix2Long(x: Fixed): LONGINT; Entry: 4(SP) = x, 8(SP) = result slot (no frame; uses D0-D1/A0) Exit:  result = x rounded to an intege... |
| **`FIX2LONG`** | `0x015BAC` | `0x0101E8` | `fixmath.s:685` | _Fix2Long ($A840) - convert Fixed (16.16) to LongInt. Rounds the fractional part: 0.5 rounds away from zero. |
| **`FIX2LONG_NEG_RND`** | `0x015BC0` | `0x0101FC` | `fixmath.s:929`<br>`fixmath.s:702` | — |
| **`FIX2LONG_POS`** | `0x015BC4` | `0x010200` | `fixmath.s:937`<br>`fixmath.s:706` | FIX2LONG_POS - positive path: shift and round |
| **`FIX2LONG_SHIFT`** | `0x015BB2` | `0x0101EE` | `fixmath.s:921`<br>`fixmath.s:694` | — |
| **`Fix2X`** | `0x015B18` | `0x010154` | `fixmath.s:761` | **Proto:** `Pascal: FUNCTION Fix2X(x: Fixed): Extended;`<br>**Regs:** `Entry: 4(SP) = x, 8(SP) = address of the 10-byte extended result Exit:  extended stored at the result address; x removed, the result`<br>_Fix2X ($A843): convert Fixed (16.16) to 80-bit SANE extended Pascal: FUNCTION Fix2X(x: Fixed): Extended; Entry: 4(SP) = x, 8(SP) = address of the 10-byte extended result (no frame; uses D0-D1/A0-A1) ... |
| **`FIX2X`** | `0x015B18` | `0x010154` | `fixmath.s:575` | _Fix2X ($A843) - convert Fixed (16.16) to 80-bit SANE extended Input: Fixed value on stack, pointer to 10-byte extended on stack. Exponent bias for Fixed: 0x400E. |
| **`FIX2X_NORMALIZE`** | `0x015B2C` | `0x010168` | `fixmath.s:785`<br>`fixmath.s:593` | FIX2X_NORMALIZE - normalize the fixed/fract mantissa |
| **`FIX2X_SHIFT_LEFT`** | `0x015B36` | `0x010172` | `fixmath.s:790`<br>`fixmath.s:598` | — |
| **`FIX2X_STORE`** | `0x015B3C` | `0x010178` | `fixmath.s:794`<br>`fixmath.s:602` | — |
| **`FIX_TO_EXTENDED`** | `0x015B22` | `0x01015E` | `fixmath.s:774`<br>`fixmath.s:584` | — |
| **`FixATan2`** | `0x015A56` | `0x010096` | `fixmath.s:641` | **Proto:** `Pascal: FUNCTION FixATan2(x, y: LONGINT): Fixed;`<br>**Regs:** `Entry: after FIXPT_ENTRY, x = $0C(A6), y = $08(A6); result at $10(A6) Exit:  result = angle in radians (Fixed), -pi..pi; (0,0) gives 0;`<br>_FixATan2 ($A818): arctangent of y/x, i.e. the angle of the point (x,y) Pascal: FUNCTION FixATan2(x, y: LONGINT): Fixed; Entry: after FIXPT_ENTRY, x = $0C(A6), y = $08(A6); result at $10(A6) Exit:  re... |
| **`FIXATAN2`** | `0x015A56` | `0x010096` | `fixmath.s:480` | FixAtan2 ($A849) - 16.16 fixed-point arctangent of dy/dx. Stack: dvsr/dx(+$0C), dvnd/dy(+$08). Returns angle in Fixed degrees. D6 tracks sign/swap flags: bit 0 = dividend negative, bit 1 = divisor neg... |
| **`FixDiv`** | `0x0158B6` | `0x00FEF8` | `fixmath.s:289` | **Proto:** `Pascal: FUNCTION FixDiv(x, y: Fixed): Fixed;`<br>**Regs:** `Entry: after FIXPT_ENTRY, x = $0C(A6), y = $08(A6); result at $10(A6) Exit:  result = x/y * 2^16, rounded (Fixed / Fixed -> Fixed);`<br>_FixDiv ($A84D): divide, giving a Fixed (16.16) quotient Pascal: FUNCTION FixDiv(x, y: Fixed): Fixed; Entry: after FIXPT_ENTRY, x = $0C(A6), y = $08(A6); result at $10(A6) Exit:  result = x/y * 2^16, ... |
| **`FIXDIV`** | `0x0158B6` | `0x00FEF8` | `fixmath.s:226` | FIXDIV - FixDiv with reduced 18-bit precision. Fewer iterations for faster approximate quotient. |
| **`FIXDIV_CONT`** | `0x0158BA` | `0x00FEFC` | `fixmath.s:292`<br>`fixmath.s:229` | — |
| **`FIXDIV_CONT_2`** | `0x0158D4` | `0x00FF16` | `fixmath.s:317`<br>`fixmath.s:250` | — |
| **`FIXDIV_CONT_3`** | `0x0158EC` | `0x00FF34` | `fixmath.s:337`<br>`fixmath.s:270` | — |
| **`FIXDIV_CONT_4`** | `0x0158F0` | `0x00FF38` | `fixmath.s:340`<br>`fixmath.s:273` | — |
| **`FIXDIV_EMPTY`** | `0x0158C8` | `0x00FF0A` | `fixmath.s:305`<br>`fixmath.s:241` | — |
| **`FIXDIV_LOOP`** | `0x0158E2` | `0x00FF2A` | `fixmath.s:330`<br>`fixmath.s:263` | FIXDIV_LOOP - shift-and-subtract binary division of D2 by D1: one quotient bit into D0 per step (D3+1 steps, entered at the compare); a carry out of D2 forces the subtract. The last bit is the round b... |
| **`FIXDIV_LOOP_2`** | `0x0158E8` | `0x00FF30` | `fixmath.s:334`<br>`fixmath.s:267` | — |
| **`FIXDIV_NO`** | `0x0158C4` | `0x00FF06` | `fixmath.s:302`<br>`fixmath.s:238` | FIXDIV_NO - Normalize divisor: shift left until MSB is set. |
| **`FIXDIV_NO_2`** | `0x0158D0` | `0x00FF12` | `fixmath.s:314`<br>`fixmath.s:247` | FIXDIV_NO_2 - Normalize dividend: shift left until MSB is set. |
| **`FixMul`** | `0x0157E6` | `0x00FE28` | `fixmath.s:95` | **Proto:** `Pascal: FUNCTION FixMul(a, b: Fixed): Fixed;`<br>**Regs:** `Entry: after FIXPT_ENTRY, a = $0C(A6), b = $08(A6); result at $10(A6) Exit:  result = a*b / 2^16, rounded; $7FFFFFFF / $80000000 on overflow;`<br>_FixMul ($A868): multiply two Fixed (16.16) values Pascal: FUNCTION FixMul(a, b: Fixed): Fixed; Entry: after FIXPT_ENTRY, a = $0C(A6), b = $08(A6); result at $10(A6) Exit:  result = a*b / 2^16, rounde... |
| **`FIXMUL`** | `0x0157E6` | `0x00FE28` | `fixmath.s:71` | FixMul ($A868) - 16.16 fixed-point multiply. Computes (D1*D2) >> 16 as Fixed result. D5=0 selects multiply. |
| **`FIXMUL_CONT`** | `0x0157EC` | `0x00FE2E` | `fixmath.s:98`<br>`fixmath.s:74` | — |
| **`FIXMUL_CONT_2`** | `0x0157F0` | `0x00FE32` | `fixmath.s:100`<br>`fixmath.s:76` | — |
| **`FIXMUL_CONT_3`** | `0x015832` | `0x00FE74` | `fixmath.s:151`<br>`fixmath.s:122` | FIXMUL_CONT_3 -- D0:D4 = unsigned 64-bit product; select the result by D5 |
| **`FIXMUL_CONT_4`** | `0x015842` | `0x00FE84` | `fixmath.s:165`<br>`fixmath.s:135` | FIXMUL_CONT_4 - FixMul: extract middle 32 bits from 64-bit product. D0:D4 holds the 64-bit unsigned product; we need bits 16-47. |
| **`FIXMUL_CONT_5`** | `0x01584C` | `0x00FE8E` | `fixmath.s:172`<br>`fixmath.s:141` | FIXMUL_CONT_5 -- round: D4 bit 31 is the first bit below the result |
| **`FIXMUL_CONT_6`** | — | `0x00FEC2` | `fixmath.s:177` | FIXMUL_CONT_6 - Common prologue for fixed-point math routines. Creates LINK frame and saves registers. Pops own return addr and jumps back (acts as macro). Called by: LONGMUL, FRACMUL, FIXMUL, FRACDIV... |
| **`FIXMUL_CONT_7`** | `0x01588C` | `0x00FECE` | `fixmath.s:227`<br>`fixmath.s:186` | FIXMUL_CONT_7 - load the two parameters: D1 = $08(A6) (2nd parameter), D2 = $0C(A6) (1st), then fall into FIXMUL_CONT_8: D1/D2 := magnitudes, D6.B = $FF if exactly one was negative (sign of the result... |
| **`FIXMUL_CONT_8`** | `0x015892` | `0x00FED4` | `fixmath.s:231`<br>`fixmath.s:189` | FIXMUL_CONT_8 -- D1/D2 := magnitudes, D6.B := sign of the result (also entered directly by LongMul and FixRatio with their own D1/D2) |
| **`FIXMUL_EXIT`** | `0x015854` | `0x00FE96` | `fixmath.s:178`<br>`fixmath.s:146` | FIXMUL_EXIT (Apple: reSign) -- apply sign D6.B to magnitude D0, pin overflow |
| **`FIXMUL_EXIT_2`** | `0x01585E` | `0x00FEA0` | `fixmath.s:185`<br>`fixmath.s:153` | FIXMUL_EXIT_2 (Apple: TwoParmExit) -- return D0 from a two-parameter function |
| **`FIXMUL_EXIT_3`** | `0x01586A` | `0x00FEAC` | `fixmath.s:197`<br>`fixmath.s:162` | FIXMUL_EXIT_3 - common exit for functions with 4 bytes of parameters (FracSqrt, FixRatio, FracCos, FracSin): long result D0 -> $0C(A6). FIXMUL_EXIT_4: restore D0-D6/A1, UNLK, pop the return address, r... |
| **`FIXMUL_EXIT_4`** | `0x015874` | `0x00FEB6` | `fixmath.s:200`<br>`fixmath.s:165` | — |
| **`FIXMUL_EXIT_5`** | — | `0x00FEE6` | `fixmath.s:207` | FIXMUL_EXIT_5 - Overflow handler: return max or min Fixed value. If D6 (sign) is set, returns $80000001 (most negative). If D6 is clear, returns $7FFFFFFF (most positive). Called by: FIXDIV_CONT_2, FI... |
| **`FIXMUL_NO`** | `0x0157FC` | `0x00FE3E` | `fixmath.s:113`<br>`fixmath.s:87` | FIXMUL_NO - Is the other operand exactly $00010000? Then the 64-bit product is just D1 << 16 (FIXMUL_NO_2), valid for all three modes; otherwise do the full multiply (ALGORITHM). |
| **`FIXMUL_NO_2`** | `0x015800` | `0x00FE42` | `fixmath.s:116`<br>`fixmath.s:90` | — |
| **`FIXMUL_SAME_SIGN_RTS`** | — | `0x00FFB0` | `fixmath.s:341` | — |
| **`FIXMUL_SKIP`** | `0x01589A` | `0x00FEDC` | `fixmath.s:236`<br>`fixmath.s:194` | — |
| **`FIXMUL_SKIP_2`** | `0x0158A2` | `0x00FEE4` | `fixmath.s:241`<br>`fixmath.s:199` | — |
| **`FIXPT_ENTRY`** | `0x015880` | — | `fixmath.s:215` | FIXPT_ENTRY - common entry of the fixed-point routines: pops its own return address into A0, LINK A6,#0, saves D0-D6/A1 and jumps back. The parameters then start at $08(A6), the caller's return addres... |
| **`FIXPT_OVERFLOW`** | `0x0158A4` | — | `fixmath.s:249` | FIXPT_OVERFLOW - overflow: return $80000000 if D6.B <> 0 (negative result), else $7FFFFFFF, through the two-parameter exit FIXMUL_EXIT_2. Apple source name: fixOver (System 7.1 Toolbox/Munger/Munger.a... |
| **`FixRatio`** | `0x01593A` | `0x00FF82` | `fixmath.s:399` | **Proto:** `Pascal: FUNCTION FixRatio(numer, denom: INTEGER): Fixed;`<br>**Regs:** `Entry: after FIXPT_ENTRY, denom = $08(A6).W, numer = $0A(A6).W; Exit:  result = numer/denom, truncated toward zero; numer = denom`<br>_FixRatio ($A869): ratio of two integers as a Fixed value Pascal: FUNCTION FixRatio(numer, denom: INTEGER): Fixed; Entry: after FIXPT_ENTRY, denom = $08(A6).W, numer = $0A(A6).W; result at $0C(A6) Exi... |
| **`FIXRATIO`** | `0x01593A` | `0x00FF82` | `fixmath.s:315` | _FixRatio ($A869) - Compute ratio of two integers as Fixed. Stack: numer(+$08 word), denom(+$0A word). Returns 16.16 Fixed = numer/denom. Equal inputs = 1.0. |
| **`FIXRATIO_CONT`** | `0x015968` | — | `fixmath.s:426` | — |
| **`FIXRATIO_EMPTY`** | `0x015956` | `0x00FF9E` | `fixmath.s:415`<br>`fixmath.s:330` | FIXRATIO_EMPTY - Standard Fixed ratio: integer part via DIVS, fractional part via DIVU on remainder. |
| **`FIXRATIO_EXIT`** | `0x015962` | `0x00FFAA` | `fixmath.s:422`<br>`fixmath.s:337` | — |
| **`FIXRATIO_EXIT_2`** | `0x01596C` | `0x00FFB4` | `fixmath.s:432`<br>`fixmath.s:344` | FIXRATIO_EXIT_2 - numer == denom: return Fixed 1.0 ($00010000). |
| **`FixRound`** | `0x015986` | `0x00FFCE` | `fixmath.s:475` | **Proto:** `Pascal: FUNCTION FixRound(x: Fixed): INTEGER;`<br>**Regs:** `Entry: 4(SP) = x, 8(SP) = INTEGER result slot (no frame; uses D0-D1) Exit:  x >= 0: result = high word of x + 1/2 ($00008000), i.e. rounded`<br>_FixRound ($A86C): round a Fixed value to an integer Pascal: FUNCTION FixRound(x: Fixed): INTEGER; Entry: 4(SP) = x, 8(SP) = INTEGER result slot (no frame; uses D0-D1) Exit:  x >= 0: result = high wor... |
| **`FIXROUND`** | `0x015986` | `0x00FFCE` | `fixmath.s:367` | _FixRound ($A86C) - Round Fixed to nearest integer. Stack: value(+$04 Fixed). Returns word in result position. |
| **`FIXROUND_CONT`** | `0x015992` | `0x00FFDA` | `fixmath.s:481`<br>`fixmath.s:374` | — |
| **`FIXROUND_CONT_2`** | `0x01599A` | — | `fixmath.s:486` | — |
| **`FIXROUND_NO`** | `0x01599E` | — | `fixmath.s:489` | — |
| **`FIXROUND_SATURATE_TAIL`** | — | `0x00FFE2` | `fixmath.s:379` | — |
| **`FlashMenuBar`** | `0x0127D8` | `0x00CDCE` | `menu_mgr.s:971` | _FlashMenuBar ($A94C) |
| **`FLASHMENUBAR`** | `0x0127D8` | `0x00CDCE` | `menu_mgr.s:706` | **Proto:** `Pascal: procedure FlashMenuBar(menuID: INTEGER);`<br>_FlashMenuBar ($A94C): briefly invert a menu title (or whole bar). Pascal: procedure FlashMenuBar(menuID: INTEGER); menuID = 0 toggles the apple/MBar background; nonzero toggles a single title. Implem... |
| **`FLASHMENUBAR_APPLE`** | — | `0x00CE0A` | `menu_mgr.s:732` | Apple-menu flash path: toggle MBFlash bit, hilite/unhilite the title region. |
| **`FLASHMENUBAR_EMPTY`** | `0x01280E` | — | `menu_mgr.s:997` | FLASHMENUBAR_EMPTY - flash entire menu bar (invert rounded rect) |
| **`FLASHMENUBAR_EXIT`** | `0x012800` | — | `menu_mgr.s:986` | — |
| **`FLASHMENUBAR_UNHILITE`** | — | `0x00CE18` | `menu_mgr.s:738` | — |
| **`FMBuildFont`** | — | `0x019832` | `font_mgr.s:872` | — |
| **`FMGREND`** | — | `0x019FFE` | `package_mgr.s:20` | **Proto:** `Pascal: procedure InitPack(packID: INTEGER);`<br>Package Manager -- _InitPack, _InitAllPacks, _Pack0 ... _Pack15 Apple source: PackageMgr.a (MacSEROM.lst module PACKDISPATCHER). InitPack loads one PACK resource and stores its handle in AppPacks (pac... |
| **`FMLoadByID`** | — | `0x019AFE` | `font_mgr.s:1173` | — |
| **`FMLoadByID_AfterGet`** | — | `0x019B16` | `font_mgr.s:1184` | — |
| **`FMLoadByID_AllMaps`** | — | `0x019B00` | `font_mgr.s:1175` | — |
| **`FMLoadByID_AltMap`** | — | `0x019AD8` | `font_mgr.s:1158` | — |
| **`FMLoadByID_DoGet`** | — | `0x019B06` | `font_mgr.s:1177` | — |
| **`FMLoadByID_RTS`** | — | `0x019B2A` | `font_mgr.s:1191` | — |
| **`FMLoadFont_Force`** | — | `0x01933E` | `font_mgr.s:304` | — |
| **`FMLoadFont_Maybe`** | — | `0x01933A` | `font_mgr.s:301` | FMLoadFont_Maybe / FMLoadFont_Force -- de-reference a font resource handle, loading it from disk if purged. A0 -> handle. Returns A0 = master pointer (handle dereferenced). FMLoadFont_Maybe: short-cir... |
| **`FMResolveFamily`** | — | `0x019D38` | `font_mgr.s:1468` | FMResolveFamily: look up FOND for D1 with system/app substitution. D1 = 0 -> SysFontFam, D1 = 1 -> ApFontID, otherwise use D1 as-is. |
| **`FMResolveFamily_NotSys`** | — | `0x019D42` | `font_mgr.s:1473` | — |
| **`FMSCALE_AFTER_STORE`** | — | `0x0199D0` | `font_mgr.s:1033` | — |
| **`FMSCALE_STORE_NUMER`** | — | `0x0199C2` | `font_mgr.s:1026` | — |
| **`FMSCALE_STORE_VFACT`** | — | `0x0199CC` | `font_mgr.s:1031` | — |
| **`FMSEARCH_AFTER_TRY`** | — | `0x0198BE` | `font_mgr.s:920` | — |
| **`FMSEARCH_FOND_LOADED`** | — | `0x01988A` | `font_mgr.s:903` | — |
| **`FMSEARCH_GOT_ALTID`** | — | `0x019AD2` | `font_mgr.s:1155` | — |
| **`FMSEARCH_NORMALIZE_SIZE`** | — | `0x0198C4` | `font_mgr.s:924` | — |
| **`FMSearchFOND_BySize`** | — | `0x019B2E` | `font_mgr.s:1194` | — |
| **`FMSearchFOND_NotFound`** | — | `0x019B42` | `font_mgr.s:1204` | — |
| **`FMSEARCHSIZE_AFTER_LOOKUP`** | — | `0x019B6A` | `font_mgr.s:1225` | — |
| **`FMSEARCHSIZE_ENTRY`** | — | `0x019B46` | `font_mgr.s:1207` | — |
| **`FMSEARCHSIZE_FOUND`** | — | `0x019BA0` | `font_mgr.s:1257` | — |
| **`FMSEARCHSIZE_RETRY`** | — | `0x019BB4` | `font_mgr.s:1268` | Called by: FMSEARCHSIZE_ENTRY, SWAPFONT_OK_17, FMSTYLE_LOAD_BEST |
| **`FMSTYLE_BIT_LOOP`** | — | `0x019BE4` | `font_mgr.s:1306` | — |
| **`FMSTYLE_BIT_NEXT`** | — | `0x019BEC` | `font_mgr.s:1310` | — |
| **`FMSTYLE_DONE`** | — | `0x019C88` | `font_mgr.s:1382` | — |
| **`FMSTYLE_KEEP_BEST`** | — | `0x019BF0` | `font_mgr.s:1312` | — |
| **`FMSTYLE_LOAD_BEST`** | — | `0x019C00` | `font_mgr.s:1321` | — |
| **`FMSTYLE_LOADED`** | — | `0x019C1E` | `font_mgr.s:1334` | — |
| **`FMSTYLE_NOT_EXACT`** | — | `0x019BD4` | `font_mgr.s:1297` | — |
| **`FMSTYLE_SAVE_BEST`** | — | `0x019C80` | `font_mgr.s:1378` | — |
| **`FMSTYLE_SCAN_INIT`** | — | `0x019BC0` | `font_mgr.s:1286` | FMSTYLE_SCAN_INIT - called from 1 place |
| **`FMSTYLE_SCAN_LOOP`** | — | `0x019BCA` | `font_mgr.s:1291` | — |
| **`FMSTYLE_SCAN_NEXT`** | — | `0x019C48` | `font_mgr.s:1351` | — |
| **`FMSTYLE_SCORE_ADV`** | — | `0x019C74` | `font_mgr.s:1372` | — |
| **`FMSTYLE_SCORE_LOOP`** | — | `0x019C60` | `font_mgr.s:1362` | — |
| **`FMSTYLE_SCORE_NEXT`** | — | `0x019C68` | `font_mgr.s:1366` | — |
| **`FMSTYLE_WEIGHT_TBL`** | — | `0x019C8C` | `font_mgr.s:1395` | FMSTYLE_WEIGHT_TBL: per-style match weight table (2nd copy, used at FMSTYLE_SCORE_LOOP). Same purpose as SWAPFONT_CONT_44 but with different weights: bit 0 (bold)        weight 4 bit 1 (italic)      w... |
| **`FMSwapFont`** | `0x00E6C0` | `0x01924E` | `font_mgr.s:113` | _FMSwapFont ($A901) _FMSwapFont ($A901): swap in a new font - most frequently called FM trap A0 = ptr to FMInput record (family, size, face, needBits, device, numer, denom) Returns: ptr to FMOutput re... |
| **`FMSWAPFONT`** | `0x00E6C0` | `0x01924E` | `font_mgr.s:188` | _FMSwapFont (FMSWAPFONT) -- swap to a different font The Font Manager's main entry point. Called from QuickDraw StdText / TextWidth, the Toolbox SetFont, and from InitFonts at boot. Stack on entry: +4... |
| **`FMSWAPFONT_ABORT`** | — | `0x019358` | `font_mgr.s:315` | — |
| **`FMSWAPFONT_AFTER_CONTROL`** | — | `0x0197DE` | `font_mgr.s:843` | — |
| **`FMSWAPFONT_BAIL_DROP2`** | — | `0x0199FE` | `font_mgr.s:1055` | — |
| **`FMSWAPFONT_BAIL_DROP4`** | — | `0x0199FC` | `font_mgr.s:1053` | — |
| **`FMSWAPFONT_BLOCK_CMP`** | — | `0x019A40` | `font_mgr.s:1086` | — |
| **`FMSWAPFONT_BODY`** | — | `0x01935C` | `font_mgr.s:329` | FMSWAPFONT_BODY -- FMSwapFont slow path: full rebuild Reached when FMSwapFont's quick check decided the cached state doesn't match. Allocates 74 bytes of locals, copies caller's input record (16 bytes... |
| **`FMSWAPFONT_BUILD_FROM_SCRATCH`** | — | `0x0193C4` | `font_mgr.s:368` | — |
| **`FMSWAPFONT_BUILD_WIDTH`** | — | `0x01961E` | `font_mgr.s:646` | — |
| **`FMSWAPFONT_CACHE_CMP`** | — | `0x0193F8` | `font_mgr.s:395` | — |
| **`FMSWAPFONT_CACHE_LOOP`** | — | `0x0193D8` | `font_mgr.s:380` | — |
| **`FMSWAPFONT_CACHE_LRU`** | — | `0x019486` | `font_mgr.s:452` | — |
| **`FMSWAPFONT_CACHE_MISS`** | — | `0x019446` | `font_mgr.s:428` | FMSWAPFONT_CACHE_MISS -- cache miss: try to allocate or recycle a slot. |
| **`FMSWAPFONT_CACHE_PURGED`** | — | `0x019438` | `font_mgr.s:419` | — |
| **`FMSWAPFONT_DEVICE_OK`** | — | `0x01938A` | `font_mgr.s:344` | — |
| **`FMSWAPFONT_EXTRA_INIT`** | — | `0x019572` | `font_mgr.s:579` | — |
| **`FMSWAPFONT_FALLBACK`** | — | `0x0192F0` | `font_mgr.s:247` | Common reload path: jump to full FMSwapFont implementation. Called by: FMSWAPFONT_FAST_CMP2, FMSWAPFONT, FMSWAPFONT_TRY_FAST, FMSWAPFONT_FAST_CMP1, SWAPFONT_EXIT |
| **`FMSWAPFONT_FAST_CMP1`** | — | `0x0192A4` | `font_mgr.s:216` | — |
| **`FMSWAPFONT_FAST_CMP2`** | — | `0x0192B8` | `font_mgr.s:225` | — |
| **`FMSWAPFONT_FILL16_LOOP`** | — | `0x0196CE` | `font_mgr.s:722` | — |
| **`FMSWAPFONT_FILL16_STORE`** | — | `0x0196E2` | `font_mgr.s:733` | — |
| **`FMSWAPFONT_FILL8_LOOP`** | — | `0x019744` | `font_mgr.s:781` | — |
| **`FMSWAPFONT_FILL8_STORE`** | — | `0x019758` | `font_mgr.s:792` | — |
| **`FMSWAPFONT_FILL_DBF`** | — | `0x019768` | `font_mgr.s:801` | — |
| **`FMSWAPFONT_FILL_DEFAULT`** | — | `0x019766` | `font_mgr.s:799` | — |
| **`FMSWAPFONT_FILL_TAIL`** | — | `0x01975E` | `font_mgr.s:795` | — |
| **`FMSWAPFONT_FINISH`** | — | `0x019A22` | `font_mgr.s:1071` | — |
| **`FMSWAPFONT_FORCE_SYSMAP`** | — | `0x019A8A` | `font_mgr.s:1120` | — |
| **`FMSWAPFONT_INVALIDATE_ALL`** | — | `0x0193C0` | `font_mgr.s:366` | — |
| **`FMSWAPFONT_LRU_DEC`** | — | `0x0194AA` | `font_mgr.s:473` | — |
| **`FMSWAPFONT_LRU_ENTER`** | — | `0x0194A4` | `font_mgr.s:468` | — |
| **`FMSWAPFONT_LRU_SHIFT`** | — | `0x0194A6` | `font_mgr.s:471` | LRU shuffle: move slot[i] -> slot[i+1] from D5 down to slot 0. |
| **`FMSWAPFONT_NEXT_STAGE`** | — | `0x019A16` | `font_mgr.s:1067` | — |
| **`FMSWAPFONT_NO_PORT`** | — | `0x019788` | `font_mgr.s:814` | — |
| **`FMSWAPFONT_NORM_CURFAM`** | — | `0x019A4C` | `font_mgr.s:1092` | — |
| **`FMSWAPFONT_NORMALIZE`** | — | `0x019368` | `font_mgr.s:333` | — |
| **`FMSWAPFONT_PUBLISH_EXTRA`** | — | `0x01976C` | `font_mgr.s:803` | — |
| **`FMSWAPFONT_REFRESH_PRIMARY`** | — | `0x0194C2` | `font_mgr.s:486` | FMSWAPFONT_REFRESH_PRIMARY -- refresh primary widthTab from FOutFontHandle. Called by: FMSWAPFONT_CACHE_MISS, FMSWAPFONT_BUILD_FROM_SCRATCH, FMSWAPFONT_CACHE_LRU, SWAPFONT_CONT_16 |
| **`FMSWAPFONT_RETRY_DEC`** | — | `0x0192F2` | `font_mgr.s:249` | — |
| **`FMSWAPFONT_RETRY_OK`** | — | `0x0193A0` | `font_mgr.s:352` | — |
| **`FMSWAPFONT_RETRY_TAIL`** | — | `0x019A00` | `font_mgr.s:1058` | Called by: FMSWAPFONT_ABORT, FMSEARCH_NORMALIZE_SIZE, SWAPFONT_NEXT_3, SWAPFONT_CONT_38, SWAPFONT_NO_22 (and 2 more) |
| **`FMSWAPFONT_RETRY_TBL`** | — | `0x019A32` | `font_mgr.s:1080` | FMSWAPFONT_RETRY_TBL: PC-relative dispatch table for FMSwapFont retry stages. Stages indexed by (FontFlag) value: each 2-byte entry holds the relative offset to the corresponding ENTRY_19A3* handler. |
| **`FMSWAPFONT_SAME_BLOCK`** | — | `0x019A58` | `font_mgr.s:1098` | — |
| **`FMSWAPFONT_SCALE`** | — | `0x01972A` | `font_mgr.s:769` | — |
| **`FMSWAPFONT_SCALE_RTS`** | — | `0x019742` | `font_mgr.s:779` | — |
| **`FMSWAPFONT_STYLE_ADD`** | — | `0x0195EA` | `font_mgr.s:621` | — |
| **`FMSWAPFONT_STYLE_INIT`** | — | `0x0195D6` | `font_mgr.s:611` | — |
| **`FMSWAPFONT_STYLE_LOOP`** | — | `0x0195D8` | `font_mgr.s:613` | — |
| **`FMSWAPFONT_STYLE_NEXT`** | — | `0x0195EE` | `font_mgr.s:624` | — |
| **`FMSWAPFONT_SYSMAP_ENTRY`** | — | `0x019A78` | `font_mgr.s:1114` | — |
| **`FMSWAPFONT_TEAR_DOWN`** | — | `0x01981E` | `font_mgr.s:864` | — |
| **`FMSWAPFONT_TRY_APFONT`** | — | `0x019A3C` | `font_mgr.s:1084` | — |
| **`FMSWAPFONT_TRY_FAST`** | — | `0x01927C` | `font_mgr.s:201` | — |
| **`FMSWAPFONT_TRY_FRACTIONAL`** | — | `0x0196EE` | `font_mgr.s:738` | — |
| **`FMSWAPFONT_TRY_SYSFONT`** | — | `0x019A72` | `font_mgr.s:1111` | — |
| **`FMSWAPFONT_UNLINK`** | — | `0x01982C` | `font_mgr.s:869` | — |
| **`FMSWAPFONT_USE_FOND_WIDTHS`** | — | `0x0195AC` | `font_mgr.s:596` | — |
| **`FMSWAPFONT_USE_GENEVA`** | — | `0x019A6E` | `font_mgr.s:1108` | — |
| **`FONTMANAGER`** | — | `0x019150` | `font_mgr.s:28` | Font Manager Apple source: FontMgr.a (MacSEROM.lst module FONTMANAGER): InitFonts, FMSwapFont (with FPOINTONE), GetFName ($A8FF), RealFont ($A902), GetFNum ($A900), SetFontLock ($A903), SetFScaleDisab... |
| **`FontMetrics`** | `0x00F274` | `0x019E4A` | `font_mgr.s:1792` | **Proto:** `Pascal: PROCEDURE FontMetrics(VAR theMetrics: FMetricRec);`<br>_FontMetrics ($A835): return fractional metrics of the current font Pascal: PROCEDURE FontMetrics(VAR theMetrics: FMetricRec); FMetricRec: ascent, descent, leading, widMax: Fixed; wTabHandle: Handle C... |
| **`FONTMETRICS`** | `0x00F274` | `0x019E4A` | `font_mgr.s:1609` | **Proto:** `Pascal: procedure FontMetrics(VAR theMetrics: FMetricRec);`<br>_FontMetrics ($A835): return detailed font metrics for current font Pascal: procedure FontMetrics(VAR theMetrics: FMetricRec); |
| **`FONTMETRICS_NO`** | `0x00F2BC` | — | `font_mgr.s:1821` | scale the font record's metrics into theMetrics scale 3 metric values (ascent, descent, leading) scale widMax adjust metrics for shadow style |
| **`FONTMETRICS_NO_SHADOW`** | — | `0x019E92` | `font_mgr.s:1635` | — |
| **`FONTMETRICS_OK`** | `0x00F2E6` | `0x019EB8` | `font_mgr.s:1851`<br>`font_mgr.s:1656` | — |
| **`FPOINTONE`** | — | `0x019C94` | `font_mgr.s:1400` | FPOINTONE: 16.16 fixed-point constant 1.0 (0x00010000). |
| **`FPWIN_FOUND`** | `0x0111E4` | `0x00B82C` | `window_mgr.s:98`<br>`window_mgr.s:111` | — |
| **`FPWIN_LOOP`** | `0x0111D6` | `0x00B81E` | `window_mgr.s:91`<br>`window_mgr.s:104` | — |
| **`Frac2Fix`** | `0x015BB0` | `0x0101EC` | `fixmath.s:919` | **Proto:** `Pascal: FUNCTION Frac2Fix(x: Fract): Fixed;`<br>_Frac2Fix ($A842): convert Fract (2.30) to Fixed (16.16) Pascal: FUNCTION Frac2Fix(x: Fract): Fixed; As Fix2Long, with a shift of D1 = 14 bits (rounded, halves away from 0). The rounding increment is ... |
| **`FRAC2FIX`** | `0x015BB0` | `0x0101EC` | `fixmath.s:692` | _Frac2Fix ($A842) - convert Fract (2.30) to Fixed (16.16) Right-shifts by 14 bits to convert 2.30 -> 16.16 format. |
| **`Frac2X`** | `0x015B1E` | `0x01015A` | `fixmath.s:772` | **Proto:** `Pascal: FUNCTION Frac2X(x: Fract): Extended;`<br>_Frac2X ($A845): convert Fract (2.30) to 80-bit SANE extended Pascal: FUNCTION Frac2X(x: Fract): Extended; As Fix2X, with D1 = $4000 = biased exponent of bit 31 of a Fract (2^1). FIX_TO_EXTENDED (Appl... |
| **`FRAC2X`** | `0x015B1E` | `0x01015A` | `fixmath.s:582` | _Frac2X ($A845) - convert Fract (2.30) to 80-bit SANE extended. Exponent bias for Fract: 0x4000. |
| **`FracCos`** | `0x0159A6` | `0x00FFE8` | `fixmath.s:506` | **Proto:** `Pascal: FUNCTION FracCos(x: Fixed): Fract;`<br>**Regs:** `Entry: after FIXPT_ENTRY, x = $08(A6) (Fixed, radians); result at Exit:  result = cos(x) as a Fract (2.30); all registers except A0`<br>_FracCos ($A847): cosine of an angle in radians Pascal: FUNCTION FracCos(x: Fixed): Fract; Entry: after FIXPT_ENTRY, x = $08(A6) (Fixed, radians); result at $0C(A6) Exit:  result = cos(x) as a Fract (... |
| **`FRACCOS`** | `0x0159A6` | `0x00FFE8` | `fixmath.s:387` | FracCos ($A847) - 16.16 fixed-point cosine (Plus's SetDeskCPat). D6=2 selects cosine mode (cos via tangent identity). |
| **`FracDiv`** | `0x0158B0` | `0x00FEF2` | `fixmath.s:268` | **Proto:** `Pascal: FUNCTION FracDiv(x, y: Fract): Fract;`<br>**Regs:** `Entry: after FIXPT_ENTRY, x = $0C(A6), y = $08(A6); result at $10(A6) Exit:  result = x/y * 2^30, rounded (Fract / Fract -> Fract);`<br>_FracDiv ($A84B): divide, giving a Fract (2.30) quotient Pascal: FUNCTION FracDiv(x, y: Fract): Fract; Entry: after FIXPT_ENTRY, x = $0C(A6), y = $08(A6); result at $10(A6) Exit:  result = x/y * 2^30,... |
| **`FRACDIV`** | `0x0158B0` | `0x00FEF2` | `fixmath.s:218` | FRACDIV - FixDiv non-restoring division (full precision). D3=31 iterations for 32-bit quotient precision. |
| **`FracMul`** | `0x0157DE` | `0x00FE20` | `fixmath.s:77` | **Proto:** `Pascal: FUNCTION FracMul(x, y: Fract): Fract;`<br>**Regs:** `Entry: after FIXPT_ENTRY, x = $0C(A6), y = $08(A6); result at $10(A6) Exit:  result = x*y / 2^30, rounded; $7FFFFFFF / $80000000 on overflow;`<br>_FracMul ($A84A): multiply two Fract (2.30) values Pascal: FUNCTION FracMul(x, y: Fract): Fract; Entry: after FIXPT_ENTRY, x = $0C(A6), y = $08(A6); result at $10(A6) Exit:  result = x*y / 2^30, round... |
| **`FRACMUL`** | `0x0157DE` | `0x00FE20` | `fixmath.s:63` | RestoreEntries / FRACMUL ($A84D) - 16.16 fixed-point divide. Computes (D1/D2) as Fixed result. D5=-1 selects divide path. Called by: FRACSIN_POLY_TERM, ATAN_POLY_LOOP, FRACSIN_REDUCED, ATAN_DO_FRACDIV |
| **`FracSin`** | `0x0159AE` | `0x00FFF0` | `fixmath.s:532` | **Proto:** `Pascal: FUNCTION FracSin(x: Fixed): Fract;`<br>**Regs:** `Entry: after FIXPT_ENTRY, x = $08(A6) (Fixed, radians); result at Exit:  result = sin(x) as a Fract (2.30); all registers except A0`<br>_FracSin ($A848): sine of an angle in radians Pascal: FUNCTION FracSin(x: Fixed): Fract; Entry: after FIXPT_ENTRY, x = $08(A6) (Fixed, radians); result at $0C(A6) Exit:  result = sin(x) as a Fract (2.... |
| **`FRACSIN`** | `0x0159AE` | `0x00FFF0` | `fixmath.s:395` | FracSin ($A848) - 16.16 fixed-point sine (Plus's LOC_C72E). D6=0 selects sine mode. |
| **`FRACSIN_CONT`** | `0x0159B4` | `0x00FFF6` | `fixmath.s:535`<br>`fixmath.s:398` | — |
| **`FRACSIN_CONT_2`** | `0x0159C0` | `0x010002` | `fixmath.s:541`<br>`fixmath.s:404` | — |
| **`FRACSIN_CS0`** | `0x015A46` | `0x010086` | `fixmath.s:619`<br>`fixmath.s:467` | FRACSIN_CS0 - cosine polynomial coefficients (Fract): cs0 = $40000000 (1.0), cs1 = $800011A7 (-2.00000), cs2 = $2AA7F29A (0.66650), cs3 = $FA6E2A42 (-0.08703); Apple source names: cs0..cs3 |
| **`FRACSIN_NO`** | `0x0159C2` | `0x010004` | `fixmath.s:543`<br>`fixmath.s:406` | — |
| **`FRACSIN_NOTSINE`** | `0x015A28` | `0x010068` | `fixmath.s:596`<br>`fixmath.s:448` | — |
| **`FRACSIN_POLY`** | `0x015A06` | `0x010046` | `fixmath.s:582`<br>`fixmath.s:434` | — |
| **`FRACSIN_POLY_LOOP`** | `0x015A0A` | — | `fixmath.s:584` | — |
| **`FRACSIN_POLY_TERM`** | — | `0x01004A` | `fixmath.s:436` | — |
| **`FRACSIN_POLYCOS`** | `0x015A00` | `0x010040` | `fixmath.s:579`<br>`fixmath.s:431` | FRACSIN_POLYCOS - FracSin/FracCos: select the cosine polynomial (the label name is a misnomer). FRACSIN_POLY: Horner evaluation in t2 (D5), starting with the last coefficient; each FracMul result repl... |
| **`FRACSIN_REDUCED`** | `0x0159DA` | `0x01001C` | `fixmath.s:554`<br>`fixmath.s:416` | FRACSIN_REDUCED -- D3.W = reduced angle r (0..pi/4, Fixed fraction) |
| **`FRACSIN_SIGN`** | `0x015A36` | — | `fixmath.s:603` | — |
| **`FRACSIN_SIGN_RTS`** | — | `0x010076` | `fixmath.s:455` | — |
| **`FRACSIN_SN0`** | `0x015A3A` | `0x01007A` | `fixmath.s:612`<br>`fixmath.s:461` | FRACSIN_SN0 - sine polynomial coefficients (Fract): sn0 = $7FFFD609 (1.99999), sn1 = $AAB3314D (-1.33281), sn2 = $10A208E5 (0.25989) Apple source names: sn0..sn2 (System 7.1 Toolbox/Munger/Munger.a) |
| **`FracSqrt`** | `0x015900` | `0x00FF48` | `fixmath.s:360` | **Proto:** `Pascal: FUNCTION FracSqrt(x: Fract): Fract;`<br>**Regs:** `Entry: after FIXPT_ENTRY, x = $08(A6); result at $0C(A6) Exit:  result = sqrt(x), rounded; x and the result are taken as`<br>_FracSqrt ($A849): square root of a Fract (2.30) Pascal: FUNCTION FracSqrt(x: Fract): Fract; Entry: after FIXPT_ENTRY, x = $08(A6); result at $0C(A6) Exit:  result = sqrt(x), rounded; x and the result... |
| **`FRACSQRT`** | `0x015900` | `0x00FF48` | `fixmath.s:284` | FRACSQRT - FracSqrt: 16.16 fixed-point square root. Non-restoring algorithm. Input at 0x8(A6). Returns 16.16 Fixed via FIXMUL_EXIT_3. |
| **`FRACSQRT_LOOP`** | `0x015912` | `0x00FF5A` | `fixmath.s:368`<br>`fixmath.s:292` | — |
| **`FRACSQRT_NO`** | `0x01591C` | `0x00FF64` | `fixmath.s:374`<br>`fixmath.s:298` | — |
| **`FreeAlert`** | `0x014DC2` | `0x00F3EC` | `dialog_mgr.s:797` | **Proto:** `FreeAlert -- _FreeAlert ($A98A): PROCEDURE FreeAlert (a l ertID : I NTEGER );`<br>FreeAlert -- _FreeAlert ($A98A): PROCEDURE FreeAlert (a l ertID : I NTEGER ); _FreeAlert ($A98A) |
| **`FREEALERT`** | `0x014DC2` | `0x00F3EC` | `dialog_mgr.s:788` | _FreeAlert ($A98A) -- mark ALRT resource and sub-resources as purgeable. |
| **`FREEALERT_CONT`** | `0x014DCE` | `0x00F3F8` | `dialog_mgr.s:801`<br>`dialog_mgr.s:792` | — |
| **`FREEALERT_CONT_2`** | `0x014DF0` | — | `dialog_mgr.s:815` | — |
| **`FREEALERT_CONT_3`** | `0x014DF4` | — | `dialog_mgr.s:823` | FREEALERT_CONT_3 Called during boot. |
| **`FREEALERT_EPILOGUE`** | — | `0x00F41A` | `dialog_mgr.s:807` | — |
| **`FREEALERT_ERR`** | `0x014DEE` | `0x00F418` | `dialog_mgr.s:813`<br>`dialog_mgr.s:805` | — |
| **`FREEALERT_WALK`** | — | `0x00F41E` | `dialog_mgr.s:810` | FREEALERT_WALK (FREEALERT_CONT_3): walk DITL preloading/freeing items + WDEF. |
| **`FreeDialog`** | `0x014DB4` | `0x00F3DE` | `dialog_mgr.s:786` | _FreeDialog ($A97A) Called during boot. |
| **`FREEDIALOG`** | `0x014DB4` | `0x00F3DE` | `dialog_mgr.s:780` | _FreeDialog ($A97A) -- mark DLOG resource and sub-resources as purgeable. Inverse of _CouldDialog: makes the DLOG, DITL, item sub-resources, and WDEF purgeable so the Memory Manager can reclaim them. |
| **`FrontWindow`** | `0x011D72` | `0x00C41E` | `window_mgr.s:1935` | **Proto:** `Pascal: function FrontWindow: WindowPtr;`<br>_FrontWindow ($A924) -> stack: WindowPtr (topmost visible window) Called during boot (14,779 times in 30s trace). _FrontWindow ($A924): return the frontmost visible window Pascal: function FrontWindow... |
| **`FRONTWINDOW`** | `0x011D72` | `0x00C41E` | `window_mgr.s:1804` | **Proto:** `Pascal: function FrontWindow: WindowPtr;`<br>_FrontWindow ($A924): return the frontmost visible window Pascal: function FrontWindow: WindowPtr; Scans window list, skipping invisible and ghost windows. |
| **`FRONTWINDOW_EXIT`** | `0x011D96` | `0x00C442` | `window_mgr.s:1956`<br>`window_mgr.s:1824` | FRONTWINDOW_EXIT - FrontWindow: return found window Called during boot (14,779 times in 30s trace). |
| **`FRONTWINDOW_EXIT_2`** | `0x011D9A` | `0x00C446` | `window_mgr.s:1958`<br>`window_mgr.s:1826` | — |
| **`FRONTWINDOW_LOOP`** | `0x011D80` | `0x00C42C` | `window_mgr.s:1940`<br>`window_mgr.s:1809` | — |
| **`FRONTWINDOW_SKIP`** | `0x011D90` | `0x00C43C` | `window_mgr.s:1947`<br>`window_mgr.s:1816` | — |
| **`FullClip`** | `0x01276A` | `0x00CD60` | `menu_mgr.s:890` | Full Clip Called during boot (28,789 times in 30s trace). |
| **`FULLCLIP`** | `0x01276A` | `0x00CD60` | `menu_mgr.s:630` | Restore the WMgr port's full clip region (after a per-menu ClipRect). |
| **`FULLCLIP_CONT`** | `0x012776` | `0x00CD6C` | `menu_mgr.s:901`<br>`menu_mgr.s:640` | FULLCLIP_CONT Called during boot. |
| **`FULLCLIP_NO`** | `0x012796` | — | `menu_mgr.s:913` | — |
| **`GET1INDRESOURCE`** | — | `0x00E2AA` | `resource_mgr.s:1357` | _Get1IndResource ($A80E), _GetIndResource ($A99D) -- get nth resource of type. _Get1IndResource searches only the current map (sets RMgrCurOnly). _GetIndResource searches all maps in chain. Stack: res... |
| **`GET1INDTYPE`** | — | `0x00E390` | `resource_mgr.s:1502` | _Get1IndType ($A80F), _GetIndType ($A99F) -- get type of nth distinct type. _Get1IndType restricts to current map (sets RMgrCurOnly). _GetIndType walks the chain. Stack: typePtr(L), index(W) -> stores... |
| **`Get1IxResource`** | `0x013CA0` | — | `resource_mgr.s:1440` | **Proto:** `Pascal: FUNCTION Get1IndResource(theType: ResType; index: INTEGER): Handle;`<br>**Regs:** `Entry: 4(SP).W = index, 6(SP).L = theType, 10(SP).L = space for the result Exit:  function result = resource handle (NIL if none); 6 bytes popped`<br>_Get1IxResource ($A80E): get the index'th resource of a given type in the current resource file only (Mac Plus addition, Inside Macintosh IV) Pascal: FUNCTION Get1IndResource(theType: ResType; index: ... |
| **`Get1IxType`** | `0x013D86` | — | `resource_mgr.s:1603` | **Proto:** `Pascal: PROCEDURE Get1IndType(VAR theType: ResType; index: INTEGER);`<br>**Regs:** `Entry: 4(SP).W = index, 6(SP).L = address of theType Exit:  theType = the type, or 0 (four NUL bytes) if index is out of`<br>_Get1IxType ($A80F): get the index'th distinct resource type in the current resource file only (Mac Plus addition, Inside Macintosh IV) Pascal: PROCEDURE Get1IndType(VAR theType: ResType; index: INTEG... |
| **`Get1NamedResour`** | `0x013E2E` | — | `resource_mgr.s:1725` | **Proto:** `Pascal: FUNCTION Get1NamedResource(theType: ResType; name: Str255): Handle;`<br>**Regs:** `Entry: 4(SP).L = name pointer, 8(SP).L = theType, 12(SP).L = result space Exit:  function result = resource handle (NIL if none); 8 bytes popped`<br>_Get1NamedResource ($A820): get a resource by type and name from the current resource file only (Mac Plus addition, Inside Macintosh IV) Pascal: FUNCTION Get1NamedResource(theType: ResType; name: Str2... |
| **`Get1NamedResource`** | `0x013E2E` | `0x00E438` | `resource_mgr.s:1726` | **Proto:** `Pascal: FUNCTION Get1NamedResource(theType: ResType; name: Str255): Handle;`<br>**Regs:** `Entry: 4(SP).L = name pointer, 8(SP).L = theType, 12(SP).L = result space Exit:  function result = resource handle (NIL if none); 8 bytes popped`<br>_Get1NamedResource ($A820): get a resource by type and name from the current resource file only (Mac Plus addition, Inside Macintosh IV) Pascal: FUNCTION Get1NamedResource(theType: ResType; name: Str2... |
| **`GET1NAMEDRESOURCE`** | `0x013E2E` | `0x00E438` | `resource_mgr.s:1595` | _Get1NamedResource ($A820), _GetNamedResource ($A9A1) -- find by name. Looks up a resource by Pascal-string name (case-insensitive) within the given type. Walks all references for the type, comparing ... |
| **`Get1Resource`** | `0x013DEA` | `0x00E3F4` | `resource_mgr.s:1673` | **Proto:** `Pascal: FUNCTION Get1Resource(theType: ResType; theID: INTEGER): Handle;`<br>**Regs:** `Entry: 4(SP).W = theID, 6(SP).L = theType, 10(SP).L = space for the result Exit:  function result = resource handle (NIL if none); 6 bytes popped`<br>_Get1Resource ($A81F): get a resource by type and ID from the current resource file only (Mac Plus addition, Inside Macintosh IV) Pascal: FUNCTION Get1Resource(theType: ResType; theID: INTEGER): Handl... |
| **`GET1RESOURCE`** | `0x013DEA` | `0x00E3F4` | `resource_mgr.s:1558` | _Get1Resource ($A81F), _GetResource ($A9A0) -- get resource by type and ID. _Get1Resource searches only the current map (sets RMgrCurOnly). _GetResource walks the entire chain, top map first. Stack: t... |
| **`GET_AUX_CTL_ENTRY`** | — | `0x00C916` | `window_mgr.s:2549` | _GetAuxCtl ($A368) entry: locate aux record for theControl. |
| **`GET_AUX_WIN_ENTRY`** | — | `0x00C910` | `window_mgr.s:2545` | **Proto:** `Pascal: function GetAuxWin(theWindow: WindowPtr; var awHndl: AuxWinHandle): BOOLEAN;`<br>_GetAuxWin ($A83C) entry: locate aux record for theWindow. Pascal: function GetAuxWin(theWindow: WindowPtr; var awHndl: AuxWinHandle): BOOLEAN; Falls into SEARCH_AUX_LIST with A1 = ghost_AuxWinHead. |
| **`GET_STR_PTR_LEN`** | `0x0111B8` | `0x00B800` | `window_mgr.s:59`<br>`window_mgr.s:74` | GET_STR_PTR_LEN - Get Pascal string pointer and byte count Returns A0 = ptr to string, D0 = length byte + 1 (total size). Called during boot. |
| **`GetCRefCon`** | `0x012F4C` | `0x00D550` | `control_mgr.s:308` | **Proto:** `Pascal: function GetCRefCon(theControl: ControlHandle): LongInt;`<br>Get C Ref Con _GetCRefCon: get control's refCon Pascal: function GetCRefCon(theControl: ControlHandle): LongInt; |
| **`GETCREFCON`** | `0x012F4C` | `0x00D550` | `control_mgr.s:269` | **Proto:** `Pascal: function GetCRefCon(theControl: ControlHandle): LongInt;`<br>_GetCRefCon ($A95A): get control's refCon longword. Pascal: function GetCRefCon(theControl: ControlHandle): LongInt; |
| **`GETCREFCON_CONT`** | `0x012F4E` | `0x00D552` | `control_mgr.s:310`<br>`control_mgr.s:272` | Shared get-longword body: stack [ret(4), result(4), handle(4)] |
| **`GetCTitle`** | `0x012FC6` | `0x00D5CA` | `control_mgr.s:410` | **Proto:** `Pascal: procedure GetCTitle(theControl: ControlHandle; title: Str255);`<br>Get C Title _GetCTitle: copy control's title to caller's string buffer Pascal: procedure GetCTitle(theControl: ControlHandle; title: Str255); |
| **`GETCTITLE`** | `0x012FC6` | `0x00D5CA` | `control_mgr.s:348` | **Proto:** `Pascal: procedure GetCTitle(theControl: ControlHandle; var title: Str255);`<br>_GetCTitle ($A95E): copy a control's title into a Pascal-string buffer. Pascal: procedure GetCTitle(theControl: ControlHandle; var title: Str255); |
| **`GetCtlAction`** | `0x012F6A` | `0x00D56E` | `control_mgr.s:338` | Get Ctl Action _GetCtlAction: get control's actionProc |
| **`GETCTLACTION`** | `0x012F6A` | `0x00D56E` | `control_mgr.s:291` | _GetCtlAction ($A96A): get control's action proc ptr. |
| **`GETCTLMAX`** | — | `0x00D636` | `control_mgr.s:409` | _GetCtlMax ($A962): get maximum of a control. |
| **`GETCTLMIN`** | — | `0x00D632` | `control_mgr.s:405` | _GetCtlMin ($A961): get minimum of a control. |
| **`GetCtlValue`** | `0x013020` | `0x00D624` | `control_mgr.s:461` | Get Ctl Value Called during boot. |
| **`GETCTLVALUE`** | `0x013020` | `0x00D624` | `control_mgr.s:395` | **Proto:** `Pascal: function GetCtlValue(theControl: ControlHandle): INTEGER;`<br>_GetCtlValue ($A960): get current value of a control. Pascal: function GetCtlValue(theControl: ControlHandle): INTEGER; |
| **`GETCTLVALUE_CONT`** | `0x013022` | `0x00D626` | `control_mgr.s:464`<br>`control_mgr.s:398` | GETCTLVALUE_CONT: generic get-word-field from ControlRecord |
| **`GetCursor`** | `0x015EE6` | `0x01053A` | `get_mgr.s:37` | _GetCursor ($A9B9) Called during boot. |
| **`GETCURSOR`** | `0x015EE6` | `0x01053A` | `get_mgr.s:34` | _GetCursor ($A9B9) - load 'CURS' resource by ID. |
| **`GetDItem`** | `0x014E3A` | `0x00F46A` | `dialog_mgr.s:870` | Get D Item |
| **`GETDITEM`** | `0x014E3A` | `0x00F46A` | `dialog_mgr.s:864` | _GetDItem ($A98D) -- read item info: type, handle, rect. Stack: theDialog(L), itemNo(W), itemType(L), item(L), box(L). Each output pointer (itemType, item, box) may be nil to skip. |
| **`GETDITEM_CONT`** | `0x014E7C` | — | `dialog_mgr.s:895` | — |
| **`GETDITEM_EMPTY`** | `0x014E62` | `0x00F492` | `dialog_mgr.s:884`<br>`dialog_mgr.s:878` | — |
| **`GETDITEM_RESTORE`** | — | `0x00F4A6` | `dialog_mgr.s:886` | — |
| **`GETDITEM_SKIP`** | `0x014E76` | — | `dialog_mgr.s:892` | — |
| **`GETDITEM_STRIP18`** | — | `0x00F4AC` | `dialog_mgr.s:889` | — |
| **`GetFName`** | `0x00F0C0` | — | `font_mgr.s:1540` | **Proto:** `Pascal: procedure GetFName(familyID: INTEGER; VAR name: Str255);`<br>_GetFName ($A8FF): get font name from font number Pascal: procedure GetFName(familyID: INTEGER; VAR name: Str255); |
| **`GETFNAME_CONT`** | `0x00F10C` | — | `font_mgr.s:1588` | GETFNAME_CONT GETFNAME_CONT: look up FOND resource by family ID with caching D3 = family ID, returns D0 = FOND handle (stripped), Z set if not found Called during boot. |
| **`GETFNAME_CONT_2`** | `0x00F112` | — | `font_mgr.s:1591` | GETFNAME_CONT_2: same but caller already set ROMMapInsert |
| **`GETFNAME_EMPTY`** | `0x00F13A` | — | `font_mgr.s:1608` | load FOND resource for this family restore purgeable flag on previous FOND before replacing cache |
| **`GETFNAME_EXIT`** | `0x00F0F2` | — | `font_mgr.s:1562` | clean up and return |
| **`GETFNAME_FOUND`** | `0x00F0DE` | — | `font_mgr.s:1554` | try FOND resource first no FOND: try old-style FONT resource found font resource: get its name via GetResInfo |
| **`GETFNAME_FOUND_2`** | `0x00F104` | — | `font_mgr.s:1576` | GETFNAME_FOUND_2 GETFNAME_FOUND_2: font not found - return empty name string |
| **`GETFNAME_FOUND_3`** | `0x00F154` | — | `font_mgr.s:1621` | cache FOND: save flags byte in high byte of handle, mark non-purgeable |
| **`GETFNAME_NO`** | `0x00F11C` | — | `font_mgr.s:1595` | — |
| **`GETFNAME_OK`** | `0x00F15C` | `0x01989C` | `font_mgr.s:1624`<br>`font_mgr.s:908` | — |
| **`GetFNum`** | `0x00F166` | `0x019DC8` | `font_mgr.s:1635` | **Proto:** `Pascal: procedure GetFNum(fontName: Str255; VAR theNum: INTEGER);`<br>_GetFNum ($A900) _GetFNum ($A900): get font number from font name Pascal: procedure GetFNum(fontName: Str255; VAR theNum: INTEGER); |
| **`GETFNUM`** | `0x00F166` | `0x019DC8` | `font_mgr.s:1544` | **Proto:** `Pascal: procedure GetFNum(fontName: Str255; VAR theNum: INTEGER);`<br>_GetFNum ($A900): get font number from font name Pascal: procedure GetFNum(fontName: Str255; VAR theNum: INTEGER); |
| **`GETFNUM_BODY`** | — | `0x019DB6` | `font_mgr.s:1534` | GETFNUM_BODY: GetNamedResource helper - load resource by type/name. D0 = resource type, D1 = name string ptr; returns D0 = handle. |
| **`GETFNUM_EXIT`** | `0x00F1C6` | — | `font_mgr.s:1671` | — |
| **`GETFNUM_FOUND`** | `0x00F1A0` | — | `font_mgr.s:1657` | try FOND resource first no FOND: try old-style FONT resource found font (FOND or FONT): get its resource ID via GetResInfo |
| **`GETFNUM_FOUND_2`** | `0x00F1D0` | — | `font_mgr.s:1682` | GETFNUM_FOUND_2: font not found by name - return 0 |
| **`GETFNUM_GET_INFO`** | — | `0x019DF0` | `font_mgr.s:1561` | — |
| **`GETFNUM_OK`** | `0x00F1C4` | — | `font_mgr.s:1669` | — |
| **`GETFNUM_RTS`** | — | `0x019E0A` | `font_mgr.s:1573` | — |
| **`GETFNUM_VIA_FOND`** | — | `0x019DEA` | `font_mgr.s:1556` | — |
| **`GETFNUM_VIA_OLDFONT`** | — | `0x019DEE` | `font_mgr.s:1559` | — |
| **`GETFONTNAME`** | — | `0x019D02` | `font_mgr.s:1440` | **Proto:** `Pascal: procedure GetFName(familyID: INTEGER; VAR name: Str255);`<br>_GetFName ($A8FF): get font name from font number Pascal: procedure GetFName(familyID: INTEGER; VAR name: Str255); |
| **`GETFONTNAME_GOT_RES`** | — | `0x019D20` | `font_mgr.s:1452` | — |
| **`GETFONTNAME_NONE`** | — | `0x019D32` | `font_mgr.s:1460` | — |
| **`GETFONTNAME_RTS`** | — | `0x019D36` | `font_mgr.s:1463` | — |
| **`GetIcon`** | `0x015EF6` | `0x01054A` | `get_mgr.s:55` | GetIcon -- trap handler for _GetIcon ($A9BB). _GetIcon ($A9BB) |
| **`GETICON`** | `0x015EF6` | `0x01054A` | `get_mgr.s:46` | _GetIcon ($A9BB) - load 'ICON' resource by ID. |
| **`GETIND_CACHE_ADV`** | `0x013CE2` | `0x00E2EC` | `resource_mgr.s:1472`<br>`resource_mgr.s:1385` | GETIND_CACHE_ADV - cache hit but type exhausted, advance to next map |
| **`GETIND_EXIT`** | `0x013D38` | `0x00E342` | `resource_mgr.s:1526`<br>`resource_mgr.s:1440` | — |
| **`GETIND_FIND_TYPE`** | `0x013CF8` | `0x00E302` | `resource_mgr.s:1487`<br>`resource_mgr.s:1402` | — |
| **`GETIND_FRESH`** | `0x013CE6` | `0x00E2F0` | `resource_mgr.s:1481`<br>`resource_mgr.s:1396` | GETIND_FRESH - fresh search: iterate maps for nth resource of type Called during boot (11,458 times in 30s trace). |
| **`GETIND_LOAD`** | `0x013D20` | `0x00E32A` | `resource_mgr.s:1513`<br>`resource_mgr.s:1428` | GETIND_LOAD: load resource at A2 and cache it. |
| **`GETIND_NEXTMAP`** | `0x013D18` | `0x00E322` | `resource_mgr.s:1509`<br>`resource_mgr.s:1423` | — |
| **`GETIND_NOTFOUND`** | `0x013D32` | `0x00E33C` | `resource_mgr.s:1524`<br>`resource_mgr.s:1438` | GETIND_NOTFOUND - resource not found by index |
| **`GETIND_SUB_SKIP`** | `0x013D14` | `0x00E31E` | `resource_mgr.s:1506`<br>`resource_mgr.s:1420` | GETIND_SUB_SKIP - not enough refs in this map, subtract and continue Called during boot (7,490 times in 30s trace). |
| **`GetIndResource`** | `0x013CA4` | `0x00E2AE` | `resource_mgr.s:1445` | **Proto:** `Pascal: FUNCTION GetIndResource(theType: ResType; index: INTEGER): Handle;`<br>GetIndResource -- _GetIndResource ($A99D): same over all open files. Pascal: FUNCTION GetIndResource(theType: ResType; index: INTEGER): Handle; Called 11,465 times during 30s boot-to-Finder. |
| **`GETINDRESOURCE`** | `0x013CA4` | `0x00E2AE` | `resource_mgr.s:1359` | — |
| **`GetIndType`** | `0x013D8A` | `0x00E394` | `resource_mgr.s:1606` | **Proto:** `GetIndType -- _GetIndType ($A99F): PROCEDURE GetIndType (VAR theType: ResType; index: Integer);`<br>GetIndType -- _GetIndType ($A99F): PROCEDURE GetIndType (VAR theType: ResType; index: Integer); |
| **`GETINDTYPE`** | `0x013D8A` | `0x00E394` | `resource_mgr.s:1504` | — |
| **`GETINDTYPE_EXIT`** | `0x013DA6` | `0x00E3B0` | `resource_mgr.s:1619`<br>`resource_mgr.s:1517` | — |
| **`GetItem`** | `0x012960` | `0x00CF8C` | `menu_mgr.s:1249` | **Proto:** `Pascal: PROCEDURE GetItem(theMenu: MenuHandle; item: INTEGER;`<br>**Regs:** `Entry: 0x4(SP) = @itemString, 0x8(SP) = item, 0xA(SP) = theMenu`<br>_GetItem ($A946): return the text of a menu item Pascal: PROCEDURE GetItem(theMenu: MenuHandle; item: INTEGER; VAR itemString: Str255); Entry: 0x4(SP) = @itemString, 0x8(SP) = item, 0xA(SP) = theMenu ... |
| **`GETITEM`** | `0x012960` | `0x00CF8C` | `menu_mgr.s:986` | **Proto:** `Pascal: procedure GetItem(theMenu: MenuHandle; item: INTEGER; var s: Str255);`<br>_GetItem ($A946): copy a menu item's text into a Pascal-string buffer. Pascal: procedure GetItem(theMenu: MenuHandle; item: INTEGER; var s: Str255); |
| **`GETITEM_CONT`** | `0x01297C` | — | `menu_mgr.s:1260` | — |
| **`GETITEM_EXIT`** | `0x012980` | — | `menu_mgr.s:1267` | GETITEM_EXIT - GetItem: no such item, return the empty string |
| **`GETITEM_FIND`** | — | `0x00CE5C` | `menu_mgr.s:784` | Walk MenuInfo to locate the Nth item (item entries are variable-length). MenuInfo layout: header(0xE bytes), title(Pascal str), items... Each item: nameLen.B, name.B*nameLen, icon.B, key.B, mark.B, st... |
| **`GETITEMICON`** | — | `0x00CED8` | `menu_mgr.s:868` | Get/Set item-attribute trap stubs: select attribute index in D2 then dispatch to the shared MENUMGR_CONT (set) or MENUMGR_CONT_2 (get). _GetItemIcon ($A93F): D2=0 |
| **`GETITEMMARK`** | — | `0x00CEE8` | `menu_mgr.s:884` | _GetItemMark ($A944): D2=2 |
| **`GETITEMSTYLE`** | — | `0x00CEE0` | `menu_mgr.s:876` | _GetItemStyle ($A943): D2=3 |
| **`GetIText`** | `0x014EB6` | `0x00F4E6` | `dialog_mgr.s:926` | Get I Text |
| **`GETITEXT`** | `0x014EB6` | `0x00F4E6` | `dialog_mgr.s:921` | _GetIText ($A990) -- read text from EditText/StaticText item. Stack: theItem(L), text(L). Reads the handle's contents and copies into caller's Pascal string buffer (clamped to 255 chars). |
| **`GETITEXT_OK`** | `0x014ECE` | `0x00F4FE` | `dialog_mgr.s:936`<br>`dialog_mgr.s:931` | — |
| **`GetItmIcon`** | `0x0128AC` | — | `menu_mgr.s:1107` | _GetItmIcon ($A93F) Item attribute accessors - D2 selects which attribute byte: 0 = icon number, 1 = key equivalent, 2 = mark character, 3 = style Get variants -> MENUMGR_CONT_2 (read), Set variants -... |
| **`GetItmMark`** | `0x0128BC` | — | `menu_mgr.s:1129` | GetItmMark -- trap handler for _GetItmMark ($A943). _GetItmMark ($A943) |
| **`GetItmStyle`** | `0x0128B4` | — | `menu_mgr.s:1118` | _GetItmStyle ($A941) |
| **`GetKeys`** | `0x010F30` | `0x00B4FC` | `toolbox_event.s:25` | **Proto:** `Pascal: PROCEDURE GetKeys(VAR theKeys: KeyMap)`<br>Toolbox Event Manager Apple source: ToolboxEventMgr.a (MacSEROM.lst module MISCMGR): GetKeys, Button, TickCount, GetMouse, StillDown, WaitMouseUp, EventAvail and GetNextEvent with the event filtering ... |
| **`GETKEYS`** | `0x010F30` | `0x00B4FC` | `toolbox_event.s:26` | **Proto:** `Pascal: PROCEDURE GetKeys(VAR theKeys: KeyMap)`<br>Toolbox Event Manager Apple source: ToolboxEventMgr.a (MacSEROM.lst module MISCMGR): GetKeys, Button, TickCount, GetMouse, StillDown, WaitMouseUp, EventAvail and GetNextEvent with the event filtering ... |
| **`GetMaxCtl`** | `0x013032` | — | `control_mgr.s:483` | Get Max Ctl |
| **`GETMENU`** | — | `0x010604` | `get_mgr.s:138` | _GetRMenu ($A9BF) / GETMENU - load MENU resource by ID. Loads the menuProc (MDEF) referenced by the MENU template if not already an MDEF resource, then calls _CalcMenuSize. |
| **`GetMenuBar`** | `0x01279E` | `0x00CD94` | `menu_mgr.s:923` | **Proto:** `GetMenuBar -- _GetMenuBar ($A93B): FUNCTION GetMenuBar: Handle;`<br>GetMenuBar -- _GetMenuBar ($A93B): FUNCTION GetMenuBar: Handle; _GetMenuBar ($A93B) |
| **`GETMENUBAR`** | `0x01279E` | `0x00CD94` | `menu_mgr.s:661` | **Proto:** `Pascal: function GetMenuBar: Handle;`<br>_GetMenuBar ($A93B): copy the current MenuList to a new handle. Pascal: function GetMenuBar: Handle; Used to save/restore menu-bar state across mode switches. |
| **`GETMENUBAR_CONT`** | `0x0127AC` | `0x00CDA2` | `menu_mgr.s:928`<br>`menu_mgr.s:666` | — |
| **`GETMENUITEMTEXT_CONT`** | — | `0x00CFA8` | `menu_mgr.s:997` | — |
| **`GETMENUITEMTEXT_EXIT`** | — | `0x00CFAC` | `menu_mgr.s:1000` | Empty-result path: store length=0 and exit. |
| **`GETMGREND`** | — | `0x0106E4` | `textedit.s:48` | TextEdit Apple source: TextEdit.a (MacSEROM.lst module TEXTEDIT). Basic text editing: TEGetText, TEInit, TEDispose, TextBox, TESetText, TECalText, TESetSelect, TENew, TEUpdate, TEClick, TECopy, TECut,... |
| **`GetMHandle`** | `0x012B7E` | `0x00D1AA` | `menu_mgr.s:1650` | **Proto:** `Pascal: FUNCTION GetMHandle(menuID: INTEGER): MenuHandle;`<br>**Regs:** `Entry: 0x4(SP) = menuID, 0x6(SP) = result. Searches the menu list`<br>_GetMHandle ($A949): return the handle of the menu with a given menu ID Pascal: FUNCTION GetMHandle(menuID: INTEGER): MenuHandle; Entry: 0x4(SP) = menuID, 0x6(SP) = result. Searches the menu list (INS... |
| **`GETMHANDLE`** | `0x012B7E` | `0x00D1AA` | `menu_mgr.s:1340` | **Proto:** `Pascal: function GetMHandle(menuID: INTEGER): MenuHandle;`<br>_GetMHandle ($A949): get MenuHandle by menuID. Pascal: function GetMHandle(menuID: INTEGER): MenuHandle; |
| **`GETMHANDLE_FOUND`** | `0x012B9A` | — | `menu_mgr.s:1660` | — |
| **`GETMHANDLE_RTS`** | — | `0x00D1C6` | `menu_mgr.s:1350` | — |
| **`GetMinCtl`** | `0x01302E` | — | `control_mgr.s:475` | Get Min Ctl |
| **`GetMouse`** | `0x010FA0` | `0x00B56C` | `toolbox_event.s:115` | **Proto:** `Pascal: PROCEDURE GetMouse(VAR mouseLoc: Point)`<br>_GetMouse ($A972) Pascal: PROCEDURE GetMouse(VAR mouseLoc: Point) Returns the current mouse position in local coordinates of the current GrafPort. Reads global coords from Mouse_v/Mouse_h, journals if... |
| **`GETMOUSE`** | `0x010FA0` | `0x00B56C` | `toolbox_event.s:108` | **Proto:** `Pascal: PROCEDURE GetMouse(VAR mouseLoc: Point)`<br>_GetMouse ($A972) Pascal: PROCEDURE GetMouse(VAR mouseLoc: Point) Returns the current mouse position in local coordinates of the current GrafPort. Reads global coords from Mouse_v/Mouse_h, journals if... |
| **`GETNAMED_CMP_NAME`** | `0x013E4C` | `0x00E456` | `resource_mgr.s:1739`<br>`resource_mgr.s:1607` | — |
| **`GETNAMED_LOOP`** | `0x013E3E` | `0x00E448` | `resource_mgr.s:1734`<br>`resource_mgr.s:1602` | — |
| **`GetNamedResource`** | `0x013E32` | `0x00E43C` | `resource_mgr.s:1729` | **Proto:** `GetNamedResource -- _GetNamedResource ($A9A1): FUNCTION GetNamedResource (theType: ResType; name: Str255): Handle;`<br>GetNamedResource -- _GetNamedResource ($A9A1): FUNCTION GetNamedResource (theType: ResType; name: Str255): Handle; |
| **`GETNAMEDRESOURCE`** | `0x013E32` | `0x00E43C` | `resource_mgr.s:1597` | — |
| **`GetNewControl`** | `0x015F5C` | `0x0105B4` | `get_mgr.s:108` | _GetNewControl ($A9BE) |
| **`GETNEWCONTROL`** | `0x015F5C` | `0x0105B4` | `get_mgr.s:100` | _GetNewControl ($A9BE) - create control from CNTL template. Loads CNTL resource by ID, then calls NewControl with the boundsRect, title, visible+value, min+max, procID and refCon from the template. |
| **`GETNEWCONTROL_FOUND`** | `0x015FA2` | `0x0105FA` | `get_mgr.s:134`<br>`get_mgr.s:127` | — |
| **`GetNewDialog`** | `0x014A90` | `0x00F0B2` | `dialog_mgr.s:293` | _GetNewDialog ($A97C) Called during boot. |
| **`GETNEWDIALOG`** | `0x014A90` | `0x00F0B2` | `dialog_mgr.s:288` | _GetNewDialog ($A97C) -- create a dialog from a 'DLOG' resource. Stack: dialogID(W), dStorage(L), behind(L) -> dialog(L). Loads the DLOG resource template, marshals its fields onto the stack as _NewDi... |
| **`GETNEWDIALOG_CONT`** | `0x014AC6` | `0x00F0E8` | `dialog_mgr.s:313`<br>`dialog_mgr.s:309` | — |
| **`GetNewMBar`** | `0x01602A` | `0x010682` | `get_mgr.s:215` | **Proto:** `GetNewMBar -- _GetNewMBar ($A9C0): FUNCTION GetNewMBar (menuBarID: Integer): Handle;`<br>GetNewMBar -- _GetNewMBar ($A9C0): FUNCTION GetNewMBar (menuBarID: Integer): Handle; _GetNewMBar ($A9C0) |
| **`GETNEWMBAR`** | `0x01602A` | `0x010682` | `get_mgr.s:206` | _GetNewMBar ($A9C0) - build menu bar from MBAR template. Loads MBAR resource, then for each menuID in the template calls _GetRMenu and _InsertMenu. Returns the resulting menu list handle (caller may p... |
| **`GETNEWMBAR_FOUND`** | `0x01607A` | `0x0106D0` | `get_mgr.s:248`<br>`get_mgr.s:239` | — |
| **`GETNEWMBAR_LOOP`** | `0x016052` | `0x0106AA` | `get_mgr.s:230`<br>`get_mgr.s:221` | — |
| **`GETNEWRGN`** | — | `0x00BA56` | `window_mgr.s:442` | GETNEWRGN (= PAINTBEHIND_EMPTY) - allocate new region; handle on stack Creates a new empty region. Returns with the handle on the stack (below the caller's return address). Called by: SAVEOLD, INITWIN... |
| **`GetNewWindow`** | `0x015F06` | `0x01055A` | `get_mgr.s:72` | _GetNewWindow ($A9BD) |
| **`GETNEWWINDOW`** | `0x015F06` | `0x01055A` | `get_mgr.s:61` | _GetNewWindow ($A9BD) - create window from WIND template. Loads WIND resource by ID and calls NewWindow with the boundsRect, title, visible flag, procID, behind window, goAwayFlag and refCon from the ... |
| **`GETNEWWINDOW_FOUND`** | `0x015F50` | `0x0105A8` | `get_mgr.s:97`<br>`get_mgr.s:88` | — |
| **`GetNextEvent`** | `0x011000` | `0x00B5CC` | `toolbox_event.s:199` | **Proto:** `Pascal: FUNCTION GetNextEvent(eventMask: INTEGER; VAR theEvent: EventRecord): BOOLEAN`<br>_GetNextEvent ($A970) Pascal: FUNCTION GetNextEvent(eventMask: INTEGER; VAR theEvent: EventRecord): BOOLEAN The main Toolbox event retrieval call. Removes event from queue. After TBOX_GET_EVENT does t... |
| **`GETNEXTEVENT`** | `0x011000` | `0x00B5CC` | `toolbox_event.s:175` | _GetNextEvent ($A970) Main Toolbox event retrieval; removes event from queue. Applies GNEFilter callback (if installed) before returning. |
| **`GetPattern`** | `0x015ECC` | `0x010520` | `get_mgr.s:19` | Resource getters -- GetPattern ... GetNewMBar Apple source: GetMgr.a (MacSEROM.lst module GMGR). Small Toolbox routines that read a resource and hand back the object built from it: GetPattern ('PAT ')... |
| **`GETPATTERN`** | `0x015ECC` | `0x010520` | `get_mgr.s:19` | Resource getters -- GetPattern ... GetNewMBar Apple source: GetMgr.a (MacSEROM.lst module GMGR). Small Toolbox routines that read a resource and hand back the object built from it: GetPattern ('PAT ')... |
| **`GETPATTERN_EXIT`** | `0x015ED2` | `0x010526` | `get_mgr.s:21`<br>`get_mgr.s:21` | — |
| **`GetPicture`** | `0x015EFE` | `0x010552` | `get_mgr.s:64` | **Proto:** `GetPicture -- _GetPicture ($A9BC): FUNCTION GetPicture (picID: INTEGER) : PicHandle;`<br>GetPicture -- _GetPicture ($A9BC): FUNCTION GetPicture (picID: INTEGER) : PicHandle; _GetPicture ($A9BC) |
| **`GETPICTURE`** | `0x015EFE` | `0x010552` | `get_mgr.s:52` | _GetPicture ($A9BC) - load 'PICT' resource by ID. |
| **`GETRES_EXIT`** | `0x013E2A` | `0x00E434` | `resource_mgr.s:1709`<br>`resource_mgr.s:1584` | — |
| **`GETRES_FIND_TYPE`** | `0x013E02` | `0x00E40C` | `resource_mgr.s:1688`<br>`resource_mgr.s:1569` | — |
| **`GETRES_FOUND`** | `0x013E1A` | `0x00E424` | `resource_mgr.s:1704`<br>`resource_mgr.s:1579` | GETRES_FOUND - GetResource: found resource, cache and load Called during boot (11,369 times in 30s trace). |
| **`GETRES_NEXTMAP`** | `0x013E12` | `0x00E41C` | `resource_mgr.s:1694`<br>`resource_mgr.s:1575` | — |
| **`GETRES_SEARCH`** | `0x013DFC` | `0x00E406` | `resource_mgr.s:1684`<br>`resource_mgr.s:1565` | — |
| **`GetResAttrs`** | `0x014538` | `0x00EB5C` | `resource_mgr.s:3050` | _GetResAttrs ($A9A6) Called during boot. |
| **`GETRESATTRS`** | `0x014538` | `0x00EB5C` | `resource_mgr.s:2890` | _GetResAttrs ($A9A6) -- read attribute byte for a resource handle. Stack: handle(L) -> attrs(B). Uses partial prologue + handle lookup via FINDRESHANDLE, then reads ref+4 attribute byte. |
| **`GETRESATTRS_NOT_FOUND`** | — | `0x00EB6C` | `resource_mgr.s:2896` | — |
| **`GETRESATTRS_SKIP`** | `0x014548` | — | `resource_mgr.s:3056` | — |
| **`GetResFileAttrs`** | `0x013838` | `0x00DE3A` | `resource_mgr.s:737` | _GetResFileAttrs ($A9F6) Returns the map attributes of the specified resource file. mAttr (+$16) = map attributes field in the resource map. Called during boot. |
| **`GETRESFILEATTRS`** | `0x013838` | `0x00DE3A` | `resource_mgr.s:727` | _GetResFileAttrs ($A9F6) -- read map attributes word for a refnum. |
| **`GetResInfo`** | `0x01457E` | `0x00EBA2` | `resource_mgr.s:3093` | _GetResInfo ($A9A8) Called during boot (3,620 times in 30s trace). |
| **`GETRESINFO`** | `0x01457E` | `0x00EBA2` | `resource_mgr.s:2937` | _GetResInfo ($A9A8) -- read type, ID, and name for a resource handle. Stack: handle(L), idPtr(L), typePtr(L), namePtr(L). Returns the resource's ID at *idPtr, type code at *typePtr, and name string at... |
| **`GETRESINFO_CONT`** | `0x0145BA` | `0x00EBDE` | `resource_mgr.s:3128`<br>`resource_mgr.s:2967` | GETRESINFO_CONT Called during boot (3,597 times in 30s trace). |
| **`GETRESINFO_EMPTY`** | `0x01459C` | `0x00EBC0` | `resource_mgr.s:3106`<br>`resource_mgr.s:2950` | — |
| **`GETRESINFO_EMPTY_2`** | `0x0145A4` | `0x00EBC8` | `resource_mgr.s:3111`<br>`resource_mgr.s:2955` | — |
| **`GETRESINFO_EMPTY_3`** | `0x0145B4` | `0x00EBD8` | `resource_mgr.s:3119`<br>`resource_mgr.s:2963` | — |
| **`GETRESINFO_EXIT`** | `0x014590` | `0x00EBB4` | `resource_mgr.s:3100`<br>`resource_mgr.s:2944` | — |
| **`GETRESNAME_EMPTY`** | — | `0x00E6E2` | `resource_mgr.s:2130` | GETRESNAME_EMPTY: no-name path -- return ptr to empty Pascal string in ROM. |
| **`GetResource`** | `0x013DEE` | `0x00E3F8` | `resource_mgr.s:1679` | **Proto:** `Pascal: FUNCTION GetResource(theType: ResType; theID: INTEGER): Handle;`<br>GetResource -- _GetResource ($A9A0): searches CurMap and all files opened before it. Pascal: FUNCTION GetResource(theType: ResType; theID: INTEGER): Handle; Called 11,438 times during 30s boot-to-Find... |
| **`GETRESOURCE`** | `0x013DEE` | `0x00E3F8` | `resource_mgr.s:1560` | — |
| **`GetRMenu`** | `0x015FAC` | — | `get_mgr.s:146` | _GetRMenu ($A9BF) Called during boot. |
| **`GETRMENU_CONT`** | `0x016010` | `0x010668` | `get_mgr.s:199`<br>`get_mgr.s:190` | GETRMENU_CONT Called during boot. |
| **`GETRMENU_DONE`** | `0x016004` | `0x01065C` | `get_mgr.s:186`<br>`get_mgr.s:177` | — |
| **`GETRMENU_NO`** | `0x015FDE` | `0x010636` | `get_mgr.s:171`<br>`get_mgr.s:162` | GETRMENU_NO |
| **`GETRMENU_NO_2`** | `0x015FE4` | `0x01063C` | `get_mgr.s:175`<br>`get_mgr.s:166` | — |
| **`GetScrap`** | `0x016EDA` | `0x012724` | `scrap_mgr.s:292` | **Proto:** `_GetScrap ($A9FD) - FUNCTION GetScrap(hDest: Handle; theType: ResType;`<br>_GetScrap ($A9FD) - FUNCTION GetScrap(hDest: Handle; theType: ResType; VAR offset: LongInt): LongInt Searches the scrap for data matching theType (e.g. 'TEXT', 'PICT'). Scrap format: repeating [type(4... |
| **`GETSCRAP`** | `0x016EDA` | `0x012724` | `scrap_mgr.s:230` | — |
| **`GETSCRAP_DONE`** | `0x016F32` | `0x01277C` | `scrap_mgr.s:347`<br>`scrap_mgr.s:282` | — |
| **`GETSCRAP_ERR`** | `0x016F2C` | `0x012776` | `scrap_mgr.s:343`<br>`scrap_mgr.s:278` | hDest is non-NIL: resize handle and copy data into it |
| **`GETSCRAP_FOUND`** | `0x016F0C` | `0x012756` | `scrap_mgr.s:328`<br>`scrap_mgr.s:263` | GETSCRAP_FOUND - found matching type; D3 = offset to data, (A1) = data length |
| **`GETSCRAP_NOTYPE`** | `0x016F08` | `0x012752` | `scrap_mgr.s:320`<br>`scrap_mgr.s:256` | skip this entry: advance D3 by data length, rounded up to even GETSCRAP_NOTYPE - requested scrap type not found in scrap |
| **`GETSCRAP_SCAN`** | `0x016EE8` | `0x012732` | `scrap_mgr.s:299`<br>`scrap_mgr.s:237` | scan through scrap entries looking for matching type |
| **`GETSCRAP_SET_ERR`** | `0x016F2E` | `0x012778` | `scrap_mgr.s:345`<br>`scrap_mgr.s:280` | — |
| **`GetSetWPort`** | `0x0114CE` | — | `window_mgr.s:593` | GetSetWPort - save current GrafPort in D4, switch to WMgr port (A5) points to CurrentA5 -> thePort. Saves old port in D4 and sets thePort to WMgrPort for window manager drawing. Called during boot. |
| **`GetString`** | `0x015EEE` | `0x010542` | `get_mgr.s:46` | **Proto:** `GetString -- _GetString ($A9BA): FUNCTION GetString (stringID: INTEGER) : StringHandle;`<br>GetString -- _GetString ($A9BA): FUNCTION GetString (stringID: INTEGER) : StringHandle; _GetString ($A9BA) |
| **`GETSTRING`** | `0x015EEE` | `0x010542` | `get_mgr.s:40` | _GetString ($A9BA) - load 'STR ' resource by ID. |
| **`GetStyleEntry`** | — | `0x0121E2` | `textedit.s:3712` | GetStyleEntry - resolve element index to StScrpRec entry. In: D0 = element index (font/face/size/color combination). Out: A0 = ptr to 18-byte StScrpRec entry. Each StScrpRec entry is 18 bytes (size/fa... |
| **`GETSYSMENUFONTINFO`** | — | `0x00C9E6` | `menu_mgr.s:118` | Get system-font metrics for menu bar layout. Saves D4 (used by SETWPORT), switches to WMgr port, calls _GetFontInfo, restores port, returns ascent:descent packed in D0 (high:low words). |
| **`GetWindowPic`** | `0x011888` | `0x00BEEE` | `window_mgr.s:1160` | **Proto:** `Pascal: function GetWindowPic(theWindow: WindowPtr): PicHandle;`<br>_GetWindowPic ($A92F): return window's auto-draw picture handle Pascal: function GetWindowPic(theWindow: WindowPtr): PicHandle; |
| **`GETWINDOWPIC`** | `0x011888` | `0x00BEEE` | `window_mgr.s:1081` | **Proto:** `Pascal: function GetWindowPic(theWindow: WindowPtr): PicHandle;`<br>_GetWindowPic ($A92F): return window's auto-draw picture handle Pascal: function GetWindowPic(theWindow: WindowPtr): PicHandle; |
| **`GetWMgrPort`** | `0x0114DE` | `0x00BB32` | `window_mgr.s:616` | **Proto:** `Pascal: procedure GetWMgrPort(VAR wPort: GrafPtr);`<br>_GetWMgrPort ($A910) _GetWMgrPort ($A910): return pointer to Window Manager's GrafPort Pascal: procedure GetWMgrPort(VAR wPort: GrafPtr); Called during boot. |
| **`GETWMGRPORT`** | `0x0114DE` | `0x00BB32` | `window_mgr.s:571` | **Proto:** `Pascal: procedure GetWMgrPort(VAR wPort: GrafPtr);`<br>_GetWMgrPort ($A910): return pointer to Window Manager's GrafPort Pascal: procedure GetWMgrPort(VAR wPort: GrafPtr); (Color variant follows for SE-internal _GetCWMgrPort.) |
| **`GetWRefCon`** | `0x011864` | `0x00BECA` | `window_mgr.s:1124` | **Proto:** `Pascal: function GetWRefCon(theWindow: WindowPtr): LongInt;`<br>_GetWRefCon ($A917): return window's refCon value Pascal: function GetWRefCon(theWindow: WindowPtr): LongInt; |
| **`GETWREFCON`** | `0x011864` | `0x00BECA` | `window_mgr.s:1048` | **Proto:** `Pascal: function GetWRefCon(theWindow: WindowPtr): LongInt;`<br>_GetWRefCon ($A917): return window's refCon value Pascal: function GetWRefCon(theWindow: WindowPtr): LongInt; |
| **`GETWREFCON_CONT`** | `0x011868` | `0x00BECE` | `window_mgr.s:1126`<br>`window_mgr.s:1050` | — |
| **`GetWTitle`** | `0x01188E` | `0x00BEF4` | `window_mgr.s:1169` | **Proto:** `Pascal: procedure GetWTitle(theWindow: WindowPtr; VAR title: Str255);`<br>_GetWTitle ($A919): copy window title into caller's buffer Pascal: procedure GetWTitle(theWindow: WindowPtr; VAR title: Str255); |
| **`GETWTITLE`** | `0x01188E` | `0x00BEF4` | `window_mgr.s:1089` | **Proto:** `Pascal: procedure GetWTitle(theWindow: WindowPtr; VAR title: Str255);`<br>_GetWTitle ($A919): copy window title into caller's buffer Pascal: procedure GetWTitle(theWindow: WindowPtr; VAR title: Str255); |
| **`GETWTITLE_LOOP`** | `0x01189C` | `0x00BF02` | `window_mgr.s:1175`<br>`window_mgr.s:1095` | — |
| **`GMGR`** | — | `0x010520` | `get_mgr.s:18` | Resource getters -- GetPattern ... GetNewMBar Apple source: GetMgr.a (MacSEROM.lst module GMGR). Small Toolbox routines that read a resource and hand back the object built from it: GetPattern ('PAT ')... |
| **`GNE_CALL_FILTER`** | `0x011022` | `0x00B5EE` | `toolbox_event.s:213`<br>`toolbox_event.s:189` | — |
| **`GNE_FKEY_CALL`** | — | `0x00B6CA` | `toolbox_event.s:303` | — |
| **`GrowWindow`** | `0x011FF4` | `0x00C6AA` | `window_mgr.s:2352` | **Proto:** `Pascal: function GrowWindow(theWindow: WindowPtr; startPt: Point;`<br>_GrowWindow ($A92B) stack: window, startPt, sizeRect -> stack: newSize _GrowWindow ($A92B): track mouse to resize a window Draws gray outline while tracking, returns new size on release Pascal: functi... |
| **`GROWWINDOW`** | `0x011FF4` | `0x00C6AA` | `window_mgr.s:2201` | **Proto:** `Pascal: function GrowWindow(theWindow: WindowPtr; startPt: Point;`<br>_GrowWindow ($A92B): track mouse to resize a window Pascal: function GrowWindow(theWindow: WindowPtr; startPt: Point; sizeRect: Rect): LongInt; Returns: high=height, low=width; 0=cancelled. |
| **`GROWWINDOW_CONT`** | `0x0120A0` | `0x00C75C` | `window_mgr.s:2430`<br>`window_mgr.s:2280` | GROWWINDOW_CONT - send wGrow message to WDEF (draw/erase grow outline) Passes grow rect (A4) as param. Preserves D3. |
| **`GROWWINDOW_CONT_2`** | `0x0120AE` | `0x00C76A` | `window_mgr.s:2444`<br>`window_mgr.s:2293` | GROWWINDOW_CONT_2 - read mouse, compute constrained new botRight for grow rect Reads mouse, applies anchor offset D5, pins size to sizeRect, computes new absolute position in D3. |
| **`GROWWINDOW_CONT_3`** | `0x0120E6` | `0x00C7A2` | `window_mgr.s:2474`<br>`window_mgr.s:2322` | pin size to sizeRect bounds compute new absolute position from pinned size GROWWINDOW_CONT_3 - compute grow rect size (botRight - topLeft) -> D0 |
| **`GROWWINDOW_EXIT`** | `0x012088` | `0x00C744` | `window_mgr.s:2413`<br>`window_mgr.s:2264` | mouse released: compute final size |
| **`GROWWINDOW_EXIT_2`** | `0x012098` | `0x00C754` | `window_mgr.s:2420`<br>`window_mgr.s:2271` | GROWWINDOW_EXIT_2 - strip 12 bytes of params and return |
| **`GROWWINDOW_OK`** | `0x012052` | `0x00C70E` | `window_mgr.s:2387`<br>`window_mgr.s:2238` | set up XOR pen for grow outline initialize grow rect in A4 (portRect in global coords) draw initial grow outline and save initial size compute offset from startPt to grow rect's botRight grow tracking... |
| **`GROWWINDOW_SKIP`** | `0x012072` | — | `window_mgr.s:2401` | — |
| **`HandAndHand`** | `0x01572C` | `0x00FD64` | `toolbox_utils.s:383` | **Proto:** `Pascal: FUNCTION HandAndHand(aHndl, bHndl: Handle): OSErr;`<br>**Regs:** `Entry: A0 = source handle (aHndl), A1 = destination handle (bHndl) Exit:  A0 = destination handle, D0 = result code`<br>_HandAndHand ($A9E4): append the data of handle A0 to handle A1 Pascal: FUNCTION HandAndHand(aHndl, bHndl: Handle): OSErr; Entry: A0 = source handle (aHndl), A1 = destination handle (bHndl) Exit:  A0 ... |
| **`HANDANDHAND`** | `0x01572C` | `0x00FD64` | `toolbox_utils.s:320` | _HandAndHand ($A9E4) - Append handle A0's data to end of handle A1. Both handles preserved. A0 state restored. |
| **`HandToHand`** | `0x0156EC` | `0x00FD1A` | `toolbox_utils.s:314` | **Proto:** `Pascal: FUNCTION HandToHand(VAR theHndl: Handle): OSErr;`<br>**Regs:** `Entry: A0 = source handle Exit:  A0 = new handle (copy), D0 = result code`<br>_HandToHand ($A9E1): copy a relocatable block into a new handle Pascal: FUNCTION HandToHand(VAR theHndl: Handle): OSErr; Entry: A0 = source handle Exit:  A0 = new handle (copy), D0 = result code The s... |
| **`HANDTOHAND`** | `0x0156EC` | `0x00FD1A` | `toolbox_utils.s:261` | **Regs:** `Entry: A0 = source handle. Exit: A0 = new handle (copy).`<br>_HandToHand ($A9E1) - Duplicate a handle. Entry: A0 = source handle. Exit: A0 = new handle (copy). Preserves source handle's master pointer state via HGetState/HSetState. |
| **`HANDTOHAND_ERR`** | `0x015704` | — | `toolbox_utils.s:326` | — |
| **`HideControl`** | `0x012EF4` | `0x00D4F8` | `control_mgr.s:255` | _HideControl ($A958) Called during boot. |
| **`HIDECONTROL`** | `0x012EF4` | `0x00D4F8` | `control_mgr.s:222` | **Proto:** `Pascal: procedure HideControl(theControl: ControlHandle);`<br>_HideControl ($A958): make a control invisible. Pascal: procedure HideControl(theControl: ControlHandle); |
| **`HideDItem`** | `0x014F92` | `0x00F5C2` | `dialog_mgr.s:1045` | **Proto:** `Pascal: PROCEDURE HideDItem(theDialog: DialogPtr; itemNo: INTEGER);`<br>_HideDItem ($A827): hide an item of a dialog Pascal: PROCEDURE HideDItem(theDialog: DialogPtr; itemNo: INTEGER); Entry (after the MODALDIALOG_CONT_3 prologue): 0x8(A6) = itemNo, 0xA(A6) = theDialog No... |
| **`HIDEDITEM`** | `0x014F92` | `0x00F5C2` | `dialog_mgr.s:1045` | _HideDItem ($A827) -- hide a dialog item by moving it offscreen. Stack: theDialog(L), itemNo(W). Adds 0x4000 to item's left and right coords (moves to "hidden" range >= 0x2000). Erases visible area, d... |
| **`HIDEDITEM_EXIT`** | `0x014FB4` | — | `dialog_mgr.s:1056` | — |
| **`HIDEDITEM_EXIT_2`** | `0x014FE8` | `0x00F618` | `dialog_mgr.s:1081`<br>`dialog_mgr.s:1076` | — |
| **`HIDEDITEM_NO`** | `0x014FBE` | `0x00F5EE` | `dialog_mgr.s:1065`<br>`dialog_mgr.s:1060` | HIDEDITEM_NO - hide dialog item by moving it offscreen |
| **`HIDEDITEM_RESTORE`** | — | `0x00F5E4` | `dialog_mgr.s:1056` | — |
| **`HIDEDITEM_SKIP`** | `0x014FCC` | `0x00F5FC` | `dialog_mgr.s:1071`<br>`dialog_mgr.s:1066` | — |
| **`HIDEDITEM_SKIP_2`** | `0x014FEE` | `0x00F61E` | `dialog_mgr.s:1085`<br>`dialog_mgr.s:1080` | — |
| **`HideWindow`** | `0x01183A` | `0x00BEA0` | `window_mgr.s:1091` | **Proto:** `Pascal: procedure HideWindow(theWindow: WindowPtr);`<br>_HideWindow ($A916) stack: window -> (makes window invisible) _HideWindow ($A916): hide a window and select next visible if it was front Pascal: procedure HideWindow(theWindow: WindowPtr); Called duri... |
| **`HIDEWINDOW`** | `0x01183A` | `0x00BEA0` | `window_mgr.s:1017` | **Proto:** `Pascal: procedure HideWindow(theWindow: WindowPtr);`<br>_HideWindow ($A916): hide a window and select next visible if it was front Pascal: procedure HideWindow(theWindow: WindowPtr); |
| **`HIDEWINDOW_DONE`** | `0x01185C` | `0x00BEC2` | `window_mgr.s:1106`<br>`window_mgr.s:1032` | — |
| **`HIDEWINDOW_EMPTY`** | `0x011860` | `0x00BEC6` | `window_mgr.s:1115`<br>`window_mgr.s:1040` | HIDEWINDOW_EMPTY - no front window: discard nil FrontWindow result Called during boot. |
| **`HiliteControl`** | `0x012F9A` | `0x00D59E` | `control_mgr.s:382` | **Proto:** `Pascal: procedure HiliteControl(theControl: ControlHandle; hiliteState: INTEGER);`<br>_HiliteControl ($A95D) Called during boot. _HiliteControl: change hilite state of a control Pascal: procedure HiliteControl(theControl: ControlHandle; hiliteState: INTEGER); |
| **`HILITECONTROL`** | `0x012F9A` | `0x00D59E` | `control_mgr.s:322` | **Proto:** `Pascal: procedure HiliteControl(theControl: ControlHandle; hiliteState: INTEGER);`<br>_HiliteControl ($A95D): set highlight state for a control part. Pascal: procedure HiliteControl(theControl: ControlHandle; hiliteState: INTEGER); |
| **`HILITECONTROL_CONT`** | `0x012FBA` | — | `control_mgr.s:395` | — |
| **`HILITECONTROL_CONT_2`** | `0x012FC0` | `0x00D5C4` | `control_mgr.s:399`<br>`control_mgr.s:340` | Common exit for 6-byte param routines. |
| **`HILITECONTROL_DRAW_NEW`** | — | `0x00D5BE` | `control_mgr.s:335` | — |
| **`HILITECONTROL_OK`** | `0x012FBE` | `0x00D5C2` | `control_mgr.s:397`<br>`control_mgr.s:337` | — |
| **`HiliteMenu`** | `0x0123DA` | `0x00CAFE` | `menu_mgr.s:370` | _HiliteMenu ($A938) stack: menuID -> (highlights menu title) Called during boot. |
| **`HILITEMENU`** | `0x0123DA` | `0x00CAFE` | `menu_mgr.s:290` | **Proto:** `Pascal: procedure HiliteMenu(menuID: INTEGER);`<br>_HiliteMenu ($A938): highlight the title of a menu in the menu bar. Pascal: procedure HiliteMenu(menuID: INTEGER); menuID=0 = unhighlight current. Hilites at most one title at a time. |
| **`HILITEMENU_NEW`** | — | `0x00CB1C` | `menu_mgr.s:301` | — |
| **`HILITEMENU_NOT_FOUND`** | — | `0x00CB40` | `menu_mgr.s:316` | Not-found path: clear TheMenu and return. |
| **`HILITEMENU_OK`** | `0x0123FA` | — | `menu_mgr.s:381` | — |
| **`HILITEMENU_RESTORE_VISRGN`** | — | `0x00CE00` | `menu_mgr.s:726` | — |
| **`HILITEMENU_SET_THEMENU`** | — | `0x00CB38` | `menu_mgr.s:311` | — |
| **`HILITEMENU_UNHILITE`** | — | `0x00CDFC` | `menu_mgr.s:724` | — |
| **`HiliteWindow`** | `0x011A84` | `0x00C11E` | `window_mgr.s:1467` | **Proto:** `Pascal: procedure HiliteWindow(theWindow: WindowPtr; fHilite: BOOLEAN);`<br>invisible: empty all regions _HiliteWindow ($A91C) stack: window, fHilite -> (highlights/unhighlights) _HiliteWindow ($A91C): highlight or unhighlight a window's title bar Pascal: procedure HiliteWind... |
| **`HILITEWINDOW`** | `0x011A84` | `0x00C11E` | `window_mgr.s:1382` | **Proto:** `Pascal: procedure HiliteWindow(theWindow: WindowPtr; fHilite: BOOLEAN);`<br>_HiliteWindow ($A91C): highlight or unhighlight a window's title bar Pascal: procedure HiliteWindow(theWindow: WindowPtr; fHilite: BOOLEAN); Only acts if the highlight state is actually changing. |
| **`HILITEWINDOW_CONT`** | `0x011AB2` | `0x00C14C` | `window_mgr.s:1489`<br>`window_mgr.s:1403` | HILITEWINDOW_CONT - clip WMgr port to window's strucRgn minus windows above Called during boot. |
| **`HILITEWINDOW_CONT_2`** | `0x011AB6` | `0x00C150` | `window_mgr.s:1491`<br>`window_mgr.s:1405` | — |
| **`HILITEWINDOW_CONT_3`** | `0x011ABE` | `0x00C158` | `window_mgr.s:1501`<br>`window_mgr.s:1414` | HILITEWINDOW_CONT_3 - clip WMgr port to GrayRgn (desktop) minus windows above A3 |
| **`HILITEWINDOW_RESTORE`** | — | `0x00C140` | `window_mgr.s:1394` | — |
| **`HILITEWINDOW_SKIP`** | `0x011AA6` | — | `window_mgr.s:1479` | — |
| **`HiWord`** | `0x01597C` | `0x00FFC4` | `fixmath.s:456` | **Proto:** `Pascal: FUNCTION HiWord(x: LONGINT): INTEGER;`<br>**Regs:** `Entry: 4(SP) = x, 8(SP) = INTEGER result slot (no frame, no registers) Exit:  result = bits 31..16 of x; x removed from the stack`<br>_HiWord ($A86A): high-order word of a long integer Pascal: FUNCTION HiWord(x: LONGINT): INTEGER; Entry: 4(SP) = x, 8(SP) = INTEGER result slot (no frame, no registers) Exit:  result = bits 31..16 of x... |
| **`HIWORD`** | `0x01597C` | `0x00FFC4` | `fixmath.s:358` | _HiWord ($A86A) - Extract high word of long. |
| **`HIWORD_EXIT`** | `0x015982` | — | `fixmath.s:458` | — |
| **`HIWORD_MOVE_RETURN`** | — | `0x00FFCA` | `fixmath.s:360` | — |
| **`HomeResFile`** | `0x0144BC` | `0x00EADE` | `resource_mgr.s:2939` | _HomeResFile ($A9A4) Called during boot. |
| **`HOMERESFILE`** | `0x0144BC` | `0x00EADE` | `resource_mgr.s:2805` | _HomeResFile ($A9A4) -- find which resource file owns a handle. Stack: handle(L) -> refNum(W). Returns -1 if not in any map. If owning map is SysMap, returns 0 (the conventional alias). |
| **`HOMERESFILE_CONT`** | `0x0144D4` | — | `resource_mgr.s:2953` | HOMERESFILE_CONT |
| **`HOMERESFILE_EXIT`** | `0x0144CC` | `0x00EAEE` | `resource_mgr.s:2945`<br>`resource_mgr.s:2811` | — |
| **`HOMERESFILE_SKIP`** | `0x0144E2` | `0x00EB06` | `resource_mgr.s:2960`<br>`resource_mgr.s:2829` | — |
| **`IAPPEND`** | — | `0x00EECA` | `dialog_mgr.s:20` | Dialog Manager Apple source: DialogMgr.a (MacSEROM.lst module DMGR). The public traps come first, in physical ROM order: InitDialogs                                     (initialization) StopAlert, Not... |
| **`InfoScrap`** | `0x016DAC` | `0x0125F6` | `scrap_mgr.s:37` | **Proto:** `_InfoScrap ($A9F9) - FUNCTION InfoScrap: PScrapStuff`<br>Scrap Manager - InfoScrap, UnloadScrap, LodeScrap, ZeroScrap, GetScrap, PutScrap Manages the desk scrap (clipboard) for cut/copy/paste between applications. The scrap lives either in memory (ScrapStat... |
| **`INFOSCRAP`** | `0x016DAC` | `0x0125F6` | `scrap_mgr.s:37` | **Proto:** `Pascal: function InfoScrap: PScrapStuff;`<br>Scrap Manager - InfoScrap, UnloadScrap, LodeScrap, ZeroScrap, GetScrap, PutScrap Manages the desk scrap (clipboard) for cut/copy/paste between applications. The scrap lives either in memory (ScrapStat... |
| **`INFOSCRAP_RETURN`** | `0x016DB8` | `0x012602` | `scrap_mgr.s:43`<br>`scrap_mgr.s:43` | — |
| **`INITALL_PUSH_LOOP`** | `0x016FB6` | `0x01A024` | `package_mgr.s:47`<br>`package_mgr.s:45` | — |
| **`InitAllPacks`** | `0x016FB2` | `0x01A020` | `package_mgr.s:44` | **Proto:** `Pascal: PROCEDURE InitAllPacks;`<br>_InitAllPacks ($A9E6) Builds a stack frame that calls InitPack for each of the 16 packages (IDs 0-15). Pushes alternating packID/return-addr pairs so the RTS chain calls InitPack 16 times. Also initia... |
| **`INITALLPACKS`** | `0x016FB2` | `0x01A020` | `package_mgr.s:42` | **Proto:** `Pascal: procedure InitAllPacks;`<br>_InitAllPacks ($A9E6) - install all 16 Packages. Pascal: procedure InitAllPacks; Pushes 16 packIDs (15..0) onto stack, each followed by the InitPack address, so the chain runs InitPack 16 times. Then ... |
| **`InitDialogs`** | `0x0148B2` | `0x00EED4` | `dialog_mgr.s:37` | **Proto:** `InitDialogs -- _InitDialogs ($A97B): PROCEDURE InitDialogs (resumeProc: ProcPtr);`<br>InitDialogs -- _InitDialogs ($A97B): PROCEDURE InitDialogs (resumeProc: ProcPtr); |
| **`INITDIALOGS`** | `0x0148B2` | `0x00EED4` | `dialog_mgr.s:34` | _InitDialogs ($A97B) -- initialize Dialog Manager state. Stack: resumeProc(L). Sets ResumeProc, clears alert state, installs default DABeeper, clears ParamText slots, sets dialog font to system. |
| **`INITDIALOGS_CONT`** | `0x0148E0` | `0x00EF02` | `dialog_mgr.s:58`<br>`dialog_mgr.s:57` | INITDIALOGS_CONT Called during boot. |
| **`INITDIALOGS_DONE`** | `0x0148F6` | `0x00EF18` | `dialog_mgr.s:75`<br>`dialog_mgr.s:73` | INITDIALOGS_DONE - beep loop done, return to caller Called during boot. |
| **`INITDIALOGS_EXIT`** | `0x0148F8` | `0x00EF1A` | `dialog_mgr.s:83`<br>`dialog_mgr.s:85` | INITDIALOGS_EXIT Called during boot. |
| **`INITDIALOGS_LOOP`** | `0x0148E4` | `0x00EF06` | `dialog_mgr.s:61`<br>`dialog_mgr.s:60` | — |
| **`INITDIALOGS_OK`** | `0x014922` | `0x00EF44` | `dialog_mgr.s:95`<br>`dialog_mgr.s:97` | — |
| **`INITDIALOGS_SKIP`** | `0x01495A` | `0x00EF7C` | `dialog_mgr.s:115`<br>`dialog_mgr.s:117` | — |
| **`INITDIALOGS_SKIP_2`** | `0x01495E` | `0x00EF80` | `dialog_mgr.s:117`<br>`dialog_mgr.s:119` | — |
| **`InitFonts`** | `0x00E5E4` | `0x019150` | `font_mgr.s:12` | Font Manager Manages font resources and provides font metrics for QuickDraw text drawing. Handles font scaling, style variations (bold, italic, underline, outline, shadow), and font substitution. Refe... |
| **`INITFONTS`** | `0x00E5E4` | `0x019150` | `font_mgr.s:29` | Font Manager Apple source: FontMgr.a (MacSEROM.lst module FONTMANAGER): InitFonts, FMSwapFont (with FPOINTONE), GetFName ($A8FF), RealFont ($A902), GetFNum ($A900), SetFontLock ($A903), SetFScaleDisab... |
| **`INITFONTS_CONT`** | `0x00E622` | — | `font_mgr.s:33` | set application font from PRAM load system font (FONT resource) |
| **`INITFONTS_CONT_2`** | `0x00E682` | `0x0191DC` | `font_mgr.s:79`<br>`font_mgr.s:85` | INITFONTS_CONT_2: invalidate all width table caches Sets font handle and FMInput fields to -1 so next SwapFont reloads |
| **`INITFONTS_DONE`** | `0x00E6B0` | — | `font_mgr.s:99` | — |
| **`INITFONTS_ERR`** | `0x00E664` | — | `font_mgr.s:58` | set up width table for fractional widths allocate width list if enough RAM (>= 512K) |
| **`INITFONTS_ERR_2`** | `0x00E67E` | `0x0191D8` | `font_mgr.s:74`<br>`font_mgr.s:73` | INITFONTS_ERR_2 |
| **`INITFONTS_FOUND`** | `0x00E630` | — | `font_mgr.s:39` | — |
| **`INITFONTS_INSTALL_VECTOR`** | — | `0x0191B0` | `font_mgr.s:56` | — |
| **`INITFONTS_LIST_LOOP`** | — | `0x0191EE` | `font_mgr.s:93` | — |
| **`INITFONTS_LOOP`** | `0x00E698` | — | `font_mgr.s:88` | — |
| **`INITFONTS_NO`** | `0x00E678` | — | `font_mgr.s:66` | — |
| **`INITFONTS_SKIP`** | `0x00E6AC` | `0x019202` | `font_mgr.s:97`<br>`font_mgr.s:102` | — |
| **`InitMenus`** | `0x012198` | `0x00C97C` | `menu_mgr.s:30` | Menu Manager Apple source: MenuMgr.a (MacSEROM.lst module MMGR). In ROM order: InitMenus, ClearMenuBar, InsertMenu, DeleteMenu, DrawMenuBar, HiliteMenu, EnableItem, DisableItem, MenuSelect, GetMenuBar... |
| **`INITMENUS`** | `0x012198` | `0x00C97C` | `menu_mgr.s:63` | **Proto:** `Pascal: procedure InitMenus;`<br>_InitMenus ($A930): initialize the Menu Manager. Loads 'MBDF' #0 (standard menu-bar definition function), allocates MenuList, sets flash count from PRAM, fires MBDF init message, draws empty menu bar.... |
| **`INITMENUS_ALREADY_INIT`** | — | `0x00C9D4` | `menu_mgr.s:98` | — |
| **`INITMENUS_BODY`** | — | `0x00C99C` | `menu_mgr.s:80` | Shared init body (called from InitMenus and InitProcMenu). Allocates MenuList if not yet created, programs MenuFlash from PRAM, zeros MBarEnable/MBarHook/MenuHook/MBFlash, fires MBDF init (msg=3), the... |
| **`INITMENUS_NO_MBDF`** | — | `0x00C970` | `menu_mgr.s:49` | Fallback path: 'MBDF' resID not found, do standard InitMenus and return. |
| **`INITMENUS_RTS_INDIRECT`** | — | `0x00C96E` | `menu_mgr.s:46` | — |
| **`InitPack`** | `0x016F90` | `0x019FFE` | `package_mgr.s:21` | **Proto:** `Pascal: PROCEDURE InitPack(packID: INTEGER);`<br>Package Manager -- _InitPack, _InitAllPacks, _Pack0 ... _Pack15 Apple source: PackageMgr.a (MacSEROM.lst module PACKDISPATCHER). InitPack loads one PACK resource and stores its handle in AppPacks (pac... |
| **`INITPACK`** | `0x016F90` | `0x019FFE` | `package_mgr.s:22` | **Proto:** `Pascal: procedure InitPack(packID: INTEGER);`<br>Package Manager -- _InitPack, _InitAllPacks, _Pack0 ... _Pack15 Apple source: PackageMgr.a (MacSEROM.lst module PACKDISPATCHER). InitPack loads one PACK resource and stores its handle in AppPacks (pac... |
| **`INITPROCMENU`** | — | `0x00C94A` | `menu_mgr.s:33` | **Proto:** `Pascal: procedure InitProcMenu(resID: INTEGER);`<br>Menu Manager Apple source: MenuMgr.a (MacSEROM.lst module MMGR). In ROM order: InitProcMenu ($A808, SE: InitMenus with a given MBDF), InitMenus, ClearMenuBar, InsertMenu, DeleteMenu, DrawMenuBar, Hili... |
| **`INITRES_LOADALL`** | — | `0x00DA9C` | `resource_mgr.s:234` | — |
| **`INITRES_LOADALL_LOOP`** | — | `0x00DAC2` | `resource_mgr.s:250` | — |
| **`InitResources`** | `0x013376` | `0x00D97A` | `resource_mgr.s:96` | **Proto:** `InitResources -- _InitResources ($A995): FUNCTION InitResources: Integer;`<br>InitResources -- _InitResources ($A995): FUNCTION InitResources: Integer; |
| **`INITRESOURCES`** | `0x013376` | `0x00D97A` | `resource_mgr.s:102` | **Proto:** `Pascal: function InitResources: INTEGER;`<br>_InitResources ($A995): initialize the Resource Manager. Pascal: function InitResources: INTEGER; Sets up the ROM resource map (TopMapHndl/SysMapHndl), then opens the system file's resource fork as th... |
| **`INITRESOURCES_CONT`** | `0x0133EC` | `0x00D9F0` | `resource_mgr.s:144`<br>`resource_mgr.s:145` | INITRESOURCES_CONT Called during boot. |
| **`INITRESOURCES_CONT_2`** | `0x013404` | `0x00DA08` | `resource_mgr.s:162`<br>`resource_mgr.s:163` | INITRESOURCES_CONT_2 Called during boot. |
| **`INITRESOURCES_CONT_3`** | `0x01345A` | `0x00DA5C` | `resource_mgr.s:201`<br>`resource_mgr.s:203` | INITRESOURCES_CONT_3 Called during boot. |
| **`INITRESOURCES_CONT_4`** | `0x013496` | `0x00DA98` | `resource_mgr.s:229`<br>`resource_mgr.s:232` | INITRESOURCES_CONT_4 Called during boot. |
| **`INITRESOURCES_CONT_5`** | `0x01349A` | — | `resource_mgr.s:232` | INITRESOURCES_CONT_5 -- preload flagged resources. |
| **`INITRESOURCES_ERR`** | `0x0134CC` | `0x00DACE` | `resource_mgr.s:253`<br>`resource_mgr.s:256` | Called by: INITRESOURCES_LOOP_2, INITRES_LOADALL |
| **`INITRESOURCES_LOOP`** | `0x013484` | `0x00DA86` | `resource_mgr.s:217`<br>`resource_mgr.s:219` | — |
| **`INITRESOURCES_LOOP_2`** | `0x0134A6` | `0x00DAA8` | `resource_mgr.s:237`<br>`resource_mgr.s:239` | — |
| **`INITRESOURCES_RETRY`** | `0x0134C0` | — | `resource_mgr.s:248` | — |
| **`INITRESOURCES_SKIP`** | `0x0133A2` | `0x00D9A6` | `resource_mgr.s:115`<br>`resource_mgr.s:117` | INITRESOURCES_SKIP Called during boot. |
| **`INITRESOURCES_SKIP_2`** | `0x0133E8` | `0x00D9EC` | `resource_mgr.s:136`<br>`resource_mgr.s:138` | — |
| **`INITRESOURCES_SKIP_3`** | `0x013402` | `0x00DA06` | `resource_mgr.s:154`<br>`resource_mgr.s:155` | — |
| **`InitWindows`** | `0x01157C` | `0x00BBDA` | `window_mgr.s:724` | _InitWindows ($A912) -> (initializes Window Manager) _InitWindows ($A912): initialize the Window Manager Creates WMgrPort, GrayRgn (desktop), paints desktop pattern |
| **`INITWINDOWS`** | `0x01157C` | `0x00BBDA` | `window_mgr.s:672` | _InitWindows ($A912): initialize the Window Manager Creates WMgrPort, GrayRgn (desktop), paints desktop pattern. SE-only: also calls _InitMenus before drawing the menu bar. |
| **`INITWINDOWS_EMPTY`** | `0x011636` | `0x00BC9C` | `window_mgr.s:800`<br>`window_mgr.s:749` | paint desktop initialize window list and globals INITWINDOWS_EMPTY - NewWindow with caller-supplied storage Strips high byte from pointer (24-bit addressing), opens as port. Called during boot. |
| **`INSERT_WINDOW`** | `0x0111E8` | `0x00B830` | `window_mgr.s:109`<br>`window_mgr.s:121` | INSERT_WINDOW - Insert window into the window list Stack: 0x8(SP) = window to insert, 0x4(SP) = behind window (or 0). If behind = 0, inserts at end of list (behind all windows). If WindowList is empty... |
| **`InsertMenu`** | `0x01220E` | `0x00CA26` | `menu_mgr.s:115` | **Proto:** `Pascal: procedure InsertMenu(theMenu: MenuHandle; beforeID: INTEGER);`<br>_InsertMenu ($A935) _InsertMenu ($A935): add a menu to the menu bar Pascal: procedure InsertMenu(theMenu: MenuHandle; beforeID: INTEGER); beforeID = 0 means append at end; negative = hierarchical subm... |
| **`INSERTMENU`** | `0x01220E` | `0x00CA26` | `menu_mgr.s:164` | **Proto:** `Pascal: procedure InsertMenu(theMenu: MenuHandle; beforeID: INTEGER);`<br>_InsertMenu ($A935): add a menu to the menu bar. Pascal: procedure InsertMenu(theMenu: MenuHandle; beforeID: INTEGER); beforeID = 0 means append at end. The SE delegates layout work (title metrics, la... |
| **`INSERTMENU_CONT`** | `0x01226E` | — | `menu_mgr.s:159` | — |
| **`INSERTMENU_CONT_2`** | `0x01228A` | `0x00CA7E` | `menu_mgr.s:177`<br>`menu_mgr.s:210` | INSERTMENU_CONT_2 Called during boot. |
| **`INSERTMENU_CONT_3`** | `0x012296` | `0x00CA8A` | `menu_mgr.s:183`<br>`menu_mgr.s:216` | — |
| **`INSERTMENU_EMPTY`** | `0x0122A8` | `0x00CA9C` | `menu_mgr.s:193`<br>`menu_mgr.s:226` | — |
| **`INSERTMENU_EXIT`** | `0x012284` | `0x00CA78` | `menu_mgr.s:167`<br>`menu_mgr.s:199` | — |
| **`INSERTMENU_FOUND`** | `0x012252` | — | `menu_mgr.s:149` | check if menu already in bar (by menuID) calculate title width for menu bar layout INSERTMENU_FOUND |
| **`INSERTMENU_FOUND_2`** | `0x0122AA` | `0x00CA9E` | `menu_mgr.s:195`<br>`menu_mgr.s:228` | — |
| **`INSERTMENU_NO`** | `0x012258` | `0x00CA52` | `menu_mgr.s:152`<br>`menu_mgr.s:184` | — |
| **`INSERTMENU_SHIFT_LOOP`** | — | `0x00CA50` | `menu_mgr.s:182` | Insertion point found: shift later entries down by one slot (6 bytes each). |
| **`INSERTMENU_SKIP`** | `0x012280` | `0x00CA74` | `menu_mgr.s:165`<br>`menu_mgr.s:197` | — |
| **`INSERTMENU_SKIP_2`** | `0x0122A4` | `0x00CA98` | `menu_mgr.s:190`<br>`menu_mgr.s:223` | — |
| **`INSERTMENU_STORE`** | — | `0x00CA64` | `menu_mgr.s:191` | Store new MenuHandle and dispatch MBDF "InsertMenu" message (#2). |
| **`InsertResMenu`** | `0x012C28` | — | `menu_mgr.s:1770` | **Proto:** `Pascal: PROCEDURE InsertResMenu(theMenu: MenuHandle; theType: ResType;`<br>(falls through) _InsertResMenu ($A951): insert the names of all resources of a type into a menu Pascal: PROCEDURE InsertResMenu(theMenu: MenuHandle; theType: ResType; afterItem: INTEGER); Apple source... |
| **`INSERTRESMENU_DONE`** | `0x012CEC` | `0x00D31A` | `menu_mgr.s:1865`<br>`menu_mgr.s:1515` | INSERTRESMENU_DONE Called during boot. INSERTRESMENU_DONE: done adding resources - recalculate menu size and clean up |
| **`INSERTRESMENU_EMPTY`** | `0x012CD8` | `0x00D306` | `menu_mgr.s:1852`<br>`menu_mgr.s:1509` | 'FOND' returned no resources -- try 'FONT' (legacy) as fallback. |
| **`INSERTRESMENU_NEXT`** | `0x012C6C` | `0x00D296` | `menu_mgr.s:1794`<br>`menu_mgr.s:1453` | loop through each resource of the type |
| **`INSERTRESMENU_NEXT_2`** | `0x012CA6` | — | `menu_mgr.s:1819` | find alphabetical insertion position for this resource name compare with the items from D6 up to the end of the menu |
| **`INSERTRESMENU_NO`** | `0x012C38` | `0x00D264` | `menu_mgr.s:1775`<br>`menu_mgr.s:1434` | — |
| **`INSERTRESMENU_OK`** | `0x012CC8` | `0x00D2F6` | `menu_mgr.s:1843`<br>`menu_mgr.s:1499` | INSERTRESMENU_OK - insert the resource name (the pending item) before item D6 Called during boot. |
| **`INSERTRESMENU_RETRY`** | `0x012C5C` | `0x00D288` | `menu_mgr.s:1786`<br>`menu_mgr.s:1445` | — |
| **`INSERTRESMENU_SKIP`** | `0x012CD2` | `0x00D300` | `menu_mgr.s:1848`<br>`menu_mgr.s:1504` | — |
| **`INSERTRESMENU_WALK_LOOP`** | — | `0x00D2D0` | `menu_mgr.s:1477` | Walk existing items to find alphabetical insertion point. |
| **`InsMenuItem`** | `0x012A22` | `0x00D04E` | `menu_mgr.s:1385` | **Proto:** `Pascal: PROCEDURE InsMenuItem(theMenu: MenuHandle; itemString: Str255;`<br>(falls through) _InsMenuItem ($A826): insert one or more items into a menu after a given item Pascal: PROCEDURE InsMenuItem(theMenu: MenuHandle; itemString: Str255; afterItem: INTEGER); Entry (after L... |
| **`INSMENUITEM`** | `0x012A22` | `0x00D04E` | `menu_mgr.s:1097` | **Proto:** `Pascal: procedure InsMenuItem(theMenu: MenuHandle; itemString: Str255; afterItem: INTEGER);`<br>_InsMenuItem ($A826): insert one or more items into a menu. Pascal: procedure InsMenuItem(theMenu: MenuHandle; itemString: Str255; afterItem: INTEGER); Parses metachars: ^=icon, /=key, !=mark, <=style... |
| **`INSMENUITEM_CONT`** | `0x012A44` | `0x00D070` | `menu_mgr.s:1407`<br>`menu_mgr.s:1114` | INSMENUITEM_CONT - parse an item string and insert its items into the menu Apple source name: AddString (System 7.1 MenuMgr.a) A4 = item string (Pascal), A3 = MenuHandle, D6 = insert-before item numbe... |
| **`INSMENUITEM_CONT_2`** | `0x012A71` | `0x00D09D` | `menu_mgr.s:1451`<br>`menu_mgr.s:1155` | INSMENUITEM_CONT_2 - style letters for '<' (Apple: STYLECHRTAB); index = style bit: 0='B' bold, 1='I' italic, 2='U' underline, 3='O' outline, 4='S' shadow |
| **`INSMENUITEM_CONT_3`** | `0x012A76` | `0x00D0A2` | `menu_mgr.s:1463`<br>`menu_mgr.s:1166` | INSMENUITEM_CONT_3 - process one item-string character (Apple: AppendChar) D0 = character, -0x114(A6) = parse state: State 0: metacharacter (INSMENUITEM_NO_3) or title text State 1 (after '^'): icon n... |
| **`INSMENUITEM_CONT_4`** | `0x012B12` | `0x00D13E` | `menu_mgr.s:1584`<br>`menu_mgr.s:1278` | INSMENUITEM_CONT_4 - insert the pending item before item D6 Apple source name: InsertTheItem (System 7.1 MenuMgr.a) Called during boot. D5 = min(D6, item count + 1) = number of the new item. If item D... |
| **`INSMENUITEM_CONT_5`** | `0x012B24` | `0x00D150` | `menu_mgr.s:1593`<br>`menu_mgr.s:1288` | Build splice buffer: title bytes + 4 attr bytes + length-prefix. |
| **`INSMENUITEM_CONT_6`** | `0x012B68` | `0x00D194` | `menu_mgr.s:1634`<br>`menu_mgr.s:1327` | INSMENUITEM_CONT_6 - insert an enable bit for new item D5 into enableFlags Apple source name: InsertEnableBit (System 7.1 MenuMgr.a) Called during boot. A0 = MenuInfo ptr. Bits 0..D5-1 stay, bits D5..... |
| **`INSMENUITEM_LOOP`** | `0x012A4C` | `0x00D078` | `menu_mgr.s:1412`<br>`menu_mgr.s:1119` | — |
| **`INSMENUITEM_LOOP_2`** | `0x012A90` | `0x00D0BC` | `menu_mgr.s:1474`<br>`menu_mgr.s:1177` | — |
| **`INSMENUITEM_LOOP_3`** | `0x012ABC` | `0x00D0E8` | `menu_mgr.s:1504`<br>`menu_mgr.s:1205` | — |
| **`INSMENUITEM_LOOP_4`** | `0x012B36` | `0x00D162` | `menu_mgr.s:1600`<br>`menu_mgr.s:1295` | — |
| **`INSMENUITEM_NEXT`** | `0x012A60` | `0x00D08C` | `menu_mgr.s:1432`<br>`menu_mgr.s:1137` | INSMENUITEM_NEXT - clear the pending-item state before the next item Apple source name: InitItem (System 7.1 MenuMgr.a) Called during boot. Clears the first 8 bytes of the item frame (InsMenuItem/Inse... |
| **`INSMENUITEM_NO`** | `0x012A88` | `0x00D0B4` | `menu_mgr.s:1470`<br>`menu_mgr.s:1173` | — |
| **`INSMENUITEM_NO_2`** | `0x012AA6` | `0x00D0D2` | `menu_mgr.s:1490`<br>`menu_mgr.s:1192` | INSMENUITEM_NO_2: attribute byte (state - 1) = D0, parse state = 0 (Apple: UPDATEPROP) |
| **`INSMENUITEM_NO_3`** | `0x012AB4` | `0x00D0E0` | `menu_mgr.s:1501`<br>`menu_mgr.s:1202` | INSMENUITEM_NO_3 - state 0: metacharacter or title text (Apple: NORMSTATE) Scans METACHAR_TBL from index 6 down; any other character is appended to the title buffer. |
| **`INSMENUITEM_NO_4`** | `0x012AE6` | `0x00D112` | `menu_mgr.s:1532`<br>`menu_mgr.s:1233` | INSMENUITEM_NO_4 - item separator (index 4-5) or disable marker (index 6) (Apple: CHECKTERM) |
| **`INSMENUITEM_NO_5`** | `0x012AF0` | `0x00D11C` | `menu_mgr.s:1545`<br>`menu_mgr.s:1244` | INSMENUITEM_NO_5 - insert the pending item (if it has title text) and clear the pending-item state. Apple source name: CloseItem (System 7.1 MenuMgr.a) Called during boot. Also used by InsertResMenu, ... |
| **`INSMENUITEM_NO_6`** | `0x012AFC` | `0x00D128` | `menu_mgr.s:1550`<br>`menu_mgr.s:1249` | — |
| **`INSMENUITEM_NO_7`** | `0x012B66` | `0x00D192` | `menu_mgr.s:1622`<br>`menu_mgr.s:1317` | — |
| **`INSMENUITEM_OK`** | `0x012A9C` | `0x00D0C8` | `menu_mgr.s:1484`<br>`menu_mgr.s:1187` | INSMENUITEM_OK - style letter D2 matched: OR bit D2 into the style byte (Apple: ADDTOSTYLE) |
| **`INSMENUITEM_OK_2`** | `0x012AD8` | `0x00D104` | `menu_mgr.s:1521`<br>`menu_mgr.s:1222` | INSMENUITEM_OK_2 - D0 is METACHAR_TBL entry D1 (Apple: SPECIALCHAR) Index 0-3 (^ / ! <): parse state = D1 + 1, the next char is the value Index 4 (CR) or 5 (;): end of item -> flush it (INSMENUITEM_NO... |
| **`INSMENUITEM_OK_3`** | `0x012B10` | `0x00D13C` | `menu_mgr.s:1571`<br>`menu_mgr.s:1269` | — |
| **`INSRTRESMENU`** | — | `0x00D254` | `menu_mgr.s:1430` | **Proto:** `Pascal: procedure InsertResMenu(theMenu: MenuHandle; theType: ResType; afterItem: INTEGER);`<br>_InsertResMenu ($A951): insert resources of a type into a menu at given position. Pascal: procedure InsertResMenu(theMenu: MenuHandle; theType: ResType; afterItem: INTEGER); Substitutes 'FOND' for 'FO... |
| **`INSWIN_AT_END`** | `0x011212` | `0x00B85A` | `window_mgr.s:128`<br>`window_mgr.s:138` | Insert at end of window list |
| **`INSWIN_HAS_LIST`** | `0x0111FE` | `0x00B846` | `window_mgr.s:119`<br>`window_mgr.s:130` | Insert window behind a specified window |
| **`InvalRect`** | `0x011FCE` | `0x00C684` | `window_mgr.s:2308` | _InvalRect ($A928) stack: rect -> (adds to update region) _InvalRect ($A928): add a rect to current window's updateRgn Converts rect to temp region, then calls InvalRgn/ValidRgn. Called during boot. |
| **`INVALRECT`** | `0x011FCE` | `0x00C684` | `window_mgr.s:2165` | **Proto:** `Pascal: procedure InvalRect(badRect: Rect); ValidRect(goodRect: Rect);`<br>_InvalRect ($A928) / _ValidRect ($A92A): add/remove a rect to/from updateRgn Pascal: procedure InvalRect(badRect: Rect); ValidRect(goodRect: Rect); |
| **`INVALRECT_CONT`** | `0x011FD0` | `0x00C686` | `window_mgr.s:2310`<br>`window_mgr.s:2167` | — |
| **`InvalRgn`** | `0x011F8E` | `0x00C63E` | `window_mgr.s:2261` | _InvalRgn ($A927) _InvalRgn ($A927): add a region to current window's updateRgn Converts region local->global, unions with updateRgn, converts back. INVALRGN_CONT entry: D0=0 for union (inval), D0=-1 ... |
| **`INVALRGN`** | `0x011F8E` | `0x00C63E` | `window_mgr.s:2123` | _InvalRgn ($A927): add a region to current window's updateRgn Converts region local->global, unions with updateRgn, converts back. INVALRGN_CONT entry: D0=0 for union (inval), D0=-1 for diff (valid). |
| **`INVALRGN_CONT`** | `0x011F90` | `0x00C640` | `window_mgr.s:2264`<br>`window_mgr.s:2125` | INVALRGN_CONT -- -> InvalRgn/ValidRgn core. |
| **`INVALRGN_CONT_2`** | `0x011FC0` | `0x00C676` | `window_mgr.s:2290`<br>`window_mgr.s:2152` | — |
| **`INVALRGN_EMPTY`** | `0x011FBE` | `0x00C674` | `window_mgr.s:2288`<br>`window_mgr.s:2150` | INVALRGN_EMPTY - ValidRgn path: subtract region from updateRgn Called during boot. |
| **`INVALRGN_EXIT`** | `0x011FC6` | `0x00C67C` | `window_mgr.s:2295`<br>`window_mgr.s:2156` | convert input region back to local coords |
| **`IsDialogEvent`** | `0x014B60` | `0x00F182` | `dialog_mgr.s:396` | _IsDialogEvent ($A97F) Called during boot (3,693 times in 30s trace). |
| **`ISDIALOGEVENT`** | `0x014B60` | `0x00F182` | `dialog_mgr.s:397` | _IsDialogEvent ($A97F) -- test if event is for a dialog window. Stack: eventPtr(L) -> isDialog(B). Returns true if event's window (or front window for non-window events) has windowKind = 2 (dialog), A... |
| **`ISDIALOGEVENT_CONT`** | `0x014B98` | `0x00F1BA` | `dialog_mgr.s:418`<br>`dialog_mgr.s:419` | — |
| **`ISDIALOGEVENT_NO`** | `0x014B92` | `0x00F1B4` | `dialog_mgr.s:414`<br>`dialog_mgr.s:415` | — |
| **`ISDIALOGEVENT_SKIP`** | `0x014B96` | `0x00F1B8` | `dialog_mgr.s:416`<br>`dialog_mgr.s:417` | — |
| **`JOURNAL_DISPATCH`** | `0x010F68` | `0x00B534` | `toolbox_event.s:76`<br>`toolbox_event.s:73` | JOURNAL_DISPATCH - Journaling dispatcher Shared by GetKeys, Button, TickCount, GetMouse, and event routines. If JournalFlag < 0: playback mode (jPlayCtl = 16), reads result from journal driver. If Jou... |
| **`JRNL_CONTROL`** | `0x010F76` | `0x00B542` | `toolbox_event.s:85`<br>`toolbox_event.s:81` | — |
| **`JRNL_DISABLE`** | `0x010F96` | `0x00B562` | `toolbox_event.s:100`<br>`toolbox_event.s:95` | Journal driver returned an error - disable journaling |
| **`JRNL_RECORD`** | `0x010F74` | `0x00B540` | `toolbox_event.s:83`<br>`toolbox_event.s:79` | — |
| **`JRNL_RTS`** | `0x010F9E` | `0x00B56A` | `toolbox_event.s:103`<br>`toolbox_event.s:98` | — |
| **`KillControls`** | `0x012EBA` | `0x00D4BE` | `control_mgr.s:202` | _KillControls ($A956) Called during boot. _KillControls: dispose all controls in a window |
| **`KILLCONTROLS`** | `0x012EBA` | `0x00D4BE` | `control_mgr.s:180` | **Proto:** `Pascal: procedure KillControls(theWindow: WindowPtr);`<br>_KillControls ($A956): dispose all controls in a window. Pascal: procedure KillControls(theWindow: WindowPtr); |
| **`KILLCONTROLS_EMPTY`** | `0x012EC0` | `0x00D4C4` | `control_mgr.s:205`<br>`control_mgr.s:183` | — |
| **`LoadResource`** | `0x0143CC` | `0x00E9E8` | `resource_mgr.s:2776` | _LoadResource ($A9A2) stack: handle -> (loads resource data) Called during boot (28,906 times in 30s trace). |
| **`LOADRESOURCE`** | `0x0143CC` | `0x00E9E8` | `resource_mgr.s:2668` | _LoadResource ($A9A2) -- load (or reload) a resource into memory. Stack: handle(L) -> (no result; ResErr indicates error). For cached handles already populated, no-op. Otherwise locates the ref entry ... |
| **`LOADRESOURCE_EXIT`** | `0x014402` | `0x00EA1E` | `resource_mgr.s:2806`<br>`resource_mgr.s:2687` | LOADRESOURCE_EXIT - LoadResource cleanup epilogue Called during boot (28,906 times in 30s trace). |
| **`LOADRESOURCE_FOUND`** | `0x0143EE` | `0x00EA0A` | `resource_mgr.s:2793`<br>`resource_mgr.s:2679` | LOADRESOURCE_FOUND - force-load resource data from file Called during boot. |
| **`LOADRESOURCE_SKIP`** | `0x0143FE` | — | `resource_mgr.s:2798` | — |
| **`LOADSCRAP`** | — | `0x0126A4` | `scrap_mgr.s:140` | — |
| **`LOC_C72E`** | — | `0x00C72E` | `window_mgr.s:2252` | — |
| **`LOC_E1FE`** | — | `0x00E1FE` | `resource_mgr.s:1259` | — |
| **`LodeScrap`** | `0x016E5A` | — | `scrap_mgr.s:165` | **Proto:** `_LoadScrap ($A9FB) - FUNCTION LoadScrap: LongInt`<br>_LoadScrap ($A9FB) - FUNCTION LoadScrap: LongInt Reads the Clipboard File from disk into a newly allocated memory handle. If scrap is already in memory (ScrapState > 0), does nothing. After loading, s... |
| **`Long2Fix`** | `0x015BCC` | `0x010208` | `fixmath.s:951` | **Proto:** `Pascal: FUNCTION Long2Fix(x: LONGINT): Fixed;`<br>**Regs:** `Entry: 4(SP) = x, 8(SP) = result slot (no frame; uses D0-D1/A0) Exit:  result = x shifted left 16 (ASL); $7FFFFFFF / $80000000 (by the`<br>_Long2Fix ($A83F): convert LongInt to Fixed (16.16) Pascal: FUNCTION Long2Fix(x: LONGINT): Fixed; Entry: 4(SP) = x, 8(SP) = result slot (no frame; uses D0-D1/A0) Exit:  result = x shifted left 16 (ASL... |
| **`LONG2FIX`** | `0x015BCC` | `0x010208` | `fixmath.s:716` | _Long2Fix ($A83F) - convert LongInt to Fixed (16.16) Left-shifts by 16 to place integer in high word. Clamps on overflow to $7FFFFFFF or $80000000. |
| **`LONG2FIX_SHIFT`** | `0x015BD2` | `0x01020E` | `fixmath.s:964`<br>`fixmath.s:726` | — |
| **`LongMul`** | `0x0157B2` | `0x00FDF4` | `fixmath.s:43` | **Proto:** `Pascal: PROCEDURE LongMul(a, b: LONGINT; VAR dest: Int64Bit);`<br>**Regs:** `Entry: after FIXPT_ENTRY, a = $10(A6), b = $0C(A6), @dest = $08(A6) Exit:  dest.hiLong:dest.loLong = a*b; 12 bytes of parameters removed;`<br>Toolbox Utilities: fixed-point arithmetic This file contains, in ROM order: - _LongMul, _FracMul, _FixMul and their shared 32 x 32-bit multiply - _FracDiv, _FixDiv (shared shift-and-subtract division)... |
| **`LONGMUL`** | `0x0157B2` | `0x00FDF4` | `fixmath.s:37` | Toolbox Utilities: fixed-point arithmetic This file contains, in ROM order: - _LongMul, _FracMul, _FixMul and their shared 32 x 32-bit multiply - _FracDiv, _FixDiv (shared shift-and-subtract division)... |
| **`LONGMUL_EXIT`** | `0x0157C4` | `0x00FE06` | `fixmath.s:54`<br>`fixmath.s:47` | LONGMUL_EXIT - LongMul epilogue: apply sign to 64-bit result and store hi:lo result at caller's pointer. |
| **`LONGMUL_NO`** | `0x0157CC` | `0x00FE0E` | `fixmath.s:59`<br>`fixmath.s:52` | — |
| **`LoWord`** | `0x015974` | `0x00FFBC` | `fixmath.s:444` | **Proto:** `Pascal: FUNCTION LoWord(x: LONGINT): INTEGER;`<br>**Regs:** `Entry: 4(SP) = x, 8(SP) = INTEGER result slot (no frame, no registers) Exit:  result = bits 15..0 of x; x removed from the stack`<br>_LoWord ($A86B): low-order word of a long integer Pascal: FUNCTION LoWord(x: LONGINT): INTEGER; Entry: 4(SP) = x, 8(SP) = INTEGER result slot (no frame, no registers) Exit:  result = bits 15..0 of x; ... |
| **`LOWORD`** | `0x015974` | `0x00FFBC` | `fixmath.s:352` | _LoWord ($A86B) - Extract low word of long. Stack: value(+$04 long). Returns word in result position. |
| **`MAP_PACK_INDEXED`** | `0x016FE4` | `0x01A052` | `package_mgr.s:82`<br>`package_mgr.s:79` | — |
| **`MAP_PACK_SLOT`** | `0x016FD6` | `0x01A044` | `package_mgr.s:76`<br>`package_mgr.s:73` | **Regs:** `Entry: D0.W = pack number (0-15) Exit: A0 = pointer to handle slot in AppPacks or App2Packs`<br>MAP_PACK_SLOT - Map pack number to AppPacks/App2Packs slot Entry: D0.W = pack number (0-15) Exit: A0 = pointer to handle slot in AppPacks or App2Packs D0.W modified (0-7 range within chosen array) |
| **`MAXLOAD`** | `0x0138FA` | — | `resource_mgr.s:876` | MAXLOAD - MaxLoad: calculate compaction buffer size Computes ideal buffer size for resource compaction. Uses the larger of the resource fork size (CHECKLOAD_CONT_12) and the largest free block (_MaxBl... |
| **`MAXLOAD_CMP`** | `0x013908` | — | `resource_mgr.s:884` | MAXLOAD_CMP -- pick larger of D0 and D3. |
| **`MAXLOAD_RET`** | `0x01390E` | — | `resource_mgr.s:888` | — |
| **`MaxSizeRsrc`** | `0x014886` | `0x00EEA8` | `resource_mgr.s:3510` | **Proto:** `Pascal: FUNCTION MaxSizeRsrc(theResource: Handle): LONGINT;`<br>**Regs:** `Entry: 4(SP).L = theResource, 8(SP).L = space for the function result Exit:  function result = size, or -1 with ResErr = resNotFound if`<br>_MaxSizeRsrc ($A821): size of a resource without reading the disk (Mac Plus addition, Inside Macintosh IV) Pascal: FUNCTION MaxSizeRsrc(theResource: Handle): LONGINT; Entry: 4(SP).L = theResource, 8(S... |
| **`MAXSIZERSRC`** | `0x014886` | `0x00EEA8` | `resource_mgr.s:3339` | _MaxSizeRsrc ($A821) -- maximum size resource could grow to in place. Stack: handle(L) -> size(L). If loaded, returns current handle size. If purged, returns the available slot size (data offset gap t... |
| **`MAXSIZERSRC_CONT`** | `0x014898` | `0x00EEBA` | `resource_mgr.s:3524`<br>`resource_mgr.s:3352` | — |
| **`MAXSIZERSRC_OK`** | `0x014894` | `0x00EEB6` | `resource_mgr.s:3521`<br>`resource_mgr.s:3349` | MAXSIZERSRC_OK - resource loaded: return actual handle size |
| **`MBDF_HILITE_DISPATCH`** | — | `0x00CB9C` | `menu_mgr.s:401` | — |
| **`MBDF_HILITE_OFFSET`** | — | `0x00CB9A` | `menu_mgr.s:399` | — |
| **`MBDF_SHOW_MENU`** | — | `0x00CCD0` | `menu_mgr.s:547` | MBDF msg #7 dispatch: show menu (compute rect, save bits, draw frame). In: D4 = byte offset of menu Out: -8(A6)..-1(A6) = menu rect; MDEF msg #0 (draw items) called inside |
| **`MBDF_UNHILITE_OFFSET`** | — | `0x00CB96` | `menu_mgr.s:396` | MBDF hilite helpers: dispatch msg #5 (hilite/unhilite) given an offset in D0. In:  D0 = byte offset of menu in MenuList header MBDF_UNHILITE_OFFSET unhilites (flag=0); MBDF_HILITE_OFFSET hilites (flag... |
| **`MDEF_CLEANUP_STRIP12`** | — | `0x00CD20` | `menu_mgr.s:586` | MDEF cleanup stub: strip 12 bytes of MDEF args and return to outer caller. |
| **`MDEF_UNLOCK`** | — | `0x00CD28` | `menu_mgr.s:593` | Unlock MDEF code after dispatch (paired with MENUSELECT_CONT_8). |
| **`MENU_CALL_MBDF`** | — | `0x00CE1E` | `menu_mgr.s:752` | MBDF dispatch helper (SE FDHD-specific). Builds an MBDF stack frame, loads the 'MBDF' resource, locks it, calls its code, unlocks, and returns the MBDF result in D0. In:  D0 = MBDF message number, D1 ... |
| **`MenuKey`** | `0x0128E4` | `0x00CF10` | `menu_mgr.s:1175` | **Proto:** `Pascal: function MenuKey(ch: CHAR): LongInt; (high=menuID, low=item)`<br>_MenuKey ($A93E) _MenuKey ($A93E): find menu item matching a Command-key equivalent Pascal: function MenuKey(ch: CHAR): LongInt; (high=menuID, low=item) |
| **`MENUKEY`** | `0x0128E4` | `0x00CF10` | `menu_mgr.s:925` | **Proto:** `Pascal: function MenuKey(ch: CHAR): LongInt;`<br>_MenuKey ($A93E): map a Cmd-key character to a menuID:item LongInt. Pascal: function MenuKey(ch: CHAR): LongInt; Returns: high word = menuID, low word = item index, 0L if no match. Walks all menus tha... |
| **`MENUKEY_DONE`** | `0x01292E` | `0x00CF5A` | `menu_mgr.s:1214`<br>`menu_mgr.s:960` | Common exit: restore regs, strip char param, indirect return. |
| **`MENUKEY_FOUND`** | `0x012936` | — | `menu_mgr.s:1222` | MENUKEY_FOUND: key match found - hilite menu and return menuID:item |
| **`MENUKEY_MATCH_FOUND`** | — | `0x00CF62` | `menu_mgr.s:964` | Match found: hilite the menu, build result LongInt, dispatch system menu if needed. |
| **`MENUKEY_NEXT`** | `0x0128F6` | — | `menu_mgr.s:1183` | scan each menu for matching key equivalent |
| **`MENUKEY_NEXT_2`** | `0x012906` | `0x00CF32` | `menu_mgr.s:1190`<br>`menu_mgr.s:940` | scan items in this menu |
| **`MENUKEY_OK`** | `0x012956` | `0x00CF82` | `menu_mgr.s:1235`<br>`menu_mgr.s:977` | — |
| **`MENUKEY_SCAN_LOOP`** | — | `0x00CF22` | `menu_mgr.s:933` | Scan each menu in the bar. |
| **`MENUKEY_SKIP`** | `0x012922` | `0x00CF4E` | `menu_mgr.s:1202`<br>`menu_mgr.s:952` | — |
| **`MENUKEY_SKIP_2`** | `0x012926` | `0x00CF52` | `menu_mgr.s:1210`<br>`menu_mgr.s:955` | MENUKEY_SKIP_2 |
| **`MENUMGR_CONT`** | `0x012862` | `0x00CE8E` | `menu_mgr.s:1060`<br>`menu_mgr.s:826` | MENUMGR_CONT Called during boot (22,164 times in 30s trace). Set item attribute: stack = [ret, value.B, pad, item#, MenuHandle] D2 = attribute index (0=icon, 1=key, 2=mark, 3=style) |
| **`MENUMGR_CONT_2`** | `0x012888` | `0x00CEB4` | `menu_mgr.s:1083`<br>`menu_mgr.s:847` | MENUMGR_CONT_2 Get item attribute: stack = [ret, resultPtr, item#, pad, MenuHandle] D2 = attribute index (0=icon, 1=key, 2=mark, 3=style) Returns attribute byte at resultPtr+1 (as VAR INTEGER, high by... |
| **`MENUMGR_FOUND`** | `0x01284C` | `0x00CE78` | `menu_mgr.s:1031`<br>`menu_mgr.s:801` | item not found: return nil |
| **`MENUMGR_NEXT`** | `0x01283E` | `0x00CE6A` | `menu_mgr.s:1022`<br>`menu_mgr.s:792` | walk through items to find the Nth one |
| **`MENUMGR_NO`** | `0x0128A4` | `0x00CED0` | `menu_mgr.s:1093`<br>`menu_mgr.s:859` | Common exit for MENUMGR_CONT_2 / GetMenuItemText / InsMenuItem etc. Called by: MENUMGR_CONT_2, GETMENUITEMTEXT_CONT, INSMENUITEM, SETMENUITEMTEXT_FOUND, INSERTRESMENU_DONE |
| **`MENUMGR_SKIP`** | `0x012882` | `0x00CEAE` | `menu_mgr.s:1071`<br>`menu_mgr.s:837` | — |
| **`MENUMGR_STRIP_PARAM_RTS`** | — | `0x00CADE` | `menu_mgr.s:261` | Called by: DELETEMENU, HILITEMENU_RESTORE_VISRGN, MENUKEY_DONE, GETMHANDLE_RTS, SETMENUFLASH |
| **`MenuSelect`** | `0x01246E` | `0x00CBAA` | `menu_mgr.s:492` | _MenuSelect ($A93D) stack: startPt -> stack: menuResult (menu ID + item) _MenuSelect ($A93D): track mouse through menus until button released Returns: menuResult = menuID<<16 \| itemNumber (0 if no sel... |
| **`MENUSELECT`** | `0x01246E` | `0x00CBAA` | `menu_mgr.s:414` | **Proto:** `Pascal: function MenuSelect(startPt: Point): LongInt;`<br>_MenuSelect ($A93D): track mouse through the menu bar and into a menu. Pascal: function MenuSelect(startPt: Point): LongInt; Returns: high word = chosen menuID (0 if none), low word = item index Stack... |
| **`MENUSELECT_AFTER_HOOK`** | — | `0x00CC70` | `menu_mgr.s:495` | — |
| **`MENUSELECT_CONT`** | `0x0124BC` | — | `menu_mgr.s:528` | — |
| **`MENUSELECT_CONT_10`** | `0x012734` | `0x00CD2C` | `menu_mgr.s:852`<br>`menu_mgr.s:595` | MENUSELECT_CONT_10 -- store computed width/height in MenuInfo. |
| **`MENUSELECT_CONT_11`** | `0x012742` | `0x00CD38` | `menu_mgr.s:865`<br>`menu_mgr.s:608` | MENUSELECT_CONT_11 Called during boot. |
| **`MENUSELECT_CONT_2`** | `0x0125D0` | `0x00CCB0` | `menu_mgr.s:651`<br>`menu_mgr.s:526` | MENUSELECT_CONT_2 - system menu selected: dispatch to Desk Manager |
| **`MENUSELECT_CONT_3`** | `0x0125DC` | — | `menu_mgr.s:662` | MENUSELECT_CONT_3 Called during boot. |
| **`MENUSELECT_CONT_4`** | `0x012622` | — | `menu_mgr.s:699` | MENUSELECT_CONT_4 Called during boot. |
| **`MENUSELECT_CONT_5`** | `0x01263E` | `0x00CCBC` | `menu_mgr.s:723`<br>`menu_mgr.s:535` | MENUSELECT_CONT_5 Called during boot. |
| **`MENUSELECT_CONT_6`** | `0x01269A` | — | `menu_mgr.s:756` | compute offscreen bitmap size for saving menu area |
| **`MENUSELECT_CONT_7`** | `0x0126E8` | — | `menu_mgr.s:799` | MENUSELECT_CONT_7 Called during boot. |
| **`MENUSELECT_CONT_8`** | `0x012710` | `0x00CD0A` | `menu_mgr.s:823`<br>`menu_mgr.s:574` | MENUSELECT_CONT_8 Called during boot (28,795 times in 30s trace). |
| **`MENUSELECT_CONT_9`** | `0x012730` | — | `menu_mgr.s:849` | MENUSELECT_CONT_9 Called during boot (28,789 times in 30s trace). |
| **`MENUSELECT_EMPTY`** | `0x0126E2` | — | `menu_mgr.s:790` | draw menu frame: 3 lines forming right and bottom edges + shadow draw menu items via MDEF |
| **`MENUSELECT_EMPTY_2`** | `0x012726` | `0x00CD1E` | `menu_mgr.s:832`<br>`menu_mgr.s:583` | — |
| **`MENUSELECT_EMPTY_3`** | `0x012740` | `0x00CD36` | `menu_mgr.s:857`<br>`menu_mgr.s:600` | — |
| **`MENUSELECT_ERR`** | `0x012634` | — | `menu_mgr.s:713` | MENUSELECT_ERR |
| **`MENUSELECT_EXIT`** | `0x0125B2` | `0x00CC90` | `menu_mgr.s:633`<br>`menu_mgr.s:510` | — |
| **`MENUSELECT_EXIT_2`** | `0x0125C0` | — | `menu_mgr.s:638` | — |
| **`MENUSELECT_EXIT_3`** | `0x012728` | — | `menu_mgr.s:839` | MENUSELECT_EXIT_3 |
| **`MENUSELECT_FLASH_SPIN`** | — | `0x00CD8C` | `menu_mgr.s:652` | — |
| **`MENUSELECT_FOUND`** | `0x0124C6` | — | `menu_mgr.s:533` | — |
| **`MENUSELECT_LOOP`** | `0x0124A2` | — | `menu_mgr.s:516` | MENUSELECT_LOOP Called during boot (28,780 times in 30s trace). |
| **`MENUSELECT_LOOP_2`** | `0x0124B0` | — | `menu_mgr.s:522` | — |
| **`MENUSELECT_LOOP_3`** | `0x012758` | `0x00CD4E` | `menu_mgr.s:873`<br>`menu_mgr.s:616` | — |
| **`MENUSELECT_NO`** | `0x0124DE` | `0x00CC06` | `menu_mgr.s:542`<br>`menu_mgr.s:449` | — |
| **`MENUSELECT_NO_2`** | `0x01254A` | — | `menu_mgr.s:583` | — |
| **`MENUSELECT_NO_3`** | `0x01257A` | `0x00CC56` | `menu_mgr.s:601`<br>`menu_mgr.s:482` | Track-mouse loop tail: wait for next event, refresh mouse, run hook, repeat. |
| **`MENUSELECT_NO_4`** | `0x012594` | — | `menu_mgr.s:614` | — |
| **`MENUSELECT_NO_5`** | `0x012598` | `0x00CC74` | `menu_mgr.s:622`<br>`menu_mgr.s:498` | MENUSELECT_NO_5 Called during boot. |
| **`MENUSELECT_NO_6`** | `0x0125A2` | `0x00CC7E` | `menu_mgr.s:627`<br>`menu_mgr.s:503` | — |
| **`MENUSELECT_NO_7`** | `0x0125C6` | `0x00CCA4` | `menu_mgr.s:641`<br>`menu_mgr.s:519` | Final exit: pop locals, strip mousePt param, leave result on stack. |
| **`MENUSELECT_NORMAL_COMMIT`** | — | `0x00CC9E` | `menu_mgr.s:515` | — |
| **`MENUSELECT_OK`** | `0x0124FA` | — | `menu_mgr.s:554` | — |
| **`MENUSELECT_OK_2`** | `0x01251A` | — | `menu_mgr.s:565` | — |
| **`MENUSELECT_OK_3`** | `0x012600` | — | `menu_mgr.s:679` | MENUSELECT_OK_3 |
| **`MENUSELECT_SHOW`** | — | `0x00CC26` | `menu_mgr.s:463` | — |
| **`MENUSELECT_SKIP`** | `0x01254E` | `0x00CC2A` | `menu_mgr.s:585`<br>`menu_mgr.s:465` | — |
| **`MENUSELECT_SKIP_2`** | `0x012550` | `0x00CC2C` | `menu_mgr.s:587`<br>`menu_mgr.s:467` | — |
| **`MENUSELECT_SKIP_3`** | `0x012766` | `0x00CD5C` | `menu_mgr.s:881`<br>`menu_mgr.s:624` | — |
| **`MENUSELECT_TRACK_LOOP`** | — | `0x00CBD6` | `menu_mgr.s:432` | Main tracking loop: ask MBDF which menu (if any) the mouse is over, switch hilite if the mouse moved between titles, then track item. |
| **`MergeAdjacentRuns`** | — | `0x01244E` | `textedit.s:4051` | MergeAdjacentRuns -- merge adjacent styleRuns with identical styleIndex Walks the styleRun array compacting adjacent runs that share a styleIndex. For each removed run, decrements that styleIndex's st... |
| **`MergeAdjacentRuns_COPY`** | — | `0x01248A` | `textedit.s:4075` | — |
| **`MergeAdjacentRuns_DONE`** | — | `0x012494` | `textedit.s:4080` | — |
| **`MergeAdjacentRuns_LOOP`** | — | `0x01246E` | `textedit.s:4063` | — |
| **`METACHAR_TBL`** | `0x012A6A` | `0x00D096` | `menu_mgr.s:1445`<br>`menu_mgr.s:1149` | METACHAR_TBL - AppendMenu metacharacters (Apple: MCHARTABLE) Index 0 '^' icon, 1 '/' key equivalent, 2 '!' mark, 3 '<' style: the next character is the value (parse state = index + 1); 4 CR and 5 ';' ... |
| **`MethodDispatch`** | `0x015760` | `0x00FD98` | `toolbox_utils.s:435` | **Regs:** `Entry: (SP) = address of the method's selector table (the trap's return`<br>_MethodDispatch ($A9F8): MacApp (Object Pascal) method dispatcher Nonstandard stack interface (Apple Munger.a, from MacApp's Method.TEXT): Entry: (SP) = address of the method's selector table (the tra... |
| **`METHODDISPATCH`** | `0x015760` | `0x00FD98` | `toolbox_utils.s:357` | StdOpcodeProc / METHODDISPATCH - MacApp opcode dispatcher. Looks up an opcode in a dispatch table, caches result, and jumps to the handler. Uses MASuperTab for inheritance. |
| **`METHODDISPATCH_CONT`** | `0x015770` | `0x00FDA8` | `toolbox_utils.s:443`<br>`toolbox_utils.s:365` | — |
| **`METHODDISPATCH_CONT_2`** | `0x01577E` | — | `toolbox_utils.s:452` | METHODDISPATCH_CONT_2 - Jump to handler via A5-relative offset (JT entry). |
| **`METHODDISPATCH_FOUND`** | `0x0157A8` | `0x00FDEA` | `toolbox_utils.s:480`<br>`toolbox_utils.s:403` | METHODDISPATCH_FOUND - Found handler: cache offset and dispatch. |
| **`METHODDISPATCH_LOOP`** | `0x01578C` | `0x00FDBE` | `toolbox_utils.s:464`<br>`toolbox_utils.s:380` | First loop: scan dispatch table for current class ID |
| **`METHODDISPATCH_NO`** | `0x015782` | — | `toolbox_utils.s:459` | METHODDISPATCH_NO - Cache miss: search dispatch table for matching class. Walks the class inheritance chain via MASuperTab. |
| **`METHODDISPATCH_RETRY`** | `0x01578E` | `0x00FDD2` | `toolbox_utils.s:466`<br>`toolbox_utils.s:391` | — |
| **`MISCMGR`** | — | `0x00B4FC` | `toolbox_event.s:25` | **Proto:** `Pascal: PROCEDURE GetKeys(VAR theKeys: KeyMap)`<br>Toolbox Event Manager Apple source: ToolboxEventMgr.a (MacSEROM.lst module MISCMGR): GetKeys, Button, TickCount, GetMouse, StillDown, WaitMouseUp, EventAvail and GetNextEvent with the event filtering ... |
| **`MMGR`** | — | `0x00C94A` | `menu_mgr.s:32` | **Proto:** `Pascal: procedure InitProcMenu(resID: INTEGER);`<br>Menu Manager Apple source: MenuMgr.a (MacSEROM.lst module MMGR). In ROM order: InitProcMenu ($A808, SE: InitMenus with a given MBDF), InitMenus, ClearMenuBar, InsertMenu, DeleteMenu, DrawMenuBar, Hili... |
| **`MMGREND`** | — | `0x00D382` | `menu_mgr.s:1578` | **Proto:** `Pascal: function NewControl(theWindow: WindowPtr; boundsRect: Rect;`<br>Control Manager begins here. Boundary: $0xD3F8 (MMGREND = NEWCONTROL). _NewControl ($A954): allocate and initialize a Control record. Pascal: function NewControl(theWindow: WindowPtr; boundsRect: Rect... |
| **`ModalDialog`** | `0x014BDA` | `0x00F1FC` | `dialog_mgr.s:456` | _ModalDialog ($A991) Called during boot. |
| **`MODALDIALOG`** | `0x014BDA` | `0x00F1FC` | `dialog_mgr.s:460` | _ModalDialog ($A991) -- run a modal dialog event loop. Stack: filterProc(L), itemHit(L). Loops calling SystemTask, TEIdle, GetNextEvent. Calls user filterProc first if non-nil; if it returns true, exi... |
| **`MODALDIALOG_CONT`** | `0x014C0A` | `0x00F22C` | `dialog_mgr.s:476`<br>`dialog_mgr.s:480` | — |
| **`MODALDIALOG_CONT_2`** | `0x014C3E` | `0x00F260` | `dialog_mgr.s:498`<br>`dialog_mgr.s:502` | — |
| **`MODALDIALOG_CONT_3`** | `0x014C50` | `0x00F272` | `dialog_mgr.s:519`<br>`dialog_mgr.s:523` | MODALDIALOG_CONT_3 Called during boot (3,696 times in 30s trace). |
| **`MODALDIALOG_CONT_4`** | `0x014C5C` | `0x00F27E` | `dialog_mgr.s:530`<br>`dialog_mgr.s:535` | MODALDIALOG_CONT_4 - Dialog Manager common epilogue Called during boot (3,696 times in 30s trace). |
| **`MODALDIALOG_EXIT`** | `0x014C3C` | `0x00F25E` | `dialog_mgr.s:496`<br>`dialog_mgr.s:500` | — |
| **`MODALDIALOG_NEXT`** | `0x014BDE` | `0x00F200` | `dialog_mgr.s:458`<br>`dialog_mgr.s:462` | _ModalDialog ($A991) Called during boot. |
| **`MODALDIALOG_NO`** | `0x014C40` | `0x00F262` | `dialog_mgr.s:506`<br>`dialog_mgr.s:509` | MODALDIALOG_NO Called during boot. |
| **`MODALDIALOG_SKIP`** | `0x014BF2` | `0x00F214` | `dialog_mgr.s:467`<br>`dialog_mgr.s:471` | — |
| **`MoveControl`** | `0x012F0E` | `0x00D512` | `control_mgr.s:273` | **Proto:** `Pascal: procedure MoveControl(theControl: ControlHandle; h, v: INTEGER);`<br>_MoveControl ($A959) Called during boot. _MoveControl: move control to new position (h,v) Pascal: procedure MoveControl(theControl: ControlHandle; h, v: INTEGER); |
| **`MOVECONTROL`** | `0x012F0E` | `0x00D512` | `control_mgr.s:236` | **Proto:** `Pascal: procedure MoveControl(theControl: ControlHandle; h, v: INTEGER);`<br>_MoveControl ($A959): move a control to absolute (h,v) in window coords. Pascal: procedure MoveControl(theControl: ControlHandle; h, v: INTEGER); |
| **`MOVECONTROL_CONT`** | `0x012F46` | `0x00D54A` | `control_mgr.s:297`<br>`control_mgr.s:261` | — |
| **`MOVECONTROL_OK`** | `0x012F3A` | `0x00D53E` | `control_mgr.s:290`<br>`control_mgr.s:254` | Common tail: re-show if was visible, clean up frame. |
| **`MOVECONTROL_SKIP`** | `0x012F42` | `0x00D546` | `control_mgr.s:295`<br>`control_mgr.s:259` | — |
| **`MoveWindow`** | `0x011974` | `0x00BFE6` | `window_mgr.s:1312` | **Proto:** `Pascal: procedure MoveWindow(theWindow: WindowPtr; hGlobal, vGlobal: INTEGER;`<br>_MoveWindow ($A91B) stack: window, h, v, front -> (repositions) _MoveWindow ($A91B): move a window to a new screen position Pascal: procedure MoveWindow(theWindow: WindowPtr; hGlobal, vGlobal: INTEGER... |
| **`MOVEWINDOW`** | `0x011974` | `0x00BFE6` | `window_mgr.s:1224` | **Proto:** `Pascal: procedure MoveWindow(theWindow: WindowPtr; hGlobal,vGlobal: INTEGER;`<br>_MoveWindow ($A91B): move a window to a new screen position Pascal: procedure MoveWindow(theWindow: WindowPtr; hGlobal,vGlobal: INTEGER; front: BOOLEAN); Optimizes by using CopyBits to blit existing p... |
| **`MOVEWINDOW_CALCRGNS`** | — | `0x00C0FE` | `window_mgr.s:1362` | — |
| **`MOVEWINDOW_CONT`** | `0x011A46` | `0x00C0B8` | `window_mgr.s:1415`<br>`window_mgr.s:1320` | WDEF not in memory: load it |
| **`MOVEWINDOW_CONT_2`** | `0x011A5A` | `0x00C0CC` | `window_mgr.s:1430`<br>`window_mgr.s:1334` | MOVEWINDOW_CONT_2 - send wDraw message to WDEF (draw window frame) Preserves D3 since wDraw doesn't need a param. Called during boot. |
| **`MOVEWINDOW_EMPTY`** | `0x011A68` | `0x00C0DA` | `window_mgr.s:1445`<br>`window_mgr.s:1349` | MOVEWINDOW_EMPTY - recalculate window regions or set them empty if invisible If visible, sends wCalcRgns to WDEF to recompute strucRgn/contRgn. If invisible, sets strucRgn, contRgn, and visRgn to empt... |
| **`MOVEWINDOW_INVIS_EMPTY`** | — | `0x00C10A` | `window_mgr.s:1368` | invisible: empty all regions |
| **`MOVEWINDOW_OK`** | `0x011A20` | `0x00C092` | `window_mgr.s:1398`<br>`window_mgr.s:1303` | MOVEWINDOW_OK - call WDEF procedure for window A3 Dispatches to the window definition function. Parameters: D0 = message (wDraw=0, wHit=1, wCalcRgns=2, wNew=3, wDispose=4, wGrow=5) D3 = param (message... |
| **`MOVEWINDOW_SKIP`** | `0x0119BA` | `0x00C02C` | `window_mgr.s:1342`<br>`window_mgr.s:1251` | compute visible portion of old strucRgn (for CopyBits optimization) move window regions to new position offset the visible-old-area region to new position optionally bring to front CopyBits to blit wi... |
| **`MOVEWINDOW_SKIP_2`** | `0x0119F8` | `0x00C06A` | `window_mgr.s:1369`<br>`window_mgr.s:1275` | compute newly exposed area at new position repaint windows behind at old position optionally select (bring to front) |
| **`Munger`** | `0x015588` | `0x00FBB6` | `toolbox_utils.s:32` | **Proto:** `Pascal: FUNCTION Munger(h: Handle; offset: LONGINT; ptr1: Ptr; len1: LONGINT;`<br>**Regs:** `Entry: after LINK, h = $1C(A6), offset = $18(A6), ptr1 = $14(A6), Exit:  result = offset just past the replacement/insertion; the match`<br>Toolbox Utilities: byte-string munger, handle/pointer copying and MacApp method dispatch Routines, in physical ROM order: _Munger ($A9E0), _XMunger ($A819)  search/replace/insert/delete bytes in a han... |
| **`MUNGER`** | `0x015588` | `0x00FBB6` | `toolbox_utils.s:28` | Toolbox Utilities: byte-string munger, handle/pointer copying and MacApp method dispatch Routines, in physical ROM order: _Munger ($A9E0), _XMunger ($A819)  search/replace/insert/delete bytes in a han... |
| **`MUNGER_CONT`** | `0x0155AA` | `0x00FBD8` | `toolbox_utils.s:46`<br>`toolbox_utils.s:40` | MUNGER_CONT -- shared exit of Munger/XMunger (Apple: mungeBye); D1 = number of parameter bytes to remove |
| **`MungerResizeIfDiff`** | — | `0x00FC76` | `toolbox_utils.s:148` | **Regs:** `Entry: D0 = desired new size. Uses -8(A6) = original size,`<br>MungerResizeIfDiff - Resize handle if new size differs from original. Entry: D0 = desired new size. Uses -8(A6) = original size, -4(A6) = slack tolerance. Only resizes if change exceeds slack. |
| **`NEWALERT_LOAD_RES`** | — | `0x00F396` | `dialog_mgr.s:734` | — |
| **`NewControl`** | `0x012D54` | `0x00D382` | `control_mgr.s:26` | **Proto:** `Pascal: function NewControl(theWindow: WindowPtr; boundsRect: Rect;`<br>Control Manager Apple source: ControlMgr.a (MacSEROM.lst module CMGR). The Control Manager traps with their local helpers, in physical ROM order: NewControl, DisposControl, KillControls, Draw1Control,... |
| **`NEWCONTROL`** | `0x012D54` | `0x00D382` | `control_mgr.s:19` | Control Manager Apple source: ControlMgr.a (MacSEROM.lst module CMGR). The Control Manager traps with their local helpers, in physical ROM order: NewControl, DisposControl, KillControls, Draw1Control,... |
| **`NEWCONTROL_CONT`** | `0x012DF8` | `0x00D426` | `control_mgr.s:101`<br>`control_mgr.s:92` | NEWCONTROL_CONT Called during boot. NEWCONTROL_CONT: draw control if visible and intersects owner window's portRect A3 = ControlHandle, D0 = CDEF message, D1 = param |
| **`NEWCONTROL_CONT_2`** | `0x012E6C` | `0x00D470` | `control_mgr.s:147`<br>`control_mgr.s:131` | — |
| **`NEWCONTROL_CONT_3`** | `0x012E70` | `0x00D474` | `control_mgr.s:159`<br>`control_mgr.s:142` | NEWCONTROL_CONT_3 Called during boot. NEWCONTROL_CONT_3: erase and invalidate control's region (used when hiding/disposing) Sends calcCRgns (2) to CDEF to get control's region, then erases and invalid... |
| **`NEWCONTROL_FOUND`** | `0x012E2C` | `0x00D430` | `control_mgr.s:121`<br>`control_mgr.s:105` | NEWCONTROL_FOUND: call CDEF proc for control A3 D0 = message (0=draw, 1=test, 2=calc, 3=init, 4=dispose, 5=pos, 6=thumb, 7=drag, 8=autoTrack), D1 = param, A3 = ControlHandle Called by: DRAGCONTROL_CON... |
| **`NEWCONTROL_OK`** | `0x012E58` | `0x00D45C` | `control_mgr.s:139`<br>`control_mgr.s:123` | — |
| **`NEWCONTROL_RETRY`** | `0x012DAE` | `0x00D3DC` | `control_mgr.s:63`<br>`control_mgr.s:57` | load CDEF resource for this control type |
| **`NEWCONTROL_SKIP`** | `0x012DEA` | `0x00D418` | `control_mgr.s:87`<br>`control_mgr.s:81` | — |
| **`NEWCONTROL_SKIP_2`** | `0x012E6E` | `0x00D472` | `control_mgr.s:149`<br>`control_mgr.s:133` | — |
| **`NewDialog`** | `0x014AC8` | `0x00F0EA` | `dialog_mgr.s:321` | _NewDialog ($A97D) Called during boot. |
| **`NEWDIALOG`** | `0x014AC8` | `0x00F0EA` | `dialog_mgr.s:320` | _NewDialog ($A97D) -- create a dialog window with item list. Stack: dStorage(L), bounds(8), title(L), visible(B), procID(W), behind(L), goAwayFlag(B), refCon(L), items(L) -> dialog(L). Allocates dialo... |
| **`NEWDIALOG_CONT`** | `0x014B46` | `0x00F168` | `dialog_mgr.s:363`<br>`dialog_mgr.s:362` | — |
| **`NEWDIALOG_CONT_2`** | `0x014B48` | `0x00F16A` | `dialog_mgr.s:371`<br>`dialog_mgr.s:372` | NEWDIALOG_CONT_2 Called during boot (3,693 times in 30s trace). |
| **`NEWDIALOG_LOCK_ITEMS`** | — | `0x00F2F6` | `dialog_mgr.s:611` | — |
| **`NEWDIALOG_OK`** | `0x014ADE` | `0x00F100` | `dialog_mgr.s:328`<br>`dialog_mgr.s:327` | — |
| **`NEWDIALOG_OK_2`** | `0x014B5A` | `0x00F17C` | `dialog_mgr.s:387`<br>`dialog_mgr.s:387` | NEWDIALOG_OK_2 - update/activate: window is in event message field Called during boot. |
| **`NewMap`** | `0x013618` | — | `resource_mgr.s:450` | New Map Called during boot. |
| **`NEWMAP_CONT`** | `0x01365A` | `0x00DC5A` | `resource_mgr.s:477`<br>`resource_mgr.s:476` | NEWMAP_CONT Called during boot. |
| **`NEWMAP_ERR`** | `0x0136DA` | — | `resource_mgr.s:528` | NEWMAP_ERR |
| **`NEWMAP_ERR_2`** | `0x0136E0` | `0x00DCDC` | `resource_mgr.s:531`<br>`resource_mgr.s:527` | NEWMAP_ERR |
| **`NEWMAP_ERR_3`** | `0x0136E4` | `0x00DCE0` | `resource_mgr.s:534`<br>`resource_mgr.s:530` | — |
| **`NEWMAP_RETRY`** | `0x0136F2` | `0x00DCEE` | `resource_mgr.s:546`<br>`resource_mgr.s:545` | NEWMAP_RETRY Called during boot. |
| **`NEWMAP_SKIP`** | `0x0136C4` | `0x00DCC0` | `resource_mgr.s:515`<br>`resource_mgr.s:514` | — |
| **`NEWMAP_SKIP_2`** | `0x013702` | `0x00DCFE` | `resource_mgr.s:551`<br>`resource_mgr.s:550` | — |
| **`NewMenu`** | `0x0129CA` | `0x00CFF6` | `menu_mgr.s:1329` | **Proto:** `Pascal: function NewMenu(menuID: INTEGER; menuTitle: Str255): MenuHandle;`<br>_NewMenu ($A931) _NewMenu ($A931): create a new menu Pascal: function NewMenu(menuID: INTEGER; menuTitle: Str255): MenuHandle; |
| **`NEWMENU`** | `0x0129CA` | `0x00CFF6` | `menu_mgr.s:1054` | **Proto:** `Pascal: function NewMenu(menuID: INTEGER; menuTitle: Str255): MenuHandle;`<br>_NewMenu ($A931): allocate a new MenuInfo with title and default MDEF. Pascal: function NewMenu(menuID: INTEGER; menuTitle: Str255): MenuHandle; Allocates 14-byte header + title length + terminator by... |
| **`NEWMENU_LOOP`** | `0x012A0E` | `0x00D03A` | `menu_mgr.s:1357`<br>`menu_mgr.s:1079` | fill MenuInfo header load default MDEF 0 copy menu title into menuData |
| **`NewString`** | `0x0111AC` | `0x00B7F4` | `window_mgr.s:46` | **Proto:** `Pascal: FUNCTION NewString(theString: Str255): StringHandle`<br>Window Manager Apple source: WindowMgr.a (MacSEROM.lst module WMGR). It starts with NewString/SetString ($A906/$A907, string handles, used for window titles) and the window-list primitives FIND_PREV_W... |
| **`NEWSTRING`** | `0x0111AC` | `0x00B7F4` | `window_mgr.s:62` | **Proto:** `Pascal: FUNCTION NewString(theString: Str255): StringHandle`<br>_NewString ($A906) Pascal: FUNCTION NewString(theString: Str255): StringHandle Allocates a new handle and copies the Pascal string into it. |
| **`NewWindow`** | `0x011642` | `0x00BCA8` | `window_mgr.s:815` | **Proto:** `Pascal: function NewWindow(wStorage: Ptr; boundsRect: Rect;`<br>_NewWindow ($A913) stack: boundsRect, title, visible, procID, behind, goAway, refCon -> WindowPtr _NewWindow ($A913): create a new window Pascal: function NewWindow(wStorage: Ptr; boundsRect: Rect; ti... |
| **`NEWWINDOW`** | `0x011642` | `0x00BCA8` | `window_mgr.s:761` | **Proto:** `Pascal: function NewWindow(wStorage: Ptr; boundsRect: Rect;`<br>_NewWindow ($A913): create a new window Pascal: function NewWindow(wStorage: Ptr; boundsRect: Rect; title: Str255; visible: BOOLEAN; procID: INTEGER; behind: WindowPtr; goAwayFlag: BOOLEAN; refCon: Lo... |
| **`NEWWINDOW_CONT`** | `0x01165E` | `0x00BCC4` | `window_mgr.s:825`<br>`window_mgr.s:771` | allocate window record in application heap |
| **`NEWWINDOW_CONT_2`** | `0x01175C` | `0x00BDC2` | `window_mgr.s:945`<br>`window_mgr.s:887` | NEWWINDOW_CONT_2 - cancel pending activate/deactivate events for window A3 If window A3 matches CurActivate or CurDeactive, invalidates that entry by setting bit 7 (high byte flag). This prevents stal... |
| **`NEWWINDOW_CONT_3`** | `0x011766` | `0x00BDCC` | `window_mgr.s:951`<br>`window_mgr.s:893` | NEWWINDOW_CONT_3 -- check/cancel CurActivate. |
| **`NEWWINDOW_EXIT`** | `0x011712` | `0x00BD78` | `window_mgr.s:901`<br>`window_mgr.s:847` | insert window into window list paint new window and recalculate visibility |
| **`NEWWINDOW_LOOP`** | `0x01169E` | — | `window_mgr.s:849` | initialize WindowRecord fields after GrafPort (offset +108) allocate 3 regions: strucRgn, contRgn, updateRgn |
| **`NEWWINDOW_NO`** | `0x011750` | `0x00BDB6` | `window_mgr.s:932`<br>`window_mgr.s:875` | — |
| **`NEWWINDOW_OK`** | `0x011734` | `0x00BD9A` | `window_mgr.s:921`<br>`window_mgr.s:864` | NEWWINDOW_OK NEWWINDOW_OK - NewWindow: insert at front of window list (behind=-1 or empty list) Called during boot. |
| **`NEWWINDOW_RETRY`** | `0x0116AE` | `0x00BD14` | `window_mgr.s:856`<br>`window_mgr.s:802` | load WDEF resource |
| **`NEWWINDOW_RGN_LOOP`** | — | `0x00BD04` | `window_mgr.s:795` | initialize WindowRecord fields after GrafPort (offset +108) allocate 3 regions: strucRgn, contRgn, updateRgn |
| **`NEWWINDOW_SKIP`** | `0x011746` | `0x00BDAC` | `window_mgr.s:929`<br>`window_mgr.s:872` | — |
| **`NEWWINDOW_SKIP_2`** | `0x011774` | `0x00BDDA` | `window_mgr.s:957`<br>`window_mgr.s:899` | — |
| **`NoteAlert`** | `0x01496C` | `0x00EF8E` | `dialog_mgr.s:136` | **Proto:** `NoteAlert -- _NoteAlert ($A987): FUNCTION NoteAlert (alertID : INTEGER; filterProc: ProcPtr) INTEGER;`<br>NoteAlert -- _NoteAlert ($A987): FUNCTION NoteAlert (alertID : INTEGER; filterProc: ProcPtr) INTEGER; _NoteAlert ($A987) |
| **`NOTEALERT`** | `0x01496C` | `0x00EF8E` | `dialog_mgr.s:133` | _NoteAlert ($A987) -- show note-icon alert dialog. |
| **`OpenDeskAcc`** | `0x015E64` | `0x0104B8` | `desk_mgr.s:404` | _OpenDeskAcc ($A9B6) |
| **`OPENDESKACC`** | `0x015E64` | `0x0104B8` | `desk_mgr.s:414` | _OpenDeskAcc ($A9B6) - open desk accessory by name. Calls _Open with read-only IOParam, then SelectWindow + ShowWindow on the DA's window from dCtlWindow ($1E in DCE). |
| **`OPENDESKACC_ERR`** | `0x015EAA` | `0x0104FE` | `desk_mgr.s:427`<br>`desk_mgr.s:437` | — |
| **`OPENRES_COMMON`** | `0x0137F4` | `0x00DDF0` | `resource_mgr.s:689`<br>`resource_mgr.s:689` | _OpenResFile ($A997) Opens a resource file and links its map into the chain. Returns the file's reference number as function result. Called during boot. |
| **`OPENRES_EXIT`** | `0x013816` | `0x00DE18` | `resource_mgr.s:700`<br>`resource_mgr.s:701` | — |
| **`OpenResFile`** | `0x0137F0` | `0x00DDEC` | `resource_mgr.s:687` | _OpenResFile ($A997) Opens a resource file and links its map into the chain. Returns the file's reference number as function result. Called during boot. |
| **`OPENRESFILE`** | `0x0137F0` | `0x00DDEC` | `resource_mgr.s:686` | _OpenResFile ($A997) -- open a resource file and link its map. Opens a resource file by filename, builds an in-memory resource map from its resource fork, and links the new map at the head of the reso... |
| **`OPENRF_SET_FNAME`** | `0x013792` | `0x00DD8E` | `resource_mgr.s:633`<br>`resource_mgr.s:634` | — |
| **`OPENRF_SKIP_BOOT`** | `0x01378C` | `0x00DD88` | `resource_mgr.s:630`<br>`resource_mgr.s:631` | RSRCZONEINIT_CONT_2 - open resource fork, checking for printer driver If the resource is 'STR ' ID -8192, uses BootDrive for vRefNum (matches the printer driver resource file convention). |
| **`OpenRFPerm`** | `0x01381A` | `0x00DE1C` | `resource_mgr.s:710` | _OpenRFPerm ($A9C4) Opens a resource file with explicit permission byte. Stack: fileName(L), vRefNum(W), permission(B) -> refNum(W) |
| **`OPENRFPERM`** | `0x01381A` | `0x00DE1C` | `resource_mgr.s:709` | _OpenRFPerm ($A9C4) -- open with explicit permission byte. Stack: fileName(L), vRefNum(W), permission(B) -> refNum(W). Pops permission byte and vRefNum, joins OpenResFile common path. |
| **`ORPHAN_RESTORE_TAIL`** | — | `0x00C854` | `window_mgr.s:2449` | Orphan tail (unreachable in SE FDHD): paired state-restore stub. Pops two saved-state buffer pointers from stack, restores 6 bytes each to (0xCF0)/(0xCF4) and ghost_DeskPatEnable/ghost_VIA2. No caller... |
| **`P_Char2Pixel`** | — | `0x0111EA` | `textedit.s:1466` | P_Char2Pixel - hookable trampoline to (0x79C) lowmem. Stacked-RTS tail-call to char-to-pixel hook. |
| **`P_CheckLoad`** | `0x014130` | `0x00E740` | `resource_mgr.s:2300`<br>`resource_mgr.s:2188` | P_Check Load Called during boot (22,904 times in 30s trace). |
| **`P_doTEDoText`** | `0x01651E` | `0x010F30` | `textedit.s:698`<br>`textedit.s:1109` | P_do TE Do Text Called during boot. |
| **`P_doTERecal`** | `0x01692A` | `0x0117A8` | `textedit.s:1389`<br>`textedit.s:2270` | P_do TE Recal Called during boot. |
| **`P_NewMap`** | `0x013612` | `0x00DC12` | `resource_mgr.s:441`<br>`resource_mgr.s:443` | P_New Map Called during boot. |
| **`P_Pixel2Char`** | — | `0x010C3E` | `textedit.s:705` | P_Pixel2Char - hookable trampoline to the pixel-to-char proc stored at lowmem 0x798. Tail-calls the hook via stacked RTS: pushes (0x798) on top of the BSR return address, then RTS jumps to the hook wi... |
| **`P_SuperLoad`** | `0x0134CE` | `0x00DAD0` | `resource_mgr.s:261`<br>`resource_mgr.s:263` | P_Super Load Called during boot. |
| **`P_TEDoText`** | `0x016524` | `0x010F36` | `textedit.s:707`<br>`textedit.s:1121` | P_TE Do Text Called during boot. |
| **`P_TEDOTEXT_CONT`** | `0x01657A` | — | `textedit.s:752` | P_TEDOTEXT_CONT Called during boot. |
| **`P_TEDOTEXT_CONT_2`** | `0x01659A` | `0x011078` | `textedit.s:777`<br>`textedit.s:1261` | P_TEDOTEXT_CONT_2 Called during boot. |
| **`P_TEDOTEXT_CONT_3`** | `0x0165DA` | — | `textedit.s:801` | — |
| **`P_TEDOTEXT_CONT_4`** | `0x0165EE` | `0x01114C` | `textedit.s:814`<br>`textedit.s:1371` | P_TEDOTEXT_CONT_4 Called during boot. |
| **`P_TEDOTEXT_EMPTY`** | `0x016564` | — | `textedit.s:739` | — |
| **`P_TEDOTEXT_EXIT`** | `0x016596` | — | `textedit.s:769` | P_TEDOTEXT_EXIT Called during boot. |
| **`P_TEDOTEXT_LAST_PARTIAL`** | — | `0x01100A` | `textedit.s:1200` | — |
| **`P_TEDOTEXT_NEXT`** | `0x016582` | — | `textedit.s:755` | — |
| **`P_TEDOTEXT_NO`** | `0x01655C` | `0x010F6E` | `textedit.s:734`<br>`textedit.s:1142` | D7=-2: caret drawing mode P_TEDOTEXT_NO |
| **`P_TEDOTEXT_NO_2`** | `0x016562` | `0x010F74` | `textedit.s:737`<br>`textedit.s:1145` | — |
| **`P_TEDOTEXT_OK`** | `0x0165E2` | — | `textedit.s:804` | — |
| **`P_TERecal`** | `0x016930` | `0x0117AE` | `textedit.s:1398`<br>`textedit.s:2281` | P_TE Recal Called during boot. |
| **`P_TERECAL_BOUNDARY`** | — | `0x011820` | `textedit.s:2323` | — |
| **`P_TERECAL_CONT`** | `0x016970` | `0x0117FC` | `textedit.s:1428`<br>`textedit.s:2309` | Decide whether to rewind to start of current word. |
| **`P_TERECAL_CONT_2`** | `0x01698E` | — | `textedit.s:1446` | P_TERECAL_CONT_2 Called during boot. |
| **`P_TERECAL_CONT_3`** | `0x016A30` | — | `textedit.s:1548` | P_TERECAL_CONT_3 Called during boot. |
| **`P_TERECAL_CONT_4`** | `0x016A44` | `0x011AEA` | `textedit.s:1556`<br>`textedit.s:2703` | P_TERECAL_CONT_4 -- draw/erase caret (XOR). |
| **`P_TERECAL_DISPATCH`** | — | `0x01182E` | `textedit.s:2331` | Dispatch to in-place recalc (TE_INPLACE_LINESTARTS) or full rebuild (TE_FULL_REBUILD_LINESTARTS). Called by: P_TERECAL_DONE, P_TERECAL_CONT |
| **`P_TERECAL_DONE`** | `0x01697C` | `0x011808` | `textedit.s:1433`<br>`textedit.s:2314` | — |
| **`P_TERECAL_DONE_2`** | `0x0169CE` | — | `textedit.s:1488` | — |
| **`P_TERECAL_DONE_3`** | `0x0169E0` | — | `textedit.s:1495` | — |
| **`P_TERECAL_DONE_4`** | `0x016A0E` | — | `textedit.s:1521` | — |
| **`P_TERECAL_FOUND`** | — | `0x0117F4` | `textedit.s:2304` | — |
| **`P_TERECAL_FULL_REBUILD`** | — | `0x011838` | `textedit.s:2337` | — |
| **`P_TERECAL_NEXT`** | `0x016956` | `0x0117E2` | `textedit.s:1411`<br>`textedit.s:2296` | Walk existing lineStarts to find which line contains selStart. |
| **`P_TERECAL_NEXT_2`** | `0x01699C` | — | `textedit.s:1458` | P_TERECAL_NEXT_2 Called during boot. |
| **`P_TERECAL_NEXT_3`** | `0x0169E8` | `0x011882` | `textedit.s:1505`<br>`textedit.s:2382` | P_TERECAL_NEXT_3 Called during boot. |
| **`P_TERECAL_NO`** | `0x0169B4` | — | `textedit.s:1469` | — |
| **`P_TERECAL_NO_2`** | `0x0169C2` | — | `textedit.s:1482` | — |
| **`P_TERECAL_NO_3`** | `0x016A10` | — | `textedit.s:1530` | P_TERECAL_NO_3 -- set caret state. P_TERECAL_NO_3 Called by: TESetSelect, TECLICK_NO_2, TECLICK_CONT_4, TEDelete, TEPASTE_CONT (and 3 more) |
| **`P_TERECAL_OK`** | `0x016968` | — | `textedit.s:1424` | P_TERECAL_OK |
| **`P_TERECAL_OK_2`** | `0x0169BC` | `0x0118A6` | `textedit.s:1479`<br>`textedit.s:2397` | P_TERECAL_OK_2 |
| **`P_TERECAL_OK_3`** | `0x016A2E` | — | `textedit.s:1540` | — |
| **`P_TERECAL_SKIP`** | `0x0169A6` | — | `textedit.s:1462` | — |
| **`P_TERECAL_STYLED_HEIGHT`** | — | `0x01183C` | `textedit.s:2339` | — |
| **`P_TEWdBreak`** | `0x0168A2` | `0x011692` | `textedit.s:1296`<br>`textedit.s:2119` | P_TE Wd Break Called during boot. |
| **`P_TEWDBREAK_CONT`** | `0x0168B4` | — | `textedit.s:1308` | P_TEWDBREAK_CONT Called during boot. |
| **`P_TEWDBREAK_NEXT`** | `0x0168C2` | `0x011726` | `textedit.s:1319`<br>`textedit.s:2200` | P_TEWDBREAK_NEXT Called during boot. |
| **`P_XTrimMeasure`** | `0x0165F4` | `0x011152` | `textedit.s:818`<br>`textedit.s:1378` | P_XTrimMeasure -- measure trimmed line width -> D0. |
| **`Pack0`** | `0x017032` | `0x01A0A2` | `package_mgr.s:145` | Pack dispatch BSR table Each BSR.B PACK_DISPATCH is exactly 2 bytes. PACK_DISPATCH uses the return address to compute which pack was called. Packs 0-7: standard Mac packages Packs 8-15: Color QuickDra... |
| **`PACK0`** | `0x017032` | `0x01A0A2` | `package_mgr.s:130` | — |
| **`Pack1`** | `0x017034` | `0x01A0A4` | `package_mgr.s:148` | Pack1 -- trap handler for _Pack1 ($A9E8). |
| **`PACK1`** | `0x017034` | `0x01A0A4` | `package_mgr.s:132` | — |
| **`Pack10`** | `0x017046` | `0x01A0B6` | `package_mgr.s:169` | — |
| **`PACK10`** | `0x017046` | `0x01A0B6` | `package_mgr.s:150` | — |
| **`Pack11`** | `0x017048` | `0x01A0B8` | `package_mgr.s:171` | — |
| **`PACK11`** | `0x017048` | `0x01A0B8` | `package_mgr.s:152` | — |
| **`Pack12`** | `0x01704A` | `0x01A0BA` | `package_mgr.s:173` | — |
| **`PACK12`** | `0x01704A` | `0x01A0BA` | `package_mgr.s:154` | — |
| **`Pack13`** | `0x01704C` | `0x01A0BC` | `package_mgr.s:175` | — |
| **`PACK13`** | `0x01704C` | `0x01A0BC` | `package_mgr.s:156` | — |
| **`Pack14`** | `0x01704E` | `0x01A0BE` | `package_mgr.s:177` | — |
| **`PACK14`** | `0x01704E` | `0x01A0BE` | `package_mgr.s:158` | — |
| **`Pack15`** | `0x017050` | `0x01A0C0` | `package_mgr.s:179` | — |
| **`PACK15`** | `0x017050` | `0x01A0C0` | `package_mgr.s:160` | — |
| **`Pack2`** | `0x017036` | `0x01A0A6` | `package_mgr.s:151` | Pack2 -- trap handler for _Pack2 ($A9E9). |
| **`PACK2`** | `0x017036` | `0x01A0A6` | `package_mgr.s:134` | — |
| **`Pack3`** | `0x017038` | `0x01A0A8` | `package_mgr.s:154` | Pack3 -- trap handler for _Pack3 ($A9EA). |
| **`PACK3`** | `0x017038` | `0x01A0A8` | `package_mgr.s:136` | — |
| **`Pack4`** | `0x01703A` | `0x01A0AA` | `package_mgr.s:156` | — |
| **`PACK4`** | `0x01703A` | `0x01A0AA` | `package_mgr.s:138` | — |
| **`Pack5`** | `0x01703C` | `0x01A0AC` | `package_mgr.s:158` | — |
| **`PACK5`** | `0x01703C` | `0x01A0AC` | `package_mgr.s:140` | — |
| **`Pack6`** | `0x01703E` | `0x01A0AE` | `package_mgr.s:161` | Pack6 -- trap handler for _Pack6 ($A9ED). |
| **`PACK6`** | `0x01703E` | `0x01A0AE` | `package_mgr.s:142` | — |
| **`Pack7`** | `0x017040` | `0x01A0B0` | `package_mgr.s:163` | — |
| **`PACK7`** | `0x017040` | `0x01A0B0` | `package_mgr.s:144` | — |
| **`Pack8`** | `0x017042` | `0x01A0B2` | `package_mgr.s:165` | — |
| **`PACK8`** | `0x017042` | `0x01A0B2` | `package_mgr.s:146` | — |
| **`Pack9`** | `0x017044` | `0x01A0B4` | `package_mgr.s:167` | — |
| **`PACK9`** | `0x017044` | `0x01A0B4` | `package_mgr.s:148` | — |
| **`PACK_DISPATCH`** | `0x016FEA` | `0x01A058` | `package_mgr.s:97`<br>`package_mgr.s:92` | PACK_DISPATCH - Pack load-and-jump dispatcher Called via the BSR table below. Uses return address to determine which pack was requested: distance from Pack1 divided by 2 gives the pack number (each BS... |
| **`PACKDISP_FAIL`** | `0x017020` | `0x01A090` | `package_mgr.s:128`<br>`package_mgr.s:123` | PACKDISP_FAIL - Package load failure handler Computes system error ID = packNum + 17 (dsNoPk range) and calls _SysError. Error IDs 17-24 display "Can't load package" in the System Error Handler. |
| **`PACKDISP_LOADED`** | `0x017014` | `0x01A082` | `package_mgr.s:114`<br>`package_mgr.s:109` | — |
| **`PACKDISPATCHER`** | — | `0x019FFE` | `package_mgr.s:21` | **Proto:** `Pascal: procedure InitPack(packID: INTEGER);`<br>Package Manager -- _InitPack, _InitAllPacks, _Pack0 ... _Pack15 Apple source: PackageMgr.a (MacSEROM.lst module PACKDISPATCHER). InitPack loads one PACK resource and stores its handle in AppPacks (pac... |
| **`PackTexturePattern`** | — | `0x01258A` | `textedit.s:4254` | PackTexturePattern -- pack 3-word texture pattern + write to GrafPort A7+4 -> 6-byte input array of three words (3 bits each). Packs them into D1 by shifting left 1 bit each, then uses D1 as an 8-bit ... |
| **`PaintBehind`** | `0x0113A2` | `0x00B9F6` | `window_mgr.s:417` | **Proto:** `Pascal: procedure PaintBehind(startWindow: WindowPeek; clobberedRgn: RgnHandle);`<br>_PaintBehind ($A90D) stack: startWindow, clobberedRgn -> (repaints behind) _PaintBehind ($A90D): repaint all windows behind startWindow Pascal: procedure PaintBehind(startWindow: WindowPeek; clobbered... |
| **`PAINTBEHIND`** | `0x0113A2` | `0x00B9F6` | `window_mgr.s:390` | **Proto:** `Pascal: procedure PaintBehind(startWindow: WindowPeek; clobberedRgn: RgnHandle);`<br>_PaintBehind ($A90D): repaint all windows behind startWindow Pascal: procedure PaintBehind(startWindow: WindowPeek; clobberedRgn: RgnHandle); |
| **`PAINTBEHIND_EMPTY`** | `0x011402` | — | `window_mgr.s:474` | PAINTBEHIND_EMPTY - allocate new region and push handle on stack Creates a new empty region. Returns with the handle on the stack (below the caller's return address). Uses trick: saves return addr, re... |
| **`PAINTBEHIND_LOOP`** | `0x0113DE` | `0x00BA32` | `window_mgr.s:444`<br>`window_mgr.s:417` | walk window list from startWindow, repainting each visible one |
| **`PAINTBEHIND_OK`** | `0x0113F6` | `0x00BA4A` | `window_mgr.s:461`<br>`window_mgr.s:430` | PAINTBEHIND_OK - PaintBehind epilogue: re-enable content erase Called during boot. |
| **`PAINTBEHIND_SKIP`** | `0x0113F0` | `0x00BA44` | `window_mgr.s:452`<br>`window_mgr.s:425` | — |
| **`PaintOne`** | `0x0112F8` | `0x00B946` | `window_mgr.s:292` | **Proto:** `Pascal: procedure PaintOne(window: WindowPeek; clobberedRgn: RgnHandle);`<br>_PaintOne ($A90C) stack: window, clobberedRgn -> (repaints) _PaintOne ($A90C): repaint one window's frame and add to updateRgn Pascal: procedure PaintOne(window: WindowPeek; clobberedRgn: RgnHandle); ... |
| **`PAINTONE`** | `0x0112F8` | `0x00B946` | `window_mgr.s:284` | **Proto:** `Pascal: procedure PaintOne(window: WindowPeek; clobberedRgn: RgnHandle);`<br>_PaintOne ($A90C): repaint one window's frame and add to updateRgn Pascal: procedure PaintOne(window: WindowPeek; clobberedRgn: RgnHandle); If window=nil, paints desktop pattern instead |
| **`PAINTONE_CONT`** | `0x011368` | `0x00B9BC` | `window_mgr.s:351`<br>`window_mgr.s:341` | PAINTONE_CONT - save current port, switch to WMgr, get clipRgn in D3 Called during boot. |
| **`PAINTONE_CONT_2`** | `0x011386` | `0x00B9DA` | `window_mgr.s:388`<br>`window_mgr.s:367` | PAINTONE_CONT_2 - paint desktop: call DeskHook or fill with DeskPattern Clips above all windows (nil param = entire desktop), then calls application's DeskHook if installed, else fills with pattern. C... |
| **`PAINTONE_DROP_RETURN`** | — | `0x00B9D6` | `window_mgr.s:357` | — |
| **`PAINTONE_ERR`** | `0x011382` | — | `window_mgr.s:377` | PAINTONE_ERR - PAINTONE_SKIP early exit: pop caller's return address, go to epilogue Called during boot. |
| **`PAINTONE_EXIT`** | `0x01130E` | `0x00B960` | `window_mgr.s:302`<br>`window_mgr.s:294` | nil window: paint desktop |
| **`PAINTONE_NO`** | `0x011316` | `0x00B968` | `window_mgr.s:311`<br>`window_mgr.s:302` | PAINTONE_NO - PaintOne: repaint a visible window's frame and content Called during boot. |
| **`PAINTONE_NO_2`** | `0x011350` | `0x00B9A4` | `window_mgr.s:334`<br>`window_mgr.s:325` | — |
| **`PAINTONE_NO_3`** | `0x011362` | `0x00B9B6` | `window_mgr.s:341`<br>`window_mgr.s:332` | — |
| **`PAINTONE_NO_4`** | `0x011396` | `0x00B9EA` | `window_mgr.s:402`<br>`window_mgr.s:380` | PAINTONE_NO_4 - default desktop paint: fill WMgr portRect with desk pattern Called during boot. |
| **`PAINTONE_SKIP`** | `0x011376` | `0x00B9CA` | `window_mgr.s:364`<br>`window_mgr.s:350` | PAINTONE_SKIP - early exit if WMgr clipRgn (D3) is empty Tests whether D3 region is empty; if so, pops return address and jumps to PaintOne epilogue (skipping the rest of the caller). Called during bo... |
| **`ParamText`** | `0x014E0E` | `0x00F43E` | `dialog_mgr.s:837` | _ParamText ($A98B) Called during boot. |
| **`PARAMTEXT`** | `0x014E0E` | `0x00F43E` | `dialog_mgr.s:830` | _ParamText ($A98B) -- replace ParamText strings ^0..^3. Stack: param0(L), param1(L), param2(L), param3(L). Updates the four DAStrings slots from caller's parameters. For each non-nil param, disposes t... |
| **`PARAMTEXT_LOOP`** | `0x014E14` | `0x00F444` | `dialog_mgr.s:840`<br>`dialog_mgr.s:833` | — |
| **`PARAMTEXT_NO`** | `0x014E22` | `0x00F452` | `dialog_mgr.s:847`<br>`dialog_mgr.s:840` | — |
| **`PARAMTEXT_SKIP`** | `0x014E2A` | `0x00F45A` | `dialog_mgr.s:851`<br>`dialog_mgr.s:844` | — |
| **`PenModePatternTbl`** | — | `0x0125B8` | `textedit.s:4276` | Lookup table for PackTexturePattern: 8 longs (16 word indices) used as canned pen-mode patterns indexed by packed input bits. |
| **`PINSCROLL_DH`** | `0x016C86` | `0x012040` | `textedit.s:1932`<br>`textedit.s:3474` | — |
| **`PINSCROLL_DH0`** | `0x016CAE` | `0x012068` | `textedit.s:1953`<br>`textedit.s:3494` | — |
| **`PINSCROLL_DV0`** | `0x016C84` | `0x01203E` | `textedit.s:1930`<br>`textedit.s:3472` | — |
| **`PINSCROLL_HEIGHT`** | — | `0x012018` | `textedit.s:3450` | — |
| **`PINSCROLL_HPOS`** | `0x016CA0` | `0x01205A` | `textedit.s:1947`<br>`textedit.s:3488` | PINSCROLL_HPOS - TEPinScroll, dh >= 0: stop destRect.left at viewRect.left |
| **`PINSCROLL_SCROLL`** | `0x016CB2` | `0x01206C` | `textedit.s:1955`<br>`textedit.s:3496` | — |
| **`PINSCROLL_VPOS`** | `0x016C78` | `0x012032` | `textedit.s:1924`<br>`textedit.s:3466` | dv < 0 (text moves up): pin the text bottom against viewRect.bottom PINSCROLL_VPOS - TEPinScroll, dv >= 0: stop destRect.top at viewRect.top |
| **`PIXELTOCHAR_CLAMP_ZERO`** | — | `0x010CB0` | `textedit.s:774` | — |
| **`PIXELTOCHAR_DISPOSE_BUF`** | — | `0x010CBE` | `textedit.s:783` | — |
| **`PIXELTOCHAR_FINALIZE`** | — | `0x010CB4` | `textedit.s:777` | — |
| **`PIXELTOCHAR_FOUND_CHAR`** | — | `0x010C96` | `textedit.s:761` | — |
| **`PIXELTOCHAR_HEAP_ALLOC`** | — | `0x010C68` | `textedit.s:735` | — |
| **`PIXELTOCHAR_MEASURE`** | — | `0x010C78` | `textedit.s:744` | — |
| **`PIXELTOCHAR_SCAN_BACK`** | — | `0x010C8C` | `textedit.s:755` | — |
| **`PIXELTOCHAR_STY_CLAMP_START`** | — | `0x010D2A` | `textedit.s:834` | — |
| **`PIXELTOCHAR_STY_CR_CHECK`** | — | `0x010D82` | `textedit.s:872` | — |
| **`PIXELTOCHAR_STY_ENTRY`** | — | `0x010CD0` | `textedit.s:799` | PIXELTOCHAR_STY_ENTRY - P_TEDoText D7=0 path: pixel-to-char on a line. In: D5 = target pixel position, A2 = lineStarts entry. Output: char offset of the click position on the line. For unstyled TE: si... |
| **`PIXELTOCHAR_STY_EXIT`** | — | `0x010D9E` | `textedit.s:885` | — |
| **`PIXELTOCHAR_STY_FINALIZE`** | — | `0x010D92` | `textedit.s:880` | — |
| **`PIXELTOCHAR_STY_LEFT_SIDE`** | — | `0x010D8C` | `textedit.s:877` | — |
| **`PIXELTOCHAR_STY_MEASURE`** | — | `0x010D32` | `textedit.s:839` | — |
| **`PIXELTOCHAR_STY_MULTI_RUN`** | — | `0x010D04` | `textedit.s:816` | — |
| **`PIXELTOCHAR_STY_PAST_END`** | — | `0x010D6A` | `textedit.s:864` | — |
| **`PIXELTOCHAR_STY_RUN_LOOP`** | — | `0x010D18` | `textedit.s:825` | — |
| **`PlotIcon`** | `0x012D18` | `0x00D346` | `menu_mgr.s:1900` | **Proto:** `Pascal: procedure PlotIcon(theRect: Rect; theIcon: Handle);`<br>_PlotIcon ($A94B) Called during boot. _PlotIcon ($A94B): draw a 32x32 icon at specified rectangle Pascal: procedure PlotIcon(theRect: Rect; theIcon: Handle); |
| **`PLOTICON`** | `0x012D18` | `0x00D346` | `menu_mgr.s:1545` | **Proto:** `Pascal: procedure PlotIcon(theRect: Rect; theIcon: Handle);`<br>_PlotIcon ($A94B): draw a 32x32 icon resource into a rect. Pascal: procedure PlotIcon(theRect: Rect; theIcon: Handle); Builds a temp BitMap (32x32, rowBytes=4) at IconBitmap and CopyBits from icon dat... |
| **`PLOTICON_SKIP`** | `0x012D50` | — | `menu_mgr.s:1920` | — |
| **`PRG_BUILTIN_DISPATCH`** | — | `0x012868` | `print_glue.s:85` | Built-in dispatch: D1 = (dispatch_byte >> 3) & 0xF (Bit 4 of D1 cleared inline -> 4-bit entry select; word offset in PRGLUE_DISPATCH_TBL.) Allocates a 0x32-byte ParamBlock on stack with ioName -> "/.P... |
| **`PRG_EPILOGUE`** | — | `0x0129AE` | `print_glue.s:250` | — |
| **`PRG_EPILOGUE_FRAME`** | — | `0x0129B4` | `print_glue.s:253` | — |
| **`PRG_EXIT_NO_RESULT`** | — | `0x0128B6` | `print_glue.s:113` | — |
| **`PRG_FRAME_RESTORE`** | — | `0x0129C8` | `print_glue.s:262` | — |
| **`PRG_FROM_DCE`** | — | `0x012802` | `print_glue.s:43` | — |
| **`PRG_GOT_NAME`** | — | `0x0128EA` | `print_glue.s:141` | — |
| **`PRG_GOT_PDEF`** | — | `0x012832` | `print_glue.s:59` | — |
| **`PRG_LOAD_PDEF`** | — | `0x012818` | `print_glue.s:50` | — |
| **`PRG_OPEN_DONE`** | — | `0x01291E` | `print_glue.s:165` | — |
| **`PRG_OPEN_FAIL`** | — | `0x012922` | `print_glue.s:167` | — |
| **`PRG_OPEN_RF_BODY`** | — | `0x0128D8` | `print_glue.s:133` | PrGlue_PRCLOSE (selector 26, PrClose): close the .Print driver, then open the printer resource file again to learn its refNum and close it. |
| **`PRG_PDEF_KEEP_LOCKED`** | — | `0x012864` | `print_glue.s:78` | — |
| **`PRG_STATUS_DCE`** | — | `0x01298A` | `print_glue.s:228` | PRG_STATUS_DCE - call _Status with csCode=1 to get DCE handle. Returns A0 = DCE handle. |
| **`PRG_STORE_ERR`** | — | `0x0129A6` | `print_glue.s:247` | PRG_STORE_ERR - store D0 into PrintErr, drop ParamBlock, fall into epilogue. Called by: PrGlue_PURGE, PrGlue_NOPURGE, PRG_OPEN_FAIL, PrGlue_OPEN, PrGlue_CLOSE (and 1 more) |
| **`PRGLUE`** | — | `0x0127DA` | `print_glue.s:28` | Printing Manager glue -- _PrGlue Apple source: PrintGlue.a (System 7.1: Toolbox/Printing/PrintGlue.a; MacSEROM.lst module PRGLUE). The _PrGlue trap ($A8FD), new with the SE: the Printing Manager calls... |
| **`PrGlue_ATTR`** | — | `0x012938` | `print_glue.s:186` | PrGlue_ATTR: read DCE byte 0x7 (driver flags / ID), return word. |
| **`PrGlue_CLOSE`** | — | `0x01292A` | `print_glue.s:174` | — |
| **`PrGlue_CONTROL`** | — | `0x01294A` | `print_glue.s:197` | PrGlue_CONTROL: copy 4 longs + 1 word from caller to ParamBlock, then call _Control. |
| **`PRGLUE_DISPATCH_TBL`** | — | `0x012890` | `print_glue.s:100` | Built-in dispatch table (14 entries; 4 unused slots default to PrGlue_FAIL = -50). Each entry is the offset from PRGLUE_DISPATCH_TBL. |
| **`PrGlue_FAIL`** | — | `0x0128B0` | `print_glue.s:111` | PrGlue_FAIL: store paramErr (-50 = 0xFFCE) and skip param copy. |
| **`PRGLUE_GET_VREFNUM`** | — | `0x0129D6` | `print_glue.s:274` | PRGLUE_GET_VREFNUM PRGLUE_GET_VREFNUM: get current volume VRefNum (returns in D0) |
| **`PrGlue_GETERR`** | — | `0x012998` | `print_glue.s:235` | PrGlue_GETERR: return current PrintErr lowmem global. |
| **`PrGlue_NOPURGE`** | — | `0x012978` | `print_glue.s:217` | PrGlue_NOPURGE: same as PURGE but _HNoPurge. |
| **`PrGlue_OPEN`** | — | `0x012926` | `print_glue.s:171` | PrGlue_OPEN: simple _Open passthrough; ParamBlock already on stack. |
| **`PrGlue_PASSTHRU`** | — | `0x0129A2` | `print_glue.s:241` | PrGlue_PASSTHRU: caller's first param word becomes result code. |
| **`PrGlue_PRCLOSE`** | — | `0x0128CE` | `print_glue.s:129` | PrGlue_PRCLOSE (selector 26, PrClose): close the .Print driver, then open the printer resource file again to learn its refNum and close it. |
| **`PrGlue_PROPEN`** | — | `0x0128C0` | `print_glue.s:120` | PrGlue_PROPEN (selector 25, PrOpen): open the .Print driver, then the current printer resource file (PRG_OPEN_RF_BODY). |
| **`PrGlue_PURGE`** | — | `0x012966` | `print_glue.s:207` | PrGlue_PURGE: _Status -> DCE; if dRAMBased (bit 6 of flags), _HPurge the driver storage handle. |
| **`PRGLUE_SET_VOL`** | — | `0x0129D8` | `print_glue.s:277` | PRGLUE_SET_VOL: set volume to D0, then get current volume back |
| **`PrGlue_STATUS`** | — | `0x01292E` | `print_glue.s:179` | PrGlue_STATUS: _Status with cs=1 -> get DCE handle, return it. |
| **`PrimeStyleEntry`** | — | `0x01238E` | `textedit.s:3958` | PrimeStyleEntry -- prime styleEntry with computed font metrics A0 -> styleEntry being constructed (in scratch). Copies the family/face/size fields (offsets +6/+8/+0xA) into the teInPort's txFont/txFac... |
| **`PrintDriverName_Str`** | — | `0x0129F4` | `print_glue.s:290` | PrintDriverName_Str: Pascal-format string ".Print" used by InitPack5 to open the printer driver via _Open after pushing a pointer to it. |
| **`PtrAndHand`** | `0x015750` | `0x00FD88` | `toolbox_utils.s:409` | **Proto:** `Pascal: FUNCTION PtrAndHand(pntr: Ptr; hndl: Handle;`<br>**Regs:** `Entry: A0 = source pointer, A1 = handle, D0 = byte count Exit:  A0 = handle, D0 = result code`<br>_PtrAndHand ($A9EF): append D0 bytes from ptr A0 to the end of handle A1 Pascal: FUNCTION PtrAndHand(pntr: Ptr; hndl: Handle; size: LONGINT): OSErr; Entry: A0 = source pointer, A1 = handle, D0 = byte ... |
| **`PTRANDHAND`** | `0x015750` | `0x00FD88` | `toolbox_utils.s:343` | **Regs:** `end of handle A1. Entry: A0=ptr, A1=handle, D0=count.`<br>_PtrAndHand ($A9EF) - Append D0 bytes from ptr A0 to end of handle A1. Entry: A0=ptr, A1=handle, D0=count. |
| **`PtrToHand`** | `0x015712` | `0x00FD4A` | `toolbox_utils.s:352` | **Proto:** `Pascal: FUNCTION PtrToHand(srcPtr: Ptr; VAR dstHndl: Handle;`<br>**Regs:** `Entry: A0 = source pointer, D0 = byte count Exit:  A0 = new handle, D0 = result code`<br>_PtrToHand ($A9E3): copy D0 bytes from ptr A0 into a new handle Pascal: FUNCTION PtrToHand(srcPtr: Ptr; VAR dstHndl: Handle; size: LONGINT): OSErr; Entry: A0 = source pointer, D0 = byte count Exit:  A... |
| **`PTRTOHAND`** | `0x015712` | `0x00FD4A` | `toolbox_utils.s:297` | **Regs:** `bytes from ptr A0. Exit: A0 = new handle.`<br>_PtrToHand ($A9E3) - Create new handle with copy of D0 bytes from ptr A0. Exit: A0 = new handle. |
| **`PTRTOHAND_CONT`** | `0x015718` | `0x00FD50` | `toolbox_utils.s:359`<br>`toolbox_utils.s:302` | PTRTOHAND_CONT (Apple: cloneCommon) -- if the preceding Memory Manager trap failed (Z clear) return its code; else copy D1 bytes from A1 to the start of handle A0. |
| **`PTRTOHAND_CONT_2`** | `0x01571C` | `0x00FD54` | `toolbox_utils.s:364`<br>`toolbox_utils.s:306` | **Regs:** `data of handle A0 at offset D2. Exit: A0 = handle, D0 = 0.`<br>PTRTOHAND_CONT_2 (Apple: clone2Common) -- copy D1 bytes from A1 to the data of handle A0 at offset D2. Exit: A0 = handle, D0 = 0. |
| **`PTRTOHAND_ERR`** | `0x01572A` | — | `toolbox_utils.s:372` | — |
| **`PTRTOHAND_FINALIZE`** | — | `0x00FD32` | `toolbox_utils.s:275` | Called by: HANDANDHAND, HANDTOHAND |
| **`PTRTOHAND_RTS`** | — | `0x00FD62` | `toolbox_utils.s:314` | — |
| **`PtrToXHand`** | `0x01570A` | `0x00FD42` | `toolbox_utils.s:339` | **Proto:** `Pascal: FUNCTION PtrToXHand(srcPtr: Ptr; dstHndl: Handle;`<br>**Regs:** `Entry: A0 = source pointer, A1 = destination handle, D0 = byte count Exit:  A0 = destination handle, D0 = result code`<br>_PtrToXHand ($A9E2): copy D0 bytes from ptr A0 into existing handle A1 Pascal: FUNCTION PtrToXHand(srcPtr: Ptr; dstHndl: Handle; size: LONGINT): OSErr; Entry: A0 = source pointer, A1 = destination han... |
| **`PTRTOXHAND`** | `0x01570A` | `0x00FD42` | `toolbox_utils.s:288` | _PtrToXHand ($A9E2) - Copy D0 bytes from ptr A0 into existing handle A1. Resizes handle to D0 bytes first. |
| **`PutScrap`** | `0x016F4A` | `0x012794` | `scrap_mgr.s:384` | **Proto:** `_PutScrap ($A9FE) - FUNCTION PutScrap(length: LongInt; theType: ResType;`<br>_PutScrap ($A9FE) - FUNCTION PutScrap(length: LongInt; theType: ResType; source: Ptr): LongInt Appends a new scrap entry to the current scrap. Writes the 8-byte header [theType + length] followed by t... |
| **`PUTSCRAP`** | `0x016F4A` | `0x012794` | `scrap_mgr.s:302` | — |
| **`RealFont`** | `0x00F20E` | `0x019D5E` | `font_mgr.s:1720` | **Proto:** `Pascal: function RealFont(fontNum: INTEGER; size: INTEGER): BOOLEAN;`<br>_RealFont ($A902): check if font exists at exact size (no scaling) Pascal: function RealFont(fontNum: INTEGER; size: INTEGER): BOOLEAN; |
| **`REALFONT`** | `0x00F20E` | `0x019D5E` | `font_mgr.s:1488` | **Proto:** `Pascal: function RealFont(fontNum: INTEGER; size: INTEGER): BOOLEAN;`<br>_RealFont ($A902): is point size available as physical font? Pascal: function RealFont(fontNum: INTEGER; size: INTEGER): BOOLEAN; |
| **`REALFONT_DEFAULT_SIZE`** | — | `0x019D6E` | `font_mgr.s:1496` | — |
| **`REALFONT_EXIT`** | `0x00F238` | — | `font_mgr.s:1736` | no FOND: try old-style FONT resource |
| **`REALFONT_EXIT_2`** | `0x00F23C` | — | `font_mgr.s:1738` | — |
| **`REALFONT_FOND_LOOP`** | — | `0x019D90` | `font_mgr.s:1511` | — |
| **`REALFONT_FOUND`** | `0x00F242` | `0x019DB2` | `font_mgr.s:1747`<br>`font_mgr.s:1526` | REALFONT_FOUND |
| **`REALFONT_GOT_SIZE`** | — | `0x019D78` | `font_mgr.s:1501` | — |
| **`REALFONT_LOOP`** | `0x00F252` | — | `font_mgr.s:1754` | — |
| **`REALFONT_RTS`** | — | `0x019DB4` | `font_mgr.s:1529` | Called by: REALFONT_FOND_LOOP, REALFONT_TRY_OLDFONT, REALFONT_GOT_SIZE |
| **`REALFONT_TRY_OLDFONT`** | — | `0x019D9E` | `font_mgr.s:1518` | — |
| **`ReleaseResource`** | `0x01440A` | `0x00EA26` | `resource_mgr.s:2817` | _ReleaseResource ($A9A3) stack: handle -> (releases resource) Called during boot. |
| **`RELEASERESOURCE`** | `0x01440A` | `0x00EA26` | `resource_mgr.s:2698` | _ReleaseResource ($A9A3) -- release a resource handle. Disposes the handle if not changed (resChanged clear), then nulls the ref's handle field so future GetResource reloads from disk. If resChanged i... |
| **`RELEASERESOURCE_CONT`** | `0x01441A` | `0x00EA36` | `resource_mgr.s:2823`<br>`resource_mgr.s:2704` | — |
| **`RELEASERESOURCE_EXIT`** | — | `0x00EA4C` | `resource_mgr.s:2711` | — |
| **`RELEASERESOURCE_FORCE_LOAD`** | — | `0x00EA1A` | `resource_mgr.s:2684` | — |
| **`RELEASERESOURCE_SKIP`** | `0x014428` | `0x00EA44` | `resource_mgr.s:2827`<br>`resource_mgr.s:2708` | — |
| **`RELEASERESOURCE_SKIP_2`** | `0x014430` | — | `resource_mgr.s:2830` | — |
| **`ResError`** | `0x014516` | `0x00EB3A` | `resource_mgr.s:3008` | **Proto:** `ResError -- _ResError ($A9AF): FUNCTION ResError: Integer;`<br>ResError -- _ResError ($A9AF): FUNCTION ResError: Integer; _ResError ($A9AF) |
| **`RESERROR`** | `0x014516` | `0x00EB3A` | `resource_mgr.s:2869` | _ResError ($A9AF) -- return the last Resource Manager error code. |
| **`RESIZERESMAP`** | — | `0x00EE04` | `resource_mgr.s:3245` | RESIZERESMAP -- grow/shrink the map handle by D0 bytes. Adjusts map.dataLength field by D0 then calls _SetHandleSize. Negative D0 shrinks; positive D0 grows. Uses CHECKLOAD_EXIT_4 to save state and CH... |
| **`RESMGR_CONT`** | `0x013EA0` | `0x00E4AA` | `resource_mgr.s:1804`<br>`resource_mgr.s:1715` | RESMGR_CONT -- GetMap: find the map with refNum D6 (0 = SysMap). Called by: INITRESOURCES_CONT_5, NewMap, SetResFileAttrs, STDMAPENTRY, CLOSERES_UNLINK |
| **`RESMGR_CONT_10`** | `0x013FF8` | `0x00E602` | `resource_mgr.s:2086`<br>`resource_mgr.s:1980` | — |
| **`RESMGR_CONT_11`** | `0x01400C` | `0x00E616` | `resource_mgr.s:2119`<br>`resource_mgr.s:2013` | Called by: RESMGR_SKIP_2, RESMGR_EXIT_4, RESMGR_EXIT_5, RESMGR_ERR_2, GETRESINFO_EMPTY_3 (and 2 more) |
| **`RESMGR_CONT_12`** | `0x014042` | `0x00E64C` | `resource_mgr.s:2150`<br>`resource_mgr.s:2043` | RESMGR_CONT_12 - FindResByHandle: find resource map entry for a given handle Given A1=resource handle, searches all maps for the reference entry whose handle field (ref+8) matches. Uses RMgrLastResHan... |
| **`RESMGR_CONT_13`** | `0x01404E` | `0x00E658` | `resource_mgr.s:2155`<br>`resource_mgr.s:2048` | — |
| **`RESMGR_CONT_14`** | `0x0140A8` | `0x00E6B2` | `resource_mgr.s:2213`<br>`resource_mgr.s:2103` | RESMGR_CONT_14/RESMGR_CONT_15 - CacheSearchState: save current search position Converts A2 (ref ptr) and A3 (type list) to relative offsets from the map base, stores them along with D3-D6/A1/A4 in RMg... |
| **`RESMGR_CONT_15`** | `0x0140AE` | `0x00E6B8` | `resource_mgr.s:2216`<br>`resource_mgr.s:2106` | RESMGR_CONT_15 -- cache search state in RMgr globals. |
| **`RESMGR_CONT_16`** | `0x0140C6` | `0x00E6D0` | `resource_mgr.s:2233`<br>`resource_mgr.s:2122` | RESMGR_CONT_16 - GetResName: get pointer to resource name string Reads the name offset from the reference entry (ref+2). If -1, the resource has no name; returns an empty Pascal string. Otherwise comp... |
| **`RESMGR_CONT_2`** | `0x013EAC` | `0x00E4B6` | `resource_mgr.s:1809`<br>`resource_mgr.s:1720` | — |
| **`RESMGR_CONT_3`** | `0x013EF2` | `0x00E4FC` | `resource_mgr.s:1880`<br>`resource_mgr.s:1786` | RESMGR_CONT_3 - CountAllRefs: count total reference entries in map Walks all type entries, summing their reference counts into D4. Used to find the end of reference lists (for name list offset calc). ... |
| **`RESMGR_CONT_4`** | `0x013F4E` | `0x00E558` | `resource_mgr.s:1996`<br>`resource_mgr.s:1893` | RESMGR_CONT_4/RESMGR_CONT_5/RESMGR_CONT_6 - Resource Manager trap prologue RESMGR_CONT_4: full prologue (clears ROMMapInsert, CurOnly, ResErr) RESMGR_CONT_5: partial prologue (clears CurOnly + ResErr,... |
| **`RESMGR_CONT_5`** | `0x013F52` | `0x00E55C` | `resource_mgr.s:1999`<br>`resource_mgr.s:1897` | RESMGR_CONT_5 -- prologue: clear CurOnly, ResErr, set up frame. |
| **`RESMGR_CONT_6`** | `0x013F56` | `0x00E560` | `resource_mgr.s:2003`<br>`resource_mgr.s:1901` | RESMGR_CONT_6 -- minimal prologue: clear ResErr. Called by: CountResources, GetIndResource, CountTypes, GetIndType, UniqueID (and 2 more) |
| **`RESMGR_CONT_7`** | `0x013F86` | `0x00E590` | `resource_mgr.s:2029`<br>`resource_mgr.s:1926` | RESMGR_CONT_7 - InsertRemoveROMMap: insert/remove ROM map in resource chain D1=0: insert ROM map between SysMap and its predecessor D1!=0: remove ROM map from chain (reverse the insertion) This allows... |
| **`RESMGR_CONT_8`** | `0x013FAE` | `0x00E5B8` | `resource_mgr.s:2048`<br>`resource_mgr.s:1944` | RESMGR_CONT_8 - inserting ROM map: update CurMap if it points to SysMap |
| **`RESMGR_CONT_9`** | `0x013FBE` | `0x00E5C8` | `resource_mgr.s:2054`<br>`resource_mgr.s:1950` | — |
| **`RESMGR_DONE`** | `0x013FDE` | `0x00E5E8` | `resource_mgr.s:2079`<br>`resource_mgr.s:1973` | — |
| **`RESMGR_EMPTY`** | `0x014072` | `0x00E67C` | `resource_mgr.s:2173`<br>`resource_mgr.s:2066` | — |
| **`RESMGR_EMPTY_2`** | `0x01412C` | `0x00E73C` | `resource_mgr.s:2291`<br>`resource_mgr.s:2176` | — |
| **`RESMGR_ERR`** | `0x013F4A` | `0x00E554` | `resource_mgr.s:1979`<br>`resource_mgr.s:1880` | RESMGR_ERR - search miss: return "not found" Called by: SUPERLOAD_ERR, RESMGR_LOOP_4, RESMGR_LOOP_5, RESMGR_EMPTY, RESMGR_EXIT_7 |
| **`RESMGR_ERR_2`** | `0x014006` | `0x00E610` | `resource_mgr.s:2106`<br>`resource_mgr.s:1999` | Called by: UseResFile, GetResFileAttrs, STDMAPENTRY_ERR, UpdateResFile, CLOSERES_DISPOSE |
| **`RESMGR_ERR_3`** | `0x014040` | `0x00E64A` | `resource_mgr.s:2139`<br>`resource_mgr.s:2033` | — |
| **`RESMGR_EXIT`** | `0x013EDA` | `0x00E4E4` | `resource_mgr.s:1852`<br>`resource_mgr.s:1760` | — |
| **`RESMGR_EXIT_2`** | `0x013F04` | `0x00E50E` | `resource_mgr.s:1896`<br>`resource_mgr.s:1801` | — |
| **`RESMGR_EXIT_3`** | `0x013F46` | `0x00E550` | `resource_mgr.s:1970`<br>`resource_mgr.s:1872` | RESMGR_EXIT_3: clear error code and return success. Called by: RESMGR_EXIT, RESMGR_FOUND_5, RESMGR_OK_3, RESMGR_CONT_16, RETURNS_28 |
| **`RESMGR_EXIT_4`** | `0x013FFE` | `0x00E608` | `resource_mgr.s:2096`<br>`resource_mgr.s:1989` | RESMGR_EXIT_4-RESMGR_EXIT_6 - trap epilogues with different parameter byte counts Each sets D0 to the number of parameter bytes to pop from caller's stack frame before returning. Falls into RESMGR_CON... |
| **`RESMGR_EXIT_5`** | `0x014002` | `0x00E60C` | `resource_mgr.s:2101`<br>`resource_mgr.s:1994` | Called by: COUNTRES_NEXTMAP, UNIQID_NEXTMAP, CHANGEDRESOURCE_ERR, WRITERESOURCE_SKIP_2, HOMERESFILE_EXIT (and 2 more) |
| **`RESMGR_EXIT_6`** | `0x01400A` | `0x00E614` | `resource_mgr.s:2116`<br>`resource_mgr.s:2009` | RESMGR_EXIT_6/RESMGR_CONT_11 - common Resource Manager trap epilogue Removes ROM map from chain if it was inserted, restores globals, then falls into the stack-frame teardown at RESMGR_SKIP_4. |
| **`RESMGR_EXIT_7`** | `0x0140D8` | — | `resource_mgr.s:2245` | RESMGR_EXIT_7 - no resource name: return empty Pascal string |
| **`RESMGR_FOUND`** | `0x013E72` | `0x00E47C` | `resource_mgr.s:1767`<br>`resource_mgr.s:1680` | RESMGR_FOUND - GetNamedResource: name matched, cache and load it Caches search state and loads the resource via CheckLoad. |
| **`RESMGR_FOUND_2`** | `0x013EB4` | `0x00E4BE` | `resource_mgr.s:1820`<br>`resource_mgr.s:1730` | RESMGR_FOUND_2 - walk to next map in resource chain Follows the nextMap handle link (offset 0x10) to traverse the chain. The map's mNext field (+$10) holds the next map handle. |
| **`RESMGR_FOUND_3`** | `0x013F44` | `0x00E54E` | `resource_mgr.s:1968`<br>`resource_mgr.s:1868` | RESMGR_FOUND_3 - search hit: back up A2 to point at matched entry |
| **`RESMGR_FOUND_4`** | `0x014054` | `0x00E65E` | `resource_mgr.s:2158`<br>`resource_mgr.s:2051` | — |
| **`RESMGR_FOUND_5`** | `0x01407E` | `0x00E688` | `resource_mgr.s:2183`<br>`resource_mgr.s:2075` | RESMGR_FOUND_5 - handle matched: back up A2 to ref entry start and cache |
| **`RESMGR_LOOP`** | `0x013EBE` | `0x00E4C8` | `resource_mgr.s:1824`<br>`resource_mgr.s:1734` | — |
| **`RESMGR_LOOP_2`** | `0x013EFC` | `0x00E506` | `resource_mgr.s:1891`<br>`resource_mgr.s:1796` | RESMGR_LOOP_2 - accumulate ref counts per type |
| **`RESMGR_LOOP_3`** | `0x013F00` | `0x00E50A` | `resource_mgr.s:1894`<br>`resource_mgr.s:1799` | — |
| **`RESMGR_LOOP_4`** | `0x013F12` | `0x00E51C` | `resource_mgr.s:1921`<br>`resource_mgr.s:1824` | — |
| **`RESMGR_LOOP_5`** | `0x013F24` | `0x00E52E` | `resource_mgr.s:1939`<br>`resource_mgr.s:1841` | — |
| **`RESMGR_LOOP_6`** | `0x01405E` | `0x00E668` | `resource_mgr.s:2163`<br>`resource_mgr.s:2056` | — |
| **`RESMGR_LOOP_7`** | `0x014060` | `0x00E66A` | `resource_mgr.s:2165`<br>`resource_mgr.s:2058` | — |
| **`RESMGR_NEXT`** | `0x013E66` | `0x00E470` | `resource_mgr.s:1756`<br>`resource_mgr.s:1675` | — |
| **`RESMGR_NEXT_2`** | `0x013ED4` | `0x00E4DE` | `resource_mgr.s:1849`<br>`resource_mgr.s:1757` | RESMGR_NEXT_2 - follow chain link to next map |
| **`RESMGR_NO`** | `0x013FBA` | `0x00E5C4` | `resource_mgr.s:2052`<br>`resource_mgr.s:1948` | — |
| **`RESMGR_OK`** | `0x013FCE` | `0x00E5D8` | `resource_mgr.s:2067`<br>`resource_mgr.s:1962` | RESMGR_OK - splice: replace A1 with A2 in predecessor's next link |
| **`RESMGR_OK_2`** | `0x013FD4` | `0x00E5DE` | `resource_mgr.s:2075`<br>`resource_mgr.s:1969` | RESMGR_OK_2 - target was TopMapHndl: replace it |
| **`RESMGR_OK_3`** | `0x01408A` | `0x00E694` | `resource_mgr.s:2196`<br>`resource_mgr.s:2087` | RESMGR_OK_3 - RestoreCachedSearch: fast path using cached search state Restores the last search position from RMgr globals. If the handle at the cached ref entry still matches, returns immediately. Ot... |
| **`RESMGR_OK_4`** | `0x014102` | `0x00E70C` | `resource_mgr.s:2277`<br>`resource_mgr.s:2160` | RESMGR_OK_4 - LoadROMResource: load resource from ROM (no file I/O) For ROM map resources, the data offset is relative to ROMBase. Creates a "fake" handle by using HandleZone to get the zone, then com... |
| **`RESMGR_SKIP`** | `0x013E60` | `0x00E46A` | `resource_mgr.s:1753`<br>`resource_mgr.s:1672` | GetNamedResource (continued): the name did not match -- try the next entry of the same type (RETURNS_28), then the next map (RETURNS_22; there is none for Get1NamedResource). |
| **`RESMGR_SKIP_2`** | `0x013E82` | `0x00E48C` | `resource_mgr.s:1772`<br>`resource_mgr.s:1685` | — |
| **`RESMGR_SKIP_3`** | `0x013F84` | `0x00E58E` | `resource_mgr.s:2018`<br>`resource_mgr.s:1916` | — |
| **`RESMGR_SKIP_4`** | `0x014018` | `0x00E622` | `resource_mgr.s:2124`<br>`resource_mgr.s:2018` | — |
| **`ResolveFontFamSize`** | — | `0x019220` | `font_mgr.s:146` | ResolveFontFamSize -- resolve (family, size) defaults from a font input A3 -> font input record (CurFMFamily / FOutFamily layout): +0 W familyID (0 -> system font) +2 W size     (0 -> default size) Re... |
| **`ResolveFontFamSize_DefSize`** | — | `0x019230` | `font_mgr.s:153` | — |
| **`ResolveFontFamSize_Done`** | — | `0x01924C` | `font_mgr.s:166` | — |
| **`ResolveFontFamSize_GotSize`** | — | `0x019238` | `font_mgr.s:157` | — |
| **`ResolveFontFamSize_Pack`** | — | `0x019242` | `font_mgr.s:161` | — |
| **`RESOURCE_MAP`** | `0x013354` | — | `resource_mgr.s:87` | **Proto:** `The "1" variants (Count1Resources, Get1IxResource (Pascal:`<br>Resource Manager Apple source: ResourceMgr.a (MacSEROM.lst module RMGR). In ROM order: the empty-map template RESOURCE_MAP, InitResources, SuperLoad, NewMap, RsrcZoneInit; the file calls (CreateResFil... |
| **`RESOURCEPURGE_HOOK`** | — | `0x00EAF6` | `resource_mgr.s:2821` | RESOURCEPURGE_HOOK -- SetResPurge purge-proc trampoline. Installed as the zone's purge proc. On purge, looks up the handle in the resource map; if it's a resource and resChanged is set, writes it back... |
| **`RestorePort`** | `0x0114D8` | `0x00BB2C` | `window_mgr.s:604` | RestorePort - restore the port saved by GetSetWPort Called during boot. |
| **`RESTOREPORT`** | `0x0114D8` | `0x00BB2C` | `window_mgr.s:561` | RESTOREPORT - restore the port saved by SETWPORT Called by: SHOWHIDE, NEWWINDOW_EXIT, CLOSEWINDOW_NO, SETWTITLE_SKIP, MOVEWINDOW_SKIP_2 (and 9 more) |
| **`RETURNS_15`** | `0x01532A` | `0x00F958` | `dialog_mgr.s:1655`<br>`dialog_mgr.s:1624` | RETURNS_15 - Main dialog event dispatcher Called from DialogSelect to process one event in a dialog. Dispatches on event.what from -0x4C(A6): 1=mouseDown, 3=keyDown, 5=keyDown(autoKey), 6=updateEvt, 8... |
| **`RETURNS_16`** | `0x012830` | — | `menu_mgr.s:1014` | RETURNS_16: find Nth menu item in MenuInfo data A0 = dereferenced MenuHandle, D0 = item number (1-based) Returns: A0 = ptr to item title, A1 = ptr to item attributes (icon,key,mark,style) D0/A0/A1 = 0... |
| **`RETURNS_17`** | `0x012856` | `0x00CE82` | `menu_mgr.s:1045`<br>`menu_mgr.s:813` | RETURNS_17 Called during boot (22,222 times in 30s trace). Found item entry point: A1 points to item title Returns: A0 = title ptr, A1 = attribute bytes after title |
| **`RETURNS_18`** | `0x0129BA` | — | `menu_mgr.s:1314` | RETURNS_18 RETURNS_18: test if menu item D4 is enabled (checks both item bit and menu bit 0) A3 = MenuHandle, D4 = item number Returns: Z=1 if disabled (either item bit or menu-global bit 0 is clear) |
| **`RETURNS_19`** | `0x012AFE` | `0x00D12A` | `menu_mgr.s:1561`<br>`menu_mgr.s:1259` | RETURNS_19 - clamp an insertion point to the menu's item count Apple source name: GetGoodIndex (System 7.1 MenuMgr.a) Called during boot. D6 = desired insertion position, A3 = MenuHandle Returns: D5 =... |
| **`RETURNS_20`** | `0x013E88` | `0x00E492` | `resource_mgr.s:1784`<br>`resource_mgr.s:1696` | RETURNS_20 - SetupMapScan: begin resource map chain traversal If RMgrCurOnly is set, searches only the current map (via RETURNS_21). Otherwise starts from the topmost (most recently opened) resource f... |
| **`RETURNS_21`** | `0x013E9C` | `0x00E4A6` | `resource_mgr.s:1800`<br>`resource_mgr.s:1711` | RETURNS_21 - FindMapByRefNum: locate map handle for a given refNum Walks the resource chain from TopMapHndl to find the map whose file refNum matches D6. refNum=0 means System file (SysMap). Returns: ... |
| **`RETURNS_22`** | `0x013ECA` | `0x00E4D4` | `resource_mgr.s:1839`<br>`resource_mgr.s:1748` | RETURNS_22 - NextMap: advance to next resource map in chain If searching current map only, returns NIL (end of search). Otherwise follows the nextMap chain link to the next open resource file. Returns... |
| **`RETURNS_23`** | `0x013EE6` | `0x00E4F0` | `resource_mgr.s:1866`<br>`resource_mgr.s:1773` | RETURNS_23 - GetTypeList: set up type list pointer for current map Dereferences the map handle and advances to the type list. The map's mTypes field (+$18) holds the offset to the type list. Returns: ... |
| **`RETURNS_24`** | `0x013F06` | `0x00E510` | `resource_mgr.s:1905`<br>`resource_mgr.s:1809` | RETURNS_24 - GetFirstType: get first type entry and its ref list Sets up A3=type list, A2=first ref list, D3=first resType, D4=count-1. Returns: N flag set if type list is empty (D5 < 0). |
| **`RETURNS_25`** | `0x013F10` | `0x00E51A` | `resource_mgr.s:1919`<br>`resource_mgr.s:1822` | RETURNS_25 - FindResID: search ref list for resource by ID Scans the reference list entries (12 bytes each) looking for a resource whose ID (at ref+0) matches D2. Returns: A2=matching ref entry if fou... |
| **`RETURNS_26`** | `0x013F1E` | `0x00E528` | `resource_mgr.s:1935`<br>`resource_mgr.s:1837` | RETURNS_26 - FindResType: search type list for matching resource type Scans the type list (8-byte entries) for a type matching D3. Returns: A2=matching type entry if found; branches to RESMGR_ERR if n... |
| **`RETURNS_27`** | `0x013F30` | `0x00E53A` | `resource_mgr.s:1954`<br>`resource_mgr.s:1855` | RETURNS_27 - GetRefList: get reference list for a type entry Given A2 pointing to a type entry, loads the count and computes the absolute pointer to its reference list. Returns: D4=count-1, A2=pointer... |
| **`RETURNS_28`** | `0x0140E0` | `0x00E6EA` | `resource_mgr.s:2256`<br>`resource_mgr.s:2140` | **Regs:** `RETURNS_28 - NextRefEntry: advance to next reference entry`<br>RETURNS_28 - NextRefEntry: advance to next reference entry Advances A2 by 12 bytes (one ref entry). If the current type's ref list is exhausted, moves to the next type in the type list. Returns: Z=1 i... |
| **`RMGR`** | — | `0x00D958` | `resource_mgr.s:86` | **Proto:** `The "1" variants (Count1Resources, Get1IxResource (Pascal:`<br>Resource Manager Apple source: ResourceMgr.a (MacSEROM.lst module RMGR). In ROM order: InitResources, SuperLoad, NewMap, CLOSEDIALOG_LOOP; the file calls (CreateResFile, OpenResFile, OpenRFPerm, UseRe... |
| **`RmveReference`** | `0x01452E` | `0x00EB52` | `resource_mgr.s:3040` | **Proto:** `PROCEDURE RmveReference(theResource: Handle)`<br>_RmveReference ($A9AE): obsolete trap, kept as a stub that always fails PROCEDURE RmveReference(theResource: Handle) (signature as given in System 7.1 ResourceMgr.a) Pops the 4-byte handle parameter a... |
| **`RMVEREFERENCE`** | `0x01452E` | `0x00EB52` | `resource_mgr.s:2880` | _RmveReference ($A9CC) -- vestigial, returns rmvRefFailed (-197). |
| **`RmveResource`** | `0x0146E8` | `0x00ED0A` | `resource_mgr.s:3280` | _RmveResource ($A9AD) |
| **`RMVERESOURCE`** | `0x0146E8` | `0x00ED0A` | `resource_mgr.s:3120` | _RmveResource ($A9AD) -- remove a resource from its file. Stack: handle(L). Removes the ref entry, deletes the name entry, and (if last ref of type) removes the type entry. Compacts the ref/type lists... |
| **`RMVERESOURCE_CONT`** | `0x0147B2` | `0x00EDD4` | `resource_mgr.s:3370`<br>`resource_mgr.s:3215` | RMVERESOURCE_CONT Called during boot. |
| **`RMVERESOURCE_CONT_2`** | `0x0147C4` | `0x00EDE6` | `resource_mgr.s:3378`<br>`resource_mgr.s:3223` | — |
| **`RMVERESOURCE_CONT_3`** | `0x0147E2` | — | `resource_mgr.s:3398` | RMVERESOURCE_CONT_3 Called during boot. |
| **`RMVERESOURCE_CONT_4`** | `0x0147F8` | `0x00EE1A` | `resource_mgr.s:3412`<br>`resource_mgr.s:3261` | RMVERESOURCE_CONT_4 Called during boot. |
| **`RMVERESOURCE_CONT_5`** | `0x01480E` | `0x00EE30` | `resource_mgr.s:3427`<br>`resource_mgr.s:3280` | RMVERESOURCE_CONT_5 Called during boot. |
| **`RMVERESOURCE_DONE`** | `0x0147DC` | `0x00EDFE` | `resource_mgr.s:3389`<br>`resource_mgr.s:3234` | — |
| **`RMVERESOURCE_EMPTY`** | `0x01477A` | `0x00ED9C` | `resource_mgr.s:3341`<br>`resource_mgr.s:3184` | RMVERESOURCE_EMPTY Called during boot. |
| **`RMVERESOURCE_LOOP`** | `0x014842` | `0x00EE64` | `resource_mgr.s:3448`<br>`resource_mgr.s:3301` | — |
| **`RMVERESOURCE_NO`** | `0x01473C` | `0x00ED5E` | `resource_mgr.s:3309`<br>`resource_mgr.s:3150` | — |
| **`RMVERESOURCE_NO_2`** | `0x01484C` | `0x00EE6E` | `resource_mgr.s:3452`<br>`resource_mgr.s:3305` | — |
| **`RMVERESOURCE_OK`** | `0x0147A8` | `0x00EDCA` | `resource_mgr.s:3360`<br>`resource_mgr.s:3203` | — |
| **`RMVERESOURCE_SKIP`** | `0x014760` | `0x00ED82` | `resource_mgr.s:3324`<br>`resource_mgr.s:3165` | — |
| **`RMVERESOURCE_SKIP_2`** | `0x01476E` | `0x00ED90` | `resource_mgr.s:3330`<br>`resource_mgr.s:3171` | — |
| **`RMVERESOURCE_SKIP_3`** | `0x014772` | `0x00ED94` | `resource_mgr.s:3332`<br>`resource_mgr.s:3173` | — |
| **`RMVERESOURCE_SKIP_4`** | `0x014858` | `0x00EE7A` | `resource_mgr.s:3456`<br>`resource_mgr.s:3309` | — |
| **`RsrcMapEntry`** | `0x01489A` | `0x00EEBC` | `resource_mgr.s:3540` | **Proto:** `Pascal: FUNCTION RsrcMapEntry(theResource: Handle): LONGINT;`<br>**Regs:** `Entry: 4(SP).L = theResource, 8(SP).L = space for the function result Exit:  function result = offset of the reference entry from the start`<br>_RsrcMapEntry ($A9C5): offset of a resource's reference entry in its map Pascal: FUNCTION RsrcMapEntry(theResource: Handle): LONGINT; Entry: 4(SP).L = theResource, 8(SP).L = space for the function res... |
| **`RSRCMAPENTRY`** | `0x01489A` | `0x00EEBC` | `resource_mgr.s:3360` | _RsrcMapEntry ($A9C5) -- get offset of ref entry from map base. Stack: handle(L) -> offset(L). Returns ref entry's relative offset (24-bit). Used for low-level resource manipulation. |
| **`RsrcZoneInit`** | `0x013708` | `0x00DD04` | `resource_mgr.s:560` | _RsrcZoneInit ($A996) Called during boot. |
| **`RSRCZONEINIT`** | `0x013708` | `0x00DD04` | `resource_mgr.s:562` | RSRCZONEINIT ($A996) -- prepare resource manager for new app zone. Closes all resource files above the system map, then walks the system map's reference list and clears the cached handle for any resou... |
| **`RSRCZONEINIT_CONT`** | `0x01372A` | `0x00DD26` | `resource_mgr.s:572`<br>`resource_mgr.s:574` | — |
| **`RSRCZONEINIT_CONT_2`** | `0x01374C` | `0x00DD48` | `resource_mgr.s:605`<br>`resource_mgr.s:611` | RSRCZONEINIT_CONT_2 Called during boot. |
| **`RSRCZONEINIT_DONE`** | `0x01374A` | `0x00DD46` | `resource_mgr.s:597`<br>`resource_mgr.s:599` | RSRCZONEINIT_DONE Called during boot. |
| **`RSRCZONEINIT_ERR`** | `0x013732` | — | `resource_mgr.s:575` | — |
| **`RSRCZONEINIT_EXIT`** | — | `0x00DD2E` | `resource_mgr.s:577` | — |
| **`RSRCZONEINIT_LOOP`** | `0x01371E` | `0x00DD1A` | `resource_mgr.s:568`<br>`resource_mgr.s:570` | — |
| **`RSRCZONEINIT_NEXT`** | `0x013736` | `0x00DD32` | `resource_mgr.s:583`<br>`resource_mgr.s:586` | RSRCZONEINIT_NEXT Called during boot. |
| **`SACT_BUILD_EVT`** | `0x011156` | `0x00B744` | `toolbox_event.s:398`<br>`toolbox_event.s:376` | — |
| **`SACT_DO_DEACT`** | `0x0111A8` | `0x00B796` | `toolbox_event.s:439`<br>`toolbox_event.s:414` | Deactivation pending: start with deactivate (activeFlag = 0) |
| **`SACT_HAS_EVENT`** | `0x011198` | `0x00B786` | `toolbox_event.s:424`<br>`toolbox_event.s:402` | — |
| **`SACT_MARK_DEACT`** | `0x0111A0` | `0x00B78E` | `toolbox_event.s:434`<br>`toolbox_event.s:410` | Mark deactivate as consumed |
| **`SACT_NO_EVENT`** | `0x01119C` | `0x00B78A` | `toolbox_event.s:429`<br>`toolbox_event.s:406` | No pending activate/deactivate events |
| **`SACT_SET_MODS`** | `0x01117C` | `0x00B76A` | `toolbox_event.s:414`<br>`toolbox_event.s:392` | — |
| **`SANE_HALT_HANDLER`** | `0x016FD2` | `0x01A040` | `package_mgr.s:65`<br>`package_mgr.s:62` | SANE_HALT_HANDLER - SANE floating-point halt handler (dsNoPk) Default FP halt vector installed by InitAllPacks. Triggers system error dsNoPk ($10 = 16). |
| **`SaveOld`** | `0x01140E` | `0x00BA62` | `window_mgr.s:489` | **Proto:** `Pascal: procedure SaveOld(theWindow: WindowPeek);`<br>_SaveOld ($A90E) _SaveOld ($A90E): snapshot a window's strucRgn and contRgn before changes Pascal: procedure SaveOld(theWindow: WindowPeek); Saves copies to OldStructure/OldContent globals for DrawNew... |
| **`SAVEOLD`** | `0x01140E` | `0x00BA62` | `window_mgr.s:454` | **Proto:** `Pascal: procedure SaveOld(theWindow: WindowPeek);`<br>_SaveOld ($A90E): snapshot a window's strucRgn and contRgn before changes Pascal: procedure SaveOld(theWindow: WindowPeek); Saves copies to OldStructure/OldContent globals for DrawNew comparison |
| **`ScaleFVal`** | `0x00F2D8` | `0x019EAA` | `font_mgr.s:1845`<br>`font_mgr.s:1650` | ScaleFVal: (A2)+ = FixMul(factor, FixMul(Fixed((A0)+), FixRatio(4(A1), (A1)))); factor = D1 if FScaleDisable, else 1.0 |
| **`ScaleVFVal`** | `0x00F2D0` | `0x019EA2` | `font_mgr.s:1840`<br>`font_mgr.s:1647` | **Regs:** `Entry: A0 -> INTEGER metric in the font record, A2 -> Fixed result Exit:  A0 += 2, A2 += 4; D0-D1/A1 trashed`<br>ScaleVFVal - scale one vertical font metric (FontMetrics helper) Entry: A0 -> INTEGER metric in the font record, A2 -> Fixed result Exit:  A0 += 2, A2 += 4; D0-D1/A1 trashed Sets D1 = FScaleVFact, A1 ... |
| **`SCRAP_APPEND`** | `0x016F72` | `0x0127BC` | `scrap_mgr.s:413`<br>`scrap_mgr.s:326` | set up IOParam for file positioning at end of current scrap write the 8-byte entry header: [theType(4) + length(4)] write the data bytes, padded to even length update ScrapSize to new total SCRAP_APPE... |
| **`SCRAP_ENSURE_INIT`** | `0x016F38` | `0x012782` | `scrap_mgr.s:358`<br>`scrap_mgr.s:292` | SCRAP_ENSURE_INIT - ensure scrap is initialized before read/write If ScrapState < 0 (uninitialized), calls ZeroScrap to create an empty scrap, then reloads globals via SCRAP_LOAD_GLOBALS. |
| **`SCRAP_EXIT`** | `0x016E42` | `0x01268C` | `scrap_mgr.s:135`<br>`scrap_mgr.s:121` | SCRAP_EXIT - common exit for Scrap Manager trap routines Stores D0 (result code) into stack frame result, restores registers, unlinks frame. D0 = byte count to strip from stack for parameters (0 for U... |
| **`SCRAP_EXIT_STRIP`** | `0x016E4A` | `0x012694` | `scrap_mgr.s:139`<br>`scrap_mgr.s:125` | — |
| **`SCRAP_IOPARAM_A0`** | `0x016E78` | `0x0126C2` | `scrap_mgr.s:192`<br>`scrap_mgr.s:165` | SCRAP_IOPARAM_A0 -- set up IOParam: buffer=*handle, count=D0. |
| **`SCRAP_IOPARAM_HDL`** | `0x016E76` | `0x0126C0` | `scrap_mgr.s:189`<br>`scrap_mgr.s:162` | ScrapState=0: scrap is on disk, load it into memory SCRAP_IOPARAM_HDL - set up IOParam for Read/Write using ScrapHandle buffer SCRAP_IOPARAM_HDL entry: dereferences ScrapHandle (D5) for ioBuffer. SCRA... |
| **`SCRAP_LOAD_GLOBALS`** | `0x016DCE` | `0x012618` | `scrap_mgr.s:69`<br>`scrap_mgr.s:68` | SCRAP_LOAD_GLOBALS -- reload scrap globals into registers. |
| **`SCRAP_NOERR`** | `0x016E40` | `0x01268A` | `scrap_mgr.s:125`<br>`scrap_mgr.s:110` | ScrapState > 0: scrap is in memory, write it to disk |
| **`SCRAP_OPEN_FILE`** | `0x016DF4` | `0x01263E` | `scrap_mgr.s:81`<br>`scrap_mgr.s:80` | ScrapState=0: scrap is on disk, open Clipboard File |
| **`SCRAP_READ_DATA`** | `0x016EBE` | `0x012708` | `scrap_mgr.s:255`<br>`scrap_mgr.s:212` | SCRAP_READ_DATA - read D0 bytes from scrap at offset D3 into buffer A1 If scrap is in memory (D6 > 0): BlockMove from *ScrapHandle+D3. If scrap is on disk (D6 = 0): Read from Clipboard File at offset ... |
| **`SCRAP_READ_FILE`** | `0x016ECC` | `0x012716` | `scrap_mgr.s:269`<br>`scrap_mgr.s:224` | scrap in memory: copy via BlockMove SCRAP_READ_FILE - read from Clipboard File at position D3 |
| **`SCRAP_RTS`** | `0x016E58` | `0x0126A2` | `scrap_mgr.s:153`<br>`scrap_mgr.s:138` | — |
| **`SCRAP_RTS_OK`** | `0x016E56` | `0x0126A0` | `scrap_mgr.s:151`<br>`scrap_mgr.s:136` | SCRAP_RTS_OK - return noErr (scrap not on disk, or directory not found) Called during boot. |
| **`SCRAP_SETUP`** | `0x016DC2` | `0x01260C` | `scrap_mgr.s:63`<br>`scrap_mgr.s:62` | SCRAP_SETUP - common Scrap Manager setup routine Creates a stack frame with a local IOParam block (-0x50(A6)) and loads all scrap globals into registers. If scrap is on disk (ScrapState=0), opens the ... |
| **`SCRAP_WRITE_FILE`** | `0x016F82` | `0x0127CC` | `scrap_mgr.s:427`<br>`scrap_mgr.s:334` | scrap in memory: append bytes to handle SCRAP_WRITE_FILE - write to Clipboard File at offset D4 (scrap on disk) |
| **`SCRAPMGR`** | — | `0x0125F6` | `scrap_mgr.s:36` | **Proto:** `Pascal: function InfoScrap: PScrapStuff;`<br>Scrap Manager - InfoScrap, UnloadScrap, LodeScrap, ZeroScrap, GetScrap, PutScrap Manages the desk scrap (clipboard) for cut/copy/paste between applications. The scrap lives either in memory (ScrapStat... |
| **`SCSI_POLL_EXIT`** | — | `0x00B7E2` | `toolbox_event.s:452` | — |
| **`SCSI_POLL_SELECT`** | — | `0x00B7BC` | `toolbox_event.s:439` | — |
| **`SE_SCSI_BG_POLL`** | — | `0x00B79A` | `toolbox_event.s:424` | SE_SCSI_BG_POLL - SE-specific SCSI background poll Called from TBOX_GET_EVENT every 1200 ticks (20 sec) when SCSIPoll bit 7 is set. Uses SCSIDispatch selectors 1,2,3,4 (SCSIReset/Selct/Cmd/Read) to pr... |
| **`SelectWindow`** | `0x011BF4` | `0x00C28E` | `window_mgr.s:1705` | _SelectWindow ($A91F) stack: window -> (brings to front, highlights) _SelectWindow ($A91F): bring a window to front and activate it Deactivates old front window, brings target to front, activates it |
| **`SELECTWINDOW`** | `0x011BF4` | `0x00C28E` | `window_mgr.s:1588` | _SelectWindow ($A91F): bring a window to front and activate it Deactivates old front window, brings target to front, activates it. |
| **`SELECTWINDOW_CONT`** | `0x011BF8` | `0x00C292` | `window_mgr.s:1708`<br>`window_mgr.s:1591` | SELECTWINDOW_CONT -- select/bring to front. |
| **`SELECTWINDOW_EMPTY`** | `0x011C20` | `0x00C2BA` | `window_mgr.s:1727`<br>`window_mgr.s:1610` | — |
| **`SELECTWINDOW_NO`** | `0x011C10` | `0x00C2AA` | `window_mgr.s:1719`<br>`window_mgr.s:1602` | SELECTWINDOW_NO -- activate the new front window. |
| **`SELECTWINDOW_OK`** | `0x011C1A` | `0x00C2B4` | `window_mgr.s:1723`<br>`window_mgr.s:1606` | — |
| **`SelIText`** | `0x014F38` | `0x00F568` | `dialog_mgr.s:992` | Sel I Text |
| **`SELITEXT`** | `0x014F38` | `0x00F568` | `dialog_mgr.s:991` | _SelIText ($A97E) -- select text range in EditText item. Stack: theDialog(L), itemNo(W), selStart(W), selEnd(W). Calls DLG_SwitchActiveField to activate text edit and select the specified range. |
| **`SELITEXT_CONT`** | `0x014F60` | `0x00F590` | `dialog_mgr.s:1011`<br>`dialog_mgr.s:1017` | SELITEXT_CONT -- compute inset rect on stack. SELITEXT_CONT |
| **`SELITEXT_OK`** | `0x014F7A` | `0x00F5AA` | `dialog_mgr.s:1022`<br>`dialog_mgr.s:1028` | — |
| **`SelView`** | `0x016CCA` | `0x012084` | `textedit.s:1988`<br>`textedit.s:3518` | **Regs:** `Entry: A3 = locked TERec, A4 = TEHandle (caller's StdEntry state)`<br>SelView - local SelView: scroll the selection start into view Entry: A3 = locked TERec, A4 = TEHandle (caller's StdEntry state) Returns at once unless TEFlags bit 6 (auto-view, TEAutoView) is set. Oth... |
| **`SELVIEW_NO_AUTO`** | — | `0x0120E6` | `textedit.s:3553` | — |
| **`SELVIEW_RTS`** | `0x016D2A` | — | `textedit.s:2025` | TempRect = viewRect less one line at the bottom, 1 pixel at the right is the caret position inside TempRect? not visible: (dv,dh) = TempRect.botRight - caret position |
| **`SendBehind`** | `0x011CC0` | `0x00C360` | `window_mgr.s:1828` | **Proto:** `Pascal: procedure SendBehind(theWindow: WindowPtr; behindWindow: WindowPtr);`<br>_SendBehind ($A921) stack: window, behindWindow -> (reorders) _SendBehind ($A921): send a window behind another in the window list Pascal: procedure SendBehind(theWindow: WindowPtr; behindWindow: Wind... |
| **`SENDBEHIND`** | `0x011CC0` | `0x00C360` | `window_mgr.s:1707` | **Proto:** `Pascal: procedure SendBehind(theWindow: WindowPtr; behindWindow: WindowPtr);`<br>_SendBehind ($A921): send a window behind another in the window list Pascal: procedure SendBehind(theWindow: WindowPtr; behindWindow: WindowPtr); If theWindow was front, selects the next visible windo... |
| **`SENDBEHIND_NO`** | `0x011CD6` | `0x00C376` | `window_mgr.s:1838`<br>`window_mgr.s:1717` | target was front: select next visible window |
| **`SENDBEHIND_NO_2`** | `0x011CE8` | — | `window_mgr.s:1846` | — |
| **`SENDBEHIND_REINSERT`** | — | `0x00C388` | `window_mgr.s:1725` | — |
| **`SENDBEHIND_RESTORE`** | — | `0x00C34A` | `window_mgr.s:1686` | — |
| **`SET_CTL_COLOR_ENTRY`** | — | `0x00C87A` | `window_mgr.s:2474` | **Proto:** `Pascal: procedure SetCtlColor(theControl: ControlHandle; newColorTable: CCTabHandle);`<br>_SetCtlColor ($A35D) -- entry: maintain Color QuickDraw aux-control record. Same scaffolding as _SetWinColor but for controls; B&W stub. Pascal: procedure SetCtlColor(theControl: ControlHandle; newCol... |
| **`SetCRefCon`** | `0x012F5A` | `0x00D55E` | `control_mgr.s:323` | **Proto:** `Pascal: procedure SetCRefCon(theControl: ControlHandle; data: LongInt);`<br>Set C Ref Con _SetCRefCon: set control's refCon Pascal: procedure SetCRefCon(theControl: ControlHandle; data: LongInt); |
| **`SETCREFCON`** | `0x012F5A` | `0x00D55E` | `control_mgr.s:280` | **Proto:** `Pascal: procedure SetCRefCon(theControl: ControlHandle; data: LongInt);`<br>_SetCRefCon ($A95B): set control's refCon longword. Pascal: procedure SetCRefCon(theControl: ControlHandle; data: LongInt); |
| **`SETCREFCON_CONT`** | `0x012F5C` | `0x00D560` | `control_mgr.s:325`<br>`control_mgr.s:283` | Shared set-longword body: stack [ret(4), value(4), handle(4)] |
| **`SetCTitle`** | `0x012FDE` | `0x00D5E2` | `control_mgr.s:428` | Set C Title Called during boot. |
| **`SETCTITLE`** | `0x012FDE` | `0x00D5E2` | `control_mgr.s:364` | **Proto:** `Pascal: procedure SetCTitle(theControl: ControlHandle; title: Str255);`<br>_SetCTitle ($A95F): replace a control's title (resizes handle). Pascal: procedure SetCTitle(theControl: ControlHandle; title: Str255); |
| **`SETCTITLE_SKIP`** | `0x013018` | `0x00D61C` | `control_mgr.s:452`<br>`control_mgr.s:388` | — |
| **`SetCtlAction`** | `0x012F6E` | `0x00D572` | `control_mgr.s:347` | Set Ctl Action _SetCtlAction: set control's actionProc |
| **`SETCTLACTION`** | `0x012F6E` | `0x00D572` | `control_mgr.s:295` | _SetCtlAction ($A96B): set control's action proc ptr. |
| **`SETCTLMAX`** | — | `0x00D680` | `control_mgr.s:447` | _SetCtlMax ($A965): set maximum (with clamp on value). |
| **`SETCTLMIN`** | — | `0x00D67C` | `control_mgr.s:443` | _SetCtlMin ($A964): set minimum (with clamp on value). |
| **`SetCtlValue`** | `0x013036` | `0x00D63A` | `control_mgr.s:492` | Set Ctl Value Called during boot. |
| **`SETCTLVALUE`** | `0x013036` | `0x00D63A` | `control_mgr.s:416` | **Proto:** `Pascal: procedure SetCtlValue(theControl: ControlHandle; theValue: INTEGER);`<br>_SetCtlValue ($A963): set value, clamp to [Min, Max], redraw indicator. Pascal: procedure SetCtlValue(theControl: ControlHandle; theValue: INTEGER); |
| **`SETCTLVALUE_CONT`** | `0x013038` | `0x00D63C` | `control_mgr.s:495`<br>`control_mgr.s:419` | SETCTLVALUE_CONT: generic set-word-field with clamping and redraw |
| **`SETCTLVALUE_NO`** | `0x01305C` | `0x00D660` | `control_mgr.s:507`<br>`control_mgr.s:431` | — |
| **`SETCTLVALUE_NO_2`** | `0x013066` | `0x00D66A` | `control_mgr.s:511`<br>`control_mgr.s:435` | — |
| **`SETCTLVALUE_OK`** | `0x013072` | `0x00D676` | `control_mgr.s:515`<br>`control_mgr.s:439` | — |
| **`SetDItem`** | `0x014E80` | `0x00F4B0` | `dialog_mgr.s:902` | Set D Item |
| **`SETDITEM`** | `0x014E80` | `0x00F4B0` | `dialog_mgr.s:896` | _SetDItem ($A98E) -- write item info: type, handle, rect. Stack: theDialog(L), itemNo(W), itemType(B), item(L), box(L). |
| **`SETDITEM_CONT`** | `0x014EB4` | `0x00F4E4` | `dialog_mgr.s:919`<br>`dialog_mgr.s:913` | — |
| **`SETDITEM_RESTORE`** | — | `0x00F4DE` | `dialog_mgr.s:910` | — |
| **`SETDITEM_SKIP`** | `0x014EAE` | — | `dialog_mgr.s:916` | — |
| **`SetFontLock`** | `0x00F1D8` | `0x019E0C` | `font_mgr.s:1693` | **Proto:** `Pascal: procedure SetFontLock(lockFlag: BOOLEAN);`<br>_SetFontLock ($A903) _SetFontLock ($A903): lock/unlock current font in memory Pascal: procedure SetFontLock(lockFlag: BOOLEAN); |
| **`SETFONTLOCK`** | `0x00F1D8` | `0x019E0C` | `font_mgr.s:1577` | **Proto:** `Pascal: procedure SetFontLock(lockFlag: BOOLEAN);`<br>_SetFontLock ($A903): lock/unlock current font in memory Pascal: procedure SetFontLock(lockFlag: BOOLEAN); |
| **`SETFONTLOCK_CONT`** | `0x00F1F8` | — | `font_mgr.s:1707` | unlock: reload if purged, clear purgeable bit |
| **`SETFONTLOCK_EXIT`** | `0x00F1F2` | — | `font_mgr.s:1702` | lock: set purgeable bit to prevent purging |
| **`SETFONTLOCK_PURGE`** | — | `0x019E2A` | `font_mgr.s:1588` | — |
| **`SETFONTLOCK_RTS`** | — | `0x019E32` | `font_mgr.s:1591` | — |
| **`SETFRACTENABLE`** | — | `0x019E42` | `font_mgr.s:1603` | **Proto:** `Pascal: procedure SetFractEnable(fractEnable: BOOLEAN);`<br>_SetFractEnable ($A814): set fractional-widths flag Pascal: procedure SetFractEnable(fractEnable: BOOLEAN); |
| **`SETFSCALE_INVALIDATE`** | — | `0x019E3A` | `font_mgr.s:1598` | — |
| **`SetFScaleDisabl`** | `0x00F260` | — | `font_mgr.s:1771` | **Proto:** `Pascal: PROCEDURE SetFScaleDisable(fontScaleDisable: BOOLEAN);`<br>_SetFScaleDisable ($A834): enable or disable font scaling Pascal: PROCEDURE SetFScaleDisable(fontScaleDisable: BOOLEAN); Stores the Boolean in FScaleDisable ($A63; TRUE = scaling disabled), sets CurFM... |
| **`SetFScaleDisable`** | `0x00F260` | `0x019E34` | `font_mgr.s:1772` | **Proto:** `Pascal: PROCEDURE SetFScaleDisable(fontScaleDisable: BOOLEAN);`<br>_SetFScaleDisable ($A834): enable or disable font scaling Pascal: PROCEDURE SetFScaleDisable(fontScaleDisable: BOOLEAN); Stores the Boolean in FScaleDisable ($A63; TRUE = scaling disabled), sets CurFM... |
| **`SETFSCALEDISABLE`** | `0x00F260` | `0x019E34` | `font_mgr.s:1595` | **Proto:** `Pascal: procedure SetFScaleDisable(fscaleDisable: BOOLEAN);`<br>_SetFScaleDisable ($A834): set scale-disable flag Pascal: procedure SetFScaleDisable(fscaleDisable: BOOLEAN); |
| **`SetItem`** | `0x012BD0` | `0x00D1FC` | `menu_mgr.s:1703` | **Proto:** `Pascal: PROCEDURE SetItem(theMenu: MenuHandle; item: INTEGER;`<br>_SetItem ($A947): change the text of a menu item Pascal: PROCEDURE SetItem(theMenu: MenuHandle; item: INTEGER; itemString: Str255); Entry (after MOVEM): 0x18(SP) = itemString, 0x1C(SP) = item, 0x1E(SP... |
| **`SETITEM`** | `0x012BD0` | `0x00D1FC` | `menu_mgr.s:1380` | **Proto:** `Pascal: procedure SetItem(theMenu: MenuHandle; item: INTEGER; itemString: Str255);`<br>_SetItem ($A947): replace a menu item's text. Pascal: procedure SetItem(theMenu: MenuHandle; item: INTEGER; itemString: Str255); |
| **`SETITEM_CONT`** | `0x012BF0` | — | `menu_mgr.s:1716` | set up Munger parameters to replace old title with new |
| **`SETITEM_FOUND`** | `0x012C0E` | — | `menu_mgr.s:1732` | _Munger: replace D4 bytes at the item with D2 bytes at A2 (D2 = 0: delete) |
| **`SETITEMICON`** | — | `0x00CEDC` | `menu_mgr.s:872` | _SetItemIcon ($A940): D2=0 |
| **`SETITEMMARK`** | — | `0x00CEEC` | `menu_mgr.s:888` | _SetItemMark ($A945): D2=2 |
| **`SETITEMSTYLE`** | — | `0x00CEE4` | `menu_mgr.s:880` | _SetItemStyle ($A942): D2=3 |
| **`SetIText`** | `0x014ED6` | `0x00F506` | `dialog_mgr.s:946` | Set I Text |
| **`SETITEXT`** | `0x014ED6` | `0x00F506` | `dialog_mgr.s:944` | _SetIText ($A98F) -- replace text of EditText/StaticText item. Stack: theItem(L), text(L). Replaces the handle's contents with the new Pascal string via _PtrToXHand. Walks all dialog windows looking f... |
| **`SETITEXT_CLOSE`** | — | `0x00F556` | `dialog_mgr.s:975` | — |
| **`SETITEXT_CONT`** | `0x014F32` | `0x00F562` | `dialog_mgr.s:983`<br>`dialog_mgr.s:981` | — |
| **`SETITEXT_CONT_2`** | `0x014F34` | `0x00F564` | `dialog_mgr.s:985`<br>`dialog_mgr.s:983` | — |
| **`SETITEXT_DONE`** | `0x014F26` | — | `dialog_mgr.s:977` | — |
| **`SETITEXT_NEXT`** | `0x014EEE` | `0x00F51E` | `dialog_mgr.s:955`<br>`dialog_mgr.s:953` | — |
| **`SETITEXT_NEXT_2`** | `0x014EFC` | — | `dialog_mgr.s:960` | — |
| **`SETITEXT_NO`** | `0x014F12` | `0x00F542` | `dialog_mgr.s:969`<br>`dialog_mgr.s:967` | — |
| **`SETITEXT_SKIP`** | `0x014F2A` | `0x00F55A` | `dialog_mgr.s:979`<br>`dialog_mgr.s:977` | — |
| **`SETITEXT_WALK`** | — | `0x00F52C` | `dialog_mgr.s:958` | — |
| **`SetItmIcon`** | `0x0128B0` | — | `menu_mgr.s:1113` | SetItmIcon -- trap handler for _SetItmIcon ($A940). _SetItmIcon ($A940) |
| **`SetItmMark`** | `0x0128C0` | — | `menu_mgr.s:1135` | SetItmMark -- trap handler for _SetItmMark ($A944). _SetItmMark ($A944) |
| **`SetItmStyle`** | `0x0128B8` | — | `menu_mgr.s:1123` | _SetItmStyle ($A942) |
| **`SetMaxCtl`** | `0x01307C` | — | `control_mgr.s:533` | Set Max Ctl Called during boot. |
| **`SetMenuBar`** | `0x0127B2` | `0x00CDA8` | `menu_mgr.s:938` | **Proto:** `SetMenuBar -- _SetMenuBar ($A93C): PROCEDURE SetMenuBar (menuList: Handle);`<br>SetMenuBar -- _SetMenuBar ($A93C): PROCEDURE SetMenuBar (menuList: Handle); _SetMenuBar ($A93C) |
| **`SETMENUBAR`** | `0x0127B2` | `0x00CDA8` | `menu_mgr.s:674` | **Proto:** `Pascal: procedure SetMenuBar(menuList: Handle);`<br>_SetMenuBar ($A93C): restore a saved MenuList. Pascal: procedure SetMenuBar(menuList: Handle); |
| **`SETMENUFLASH`** | — | `0x00D242` | `menu_mgr.s:1416` | **Proto:** `Pascal: procedure SetMenuFlash(count: INTEGER);`<br>_SetMenuFlash ($A94A): set MenuFlash count. Pascal: procedure SetMenuFlash(count: INTEGER); |
| **`SETMENUITEMTEXT_CONT`** | — | `0x00D21C` | `menu_mgr.s:1394` | Shared _Munger splice (entry from DelMenuItem and SetItem). In: A0 = old item ptr, A2/D2 = replacement bytes/length, D4 = old length to remove |
| **`SETMENUITEMTEXT_FOUND`** | — | `0x00D23A` | `menu_mgr.s:1409` | — |
| **`SetMFlash`** | `0x012C16` | — | `menu_mgr.s:1741` | Set M Flash _SetMFlash: set menu flash count (number of blinks on selection) |
| **`SetMinCtl`** | `0x013078` | — | `control_mgr.s:524` | Set Min Ctl Called during boot. |
| **`SetPortFromStyleRun`** | — | `0x012422` | `textedit.s:4031` | SetPortFromStyleRun -- pack styleEntry to TextStyle + emit pen-mode A0 -> styleRun. Looks up its styleEntry, copies its font metrics into teInPort, then emits pen-mode pattern via PackTexturePattern u... |
| **`SETRESATTR_EXIT`** | `0x013858` | — | `resource_mgr.s:754` | — |
| **`SetResAttrs`** | `0x01454C` | `0x00EB70` | `resource_mgr.s:3063` | _SetResAttrs ($A9A7) |
| **`SETRESATTRS`** | `0x01454C` | `0x00EB70` | `resource_mgr.s:2904` | _SetResAttrs ($A9A7) -- write attribute byte for a resource handle. Stack: handle(L), attrs(B). Cannot modify ROM-map resources (they're read-only). Sets mapChanged on the owning map. |
| **`SETRESATTRS_CONT`** | `0x014570` | — | `resource_mgr.s:3081` | SETRESATTRS_CONT Called during boot (4,238 times in 30s trace). |
| **`SETRESATTRS_EXIT`** | `0x01457C` | `0x00EB90` | `resource_mgr.s:3085`<br>`resource_mgr.s:2914` | — |
| **`SETRESATTRS_MARK_CHANGED`** | — | `0x00EA94` | `resource_mgr.s:2753` | — |
| **`SETRESATTRS_RESTORE`** | — | `0x00EA9A` | `resource_mgr.s:2755` | — |
| **`SETRESATTRS_SKIP`** | `0x01456C` | — | `resource_mgr.s:3073` | — |
| **`SetResFileAttrs`** | `0x013844` | `0x00DE46` | `resource_mgr.s:748` | _SetResFileAttrs ($A9F7) Sets the map attributes of the specified resource file. Called during boot. |
| **`SETRESFILEATTRS`** | `0x013844` | `0x00DE46` | `resource_mgr.s:734` | _SetResFileAttrs ($A9F7) -- write map attributes word for a refnum. |
| **`SETRESFILEATTRS_EXIT`** | — | `0x00DE5A` | `resource_mgr.s:740` | — |
| **`SetResInfo`** | `0x0145C4` | `0x00EBE8` | `resource_mgr.s:3140` | _SetResInfo ($A9A9) Called during boot. |
| **`SETRESINFO`** | `0x0145C4` | `0x00EBE8` | `resource_mgr.s:2981` | _SetResInfo ($A9A9) -- update id and name of a resource. Stack: handle(L), id(W), namePtr(L). Reassigns the resource's id in its ref entry. If a non-nil namePtr is provided, calls RMVERESOURCE_CONT_5 ... |
| **`SETRESINFO_CONT`** | `0x014602` | `0x00EC26` | `resource_mgr.s:3166`<br>`resource_mgr.s:3002` | SETRESINFO_CONT - resource is protected |
| **`SETRESINFO_ERR`** | `0x014608` | `0x00EC2C` | `resource_mgr.s:3168`<br>`resource_mgr.s:3004` | SETRESINFO_CONT - resource is protected |
| **`SETRESINFO_SKIP`** | `0x0145F4` | `0x00EC18` | `resource_mgr.s:3156`<br>`resource_mgr.s:2997` | — |
| **`SetResLoad`** | `0x014504` | `0x00EB28` | `resource_mgr.s:2988` | _SetResLoad ($A99B) Called during boot. |
| **`SETRESLOAD`** | `0x014504` | `0x00EB28` | `resource_mgr.s:2859` | _SetResLoad ($A99B) -- set the auto-load flag. Stack: load(B). Updates the global ResLoad flag controlling whether GetResource etc. read data immediately or return empty handles. |
| **`SetResPurge`** | `0x0144E4` | `0x00EB08` | `resource_mgr.s:2967` | _SetResPurge ($A993) |
| **`SETRESPURGE`** | `0x0144E4` | `0x00EB08` | `resource_mgr.s:2838` | _SetResPurge ($A993) -- install/remove resource purge handler. Stack: install(B). If install != 0, replaces zone purgeProc with RESOURCEPURGE_HOOK trampoline so changed resources auto-flush on purge. ... |
| **`SETRESPURGE_CONT`** | `0x0144F4` | `0x00EB18` | `resource_mgr.s:2974`<br>`resource_mgr.s:2845` | — |
| **`SETRESPURGE_EXIT`** | `0x0144FA` | `0x00EB1E` | `resource_mgr.s:2978`<br>`resource_mgr.s:2849` | Called by: SetResLoad, CurResFile, ResError, AddReference, RmveReference |
| **`SetString`** | `0x0111C4` | `0x00B80C` | `window_mgr.s:72` | **Proto:** `Pascal: PROCEDURE SetString(h: StringHandle; theString: Str255)`<br>_SetString ($A907) Pascal: PROCEDURE SetString(h: StringHandle; theString: Str255) Replaces the contents of an existing string handle. |
| **`SETSTRING`** | `0x0111C4` | `0x00B80C` | `window_mgr.s:86` | **Proto:** `Pascal: PROCEDURE SetString(h: StringHandle; theString: Str255)`<br>_SetString ($A907) Pascal: PROCEDURE SetString(h: StringHandle; theString: Str255) Replaces the contents of an existing string handle. |
| **`SETWINCOLOR_ALLOC_NEW`** | — | `0x00C8D4` | `window_mgr.s:2512` | Allocate new aux record (28 bytes), link in front, init key+color. |
| **`SETWINCOLOR_BODY`** | — | `0x00C886` | `window_mgr.s:2479` | Shared body (both SetWinColor and SetCtlColor entries fall here): |
| **`SETWINCOLOR_ENTRY`** | — | `0x00C86C` | `window_mgr.s:2464` | **Proto:** `Pascal: procedure SetWinColor(theWindow: WindowPtr; newColorTable: WCTabHandle);`<br>_SetWinColor ($A809) -- entry: maintain Color QuickDraw aux-window record. On B&W SE FDHD this code maintains the ghost_AuxWinHead linked list but the records are unused by the B&W WMgr; provided for ... |
| **`SETWINCOLOR_EXIT`** | — | `0x00C8C8` | `window_mgr.s:2505` | Common exit: unwind frame and return. |
| **`SETWINCOLOR_FIND_TO_DEL`** | — | `0x00C8EC` | `window_mgr.s:2522` | Default-color path: walk list, unlink and dispose record matching key. |
| **`SETWINCOLOR_UNLINK_DISP`** | — | `0x00C902` | `window_mgr.s:2533` | — |
| **`SETWINCOLOR_WALK_LOOP`** | — | `0x00C8EE` | `window_mgr.s:2524` | — |
| **`SetWindowPic`** | `0x011882` | `0x00BEE8` | `window_mgr.s:1151` | **Proto:** `Pascal: procedure SetWindowPic(theWindow: WindowPtr; pic: PicHandle);`<br>_SetWindowPic ($A92E): set window's auto-draw picture handle Pascal: procedure SetWindowPic(theWindow: WindowPtr; pic: PicHandle); |
| **`SETWINDOWPIC`** | `0x011882` | `0x00BEE8` | `window_mgr.s:1073` | **Proto:** `Pascal: procedure SetWindowPic(theWindow: WindowPtr; pic: PicHandle);`<br>_SetWindowPic ($A92E): set window's auto-draw picture handle Pascal: procedure SetWindowPic(theWindow: WindowPtr; pic: PicHandle); |
| **`SETWPORT`** | — | `0x00BB22` | `window_mgr.s:551` | SETWPORT (= GetSetWPort) - save current GrafPort in D4, switch to WMgr port (A5) points to CurrentA5 -> thePort. Saves old port in D4 and sets thePort to WMgrPort for window manager drawing. Called by... |
| **`SetWRefCon`** | `0x011872` | `0x00BED8` | `window_mgr.s:1137` | **Proto:** `Pascal: procedure SetWRefCon(theWindow: WindowPtr; data: LongInt);`<br>_SetWRefCon ($A918): set window's refCon value Pascal: procedure SetWRefCon(theWindow: WindowPtr; data: LongInt); |
| **`SETWREFCON`** | `0x011872` | `0x00BED8` | `window_mgr.s:1060` | **Proto:** `Pascal: procedure SetWRefCon(theWindow: WindowPtr; data: LongInt);`<br>_SetWRefCon ($A918): set window's refCon value Pascal: procedure SetWRefCon(theWindow: WindowPtr; data: LongInt); |
| **`SETWREFCON_CONT`** | `0x011876` | `0x00BEDC` | `window_mgr.s:1139`<br>`window_mgr.s:1062` | — |
| **`SetWTitle`** | `0x0118A6` | `0x00BF0C` | `window_mgr.s:1188` | **Proto:** `Pascal: procedure SetWTitle(theWindow: WindowPtr; title: Str255);`<br>_SetWTitle ($A91A): change a window's title Pascal: procedure SetWTitle(theWindow: WindowPtr; title: Str255); Saves old strucRgn, updates title, recalculates regions, repaints if structure changed (ti... |
| **`SETWTITLE`** | `0x0118A6` | `0x00BF0C` | `window_mgr.s:1107` | **Proto:** `Pascal: procedure SetWTitle(theWindow: WindowPtr; title: Str255);`<br>_SetWTitle ($A91A): change a window's title Pascal: procedure SetWTitle(theWindow: WindowPtr; title: Str255); Saves old strucRgn, updates title, recalculates regions, repaints if structure changed (ti... |
| **`SETWTITLE_CONT`** | `0x011918` | `0x00BF7E` | `window_mgr.s:1248`<br>`window_mgr.s:1163` | SETWTITLE_CONT - subtract content region from D3 (leaving frame-only area) |
| **`SETWTITLE_EXIT`** | `0x011914` | `0x00BF7A` | `window_mgr.s:1241`<br>`window_mgr.s:1157` | — |
| **`SETWTITLE_NO`** | `0x0118F0` | `0x00BF56` | `window_mgr.s:1224`<br>`window_mgr.s:1140` | check if structure region changed (title may affect frame size) regions equal: just repaint this window's frame SETWTITLE_NO - strucRgn changed: repaint old+new area and windows behind |
| **`SETWTITLE_SKIP`** | `0x011908` | `0x00BF6E` | `window_mgr.s:1236`<br>`window_mgr.s:1152` | — |
| **`ShowControl`** | `0x012ED6` | `0x00D4DA` | `control_mgr.s:235` | _ShowControl ($A957) Called during boot. |
| **`SHOWCONTROL`** | `0x012ED6` | `0x00D4DA` | `control_mgr.s:202` | **Proto:** `Pascal: procedure ShowControl(theControl: ControlHandle);`<br>_ShowControl ($A957): make a control visible (and draw it). Pascal: procedure ShowControl(theControl: ControlHandle); |
| **`SHOWCONTROL_CONT`** | `0x012EE8` | `0x00D4EC` | `control_mgr.s:242`<br>`control_mgr.s:209` | — |
| **`SHOWCONTROL_EXIT`** | `0x012EEE` | `0x00D4F2` | `control_mgr.s:245`<br>`control_mgr.s:214` | Common exit for control routines that pushed A3. Called by: HIDECONTROL, DISPOSECONTROL, KILLCONTROLS_EMPTY, SHOWCONTROL |
| **`ShowDItem`** | `0x014FF0` | `0x00F620` | `dialog_mgr.s:1100` | **Proto:** `Pascal: PROCEDURE ShowDItem(theDialog: DialogPtr; itemNo: INTEGER);`<br>_ShowDItem ($A828): show a dialog item that HideDItem has hidden Pascal: PROCEDURE ShowDItem(theDialog: DialogPtr; itemNo: INTEGER); Entry (after the MODALDIALOG_CONT_3 prologue): 0x8(A6) = itemNo, 0x... |
| **`SHOWDITEM`** | `0x014FF0` | `0x00F620` | `dialog_mgr.s:1089` | _ShowDItem ($A828) -- show a hidden dialog item. Stack: theDialog(L), itemNo(W). Subtracts 0x4000 from coords to bring item back onscreen. MoveControl with visible flag temporarily cleared (to avoid d... |
| **`SHOWDITEM_CONT`** | `0x015044` | `0x00F674` | `dialog_mgr.s:1136`<br>`dialog_mgr.s:1124` | SHOWDITEM_CONT - common part of HideDItem/ShowDItem (Apple: ShowHideCmn) If no editText item is active, activates the first visible one (CLOSEDIALOG_CONT_5) with the insertion point at its start. Retu... |
| **`SHOWDITEM_SKIP`** | `0x015042` | `0x00F672` | `dialog_mgr.s:1126`<br>`dialog_mgr.s:1115` | — |
| **`SHOWDITEM_SKIP_2`** | `0x015058` | `0x00F688` | `dialog_mgr.s:1144`<br>`dialog_mgr.s:1132` | — |
| **`SHOWDITEM_SKIP_3`** | `0x01505A` | `0x00F68A` | `dialog_mgr.s:1146`<br>`dialog_mgr.s:1134` | — |
| **`ShowHide`** | `0x01149C` | `0x00BAF0` | `window_mgr.s:565` | **Proto:** `Pascal: procedure ShowHide(theWindow: WindowPtr; showFlag: BOOLEAN);`<br>_ShowHide ($A908) _ShowHide ($A908): set window visibility and update screen Pascal: procedure ShowHide(theWindow: WindowPtr; showFlag: BOOLEAN); Only acts if visibility is actually changing (XOR test... |
| **`SHOWHIDE`** | `0x01149C` | `0x00BAF0` | `window_mgr.s:524` | **Proto:** `Pascal: procedure ShowHide(theWindow: WindowPtr; showFlag: BOOLEAN);`<br>_ShowHide ($A908): set window visibility and update screen Pascal: procedure ShowHide(theWindow: WindowPtr; showFlag: BOOLEAN); Only acts if visibility is actually changing (XOR test). |
| **`SHOWHIDE_SKIP`** | `0x0114C8` | `0x00BB1C` | `window_mgr.s:582`<br>`window_mgr.s:541` | — |
| **`ShowWindow`** | `0x011812` | `0x00BE78` | `window_mgr.s:1060` | _ShowWindow ($A915) stack: window -> (makes window visible) _ShowWindow ($A915): make a window visible If this would be the frontmost visible window, also selects it |
| **`SHOWWINDOW`** | `0x011812` | `0x00BE78` | `window_mgr.s:990` | _ShowWindow ($A915): make a window visible If this would be the frontmost visible window, also selects it. |
| **`SHOWWINDOW_FOUND`** | `0x01182A` | `0x00BE90` | `window_mgr.s:1072`<br>`window_mgr.s:1002` | show the window (another visible window is already in front) |
| **`SHOWWINDOW_NO`** | `0x011816` | `0x00BE7C` | `window_mgr.s:1063`<br>`window_mgr.s:993` | find first visible window in front of target |
| **`SHOWWINDOW_OK`** | `0x011834` | `0x00BE9A` | `window_mgr.s:1078`<br>`window_mgr.s:1008` | target would be frontmost: select it (brings to front + activates) |
| **`SizeControl`** | `0x012F72` | `0x00D576` | `control_mgr.s:358` | **Proto:** `Pascal: procedure SizeControl(theControl: ControlHandle; w, h: INTEGER);`<br>_SizeControl ($A95C) Called during boot. _SizeControl: resize control to new width and height Pascal: procedure SizeControl(theControl: ControlHandle; w, h: INTEGER); |
| **`SIZECONTROL`** | `0x012F72` | `0x00D576` | `control_mgr.s:302` | **Proto:** `Pascal: procedure SizeControl(theControl: ControlHandle; w, h: INTEGER);`<br>_SizeControl ($A95C): resize a control to (width, height). Pascal: procedure SizeControl(theControl: ControlHandle; w, h: INTEGER); |
| **`SIZERESOURCE`** | — | `0x00EE86` | `resource_mgr.s:3319` | _SizeRsrc / _SizeResource ($A9A5) -- get resource data size. Stack: handle(L) -> size(L). If loaded, returns _GetHandleSize. If purged, reads the 4-byte length prefix from the file. |
| **`SizeRsrc`** | `0x014864` | — | `resource_mgr.s:3476` | **Proto:** `Pascal: FUNCTION SizeResource(theResource: Handle): LONGINT;`<br>**Regs:** `Entry: 4(SP).L = theResource, 8(SP).L = space for the function result Exit:  function result = size, or -1 with ResErr = resNotFound if`<br>_SizeRsrc ($A9A5): size of a resource's data in bytes Pascal: FUNCTION SizeResource(theResource: Handle): LONGINT; Apple source name: SizeResource (System 7.1 ResourceMgr.a, MacSEROM.lst) Entry: 4(SP)... |
| **`SIZERSRC_EXIT`** | `0x01487E` | `0x00EEA0` | `resource_mgr.s:3493`<br>`resource_mgr.s:3330` | — |
| **`SIZERSRC_NO`** | `0x014872` | `0x00EE94` | `resource_mgr.s:3489`<br>`resource_mgr.s:3326` | SIZERSRC_NO - resource not loaded: read its length word from the file Called during boot. |
| **`SizeWindow`** | `0x011AC4` | `0x00C15E` | `window_mgr.s:1516` | **Proto:** `Pascal: PROCEDURE SizeWindow(theWindow: WindowPtr; w, h: INTEGER;`<br>**Regs:** `Entry: 0x4(SP) = fUpdate, 0x6(SP) = h, 0x8(SP) = w, 0xA(SP) = theWindow`<br>_SizeWindow ($A91D): set the width and height of a window's portRect Pascal: PROCEDURE SizeWindow(theWindow: WindowPtr; w, h: INTEGER; fUpdate: BOOLEAN); Entry: 0x4(SP) = fUpdate, 0x6(SP) = h, 0x8(SP)... |
| **`SIZEWINDOW`** | `0x011AC4` | `0x00C15E` | `window_mgr.s:1424` | **Proto:** `Pascal: procedure SizeWindow(theWindow: WindowPtr; w,h: INTEGER;`<br>_SizeWindow ($A91D): resize a window Pascal: procedure SizeWindow(theWindow: WindowPtr; w,h: INTEGER; fUpdate: BOOLEAN); Computes new portRect.botRight from size, then redraws if visible. |
| **`SIZEWINDOW_CONT`** | `0x011B02` | — | `window_mgr.s:1551` | SIZEWINDOW_CONT - recalculate regions, redraw frame, call DrawNew Apple source name: SizeGuts (System 7.1 WindowMgr.a) Shared by SizeWindow (visible windows only) and ZoomWindow, after SaveOld. A3 = w... |
| **`SIZEWINDOW_DONE`** | `0x011AF6` | `0x00C190` | `window_mgr.s:1534`<br>`window_mgr.s:1442` | — |
| **`SIZEWINDOW_EXIT`** | `0x011AFA` | — | `window_mgr.s:1538` | SIZEWINDOW_EXIT - strip 10 bytes of params and return (Apple: TenBytExit; also the exit of MoveWindow and TrackBox/TrackGoAway) |
| **`SIZEWINDOW_REFRESH`** | — | `0x00C19C` | `window_mgr.s:1456` | SIZEWINDOW_REFRESH - recalculate regions, redraw frame, call DrawNew Used after SizeWindow/ZoomWindow when window is visible. D3 = fUpdate parameter for DrawNew. |
| **`STACK_2`** | `0x012984` | `0x00CFB0` | `menu_mgr.s:1277`<br>`menu_mgr.s:1009` | STACK_2 STACK_2: invalidate menu dimensions (forces recalc on next draw) Stack: [ret, MenuHandle] |
| **`STDMAPENTRY`** | `0x01385C` | `0x00DE5E` | `resource_mgr.s:765`<br>`resource_mgr.s:749` | STDMAPENTRY - StdMapEntry Standard entry for routines that take a refnum parameter. Calls StdEntry, reads refnum from stack, finds the map. On failure, pops return address and exits with resNotFound. ... |
| **`STDMAPENTRY_ERR`** | `0x01386E` | `0x00DE70` | `resource_mgr.s:779`<br>`resource_mgr.s:758` | STDMAPENTRY_ERR - StdMapEntry error exit Map not found: pop caller's return address, report resFNotFound. |
| **`STDOPCODE_NEXT_ENTRY`** | — | `0x00FDD0` | `toolbox_utils.s:389` | Second loop: continue scanning with parent class ID |
| **`STDOPCODE_PARENT_CLASS`** | — | `0x00FDDA` | `toolbox_utils.s:395` | — |
| **`STDOPCODE_PCREL_JMP`** | — | `0x00FDB6` | `toolbox_utils.s:370` | — |
| **`STDOPCODE_SEARCH_TABLE`** | — | `0x00FDBA` | `toolbox_utils.s:376` | Cache miss: search dispatch table for matching class. Walks the class inheritance chain via MASuperTab. |
| **`STILLDN_DONE`** | `0x010FDA` | `0x00B5A6` | `toolbox_event.s:150`<br>`toolbox_event.s:138` | — |
| **`StillDown`** | `0x010FB6` | `0x00B582` | `toolbox_event.s:136` | **Proto:** `Pascal: FUNCTION StillDown: BOOLEAN`<br>_StillDown ($A973) Pascal: FUNCTION StillDown: BOOLEAN Returns TRUE only if the mouse button is still held down AND no mouse-up event (bit 2 = mouseUp=2, bit 1 = mouseDown=1, bit 0 = null; mask 0x7 = ... |
| **`STILLDOWN`** | `0x010FB6` | `0x00B582` | `toolbox_event.s:124` | **Proto:** `Pascal: FUNCTION StillDown: BOOLEAN`<br>_StillDown ($A973) Pascal: FUNCTION StillDown: BOOLEAN Returns TRUE only if mouse button still held AND no mouse-up event (mask 0x7 = mouseDown+mouseUp+null+keyDown) is pending in the queue. |
| **`StopAlert`** | `0x014968` | `0x00EF8A` | `dialog_mgr.s:127` | **Proto:** `StopAlert -- _StopAlert ($A986): FUNCTION StopAlert (alertID: INTEGER; filterProc : ProcPtr) INTEGER;`<br>StopAlert -- _StopAlert ($A986): FUNCTION StopAlert (alertID: INTEGER; filterProc : ProcPtr) INTEGER; _StopAlert ($A986) |
| **`STOPALERT`** | `0x014968` | `0x00EF8A` | `dialog_mgr.s:127` | _StopAlert ($A986) -- show stop-icon alert dialog. Stack: alertID(W), filterProc(L) -> itemHit(W). |
| **`STRIP_2PARAMS_RTS`** | `0x01121A` | `0x00B862` | `window_mgr.s:133`<br>`window_mgr.s:145` | Called by: SetString, INSERT_WINDOW, INSWIN_HAS_LIST, CALCVBEHIND_EMPTY, PAINTONE_EXIT (and 4 more) |
| **`StyleMatchesTemplate`** | — | `0x0124A8` | `textedit.s:4109` | StyleMatchesTemplate -- decide whether to apply edit to current style run A0 -> existing styleEntry, A6 -> conditional-match template (nil to force always-apply), D7 = mode bitmask. Returns D0: 1 = ap... |
| **`StyleMatchesTemplate_ColorCheck`** | — | `0x0124DE` | `textedit.s:4130` | — |
| **`StyleMatchesTemplate_FaceCheck`** | — | `0x0124BE` | `textedit.s:4118` | — |
| **`StyleMatchesTemplate_No`** | — | `0x0124F8` | `textedit.s:4139` | — |
| **`StyleMatchesTemplate_RTS`** | — | `0x0124FA` | `textedit.s:4141` | — |
| **`StyleMatchesTemplate_SizeCheck`** | — | `0x0124CE` | `textedit.s:4124` | — |
| **`SuperLoad`** | `0x0134D4` | — | `resource_mgr.s:270` | Super Load Called during boot. |
| **`SUPERLOAD_CAP_OK`** | — | `0x00DBBE` | `resource_mgr.s:388` | — |
| **`SUPERLOAD_CONT`** | `0x013540` | `0x00DB42` | `resource_mgr.s:314`<br>`resource_mgr.s:313` | Common: read resource data into A1 buffer, register handle in map. |
| **`SUPERLOAD_CONT_2`** | `0x01357A` | `0x00DB7C` | `resource_mgr.s:352`<br>`resource_mgr.s:348` | SUPERLOAD_CONT_2 -- read 4 bytes from A0 as big-endian long. |
| **`SUPERLOAD_CONT_3`** | `0x01358A` | `0x00DB8C` | `resource_mgr.s:367`<br>`resource_mgr.s:367` | SUPERLOAD_CONT_3 Called during boot. |
| **`SUPERLOAD_CONT_4`** | `0x0135D6` | `0x00DBD6` | `resource_mgr.s:398`<br>`resource_mgr.s:398` | — |
| **`SUPERLOAD_CONT_5`** | `0x0135FA` | `0x00DBFA` | `resource_mgr.s:424`<br>`resource_mgr.s:425` | SUPERLOAD_CONT_5 -- SizeFits: does a D0-byte buffer (twice, + map) fit? SUPERLOAD_CONT_5 |
| **`SUPERLOAD_ERR`** | `0x013568` | `0x00DB6A` | `resource_mgr.s:336`<br>`resource_mgr.s:331` | SUPERLOAD_ERR |
| **`SUPERLOAD_ERR_2`** | `0x0135F6` | `0x00DBF6` | `resource_mgr.s:414`<br>`resource_mgr.s:414` | — |
| **`SUPERLOAD_EXIT`** | `0x013610` | `0x00DC10` | `resource_mgr.s:433`<br>`resource_mgr.s:434` | — |
| **`SUPERLOAD_NEXT`** | `0x0134E2` | `0x00DAE4` | `resource_mgr.s:275`<br>`resource_mgr.s:277` | — |
| **`SUPERLOAD_NEXT_TAIL`** | — | `0x00DB5C` | `resource_mgr.s:323` | — |
| **`SUPERLOAD_NO`** | `0x013502` | `0x00DB04` | `resource_mgr.s:284`<br>`resource_mgr.s:286` | — |
| **`SUPERLOAD_NO_2`** | `0x013538` | `0x00DB3A` | `resource_mgr.s:309`<br>`resource_mgr.s:307` | SUPERLOAD_NO_2 |
| **`SUPERLOAD_NO_3`** | `0x0135BE` | — | `resource_mgr.s:388` | — |
| **`SUPERLOAD_OK`** | `0x0135A6` | `0x00DBA6` | `resource_mgr.s:377`<br>`resource_mgr.s:377` | — |
| **`SUPERLOAD_OK_2`** | `0x0135F8` | `0x00DBF8` | `resource_mgr.s:416`<br>`resource_mgr.s:416` | — |
| **`SUPERLOAD_RETRY`** | `0x013574` | `0x00DB76` | `resource_mgr.s:347`<br>`resource_mgr.s:343` | SUPERLOAD_RETRY -- A0 = preload buffer + D2: read the length word. SUPERLOAD_RETRY |
| **`SUPERLOAD_SKIP`** | `0x01355A` | — | `resource_mgr.s:324` | — |
| **`SUPERLOAD_SKIP_2`** | `0x0135B6` | `0x00DBB6` | `resource_mgr.s:383`<br>`resource_mgr.s:383` | — |
| **`SwapFont`** | `0x00E6C6` | — | `font_mgr.s:122` | SwapFont: actual implementation (37,171 calls in 30s boot trace) Checks if requested font matches current cache, loads new strike if not |
| **`SWAPFONT_CONT`** | `0x00E6CE` | `0x01930A` | `font_mgr.s:126`<br>`font_mgr.s:259` | SWAPFONT_CONT: fast-path cache check - compare FMInput with cached state |
| **`SWAPFONT_CONT_10`** | `0x00E946` | — | `font_mgr.s:481` | SWAPFONT_CONT_10 SWAPFONT_CONT_10: determine effective font size Returns D0 = font size: from FMInput.size, SysFontSize, or FMDefaultSize Called during boot. |
| **`SWAPFONT_CONT_11`** | `0x00E95A` | — | `font_mgr.s:490` | — |
| **`SWAPFONT_CONT_12`** | `0x00E95C` | — | `font_mgr.s:498` | SWAPFONT_CONT_12 SWAPFONT_CONT_12: compute missing char width from FOND width subtable |
| **`SWAPFONT_CONT_13`** | `0x00EA96` | `0x01931C` | `font_mgr.s:637`<br>`font_mgr.s:278` | SWAPFONT_CONT_13 SWAPFONT_CONT_13: restore cached numer/denom and scale factor from width table D1 = 0 for horizontal, 2 for vertical; A1 = cached values in width table Called during boot (3,318 times... |
| **`SWAPFONT_CONT_14`** | `0x00EAD8` | — | `font_mgr.s:675` | SWAPFONT_CONT_14 SWAPFONT_CONT_14: SwapFont slow path - cache miss, must find/load new font Called during boot (1,663 times in 30s trace). |
| **`SWAPFONT_CONT_15`** | `0x00EB7E` | — | `font_mgr.s:759` | SWAPFONT_CONT_15: reallocate purged width table cache entry |
| **`SWAPFONT_CONT_16`** | `0x00EB94` | `0x01948A` | `font_mgr.s:774`<br>`font_mgr.s:456` | SWAPFONT_CONT_16 -- install new widthTab handle into cache slot D5. |
| **`SWAPFONT_CONT_17`** | `0x00EBB2` | — | `font_mgr.s:792` | — |
| **`SWAPFONT_CONT_18`** | `0x00EBBA` | `0x0194CA` | `font_mgr.s:797`<br>`font_mgr.s:489` | SWAPFONT_CONT_18: extract font metrics from strike into FMOutput |
| **`SWAPFONT_CONT_19`** | `0x00EBDC` | — | `font_mgr.s:808` | no scaling: copy metrics directly from font strike |
| **`SWAPFONT_CONT_2`** | `0x00E758` | `0x01952C` | `font_mgr.s:212`<br>`font_mgr.s:551` | SWAPFONT_CONT_2 SWAPFONT_CONT_2: apply font style modifications from FMStyleTab Called during boot (1,663 times in 30s trace). |
| **`SWAPFONT_CONT_20`** | `0x00EC02` | — | `font_mgr.s:835` | SWAPFONT_CONT_20 SWAPFONT_CONT_20: dereference font handle, loading from resource if purged A0 = font handle on entry, A0 = font data pointer on exit Called during boot (1,667 times in 30s trace). |
| **`SWAPFONT_CONT_21`** | `0x00EC14` | `0x0194EE` | `font_mgr.s:851`<br>`font_mgr.s:511` | SWAPFONT_CONT_21 SWAPFONT_CONT_21: scale metric by vertical factor, round, store byte D0.B = metric value, A1 = output ptr (auto-incremented) |
| **`SWAPFONT_CONT_22`** | `0x00EC18` | `0x0194F2` | `font_mgr.s:854`<br>`font_mgr.s:513` | SWAPFONT_CONT_22: scale D0.B by D1 (16.16 fixed), round, store to (A1)+ |
| **`SWAPFONT_CONT_23`** | `0x00EC38` | — | `font_mgr.s:872` | SWAPFONT_CONT_23 SWAPFONT_CONT_23: fixed-point constant 1.0 ($00010000) for scale factor comparison |
| **`SWAPFONT_CONT_24`** | `0x00EC3C` | — | `font_mgr.s:879` | SWAPFONT_CONT_24: FixMul - multiply two 16.16 fixed-point values Pascal calling convention: pop D0 and D1 from stack, push result Optimizes identity (1.0) and integer cases to avoid full FixMul trap C... |
| **`SWAPFONT_CONT_25`** | `0x00EC7A` | — | `font_mgr.s:923` | SWAPFONT_CONT_25: FixRatio - compute fixed-point ratio D0/D1 If D0 == D1, returns 1.0 (identity). Otherwise calls _FixRatio trap. Called during boot. |
| **`SWAPFONT_CONT_26`** | `0x00EC9A` | `0x019AF4` | `font_mgr.s:950`<br>`font_mgr.s:1169` | SWAPFONT_CONT_26: load FONT resource, ROM map first (higher priority) |
| **`SWAPFONT_CONT_27`** | `0x00ECA0` | `0x019D4C` | `font_mgr.s:952`<br>`font_mgr.s:1478` | Called by: FMResolveFamily, GETFONTNAME, REALFONT (and other Font Mgr code) |
| **`SWAPFONT_CONT_28`** | `0x00ECB6` | — | `font_mgr.s:969` | SWAPFONT_CONT_28 SWAPFONT_CONT_28: full font search - find FOND, then FONT resource for requested family/size A3 = FMInput record, sets FOutFontHandle and computes scale factors Called during boot. |
| **`SWAPFONT_CONT_29`** | `0x00ECC4` | — | `font_mgr.s:975` | — |
| **`SWAPFONT_CONT_3`** | `0x00E860` | `0x01969E` | `font_mgr.s:329`<br>`font_mgr.s:704` | SWAPFONT_CONT_3: apply horizontal scaling to missing char width |
| **`SWAPFONT_CONT_30`** | `0x00ECCA` | — | `font_mgr.s:978` | — |
| **`SWAPFONT_CONT_31`** | `0x00ECD0` | — | `font_mgr.s:981` | — |
| **`SWAPFONT_CONT_32`** | `0x00ED06` | — | `font_mgr.s:1002` | compute scaled point size: size * (deviceDPI/72) * (numer/denom) |
| **`SWAPFONT_CONT_33`** | `0x00ED08` | — | `font_mgr.s:1005` | SWAPFONT_CONT_33: look up FOND resource for family D3 |
| **`SWAPFONT_CONT_34`** | `0x00ED1A` | `0x0198AE` | `font_mgr.s:1016`<br>`font_mgr.s:914` | SWAPFONT_CONT_34: try FONT resource with family in high bits, D0 as size |
| **`SWAPFONT_CONT_35`** | `0x00ED50` | `0x0198F2` | `font_mgr.s:1050`<br>`font_mgr.s:946` | SWAPFONT_CONT_35: exact/double/half not found - search adjacent sizes |
| **`SWAPFONT_CONT_36`** | `0x00ED9E` | `0x019946` | `font_mgr.s:1084`<br>`font_mgr.s:977` | compute size ratio: requested size / actual size compute horizontal and vertical scale factors SWAPFONT_CONT_36: compute numer/denom scale factor for axis D5 (0=horiz, 2=vert) |
| **`SWAPFONT_CONT_37`** | `0x00EDEA` | `0x01998E` | `font_mgr.s:1108`<br>`font_mgr.s:1001` | normalize numer/denom to range [0xC0..0x200) for best scaling precision |
| **`SWAPFONT_CONT_38`** | `0x00EE5E` | `0x0199E6` | `font_mgr.s:1179`<br>`font_mgr.s:1041` | SWAPFONT_CONT_38: adjacent size search exhausted (wrapped to 0) Decide whether to reverse search direction or try fallback |
| **`SWAPFONT_CONT_39`** | `0x00EE82` | `0x019A9A` | `font_mgr.s:1214`<br>`font_mgr.s:1132` | SWAPFONT_CONT_39 SWAPFONT_CONT_39: query device driver for its DPI resolution D0 = device (0=screen, nonzero=printer driver refNum) Fills FMDotsPerInch_h/v with device resolution |
| **`SWAPFONT_CONT_4`** | `0x00E8AC` | `0x019752` | `font_mgr.s:372`<br>`font_mgr.s:788` | SWAPFONT_CONT_4 SWAPFONT_CONT_4: extract 8-bit width from low byte, scale it Called during boot. |
| **`SWAPFONT_CONT_40`** | `0x00EEBA` | — | `font_mgr.s:1250` | SWAPFONT_CONT_40 SWAPFONT_CONT_40: search FOND font association table for size D3 A2 = FOND handle; returns D0 = font resource handle (or 0 if not found) |
| **`SWAPFONT_CONT_41`** | `0x00EED8` | — | `font_mgr.s:1272` | SWAPFONT_CONT_41: try loading NFNT resource first, fall back to FONT |
| **`SWAPFONT_CONT_42`** | `0x00EF48` | `0x019B8A` | `font_mgr.s:1337`<br>`font_mgr.s:1244` | — |
| **`SWAPFONT_CONT_43`** | `0x00EFF0` | — | `font_mgr.s:1450` | SWAPFONT_CONT_43: load font resource from best matching entry |
| **`SWAPFONT_CONT_44`** | `0x00F04E` | `0x019BB8` | `font_mgr.s:1512`<br>`font_mgr.s:1281` | SWAPFONT_CONT_44 SWAPFONT_CONT_44: style match priority weights (indexed by style bit number) bold=4, italic=8, underline=1, outline=3, shadow=3, condense=2, extend=1 |
| **`SWAPFONT_CONT_45`** | `0x00F056` | `0x019C98` | `font_mgr.s:1518`<br>`font_mgr.s:1410` | SWAPFONT_CONT_45: default FMOutput record + FMStyleTab + cursor data First 28 bytes: default DPI (80x80), style modification table, UL params |
| **`SWAPFONT_CONT_5`** | `0x00E8B4` | — | `font_mgr.s:377` | — |
| **`SWAPFONT_CONT_6`** | `0x00E8BA` | — | `font_mgr.s:381` | SWAPFONT_CONT_6: fill widths for chars above lastChar (codes 256+) |
| **`SWAPFONT_CONT_7`** | `0x00E8EC` | `0x01971C` | `font_mgr.s:415`<br>`font_mgr.s:763` | — |
| **`SWAPFONT_CONT_8`** | `0x00E8F8` | — | `font_mgr.s:427` | SWAPFONT_CONT_8: conditionally apply horizontal scaling to width in D0 D5 = nonzero if scaling needed, D0 = 16.16 fixed-point width Called during boot. |
| **`SWAPFONT_CONT_9`** | `0x00E936` | — | `font_mgr.s:467` | — |
| **`SWAPFONT_EMPTY`** | `0x00EB90` | — | `font_mgr.s:771` | SWAPFONT_EMPTY: allocate new width table cache entry Called during boot. |
| **`SWAPFONT_ERR`** | `0x00EBAE` | — | `font_mgr.s:789` | SWAPFONT_ERR: width list full or alloc failed - reuse last slot |
| **`SWAPFONT_EXIT`** | `0x00E71A` | `0x0192F6` | `font_mgr.s:171`<br>`font_mgr.s:251` | SWAPFONT_EXIT SWAPFONT_EXIT: SwapFont exit - verify font handle still valid before returning Called during boot (37,171 times in 30s trace). |
| **`SWAPFONT_EXIT_2`** | `0x00E752` | — | `font_mgr.s:201` | SWAPFONT_EXIT_2: SwapFont return - pop saved regs and jump to return address |
| **`SWAPFONT_EXIT_3`** | `0x00E90E` | — | `font_mgr.s:435` | — |
| **`SWAPFONT_EXIT_4`** | `0x00EC74` | — | `font_mgr.s:913` | — |
| **`SWAPFONT_FOUND`** | `0x00EAB6` | — | `font_mgr.s:657` | SWAPFONT_FOUND SWAPFONT_FOUND: swap width table cache - exchange current table with one from width list A4 = slot in width list array; promotes the cached table to active Called during boot (1,661 tim... |
| **`SWAPFONT_FOUND_10`** | `0x00EF9E` | — | `font_mgr.s:1394` | SWAPFONT_FOUND_10 SWAPFONT_FOUND_10: find matching style variant at size D3 in FOND association table |
| **`SWAPFONT_FOUND_2`** | `0x00EB46` | — | `font_mgr.s:735` | SWAPFONT_FOUND_2 Called during boot (1,659 times in 30s trace). |
| **`SWAPFONT_FOUND_3`** | `0x00ED74` | `0x01991A` | `font_mgr.s:1066`<br>`font_mgr.s:962` | SWAPFONT_FOUND_3: font resource found - compute scale factors |
| **`SWAPFONT_FOUND_4`** | `0x00EECE` | — | `font_mgr.s:1260` | — |
| **`SWAPFONT_FOUND_5`** | `0x00EED2` | — | `font_mgr.s:1268` | SWAPFONT_FOUND_5: found size in FOND association table - load font resource |
| **`SWAPFONT_FOUND_6`** | `0x00EEF4` | — | `font_mgr.s:1288` | SWAPFONT_FOUND_6: NFNT not found, try FONT resource with same ID |
| **`SWAPFONT_FOUND_7`** | `0x00EF0A` | — | `font_mgr.s:1302` | SWAPFONT_FOUND_7 SWAPFONT_FOUND_7: FOND found - search its font association table for requested size |
| **`SWAPFONT_FOUND_8`** | `0x00EF28` | — | `font_mgr.s:1318` | try double and half sizes for scaling |
| **`SWAPFONT_FOUND_9`** | `0x00EF5E` | — | `font_mgr.s:1350` | SWAPFONT_FOUND_9: FOND search failed - fall back to old-style FONT |
| **`SWAPFONT_LOOP`** | `0x00E776` | `0x01954A` | `font_mgr.s:224`<br>`font_mgr.s:563` | — |
| **`SWAPFONT_LOOP_10`** | `0x00EEC2` | `0x019B36` | `font_mgr.s:1254`<br>`font_mgr.s:1198` | — |
| **`SWAPFONT_LOOP_11`** | `0x00EF36` | `0x019B78` | `font_mgr.s:1327`<br>`font_mgr.s:1234` | — |
| **`SWAPFONT_LOOP_12`** | `0x00EFA6` | `0x019BAA` | `font_mgr.s:1398`<br>`font_mgr.s:1262` | — |
| **`SWAPFONT_LOOP_13`** | `0x00EFD0` | — | `font_mgr.s:1433` | check if entry has styles we didn't request (extra styles = bad match) score: count how many requested styles this entry provides |
| **`SWAPFONT_LOOP_14`** | `0x00F032` | — | `font_mgr.s:1479` | search FOND for width subtable matching this style |
| **`SWAPFONT_LOOP_2`** | `0x00E87E` | `0x0196B8` | `font_mgr.s:345`<br>`font_mgr.s:713` | SWAPFONT_LOOP_2 |
| **`SWAPFONT_LOOP_3`** | `0x00E880` | `0x0196BA` | `font_mgr.s:347`<br>`font_mgr.s:715` | — |
| **`SWAPFONT_LOOP_4`** | `0x00E8A2` | — | `font_mgr.s:359` | SWAPFONT_LOOP_4: build width table from 8-bit offset/width entries |
| **`SWAPFONT_LOOP_5`** | `0x00E8C4` | — | `font_mgr.s:386` | — |
| **`SWAPFONT_LOOP_6`** | `0x00E8D6` | `0x019706` | `font_mgr.s:398`<br>`font_mgr.s:751` | SWAPFONT_LOOP_6: build width table from 16-bit fixed-point width entries |
| **`SWAPFONT_LOOP_7`** | `0x00E91E` | — | `font_mgr.s:449` | — |
| **`SWAPFONT_LOOP_8`** | `0x00E980` | — | `font_mgr.s:519` | — |
| **`SWAPFONT_LOOP_9`** | `0x00EA54` | — | `font_mgr.s:601` | — |
| **`SWAPFONT_NEXT`** | `0x00EB16` | — | `font_mgr.s:705` | — |
| **`SWAPFONT_NEXT_2`** | `0x00EB38` | `0x01943A` | `font_mgr.s:722`<br>`font_mgr.s:421` | — |
| **`SWAPFONT_NEXT_3`** | `0x00ED5C` | `0x0198FE` | `font_mgr.s:1056`<br>`font_mgr.s:952` | — |
| **`SWAPFONT_NEXT_4`** | `0x00EF86` | — | `font_mgr.s:1373` | — |
| **`SWAPFONT_NEXT_5`** | `0x00EF8A` | — | `font_mgr.s:1380` | SWAPFONT_NEXT_5: enumerate FOND IDs within block, searching for one with fonts |
| **`SWAPFONT_NEXT_6`** | `0x00EFBE` | — | `font_mgr.s:1421` | — |
| **`SWAPFONT_NO`** | `0x00E7D2` | `0x019614` | `font_mgr.s:259`<br>`font_mgr.s:641` | SWAPFONT_NO: build width table from font strike's offset/width table |
| **`SWAPFONT_NO_10`** | `0x00EA36` | — | `font_mgr.s:590` | SWAPFONT_NO_10 SWAPFONT_NO_10: compute extra width from FOND style width offsets FOND at offset $1C has base width + 8 per-style adjustments |
| **`SWAPFONT_NO_11`** | `0x00EA82` | — | `font_mgr.s:623` | — |
| **`SWAPFONT_NO_12`** | `0x00EAF0` | `0x0193AA` | `font_mgr.s:682`<br>`font_mgr.s:357` | — |
| **`SWAPFONT_NO_13`** | `0x00EB06` | — | `font_mgr.s:690` | — |
| **`SWAPFONT_NO_14`** | `0x00EB0A` | `0x0193C8` | `font_mgr.s:700`<br>`font_mgr.s:371` | SWAPFONT_NO_14 SWAPFONT_NO_14: search width list cache for matching FMInput 12 slots, each with a full width table keyed by FMInput Called during boot (1,661 times in 30s trace). |
| **`SWAPFONT_NO_15`** | `0x00EBB6` | — | `font_mgr.s:794` | — |
| **`SWAPFONT_NO_16`** | `0x00EC10` | `0x019354` | `font_mgr.s:841`<br>`font_mgr.s:312` | — |
| **`SWAPFONT_NO_17`** | `0x00ECD4` | — | `font_mgr.s:983` | — |
| **`SWAPFONT_NO_18`** | `0x00EDF6` | `0x01999A` | `font_mgr.s:1119`<br>`font_mgr.s:1007` | SWAPFONT_NO_18: normalize small numer values upward |
| **`SWAPFONT_NO_19`** | `0x00EE02` | `0x0199A6` | `font_mgr.s:1130`<br>`font_mgr.s:1013` | SWAPFONT_NO_19: fine adjust if numer in [192..256) using 3/4 interpolation |
| **`SWAPFONT_NO_2`** | `0x00E7F4` | — | `font_mgr.s:272` | — |
| **`SWAPFONT_NO_20`** | `0x00EE28` | — | `font_mgr.s:1147` | — |
| **`SWAPFONT_NO_21`** | `0x00EE4A` | — | `font_mgr.s:1166` | SWAPFONT_NO_21: store normalized numer/denom in width table cache |
| **`SWAPFONT_NO_22`** | `0x00EE6A` | `0x0199F2` | `font_mgr.s:1190`<br>`font_mgr.s:1047` | SWAPFONT_NO_22: scaling enabled, reverse direction check |
| **`SWAPFONT_NO_23`** | `0x00EF46` | `0x019B88` | `font_mgr.s:1335`<br>`font_mgr.s:1242` | — |
| **`SWAPFONT_NO_24`** | `0x00EF50` | `0x019B92` | `font_mgr.s:1342`<br>`font_mgr.s:1249` | — |
| **`SWAPFONT_NO_25`** | `0x00EF64` | — | `font_mgr.s:1355` | SWAPFONT_NO_25: try family as old-style FONT ID (family < 512 only) |
| **`SWAPFONT_NO_26`** | `0x00EF72` | `0x019A62` | `font_mgr.s:1366`<br>`font_mgr.s:1103` | SWAPFONT_NO_26: FOND family >= 16384 - enumerate FOND resources |
| **`SWAPFONT_NO_27`** | `0x00F03E` | — | `font_mgr.s:1485` | — |
| **`SWAPFONT_NO_3`** | `0x00E850` | `0x01968E` | `font_mgr.s:314`<br>`font_mgr.s:691` | SWAPFONT_NO_3 SWAPFONT_NO_3: get missing symbol width from integer offset/width table Called during boot. |
| **`SWAPFONT_NO_4`** | `0x00E8CA` | — | `font_mgr.s:389` | — |
| **`SWAPFONT_NO_5`** | `0x00E8E4` | `0x0196DC` | `font_mgr.s:410`<br>`font_mgr.s:729` | SWAPFONT_NO_5: scale 16-bit fixed-point char width |
| **`SWAPFONT_NO_6`** | `0x00E92C` | `0x019714` | `font_mgr.s:461`<br>`font_mgr.s:758` | SWAPFONT_NO_6: scale FOND width by point size factor |
| **`SWAPFONT_NO_7`** | `0x00E986` | — | `font_mgr.s:523` | SWAPFONT_NO_7: apply spExtra (space character extra width) adjustment |
| **`SWAPFONT_NO_8`** | `0x00E9C8` | `0x0197BC` | `font_mgr.s:547`<br>`font_mgr.s:833` | scale spExtra delta by numer/denom ratio and add to space char width SWAPFONT_NO_8: notify printer driver of font change if device port active |
| **`SWAPFONT_NO_9`** | `0x00E9EE` | — | `font_mgr.s:561` | SWAPFONT_NO_9: save current FMInput as cached state for fast-path comparison |
| **`SWAPFONT_OK`** | `0x00E70E` | — | `font_mgr.s:160` | compare 16 bytes: family(2)+size(2)+face(2)+needBits(2)+device(2)+numer(4)+denom(4) cache hit - check if spExtra changed (affects width calculations) spExtra changed: just recalculate widths, don't re... |
| **`SWAPFONT_OK_10`** | `0x00EC6E` | — | `font_mgr.s:909` | fast path: D1 is pure fraction (0.xxxx), use MULU optimization SWAPFONT_OK_10: full FixMul via ROM trap (both operands have integer parts) |
| **`SWAPFONT_OK_11`** | `0x00ED24` | — | `font_mgr.s:1027` | SWAPFONT_OK_11 SWAPFONT_OK_11: no FOND found, try old-style FONT resource (family<<7 \| size) Called during boot. |
| **`SWAPFONT_OK_12`** | `0x00EE1A` | `0x0199BC` | `font_mgr.s:1141`<br>`font_mgr.s:1023` | — |
| **`SWAPFONT_OK_13`** | `0x00EE40` | — | `font_mgr.s:1161` | SWAPFONT_OK_13: check if vertical scale factor changed |
| **`SWAPFONT_OK_14`** | `0x00EE6E` | `0x0199F6` | `font_mgr.s:1193`<br>`font_mgr.s:1050` | — |
| **`SWAPFONT_OK_15`** | `0x00EE74` | — | `font_mgr.s:1201` | SWAPFONT_OK_15: both directions exhausted - try alternate font family |
| **`SWAPFONT_OK_16`** | `0x00EEAC` | `0x019AC4` | `font_mgr.s:1237`<br>`font_mgr.s:1149` | SWAPFONT_OK_16 Called during boot. |
| **`SWAPFONT_OK_17`** | `0x00EF56` | `0x019B98` | `font_mgr.s:1345`<br>`font_mgr.s:1252` | — |
| **`SWAPFONT_OK_18`** | `0x00EF6E` | — | `font_mgr.s:1359` | — |
| **`SWAPFONT_OK_19`** | `0x00EFB2` | — | `font_mgr.s:1409` | SWAPFONT_OK_19: exact style match found - record position |
| **`SWAPFONT_OK_2`** | `0x00E7BA` | — | `font_mgr.s:250` | — |
| **`SWAPFONT_OK_20`** | `0x00EFB6` | — | `font_mgr.s:1417` | SWAPFONT_OK_20: found size in FOND - find best style match among duplicates |
| **`SWAPFONT_OK_21`** | `0x00F00C` | — | `font_mgr.s:1462` | SWAPFONT_OK_21: remove intrinsic styles, search FOND width subtable |
| **`SWAPFONT_OK_22`** | `0x00F044` | — | `font_mgr.s:1493` | SWAPFONT_OK_22: SWAPFONT_CONT_41 succeeded, discard saved D0 |
| **`SWAPFONT_OK_23`** | `0x00F048` | — | `font_mgr.s:1501` | SWAPFONT_OK_23: found matching width subtable - save offset in A4 |
| **`SWAPFONT_OK_3`** | `0x00E7C8` | `0x019596` | `font_mgr.s:255`<br>`font_mgr.s:589` | — |
| **`SWAPFONT_OK_4`** | `0x00E7DC` | — | `font_mgr.s:264` | — |
| **`SWAPFONT_OK_5`** | `0x00E858` | `0x019696` | `font_mgr.s:324`<br>`font_mgr.s:700` | SWAPFONT_OK_5 SWAPFONT_OK_5: get missing symbol width from 16-bit fixed-point width table |
| **`SWAPFONT_OK_6`** | `0x00E910` | — | `font_mgr.s:443` | SWAPFONT_OK_6 SWAPFONT_OK_6: build widths from FOND width subtable with per-point scaling |
| **`SWAPFONT_OK_7`** | `0x00E956` | — | `font_mgr.s:488` | — |
| **`SWAPFONT_OK_8`** | `0x00E970` | — | `font_mgr.s:512` | SWAPFONT_OK_8: width table cache hit but extra width changed Adjusts all 256 cached widths by the extra delta Called during boot (1,659 times in 30s trace). |
| **`SWAPFONT_OK_9`** | `0x00EBE0` | `0x01950C` | `font_mgr.s:815`<br>`font_mgr.s:527` | SWAPFONT_OK_9: scaled metrics - apply V/H scale factors to font metrics |
| **`SWAPFONT_RETRY`** | `0x00E73C` | — | `font_mgr.s:190` | font was purged - try to reload it SWAPFONT_RETRY: font reload failed - build synthetic FMInput and retry via SWAPFONT_CONT |
| **`SWAPFONT_RETRY_2`** | `0x00EC92` | — | `font_mgr.s:942` | SWAPFONT_RETRY_2 SWAPFONT_RETRY_2: load FONT resource by ID, searching ROM map too D3 = font resource ID (family<<7 \| size) -> A0 = FONT handle (or nil) |
| **`SWAPFONT_SKIP`** | `0x00E788` | `0x01955C` | `font_mgr.s:232`<br>`font_mgr.s:571` | — |
| **`SWAPFONT_SKIP_2`** | `0x00E79E` | — | `font_mgr.s:240` | — |
| **`SWAPFONT_SKIP_3`** | `0x00EA5E` | — | `font_mgr.s:607` | — |
| **`SWAPFONT_SKIP_4`** | `0x00EA62` | `0x0195F2` | `font_mgr.s:609`<br>`font_mgr.s:626` | — |
| **`SWAPFONT_SKIP_5`** | `0x00EB5C` | `0x019416` | `font_mgr.s:743`<br>`font_mgr.s:407` | Cache hit: publish cached state. |
| **`SWAPFONT_SKIP_6`** | `0x00ED46` | `0x0198E8` | `font_mgr.s:1043`<br>`font_mgr.s:939` | not found at exact size: try double and half sizes for scaling |
| **`SWAPFONT_SKIP_7`** | `0x00EF2A` | `0x019B6C` | `font_mgr.s:1321`<br>`font_mgr.s:1228` | SWAPFONT_SKIP_7: no exact/double/half - find closest available size in FOND |
| **`SWAPFONT_SKIP_8`** | `0x00EFDC` | — | `font_mgr.s:1439` | — |
| **`SWAPFONT_SKIP_9`** | `0x00EFE8` | `0x019BF8` | `font_mgr.s:1445`<br>`font_mgr.s:1317` | — |
| **`SYNTH_ACTIVATE`** | `0x011142` | `0x00B730` | `toolbox_event.s:389`<br>`toolbox_event.s:367` | SYNTH_ACTIVATE - Synthesize activate/deactivate events Checks CurActivate and CurDeactive for pending window activation changes. If a window needs activation or deactivation, builds an activateEvt (8)... |
| **`SysEdit`** | `0x015E36` | — | `desk_mgr.s:381` | SysEdit -- trap handler for _SysEdit ($A9C2). _SysEdit ($A9C2) |
| **`SYSEDIT_SKIP`** | `0x015E60` | `0x0104B4` | `desk_mgr.s:396`<br>`desk_mgr.s:406` | — |
| **`SYSEVT_DISPATCH`** | `0x015C04` | `0x010240` | `desk_mgr.s:58`<br>`desk_mgr.s:55` | SYSEVT_DISPATCH - SystemEvent dispatch table (word offsets from SYSEVT_DISPATCH) Entries for event codes 0-11: 0 (null): -> SYSEVT_HANDLED (not handled) 1 (mouseDown): -> SYSEVT_HANDLED (not handled b... |
| **`SYSEVT_HANDLED`** | `0x015C1C` | `0x010258` | `desk_mgr.s:63`<br>`desk_mgr.s:64` | SYSEVT_HANDLED - called from 3 places |
| **`SYSEVT_RESTORE`** | `0x015C20` | `0x01025C` | `desk_mgr.s:65`<br>`desk_mgr.s:67` | Called by: TEXTEDIT_CONT, SYSTEMEVENT, TEXTEDIT_CONT_6, TEXTEDIT_CONT_7 |
| **`SystemClick`** | `0x015CA0` | `0x0102F2` | `desk_mgr.s:163` | **Proto:** `SystemClick -- _SystemClick ($A9B3): PROCEDURE SystemClick (theEvent: EventRecord; theWindow:`<br>SystemClick -- _SystemClick ($A9B3): PROCEDURE SystemClick (theEvent: EventRecord; theWindow: |
| **`SYSTEMCLICK`** | `0x015CA0` | `0x0102F2` | `desk_mgr.s:179` | _SystemClick ($A9B3) - process mouse click on a window. If theWindow is a desk accessory window, dispatches by part code (drag/goAway/content) and notifies DA via accEvent. If nil, calls DeskHook to h... |
| **`SYSTEMCLICK_EMPTY`** | `0x015D12` | `0x010366` | `desk_mgr.s:217`<br>`desk_mgr.s:232` | SYSTEMCLICK_EMPTY Called during boot. |
| **`SYSTEMCLICK_EXIT`** | `0x015D06` | `0x01035A` | `desk_mgr.s:205`<br>`desk_mgr.s:221` | Called by: SYSTEMCLICK_EMPTY, SYSTEMCLICK_NO, SYSTEMCLICK_OK, SYSTEMCLICK_OK_2, SYSTEMCLICK_OK_3 |
| **`SYSTEMCLICK_NO`** | `0x015D34` | `0x010388` | `desk_mgr.s:236`<br>`desk_mgr.s:250` | SYSTEMCLICK_NO |
| **`SYSTEMCLICK_OK`** | `0x015D3A` | `0x01038E` | `desk_mgr.s:245`<br>`desk_mgr.s:258` | SYSTEMCLICK_OK |
| **`SYSTEMCLICK_OK_2`** | `0x015D4C` | `0x0103A0` | `desk_mgr.s:258`<br>`desk_mgr.s:270` | SYSTEMCLICK_OK_2 |
| **`SYSTEMCLICK_OK_3`** | `0x015D6C` | `0x0103C0` | `desk_mgr.s:277`<br>`desk_mgr.s:288` | SYSTEMCLICK_OK_3 |
| **`SYSTEMEDIT`** | — | `0x01048A` | `desk_mgr.s:391` | _SysEdit ($A9C2) - dispatch Edit menu command (Undo, Cut, Copy, Paste, Clear) to front DA. Returns TRUE if DA handled it. editCmd 0..3 -> csCode 68..71 (accUndo..accPaste). |
| **`SystemEvent`** | `0x015BE0` | `0x01021C` | `desk_mgr.s:25` | **Proto:** `FUNCTION SystemEvent(theEvent: EventRecord): BOOLEAN`<br>Desk Manager -- desk accessories Apple source: DeskMgr.a (MacSEROM.lst module DESKMGR): SystemEvent ($A9B2), SystemClick ($A9B3), SystemTask ($A9B4), SystemMenu ($A9B5), SysEdit ($A9C2), OpenDeskAcc (... |
| **`SYSTEMEVENT`** | `0x015BE0` | `0x01021C` | `desk_mgr.s:23` | **Proto:** `FUNCTION SystemEvent(theEvent: EventRecord): BOOLEAN`<br>Desk Manager -- desk accessories Apple source: DeskMgr.a (MacSEROM.lst module DESKMGR): SystemEvent ($A9B2), SystemClick ($A9B3), SystemTask ($A9B4), SystemMenu ($A9B5), SysEdit ($A9C2), OpenDeskAcc (... |
| **`SystemMenu`** | `0x015DEE` | `0x010442` | `desk_mgr.s:340` | **Proto:** `SystemMenu -- _SystemMenu ($A9B5): PROCEDURE SystemMenu (menuResult: LONGINT);`<br>SystemMenu -- _SystemMenu ($A9B5): PROCEDURE SystemMenu (menuResult: LONGINT); _SystemMenu ($A9B5) |
| **`SYSTEMMENU`** | `0x015DEE` | `0x010442` | `desk_mgr.s:352` | _SystemMenu ($A9B5) - dispatch DA menu choice. If a DA owns the selected menuID, sends accMenu (csCode=$43) with the menu result (menuID:item) to the DA. |
| **`SYSTEMMENU_DONE`** | `0x015E2E` | `0x010482` | `desk_mgr.s:371`<br>`desk_mgr.s:382` | — |
| **`SYSTEMMENU_EMPTY`** | `0x015E00` | `0x010454` | `desk_mgr.s:347`<br>`desk_mgr.s:359` | — |
| **`SYSTEMMENU_LOOP`** | `0x015E08` | `0x01045C` | `desk_mgr.s:350`<br>`desk_mgr.s:362` | — |
| **`SYSTEMMENU_SKIP`** | `0x015E2A` | `0x01047E` | `desk_mgr.s:368`<br>`desk_mgr.s:379` | SYSTEMMENU_SKIP |
| **`SystemTask`** | `0x015D72` | `0x0103C6` | `desk_mgr.s:287` | _SystemTask ($A9B4) Called during boot (3,694 times in 30s trace). |
| **`SYSTEMTASK`** | `0x015D72` | `0x0103C6` | `desk_mgr.s:300` | _SystemTask ($A9B4) - give time to desk accessories. Called from event loop. Iterates unit table; for each DA with dNeedTime+dOpened set whose dCtlDelay has elapsed, sends accRun (csCode=$41) via TEXT... |
| **`SYSTEMTASK_CONT`** | `0x015DE8` | `0x01043C` | `desk_mgr.s:331`<br>`desk_mgr.s:344` | — |
| **`SYSTEMTASK_EMPTY`** | `0x015DDA` | — | `desk_mgr.s:324` | — |
| **`SYSTEMTASK_LOOP`** | `0x015DAC` | `0x010400` | `desk_mgr.s:308`<br>`desk_mgr.s:321` | — |
| **`SYSTEMTASK_RUN_DA`** | — | `0x01042E` | `desk_mgr.s:337` | — |
| **`SYSTEMTASK_SKIP`** | `0x015DA4` | `0x0103F8` | `desk_mgr.s:305`<br>`desk_mgr.s:318` | — |
| **`SYSTEMTASK_SKIP_2`** | `0x015DDE` | `0x010432` | `desk_mgr.s:326`<br>`desk_mgr.s:339` | — |
| **`TBOX_GET_EVENT`** | `0x011024` | `0x00B5F0` | `toolbox_event.s:231`<br>`toolbox_event.s:206` | TBOX_GET_EVENT - Shared Toolbox event retrieval logic Used by both GetNextEvent (D3=0) and EventAvail (D3=-1). Stack frame: 0x8(A6) = eventPtr, 0xC(A6) = eventMask, 0xE(A6) = result. Flow: 1. On first... |
| **`TE68KEND`** | — | `0x0125F6` | `scrap_mgr.s:35` | **Proto:** `Pascal: function InfoScrap: PScrapStuff;`<br>Scrap Manager - InfoScrap, UnloadScrap, LodeScrap, ZeroScrap, GetScrap, PutScrap Manages the desk scrap (clipboard) for cut/copy/paste between applications. The scrap lives either in memory (ScrapStat... |
| **`TE_AD_EPILOGUE`** | — | `0x011B64` | `textedit.s:2767` | Called by: TEDEACTIVATE, TEIDLE, TEACTIVATE_OK, TEPASTE |
| **`TE_ADJ_RUNS_AFTER_DEL`** | — | `0x0115DE` | `textedit.s:2002` | TE_ADJ_RUNS_AFTER_DEL -- decrement follow-run start offsets by selLen After deleting selLen bytes, runs after the affected range need their start offsets adjusted downward by selLen. Skips runs whose ... |
| **`TE_ADJ_RUNS_LOOP`** | — | `0x0115E2` | `textedit.s:2005` | — |
| **`TE_ADJ_RUNS_NEXT`** | — | `0x0115F0` | `textedit.s:2011` | — |
| **`TE_ADVANCE_LINESTART`** | — | `0x010F20` | `textedit.s:1094` | TE_ADVANCE_LINESTART - advance lineStarts pointer past D0 char offset. Walks A2 forward through lineStarts until lineStart[A2+1] > D0. |
| **`TE_ADVANCE_STYLERUN`** | — | `0x010ECE` | `textedit.s:1038` | TE_ADVANCE_STYLERUN - advance/back style run pointer by one entry. LTR text: A0 += 4 (forward); RTL: A0 -= 4 (backward). |
| **`TE_ADVANCE_STYLERUN_LTR`** | — | `0x010ED8` | `textedit.s:1043` | — |
| **`TE_ADVANCE_STYLERUN_RTS`** | — | `0x010EDA` | `textedit.s:1045` | — |
| **`TE_APPEND_STYLEENTRY`** | — | `0x011DC2` | `textedit.s:3118` | TE_APPEND_STYLEENTRY -- append new styleEntry from input at A0 Walks styleEntry table looking for a free slot (refCount = 0). If none found, grows the handle by 18 bytes via TE_RESIZE_TEXTHANDLE. Bloc... |
| **`TE_APPEND_STYLEENTRY_LOOP`** | — | `0x011DD8` | `textedit.s:3126` | — |
| **`TE_APPEND_STYLEENTRY_STORE`** | — | `0x011E06` | `textedit.s:3145` | No free slot: grow handle by 18 bytes. |
| **`TE_APPLY_JUST`** | — | `0x0110AA` | `textedit.s:1288` | Fall through to TE_APPLY_JUST (apply justification) |
| **`TE_APPLY_JUST_MEASURE`** | — | `0x0110B6` | `textedit.s:1293` | — |
| **`TE_CARET_ERASE`** | — | `0x011AD4` | `textedit.s:2688` | TE_CARET_ERASE -- erase caret (pre-edit) Disables caret-blink, clears caret-shown flag, then XORs the caret pixels off via P_TERECAL_CONT_4. No-op if TERec is inactive. Called by: TESETSELECT, TECLICK... |
| **`TE_CARET_REDRAW`** | — | `0x011AD2` | `textedit.s:2678` | — |
| **`TE_CARET_RESTORE`** | — | `0x011AB2` | `textedit.s:2667` | TE_CARET_RESTORE / TE_CARET_SHOW -- restore caret to visible (post-edit) If TERec is active and selection is empty (caret), enable the blink flag (0x39) and ensure caret is shown (0x38). Falls into P_... |
| **`TE_CARET_RTS`** | — | `0x011B06` | `textedit.s:2713` | Called by: TE_CARET_RESTORE, TE_CARET_ERASE, TE_CARET_SHOW |
| **`TE_CARET_SHOW`** | — | `0x011AC8` | `textedit.s:2674` | — |
| **`TE_CMP_STYLE_BYTES`** | — | `0x011DAA` | `textedit.s:3097` | TE_CMP_STYLE_BYTES -- compare 12 style-record bytes for equality A0 -> input style record, A1 -> existing styleEntry record. Compares 12 bytes from A0 against A1+6 (the actual style portion, after cha... |
| **`TE_CMP_STYLE_BYTES_LOOP`** | — | `0x011DB4` | `textedit.s:3101` | — |
| **`TE_CMP_STYLE_BYTES_RTS`** | — | `0x011DBC` | `textedit.s:3106` | — |
| **`TE_CUR_LINE_HEIGHT`** | — | `0x011126` | `textedit.s:1352` | TE_CUR_LINE_HEIGHT - get height of single line at index D0. Out: D1 = line height (masked 0x7FFF). Unstyled TE: returns teLineHite. |
| **`TE_CUR_LINE_HEIGHT_RTS`** | — | `0x01114A` | `textedit.s:1365` | — |
| **`TE_DELETE_ADJ_FIRST_RUN`** | — | `0x0115A4` | `textedit.s:1966` | — |
| **`TE_DELETE_REDUCE_COMPACT`** | — | `0x0115B6` | `textedit.s:1975` | — |
| **`TE_DELETE_RTS`** | — | `0x0115D8` | `textedit.s:1991` | — |
| **`TE_DELETE_SEL`** | — | `0x01153E` | `textedit.s:1910` | TE_DELETE_SEL - remove selection bytes from text handle. Updates text via _Munger (search-and-replace with 0-byte replacement), shrinks teLength, sets selEnd = selStart. For styled TE: also collapses ... |
| **`TE_DELETE_SEL_RTS`** | — | `0x011566` | `textedit.s:1927` | — |
| **`TE_DELETE_STYLES`** | — | `0x011568` | `textedit.s:1940` | TE_DELETE_STYLES -- collapse styleRun runs that fall in the deleted selection range [D0, D1). Used by TEDELETE for styled TextEdit (teStyleRec set, high bit of teJust+1).  Walks the styleRun array and... |
| **`TE_DO_PASTE`** | — | `0x011BD2` | `textedit.s:2851` | TE_DO_PASTE -- core paste implementation D5 = scrap byte count, D6 = scrap text ptr. Hides caret, erases selection, applies style updates (for styled TE), then _Munger replaces the selection with the ... |
| **`TE_DO_PASTE_COLLAPSE_STYLES`** | — | `0x011BEC` | `textedit.s:2861` | — |
| **`TE_DO_PASTE_EDIT`** | — | `0x011BF0` | `textedit.s:2863` | — |
| **`TE_EXIT_3PARAM`** | — | `0x010938` | `textedit.s:343` | Called by: TESTYLPASTE_ENTRY, TESetStyle_Exit, TEContinuousStyle_Exit, TEReplaceStyle_Exit, TEGetStyleHandle_Exit (and 1 more) |
| **`TE_EXIT_4PARAM`** | — | `0x010932` | `textedit.s:339` | — |
| **`TE_EXIT_BODY`** | — | `0x01093C` | `textedit.s:345` | — |
| **`TE_EXIT_TAIL`** | — | `0x010982` | `textedit.s:367` | — |
| **`TE_FIND_LINE_BREAK`** | — | `0x0116B2` | `textedit.s:2136` | TE_FIND_LINE_BREAK - find pixel offset where line breaks (D6..D7). In: D6 = line start, D7 = line end, D4 = available pixels. Out: D0 = found-flag (0 = wraps), D1 = char where wrap. Walks chars (or st... |
| **`TE_FIND_LINE_BREAK_FOUND`** | — | `0x011702` | `textedit.s:2172` | — |
| **`TE_FIND_LINE_BREAK_RTS`** | — | `0x011704` | `textedit.s:2174` | — |
| **`TE_FIND_LINE_BREAK_RUN_LOOP`** | — | `0x0116DE` | `textedit.s:2154` | — |
| **`TE_FIND_LINE_BREAK_STYLED`** | — | `0x0116CA` | `textedit.s:2145` | — |
| **`TE_FIND_LINE_BREAK_USE_END`** | — | `0x0116F0` | `textedit.s:2163` | — |
| **`TE_FIND_LINE_MEASURE`** | — | `0x01170A` | `textedit.s:2183` | TE_FIND_LINE_MEASURE - measure chars D1..D0 in current font. Calls P_Pixel2Char with D4 = remaining pixel budget. Out: D0 = chars consumed (high word = found flag), D4 -= consumed pixels. |
| **`TE_FULL_REBUILD_APPEND`** | — | `0x011936` | `textedit.s:2472` | — |
| **`TE_FULL_REBUILD_CHK_INSERT`** | — | `0x01190A` | `textedit.s:2454` | — |
| **`TE_FULL_REBUILD_DISPOSE_BUF`** | — | `0x0119AC` | `textedit.s:2524` | _Munger params: replace teLineStarts[A2-A3..-0xC(A6)-A3] with buf contents (D5 bytes, ptr from -0x8(A6)). |
| **`TE_FULL_REBUILD_DO_MUNGER`** | — | `0x011978` | `textedit.s:2498` | — |
| **`TE_FULL_REBUILD_FINALIZE`** | — | `0x011960` | `textedit.s:2489` | — |
| **`TE_FULL_REBUILD_FORWARD`** | — | `0x0118FE` | `textedit.s:2448` | — |
| **`TE_FULL_REBUILD_GROW_BUF`** | — | `0x01191A` | `textedit.s:2461` | — |
| **`TE_FULL_REBUILD_LINESTARTS`** | — | `0x0118BE` | `textedit.s:2424` | TE_FULL_REBUILD_LINESTARTS -- full lineStarts rebuild via auxiliary buffer Used when text shrunk (D7 <= 0). Allocates a 256-byte working buffer (grows by +256 if needed), accumulates new lineStart pos... |
| **`TE_FULL_REBUILD_LOOP`** | — | `0x0118E6` | `textedit.s:2438` | — |
| **`TE_FULL_REBUILD_NEXT_BREAK`** | — | `0x011958` | `textedit.s:2485` | — |
| **`TE_FULL_REBUILD_RTS`** | — | `0x0119C6` | `textedit.s:2535` | — |
| **`TE_FULL_REBUILD_TAIL_SHIFT`** | — | `0x0119B8` | `textedit.s:2529` | — |
| **`TE_GET_FONT_INFO`** | — | `0x0108FA` | `textedit.s:305` | Called by: TE_INIT_STYLEREC, TENEW, TE_REBUILD_LINEHEIGHTS, PrimeStyleEntry, TEContinuousStyle_PlainPath TE_GET_FONT_INFO - get current font ascent and lineHeight. Returns D0 = font ascent, D1 = ascen... |
| **`TE_GROW_STYLERUN_ARRAY`** | — | `0x011CF8` | `textedit.s:2991` | TE_GROW_STYLERUN_ARRAY -- grow styleRun array by D2 entries (4 bytes each) A0 -> insertion position. Resizes the styleRun handle to make room for D2 new entries past A0, then BlockMoves the trailing e... |
| **`TE_INIT_STYLEREC`** | — | `0x0108AE` | `textedit.s:279` | **Regs:** `Entry: A0 = StyleRec base, D0 = text length.`<br>TE_INIT_STYLEREC - initialize StyleRec arrays with single style run. Entry: A0 = StyleRec base, D0 = text length. Sets nRuns=1, lineHeightTab.startChar=0, ends at -1 (sentinel), then calls TE_GET_FONT... |
| **`TE_INPLACE_LINESTARTS`** | — | `0x011850` | `textedit.s:2359` | TE_INPLACE_LINESTARTS -- in-place lineStarts patcher (text grew, D7 > 0) Walks the existing teLineStarts array (A2) past the change point, inserting new lineStarts where word breaks now fall and shift... |
| **`TE_INPLACE_LINESTARTS_COPY_TAIL`** | — | `0x011898` | `textedit.s:2391` | — |
| **`TE_INPLACE_LINESTARTS_FORWARD`** | — | `0x011876` | `textedit.s:2376` | Walk lineStarts forward to the slot whose value > scan + insert. |
| **`TE_INPLACE_LINESTARTS_LOOP`** | — | `0x011856` | `textedit.s:2362` | — |
| **`TE_INPLACE_LINESTARTS_RTS`** | — | `0x0118BC` | `textedit.s:2407` | — |
| **`TE_INPLACE_LINESTARTS_SHIFT`** | — | `0x0118AA` | `textedit.s:2399` | — |
| **`TE_INSERT_BODY`** | — | `0x011E2A` | `textedit.s:3180` | TE_INSERT_BODY -- _TEInsert text-edit body D5 = insert byte count, D6 = insert text ptr.  Calls TEPASTE_CONT_2 to set up _Munger params, pushes destination info, runs _Munger, then HLocks teText again... |
| **`TE_INSERT_BODY_RTS`** | — | `0x011E56` | `textedit.s:3197` | — |
| **`TE_INSERT_EPILOGUE`** | — | `0x011E80` | `textedit.s:3219` | — |
| **`TE_JUST_FULL_OFFSET`** | — | `0x0110CC` | `textedit.s:1302` | — |
| **`TE_JUST_STORE`** | — | `0x0110D0` | `textedit.s:1304` | — |
| **`TE_LINE_HEIGHT_AT_CHAR`** | — | `0x011F58` | `textedit.s:3339` | TE_LINE_HEIGHT_AT_CHAR - get height of line containing char D3. Out: D1 = line height (from TE_CUR_LINE_HEIGHT). Saves/restores A2 since TE_ADVANCE_LINESTART/P_TEDOTEXT_CONT_2 modify it. |
| **`TE_LOCATE_STYLERUNS`** | — | `0x010EB4` | `textedit.s:1022` | TE_LOCATE_STYLERUNS - locate first style run covering chars D0..D1. Out: A0 = first run, D0 = run count covering range. For RTL text, advances A0 to last run (descending order). Called by: PIXELTOCHAR... |
| **`TE_LOCATE_STYLERUNS_RTS`** | — | `0x010ECC` | `textedit.s:1032` | — |
| **`TE_LOOKUP_STYLEENTRY`** | — | `0x011D6A` | `textedit.s:3058` | TE_LOOKUP_STYLEENTRY -- look up styleEntry matching A0's input style Walks the styleEntry array searching for one whose 12-byte style portion (offset +6) matches A0+6. If found, increments its refCoun... |
| **`TE_LOOKUP_STYLEENTRY_FOUND`** | — | `0x011D9A` | `textedit.s:3079` | — |
| **`TE_LOOKUP_STYLEENTRY_LOOP`** | — | `0x011D82` | `textedit.s:3067` | — |
| **`TE_LOOKUP_STYLEENTRY_NEXT`** | — | `0x011D8E` | `textedit.s:3073` | — |
| **`TE_LOOKUP_STYLEENTRY_RTS`** | — | `0x011DA6` | `textedit.s:3086` | — |
| **`TE_MEASURE_CLAMP_RUN_END`** | — | `0x01127A` | `textedit.s:1544` | — |
| **`TE_MEASURE_LAST_RUN`** | — | `0x01129A` | `textedit.s:1557` | — |
| **`TE_MEASURE_RANGE`** | — | `0x011240` | `textedit.s:1518` | TE_MEASURE_RANGE - measure pixels for partial char range D6..D7. D6 = current line start, D7 = char position to measure to. For unstyled or LTR styled: walks chars via XTRIMMEASURE_CONT. For RTL style... |
| **`TE_MEASURE_RANGE_LOOP`** | — | `0x011266` | `textedit.s:1533` | — |
| **`TE_MEASURE_RTS`** | — | `0x0112A0` | `textedit.s:1560` | — |
| **`TE_MEASURE_RUN`** | — | `0x011288` | `textedit.s:1549` | — |
| **`TE_MEASURE_USE_RUN_START`** | — | `0x01126E` | `textedit.s:1538` | — |
| **`TE_ORDER_SEL_RTS`** | — | `0x011444` | `textedit.s:1779` | — |
| **`TE_PASTE_BODY`** | — | `0x011B74` | `textedit.s:2789` | TE_PASTE_BODY -- shared paste body (TEPaste / TEStylPaste) For unstyled TE: pastes the TEScrpHandle text directly. For styled TE: allocates a temp handle, calls _GetScrap with 'TEXT' resType (0x544558... |
| **`TE_PASTE_BODY_RTS`** | — | `0x011BC6` | `textedit.s:2825` | — |
| **`TE_PASTE_DISPOSE_TEMP`** | — | `0x011BAA` | `textedit.s:2812` | — |
| **`TE_PASTE_PLAIN`** | — | `0x011BB0` | `textedit.s:2816` | — |
| **`TE_PIXELY_FOUND_LINE`** | — | `0x011338` | `textedit.s:1643` | — |
| **`TE_PIXELY_RTS`** | — | `0x01133C` | `textedit.s:1646` | — |
| **`TE_PIXELY_SIMPLE_DIV`** | — | `0x011312` | `textedit.s:1624` | — |
| **`TE_PIXELY_TO_LINE`** | — | `0x0112F6` | `textedit.s:1613` | TE_PIXELY_TO_LINE - convert y-coord to line index. In: D0 = absolute y-coord (port-relative). Out: D0 = line index, D1 set negative if before, GE if past. Unstyled TE: divides by lineHite. Styled TE: ... |
| **`TE_PIXELY_WALK_HEIGHTS`** | — | `0x011316` | `textedit.s:1627` | — |
| **`TE_PIXELY_WALK_LOOP`** | — | `0x011326` | `textedit.s:1634` | — |
| **`TE_PREP_STYLES_FOR_PASTE`** | — | `0x011F2A` | `textedit.s:3313` | TE_PREP_STYLES_FOR_PASTE - prepare style runs for non-styled paste. For unstyled TE: just preserves D5. For styled TE: collapses adjacent identical style runs in the selection range so paste doesn't f... |
| **`TE_PREP_STYLES_INSERT_AT`** | — | `0x011F46` | `textedit.s:3325` | — |
| **`TE_PREP_STYLES_RTS`** | — | `0x011F54` | `textedit.s:3331` | — |
| **`TE_PROLOGUE_BODY`** | — | `0x011354` | `textedit.s:1677` | — |
| **`TE_PROLOGUE_COMMON`** | — | `0x011384` | `textedit.s:1695` | — |
| **`TE_PROLOGUE_DISPATCHED`** | — | `0x011428` | `textedit.s:1753` | — |
| **`TE_PROLOGUE_NO_DISPATCH`** | — | `0x01137E` | `textedit.s:1692` | — |
| **`TE_PROLOGUE_NODISP`** | — | `0x011352` | `textedit.s:1675` | TE_PROLOGUE_NODISP - universal _TE prologue (non-dispatched). Called by all standard _TE traps with TEHandle as param. Sets up A6 frame, locks TERec and text handle, saves port, clips to teViewRect, a... |
| **`TE_PROLOGUE_PORT_STYLED`** | — | `0x0113D0` | `textedit.s:1722` | — |
| **`TE_PROLOGUE_RTS`** | — | `0x01142C` | `textedit.s:1755` | — |
| **`TE_PROLOGUE_SEL_OK`** | — | `0x01141A` | `textedit.s:1746` | — |
| **`TE_PUT_STYL_SCRAP`** | — | `0x01149E` | `textedit.s:1829` | TE_PUT_STYL_SCRAP - write 'styl' resource for selection to scrap. In: D0 = packed (selStart, selEnd). Builds a styl record (header word + 20-byte StScrpRec entries per style run in selection range), c... |
| **`TE_REBUILD_LH_AFTER_DETECT`** | — | `0x011A80` | `textedit.s:2638` | — |
| **`TE_REBUILD_LH_BOTH`** | — | `0x011A70` | `textedit.s:2628` | — |
| **`TE_REBUILD_LH_NEXT_LINE`** | — | `0x011A72` | `textedit.s:2630` | — |
| **`TE_REBUILD_LH_NEXT_RUN`** | — | `0x011A60` | `textedit.s:2621` | — |
| **`TE_REBUILD_LH_RTS`** | — | `0x011AAC` | `textedit.s:2655` | Done: write terminator and compute redraw bounds. |
| **`TE_REBUILD_LH_RUN_LOOP`** | — | `0x011A3E` | `textedit.s:2608` | — |
| **`TE_REBUILD_LH_STORE`** | — | `0x011A58` | `textedit.s:2618` | — |
| **`TE_REBUILD_LH_WALK`** | — | `0x011A28` | `textedit.s:2599` | Empty-TE special case: write one line with default style metrics. TE_REBUILD_LH_WALK -- per-line height computation walk For each line: walks all style runs covering this line, computing max(line heig... |
| **`TE_REBUILD_LINEHEIGHTS`** | — | `0x0119CC` | `textedit.s:2552` | TE_REBUILD_LINEHEIGHTS -- styled-TextEdit per-line height table rebuild For styled TE, walks the per-line styleRun + lineHeights table recomputing each line's height from the maximum style-run height.... |
| **`TE_RECALC_LINES`** | — | `0x0115F8` | `textedit.s:2023` | TE_RECALC_LINES - recalculate line breaks after text change. Saves total height before recalc, calls P_doTERecal, then computes new total height; if shrunk, erases the now-empty portion of teRect and ... |
| **`TE_RECALC_LINES_REDRAW`** | — | `0x011638` | `textedit.s:2045` | — |
| **`TE_REENABLE_BLINK`** | — | `0x011FD8` | `textedit.s:3419` | TE_REENABLE_BLINK - re-enable caret blink if active and at caret. Used after scroll/insert to ensure caret keeps blinking. |
| **`TE_REENABLE_BLINK_EXIT`** | — | `0x011FEE` | `textedit.s:3426` | — |
| **`TE_RESIZE_AND_DEREF`** | — | `0x010ADA` | `textedit.s:508` | TE_RESIZE_AND_DEREF - allocate handle for styled TE without losing TERec/text-handle locks across heap compaction. In: D0 = size to allocate. Out: A0 = new handle (relocked TERec/text after). Unlocks ... |
| **`TE_RESIZE_STYLERECS`** | — | `0x01085E` | `textedit.s:236` | TE_RESIZE_STYLERECS - resize StyleRec arrays after text change. Only called for styled TextEdit (high bit of $50(A3) set). Resizes element handle to $1C bytes and line heights handle to $12 bytes, the... |
| **`TE_RESIZE_STYLERECS_RTS`** | — | `0x010888` | `textedit.s:250` | — |
| **`TE_RESIZE_SYSERROR`** | — | `0x0108AC` | `textedit.s:270` | Called by: TENEW, TESTYLNEW, TE_RESIZE_TEXTHANDLE, TE_RESIZE_AND_DEREF |
| **`TE_RESIZE_TEXTHANDLE`** | — | `0x01088A` | `textedit.s:257` | TE_RESIZE_TEXTHANDLE - resize handle while keeping text handle locked. Unlocks text handle, resizes A0 to D0 bytes, re-locks text. Called by: TE_RESIZE_STYLERECS, TE_FULL_REBUILD_GROW_BUF, TE_REBUILD_... |
| **`TE_SPLIT_STYLERUN_AT`** | — | `0x011D40` | `textedit.s:3029` | TE_SPLIT_STYLERUN_AT -- split styleRun at charPos D0 A0 -> styleRun array cursor. If the next run already starts at D0, no split needed (TE_SPLIT_STYLERUN_RTS). Otherwise inserts a new run at A0+4 wit... |
| **`TE_SPLIT_STYLERUN_RTS`** | — | `0x011D64` | `textedit.s:3045` | — |
| **`TE_STYL_PASTE`** | — | `0x011C30` | `textedit.s:2899` | TE_STYL_PASTE -- styled-paste 'styl' resource handler Called from TE_DO_PASTE when both teStyleRec is set and the caller requested styled paste (TEStylPaste). Fetches the 'styl' resource (resType 0x73... |
| **`TE_STYL_PASTE_DISPOSE`** | — | `0x011CEE` | `textedit.s:2976` | — |
| **`TE_STYL_PASTE_LOOP`** | — | `0x011CA8` | `textedit.s:2947` | TE_STYL_PASTE_LOOP -- per-styl-element walk |
| **`TE_STYL_PASTE_NEXT_ELEM`** | — | `0x011CD2` | `textedit.s:2965` | — |
| **`TE_STYL_PASTE_RTS`** | — | `0x011CF6` | `textedit.s:2980` | — |
| **`TE_STYL_PASTE_USE_INDEX`** | — | `0x011CCC` | `textedit.s:2961` | — |
| **`TE_STYL_PASTE_WALK`** | — | `0x011C74` | `textedit.s:2925` | — |
| **`TE_TOTAL_HEIGHT`** | — | `0x0110E4` | `textedit.s:1317` | TE_TOTAL_HEIGHT - sum line heights for lines D0..D1-1. Unstyled TE: lineHeight is constant in TERec.lineHite. Styled TE: walks lineHeights array in StyleRec, masking 0x7FFF (the high bit is the line-e... |
| **`TE_TOTAL_HEIGHT_LOOP`** | — | `0x011110` | `textedit.s:1336` | — |
| **`TE_TOTAL_HEIGHT_RTS`** | — | `0x01111E` | `textedit.s:1343` | — |
| **`TE_TOTAL_HEIGHT_SIMPLE`** | — | `0x0110F8` | `textedit.s:1325` | — |
| **`TE_TOTAL_HEIGHT_WALK`** | — | `0x0110FE` | `textedit.s:1328` | — |
| **`TE_VIEWRECT_BOTTOM_OK`** | — | `0x0112CA` | `textedit.s:1586` | — |
| **`TEActivate`** | `0x016A62` | `0x011B08` | `textedit.s:1572` | _TEActivate ($A9D8) Called during boot. |
| **`TEACTIVATE`** | `0x016A62` | `0x011B08` | `textedit.s:2721` | **Proto:** `Pascal: procedure TEActivate(hTE: TEHandle);`<br>_TEActivate ($A9D8) - activate a TE field (start blinking). Pascal: procedure TEActivate(hTE: TEHandle); Sets teActive flag, marks for caret blink if no selection, highlights selection if any. |
| **`TEACTIVATE_NO`** | `0x016A7A` | `0x011B20` | `textedit.s:1580`<br>`textedit.s:2729` | — |
| **`TEACTIVATE_OK`** | `0x016A82` | `0x011B28` | `textedit.s:1583`<br>`textedit.s:2732` | — |
| **`TEAutoView`** | `0x016D2C` | `0x0120E8` | `textedit.s:2037` | **Proto:** `Pascal: PROCEDURE TEAutoView(auto: BOOLEAN; hTE: TEHandle);`<br>**Regs:** `Entry: 8(A6) = hTE, $C(A6) = auto (6 bytes, popped on exit)`<br>_TEAutoView ($A813): enable or disable automatic scrolling Pascal: PROCEDURE TEAutoView(auto: BOOLEAN; hTE: TEHandle); Entry: 8(A6) = hTE, $C(A6) = auto (6 bytes, popped on exit) Sets (auto = TRUE) or... |
| **`TEAUTOVIEW`** | `0x016D2C` | `0x0120E8` | `textedit.s:3561` | **Proto:** `Pascal: procedure TEAutoView(auto: BOOLEAN; hTE: TEHandle);`<br>_TEAutoView ($A813) - enable/disable automatic selection scrolling. Pascal: procedure TEAutoView(auto: BOOLEAN; hTE: TEHandle); Sets bit 6 of teCROnly+1 (0x42 in TERec) based on param. |
| **`TEAUTOVIEW_EXIT`** | — | `0x0120FE` | `textedit.s:3569` | — |
| **`TECalText`** | `0x016200` | `0x01092A` | `textedit.s:251` | **Proto:** `TECalText -- _TECalText ($A9D0): PROCEDURE TECalText (hTE: TEHandle);`<br>TECalText -- _TECalText ($A9D0): PROCEDURE TECalText (hTE: TEHandle); _TECalText ($A9D0) |
| **`TECALTEXT`** | `0x016200` | `0x01092A` | `textedit.s:334` | _TECalText ($A9D0) - recalculate line starts after manual edit. |
| **`TECALTEXT_EXIT`** | `0x016206` | `0x010930` | `textedit.s:254`<br>`textedit.s:337` | — |
| **`TECALTEXT_EXIT_2`** | `0x016208` | — | `textedit.s:256` | — |
| **`TECALTEXT_EXIT_3`** | `0x01622E` | — | `textedit.s:270` | — |
| **`TEClick`** | `0x01630E` | `0x010B2E` | `textedit.s:390` | **Proto:** `Pascal: procedure TEClick(pt: Point; extend: BOOLEAN; hTE: TEHandle);`<br>_TEClick ($A9D4) _TEClick ($A9D4): handle a mouse click in a TextEdit field Pascal: procedure TEClick(pt: Point; extend: BOOLEAN; hTE: TEHandle); Sets selection, handles double-click word selection, t... |
| **`TECLICK`** | `0x01630E` | `0x010B2E` | `textedit.s:568` | **Proto:** `Pascal: procedure TEClick(pt: Point; extend: BOOLEAN; hTE: TEHandle);`<br>_TEClick ($A9D4) - handle a mouse click in a TextEdit field. Pascal: procedure TEClick(pt: Point; extend: BOOLEAN; hTE: TEHandle); Sets selection, handles double-click word selection, and tracks the m... |
| **`TECLICK_AFTER_ANCHOR`** | — | `0x010B78` | `textedit.s:595` | — |
| **`TECLICK_CONT`** | `0x01635C` | — | `textedit.s:424` | — |
| **`TECLICK_CONT_10`** | `0x0164E6` | `0x010EF0` | `textedit.s:660`<br>`textedit.s:1069` | TECLICK_CONT_10 Called during boot. |
| **`TECLICK_CONT_10_RTS`** | — | `0x010F1E` | `textedit.s:1088` | — |
| **`TECLICK_CONT_11`** | `0x0164F4` | `0x010EFE` | `textedit.s:667`<br>`textedit.s:1076` | — |
| **`TECLICK_CONT_12`** | `0x01650E` | — | `textedit.s:677` | — |
| **`TECLICK_CONT_2`** | `0x0163A4` | `0x010BBE` | `textedit.s:460`<br>`textedit.s:626` | — |
| **`TECLICK_CONT_3`** | `0x0163D8` | `0x010BF2` | `textedit.s:492`<br>`textedit.s:655` | — |
| **`TECLICK_CONT_4`** | `0x0163EA` | — | `textedit.s:506` | TECLICK_CONT_4 |
| **`TECLICK_CONT_5`** | `0x0163F4` | `0x010C16` | `textedit.s:516`<br>`textedit.s:678` | TECLICK_CONT_5 -- convert point to char offset -> D6. TECLICK_CONT_5 |
| **`TECLICK_CONT_6`** | `0x016406` | `0x010C28` | `textedit.s:529`<br>`textedit.s:689` | TECLICK_CONT_6 |
| **`TECLICK_CONT_7`** | `0x01640C` | `0x010C2E` | `textedit.s:537`<br>`textedit.s:692` | TECLICK_CONT_7 |
| **`TECLICK_CONT_8`** | `0x01648A` | — | `textedit.s:594` | — |
| **`TECLICK_CONT_9`** | `0x0164CE` | — | `textedit.s:644` | TECLICK_CONT_9 Called during boot. |
| **`TECLICK_DONE`** | `0x01651C` | `0x010F2E` | `textedit.s:690`<br>`textedit.s:1102` | — |
| **`TECLICK_EMPTY`** | `0x01638C` | `0x010BA6` | `textedit.s:449`<br>`textedit.s:615` | — |
| **`TECLICK_EXIT`** | `0x016484` | — | `textedit.s:591` | — |
| **`TECLICK_EXIT_2`** | `0x0164C2` | `0x010E6C` | `textedit.s:632`<br>`textedit.s:980` | TECLICK_EXIT_2 Called during boot. |
| **`TECLICK_FOUND`** | `0x01641C` | — | `textedit.s:548` | TECLICK_FOUND |
| **`TECLICK_FOUND_2`** | `0x01645A` | — | `textedit.s:577` | TECLICK_FOUND_2 |
| **`TECLICK_FOUND_3`** | `0x016518` | `0x010F2A` | `textedit.s:687`<br>`textedit.s:1099` | TECLICK_FOUND_3 |
| **`TECLICK_LOOP`** | `0x016380` | `0x010B9A` | `textedit.s:443`<br>`textedit.s:609` | — |
| **`TECLICK_NEXT`** | `0x016494` | — | `textedit.s:606` | — |
| **`TECLICK_NO`** | `0x016358` | `0x010B74` | `textedit.s:421`<br>`textedit.s:592` | detect double-click: compare click time with previous TECLICK_NO |
| **`TECLICK_NO_2`** | `0x016360` | — | `textedit.s:432` | TECLICK_NO_2 |
| **`TECLICK_NO_3`** | `0x016436` | — | `textedit.s:558` | — |
| **`TECLICK_NO_4`** | `0x016474` | — | `textedit.s:585` | — |
| **`TECLICK_OK`** | `0x0163C4` | `0x010BDE` | `textedit.s:481`<br>`textedit.s:644` | dragging backward: update selStart TECLICK_OK |
| **`TECLICK_OK_2`** | `0x0163E6` | `0x010C00` | `textedit.s:498`<br>`textedit.s:661` | — |
| **`TECLICK_OK_3`** | `0x01648E` | — | `textedit.s:603` | TECLICK_OK_3 Called during boot. |
| **`TECLICK_OK_4`** | `0x0164DE` | — | `textedit.s:650` | — |
| **`TECLICK_OK_5`** | `0x0164FE` | `0x010F08` | `textedit.s:671`<br>`textedit.s:1080` | — |
| **`TECLICK_SET_CARET`** | — | `0x010C04` | `textedit.s:664` | — |
| **`TECLICK_UNHIGHLIGHT`** | — | `0x010B7C` | `textedit.s:598` | — |
| **`TEContinuousStyle_Entry`** | — | `0x0123B6` | `textedit.s:3981` | _TEContinuousStyle ($A83A) -- query continuous style at selection Stack: hTE, var mode (W), var TextStyle (18 bytes). For styled TE: looks up the style at selStart and writes its family/face/size/colo... |
| **`TEContinuousStyle_Exit`** | — | `0x01241C` | `textedit.s:4019` | — |
| **`TEContinuousStyle_PlainPath`** | — | `0x0123F8` | `textedit.s:4006` | TEContinuousStyle_PlainPath -- plain TE: synthesize TextStyle from teInPort |
| **`TECopy`** | `0x0167AE` | `0x011446` | `textedit.s:1106` | _TECopy ($A9D5) _TECopy ($A9D5): copy selection to TE scrap |
| **`TECOPY`** | `0x0167AE` | `0x011446` | `textedit.s:1788` | **Proto:** `Pascal: procedure TECopy(hTE: TEHandle);`<br>_TECopy ($A9D5) - copy selection to TextEdit scrap. Pascal: procedure TECopy(hTE: TEHandle); Copies teSelStart..teSelEnd bytes into TEScrpHandle, then (for styled TE) writes 'styl' resource to system ... |
| **`TECOPY_CLAMP_ZERO`** | — | `0x0114EE` | `textedit.s:1862` | — |
| **`TECOPY_DISPOSE_TEMP`** | — | `0x01150E` | `textedit.s:1876` | — |
| **`TECOPY_EXIT`** | `0x0167D0` | — | `textedit.s:1120` | copy selected text to scrap handle |
| **`TECOPY_FIRST_RUN`** | — | `0x0114D4` | `textedit.s:1850` | — |
| **`TECOPY_PUTSCRAP_DONE`** | — | `0x01149A` | `textedit.s:1820` | — |
| **`TECut`** | `0x0167D4` | `0x011514` | `textedit.s:1127` | _TECut ($A9D6): cut selection (copy + delete) |
| **`TECUT`** | `0x0167D4` | `0x011514` | `textedit.s:1883` | _TECut ($A9D6) - copy selection then delete. Implementation: _TECopy followed by _TEDelete. |
| **`TEDeactivate`** | `0x016A84` | `0x011B2A` | `textedit.s:1591` | _TEDeactivate ($A9D9) Called during boot. |
| **`TEDEACTIVATE`** | `0x016A84` | `0x011B2A` | `textedit.s:2739` | **Proto:** `Pascal: procedure TEDeactivate(hTE: TEHandle);`<br>_TEDeactivate ($A9D9) - deactivate TE field (stop caret). Pascal: procedure TEDeactivate(hTE: TEHandle); Hides caret, unhighlights selection, clears teActive flag. |
| **`TEDelete`** | `0x0167E2` | `0x011524` | `textedit.s:1140` | _TEDelete ($A9D7) _TEDelete ($A9D7): delete the current selection |
| **`TEDELETE`** | `0x0167E2` | `0x011524` | `textedit.s:1896` | **Proto:** `Pascal: procedure TEDelete(hTE: TEHandle);`<br>_TEDelete ($A9D7) - delete selection range. Pascal: procedure TEDelete(hTE: TEHandle); Hides caret, removes chars from text via _Munger, recalcs line breaks, repositions caret, scrolls into view. |
| **`TEDELETE_CONT`** | `0x0167F8` | — | `textedit.s:1154` | TEDELETE_CONT -- remove selected text from buffer. TEDELETE_CONT |
| **`TEDELETE_CONT_2`** | `0x016818` | `0x010E78` | `textedit.s:1176`<br>`textedit.s:992` | TEDELETE_CONT_2 -- recalculate lines and redraw. TEDELETE_CONT_2 |
| **`TEDELETE_CONT_3`** | `0x01684E` | `0x01163E` | `textedit.s:1201`<br>`textedit.s:2052` | TEDELETE_CONT_3 Called during boot. |
| **`TEDELETE_EMPTY`** | `0x016816` | — | `textedit.s:1168` | — |
| **`TEDISPATCH`** | — | `0x01142E` | `textedit.s:1763` | **Proto:** `Pascal: procedure TEDispatch(selector: INTEGER; ...);`<br>TEDISPATCH ($A83D) - styled-TE dispatch trap. Pascal: procedure TEDispatch(selector: INTEGER; ...); Calls TE_PROLOGUE_BODY with D0=1 to take dispatch table indirection, then jumps to the handler retur... |
| **`TEDispose`** | `0x0160C0` | `0x010722` | `textedit.s:84` | install default hook routines _TEDispose ($A9CD) Called during boot. |
| **`TEDISPOSE`** | `0x0160C0` | `0x010722` | `textedit.s:88` | _TEDispose ($A9CD) - free TERec and its text handle. If teStyleRec (high bit of teJust+1) is set, also frees the StyleRec, its element handle, and line height handle. (SE FDHD adds StyleRec disposal t... |
| **`TEDISPOSE_FREE_STYLEREC`** | — | `0x010754` | `textedit.s:105` | — |
| **`TEDOTEXT_ADV_PAST_LINES`** | — | `0x011058` | `textedit.s:1247` | TEDOTEXT_ADV_PAST_LINES - advance pen (teRectTop) past N lines. In: D0 = number of lines to advance, D1 = run height. Updates teRectTop, teRectLeft, A2 = lineStarts entry. |
| **`TEDOTEXT_CLAMP_DRAW_END`** | — | `0x010E36` | `textedit.s:951` | — |
| **`TEDOTEXT_DRAW_BEGIN`** | — | `0x010DA4` | `textedit.s:894` | TEDOTEXT_DRAW_BEGIN - P_TEDoText D7=-1 path: redraw all visible lines. Used by _TEUpdate. Walks each line in the destRect, erases trailing space, _MoveTo's the baseline, and _DrawText's the line conte... |
| **`TEDOTEXT_DRAW_RUN`** | — | `0x010E24` | `textedit.s:942` | — |
| **`TEDOTEXT_ERASE_TAIL`** | — | `0x010EA8` | `textedit.s:1011` | — |
| **`TEDOTEXT_EXTEND_LEFT`** | — | `0x010E92` | `textedit.s:1002` | — |
| **`TEDOTEXT_INIT_SCAN_STATE`** | — | `0x011084` | `textedit.s:1273` | TEDOTEXT_INIT_SCAN_STATE - initialize text scan state for P_TEDoText loop. Sets teRect to teDestRect, advances teRectTop past prior lines (using cumulative line heights), applies justification, stores... |
| **`TEDOTEXT_LINE_BOUNDS`** | — | `0x01100E` | `textedit.s:1210` | TEDOTEXT_LINE_BOUNDS - compute hilite-rect bounds for D3..D4 char range on the current line. Out: D0/D1 = pixel positions of selStart/selEnd within line. Sets teRectLeft = start-marker if D0 == D3 (ra... |
| **`TEDOTEXT_LINE_BOUNDS_CMP_SEL`** | — | `0x011042` | `textedit.s:1232` | — |
| **`TEDOTEXT_LINE_BOUNDS_LAST_RUN`** | — | `0x011030` | `textedit.s:1223` | — |
| **`TEDOTEXT_LINE_BOUNDS_NORMAL_LEFT`** | — | `0x01104C` | `textedit.s:1236` | — |
| **`TEDOTEXT_LINE_BOUNDS_OK`** | — | `0x010EE8` | `textedit.s:1057` | — |
| **`TEDOTEXT_LINE_BOUNDS_RTS`** | — | `0x011056` | `textedit.s:1240` | — |
| **`TEDOTEXT_LINE_DONE`** | — | `0x010E5C` | `textedit.s:970` | — |
| **`TEDOTEXT_LINE_LEFT`** | — | `0x010F76` | `textedit.s:1148` | Called by: P_TEDoText, P_TEDOTEXT_NO |
| **`TEDOTEXT_NEG_ASCENT`** | — | `0x010DFA` | `textedit.s:924` | — |
| **`TEDOTEXT_NEXT_LINE`** | — | `0x010DB0` | `textedit.s:898` | — |
| **`TEDOTEXT_NEXT_VISLINE`** | — | `0x010EDC` | `textedit.s:1052` | TEDOTEXT_NEXT_VISLINE - check if next line is in viewable range. Out: D4 = clamped line end, CCR = compare D5 vs D3 (LS=past visible, GT=more lines to draw). |
| **`TEDOTEXT_NORMAL_DRAW`** | — | `0x010DC8` | `textedit.s:905` | — |
| **`TEDOTEXT_REPOS_MOVETO`** | — | `0x011228` | `textedit.s:1504` | — |
| **`TEDOTEXT_REPOS_PEN`** | — | `0x0111FE` | `textedit.s:1488` | TEDOTEXT_REPOS_PEN - reposition pen for line drawing. Computes pen position based on selStart/selEnd char range within the current line, then _MoveTo's there. Used at the start of each line during P_T... |
| **`TEDOTEXT_REPOS_RANGE`** | — | `0x011214` | `textedit.s:1497` | — |
| **`TEDOTEXT_USE_ASCENT`** | — | `0x010E16` | `textedit.s:935` | — |
| **`TEDOTEXT_USE_RUN_START`** | — | `0x010E44` | `textedit.s:958` | — |
| **`TEFindLine`** | `0x0168C8` | — | `textedit.s:1328` | TE Find Line Called during boot. |
| **`TEFINDLINE_CONT`** | `0x0168DA` | `0x011742` | `textedit.s:1335`<br>`textedit.s:2221` | — |
| **`TEFINDLINE_EMPTY`** | `0x01691E` | — | `textedit.s:1376` | TEFINDLINE_EMPTY |
| **`TEFINDLINE_EXIT`** | `0x016916` | `0x0117A0` | `textedit.s:1367`<br>`textedit.s:2262` | — |
| **`TEFINDLINE_OK`** | `0x016910` | `0x011780` | `textedit.s:1363`<br>`textedit.s:2247` | TEFINDLINE_OK Called during boot. |
| **`TEFINDLINE_SKIP`** | `0x0168F0` | `0x01175A` | `textedit.s:1345`<br>`textedit.s:2231` | — |
| **`TEFindWord`** | `0x016854` | — | `textedit.s:1210` | TE Find Word Called during boot. |
| **`TEFINDWORD_CONT`** | `0x016862` | `0x011652` | `textedit.s:1218`<br>`textedit.s:2070` | — |
| **`TEFINDWORD_CONT_2`** | `0x016874` | `0x011664` | `textedit.s:1240`<br>`textedit.s:2083` | TEFINDWORD_CONT_2 Called during boot. |
| **`TEFINDWORD_CONT_3`** | `0x016878` | `0x011668` | `textedit.s:1242`<br>`textedit.s:2085` | — |
| **`TEFINDWORD_CONT_4`** | `0x01688A` | `0x01167A` | `textedit.s:1266`<br>`textedit.s:2103` | TEFINDWORD_CONT_4 Called during boot. |
| **`TEFINDWORD_DONE`** | `0x016872` | `0x011662` | `textedit.s:1232`<br>`textedit.s:2078` | TEFINDWORD_DONE Called during boot. |
| **`TEFINDWORD_DONE_2`** | `0x016888` | `0x011678` | `textedit.s:1258`<br>`textedit.s:2095` | — |
| **`TEFINDWORD_FOUND`** | `0x016886` | `0x011676` | `textedit.s:1256`<br>`textedit.s:2093` | TEFINDWORD_FOUND Called during boot. |
| **`TEFINDWORD_SKIP`** | `0x01685E` | `0x01164E` | `textedit.s:1216`<br>`textedit.s:2068` | — |
| **`TEGETOFFSET`** | — | `0x01254E` | `textedit.s:4206` | _TEGetOffset ($A83A) -- pixel position to char offset Stack: hTE, point, var offset.  Sets teSelPoint (0x1C) to the supplied point, calls TECLICK_CONT_5 which fills D6 with the char offset under the p... |
| **`TEGetStyleHandle_Entry`** | — | `0x012568` | `textedit.s:4221` | _TEGetStyleHandle ($A839) -- get StyleRec handle Returns TERec.teStyleRec (offset 0x4A, the StyleHandle) on stack, or nil if TE is unstyled (teStyleRec offset 0x50 >= 0). |
| **`TEGetStyleHandle_Exit`** | — | `0x012574` | `textedit.s:4226` | — |
| **`TEGetText`** | `0x01608E` | `0x0106F0` | `textedit.s:53` | **Proto:** `TEGetText -- _TEGetText ($A9CB): FUNCTION TEGetText (hTE: TEHandle) : CharsHandle;`<br>TextEdit Apple source: TextEdit.a (MacSEROM.lst module TEXTEDIT). Basic text editing: TEGetText, TEInit, TEDispose, TextBox, TESetText, TECalText, TESetSelect, TENew, TEUpdate, TEClick, TECopy, TECut,... |
| **`TEGETTEXT`** | `0x01608E` | `0x0106F0` | `textedit.s:61` | _TEGetText ($A9CB) -- return TERec.hText handle Stack: hTE(L) -> Handle. Walks the TERec to find hText (the Pascal handle to the underlying text storage) and returns it on the stack. |
| **`TEHILITE_DRAW_ENTRY`** | — | `0x010F90` | `textedit.s:1163` | TEHILITE_DRAW_ENTRY - P_TEDoText D7=1 path: highlight selection range. Calls 0x56(A3) (teHiliteHook) once per fully-selected line, then handles partial-line highlighting at the boundaries. Used for bo... |
| **`TEHILITE_END_LINE`** | — | `0x010FF2` | `textedit.s:1192` | — |
| **`TEIdle`** | `0x016A9A` | `0x011B40` | `textedit.s:1606` | _TEIdle ($A9DA) _TEIdle ($A9DA): blink the text cursor (caret) Called repeatedly from event loop; toggles caret at CaretTime rate |
| **`TEIDLE`** | `0x016A9A` | `0x011B40` | `textedit.s:2753` | **Proto:** `Pascal: procedure TEIdle(hTE: TEHandle);`<br>_TEIdle ($A9DA) - blink the caret if blink interval passed. Pascal: procedure TEIdle(hTE: TEHandle); If caret-blink enabled and CaretTime ticks have elapsed, toggle caret state via XOR. |
| **`TEIDLE_EXIT`** | `0x016ABE` | — | `textedit.s:1619` | — |
| **`TEInit`** | `0x01609A` | `0x0106FC` | `textedit.s:65` | _TEInit ($A9CC) Called during boot. _TEInit ($A9CC): initialize TextEdit Sets up scrap handle and hook vectors for text operations |
| **`TEINIT`** | `0x01609A` | `0x0106FC` | `textedit.s:70` | _TEInit ($A9CC) - initialize TextEdit globals. Allocates empty scrap handle and installs default TEDoText/TERecal/TEWdBreak hook procedures. |
| **`TEInsert`** | `0x016B80` | `0x011E58` | `textedit.s:1738` | TEInsert -- trap handler for _TEInsert ($A9DE). _TEInsert ($A9DE) |
| **`TEINSERT`** | `0x016B80` | `0x011E58` | `textedit.s:3207` | **Proto:** `Pascal: procedure TEInsert(text: Ptr; length: LongInt;`<br>_TEInsert ($A9DE) - insert text into TE field at selection. Pascal: procedure TEInsert(text: Ptr; length: LongInt; hTE: TEHandle); Hides caret, inserts text via _Munger, recalcs lines, moves selection... |
| **`TEINSERT_EXIT`** | `0x016BA8` | — | `textedit.s:1750` | — |
| **`TEKey`** | `0x016BAE` | `0x011E86` | `textedit.s:1761` | **Proto:** `Pascal: procedure TEKey(key: CHAR; hTE: TEHandle);`<br>_TEKey ($A9DC) _TEKey ($A9DC): handle a keystroke in a TextEdit field Pascal: procedure TEKey(key: CHAR; hTE: TEHandle); Inserts character at selection, or handles backspace/arrows |
| **`TEKEY`** | `0x016BAE` | `0x011E86` | `textedit.s:3229` | **Proto:** `Pascal: procedure TEKey(key: CHAR; hTE: TEHandle);`<br>_TEKey ($A9DC) - process a typed character. Pascal: procedure TEKey(key: CHAR; hTE: TEHandle); Handles arrows (28-31): move caret without inserting. Backspace (8): delete char before selection or sele... |
| **`TEKEY_CONT`** | `0x016BE2` | `0x011F20` | `textedit.s:1783`<br>`textedit.s:3300` | — |
| **`TEKEY_DONE`** | `0x016BE6` | `0x011F24` | `textedit.s:1786`<br>`textedit.s:3304` | Called by: TEKEY_SET_SELECTION, TEKEY_INSERT_CHAR, TEKEY_OK, TESETJUST, TEAUTOVIEW_EXIT |
| **`TEKEY_DOWN_ARROW`** | — | `0x011EDC` | `textedit.s:3265` | — |
| **`TEKEY_INSERT_CHAR`** | — | `0x011EFC` | `textedit.s:3281` | — |
| **`TEKEY_LEFT_ARROW`** | — | `0x011EE4` | `textedit.s:3269` | — |
| **`TEKEY_NOT_ARROW`** | — | `0x011EAE` | `textedit.s:3247` | — |
| **`TEKEY_OK`** | `0x016BCC` | `0x011F0A` | `textedit.s:1775`<br>`textedit.s:3292` | normal character: insert at selection point backspace: delete character before selection |
| **`TEKEY_SET_SELECTION`** | — | `0x011EEC` | `textedit.s:3273` | — |
| **`TEKEY_UP_ARROW`** | — | `0x011EB0` | `textedit.s:3249` | — |
| **`TEKEY_VERT_ARROW`** | — | `0x011EB2` | `textedit.s:3251` | — |
| **`TENew`** | `0x016266` | `0x0109BA` | `textedit.s:300` | **Proto:** `Pascal: function TENew(destRect, viewRect: Rect): TEHandle;`<br>_TENew ($A9D2) _TENew ($A9D2): create a new TextEdit record Pascal: function TENew(destRect, viewRect: Rect): TEHandle; Allocates a 104-byte TERec, sets up text handle, font metrics |
| **`TENEW`** | `0x016266` | `0x0109BA` | `textedit.s:398` | **Proto:** `Pascal: function TENew(destRect, viewRect: Rect): TEHandle;`<br>_TENew ($A9D2) - allocate a new TextEdit record. Pascal: function TENew(destRect, viewRect: Rect): TEHandle; Allocates 104-byte TERec, sets text handle, font metrics (ascent + lineHeight), grafPort, f... |
| **`TENEW_ERR`** | `0x0162DA` | — | `textedit.s:342` | allocate empty text handle copy destRect and viewRect from parameters get font metrics for line height calculation |
| **`TEPaste`** | `0x016AC2` | `0x011B68` | `textedit.s:1626` | _TEPaste ($A9DB): paste TE scrap at selection point |
| **`TEPASTE`** | `0x016AC2` | `0x011B68` | `textedit.s:2775` | **Proto:** `Pascal: procedure TEPaste(hTE: TEHandle);`<br>_TEPaste ($A9DB) - paste TE scrap into selection. Pascal: procedure TEPaste(hTE: TEHandle); For unstyled TE: pastes text from TEScrpHandle. For styled TE: also reads 'styl' resource from system scrap. |
| **`TEPASTE_CONT`** | `0x016AE2` | — | `textedit.s:1643` | TEPASTE_CONT -- insert scrap text, replacing selection. TEPASTE_CONT |
| **`TEPASTE_CONT_2`** | `0x016B32` | `0x011E14` | `textedit.s:1681`<br>`textedit.s:3160` | TEPASTE_CONT_2 -- set up Munger params (unlock text, push handle+offset). TEPASTE_CONT_2 |
| **`TEPASTE_CONT_3`** | `0x016B48` | — | `textedit.s:1697` | TEPASTE_CONT_3 Called during boot (2,791 times in 30s trace). |
| **`TEPASTE_CONT_4`** | `0x016B60` | — | `textedit.s:1716` | TEPASTE_CONT_4 -- insert text at selection. TEPASTE_CONT_4 |
| **`TEPASTE_ERR`** | `0x016B5E` | — | `textedit.s:1708` | — |
| **`TEPASTE_NO`** | `0x016B30` | — | `textedit.s:1673` | — |
| **`TEPASTE_NO_2`** | `0x016B7E` | — | `textedit.s:1730` | — |
| **`TEPASTE_OK`** | `0x016B5C` | — | `textedit.s:1706` | — |
| **`TEPinScroll`** | `0x016C54` | `0x011FF0` | `textedit.s:1904` | **Proto:** `Pascal: PROCEDURE TEPinScroll(dh, dv: INTEGER; hTE: TEHandle);`<br>**Regs:** `Entry: 8(A6) = hTE, $C(A6) = dv, $E(A6) = dh (8 bytes, popped on exit)`<br>TextEdit automatic scrolling (Mac Plus additions, Inside Macintosh IV) TextEdit code that follows TEScroll directly: TEPinScroll ($A812)  TEScroll with the scroll amount pinned to the text TESelView (... |
| **`TEPINSCROLL`** | `0x016C54` | `0x011FF0` | `textedit.s:3435` | **Proto:** `Pascal: procedure TEPinScroll(dh, dv: INTEGER; hTE: TEHandle);`<br>_TEPinScroll ($A812) - scroll, pinned to text bounds. Pascal: procedure TEPinScroll(dh, dv: INTEGER; hTE: TEHandle); Like TEScroll but clamps the scroll so the destRect stays within the viewable text.... |
| **`TEReplaceStyle_Entry`** | — | `0x0124FC` | `textedit.s:4153` | _TEReplaceStyle ($A83E) -- conditionally apply style edits Like TESetStyle but only edits runs whose existing style matches a caller-supplied template (via StyleMatchesTemplate). Stack has TextStyle p... |
| **`TEReplaceStyle_Exit`** | — | `0x01252E` | `textedit.s:4173` | — |
| **`TEReplaceStyle_Frame`** | — | `0x012534` | `textedit.s:4186` | TEReplaceStyle_Frame -- TEReplaceStyle dispatch frame A2 -> [TextStyle (L), MatchTemplate (L), mode (W)]. Saves regs and sets up A4 = TextStyle, A6 = MatchTemplate (the conditional template used by St... |
| **`TEReplaceStyle_Frame_Exit`** | — | `0x012548` | `textedit.s:4194` | — |
| **`TEReplaceStyle_Redraw`** | — | `0x01250E` | `textedit.s:4162` | TEReplaceStyle_Redraw redraw path: hide caret, edit, recalc, show, scroll. |
| **`TEScroll`** | `0x016C12` | `0x011F96` | `textedit.s:1830` | **Proto:** `TEScroll -- _TEScroll ($A9DD): PROCEDURE TEScroll {dh,dv: INTEGER; hTE : TEHandle);`<br>TEScroll -- _TEScroll ($A9DD): PROCEDURE TEScroll {dh,dv: INTEGER; hTE : TEHandle); _TEScroll ($A9DD) |
| **`TESCROLL`** | `0x016C12` | `0x011F96` | `textedit.s:3379` | **Proto:** `Pascal: procedure TEScroll(dh, dv: INTEGER; hTE: TEHandle);`<br>_TEScroll ($A9DD) - scroll text within view rect. Pascal: procedure TEScroll(dh, dv: INTEGER; hTE: TEHandle); Hides caret, shifts destRect by (dh,dv), invalidates the now-exposed area, redraws. Params... |
| **`TESCROLL_CONT`** | `0x016C24` | `0x011FA8` | `textedit.s:1844`<br>`textedit.s:3392` | TESCROLL_CONT -- apply scroll to text. TESCROLL_CONT |
| **`TESCROLL_DONE`** | `0x016C52` | — | `textedit.s:1865` | — |
| **`TESCROLL_EPILOGUE`** | — | `0x011FA2` | `textedit.s:3384` | — |
| **`TESCROLL_EXIT`** | `0x016C1E` | — | `textedit.s:1835` | — |
| **`TESCROLL_RTS`** | — | `0x011FD6` | `textedit.s:3413` | — |
| **`TESelView`** | `0x016CC0` | `0x01207A` | `textedit.s:1969` | **Proto:** `Pascal: PROCEDURE TESelView(hTE: TEHandle);`<br>_TESelView ($A811): make sure the selection is visible Pascal: PROCEDURE TESelView(hTE: TEHandle); If automatic scrolling is on (TEAutoView), scrolls the text so that the start of the selection is ins... |
| **`TESELVIEW`** | `0x016CC0` | `0x01207A` | `textedit.s:3507` | **Proto:** `Pascal: procedure TESelView(hTE: TEHandle);`<br>_TESelView ($A811) - scroll selection into view if auto. Pascal: procedure TESelView(hTE: TEHandle); If teAutoView (bit 6 of 0x42) is set, scrolls the view so the selection becomes visible. |
| **`TESETALIGNMENT_CONT`** | — | `0x011F7A` | `textedit.s:3362` | TESETALIGNMENT_CONT - redraw text via _TEUpdate of full destRect. Used after scrolling. Runs draw mode (D7=-1) on entire view, refreshes hilite, restores caret. |
| **`TESetJust`** | `0x016BEC` | `0x011F70` | `textedit.s:1799` | **Proto:** `Pascal: PROCEDURE TESetJust(just: INTEGER; hTE: TEHandle);`<br>**Regs:** `Entry: 8(A6) = hTE, $C(A6) = just (6 bytes, popped on exit)`<br>_TESetJust ($A9DF): set the justification of an edit record Pascal: PROCEDURE TESetJust(just: INTEGER; hTE: TEHandle); Entry: 8(A6) = hTE, $C(A6) = just (6 bytes, popped on exit) Stores just (teJustLe... |
| **`TESETJUST`** | `0x016BEC` | `0x011F70` | `textedit.s:3353` | **Proto:** `Pascal: procedure TESetJust(just: INTEGER; hTE: TEHandle);`<br>_TESetJust ($A9DF) - set justification mode. Pascal: procedure TESetJust(just: INTEGER; hTE: TEHandle); Stores just value in teJust (0x3A). |
| **`TESETJUST_CONT`** | `0x016BF6` | — | `textedit.s:1814` | **Regs:** `Entry: A0 -> rect (local coordinates), A3 = TERec (StdEntry state)`<br>TESETJUST_CONT - redraw the text lines that intersect the rect at A0 Entry: A0 -> rect (local coordinates), A3 = TERec (StdEntry state) Draws the visible lines within the rect (TEDoText mode -1), redr... |
| **`TESetSelect`** | `0x01623A` | `0x01098E` | `textedit.s:281` | _TESetSelect ($A9D1) |
| **`TESETSELECT`** | `0x01623A` | `0x01098E` | `textedit.s:379` | **Proto:** `Pascal: procedure TESetSelect(selStart, selEnd: LongInt; hTE: TEHandle);`<br>_TESetSelect ($A9D1) - change selection range. Pascal: procedure TESetSelect(selStart, selEnd: LongInt; hTE: TEHandle); Hides the caret/old selection, updates selStart/selEnd, then highlights the new ... |
| **`TESetStyle_AddSize`** | — | `0x012344` | `textedit.s:3919` | — |
| **`TESetStyle_AddSizeDelta`** | — | `0x012356` | `textedit.s:3925` | — |
| **`TESetStyle_Apply`** | — | `0x0122EE` | `textedit.s:3882` | — |
| **`TESetStyle_AssignIndex`** | — | `0x012372` | `textedit.s:3936` | — |
| **`TESetStyle_ColorCheck`** | — | `0x012332` | `textedit.s:3912` | — |
| **`TESetStyle_Entry`** | — | `0x01220C` | `textedit.s:3753` | _TESetStyle ($A83D) -- apply a TextStyle to the selection Stack: hTE, mode, newStyle, redraw.  Walks the StyleRec applying the requested attribute changes to all style runs that intersect the current ... |
| **`TESetStyle_Exit`** | — | `0x01223E` | `textedit.s:3773` | — |
| **`TESetStyle_FaceCheck`** | — | `0x012300` | `textedit.s:3891` | Apply per-bit edits to the scratch styleEntry at A4: bit 0=family, 1=face, 2=size, 3=color, 4=add-to-size |
| **`TESetStyle_FaceCleared`** | — | `0x01231E` | `textedit.s:3904` | — |
| **`TESetStyle_FaceReplace`** | — | `0x012316` | `textedit.s:3900` | — |
| **`TESetStyle_FindOrAddIndex`** | — | `0x01235A` | `textedit.s:3927` | — |
| **`TESetStyle_Frame`** | — | `0x012244` | `textedit.s:3785` | TESetStyle_Frame -- TESetStyle dispatch frame A2 -> [TextStyle ptr (L), mode (W)].  Saves regs, validates mode in [0..0x10], and dispatches to TESetStyle_Start (the actual style-edit walker).  A4 = Te... |
| **`TESetStyle_Frame_Exit`** | — | `0x012256` | `textedit.s:3793` | — |
| **`TESetStyle_NextRun`** | — | `0x012376` | `textedit.s:3938` | — |
| **`TESetStyle_NoOpRTS`** | — | `0x01238C` | `textedit.s:3946` | — |
| **`TESetStyle_NoStartSplit`** | — | `0x0122D8` | `textedit.s:3872` | — |
| **`TESetStyle_Redraw`** | — | `0x01221E` | `textedit.s:3762` | TESetStyle_Redraw -- redraw path: hide caret, edit, recalc, show, scroll. |
| **`TESetStyle_RunLoop`** | — | `0x0122AE` | `textedit.s:3855` | TESetStyle_RunLoop -- per-run edit loop body For each style run intersecting the selection: 1. Look up its existing styleEntry (GetStyleEntry -> A0) 2. Check if requested edit actually changes anythin... |
| **`TESetStyle_SizeCheck`** | — | `0x012322` | `textedit.s:3906` | — |
| **`TESetStyle_Start`** | — | `0x01225C` | `textedit.s:3813` | TESetStyle_Start -- TESetStyle inner walker A4 -> TextStyle, D7 = mode bitmask. Locates the first style run at selStart (DateToSeconds) and last run at selEnd (CountRunsBefore). Allocates an 18-byte s... |
| **`TESetStyleHandle_Entry`** | — | `0x01257A` | `textedit.s:4235` | _TESetStyleHandle ($A83B) -- install caller-supplied StyleRec Stack: hTE, newStyleHandle.  No-op if TE is unstyled. |
| **`TESetStyleHandle_Exit`** | — | `0x012584` | `textedit.s:4239` | — |
| **`TESetText`** | `0x0161BC` | `0x010828` | `textedit.s:216` | **Proto:** `Pascal: procedure TESetText(text: Ptr; length: LongInt; hTE: TEHandle);`<br>_TESetText ($A9CF) _TESetText ($A9CF): replace all text in a TextEdit field Pascal: procedure TESetText(text: Ptr; length: LongInt; hTE: TEHandle); |
| **`TESETTEXT`** | `0x0161BC` | `0x010828` | `textedit.s:210` | **Proto:** `Pascal: procedure TESetText(text: Ptr; length: LongInt; hTE: TEHandle);`<br>_TESetText ($A9CF) - replace all text in a TextEdit field. Pascal: procedure TESetText(text: Ptr; length: LongInt; hTE: TEHandle); |
| **`TESETTEXT_CONT`** | `0x0161E6` | `0x010910` | `textedit.s:237`<br>`textedit.s:323` | TESETTEXT_CONT: recalculate all line starts after text change Clears selection, calls TERecal, then redraws |
| **`TESETTEXT_EXIT`** | `0x0161E2` | `0x01085A` | `textedit.s:229`<br>`textedit.s:227` | — |
| **`TestControl`** | `0x013080` | `0x00D684` | `control_mgr.s:542` | _TestControl ($A966) Called during boot. |
| **`TESTCONTROL`** | `0x013080` | `0x00D684` | `control_mgr.s:455` | **Proto:** `Pascal: function TestControl(theControl: ControlHandle; thePt: Point): INTEGER;`<br>_TestControl ($A966): which part of a control is the point in? Pascal: function TestControl(theControl: ControlHandle; thePt: Point): INTEGER; Returns 0 if invisible, fully disabled (hilite=$FF), or p... |
| **`TESTCONTROL_FOUND`** | `0x0130A8` | `0x00D6AC` | `control_mgr.s:555`<br>`control_mgr.s:468` | — |
| **`TESTYLNEW`** | — | `0x010A2E` | `textedit.s:444` | **Proto:** `Pascal: function TEStylNew(dest, view: Rect): TEHandle;`<br>TEStylNew - allocate a styled TextEdit record (SE FDHD). Pascal: function TEStylNew(dest, view: Rect): TEHandle; Like _TENew but also allocates the StyleRec, element handle, and lineHeights handle, an... |
| **`TESTYLPASTE_ENTRY`** | — | `0x011BC8` | `textedit.s:2835` | TESTYLPASTE_ENTRY -- _TEStylPaste ($A83C) trap entry Same as TEPaste but D7 = 1 indicates styled paste should also read the 'styl' resource via TE_STYL_PASTE. Strips 6 bytes of stack params on return. |
| **`TETEXTBOX_CONT`** | — | `0x010774` | `textedit.s:123` | — |
| **`TETEXTBOX_CONT_2`** | — | `0x0107DA` | `textedit.s:163` | — |
| **`TETEXTBOX_CONT_3`** | — | `0x0107E0` | `textedit.s:167` | — |
| **`TETEXTBOX_DISPOSE_TAIL`** | — | `0x010822` | `textedit.s:203` | — |
| **`TETEXTBOX_EMPTY`** | — | `0x01077E` | `textedit.s:128` | — |
| **`TETEXTBOX_FOUND`** | — | `0x0107EE` | `textedit.s:181` | TETEXTBOX_FOUND - multi-line path: use temporary TERec. Creates TERec with destRect = viewRect = box, sets justification, installs text via TESetText, draws via TEUpdate, then disposes. Called during ... |
| **`TETEXTBOX_NO`** | — | `0x0107EC` | `textedit.s:172` | — |
| **`TETEXTBOX_SKIP`** | — | `0x01081E` | `textedit.s:200` | — |
| **`TEUpdate`** | `0x0162E0` | `0x010B00` | `textedit.s:351` | _TEUpdate ($A9D3) Called during boot. |
| **`TEUPDATE`** | `0x0162E0` | `0x010B00` | `textedit.s:532` | **Proto:** `Pascal: procedure TEUpdate(updateRect: Rect; hTE: TEHandle);`<br>_TEUpdate ($A9D3) - redraw text within an update rectangle. Pascal: procedure TEUpdate(updateRect: Rect; hTE: TEHandle); Called during window updates to redraw the text inside the supplied update rect... |
| **`TEUPDATE_CONT`** | `0x0162EE` | `0x010B0E` | `textedit.s:362`<br>`textedit.s:542` | TEUPDATE_CONT -- get word bounds if double-click. TEUPDATE_CONT |
| **`TEUPDATE_CONT_2`** | `0x0162FC` | `0x010B1C` | `textedit.s:376`<br>`textedit.s:556` | TEUPDATE_CONT_2 Called during boot. |
| **`TEUPDATE_EXIT`** | `0x0162FA` | `0x010B1A` | `textedit.s:368`<br>`textedit.s:548` | — |
| **`TextBox`** | `0x0160DE` | `0x01075E` | `textedit.s:113` | **Proto:** `Pascal: PROCEDURE TextBox(text: Ptr; length: LONGINT; box: Rect;`<br>**Regs:** `Entry: 8(A6) = just, $A(A6) = @box, $E(A6) = length, $12(A6) = text`<br>_TextBox ($A9CE): draw text in a box with the given justification Pascal: PROCEDURE TextBox(text: Ptr; length: LONGINT; box: Rect; just: INTEGER); Entry: 8(A6) = just, $A(A6) = @box, $E(A6) = length, ... |
| **`TEXTBOX`** | `0x0160DE` | `0x01075E` | `textedit.s:116` | _TETextBox ($A9CE) - draw text in a box with justification. Single-line fast path uses _TextWidth/_DrawText with optional centering or right-justify. Multi-line path (CR found or text wider than box) ... |
| **`TEXTBOX_CONT`** | `0x016108` | — | `textedit.s:125` | — |
| **`TEXTBOX_CONT_2`** | `0x01616E` | — | `textedit.s:165` | — |
| **`TEXTBOX_CONT_3`** | `0x016174` | — | `textedit.s:169` | — |
| **`TEXTBOX_EMPTY`** | `0x016112` | — | `textedit.s:130` | — |
| **`TEXTBOX_EXIT`** | `0x0161B6` | — | `textedit.s:205` | — |
| **`TEXTBOX_EXIT_2`** | `0x0161B8` | — | `textedit.s:207` | — |
| **`TEXTBOX_FOUND`** | `0x016182` | — | `textedit.s:183` | TEXTBOX_FOUND - TextBox slow path: text has a CR or is too wide; draw it with a temporary edit record (TENew/TESetText/TEUpdate/TEDispose) Called during boot. |
| **`TEXTBOX_NO`** | `0x016180` | — | `textedit.s:174` | — |
| **`TEXTBOX_SKIP`** | `0x0161B2` | — | `textedit.s:202` | — |
| **`TEXTEDIT`** | — | `0x0106E4` | `textedit.s:49` | TextEdit Apple source: TextEdit.a (MacSEROM.lst module TEXTEDIT). Basic text editing: TEGetText, TEInit, TEDispose, TextBox, TESetText, TECalText, TESetSelect, TENew, TEUpdate, TEClick, TECopy, TECut,... |
| **`TEXTEDIT_CONT`** | `0x015C28` | `0x010264` | `desk_mgr.s:71`<br>`desk_mgr.s:77` | TEXTEDIT_CONT - mouseUp / keyDown / keyUp / autoKey path: dispatch event to front window if it is a desk accessory and the DA's event mask covers this event code. |
| **`TEXTEDIT_CONT_2`** | `0x015C40` | `0x01027C` | `desk_mgr.s:89`<br>`desk_mgr.s:94` | TEXTEDIT_CONT_2 Called during boot (3,697 times in 30s trace). |
| **`TEXTEDIT_CONT_3`** | `0x015C5C` | `0x010298` | `desk_mgr.s:114`<br>`desk_mgr.s:117` | TEXTEDIT_CONT_3 -- send accEvent control call to DA. TEXTEDIT_CONT_3 |
| **`TEXTEDIT_CONT_4`** | `0x015C5E` | `0x01029A` | `desk_mgr.s:117`<br>`desk_mgr.s:120` | TEXTEDIT_CONT_4 -- send accCursor to front DA. |
| **`TEXTEDIT_CONT_5`** | `0x015C78` | `0x0102B4` | `desk_mgr.s:133`<br>`desk_mgr.s:135` | TEXTEDIT_CONT_5 -- send accRun to this DA. TEXTEDIT_CONT_5 |
| **`TEXTEDIT_CONT_6`** | `0x015C7C` | `0x0102B8` | `desk_mgr.s:142`<br>`desk_mgr.s:142` | TEXTEDIT_CONT_6 Called during boot. |
| **`TEXTEDIT_CONT_7`** | `0x015C88` | `0x0102D8` | `desk_mgr.s:153`<br>`desk_mgr.s:165` | TEXTEDIT_CONT_7 |
| **`TEXTEDIT_ERR`** | `0x015C58` | `0x010294` | `desk_mgr.s:105`<br>`desk_mgr.s:109` | TEXTEDIT_ERR Called during boot (3,697 times in 30s trace). |
| **`TGEVT_BEGIN`** | `0x011064` | `0x00B630` | `toolbox_event.s:259`<br>`toolbox_event.s:234` | — |
| **`TGEVT_CALL_SYSEVENT`** | — | `0x00B6EA` | `toolbox_event.s:324` | — |
| **`TGEVT_CHK_FKEY`** | `0x0110CE` | — | `toolbox_event.s:317` | Checks for keyDown/autoKey with Cmd+Shift held and digit key 0-9. evtMeta byte: bit 0=shiftKey, bit 1=alphaLock, bit 3=cmdKey. Test (evtMeta & 0x0B) == 0x03: cmdKey + shiftKey both set. |
| **`TGEVT_CHK_UPDATE`** | `0x0110A0` | `0x00B66C` | `toolbox_event.s:290`<br>`toolbox_event.s:262` | — |
| **`TGEVT_CLEANUP`** | `0x01112C` | `0x00B71A` | `toolbox_event.s:363`<br>`toolbox_event.s:342` | — |
| **`TGEVT_CLEAR_RESULT`** | — | `0x00B6FA` | `toolbox_event.s:332` | — |
| **`TGEVT_CLR_RESULT`** | `0x011128` | — | `toolbox_event.s:360` | — |
| **`TGEVT_GET_OS`** | `0x01108C` | `0x00B658` | `toolbox_event.s:278`<br>`toolbox_event.s:251` | — |
| **`TGEVT_JOURNAL`** | `0x01108E` | `0x00B65A` | `toolbox_event.s:280`<br>`toolbox_event.s:253` | — |
| **`TGEVT_POLL_OS`** | `0x01107E` | `0x00B64A` | `toolbox_event.s:270`<br>`toolbox_event.s:244` | — |
| **`TGEVT_RETURN`** | `0x011136` | `0x00B724` | `toolbox_event.s:368`<br>`toolbox_event.s:347` | — |
| **`TGEVT_RUN_FKEY`** | `0x011110` | `0x00B6D4` | `toolbox_event.s:347`<br>`toolbox_event.s:309` | — |
| **`TGEVT_SCSI_POLL_CHECK`** | — | `0x00B6FE` | `toolbox_event.s:334` | — |
| **`TGEVT_SWALLOW`** | `0x011126` | `0x00B6E6` | `toolbox_event.s:358`<br>`toolbox_event.s:321` | Called by: TGEVT_SYSEVT, GNE_FKEY_CALL, TGEVT_RUN_FKEY |
| **`TGEVT_SYSEVT`** | `0x0110B4` | `0x00B680` | `toolbox_event.s:301`<br>`toolbox_event.s:273` | Intercepts events destined for desk accessories and handles Cmd-Shift-number key combos (FKEY resources). |
| **`TickCount`** | `0x010F5E` | `0x00B52A` | `toolbox_event.s:64` | **Proto:** `Pascal: FUNCTION TickCount: LONGINT`<br>_TickCount ($A975) Pascal: FUNCTION TickCount: LONGINT Returns the number of ticks (1/60 sec) since system startup. Called during boot. |
| **`TICKCOUNT`** | `0x010F5E` | `0x00B52A` | `toolbox_event.s:61` | **Proto:** `Pascal: FUNCTION TickCount: LONGINT`<br>_TickCount ($A975) Pascal: FUNCTION TickCount: LONGINT Returns the number of ticks (1/60 sec) since system startup. |
| **`TrackBox`** | `0x011B86` | `0x00C220` | `window_mgr.s:1642` | **Proto:** `Pascal: FUNCTION TrackBox(theWindow: WindowPtr; thePt: Point;`<br>(falls through) _TrackBox ($A83B): track the mouse in a window's zoom box (or go-away box) Pascal: FUNCTION TrackBox(theWindow: WindowPtr; thePt: Point; partCode: INTEGER): BOOLEAN; Entry (after LINK)... |
| **`TRACKBOX`** | `0x011B86` | `0x00C220` | `window_mgr.s:1531` | TRACKBOX (= AddComp) - generic WDEF part tracking loop (go-away, zoom) Shared by TrackGoAway and TrackBox. Tracks mouse, toggling the part highlight while mouse is inside, returns result. |
| **`TRACKBOX_CONT`** | `0x011BEA` | `0x00C284` | `window_mgr.s:1692`<br>`window_mgr.s:1578` | TRACKBOX_CONT - toggle the tracked part's highlight: wDraw, param = D6 (WDEF hit code). Apple source name: EORSymbol (System 7.1 WindowMgr.a) Called during boot. |
| **`TRACKBOX_NO`** | `0x011BDC` | — | `window_mgr.s:1680` | mouse released |
| **`TRACKBOX_OK`** | `0x011BA8` | `0x00C242` | `window_mgr.s:1655`<br>`window_mgr.s:1544` | tracking loop: send wHit to WDEF, toggle highlight as needed |
| **`TRACKBOX_OK_2`** | `0x011BB8` | `0x00C252` | `window_mgr.s:1662`<br>`window_mgr.s:1551` | — |
| **`TRACKBOX_RESTORE`** | — | `0x00C276` | `window_mgr.s:1569` | mouse released |
| **`TRACKBOX_SKIP`** | `0x011BC0` | `0x00C25A` | `window_mgr.s:1667`<br>`window_mgr.s:1556` | — |
| **`TrackControl`** | `0x013160` | `0x00D764` | `control_mgr.s:654` | _TrackControl ($A968) Called during boot. |
| **`TRACKCONTROL`** | `0x013160` | `0x00D764` | `control_mgr.s:576` | **Proto:** `Pascal: function TrackControl(theControl: ControlHandle; startPt: Point;`<br>_TrackControl ($A968): track mouse in a control until button is released. Pascal: function TrackControl(theControl: ControlHandle; startPt: Point; actionProc: ProcPtr): INTEGER; Returns the part code ... |
| **`TRACKCONTROL_EMPTY`** | `0x0131CA` | `0x00D7CE` | `control_mgr.s:710`<br>`control_mgr.s:625` | — |
| **`TRACKCONTROL_EXIT`** | `0x0131DE` | `0x00D7E2` | `control_mgr.s:720`<br>`control_mgr.s:637` | Common exit: D3 holds the part code returned to caller. Called by: FINDCONTROL, TRACKCONTROL_OK_2, TRACKCONTROL_NO_4, FINDCONTROL_SKIP |
| **`TRACKCONTROL_LOOP`** | `0x013176` | `0x00D77A` | `control_mgr.s:662`<br>`control_mgr.s:584` | TRACKCONTROL_LOOP: mouse tracking loop |
| **`TRACKCONTROL_NO`** | `0x01318E` | `0x00D792` | `control_mgr.s:680`<br>`control_mgr.s:598` | TRACKCONTROL_NO: subsequent iterations - check if mouse still in same part Called during boot. |
| **`TRACKCONTROL_NO_2`** | `0x013194` | `0x00D798` | `control_mgr.s:684`<br>`control_mgr.s:603` | Hilite the part (or unhilite via 0), then run action proc / auto-track. |
| **`TRACKCONTROL_NO_3`** | `0x0131C0` | `0x00D7C4` | `control_mgr.s:705`<br>`control_mgr.s:620` | TRACKCONTROL_NO_3: call user's actionProc callback |
| **`TRACKCONTROL_NO_4`** | `0x013248` | `0x00D84C` | `control_mgr.s:769`<br>`control_mgr.s:685` | TRACKCONTROL_NO_4: thumb drag cancelled -- return part code 0 |
| **`TRACKCONTROL_OK`** | `0x0131EE` | `0x00D7F2` | `control_mgr.s:733`<br>`control_mgr.s:649` | TRACKCONTROL_OK TRACKCONTROL_OK: indicator/thumb tracking -- drag the thumb |
| **`TRACKCONTROL_OK_2`** | `0x013220` | `0x00D824` | `control_mgr.s:750`<br>`control_mgr.s:666` | — |
| **`TrackGoAway`** | `0x011B7E` | `0x00C218` | `window_mgr.s:1626` | **Proto:** `Pascal: FUNCTION TrackGoAway(theWindow: WindowPtr; thePt: Point): BOOLEAN;`<br>_TrackGoAway ($A91E): track the mouse in a window's go-away box Pascal: FUNCTION TrackGoAway(theWindow: WindowPtr; thePt: Point): BOOLEAN; Inserts partCode = inGoAway (6) below the return address and ... |
| **`TRACKGOAWAY`** | `0x011B7E` | `0x00C218` | `window_mgr.s:1523` | **Proto:** `Pascal: function TrackGoAway(theWindow: WindowPtr; thePt: Point): BOOLEAN;`<br>_TrackGoAway ($A91E): track mouse in go-away box Pascal: function TrackGoAway(theWindow: WindowPtr; thePt: Point): BOOLEAN; Returns true if mouse released inside go-away box. Falls through to TRACKBOX... |
| **`Trap1_16D`** | `0x012ECC` | — | `control_mgr.s:223` | **Proto:** `Pascal: PROCEDURE Draw1Control(theControl: ControlHandle);`<br>**Regs:** `Entry: 0x4(SP) = theControl. Saves A3 and joins ShowControl at`<br>_Draw1Control ($A96D): draw one control if it is visible Pascal: PROCEDURE Draw1Control(theControl: ControlHandle); Apple source name: DrawOneControl (System 7.1 ControlMgr.a; MacSEROM.lst DRAWONECONT... |
| **`Trap1_1AC`** | `0x01451E` | — | `resource_mgr.s:3022` | **Proto:** `PROCEDURE AddReference(theResource: Handle; theID: INTEGER; name: Str255)`<br>_AddReference ($A9AC): obsolete trap, kept as a stub that always fails PROCEDURE AddReference(theResource: Handle; theID: INTEGER; name: Str255) (signature as given in System 7.1 ResourceMgr.a) Pops i... |
| **`Trap1_1AE`** | `0x01452E` | — | `resource_mgr.s:3039` | **Proto:** `PROCEDURE RmveReference(theResource: Handle)`<br>_RmveReference ($A9AE): obsolete trap, kept as a stub that always fails PROCEDURE RmveReference(theResource: Handle) (signature as given in System 7.1 ResourceMgr.a) Pops the 4-byte handle parameter a... |
| **`Trap1_1C5`** | `0x01489A` | — | `resource_mgr.s:3539` | **Proto:** `Pascal: FUNCTION RsrcMapEntry(theResource: Handle): LONGINT;`<br>**Regs:** `Entry: 4(SP).L = theResource, 8(SP).L = space for the function result Exit:  function result = offset of the reference entry from the start`<br>_RsrcMapEntry ($A9C5): offset of a resource's reference entry in its map Pascal: FUNCTION RsrcMapEntry(theResource: Handle): LONGINT; Entry: 4(SP).L = theResource, 8(SP).L = space for the function res... |
| **`UNIQID_CHECK`** | `0x013DCC` | `0x00E3D6` | `resource_mgr.s:1649`<br>`resource_mgr.s:1540` | — |
| **`UNIQID_NEXTMAP`** | `0x013DDC` | `0x00E3E6` | `resource_mgr.s:1655`<br>`resource_mgr.s:1546` | — |
| **`UNIQID_RETRY`** | `0x013DB8` | `0x00E3C2` | `resource_mgr.s:1641`<br>`resource_mgr.s:1532` | — |
| **`Unique1ID`** | `0x013DAC` | `0x00E3B6` | `resource_mgr.s:1635` | **Proto:** `Pascal: FUNCTION Unique1ID(theType: ResType): INTEGER;`<br>**Regs:** `Entry: 4(SP).L = theType, 8(SP).W = space for the function result Exit:  function result = unused ID in 0..32767; 4 bytes popped`<br>_Unique1ID ($A810): return a resource ID that is not in use for a given type in the current resource file (Mac Plus addition, Inside Macintosh IV) Pascal: FUNCTION Unique1ID(theType: ResType): INTEGER... |
| **`UNIQUE1ID`** | `0x013DAC` | `0x00E3B6` | `resource_mgr.s:1527` | _Unique1ID ($A810), _UniqueID ($A9C1) -- generate unique resource ID. Picks a random ID in 0..0x7FFF that is not already used by any resource of the given type. _Unique1ID restricts to current map. St... |
| **`UniqueID`** | `0x013DB0` | `0x00E3BA` | `resource_mgr.s:1638` | **Proto:** `UniqueID -- _UniqueID ($A9C1): FUNCTION UniqueID (theType: ResType): Integer;`<br>UniqueID -- _UniqueID ($A9C1): FUNCTION UniqueID (theType: ResType): Integer; |
| **`UNIQUEID`** | `0x013DB0` | `0x00E3BA` | `resource_mgr.s:1529` | — |
| **`UnloadScrap`** | `0x016E26` | `0x012670` | `scrap_mgr.s:110` | **Proto:** `_UnloadScrap ($A9FA) - FUNCTION UnloadScrap: LongInt`<br>Clipboard File does not exist - create it _UnloadScrap ($A9FA) - FUNCTION UnloadScrap: LongInt Writes the in-memory scrap to the Clipboard File on disk, then disposes the memory handle. If scrap is al... |
| **`UNLOADSCRAP`** | `0x016E26` | `0x012670` | `scrap_mgr.s:96` | — |
| **`UpdateResFIle`** | `0x013910` | `0x00DEFC` | `resource_mgr.s:897` | _UpdateResFile ($A999); the label is MacPlusROM.lst's spelling UpdateResFIle Called during boot. |
| **`UPDATERESFILE`** | `0x013910` | `0x00DEFC` | `resource_mgr.s:851` | _UpdateResFile ($A999) -- write changed resources back to file. Two paths: if mapCompact is clear, write only changed resources in file order. If mapCompact is set, do full compaction (write all resou... |
| **`UPDRES_ADJ_LOOP`** | `0x01396A` | `0x00DF56` | `resource_mgr.s:944`<br>`resource_mgr.s:883` | UPDRES_ADJ_LOOP: shift every ref entry's data offset by D7. |
| **`UPDRES_CHECK_CHG`** | `0x013924` | `0x00DF10` | `resource_mgr.s:912`<br>`resource_mgr.s:857` | UPDRES_CHECK_CHG - UpdateResFile: check mapChanged and write resources Tests the mapChanged flag; if not set, nothing to update. Two paths: if mapCompact is clear, write only changed resources in file... |
| **`UPDRES_CMP_START`** | `0x01397E` | — | `resource_mgr.s:950` | — |
| **`UPDRES_COMPACT`** | `0x013954` | — | `resource_mgr.s:936` | UPDRES_COMPACT - UpdateResFile compaction path Compacts the resource fork by rewriting all resources in file order. First adjusts data offsets if the map has moved, then enters the CmpFrm compaction l... |
| **`UPDRES_DONE_CHANGED`** | — | `0x00DF3C` | `resource_mgr.s:871` | — |
| **`UPDRES_FULL_COMPACT`** | — | `0x00DF40` | `resource_mgr.s:874` | Full-compaction path: rewrite every resource sequentially. |
| **`UPDRES_WRITE_CHANGED_LOOP`** | — | `0x00DF32` | `resource_mgr.s:867` | — |
| **`UPDRES_WRITE_LOOP`** | `0x013946` | — | `resource_mgr.s:922` | — |
| **`UPDRES_WRITE_MAP`** | `0x013950` | — | `resource_mgr.s:926` | — |
| **`UpdtControls`** | `0x01324E` | `0x00D852` | `control_mgr.s:784` | **Proto:** `Pascal: PROCEDURE UpdtControls(theWindow: WindowPtr; updateRgn: RgnHandle);`<br>_UpdtControl ($A953): draw the controls of a window that are in a region Pascal: PROCEDURE UpdtControls(theWindow: WindowPtr; updateRgn: RgnHandle); (the MPW interfaces spell it UpdtControl, like the ... |
| **`UPDTCONTROLS`** | `0x01324E` | `0x00D852` | `control_mgr.s:693` | **Proto:** `Pascal: procedure UpdtControl(theWindow: WindowPtr; updateRgn: RgnHandle);`<br>_UpdtControl ($A953): redraw all controls within an updateRgn. Pascal: procedure UpdtControl(theWindow: WindowPtr; updateRgn: RgnHandle); Stack: 8(A6) = updateRgn (long), 0xC(A6) = theWindow (long) |
| **`UpdtDialog`** | `0x014C80` | `0x00F2A2` | `dialog_mgr.s:558` | UpdtDialog -- trap handler for _UpdtDialog ($A978). _UpdtDialog ($A978) |
| **`UPDTDIALOG`** | `0x014C80` | `0x00F2A2` | `dialog_mgr.s:563` | _UpdtDialog ($A978) -- redraw dialog items in update region. Stack: theDialog(L), updateRgn(L). Calls _UpdtControl + iterates items with operation 3 (update only items in updateRgn). |
| **`UseResFile`** | `0x01382E` | `0x00DE30` | `resource_mgr.s:725` | _UseResFile ($A998) Sets the current resource file to the specified refnum. Called during boot. |
| **`USERESFILE`** | `0x01382E` | `0x00DE30` | `resource_mgr.s:720` | _UseResFile ($A998) -- set current resource file by refnum. |
| **`ValidRect`** | `0x011FF0` | `0x00C6A6` | `window_mgr.s:2339` | _ValidRect ($A92A) stack: rect -> (removes from update region) _ValidRect ($A92A): remove a rect from current window's updateRgn Called during boot. |
| **`VALIDRECT`** | `0x011FF0` | `0x00C6A6` | `window_mgr.s:2191` | _ValidRect ($A92A): subtract a rect from current window's updateRgn |
| **`ValidRgn`** | `0x011FEC` | `0x00C6A2` | `window_mgr.s:2328` | _ValidRgn ($A929): remove a region from current window's updateRgn |
| **`VALIDRGN`** | `0x011FEC` | `0x00C6A2` | `window_mgr.s:2184` | _ValidRgn ($A929): subtract a region from current window's updateRgn |
| **`VCHAR2PIXEL`** | — | `0x0111F0` | `textedit.s:1474` | VCHAR2PIXEL - default char-to-pixel converter. In: D0 = char count, D1 = start offset, A0 = text ptr. Out: D1 = pixel width, via _TextWidth trap. |
| **`VCHECKLOAD`** | — | `0x00E746` | `resource_mgr.s:2191` | — |
| **`VCMPFRM`** | — | `0x00DFE6` | `resource_mgr.s:953` | VCMPFRM (CmpFrm) -- compaction frame: copy resources to close gaps. For each resource in file order, either copies from memory (changed) or from disk (unchanged) into the compaction buffer, then flush... |
| **`VNEWMAP`** | — | `0x00DC18` | `resource_mgr.s:454` | VNEWMAP -- create a new in-memory resource map for an open file. Allocates a 36-byte map header, opens the resource fork, reads the map header from disk, expands the handle to fit the entire map, then... |
| **`VNEWMAP_ERR_CLOSE`** | — | `0x00DCD6` | `resource_mgr.s:524` | Error tail: close file, dispose header, clear scratch. Called by: NEWMAP_CONT, NEWMAP_SKIP |
| **`VPIXEL2CHAR`** | — | `0x010C44` | `textedit.s:719` | VPIXEL2CHAR - default pixel-to-char converter for variable- width fonts. Measures all char widths on the run via _MeasureText, then locates which char's rect contains the target pixel. In: D0 = char c... |
| **`VPIXEL2CHAR_EXIT`** | — | `0x010CCA` | `textedit.s:788` | — |
| **`VSUPERLOAD`** | — | `0x00DAD6` | `resource_mgr.s:272` | VSUPERLOAD: bulk-load all preload-flagged resources from one map. Walks the type list, allocating handles or pointers (sysHeap if attr bit 6 set) for each entry that the resource map says to preload a... |
| **`WaitMouseUp`** | `0x010FDE` | `0x00B5AA` | `toolbox_event.s:163` | **Proto:** `Pascal: FUNCTION WaitMouseUp: BOOLEAN`<br>_WaitMouseUp ($A977) Pascal: FUNCTION WaitMouseUp: BOOLEAN Returns TRUE if button is still held. If button was released, consumes the pending mouseUp event (mask 0x4 = bit 2 = mouseUp) via GetNextEven... |
| **`WAITMOUSEUP`** | `0x010FDE` | `0x00B5AA` | `toolbox_event.s:148` | **Proto:** `Pascal: FUNCTION WaitMouseUp: BOOLEAN`<br>_WaitMouseUp ($A977) Pascal: FUNCTION WaitMouseUp: BOOLEAN Returns TRUE if button still held. If button was released, consumes the pending mouseUp event (mask 0x4) via GetNextEvent. |
| **`WAITMUP_DONE`** | `0x010FF8` | `0x00B5C4` | `toolbox_event.s:173`<br>`toolbox_event.s:158` | — |
| **`WidthTab_DerefPrimary`** | — | `0x019218` | `font_mgr.s:128` | WidthTab_DerefPrimary -- A0 := *(WidthTabHandle) Returns the dereferenced WidthTabHandle (the primary widthTab pointer) in A0. Used by all routines that need to read or modify the primary cached width... |
| **`WidthTab_InvalidateAll`** | — | `0x019206` | `font_mgr.s:112` | WidthTab_InvalidateAll -- invalidate the primary cached widthTab Stamps -1 into LastSPExtra and font-id slots of the WidthTabHandle widthTab (the one returned by WidthTab_DerefPrimary), and clears Cur... |
| **`WMGR`** | — | `0x00B7E6` | `window_mgr.s:48` | Window Manager Apple source: WindowMgr.a (MacSEROM.lst module WMGR). It starts with NewString/SetString ($A906/$A907, string handles, used for window titles) and the window-list primitives FIND_PREV_W... |
| **`WMGR_RTS`** | — | `0x00B7F2` | `window_mgr.s:54` | — |
| **`WMGR_STRIP_10_RTS`** | — | `0x00C194` | `window_mgr.s:1446` | WMGR_STRIP_10_RTS - strip 10 bytes of params and return. |
| **`WMGREND`** | — | `0x00C94A` | `window_mgr.s:2581` | — |
| **`WMGRGRAY`** | — | `0x00C502` | `window_mgr.s:1924` | Window Manager gray pattern (50% checkerboard, same as QD gray): #.#.#.#. 0xAA Used for window drag outlines .#.#.#.# 0x55 and desktop background pattern |
| **`WriteResource`** | `0x014482` | `0x00EAA4` | `resource_mgr.s:2886` | _WriteResource ($A9B0) |
| **`WRITERESOURCE`** | `0x014482` | `0x00EAA4` | `resource_mgr.s:2766` | _WriteResource ($A9B0) -- write a changed resource to disk. Writes the in-memory data of a resource back to its file. Only acts if file is writable AND resChanged is set. Otherwise no-op. |
| **`WRITERESOURCE_CONT`** | `0x01449A` | `0x00EABC` | `resource_mgr.s:2905`<br>`resource_mgr.s:2776` | WRITERESOURCE_CONT - entry for SizeRsrc, MaxSizeRsrc and RsrcMapEntry Presets their LONGINT function result to -1 (0xC(SP): above this BSR's return address, the trap return address and the handle para... |
| **`WRITERESOURCE_CONT_2`** | `0x0144A0` | `0x00EAC2` | `resource_mgr.s:2913`<br>`resource_mgr.s:2780` | WRITERESOURCE_CONT_2 -- prologue + find the ref entry of the handle parameter (A1 = handle, A2 = ref entry, A4 = map handle). If it is not a resource (ResErr = resNotFound), drops the caller's return ... |
| **`WRITERESOURCE_EXIT`** | `0x0144BA` | `0x00EADC` | `resource_mgr.s:2931`<br>`resource_mgr.s:2797` | WRITERESOURCE_EXIT - handle found, return to caller's operation body Called during boot. |
| **`WRITERESOURCE_SKIP`** | `0x014496` | — | `resource_mgr.s:2893` | — |
| **`WRITERESOURCE_SKIP_2`** | `0x0144B4` | `0x00EAD6` | `resource_mgr.s:2922`<br>`resource_mgr.s:2789` | — |
| **`X2Fix`** | `0x015B4A` | `0x010186` | `fixmath.s:811` | **Proto:** `Pascal: FUNCTION X2Fix(x: Extended): Fixed;`<br>**Regs:** `Entry: 4(SP) = address of x (10 bytes), 8(SP) = result slot Exit:  result = x rounded to Fixed (the magnitude is rounded up when the`<br>_X2Fix ($A844): convert 80-bit SANE extended to Fixed (16.16) Pascal: FUNCTION X2Fix(x: Extended): Fixed; Entry: 4(SP) = address of x (10 bytes), 8(SP) = result slot (no frame; uses D0-D1/A0-A1) Exit:... |
| **`X2FIX`** | `0x015B4A` | `0x010186` | `fixmath.s:612` | _X2Fix ($A844) - convert 80-bit SANE extended to Fixed (16.16) Clamps to $80000000 / $7FFFFFFF on overflow. |
| **`X2FIX_CHK_ROUND`** | `0x015B7E` | `0x0101BA` | `fixmath.s:845`<br>`fixmath.s:640` | — |
| **`X2FIX_CHK_SIGN`** | `0x015B8A` | `0x0101C6` | `fixmath.s:859`<br>`fixmath.s:652` | — |
| **`X2FIX_CLAMP`** | `0x015B9E` | `0x0101DA` | `fixmath.s:880`<br>`fixmath.s:670` | — |
| **`X2FIX_CONVERT`** | `0x015B54` | `0x010190` | `fixmath.s:823`<br>`fixmath.s:620` | — |
| **`X2FIX_DO_SHIFT`** | `0x015B82` | `0x0101BE` | `fixmath.s:853`<br>`fixmath.s:646` | X2FIX_DO_SHIFT - right-shift mantissa by D1 (1..31) bits |
| **`X2FIX_NEGATE`** | `0x015B98` | `0x0101D4` | `fixmath.s:874`<br>`fixmath.s:664` | — |
| **`X2FIX_OVERFLOW`** | `0x015B9C` | `0x0101D8` | `fixmath.s:878`<br>`fixmath.s:668` | fall through to overflow handler |
| **`X2FIX_POS_CLAMP`** | `0x015BA4` | `0x0101E0` | `fixmath.s:889`<br>`fixmath.s:675` | X2FIX_POS_CLAMP - positive overflow: clamp to $7FFFFFFF |
| **`X2FIX_ROTATE`** | `0x015BA8` | `0x0101E4` | `fixmath.s:892`<br>`fixmath.s:678` | — |
| **`X2FIX_ROUND_UP`** | `0x015B86` | `0x0101C2` | `fixmath.s:856`<br>`fixmath.s:649` | — |
| **`X2FIX_SHIFT`** | `0x015B70` | `0x0101AC` | `fixmath.s:839`<br>`fixmath.s:634` | X2FIX_SHIFT - mantissa needs right-shifting by D1 bits |
| **`X2FIX_STORE`** | `0x015B92` | `0x0101CE` | `fixmath.s:864`<br>`fixmath.s:658` | Called by: FIX2LONG_POS, X2FIX_NEGATE, X2FIX_ROTATE, FIX2LONG_NEG_RND, LONG2FIX_SHIFT |
| **`X2FIX_UNDERFLOW`** | `0x015B96` | `0x0101D2` | `fixmath.s:872`<br>`fixmath.s:662` | X2FIX_UNDERFLOW - shift > 32: result underflows to 0 |
| **`X2Frac`** | `0x015B50` | `0x01018C` | `fixmath.s:821` | **Proto:** `Pascal: FUNCTION X2Frac(x: Extended): Fract;`<br>_X2Frac ($A846): convert 80-bit SANE extended to Fract (2.30) Pascal: FUNCTION X2Frac(x: Extended): Fract; As X2Fix, with D1 = $4000; X2FIX_CONVERT (Apple: X2F) is shared. |
| **`X2FRAC`** | `0x015B50` | `0x01018C` | `fixmath.s:618` | _X2Frac ($A846) - convert 80-bit SANE extended to Fract (2.30) |
| **`XFINDLINE`** | — | `0x01172C` | `textedit.s:2212` | XFINDLINE - default line-break finder. In: D6 = char offset to start scanning from. Out: D0 = char offset where line breaks. Iterates: at each position, calls TEFindWord (D2=$C: word- start mode) to a... |
| **`XFINDLINE_FORCE_BREAK`** | — | `0x01179C` | `textedit.s:2259` | — |
| **`XFINDLINE_NEXT_WORD`** | — | `0x01177A` | `textedit.s:2243` | — |
| **`XFINDLINE_SKIP_SPACE`** | — | `0x01178A` | `textedit.s:2252` | — |
| **`XFINDWORD`** | — | `0x011644` | `textedit.s:2062` | XFINDWORD - default TEFindWord implementation. In: D0 = char offset, D2 high word = flags. Out: D0,D1 = word start/end offsets. Scans backward from D0 to find word start, then forward from D0 to find ... |
| **`XMunger`** | `0x0155B6` | `0x00FBE4` | `toolbox_utils.s:66` | **Regs:** `Entry: after LINK, logical = $24(A6), slop = $20(A6), h = $1C(A6) ... Exit:  result as for Munger; 32 bytes of parameters removed`<br>_XMunger ($A819): Munger with a caller-supplied logical length and slop Parameters (Pascal order): logical, slop: LONGINT, then h, offset, ptr1, len1, ptr2, len2 as for Munger; LONGINT result. Entry: ... |
| **`XMUNGER`** | `0x0155B6` | `0x00FBE4` | `toolbox_utils.s:52` | GetForeColor / Munger variant with explicit offset and size. Extended stack frame with extra params at +$24 and +$20. Used when caller provides both search offset and handle size. (XMUNGER in SE FDHD ... |
| **`XMUNGER_CONT`** | `0x0155DE` | `0x00FC0C` | `toolbox_utils.s:94`<br>`toolbox_utils.s:73` | **Regs:** `Entry: A2 = handle, D5 = logical data length, -8(A6) = physical size, Exit:  D2 = result offset (-1 = not found)`<br>XMUNGER_CONT - Munger/XMunger core. Entry: A2 = handle, D5 = logical data length, -8(A6) = physical size, -4(A6) = slop, Munger parameters at $08..$18(A6) Loads D2 = offset, A3 = ptr1, A4 = ptr2, D3 =... |
| **`XMUNGER_CONT_2`** | `0x0155F4` | `0x00FC22` | `toolbox_utils.s:101`<br>`toolbox_utils.s:80` | — |
| **`XMUNGER_CONT_3`** | `0x015632` | `0x00FC60` | `toolbox_utils.s:153`<br>`toolbox_utils.s:126` | **Regs:** `Exit: D0 = 0 (noErr).`<br>XMUNGER_CONT_3 - Move D0 bytes from A0 to A1 (overlap-safe _BlockMove); moves of 0 or 1 byte, or with A0 = A1, are done without the trap. Exit: D0 = 0 (noErr). Apple source name: bm (System 7.1 Toolbo... |
| **`XMUNGER_CONT_4`** | `0x015640` | `0x00FC6E` | `toolbox_utils.s:165`<br>`toolbox_utils.s:137` | XMUNGER_CONT_4 - Handle 0 or 1 byte move without BlockMove. |
| **`XMUNGER_CONT_5`** | `0x01565E` | `0x00FC8C` | `toolbox_utils.s:196`<br>`toolbox_utils.s:162` | XMUNGER_CONT_5 - Resize the handle to the new size plus the slop. |
| **`XMUNGER_CONT_6`** | `0x015668` | `0x00FC96` | `toolbox_utils.s:210`<br>`toolbox_utils.s:172` | XMUNGER_CONT_6 - target found at offset D2: ptr2 (A4) = nil just returns the match offset. XMUNGER_EMPTY (also entered directly when ptr1 = nil): len2 = 0 deletes the len1 bytes at D2 and shrinks the ... |
| **`XMUNGER_CONT_7`** | `0x0156AA` | `0x00FCD8` | `toolbox_utils.s:252`<br>`toolbox_utils.s:211` | — |
| **`XMUNGER_CONT_8`** | `0x0156C4` | `0x00FCF2` | `toolbox_utils.s:275`<br>`toolbox_utils.s:231` | — |
| **`XMUNGER_CONT_9`** | `0x0156D8` | `0x00FD06` | `toolbox_utils.s:292`<br>`toolbox_utils.s:246` | XMUNGER_CONT_9 - Shift trailing data within handle to open/close gap. Moves bytes from (base+offset+searchLen) to (base+offset+replaceLen), covering all trailing data. Apple source name: MoveTail (Sys... |
| **`XMUNGER_EMPTY`** | `0x01566C` | `0x00FC9A` | `toolbox_utils.s:213`<br>`toolbox_utils.s:175` | — |
| **`XMUNGER_EMPTY_2`** | `0x0156BA` | `0x00FCE8` | `toolbox_utils.s:269`<br>`toolbox_utils.s:225` | XMUNGER_EMPTY_2 - Replace the len1 (D3) bytes at D2 with (ptr2,len2). D1 = len2 - len1. Equal: copy in place. Shrinking: move the tail down first, then resize. Growing: resize first, then move the tai... |
| **`XMUNGER_EXIT`** | `0x015644` | `0x00FC72` | `toolbox_utils.s:168`<br>`toolbox_utils.s:140` | — |
| **`XMUNGER_EXIT_2`** | `0x01568A` | `0x00FCB8` | `toolbox_utils.s:228`<br>`toolbox_utils.s:190` | — |
| **`XMUNGER_LOOP`** | `0x015618` | `0x00FC46` | `toolbox_utils.s:122`<br>`toolbox_utils.s:101` | — |
| **`XMUNGER_NEXT`** | `0x01562A` | `0x00FC58` | `toolbox_utils.s:135`<br>`toolbox_utils.s:113` | XMUNGER_NEXT - Advance search position by one byte and retry. |
| **`XMUNGER_NO`** | `0x01565A` | `0x00FC88` | `toolbox_utils.s:189`<br>`toolbox_utils.s:156` | — |
| **`XMUNGER_NO_2`** | `0x01568C` | `0x00FCBA` | `toolbox_utils.s:237`<br>`toolbox_utils.s:196` | XMUNGER_NO_2 - len1 = 0: pure insert of (ptr2,len2) at offset D2. Grows the handle, shifts the tail up, copies the data in (XMUNGER_CONT_7) and returns D2 = offset + len2 (XMUNGER_RTS is the normal re... |
| **`XMUNGER_NOTFOUND`** | `0x01562E` | `0x00FC5C` | `toolbox_utils.s:143`<br>`toolbox_utils.s:119` | XMUNGER_NOTFOUND - target not found (despite the label name): D2 = -1. Also taken when len1 is longer than the data. |
| **`XMUNGER_OK`** | `0x0155F8` | `0x00FC26` | `toolbox_utils.s:104`<br>`toolbox_utils.s:83` | — |
| **`XMUNGER_RETRY`** | `0x015610` | `0x00FC3E` | `toolbox_utils.s:117`<br>`toolbox_utils.s:96` | — |
| **`XMUNGER_RTS`** | `0x0156B8` | `0x00FCE6` | `toolbox_utils.s:259`<br>`toolbox_utils.s:218` | — |
| **`XMUNGER_SETSIZE`** | `0x015648` | — | `toolbox_utils.s:181` | **Regs:** `Entry: A0 = handle, D0 = new logical size; -8(A6) = physical size, Exit: D0 = result code, condition codes set from D0`<br>XMUNGER_SETSIZE - SetHandleSize cover that honours the slop. Entry: A0 = handle, D0 = new logical size; -8(A6) = physical size, -4(A6) = slop Same size, or shrinking by no more than the slop: no call,... |
| **`XTrimMeasure`** | `0x0165FA` | `0x011158` | `textedit.s:827` | X Trim Measure Called during boot. |
| **`XTRIMMEASURE`** | `0x0165FA` | `0x011158` | `textedit.s:1388` | XTRIMMEASURE - default trimmed-line measurer. Pascal-style: function XTrimMeasure(D6=lineStart, D7=lineEnd): D0 (pixels). Trims trailing spaces (chars <= 0x20) before measuring so that justification i... |
| **`XTRIMMEASURE_CHAR2PIXEL`** | — | `0x0111D4` | `textedit.s:1452` | XTRIMMEASURE_CHAR2PIXEL - call P_Char2Pixel for char range D6..D0. Out: D1 = pixel width. |
| **`XTRIMMEASURE_CLAMP_END`** | — | `0x0111B8` | `textedit.s:1433` | — |
| **`XTRIMMEASURE_CONT`** | `0x01661E` | `0x01117C` | `textedit.s:844`<br>`textedit.s:1408` | XTRIMMEASURE_CONT -- measure width from lineStart to D3. |
| **`XTRIMMEASURE_CONT_10`** | `0x0166FE` | — | `textedit.s:1004` | XTRIMMEASURE_CONT_10 Called during boot. |
| **`XTRIMMEASURE_CONT_11`** | `0x016702` | — | `textedit.s:1012` | XTRIMMEASURE_CONT_11 |
| **`XTRIMMEASURE_CONT_12`** | `0x016706` | — | `textedit.s:1021` | XTRIMMEASURE_CONT_12 Called during boot (2,775 times in 30s trace). |
| **`XTRIMMEASURE_CONT_13`** | `0x016708` | — | `textedit.s:1023` | — |
| **`XTRIMMEASURE_CONT_14`** | `0x016778` | `0x0113FC` | `textedit.s:1070`<br>`textedit.s:1735` | XTRIMMEASURE_CONT_14 -- clamp selection to text length. |
| **`XTRIMMEASURE_CONT_15`** | `0x01679E` | `0x011436` | `textedit.s:1091`<br>`textedit.s:1772` | XTRIMMEASURE_CONT_15 Called during boot (2,779 times in 30s trace). |
| **`XTRIMMEASURE_CONT_2`** | `0x016642` | — | `textedit.s:874` | XTRIMMEASURE_CONT_2 Called during boot. |
| **`XTRIMMEASURE_CONT_3`** | `0x01668E` | `0x0112A8` | `textedit.s:908`<br>`textedit.s:1571` | XTRIMMEASURE_CONT_3 Called during boot. |
| **`XTRIMMEASURE_CONT_4`** | `0x016692` | `0x0112AC` | `textedit.s:911`<br>`textedit.s:1573` | XTRIMMEASURE_CONT_4 -- clip to visible lines in update rect. |
| **`XTRIMMEASURE_CONT_5`** | `0x0166D6` | `0x0112F2` | `textedit.s:945`<br>`textedit.s:1603` | XTRIMMEASURE_CONT_5 |
| **`XTRIMMEASURE_CONT_6`** | `0x0166DA` | — | `textedit.s:954` | XTRIMMEASURE_CONT_6 Called during boot. |
| **`XTRIMMEASURE_CONT_7`** | `0x0166E8` | `0x011344` | `textedit.s:966`<br>`textedit.s:1655` | XTRIMMEASURE_CONT_7 Called during boot. |
| **`XTRIMMEASURE_CONT_8`** | `0x0166F6` | — | `textedit.s:986` | XTRIMMEASURE_CONT_8 Called during boot. |
| **`XTRIMMEASURE_CONT_9`** | `0x0166FA` | — | `textedit.s:995` | XTRIMMEASURE_CONT_9 -- set up TE state (A3, A6 frame). XTRIMMEASURE_CONT_9 |
| **`XTRIMMEASURE_DONE`** | `0x0166D4` | `0x0112F0` | `textedit.s:938`<br>`textedit.s:1601` | — |
| **`XTRIMMEASURE_EMPTY`** | — | `0x0111D0` | `textedit.s:1445` | — |
| **`XTRIMMEASURE_EXIT`** | `0x01663E` | — | `textedit.s:865` | XTRIMMEASURE_EXIT Called during boot. |
| **`XTRIMMEASURE_NO`** | `0x01667E` | — | `textedit.s:895` | — |
| **`XTRIMMEASURE_NO_2`** | `0x01668A` | — | `textedit.s:899` | — |
| **`XTRIMMEASURE_NO_3`** | `0x0166A6` | `0x0112C0` | `textedit.s:920`<br>`textedit.s:1582` | — |
| **`XTRIMMEASURE_NO_4`** | `0x0166CA` | `0x0112E6` | `textedit.s:934`<br>`textedit.s:1597` | — |
| **`XTRIMMEASURE_NO_5`** | `0x0166F2` | `0x01134E` | `textedit.s:977`<br>`textedit.s:1660` | XTRIMMEASURE_NO_5 Called during boot. |
| **`XTRIMMEASURE_OK`** | `0x016604` | `0x01116C` | `textedit.s:832`<br>`textedit.s:1395` | — |
| **`XTRIMMEASURE_OK_2`** | `0x01661C` | `0x01117A` | `textedit.s:841`<br>`textedit.s:1401` | — |
| **`XTRIMMEASURE_OK_3`** | `0x016722` | — | `textedit.s:1039` | XTRIMMEASURE_OK_3 Called during boot (2,779 times in 30s trace). |
| **`XTRIMMEASURE_OK_4`** | `0x016788` | `0x01140C` | `textedit.s:1076`<br>`textedit.s:1741` | — |
| **`XTRIMMEASURE_OK_5`** | `0x016796` | — | `textedit.s:1081` | — |
| **`XTRIMMEASURE_OK_6`** | `0x0167AC` | — | `textedit.s:1098` | — |
| **`XTRIMMEASURE_PLAIN`** | — | `0x01119A` | `textedit.s:1419` | — |
| **`XTRIMMEASURE_RTS`** | — | `0x0111CA` | `textedit.s:1442` | — |
| **`XTRIMMEASURE_RUN_LOOP`** | — | `0x0111AA` | `textedit.s:1426` | — |
| **`XTRIMMEASURE_SKIP`** | `0x0166B0` | — | `textedit.s:924` | — |
| **`ZERO_CHK_STATE`** | `0x016EA2` | `0x0126EC` | `scrap_mgr.s:218`<br>`scrap_mgr.s:179` | — |
| **`ZERO_RESIZE_HDL`** | `0x016EAC` | `0x0126F6` | `scrap_mgr.s:230`<br>`scrap_mgr.s:189` | ScrapState < 0: uninitialized, allocate new handle ZERO_RESIZE_HDL - resize existing scrap handle to 0 bytes |
| **`ZERO_STORE_HDL`** | `0x016EB0` | `0x0126FA` | `scrap_mgr.s:233`<br>`scrap_mgr.s:192` | — |
| **`ZERO_TRUNCATE`** | `0x016EB6` | `0x012700` | `scrap_mgr.s:242`<br>`scrap_mgr.s:200` | ZERO_TRUNCATE - scrap on disk: truncate Clipboard File to 0 bytes |
| **`ZeroScrap`** | `0x016E8E` | `0x0126D8` | `scrap_mgr.s:211` | **Proto:** `_ZeroScrap ($A9FC) - FUNCTION ZeroScrap: LongInt`<br>_ZeroScrap ($A9FC) - FUNCTION ZeroScrap: LongInt Clears the scrap contents and reinitializes it for new data. Bumps ScrapCount (ensures it stays positive by negating if needed). If scrap is in memory:... |
| **`ZEROSCRAP`** | `0x016E8E` | `0x0126D8` | `scrap_mgr.s:172` | — |
| **`ZoomWindow`** | `0x011B18` | `0x00C1B2` | `window_mgr.s:1574` | **Proto:** `Pascal: PROCEDURE ZoomWindow(theWindow: WindowPtr; partCode: INTEGER;`<br>**Regs:** `Entry: 0x4(SP) = front, 0x6(SP) = partCode, 0x8(SP) = theWindow`<br>_ZoomWindow ($A83A): zoom a window to its user state or its standard state Pascal: PROCEDURE ZoomWindow(theWindow: WindowPtr; partCode: INTEGER; front: BOOLEAN); Entry: 0x4(SP) = front, 0x6(SP) = part... |
| **`ZOOMWINDOW`** | `0x011B18` | `0x00C1B2` | `window_mgr.s:1473` | _ZoomWindow ($A95C): zoom window between standard and user state partCode 7 = inZoomIn (restore to user state) partCode 8 = inZoomOut (zoom to standard state) wDataHandle contains two rects: user stat... |
| **`ZOOMWINDOW_OK`** | `0x011B3C` | `0x00C1D6` | `window_mgr.s:1587`<br>`window_mgr.s:1486` | get zoom state rect from wDataHandle |
| **`ZOOMWINDOW_SKIP`** | `0x011B70` | `0x00C20A` | `window_mgr.s:1612`<br>`window_mgr.s:1511` | move window origin to zoom state's topLeft compute new portRect size from zoom state rect redraw at new size optionally bring to front |

---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

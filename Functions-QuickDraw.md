# QuickDraw Function & Routine Directory

This catalog lists all **1,497** routines, functions, exception vectors, and labels belonging to the **QuickDraw** subsystem across the Macintosh Plus (128 KB) and Macintosh SE (256 KB) ROMs.

| Symbol / Routine | Mac Plus Offset | Mac SE Offset | Source File : Line | Description / Prototype |
| :--- | :--- | :--- | :--- | :--- |
| **`ABCDONE`** | `0x00AB72` | `0x0152E2` | `RgnBlt.s:810`<br>`RgnBlt.s:599` | — |
| **`ABCDONE_LOOP`** | `0x00AB84` | `0x0152F4` | `RgnBlt.s:821`<br>`RgnBlt.s:627` | INTERFACE TO EACH OF THE RGNBLT SCANLINE LOOPS: A0: -            D0: scratch A1: -            D1: scratch A2: -            D2: LONGCNT A3: SRCPTR       D3: - A4: MASKPTR      D4: - A5: DSTPTR       D5... |
| **`ABCDONE_LOOP_2`** | `0x00ABB4` | `0x015324` | `RgnBlt.s:863`<br>`RgnBlt.s:650` | ABCDONE_LOOP_2 |
| **`ABCDONE_LOOP_3`** | `0x00ABDC` | `0x01534C` | `RgnBlt.s:889`<br>`RgnBlt.s:669` | MODE 1 OR 5: SRC OR DST --> DST ABCDONE_LOOP_3 Called during boot. |
| **`ABCDONE_LOOP_4`** | `0x00AC04` | `0x015374` | `RgnBlt.s:915`<br>`RgnBlt.s:688` | MODE 2 OR 6: SRC XOR DST --> DST ABCDONE_LOOP_4 Called during boot. |
| **`ABCDONE_LOOP_5`** | `0x00AC2E` | `0x01539E` | `RgnBlt.s:942`<br>`RgnBlt.s:709` | MODE 3 OR 7: SRC BIC DST --> DST MODE 8 OR 12: PATTERN --> DST (FILLING AREAS, DRAWING LINES) Called during boot (15,986 times in 30s trace). |
| **`ABCDONE_LOOP_6`** | `0x00AC44` | `0x0153B4` | `RgnBlt.s:957`<br>`RgnBlt.s:723` | MODE 9 OR 13: PATTERN OR DST --> DST |
| **`ABCDONE_LOOP_7`** | `0x00AC52` | `0x0153C2` | `RgnBlt.s:969`<br>`RgnBlt.s:734` | MODE 10 OR 14: PATTERN XOR DST --> DST (INVERTING AREAS, XOR LINES) Called during boot. |
| **`ABCDONE_LOOP_8`** | `0x00AC60` | `0x0153D0` | `RgnBlt.s:980`<br>`RgnBlt.s:744` | MODE 11 OR 15: PATTERN BIC DST --> DST |
| **`ABCDONE_MODE_TBL`** | `0x00AB74` | `0x0152E4` | `RgnBlt.s:817`<br>`RgnBlt.s:608` | ABCDONE_MODE_TBL - indexed branch table for RgnBlt transfer modes |
| **`ABCLOOP`** | `0x00AB66` | `0x0152D6` | `RgnBlt.s:804`<br>`RgnBlt.s:593` | — |
| **`ABLOOP`** | `0x00B6A0` | `0x015E10` | `DrawArc.s:1058`<br>`DrawArc.s:812` | — |
| **`ABORT`** | `0x00CF76` | `0x0176F2` | `Bitmaps.s:999`<br>`Bitmaps.s:839` | _DisposHandle ;DISCARD IT ABORT |
| **`ABORT_DONE`** | `0x00CF7E` | `0x0176FA` | `Bitmaps.s:1002`<br>`Bitmaps.s:842` | — |
| **`ACROSS1`** | `0x00957A` | `0x013CEA` | `DrawText.s:958`<br>`DrawText.s:842` | Bold buf2 across to the right enough for shadow. |
| **`ACROSS2`** | `0x009584` | `0x013CF4` | `DrawText.s:962`<br>`DrawText.s:846` | — |
| **`ACUTE`** | `0x00B244` | `0x0159B4` | `DrawArc.s:404`<br>`DrawArc.s:290` | SET UP SKIPFLAG TO SKIP OVER UNUSED ARC PORTIONS ACUTE |
| **`ACUTE1`** | `0x00B470` | `0x015BE0` | `DrawArc.s:732`<br>`DrawArc.s:538` | ADJUST ARC STUFF AS WE CROSS THE MIDDLE VERTICALLY RE-CALCULATE SKIPFLAG, AND QUIT IF IT BECOMES TRUE ACUTE1 |
| **`ACUTE1_SKIP`** | `0x00B47C` | `0x015BEC` | `DrawArc.s:742`<br>`DrawArc.s:546` | OBTUSE1 NOW SWAP THE ROLES OF LINE1 AND LINE2 AS THEY CROSS THE MIDDLE |
| **`ACUTE1_SKIP_2`** | `0x00B4A6` | `0x015C16` | `DrawArc.s:752`<br>`DrawArc.s:556` | — |
| **`AddPt`** | `0x00898A` | `0x0130C0` | `GrafAsm.s:312` | **Proto:** `PROCEDURE AddPt(src: Point; VAR dst: Point);`<br>PROCEDURE AddPt(src: Point; VAR dst: Point); { add two points together, restores all regs } |
| **`ADDPT`** | `0x00898A` | `0x0130C0` | `GrafAsm.s:316` | **Proto:** `PROCEDURE AddPt(src: Point; VAR dst: Point);`<br>PROCEDURE AddPt(src: Point; VAR dst: Point); { add two points together, restores all regs } |
| **`ADDSUB`** | `0x00897C` | `0x0130B2` | `GrafAsm.s:298`<br>`GrafAsm.s:303` | ADDSUB Called during boot (62,279 times in 30s trace). |
| **`AGAIN`** | `0x00CB72` | `0x0172EE` | `Bitmaps.s:419`<br>`Bitmaps.s:348` | CALC BUFLEFT SO THAT RGNBUF WILL ALIGN TO DSTBITS INIT BOTH REGION STATE RECORDS AND ALLOCATE BUFFERS AGAIN - bitmap region init loop entry: dereference rgn, init scan state, allocate scanline buffer |
| **`ALESS`** | `0x00C62A` | `0x016D9A` | `RgnOp.s:402`<br>`RgnOp.s:355` | ALESS Called during boot (104,814 times in 30s trace). |
| **`ALLOC`** | `0x00C44C` | `0x016BBC` | `RgnOp.s:120`<br>`RgnOp.s:105` | — |
| **`AngleFromSlope`** | `0x00B790` | `0x015F00` | `Angles.s:9` | **Proto:** `FUNCTION AngleFromSlope(slope: Fixed): INTEGER;`<br>.FUNC AngleFromSlope,1 .DEF SlopeFromAngle FUNCTION AngleFromSlope(slope: Fixed): INTEGER; Scans slope table for angle and returns angle 0..180 |
| **`ANGLEFROMSLOPE`** | `0x00B790` | `0x015F00` | `Angles.s:15` | **Proto:** `FUNCTION AngleFromSlope(slope: Fixed): INTEGER;`<br>.FUNC AngleFromSlope,1 .DEF SlopeFromAngle FUNCTION AngleFromSlope(slope: Fixed): INTEGER; Scans slope table for angle and returns angle 0..180 FUNCTION AngleFromSlope(slope: Fixed): INTEGER; Scans sl... |
| **`APPEND`** | `0x00AF52` | `0x0156C2` | `PutOval.s:253`<br>`PutOval.s:202` | APPEND Called during boot. |
| **`ARCOP`** | `0x00DF72` | `0x0186FE` | `Pictures.s:1100`<br>`Pictures.s:817` | Arc: OP, RECT, STARTANGLE, ARCANGLE |
| **`ARCOP_CONT`** | `0x00DFCA` | — | `Pictures.s:1140` | Rgn: OP, RGN |
| **`ARCOP_CONT_2`** | `0x00DFFC` | — | `Pictures.s:1161` | ARCOP_CONT_2 |
| **`ARCOP_OK`** | `0x00DF94` | `0x018720` | `Pictures.s:1112`<br>`Pictures.s:829` | — |
| **`ARCOP_OK_2`** | `0x00DFC6` | — | `Pictures.s:1133` | — |
| **`ARCOP_OK_3`** | `0x00DFF8` | — | `Pictures.s:1154` | — |
| **`BackColor`** | `0x0083F2` | `0x012B28` | `Util.s:222` | **Proto:** `PROCEDURE PortLong(long: LongInt);`<br>PROCEDURE BackColor(color: LongInt); BackColor FALL THRU INTO PORTLONG PROCEDURE PortLong(long: LongInt); INSTALL A LONG INTO CURRENT GRAFPORT. ENTER WITH OFFSET IN D0 PortLong |
| **`BACKCOLOR`** | `0x0083F2` | `0x012B28` | `Util.s:133` | — |
| **`BackPat`** | `0x0089E0` | `0x013116` | `GrafAsm.s:393` | **Proto:** `PROCEDURE BackPat(pat: Pattern);`<br>PROCEDURE BackPat(pat: Pattern); { set the background pattern } |
| **`BACKPAT`** | `0x0089E0` | `0x013116` | `GrafAsm.s:390` | **Proto:** `PROCEDURE BackPat(pat: Pattern);`<br>PROCEDURE BackPat(pat: Pattern); { set the background pattern } |
| **`BBOXES`** | `0x00C03E` | `0x0167AE` | `Regions.s:866`<br>`Regions.s:712` | IF op = SectScan OR DIFF, THEN INTERSECT THE BOUNDING BOXES. Called during boot (10,188 times in 30s trace). |
| **`BCLOOP`** | `0x00AB26` | `0x015296` | `RgnBlt.s:772`<br>`RgnBlt.s:565` | — |
| **`BCLOOP_CONT`** | `0x00AB32` | `0x0152A2` | `RgnBlt.s:785`<br>`RgnBlt.s:577` | REGIONS A, B AND C ARE ALL NON-RECTANGULAR. UPDATE EACH, THEN FORM INTERSECTION IN THE MASK BUFFER. |
| **`BCLOOP_DONE`** | `0x00AB30` | `0x0152A0` | `RgnBlt.s:777`<br>`RgnBlt.s:570` | — |
| **`BICMODE`** | `0x008598` | `0x012CCE` | `Util.s:517`<br>`Util.s:358` | THE BIC MODES DEPEND ONLY ON THE BACKGROUND COLOR Called during boot. |
| **`BitAnd`** | `0x00833C` | `0x012A72` | `Util.s:26` | .FUNC BitAnd,2 .DEF BitXor,BitOr,BitShift Function BitAnd(long1,long2: LongInt): LongInt; Called during boot (25,880 times in 30s trace). |
| **`BITAND`** | `0x00833C` | `0x012A72` | `Util.s:21` | BitAnd ($A858 sel ?) - long1 AND long2 |
| **`BitBlt`** | `0x00A284` | `0x0149F4` | `BitBlt.s:46` | **Proto:** `PROCEDURE BitBlt(srcBits,dstBits: BitMap;`<br>--> BITBLT.TEXT Low-level bit boundary block transfer. .PROC BITBLT,7 .REF LEFTMASK,RIGHTMASK,PATEXPAND PROCEDURE BitBlt(srcBits,dstBits: BitMap; srcRect,dstRect: Rect; mode: INTEGER; pat: Pattern); T... |
| **`BITBLT`** | `0x00A284` | `0x0149F4` | `BitBlt.s:34` | **Proto:** `PROCEDURE BitBlt(srcBits,dstBits: BitMap;`<br>--> BITBLT.TEXT Low-level bit boundary block transfer. .PROC BITBLT,7 .REF LEFTMASK,RIGHTMASK,PATEXPAND PROCEDURE BitBlt(srcBits,dstBits: BitMap; srcRect,dstRect: Rect; mode: INTEGER; pat: Pattern); T... |
| **`BitClr`** | `0x008384` | `0x012ABA` | `Util.s:110` | **Proto:** `PROCEDURE BitClr(bytePtr: Ptr; bitNum: LongInt);`<br>PROCEDURE BitClr(bytePtr: Ptr; bitNum: LongInt); |
| **`BITCLR`** | `0x008384` | `0x012ABA` | `Util.s:73` | BitClr(bytePtr, bitNum) - clear single bit |
| **`BITCLR_CONT`** | `0x00838E` | `0x012AC4` | `Util.s:122`<br>`Util.s:84` | BITCLR_CONT Called during boot. |
| **`BitMask`** | `0x00842C` | `0x012B62` | `Util.s:307` | RTS RIGHTMASK Bit Mask |
| **`BITMASK`** | `0x00842C` | `0x012B62` | `Util.s:170` | BitMask(D0) -> word in D0 - mask with single bit at position D0 |
| **`BitNot`** | `0x008334` | `0x012A6A` | `Util.s:13` | --> UTIL.TEXT SMALL UTILITY ROUTINES USED BY QuickDraw. .FUNC BitNot,1 Function BitNot(long: LongInt): LongInt; |
| **`BITNOT`** | `0x008334` | `0x012A6A` | `Util.s:14` | --> UTIL.TEXT SMALL UTILITY ROUTINES USED BY QuickDraw. QuickDraw bit utilities (BitNot/And/Xor/Or/Shift/Tst/Set/Clr) Each is a Pascal-callable function with stacked args; pop ret addr to A0, do opera... |
| **`BitOr`** | `0x00834E` | `0x012A84` | `Util.s:48` | Function BitOr(long1,long2: LongInt): LongInt; Called during boot. |
| **`BITOR`** | `0x00834E` | `0x012A84` | `Util.s:36` | BitOr - long1 OR long2 |
| **`BitSet`** | `0x00837A` | `0x012AB0` | `Util.s:100` | **Proto:** `PROCEDURE BitSet(bytePtr: Ptr; bitNum: LongInt);`<br>PROCEDURE BitSet(bytePtr: Ptr; bitNum: LongInt); |
| **`BITSET`** | `0x00837A` | `0x012AB0` | `Util.s:67` | BitSet(bytePtr, bitNum) - set single bit |
| **`BitShift`** | `0x008356` | `0x012A8C` | `Util.s:61` | Function BitShift(long: LongInt; count: INTEGER): LongInt; positive count --> shift left. negative count --> shift right. |
| **`BITSHIFT`** | `0x008356` | `0x012A8C` | `Util.s:43` | BitShift(long, count: INTEGER) - positive=left, negative=right |
| **`BITSHIFT_DONE`** | `0x008368` | `0x012A9E` | `Util.s:77`<br>`Util.s:54` | — |
| **`BITSOK`** | `0x00E0C0` | `0x01884C` | `Pictures.s:1264`<br>`Pictures.s:953` | — |
| **`BITSOK_OK`** | `0x00E0F0` | — | `Pictures.s:1288` | — |
| **`BITSOP`** | — | `0x018788` | `Pictures.s:882` | BITSOP -- bitsRect / bitsRgn / packBitsRect / packBitsRgn opcodes BitsRect:    $90, rowBytes, bounds, srcRect, dstRect, mode, bitData BitsRgn:     $91, rowBytes, bounds, srcRect, dstRect, mode, maskRg... |
| **`BitTst`** | `0x00836C` | `0x012AA2` | `Util.s:88` | **Proto:** `FUNCTION BitTst(bytePtr: Ptr; bitNum: LongInt): BOOLEAN;`<br>.FUNC BitTst,2 .DEF BitSet,BitClr FUNCTION BitTst(bytePtr: Ptr; bitNum: LongInt): BOOLEAN; Called during boot. |
| **`BITTST`** | `0x00836C` | `0x012AA2` | `Util.s:59` | BitTst(bytePtr, bitNum) -> Boolean - test single bit |
| **`BitXor`** | `0x008344` | `0x012A7A` | `Util.s:36` | Function BitXor(long1,long2: LongInt): LongInt; |
| **`BITXOR`** | `0x008344` | `0x012A7A` | `Util.s:28` | BitXor - long1 XOR long2 |
| **`BLACK1`** | `0x00CD7A` | `0x0174F6` | `Bitmaps.s:672`<br>`Bitmaps.s:567` | prepare height and words for DBRA count. Quit if either <= 0. init dst to all ones: |
| **`BLACK16`** | `0x00D83C` | `0x017FB8` | `Stretch.s:1286`<br>`Stretch.s:1115` | BLACK16 |
| **`BLACK16_CONT`** | `0x00D844` | — | `Stretch.s:1296` | BLACK16_CONT |
| **`BLACK2`** | `0x00CD7C` | `0x0174F8` | `Bitmaps.s:674`<br>`Bitmaps.s:569` | — |
| **`BLACKOK`** | `0x00D8AA` | `0x018026` | `Stretch.s:1386`<br>`Stretch.s:1196` | BLACKOK |
| **`BLACKOK_CONT`** | `0x00D8AE` | `0x01802A` | `Stretch.s:1389`<br>`Stretch.s:1199` | — |
| **`BLESS`** | `0x00C636` | `0x016DA6` | `RgnOp.s:416`<br>`RgnOp.s:367` | BLESS Called during boot (51,958 times in 30s trace). |
| **`BOLDIT`** | `0x00941E` | `0x013B8E` | `DrawText.s:762`<br>`DrawText.s:661` | BOLDIT Called during boot. |
| **`BOLDLP`** | `0x009428` | `0x013B98` | `DrawText.s:766`<br>`DrawText.s:665` | — |
| **`BOTH`** | `0x00C4E2` | `0x016C52` | `RgnOp.s:191`<br>`RgnOp.s:168` | BOTH Called during boot (11,252 times in 30s trace). |
| **`BOTOK`** | `0x00C91A` | `0x017096` | `Bitmaps.s:74`<br>`Bitmaps.s:64` | — |
| **`BumpOval`** | `0x00B74E` | `0x015EBE` | `DrawArc.s:1183` | **Proto:** `LOCAL PROCEDURE BumpOval(VAR oval: OvalRec; vert: INTEGER);`<br>_LongMul ;CALC 64BIT (HEIGHT/WIDTH) SQUARED ODDBUMP:= 2 TIMES ASPECT RATIO SQUARED ONLY BUMP IF VERT IS BETWEEN OVALTOP AND OVALBOT .PROC BUMPOVAL,2 LOCAL PROCEDURE BumpOval(VAR oval: OvalRec; vert: I... |
| **`BUMPOVAL`** | `0x00B74E` | `0x015EBE` | `DrawArc.s:920` | **Proto:** `LOCAL PROCEDURE BumpOval(VAR oval: OvalRec; vert: INTEGER);`<br>LOCAL PROCEDURE BumpOval(VAR oval: OvalRec; vert: INTEGER); Bump an oval state record to the next scanline down. INPUTS:  A3 points to oval state record D0 contains current vert CLOBBERS D0-D7, A0-A3 |
| **`BUMPOVAL_GOHOME`** | `0x00B78E` | `0x015EFE` | `DrawArc.s:1244`<br>`DrawArc.s:978` | — |
| **`BUMPOVAL_MORE1`** | `0x00B760` | `0x015ED0` | `DrawArc.s:1212`<br>`DrawArc.s:948` | register usage: D0: vert D1: RSQYSQ D2,D3: SQUARE D4,D5: ODDNUM D6,D7: ODDBUMP A0: LEFTEDGE A1: RIGHTEDGE A2: #$00008000 A3: modified oval ptr WHILE SQUARE < RSQYSQ DO MAKE OVAL BIGGER Called during b... |
| **`BUMPOVAL_MORE2`** | `0x00B772` | `0x015EE2` | `DrawArc.s:1229`<br>`DrawArc.s:963` | WHILE SQUARE > RSQYSQ DO MAKE OVAL SMALLER Called during boot. |
| **`BUMPV`** | `0x00AA52` | `0x0151C2` | `RgnBlt.s:611`<br>`RgnBlt.s:442` | BUMP DESTINATION VERTICALLY AND LOOP FOR ALL ROWS Called during boot (1,767 times in 30s trace). |
| **`CALC`** | `0x00C504` | `0x016C74` | `RgnOp.s:210`<br>`RgnOp.s:185` | CALCULATE SectScan, DIFF, UNION, XOR, OR INSET INTO SCANC Called during boot (63,457 times in 30s trace). |
| **`CALCLP`** | `0x00A5CE` | `0x014D3E` | `BitBlt.s:679`<br>`BitBlt.s:569` | — |
| **`CalcMask`** | `0x00CD38` | `0x0174B4` | `Bitmaps.s:615` | **Proto:** `PROCEDURE CalcMask(srcPtr,dstPtr: Ptr;`<br>PROCEDURE CalcMask(srcPtr,dstPtr: Ptr; srcRow,dstRow,height,words: INTEGER); |
| **`CALCMASK`** | `0x00CD38` | `0x0174B4` | `Bitmaps.s:526` | **Proto:** `PROCEDURE CalcMask(srcPtr, dstPtr: Ptr;`<br>PROCEDURE CalcMask(srcPtr, dstPtr: Ptr; srcRow, dstRow, height, words: INTEGER); |
| **`CALCMASK_NEXTROW`** | `0x00CDC2` | `0x01753E` | `Bitmaps.s:720`<br>`Bitmaps.s:605` | smear dst zeros down and to the right, smear limited by src. |
| **`CALCMASK_SHARE`** | `0x00CD40` | `0x0174BC` | `Bitmaps.s:620`<br>`Bitmaps.s:543` | **Proto:** `LOCAL PROCEDURE MakeMask(srcPtr, dstPtr: Ptr;`<br>LOCAL PROCEDURE MakeMask(srcPtr, dstPtr: Ptr; srcRow, dstRow, height, words: INTEGER; seedH, seedV: INTEGER; edge: LongInt); A6 offsets after LINK: srcPtr=0x1C, dstPtr=0x18, srcRow=0x16, dstRow=0x14, ... |
| **`CALL0`** | `0x00E250` | `0x0189DC` | `Pictures.s:1585`<br>`Pictures.s:1163` | _HLock ;LOCK IT CALL BOTTLENECK PROC, DISPOSE OF ONE OR TWO HANDLES, AND QUIT |
| **`CALL1`** | `0x00E254` | `0x0189E0` | `Pictures.s:1593`<br>`Pictures.s:1167` | CALL1 |
| **`CallArc`** | `0x00AFFC` | `0x01576C` | `Arcs.s:142` | **Proto:** `PROCEDURE CallArc(r: Rect; startAngle,arcAngle: INTEGER);`<br>PROCEDURE CallArc(r: Rect; startAngle,arcAngle: INTEGER); code shared by FrameArc, PaintArc, EraseArc, InvertArc, and FillArc. enter with verb in D0. |
| **`CALLARC`** | `0x00AFFC` | `0x01576C` | `Arcs.s:135` | **Proto:** `PROCEDURE CallArc(r: Rect; startAngle,arcAngle: INTEGER);`<br>PROCEDURE CallArc(r: Rect; startAngle,arcAngle: INTEGER); code shared by FrameArc, PaintArc, EraseArc, InvertArc, and FillArc. enter with verb in D0. |
| **`CallOval`** | `0x00ADFA` | `0x01556A` | `Ovals.s:154` | **Proto:** `PROCEDURE CallOval(r: Rect);`<br>PROCEDURE CallOval(r: Rect); code shared by FrameOval, PaintOval, EraseOval, InvertOval, and FillOval. enter with verb in D0. |
| **`CALLOVAL`** | `0x00ADFA` | `0x01556A` | `Ovals.s:138` | **Proto:** `PROCEDURE CallOval(r: Rect);`<br>PROCEDURE CallOval(r: Rect); code shared by FrameOval, PaintOval, EraseOval, InvertOval, and FillOval. enter with verb in D0. |
| **`CALLOVAL_USESTD`** | `0x00AE18` | `0x015588` | `Ovals.s:167`<br>`Ovals.s:151` | — |
| **`CallPoly`** | `0x00BA1E` | `0x01618E` | `Polygons.s:143` | **Proto:** `PROCEDURE CallPoly(poly: PolyHandle);`<br>PROCEDURE CallPoly(poly: PolyHandle); code shared by FramePoly, PaintPoly, ErasePoly, InvertPoly, and FillPoly. enter with verb in D0. |
| **`CALLPOLY`** | `0x00BA1E` | `0x01618E` | `Polygons.s:120` | **Proto:** `PROCEDURE CallPoly(poly: PolyHandle);`<br>PROCEDURE CallPoly(poly: PolyHandle); Code shared by FramePoly, PaintPoly, ErasePoly, InvertPoly, FillPoly. Enter with verb in D0. |
| **`CALLPOLY_USESTD`** | `0x00BA3C` | `0x0161AC` | `Polygons.s:156`<br>`Polygons.s:133` | — |
| **`CallRect`** | `0x009F38` | `0x0146A8` | `Rects.s:218` | **Proto:** `PROCEDURE CallRect(r: Rect);`<br>PROCEDURE CallRect(r: Rect); code shared by FrameRect, PaintRect, EraseRect, InvertRect, and FillRect. enter with verb in D0. Called during boot. |
| **`CALLRECT`** | `0x009F38` | `0x0146A8` | `Rects.s:184` | CallRect: shared by FrameRect, PaintRect, EraseRect, InvertRect, FillRect. Pops return addr + rect addr, pushes verb byte + rect + return addr, dispatches via grafProcs.rectProc or _StdRect. |
| **`CALLRECT_USESTD`** | `0x009F56` | `0x0146C6` | `Rects.s:231`<br>`Rects.s:197` | — |
| **`CallRgn`** | `0x00BC82` | `0x0163F2` | `Regions.s:135` | **Proto:** `PROCEDURE CallRgn(rgn: RgnHandle);`<br>PROCEDURE CallRgn(rgn: RgnHandle); code shared by FrameRgn, PaintRgn, EraseRgn, InvertRgn, and FillRgn. enter with verb in D0. Called during boot. |
| **`CALLRGN`** | `0x00BC82` | `0x0163F2` | `Regions.s:115` | **Proto:** `PROCEDURE CallRgn(rgn: RgnHandle);`<br>PROCEDURE CallRgn(rgn: RgnHandle); Code shared by FrameRgn, PaintRgn, EraseRgn, InvertRgn, FillRgn. Enter with verb in D0. |
| **`CALLRGN_USESTD`** | `0x00BCA0` | `0x016410` | `Regions.s:148`<br>`Regions.s:128` | — |
| **`CallRRect`** | `0x00AD28` | `0x015498` | `RRects.s:154` | **Proto:** `PROCEDURE CallRRect(r: Rect; ovWd,ovHt: INTEGER);`<br>PROCEDURE CallRRect(r: Rect; ovWd,ovHt: INTEGER); code shared by FrameRoundRect, PaintRoundRect, EraseRoundRect, InvertRoundRect, and FillRoundRect. enter with verb in D0. Called during boot. |
| **`CALLRRECT`** | `0x00AD28` | `0x015498` | `RRects.s:151` | **Proto:** `PROCEDURE CallRRect(r: Rect; ovWd,ovHt: INTEGER);`<br>PROCEDURE CallRRect(r: Rect; ovWd,ovHt: INTEGER); code shared by FrameRoundRect, PaintRoundRect, EraseRoundRect, InvertRoundRect, and FillRoundRect. enter with verb in D0. Called during boot. |
| **`CALLRRECT_USESTD`** | `0x00AD4A` | `0x0154BA` | `RRects.s:169`<br>`RRects.s:166` | — |
| **`CallText`** | `0x008C42` | `0x013378` | `Text.s:280` | **Proto:** `PROCEDURE CallText(count: INTEGER; textAddr: Ptr);`<br>.PROC CallText,2 .REF STDTEXT PROCEDURE CallText(count: INTEGER; textAddr: Ptr); Called during boot. |
| **`CALLTEXT`** | `0x008C42` | `0x013378` | `Text.s:245` | **Proto:** `PROCEDURE CallText(count: INTEGER; textAddr: Ptr);`<br>.PROC CallText,2 .REF STDTEXT PROCEDURE CallText(count: INTEGER; textAddr: Ptr); Called during boot. |
| **`CALLTEXT_USESTD`** | `0x008C60` | `0x013396` | `Text.s:292`<br>`Text.s:257` | — |
| **`CASEOK`** | `0x00C420` | `0x016B90` | `RgnOp.s:93`<br>`RgnOp.s:82` | — |
| **`CHANGES`** | `0x00C518` | `0x016C88` | `RgnOp.s:224`<br>`RgnOp.s:197` | FIND ANY CHANGES NOT IN PREVIOUS SCANC, THEN UPDATE SCANC Called during boot (63,457 times in 30s trace). |
| **`CHANGES_NO`** | `0x00C538` | `0x016CA8` | `RgnOp.s:241`<br>`RgnOp.s:212` | CHANGES_NO Called during boot (88,978 times in 30s trace). |
| **`CharWidth`** | `0x008C7C` | `0x0133B2` | `Text.s:326` | **Proto:** `FUNCTION CharWidth(ch: CHAR): INTEGER;`<br>FUNCTION CharWidth(ch: CHAR): INTEGER; Called during boot. |
| **`CHARWIDTH`** | `0x008C7C` | `0x0133B2` | `Text.s:288` | **Proto:** `FUNCTION CharWidth(ch: CHAR): INTEGER;`<br>FUNCTION CharWidth(ch: CHAR): INTEGER; Called during boot. |
| **`CHARWIDTH_SHARE`** | `0x008C8E` | `0x0133C4` | `Text.s:332`<br>`Text.s:294` | — |
| **`CHECK`** | `0x00B816` | `0x015F86` | `Angles.s:78`<br>`Angles.s:82` | — |
| **`CheckPic`** | `0x00E448` | `0x018BD4` | `Pictures.s:1937` | Check Pic Called during boot. |
| **`CHECKPIC`** | `0x00E448` | `0x018BD4` | `Pictures.s:1425` | **Proto:** `PROCEDURE CheckPic`<br>PROCEDURE CheckPic Called from every StdXxx routine (StdLine/StdRect/etc.) before writing geometry. Returns flags LE if not recording (PicSave nil or pen hidden). Otherwise checks fgColor, bkColor, or... |
| **`CHECKPIC_NO`** | `0x00E486` | `0x018C12` | `Pictures.s:1979`<br>`Pictures.s:1447` | CHECK FOR CHANGES IN FOREGROUND COLOR FGCOLOK CHECK FOR CHANGES IN BACKGROUND COLOR |
| **`CHECKPIC_NO_2`** | `0x00E4A6` | `0x018C32` | `Pictures.s:1990`<br>`Pictures.s:1459` | Check for origin changes (portRect.topLeft vs picOrigin). |
| **`CHECKUL`** | `0x00947A` | `0x013BEA` | `DrawText.s:822`<br>`DrawText.s:718` | Underline characters in buffer if necessary. Use characters in buffer to hide parts of the underline. Called during boot. |
| **`CKBOLD`** | `0x009416` | — | `DrawText.s:752` | Make buffer bold if necessary: Called during boot. |
| **`CKPAT`** | `0x00B0B8` | `0x015828` | `DrawArc.s:182`<br>`DrawArc.s:98` | CHECK FOR BLACK OR WHITE PATTERN Called during boot. |
| **`CLEANUP`** | `0x00CADA` | `0x017256` | `Bitmaps.s:312`<br>`Bitmaps.s:269` | — |
| **`CLIPOK`** | `0x00E508` | `0x018C94` | `Pictures.s:2030`<br>`Pictures.s:1491` | — |
| **`ClipRect`** | `0x008A6E` | `0x0131A4` | `GrafAsm.s:485` | **Proto:** `PROCEDURE ClipRect(r: Rect);`<br>PROCEDURE ClipRect(r: Rect); { Make the current grafport's clipRgn match a given rectangle } Called during boot (64,069 times in 30s trace). |
| **`CLIPRECT`** | `0x008A6E` | `0x0131A4` | `GrafAsm.s:475` | **Proto:** `PROCEDURE ClipRect(r: Rect);`<br>PROCEDURE ClipRect(r: Rect); { Make the current grafport's clipRgn match a given rectangle } Called during boot (64,069 times in 30s trace). |
| **`CLOSEPIC_OVERFLO`** | — | `0x01824A` | `Pictures.s:287` | — |
| **`ClosePicture`** | `0x00DAA8` | `0x018224` | `Pictures.s:339` | **Proto:** `PROCEDURE ClosePicture;`<br>.PROC ClosePicture,0 .REF PutPicByte,ShowPen,SetSize PROCEDURE ClosePicture; |
| **`CLOSEPICTURE`** | `0x00DAA8` | `0x018224` | `Pictures.s:272` | **Proto:** `PROCEDURE ClosePicture;`<br>PROCEDURE ClosePicture; Closes the picture currently being recorded. Appends the endPic opcode (0xFF), trims the picture handle to its final size, and disposes of PicSave (clip rgn + record itself). T... |
| **`CLOSEPICTURE_GOHOME`** | `0x00DADE` | `0x01825A` | `Pictures.s:363`<br>`Pictures.s:294` | _DisposHandle ;DISCARD IT |
| **`ClosePoly`** | `0x00BA72` | `0x0161E2` | `Polygons.s:194` | **Proto:** `PROCEDURE ClosePoly;`<br>.PROC ClosePoly,0 .REF SetSize,ShowPen PROCEDURE ClosePoly; A6 OFFSETS OF PARAMS AND LOCALS AFTER LINK: |
| **`CLOSEPOLY`** | `0x00BA72` | `0x0161E2` | `Polygons.s:163` | **Proto:** `PROCEDURE ClosePoly;`<br>PROCEDURE ClosePoly; |
| **`CLOSEPOLY_BOTOK`** | `0x00BAAE` | `0x01621E` | `Polygons.s:233`<br>`Polygons.s:200` | — |
| **`CLOSEPOLY_LEFTOK`** | `0x00BAB6` | `0x016226` | `Polygons.s:238`<br>`Polygons.s:205` | — |
| **`CLOSEPOLY_NEXTPT`** | `0x00BAA0` | `0x016210` | `Polygons.s:224`<br>`Polygons.s:191` | SCAN FOR BOUNDING BOX OF POLYGON CLOSEPOLY_NEXTPT |
| **`CLOSEPOLY_TOPOK`** | `0x00BAA8` | `0x016218` | `Polygons.s:229`<br>`Polygons.s:196` | — |
| **`ClosePort`** | `0x008904` | `0x01303A` | `GrafAsm.s:228` | **Proto:** `PROCEDURE ClosePort(port: GrafPtr);`<br>.PROC ClosePort,1 PROCEDURE ClosePort(port: GrafPtr); { just disposes of clipRgn and visRgn } Called during boot. |
| **`CLOSEPORT`** | `0x008904` | `0x01303A` | `GrafAsm.s:235` | **Proto:** `PROCEDURE ClosePort(port: GrafPtr);`<br>.PROC ClosePort,1 PROCEDURE ClosePort(port: GrafPtr); { just disposes of clipRgn and visRgn } Called during boot. |
| **`CloseRgn`** | `0x00BDA8` | `0x016518` | `Regions.s:337` | **Proto:** `PROCEDURE CloseRgn(* dstRgn: RgnHandle *);`<br>.PROC CloseRgn,1 .REF ShowPen,SortPoints,CullPoints,PackRgn PROCEDURE CloseRgn(* dstRgn: RgnHandle *); Sort array of inversion points and pack into region. A6 OFFSETS OF PARAMS AND LOCALS AFTER LINK: ... |
| **`CLOSERGN`** | `0x00BDA8` | `0x016518` | `Regions.s:273` | **Proto:** `PROCEDURE CloseRgn(* dstRgn: RgnHandle *);`<br>PROCEDURE CloseRgn(* dstRgn: RgnHandle *); Sort array of inversion points and pack into region. |
| **`CLOSERGN_DONE`** | `0x00BDF4` | `0x016564` | `Regions.s:370`<br>`Regions.s:298` | _DisposHandle ;DISCARD IT Called during boot. |
| **`CLR2`** | `0x009558` | `0x013CC8` | `DrawText.s:941`<br>`DrawText.s:826` | Shadowing will be used. Allocate buf2, 4 scans taller than BUF1. Clear out new 4 scanlines, and copy BUF1 into the rest. |
| **`CLRDST`** | `0x00D164` | `0x0178E0` | `Stretch.s:205`<br>`Stretch.s:152` | ALLOCATE AND CLEAR DSTBUF TO HOLD DSTWIDTH. |
| **`CLRLOOP`** | `0x0091C4` | `0x013934` | `DrawText.s:383`<br>`DrawText.s:328` | Allocate and clear an off-screen buffer |
| **`CLRLP`** | `0x0087BE` | `0x012EF4` | `GrafAsm.s:29`<br>`GrafAsm.s:65` | new addition 22 Apr 85 |
| **`CLRMASK`** | `0x00B30E` | `0x015A7E` | `DrawArc.s:531`<br>`DrawArc.s:380` | IF FASTFLAG, THEN SKIP REGION SETUP CALC BUFSIZE ALLOCATE AND CLEAR A SCANLINE BUFFER FOR THE COMPOSITE MASK Called during boot. |
| **`CLRMASK_CONT`** | `0x00B354` | `0x015AC4` | `DrawArc.s:561`<br>`DrawArc.s:407` | ARECT CLRMASK_CONT -- iNIT STATE, ALLOC BUFFER. |
| **`CLRMASK_EXIT`** | `0x00B364` | `0x015AD4` | `DrawArc.s:572`<br>`DrawArc.s:417` | CLRMASK_EXIT Called during boot. |
| **`CLRMASK_NO`** | `0x00B3DE` | `0x015B4E` | `DrawArc.s:645`<br>`DrawArc.s:468` | SET UP CASE JUMP BASED ON MODE AND FASTFLAG CLRMASK_NO Called during boot. |
| **`CLRMASK_OK`** | `0x00B336` | `0x015AA6` | `DrawArc.s:549`<br>`DrawArc.s:397` | INIT STATE RECORDS AND ALLOCATE BUFFERS FOR EACH NON-RECTANGULAR REGION |
| **`CLRMASK_SKIP`** | `0x00B382` | `0x015AF2` | `DrawArc.s:588`<br>`DrawArc.s:426` | BRECT IF BOTH REGIONS ARE RECTANGULAR, THEN DRAW MINRECT INTO MASK BUFFER |
| **`CLRMASK_SKIP_2`** | `0x00B3F4` | `0x015B64` | `DrawArc.s:658`<br>`DrawArc.s:480` | EXPAND 8 BYTE PATTERN TO 16 LONGS AND INIT PATTERN SELECTOR |
| **`CLRMORE`** | `0x009CC8` | `0x014438` | `DrawLine.s:733`<br>`DrawLine.s:611` | — |
| **`CLRONE`** | `0x009CC4` | `0x014434` | `DrawLine.s:730`<br>`DrawLine.s:608` | — |
| **`CLRSRC`** | `0x00D14A` | `0x0178C6` | `Stretch.s:190`<br>`Stretch.s:138` | Hide the cursor if it intersects MinRect Allocate and clear SrcBuf to hold SrcWidth |
| **`CLRTWO`** | `0x009CC2` | `0x014432` | `DrawLine.s:728`<br>`DrawLine.s:606` | ELSE WHITE DRAW A WHITE HORIZONTAL LINE CLRTWO |
| **`ColorBit`** | `0x008400` | `0x012B36` | `Util.s:237` | **Proto:** `PROCEDURE ColorBit(whichBit: INTEGER);`<br>PROCEDURE ColorBit(whichBit: INTEGER); ColorBit FALL THRU INTO PORTWORD |
| **`COLORBIT`** | `0x008400` | `0x012B36` | `Util.s:143` | ColorBit ($A864) - set port colorBit (1-byte plane index) |
| **`ColorMap`** | `0x008560` | `0x012C96` | `Util.s:478` | **Proto:** `PROCEDURE ColorMap(mode: INTEGER, pat: Pattern);`<br>.PROC ColorMap,2 PROCEDURE ColorMap(mode: INTEGER, pat: Pattern); ADJUST INPUT MODE AND PATTERN TO ACCOMPLISH COLOR SEPARATION. Returns (altered) mode and pat on the stack where they were. PRESERVES A... |
| **`COLORMAP`** | `0x008560` | `0x012C96` | `Util.s:334` | ColorMap(mode: INTEGER, pat: Pattern) - adjust mode/pat for color separation. Modifies caller's mode (0x1C(SP)) and pat (0x18(SP)) in place. Preserves all registers. Used to map drawing modes onto a s... |
| **`COLORMAP_COPY`** | `0x0085A0` | `0x012CD6` | `Util.s:526`<br>`Util.s:363` | THE COPY MODES DEPEND ON BOTH FOREGOUND AND BACKGROUND Called during boot. |
| **`COLORMAP_SHARE`** | `0x00858E` | `0x012CC4` | `Util.s:507`<br>`Util.s:352` | — |
| **`COLOROK`** | `0x0085CE` | `0x012D04` | `Util.s:559`<br>`Util.s:388` | Called by: COLORMAP, COLORMAP_SHARE, COLORMAP_COPY |
| **`COMMENTOP`** | `0x00E0D2` | `0x01885E` | `Pictures.s:1276`<br>`Pictures.s:964` | CommentOp: OP, KIND, { SIZE, DATA } |
| **`COMMENTOP_OK`** | — | `0x01887C` | `Pictures.s:976` | — |
| **`CONTEXT`** | `0x00E118` | — | `Pictures.s:1331` | CONTEXT Easter Egg - draws a small bitmap ("stolen from Apple Computer") into the screen buffer and then halts by spinning forever. Context: - A5 points into QuickDraw state / globals used here. - (A5... |
| **`CONTINUE`** | `0x00B7B2` | `0x015F22` | `Angles.s:26`<br>`Angles.s:31` | CONTINUE |
| **`COPY`** | `0x00BE36` | `0x0165A6` | `Regions.s:410`<br>`Regions.s:333` | — |
| **`COPY0`** | `0x00A522` | — | `BitBlt.s:558` | — |
| **`COPY31`** | `0x00A524` | — | `BitBlt.s:565` | COPY31 |
| **`COPY32`** | `0x00A502` | `0x014C72` | `BitBlt.s:541`<br>`BitBlt.s:442` | COPY32 -- else copy 32 words. COPY32 |
| **`COPYBIG`** | `0x00A4EA` | `0x014C5A` | `BitBlt.s:518`<br>`BitBlt.s:416` | Call copybig with wordcount in D2 (clobbered) |
| **`COPYBIG_DONE`** | `0x00A4FC` | `0x014C6C` | `BitBlt.s:532`<br>`BitBlt.s:429` | COPYBIG_DONE |
| **`COPYBIG_LOOP`** | `0x00A4F2` | `0x014C62` | `BitBlt.s:522`<br>`BitBlt.s:420` | — |
| **`CopyBits`** | `0x00CA4A` | `0x0171C6` | `Bitmaps.s:229` | **Proto:** `PROCEDURE CopyBits(srcBits,dstBits: BitMap;`<br>.PROC CopyBits,6 .REF StdBits,ShieldCursor,ShowCursor,StretchBits PROCEDURE CopyBits(srcBits,dstBits: BitMap; srcRect,dstRect: Rect; mode: INTEGER; maskRgn: RgnHandle *); A6 OFFSETS OF PARAMS AND LOCA... |
| **`COPYBITS`** | `0x00CA4A` | `0x0171C6` | `Bitmaps.s:205` | **Proto:** `PROCEDURE CopyBits(srcBits, dstBits: BitMap;`<br>PROCEDURE CopyBits(srcBits, dstBits: BitMap; srcRect, dstRect: Rect; mode: INTEGER; maskRgn: RgnHandle); A6 offsets of params and locals after LINK: PARAMSIZE = 22 SRCBITS   = PARAMSIZE+8-4  (LONG, ad... |
| **`COPYBITS_DONE`** | `0x00CAE2` | `0x01725E` | `Bitmaps.s:316`<br>`Bitmaps.s:273` | — |
| **`COPYBITS_MASKOK`** | `0x00CAB0` | `0x01722C` | `Bitmaps.s:290`<br>`Bitmaps.s:249` | — |
| **`COPYBITS_USESTD`** | `0x00CAD8` | `0x017254` | `Bitmaps.s:310`<br>`Bitmaps.s:267` | — |
| **`COPYLP`** | `0x009568` | `0x013CD8` | `DrawText.s:947`<br>`DrawText.s:832` | — |
| **`CopyMask`** | `0x00CAF0` | `0x01726C` | `Bitmaps.s:336` | **Proto:** `PROCEDURE CopyMask(srcBits,maskBits,dstBits: BitMap;`<br>.PROC CopyMask .REF RSect,HideCursor,ShowCursor,InitRgn,SeekRgn,XorSlab PROCEDURE CopyMask(srcBits,maskBits,dstBits: BitMap; srcRect,maskRect,dstRect: Rect); NEW ROUTINE ADDED TO QUICKDRAW April 28, 1... |
| **`COPYMASK`** | `0x00CAF0` | `0x01726C` | `Bitmaps.s:296` | **Proto:** `PROCEDURE CopyMask(srcBits, maskBits, dstBits: BitMap;`<br>PROCEDURE CopyMask(srcBits, maskBits, dstBits: BitMap; srcRect, maskRect, dstRect: Rect); New routine added to QuickDraw April 28, 1985 by Bill Atkinson. CopyRight 1985 Apple Computer Inc. A6 offsets ... |
| **`COPYMASK_GOHOME`** | `0x00CD1E` | `0x01749A` | `Bitmaps.s:588`<br>`Bitmaps.s:503` | bump vertically and loop for all scanlines |
| **`COPYMASK_NEXTROW`** | `0x00CCA0` | `0x01741C` | `Bitmaps.s:538`<br>`Bitmaps.s:456` | Set up srcRow, srcShift, and starting srcAddr Set up maskRow, maskShift, and starting maskAddr MAKE REGION BUFFERS CURRENT FOR THIS VERTICAL. THEN SET UP AND DRAW CURRENT SCANLINE. |
| **`COPYMASK_NEXTROW_LOOP`** | `0x00CCCC` | `0x017448` | `Bitmaps.s:551`<br>`Bitmaps.s:469` | — |
| **`COPYMASK_NO`** | `0x00CB28` | `0x0172A4` | `Bitmaps.s:388`<br>`Bitmaps.s:319` | A6 OFFSETS OF LOCALS AFTER LINK: if dst is in thePort, then clip to visRgn and clipRgn NOTPORT CALC MINRECT, THE INTERSECTION OF DSTRECT, DSTBITS.BOUNDS, AND TWO REGION BOUNDING BOXES. QUIT IF RESULT ... |
| **`COPYOP`** | `0x00CFDC` | `0x017758` | `Bitmaps.s:1085`<br>`Bitmaps.s:913` | COPYOP |
| **`CopyRgn`** | `0x00BDFE` | `0x01656E` | `Regions.s:386` | **Proto:** `PROCEDURE CopyRgn(* srcRgn,dstRgn: RgnHandle *);`<br>.PROC CopyRgn,1 .REF SetSize PROCEDURE CopyRgn(* srcRgn,dstRgn: RgnHandle *); PARAMSIZE .EQU 8 SRCRGN .EQU PARAMSIZE+8-4 ;RGNHANDLE DSTRGN .EQU SRCRGN-4 ;RGNHANDLE Called during boot (9,298 times in 3... |
| **`COPYRGN`** | `0x00BDFE` | `0x01656E` | `Regions.s:313` | **Proto:** `PROCEDURE CopyRgn(* srcRgn, dstRgn: RgnHandle *);`<br>PROCEDURE CopyRgn(* srcRgn, dstRgn: RgnHandle *); A6 offsets of params after LINK: PARAMSIZE = 8 SRCRGN    = PARAMSIZE+8-4  (RgnHandle) DSTRGN    = SRCRGN-4       (RgnHandle) Called by: INITPORT, GETC... |
| **`COPYRGN_COPYLP`** | `0x00BE3E` | `0x0165AE` | `Regions.s:421`<br>`Regions.s:342` | COPYRGN_COPYLP Called during boot (111,099 times in 30s trace). |
| **`COUNTOK`** | `0x008AD0` | `0x013206` | `Text.s:61`<br>`Text.s:44` | — |
| **`CPY2BUF`** | `0x00AB1E` | `0x01528E` | `RgnBlt.s:769`<br>`RgnBlt.s:562` | — |
| **`CRSR_CLEAR_BUSY`** | `0x001CE6` | `0x018E18` | `CrsrCore.s:73`<br>`CrsrCore.s:92` | — |
| **`CRSRCORE`** | — | `0x018DBC` | `CrsrCore.s:42` | Cursor core -- cursor drawing, ScrnAddress/ScrnSize/ScrnBitMap, CrsrVBLTask, PinRect Apple source: CrsrCore.a (System 7.1: QuickDraw/Classic/CrsrCore.a; the SE link map calls the module CRSRCORE). The... |
| **`CRSRLP`** | `0x0087F2` | `0x012F28` | `GrafAsm.s:63`<br>`GrafAsm.s:84` | _GetScrnBits ;fill in screenBits |
| **`CrsrVBLTask`** | `0x001E86` | `0x018FB8` | `CrsrCore.s:343` | CrsrVBLTask - Cursor update task called every VBL (60.15 Hz) Processes pending mouse movement (from SCC quadrature interrupts): applies mouse scaling/acceleration, constrains to CrsrPin rect, applies ... |
| **`CRSRVBLTASK`** | `0x001E86` | `0x018FB8` | `CrsrCore.s:341` | CrsrVBLTask -- per-VBL cursor + mouse acceleration tick Runs from the VBL ISR. If CrsrNew is set (mouse moved), reads the latest raw mouse delta from MTemp - RawMouse, accumulates mickey samples in a ... |
| **`CRSVBL_ABS_DV`** | — | `0x018FE6` | `CrsrCore.s:355` | — |
| **`CRSVBL_ACCEL`** | `0x001EB6` | — | `CrsrCore.s:374` | CRSVBL_ACCEL - Apply mouse acceleration if distance exceeds threshold |
| **`CRSVBL_ADD_HDELTA`** | `0x001EB4` | — | `CrsrCore.s:367` | CRSVBL_ADD_HDELTA - Add positive horizontal delta to Manhattan distance Called during boot. |
| **`CRSVBL_APPLY_DELTA`** | `0x001EC6` | — | `CrsrCore.s:381` | — |
| **`CRSVBL_AVG_OK`** | — | `0x019096` | `CrsrCore.s:439` | — |
| **`CRSVBL_CLEAR_FLAGS`** | `0x001EFC` | `0x0190E8` | `CrsrCore.s:400`<br>`CrsrCore.s:471` | — |
| **`CRSVBL_COMPUTE_MICKEY`** | — | `0x018FF2` | `CrsrCore.s:363` | — |
| **`CRSVBL_DELTA_OK`** | — | `0x019084` | `CrsrCore.s:432` | — |
| **`CRSVBL_HORIZ_DELTA`** | `0x001EA6` | — | `CrsrCore.s:355` | — |
| **`CRSVBL_PICK_MAX`** | — | `0x018FEC` | `CrsrCore.s:359` | — |
| **`CRSVBL_REDRAW`** | `0x001EF2` | `0x0190E0` | `CrsrCore.s:396`<br>`CrsrCore.s:467` | — |
| **`CRSVBL_RESET_AND_REDRAW`** | — | `0x019102` | `CrsrCore.s:483` | Coupled but no mickey delta: reset window and redraw. |
| **`CRSVBL_RESET_AND_RTS`** | — | `0x0190F4` | `CrsrCore.s:477` | Mouse not moved (or busy): reset the mickey window and return. |
| **`CRSVBL_RETURN`** | `0x001F08` | — | `CrsrCore.s:404` | — |
| **`CRSVBL_RING_DISPATCH`** | — | `0x01900C` | `CrsrCore.s:373` | — |
| **`CRSVBL_RING_N2`** | — | `0x01901A` | `CrsrCore.s:387` | Fan-in summer dispatch table -- compute D5 = sum of latest N mickeys stored in the ring buffer at A0+4..A0+16. Each entry shifts older samples down by one slot to make room for the new sample (which i... |
| **`CRSVBL_RING_N3`** | — | `0x01901C` | `CrsrCore.s:389` | Fan-in summer dispatch table -- compute D5 = sum of latest N mickeys stored in the ring buffer at A0+4..A0+16. Each entry shifts older samples down by one slot to make room for the new sample (which i... |
| **`CRSVBL_RING_N4`** | — | `0x01901E` | `CrsrCore.s:391` | Fan-in summer dispatch table -- compute D5 = sum of latest N mickeys stored in the ring buffer at A0+4..A0+16. Each entry shifts older samples down by one slot to make room for the new sample (which i... |
| **`CRSVBL_RING_N5`** | — | `0x019020` | `CrsrCore.s:393` | Fan-in summer dispatch table -- compute D5 = sum of latest N mickeys stored in the ring buffer at A0+4..A0+16. Each entry shifts older samples down by one slot to make room for the new sample (which i... |
| **`CRSVBL_RING_N6`** | — | `0x019022` | `CrsrCore.s:395` | Fan-in summer dispatch table -- compute D5 = sum of latest N mickeys stored in the ring buffer at A0+4..A0+16. Each entry shifts older samples down by one slot to make room for the new sample (which i... |
| **`CRSVBL_RING_N7`** | — | `0x019024` | `CrsrCore.s:397` | Fan-in summer dispatch table -- compute D5 = sum of latest N mickeys stored in the ring buffer at A0+4..A0+16. Each entry shifts older samples down by one slot to make room for the new sample (which i... |
| **`CRSVBL_RING_N8`** | — | `0x019026` | `CrsrCore.s:399` | Fan-in summer dispatch table -- compute D5 = sum of latest N mickeys stored in the ring buffer at A0+4..A0+16. Each entry shifts older samples down by one slot to make room for the new sample (which i... |
| **`CRSVBL_RING_TBL`** | — | `0x019018` | `CrsrCore.s:385` | Fan-in summer dispatch table -- compute D5 = sum of latest N mickeys stored in the ring buffer at A0+4..A0+16. Each entry shifts older samples down by one slot to make room for the new sample (which i... |
| **`CRSVBL_STORE_NEW`** | — | `0x019066` | `CrsrCore.s:419` | — |
| **`CRSVBL_SUM_SLOT1`** | — | `0x01902A` | `CrsrCore.s:401` | Fan-in summer dispatch table -- compute D5 = sum of latest N mickeys stored in the ring buffer at A0+4..A0+16. Each entry shifts older samples down by one slot to make room for the new sample (which i... |
| **`CRSVBL_SUM_SLOT2`** | — | `0x019034` | `CrsrCore.s:404` | — |
| **`CRSVBL_SUM_SLOT3`** | — | `0x01903E` | `CrsrCore.s:407` | — |
| **`CRSVBL_SUM_SLOT4`** | — | `0x019048` | `CrsrCore.s:410` | — |
| **`CRSVBL_SUM_SLOT5`** | — | `0x019052` | `CrsrCore.s:413` | — |
| **`CRSVBL_SUM_SLOT6`** | — | `0x01905C` | `CrsrCore.s:416` | — |
| **`CRSVBL_THRESHOLD_LOOP`** | — | `0x0190A0` | `CrsrCore.s:443` | — |
| **`CRSVBL_UPDATE_POS`** | `0x001EEE` | `0x0190DC` | `CrsrCore.s:394`<br>`CrsrCore.s:465` | — |
| **`CullPoints`** | `0x00C73C` | `0x016EAC` | `SortPoints.s:161` | **Proto:** `PROCEDURE CullPoints(ptBuf: PointsPtr; VAR ptCount: INTEGER);`<br>.PROC CullPoints,2 PROCEDURE CullPoints(ptBuf: PointsPtr; VAR ptCount: INTEGER); CANCEL ANY DUPLICATE PAIRS OF POINTS IN AN ARRAY OF POINTS. A6 OFFSETS OF PARAMETERS AFTER LINK: PARAMSIZE .EQU 8 PTBUF... |
| **`CULLPOINTS`** | `0x00C73C` | `0x016EAC` | `SortPoints.s:132` | **Proto:** `PROCEDURE CullPoints(ptBuf: PointsPtr; VAR ptCount: INTEGER);`<br>PROCEDURE CullPoints(ptBuf: PointsPtr; VAR ptCount: INTEGER); Cancel any duplicate pairs of points in an array of points. A6 offsets of params after LINK: PARAMSIZE = 8 PTBUF     = PARAMSIZE+8-4  (LON... |
| **`CULLPOINTS_DELETE`** | `0x00C762` | `0x016ED2` | `SortPoints.s:186`<br>`SortPoints.s:151` | CULLPOINTS_DELETE -- the source pair was a duplicate: drop both points Called during boot. |
| **`CULLPOINTS_DONE`** | `0x00C776` | `0x016EE6` | `SortPoints.s:205`<br>`SortPoints.s:168` | — |
| **`CULLPOINTS_GOHOME`** | `0x00C782` | `0x016EF2` | `SortPoints.s:211`<br>`SortPoints.s:174` | — |
| **`CULLPOINTS_MORE1`** | `0x00C766` | `0x016ED6` | `SortPoints.s:195`<br>`SortPoints.s:158` | CULLPOINTS_MORE1 Called during boot. |
| **`CULLPOINTS_WHILE1`** | `0x00C76E` | `0x016EDE` | `SortPoints.s:200`<br>`SortPoints.s:163` | — |
| **`CURDATA`** | `0x008800` | `0x012F36` | `GrafAsm.s:93`<br>`GrafAsm.s:124` | thePort := NIL QuickDraw default globals data: arrow cursor + 5 standard patterns Patterns are 8x8 pixels, 1 bit per pixel, 1 byte per row. Bit 7 = leftmost pixel, bit 0 = rightmost pixel (MSB first).... |
| **`DHDV`** | `0x0096D0` | `0x013E40` | `Lines.s:86`<br>`Lines.s:86` | DHDV |
| **`DHOK`** | `0x00B928` | `0x016098` | `Angles.s:164`<br>`Angles.s:204` | DHOK |
| **`DHPOS`** | `0x009DAE` | `0x01451E` | `PutLine.s:45`<br>`PutLine.s:36` | IF LINE IS VERTICAL, IGNORE IT. CALC BYTESNEEDED = 8 * ( Min(ABS(dh),ABS(dv)) + 1) |
| **`DiffRgn`** | `0x00BFE6` | `0x016756` | `Regions.s:769` | **Proto:** `PROCEDURE DiffRgn(srcRgnA,srcRgnB,dstRgn: RgnHandle);`<br>PROCEDURE DiffRgn(srcRgnA,srcRgnB,dstRgn: RgnHandle); calculate the difference A-B of two regions Called during boot (3,700 times in 30s trace). |
| **`DIFFRGN`** | `0x00BFE6` | `0x016756` | `Regions.s:639` | **Proto:** `PROCEDURE DiffRgn(srcRgnA,srcRgnB,dstRgn: RgnHandle);`<br>PROCEDURE DiffRgn(srcRgnA,srcRgnB,dstRgn: RgnHandle); Calculate the difference A-B of two regions. |
| **`DiffScan`** | `0x00C602` | `0x016D72` | `RgnOp.s:365` | Diff Scan Called during boot (36,951 times in 30s trace). |
| **`DIFFSCAN`** | `0x00C602` | `0x016D72` | `RgnOp.s:322` | DiffScan |
| **`DIREC`** | `0x00A308` | `0x014A78` | `BitBlt.s:164`<br>`BitBlt.s:106` | DIREC Called during boot. |
| **`DIROK`** | `0x00A3CE` | `0x014B3E` | `BitBlt.s:302`<br>`BitBlt.s:215` | — |
| **`DIROK_NO`** | `0x00A3FC` | `0x014B6C` | `BitBlt.s:332`<br>`BitBlt.s:240` | SET UP MODE CASE JUMP IN A1 DIROK_NO Called during boot. |
| **`DISPOSERGN`** | — | `0x0164E2` | `Regions.s:243` | **Proto:** `PROCEDURE DisposeRgn(rgn: RgnHandle);`<br>PROCEDURE DisposeRgn(rgn: RgnHandle); |
| **`DisposRgn`** | `0x00BD72` | — | `Regions.s:292` | **Proto:** `PROCEDURE DisposeRgn(rgn: RgnHandle);`<br>RTS ;RETURN TO CALLER .PROC DisposeRgn PROCEDURE DisposeRgn(rgn: RgnHandle); Called during boot (4,137 times in 30s trace). |
| **`DLOOP`** | `0x0084F4` | `0x012C2A` | `Util.s:418`<br>`Util.s:271` | — |
| **`DOBITS`** | `0x00E0A8` | `0x018834` | `Pictures.s:1256`<br>`Pictures.s:945` | — |
| **`DOCOPY`** | `0x00CFCE` | `0x01774A` | `Bitmaps.s:1072`<br>`Bitmaps.s:901` | — |
| **`DOFILL`** | `0x00CFEC` | `0x017768` | `Bitmaps.s:1094`<br>`Bitmaps.s:922` | — |
| **`DOIT`** | `0x00AFB4` | `0x015724` | `Arcs.s:70`<br>`Arcs.s:70` | Currently, FrameArc does not put inversion points to theRgn. If this changes, add test and call to PutArc here. |
| **`DoLine`** | `0x009748` | `0x013EB8` | `Lines.s:175` | **Proto:** `PROCEDURE DoLine(newPt: Point);`<br>.PROC DoLine,1 .REF DrawLine,PutLine,SetSize PROCEDURE DoLine(newPt: Point); { called by StdLine and StdPoly frame } Called during boot. |
| **`DOLINE`** | `0x009748` | `0x013EB8` | `Lines.s:171` | **Proto:** `PROCEDURE DoLine(newPt: Point);`<br>.PROC DoLine,1 .REF DrawLine,PutLine,SetSize PROCEDURE DoLine(newPt: Point); { called by StdLine and StdPoly frame } Called during boot. |
| **`DOLINE_NO`** | `0x009772` | `0x013EE2` | `Lines.s:194`<br>`Lines.s:189` | CHECK IF WE ARE SAVING FOR A POLYGON |
| **`DOLINE_NOTRGN`** | `0x0097AC` | `0x013F1C` | `Lines.s:221`<br>`Lines.s:215` | — |
| **`DOMAIN`** | `0x00A410` | `0x014B80` | `BitBlt.s:340`<br>`BitBlt.s:248` | — |
| **`DONE`** | `0x00B7C6` | `0x015F36` | `Angles.s:35`<br>`Angles.s:40` | — |
| **`DONE1`** | `0x00C3BE` | `0x016B2E` | `SeekRgn.s:195`<br>`SeekRgn.s:173` | DONE1 Called during boot. |
| **`DONESLAB`** | `0x0086C2` | `0x012DF8` | `Util.s:777`<br>`Util.s:531` | SET UP LEFTMASK AND RIGHTMASK: (A0 already points to MaskTab) CALC WORDCOUNT, DSTPTR, MASKPTR, AND TAKE CASE JUMP DONESLAB Called during boot. |
| **`DORECT`** | `0x00A050` | `0x0147C0` | `Rects.s:374`<br>`Rects.s:303` | DORECT Called during boot. |
| **`DoRgnOp`** | `0x00BFEE` | `0x01675E` | `Regions.s:807` | **Proto:** `PROCEDURE DoRgnOp(srcRgnA,srcRgnB,dstRgn: RgnHandle);`<br>PROCEDURE DoRgnOp(srcRgnA,srcRgnB,dstRgn: RgnHandle); Computes the Intersection, Difference, Union, or Xor of two regions. enter with op in D0. op = 0: SectScan 2: DIFF A-B 4: UNION 6: XOR A6 OFFSETS ... |
| **`DORGNOP`** | `0x00BFEE` | `0x01675E` | `Regions.s:661` | **Proto:** `PROCEDURE DoRgnOp(srcRgnA,srcRgnB,dstRgn: RgnHandle);`<br>PROCEDURE DoRgnOp(srcRgnA,srcRgnB,dstRgn: RgnHandle); Computes the Intersection, Difference, Union, or Xor of two regions. Enter with op in D0: op = 0: SectScan 2: DIFF A-B 4: UNION 6: XOR |
| **`DOSLAB`** | `0x00B610` | `0x015D80` | `DrawArc.s:972`<br>`DrawArc.s:724` | SOLID OVAL: DRAW ONE SLAB BETWEEN LEFT AND RIGHT EDGES OF OUTER OVAL Called during boot. |
| **`DOSLAB_SKIP`** | `0x00B612` | `0x015D82` | `DrawArc.s:974`<br>`DrawArc.s:731` | Bump pattern index, dstPtr, line endpoints to next scanline Called by: NOMASK_NO, SARC, ACUTE1_SKIP_2, HOVAL |
| **`DOSLANT`** | `0x009476` | `0x013BE6` | `DrawText.s:813`<br>`DrawText.s:710` | — |
| **`DOUBLE`** | `0x0084F2` | `0x012C28` | `Util.s:416`<br>`Util.s:269` | STRETCHED BY TWO: DOUBLE EACH BIT HORIZONTALLY AND VERTICALLY |
| **`DoubleNibbleTbl`** | — | `0x012C76` | `Util.s:317` | DoubleNibbleTbl / PATEXPAND_DONE_CONT_2: 16-entry x 1-byte nibble-doubling and nibble-thinning tables for PatExpand's bold/halftone variants. Indexed by D0 = nibble value 0..15. DoubleNibbleTbl (DOUBL... |
| **`DOWN`** | `0x00C33A` | `0x016AAA` | `SeekRgn.s:96`<br>`SeekRgn.s:86` | WHILE DESIRED VERT >= NEXTV DO BUMP DOWN. Called during boot. |
| **`DOWN1`** | `0x009596` | `0x013D06` | `DrawText.s:973`<br>`DrawText.s:856` | Bold BUF2 down enough for shadow. |
| **`DOWN2`** | `0x0095A0` | `0x013D10` | `DrawText.s:981`<br>`DrawText.s:860` | Bold BUF2 down enough for shadow. |
| **`DOWN2_CONT`** | `0x0095F2` | `0x013D62` | `DrawText.s:1015`<br>`DrawText.s:890` | Alter srcBits to use BUF2 Push params and call StretchBits to transfer shadow to screen |
| **`DPutPicByte`** | `0x00E2A4` | `0x018A30` | `Pictures.s:1672` | DPutPicByte -- aDD TO THEPIC. D Put Pic Byte Called by: FONTOK, COUNTOK, FACEOK, StdRRect, StdPoly (and 14 more) |
| **`DPUTPICBYTE`** | `0x00E2A4` | `0x018A30` | `Pictures.s:1228` | Helpers to push N bytes onto the picture stream via PutPicData. DPUTPICBYTE accepts byte in D0; PUTPICBYTE/WORD/LONG/PAT/RECT accept the value(s) on the stack at +4(SP) and pop them after. Called by: ... |
| **`DrawArc`** | `0x00B020` | `0x015790` | `DrawArc.s:27` | **Proto:** `PROCEDURE DrawArc(dstRect: Rect;`<br>--> DRAWARC.TEXT Routine to draw solid or hollow Ovals, RoundRects or Arcs. OFFSETS IN AN OVAL STATE RECORD: .PROC DrawArc,8 .REF InitOval,BumpOval,SlopeFromAngle .REF RSect,ShieldCursor,ShowCursor,Tr... |
| **`DRAWARC`** | `0x00B020` | `0x015790` | `DrawArc.s:24` | **Proto:** `PROCEDURE DrawArc(dstRect: Rect;`<br>--> DRAWARC.TEXT Routine to draw solid or hollow Ovals, RoundRects or Arcs. .PROC DrawArc,8 .REF InitOval,BumpOval,SlopeFromAngle .REF RSect,ShieldCursor,ShowCursor,TrimRect .REF InitRgn,SeekRgn,PatEx... |
| **`DRAWARC_DONE`** | `0x00B63A` | `0x015DAA` | `DrawArc.s:992`<br>`DrawArc.s:748` | DRAWARC_DONE -- show cursor and unwind |
| **`DRAWARC_GOHOME`** | `0x00B642` | `0x015DB2` | `DrawArc.s:995`<br>`DrawArc.s:756` | DRAWARC_GOHOME -- restore stack and return to caller Called by: DRAWARC, NOCOLOR, YESFLAG, YESFLAG_NO |
| **`DRAWARC_GOHOME_CONT`** | `0x00B654` | `0x015DC4` | `DrawArc.s:1009`<br>`DrawArc.s:768` | LOCAL ROUTINE TO UPDATE THE MASK BUFFER BASED ON WHICH REGIONS ARE RECTANGULAR Called during boot. |
| **`DRAWARC_GOHOME_CONT_2`** | `0x00B662` | `0x015DD2` | `DrawArc.s:1019`<br>`DrawArc.s:778` | DRAWARC_GOHOME_CONT_2 - indexed branch table for DrawArc region masking modes |
| **`DRAWARC_GOHOME_CONT_3`** | `0x00B66A` | `0x015DDA` | `DrawArc.s:1026`<br>`DrawArc.s:785` | ONLY REGION A IS NON RECTANGULAR. UPDATE IT AND USE IT AS THE MASK |
| **`DRAWARC_NEXTROW`** | `0x00B41C` | `0x015B8C` | `DrawArc.s:677`<br>`DrawArc.s:498` | BUMP OVAL STATE RECORDS UNLESS VERT IS BETWEEN SKIPTOP AND SKIPBOT Called during boot. |
| **`DrawChar`** | `0x008C6E` | `0x0133A4` | `Text.s:315` | **Proto:** `PROCEDURE DrawChar(ch: CHAR);`<br>PROCEDURE DrawChar(ch: CHAR); Called during boot. |
| **`DRAWCHAR`** | `0x008C6E` | `0x0133A4` | `Text.s:278` | **Proto:** `PROCEDURE DrawChar(ch: CHAR);`<br>PROCEDURE DrawChar(ch: CHAR); Called during boot. |
| **`DrawLine`** | `0x00984C` | `0x013FBC` | `DrawLine.s:22` | **Proto:** `PROCEDURE DRAWLINE(P1,P2: POINT);`<br>--> DRAWLINE.TEXT .PROC DrawLine .REF RgnBlt,RSect,ShieldCursor,ShowCursor,TrimRect .REF InitRgn,SeekRgn,PatExpand,ColorMap .REF XorSlab,DrawSlab,SlabMode,FastSlabMode,MaskTab PROCEDURE DRAWLINE(P1,P2... |
| **`DRAWLINE`** | `0x00984C` | `0x013FBC` | `DrawLine.s:24` | **Proto:** `PROCEDURE DRAWLINE(P1,P2: POINT);`<br>--> DRAWLINE.TEXT .PROC DrawLine .REF RgnBlt,RSect,ShieldCursor,ShowCursor,TrimRect .REF InitRgn,SeekRgn,PatExpand,ColorMap .REF XorSlab,DrawSlab,SlabMode,FastSlabMode,MaskTab PROCEDURE DRAWLINE(P1,P2... |
| **`DRAWLINE_ABLOOP`** | `0x009C6E` | `0x0143DE` | `DrawLine.s:675`<br>`DrawLine.s:558` | — |
| **`DRAWLINE_CKPAT`** | `0x00991E` | `0x01408E` | `DrawLine.s:170`<br>`DrawLine.s:123` | CHECK FOR BOTH VISRGN AND CLIPRGN RECTANGULAR If only visRgn is non-rectangular, then check if its intersection with minrect would be rectangular. IF TrimRect(visRgn,minRect) then treat as rectangular... |
| **`DRAWLINE_CLRMASK`** | `0x009A90` | `0x014200` | `DrawLine.s:421`<br>`DrawLine.s:335` | TOPOK CALC BUFLEFT IF FASTFLAG, THEN SKIP REGION SETUP CALC BUFSIZE ALLOCATE AND CLEAR A SCANLINE BUFFER FOR THE COMPOSITE MASK |
| **`DRAWLINE_CLRMASK_CONT`** | `0x009AD6` | `0x014246` | `DrawLine.s:451`<br>`DrawLine.s:362` | ARECT DRAWLINE_CLRMASK_CONT -- iNIT STATE, ALLOC BUFFER. |
| **`DRAWLINE_CLRMASK_EXIT`** | `0x009AE6` | `0x014256` | `DrawLine.s:461`<br>`DrawLine.s:371` | DRAWLINE_CLRMASK_EXIT |
| **`DRAWLINE_CLRMASK_LOOP`** | `0x009B62` | `0x0142D2` | `DrawLine.s:529`<br>`DrawLine.s:423` | TAKE FAST OR SLOW OUTER CONTROL LOOP FOR SLANTED LINES: |
| **`DRAWLINE_CLRMASK_OK`** | `0x009AB8` | `0x014228` | `DrawLine.s:439`<br>`DrawLine.s:352` | INIT STATE RECORDS AND ALLOCATE BUFFERS FOR EACH NON-RECTANGULAR REGION |
| **`DRAWLINE_CLRMASK_SKIP`** | `0x009B04` | `0x014274` | `DrawLine.s:477`<br>`DrawLine.s:384` | BRECT IF BOTH REGIONS ARE RECTANGULAR, THEN DRAW MINRECT INTO MASK BUFFER |
| **`DRAWLINE_DONE`** | `0x009C08` | `0x014378` | `DrawLine.s:596`<br>`DrawLine.s:486` | Called by: NOTFAST, DRAWLINE_CLRMASK_LOOP, ENDCLR, ENDTOGL, ENDSET (and 3 more) |
| **`DRAWLINE_GOHOME`** | `0x009C10` | `0x014380` | `DrawLine.s:599`<br>`DrawLine.s:489` | — |
| **`DRAWLINE_GOHOME_CONT`** | `0x009C20` | `0x014390` | `DrawLine.s:612`<br>`DrawLine.s:501` | LOCAL ROUTINE TO UPDATE THE MASK BUFFER BASED ON WHICH REGIONS ARE RECTANGULAR |
| **`DRAWLINE_GOHOME_CONT_2`** | `0x009C30` | `0x0143A0` | `DrawLine.s:622`<br>`DrawLine.s:515` | DRAWLINE_GOHOME_CONT_2 - indexed branch table for DrawLine region masking modes |
| **`DRAWLINE_GOHOME_CONT_3`** | `0x009C38` | `0x0143A8` | `DrawLine.s:630`<br>`DrawLine.s:522` | ONLY REGION A IS NON RECTANGULAR. UPDATE IT AND USE IT AS THE MASK |
| **`DRAWLINE_JSRSEEK`** | `0x009C3C` | `0x0143AC` | `DrawLine.s:641`<br>`DrawLine.s:532` | LOCAL ROUTINE TO UPDATE THE MASK BUFFER BASED ON WHICH REGIONS ARE RECTANGULAR |
| **`DRAWLINE_JSRSEEK_CONT`** | `0x009C46` | `0x0143B6` | `DrawLine.s:644`<br>`DrawLine.s:535` | — |
| **`DRAWLINE_JSRSEEK_CONT_2`** | `0x009C48` | `0x0143B8` | `DrawLine.s:651`<br>`DrawLine.s:541` | ONLY REGION B IS NON RECTANGULAR. UPDATE IT AND USE IT AS THE MASK |
| **`DRAWLINE_JSRSEEK_CONT_3`** | `0x009C4E` | `0x0143BE` | `DrawLine.s:663`<br>`DrawLine.s:549` | REGIONS A AND B ARE NON-RECTANGULAR. UPDATE EACH, THEN FORM INTERSECTION IN THE MASK BUFFER. |
| **`DRAWLINE_NOCOLOR`** | `0x009892` | `0x014002` | `DrawLine.s:87`<br>`DrawLine.s:52` | Check for color filtering. Alter mode and pattern accordingly. |
| **`DRAWLINE_YESFLAG`** | `0x009936` | `0x0140A6` | `DrawLine.s:184`<br>`DrawLine.s:136` | CHECK FOR BLACK OR WHITE PATTERN |
| **`DRAWLINE_YESFLAG_CONT`** | `0x00994E` | `0x0140BE` | `DrawLine.s:201`<br>`DrawLine.s:156` | fast case: map mode into black,xor,white, or do-nothing DRAWLINE_YESFLAG_CONT - indexed branch table for DrawLine region scan modes |
| **`DRAWLINE_YESFLAG_NO`** | `0x009956` | `0x0140C6` | `DrawLine.s:205`<br>`DrawLine.s:162` | DRAWLINE_YESFLAG_NO - DrawLine entry point when pen mode skip-flag is clear |
| **`DrawPicture`** | `0x00DAEC` | `0x018268` | `Pictures.s:387` | **Proto:** `PROCEDURE DrawPicture(myPicture: PicHandle; dstRect: Rect);`<br>_DisposHandle ;discard it .PROC DrawPicture,2 .REF PicItem,NewRgn PROCEDURE DrawPicture(myPicture: PicHandle; dstRect: Rect); |
| **`DRAWPICTURE`** | `0x00DAEC` | `0x018268` | `Pictures.s:318` | **Proto:** `PROCEDURE DrawPicture(myPicture: PicHandle; dstRect: Rect);`<br>PROCEDURE DrawPicture(myPicture: PicHandle; dstRect: Rect); Plays back a picture into the current grafPort. Sets up scale numerator/denominator from dstRect/picFrame, snapshots the current grafPort to... |
| **`DRAWPICTURE_GOHOME`** | `0x00DC0C` | `0x018388` | `Pictures.s:575`<br>`Pictures.s:428` | _DisposHandle ;DISCARD IT |
| **`DRAWPICTURE_LOOP`** | `0x00DB62` | `0x0182DE` | `Pictures.s:474`<br>`Pictures.s:354` | PRESERVE THE CURRENT GRAFPORT IN SAVEPORT |
| **`DrawPoly`** | `0x00BBA0` | `0x016310` | `Polygons.s:420` | **Proto:** `PROCEDURE DrawPoly(poly: PolyHandle; mode: INTEGER; VAR pat: Pattern);`<br>.PROC DrawPoly,3 .REF OpenRgn,FrPoly,DoLine,NewRgn,CloseRgn,DrawRgn PROCEDURE DrawPoly(poly: PolyHandle; mode: INTEGER; VAR pat: Pattern); A6 OFFSETS OF PARAMS AND LOCALS AFTER LINK: PARAMSIZE .EQU 10... |
| **`DRAWPOLY`** | `0x00BBA0` | `0x016310` | `Polygons.s:357` | **Proto:** `PROCEDURE DrawPoly(poly: PolyHandle; mode: INTEGER; VAR pat: Pattern);`<br>PROCEDURE DrawPoly(poly: PolyHandle; mode: INTEGER; VAR pat: Pattern); A6 offsets of params and locals after LINK: PARAMSIZE = 10 POLY      = PARAMSIZE+8-4  (LONG, PolyHandle) MODE      = POLY-2      ... |
| **`DRAWPOLY_DONE`** | `0x00BBE8` | `0x016358` | `Polygons.s:451`<br>`Polygons.s:381` | _DisposHandle ;DISCARD IT |
| **`DrawRect`** | `0x009F58` | `0x0146C8` | `Rects.s:249` | **Proto:** `PROCEDURE DrawRect(r: Rect; mode: INTEGER; pat: Pattern);`<br>.PROC DrawRect,3 .REF RgnBlt PROCEDURE DrawRect(r: Rect; mode: INTEGER; pat: Pattern); Rectangle is given in local coordinates. A6 OFFSETS OF PARAMS AND LOCALS AFTER LINK: PARAMSIZE .EQU 10 ;TOTAL BYT... |
| **`DRAWRECT`** | `0x009F58` | `0x0146C8` | `Rects.s:207` | **Proto:** `PROCEDURE DrawRect(rect: Rect; mode: INTEGER; pat: Pattern);`<br>.PROC DrawRect,3 .REF RgnBlt PROCEDURE DrawRect(rect: Rect; mode: INTEGER; pat: Pattern); Called by StdRect after PushVerb. |
| **`DRAWRECT_EXIT`** | `0x009F8A` | `0x0146FA` | `Rects.s:270`<br>`Rects.s:223` | — |
| **`DrawRgn`** | `0x00BCA2` | `0x016412` | `Regions.s:164` | **Proto:** `PROCEDURE DrawRgn(rgn: RgnHandle; mode: INTEGER; pat: Pattern);`<br>.PROC DrawRgn,3 .REF RgnBlt PROCEDURE DrawRgn(rgn: RgnHandle; mode: INTEGER; pat: Pattern); A6 OFFSETS OF PARAMS AFTER LINK: PARAMSIZE .EQU 10 RGN .EQU PARAMSIZE+8-4 ;LONG, RGNHANDLE MODE .EQU RGN-2 ;... |
| **`DRAWRGN`** | `0x00BCA2` | `0x016412` | `Regions.s:140` | **Proto:** `PROCEDURE DrawRgn(rgn: RgnHandle; mode: INTEGER; pat: Pattern);`<br>PROCEDURE DrawRgn(rgn: RgnHandle; mode: INTEGER; pat: Pattern); A6 offsets of params after LINK: PARAMSIZE = 10 RGN       = PARAMSIZE+8-4  (LONG, RgnHandle) MODE      = RGN-2          (WORD) PAT      ... |
| **`DRAWRGN_EXIT`** | `0x00BCD4` | `0x016444` | `Regions.s:185`<br>`Regions.s:156` | — |
| **`DrawSlab`** | `0x008686` | `0x012DBC` | `Util.s:735` | **Proto:** `LOCAL PROCEDURE DRAWSLAB`<br>LOCAL ROUTINE TO GET NEXT HEX DIGIT AND CONVERT ASCII TO BINARY .PROC DrawSlab,0 .DEF SlabMode,FastSlabMode .REF MaskTab LOCAL PROCEDURE DRAWSLAB INPUTS: D0: scratch A0: MASKTAB D1: left A1: DSTLEFT, ... |
| **`DRAWSLAB`** | `0x008686` | `0x012DBC` | `Util.s:502` | DrawSlab - draw a horizontal slab via mode-specific scan routine Inputs: D1 = left, D2 = right, D6 = pattern A0 = MaskTab base (used relative; +0x20 = right masks) A1 = dstPtr (row start), A2 = maskPt... |
| **`DRAWSLAB_END8`** | `0x0086C4` | `0x012DFA` | `Util.s:800`<br>`Util.s:540` | **Regs:** `Entry: A1=dstPtr, A2=maskPtr, D1=leftMask, D2=wordCnt,`<br>INTERFACE TO EACH SCAN LINE ROUTINE: ENTER WITH Z-FLAG SET IF ALL IN ONE WORD INPUTS: A1: DSTPTR A2: MASKPTR D1: LEFTMASK D2: WORDCNT D3: RIGHTMASK D6: PATTERN CLOBBERS: D0,D1,D2,A1,A2 MODE 8 OR 12: P... |
| **`DRAWSLAB_LEFTOK`** | `0x008690` | `0x012DC6` | `Util.s:739`<br>`Util.s:506` | — |
| **`DRAWSLAB_RIGHTOK`** | `0x00869A` | `0x012DD0` | `Util.s:743`<br>`Util.s:510` | — |
| **`DrawString`** | `0x008CAE` | `0x0133E4` | `Text.s:386` | **Proto:** `PROCEDURE DrawString(s: Str255);`<br>PROCEDURE DrawString(s: Str255); Called during boot. |
| **`DRAWSTRING`** | `0x008CAE` | `0x0133E4` | `Text.s:343` | **Proto:** `PROCEDURE DrawString(s: Str255);`<br>PROCEDURE DrawString(s: Str255); Called during boot. |
| **`DrawText`** | `0x008CC0` | `0x0133F6` | `Text.s:403` | **Proto:** `PROCEDURE DrawText(textBuf: WordPtr; start,count: INTEGER);`<br>PROCEDURE DrawText(textBuf: WordPtr; start,count: INTEGER); Called during boot. |
| **`DRAWTEXT`** | `0x008CC0` | `0x0133F6` | `Text.s:356` | **Proto:** `PROCEDURE DrawText(textBuf: WordPtr; start,count: INTEGER);`<br>PROCEDURE DrawText(textBuf: WordPtr; start,count: INTEGER); Called during boot. |
| **`DRAWTEXT_SHARE`** | `0x008CD4` | `0x01340A` | `Text.s:413`<br>`Text.s:363` | — |
| **`DRAWVERB_TBL`** | — | `0x0183E0` | `Pictures.s:480` | Drawing opcode: split into noun (hi nibble) + verb (lo nibble) + sameFlag (bit 3). Drawing-opcode noun-dispatch table: 17 word offsets relative to DRAWVERB_TBL, indexed by (opcode>>4)*2. Out-of-range ... |
| **`DrText`** | `0x008F26` | `0x013696` | `DrawText.s:21` | **Proto:** `PROCEDURE DrText(count: INTEGER; textAddr: Ptr; numer,denom: Point);`<br>--> DRAWTEXT.TEXT QuickDraw Character Generator Completely reworked 29 Apr 85 by Bill Atkinson to get 50% speed up. Takes advantage of optional height table at end of font. .PROC DrText,4 .REF RightMa... |
| **`DRTEXT`** | `0x008F26` | `0x013696` | `DrawText.s:62` | **Proto:** `PROCEDURE DrText(count: INTEGER; textAddr: Ptr; numer,denom: Point);`<br>--> DRAWTEXT.TEXT QuickDraw Character Generator Completely reworked 29 Apr 85 by Bill Atkinson to get 50% speed up. Takes advantage of optional height table at end of font. .PROC DrText,4 .REF RightMa... |
| **`DRTEXT_NOCOLOR`** | `0x0090A4` | `0x013814` | `DrawText.s:247`<br>`DrawText.s:200` | — |
| **`DRTEXT_NOTFAST`** | `0x009122` | `0x013892` | `DrawText.s:307`<br>`DrawText.s:256` | Slow case: Setup for an off-screen buffer. Calc bufLeft: (word-align to avoid shift) Called during boot. |
| **`DRTEXT_NOTFAST_CONT`** | `0x009168` | `0x0138D8` | `DrawText.s:337`<br>`DrawText.s:285` | Calculate buffer size Calculate total stack requirements for off-screen buffers. |
| **`DRTEXT_NOTFAST_NO`** | `0x0091BC` | `0x01392C` | `DrawText.s:375`<br>`DrawText.s:321` | If stack is too small to allocate buffer(s), then recursively call DrText with the left half and the right half of the text string. _StackAvail ;Get StackAvail IN D0 DRTEXT_NOTFAST_NO Called during bo... |
| **`DT_mCRSRCore`** | `0x001C8A` | — | `CrsrCore.s:24` | Cursor core -- cursor drawing, ScrnAddress/ScrnSize/ScrnBitMap, CrsrVBLTask, PinRect Apple source: CrsrCore.a (System 7.1: QuickDraw/Classic/CrsrCore.a; the SE link map calls the module CRSRCORE). The... |
| **`DT_mMaskTab`** | `0x008438` | — | `Util.s:319` | RTS DT_m Mask Tab |
| **`DT_MMASKTAB_CONT`** | `0x008458` | — | `Util.s:326` | — |
| **`DT_MMASKTAB_CONT_2`** | `0x008478` | `0x012BAE` | `Util.s:333`<br>`Util.s:209` | — |
| **`DV`** | `0x008BDC` | `0x013312` | `Text.s:213`<br>`Text.s:182` | DV |
| **`DVPOS`** | `0x009DBA` | `0x01452A` | `PutLine.s:50`<br>`PutLine.s:41` | — |
| **`DVPOS_NO`** | `0x009DE8` | `0x014558` | `PutLine.s:76`<br>`PutLine.s:65` | GROW POINT BUFFER AS NECESSARY TO HOLD BYTESNEEDED NOGROW |
| **`DVPOS_OK`** | `0x009DC0` | `0x014530` | `PutLine.s:54`<br>`PutLine.s:45` | — |
| **`EIGHT`** | `0x00D7C4` | `0x017F40` | `Stretch.s:1229`<br>`Stretch.s:1054` | RTS ;ALL DONE SCALE UP BY EIGHT USING TABLE LOOKUP |
| **`EIGHT_CONT`** | `0x00D7E2` | `0x017F5E` | `Stretch.s:1246`<br>`Stretch.s:1072` | EIGHT_CONT - indexed branch table for stretch pixel replication |
| **`EIGHT_CONT_2`** | `0x00D822` | — | `Stretch.s:1259` | — |
| **`EIGHTS`** | `0x00D844` | `0x017FC0` | `Stretch.s:1302`<br>`Stretch.s:1125` | SCALE UP BY ANY MULTIPLE OF 8 GREATER THAN 2 |
| **`EIGHTS1`** | `0x00D84C` | `0x017FC8` | `Stretch.s:1306`<br>`Stretch.s:1129` | — |
| **`EIGHTS2`** | `0x00D854` | `0x017FD0` | `Stretch.s:1311`<br>`Stretch.s:1134` | — |
| **`EIGHTS3`** | `0x00D858` | `0x017FD4` | `Stretch.s:1314`<br>`Stretch.s:1137` | — |
| **`EIGHTS3_CONT`** | `0x00D864` | — | `Stretch.s:1325` | EIGHTS3_CONT |
| **`EMPTY`** | `0x00BACE` | `0x01623E` | `Polygons.s:255`<br>`Polygons.s:221` | TRIM THEPOLY TO FINAL SIZE, SHOW PEN AND QUIT |
| **`EmptyRect`** | `0x00A0AA` | `0x01481A` | `Rects.s:458` | **Proto:** `FUNCTION EmptyRect(r: Rect): BOOLEAN;`<br>.PROC EmptyRect FUNCTION EmptyRect(r: Rect): BOOLEAN; CLOBBERS D0,D1,A0,A1. Called during boot (7,391 times in 30s trace). |
| **`EMPTYRECT`** | `0x00A0AA` | `0x01481A` | `Rects.s:376` | **Proto:** `FUNCTION EmptyRect(r: Rect): BOOLEAN;`<br>.PROC EmptyRect FUNCTION EmptyRect(r: Rect): BOOLEAN; CLOBBERS D0,D1,A0,A1. Called during boot (7,391 times in 30s trace). |
| **`EMPTYRECT_DONE`** | `0x00A0C2` | `0x014832` | `Rects.s:477`<br>`Rects.s:394` | EMPTYRECT_EMPTY Called during boot (7,383 times in 30s trace). |
| **`EMPTYRECT_EMPTY`** | `0x00A0BE` | `0x01482E` | `Rects.s:475`<br>`Rects.s:392` | EMPTYRECT_EMPTY Called during boot (7,383 times in 30s trace). |
| **`EmptyRgn`** | `0x00BF90` | `0x016700` | `Regions.s:684` | **Proto:** `FUNCTION EmptyRgn(rgn: RgnHandle): BOOLEAN;`<br>.FUNC EmptyRgn,1 .REF EmptyRect FUNCTION EmptyRgn(rgn: RgnHandle): BOOLEAN; Called during boot (7,389 times in 30s trace). |
| **`EMPTYRGN`** | `0x00BF90` | `0x016700` | `Regions.s:569` | **Proto:** `FUNCTION EmptyRgn(rgn: RgnHandle): BOOLEAN;`<br>FUNCTION EmptyRgn(rgn: RgnHandle): BOOLEAN; |
| **`END0`** | `0x00A4C6` | `0x014C36` | `BitBlt.s:495`<br>`BitBlt.s:394` | MODE 0 OR 4: SRC --> DST Called during boot. |
| **`END1`** | `0x00A546` | `0x014CB6` | `BitBlt.s:590`<br>`BitBlt.s:484` | MODE 1 OR 5: SRC OR DST --> DST Called during boot. |
| **`END10`** | `0x0086F0` | `0x012E26` | `Util.s:840`<br>`Util.s:570` | MODE 10 OR 14: PATTERN XOR DST --> DST |
| **`END11`** | `0x008702` | `0x012E38` | `Util.s:858`<br>`Util.s:583` | MODE 11 OR 15: PATTERN BIC DST --> DST |
| **`END1_LOOP`** | `0x00A548` | `0x014CB8` | `BitBlt.s:592`<br>`BitBlt.s:486` | MODE 1 OR 5: SRC OR DST --> DST Called during boot. |
| **`END2`** | `0x00A564` | `0x014CD4` | `BitBlt.s:611`<br>`BitBlt.s:504` | MODE 2 OR 6: SRC XOR DST --> DST Called during boot. |
| **`END2_LOOP`** | `0x00A566` | `0x014CD6` | `BitBlt.s:613`<br>`BitBlt.s:506` | MODE 2 OR 6: SRC XOR DST --> DST Called during boot. |
| **`END3`** | `0x00A582` | `0x014CF2` | `BitBlt.s:632`<br>`BitBlt.s:524` | MODE 3 OR 7: SRC BIC DST --> DST Called during boot. |
| **`END3_LOOP`** | `0x00A584` | `0x014CF4` | `BitBlt.s:634`<br>`BitBlt.s:526` | MODE 3 OR 7: SRC BIC DST --> DST Called during boot. |
| **`END8`** | `0x00A5F8` | `0x014D68` | `BitBlt.s:706`<br>`BitBlt.s:595` | — |
| **`END9`** | `0x0086DE` | `0x012E14` | `Util.s:822`<br>`Util.s:557` | MODE 9 OR 13: PATTERN OR DST --> DST |
| **`ENDCLR`** | `0x009CCC` | `0x01443C` | `DrawLine.s:736`<br>`DrawLine.s:614` | — |
| **`ENDCOPY`** | `0x00CFD4` | `0x017750` | `Bitmaps.s:1075`<br>`Bitmaps.s:904` | — |
| **`ENDFILL`** | `0x00CFFA` | `0x017776` | `Bitmaps.s:1102`<br>`Bitmaps.s:930` | — |
| **`ENDFILL_EXIT`** | `0x00D000` | `0x01777C` | `Bitmaps.s:1106`<br>`Bitmaps.s:934` | — |
| **`ENDFILL_EXIT_2`** | `0x00D014` | `0x017790` | `Bitmaps.s:1114`<br>`Bitmaps.s:942` | — |
| **`ENDHEX`** | `0x00862E` | `0x012D64` | `Util.s:619`<br>`Util.s:438` | — |
| **`ENDSCAN`** | `0x00C7E8` | `0x016FDA` | `PackRgn.s:96`<br>`PackRgn.s:97` | ENDSCAN Called during boot (7,410 times in 30s trace). |
| **`ENDSET`** | `0x009D1C` | `0x01448C` | `DrawLine.s:806`<br>`DrawLine.s:680` | — |
| **`ENDTOGL`** | `0x009CF4` | `0x014464` | `DrawLine.s:770`<br>`DrawLine.s:646` | — |
| **`ENDWORD`** | `0x00C3BA` | `0x016B2A` | `SeekRgn.s:186`<br>`SeekRgn.s:166` | — |
| **`EQUAL`** | `0x00C68C` | `0x016DFC` | `RgnOp.s:526`<br>`RgnOp.s:450` | EQUAL Called during boot (264,977 times in 30s trace). |
| **`EqualPt`** | `0x008AAA` | `0x0131E0` | `GrafAsm.s:548` | **Proto:** `FUNCTION EqualPt(pt1,pt2: Point): BOOLEAN;`<br>.PROC EqualPt FUNCTION EqualPt(pt1,pt2: Point): BOOLEAN; CLOBBERS D0,A0. |
| **`EQUALPT`** | `0x008AAA` | `0x0131E0` | `GrafAsm.s:522` | **Proto:** `FUNCTION EqualPt(pt1,pt2: Point): BOOLEAN;`<br>FUNCTION EqualPt(pt1,pt2: Point): BOOLEAN; { return TRUE if pt1=pt2 } |
| **`EqualRect`** | `0x00A090` | `0x014800` | `Rects.s:429` | **Proto:** `FUNCTION EqualRect(rect1,rect2: Rect): BOOLEAN;`<br>.PROC EqualRect FUNCTION EqualRect(rect1,rect2: Rect): BOOLEAN; CLOBBERS D0,A0,A1. |
| **`EQUALRECT`** | `0x00A090` | `0x014800` | `Rects.s:349` | **Proto:** `FUNCTION EqualRect(rect1,rect2: Rect): BOOLEAN;`<br>.PROC EqualRect FUNCTION EqualRect(rect1,rect2: Rect): BOOLEAN; { return TRUE if rect1 = rect2 } |
| **`EQUALRECT_DONE`** | `0x00A0A6` | `0x014816` | `Rects.s:446`<br>`Rects.s:365` | — |
| **`EqualRgn`** | `0x00BFA0` | `0x016710` | `Regions.s:700` | **Proto:** `FUNCTION EqualRgn(rgnA,rgnB: RgnHandle): BOOLEAN;`<br>.FUNC EqualRgn,2 FUNCTION EqualRgn(rgnA,rgnB: RgnHandle): BOOLEAN; RETURNS TRUE IF RGNA AND RGNB DESCRIBE THE SAME AREA Called during boot (10,214 times in 30s trace). |
| **`EQUALRGN`** | `0x00BFA0` | `0x016710` | `Regions.s:582` | **Proto:** `FUNCTION EqualRgn(rgnA, rgnB: RgnHandle): BOOLEAN;`<br>FUNCTION EqualRgn(rgnA, rgnB: RgnHandle): BOOLEAN; Returns TRUE if RgnA and RgnB describe the same area. |
| **`EQUALRGN_DONE`** | `0x00BFD4` | `0x016744` | `Regions.s:733`<br>`Regions.s:613` | — |
| **`EQUALRGN_LOOP`** | `0x00BFB8` | `0x016728` | `Regions.s:711`<br>`Regions.s:593` | — |
| **`EQUALRGN_LOOP2`** | `0x00BFC6` | `0x016736` | `Regions.s:717`<br>`Regions.s:599` | — |
| **`EQUALRGN_LOOP2_CONT`** | `0x00BFD2` | `0x016742` | `Regions.s:731`<br>`Regions.s:611` | EQUALRGN_LOOP2_CONT Called during boot (10,210 times in 30s trace). |
| **`EQUALRGN_LOOP2_OK`** | `0x00BFCE` | `0x01673E` | `Regions.s:722`<br>`Regions.s:604` | — |
| **`ERASE1`** | `0x00E3A4` | `0x018B30` | `Pictures.s:1869`<br>`Pictures.s:1354` | ERASE1 |
| **`EraseArc`** | `0x00AFDE` | `0x01574E` | `Arcs.s:107` | **Proto:** `PROCEDURE EraseArc(* r: Rect; startAngle,arcAngle: INTEGER *);`<br>PROCEDURE EraseArc(* r: Rect; startAngle,arcAngle: INTEGER *); |
| **`ERASEARC`** | `0x00AFDE` | `0x01574E` | `Arcs.s:103` | **Proto:** `PROCEDURE EraseArc(* r: Rect; startAngle,arcAngle: INTEGER *);`<br>PROCEDURE EraseArc(* r: Rect; startAngle,arcAngle: INTEGER *); |
| **`EraseOval`** | `0x00ADDC` | `0x01554C` | `Ovals.s:119` | **Proto:** `PROCEDURE EraseOval(* r: Rect *);`<br>PROCEDURE EraseOval(* r: Rect *); |
| **`ERASEOVAL`** | `0x00ADDC` | `0x01554C` | `Ovals.s:106` | **Proto:** `PROCEDURE EraseOval(* r: Rect *);`<br>PROCEDURE EraseOval(* r: Rect *); |
| **`ErasePoly`** | `0x00BA00` | `0x016170` | `Polygons.s:108` | **Proto:** `PROCEDURE ErasePoly(* poly: PolyHandle *);`<br>PROCEDURE ErasePoly(* poly: PolyHandle *); |
| **`ERASEPOLY`** | `0x00BA00` | `0x016170` | `Polygons.s:88` | **Proto:** `PROCEDURE ErasePoly(* poly: PolyHandle *);`<br>PROCEDURE ErasePoly(* poly: PolyHandle *); |
| **`EraseRect`** | `0x009F30` | `0x0146A0` | `Rects.s:191` | **Proto:** `PROCEDURE EraseRect(r: Rect);`<br>PROCEDURE EraseRect(r: Rect); EraseRect _EraseRect ($A8A3) Called during boot. |
| **`ERASERECT`** | `0x009F30` | `0x0146A0` | `Rects.s:168` | **Proto:** `PROCEDURE EraseRect(r: Rect);`<br>PROCEDURE EraseRect(r: Rect); |
| **`EraseRgn`** | `0x00BC64` | `0x0163D4` | `Regions.s:99` | **Proto:** `PROCEDURE EraseRgn(* rgn: RgnHandle *);`<br>PROCEDURE EraseRgn(* rgn: RgnHandle *); Called during boot. |
| **`ERASERGN`** | `0x00BC64` | `0x0163D4` | `Regions.s:83` | **Proto:** `PROCEDURE EraseRgn(* rgn: RgnHandle *);`<br>PROCEDURE EraseRgn(* rgn: RgnHandle *); |
| **`EraseRoundRect`** | `0x00AD0A` | `0x01547A` | `RRects.s:115` | **Proto:** `PROCEDURE EraseRoundRect(* r: Rect; ovWd,ovHt: INTEGER *);`<br>PROCEDURE EraseRoundRect(* r: Rect; ovWd,ovHt: INTEGER *); Called during boot. |
| **`ERASEROUNDRECT`** | `0x00AD0A` | `0x01547A` | `RRects.s:115` | **Proto:** `PROCEDURE EraseRoundRect(* r: Rect; ovWd,ovHt: INTEGER *);`<br>PROCEDURE EraseRoundRect(* r: Rect; ovWd,ovHt: INTEGER *); Called during boot. |
| **`EVEN`** | `0x00BE40` | `0x0165B0` | `Regions.s:423`<br>`Regions.s:344` | COPYRGN_COPYLP Called during boot (111,099 times in 30s trace). |
| **`EVEN_EXIT`** | `0x00BE44` | `0x0165B4` | `Regions.s:425`<br>`Regions.s:346` | — |
| **`EXPAND`** | `0x00C59E` | `0x016D0E` | `RgnOp.s:293`<br>`RgnOp.s:262` | EXPAND Called during boot (14,948 times in 30s trace). |
| **`FACEOK`** | `0x008B1E` | `0x013254` | `Text.s:99`<br>`Text.s:79` | CHECK TXMODE |
| **`FALSE`** | `0x00A0A4` | `0x014814` | `Rects.s:444`<br>`Rects.s:363` | FALSE |
| **`FAST`** | `0x0090CA` | `0x01383A` | `DrawText.s:274`<br>`DrawText.s:225` | All systems go except for VisRgn not rectangular. Check if visRgn sect minRect is rectangular. IF TrimRect(visRgn,minRect) THEN take the fast way. Fast case, go directly to screen. If text is clipped ... |
| **`FAST0`** | `0x00A4B0` | `0x014C20` | `BitBlt.s:477`<br>`BitBlt.s:377` | FAST0 |
| **`FASTLINE`** | `0x009C7A` | `0x0143EA` | `DrawLine.s:688`<br>`DrawLine.s:569` | SET UP AND DRAW A FAST HORIZONTAL OR VERTICAL LINE. Called during boot. |
| **`FastSlabMode`** | `0x008770` | `0x012EA6` | `Util.s:991` | **Proto:** `PROCEDURE FastSlabMode, Call when rect clipped and pattern black.`<br>PROCEDURE FastSlabMode, Call when rect clipped and pattern black. INPUT: D2: MODE, CLOBBERED mode 0=black, 1=xor, 2=white OUTPUT: A4: MODECASE Called during boot. |
| **`FASTSLABMODE`** | `0x008770` | `0x012EA6` | `Util.s:695` | **Proto:** `PROCEDURE FastSlabMode, Call when rect clipped and pattern black.`<br>PROCEDURE FastSlabMode, Call when rect clipped and pattern black. INPUT:  D2 = MODE (clobbered): 0=black, 1=xor, 2=white OUTPUT: A4 = MODECASE |
| **`FASTSLABMODE_CONT`** | `0x008784` | — | `Util.s:1007` | FASTSLABMODE_CONT -- aLLOCATE PTBUF. Called by: OpenPoly, NewRgn, OpenRgn, INSETRGN_NOTRECT, JDONE_NO_2 (and 1 more) |
| **`FASTSLABMODE_ERR`** | `0x008792` | `0x012EC8` | `Util.s:1020`<br>`GrafAsm.s:34` | FASTSLABMODE_ERR |
| **`FASTSLABMODE_MODE_TBL`** | `0x008780` | `0x012EB6` | `Util.s:1002`<br>`Util.s:709` | FASTSLABMODE_MODE_TBL |
| **`FILL31`** | `0x00A642` | — | `BitBlt.s:766` | FILL31 Called during boot. |
| **`FILL31_CONT`** | `0x00A664` | `0x014DD4` | `BitBlt.s:790`<br>`BitBlt.s:669` | MODE 9 OR 13: PATTERN OR DST --> DST |
| **`FILL32`** | `0x00A620` | `0x014D90` | `BitBlt.s:742`<br>`BitBlt.s:629` | FILL32 Called during boot. |
| **`FillArc`** | `0x00AFE6` | `0x015756` | `Arcs.s:123` | **Proto:** `PROCEDURE FillArc(* r: Rect; startAngle,arcAngle: INTEGER; pat: Pattern *);`<br>PROCEDURE FillArc(* r: Rect; startAngle,arcAngle: INTEGER; pat: Pattern *); |
| **`FILLARC`** | `0x00AFE6` | `0x015756` | `Arcs.s:117` | **Proto:** `PROCEDURE FillArc(* r: Rect; startAngle,arcAngle: INTEGER; pat: Pattern *);`<br>PROCEDURE FillArc(* r: Rect; startAngle,arcAngle: INTEGER; pat: Pattern *); |
| **`FILLBIG`** | `0x00A608` | `0x014D78` | `BitBlt.s:719`<br>`BitBlt.s:607` | Call fillbig with wordcount in D2 (clobbered) |
| **`FILLBIG_DONE`** | `0x00A61A` | `0x014D8A` | `BitBlt.s:733`<br>`BitBlt.s:620` | FILLBIG_DONE |
| **`FILLBIG_LOOP`** | `0x00A610` | `0x014D80` | `BitBlt.s:723`<br>`BitBlt.s:611` | — |
| **`FILLED`** | `0x00A07A` | `0x0147EA` | `Rects.s:399`<br>`Rects.s:322` | LOCAL ROUTINE TO PAINT TEMPRECT, GIVEN IN LOCAL COORDS FILLED Called during boot. |
| **`FILLED_SKIP`** | `0x00A07C` | `0x0147EC` | `Rects.s:401`<br>`Rects.s:324` | — |
| **`FILLOP`** | `0x00CFA6` | `0x017722` | `Bitmaps.s:1047`<br>`Bitmaps.s:877` | FILLOP |
| **`FillOval`** | `0x00ADE4` | `0x015554` | `Ovals.s:135` | **Proto:** `PROCEDURE FillOval(* r: Rect; pat: Pattern *);`<br>PROCEDURE FillOval(* r: Rect; pat: Pattern *); |
| **`FILLOVAL`** | `0x00ADE4` | `0x015554` | `Ovals.s:120` | **Proto:** `PROCEDURE FillOval(* r: Rect; pat: Pattern *);`<br>PROCEDURE FillOval(* r: Rect; pat: Pattern *); |
| **`FillPoly`** | `0x00BA08` | `0x016178` | `Polygons.s:124` | **Proto:** `PROCEDURE FillPoly(* poly: PolyHandle; pat: Pattern *);`<br>PROCEDURE FillPoly(* poly: PolyHandle; pat: Pattern *); |
| **`FILLPOLY`** | `0x00BA08` | `0x016178` | `Polygons.s:102` | **Proto:** `PROCEDURE FillPoly(* poly: PolyHandle; pat: Pattern *);`<br>PROCEDURE FillPoly(* poly: PolyHandle; pat: Pattern *); |
| **`FillRect`** | `0x009F12` | `0x014682` | `Rects.s:138` | **Proto:** `PROCEDURE FillRect(r: Rect; pat: Pattern);`<br>.PROC FillRect,2 .DEF CallRect,FrameRect,PaintRect,EraseRect,InvertRect .REF StdRect PROCEDURE FillRect(r: Rect; pat: Pattern); Called during boot. |
| **`FILLRECT`** | `0x009F12` | `0x014682` | `Rects.s:139` | **Proto:** `PROCEDURE FillRect(r: Rect; pat: Pattern);`<br>.PROC FillRect,2 .DEF CallRect,FrameRect,PaintRect,EraseRect,InvertRect .REF StdRect PROCEDURE FillRect(r: Rect; pat: Pattern); Called during boot. |
| **`FillRgn`** | `0x00BC6C` | `0x0163DC` | `Regions.s:115` | **Proto:** `PROCEDURE FillRgn(* rgn: RgnHandle; pat: Pattern *);`<br>PROCEDURE FillRgn(* rgn: RgnHandle; pat: Pattern *); |
| **`FILLRGN`** | `0x00BC6C` | `0x0163DC` | `Regions.s:97` | **Proto:** `PROCEDURE FillRgn(* rgn: RgnHandle; pat: Pattern *);`<br>PROCEDURE FillRgn(* rgn: RgnHandle; pat: Pattern *); |
| **`FillRoundRect`** | `0x00AD12` | `0x015482` | `RRects.s:133` | **Proto:** `PROCEDURE FillRoundRect(r: Rect; ovWd,ovHt: INTEGER; pat: Pattern);`<br>PROCEDURE FillRoundRect(r: Rect; ovWd,ovHt: INTEGER; pat: Pattern); Called during boot. |
| **`FILLROUNDRECT`** | `0x00AD12` | `0x015482` | `RRects.s:131` | **Proto:** `PROCEDURE FillRoundRect(r: Rect; ovWd,ovHt: INTEGER; pat: Pattern);`<br>PROCEDURE FillRoundRect(r: Rect; ovWd,ovHt: INTEGER; pat: Pattern); Called during boot. |
| **`FONTOK`** | `0x008AFE` | `0x013234` | `Text.s:84`<br>`Text.s:65` | CHECK TXFONT CHECK TXFACE |
| **`FORE0`** | `0x0085BE` | `0x012CF4` | `Util.s:545`<br>`Util.s:377` | FORE0 |
| **`FORE1`** | `0x0085AC` | — | `Util.s:531` | — |
| **`ForeColor`** | `0x0083EE` | `0x012B24` | `Util.s:204` | **Proto:** `PROCEDURE ForeColor(color: LongInt);`<br>.PROC ForeColor,1 .DEF BackColor,PortLong,ColorBit,PortWord PROCEDURE ForeColor(color: LongInt); |
| **`FORECOLOR`** | `0x0083EE` | `0x012B24` | `Util.s:130` | ForeColor ($A862), BackColor ($A863) - set port color long |
| **`FOUND`** | `0x00D5B8` | `0x017D34` | `Stretch.s:908`<br>`Stretch.s:726` | Called by: SETUPSTRETCH, SHRNKING |
| **`FOUR`** | `0x00C6FE` | `0x016E6E` | `SortPoints.s:96`<br>`SortPoints.s:78` | FOUR Called during boot. |
| **`FRAME1`** | `0x00E3D2` | `0x018B5E` | `Pictures.s:1889`<br>`Pictures.s:1370` | FRAME1 |
| **`FrameArc`** | `0x00AFD6` | `0x015746` | `Arcs.s:91` | **Proto:** `PROCEDURE FrameArc(* r: Rect; startAngle,arcAngle: INTEGER *);`<br>DrawArc(r,hollow,ovWd,ovHt,mode,pat,startAng,arcAng); .PROC FrameArc,3 .DEF CallArc,PaintArc,EraseArc,InvertArc,FillArc .REF STDARC PROCEDURE FrameArc(* r: Rect; startAngle,arcAngle: INTEGER *); |
| **`FRAMEARC`** | `0x00AFD6` | `0x015746` | `Arcs.s:89` | **Proto:** `PROCEDURE FrameArc(* r: Rect; startAngle,arcAngle: INTEGER *);`<br>DrawArc(r,hollow,ovWd,ovHt,mode,pat,startAng,arcAng); .PROC FrameArc,3 .DEF CallArc,PaintArc,EraseArc,InvertArc,FillArc .REF STDARC PROCEDURE FrameArc(* r: Rect; startAngle,arcAngle: INTEGER *); |
| **`FrameOval`** | `0x00ADD4` | `0x015544` | `Ovals.s:103` | **Proto:** `PROCEDURE FrameOval(* r: Rect *);`<br>DrawArc(r,hollow,ovWd,ovHt,mode,pat,startAng,arcAng); .PROC FrameOval,1 .DEF CallOval,PaintOval,EraseOval,InvertOval,FillOval .REF StdOval PROCEDURE FrameOval(* r: Rect *); |
| **`FRAMEOVAL`** | `0x00ADD4` | `0x015544` | `Ovals.s:92` | **Proto:** `PROCEDURE FrameOval(* r: Rect *);`<br>DrawArc(r,hollow,ovWd,ovHt,mode,pat,startAng,arcAng); .PROC FrameOval,1 .DEF CallOval,PaintOval,EraseOval,InvertOval,FillOval .REF StdOval PROCEDURE FrameOval(* r: Rect *); |
| **`FramePoly`** | `0x00B9F8` | `0x016168` | `Polygons.s:92` | **Proto:** `PROCEDURE FramePoly(* poly: PolyHandle *);`<br>.PROC FramePoly,1 .DEF CallPoly,PaintPoly,ErasePoly,InvertPoly,FillPoly .REF StdPoly PROCEDURE FramePoly(* poly: PolyHandle *); |
| **`FRAMEPOLY`** | `0x00B9F8` | `0x016168` | `Polygons.s:74` | **Proto:** `PROCEDURE FramePoly(* poly: PolyHandle *);`<br>PROCEDURE FramePoly(* poly: PolyHandle *); |
| **`FrameRect`** | `0x009F28` | `0x014698` | `Rects.s:161` | **Proto:** `PROCEDURE FrameRect(r: Rect);`<br>PROCEDURE FrameRect(r: Rect); FrameRect _CopyPalette ($A8A1) Called during boot. |
| **`FRAMERECT`** | `0x009F28` | `0x014698` | `Rects.s:154` | **Proto:** `PROCEDURE FrameRect(r: Rect);`<br>PROCEDURE FrameRect(r: Rect); |
| **`FrameRgn`** | `0x00BC5C` | `0x0163CC` | `Regions.s:82` | **Proto:** `PROCEDURE FrameRgn(* rgn: RgnHandle *);`<br>.PROC FrameRgn,1 .DEF CallRgn,PaintRgn,EraseRgn,InvertRgn,FillRgn .REF StdRgn PROCEDURE FrameRgn(* rgn: RgnHandle *); Called during boot. |
| **`FRAMERGN`** | `0x00BC5C` | `0x0163CC` | `Regions.s:69` | **Proto:** `PROCEDURE FrameRgn(* rgn: RgnHandle *);`<br>PROCEDURE FrameRgn(* rgn: RgnHandle *); |
| **`FrameRoundRect`** | `0x00AD02` | `0x015472` | `RRects.s:98` | **Proto:** `PROCEDURE FrameRoundRect(* r: Rect; ovWd,ovHt: INTEGER *);`<br>DrawArc(r,hollow,ovWd,ovHt,mode,pat,startAng,arcAng); .PROC FrameRoundRect,3 .DEF CallRRect,PaintRoundRect,EraseRoundRect .DEF InvertRoundRect,FillRoundRect .REF StdRRect PROCEDURE FrameRoundRect(* r:... |
| **`FRAMEROUNDRECT`** | `0x00AD02` | `0x015472` | `RRects.s:100` | **Proto:** `PROCEDURE FrameRoundRect(* r: Rect; ovWd,ovHt: INTEGER *);`<br>DrawArc(r,hollow,ovWd,ovHt,mode,pat,startAng,arcAng); .PROC FrameRoundRect,3 .DEF CallRRect,PaintRoundRect,EraseRoundRect .DEF InvertRoundRect,FillRoundRect .REF StdRRect PROCEDURE FrameRoundRect(* r:... |
| **`FrPoly`** | `0x00BB60` | `0x0162D0` | `Polygons.s:373` | **Proto:** `PROCEDURE FrPoly(poly: PolyHandle);`<br>.PROC FrPoly,1 .REF MoveTo,DoLine PROCEDURE FrPoly(poly: PolyHandle); A6 OFFSETS OF PARAMS AND LOCALS AFTER LINK: PARAMSIZE .EQU 4 POLY .EQU PARAMSIZE+8-4 ;LONG, POLYHANDLE |
| **`FRPOLY`** | `0x00BB60` | `0x0162D0` | `Polygons.s:317` | **Proto:** `PROCEDURE FrPoly(poly: PolyHandle);`<br>PROCEDURE FrPoly(poly: PolyHandle); MoveTo first point, DoLine to each subsequent point. |
| **`FRPOLY_DONE`** | `0x00BB96` | `0x016306` | `Polygons.s:402`<br>`Polygons.s:342` | — |
| **`FRPOLY_NEXTPT`** | `0x00BB86` | `0x0162F6` | `Polygons.s:395`<br>`Polygons.s:335` | FRPOLY_NEXTPT |
| **`FRPOLY_START`** | `0x00BB92` | `0x016302` | `Polygons.s:400`<br>`Polygons.s:340` | — |
| **`FrRect`** | `0x009F94` | `0x014704` | `Rects.s:297` | **Proto:** `PROCEDURE FrRect(r: Rect);`<br>.PROC FrRect,1 .REF RgnBlt PROCEDURE FrRect(r: Rect); Draws an outline inside a rect. A6 OFFSETS OF PARAMETERS AND LOCALS AFTER LINK: DSTRECT .EQU 8 ;LONG, ADDR OF RECT H1 .EQU -2 ;WORD H2 .EQU H1-2 ;... |
| **`FRRECT`** | `0x009F94` | `0x014704` | `Rects.s:242` | **Proto:** `PROCEDURE FrRect(r: Rect);`<br>.PROC FrRect,1 .REF RgnBlt PROCEDURE FrRect(r: Rect); Draws an outline inside a rect. A6 OFFSETS OF PARAMETERS AND LOCALS AFTER LINK: DSTRECT +0x8 long, addr-of-rect H1 -0x2, H2 -0x4, H3 -0x6, H4 -0xA... |
| **`FRRECT_OK`** | `0x00A04E` | `0x0147BE` | `Rects.s:366`<br>`Rects.s:296` | Now set up h1,h2,h3,h4 and v1,v2,v3,v4 PEN IS NOT SO BIG AS TO FILL IN SOLID. BREAK RECT INTO 4 EDGES. |
| **`FrRgn`** | `0x00BCDE` | `0x01644E` | `Regions.s:204` | **Proto:** `PROCEDURE FrRgn(rgn: RgnHandle; mode: INTEGER; pat: Pattern);`<br>.PROC FrRgn,3 .REF FrRect,NewRgn,CopyRgn,InsetRgn,DiffRgn,DrawRgn PROCEDURE FrRgn(rgn: RgnHandle; mode: INTEGER; pat: Pattern); A6 OFFSETS OF PARAMS AFTER LINK: PARAMSIZE .EQU 10 RGN .EQU PARAMSIZE+8-... |
| **`FRRGN`** | `0x00BCDE` | `0x01644E` | `Regions.s:171` | **Proto:** `PROCEDURE FrRgn(rgn: RgnHandle; mode: INTEGER; pat: Pattern);`<br>PROCEDURE FrRgn(rgn: RgnHandle; mode: INTEGER; pat: Pattern); A6 offsets of params after LINK: PARAMSIZE = 10 RGN       = PARAMSIZE+8-4  (LONG, RgnHandle) MODE      = RGN-2          (WORD) PAT       =... |
| **`FRRGN_DONE`** | `0x00BD40` | `0x0164B0` | `Regions.s:256`<br>`Regions.s:213` | _DisposHandle ;DISCARD IT Called during boot. |
| **`FRRGN_NOTRECT`** | `0x00BD06` | `0x016476` | `Regions.s:233`<br>`Regions.s:193` | special case rectangular region for speed. FRRGN_NOTRECT |
| **`GET2`** | `0x00DD20` | `0x01849C` | `Pictures.s:756`<br>`Pictures.s:547` | GET2 |
| **`GET2_CONT`** | `0x00DD26` | `0x0184A2` | `Pictures.s:764`<br>`Pictures.s:551` | GET2_CONT |
| **`GET2_CONT_10`** | `0x00DD7A` | `0x0184F6` | `Pictures.s:843`<br>`Pictures.s:594` | GET2_CONT_10 |
| **`GET2_CONT_11`** | `0x00DDA2` | `0x01852E` | `Pictures.s:859`<br>`Pictures.s:610` | GET2_CONT_11 |
| **`GET2_CONT_12`** | `0x00DDAA` | `0x018536` | `Pictures.s:867`<br>`Pictures.s:614` | GET2_CONT_12 |
| **`GET2_CONT_13`** | `0x00DDB2` | `0x01853E` | `Pictures.s:875`<br>`Pictures.s:618` | GET2_CONT_13 |
| **`GET2_CONT_14`** | `0x00DDBA` | `0x018546` | `Pictures.s:883`<br>`Pictures.s:622` | GET2_CONT_14 |
| **`GET2_CONT_15`** | `0x00DDC2` | `0x01854E` | `Pictures.s:891`<br>`Pictures.s:626` | GET2_CONT_15 |
| **`GET2_CONT_16`** | `0x00DDE2` | `0x01856E` | `Pictures.s:906`<br>`Pictures.s:641` | CHANGE ORIGIN: ADD DH AND DV TO FROMRECT, ADJUST PATALIGN, THEN RE-MAP THECLIP |
| **`GET2_CONT_17`** | `0x00DE16` | `0x0185A2` | `Pictures.s:938`<br>`Pictures.s:678` | RE-COMPUTE MAPPED CLIPRGN FROM UNMAPPED THECLIP TEXT OR LINE OPCODES: LINE: 20, PNLOC(pt), NEWPT(pt) LINEFROM: 21, NEWPT(pt) SHORT LINE: 22, PNLOC(pt), DH(byte), DV(byte) SHORTLNFROM: 23, DH(byte), DV... |
| **`GET2_CONT_2`** | `0x00DD2C` | `0x0184A8` | `Pictures.s:772`<br>`Pictures.s:555` | GET2_CONT_2 |
| **`GET2_CONT_3`** | `0x00DD32` | `0x0184AE` | `Pictures.s:780`<br>`Pictures.s:559` | GET2_CONT_3 |
| **`GET2_CONT_4`** | `0x00DD38` | `0x0184B4` | `Pictures.s:788`<br>`Pictures.s:563` | GET2_CONT_4 |
| **`GET2_CONT_5`** | `0x00DD3E` | `0x0184BA` | `Pictures.s:796`<br>`Pictures.s:567` | GET2_CONT_5 |
| **`GET2_CONT_6`** | `0x00DD48` | `0x0184C4` | `Pictures.s:805`<br>`Pictures.s:572` | GET2_CONT_6 |
| **`GET2_CONT_7`** | `0x00DD4E` | `0x0184CA` | `Pictures.s:813`<br>`Pictures.s:576` | GET2_CONT_7 |
| **`GET2_CONT_8`** | `0x00DD54` | `0x0184D0` | `Pictures.s:821`<br>`Pictures.s:580` | GET2_CONT_8 |
| **`GET2_CONT_9`** | `0x00DD5A` | `0x0184D6` | `Pictures.s:829`<br>`Pictures.s:584` | GET2_CONT_9 |
| **`GET4`** | `0x00DD1A` | `0x018496` | `Pictures.s:748`<br>`Pictures.s:544` | GET4 |
| **`GET8`** | `0x00DD14` | `0x018490` | `Pictures.s:740`<br>`Pictures.s:541` | GET8 |
| **`GetClip`** | `0x008A8C` | `0x0131C2` | `GrafAsm.s:517` | **Proto:** `PROCEDURE GetClip(rgn: RgnHandle);`<br>PROCEDURE GetClip(rgn: RgnHandle); copy from theport^.clipRgn into rgn. Called during boot (2,785 times in 30s trace). |
| **`GETCLIP`** | `0x008A8C` | `0x0131C2` | `GrafAsm.s:498` | **Proto:** `PROCEDURE GetClip(rgn: RgnHandle);`<br>PROCEDURE GetClip(rgn: RgnHandle); { COPY THEPORT^.CLIPRGN INTO rgn } |
| **`GETCLIP_SHARE`** | `0x008A9A` | `0x0131D0` | `GrafAsm.s:524`<br>`GrafAsm.s:505` | — |
| **`GETDONE`** | `0x00E196` | `0x018922` | `Pictures.s:1440`<br>`Pictures.s:1046` | GET SOME BYTES AND QUIT |
| **`GETDST`** | `0x00CBC2` | `0x01733E` | `Bitmaps.s:453`<br>`Bitmaps.s:380` | Set up dstRow and starting dstAddr |
| **`GetFontInfo`** | `0x008E84` | `0x0135F4` | `Text.s:739` | **Proto:** `PROCEDURE GetFontInfo(VAR info: FontInfo);`<br>FUNCTION FMSwapFont(inRec: FMInput): FMOutPtr; FMSwapFont is the only contact between QuickDraw and the Font Manager. It swaps in the requested font and returns a pointer to an output record telling h... |
| **`GETFONTINFO`** | `0x008E84` | `0x0135F4` | `Text.s:641` | **Proto:** `PROCEDURE GetFontInfo(VAR info: FontInfo);`<br>.PROC GetFontInfo,1 .REF StdTxMeas PROCEDURE GetFontInfo(VAR info: FontInfo); Calls StdTxMeas thru capture proc, then adjusts and scales the result. 13 MAY 85, changed so that all 4 values round UP in... |
| **`GETFONTINFO_USESTD`** | `0x008EBC` | `0x01362C` | `Text.s:762`<br>`Text.s:662` | — |
| **`GETFONTINFO_USESTD_SKIP`** | `0x008EE2` | `0x013652` | `Text.s:791`<br>`Text.s:687` | ADJUST WIDMAX FOR EXTRA ADJUST ASCENT & DESCENT FOR SHADOW NOTSHAD SCALE RESULT IF NUMER <> DENOM Called during boot (30,141 times in 30s trace). |
| **`GETFONTINFO_USESTD_SKIP_2`** | `0x008F08` | `0x013678` | `Text.s:812`<br>`Text.s:702` | NOTSHAD SCALE RESULT IF NUMER <> DENOM |
| **`GETHND2`** | `0x00E224` | `0x0189B0` | `Pictures.s:1561`<br>`Pictures.s:1141` | GETHND2 -- gET DATA INTO HANDLE1. |
| **`GETHNDL`** | `0x00E220` | `0x0189AC` | `Pictures.s:1557`<br>`Pictures.s:1137` | LOCAL ROUTINE TO ALLOCATE, AND COPY HANDLE1 CLOBBERS D0-D2,A0-A1,D4,D5 TRICKY ENTRY AT GETHND2 WITH COUNT IN D0, D4 = 0 |
| **`GETLONG`** | `0x00E1D6` | `0x018962` | `Pictures.s:1499`<br>`Pictures.s:1093` | **Proto:** `LOCAL PROCEDURE TO GET A LONG FROM PICTURE INTO D0`<br>LOCAL PROCEDURE TO GET A LONG FROM PICTURE INTO D0 |
| **`GETMASKTAB`** | — | `0x012B44` | `Util.s:153` | GetMaskTable ($A836) - return ptr to 16-entry MASKTAB |
| **`GetMaskTable`** | `0x00840E` | — | `Util.s:269` | GetMaskTable -- trap handler for _RealColor ($A836). _RealColor ($A836) |
| **`GetPen`** | `0x0097F6` | `0x013F66` | `Lines.s:297` | **Proto:** `PROCEDURE GetPen(VAR pt: Point);`<br>.PROC GetPen,1 PROCEDURE GetPen(VAR pt: Point); { inquire the current pen location } Called during boot. |
| **`GETPEN`** | `0x0097F6` | `0x013F66` | `Lines.s:286` | **Proto:** `PROCEDURE GetPen(VAR pt: Point);`<br>.PROC GetPen,1 PROCEDURE GetPen(VAR pt: Point); { inquire the current pen location } Called during boot. |
| **`GetPenState`** | `0x0097D0` | `0x013F40` | `Lines.s:259` | _PmBackColor ($A898) Called during boot. |
| **`GETPENSTATE`** | `0x0097D0` | `0x013F40` | `Lines.s:250` | _PmBackColor ($A898) Called during boot. |
| **`GetPicData`** | `0x00E278` | `0x018A04` | `Pictures.s:1636` | **Proto:** `FUNCTION GetPicData(dataPtr: QDPtr; byteCount: INTEGER);`<br>.FUNC GetPicData,2 .REF StdGetPic FUNCTION GetPicData(dataPtr: QDPtr; byteCount: INTEGER); Called by: TEXTOP2, ARCOP_CONT_2, PICITEM_MORE1, PICITEM_NOPACK, GETDONE (and 6 more) |
| **`GETPICDATA`** | `0x00E278` | `0x018A04` | `Pictures.s:1195` | GETPICDATA -- dispatch to current GrafProcs.getPicProc or _StdGetPic if grafProcs is nil. Called by: TEXTOP2, BITSOP, PICITEM_MORE1, PICITEM_NOPACK, GETDONE (and 6 more) |
| **`GETPICDATA_EMPTY`** | `0x00E28C` | — | `Pictures.s:1644` | — |
| **`GETPICDATA_STD`** | — | `0x018A18` | `Pictures.s:1203` | — |
| **`GetPixel`** | `0x0085D4` | `0x012D0A` | `Util.s:573` | **Proto:** `FUNCTION GetPixel(h,v: INTEGER): BOOLEAN;`<br>.FUNC GetPixel,2 .REF HideCursor,ShowCursor FUNCTION GetPixel(h,v: INTEGER): BOOLEAN; Returns TRUE if the pixel at (h,v) is set to black. h and v are in local coords of the current grafport. CLOBBERS ... |
| **`GETPIXEL`** | `0x0085D4` | `0x012D0A` | `Util.s:396` | GetPixel(h, v: INTEGER) -> Boolean - test pixel state at (h,v) in current GrafPort's local coords. Returns TRUE if pixel set (black on default GrafPort). Hides cursor before reading and restores via S... |
| **`GetPort`** | `0x0089B8` | `0x0130EE` | `GrafAsm.s:352` | **Proto:** `PROCEDURE GetPort(VAR gp: GrafPtr);`<br>PROCEDURE GetPort(VAR gp: GrafPtr); { inquire the current GrafPort } Called during boot (17,610 times in 30s trace). |
| **`GETPORT`** | `0x0089B8` | `0x0130EE` | `GrafAsm.s:353` | **Proto:** `PROCEDURE GetPort(VAR gp: GrafPtr);`<br>PROCEDURE GetPort(VAR gp: GrafPtr); { inquire the current GrafPort } Called during boot (17,610 times in 30s trace). |
| **`GETPTRS`** | `0x0091D0` | `0x013940` | `DrawText.s:393`<br>`DrawText.s:337` | Get pointers to location table, width table, and height table in font Called during boot. |
| **`GETPTRS_NO`** | `0x009212` | `0x013982` | `DrawText.s:418`<br>`DrawText.s:358` | Get pointers to location table, width table, and height table in font |
| **`GETRECT`** | `0x00E1E6` | `0x018972` | `Pictures.s:1512`<br>`Pictures.s:1108` | GETRECT -- gET AND PUSH DSTRECT. GETRECT |
| **`GETSBYTE`** | `0x00E1B4` | `0x018940` | `Pictures.s:1465`<br>`Pictures.s:1068` | **Proto:** `LOCAL PROCEDURE TO GET A SIGNED BYTE INTO D0 FROM PICTURE`<br>LOCAL PROCEDURE TO GET A SIGNED BYTE INTO D0 FROM PICTURE |
| **`GETSRC`** | `0x00A348` | `0x014AB8` | `BitBlt.s:208`<br>`BitBlt.s:138` | SET UP SHIFTCNT IN D6 (RELATIVE SHIFT BETWEEN SRC & DST) DO UPSIDE DOWN TO AVOID CLOBBERING SRC Called during boot. |
| **`GETUBYTE`** | `0x00E1A2` | `0x01892E` | `Pictures.s:1451`<br>`Pictures.s:1056` | **Proto:** `LOCAL PROCEDURE TO GET AN UNSIGNED BYTE INTO D0 FROM PICTURE`<br>LOCAL PROCEDURE TO GET AN UNSIGNED BYTE INTO D0 FROM PICTURE Called by: PicItem, GET2_CONT_11, TEXTOP, PICITEM_DHOK, TEXTOP2 (and 1 more) |
| **`GETWORD`** | `0x00E1C6` | `0x018952` | `Pictures.s:1480`<br>`Pictures.s:1081` | **Proto:** `LOCAL PROCEDURE TO GET A WORD FROM PICTURE INTO D0`<br>LOCAL PROCEDURE TO GET A WORD FROM PICTURE INTO D0 Called by: ARCOP, ARCOP_CONT_2, COMMENTOP, LONGCOM, GETHNDL |
| **`GETWORD_NO`** | `0x00E1D6` | — | `Pictures.s:1493` | GETWORD_NO -- gET PNSIZE. GETWORD_NO |
| **`GlobalToLocal`** | `0x00895E` | `0x013094` | `GrafAsm.s:280` | **Proto:** `PROCEDURE GlobalToLocal(VAR pt: Point);`<br>PROCEDURE GlobalToLocal(VAR pt: Point); restores all registers. Called during boot (62,271 times in 30s trace). |
| **`GLOBALTOLOCAL`** | `0x00895E` | `0x013094` | `GrafAsm.s:285` | **Proto:** `PROCEDURE GlobalToLocal(VAR pt: Point);`<br>PROCEDURE GlobalToLocal(VAR pt: Point); restores all registers. Called during boot (62,271 times in 30s trace). |
| **`GLOBALTOLOCAL_CONT`** | `0x008964` | `0x01309A` | `GrafAsm.s:283`<br>`GrafAsm.s:288` | — |
| **`GOFORIT`** | `0x00B418` | `0x015B88` | `DrawArc.s:669`<br>`DrawArc.s:491` | — |
| **`GOHOME`** | `0x00A442` | `0x014BB2` | `BitBlt.s:390`<br>`BitBlt.s:288` | then quit Called during boot. |
| **`GOSLOW`** | `0x009B82` | `0x0142F2` | `DrawLine.s:544`<br>`DrawLine.s:437` | GOSLOW |
| **`GOSLOW_SKIP`** | `0x009B98` | `0x014308` | `DrawLine.s:557`<br>`DrawLine.s:449` | EXPAND 8 BYTE PATTERN TO 16 LONGS AND INIT PATTERN SELECTOR |
| **`GrafDevice`** | `0x0089C2` | `0x0130F8` | `GrafAsm.s:365` | **Proto:** `PROCEDURE GrafDevice(device: INTEGER);`<br>.PROC GrafDevice,1 .REF PortWord PROCEDURE GrafDevice(device: INTEGER); |
| **`GRAFDEVICE`** | `0x0089C2` | `0x0130F8` | `GrafAsm.s:364` | **Proto:** `PROCEDURE GrafDevice(device: INTEGER);`<br>.PROC GrafDevice,1 .REF PortWord PROCEDURE GrafDevice(device: INTEGER); |
| **`HALF`** | `0x00D622` | `0x017D9E` | `Stretch.s:976`<br>`Stretch.s:789` | SHRINK TO ONE HALF. |
| **`HALF1`** | `0x00D626` | `0x017DA2` | `Stretch.s:979`<br>`Stretch.s:792` | — |
| **`HALF2`** | `0x00D62A` | `0x017DA6` | `Stretch.s:982`<br>`Stretch.s:795` | — |
| **`HALF2_CONT`** | `0x00D642` | `0x017DBE` | `Stretch.s:999`<br>`Stretch.s:811` | SHRINK TO ONE QUARTER. |
| **`HEXLOOP`** | `0x00861E` | `0x012D54` | `Util.s:610`<br>`Util.s:429` | — |
| **`HIDE_CLEAR_VIS`** | `0x001CDA` | `0x018E0C` | `CrsrCore.s:68`<br>`CrsrCore.s:87` | — |
| **`HIDE_DEC_STATE`** | `0x001CE2` | `0x018E14` | `CrsrCore.s:71`<br>`CrsrCore.s:90` | — |
| **`HIDE_RESTORE_ROW`** | `0x001CD2` | `0x018E04` | `CrsrCore.s:63`<br>`CrsrCore.s:82` | — |
| **`HideCursor`** | `0x0082F2` | `0x012A28` | `LCursor.s:61` | **Proto:** `PROCEDURE HideCursor;`<br>.PROC HideCursor PROCEDURE HideCursor; ALL REGS PRESERVED. Called during boot. |
| **`HIDECURSOR`** | `0x0082F2` | `0x012A28` | `LCursor.s:40` | **Proto:** `Pascal: procedure HideCursor;`<br>HIDECURSOR ($A852) - hide cursor via JHideCursor lowmem vector Pascal: procedure HideCursor; |
| **`HidePen`** | `0x0097C0` | `0x013F30` | `Lines.s:237` | **Proto:** `PROCEDURE HidePen;`<br>.PROC HidePen,0 .DEF ShowPen PROCEDURE HidePen; Called during boot. |
| **`HIDEPEN`** | `0x0097C0` | `0x013F30` | `Lines.s:230` | **Proto:** `PROCEDURE HidePen;`<br>.PROC HidePen,0 .DEF ShowPen PROCEDURE HidePen; Called during boot. |
| **`HINSET`** | `0x00BF44` | `0x0166B4` | `Regions.s:615`<br>`Regions.s:511` | LOCAL ROUTINE TO INSET HORIZONTALLY, SWAP H AND V COORDS, AND RE-SORT RgnOp(rgn,rgn,bufHandle,maxBytes,op,dh,TRUE); |
| **`HOK`** | `0x00A1D4` | `0x014944` | `Rects.s:693`<br>`Rects.s:585` | — |
| **`HOK_NO`** | `0x00A1EA` | `0x01495A` | `Rects.s:701`<br>`Rects.s:593` | — |
| **`HORIZOK`** | `0x0092FE` | `0x013A6E` | `DrawText.s:581`<br>`DrawText.s:496` | HORIZOK Inputs to local block CharBlt: srcAddr(A6) srcRow(A6) bufStart(A6) = dstAddr bufRow(A6) = dstRow D1 = srcLeft D2 = dstRight relative to buffer, > dstLeft D3 = dstLeft relative to buffer TOPHT(... |
| **`HOVAL`** | `0x00B5F2` | `0x015D62` | `DrawArc.s:944`<br>`DrawArc.s:705` | ELSE IF BOTH LINES ACTIVE AND ANGLE > 180 THEN PAINT TWO SLABS HOVAL Called during boot. |
| **`HSET`** | `0x009CFC` | `0x01446C` | `DrawLine.s:780`<br>`DrawLine.s:655` | DRAW A BLACK HORIZONTAL LINE Called during boot. |
| **`HTOGL`** | `0x009CD4` | `0x014444` | `DrawLine.s:745`<br>`DrawLine.s:622` | DRAW AN XOR HORIZONTAL LINE |
| **`HVLINE`** | `0x009966` | `0x0140D6` | `DrawLine.s:229`<br>`DrawLine.s:182` | FLAGOK GET THE TWO LINE ENDPOINTS INTO REGISTERS AND CHECK FOR HORIZONTAL OR VERTICAL LINE ELSE V1=V2, DO HORIZONTAL LINE IS EITHER HORIZONTAL OR VERTICAL. CHECK FOR ONE DOT LINE, BLACK OR WHITE PATTE... |
| **`HVSETUP`** | `0x009D64` | `0x0144D4` | `DrawLine.s:860`<br>`DrawLine.s:734` | HVSETUP Called during boot. |
| **`InitCrsr`** | `0x001CEC` | — | `CrsrCore.s:85` | InitCrsr - Initialize cursor state (called once at boot) Resets CrsrObscure, sets CrsrState to 0, then falls through to ShowCursor to draw the initial cursor on screen. Called during boot. |
| **`INITCRTABLE`** | — | `0x018DBC` | `CrsrCore.s:43` | Cursor core -- cursor drawing, ScrnAddress/ScrnSize/ScrnBitMap, CrsrVBLTask, PinRect Apple source: CrsrCore.a (System 7.1: QuickDraw/Classic/CrsrCore.a; the SE link map calls the module CRSRCORE). The... |
| **`InitCursor`** | `0x0082C6` | `0x0129FC` | `LCursor.s:19` | **Proto:** `PROCEDURE InitCursor;`<br>--> LCURSOR.TEXT Links to MacIntosh Cursor routines. System Graphic Jump Vectors: Long pointers to system routine entry points. .PROC InitCursor,0 .REF SetCursor PROCEDURE InitCursor; Called during bo... |
| **`INITCURSOR`** | `0x0082C6` | `0x0129FC` | `LCursor.s:17` | **Proto:** `Pascal: procedure InitCursor;`<br>--> LCURSOR.TEXT Links to MacIntosh Cursor routines. System Graphic Jump Vectors: Long pointers to system routine entry points. INITCURSOR ($A850) - install standard arrow cursor and call jump Pascal:... |
| **`InitGraf`** | `0x0087A6` | `0x012EDC` | `GrafAsm.s:14` | **Proto:** `PROCEDURE InitGraf(globalPtr: Ptr);`<br>--> GRAFASM.TEXT Miscellaneous unclassified routines. .PROC InitGraf,1 PROCEDURE InitGraf(globalPtr: Ptr); Called during boot. |
| **`INITGRAF`** | `0x0087A6` | `0x012EDC` | `GrafAsm.s:55` | — |
| **`InitOval`** | `0x00B6AC` | `0x015E1C` | `DrawArc.s:1081` | **Proto:** `PROCEDURE InitOval(dstRect: Rect; VAR oval: OvalRec;`<br>.PROC INITOVAL,4 PROCEDURE InitOval(dstRect: Rect; VAR oval: OvalRec; ovalWidth,ovalHeight: INTEGER); initialize an oval state record to fit the given rectangle. INPUTS: A0: dstRect A1: ovalRec D1: ov... |
| **`INITOVAL`** | `0x00B6AC` | `0x015E1C` | `DrawArc.s:832` | **Proto:** `PROCEDURE InitOval(dstRect: Rect; VAR oval: OvalRec;`<br>PROCEDURE InitOval(dstRect: Rect; VAR oval: OvalRec; ovalWidth, ovalHeight: INTEGER); Initialize an oval state record to fit the given rectangle. INPUTS:  A0: dstRect A1: ovalRec D1: ovalHeight D2: ov... |
| **`INITOVAL_OK3`** | `0x00B6CE` | `0x015E3E` | `DrawArc.s:1106`<br>`DrawArc.s:856` | — |
| **`INITOVAL_OK3_NO`** | `0x00B6DA` | `0x015E4A` | `DrawArc.s:1112`<br>`DrawArc.s:866` | Set up oval left edge and oval right edge as fixed-point numbers |
| **`InitPort`** | `0x008884` | `0x012FBA` | `GrafAsm.s:172` | **Proto:** `PROCEDURE InitPort(port: GrafPtr);`<br>\| FALL THRU TO InitPort .PROC InitPort,1 .REF RectRgn,CopyRgn PROCEDURE InitPort(port: GrafPtr); { initialize all fields of an existing GrafPort } Called during boot. |
| **`INITPORT`** | `0x008884` | `0x012FBA` | `GrafAsm.s:180` | **Proto:** `PROCEDURE InitPort(port: GrafPtr);`<br>\| FALL THRU TO InitPort .PROC InitPort,1 .REF RectRgn,CopyRgn PROCEDURE InitPort(port: GrafPtr); { initialize all fields of an existing GrafPort } Called during boot. |
| **`InitRgn`** | `0x00C2C6` | `0x016A36` | `SeekRgn.s:24` | --> SEEKRGN.TEXT Routines to play back a region into a scanline buffer. .PROC INITRGN,0 INPUTS: A0: RGNPTR A1: STATE RECORD D0: MINH D1: MAXH D2: BUFLEFT OUTPUTS: ALL FIELDS OF STATE RECORD, SCANBUF A... |
| **`INITRGN`** | `0x00C2C6` | `0x016A36` | `SeekRgn.s:23` | --> SEEKRGN.TEXT Routines to play back a region into a scanline buffer. InitRgn -- initialize a region state record at top. INPUTS:  A0 = RgnPtr A1 = state record D0 = MinH D1 = MaxH D2 = BufLeft OUTP... |
| **`INITRGN_CLRLOOP`** | `0x00C2F2` | `0x016A62` | `SeekRgn.s:37`<br>`SeekRgn.s:36` | — |
| **`INSET`** | `0x00C64C` | `0x016DBC` | `RgnOp.s:460`<br>`RgnOp.s:399` | Get each pair of coords, inset them, and cancel if they cross. |
| **`InsetRect`** | `0x00A0D6` | `0x014846` | `Rects.s:505` | **Proto:** `PROCEDURE InsetRect(VAR r: Rect; dh,dv: INTEGER);`<br>RTS ;AND RETURN .PROC InsetRect PROCEDURE InsetRect(VAR r: Rect; dh,dv: INTEGER); { inset a rectangle on all 4 sides } Called during boot. |
| **`INSETRECT`** | `0x00A0D6` | `0x014846` | `Rects.s:419` | **Proto:** `PROCEDURE InsetRect(VAR r: Rect; dh,dv: INTEGER);`<br>.PROC InsetRect PROCEDURE InsetRect(VAR r: Rect; dh,dv: INTEGER); { inset a rectangle on all 4 sides } Called during boot. |
| **`InsetRgn`** | `0x00BEF4` | `0x016664` | `Regions.s:559` | **Proto:** `PROCEDURE InsetRgn(rgn: RgnHandle; dh,dv: INTEGER);`<br>.PROC InsetRgn,3 .REF InsetRect,SortPoints .REF NewHandle,RgnOp,PackRgn PROCEDURE InsetRgn(rgn: RgnHandle; dh,dv: INTEGER); Inset a region by (dh,dv). Outset if dh or dv neg A6 OFFSETS OF PARAMS AFTER... |
| **`INSETRGN`** | `0x00BEF4` | `0x016664` | `Regions.s:461` | **Proto:** `PROCEDURE InsetRgn(rgn: RgnHandle; dh,dv: INTEGER);`<br>PROCEDURE InsetRgn(rgn: RgnHandle; dh,dv: INTEGER); Inset a region by (dh,dv). Outset if dh or dv neg. A6 offsets of params after LINK: PARAMSIZE = 8 RGN       = PARAMSIZE+8-4  (LONG, RgnHandle) DH   ... |
| **`INSETRGN_DONE`** | `0x00BF80` | `0x0166F0` | `Regions.s:665`<br>`Regions.s:556` | RE-SORT THE POINTS IN V.H ORDER PACK THE RESULTING POINTS DISCARD POINT BUFFER AND QUIT. |
| **`INSETRGN_EMPTY`** | `0x00BF2A` | `0x01669A` | `Regions.s:588`<br>`Regions.s:484` | .set DV, DH-2 ;WORD IF RECTANGULAR REGION, CALL INSETRECT AND CHECK FOR EMPTY. |
| **`INSETRGN_GOHOME`** | `0x00BF84` | `0x0166F4` | `Regions.s:670`<br>`Regions.s:559` | _DisposHandle ;DISCARD IT |
| **`INSETRGN_NOTRECT`** | `0x00BF30` | `0x0166A0` | `Regions.s:598`<br>`Regions.s:494` | THE REGION IS NOT RECTANGULAR. ALLOCATE A POINT BUFFER IN THE HEAP. |
| **`InsetScan`** | `0x00C648` | `0x016DB8` | `RgnOp.s:457` | **Proto:** `PROCEDURE InsetScan(src,dst: ScanPtr; dh: INTEGER);`<br>LOCAL ROUTINE TO EXPAND A RECTANGULAR REGION TO ITS INVERSION POINTS. ENTER WITH ADDR OF RGNHANDLE IN A0, ADDR OF FAKE MASTER IN A2. RETURNS IN A0 DE-REFERENCED POINTER BUMPED TO FIRST RGNDATA, AND A2... |
| **`INSETSCAN`** | `0x00C648` | `0x016DB8` | `RgnOp.s:392` | **Proto:** `PROCEDURE InsetScan(src, dst: ScanPtr; dh: INTEGER);`<br>PROCEDURE InsetScan(src, dst: ScanPtr; dh: INTEGER); Horizontally inset an inversion scan by dh. INPUTS:  A0 src, A2 dst, D2 dh CLOBBERS D0-D1, A0-A2 |
| **`INSETSCAN_ALESS`** | `0x00C6A2` | `0x016E12` | `RgnOp.s:564`<br>`RgnOp.s:477` | INSETSCAN_ALESS Called during boot (186,218 times in 30s trace). |
| **`INSETSCAN_NEXT`** | `0x00C696` | `0x016E06` | `RgnOp.s:551`<br>`RgnOp.s:466` | — |
| **`InverRect`** | `0x009F34` | — | `Rects.s:206` | **Proto:** `PROCEDURE InvertRect(r: Rect);`<br>PROCEDURE InvertRect(r: Rect); InvertRect _InverRect ($A8A4) Called during boot. |
| **`InverRgn`** | `0x00BC68` | — | `Regions.s:107` | **Proto:** `PROCEDURE InvertRgn(* rgn: RgnHandle *);`<br>PROCEDURE InvertRgn(* rgn: RgnHandle *); |
| **`InverRoundRect`** | `0x00AD0E` | — | `RRects.s:124` | **Proto:** `PROCEDURE InvertRoundRect(* r: Rect; ovWd,ovHt: INTEGER *);`<br>PROCEDURE InvertRoundRect(* r: Rect; ovWd,ovHt: INTEGER *); Called during boot. |
| **`INVERT1`** | `0x00CE6E` | `0x0175EA` | `Bitmaps.s:847`<br>`Bitmaps.s:717` | LDONE bump three pointers down and loop for height scanlines switch directions, adjust pointers, and loop till no change if seedFill, then invert dst |
| **`INVERT2`** | `0x00CE70` | `0x0175EC` | `Bitmaps.s:849`<br>`Bitmaps.s:719` | — |
| **`INVERT2_EXIT`** | `0x00CE7C` | `0x0175F8` | `Bitmaps.s:854`<br>`Bitmaps.s:724` | — |
| **`InvertArc`** | `0x00AFE2` | `0x015752` | `Arcs.s:115` | **Proto:** `PROCEDURE InvertArc(* r: Rect; startAngle,arcAngle: INTEGER *);`<br>PROCEDURE InvertArc(* r: Rect; startAngle,arcAngle: INTEGER *); |
| **`INVERTARC`** | `0x00AFE2` | `0x015752` | `Arcs.s:110` | **Proto:** `PROCEDURE InvertArc(* r: Rect; startAngle,arcAngle: INTEGER *);`<br>PROCEDURE InvertArc(* r: Rect; startAngle,arcAngle: INTEGER *); |
| **`InvertOval`** | `0x00ADE0` | `0x015550` | `Ovals.s:127` | **Proto:** `PROCEDURE InvertOval(* r: Rect *);`<br>PROCEDURE InvertOval(* r: Rect *); |
| **`INVERTOVAL`** | `0x00ADE0` | `0x015550` | `Ovals.s:113` | **Proto:** `PROCEDURE InvertOval(* r: Rect *);`<br>PROCEDURE InvertOval(* r: Rect *); |
| **`InvertPoly`** | `0x00BA04` | `0x016174` | `Polygons.s:116` | **Proto:** `PROCEDURE InvertPoly(* poly: PolyHandle *);`<br>PROCEDURE InvertPoly(* poly: PolyHandle *); |
| **`INVERTPOLY`** | `0x00BA04` | `0x016174` | `Polygons.s:95` | **Proto:** `PROCEDURE InvertPoly(* poly: PolyHandle *);`<br>PROCEDURE InvertPoly(* poly: PolyHandle *); |
| **`INVERTRECT`** | — | `0x0146A4` | `Rects.s:175` | **Proto:** `PROCEDURE InvertRect(r: Rect);`<br>PROCEDURE InvertRect(r: Rect); |
| **`INVERTRGN`** | — | `0x0163D8` | `Regions.s:90` | **Proto:** `PROCEDURE InvertRgn(* rgn: RgnHandle *);`<br>PROCEDURE InvertRgn(* rgn: RgnHandle *); |
| **`INVERTROUNDRECT`** | — | `0x01547E` | `RRects.s:123` | **Proto:** `PROCEDURE InvertRoundRect(* r: Rect; ovWd,ovHt: INTEGER *);`<br>PROCEDURE InvertRoundRect(* r: Rect; ovWd,ovHt: INTEGER *); Called during boot. |
| **`INVLONG`** | `0x00C3B0` | `0x016B20` | `SeekRgn.s:179`<br>`SeekRgn.s:159` | INVLONG Called during boot. |
| **`INVLONG_CONT`** | `0x00C3B2` | `0x016B22` | `SeekRgn.s:181`<br>`SeekRgn.s:161` | — |
| **`INVMODE`** | `0x0085C6` | `0x012CFC` | `Util.s:555`<br>`Util.s:383` | INVMODE |
| **`JDONE`** | `0x00C074` | `0x0167E4` | `Regions.s:900`<br>`Regions.s:743` | — |
| **`JDONE_DONE`** | `0x00C0C6` | `0x016836` | `Regions.s:958`<br>`Regions.s:790` | PtCount := RgnOp(srcA,srcB,bufHandle,maxBytes,op,0,TRUE); _DisposHandle ;DISCARD IT Called during boot (10,214 times in 30s trace). |
| **`JDONE_NO_2`** | `0x00C08E` | `0x0167FE` | `Regions.s:927`<br>`Regions.s:763` | OP = UNION OR XOR: IF EITHER REGION IS EMPTY, COPY THE OTHER. JDONE_NO_2 Called during boot (7,414 times in 30s trace). |
| **`JGOHOME`** | `0x00BF2E` | `0x01669E` | `Regions.s:591`<br>`Regions.s:487` | — |
| **`JMPSEEK`** | `0x00AAB6` | `0x015226` | `RgnBlt.s:701`<br>`RgnBlt.s:511` | — |
| **`JMPSEEK_CONT`** | `0x00AAC0` | `0x015230` | `RgnBlt.s:715`<br>`RgnBlt.s:519` | ONLY REGION C IS NON RECTANGULAR. UPDATE IT AND USE IT AS THE MASK REGIONS A AND B ARE NON-RECTANGULAR. UPDATE EACH, THEN FORM INTERSECTION IN THE MASK BUFFER. |
| **`JMPSEEK_CONT_2`** | `0x00AAE0` | `0x015250` | `RgnBlt.s:736`<br>`RgnBlt.s:536` | REGIONS A AND C ARE NON-RECTANGULAR. UPDATE EACH, THEN FORM INTERSECTION IN THE MASK BUFFER. Called during boot. |
| **`JMPSEEK_CONT_3`** | `0x00AB00` | `0x015270` | `RgnBlt.s:756`<br>`RgnBlt.s:552` | REGIONS B AND C ARE NON-RECTANGULAR. UPDATE EACH, THEN FORM INTERSECTION IN THE MASK BUFFER. |
| **`JSRSEEK`** | `0x00B66E` | `0x015DDE` | `DrawArc.s:1030`<br>`DrawArc.s:788` | JSRSEEK - call SeekRgn(StateA), store buffer pointer as scan mask |
| **`JSRSEEK_CONT`** | `0x00B678` | `0x015DE8` | `DrawArc.s:1033`<br>`DrawArc.s:791` | — |
| **`JSRSEEK_CONT_2`** | `0x00B67A` | `0x015DEA` | `DrawArc.s:1039`<br>`DrawArc.s:796` | ONLY REGION B IS NON RECTANGULAR. UPDATE IT AND USE IT AS THE MASK |
| **`JSRSEEK_CONT_3`** | `0x00B680` | `0x015DF0` | `DrawArc.s:1048`<br>`DrawArc.s:803` | REGIONS A AND B ARE NON-RECTANGULAR. UPDATE EACH, THEN FORM INTERSECTION IN THE MASK BUFFER. |
| **`JSRSEEK_RTS`** | — | `0x017BE8` | `Stretch.s:523` | — |
| **`JUSTADD`** | `0x008984` | `0x0130BA` | `GrafAsm.s:303`<br>`GrafAsm.s:308` | — |
| **`KILL1`** | `0x00E25E` | `0x0189EA` | `Pictures.s:1605`<br>`Pictures.s:1174` | _DisposHandle ;DISCARD IT |
| **`KILL1_ERR`** | `0x00E266` | `0x0189F2` | `Pictures.s:1619`<br>`Pictures.s:1179` | _DisposHandle ;DISCARD IT KILL ONE OR TWO HANDLE TEMPS KILL1_ERR |
| **`KILL1_EXIT`** | `0x00E26E` | `0x0189FA` | `Pictures.s:1623`<br>`Pictures.s:1184` | Called by: PicItem, GET2_CONT_9, GET2_CONT_10, GET2_CONT_11, GET2_CONT_15 (and 3 more) |
| **`KILL2`** | `0x00E258` | `0x0189E4` | `Pictures.s:1600`<br>`Pictures.s:1171` | KILL ONE OR TWO HANDLE TEMPS |
| **`KillPicture`** | `0x00DAE4` | `0x018260` | `Pictures.s:373` | **Proto:** `PROCEDURE KillPicture(myPicture: PicHandle);`<br>RTS ;AND RETURN .PROC KillPicture PROCEDURE KillPicture(myPicture: PicHandle); |
| **`KILLPICTURE`** | `0x00DAE4` | `0x018260` | `Pictures.s:303` | **Proto:** `PROCEDURE KillPicture(myPicture: PicHandle);`<br>PROCEDURE KillPicture(myPicture: PicHandle); Disposes of a picture handle. |
| **`KillPoly`** | `0x00BAE0` | `0x016250` | `Polygons.s:268` | **Proto:** `PROCEDURE KillPoly(poly: PolyHandle);`<br>.PROC KillPoly PROCEDURE KillPoly(poly: PolyHandle); |
| **`KILLPOLY`** | `0x00BAE0` | `0x016250` | `Polygons.s:232` | **Proto:** `PROCEDURE KillPoly(poly: PolyHandle);`<br>PROCEDURE KillPoly(poly: PolyHandle); |
| **`L_mPortLong`** | `0x0083F4` | — | `Util.s:224` | — |
| **`L_mPortWord`** | `0x008402` | — | `Util.s:257` | **Proto:** `ASSEMBLY LANGUAGE CALLABLE PROCEDURES LEFTMASK, RIGHTMASK, AND BITMASK:`<br>PROCEDURE PortWord(word: INTEGER); INSTALL A WORD INTO CURRENT GRAFPORT. ENTER WITH OFFSET IN D0 PortWord .PROC GetMaskTab,0 .DEF LeftMask,RightMask,BitMask,MaskTab ASSEMBLY LANGUAGE CALLABLE PROCEDUR... |
| **`LAST10`** | `0x008752` | `0x012E88` | `Util.s:948`<br>`Util.s:658` | — |
| **`LAST10_CONT`** | `0x008756` | `0x012E8C` | `Util.s:957`<br>`Util.s:668` | LAST10_CONT Called during boot. |
| **`LAST11`** | `0x00876A` | `0x012EA0` | `Util.s:978`<br>`Util.s:684` | — |
| **`LAST8`** | `0x00873C` | `0x012E72` | `Util.s:919`<br>`Util.s:633` | — |
| **`LAST8_CONT`** | `0x008740` | `0x012E76` | `Util.s:928`<br>`Util.s:643` | LAST8_CONT Called during boot. |
| **`LAYOUT`** | `0x00E132` | — | `Pictures.s:1409` | Infinite loop. Once the bitmap has been drawn, the machine spins here forever. This effectively freezes execution with the image left on screen. LAYOUT Embedded 1-bit bitmap data: "STOLEN FROM APPLE C... |
| **`LDSTOK`** | `0x00CE12` | `0x01758E` | `Bitmaps.s:785`<br>`Bitmaps.s:664` | LDSTOK |
| **`LEFT0`** | `0x00A470` | `0x014BE0` | `BitBlt.s:427`<br>`BitBlt.s:330` | ; INTERFACE TO EACH BITBLT SCANLINE LOOP: ; REGISTERS: A0: hBump (+-2) D0: scratch ; A1: MODE CASE JUMP D1: FIRSTMASK ; A2: used for loop jmp D2: WORDCNT ; A3: dstBump D3: height-1 ; A4: SRCPTR D4: FI... |
| **`LeftMask`** | `0x008414` | `0x012B4A` | `Util.s:278` | Left Mask Called during boot. |
| **`LEFTMASK`** | `0x008414` | `0x012B4A` | `Util.s:158` | LeftMask(D0) -> word in D0 - mask of bits left of bit D0 |
| **`LeftMaskTbl`** | — | `0x012B8E` | `Util.s:199` | — |
| **`LEFTOK`** | `0x00C92E` | `0x0170AA` | `Bitmaps.s:82`<br>`Bitmaps.s:72` | — |
| **`LEFTOK_NO`** | `0x00C94A` | `0x0170C6` | `Bitmaps.s:92`<br>`Bitmaps.s:82` | — |
| **`Line`** | `0x009710` | `0x013E80` | `Lines.s:127` | **Proto:** `PROCEDURE Line(dh,dv: INTEGER);`<br>.PROC Line,2 .REF LineTo PROCEDURE Line(dh,dv: INTEGER); |
| **`LINE`** | `0x009710` | `0x013E80` | `Lines.s:125` | **Proto:** `PROCEDURE Line(dh,dv: INTEGER);`<br>.PROC Line,2 .REF LineTo PROCEDURE Line(dh,dv: INTEGER); |
| **`LineTo`** | `0x0096FA` | `0x013E6A` | `Lines.s:110` | **Proto:** `PROCEDURE LineTo(h,v: INTEGER);`<br>.PROC LineTo,2 .REF StdLine PROCEDURE LineTo(h,v: INTEGER); Called during boot. |
| **`LINETO`** | `0x0096FA` | `0x013E6A` | `Lines.s:109` | **Proto:** `PROCEDURE LineTo(h,v: INTEGER);`<br>.PROC LineTo,2 .REF StdLine PROCEDURE LineTo(h,v: INTEGER); Called during boot. |
| **`LINETO_USESTD`** | `0x00970E` | `0x013E7E` | `Lines.s:118`<br>`Lines.s:117` | — |
| **`LMORE`** | `0x00CE1A` | `0x017596` | `Bitmaps.s:795`<br>`Bitmaps.s:673` | LMORE |
| **`LMORE0`** | `0x00A49A` | `0x014C0A` | `BitBlt.s:456`<br>`BitBlt.s:358` | — |
| **`LNEXT`** | `0x00CE02` | `0x01757E` | `Bitmaps.s:772`<br>`Bitmaps.s:652` | — |
| **`LNFROM`** | `0x00DE2E` | `0x0185BA` | `Pictures.s:949`<br>`Pictures.s:686` | — |
| **`LNOK`** | `0x00DE68` | `0x0185F4` | `Pictures.s:972`<br>`Pictures.s:705` | — |
| **`LNOK_OK`** | `0x00DE96` | `0x018622` | `Pictures.s:985`<br>`Pictures.s:718` | — |
| **`LocalToGlobal`** | `0x008956` | `0x01308C` | `GrafAsm.s:268` | **Proto:** `PROCEDURE LocalToGlobal(VAR pt: Point);`<br>.PROC LocalToGlobal,1 .DEF GlobalToLocal,AddPt,SubPt,SetPort,GetPort PROCEDURE LocalToGlobal(VAR pt: Point); restores all registers. Called during boot. |
| **`LOCALTOGLOBAL`** | `0x008956` | `0x01308C` | `GrafAsm.s:274` | **Proto:** `PROCEDURE LocalToGlobal(VAR pt: Point);`<br>.PROC LocalToGlobal,1 .DEF GlobalToLocal,AddPt,SubPt,SetPort,GetPort PROCEDURE LocalToGlobal(VAR pt: Point); restores all registers. Called during boot. |
| **`LOK`** | `0x00C368` | `0x016AD8` | `SeekRgn.s:121`<br>`SeekRgn.s:108` | — |
| **`LONE0`** | `0x00A496` | `0x014C06` | `BitBlt.s:453`<br>`BitBlt.s:355` | — |
| **`LONG1`** | `0x0093AC` | `0x013B1C` | `DrawText.s:688`<br>`DrawText.s:592` | LONG1 Called during boot. |
| **`LONG1A`** | `0x0093AE` | `0x013B1E` | `DrawText.s:695`<br>`DrawText.s:598` | Optimize if dst fits in one long. (30% of normal characters do) Called during boot. |
| **`LONGCOM`** | `0x00E0F4` | `0x018880` | `Pictures.s:1295`<br>`Pictures.s:979` | LONGCOM |
| **`LONGCOM_OK`** | `0x00E114` | `0x0188A0` | `Pictures.s:1306`<br>`Pictures.s:990` | — |
| **`LONGTXT`** | `0x00DEC2` | `0x01864E` | `Pictures.s:1020`<br>`Pictures.s:741` | LONGTXT |
| **`LOOP`** | `0x009E44` | `0x0145B4` | `PutLine.s:159`<br>`PutLine.s:140` | SLOPEOK FOR VERT:=TOPV TO BOTV-1 ADD SLOPE TO HORIZ AND PUT SLABS |
| **`LOOP1`** | `0x00E128` | `0x0188B4` | `Pictures.s:1362`<br>`Pictures.s:1006` | — |
| **`LOOP10`** | `0x008748` | `0x012E7E` | `Util.s:937`<br>`Util.s:648` | FAST XOR SLAB: |
| **`LOOP11`** | `0x008760` | `0x012E96` | `Util.s:967`<br>`Util.s:674` | FAST WHITE SLAB: |
| **`LOOP2`** | `0x00E130` | `0x0188BC` | `Pictures.s:1387`<br>`Pictures.s:1010` | — |
| **`LOOP8`** | `0x008734` | `0x012E6A` | `Util.s:914`<br>`Util.s:628` | — |
| **`LSAME`** | `0x00CE30` | `0x0175AC` | `Bitmaps.s:808`<br>`Bitmaps.s:686` | — |
| **`LSAME_CONT`** | `0x00CE36` | `0x0175B2` | `Bitmaps.s:816`<br>`Bitmaps.s:692` | LDONE bump three pointers down and loop for height scanlines |
| **`LSMEAR`** | `0x00CDFE` | `0x01757A` | `Bitmaps.s:769`<br>`Bitmaps.s:649` | RDONE smear dst zeros down and to the left, smear limited by src. |
| **`LSTART`** | `0x00CE1C` | `0x017598` | `Bitmaps.s:797`<br>`Bitmaps.s:675` | — |
| **`LTWO0`** | `0x00A494` | `0x014C04` | `BitBlt.s:451`<br>`BitBlt.s:353` | LTWO0 |
| **`MAIN0`** | `0x00A4C8` | `0x014C38` | `BitBlt.s:497`<br>`BitBlt.s:396` | MODE 0 OR 4: SRC --> DST Called during boot. |
| **`MAIN1`** | `0x00936C` | `0x013ADC` | `DrawText.s:657`<br>`DrawText.s:562` | Branch based on total number of dst words Slow loop only taken in wierd cases where dst wider than a long. |
| **`MAIN11`** | `0x00A6FC` | `0x014E6C` | `BitBlt.s:910`<br>`BitBlt.s:775` | MODE 11 OR 15: PATTERN BIC DST --> DST Called during boot. |
| **`MAIN9`** | `0x00A666` | `0x014DD6` | `BitBlt.s:792`<br>`BitBlt.s:671` | MODE 9 OR 13: PATTERN OR DST --> DST |
| **`MAIN9_CONT`** | `0x00A678` | `0x014DE8` | `BitBlt.s:807`<br>`BitBlt.s:685` | MODE 10 OR 14: PATTERN XOR DST --> DST (INVERTING AREAS, XOR LINES) Called during boot. |
| **`MAIN9_CONT_2`** | `0x00A684` | `0x014DF4` | `BitBlt.s:817`<br>`BitBlt.s:694` | MAIN9_CONT_2 Called during boot (1,516 times in 30s trace). |
| **`MAIN9_NO`** | `0x00A694` | `0x014E04` | `BitBlt.s:826`<br>`BitBlt.s:703` | — |
| **`MAP1`** | `0x00E596` | `0x018D22` | `Pictures.s:2170`<br>`Pictures.s:1586` | MAP1 -- mAP THE VERTICAL COORD. MAP1 |
| **`MapPoly`** | `0x00BB04` | `0x016274` | `Polygons.s:309` | **Proto:** `PROCEDURE MapPoly(poly: PolyHandle; fromRect,toRect: Rect);`<br>.PROC MapPoly,3 .REF MapPt,MapRect PROCEDURE MapPoly(poly: PolyHandle; fromRect,toRect: Rect); A6 OFFSETS OF PARAMETERS AND LOCALS AFTER LINK: PARAMSIZE .EQU 12 POLY .EQU PARAMSIZE+8-4 ;LONG, RGNHANDL... |
| **`MAPPOLY`** | `0x00BB04` | `0x016274` | `Polygons.s:266` | **Proto:** `PROCEDURE MapPoly(poly: PolyHandle; fromRect, toRect: Rect);`<br>PROCEDURE MapPoly(poly: PolyHandle; fromRect, toRect: Rect); A6 offsets of parameters and locals after LINK: PARAMSIZE = 12 POLY      = PARAMSIZE+8-4  (LONG, RgnHandle) FROMRECT  = POLY-4         (LON... |
| **`MAPPOLY_DONE`** | `0x00BB52` | `0x0162C2` | `Polygons.s:356`<br>`Polygons.s:305` | — |
| **`MAPPOLY_NEXTPT`** | `0x00BB42` | `0x0162B2` | `Polygons.s:348`<br>`Polygons.s:297` | MAPPOLY_NEXTPT |
| **`MAPPOLY_NOTSAME`** | `0x00BB24` | `0x016294` | `Polygons.s:330`<br>`Polygons.s:280` | QUIT FAST IF FROMRECT = TORECT |
| **`MAPPOLY_START`** | `0x00BB4E` | `0x0162BE` | `Polygons.s:354`<br>`Polygons.s:303` | — |
| **`MapPt`** | `0x00E56A` | `0x018CF6` | `Pictures.s:2143` | **Proto:** `PROCEDURE MapPt(VAR pt: Point; fromRect,toRect: Rect);`<br>.PROC MapPt PROCEDURE MapPt(VAR pt: Point; fromRect,toRect: Rect); Map a point from one coordinate system to another. pt.h := ((pt.h-fromLeft) * toWidth) / fromWidth + toLeft pt.v := ((pt.v-fromTop) *... |
| **`MAPPT`** | `0x00E56A` | `0x018CF6` | `Pictures.s:1569` | **Proto:** `PROCEDURE MapPt(VAR pt: Point; fromRect, toRect: Rect)`<br>PROCEDURE MapPt(VAR pt: Point; fromRect, toRect: Rect) Map a point from one coordinate system to another. pt.h := ((pt.h-fromLeft)*toWidth)  /fromWidth  + toLeft pt.v := ((pt.v-fromTop) *toHeight) /fr... |
| **`MAPRATIO`** | — | `0x018D70` | `Pictures.s:1638` | MAPRATIO(VAR numer, denom: Point; srcRect: Rect) Adjust txRatio (numer/denom) for a rect-to-rect mapping. Used by GET2_CONT_10 (txRatio opcode) when playing a picture into a destination rect of differ... |
| **`MapRect`** | `0x00E5CC` | `0x018D58` | `Pictures.s:2214` | **Proto:** `PROCEDURE MapRect(VAR dstRect: Rect; fromRect,toRect: Rect);`<br>.PROC MapRect,3 .REF MapPt PROCEDURE MapRect(VAR dstRect: Rect; fromRect,toRect: Rect); Map both points of a rectangle from one coordinate system to another. restores ALL registers. Called by: NOSLOP,... |
| **`MAPRECT`** | `0x00E5CC` | `0x018D58` | `Pictures.s:1623` | **Proto:** `PROCEDURE MapRect(VAR r: Rect; fromRect, toRect: Rect)`<br>PROCEDURE MapRect(VAR r: Rect; fromRect, toRect: Rect) Map both corners of a rect by calling MapPt twice. Manipulates the call-site stack so each MapPt call sees: ptAddr, fromRect, toRect. Called by: ... |
| **`MapRgn`** | `0x00C218` | `0x016988` | `Regions.s:1236` | **Proto:** `PROCEDURE MapRgn(rgn: RgnHandle; fromRect,toRect: Rect);`<br>.PROC MapRgn,3 .REF MapRect,NewHandle,PutRgn,MapPt .REF SortPoints,CullPoints,PackRgn PROCEDURE MapRgn(rgn: RgnHandle; fromRect,toRect: Rect); A6 OFFSETS OF PARAMETERS AND LOCALS AFTER LINK: PARAMSIZE... |
| **`MAPRGN`** | `0x00C218` | `0x016988` | `Regions.s:1017` | **Proto:** `PROCEDURE MapRgn(rgn: RgnHandle; fromRect, toRect: Rect);`<br>PROCEDURE MapRgn(rgn: RgnHandle; fromRect, toRect: Rect); A6 offsets of parameters and locals after LINK: PARAMSIZE = 12 RGN       = PARAMSIZE+8-4  (LONG, RgnHandle) FROMRECT  = RGN-4          (LONG, ... |
| **`MAPRGN_DONE`** | `0x00C2B8` | `0x016A28` | `Regions.s:1338`<br>`Regions.s:1093` | _DisposHandle ;DISCARD IT |
| **`MAPRGN_EXIT`** | `0x00C24C` | `0x0169BC` | `Regions.s:1282`<br>`Regions.s:1041` | SPECIAL CASE RECTANGULAR RGN |
| **`MAPRGN_LOOP`** | `0x00C27E` | `0x0169EE` | `Regions.s:1315`<br>`Regions.s:1072` | MAP ALL INVERSION POINTS MAPRGN_LOOP |
| **`MAPRGN_LOOP_2`** | `0x00C28E` | `0x0169FE` | `Regions.s:1321`<br>`Regions.s:1078` | — |
| **`MAPRGN_NO`** | `0x00C230` | `0x0169A0` | `Regions.s:1269`<br>`Regions.s:1032` | SPECIAL CASE RECTANGULAR RGN |
| **`MAPRGN_NO_2`** | `0x00C24E` | `0x0169BE` | `Regions.s:1289`<br>`Regions.s:1048` | MAPRGN_NO_2 |
| **`MASKOK`** | `0x00CA38` | `0x0171B4` | `Bitmaps.s:200`<br>`Bitmaps.s:181` | — |
| **`MASKTAB`** | — | `0x012B6E` | `Util.s:189` | MASKTAB / LeftMaskTbl / DT_MMASKTAB_CONT_2: 17-entry x 16-bit QuickDraw word-boundary mask tables, each indexed by D0 = bit position 0..16. Returned in a single contiguous block by _GetMaskTable ($A83... |
| **`MeasureText`** | `0x008DF6` | `0x01352C` | `Text.s:604` | **Proto:** `PROCEDURE MeasureText(count: INTEGER; textAddr,charLocs: Ptr);`<br>.PROC MeasureText PROCEDURE MeasureText(count: INTEGER; textAddr,charLocs: Ptr); Measure some text, returning (scaled) screen widths in charlocs. Charlocs points to an array of count+1 integers. PARAM... |
| **`MEASURETEXT`** | `0x008DF6` | `0x01352C` | `Text.s:545` | **Proto:** `PROCEDURE MeasureText(count: INTEGER; textAddr,charLocs: Ptr);`<br>.PROC MeasureText PROCEDURE MeasureText(count: INTEGER; textAddr,charLocs: Ptr); Measure some text, returning (scaled) screen widths in charLocs. Charlocs points to an array of count+1 integers. The S... |
| **`MEASURETEXT_CUSTOM_LOOP`** | — | `0x01355E` | `Text.s:569` | — |
| **`MEASURETEXT_CUSTOM_STORE`** | — | `0x013570` | `Text.s:578` | — |
| **`MEASURETEXT_NEXTCH`** | `0x008E4A` | `0x0135B0` | `Text.s:652`<br>`Text.s:602` | — |
| **`MEASURETEXT_USESTD`** | — | `0x013580` | `Text.s:588` | -- USESTD: inline FMSwapFont + width-table walk ----------------- |
| **`MEMOK`** | `0x00E062` | `0x0187EE` | `Pictures.s:1217`<br>`Pictures.s:917` | _DisposHandle ;DISCARD IT MEMOK |
| **`MERGE10`** | `0x008750` | `0x012E86` | `Util.s:946`<br>`Util.s:656` | MERGE10 |
| **`MERGE11`** | `0x008768` | `0x012E9E` | `Util.s:976`<br>`Util.s:682` | MERGE11 |
| **`MERGE8`** | `0x00873A` | `0x012E70` | `Util.s:917`<br>`Util.s:631` | — |
| **`MINSIZE`** | `0x00E564` | — | `Pictures.s:2117` | — |
| **`MINSIZE_EMPTY`** | `0x00E566` | `0x018CF2` | `Pictures.s:2119`<br>`Pictures.s:1553` | — |
| **`MISSING`** | `0x00927A` | `0x0139EA` | `DrawText.s:471`<br>`DrawText.s:403` | — |
| **`MOD_POS`** | `0x00B7E2` | `0x015F52` | `Angles.s:56`<br>`Angles.s:60` | — |
| **`MODEOK`** | `0x00A2DE` | `0x014A4E` | `BitBlt.s:128`<br>`BitBlt.s:78` | — |
| **`MODETAB`** | `0x00A450` | `0x014BC0` | `BitBlt.s:401`<br>`BitBlt.s:303` | MODETAB |
| **`MOOV`** | — | `0x013EA4` | `Lines.s:153` | **Proto:** `PROCEDURE Move(dh,dv: INTEGER);`<br>.PROC MQVE,2 .DEF Moov PROCEDURE Move(dh,dv: INTEGER); Called during boot. |
| **`MORE`** | `0x00DBDA` | `0x018356` | `Pictures.s:549`<br>`Pictures.s:409` | LEAVE COLRBIT ALONE LEAVE PATSTRETCH ALONE LEAVE PICSAVE ALONE LEAVE RGNSAVE ALONE LEAVE POLYSAVE ALONE LEAVE GRAFPROCS ALONE NOW DRAW THE PICTURE: REPEAT UNTIL NOT PicItem(playState); |
| **`MORE1`** | `0x00C9C0` | `0x01713C` | `Bitmaps.s:154`<br>`Bitmaps.s:136` | NOMASK NOW PUT THE BITMAP DATA: IF NEWROW >= 8 THEN USE PACKBITS MORE1 |
| **`MORE2`** | `0x00C9FC` | `0x017178` | `Bitmaps.s:178`<br>`Bitmaps.s:159` | ROWBYTES < 8, DONT USE PACKBITS |
| **`MORE_LOOP`** | `0x00DBFA` | `0x018376` | `Pictures.s:567`<br>`Pictures.s:421` | DISCARD HANDLES, RESTORE GRAFPORT STATE AND QUIT _DisposHandle ;DISCARD IT |
| **`Move`** | `0x009734` | `0x013EA4` | `Lines.s:156` | **Proto:** `PROCEDURE Move(dh,dv: INTEGER);`<br>.PROC MQVE,2 .DEF Moov PROCEDURE Move(dh,dv: INTEGER); Called during boot. |
| **`MOVE`** | `0x009734` | `0x013EA4` | `Lines.s:152` | **Proto:** `PROCEDURE Move(dh,dv: INTEGER);`<br>.PROC MQVE,2 .DEF Moov PROCEDURE Move(dh,dv: INTEGER); Called during boot. |
| **`MovePortTo`** | `0x008A0E` | `0x013144` | `GrafAsm.s:427` | **Proto:** `PROCEDURE MovePortTo(leftGlobal,topGlobal: INTEGER);`<br>.PROC MovePortTo,2 .DEF SetOrigin,ClipRect .REF OffsetRgn,RectRgn PROCEDURE MovePortTo(leftGlobal,topGlobal: INTEGER); { move portRect to a different part of the bitmap } Called during boot. |
| **`MOVEPORTTO`** | `0x008A0E` | `0x013144` | `GrafAsm.s:422` | **Proto:** `PROCEDURE MovePortTo(leftGlobal,topGlobal: INTEGER);`<br>.PROC MovePortTo,2 .DEF SetOrigin,ClipRect .REF OffsetRgn,RectRgn PROCEDURE MovePortTo(leftGlobal,topGlobal: INTEGER); { move portRect to a different part of the bitmap } Called during boot. |
| **`MoveTo`** | `0x009728` | `0x013E98` | `Lines.s:142` | **Proto:** `PROCEDURE MoveTo(h,v: INTEGER);`<br>.PROC MoveTo PROCEDURE MoveTo(h,v: INTEGER); Called during boot. |
| **`MOVETO`** | `0x009728` | `0x013E98` | `Lines.s:139` | **Proto:** `PROCEDURE MoveTo(h,v: INTEGER);`<br>.PROC MoveTo PROCEDURE MoveTo(h,v: INTEGER); Called during boot. |
| **`NEGSLOPE`** | `0x009A28` | `0x014198` | `DrawLine.s:353`<br>`DrawLine.s:279` | SLOPE IS NEGATIVE |
| **`NEGSLOPE_CONT`** | `0x009A3E` | `0x0141AE` | `DrawLine.s:371`<br>`DrawLine.s:291` | — |
| **`NEGSLOPE_NO`** | `0x009A3A` | `0x0141AA` | `DrawLine.s:369`<br>`DrawLine.s:289` | SLOPE IS NEGATIVE NEGSLOPE_NO |
| **`NEGSLOPE_NO_2`** | `0x009A68` | `0x0141D8` | `DrawLine.s:391`<br>`DrawLine.s:310` | ADJUST LEFTEDGE AND RIGHTEDGE IF LINE WAS CLIPPED VERTICALLY |
| **`NEWBK`** | `0x00E3BA` | `0x018B46` | `Pictures.s:1876`<br>`Pictures.s:1361` | — |
| **`NEWHANDLE`** | `0x01014E` | `0x012EBA` | `GrafAsm.s:21` | --> GRAFASM.TEXT Miscellaneous unclassified routines. In the SE ROM the file starts with QuickDraw's NewHandle (allocate a handle, system error 25 if memory is full). NewHandle: allocate a relocatable... |
| **`NEWMODE`** | `0x0085CA` | `0x012D00` | `Util.s:557`<br>`Util.s:385` | — |
| **`NewRgn`** | `0x00BD4E` | `0x0164BE` | `Regions.s:271` | **Proto:** `FUNCTION NewRgn;`<br>.FUNC NewRgn,0 .REF NewHandle FUNCTION NewRgn; Allocate a new region and set it to the empty region. Called during boot (4,158 times in 30s trace). |
| **`NEWRGN`** | `0x00BD4E` | `0x0164BE` | `Regions.s:226` | **Proto:** `FUNCTION NewRgn;`<br>FUNCTION NewRgn; Allocate a new region and set it to the empty region. Called by: OPENPORT, SCROLLRECT, DRAWPICTURE_LOOP, DRAWPOLY, FRRGN_NOTRECT (and 2 more) |
| **`NEXT`** | `0x00C60E` | `0x016D7E` | `RgnOp.s:381`<br>`RgnOp.s:336` | — |
| **`NEXT10`** | `0x0086F2` | `0x012E28` | `Util.s:842`<br>`Util.s:572` | — |
| **`NEXT10_CONT`** | `0x0086FC` | `0x012E32` | `Util.s:848`<br>`Util.s:578` | — |
| **`NEXT11`** | `0x008704` | `0x012E3A` | `Util.s:860`<br>`Util.s:585` | — |
| **`NEXT11_CONT`** | `0x008710` | `0x012E46` | `Util.s:867`<br>`Util.s:592` | — |
| **`NEXT8`** | `0x0086C6` | `0x012DFC` | `Util.s:802`<br>`Util.s:542` | INTERFACE TO EACH SCAN LINE ROUTINE: ENTER WITH Z-FLAG SET IF ALL IN ONE WORD INPUTS: A1: DSTPTR A2: MASKPTR D1: LEFTMASK D2: WORDCNT D3: RIGHTMASK D6: PATTERN CLOBBERS: D0,D1,D2,A1,A2 MODE 8 OR 12: P... |
| **`NEXT8_CONT`** | `0x0086D8` | `0x012E0E` | `Util.s:812`<br>`Util.s:552` | — |
| **`NEXT9`** | `0x0086E0` | `0x012E16` | `Util.s:824`<br>`Util.s:559` | — |
| **`NEXT9_CONT`** | `0x0086EA` | `0x012E20` | `Util.s:830`<br>`Util.s:565` | — |
| **`NEXTBUF`** | `0x00CDAC` | `0x017528` | `Bitmaps.s:707`<br>`Bitmaps.s:593` | NOSEED allocate a scanline buffer of ones or zeros on the stack: |
| **`NEXTCH`** | `0x00925A` | `0x0139CA` | `DrawText.s:459`<br>`DrawText.s:391` | Here's the main character drawing loop: |
| **`NEXTCH2`** | `0x008E6A` | `0x0135DA` | `Text.s:669`<br>`Text.s:618` | if font is horizontally stretched, scale all widths accordingly |
| **`NEXTCH2_SKIP`** | `0x008E76` | `0x0135E6` | `Text.s:675`<br>`Text.s:624` | — |
| **`NEXTDST`** | `0x00D388` | `0x017B04` | `Stretch.s:525`<br>`Stretch.s:397` | TRANSFER ONE OR MORE COPIES OF DSTBUF INTO DSTBITS NEXTDST Called during boot. |
| **`NEXTDST_SKIP`** | `0x00D390` | `0x017B0C` | `Stretch.s:528`<br>`Stretch.s:400` | — |
| **`NEXTHEX`** | `0x008630` | `0x012D66` | `Util.s:627`<br>`Util.s:443` | NEXTHEX -- gET HEX DIGIT AND CONVERT TO BINARY. NEXTHEX |
| **`NEXTHOR`** | `0x00C114` | `0x016884` | `Regions.s:1024`<br>`Regions.s:842` | — |
| **`NEXTHOR_EXIT`** | `0x00C124` | `0x016894` | `Regions.s:1038`<br>`Regions.s:855` | NEXTHOR_EXIT Called during boot (4,005 times in 30s trace). |
| **`NEXTPT`** | `0x00C814` | `0x017006` | `PackRgn.s:129`<br>`PackRgn.s:126` | EXPAND DSTRGN TO HOLD WORST CASE = 12 + 4*NPOINTS bytes. NEWLY DE-REFERENCE SRC AND DST HANDLES NEXTPT Called during boot (170,308 times in 30s trace). |
| **`NEXTRECT`** | `0x00A12A` | `0x01489A` | `Rects.s:585`<br>`Rects.s:483` | NEXTRECT Called during boot (12,436 times in 30s trace). |
| **`NEXTROW`** | `0x00A418` | `0x014B88` | `BitBlt.s:350`<br>`BitBlt.s:257` | OUTER LOOP: DO EACH SCAN LINE AND COME BACK TO NXTSRC OR NXTPAT. SOME MODES OPTIMIZE AND DO WHOLE OUTER LOOP AND COME BACK TO GOHOME. Called during boot. |
| **`NEXTSRC`** | `0x00D2DE` | `0x017A5A` | `Stretch.s:420`<br>`Stretch.s:324` | CALC STARTING DSTROW, DSTSHIFT, AND DSTADDR INIT ERROR TERM FOR DDA GET FIRST SCANLINE OF SRC INTO SRCBUF Called during boot. |
| **`NEXTSRC_LOOP`** | `0x00D2F2` | `0x017A6E` | `Stretch.s:426`<br>`Stretch.s:330` | — |
| **`NIBBLE_DOUBLE_TBL`** | — | `0x017E42` | `Stretch.s:898` | NIBBLE_DOUBLE_TBL -- 4-bit nibble -> 8-bit doubled output for 2x stretch. 16 entries: each input bit replicated to 2 output bits. E.g. 0001 -> 00000011 (0x03), 1010 -> 11001100 (0xCC). |
| **`NOBUMP`** | `0x00B440` | `0x015BB0` | `DrawArc.s:702`<br>`DrawArc.s:516` | ADJUST ARC STUFF AS WE CROSS THE MIDDLE VERTICALLY Called during boot. |
| **`NOCHNG`** | `0x009E54` | `0x0145C4` | `PutLine.s:168`<br>`PutLine.s:149` | — |
| **`NOCHNG_EXIT`** | `0x009E6A` | `0x0145DA` | `PutLine.s:185`<br>`PutLine.s:165` | FINISH UP LAST SLAB |
| **`NOCOLOR`** | `0x00B068` | `0x0157D8` | `DrawArc.s:128`<br>`DrawArc.s:53` | QUIT IF MODE NOT IN 8..15 ADJUST MODE AND PATTERN IF COLOR FILTERING. |
| **`NODRAW`** | `0x00B620` | `0x015D90` | `DrawArc.s:984`<br>`DrawArc.s:736` | BUMP DESTINATION VERTICALLY AND LOOP FOR ALL SCAN LINES |
| **`NOGROW`** | `0x00C88E` | — | `PutRgn.s:48` | EXPAND BUF TO FIT WORST CASE BYTESNEEDED = RGNSIZE * 2 |
| **`NOMASK`** | `0x00B4C0` | `0x015C30` | `DrawArc.s:775`<br>`DrawArc.s:569` | Seek mask to the current vertical, and branch based on solid or hollow oval or arc. |
| **`NOMASK_CONT`** | `0x00B594` | `0x015D04` | `DrawArc.s:885`<br>`DrawArc.s:657` | NOT3 |
| **`NOMASK_NO`** | `0x00B560` | `0x015CD0` | `DrawArc.s:858`<br>`DrawArc.s:636` | IF OUTERLEFT < OUTERRIGHT THEN PAINT TWO SLABS HOLLOW ARC: CALC INNERLEFT AND INNERRIGHT ELSE IF BOTH LINES ACTIVE AND ANGLE > 180 THEN PAINT TWO OR THREE SLABS |
| **`NOMASK_NO_2`** | `0x00B582` | `0x015CF2` | `DrawArc.s:877`<br>`DrawArc.s:650` | ELSE IF BOTH LINES ACTIVE AND ANGLE > 180 THEN PAINT TWO OR THREE SLABS NOMASK_NO_2 |
| **`NOMASK_NO_3`** | `0x00B596` | `0x015D06` | `DrawArc.s:887`<br>`DrawArc.s:659` | — |
| **`NOMASK_OK`** | `0x00B4DA` | `0x015C4A` | `DrawArc.s:788`<br>`DrawArc.s:581` | NOMASK_OK |
| **`NOMASK_SKIP`** | `0x00B4EE` | `0x015C5E` | `DrawArc.s:800`<br>`DrawArc.s:588` | SOLID OR HOLLOW ARC: CALC OUTERLEFT AND OUTERRIGHT |
| **`NOMASK_SKIP_2`** | `0x00B506` | `0x015C76` | `DrawArc.s:808`<br>`DrawArc.s:596` | — |
| **`NOMASK_SKIP_3`** | `0x00B52E` | `0x015C9E` | `DrawArc.s:830`<br>`DrawArc.s:612` | SOLID OR HOLLOW ARC: CALC OUTERLEFT AND OUTERRIGHT HOLLOW ARC: CALC INNERLEFT AND INNERRIGHT |
| **`NOMASK_SKIP_4`** | `0x00B546` | `0x015CB6` | `DrawArc.s:838`<br>`DrawArc.s:620` | — |
| **`NOMATCH`** | `0x00D5B4` | `0x017D30` | `Stretch.s:906`<br>`Stretch.s:723` | check for any multiple of 8: NOMATCH |
| **`NOPACK`** | `0x00C974` | `0x0170F0` | `Bitmaps.s:115`<br>`Bitmaps.s:101` | — |
| **`NOPACK_SKIP`** | `0x00C9AE` | `0x01712A` | `Bitmaps.s:137`<br>`Bitmaps.s:122` | NOMASK NOW PUT THE BITMAP DATA: IF NEWROW >= 8 THEN USE PACKBITS |
| **`NORMAL`** | `0x0084D8` | `0x012C0E` | `Util.s:401`<br>`Util.s:257` | VERTOK ANY OTHER, USE NORMAL NORMAL PATTERN. SIMPLY REPLICATE THE 8 BY 8 PATTERN. Called during boot (3,160 times in 30s trace). |
| **`NOSCALE`** | `0x00E5C6` | `0x018D52` | `Pictures.s:2199`<br>`Pictures.s:1610` | — |
| **`NOSEED`** | `0x00CDA6` | `0x017522` | `Bitmaps.s:699`<br>`Bitmaps.s:590` | clear one dst pixel at seedH,seedV NOSEED allocate a scanline buffer of ones or zeros on the stack: |
| **`NOSHAD`** | `0x009624` | `0x013D94` | `DrawText.s:1038`<br>`DrawText.s:911` | restore altered srcBits Push params and call StretchBits to transfer buffer to screen Called during boot. |
| **`NOSHAD_EXIT`** | `0x009656` | `0x013DC6` | `DrawText.s:1061`<br>`DrawText.s:927` | Called by: NOSTRCH, DRTEXT_NOTFAST_CONT, DRTEXT, DRTEXT_NOCOLOR, STRDONE |
| **`NOSHAD_NO`** | `0x009642` | `0x013DB2` | `DrawText.s:1055`<br>`DrawText.s:920` | restore altered srcBits Push params and call StretchBits to transfer buffer to screen |
| **`NOSLOP`** | `0x008FA2` | `0x013712` | `DrawText.s:146`<br>`DrawText.s:108` | — |
| **`NOSTRCH`** | `0x00901C` | `0x01378C` | `DrawText.s:188`<br>`DrawText.s:147` | Check for stretching We will be stretching. Setup fromRect and toRect and map textR2. |
| **`NOSWAP`** | `0x009E08` | `0x014578` | `PutLine.s:105`<br>`PutLine.s:92` | — |
| **`NOSWAP_NO`** | `0x009E42` | `0x0145B2` | `PutLine.s:157`<br>`PutLine.s:138` | SLOPEOK FOR VERT:=TOPV TO BOTV-1 ADD SLOPE TO HORIZ AND PUT SLABS |
| **`NOSWAP_OK`** | `0x009E38` | `0x0145A8` | `PutLine.s:146`<br>`PutLine.s:129` | NOSWAP_OK |
| **`NOTARC`** | `0x00B250` | `0x0159C0` | `DrawArc.s:418`<br>`DrawArc.s:298` | OBTUSE NOTARC INIT OUTER OVAL STATE RECORD Called during boot. |
| **`NOTEMPTY`** | `0x00C058` | `0x0167C8` | `Regions.s:887`<br>`Regions.s:730` | THE BOUNDING BOXES DON'T INTERSECT. IF OP = SectScan, THEN RETURN EMPTY. IF OP = DIFF, THEN COPY RGNA INTO DSTRGN. IF OP = SectScan, THEN CHECK FOR BOTH INPUTS RECTANGULAR Called during boot (10,182 t... |
| **`NOTEND`** | `0x00DC3C` | `0x0183B8` | `Pictures.s:658`<br>`Pictures.s:463` | GET PICTURE OPCODE AND CHECK FOR END OF PICTURE. NOTEND |
| **`NOTEND_CONT`** | `0x00DC64` | — | `Pictures.s:682` | CHECK FOR PARAM OPCODES $00..$1F GET LO AND HI NIBBLES OF OPCODE, AND CASE ON HI NIBBLE (NOUN). NOTEND_CONT |
| **`NOTEND_CONT_2`** | `0x00DC94` | — | `Pictures.s:704` | OPCODES $00..$1F DO NO DRAWING, THEY JUST SET PARAMETERS. NOTEND_CONT_2 |
| **`NOTEND_CONT_3`** | `0x00DCD4` | `0x018450` | `Pictures.s:717`<br>`Pictures.s:520` | NOTEND_CONT_3 -- $01 clipRgn opcode handler |
| **`NOTEND_OK`** | `0x00DC86` | `0x018402` | `Pictures.s:689`<br>`Pictures.s:492` | NOTEND_OK -- handle a state-setting param opcode ($00..$1F) |
| **`NOTFAST`** | `0x009978` | `0x0140E8` | `DrawLine.s:250`<br>`DrawLine.s:192` | NOT FASTLINE. PUSH PARAMS AND CALL RGNBLT FOR HORIZ OR VERT LINE. Called during boot. |
| **`NOTFR`** | `0x00ADB4` | `0x015524` | `Ovals.s:80`<br>`Ovals.s:71` | NOTFR |
| **`NOTIN1`** | `0x00C3AC` | `0x016B1C` | `SeekRgn.s:170`<br>`SeekRgn.s:152` | NOT ALL IN ONE WORD. DO LEFT, MIDDLE IF ANY, THEN RIGHT Called during boot. |
| **`NOTMISS`** | `0x00929A` | `0x013A0A` | `DrawText.s:490`<br>`DrawText.s:421` | — |
| **`NOTMISS_NO`** | `0x0092C6` | `0x013A36` | `DrawText.s:518`<br>`DrawText.s:448` | NOHEIGHT \| DIVIDE BY 8 Horizontal clip only if FastFlag: (else stretch,outline,shadow,italic die) skip if hidden on left, string done if hidden on right. at this point: D1: srcLeft D2: dstRight D3: ds... |
| **`NOTMISS_NO_2`** | `0x0092EC` | `0x013A5C` | `DrawText.s:551`<br>`DrawText.s:467` | NOTMISS_NO_2 Called during boot. |
| **`NOTNEG`** | `0x00E5BA` | `0x018D46` | `Pictures.s:2192`<br>`Pictures.s:1603` | LOCAL ROUTINE TO MAP A SINGLE COORDINATE: |
| **`NOTPIC`** | `0x00AF8E` | `0x0156FE` | `Arcs.s:52`<br>`Arcs.s:53` | — |
| **`NOTPOLY`** | `0x009792` | `0x013F02` | `Lines.s:212`<br>`Lines.s:206` | IF NOT POLY, THEN CHECK FOR RGNSAVE. IF RGNSAVE THEN PutLine(oldPt,newPt,rgnBuf,rgnIndex,rgnMax); Called during boot. |
| **`NOTPORT`** | `0x00CA90` | `0x01720C` | `Bitmaps.s:279`<br>`Bitmaps.s:238` | TEST IF DST IS TO THEPORT, (IF SO WE CLIP) DST IS DEFINITELY NOT TO THEPORT, SO WE CAN'T USE THE CAPTURE PROC. StretchBits(srcBits,dstBits,srcRect,dstRect,mode,wideOpen,wideOpen,maskRgn); Called durin... |
| **`NOTRECT`** | `0x00CBB2` | `0x01732E` | `Bitmaps.s:442`<br>`Bitmaps.s:370` | IF REGION WAS RECTANGULAR, DRAW TOP SCANLINE INTO ITS BUFFER AND SET UP THISV AND NEXTV SO SEEKRGN DOES NOTHING |
| **`NOTRGN`** | `0x00C96E` | `0x0170EA` | `Bitmaps.s:111`<br>`Bitmaps.s:97` | RIGHTOK CALC NEW ROWBYTES AFTER TRIMMING FIXED BUG 12/3/83, RP |
| **`NOTSAME`** | `0x00E314` | `0x018AA0` | `Pictures.s:1786`<br>`Pictures.s:1286` | NOTSAME |
| **`NOTSET`** | `0x0097E8` | `0x013F58` | `Lines.s:281`<br>`Lines.s:271` | — |
| **`NOTSRC`** | `0x00A374` | `0x014AE4` | `BitBlt.s:239`<br>`BitBlt.s:159` | SET UP SRCLEFT IN A4, ADDR OF LEFTMOST SRC WORD (GOODBYE SRCBITS PTR) SET UP DSTLEFT IN A5, ADDR OF LEFTMOST DST WORD (GOODBYE DSTBITS PTR) Called during boot. |
| **`NOTUL`** | `0x009500` | `0x013C70` | `DrawText.s:891`<br>`DrawText.s:783` | — |
| **`NXTBOLD`** | `0x009432` | `0x013BA2` | `DrawText.s:771`<br>`DrawText.s:670` | — |
| **`NXTBYTE`** | `0x00D94E` | `0x0180CA` | `Pictures.s:100`<br>`Pictures.s:89` | NXTBYTE |
| **`NXTCOPY`** | `0x00CFC2` | `0x01773E` | `Bitmaps.s:1066`<br>`Bitmaps.s:895` | NXTCOPY |
| **`NXTFILL`** | `0x00CFEE` | `0x01776A` | `Bitmaps.s:1096`<br>`Bitmaps.s:924` | — |
| **`NXTHOR`** | `0x00C8A6` | `0x016F5A` | `PutRgn.s:66`<br>`PutRgn.s:62` | — |
| **`NXTLONG`** | `0x00C190` | `0x016900` | `Regions.s:1127`<br>`Regions.s:926` | — |
| **`NXTMASK`** | `0x009BCE` | `0x01433E` | `DrawLine.s:577`<br>`DrawLine.s:467` | FOR EACH SLAB, MAKE MASK BUFFER CURRENT AND DRAW SLAB |
| **`NXTPASS`** | `0x00CDBA` | `0x017536` | `Bitmaps.s:712`<br>`Bitmaps.s:598` | — |
| **`NXTROW`** | `0x009454` | `0x013BC4` | `DrawText.s:795`<br>`DrawText.s:692` | Slant the buffer if necessary: Work from bottom of buffer up, shifting each row right. Work right to left to avoid clobbering src. NXTROW |
| **`NXTSRC`** | `0x00A426` | `0x014B96` | `BitBlt.s:370`<br>`BitBlt.s:270` | NXTSRC Called during boot (1,458 times in 30s trace). |
| **`NXTSRC1`** | `0x00D870` | `0x017FEC` | `Stretch.s:1338`<br>`Stretch.s:1154` | — |
| **`NXTSRC1_CONT`** | `0x00D87C` | `0x017FF8` | `Stretch.s:1345`<br>`Stretch.s:1161` | — |
| **`NXTSRC2`** | `0x00D89C` | `0x018018` | `Stretch.s:1373`<br>`Stretch.s:1184` | DO FULL RATIO SCALING, STRETCHING ONE BIT AT A TIME |
| **`NXTSRC_NEXT`** | `0x00A432` | `0x014BA2` | `BitBlt.s:381`<br>`BitBlt.s:280` | NXTSRC_NEXT Called during boot (7,476 times in 30s trace). |
| **`NXTVERT`** | `0x00AE8C` | `0x0155FC` | `PutOval.s:126`<br>`PutOval.s:82` | PUT THE TOP EDGE FOR EACH VERTICAL, BUMP LEFTEDGE AND RIGHTEDGE. IF THEY DIFFER FROM OLDLEFT AND OLDRIGHT, PUT INVERSION POINTS FOR THE DIFFERENCES Called during boot. |
| **`NXTWORD`** | `0x00946A` | `0x013BDA` | `DrawText.s:807`<br>`DrawText.s:704` | — |
| **`ObscureCursor`** | `0x00832E` | `0x012A64` | `LCursor.s:112` | **Proto:** `PROCEDURE ObscureCursor;`<br>.PROC ObscureCursor PROCEDURE ObscureCursor; Hide the cursor image until the next time the mouse moves. |
| **`OBSCURECURSOR`** | `0x00832E` | `0x012A64` | `LCursor.s:78` | **Proto:** `Pascal: procedure ObscureCursor;`<br>OBSCURECURSOR ($A856) - hide cursor until mouse moves Pascal: procedure ObscureCursor; |
| **`OffsetPoly`** | `0x00BAE8` | `0x016258` | `Polygons.s:281` | **Proto:** `PROCEDURE OffsetPoly(poly: PolyHandle; dh,dv: INTEGER);`<br>_DisposHandle ;discard it .PROC OffsetPoly PROCEDURE OffsetPoly(poly: PolyHandle; dh,dv: INTEGER); |
| **`OFFSETPOLY`** | `0x00BAE8` | `0x016258` | `Polygons.s:241` | **Proto:** `PROCEDURE OffsetPoly(poly: PolyHandle; dh,dv: INTEGER);`<br>PROCEDURE OffsetPoly(poly: PolyHandle; dh,dv: INTEGER); |
| **`OFFSETPOLY_NEXTPT`** | `0x00BAFA` | `0x01626A` | `Polygons.s:291`<br>`Polygons.s:251` | — |
| **`OffsetRect`** | `0x00A0C4` | `0x014834` | `Rects.s:486` | **Proto:** `PROCEDURE OffsetRect(VAR r: Rect; dh,dv: INTEGER);`<br>.PROC OffsetRect PROCEDURE OffsetRect(VAR r: Rect; dh,dv: INTEGER); Called during boot. |
| **`OFFSETRECT`** | `0x00A0C4` | `0x014834` | `Rects.s:402` | **Proto:** `PROCEDURE OffsetRect(VAR r: Rect; dh,dv: INTEGER);`<br>.PROC OffsetRect PROCEDURE OffsetRect(VAR r: Rect; dh,dv: INTEGER); Called during boot. |
| **`OFFSETRGN`** | — | `0x016632` | `Regions.s:416` | **Proto:** `PROCEDURE OffsetRgn(rgn: RgnHandle; dh,dv: INTEGER);`<br>PROCEDURE OffsetRgn(rgn: RgnHandle; dh,dv: INTEGER); |
| **`OFFSETRGN_DONE`** | `0x00BEF2` | `0x016662` | `Regions.s:541`<br>`Regions.s:447` | — |
| **`OFFSETRGN_NXTHOR`** | `0x00BEE0` | `0x016650` | `Regions.s:533`<br>`Regions.s:439` | OFFSET THE BOUNDING BOX IF NON-RECTANGULAR REGION, OFFSET THE COORDINATES TOO. |
| **`OFFSETRGN_NXTVERT`** | `0x00BEDE` | `0x01664E` | `Regions.s:531`<br>`Regions.s:437` | OFFSET THE BOUNDING BOX IF NON-RECTANGULAR REGION, OFFSET THE COORDINATES TOO. |
| **`OfsetRgn`** | `0x00BEC2` | — | `Regions.s:508` | **Proto:** `PROCEDURE OffsetRgn(rgn: RgnHandle; dh,dv: INTEGER);`<br>.PROC OffsetRgn PROCEDURE OffsetRgn(rgn: RgnHandle; dh,dv: INTEGER); Called during boot. |
| **`OFSPORT`** | `0x008A2C` | `0x013162` | `GrafAsm.s:438`<br>`GrafAsm.s:433` | OFSPORT -- oFFSET PORTBITS.BOUNDS. |
| **`OFSRECT`** | `0x008A30` | `0x013166` | `GrafAsm.s:441`<br>`GrafAsm.s:436` | OFSRECT -- oFFSET PORTRECT. |
| **`OK1`** | `0x00B6BA` | `0x015E2A` | `DrawArc.s:1091`<br>`DrawArc.s:842` | INIT OVAL TOP AND BOTTOM TO DSTRECT TOP AND BOTTOM |
| **`OK1_NO`** | `0x00B6C0` | `0x015E30` | `DrawArc.s:1100`<br>`DrawArc.s:850` | OK2 CHECK OVALWIDTH AND OVALHEIGHT, TRIM IF BIGGER THAN DSTRECT Called during boot. |
| **`OK3`** | `0x00B81E` | `0x015F8E` | `Angles.s:82`<br>`Angles.s:86` | — |
| **`OKCHAR`** | `0x00928E` | `0x0139FE` | `DrawText.s:485`<br>`DrawText.s:416` | OKCHAR Called during boot. |
| **`OKRECT`** | `0x00A7C0` | `0x014F30` | `RgnBlt.s:184`<br>`RgnBlt.s:103` | If only rgnB (visRgn) is non-rectangular, then check if its intersection with minrect would be rectangular. IF TrimRect(rgnB,minRect) then take the fast way. SINCE ALL THREE REGIONS ARE RECTANGULAR, W... |
| **`OKRECT_NO`** | `0x00A802` | `0x014F72` | `RgnBlt.s:224`<br>`RgnBlt.s:132` | OKRECT_NO Called during boot. |
| **`ONESLAB`** | `0x00B5AA` | `0x015D1A` | `DrawArc.s:902`<br>`DrawArc.s:671` | **Proto:** `LOCAL PROCEDURE TO SET UP AND DRAW ONE SLAB`<br>NOT3 LOCAL PROCEDURE TO SET UP AND DRAW ONE SLAB Called during boot (1,086 times in 30s trace). |
| **`ONLY2`** | `0x0094A8` | `0x013C18` | `DrawText.s:840`<br>`DrawText.s:735` | — |
| **`OpenPicture`** | `0x00D9EC` | `0x018168` | `Pictures.s:225` | **Proto:** `FUNCTION OpenPicture(picFrame: Rect): PicHandle;`<br>.FUNC OpenPicture,1 .REF HidePen,NewRgn,PutPicWord,EqualRgn,ClipRect FUNCTION OpenPicture(picFrame: Rect): PicHandle; A6 OFFSETS OF PARAMS AFTER LINK: PARAMSIZE .EQU 4 RESULT .EQU PARAMSIZE+8 ;LONG, P... |
| **`OPENPICTURE`** | `0x00D9EC` | `0x018168` | `Pictures.s:199` | **Proto:** `FUNCTION OpenPicture(picFrame: Rect): PicHandle;`<br>FUNCTION OpenPicture(picFrame: Rect): PicHandle; Opens a new picture for recording. Allocates the PicSave record and the picture handle (initial 256 bytes), seeds the picture header (size, frame, vers... |
| **`OPENPICTURE_DONE`** | `0x00DA9E` | `0x01821A` | `Pictures.s:327`<br>`Pictures.s:258` | — |
| **`OpenPoly`** | `0x00BA3E` | `0x0161AE` | `Polygons.s:166` | **Proto:** `FUNCTION OpenPoly: PolyHandle;`<br>.FUNC OpenPoly,0 .REF HidePen,NewHandle FUNCTION OpenPoly: PolyHandle; STARTSIZE .EQU 138 ;ENOUGH FOR 32 POINTS |
| **`OPENPOLY`** | `0x00BA3E` | `0x0161AE` | `Polygons.s:141` | **Proto:** `FUNCTION OpenPoly: PolyHandle;`<br>FUNCTION OpenPoly: PolyHandle; STARTSIZE = 138 (enough for 32 points) |
| **`OpenPort`** | `0x00886C` | `0x012FA2` | `GrafAsm.s:153` | **Proto:** `PROCEDURE OpenPort(port: GrafPtr);`<br>.PROC OpenPort,1 .REF NewRgn PROCEDURE OpenPort(port: GrafPtr); { allocate clipRgn and visRgn, then call InitPort. Called during boot. |
| **`OPENPORT`** | `0x00886C` | `0x012FA2` | `GrafAsm.s:161` | **Proto:** `PROCEDURE OpenPort(port: GrafPtr);`<br>.PROC OpenPort,1 .REF NewRgn PROCEDURE OpenPort(port: GrafPtr); { allocate clipRgn and visRgn, then call InitPort. Called during boot. |
| **`OpenRgn`** | `0x00BD7A` | `0x0164EA` | `Regions.s:307` | **Proto:** `PROCEDURE OpenRgn;`<br>_DisposHandle ;discard it .PROC OpenRgn,0 .REF NewHandle,HidePen PROCEDURE OpenRgn; Called during boot. |
| **`OPENRGN`** | `0x00BD7A` | `0x0164EA` | `Regions.s:252` | **Proto:** `PROCEDURE OpenRgn;`<br>PROCEDURE OpenRgn; |
| **`ORIGNOK`** | `0x00E4DC` | `0x018C68` | `Pictures.s:2016`<br>`Pictures.s:1477` | BKCOLOK CHECK FOR ORIGIN CHANGES CHECK FOR CLIPRGN CHANGES |
| **`ORIGNOK_EXIT_2`** | `0x00E50C` | `0x018C98` | `Pictures.s:2033`<br>`Pictures.s:1494` | — |
| **`ORMODE`** | `0x00858A` | — | `Util.s:505` | THE XOR MODES DEPEND ON NEITHER FOREGROUND OR BACKGROUND COLOR ELSE MUST BE OR THE OR MODES DEPEND ONLY ON THE FOREGROUND COLOR Called during boot. |
| **`OUTLOOP`** | `0x00C66A` | `0x016DDA` | `RgnOp.s:495`<br>`RgnOp.s:422` | GET EACH PAIR OF COORDS, OUTSET THEM, AND CANCEL IF THEY CROSS. OUTLOOP |
| **`OUTOK`** | `0x00C67A` | `0x016DEA` | `RgnOp.s:509`<br>`RgnOp.s:435` | OUTOK |
| **`OUTOK2`** | `0x00C67C` | `0x016DEC` | `RgnOp.s:511`<br>`RgnOp.s:437` | — |
| **`OUTOK2_EXIT`** | `0x00C686` | `0x016DF6` | `RgnOp.s:517`<br>`RgnOp.s:443` | — |
| **`OUTOK2_LOOP`** | `0x00C680` | `0x016DF0` | `RgnOp.s:514`<br>`RgnOp.s:440` | — |
| **`OUTSET`** | `0x00C664` | `0x016DD4` | `RgnOp.s:482`<br>`RgnOp.s:415` | GET EACH PAIR OF COORDS, INSET THEM, AND CANCEL IF THEY CROSS. GET EACH PAIR OF COORDS, OUTSET THEM, AND CANCEL IF THEY CROSS. |
| **`OUTTEST`** | `0x00C540` | `0x016CB0` | `RgnOp.s:246`<br>`RgnOp.s:217` | — |
| **`OUTTEST_NO`** | `0x00C590` | `0x016D00` | `RgnOp.s:282`<br>`RgnOp.s:250` | THE POINT BUFFER IS FULL, GROW IT IF OKGROW IS TRUE |
| **`OVALOK`** | `0x00ACA8` | `0x015418` | `RRects.s:54`<br>`RRects.s:58` | CHECK FOR NEW OVAL SIZE |
| **`OVALOP`** | `0x00DF58` | `0x0186E4` | `Pictures.s:1085`<br>`Pictures.s:803` | Oval: OP, RECT |
| **`OVALOP_OK`** | `0x00DF6E` | `0x0186FA` | `Pictures.s:1093`<br>`Pictures.s:811` | — |
| **`OVERFLO`** | `0x00DACE` | — | `Pictures.s:354` | — |
| **`P_CrsrObscure`** | `0x001C9A` | `0x018DCC` | `CrsrCore.s:36`<br>`CrsrCore.s:55` | P_CrsrObscure - Hide cursor and mark as obscured Called by _ObscureCursor trap. Sets the CrsrObscure flag so the cursor stays hidden until the next mouse movement. |
| **`P_HideCursor`** | `0x001CA8` | `0x018DDA` | `CrsrCore.s:48`<br>`CrsrCore.s:67` | P_HideCursor - Erase cursor from screen, decrement CrsrState Restores saved background pixels under the cursor rectangle, clears CrsrVis, and decrements CrsrState (hide depth counter). |
| **`P_InitCrsr`** | — | `0x018E1E` | `CrsrCore.s:102` | P_InitCrsr - Initialize cursor state at boot Sets CrsrObscure and CrsrState to 0, leaves CrsrBusy set so the next ShowCursor can come up safely. |
| **`P_ScrnAddress`** | `0x001E5A` | — | `CrsrCore.s:294` | P_ScrnAddress - ScrnAddress: return the screen base address (MacSEROM.lst: SCRNADDRESS; MacPlusROM.lst lists ScrnAddress at the unimplemented-trap handler, where that name is a label) Stack: retAddr, ... |
| **`P_ScrnSize`** | `0x001E62` | — | `CrsrCore.s:307` | P_ScrnSize - ScrnSize: return screen dimensions (height and width) (MacSEROM.lst: SCRNSIZE; MacPlusROM.lst lists ScrnSize at the unimplemented-trap handler, where that name is a label) Stack: retAddr,... |
| **`P_SetCrsr`** | — | `0x018F3C` | `CrsrCore.s:259` | P_SetCrsr - Install a new cursor (data + mask + hotspot) Compares each longword of the new cursor with the installed TheCrsr; if any differ, increment change counter and copy. Clamps hotspot to 16x16.... |
| **`P_ShieldCursor`** | `0x001DC8` | `0x018EFA` | `CrsrCore.s:203`<br>`CrsrCore.s:218` | P_ShieldCursor - Temporarily hide cursor if it overlaps a rectangle Called before drawing into a screen area. If the cursor's bounding rectangle (CrsrRect) intersects the shield rectangle passed on th... |
| **`P_ShowCursor`** | `0x001CFA` | `0x018E2C` | `CrsrCore.s:98`<br>`CrsrCore.s:115` | P_ShowCursor - Draw cursor on screen, increment CrsrState Computes cursor screen position from Mouse and hotspot, clips to screen bounds, saves background pixels, then XORs cursor data with mask onto ... |
| **`PackBits`** | `0x00CF8C` | `0x017708` | `Bitmaps.s:1025` | **Proto:** `PROCEDURE PackBits(VAR srcPtr,dstPtr: Ptr; srcBytes: INTEGER);`<br>.PROC PackBits .DEF UnpackBits PROCEDURE PackBits(VAR srcPtr,dstPtr: Ptr; srcBytes: INTEGER); Packs one scanline of data, compressing equal bytes. Returns updated srcPtr and dstPtr. Equates for parame... |
| **`PACKBITS`** | `0x00CF8C` | `0x017708` | `Bitmaps.s:862` | **Proto:** `PROCEDURE PackBits(VAR srcPtr, dstPtr: Ptr; srcBytes: INTEGER);`<br>PROCEDURE PackBits(VAR srcPtr, dstPtr: Ptr; srcBytes: INTEGER); Packs one scanline of data, compressing equal bytes. Returns updated srcPtr and dstPtr. Equates for parameters are shared with UnpackBit... |
| **`PackRgn`** | `0x00C78E` | `0x016F80` | `PackRgn.s:20` | **Proto:** `PROCEDURE PackRgn(srcHandle: Handle; nPoints: INTEGER; dstRgn: RgnHandle);`<br>.PROC PACKRGN,3 .REF SETSIZE PROCEDURE PackRgn(srcHandle: Handle; nPoints: INTEGER; dstRgn: RgnHandle); Converts a sorted array of inversion points into a region. Calls storage allocator to make more ... |
| **`PACKRGN`** | `0x00C78E` | `0x016F80` | `PackRgn.s:44` | **Proto:** `PROCEDURE PackRgn(srcHandle: Handle; nPoints: INTEGER;`<br>.PROC PACKRGN,3 .REF SETSIZE PROCEDURE PackRgn(srcHandle: Handle; nPoints: INTEGER; dstRgn: RgnHandle); Converts a sorted array of inversion points into a region. Calls storage allocator to make more ... |
| **`PACKRGN_DONE`** | `0x00C830` | `0x017022` | `PackRgn.s:150`<br>`PackRgn.s:145` | INSTALL RGNSIZE AND RGNBBOX. Called during boot (7,415 times in 30s trace). |
| **`PACKRGN_LOOP`** | `0x00C7D2` | `0x016FC4` | `PackRgn.s:71`<br>`PackRgn.s:76` | MORE THAN FOUR POINTS, NON-RECTANGULAR. SCAN FOR BBOX LEFT AND RIGHT. |
| **`PACKRGN_NO`** | `0x00C7C6` | `0x016FB8` | `PackRgn.s:61`<br>`PackRgn.s:71` | A6 OFFSETS OF LOCAL VARIABLES AFTER LINK: CHECK NPOINTS TO SPECIAL CASE EMPTY AND RECTANGULAR REGIONS. PACKRGN_NO Called during boot (7,410 times in 30s trace). |
| **`PACKRGN_NO_2`** | `0x00C7E0` | `0x016FD2` | `PackRgn.s:85`<br>`PackRgn.s:88` | PACKRGN_NO_2 Called during boot (177,703 times in 30s trace). |
| **`PACKRGN_SIZEOK`** | `0x00C848` | `0x01703A` | `PackRgn.s:171`<br>`PackRgn.s:163` | TRIM DSTRGN TO EXACT SIZE IF IT ISN'T ALREADY. CLEAN UP THE STACK AND GO HOME. Called during boot (7,415 times in 30s trace). |
| **`PACKRGN_START`** | `0x00C81E` | `0x017010` | `PackRgn.s:134`<br>`PackRgn.s:131` | — |
| **`PAINT1`** | `0x00E3F2` | `0x018B7E` | `Pictures.s:1900`<br>`Pictures.s:1381` | — |
| **`PAINT1_EXIT`** | `0x00E43C` | `0x018BC8` | `Pictures.s:1925`<br>`Pictures.s:1408` | Common epilog for PutPicVerb branches. Called by: PUTPICVERB, PUTPICVERB_NO, ERASE1, NEWBK, PAINT1_NO |
| **`PAINT1_NO`** | `0x00E412` | `0x018B9E` | `Pictures.s:1911`<br>`Pictures.s:1392` | — |
| **`PAINT1_NO_2`** | `0x00E426` | `0x018BB2` | `Pictures.s:1918`<br>`Pictures.s:1399` | — |
| **`PaintArc`** | `0x00AFDA` | `0x01574A` | `Arcs.s:99` | **Proto:** `PROCEDURE PaintArc(* r: Rect; startAngle,arcAngle: INTEGER *);`<br>PROCEDURE PaintArc(* r: Rect; startAngle,arcAngle: INTEGER *); |
| **`PAINTARC`** | `0x00AFDA` | `0x01574A` | `Arcs.s:96` | **Proto:** `PROCEDURE PaintArc(* r: Rect; startAngle,arcAngle: INTEGER *);`<br>PROCEDURE PaintArc(* r: Rect; startAngle,arcAngle: INTEGER *); |
| **`PaintOval`** | `0x00ADD8` | `0x015548` | `Ovals.s:111` | **Proto:** `PROCEDURE PaintOval(* r: Rect *);`<br>PROCEDURE PaintOval(* r: Rect *); |
| **`PAINTOVAL`** | `0x00ADD8` | `0x015548` | `Ovals.s:99` | **Proto:** `PROCEDURE PaintOval(* r: Rect *);`<br>PROCEDURE PaintOval(* r: Rect *); |
| **`PaintPoly`** | `0x00B9FC` | `0x01616C` | `Polygons.s:100` | **Proto:** `PROCEDURE PaintPoly(* poly: PolyHandle *);`<br>PROCEDURE PaintPoly(* poly: PolyHandle *); |
| **`PAINTPOLY`** | `0x00B9FC` | `0x01616C` | `Polygons.s:81` | **Proto:** `PROCEDURE PaintPoly(* poly: PolyHandle *);`<br>PROCEDURE PaintPoly(* poly: PolyHandle *); |
| **`PaintRect`** | `0x009F2C` | `0x01469C` | `Rects.s:176` | **Proto:** `PROCEDURE PaintRect(r: Rect);`<br>PROCEDURE PaintRect(r: Rect); PaintRect _PaletteDispatch ($A8A2) Called during boot. |
| **`PAINTRECT`** | `0x009F2C` | `0x01469C` | `Rects.s:161` | **Proto:** `PROCEDURE PaintRect(r: Rect);`<br>PROCEDURE PaintRect(r: Rect); |
| **`PaintRgn`** | `0x00BC60` | `0x0163D0` | `Regions.s:90` | **Proto:** `PROCEDURE PaintRgn(* rgn: RgnHandle *);`<br>PROCEDURE PaintRgn(* rgn: RgnHandle *); |
| **`PAINTRGN`** | `0x00BC60` | `0x0163D0` | `Regions.s:76` | **Proto:** `PROCEDURE PaintRgn(* rgn: RgnHandle *);`<br>PROCEDURE PaintRgn(* rgn: RgnHandle *); |
| **`PaintRoundRect`** | `0x00AD06` | `0x015476` | `RRects.s:106` | **Proto:** `PROCEDURE PaintRoundRect(* r: Rect; ovWd,ovHt: INTEGER *);`<br>PROCEDURE PaintRoundRect(* r: Rect; ovWd,ovHt: INTEGER *); |
| **`PAINTROUNDRECT`** | `0x00AD06` | `0x015476` | `RRects.s:107` | **Proto:** `PROCEDURE PaintRoundRect(* r: Rect; ovWd,ovHt: INTEGER *);`<br>PROCEDURE PaintRoundRect(* r: Rect; ovWd,ovHt: INTEGER *); |
| **`PARAMOP_TBL`** | — | `0x018410` | `Pictures.s:502` | Opcodes $00..$1F do no drawing, they just set parameters. Param-opcode dispatch table: 32 word offsets relative to PARAMOP_TBL, indexed by opcode*2. Most slots above $11 route to KILL1 (offset 0x05EA)... |
| **`PatExpand`** | `0x008498` | `0x012BCE` | `Util.s:360` | .PROC PatExpand,0 EXPAND AN 8 BYTE PATTERN OUT TO 16 LONGS. CALLED ONLY FROM BITBLT,RGNBLT,DRAWLINE,DRAWARC. INPUTS: A0: POINTS TO 8 BYTE PATTERN A1: POINTS TO 16 LONGS OF DESTINATION A5: PASCAL GLOBA... |
| **`PATEXPAND`** | `0x008498` | `0x012BCE` | `Util.s:231` | PatExpand - expand 8-byte pattern to 16 longs Inputs: A0 -> 8-byte pattern source A1 -> 16 longs of destination buffer A5 -> Pascal globals D2 = horizontal global-local offset (for pre-rotate) D7 = -1... |
| **`PATEXPAND_DONE`** | `0x00853A` | `0x012C70` | `Util.s:452`<br>`Util.s:302` | — |
| **`PATEXPAND_DONE_CONT`** | `0x008540` | — | `Util.s:461` | PATEXPAND_DONE_CONT |
| **`PATEXPAND_DONE_CONT_2`** | `0x008550` | `0x012C86` | `Util.s:465`<br>`Util.s:323` | — |
| **`PATEXPAND_SKIP`** | `0x0084BE` | `0x012BF4` | `Util.s:381`<br>`Util.s:244` | IF PATALIGN VERT NON-ZERO, COPY PAT TWICE AND REPLACE A0 |
| **`PenMode`** | `0x009814` | `0x013F84` | `Lines.s:327` | **Proto:** `PROCEDURE PenMode(mode: INTEGER);`<br>.PROC PenMode,1 .REF PortWord PROCEDURE PenMode(mode: INTEGER); { set the transfer mode for line drawing } Called during boot. |
| **`PENMODE`** | `0x009814` | `0x013F84` | `Lines.s:313` | **Proto:** `PROCEDURE PenMode(mode: INTEGER);`<br>.PROC PenMode,1 .REF PortWord PROCEDURE PenMode(mode: INTEGER); { set the transfer mode for line drawing } Called during boot. |
| **`PenNormal`** | `0x00982E` | `0x013F9E` | `Lines.s:355` | **Proto:** `PROCEDURE PenNormal;`<br>.PROC PenNormal,0 PROCEDURE PenNormal; { restore all line drawing parameters to normal } Called during boot. |
| **`PENNORMAL`** | `0x00982E` | `0x013F9E` | `Lines.s:337` | **Proto:** `PROCEDURE PenNormal;`<br>.PROC PenNormal,0 PROCEDURE PenNormal; { reset the pen to its standard 1x1 black pattern } |
| **`PenPat`** | `0x00981A` | `0x013F8A` | `Lines.s:338` | **Proto:** `PROCEDURE PenPat(pat: Pattern);`<br>.PROC PenPat,1 PROCEDURE PenPat(pat: Pattern); { set the pattern for line drawing } Called during boot. |
| **`PENPAT`** | `0x00981A` | `0x013F8A` | `Lines.s:322` | **Proto:** `PROCEDURE PenPat(pat: Pattern);`<br>.PROC PenPat,1 PROCEDURE PenPat(pat: Pattern); { set the pen pattern } |
| **`PenSize`** | `0x009806` | `0x013F76` | `Lines.s:313` | **Proto:** `PROCEDURE PenSize(width,height: INTEGER);`<br>SetPenState .PROC PenSize,2 PROCEDURE PenSize(width,height: INTEGER); { set the pen width and height } Called during boot. |
| **`PENSIZE`** | `0x009806` | `0x013F76` | `Lines.s:300` | **Proto:** `PROCEDURE PenSize(width,height: INTEGER);`<br>.PROC PenSize,2 PROCEDURE PenSize(width,height: INTEGER); { set the pen width and height } Called during boot. |
| **`PicComment`** | `0x00D9D6` | `0x018152` | `Pictures.s:203` | **Proto:** `PROCEDURE PicComment(kind,dataSize: INTEGER; dataHandle: Handle;`<br>.PROC PicComment,3 .REF StdComment PROCEDURE PicComment(kind,dataSize: INTEGER; dataHandle: Handle; |
| **`PICCOMMENT`** | `0x00D9D6` | `0x018152` | `Pictures.s:180` | **Proto:** `PROCEDURE PicComment(kind, dataSize: INTEGER; dataHandle: Handle);`<br>PROCEDURE PicComment(kind, dataSize: INTEGER; dataHandle: Handle); Trap entry stub for StdComment with GrafProcs dispatch. |
| **`PICCOMMENT_USESTD`** | `0x00D9EA` | `0x018166` | `Pictures.s:211`<br>`Pictures.s:188` | — |
| **`PicItem`** | `0x00DC18` | `0x018394` | `Pictures.s:595` | **Proto:** `FUNCTION PicItem(VAR playState: PicPlayRec): BOOLEAN;`<br>.FUNC PicItem,1 .REF GetPicData,ScalePt,MapPt,MapRect,MapRgn,MapPoly .REF NewRgn,CopyRgn,SectRgn,UnpackBits .REF StdText,StdLine,StdRect,StdRRect,StdOval .REF StdArc,StdPoly,StdRgn,StdBits,StdComment ... |
| **`PICITEM`** | `0x00DC18` | `0x018394` | `Pictures.s:443` | **Proto:** `FUNCTION PicItem(VAR playState: PicPlayRec): BOOLEAN;`<br>FUNCTION PicItem(VAR playState: PicPlayRec): BOOLEAN; Draws one picture item, updating playState and thePort. Returns FALSE when an endPic opCode is encountered. The only state modified other than the... |
| **`PICITEM_DHOK`** | `0x00DEB0` | `0x01863C` | `Pictures.s:1008`<br>`Pictures.s:733` | — |
| **`PICITEM_MORE1`** | `0x00E078` | `0x018804` | `Pictures.s:1235`<br>`Pictures.s:927` | IF OPCODE BIT3 SET, THEN UNPACK COMPRESSED SCANLINES PICITEM_MORE1 |
| **`PICITEM_NOPACK`** | `0x00E0A0` | `0x01882C` | `Pictures.s:1252`<br>`Pictures.s:941` | BIT3 = 0, DONT USE PACKING |
| **`PICITEM_START1`** | `0x00E09A` | `0x018826` | `Pictures.s:1245`<br>`Pictures.s:937` | — |
| **`PICRGNOP`** | — | `0x018756` | `Pictures.s:855` | Rgn: OP, RGN |
| **`PICRGNOP_OK`** | — | `0x018784` | `Pictures.s:869` | — |
| **`PIN_CHECK_BOTTOM`** | `0x001F28` | `0x01912E` | `CrsrCore.s:431`<br>`CrsrCore.s:512` | — |
| **`PIN_CHECK_RIGHT`** | `0x001F14` | `0x01911A` | `CrsrCore.s:421`<br>`CrsrCore.s:502` | — |
| **`PIN_CHECK_TOP`** | `0x001F20` | `0x019126` | `CrsrCore.s:426`<br>`CrsrCore.s:507` | — |
| **`PIN_DONE`** | `0x001F34` | `0x01913A` | `CrsrCore.s:436`<br>`CrsrCore.s:517` | — |
| **`PIN_POINT_TO_RECT`** | `0x001F0A` | `0x019110` | `CrsrCore.s:417`<br>`CrsrCore.s:498` | PIN_POINT_TO_RECT - PinRect helper: constrain a point within a rectangle D0 = point (v:h packed as two 16-bit words) A0 = pointer to pin rectangle (top, left, bottom, right) Returns D0 with point clam... |
| **`PinRect`** | `0x001F38` | `0x01913E` | `CrsrCore.s:447` | _PinRect ($A94E) - Constrain a point within a rectangle Stack: retAddr, point (longword v:h), rectPtr (longword) Returns point (clamped to rect) in place of the rect pointer. |
| **`PINRECT`** | `0x001F38` | `0x01913E` | `CrsrCore.s:525` | PinRect(pt: Point; r: Rect): Point -- public stack wrapper around PIN_POINT_TO_RECT. |
| **`POLY`** | `0x00DF98` | `0x018724` | `Pictures.s:1119`<br>`Pictures.s:835` | Poly: OP, POLY |
| **`POLY_OK`** | — | `0x018752` | `Pictures.s:849` | — |
| **`PORTLONG`** | — | `0x012B2A` | `Util.s:135` | — |
| **`PortSize`** | `0x0089EE` | `0x013124` | `GrafAsm.s:406` | **Proto:** `PROCEDURE PortSize(width,height: INTEGER);`<br>.PROC PortSize,2 PROCEDURE PortSize(width,height: INTEGER); Called during boot. |
| **`PORTSIZE`** | `0x0089EE` | `0x013124` | `GrafAsm.s:402` | **Proto:** `PROCEDURE PortSize(width,height: INTEGER);`<br>.PROC PortSize,2 PROCEDURE PortSize(width,height: INTEGER); Called during boot. |
| **`PORTWORD`** | — | `0x012B38` | `Util.s:145` | — |
| **`POS`** | `0x00E55C` | `0x018CE8` | `Pictures.s:2112`<br>`Pictures.s:1547` | POS |
| **`POSANG`** | `0x00B108` | `0x015878` | `DrawArc.s:238`<br>`DrawArc.s:146` | — |
| **`Pt2Rect`** | `0x00A1C2` | `0x014932` | `Rects.s:683` | **Proto:** `PROCEDURE Pt2Rect(* pt1,pt2: Point; VAR dst: Rect *);`<br>PROCEDURE Pt2Rect(* pt1,pt2: Point; VAR dst: Rect *); { make a rectangle from two points } Called during boot. |
| **`PT2RECT`** | `0x00A1C2` | `0x014932` | `Rects.s:578` | **Proto:** `PROCEDURE Pt2Rect(* pt1,pt2: Point; VAR dst: Rect *);`<br>PROCEDURE Pt2Rect(* pt1,pt2: Point; VAR dst: Rect *); { make a rectangle from two points } Called during boot. |
| **`PT2RECT_SHARE`** | `0x00A1F0` | `0x014960` | `Rects.s:704`<br>`Rects.s:596` | — |
| **`PtInRect`** | `0x00A1F8` | `0x014968` | `Rects.s:723` | **Proto:** `FUNCTION PtInRect(pt: Point; r: Rect): BOOLEAN;`<br>.PROC PtInRect FUNCTION PtInRect(pt: Point; r: Rect): BOOLEAN; Returns TRUE if point is within the rectangle. A6 OFFSETS OF PARAMETERS AFTER LINK: PARAMSIZE .EQU 8 ;SIZE OF PARAMETERS RESULT .EQU PARA... |
| **`PTINRECT`** | `0x00A1F8` | `0x014968` | `Rects.s:608` | **Proto:** `FUNCTION PtInRect(pt: Point; r: Rect): BOOLEAN;`<br>.PROC PtInRect FUNCTION PtInRect(pt: Point; r: Rect): BOOLEAN; Returns TRUE if point is within the rectangle. Called during boot (43,763 times in 30s trace). |
| **`PTINRECT_EXIT`** | `0x00A220` | `0x014990` | `Rects.s:743`<br>`Rects.s:623` | — |
| **`PtInRgn`** | `0x00C0D4` | `0x016844` | `Regions.s:979` | **Proto:** `FUNCTION PtInRgn(pt: Point; rgn: RgnHandle): BOOLEAN;`<br>.PROC PtInRgn FUNCTION PtInRgn(pt: Point; rgn: RgnHandle): BOOLEAN; TESTS IF A GIVEN POINT IS INSIDE A REGION. A6 OFFSETS OF PARAMETERS AFTER LINK: PARAMSIZE .EQU 8 ;SIZE OF PARAMETERS RESULT .EQU PAR... |
| **`PTINRGN`** | `0x00C0D4` | `0x016844` | `Regions.s:808` | **Proto:** `FUNCTION PtInRgn(pt: Point; rgn: RgnHandle): BOOLEAN;`<br>FUNCTION PtInRgn(pt: Point; rgn: RgnHandle): BOOLEAN; Tests if a given point is inside a region. A6 offsets of parameters after LINK: PARAMSIZE = 8 RESULT    = PARAMSIZE+8    (BOOLEAN) PT        = RES... |
| **`PTINRGN_NEXT`** | `0x00C110` | `0x016880` | `Regions.s:1021`<br>`Regions.s:839` | — |
| **`PTINRGN_NO`** | `0x00C10C` | `0x01687C` | `Regions.s:1019`<br>`Regions.s:837` | FIRST CHECK BOUNDING BOX PT IS INSIDE BOUNDING BOX AND REGION IS NOT RECTANGULAR. LOOK AT THE INVERSION POINTS TO DETERMINE IF PT IN REGION. Called during boot (1,323 times in 30s trace). |
| **`PtToAngle`** | `0x00B8F2` | `0x016062` | `Angles.s:135` | **Proto:** `PROCEDURE PtToAngle(r: Rect; pt: Point; VAR angle: INTEGER);`<br>.PROC PtToAngle,3 .REF AngleFromSlope PROCEDURE PtToAngle(r: Rect; pt: Point; VAR angle: INTEGER); Given a rectangle and a point, return the angle subtended by pt. A6 OFFSETS OF PARAMETERS AFTER LINK: |
| **`PTTOANGLE`** | `0x00B8F2` | `0x016062` | `Angles.s:180` | **Proto:** `PROCEDURE PtToAngle(r: Rect; pt: Point; VAR angle: INTEGER);`<br>PROCEDURE PtToAngle(r: Rect; pt: Point; VAR angle: INTEGER); Given a rectangle and a point, return the angle subtended by pt. A6 offsets of parameters after LINK: RECT  = 0x10  (LONG: addr of Rect) PT... |
| **`PTTOANGLE_DONE`** | `0x00B96E` | `0x0160DE` | `Angles.s:195`<br>`Angles.s:235` | — |
| **`PushVerb`** | `0x009EE0` | `0x014650` | `Rects.s:89` | .PROC PushVerb PUSH A MODE AND A PATTERN, BASED ON VERB ENTER WITH VERB IN D7, GRAFGLOBALS IN A4, THEPORT IN A3. CLOBBERS A0. frame: pnMode, pnPat paint: pnMode, pnPat erase: patCopy, bkPat invert: pa... |
| **`PUSHVERB`** | `0x009EE0` | `0x014650` | `Rects.s:94` | .PROC PushVerb PUSH A MODE AND A PATTERN, BASED ON VERB ENTER WITH VERB IN D7, GRAFGLOBALS IN A4, THEPORT IN A3. CLOBBERS A0. frame: pnMode, pnPat paint: pnMode, pnPat erase: patCopy, bkPat invert: pa... |
| **`PUSHVERB_DONE`** | `0x009F10` | `0x014680` | `Rects.s:127`<br>`Rects.s:129` | — |
| **`PUSHVERB_ERASE1`** | `0x009EFA` | `0x01466A` | `Rects.s:105`<br>`Rects.s:109` | PUSHVERB_ERASE1 Called during boot. |
| **`PUSHVERB_ERASE1_CONT`** | `0x009F00` | `0x014670` | `Rects.s:114`<br>`Rects.s:117` | PUSHVERB_ERASE1_CONT Called during boot. |
| **`PUSHVERB_PAINT1`** | `0x009F08` | `0x014678` | `Rects.s:124`<br>`Rects.s:126` | PUSHVERB_PAINT1 Called during boot. |
| **`PutLine`** | `0x009D94` | `0x014504` | `PutLine.s:18` | **Proto:** `PROCEDURE PutLine(pt1,pt2: Point; dst: Handle; VAR index,bufMax: INTEGER);`<br>--> PUTLINE.TEXT Decompose a line segment into a list of inversion points. .PROC PUTLINE,5 .REF SETSIZE PROCEDURE PutLine(pt1,pt2: Point; dst: Handle; VAR index,bufMax: INTEGER); INVERSION POINTS FOR ... |
| **`PUTLINE`** | `0x009D94` | `0x014504` | `PutLine.s:18` | **Proto:** `PROCEDURE PutLine(pt1,pt2: Point; dst: Handle; VAR index,bufMax: INTEGER);`<br>--> PUTLINE.TEXT Decompose a line segment into a list of inversion points. .PROC PUTLINE,5 .REF SETSIZE PROCEDURE PutLine(pt1,pt2: Point; dst: Handle; VAR index,bufMax: INTEGER); INVERSION POINTS FOR ... |
| **`PUTLINE_GOHOME`** | `0x009E72` | `0x0145E2` | `PutLine.s:194`<br>`PutLine.s:173` | UPDATE INDEX TO REFLECT POINTS ADDED. |
| **`PUTLINE_SLANTED`** | `0x009E02` | `0x014572` | `PutLine.s:101`<br>`PutLine.s:88` | IF LINE IS HORIZONTAL, PUT ITS TWO ENDPOINTS LINE IS SLANTED. DIVIDE IT INTO HORIZONTAL SLABS AND PUT THE TWO ENDPOINTS OF EACH SLAB. START BY SORTING POINTS VERTICALLY. |
| **`PUTOP`** | `0x0096B0` | `0x013E20` | `Lines.s:68`<br>`Lines.s:69` | — |
| **`PutOval`** | `0x00AE1A` | `0x01558A` | `PutOval.s:26` | **Proto:** `PROCEDURE PutOval(dstRect: Rect; ovalWidth,ovalHeight: INTEGER;`<br>--> PUTOVAL.TEXT Routine to add the inversion points for an oval to a region. OFFSETS IN AN OVAL STATE RECORD: .PROC PUTOVAL,6 .REF INITOVAL,BUMPOVAL,SETSIZE PROCEDURE PutOval(dstRect: Rect; ovalWidth... |
| **`PUTOVAL`** | `0x00AE1A` | `0x01558A` | `PutOval.s:27` | **Proto:** `PROCEDURE PutOval(dstRect: Rect; ovalWidth,ovalHeight: INTEGER;`<br>--> PUTOVAL.TEXT Routine to add the inversion points for an oval to a region. .PROC PUTOVAL,6 .REF INITOVAL,BUMPOVAL,SETSIZE PROCEDURE PutOval(dstRect: Rect; ovalWidth,ovalHeight: INTEGER; bufHandle: ... |
| **`PUTOVAL_SIZEOK`** | `0x00AF3E` | `0x0156AE` | `PutOval.s:238`<br>`PutOval.s:188` | BUFFER IS FULL, CALL STORAGE ALLOCATOR TO MAKE ROOM FOR 256 MORE POINTS. UPDATE BUFPTR, BUFSTART, BUFLIMIT, AND BUFSIZE AFTER RELOCATION. ADD NEW POINT TO THE SAVE BUFFER UNLESS IT MATCHED THE PREVIOU... |
| **`PUTOVAL_YESBUMP`** | `0x00AE98` | `0x015608` | `PutOval.s:138`<br>`PutOval.s:87` | FOR EACH VERTICAL, BUMP LEFTEDGE AND RIGHTEDGE. IF THEY DIFFER FROM OLDLEFT AND OLDRIGHT, PUT INVERSION POINTS FOR THE DIFFERENCES |
| **`PUTOVAL_YESBUMP_OK`** | `0x00AEC6` | `0x015636` | `PutOval.s:153`<br>`PutOval.s:101` | CHECK LEFT EDGE AND PUT TWO INVERSION POINTS IF IT HAS CHANGED |
| **`PUTOVAL_YESBUMP_SKIP`** | `0x00AEE2` | `0x015652` | `PutOval.s:163`<br>`PutOval.s:110` | CHECK RIGHT EDGE AND PUT TWO INVERSION POINTS IF IT HAS CHANGED |
| **`PutPicByte`** | `0x00E2AA` | `0x018A36` | `Pictures.s:1685` | **Proto:** `PROCEDURE PutPicByte(data: Byte);`<br>.PROC DPutPicByte,1 .DEF PutPicByte .REF PutPicData PROCEDURE PutPicByte(data: Byte); Called by: DHDV, PUTOP, NOPACK, MORE1, ClosePicture |
| **`PUTPICBYTE`** | `0x00E2AA` | `0x018A36` | `Pictures.s:1233` | Called by: DHDV, PUTOP, NOPACK, MORE1, CLOSEPICTURE |
| **`PutPicData`** | `0x00E28E` | `0x018A1A` | `Pictures.s:1655` | **Proto:** `PROCEDURE PutPicData(dataPtr: QDPtr; byteCount:INTEGER);`<br>.PROC PutPicData,2 .REF StdPutPic PROCEDURE PutPicData(dataPtr: QDPtr; byteCount:INTEGER); ADD SOME BYTES TO THEPIC. Called by: NOPACK, TEXT2, MORE1, MORE2, STDCOMMENT_OK (and 6 more) |
| **`PUTPICDATA`** | `0x00E28E` | `0x018A1A` | `Pictures.s:1211` | PUTPICDATA -- dispatch to current GrafProcs.putPicProc or _StdPutPic if grafProcs is nil. Called by: NOPACK, TEXT2, MORE1, MORE2, STDCOMMENT_OK (and 6 more) |
| **`PUTPICDATA_EMPTY`** | `0x00E2A2` | `0x018A2E` | `Pictures.s:1663`<br>`Pictures.s:1219` | — |
| **`PutPicLong`** | `0x00E2CE` | `0x018A5A` | `Pictures.s:1720` | **Proto:** `PROCEDURE PutPicWord(data: INTEGER);`<br>.PROC PutPicWord,1 .REF PutPicData PROCEDURE PutPicWord(data: INTEGER); PutPicLong -- yES, PUT STARTPT = PNLOC. Put Pic Long Called by: PUTOP, STDLINE_STARTOK, StdRRect, FRAME1, CheckPic (and 2 more) |
| **`PUTPICLONG`** | `0x00E2CE` | `0x018A5A` | `Pictures.s:1249` | Called by: STDTEXT_NOTSAME_CONT, PUTOP, STDLINE_STARTOK, STDRRECT, FRAME1 (and 3 more) |
| **`PutPicPat`** | `0x00E2DE` | `0x018A6A` | `Pictures.s:1738` | **Proto:** `PROCEDURE PutPicLong(data: LongInt);`<br>.PROC PutPicLong,1 .REF PutPicData PROCEDURE PutPicLong(data: LongInt); PutPicPat -- pUT PATTERN DATA. Put Pic Pat |
| **`PUTPICPAT`** | `0x00E2DE` | `0x018A6A` | `Pictures.s:1255` | — |
| **`PutPicRect`** | `0x00E2EA` | `0x018A76` | `Pictures.s:1755` | **Proto:** `PROCEDURE PutPicPat(pat: Pattern);`<br>.PROC PutPicPat,1 .REF PutPicData PROCEDURE PutPicPat(pat: Pattern); PutPicRect -- pUT OPCODE AND RECTANGLE. Put Pic Rect |
| **`PUTPICRECT`** | `0x00E2EA` | `0x018A76` | `Pictures.s:1268` | PUTPICRECT(verb, rectAddr) -- compress rect into picture If the rect equals theRect (last rect put to thePic), set sameFlag (verb \|= 8) and emit only the verb byte. Otherwise emit verb + 8 bytes of re... |
| **`PutPicRgn`** | `0x00E32C` | `0x018AB8` | `Pictures.s:1803` | **Proto:** `PROCEDURE PutPicRgn(rgn: RgnHandle);`<br>.PROC PutPicRgn,1 .REF PutPicData PROCEDURE PutPicRgn(rgn: RgnHandle); ALSO called to put a polygon. _HLock ;LOCK IT |
| **`PUTPICRGN`** | `0x00E32C` | `0x018AB8` | `Pictures.s:1299` | PUTPICRGN -- HLock the region handle, emit (length-prefixed) rgn data, then HUnlock. |
| **`PutPicVerb`** | `0x00E34A` | `0x018AD6` | `Pictures.s:1822` | PutPicVerb -- pUT ADDIONAL PARAMS TO THEPIC. Put Pic Verb Called by: StdLine, StdRect, StdRRect, StdOval, StdArc (and 2 more) |
| **`PUTPICVERB`** | `0x00E34A` | `0x018AD6` | `Pictures.s:1325` | **Proto:** `PROCEDURE PutPicVerb(verb: GrafVerb)`<br>PROCEDURE PutPicVerb(verb: GrafVerb) Check additional picture params associated with this verb, and add those that have changed to thePic. Verb selects which state to compare: 0 (frame): pnSize, pnMod... |
| **`PUTPICVERB_NO`** | `0x00E38A` | `0x018B16` | `Pictures.s:1856`<br>`Pictures.s:1345` | — |
| **`PutPicWord`** | `0x00E2BC` | `0x018A48` | `Pictures.s:1700` | PutPicByte PutPicWord -- pUT KIND. Put Pic Word Called by: StdArc, STDCOMMENT_OK, COUNTOK, FACEOK, STDTEXT_MODEOK (and 4 more) |
| **`PUTPICWORD`** | `0x00E2BC` | `0x018A48` | `Pictures.s:1241` | Called by: STDARC, STDCOMMENT_OK, COUNTOK, FACEOK, STDTEXT_MODEOK (and 4 more) |
| **`PUTPT`** | `0x00AF10` | `0x015680` | `PutOval.s:208`<br>`PutOval.s:160` | Local routine to Append a point to the end of the saved points buffer, extending buffer if necessary. If pt is a duplicate of the last pt, cancel both instead. INPUTS: D5: HORIZ COORD D6: VERT COORD A... |
| **`PutRect`** | `0x00A228` | `0x014998` | `Rects.s:766` | **Proto:** `PROCEDURE PutRect(r: Rect; bufHandle: Handle; VAR index,size: INTEGER);`<br>.PROC PutRect,4 .REF SetSize PROCEDURE PutRect(r: Rect; bufHandle: Handle; VAR index,size: INTEGER); Puts the four inversion points of a rectangle Clobbers D0,A0,A1 A6 OFFSETS OF PARAMETERS AFTER LINK... |
| **`PUTRECT`** | `0x00A228` | `0x014998` | `Rects.s:638` | **Proto:** `PROCEDURE PutRect(r: Rect; bufHandle: Handle; VAR index,size: INTEGER);`<br>.PROC PutRect,4 .REF SetSize PROCEDURE PutRect(r: Rect; bufHandle: Handle; VAR index,size: INTEGER); Puts the four inversion points of a rectangle. Clobbers D0,A0,A1 |
| **`PUTRECT_SIZEOK`** | `0x00A256` | `0x0149C6` | `Rects.s:805`<br>`Rects.s:665` | NOW INSTALL THE 4 NEW INVERSION POINTS |
| **`PutRgn`** | `0x00C856` | `0x016EFE` | `PutRgn.s:14` | **Proto:** `PROCEDURE PutRgn(Rgn: RgnHandle; bufHandle: Handle; VAR index,size: INTEGER);`<br>A6 OFFSETS OF PARAMETERS AFTER LINK: .PROC PUTRGN,4 .REF SETSIZE PROCEDURE PutRgn(Rgn: RgnHandle; bufHandle: Handle; VAR index,size: INTEGER); Expands a region out to an array of inversion points. |
| **`PUTRGN`** | `0x00C856` | `0x016EFE` | `PutRgn.s:19` | **Proto:** `PROCEDURE PutRgn(Rgn: RgnHandle; bufHandle: Handle;`<br>A6 OFFSETS OF PARAMETERS AFTER LINK: PROCEDURE PutRgn(Rgn: RgnHandle; bufHandle: Handle; VAR index, size: INTEGER); Expands a region out to an array of inversion points. A6 offsets of params after LIN... |
| **`PUTRGN_DONE`** | `0x00C8BA` | `0x016F6E` | `PutRgn.s:75`<br>`PutRgn.s:71` | — |
| **`PUTRGN_FITS`** | — | `0x016F36` | `PutRgn.s:39` | — |
| **`PUTRGN_NOTRECT`** | `0x00C8A0` | `0x016F54` | `PutRgn.s:62`<br>`PutRgn.s:58` | PUTRGN_NOTRECT |
| **`PUTRGN_NXTVERT`** | `0x00C8A4` | `0x016F58` | `PutRgn.s:64`<br>`PutRgn.s:60` | — |
| **`QRTR1`** | `0x00D648` | `0x017DC4` | `Stretch.s:1004`<br>`Stretch.s:813` | — |
| **`QRTR2`** | `0x00D64C` | `0x017DC8` | `Stretch.s:1007`<br>`Stretch.s:816` | — |
| **`QRTR2_CONT`** | `0x00D69E` | `0x017E1A` | `Stretch.s:1060`<br>`Stretch.s:864` | RTS ;YES, QUIT STRETCH TO 1.5 TIMES AS WIDE QRTR2_CONT - indexed branch table for stretch source sampling |
| **`QRTR2_CONT_2`** | `0x00D6C6` | — | `Stretch.s:1090` | QRTR2_CONT_2 - indexed branch table for stretch 3/4 sampling |
| **`QRTR2_LOOP`** | `0x00D65E` | `0x017DDA` | `Stretch.s:1021`<br>`Stretch.s:831` | QRTR2_LOOP |
| **`QRTR2_LOOP_2`** | `0x00D6AE` | `0x017E2A` | `Stretch.s:1075`<br>`Stretch.s:882` | RTS ;ALL DONE .BYTE $60,$6C,$70,$7C .BYTE $80,$8C,$90,$9C .BYTE $E0,$EC,$F0,$FC DOUBLE USING TABLE LOOKUP |
| **`QUAD`** | `0x00D71A` | `0x017E96` | `Stretch.s:1150`<br>`Stretch.s:965` | .BYTE $E0,$E3,$FC,$FF .BYTE $70,$71,$7E,$7F .BYTE $80,$81,$8E,$8F .BYTE $F0,$F1,$FE,$FF .BYTE $C0,$C7,$F8,$FF QUADRUPLE USING TABLE LOOKUP |
| **`QUAD_CONT`** | `0x00D738` | `0x017EB4` | `Stretch.s:1167`<br>`Stretch.s:983` | QUAD_CONT - indexed branch table for stretch double expansion |
| **`QUAD_LOOP`** | `0x00D758` | — | `Stretch.s:1175` | — |
| **`QUADRANT1`** | `0x00B7F4` | `0x015F64` | `Angles.s:65`<br>`Angles.s:69` | — |
| **`Random`** | `0x00839C` | `0x012AD2` | `Util.s:149` | **Proto:** `FUNCTION Random: INTEGER;`<br>.FUNC Random,0 FUNCTION Random: INTEGER; returns a signed 16 bit number, and updates unsigned 32 bit randSeed. recursion is randSeed := (randSeed * 16807) MOD 2147483647. See paper by Linus Schrage, A... |
| **`RANDOM`** | `0x00839C` | `0x012AD2` | `Util.s:98` | **Proto:** `Pascal: function Random: INTEGER;`<br>Random ($A861) - linear-congruential 16-bit pseudorandom Pascal: function Random: INTEGER; State: RandSeed (long) at -0x7E(qdGlobals). Algorithm: seed = (seed * 16807) mod (2^31 - 1) - Park-Miller. Re... |
| **`RANDOM_UPDATE`** | `0x0083DC` | `0x012B12` | `Util.s:190`<br>`Util.s:120` | IF seed < 0 THEN seed:=seed+p; |
| **`RANDOM_UPDATE_NO`** | `0x0083E8` | `0x012B1E` | `Util.s:195`<br>`Util.s:125` | — |
| **`RDSTOK`** | `0x00CDDA` | `0x017556` | `Bitmaps.s:737`<br>`Bitmaps.s:621` | RDSTOK |
| **`RectInRgn`** | `0x00C134` | `0x0168A4` | `Regions.s:1058` | **Proto:** `FUNCTION RectInRgn(r: Rect; rgn: RgnHandle): BOOLEAN;`<br>.FUNC RectInRgn,2 .REF RSect,InitRgn,SeekRgn FUNCTION RectInRgn(r: Rect; rgn: RgnHandle): BOOLEAN; Returns TRUE if any part of the rectangle intersects the region. A6 OFFSETS OF PARAMETERS AFTER LINK: |
| **`RECTINRGN`** | `0x00C134` | `0x0168A4` | `Regions.s:880` | **Proto:** `FUNCTION RectInRgn(r: Rect; rgn: RgnHandle): BOOLEAN;`<br>FUNCTION RectInRgn(r: Rect; rgn: RgnHandle): BOOLEAN; Returns TRUE if any part of the rectangle intersects the region. A6 offsets of parameters after LINK: PARAMSIZE = 8 RESULT    = PARAMSIZE+8    (by... |
| **`RECTOP`** | `0x00DF1C` | `0x0186A8` | `Pictures.s:1053`<br>`Pictures.s:773` | Rect: OP, RECT |
| **`RECTOP_OK`** | `0x00DF32` | `0x0186BE` | `Pictures.s:1061`<br>`Pictures.s:781` | — |
| **`RectRgn`** | `0x00BEB4` | `0x016624` | `Regions.s:494` | **Proto:** `PROCEDURE RectRgn(rgn: RgnHandle; r: Rect);`<br>.PROC RectRgn,2 .REF SetRectRgn PROCEDURE RectRgn(rgn: RgnHandle; r: Rect); make a rectangular region from a rectangle Called during boot (66,892 times in 30s trace). |
| **`RECTRGN`** | `0x00BEB4` | `0x016624` | `Regions.s:405` | **Proto:** `PROCEDURE RectRgn(rgn: RgnHandle; r: Rect);`<br>PROCEDURE RectRgn(rgn: RgnHandle; r: Rect); Make a rectangular region from a rectangle. |
| **`RgnBlt`** | `0x00A732` | `0x014EA2` | `RgnBlt.s:50` | **Proto:** `PROCEDURE RgnBlt(srcBits,dstBits: BitMap;`<br>--> RGNBLT.TEXT Low level block transfer clipped to an arbitrary region. .PROC RgnBlt,9 .REF BitBlt,RSect,ShieldCursor,ShowCursor .REF SeekRgn,PatExpand,ColorMap,InitRgn,TrimRect PROCEDURE RgnBlt(srcB... |
| **`RGNBLT`** | `0x00A732` | `0x014EA2` | `RgnBlt.s:31` | **Proto:** `PROCEDURE RgnBlt(srcBits,dstBits: BitMap;`<br>--> RGNBLT.TEXT Low level block transfer clipped to an arbitrary region. RGNBLT - called from 7 places .PROC RgnBlt,9 .REF BitBlt,RSect,ShieldCursor,ShowCursor .REF SeekRgn,PatExpand,ColorMap,InitRgn,... |
| **`RGNBLT_CLRMASK`** | `0x00A822` | `0x014F92` | `RgnBlt.s:248`<br>`RgnBlt.s:151` | CALC BUFLEFT AND BUFSIZE ALLOCATE AND CLEAR A SCANLINE BUFFER FOR THE COMPOSITE MASK. Called during boot. |
| **`RGNBLT_CLRMASK_CONT`** | `0x00A88A` | `0x014FFA` | `RgnBlt.s:308`<br>`RgnBlt.s:200` | BRECT RGNBLT_CLRMASK_CONT -- iNIT STATE, ALLOC BUFFER. |
| **`RGNBLT_CLRMASK_EXIT`** | `0x00A89A` | `0x01500A` | `RgnBlt.s:322`<br>`RgnBlt.s:213` | CRECT IF ONLY ONE REGION IS NON-RECTANGULAR, PLAY IT BACK DIRECTLY INTO THE MASK BUFFER. Called during boot. |
| **`RGNBLT_CLRMASK_NO`** | `0x00A8AE` | `0x01501E` | `RgnBlt.s:343`<br>`RgnBlt.s:225` | CRECT IF ONLY ONE REGION IS NON-RECTANGULAR, PLAY IT BACK DIRECTLY INTO THE MASK BUFFER. RGNBLT_CLRMASK_NO Called during boot. |
| **`RGNBLT_CLRMASK_NO_2`** | `0x00A8BA` | `0x01502A` | `RgnBlt.s:354`<br>`RgnBlt.s:235` | RGNBLT_CLRMASK_NO_2 Called during boot. |
| **`RGNBLT_CLRMASK_SKIP`** | `0x00A860` | `0x014FD0` | `RgnBlt.s:284`<br>`RgnBlt.s:181` | ARECT Called during boot. |
| **`RGNBLT_CLRMASK_SKIP_2`** | `0x00A874` | `0x014FE4` | `RgnBlt.s:297`<br>`RgnBlt.s:191` | ARECT BRECT Called during boot. |
| **`RGNBLT_CLRMASK_SKIP_3`** | `0x00A8C4` | `0x015034` | `RgnBlt.s:358`<br>`RgnBlt.s:239` | — |
| **`RGNBLT_CLRMASK_SKIP_4`** | `0x00A8F8` | `0x015068` | `RgnBlt.s:388`<br>`RgnBlt.s:262` | — |
| **`RGNBLT_DONE`** | `0x00AA6C` | `0x0151DC` | `RgnBlt.s:630`<br>`RgnBlt.s:455` | BUMP DESTINATION VERTICALLY AND LOOP FOR ALL ROWS ENTIRE RGNBLT COMPLETE. RESTORE REGS AND STACK AND GO HOME. Called during boot. |
| **`RGNBLT_GETDST`** | `0x00A9E2` | `0x015152` | `RgnBlt.s:531`<br>`RgnBlt.s:377` | CALC STARTING SRCADDR CALC STARTING DSTADDR Called during boot. |
| **`RGNBLT_GETDST_NO`** | `0x00AA1E` | `0x01518E` | `RgnBlt.s:567`<br>`RgnBlt.s:403` | HBUMPOK Called during boot. |
| **`RGNBLT_GOHOME`** | `0x00AA74` | `0x0151E4` | `RgnBlt.s:638`<br>`RgnBlt.s:458` | ENTIRE RGNBLT COMPLETE. RESTORE REGS AND STACK AND GO HOME. |
| **`RGNBLT_GOHOME_CONT`** | `0x00AA86` | `0x0151F6` | `RgnBlt.s:651`<br>`RgnBlt.s:470` | LOCAL ROUTINE TO UPDATE MASK BUFFER TO CURRENT VERTICAL COORD. Called during boot (1,767 times in 30s trace). |
| **`RGNBLT_GOHOME_CONT_2`** | `0x00AA96` | `0x015206` | `RgnBlt.s:661`<br>`RgnBlt.s:483` | RGNBLT_GOHOME_CONT_2 - indexed branch table for RgnBlt region masking modes |
| **`RGNBLT_GOHOME_CONT_3`** | `0x00AAA6` | `0x015216` | `RgnBlt.s:671`<br>`RgnBlt.s:494` | ONLY REGION A IS NON RECTANGULAR. UPDATE IT AND USE IT AS THE MASK Called during boot (1,172 times in 30s trace). |
| **`RGNBLT_GOHOME_CONT_4`** | `0x00AAAC` | `0x01521C` | `RgnBlt.s:688`<br>`RgnBlt.s:502` | LOCAL ROUTINE TO UPDATE MASK BUFFER TO CURRENT VERTICAL COORD. ONLY REGION B IS NON RECTANGULAR. UPDATE IT AND USE IT AS THE MASK Called during boot. |
| **`RGNBLT_GOHOME_CONT_5`** | `0x00AAB2` | `0x015222` | `RgnBlt.s:699`<br>`RgnBlt.s:509` | ONLY REGION C IS NON RECTANGULAR. UPDATE IT AND USE IT AS THE MASK |
| **`RGNBLT_NXTMASK`** | `0x00AA24` | `0x015194` | `RgnBlt.s:577`<br>`RgnBlt.s:411` | MAKE MASK BUFFER CURRENT FOR THIS VERTICAL. THEN SET UP AND DRAW CURRENT SCANLINE. HBUMPOK Called during boot (1,767 times in 30s trace). |
| **`RGNBLT_NXTMASK_NEXT`** | `0x00AA3E` | `0x0151AE` | `RgnBlt.s:591`<br>`RgnBlt.s:424` | RGNBLT_NXTMASK_NEXT Called during boot. |
| **`RGNBLT_NXTMASK_NEXT_2`** | `0x00AA48` | `0x0151B8` | `RgnBlt.s:601`<br>`RgnBlt.s:433` | RGNBLT_NXTMASK_NEXT_2 Called during boot (1,687 times in 30s trace). |
| **`RGNBLT_SRCOK`** | `0x00A99C` | `0x01510C` | `RgnBlt.s:494`<br>`RgnBlt.s:345` | CALC SHIFTCNT DV IS POSITIVE, WE MUST TRANSFER UPSIDE-DOWN FROM BOTTOM. Called during boot. |
| **`RGNBLT_UPSIDE`** | `0x00A97C` | `0x0150EC` | `RgnBlt.s:476`<br>`RgnBlt.s:332` | DV IS POSITIVE, WE MUST TRANSFER UPSIDE-DOWN FROM BOTTOM. |
| **`RgnOp`** | `0x00C3D6` | `0x016B46` | `RgnOp.s:27` | **Proto:** `FUNCTION RgnOp(rgnA,rgnB: RgnHandle;`<br>.FUNC RgnOp,7 .REF SectScan,DiffScan,UnionScan,XorScan,InsetScan,SetSize FUNCTION RgnOp(rgnA,rgnB: RgnHandle; bufHandle: Handle; maxBytes: INTEGER; op,dh: INTEGER; okGrow: BOOLEAN): INTEGER; Computes ... |
| **`RGNOP`** | `0x00C3D6` | `0x016B46` | `RgnOp.s:49` | **Proto:** `FUNCTION RgnOp(rgnA,rgnB: RgnHandle;`<br>.FUNC RgnOp,7 .REF SectScan,DiffScan,UnionScan,XorScan,InsetScan,SetSize FUNCTION RgnOp(rgnA,rgnB: RgnHandle; bufHandle: Handle; maxBytes: INTEGER; op,dh: INTEGER; okGrow: BOOLEAN): INTEGER; Computes ... |
| **`RGNOP_ABORT`** | `0x00C5D6` | `0x016D46` | `RgnOp.s:320`<br>`RgnOp.s:288` | RGNOP_ABORT Called during boot. |
| **`RGNOP_DONE`** | `0x00C5DA` | `0x016D4A` | `RgnOp.s:322`<br>`RgnOp.s:290` | — |
| **`RGNOP_NOTRECT`** | `0x00C5D0` | `0x016D40` | `RgnOp.s:311`<br>`RgnOp.s:280` | — |
| **`RGNOP_NXTVERT`** | `0x00C4B8` | `0x016C28` | `RgnOp.s:162`<br>`RgnOp.s:143` | INIT ASSORTED POINTERS |
| **`RightMask`** | `0x008420` | `0x012B56` | `Util.s:293` | RTS ;AND RETURN LeftMask Right Mask Called during boot. |
| **`RIGHTMASK`** | `0x008420` | `0x012B56` | `Util.s:164` | RightMask(D0) -> word in D0 - mask of bits right of bit D0 |
| **`RIGHTOK`** | `0x00BABC` | `0x01622C` | `Polygons.s:242`<br>`Polygons.s:209` | — |
| **`RMORE`** | `0x00CDE2` | `0x01755E` | `Bitmaps.s:747`<br>`Bitmaps.s:630` | RMORE |
| **`RNEXT`** | `0x00CDC6` | `0x017542` | `Bitmaps.s:723`<br>`Bitmaps.s:608` | — |
| **`ROK`** | `0x00C372` | `0x016AE2` | `SeekRgn.s:125`<br>`SeekRgn.s:112` | — |
| **`ROWLOOP`** | `0x00A41E` | `0x014B8E` | `BitBlt.s:360`<br>`BitBlt.s:261` | OUTER LOOP: DO EACH SCAN LINE AND COME BACK TO NXTSRC OR NXTPAT. SOME MODES OPTIMIZE AND DO WHOLE OUTER LOOP AND COME BACK TO GOHOME. Called during boot (8,945 times in 30s trace). |
| **`RRECTOP`** | `0x00DF36` | `0x0186C2` | `Pictures.s:1068`<br>`Pictures.s:787` | RRect: OP, RECT, OVALPT |
| **`RRECTOP_OK`** | `0x00DF54` | `0x0186E0` | `Pictures.s:1078`<br>`Pictures.s:797` | — |
| **`RSAME`** | `0x00CDF6` | `0x017572` | `Bitmaps.s:759`<br>`Bitmaps.s:642` | — |
| **`RSect`** | `0x00A110` | `0x014880` | `Rects.s:569` | ASSEMBLY CALLABLE ROUTINE TO COMPUTE THE INTERSECTION OF ANY NUMBER OF RECTANGLES. INPUTS: PUSH ADDRESSES OF EACH INPUT RECTANGLE (LONGS) PUSH # OF RECTANGLES (WORD) PUSH ADDRESS OF OUTPUT RECTANGLE (... |
| **`RSECT`** | `0x00A110` | `0x014880` | `Rects.s:468` | ASSEMBLY CALLABLE ROUTINE TO COMPUTE THE INTERSECTION OF ANY NUMBER OF RECTANGLES. INPUTS: PUSH ADDRESSES OF EACH INPUT RECTANGLE (LONGS) PUSH # OF RECTANGLES (WORD) PUSH ADDRESS OF OUTPUT RECTANGLE (... |
| **`RSTART`** | `0x00CDE4` | `0x017560` | `Bitmaps.s:749`<br>`Bitmaps.s:632` | — |
| **`RTOK`** | `0x00A14C` | `0x0148BC` | `Rects.s:602`<br>`Rects.s:500` | — |
| **`SAME1`** | `0x00E1FA` | `0x018986` | `Pictures.s:1530`<br>`Pictures.s:1115` | — |
| **`SAME1_CONT`** | `0x00E220` | — | `Pictures.s:1547` | SAME1_CONT -- cOPY RGN INTO HANDLE1. SAME1_CONT |
| **`SARC`** | `0x00B5CC` | `0x015D3C` | `DrawArc.s:920`<br>`DrawArc.s:685` | SOLID ARC: IF OUTERLEFT < OUTERRIGHT THEN PAINT ONE SLAB |
| **`SCALE`** | `0x008F0E` | `0x01367E` | `Text.s:822`<br>`Text.s:711` | SCALE -- sCALE ASCENT. SCALE |
| **`SCALE1`** | `0x00E53E` | `0x018CCA` | `Pictures.s:2093`<br>`Pictures.s:1532` | LOCAL ROUTINE TO SCALE A SINGLE WIDTH OR HEIGHT: IF INPUT <= 0, THEN OUTPUT WILL BE 0. IF INPUT > 0, THEN OUTPUT WILL BE AT LEAST 1. |
| **`ScalePt`** | `0x00E512` | `0x018C9E` | `Pictures.s:2057` | **Proto:** `PROCEDURE ScalePt(VAR pt: Point; fromRect,toRect: Rect);`<br>.PROC ScalePt PROCEDURE ScalePt(VAR pt: Point; fromRect,toRect: Rect); Scale a width and height from one coordinate system to another. If fromRect and toRect are the same size, then no change. If the ... |
| **`SCALEPT`** | `0x00E512` | `0x018C9E` | `Pictures.s:1510` | **Proto:** `PROCEDURE ScalePt(VAR pt: Point; fromRect, toRect: Rect)`<br>PROCEDURE ScalePt(VAR pt: Point; fromRect, toRect: Rect) Scale a width and height from one coordinate system to another. If fromRect and toRect are the same size, then no change. If the input > 0, the... |
| **`SCALEPT_CONT`** | `0x00E53E` | — | `Pictures.s:2085` | RTS ;AND RETURN SCALEPT_CONT -- sCALE THE HEIGHT. SCALEPT_CONT |
| **`SCAN_LOOP`** | `0x00B7AA` | `0x015F1A` | `Angles.s:19`<br>`Angles.s:25` | — |
| **`SCDONE`** | `0x00E568` | `0x018CF4` | `Pictures.s:2121`<br>`Pictures.s:1555` | — |
| **`SCRNADDRESS`** | `0x000806` | `0x018F8C` | `CrsrCore.s:302` | ScreenAddress / ScreenSize / ScreenBitmap - SE Toolbox-only screen-info accessors.  Hardcoded for SE 512x342, rowBytes = 64. |
| **`ScrnBitMap`** | `0x001E72` | `0x018FA4` | `CrsrCore.s:325` | ScrnBitMap - Return screen bitmap info (base, rowBytes, bounds) On Mac Plus (1-bit display), returns a bitmap descriptor: ScrnBase, ScreenRow (64), bounds rect (0,0,342,512). Re-uses STORE_SCRN_WIDTH ... |
| **`SCRNBITMAP`** | `0x001E72` | `0x018FA4` | `CrsrCore.s:313` | — |
| **`SCRNSIZE`** | `0x000806` | `0x018F94` | `CrsrCore.s:305` | — |
| **`ScrollRect`** | `0x00CE8E` | `0x01760A` | `Bitmaps.s:878` | **Proto:** `PROCEDURE ScrollRect(dstRect: Rect; dh,dv: INTEGER; updateRgn: RgnHandle);`<br>.PROC ScrollRect,4 .REF NewRgn,RectRgn,SectRgn,CopyRgn,OffsetRgn,SetEmptyRgn .REF DiffRgn,ShieldCursor,RgnBlt,ShowCursor PROCEDURE ScrollRect(dstRect: Rect; dh,dv: INTEGER; updateRgn: RgnHandle); Scro... |
| **`SCROLLRECT`** | `0x00CE8E` | `0x01760A` | `Bitmaps.s:739` | **Proto:** `PROCEDURE ScrollRect(dstRect: Rect; dh, dv: INTEGER;`<br>PROCEDURE ScrollRect(dstRect: Rect; dh, dv: INTEGER; updateRgn: RgnHandle); Scroll a rectangular block of bits, erase, and return an update region. |
| **`SectRect`** | `0x00A0E8` | `0x014858` | `Rects.s:535` | **Proto:** `FUNCTION SectRect(srcA,srcB: Rect; VAR dstC: Rect): BOOLEAN;`<br>.FUNC SectRect,3 .DEF RSect FUNCTION SectRect(srcA,srcB: Rect; VAR dstC: Rect): BOOLEAN; Returns TRUE and intersection in dst, else FALSE and dst = 0,0,0,0. Dst may also be used as one of the inputs A... |
| **`SECTRECT`** | `0x00A0E8` | `0x014858` | `Rects.s:440` | **Proto:** `FUNCTION SectRect(srcA,srcB: Rect; VAR dstC: Rect): BOOLEAN;`<br>.FUNC SectRect,3 .DEF RSect FUNCTION SectRect(srcA,srcB: Rect; VAR dstC: Rect): BOOLEAN; Returns TRUE and intersection in dst, else FALSE and dst = 0,0,0,0. Dst may also be used as one of the inputs C... |
| **`SECTRECT_BOTOK`** | `0x00A144` | `0x0148B4` | `Rects.s:598`<br>`Rects.s:496` | — |
| **`SECTRECT_DONE`** | `0x00A162` | `0x0148D2` | `Rects.s:620`<br>`Rects.s:517` | — |
| **`SECTRECT_EMPTY`** | `0x00A15A` | `0x0148CA` | `Rects.s:615`<br>`Rects.s:512` | SECTRECT_EMPTY Called during boot. |
| **`SECTRECT_LEFTOK`** | `0x00A13C` | `0x0148AC` | `Rects.s:594`<br>`Rects.s:492` | — |
| **`SECTRECT_TOPOK`** | `0x00A134` | `0x0148A4` | `Rects.s:590`<br>`Rects.s:488` | — |
| **`SectRgn`** | `0x00BFDE` | `0x01674E` | `Regions.s:749` | **Proto:** `PROCEDURE SectRgn(srcRgnA,srcRgnB,dstRgn: RgnHandle);`<br>.PROC SectRgn,3 .DEF DoRgnOp,UnionRgn,DiffRgn,XorRgn .REF EqualRgn,CopyRgn,RSect,RectRgn,SetEmptyRgn .REF NewHandle,RgnOp,PackRgn PROCEDURE SectRgn(srcRgnA,srcRgnB,dstRgn: RgnHandle); calculate the in... |
| **`SECTRGN`** | `0x00BFDE` | `0x01674E` | `Regions.s:623` | **Proto:** `PROCEDURE SectRgn(srcRgnA,srcRgnB,dstRgn: RgnHandle);`<br>PROCEDURE SectRgn(srcRgnA,srcRgnB,dstRgn: RgnHandle); Calculate the intersection of two regions. |
| **`SectScan`** | `0x00C5FC` | `0x016D6C` | `RgnOp.s:355` | **Proto:** `PROCEDURE SectScan(srcA,srcB,dstC: ScanPtr);`<br>RTS ;AND RETURN .PROC SectScan,3 .DEF DiffScan,UnionScan PROCEDURE SectScan(srcA,srcB,dstC: ScanPtr); Calculate the intersection, difference, or union of two inversion scans. Each input scan is a sort... |
| **`SECTSCAN`** | `0x00C5FC` | `0x016D6C` | `RgnOp.s:314` | **Proto:** `PROCEDURE SectScan(srcA, srcB, dstC: ScanPtr);`<br>PROCEDURE SectScan(srcA, srcB, dstC: ScanPtr); Calculate the intersection, difference, or union of two inversion scans. Each input scan is a sorted array of integers terminated by 32767. INPUTS:  A0 S... |
| **`SECTSCAN_SHARE`** | `0x00C60A` | `0x016D7A` | `RgnOp.s:378`<br>`RgnOp.s:333` | — |
| **`SeedFill`** | `0x00CD30` | `0x0174AC` | `Bitmaps.s:604` | **Proto:** `PROCEDURE SeedFill(srcPtr,dstPtr: Ptr;`<br>.PROC SeedFill .DEF CalcMask PROCEDURE SeedFill(srcPtr,dstPtr: Ptr; srcRow,dstRow,height,words: INTEGER; seedH,seedV: INTEGER) |
| **`SEEDFILL`** | `0x00CD30` | `0x0174AC` | `Bitmaps.s:516` | **Proto:** `PROCEDURE SeedFill(srcPtr, dstPtr: Ptr;`<br>PROCEDURE SeedFill(srcPtr, dstPtr: Ptr; srcRow, dstRow, height, words: INTEGER; seedH, seedV: INTEGER); |
| **`SeekRgn`** | `0x00C2FE` | `0x016A6E` | `SeekRgn.s:65` | RETURN QUICKLY IF SCANBUF IS ALREADY CURRENT. .PROC SEEKRGN,0 .REF MaskTab SeekRgn(rgnState,vert); ROUTINE TO PLAY BACK A REGION FORWARD OR BACKWARD UNTIL ITS SCAN BUFFER CONTAINS THE BITMAP FOR THE G... |
| **`SEEKRGN`** | `0x00C2FE` | `0x016A6E` | `SeekRgn.s:58` | SeekRgn(rgnState,vert) Routine to play back a region forward or backward until its scan buffer contains the bitmap for the given vertical coordinate. INPUTS:  A1 points to a region state record D0 con... |
| **`SEEKRGN_CLRLP`** | `0x00C316` | `0x016A86` | `SeekRgn.s:80`<br>`SeekRgn.s:72` | — |
| **`SEEKRGN_DONE`** | `0x00C3D2` | `0x016B42` | `SeekRgn.s:201`<br>`SeekRgn.s:179` | — |
| **`SEEKRGN_DOWN1`** | `0x00C344` | `0x016AB4` | `SeekRgn.s:100`<br>`SeekRgn.s:90` | — |
| **`SEEKRGN_NEXTHOR`** | `0x00C348` | `0x016AB8` | `SeekRgn.s:109`<br>`SeekRgn.s:96` | GET LEFT AND RIGHT HORIZ COORDS AND TRIM AGAINST MINH AND MAXH Called during boot. |
| **`SetClip`** | `0x008A80` | `0x0131B6` | `GrafAsm.s:503` | **Proto:** `PROCEDURE SetClip(rgn: RgnHandle);`<br>.PROC SetClip,1 .DEF GetClip .REF CopyRgn PROCEDURE SetClip(rgn: RgnHandle); copy rgn into theport^.clipRgn Called during boot (2,787 times in 30s trace). |
| **`SETCLIP`** | `0x008A80` | `0x0131B6` | `GrafAsm.s:487` | **Proto:** `PROCEDURE SetClip(rgn: RgnHandle);`<br>PROCEDURE SetClip(rgn: RgnHandle); { COPY rgn INTO THEPORT^.CLIPRGN } |
| **`SetCrsr`** | `0x001E0A` | — | `CrsrCore.s:246` | SetCrsr - Set the current cursor image and hotspot Stack: retAddr, cursorPtr (68 bytes: 32 data + 32 mask + 4 hotspot) Compares new cursor with current TheCrsr; if different, hides old cursor and show... |
| **`SETCRSR_CHECK_CHG`** | `0x001E38` | `0x018F6A` | `CrsrCore.s:269`<br>`CrsrCore.s:282` | — |
| **`SETCRSR_CLAMP_V`** | `0x001E30` | `0x018F62` | `CrsrCore.s:264`<br>`CrsrCore.s:277` | — |
| **`SETCRSR_CMP_LOOP`** | `0x001E16` | `0x018F48` | `CrsrCore.s:251`<br>`CrsrCore.s:264` | — |
| **`SETCRSR_REDRAW`** | `0x001E46` | `0x018F78` | `CrsrCore.s:275`<br>`CrsrCore.s:288` | — |
| **`SETCRSR_RETURN`** | `0x001E52` | `0x018F84` | `CrsrCore.s:280`<br>`CrsrCore.s:293` | — |
| **`SETCRSR_STORE`** | `0x001E1E` | `0x018F50` | `CrsrCore.s:256`<br>`CrsrCore.s:269` | — |
| **`SetCursor`** | `0x0082D6` | `0x012A0C` | `LCursor.s:42` | **Proto:** `PROCEDURE SetCursor(crsr: Cursor);`<br>.PROC SetCursor,1 PROCEDURE SetCursor(crsr: Cursor); Called during boot (3,700 times in 30s trace). |
| **`SETCURSOR`** | `0x0082D6` | `0x012A0C` | `LCursor.s:27` | **Proto:** `Pascal: procedure SetCursor(crsr: Cursor);`<br>SETCURSOR ($A851) - install caller's cursor through JSetCrsr Pascal: procedure SetCursor(crsr: Cursor); Cursor record (68 bytes): 32 data + 32 mask + Point hotSpot. |
| **`SetEmptyRgn`** | `0x00BE4C` | `0x0165BC` | `Regions.s:438` | **Proto:** `PROCEDURE SetEmptyRgn(rgn: RgnHandle);`<br>.PROC SetEmptyRgn,1 .REF SetRectRgn PROCEDURE SetEmptyRgn(rgn: RgnHandle); Called during boot. |
| **`SETEMPTYRGN`** | `0x00BE4C` | `0x0165BC` | `Regions.s:355` | **Proto:** `PROCEDURE SetEmptyRgn(rgn: RgnHandle);`<br>PROCEDURE SetEmptyRgn(rgn: RgnHandle); |
| **`SetHSize`** | `0x008798` | `0x012ECE` | `Util.s:1026` | SetHSize -- mAKE THE BUFFER BIGGER. Called by: DOLINE_NO, DVPOS_OK, PutRect, PUTPT, EMPTY (and 6 more) |
| **`SETHSIZE`** | `0x008798` | `0x012ECE` | `GrafAsm.s:47` | SetHSize -- mAKE THE BUFFER BIGGER. Wraps _SetHandleSize, popping handle and new size off the stack. INPUT:   handle (long), new size (word), return address OUTPUT:  - (handle resized in place) Called... |
| **`SETMORE`** | `0x009D18` | `0x014488` | `DrawLine.s:803`<br>`DrawLine.s:677` | — |
| **`SETONE`** | `0x009D14` | `0x014484` | `DrawLine.s:800`<br>`DrawLine.s:674` | — |
| **`SetOrigin`** | `0x008A3A` | `0x013170` | `GrafAsm.s:455` | **Proto:** `PROCEDURE SetOrigin(h,v: INTEGER);`<br>PROCEDURE SetOrigin(h,v: INTEGER); { re-define the local coords by adjusting portBits.bounds, } { portRect, and visRgn } Called during boot. |
| **`SETORIGIN`** | `0x008A3A` | `0x013170` | `GrafAsm.s:449` | **Proto:** `PROCEDURE SetOrigin(h,v: INTEGER);`<br>PROCEDURE SetOrigin(h,v: INTEGER); { re-define the local coords by adjusting portBits.bounds, } { portRect, and visRgn } Called during boot. |
| **`SETORIGIN_DONE`** | `0x008A6A` | `0x0131A0` | `GrafAsm.s:475`<br>`GrafAsm.s:466` | — |
| **`SetPBits`** | `0x0089C8` | — | `GrafAsm.s:376` | **Proto:** `PROCEDURE SetPortBits(bm: BitMap);`<br>.PROC SetPortBits,1 .DEF BackPat PROCEDURE SetPortBits(bm: BitMap); { re-direct output to a different BitMap } |
| **`SetPenState`** | `0x0097D4` | `0x013F44` | `Lines.s:271` | **Proto:** `PROCEDURE SetPenState(pnState: PenState);`<br>.PROC GetPenState,1 .DEF SetPenState PROCEDURE GetPenState(VAR pnState: PenState); PROCEDURE SetPenState(pnState: PenState); Called during boot. |
| **`SETPENSTATE`** | `0x0097D4` | `0x013F44` | `Lines.s:261` | **Proto:** `PROCEDURE SetPenState(pnState: PenState);`<br>.PROC GetPenState,1 .DEF SetPenState PROCEDURE GetPenState(VAR pnState: PenState); PROCEDURE SetPenState(pnState: PenState); Called during boot. |
| **`SETPENSTATE_CONT`** | `0x0097D6` | `0x013F46` | `Lines.s:273`<br>`Lines.s:263` | — |
| **`SetPort`** | `0x0089B0` | `0x0130E6` | `GrafAsm.s:341` | **Proto:** `PROCEDURE SetPort(gp: GrafPtr);`<br>PROCEDURE SetPort(gp: GrafPtr); { switch the current port to a different GrafPort } Called during boot (30,216 times in 30s trace). |
| **`SETPORT`** | `0x0089B0` | `0x0130E6` | `GrafAsm.s:343` | **Proto:** `PROCEDURE SetPort(gp: GrafPtr);`<br>PROCEDURE SetPort(gp: GrafPtr); { switch the current port to a different GrafPort } Called during boot (30,216 times in 30s trace). |
| **`SETPORTBITS`** | — | `0x0130FE` | `GrafAsm.s:374` | **Proto:** `PROCEDURE SetPortBits(bm: BitMap);`<br>.PROC SetPortBits,1 .DEF BackPat PROCEDURE SetPortBits(bm: BitMap); { re-direct output to a different BitMap } |
| **`SETPORTBITS_SHARE`** | `0x0089D8` | `0x01310E` | `GrafAsm.s:383`<br>`GrafAsm.s:381` | — |
| **`SetPt`** | `0x008AA0` | `0x0131D6` | `GrafAsm.s:534` | **Proto:** `PROCEDURE SetPt(VAR pt: Point; h,v: INTEGER);`<br>.PROC SetPt PROCEDURE SetPt(VAR pt: Point; h,v: INTEGER); Called during boot. |
| **`SETPT`** | `0x008AA0` | `0x0131D6` | `GrafAsm.s:512` | **Proto:** `PROCEDURE SetPt(VAR pt: Point; h,v: INTEGER);`<br>PROCEDURE SetPt(VAR pt: Point; h,v: INTEGER); { stuff h,v into a Point variable } |
| **`SetRecRgn`** | `0x00BE58` | — | `Regions.s:453` | **Proto:** `PROCEDURE SetRectRgn(rgn: RgnHandle; left,top,right,bottom: INTEGER);`<br>.PROC SetRectRgn,5 .REF SetSize PROCEDURE SetRectRgn(rgn: RgnHandle; left,top,right,bottom: INTEGER); make a rectangular region from 4 integers. Called during boot (66,914 times in 30s trace). |
| **`SetRect`** | `0x00A082` | `0x0147F2` | `Rects.s:413` | **Proto:** `PROCEDURE SetRect(VAR r: Rect; left,top,right,bottom: INTEGER);`<br>.PROC SetRect PROCEDURE SetRect(VAR r: Rect; left,top,right,bottom: INTEGER); { assign 4 integers into a rectangle } Called during boot. |
| **`SETRECT`** | `0x00A082` | `0x0147F2` | `Rects.s:335` | **Proto:** `PROCEDURE SetRect(VAR r: Rect; left,top,right,bottom: INTEGER);`<br>.PROC SetRect PROCEDURE SetRect(VAR r: Rect; left,top,right,bottom: INTEGER); { assign 4 integers into a rectangle } Called during boot. |
| **`SETRECTRGN`** | — | `0x0165C8` | `Regions.s:367` | **Proto:** `PROCEDURE SetRectRgn(rgn: RgnHandle; left,top,right,bottom: INTEGER);`<br>PROCEDURE SetRectRgn(rgn: RgnHandle; left,top,right,bottom: INTEGER); Make a rectangular region from 4 integers. |
| **`SETRECTRGN_DONE`** | `0x00BEA6` | `0x016616` | `Regions.s:479`<br>`Regions.s:393` | — |
| **`SETRECTRGN_EMPTY`** | `0x00BE9E` | `0x01660E` | `Regions.s:476`<br>`Regions.s:390` | — |
| **`SETRECTRGN_OK`** | `0x00BE7E` | `0x0165EE` | `Regions.s:467`<br>`Regions.s:381` | — |
| **`SetStdProcs`** | `0x00891C` | `0x013052` | `GrafAsm.s:242` | _DisposHandle \| DISCARD IT .PROC SetStdProcs Fill a QDProcs record with standard QuickDraw procedure pointers from the Toolbox trap dispatch table. Order matches QDProcs (GrafTypes.s). |
| **`SETSTDPROCS`** | `0x00891C` | `0x013052` | `GrafAsm.s:249` | .PROC SetStdProcs Fill a QDProcs record with standard QuickDraw procedure pointers from the Toolbox trap dispatch table. Order matches QDProcs (GrafTypes.s). (SE FDHD trap-table addresses are offset 0... |
| **`SETTWO`** | `0x009D12` | `0x014482` | `DrawLine.s:798`<br>`DrawLine.s:672` | SETTWO Called during boot. |
| **`SETUP0`** | `0x00A4A4` | `0x014C14` | `BitBlt.s:468`<br>`BitBlt.s:369` | OPTIMIZE VERTICAL AND LEFT HORIZONTAL SCROLL IF SHIFT = 0. ONLY IF MODE 0, BUMPING LEFT TO RIGHT, WORDCNT > 0, AND NO SHIFT. |
| **`SetUpStretch`** | `0x00D52E` | `0x017CAA` | `Stretch.s:846` | SetUpStretch -- cALC CASEJUMP AND HORIZ FRACT. |
| **`SETUPSTRETCH`** | `0x00D52E` | `0x017CAA` | `Stretch.s:667` | SetUpStretch -- calc CaseJump and horiz Fract. Call with Numer in D0, Denom in D1. Returns case jump in A0, fraction in D0. |
| **`SHARE`** | `0x00B80E` | `0x015F7E` | `Angles.s:75`<br>`Angles.s:79` | look up tangent low word from table and apply sign |
| **`SHARE1`** | `0x008BEE` | `0x013324` | `Text.s:229`<br>`Text.s:197` | — |
| **`SHARE2`** | `0x008998` | `0x0130CE` | `GrafAsm.s:325`<br>`GrafAsm.s:328` | — |
| **`SHARE3`** | `0x0089AC` | `0x0130E2` | `GrafAsm.s:332`<br>`GrafAsm.s:335` | — |
| **`SHIELD_DO_HIDE`** | `0x001DF6` | `0x018F28` | `CrsrCore.s:220`<br>`CrsrCore.s:235` | — |
| **`SHIELD_NO_OVERLAP`** | `0x001DFC` | `0x018F2E` | `CrsrCore.s:229`<br>`CrsrCore.s:243` | SHIELD_NO_OVERLAP - No overlap: just decrement CrsrState Called during boot. |
| **`SHIELD_RETURN`** | `0x001E00` | `0x018F32` | `CrsrCore.s:231`<br>`CrsrCore.s:245` | — |
| **`ShieldCursor`** | `0x0082FE` | `0x012A34` | `LCursor.s:85` | **Proto:** `PROCEDURE ShieldCursor(shieldRect: Rect; offset: Point);`<br>.PROC ShieldCursor PROCEDURE ShieldCursor(shieldRect: Rect; offset: Point); ALL REGS PRESERVED. Called during boot. |
| **`SHIELDCURSOR`** | `0x0082FE` | `0x012A34` | `LCursor.s:56` | **Proto:** `Pascal: procedure ShieldCursor(shieldRect: Rect; offset: Point);`<br>SHIELDCURSOR ($A855) - hide cursor while drawing inside rect Pascal: procedure ShieldCursor(shieldRect: Rect; offset: Point); Translates global rect by offset, calls JShieldCursor with the 4 separate ... |
| **`SHLEFT`** | `0x008364` | `0x012A9A` | `Util.s:74`<br>`Util.s:51` | SHLEFT |
| **`SHORT`** | `0x008BCC` | `0x013302` | `Text.s:201`<br>`Text.s:171` | SHORT |
| **`SHORTLN`** | `0x00DE58` | `0x0185E4` | `Pictures.s:967`<br>`Pictures.s:700` | SHORTLN |
| **`SHOW_CLIP_BOTTOM`** | `0x001D6C` | `0x018E9E` | `CrsrCore.s:142`<br>`CrsrCore.s:159` | — |
| **`SHOW_CLIP_RIGHT`** | `0x001D46` | `0x018E78` | `CrsrCore.s:125`<br>`CrsrCore.s:142` | — |
| **`SHOW_CLIP_VERT`** | `0x001D56` | `0x018E88` | `CrsrCore.s:132`<br>`CrsrCore.s:149` | — |
| **`SHOW_DRAW_ROW`** | `0x001D9E` | `0x018ED0` | `CrsrCore.s:173`<br>`CrsrCore.s:189` | SHOW_DRAW_ROW - Cursor drawing inner loop For each row: reads cursor data and mask, shifts/clips to screen alignment, saves background longword, applies mask (AND NOT) then XORs cursor data onto scree... |
| **`SHOW_DRAW_TEST`** | `0x001DB4` | `0x018EE6` | `CrsrCore.s:185`<br>`CrsrCore.s:201` | — |
| **`SHOW_SET_RECT`** | `0x001D78` | `0x018EAA` | `CrsrCore.s:147`<br>`CrsrCore.s:164` | — |
| **`ShowCursor`** | `0x0082F8` | `0x012A2E` | `LCursor.s:73` | **Proto:** `PROCEDURE ShowCursor;`<br>.PROC ShowCursor PROCEDURE ShowCursor; ALL REGS PRESERVED. Called during boot. |
| **`SHOWCURSOR`** | `0x0082F8` | `0x012A2E` | `LCursor.s:47` | **Proto:** `Pascal: procedure ShowCursor;`<br>SHOWCURSOR ($A853) - show cursor via JShowCursor lowmem vector Pascal: procedure ShowCursor; Called by: GETPIXEL, STRDONE, DRAWLINE_DONE, RGNBLT_DONE, DRAWARC_DONE (and 4 more) |
| **`ShowPen`** | `0x0097C4` | `0x013F34` | `Lines.s:246` | **Proto:** `PROCEDURE ShowPen;`<br>PROCEDURE ShowPen; Called during boot. |
| **`SHOWPEN`** | `0x0097C4` | `0x013F34` | `Lines.s:238` | **Proto:** `PROCEDURE ShowPen;`<br>PROCEDURE ShowPen; Called during boot. |
| **`SHOWPEN_CONT`** | `0x0097C6` | `0x013F36` | `Lines.s:248`<br>`Lines.s:240` | — |
| **`SHRINK`** | `0x00D864` | `0x017FE0` | `Stretch.s:1332`<br>`Stretch.s:1148` | DO FULL RATIO SCALING, SHRINKING ONE BIT AT A TIME Called during boot. |
| **`SHRNKING`** | `0x00D5BA` | `0x017D36` | `Stretch.s:915`<br>`Stretch.s:731` | We will be shrinking. Calc fract = numer/denom and check for fast. Called during boot. |
| **`SHRNKING_LOOP`** | `0x00D5E8` | `0x017D64` | `Stretch.s:937`<br>`Stretch.s:752` | NUMERATOR = DENOMINATOR, JUST COPY LONGS |
| **`SIX`** | `0x00D758` | `0x017ED4` | `Stretch.s:1182`<br>`Stretch.s:999` | RTS ;ALL DONE STRETCH BY SIX USING TABLE LOOKUP |
| **`SIX_CONT`** | `0x00D784` | `0x017F00` | `Stretch.s:1204`<br>`Stretch.s:1021` | SIX_CONT - indexed branch table for stretch triple expansion |
| **`SIX_CONT_2`** | `0x00D794` | `0x017F10` | `Stretch.s:1209`<br>`Stretch.s:1030` | SIX_CONT_2 -- 4-bit input -> 16-bit sextupled mid word. 16 entries. |
| **`SIX_CONT_3`** | `0x00D7B4` | `0x017F30` | `Stretch.s:1217`<br>`Stretch.s:1043` | SIX_CONT_3 -- 3-bit input -> 16-bit sextupled lo word. 8 entries. |
| **`SIX_LOOP`** | `0x00D7C4` | — | `Stretch.s:1222` | — |
| **`SIXTEEN`** | `0x00D822` | `0x017F9E` | `Stretch.s:1266`<br>`Stretch.s:1096` | RTS ;ALL DONE SCALE UP BY 16 |
| **`SIXTENA`** | `0x00D828` | `0x017FA4` | `Stretch.s:1269`<br>`Stretch.s:1099` | — |
| **`SIZEOK`** | `0x009790` | `0x013F00` | `Lines.s:204`<br>`Lines.s:199` | — |
| **`SKIP0`** | `0x00C620` | `0x016D90` | `RgnOp.s:390`<br>`RgnOp.s:345` | — |
| **`SKIP1`** | `0x00C630` | `0x016DA0` | `RgnOp.s:406`<br>`RgnOp.s:359` | — |
| **`SKIP2`** | `0x00C63C` | `0x016DAC` | `RgnOp.s:420`<br>`RgnOp.s:371` | — |
| **`SKIP2_EXIT`** | `0x00C642` | `0x016DB2` | `RgnOp.s:430`<br>`RgnOp.s:379` | SKIP2_EXIT Called during boot (63,457 times in 30s trace). |
| **`SKIPCH`** | `0x009252` | `0x0139C2` | `DrawText.s:451`<br>`DrawText.s:387` | — |
| **`SlabMode`** | `0x008716` | `0x012E4C` | `Util.s:880` | **Proto:** `PROCEDURE SlabMode`<br>PROCEDURE SlabMode INPUT: D2: MODE, CLOBBERED OUTPUT: A4: MODECASE Called during boot. |
| **`SLABMODE`** | `0x008716` | `0x012E4C` | `Util.s:599` | SlabMode(D2 = mode) -> A4 = mode-specific scan handler Maps low 2 bits of mode to a JMP address from MODETAB. |
| **`SLABMODE_CONT`** | `0x00872A` | `0x012E60` | `Util.s:908`<br>`Util.s:622` | .BYTE MODETAB-MASK9 .BYTE MODETAB-MASK10 .BYTE MODETAB-MASK11 FAST LOOPS, OPTIMIZED FOR BLACK PATTERN AND RECTANGLE CLIPPED FAST BLACK SLAB: Called during boot. |
| **`SLABMODE_MODE_TBL`** | `0x008726` | `0x012E5C` | `Util.s:893`<br>`Util.s:609` | RTS SLABMODE_MODE_TBL |
| **`SLANTED`** | `0x0099A8` | `0x014118` | `DrawLine.s:278`<br>`DrawLine.s:213` | THE LINE IS SLANTED. SORT VERTICALLY AND DRAW TOP TO BOTTOM AS HORIZONTAL SLABS. |
| **`SLANTED_NO`** | `0x009A22` | `0x014192` | `DrawLine.s:345`<br>`DrawLine.s:272` | CALC adjust := pen height * slope ADJUST LEFTEDGE AND RIGHTEDGE DEPENDING ON SIGN AND MAGNITUDE OF SLOPE SLANTED_NO |
| **`SLOPE_POS`** | `0x00B79A` | `0x015F0A` | `Angles.s:14`<br>`Angles.s:20` | — |
| **`SlopeFromAngle`** | `0x00B7CE` | `0x015F3E` | `Angles.s:47` | **Proto:** `FUNCTION SlopeFromAngle(angle: INTEGER): Fixed;`<br>FUNCTION SlopeFromAngle(angle: INTEGER): Fixed; calculate the fixed point slope of a line, DH/DV = -65536 * Tan(angle). Input angle is treated MOD 180. |
| **`SLOPEFROMANGLE`** | `0x00B7CE` | `0x015F3E` | `Angles.s:51` | **Proto:** `FUNCTION SlopeFromAngle(angle: INTEGER): Fixed;`<br>FUNCTION SlopeFromAngle(angle: INTEGER): Fixed; Calculate the fixed point slope of a line, DH/DV = -65536 * Tan(angle). Input angle is treated MOD 180. |
| **`SMALL`** | `0x00863C` | `0x012D72` | `Util.s:632`<br>`Util.s:448` | — |
| **`SOLID`** | `0x00B2D2` | `0x015A42` | `DrawArc.s:485`<br>`DrawArc.s:349` | SOLID HIDE CURSOR IF CURSOR INTERSECTS MINRECT. Called during boot. |
| **`SortPoints`** | `0x00C6A8` | `0x016E18` | `SortPoints.s:23` | **Proto:** `PROCEDURE SortPoints(ptBuf: PointsPtr; ptCount: INTEGER);`<br>--> SORTPOINTS.TEXT Routines to sort inversion points and cull duplicates. .PROC SortPoints PROCEDURE SortPoints(ptBuf: PointsPtr; ptCount: INTEGER); PERFORMS A NON-RECURSIVE QUICKSORT ON AN ARRAY OF ... |
| **`SORTPOINTS`** | `0x00C6A8` | `0x016E18` | `SortPoints.s:21` | **Proto:** `PROCEDURE SortPoints(ptBuf: PointsPtr; ptCount: INTEGER);`<br>--> SORTPOINTS.TEXT Routines to sort inversion points and cull duplicates. PROCEDURE SortPoints(ptBuf: PointsPtr; ptCount: INTEGER); Performs a non-recursive Quicksort on an array of points to put the... |
| **`SORTPOINTS_GOHOME`** | `0x00C730` | `0x016EA0` | `SortPoints.s:140`<br>`SortPoints.s:115` | — |
| **`SORTPOINTS_LOOP`** | `0x00C6D0` | `0x016E40` | `SortPoints.s:42`<br>`SortPoints.s:36` | — |
| **`SORTPOINTS_NOSWAP`** | `0x00C71A` | `0x016E8A` | `SortPoints.s:124`<br>`SortPoints.s:100` | repeat until this partitioning is complete, IPtr > JPtr Called during boot. |
| **`SORTPOINTS_RIGHTOK`** | `0x00C726` | `0x016E96` | `SortPoints.s:134`<br>`SortPoints.s:109` | IF i < right then stack request to sort right partition |
| **`SOVAL`** | `0x00B608` | `0x015D78` | `DrawArc.s:963`<br>`DrawArc.s:717` | HOLLOW OVAL: DRAW TWO SLABS BETWEEN OUTER AND INNER OVALS SOVAL Called during boot. |
| **`SPACECH`** | `0x00924A` | `0x0139BA` | `DrawText.s:448`<br>`DrawText.s:384` | Set up space width Setup misc stuff in registers for speed Here's the main character drawing loop: Called during boot. |
| **`SpaceExtra`** | `0x008CA2` | `0x0133D8` | `Text.s:375` | **Proto:** `PROCEDURE SpaceExtra(extra: LongInt);`<br>.PROC SpaceExtra,1 .DEF DrawString,DrawText .REF CallText PROCEDURE SpaceExtra(extra: LongInt); |
| **`SPACEEXTRA`** | `0x008CA2` | `0x0133D8` | `Text.s:333` | **Proto:** `PROCEDURE SpaceExtra(extra: LongInt);`<br>.PROC SpaceExtra,1 .DEF DrawString,DrawText .REF CallText PROCEDURE SpaceExtra(extra: LongInt); |
| **`SPLIT`** | `0x00C6D4` | `0x016E44` | `SortPoints.s:44`<br>`SortPoints.s:38` | — |
| **`SPLIT_DONE_2`** | `0x00C70C` | `0x016E7C` | `SortPoints.s:111`<br>`SortPoints.s:89` | SIX if IPtr <= JPtr then swap IPtr^ and JPtr^, and bump both pointers Called during boot. |
| **`SPLIT_LOOP`** | `0x00C6F0` | `0x016E60` | `SortPoints.s:75`<br>`SortPoints.s:63` | — |
| **`SPLIT_LOOP_2`** | `0x00C700` | `0x016E70` | `SortPoints.s:98`<br>`SortPoints.s:80` | — |
| **`SPLIT_NEXT`** | `0x00C6EE` | `0x016E5E` | `SortPoints.s:73`<br>`SortPoints.s:61` | SPLIT_NEXT Called during boot. |
| **`SPLIT_RETRY`** | `0x00C6EC` | `0x016E5C` | `SortPoints.s:65`<br>`SortPoints.s:55` | CALC MIDPTR AND MIDPT SCAN WHILE IPTR^ < MIDPT DO BUMP IPTR TO RIGHT Called during boot. |
| **`SPOK`** | `0x008B78` | `0x0132AE` | `Text.s:144`<br>`Text.s:121` | CHECK NUMER, DENOM |
| **`SRCLOOP`** | `0x00D316` | `0x017A92` | `Stretch.s:450`<br>`Stretch.s:347` | GET FIRST SCANLINE OF SRC INTO SRCBUF WHILE (VERROR < 0) DO MERGE OTHER SCANLINES INTO SRCBUF. Called during boot. |
| **`SRCLOOP_EXIT`** | `0x00D348` | `0x017AC4` | `Stretch.s:481`<br>`Stretch.s:369` | WHILE (VERROR < 0) DO MERGE OTHER SCANLINES INTO SRCBUF. SRCOK HORIZONTALLY STRETCH SRCBUF INTO DSTBUF Called during boot. |
| **`SRCLOOP_LOOP`** | `0x00D328` | `0x017AA4` | `Stretch.s:456`<br>`Stretch.s:353` | — |
| **`SRCOK`** | `0x00CA70` | `0x0171EC` | `Bitmaps.s:256`<br>`Bitmaps.s:222` | TEST IF DST IS TO THEPORT, (IF SO WE CLIP) Called during boot. |
| **`START`** | `0x00CFB0` | `0x01772C` | `Bitmaps.s:1052`<br>`Bitmaps.s:882` | — |
| **`START1`** | `0x00C9F6` | `0x017172` | `Bitmaps.s:171`<br>`Bitmaps.s:153` | — |
| **`START2`** | `0x00CA06` | `0x017182` | `Bitmaps.s:183`<br>`Bitmaps.s:164` | — |
| **`START2_DONE`** | `0x00CA0A` | `0x017186` | `Bitmaps.s:185`<br>`Bitmaps.s:166` | — |
| **`STARTOK`** | `0x00B128` | `0x015898` | `DrawArc.s:259`<br>`DrawArc.s:163` | IF ARCANGLE < 360 THEN SET UP ARC STUFF TREAT STARTANGLE MOD 360 |
| **`STD`** | `0x008D30` | `0x013466` | `Text.s:480`<br>`Text.s:424` | UNLK TAKES CARE OF SP |
| **`StdArc`** | `0x00AF58` | `0x0156C8` | `Arcs.s:24` | **Proto:** `PROCEDURE StdArc(verb: GrafVerb; r: Rect; startAngle,arcAngle: INTEGER);`<br>*    *****    ***    *** * *   *    *  *   *  *   * *   *  *    *  *      * *   *  *****   *       *** *****  *  *    *          * *   *  *   *   *   *  *   * *   *  *    *   ***    *** Procedures for... |
| **`STDARC`** | `0x00AF58` | `0x0156C8` | `Arcs.s:36` | **Proto:** `PROCEDURE StdArc(verb: GrafVerb; r: Rect; startAngle,arcAngle: INTEGER);`<br>*    *****    ***    *** * *   *    *  *   *  *   * *   *  *    *  *      * *   *  *****   *       *** *****  *  *    *          * *   *  *   *   *   *  *   * *   *  *    *   ***    *** Procedures for... |
| **`StdBits`** | `0x00C8CC` | `0x017048` | `Bitmaps.s:31` | **Proto:** `PROCEDURE StdBits(VAR srcBits: BitMap;`<br>****   ***  *****  *     *     *     ****    *** *   *   *     *    **   **    * *    *   *  *   * *   *   *     *    * * * *   *   *   *   *  * ****    *     *    *  *  *   *   *   ****    *** *   * ... |
| **`STDBITS`** | `0x00C8CC` | `0x017048` | `Bitmaps.s:37` | **Proto:** `PROCEDURE StdBits(VAR srcBits: BitMap;`<br>****   ***  *****  *     *     *     ****    *** *   *   *     *    **   **    * *    *   *  *   * *   *   *     *    * * * *   *   *   *   *  * ****    *     *    *  *  *   *   *   ****    *** *   * ... |
| **`STDBITS_GOHOME`** | `0x00CA3C` | `0x0171B8` | `Bitmaps.s:202`<br>`Bitmaps.s:183` | — |
| **`STDBITS_NOTPIC`** | `0x00CA0C` | `0x017188` | `Bitmaps.s:187`<br>`Bitmaps.s:168` | — |
| **`StdComment`** | `0x00D8D0` | `0x01804C` | `Pictures.s:22` | **Proto:** `PROCEDURE StdComment(kind,dataSize: INTEGER; dataHandle: Handle);`<br>****   ***   ***   *****  *   *  ****   *****   *** *   *   *   *   *    *    *   *  *   *  *      *   * *   *   *   *        *    *   *  *   *  *      * ****    *   *        *    *   *  ****   ***   ... |
| **`STDCOMMENT`** | `0x00D8D0` | `0x01804C` | `Pictures.s:22` | **Proto:** `PROCEDURE StdComment(kind, dataSize: INTEGER; dataHandle: Handle);`<br>****   ***   ***   *****  *   *  ****   *****   *** *   *   *   *   *    *    *   *  *   *  *      *   * *   *   *   *        *    *   *  *   *  *      * ****    *   *        *    *   *  ****   ***   ... |
| **`STDCOMMENT_DONE`** | `0x00D924` | `0x0180A0` | `Pictures.s:70`<br>`Pictures.s:59` | DATASIZE > 0, USE LONG FORMAT |
| **`STDCOMMENT_OK`** | `0x00D8FA` | `0x018076` | `Pictures.s:51`<br>`Pictures.s:44` | DATASIZE 0, USE SHORT FORMAT STDCOMMENT_OK |
| **`StdGetPic`** | `0x00D930` | `0x0180AC` | `Pictures.s:82` | **Proto:** `PROCEDURE StdGetPic(dataPtr: QDPtr; byteCount: INTEGER);`<br>.PROC StdGetPic PROCEDURE StdGetPic(dataPtr: QDPtr; byteCount: INTEGER); |
| **`STDGETPIC`** | `0x00D930` | `0x0180AC` | `Pictures.s:72` | **Proto:** `PROCEDURE StdGetPic(dataPtr: QDPtr; byteCount: INTEGER);`<br>PROCEDURE StdGetPic(dataPtr: QDPtr; byteCount: INTEGER); Read byteCount bytes from the picture being played back into the buffer at dataPtr. Bumps PlayIndex by byteCount. |
| **`STDGETPIC_START`** | `0x00D950` | `0x0180CC` | `Pictures.s:102`<br>`Pictures.s:91` | — |
| **`StdLine`** | `0x009668` | `0x013DD8` | `Lines.s:24` | **Proto:** `PROCEDURE StdLine(newPt: Point);`<br>*      ***   *   *  *****   *** *       *    *   *  *      *   * *       *    **  *  *      * *       *    * * *  ***     *** *       *    *  **  *          * *       *    *   *  *      *   * *****  *... |
| **`STDLINE`** | `0x009668` | `0x013DD8` | `Lines.s:32` | **Proto:** `PROCEDURE StdLine(newPt: Point);`<br>*      ***   *   *  *****   *** *       *    *   *  *      *   * *       *    **  *  *      * *       *    * * *  ***     *** *       *    *  **  *          * *       *    *   *  *      *   * *****  *... |
| **`STDLINE_NO`** | `0x009690` | `0x013E00` | `Lines.s:54`<br>`Lines.s:55` | — |
| **`STDLINE_NOTPIC`** | `0x0096E8` | `0x013E58` | `Lines.s:95`<br>`Lines.s:95` | — |
| **`STDLINE_STARTOK`** | `0x0096C2` | `0x013E32` | `Lines.s:75`<br>`Lines.s:76` | — |
| **`StdOval`** | `0x00AD4C` | `0x0154BC` | `Ovals.s:26` | **Proto:** `PROCEDURE StdOval(verb: GrafVerb; r: Rect);`<br>***   *   *    *    *      *** *   *  *   *   * *   *     *   * *   *  *   *  *   *  *     * *   *  *   *  *   *  *      *** *   *  *   *  *****  *         * *   *   * *   *   *  *     *   * ***     *... |
| **`STDOVAL`** | `0x00AD4C` | `0x0154BC` | `Ovals.s:32` | **Proto:** `PROCEDURE StdOval(verb: GrafVerb; r: Rect);`<br>***   *   *    *    *      *** *   *  *   *   * *   *     *   * *   *  *   *  *   *  *     * *   *  *   *  *   *  *      *** *   *  *   *  *****  *         * *   *   * *   *   *  *     *   * ***     *... |
| **`STDOVAL_DOIT`** | `0x00ADB6` | `0x015526` | `Ovals.s:82`<br>`Ovals.s:73` | — |
| **`STDOVAL_NOTPIC`** | `0x00AD72` | `0x0154E2` | `Ovals.s:53`<br>`Ovals.s:45` | OVWD .EQU -2 ;WORD OVHT .EQU OVWD-2 ;WORD VARSIZE .EQU OVHT ;TOTAL BYTES OF LOCALS |
| **`STDOVAL_NOTRGN`** | `0x00ADAE` | `0x01551E` | `Ovals.s:72`<br>`Ovals.s:64` | — |
| **`StdPoly`** | `0x00B982` | `0x0160F2` | `Polygons.s:25` | **Proto:** `PROCEDURE StdPoly(verb: GrafVerb; poly: PolyHandle);`<br>****    ***   *    *   *   ***    ***   *   *   *** *   *  *   *  *     * *   *   *  *   *  *   *  *   * *   *  *   *  *      *    *      *   *  **  *  * ****   *   *  *      *    *  **  *   *  * * * ... |
| **`STDPOLY`** | `0x00B982` | `0x0160F2` | `Polygons.s:23` | **Proto:** `PROCEDURE StdPoly(verb: GrafVerb; poly: PolyHandle);`<br>****    ***   *    *   *   ***    ***   *   *   *** *   *  *   *  *     * *   *   *  *   *  *   *  *   * *   *  *   *  *      *    *      *   *  **  *  * ****   *   *  *      *    *  **  *   *  * * * ... |
| **`STDPOLY_GOHOME`** | `0x00B9EC` | `0x01615C` | `Polygons.s:78`<br>`Polygons.s:64` | — |
| **`STDPOLY_NOTFR`** | `0x00B9BA` | `0x01612A` | `Polygons.s:62`<br>`Polygons.s:48` | STDPOLY_NOTFR |
| **`STDPOLY_NOTPIC`** | `0x00B9AA` | `0x01611A` | `Polygons.s:50`<br>`Polygons.s:36` | MINRECT .EQU -8 ;RECT VARSIZE .EQU MINRECT ;TOTAL BYTES OF LOCALS |
| **`StdPutPic`** | `0x00D956` | `0x0180D2` | `Pictures.s:117` | **Proto:** `PROCEDURE StdPutPic(dataPtr: QDPtr; byteCount: INTEGER);`<br>.PROC StdPutPic,1 .REF SetSize PROCEDURE StdPutPic(dataPtr: QDPtr; byteCount: INTEGER); Append some picture bytes to a growing handle. PARAMSIZE .EQU 6 SRCPTR .EQU PARAMSIZE+8-4 ;LONG BYTECOUNT .EQU S... |
| **`STDPUTPIC`** | `0x00D956` | `0x0180D2` | `Pictures.s:107` | **Proto:** `PROCEDURE StdPutPic(dataPtr: QDPtr; byteCount: INTEGER);`<br>PROCEDURE StdPutPic(dataPtr: QDPtr; byteCount: INTEGER); Append some picture bytes to a growing handle. Auto-grows by 256 bytes if PicMax is exceeded. On allocation failure, marks the picture dead (Pi... |
| **`STDPUTPIC_ERR`** | `0x00D9B4` | `0x018130` | `Pictures.s:170`<br>`Pictures.s:153` | time to grow the picture in chunks of at least 256 bytes Failed to grow picture, so we will trim handle down to 10 bytes, clear PicIndex, and set picSize to -1, PicFrame to (0,0,0,0). STDPUTPIC_ERR |
| **`STDPUTPIC_GOHOME`** | `0x00D9CA` | `0x018146` | `Pictures.s:190`<br>`Pictures.s:168` | — |
| **`STDPUTPIC_NXTBYTE`** | `0x00D9C4` | `0x018140` | `Pictures.s:186`<br>`Pictures.s:164` | now copy the data bytes into the picture: STDPUTPIC_NXTBYTE |
| **`STDPUTPIC_START`** | `0x00D9C6` | `0x018142` | `Pictures.s:188`<br>`Pictures.s:166` | now copy the data bytes into the picture: STDPUTPIC_NXTBYTE |
| **`StdRect`** | `0x009E7E` | `0x0145EE` | `Rects.s:27` | **Proto:** `PROCEDURE StdRect(verb: GrafVerb; r: Rect);`<br>****   *****   ***   *****   *** *   *  *      *   *    *    *   * *   *  *      *        *    * ****   ***    *        *     *** * *    *      *        *        * *  *   *      *   *    *    *   * * ... |
| **`STDRECT`** | `0x009E7E` | `0x0145EE` | `Rects.s:38` | **Proto:** `PROCEDURE StdRect(verb: GrafVerb; r: Rect);`<br>****   *****   ***   *****   *** *   *  *      *   *    *    *   * *   *  *      *        *    * ****   ***    *        *     *** * *    *      *        *        * *  *   *      *   *    *    *   * * ... |
| **`STDRECT_GOHOME`** | `0x009ED4` | `0x014644` | `Rects.s:67`<br>`Rects.s:73` | — |
| **`STDRECT_NOTFR`** | `0x009ECC` | `0x01463C` | `Rects.s:64`<br>`Rects.s:70` | STDRECT_NOTFR Called during boot. |
| **`STDRECT_NOTPIC`** | `0x009EA4` | `0x014614` | `Rects.s:44`<br>`Rects.s:51` | — |
| **`STDRECT_NOTRGN`** | `0x009EC6` | `0x014636` | `Rects.s:55`<br>`Rects.s:62` | — |
| **`StdRgn`** | `0x00BBF6` | `0x016366` | `Regions.s:27` | **Proto:** `PROCEDURE StdRgn(verb: GrafVerb; rgn: RgnHandle);`<br>****   *****   ***   ***   ***   *   *   *** *   *  *      *   *   *   *   *  *   *  *   * *   *  *      *       *   *   *  **  *  * ****   ***    *  **   *   *   *  * * *   *** * *    *      *   *   ... |
| **`STDRGN`** | `0x00BBF6` | `0x016366` | `Regions.s:25` | **Proto:** `PROCEDURE StdRgn(verb: GrafVerb; rgn: RgnHandle);`<br>****   *****   ***   ***   ***   *   *   *** *   *  *      *   *   *   *   *  *   *  *   * *   *  *      *       *   *   *  **  *  * ****   ***    *  **   *   *   *  * * *   *** * *    *      *   *   ... |
| **`STDRGN_GOHOME`** | `0x00BC50` | `0x0163C0` | `Regions.s:67`<br>`Regions.s:59` | — |
| **`STDRGN_NOTFR`** | `0x00BC4C` | `0x0163BC` | `Regions.s:65`<br>`Regions.s:57` | STDRGN_NOTFR Called during boot. |
| **`STDRGN_NOTPIC`** | `0x00BC20` | `0x016390` | `Regions.s:44`<br>`Regions.s:38` | — |
| **`STDRGN_NOTRGN`** | `0x00BC46` | `0x0163B6` | `Regions.s:56`<br>`Regions.s:50` | — |
| **`StdRRect`** | `0x00AC70` | `0x0153E0` | `RRects.s:26` | **Proto:** `PROCEDURE StdRRect(verb: GrafVerb; r: Rect; ovWd,ovHt: INTEGER);`<br>****   ****   *****   ***   *****   *** *   *  *   *  *      *   *    *    *   * *   *  *   *  *      *        *    * ****   ****   ***    *        *     *** * *    * *    *      *        *        * *... |
| **`STDRRECT`** | `0x00AC70` | `0x0153E0` | `RRects.s:37` | **Proto:** `PROCEDURE StdRRect(verb: GrafVerb; r: Rect; ovWd,ovHt: INTEGER);`<br>****   ****   *****   ***   *****   *** *   *  *   *  *      *   *    *    *   * *   *  *   *  *      *        *    * ****   ****   ***    *        *     *** * *    * *    *      *        *        * *... |
| **`STDRRECT_DOIT`** | `0x00ACE2` | `0x015452` | `RRects.s:75`<br>`RRects.s:79` | — |
| **`STDRRECT_NOTPIC`** | `0x00ACB6` | `0x015426` | `RRects.s:60`<br>`RRects.s:64` | — |
| **`STDRRECT_NOTRGN`** | `0x00ACDE` | `0x01544E` | `RRects.s:73`<br>`RRects.s:77` | — |
| **`StdText`** | `0x008AB6` | `0x0131EC` | `Text.s:26` | **Proto:** `PROCEDURE StdText(count: INTEGER; textAddr: Ptr; numer,denom: Point);`<br>*****  *****  *   *  ***** *    *      *   *    * *    *       * *     * *    ***      *      * *    *       * *     * *    *      *   *    * *    *****  *   *    * Routines for measuring and drawing ... |
| **`STDTEXT`** | `0x008AB6` | `0x0131EC` | `Text.s:28` | **Proto:** `PROCEDURE StdText(count: INTEGER; textAddr: Ptr; numer,denom: Point);`<br>*****  *****  *   *  ***** *    *      *   *    * *    *       * *     * *    ***      *      * *    *       * *     * *    *      *   *    * *    *****  *   *    * Routines for measuring and drawing ... |
| **`STDTEXT_DHDV`** | `0x008BE6` | `0x01331C` | `Text.s:224`<br>`Text.s:192` | STDTEXT_DHDV |
| **`STDTEXT_GOHOME`** | `0x008C34` | `0x01336A` | `Text.s:266`<br>`Text.s:232` | STDTEXT_GOHOME Called during boot. |
| **`STDTEXT_MODEOK`** | `0x008B3E` | `0x013274` | `Text.s:114`<br>`Text.s:93` | CHECK TXSIZE |
| **`STDTEXT_NOTPIC`** | `0x008C0E` | `0x013344` | `Text.s:248`<br>`Text.s:215` | DrText(count,textAddr,numer,denom); Called during boot. |
| **`STDTEXT_NOTSAME`** | `0x008B8C` | `0x0132C2` | `Text.s:155`<br>`Text.s:128` | CHECK NUMER, DENOM |
| **`STDTEXT_NOTSAME_CONT`** | `0x008BC8` | `0x0132FE` | `Text.s:194`<br>`Text.s:165` | STDTEXT_NOTSAME_CONT |
| **`STDTEXT_NOTSAME_NO`** | `0x008BA6` | `0x0132DC` | `Text.s:173`<br>`Text.s:145` | NUMEROK USE DH AND DV TO CHOOSE ONE OF FOUR TEXT OPCODES. |
| **`STDTEXT_NOTSAME_NO_2`** | `0x008BC4` | `0x0132FA` | `Text.s:187`<br>`Text.s:159` | STDTEXT_NOTSAME_NO_2 -- pUT OPCODE. JDPutPicByte |
| **`STDTEXT_SHARE2`** | `0x008BF0` | `0x013326` | `Text.s:231`<br>`Text.s:199` | — |
| **`STDTEXT_SIZEOK`** | `0x008B5C` | `0x013292` | `Text.s:129`<br>`Text.s:107` | CHECK SPEXTRA |
| **`StdTxMeas`** | `0x008D50` | `0x013486` | `Text.s:512` | **Proto:** `FUNCTION StdTxMeas(count: INTEGER; textAddr: Ptr;`<br>.FUNC StdTxMeas,5 FUNCTION StdTxMeas(count: INTEGER; textAddr: Ptr; VAR numer,denom: Point; VAR info: FontInfo): INTEGER; Measure some text, returning unscaled values plus updated scale factor. Fills ... |
| **`STDTXMEAS`** | `0x008D50` | `0x013486` | `Text.s:455` | **Proto:** `FUNCTION StdTxMeas(count: INTEGER; textAddr: Ptr;`<br>.FUNC StdTxMeas,5 FUNCTION StdTxMeas(count: INTEGER; textAddr: Ptr; VAR numer,denom: Point; VAR info: FontInfo): INTEGER; Measure some text, returning unscaled values plus updated scale factor. Fills ... |
| **`STDTXMEAS_MORE`** | `0x008DDC` | `0x013512` | `Text.s:580`<br>`Text.s:516` | — |
| **`STDTXMEAS_NEXTCH`** | `0x008DD2` | `0x013508` | `Text.s:575`<br>`Text.s:511` | _SwapFont ;CALL FMSWAPFONT UPDATE NUMER AND DENOM STDTXMEAS_NEXTCH Called during boot (62,735 times in 30s trace). |
| **`STKOK1`** | `0x00C43E` | `0x016BAE` | `RgnOp.s:114`<br>`RgnOp.s:99` | Calc bufSize based on StackAvail and allocate 5 scan buffers _StackAvail ;get stack avail in D0.L STKOK1 Called during boot (7,474 times in 30s trace). |
| **`STKOK2`** | `0x00C448` | `0x016BB8` | `RgnOp.s:118`<br>`RgnOp.s:103` | — |
| **`StolenFromAppleBitmap`** | — | `0x0188BE` | `Pictures.s:1013` | — |
| **`StolenFromAppleBitmap_32x25`** | — | `0x0188BE` | `Pictures.s:1015` | 25 rows x 32 pixels embedded bitmap. |
| **`StolenFromAppleEntrypoint`** | — | `0x0188A4` | `Pictures.s:1000` | Debugger trigger G 4188A4; copies bitmap then loops forever. Easter egg, executable only via debugger trigger "G 4188A4". Loads QuickDraw thePort baseAddr (A1) and rowBytes (D0), then copies a 32x25 1... |
| **`StolenFromAppleRoutine`** | — | `0x0188A4` | `Pictures.s:993` | — |
| **`STOPOK`** | `0x00B13A` | `0x0158AA` | `DrawArc.s:265`<br>`DrawArc.s:169` | — |
| **`STOPOK_CONT`** | `0x00B20E` | `0x01597E` | `DrawArc.s:370`<br>`DrawArc.s:260` | SET UP FLAG1 AND FLAG2 TO TELL WHICH HALF EACH LINE IS ACTIVE IN: CODE IS: NEG = ACTIVE IN TOP, POS = ACTIVE IN BOTTOM, 0 = HORIZONTAL |
| **`STOPOK_CONT_2`** | `0x00B228` | `0x015998` | `DrawArc.s:385`<br>`DrawArc.s:274` | — |
| **`STOPOK_OK`** | `0x00B208` | `0x015978` | `DrawArc.s:361`<br>`DrawArc.s:257` | SET UP FLAG1 AND FLAG2 TO TELL WHICH HALF EACH LINE IS ACTIVE IN: CODE IS: NEG = ACTIVE IN TOP, POS = ACTIVE IN BOTTOM, 0 = HORIZONTAL STOPOK_OK |
| **`STOPOK_OK_2`** | `0x00B222` | `0x015992` | `DrawArc.s:382`<br>`DrawArc.s:271` | STOPOK_OK_2 |
| **`STORE_SCRN_WIDTH`** | `0x001E6C` | `0x018F9E` | `CrsrCore.s:312`<br>`CrsrCore.s:310` | — |
| **`STRCHING`** | `0x00D54A` | — | `Stretch.s:860` | We will be stretching. Calc fract = denom/numer and check for fast. |
| **`STRDONE`** | `0x0093EE` | `0x013B5E` | `DrawText.s:727`<br>`DrawText.s:629` | — |
| **`STRDONE_CONT`** | `0x009400` | `0x013B70` | `DrawText.s:739`<br>`DrawText.s:640` | STRDONE_CONT Called during boot. |
| **`STRETCH`** | `0x00D0C6` | `0x017842` | `Stretch.s:121`<br>`Stretch.s:82` | STRETCH Called during boot. |
| **`StretchBits`** | `0x00D062` | `0x0177DE` | `Stretch.s:28` | **Proto:** `PROCEDURE StretchBits(srcBits,dstBits: BitMap;`<br>--> STRETCH.TEXT .PROC StretchBits,8 .REF RgnBlt,RSect,ShieldCursor,ShowCursor .REF InitRgn,SeekRgn,SetupStretch,ColorMap,XorSlab PROCEDURE StretchBits(srcBits,dstBits: BitMap; srcRect,dstRect: Rect; ... |
| **`STRETCHBITS`** | `0x00D062` | `0x0177DE` | `Stretch.s:34` | **Proto:** `PROCEDURE StretchBits(srcBits, dstBits: BitMap;`<br>--> STRETCH.TEXT PROCEDURE StretchBits(srcBits, dstBits: BitMap; srcRect, dstRect: Rect; mode: INTEGER; rgnA, rgnB, rgnC: RgnHandle); Transfer a rectangle of bits from srcBits to dstBits, stretching o... |
| **`STRETCHBITS_ABCDONE`** | `0x00D4AE` | `0x017C2A` | `Stretch.s:715`<br>`Stretch.s:552` | — |
| **`STRETCHBITS_ABCDONE_LOOP`** | `0x00D4B0` | `0x017C2C` | `Stretch.s:723`<br>`Stretch.s:571` | STRETCHBITS_ABCDONE_LOOP Called during boot. |
| **`STRETCHBITS_ABCDONE_LOOP_2`** | `0x00D4D4` | `0x017C50` | `Stretch.s:762`<br>`Stretch.s:591` | STRETCHBITS_ABCDONE_LOOP_2 |
| **`STRETCHBITS_ABCDONE_LOOP_3`** | `0x00D4F0` | `0x017C6C` | `Stretch.s:784`<br>`Stretch.s:607` | MODE 1 OR 5: SRC OR DST --> DST STRETCHBITS_ABCDONE_LOOP_3 |
| **`STRETCHBITS_ABCDONE_LOOP_4`** | `0x00D50C` | `0x017C88` | `Stretch.s:806`<br>`Stretch.s:623` | MODE 2 OR 6: SRC XOR DST --> DST STRETCHBITS_ABCDONE_LOOP_4 |
| **`STRETCHBITS_ABCDONE_MODE_TBL`** | `0x00D52A` | `0x017CA6` | `Stretch.s:843`<br>`Stretch.s:657` | MODE 3 OR 7: SRC BIC DST --> DST .PROC SetupStretch Routine to setup case jump for StretchRow, based on horiz numer and denom. Call SetupStretch with numer in D0, denom in D1. Returns case jump in A0,... |
| **`STRETCHBITS_ABCLOOP`** | `0x00D4A2` | `0x017C1E` | `Stretch.s:709`<br>`Stretch.s:546` | — |
| **`STRETCHBITS_BCLOOP`** | `0x00D462` | `0x017BDE` | `Stretch.s:677`<br>`Stretch.s:518` | Common 2-region intersection into MaskBuf |
| **`STRETCHBITS_BCLOOP_CONT`** | `0x00D46E` | — | `Stretch.s:690` | REGIONS A, B AND C ARE ALL NON-RECTANGULAR. UPDATE EACH, THEN FORM INTERSECTION IN THE MASK BUFFER. |
| **`STRETCHBITS_BCLOOP_DONE`** | `0x00D46C` | — | `Stretch.s:682` | — |
| **`STRETCHBITS_CLRMASK`** | `0x00D192` | `0x01790E` | `Stretch.s:233`<br>`Stretch.s:174` | CALC BUFLEFT AND BUFSIZE FOR RGN SCANLINE BUFFERS ALLOCATE AND CLEAR A SCANLINE BUFFER FOR THE COMPOSITE MASK. Called during boot. |
| **`STRETCHBITS_CLRMASK_CONT`** | `0x00D1F6` | `0x017972` | `Stretch.s:294`<br>`Stretch.s:220` | BRECT STRETCHBITS_CLRMASK_CONT -- iNIT STATE, ALLOC BUFFER. |
| **`STRETCHBITS_CLRMASK_EXIT`** | `0x00D206` | `0x017982` | `Stretch.s:305`<br>`Stretch.s:229` | STRETCHBITS_CLRMASK_EXIT Called during boot. |
| **`STRETCHBITS_CLRMASK_NO`** | `0x00D224` | `0x0179A0` | `Stretch.s:329`<br>`Stretch.s:242` | CRECT IF ALL REGIONS ARE RECTANGULAR, THEN DRAW MINRECT INTO MASK BUFFER NOTRECT SET UP INVERT FLAG IN D7 TO REFLECT MODE BIT 2 Called during boot. |
| **`STRETCHBITS_CLRMASK_SKIP`** | `0x00D1D0` | `0x01794C` | `Stretch.s:270`<br>`Stretch.s:203` | ARECT Called during boot. |
| **`STRETCHBITS_CLRMASK_SKIP_2`** | `0x00D1E2` | `0x01795E` | `Stretch.s:283`<br>`Stretch.s:211` | ARECT BRECT Called during boot. |
| **`STRETCHBITS_CLRMASK_SKIP_3`** | `0x00D236` | `0x0179B2` | `Stretch.s:336`<br>`Stretch.s:249` | — |
| **`STRETCHBITS_CPY2BUF`** | `0x00D45A` | `0x017BD6` | `Stretch.s:674`<br>`Stretch.s:515` | Common 2-region intersection into MaskBuf |
| **`STRETCHBITS_DONE`** | `0x00D3AC` | `0x017B28` | `Stretch.s:543`<br>`Stretch.s:409` | ENTIRE STRETCHBITS COMPLETE. RESTORE REGS AND STACK AND GO HOME. Called during boot. |
| **`STRETCHBITS_GOHOME`** | `0x00D3B0` | `0x017B2C` | `Stretch.s:545`<br>`Stretch.s:411` | — |
| **`STRETCHBITS_GOHOME_CONT`** | `0x00D3C2` | `0x017B3E` | `Stretch.s:558`<br>`Stretch.s:422` | LOCAL ROUTINE TO UPDATE MASK BUFFER TO CURRENT VERTICAL COORD. Called during boot. |
| **`STRETCHBITS_GOHOME_CONT_2`** | `0x00D3D2` | — | `Stretch.s:568` | STRETCHBITS_GOHOME_CONT_2 - indexed branch table for StretchBits region masking modes |
| **`STRETCHBITS_GOHOME_CONT_3`** | `0x00D3E2` | `0x017B5E` | `Stretch.s:577`<br>`Stretch.s:449` | ONLY REGION A IS NON RECTANGULAR. UPDATE IT AND USE IT AS THE MASK |
| **`STRETCHBITS_GOHOME_CONT_4`** | `0x00D3E8` | `0x017B64` | `Stretch.s:594`<br>`Stretch.s:456` | LOCAL ROUTINE TO UPDATE MASK BUFFER TO CURRENT VERTICAL COORD. ONLY REGION B IS NON RECTANGULAR. UPDATE IT AND USE IT AS THE MASK Called during boot. |
| **`STRETCHBITS_GOHOME_CONT_5`** | `0x00D3EE` | `0x017B6A` | `Stretch.s:605`<br>`Stretch.s:463` | ONLY REGION C IS NON RECTANGULAR. UPDATE IT AND USE IT AS THE MASK |
| **`STRETCHBITS_GOHOME_CONT_AB`** | — | `0x017B78` | `Stretch.s:474` | Two regions A and B are non rectangular. Update each, then form intersection in the MaskBuf. |
| **`STRETCHBITS_GOHOME_CONT_ABC`** | — | `0x017BEA` | `Stretch.s:530` | Three regions A, B, C are non rectangular. Update each, then form intersection in MaskBuf. |
| **`STRETCHBITS_GOHOME_CONT_AC`** | — | `0x017B98` | `Stretch.s:489` | Two regions A and C are non rectangular. |
| **`STRETCHBITS_GOHOME_CONT_BC`** | — | `0x017BB8` | `Stretch.s:504` | Two regions B and C are non rectangular. |
| **`STRETCHBITS_JMPSEEK`** | `0x00D3F2` | — | `Stretch.s:607` | — |
| **`STRETCHBITS_JMPSEEK_CONT`** | `0x00D3FC` | — | `Stretch.s:621` | ONLY REGION C IS NON RECTANGULAR. UPDATE IT AND USE IT AS THE MASK REGIONS A AND B ARE NON-RECTANGULAR. UPDATE EACH, THEN FORM INTERSECTION IN THE MASK BUFFER. |
| **`STRETCHBITS_JMPSEEK_CONT_2`** | `0x00D41C` | — | `Stretch.s:641` | REGIONS A AND C ARE NON-RECTANGULAR. UPDATE EACH, THEN FORM INTERSECTION IN THE MASK BUFFER. |
| **`STRETCHBITS_JMPSEEK_CONT_3`** | `0x00D43C` | — | `Stretch.s:661` | REGIONS B AND C ARE NON-RECTANGULAR. UPDATE EACH, THEN FORM INTERSECTION IN THE MASK BUFFER. |
| **`STRETCHBITS_JSRSEEK`** | — | `0x017B6E` | `Stretch.s:466` | Common: SeekRgn for one region, then store its scan buffer as MaskBuf |
| **`STRETCHBITS_NXTMASK`** | `0x00D364` | `0x017AE0` | `Stretch.s:503`<br>`Stretch.s:382` | SRCOK HORIZONTALLY STRETCH SRCBUF INTO DSTBUF TRANSFER ONE OR MORE COPIES OF DSTBUF INTO DSTBITS Called during boot. |
| **`STRETCHBITS_RECTFLAG_TBL`** | — | `0x017B4E` | `Stretch.s:439` | STRETCHBITS_RECTFLAG_TBL -- branch offsets table for RectFlag (5 entries): 0x009A: all rect (no-op, jump to JSRSEEK_CONT) 0x0010: only A non-rect (-> _CONT_3) 0x0016: only A non-rect (alt path) 0x002A... |
| **`StringWidth`** | `0x008CD8` | `0x01340E` | `Text.s:424` | **Proto:** `FUNCTION StringWidth(s: Str255): INTEGER;`<br>.FUNC StringWidth,1 .REF TextWidth FUNCTION StringWidth(s: Str255): INTEGER; Called during boot (6,954 times in 30s trace). |
| **`STRINGWIDTH`** | `0x008CD8` | `0x01340E` | `Text.s:373` | **Proto:** `FUNCTION StringWidth(s: Str255): INTEGER;`<br>.FUNC StringWidth,1 .REF TextWidth FUNCTION StringWidth(s: Str255): INTEGER; Called during boot (6,954 times in 30s trace). |
| **`StuffHex`** | `0x008608` | `0x012D3E` | `Util.s:602` | **Proto:** `PROCEDURE STUFFHEX(THINGPTR: WORDPTR; S: STR255);`<br>.PROC StuffHex,2 PROCEDURE STUFFHEX(THINGPTR: WORDPTR; S: STR255); CONVENIENCE ROUTINE TO STUFF HEX INTO ANY VARIABLE. BEWARE, NO RANGE-CHECKING. |
| **`STUFFHEX`** | `0x008608` | `0x012D3E` | `Util.s:421` | **Proto:** `Pascal: procedure StuffHex(thingPtr: Ptr; s: Str255);`<br>StuffHex($A866) - copy hex string into memory location Pascal: procedure StuffHex(thingPtr: Ptr; s: Str255); Each pair of hex digits in s is decoded to a byte; written to consecutive bytes starting at... |
| **`SubPt`** | `0x008992` | `0x0130C8` | `GrafAsm.s:322` | **Proto:** `PROCEDURE SubPt(src: Point; VAR dst: Point);`<br>PROCEDURE SubPt(src: Point; VAR dst: Point); { subtract src Point from dst point, restores all regs } |
| **`SUBPT`** | `0x008992` | `0x0130C8` | `GrafAsm.s:325` | **Proto:** `PROCEDURE SubPt(src: Point; VAR dst: Point);`<br>PROCEDURE SubPt(src: Point; VAR dst: Point); { subtract src Point from dst point, restores all regs } |
| **`SWAP2`** | `0x00BF68` | `0x0166D8` | `Regions.s:642`<br>`Regions.s:536` | — |
| **`SWAPLP`** | `0x00BF62` | `0x0166D2` | `Regions.s:638`<br>`Regions.s:532` | SWAP VERT AND HORIZ COORDS OF ALL INVERSION POINTS SWAPLP |
| **`TABLE_LOOKUP`** | `0x00B7E6` | `0x015F56` | `Angles.s:59`<br>`Angles.s:63` | shared entry: map angle 0..180 to tangent table index |
| **`TAN_TABLE`** | `0x00B83C` | `0x015FAC` | `Angles.s:92`<br>`Angles.s:122` | high byte approximation table for slopes at angles 64-90 degrees TAN_TABLE: tangent table - fixed-point slope values for angles 0-90 Each word = -65536 * tan(angle), indexed by angle * 2 |
| **`TESTBUF`** | `0x00C18A` | `0x0168FA` | `Regions.s:1124`<br>`Regions.s:923` | PLAY THE REGION BACK INTO SCAN BUFFER UNTIL IT GETS DOWN TO MINRECT, THEN CHECK EACH SCANLINE FOR NON-ZERO PLAYBACK. QUIT AND RETURN TRUE IF NON-ZERO FOUND BEFORE RGN GOES BEYOND MINRECT. |
| **`TEXT2`** | `0x008BF4` | `0x01332A` | `Text.s:234`<br>`Text.s:202` | — |
| **`TextFace`** | `0x008C62` | `0x013398` | `Text.s:304` | **Proto:** `PROCEDURE TextFace(face: Style);`<br>JPutPicLong .PROC TextFace,1 .DEF DrawChar,CharWidth .REF CallText,TextWidth PROCEDURE TextFace(face: Style); Called during boot. |
| **`TEXTFACE`** | `0x008C62` | `0x013398` | `Text.s:268` | **Proto:** `PROCEDURE TextFace(face: Style);`<br>JPutPicLong .PROC TextFace,1 .DEF DrawChar,CharWidth .REF CallText,TextWidth PROCEDURE TextFace(face: Style); Called during boot. |
| **`TextFont`** | `0x008C94` | `0x0133CA` | `Text.s:346` | **Proto:** `PROCEDURE TextFont(font: INTEGER);`<br>.PROC TextFont,1 .DEF TextSize .DEF TextMode .REF PortWord PROCEDURE TextFont(font: INTEGER); Called during boot. |
| **`TEXTFONT`** | `0x008C94` | `0x0133CA` | `Text.s:307` | **Proto:** `PROCEDURE TextFont(font: INTEGER);`<br>.PROC TextFont,1 .DEF TextSize .DEF TextMode .REF PortWord PROCEDURE TextFont(font: INTEGER); Called during boot. |
| **`TextMode`** | `0x008C98` | `0x0133CE` | `Text.s:354` | **Proto:** `PROCEDURE TextMode(mode: INTEGER);`<br>PROCEDURE TextMode(mode: INTEGER); |
| **`TEXTMODE`** | `0x008C98` | `0x0133CE` | `Text.s:314` | **Proto:** `PROCEDURE TextMode(mode: INTEGER);`<br>PROCEDURE TextMode(mode: INTEGER); |
| **`TEXTOP`** | `0x00DE9A` | `0x018626` | `Pictures.s:992`<br>`Pictures.s:725` | TEXTOP |
| **`TEXTOP2`** | `0x00DECE` | `0x01865A` | `Pictures.s:1024`<br>`Pictures.s:745` | — |
| **`TEXTOP2_OK`** | `0x00DF18` | `0x0186A4` | `Pictures.s:1046`<br>`Pictures.s:767` | — |
| **`TextSize`** | `0x008C9C` | `0x0133D2` | `Text.s:363` | **Proto:** `PROCEDURE TextSize(mode: INTEGER);`<br>PROCEDURE TextSize(mode: INTEGER); Called during boot. |
| **`TEXTSIZE`** | `0x008C9C` | `0x0133D2` | `Text.s:322` | **Proto:** `PROCEDURE TextSize(mode: INTEGER);`<br>PROCEDURE TextSize(mode: INTEGER); Called during boot. |
| **`TEXTSIZE_SHARE`** | `0x008C9E` | `0x0133D4` | `Text.s:365`<br>`Text.s:324` | — |
| **`TextWidth`** | `0x008CE8` | `0x01341E` | `Text.s:445` | **Proto:** `FUNCTION TEXTWIDTH(TEXTBUF: WordPtr; firstbyte,byteCount: INTEGER): INTEGER;`<br>FALL THRU INTO TEXTWIDTH .FUNC TextWidth,3 .REF StdTxMeas FUNCTION TEXTWIDTH(TEXTBUF: WordPtr; firstbyte,byteCount: INTEGER): INTEGER; Called during boot (6,985 times in 30s trace). |
| **`TEXTWIDTH`** | `0x008CE8` | `0x01341E` | `Text.s:392` | **Proto:** `FUNCTION TEXTWIDTH(TEXTBUF: WordPtr; firstbyte,byteCount: INTEGER): INTEGER;`<br>FALL THRU INTO TEXTWIDTH .FUNC TextWidth,3 .REF StdTxMeas FUNCTION TEXTWIDTH(TEXTBUF: WordPtr; firstbyte,byteCount: INTEGER): INTEGER; Called during boot (6,985 times in 30s trace). |
| **`TEXTWIDTH_DONE`** | `0x008D44` | `0x01347A` | `Text.s:489`<br>`Text.s:433` | — |
| **`TEXTWIDTH_DONE_EXIT`** | `0x008D48` | `0x01347E` | `Text.s:491`<br>`Text.s:435` | — |
| **`THIN`** | `0x008518` | `0x012C4E` | `Util.s:437`<br>`Util.s:287` | STRETCH BY TWO AND THIN OUT THE BITS. ADD EXTRA WHITE DOTS. |
| **`THINLP`** | `0x00851A` | `0x012C50` | `Util.s:439`<br>`Util.s:289` | — |
| **`THREE`** | `0x00C6FC` | `0x016E6C` | `SortPoints.s:88`<br>`SortPoints.s:72` | THREE WHILE JPTR^ > MIDPT DO BUMP JPTR TO LEFT Called during boot. |
| **`THREE4`** | `0x00D5F2` | `0x017D6E` | `Stretch.s:948`<br>`Stretch.s:762` | SHRINK TO THREE QUARTERS. |
| **`THREE4A`** | `0x00D5F8` | `0x017D74` | `Stretch.s:952`<br>`Stretch.s:766` | — |
| **`THREE4B`** | `0x00D5FC` | `0x017D78` | `Stretch.s:955`<br>`Stretch.s:769` | — |
| **`TOGLMORE`** | `0x009CF0` | `0x014460` | `DrawLine.s:767`<br>`DrawLine.s:643` | — |
| **`TOGLONE`** | `0x009CEC` | `0x01445C` | `DrawLine.s:764`<br>`DrawLine.s:640` | — |
| **`TOGLTWO`** | `0x009CEA` | `0x01445A` | `DrawLine.s:762`<br>`DrawLine.s:638` | TOGLTWO |
| **`TOPOK`** | `0x00C90C` | `0x017088` | `Bitmaps.s:69`<br>`Bitmaps.s:59` | TRIM SRCBITS |
| **`TOPORT`** | `0x00CAB6` | `0x017232` | `Bitmaps.s:299`<br>`Bitmaps.s:256` | DST IS PROBABLY TO THEPORT, SO WE USE THE CAPTURE PROC. CallBits(srcBits,srcRect,dstRect,mode,maskRgn) Called during boot. |
| **`TrimRect`** | `0x00C1BA` | `0x01692A` | `Regions.s:1177` | **Proto:** `FUNCTION TrimRect(rgn: RgnHandle; VAR dstRect: Rect): CCR TRISTATE;`<br>.FUNC TrimRect,2 .REF RgnOp FUNCTION TrimRect(rgn: RgnHandle; VAR dstRect: Rect): CCR TRISTATE; RESULT IN CONDITION CODES: < RESULT EMPTY, DSTRECT NOT MODIFIED > RESULT NON-RECT, DSTRECT NOT MODIFIED ... |
| **`TRIMRECT`** | `0x00C1BA` | `0x01692A` | `Regions.s:969` | **Proto:** `FUNCTION TrimRect(rgn: RgnHandle; VAR dstRect: Rect): CCR TRISTATE;`<br>FUNCTION TrimRect(rgn: RgnHandle; VAR dstRect: Rect): CCR TRISTATE; Result in condition codes: < result empty, dstRect not modified > result non-rect, dstRect not modified If the intersection of rgn a... |
| **`TRIMRECT_EXIT`** | `0x00C20C` | `0x01697C` | `Regions.s:1216`<br>`Regions.s:997` | RgnOp(rgn,rectRgn,BufHandle,24,sect,0,FALSE) |
| **`TRIMRT`** | `0x0092FA` | `0x013A6A` | `DrawText.s:556`<br>`DrawText.s:472` | — |
| **`TRIPLE`** | `0x00D6D6` | `0x017E52` | `Stretch.s:1105`<br>`Stretch.s:916` | RTS ;ALL DONE .BYTE $30,$33,$3C,$3F .BYTE $C0,$C3,$CC,$CF .BYTE $F0,$F3,$FC,$FF TRIPLE USING TABLE LOOKUP |
| **`TRIPLE_CONT`** | `0x00D6FA` | `0x017E76` | `Stretch.s:1124`<br>`Stretch.s:936` | TRIPLE_CONT - indexed branch table for stretch half sampling |
| **`TRIPLE_CONT_2`** | `0x00D702` | `0x017E7E` | `Stretch.s:1128`<br>`Stretch.s:945` | TRIPLE_CONT_2 -- 4-bit input -> 8-bit triplicated mid byte. 16 entries. |
| **`TRIPLE_CONT_3`** | `0x00D712` | `0x017E8E` | `Stretch.s:1133`<br>`Stretch.s:956` | TRIPLE_CONT_3 -- 3-bit input -> 8-bit triplicated lo byte. 8 entries. |
| **`TRIPLE_LOOP`** | `0x00D71A` | — | `Stretch.s:1138` | RTS ;ALL DONE |
| **`TRUE`** | `0x00C1A6` | `0x016916` | `Regions.s:1141`<br>`Regions.s:939` | TRUE |
| **`TRUE_EXIT`** | `0x00C1AA` | `0x01691A` | `Regions.s:1143`<br>`Regions.s:941` | — |
| **`TXTLOOP`** | `0x008ABE` | `0x0131F4` | `Text.s:55`<br>`Text.s:38` | — |
| **`UL1`** | `0x0094B8` | `0x013C28` | `DrawText.s:848`<br>`DrawText.s:743` | — |
| **`UL2`** | `0x0094CC` | `0x013C3C` | `DrawText.s:858`<br>`DrawText.s:753` | — |
| **`UL3`** | `0x0094EC` | `0x013C5C` | `DrawText.s:884`<br>`DrawText.s:776` | — |
| **`ULTRIM`** | `0x0094EA` | `0x013C5A` | `DrawText.s:882`<br>`DrawText.s:774` | Trim right edge of underline. (left edge trimmed by StretchBits) ULTRIM |
| **`UNION2`** | `0x00C608` | `0x016D78` | `RgnOp.s:376`<br>`RgnOp.s:331` | — |
| **`UnionRect`** | `0x00A184` | `0x0148F4` | `Rects.s:646` | **Proto:** `PROCEDURE UnionRect(* src1,src2: Rect; VAR dst: Rect *);`<br>.PROC UnionRect,3 .DEF Pt2Rect PROCEDURE UnionRect(* src1,src2: Rect; VAR dst: Rect *); { compute smallest rectangle containing both input rectangles } { works correctly even if one of the sources is ... |
| **`UNIONRECT`** | `0x00A184` | `0x0148F4` | `Rects.s:542` | **Proto:** `PROCEDURE UnionRect(* src1,src2: Rect; VAR dst: Rect *);`<br>.PROC UnionRect,3 .DEF Pt2Rect PROCEDURE UnionRect(* src1,src2: Rect; VAR dst: Rect *); { compute smallest rectangle containing both input rectangles } { works correctly even if one of the sources is ... |
| **`UNIONRECT_BOTOK`** | `0x00A1AC` | `0x01491C` | `Rects.s:664`<br>`Rects.s:560` | — |
| **`UNIONRECT_LEFTOK`** | `0x00A1A2` | `0x014912` | `Rects.s:659`<br>`Rects.s:555` | — |
| **`UNIONRECT_RIGHTOK`** | `0x00A1B8` | `0x014928` | `Rects.s:670`<br>`Rects.s:566` | — |
| **`UNIONRECT_TOPOK`** | `0x00A196` | `0x014906` | `Rects.s:653`<br>`Rects.s:549` | — |
| **`UnionRgn`** | `0x00BFE2` | `0x016752` | `Regions.s:759` | **Proto:** `PROCEDURE UnionRgn(srcRgnA,srcRgnB,dstRgn: RgnHandle);`<br>PROCEDURE UnionRgn(srcRgnA,srcRgnB,dstRgn: RgnHandle); calculate the union of two regions. Called during boot. |
| **`UNIONRGN`** | `0x00BFE2` | `0x016752` | `Regions.s:631` | **Proto:** `PROCEDURE UnionRgn(srcRgnA,srcRgnB,dstRgn: RgnHandle);`<br>PROCEDURE UnionRgn(srcRgnA,srcRgnB,dstRgn: RgnHandle); Calculate the union of two regions. |
| **`UnionScan`** | `0x00C606` | `0x016D76` | `RgnOp.s:374` | Union Scan Called during boot. |
| **`UNIONSCAN`** | `0x00C606` | `0x016D76` | `RgnOp.s:329` | UnionScan |
| **`UNIXOR`** | `0x00C076` | `0x0167E6` | `Regions.s:908`<br>`Regions.s:750` | UNIXOR Called during boot. |
| **`UnpackBits`** | `0x00D01C` | `0x017798` | `Bitmaps.s:1128` | **Proto:** `PROCEDURE UnpackBits(VAR srcPtr,dstPtr: Ptr; dstBytes: INTEGER);`<br>PROCEDURE UnpackBits(VAR srcPtr,dstPtr: Ptr; dstBytes: INTEGER); Unpacks one scanline of data, as compressed by PackBits. Returns updated srcPtr and dstPtr. Equates for parameters are the same as Pack... |
| **`UNPACKBITS`** | `0x00D01C` | `0x017798` | `Bitmaps.s:955` | **Proto:** `PROCEDURE UnpackBits(VAR srcPtr, dstPtr: Ptr; dstBytes: INTEGER);`<br>PROCEDURE UnpackBits(VAR srcPtr, dstPtr: Ptr; dstBytes: INTEGER); Unpacks one scanline of data, as compressed by PackBits. Returns updated srcPtr and dstPtr. Equates for parameters are the same as Pac... |
| **`UNPACKBITS_CONT`** | `0x00D032` | `0x0177AE` | `Bitmaps.s:1145`<br>`Bitmaps.s:968` | UNPACKBITS_CONT |
| **`UNPACKBITS_DONE`** | `0x00D052` | `0x0177CE` | `Bitmaps.s:1168`<br>`Bitmaps.s:990` | UNPACKBITS_DONE |
| **`UNPACKBITS_LOOP`** | `0x00D034` | `0x0177B0` | `Bitmaps.s:1147`<br>`Bitmaps.s:970` | — |
| **`UNPACKBITS_LOOP_2`** | `0x00D04A` | `0x0177C6` | `Bitmaps.s:1159`<br>`Bitmaps.s:982` | — |
| **`UNPACKBITS_SKIP`** | `0x00D03A` | `0x0177B6` | `Bitmaps.s:1150`<br>`Bitmaps.s:973` | — |
| **`UP`** | `0x00C30E` | `0x016A7E` | `SeekRgn.s:77`<br>`SeekRgn.s:69` | TO MOVE UPWARDS, JUST RESET TO START AND MOVE DOWN. |
| **`UPDATE`** | `0x0096DC` | `0x013E4C` | `Lines.s:91`<br>`Lines.s:91` | — |
| **`UPDATEA`** | `0x00C4C8` | `0x016C38` | `RgnOp.s:175`<br>`RgnOp.s:154` | UPDATEA Called during boot (30,111 times in 30s trace). |
| **`UPDATEB`** | `0x00C4EC` | `0x016C5C` | `RgnOp.s:195`<br>`RgnOp.s:172` | — |
| **`UPSIDE`** | `0x00A332` | `0x014AA2` | `BitBlt.s:191`<br>`BitBlt.s:126` | SOURCE WILL BE USED, SO SET UP VERT AND HORIZ DIRECTIONS SUCH THAT SRC WON'T GET CLOBBERED TILL AFTER IT HAS BEEN USED DO UPSIDE DOWN TO AVOID CLOBBERING SRC |
| **`USEPAT`** | `0x0085B2` | `0x012CE8` | `Util.s:535`<br>`Util.s:371` | — |
| **`USERGN`** | `0x00E036` | `0x0187C2` | `Pictures.s:1195`<br>`Pictures.s:901` | USERGN |
| **`USERGN_CONT`** | `0x00E044` | `0x0187D0` | `Pictures.s:1199`<br>`Pictures.s:905` | — |
| **`USESRC`** | `0x00A934` | `0x0150A4` | `RgnBlt.s:435`<br>`RgnBlt.s:299` | SET UP (VERT * 4) MOD 64 AS PATTERN SELECTOR SRC WILL BE USED. CHECK FOR OVERLAP AND CHOOSE DIRECTION SO THAT SRC WONT GET CLOBBERED BEFORE IT IS USED. Called during boot. |
| **`USESTD`** | `0x00B01E` | `0x01578E` | `Arcs.s:157`<br>`Arcs.s:150` | — |
| **`VCLIP`** | `0x0090E2` | `0x013852` | `DrawText.s:283`<br>`DrawText.s:233` | — |
| **`VCLIP_NO`** | `0x0090F2` | `0x013862` | `DrawText.s:288`<br>`DrawText.s:238` | — |
| **`VCLR`** | `0x009D40` | `0x0144B0` | `DrawLine.s:828`<br>`DrawLine.s:700` | ELSE WHITE |
| **`VLINE`** | `0x009D24` | `0x014494` | `DrawLine.s:816`<br>`DrawLine.s:689` | DRAW A VERTICAL LINE. Called during boot. |
| **`VOK2`** | `0x0098B4` | `0x014024` | `DrawLine.s:109`<br>`DrawLine.s:72` | GET CLIPRGN AND VISRGN HANDLES AND DE-REFERENCE THEM SET UP LINERECT, THE RECTANGLE BOUNDING THE LINE AND PEN |
| **`VOK2_NO`** | `0x0098BA` | `0x01402A` | `DrawLine.s:113`<br>`DrawLine.s:76` | — |
| **`VSAME`** | `0x00C820` | `0x017012` | `PackRgn.s:136`<br>`PackRgn.s:133` | — |
| **`VSET`** | `0x009D58` | `0x0144C8` | `DrawLine.s:849`<br>`DrawLine.s:719` | VSET Called during boot. |
| **`VSWAP`** | `0x0099A4` | `0x014114` | `DrawLine.s:269`<br>`DrawLine.s:210` | THE LINE IS SLANTED. SORT VERTICALLY AND DRAW TOP TO BOTTOM AS HORIZONTAL SLABS. |
| **`VTOGL`** | `0x009D4C` | `0x0144BC` | `DrawLine.s:838`<br>`DrawLine.s:709` | VTOGL |
| **`WHILE1`** | `0x00B76C` | `0x015EDC` | `DrawArc.s:1219`<br>`DrawArc.s:955` | — |
| **`WHILE2`** | `0x00B77E` | `0x015EEE` | `DrawArc.s:1236`<br>`DrawArc.s:970` | — |
| **`WHITE1`** | `0x00D87E` | `0x017FFA` | `Stretch.s:1347`<br>`Stretch.s:1163` | — |
| **`WHITE16`** | `0x00D834` | `0x017FB0` | `Stretch.s:1276`<br>`Stretch.s:1106` | — |
| **`WHITE1_CONT`** | `0x00D890` | `0x01800C` | `Stretch.s:1362`<br>`Stretch.s:1178` | WHITE1_CONT |
| **`WHITE2`** | `0x00D8C2` | `0x01803E` | `Stretch.s:1406`<br>`Stretch.s:1215` | — |
| **`WHITE2_ERR`** | `0x00D8CE` | `0x01804A` | `Stretch.s:1413`<br>`Stretch.s:1222` | — |
| **`WHITEOK`** | `0x00D8BE` | `0x01803A` | `Stretch.s:1403`<br>`Stretch.s:1212` | WHITEOK |
| **`WIDE1`** | `0x009390` | `0x013B00` | `DrawText.s:673`<br>`DrawText.s:578` | — |
| **`WORD1`** | `0x0093D4` | `0x013B44` | `DrawText.s:715`<br>`DrawText.s:617` | Optimize if dst fits in one word. (70% of normal characters do) Called during boot. |
| **`WORD1B`** | `0x0093D6` | `0x013B46` | `DrawText.s:717`<br>`DrawText.s:619` | — |
| **`WORD8`** | `0x00A5A2` | `0x014D12` | `BitBlt.s:654`<br>`BitBlt.s:545` | OPTIMIZE MODE 8 OR 12 IF DST FITS IN ONE WORD (VERT LINES ETC) Called during boot. |
| **`WORD8A`** | `0x00A5A8` | `0x014D18` | `BitBlt.s:658`<br>`BitBlt.s:549` | — |
| **`WORD8A_CONT`** | `0x00A5C6` | `0x014D36` | `BitBlt.s:676`<br>`BitBlt.s:566` | MODE 8 OR 12: PATTERN --> DST (FILLING AREAS, DRAWING LINES) Called during boot. |
| **`WORD8A_CONT_2`** | `0x00A5E2` | `0x014D52` | `BitBlt.s:686`<br>`BitBlt.s:576` | — |
| **`WORD8A_CONT_3`** | `0x00A5E4` | `0x014D54` | `BitBlt.s:688`<br>`BitBlt.s:578` | — |
| **`WORD8A_CONT_4`** | `0x00A5E6` | `0x014D56` | `BitBlt.s:696`<br>`BitBlt.s:585` | WORD8A_CONT_4 Called during boot (1,444 times in 30s trace). |
| **`XCLIP2`** | `0x00DCE4` | `0x018460` | `Pictures.s:722`<br>`Pictures.s:525` | — |
| **`XOR31`** | `0x00A6D8` | — | `BitBlt.s:883` | XOR31 Called during boot. |
| **`XOR31_CONT`** | `0x00A6FA` | `0x014E6A` | `BitBlt.s:908`<br>`BitBlt.s:773` | MODE 11 OR 15: PATTERN BIC DST --> DST Called during boot. |
| **`XOR32`** | `0x00A6B6` | `0x014E26` | `BitBlt.s:859`<br>`BitBlt.s:732` | XOR32 Called during boot. |
| **`XORBIG`** | `0x00A69E` | `0x014E0E` | `BitBlt.s:836`<br>`BitBlt.s:712` | Call XORbig with wordcount in D2 (clobbered) |
| **`XORBIG_DONE`** | `0x00A6B0` | `0x014E20` | `BitBlt.s:850`<br>`BitBlt.s:725` | XORBIG_DONE |
| **`XORBIG_LOOP`** | `0x00A6A6` | `0x014E16` | `BitBlt.s:840`<br>`BitBlt.s:716` | — |
| **`XorRgn`** | `0x00BFEA` | `0x01675A` | `Regions.s:779` | **Proto:** `PROCEDURE XorRgn(srcRgnA,srcRgnB,dstRgn: RgnHandle);`<br>PROCEDURE XorRgn(srcRgnA,srcRgnB,dstRgn: RgnHandle); calculate the exclusive or of two regions Called during boot. |
| **`XORRGN`** | `0x00BFEA` | `0x01675A` | `Regions.s:647` | **Proto:** `PROCEDURE XorRgn(srcRgnA,srcRgnB,dstRgn: RgnHandle);`<br>PROCEDURE XorRgn(srcRgnA,srcRgnB,dstRgn: RgnHandle); Calculate the exclusive or of two regions. |
| **`XORRGN_COPY`** | `0x00C018` | `0x016788` | `Regions.s:832`<br>`Regions.s:684` | ARE THE TWO INPUT REGIONS THE SAME ? THE TWO REGIONS ARE THE SAME. IF SectScan OR UNION THEN COPY RGNA INTO DSTRGN, ELSE ZERO OUT DSTRGN. |
| **`XORRGN_NOTSAME`** | `0x00C02A` | `0x01679A` | `Regions.s:852`<br>`Regions.s:700` | IF OP = DIFF AND RGNB = EMPTY, COPY RGNA INTO DST Called during boot (10,210 times in 30s trace). |
| **`XORRGN_ZERO`** | `0x00C022` | `0x016792` | `Regions.s:843`<br>`Regions.s:693` | XORRGN_ZERO Called during boot. |
| **`XorScan`** | `0x00C692` | `0x016E02` | `RgnOp.s:548` | XorScan -- xORSCAN(PTRA,SCANA,TEMPSCAN). |
| **`XORSCAN`** | `0x00C692` | `0x016E02` | `RgnOp.s:463` | **Proto:** `LOCAL PROCEDURE XorScan(srcA, srcB, dstC: ScanPtr);`<br>LOCAL PROCEDURE XorScan(srcA, srcB, dstC: ScanPtr); Form the exclusive-or of two inversion scans. INPUTS:  A0 SrcA, A1 SrcB, A2 DstC CLOBBERS D0-D1, A0-A2 |
| **`XorSlab`** | `0x008642` | `0x012D78` | `Util.s:653` | **Proto:** `LOCAL PROCEDURE XorSlab(bufAddr: Ptr; left,right: INTEGER);`<br>.PROC XorSlab .REF MaskTab LOCAL PROCEDURE XorSlab(bufAddr: Ptr; left,right: INTEGER); Enter with: A0: bufAddr D3: left coord D4: right coord Clobbers: A0,D0,D1,D3,D4,D5,D6 GET LEFTMASK AND RIGHTMASK ... |
| **`XORSLAB`** | `0x008642` | `0x012D78` | `Util.s:456` | XorSlab - XOR a horizontal slab of pixels into A0's row Inputs: A0 = bufAddr, D3 = left pixel, D4 = right pixel. Computes left/right word-boundary masks via MASKTAB then XORs the combined mask into th... |
| **`XORSLAB_ENDWORD`** | `0x008682` | `0x012DB8` | `Util.s:705`<br>`Util.s:490` | — |
| **`XORSLAB_INVLONG`** | `0x008678` | `0x012DAE` | `Util.s:698`<br>`Util.s:483` | XORSLAB_INVLONG Called during boot. |
| **`XORSLAB_INVLONG_CONT`** | `0x00867A` | `0x012DB0` | `Util.s:700`<br>`Util.s:485` | XORSLAB_INVLONG Called during boot. |
| **`XORSLAB_NOTIN1`** | `0x008674` | `0x012DAA` | `Util.s:689`<br>`Util.s:480` | CALC LEFTWORD, BUFPTR, WORDCOUNT LEFT AND RIGHT ARE ALL IN ONE WORD NOT ALL IN ONE WORD. DO LEFT, MIDDLE IF ANY, THEN RIGHT Called during boot. |
| **`XRGNBLT`** | `0x00D09A` | `0x017816` | `Stretch.s:103`<br>`Stretch.s:61` | Calc Numer and Denom based on dstRect and srcRect. If Numer = Denom then just call RgnBlt. XRGNBLT -- 1:1 size: just call RgnBlt directly |
| **`YESBUMP`** | `0x00B428` | `0x015B98` | `DrawArc.s:687`<br>`DrawArc.s:503` | BUMP OVAL STATE RECORDS UNLESS VERT IS BETWEEN SKIPTOP AND SKIPBOT |
| **`YESFLAG`** | `0x00B0D0` | `0x015840` | `DrawArc.s:196`<br>`DrawArc.s:108` | CHECK FOR BLACK OR WHITE PATTERN |
| **`YESFLAG_CONT`** | `0x00B0E8` | `0x015858` | `DrawArc.s:213`<br>`DrawArc.s:130` | fast case: map mode into black,xor,white, or do-nothing YESFLAG_CONT - indexed branch table for DrawArc region scan modes |
| **`YESFLAG_NO`** | `0x00B0F0` | `0x015860` | `DrawArc.s:219`<br>`DrawArc.s:138` | FLAGOK Called during boot. |
| **`ZERO`** | `0x00B96C` | `0x0160DC` | `Angles.s:193`<br>`Angles.s:233` | — |

---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

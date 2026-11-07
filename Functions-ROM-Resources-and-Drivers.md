# ROM Resources & Drivers Function & Routine Directory

This catalog lists all **2,777** routines, functions, exception vectors, and labels belonging to the **ROM Resources & Drivers** subsystem across the Macintosh Plus (128 KB) and Macintosh SE (256 KB) ROMs.

| Symbol / Routine | Mac Plus Offset | Mac SE Offset | Source File : Line | Description / Prototype |
| :--- | :--- | :--- | :--- | :--- |
| **`_bbmc_0_`** | — | `0x01D924` | `res_bbmc.s:20` | Bbmc 0 resource body. |
| **`_CDEF_0_`** | — | `0x037A30` | `res_cdef_0.s:107` | Entry point and Apple's standard defproc header: a branch around it, flags, resource type, resource ID and version number. |
| **`_CDEF_1_`** | — | `0x037D5A` | `res_cdef_1.s:103` | Entry point and Apple's standard defproc header: a branch around it, flags, resource type, resource ID and version number. |
| **`_CURS_1_`** | `0x01F1EC` | `0x039C94` | `res_curs.s:60`<br>`res_curs.s:51` | end of resource : 'CURS' 3 resource : 'CURS' 1 IBeamCursor (I-beam text insertion cursor) Standard cursor ID 1: iBeamCursor Vertical bar with serifs top/bottom for text editing Mask is empty (transpar... |
| **`_CURS_2_`** | `0x01F154` | `0x039D2C` | `res_curs.s:12`<br>`res_curs.s:115` | resource : 'CURS' 2 CrossCursor (cross-hair for drawing tools) Standard cursor ID 2: crossCursor 11-pixel vertical + horizontal cross-hair Mask is empty (transparent background) Hotspot at (5,5) = cen... |
| **`_CURS_3_`** | `0x01F1A0` | `0x039CE0` | `res_curs.s:36`<br>`res_curs.s:83` | end of resource : 'CURS' 2 resource : 'CURS' 3 PlusCursor (3D plus sign for precision positioning) Standard cursor ID 3: plusCursor 3D beveled plus sign used for cell selection Mask outlines entire pl... |
| **`_CURS_4_`** | `0x01F238` | `0x039C48` | `res_curs.s:84`<br>`res_curs.s:19` | end of resource : 'CURS' 1 resource : 'CURS' 4 WatchCursor (wristwatch for busy/wait state) Standard cursor ID 4: watchCursor Wristwatch icon shown during lengthy operations Mask is filled rectangle a... |
| **`_DRVR_10_.ATP`** | `0x019DA0` | `0x0324AA` | `res_drvr_atp.s:61`<br>`res_drvr_atp.s:129` | MacSEROM.lst name of the driver resource |
| **`_DRVR_2_.Print`** | `0x01784C` | — | `res_drvr_print.s:11` | — |
| **`_DRVR_3_.Sound`** | `0x0179C0` | `0x036C90` | `res_drvr_sound.s:147`<br>`res_drvr_sound.s:129` | Driver header (IM II-188): flags, delay, event mask, menu, the offsets of the five routines and the driver name. |
| **`_DRVR_40_.XPP`** | — | `0x037028` | `res_drvr_xpp.s:334` | DRVR header (Inside Macintosh II-188): flags, delay, event mask, menu, the offsets of the five entry points, the name and the version. |
| **`_DRVR_4_.Sony`** | `0x017D30` | `0x034680` | `res_drvr_sony.s:75`<br>`res_drvr_sony_fdhd.s:200` | DRVR header (Inside Macintosh II-188): flags, delay, event mask, menu, the offsets of the five entry points from the start of the header, and the driver name. |
| **`_DRVR_9_.MPP`** | `0x01A6FA` | `0x03312A` | `res_drvr_mpp.s:66`<br>`res_drvr_mpp.s:144` | MacSEROM.lst name of the driver resource |
| **`_FONT_0_Chicago`** | `0x01F284` | `0x03AB62` | `res_font_chicago.s:19`<br>`res_font_chicago.s:923` | resource : 'FONT' 0 'Chicago' FONT resource ID 0 = 128*0 + 0 = font #0 (Chicago), size 0 This is the FONT name resource (font family ID 0 = Chicago) Contains no glyph data, just marks the font family ... |
| **`_FONT_12_`** | `0x01F28C` | `0x039D78` | `res_font_chicago.s:40`<br>`res_font_chicago.s:16` | resource : 'FONT' 12 - System font (Chicago 12pt) FontRec header (26 bytes): $9001 = fontType (proportional, has height table) $0000 = firstChar (NUL) $00D8 = lastChar (216 = number of glyphs - 1) $00... |
| **`_FONT_393_`** | — | `0x03AB6A` | `res_font_geneva.s:13` | FONT 393 resource body. |
| **`_FONT_396_`** | — | `0x03B594` | `res_font_geneva.s:677` | FONT 396 resource body. |
| **`_FONT_521_`** | — | `0x03C204` | `res_font_monaco.s:12` | FONT 521 resource body. |
| **`_KCHR_0_`** | — | `0x038254` | `res_kchr.s:15` | KCHR 0 resource body. |
| **`_KMAP_0_`** | — | `0x0387C6` | `res_kmap.s:13` | KMAP 0 resource body. |
| **`_MBDF_0_`** | — | `0x038854` | `res_mbdf.s:140` | _MBDF_0_ -- entry point and standard defproc header |
| **`_MDEF_0_`** | `0x01BF40` | `0x038E02` | `res_mdef.s:67`<br>`res_mdef.s:89` | _MDEF_0_ -- entry point and standard defproc header |
| **`_PACK_4_`** | `0x01DF94` | `0x01C188` | `res_pack_4.s:69`<br>`res_pack_4.s:71` | Package header: branch to the entry, flags word, 'PACK', ID, version. |
| **`_PACK_5_`** | `0x01CF2E` | `0x01B122` | `res_pack_5.s:70`<br>`res_pack_5.s:71` | Package header: branch to the entry, flags word, 'PACK', ID, version. Called by: the _Pack5 trap (_Elems68K, $A9EC); recursively by XPWRY (ELEMS_XPWRY), Compound (ELEMS_CMPTOFIN, ELEMS_CMPRESULT) and ... |
| **`_PACK_7_`** | `0x01C9E0` | `0x01D348` | `res_pack_7.s:62`<br>`res_pack_7.s:64` | Package header: branch to the entry, flags word, 'PACK', ID, version. |
| **`_SERD_0_`** | `0x01B6D0` | `0x031BAE` | `res_serd.s:161`<br>`res_serd.s:185` | shadow registers, in the order SERD_WRITEREGS uses them (SV_WR4 on): resource header: pseudo heap-block header of the ROM resource (as the Memory Manager's block header, so that a handle to the ROM re... |
| **`_tcsl_0_`** | — | `0x01D896` | `res_tcsl.s:55` | _tcsl_0_ -- two words of unknown meaning (as an instruction: ORI.B #1,D0), then the code |
| **`_WDEF_0_`** | `0x01C346` | `0x0395AC` | `res_wdef.s:59`<br>`res_wdef_0.s:77` | _WDEF_0_ -- entry point and standard defproc header |
| **`_WDEF_1_`** | — | `0x039212` | `res_wdef_1.s:87` | _WDEF_1_ -- entry point and standard defproc header |
| **`ADDRESPONSE`** | `0x01A08C` | `0x03284C` | `res_drvr_atp.s:502`<br>`res_drvr_atp.s:654` | AddResponse (csCode 251): send one more response packet: rspNum (0-7), reqLength/reqPointer = data, userData, atpFlags (EOM), transID, addrBlock.  For an exactly-once transaction the packet is also en... |
| **`ADDRESPONSE_BDS`** | `0x01A0FC` | `0x0328BC` | `res_drvr_atp.s:544`<br>`res_drvr_atp.s:696` | — |
| **`ADDRESPONSE_EXIT`** | `0x01A11C` | `0x0328DC` | `res_drvr_atp.s:557`<br>`res_drvr_atp.s:710` | ADDRESPONSE_EXIT (JATPEx2 in Apple's source): -> ATP_DONE |
| **`ADDRESPONSE_NOERR`** | `0x01A118` | `0x0328D8` | `res_drvr_atp.s:553`<br>`res_drvr_atp.s:705` | — |
| **`ADDRESPONSE_RESTSR`** | `0x01A11A` | `0x0328DA` | `res_drvr_atp.s:555`<br>`res_drvr_atp.s:707` | — |
| **`ATP_APPENDREQ`** | — | `0x0326E4` | `res_drvr_atp.s:446` | ATP_APPENDREQ: append call A0 at the end of the queue whose head is at A1 (interrupts off), then ATP_DETACHREQ.  Also called (BSR) by NSENDREQUEST: it returns to its caller with D0 = 0 after ATP_DETAC... |
| **`ATP_APPENDREQ_LINK`** | — | `0x0326F2` | `res_drvr_atp.s:455` | link the call in at the end (its qLink is cleared below) |
| **`ATP_APPENDREQ_LOOP`** | — | `0x0326EA` | `res_drvr_atp.s:449` | — |
| **`ATP_BUILDTREQ`** | `0x01A23E` | `0x032A6E` | `res_drvr_atp.s:710`<br>`res_drvr_atp.s:924` | ATP_BUILDTREQ: TReq header in CB A3 from SendRequest A0 (D2 = word index of its request slot): control $40 + atpFlags without EOM, bitmap = currBitmap, slot TID; D3 = addrBlock.  Falls into ATP_SETDAT... |
| **`ATP_CHECKSUM`** | `0x01A6AC` | `0x0330D8` | `res_drvr_atp.s:1340`<br>`res_drvr_atp.s:1868` | ATP_CHECKSUM: DDP checksum over D2 bytes at (A0)+: D3 = (D3 + byte) rotated left one bit, per byte.  D0 must have bits 15-8 clear. |
| **`ATP_CHKPKT`** | `0x01A64E` | `0x033070` | `res_drvr_atp.s:1284`<br>`res_drvr_atp.s:1808` | accepted: request size, dequeue, complete ATP_CHKPKT: after ReadRest (Z = no error): verify the DDP checksum of a long-header packet (if nonzero) and return D1 = source address (net.W, node.B, socket.... |
| **`ATP_CHKPKT_ADDR`** | `0x01A6A4` | `0x0330D0` | `res_drvr_atp.s:1328`<br>`res_drvr_atp.s:1856` | source address from the long header |
| **`ATP_CHKPKT_COMPARE`** | `0x01A690` | `0x0330B2` | `res_drvr_atp.s:1319`<br>`res_drvr_atp.s:1843` | — |
| **`ATP_CHKPKT_EXIT`** | `0x01A6AA` | `0x0330D6` | `res_drvr_atp.s:1332`<br>`res_drvr_atp.s:1860` | — |
| **`ATP_CHKPKT_RESTORE`** | `0x01A692` | `0x0330B4` | `res_drvr_atp.s:1321`<br>`res_drvr_atp.s:1845` | — |
| **`ATP_CHKPKT_SHORT`** | — | `0x0330CC` | `res_drvr_atp.s:1854` | source address from the long header |
| **`ATP_CHKPKT_ZERO`** | `0x01A68A` | `0x0330AC` | `res_drvr_atp.s:1315`<br>`res_drvr_atp.s:1839` | long header: checksum checksum the header from ddpDstNet to ddpSrcSkt, the type byte the ATP header the data (D1 bytes ending at A3) a computed 0 is sent as $FFFF |
| **`ATP_CLOSESOCKETS`** | `0x019ED8` | `0x032630` | `res_drvr_atp.s:233`<br>`res_drvr_atp.s:333` | ATP_CLOSESOCKETS: CloseSkt (via .MPP) every nonzero socket of a table. A0 = socket table, D2 = entries, A3 = claimed CB (ioResult cleared first, so the caller's wait loop ends when nothing was closed)... |
| **`ATP_CLOSESOCKETS_LOOP`** | `0x019EDC` | `0x032634` | `res_drvr_atp.s:235`<br>`res_drvr_atp.s:335` | — |
| **`ATP_CMPADDR`** | `0x01A076` | `0x032836` | `res_drvr_atp.s:480`<br>`res_drvr_atp.s:633` | ATP_CMPADDR ATP_CMPADDR: compare internet address D3 (net.W, node.B, socket.B) with the one at (A1) -> EQ if equal; node and socket must match, a network number of 0 on either side matches any network... |
| **`ATP_CMPADDR_EXIT`** | `0x01A08A` | `0x03284A` | `res_drvr_atp.s:490`<br>`res_drvr_atp.s:643` | — |
| **`ATP_COMPLETE`** | `0x01A31A` | `0x032C06` | `res_drvr_atp.s:825`<br>`res_drvr_atp.s:1155` | ATP_COMPLETE: complete a call that ATP_DETACHREQ took off the queue: ioResult = D0, then call its ioCompletion routine (A0 = parameter block, D0 = result), if any.  Preserves D1-D3/A0-A3. Called by: A... |
| **`ATP_COMPLETE_EXIT`** | `0x01A32E` | `0x032C1A` | `res_drvr_atp.s:833`<br>`res_drvr_atp.s:1163` | — |
| **`ATP_DETACHREQ`** | `0x019F8E` | `0x0326F4` | `res_drvr_atp.s:350`<br>`res_drvr_atp.s:462` | ATP_DETACHREQ: take the current call (A0) off the .ATP I/O queue without completing it, then start the next queued call, if any (as a new E_ATP_Control).  Entered with the caller's SR on the stack. |
| **`ATP_DETACHREQ_EXIT`** | `0x019FBA` | `0x03272C` | `res_drvr_atp.s:367`<br>`res_drvr_atp.s:483` | start the next queued call no other call queued |
| **`ATP_DETACHREQ_UNLINK`** | `0x019FA2` | `0x032708` | `res_drvr_atp.s:356`<br>`res_drvr_atp.s:468` | — |
| **`ATP_DONE`** | `0x019F66` | `0x0326CC` | `res_drvr_atp.s:310`<br>`res_drvr_atp.s:420` | ATP_DONE - A1 = .ATP DCE, then IODone with D0 |
| **`ATP_DONE_A1`** | `0x019F6A` | `0x0326D0` | `res_drvr_atp.s:312`<br>`res_drvr_atp.s:422` | — |
| **`ATP_DONE_NOERR`** | `0x019F64` | `0x0326CA` | `res_drvr_atp.s:307`<br>`res_drvr_atp.s:414` | ATP_DONE_NOERR / ATP_DONE / ATP_DONE_A1: common exits, IODone with D0 (noErr; A1 = .ATP DCE from ATPVars; A1 already loaded) |
| **`ATP_FINDRSPCB`** | `0x01A054` | `0x032814` | `res_drvr_atp.s:455`<br>`res_drvr_atp.s:609` | ATP_FINDRSPCB ATP_FINDRSPCB: find the RspCB of a transaction.  D1.B = responding socket, D3 = requester address, D0 = TID -> EQ and A1 = RspCB if found (NE if not).  Uses D2. |
| **`ATP_FINDRSPCB_EXIT`** | `0x01A074` | `0x032834` | `res_drvr_atp.s:470`<br>`res_drvr_atp.s:624` | — |
| **`ATP_FINDRSPCB_LOOP`** | `0x01A05A` | `0x03281A` | `res_drvr_atp.s:458`<br>`res_drvr_atp.s:612` | — |
| **`ATP_FINDRSPCB_NEXT`** | `0x01A06C` | `0x03282C` | `res_drvr_atp.s:467`<br>`res_drvr_atp.s:621` | — |
| **`ATP_FIRSTNSREQ`** | — | `0x032A9C` | `res_drvr_atp.s:948` | ATP_FIRSTNSREQ: A0 = first NSendRequest queued on responding socket slot D2 (A2 = ATPVars), D0 = A0; EQ if none. Called by ATP_VBLTASK (twice). |
| **`ATP_FREECB`** | `0x01A6EC` | `0x03311C` | `res_drvr_atp.s:1388`<br>`res_drvr_atp.s:1918` | ATP_FREECB: release CB A3 Called by: OPENATPSKT, CLOSEATPSKT, SENDRESPONSE, ADDRESPONSE, SENDREQUEST, ATP_VBLTASK, RELTCB_FOUND, ATP_LISTENER |
| **`ATP_GETCB`** | `0x01A6B8` | `0x0330E4` | `res_drvr_atp.s:1356`<br>`res_drvr_atp.s:1887` | ATP_GETCB: claim a free CB for a call to .MPP -> A3 = CB, D0 = noErr, or D0 = noDataArea (all three busy).  A CB is free when its ioRefNum is 0; claiming it stores the .MPP refNum there. Called by: E_... |
| **`ATP_GETCB_CLAIM`** | `0x01A6E4` | `0x033114` | `res_drvr_atp.s:1377`<br>`res_drvr_atp.s:1908` | second CB third CB ATP_GETCB_CLAIM: mark CB A3 as in use |
| **`ATP_GETCB_EXIT`** | — | `0x03310C` | `res_drvr_atp.s:1902` | — |
| **`ATP_GETCB_LOOP`** | — | `0x0330FA` | `res_drvr_atp.s:1895` | — |
| **`ATP_LISTENER`** | `0x01A418` | `0x032D38` | `res_drvr_atp.s:987`<br>`res_drvr_atp.s:1326` | free the RspCB, complete its SendResponse ATP_LISTENER: DDP socket listener of all ATP sockets (MPP socket listener conventions: A2 = MPP variables, A3 -> next free RHA byte, A4 = ReadPacket/ReadRest ... |
| **`ATP_LISTENER_ALLRCVD`** | `0x01A4F2` | `0x032EF0` | `res_drvr_atp.s:1087`<br>`res_drvr_atp.s:1602` | send the TReq again all responses received? then the transaction is complete |
| **`ATP_LISTENER_CHKERR`** | `0x01A41E` | — | `res_drvr_atp.s:991` | — |
| **`ATP_LISTENER_CLOSE`** | `0x01A524` | `0x032F3C` | `res_drvr_atp.s:1104`<br>`res_drvr_atp.s:1634` | free the slot, send TRel if exactly-once, close the socket, complete exactly-once: send TRel to the responder |
| **`ATP_LISTENER_COMMON`** | — | `0x032DB8` | `res_drvr_atp.s:1428` | ATP_LISTENER_COMMON: check the DDP type (3 = ATP), read 3 header bytes over the DDP type byte (atpControl, bitmap/sequence, TID high byte; the TID and user bytes come out word aligned) and dispatch on... |
| **`ATP_LISTENER_COMPLETE`** | — | `0x032F4C` | `res_drvr_atp.s:1639` | — |
| **`ATP_LISTENER_DELIVER`** | `0x01A60A` | `0x03302A` | `res_drvr_atp.s:1245`<br>`res_drvr_atp.s:1767` | ATP_LISTENER_DELIVER: complete the first GetRequest queued on the socket with the request: userData, bitMap, transID, atpFlags = atpControl, addrBlock = requester, reqLength = request size; dropped if... |
| **`ATP_LISTENER_DISCARD`** | `0x01A3A8` | `0x032DF2` | `res_drvr_atp.s:908`<br>`res_drvr_atp.s:1458` | ATP_LISTENER_DISCARD: drop the packet: ReadRest with a zero buffer (it returns to MPP), discarding the saved RHA pointer |
| **`ATP_LISTENER_DROP`** | `0x01A3E2` | — | `res_drvr_atp.s:947` | ATP_LISTENER_DROP - short-branch path to ATP_LISTENER_DISCARD |
| **`ATP_LISTENER_EOMLOOP`** | `0x01A4C2` | `0x032EC0` | `res_drvr_atp.s:1066`<br>`res_drvr_atp.s:1582` | and carry the TID of the request store bdsDataSz and bdsUserData of the response clear the bit of this response in currBitmap EOM: no responses beyond this one |
| **`ATP_LISTENER_EXIT`** | `0x01A3E0` | `0x032D36` | `res_drvr_atp.s:940`<br>`res_drvr_atp.s:1315` | — |
| **`ATP_LISTENER_FILTLOOP`** | `0x01A636` | `0x033058` | `res_drvr_atp.s:1264`<br>`res_drvr_atp.s:1787` | — |
| **`ATP_LISTENER_FILTNEXT`** | `0x01A640` | `0x033062` | `res_drvr_atp.s:1269`<br>`res_drvr_atp.s:1792` | — |
| **`ATP_LISTENER_FILTNODE`** | `0x01A634` | `0x033056` | `res_drvr_atp.s:1262`<br>`res_drvr_atp.s:1785` | return the request fields check the requester against the addrBlock filter of the socket |
| **`ATP_LISTENER_FREESLOT`** | — | `0x032F1A` | `res_drvr_atp.s:1621` | — |
| **`ATP_LISTENER_GOTREQ`** | `0x01A544` | `0x032F64` | `res_drvr_atp.s:1132`<br>`res_drvr_atp.s:1664` | ATP_LISTENER_GOTREQ ATP_LISTENER_GOTREQ: request read (A3 -> end of the ATP header in the RHA, D1 = requester address, D2 = socket slot * 4).  Exactly-once: a known transaction (RspCB present) is a re... |
| **`ATP_LISTENER_GOTRSP`** | — | `0x032E6A` | `res_drvr_atp.s:1543` | ATP_LISTENER_GOTRSP: a response read for request A0 (D1 = responder, D3 = bytes not filled, A3 -> end of the ATP header in the RHA, D2 = slot * 4: request slot or responding-socket slot).  It must com... |
| **`ATP_LISTENER_NEWRSPCB`** | `0x01A584` | `0x032FA4` | `res_drvr_atp.s:1165`<br>`res_drvr_atp.s:1692` | no RspCB free: ignore the request (the requester retries) ATP_LISTENER_NEWRSPCB fill in the free RspCB at A1 |
| **`ATP_LISTENER_NSFOUND`** | — | `0x032E00` | `res_drvr_atp.s:1466` | the NSendRequest A5 of the TID: read the last 2 header bytes |
| **`ATP_LISTENER_NSLOOP`** | — | `0x032DE6` | `res_drvr_atp.s:1448` | function code 10 = TResp: an NSendRequest of this socket with the TID? |
| **`ATP_LISTENER_REQDONE`** | — | `0x032F04` | `res_drvr_atp.s:1614` | no CB free: set the bit of this response again, so that the transaction ends when the response comes again (the TReq retransmission asks for it; numOfResps then counts it twice) free the slot (SendReq... |
| **`ATP_LISTENER_RESEND`** | `0x01A594` | `0x032FB4` | `res_drvr_atp.s:1183`<br>`res_drvr_atp.s:1709` | ATP_LISTENER_RESEND: retransmitted exactly-once request - resend the response packets it asks for (atpBitmap) from the BDS of the pending SendResponse (entries with bdsDataSz <> 0); A1 = RspCB |
| **`ATP_LISTENER_RESENDBDS`** | `0x01A5EA` | `0x03300A` | `res_drvr_atp.s:1214`<br>`res_drvr_atp.s:1740` | — |
| **`ATP_LISTENER_RESENDLOOP`** | `0x01A5CE` | `0x032FEE` | `res_drvr_atp.s:1205`<br>`res_drvr_atp.s:1731` | D1.B = requested bitmap (socket in the high word), A1 = BDS TResp header with sequence number -1 (incremented per entry) one pass per BDS entry |
| **`ATP_LISTENER_RSPCBLOOP`** | `0x01A572` | `0x032F92` | `res_drvr_atp.s:1151`<br>`res_drvr_atp.s:1683` | exactly-once request? known transaction? new transaction: allocate an RspCB if a GetRequest waits |
| **`ATP_LISTENER_RTS`** | `0x01A608` | `0x033028` | `res_drvr_atp.s:1235`<br>`res_drvr_atp.s:1758` | take the BDS entry; send it if requested and present send it ATP_LISTENER_RTS return to MPP |
| **`ATP_LISTENER_SLOT1`** | — | `0x032D3C` | `res_drvr_atp.s:1329` | — |
| **`ATP_LISTENER_SLOT10`** | — | `0x032D60` | `res_drvr_atp.s:1356` | — |
| **`ATP_LISTENER_SLOT11`** | — | `0x032D64` | `res_drvr_atp.s:1359` | — |
| **`ATP_LISTENER_SLOT12`** | — | `0x032D68` | `res_drvr_atp.s:1362` | — |
| **`ATP_LISTENER_SLOT13`** | — | `0x032D6C` | `res_drvr_atp.s:1365` | — |
| **`ATP_LISTENER_SLOT14`** | — | `0x032D70` | `res_drvr_atp.s:1368` | — |
| **`ATP_LISTENER_SLOT15`** | — | `0x032D74` | `res_drvr_atp.s:1371` | — |
| **`ATP_LISTENER_SLOT16`** | — | `0x032D78` | `res_drvr_atp.s:1374` | — |
| **`ATP_LISTENER_SLOT17`** | — | `0x032D7C` | `res_drvr_atp.s:1377` | — |
| **`ATP_LISTENER_SLOT18`** | — | `0x032D80` | `res_drvr_atp.s:1380` | — |
| **`ATP_LISTENER_SLOT19`** | — | `0x032D84` | `res_drvr_atp.s:1383` | — |
| **`ATP_LISTENER_SLOT2`** | — | `0x032D40` | `res_drvr_atp.s:1332` | — |
| **`ATP_LISTENER_SLOT20`** | — | `0x032D88` | `res_drvr_atp.s:1386` | — |
| **`ATP_LISTENER_SLOT21`** | — | `0x032D8C` | `res_drvr_atp.s:1389` | — |
| **`ATP_LISTENER_SLOT22`** | — | `0x032D90` | `res_drvr_atp.s:1392` | — |
| **`ATP_LISTENER_SLOT23`** | — | `0x032D94` | `res_drvr_atp.s:1395` | — |
| **`ATP_LISTENER_SLOT24`** | — | `0x032D98` | `res_drvr_atp.s:1398` | — |
| **`ATP_LISTENER_SLOT25`** | — | `0x032D9C` | `res_drvr_atp.s:1401` | — |
| **`ATP_LISTENER_SLOT26`** | — | `0x032DA0` | `res_drvr_atp.s:1404` | — |
| **`ATP_LISTENER_SLOT27`** | — | `0x032DA4` | `res_drvr_atp.s:1407` | — |
| **`ATP_LISTENER_SLOT28`** | — | `0x032DA8` | `res_drvr_atp.s:1410` | — |
| **`ATP_LISTENER_SLOT29`** | — | `0x032DAC` | `res_drvr_atp.s:1413` | — |
| **`ATP_LISTENER_SLOT3`** | — | `0x032D44` | `res_drvr_atp.s:1335` | — |
| **`ATP_LISTENER_SLOT30`** | — | `0x032DB0` | `res_drvr_atp.s:1416` | — |
| **`ATP_LISTENER_SLOT31`** | — | `0x032DB4` | `res_drvr_atp.s:1419` | — |
| **`ATP_LISTENER_SLOT4`** | — | `0x032D48` | `res_drvr_atp.s:1338` | — |
| **`ATP_LISTENER_SLOT5`** | — | `0x032D4C` | `res_drvr_atp.s:1341` | — |
| **`ATP_LISTENER_SLOT6`** | — | `0x032D50` | `res_drvr_atp.s:1344` | — |
| **`ATP_LISTENER_SLOT7`** | — | `0x032D54` | `res_drvr_atp.s:1347` | — |
| **`ATP_LISTENER_SLOT8`** | — | `0x032D58` | `res_drvr_atp.s:1350` | — |
| **`ATP_LISTENER_SLOT9`** | — | `0x032D5C` | `res_drvr_atp.s:1353` | — |
| **`ATP_LISTENER_STS`** | `0x01A4D0` | `0x032ECE` | `res_drvr_atp.s:1073`<br>`res_drvr_atp.s:1589` | STS set in the response: resend the TReq with the bitmap still missing |
| **`ATP_LISTENER_TODELIVER`** | `0x01A592` | `0x032FB2` | `res_drvr_atp.s:1174`<br>`res_drvr_atp.s:1701` | deliver the request |
| **`ATP_LISTENER_TOTREL`** | — | `0x032DFC` | `res_drvr_atp.s:1463` | — |
| **`ATP_LISTENER_TOTREQ`** | — | `0x032DF8` | `res_drvr_atp.s:1461` | — |
| **`ATP_LISTENER_TREL`** | `0x01A3E4` | `0x032CD8` | `res_drvr_atp.s:956`<br>`res_drvr_atp.s:1272` | ATP_LISTENER_TREL: TRel (function code 11) - the requester releases an exactly-once transaction: free its RspCB and complete the SendResponse (userData = user bytes of the TRel).  D0 = destination soc... |
| **`ATP_LISTENER_TREQ`** | `0x01A3B0` | `0x032D0C` | `res_drvr_atp.s:919`<br>`res_drvr_atp.s:1299` | ATP_LISTENER_TREQ: TReq (function code 01) - D0 = destination socket, A5 = ATPVars.  Reads the request data into the buffer of the first GetRequest queued on the socket (nothing if none is queued). |
| **`ATP_LISTENER_TREQLOOP`** | `0x01A3B6` | — | `res_drvr_atp.s:924` | find the responding socket |
| **`ATP_LISTENER_TREQREAD`** | `0x01A3D2` | `0x032D2A` | `res_drvr_atp.s:935`<br>`res_drvr_atp.s:1311` | read the request into the first queued GetRequest's buffer |
| **`ATP_LISTENER_TRESPEXIT`** | — | `0x032E30` | `res_drvr_atp.s:1499` | BDS entry = bdsPointer + 12 * atpRespNo ReadRest into the buffer Called by: ATP_LISTENER_COMMON, ATP_LISTENER_NSFOUND, ATP_REQLISTENER, ATP_LISTENER_GOTRSP (bad packet or not for us) |
| **`ATP_LISTENER_TRESPLOOP`** | `0x01A436` | — | `res_drvr_atp.s:1003` | function code 10 = TResp: find the request slot of the socket |
| **`ATP_LISTENER_XO`** | — | `0x032F1E` | `res_drvr_atp.s:1623` | — |
| **`ATP_LISTENER_XODONE`** | `0x01A58E` | `0x032FAE` | `res_drvr_atp.s:1171`<br>`res_drvr_atp.s:1698` | — |
| **`ATP_MPPCALL`** | `0x01A206` | `0x032A34` | `res_drvr_atp.s:678`<br>`res_drvr_atp.s:892` | WDS entry 1: DDP header template (odd address CB+$4F) WDS entry 2: ATP header, entry 3: data, then the terminator WriteDDP via .MPP ATP_MPPCALL: async _Control D0 to .MPP with CB A3 (socket D1).  Save... |
| **`ATP_MPPDONE`** | `0x01A226` | `0x032A56` | `res_drvr_atp.s:695`<br>`res_drvr_atp.s:909` | ATP_MPPDONE: ioCompletion of the CBs (A0 = CB, D0 = result): restore the saved registers and continue after the BSR ATP_MPPCALL, with A3 = CB, A2 = ATPVars and the condition codes set from D0 |
| **`ATP_READRESP`** | — | `0x032E06` | `res_drvr_atp.s:1478` | ATP_READRESP (ReadResp in Apple's source): TResp for request A5 (SendRequest or NSendRequest; whole ATP header read, A3 -> its end): read the data straight into the BDS buffer of the response number. ... |
| **`ATP_REQFAILED`** | — | `0x032AAC` | `res_drvr_atp.s:960` | ATP_REQFAILED: complete request A0 with reqFailed (retries used up) |
| **`ATP_REQLISTENER`** | — | `0x032E32` | `res_drvr_atp.s:1509` | ATP_REQLISTENER: DDP socket listener of the private sockets of the SendRequests (one per request slot): only TResp packets count; finds the request slot of the destination socket (D2 = slot * 4, A5 = ... |
| **`ATP_REQLISTENER_LOOP`** | — | `0x032E56` | `res_drvr_atp.s:1524` | find the request slot of the socket |
| **`ATP_RETRYCOUNT`** | — | `0x032AB4` | `res_drvr_atp.s:969` | ATP_RETRYCOUNT: one retry of request A0 used up: retryCount - 1 unless it is 255 (retry forever).  C set if retryCount was already 0 (give up). Called by ATP_VBLTASK (SendRequest and NSendRequest time... |
| **`ATP_RETRYCOUNT_EXIT`** | — | `0x032AC0` | `res_drvr_atp.s:973` | — |
| **`ATP_SCCENABLE`** | `0x01A536` | `0x032F56` | `res_drvr_atp.s:1116`<br>`res_drvr_atp.s:1649` | ATP_SCCENABLE: SR = vSCCEnable (MPP variables +$1C): allow SCC interrupts during the post-processing of a received packet |
| **`ATP_SCCENABLE_EXIT`** | `0x01A542` | `0x032F62` | `res_drvr_atp.s:1121`<br>`res_drvr_atp.s:1654` | — |
| **`ATP_SENDPKT`** | `0x01A1BC` | `0x0329EA` | `res_drvr_atp.s:646`<br>`res_drvr_atp.s:860` | next transaction ID socket and retry timer of the slot send the TReq ATP_SENDPKT ATP_SENDPKT: send the ATP packet of CB A3 (header at CB+$60): builds the WDS (DDP header template with type ATP and des... |
| **`ATP_SETBITMAP`** | — | `0x0329CA` | `res_drvr_atp.s:836` | ATP_SETBITMAP: currBitmap of request A0 = one bit per expected response (bits 0..numOfBuffs-1), EOM cleared, numOfResps = 0; D2 = D2 * 4 (slot -> long index).  Uses D0, A1.  Called by SENDREQUEST, NSE... |
| **`ATP_SETBITMAP_DONE`** | — | `0x0329E2` | `res_drvr_atp.s:847` | — |
| **`ATP_SETBITMAP_LOOP`** | — | `0x0329DC` | `res_drvr_atp.s:843` | — |
| **`ATP_SETDATA`** | `0x01A25A` | `0x032A8A` | `res_drvr_atp.s:721`<br>`res_drvr_atp.s:935` | ATP_SETDATA: atpUserData = userData, D0/D2 = reqLength/reqPointer of parameter block A0; A3 back to the CB (A3 = CB+$64 on entry) |
| **`ATP_SETDATA_EXIT`** | — | `0x032A9A` | `res_drvr_atp.s:940` | — |
| **`ATP_SNDRQINIT`** | — | `0x0329B8` | `res_drvr_atp.s:822` | ATP_SNDRQINIT (SndRqInit in Apple's source): reqLength of A0 must be <= atpMaxData (578), else D0 = ddpLenErr; then claim a CB (A3; D0 = noDataArea if none).  Returns the condition codes of D0 (EQ = o... |
| **`ATP_SNDRQINIT_EXIT`** | — | `0x0329C6` | `res_drvr_atp.s:827` | — |
| **`ATP_UNLINKNSREQ`** | — | `0x032AC2` | `res_drvr_atp.s:982` | ATP_UNLINKNSREQ: remove request A0 from the NSendRequest queue of responding socket slot D2 (interrupts off) -> EQ and D0 = 0 if it was there, else NE and D0 = cbNotFound.  Uses A1. Called by ATP_VBLT... |
| **`ATP_UNLINKNSREQ_EXIT`** | — | `0x032AE4` | `res_drvr_atp.s:999` | — |
| **`ATP_UNLINKNSREQ_FOUND`** | — | `0x032AE2` | `res_drvr_atp.s:997` | — |
| **`ATP_UNLINKNSREQ_LOOP`** | — | `0x032AD2` | `res_drvr_atp.s:989` | — |
| **`ATP_UNLINKNSREQ_NONE`** | — | `0x032AEA` | `res_drvr_atp.s:1003` | — |
| **`ATP_VBLTASK`** | `0x01A26C` | `0x032AF0` | `res_drvr_atp.s:737`<br>`res_drvr_atp.s:1021` | ATP_VBLTASK: VBL task, once per second (A0 = task).  Request slots: count down the retry timers; on expiry retransmit the TReq (bitmap of the responses still missing) or, when retryCount is used up, c... |
| **`ATP_VBLTASK_EXIT`** | `0x01A316` | `0x032BFC` | `res_drvr_atp.s:814`<br>`res_drvr_atp.s:1143` | done |
| **`ATP_VBLTASK_FAIL`** | `0x01A2C4` | `0x032B50` | `res_drvr_atp.s:776`<br>`res_drvr_atp.s:1059` | retries used up: close the socket, complete with reqFailed |
| **`ATP_VBLTASK_NEXTREQ`** | `0x01A284` | `0x032B18` | `res_drvr_atp.s:747`<br>`res_drvr_atp.s:1034` | — |
| **`ATP_VBLTASK_NEXTRSP`** | `0x01A310` | `0x032BF6` | `res_drvr_atp.s:810`<br>`res_drvr_atp.s:1139` | RspCB in use: one second older; released after 30 seconds release timeout: free the RspCB, complete its SendResponse with noRelErr |
| **`ATP_VBLTASK_NEXTSKT`** | — | `0x032B66` | `res_drvr_atp.s:1069` | — |
| **`ATP_VBLTASK_NSCOUNT`** | — | `0x032B76` | `res_drvr_atp.s:1077` | one second less for every NSendRequest of the socket |
| **`ATP_VBLTASK_NSEXPIRED`** | — | `0x032B94` | `res_drvr_atp.s:1094` | expired: retransmit (timer = timeOutVal) or give up |
| **`ATP_VBLTASK_NSFAIL`** | — | `0x032BB6` | `res_drvr_atp.s:1108` | retries used up: dequeue it, complete with reqFailed |
| **`ATP_VBLTASK_NSFIND`** | — | `0x032B86` | `res_drvr_atp.s:1086` | — |
| **`ATP_VBLTASK_NSREQS`** | — | `0x032B64` | `res_drvr_atp.s:1067` | NSendRequests: the responding sockets (interrupts still off) |
| **`ATP_VBLTASK_NSRESCAN`** | — | `0x032BAE` | `res_drvr_atp.s:1103` | — |
| **`ATP_VBLTASK_NSSCAN`** | — | `0x032B80` | `res_drvr_atp.s:1083` | look for an expired one (from the start of the queue) |
| **`ATP_VBLTASK_REQDONE`** | `0x01A2DC` | `0x032BC2` | `res_drvr_atp.s:785`<br>`res_drvr_atp.s:1114` | request slots done: release the CB |
| **`ATP_VBLTASK_REQLOOP`** | `0x01A27E` | `0x032B12` | `res_drvr_atp.s:744`<br>`res_drvr_atp.s:1031` | scan the request slots |
| **`ATP_VBLTASK_RETRY`** | `0x01A2B0` | — | `res_drvr_atp.s:766` | retry timer expired retransmit the TReq |
| **`ATP_VBLTASK_RSPCBS`** | `0x01A2E2` | `0x032BC8` | `res_drvr_atp.s:789`<br>`res_drvr_atp.s:1118` | release timers of the RspCBs |
| **`ATP_VBLTASK_RSPLOOP`** | `0x01A2EE` | `0x032BD4` | `res_drvr_atp.s:794`<br>`res_drvr_atp.s:1123` | — |
| **`ATTACHPH`** | `0x01A928` | `0x033460` | `res_drvr_mpp.s:485`<br>`res_drvr_mpp.s:679` | AttachPH (csCode 245): enter protocol handler handler for LAP type protType (1..127) in the protocol table.  lapProtErr if invalid, already attached or the table (4 entries, 2 used by DDP) is full. |
| **`ATTACHPH_DONE`** | `0x01A94A` | `0x033482` | `res_drvr_mpp.s:502`<br>`res_drvr_mpp.s:697` | Called by: ATTACHPH, DETACHPH, WRITELAP |
| **`ATTACHPH_LOOP`** | `0x01A934` | `0x03346C` | `res_drvr_mpp.s:492`<br>`res_drvr_mpp.s:686` | — |
| **`ATTACHPH_NOERR`** | `0x01A948` | `0x033480` | `res_drvr_mpp.s:500`<br>`res_drvr_mpp.s:694` | — |
| **`BBMC_Frame_1_PackBits`** | — | `0x01D93C` | `res_bbmc.s:28` | Hidden image frame 1 data. |
| **`BBMC_Frame_2_PackBits`** | — | `0x022F3C` | `res_bbmc.s:5534` | Hidden image frame 2 data. |
| **`BBMC_Frame_3_PackBits`** | — | `0x028040` | `res_bbmc.s:10722` | Hidden image frame 3 data. |
| **`BBMC_Frame_4_PackBits`** | — | `0x02D024` | `res_bbmc.s:15837` | Hidden image frame 4 data. |
| **`bbmc_team_photos`** | — | `0x01D924` | `res_bbmc.s:16` | — |
| **`CDEF0_BUTSTUB`** | — | `0x037A92` | `res_cdef_0.s:156` | ButStub -- DrawPBut's exit for an invisible control |
| **`CDEF0_CALCPBUT`** | — | `0x037C6A` | `res_cdef_0.s:460` | CalcPBut -- message 2 (calcCRgns): return the bounding region of the button. D3 (in)   handle of the region to set (buttons have no indicator: the Control Manager never sets the high bit here) A push ... |
| **`CDEF0_CALCSQUARE`** | — | `0x037C9C` | `res_cdef_0.s:482` | — |
| **`CDEF0_CHECKROUND`** | — | `0x037C34` | `res_cdef_0.s:414` | — |
| **`CDEF0_DISABLETEXT`** | — | `0x037BF4` | `res_cdef_0.s:377` | DisableText -- dim an inactive control: paint contrlRect, inset by 3 pixels horizontally and 1 vertically (inside a push button's frame), with the gray pattern in patBic mode, which clears every other... |
| **`CDEF0_DONEDRWBUT`** | — | `0x037BBE` | `res_cdef_0.s:313` | restore original font, face and size hilite the button if necessary restore original clipping region and we're done |
| **`CDEF0_DONEP1`** | — | `0x037A7E` | `res_cdef_0.s:142` | we're done -- restore registers and return to caller |
| **`CDEF0_DONEPCHECK`** | — | `0x037D4C` | `res_cdef_0.s:572` | — |
| **`CDEF0_DONEXTLINE`** | — | `0x037B40` | `res_cdef_0.s:252` | now get a font info record on stack, pointer to it in A3 Set up D5 to point to the baseline of the last line draw the lines from the last one up: get the width of the current line into D0 |
| **`CDEF0_DRAGGRAY`** | — | `0x037C8C` | `res_cdef_0.s:476` | set the pattern for indicator dragging |
| **`CDEF0_DRAWBTITLE`** | — | `0x037B72` | `res_cdef_0.s:275` | — |
| **`CDEF0_DRAWPBUT`** | — | `0x037A94` | `res_cdef_0.s:174` | DrawPBut -- message 0 (drawCntl): draw the push button, check box or radio button with its title and hilite state. D3 (in)  low byte: the part to draw; the whole control is drawn anyway, but a check b... |
| **`CDEF0_DRAWPBUT_COUNT`** | — | `0x037B10` | `res_cdef_0.s:228` | Save off some registers for mondo button title calculations, then set them up for our use now count the number of lines in the title. Lines are separated by CR's |
| **`CDEF0_DRAWPBUT_GOTFONT`** | — | `0x037ADC` | `res_cdef_0.s:205` | save old clip region and clip to the bounding rectangle sected with oldClip |
| **`CDEF0_DRAWPBUT_GOTSIZE`** | — | `0x037AD8` | `res_cdef_0.s:202` | — |
| **`CDEF0_DRAWRBUTTON`** | — | `0x037D3E` | `res_cdef_0.s:566` | now we can draw the check if we're supposed to draw the radio button check mark -- a little circle |
| **`CDEF0_ELCENTRO`** | — | `0x037B62` | `res_cdef_0.s:269` | if it's a checkbox, don't center it, just move to right a little center the line in the rect |
| **`CDEF0_ENTRY`** | — | `0x037A30` | `res_cdef_0.s:106` | Entry point and Apple's standard defproc header: a branch around it, flags, resource type, resource ID and version number. |
| **`CDEF0_ERASECBOUND`** | — | `0x037AAA` | `res_cdef_0.s:183` | — |
| **`CDEF0_FRAMECHECK`** | — | `0x037CF8` | `res_cdef_0.s:534` | — |
| **`CDEF0_FRAMECHECK_DONE`** | — | `0x037D06` | `res_cdef_0.s:542` | — |
| **`CDEF0_FRAMECHECK_OVAL`** | — | `0x037D04` | `res_cdef_0.s:540` | — |
| **`CDEF0_GETHEIGHT`** | — | `0x037BE2` | `res_cdef_0.s:354` | GetHeight -- return in D0 the height of one line. A3 (in)   FontInfo record D0 (out)  line height = ascent + descent + leading Called by: CDEF0_DRAWPBUT (before and after each line) |
| **`CDEF0_GOPUSHBUT`** | — | `0x037A8C` | `res_cdef_0.s:151` | GoPushBut -- dispatch table: offsets of the message routines from the table, indexed by message * 2 |
| **`CDEF0_HITPBUT`** | — | `0x037C38` | `res_cdef_0.s:426` | HitPBut -- message 1 (testCntl): the button hit test. D3 (in)   the point, in local coordinates of the window Result (low word of the function result): 0 if contrlHilite is 255 or the point is outside... |
| **`CDEF0_HITPBUT_DONE`** | — | `0x037C60` | `res_cdef_0.s:442` | — |
| **`CDEF0_NOTITLE`** | — | `0x037B8E` | `res_cdef_0.s:291` | bump baseline point up to next line, test for end |
| **`CDEF0_PLOTCHECK`** | — | `0x037CA6` | `res_cdef_0.s:501` | PlotCheck takes care of drawing the actual check box of the check box button. It figures out where to draw the box, draws it, and then checks it or not based on the current value and hilite state of t... |
| **`CDEF0_PT2NEXT`** | — | `0x037BCA` | `res_cdef_0.s:334` | Pt2Next -- point to the next line within the title, going backwards from the end of the title. A2 (in)   title pointer (Pascal string) D7 (in)   offset of the last character of the next line to do D7 ... |
| **`CDEF0_PT2NEXT_DONE`** | — | `0x037BDE` | `res_cdef_0.s:344` | — |
| **`CDEF0_PT2NEXT_LOOP`** | — | `0x037BD0` | `res_cdef_0.s:338` | — |
| **`CDEF0_RETURN254`** | — | `0x037C62` | `res_cdef_0.s:444` | — |
| **`CDEF0_ROUNDCALC`** | — | `0x037C1E` | `res_cdef_0.s:404` | RoundCalc calculates the rounding factor in D4 based on the control's rect. A0 (in)   control pointer D6 (in)   variation code AND 7 D4 (out)  oval width (high word) and height (low word) of the corne... |
| **`CDEF0_SKIPCERASE`** | — | `0x037AB0` | `res_cdef_0.s:188` | save the current font and force the system font |
| **`CDEF0_SKIPDIS`** | — | `0x037CF0` | `res_cdef_0.s:531` | erase the check box OK, now we must fill in the checkBox rectangle based on the value and hilite state of the control its hilited so up the penSize to indicate its hilited |
| **`CDEF0_SPECIALHILITE`** | — | `0x037BF0` | `res_cdef_0.s:362` | SpecialHilite -- contrlHilite 254 or 255: dim the push button |
| **`CDEF0_START`** | — | `0x037A3C` | `res_cdef_0.s:118` | PushButProc -- save the registers and the pen state, fetch the parameters and dispatch on the message through GoPushBut. |
| **`CDEF1_CALCIBOX`** | — | `0x038000` | `res_cdef_1.s:541` | CalcIBox is the crucial routine that computes the position of the top/left of the thumb by scaling the control's value according to its range and the screen area. Return the rectangle in IndicatorRect... |
| **`CDEF1_CALCSBAR`** | — | `0x038124` | `res_cdef_1.s:727` | CalcSBar returns the bounding region of the scroll bar (message 2, calcCRgns). D3 holds the region parameter. If the high bit of D3 is set, return the indicator region, otherwise return the entire bou... |
| **`CDEF1_CHECKIND`** | — | `0x0380CE` | `res_cdef_1.s:665` | its not in either button so it must be the thumb or one of the page areas. Check for the thumb first |
| **`CDEF1_CHECKPAGE`** | — | `0x0380F0` | `res_cdef_1.s:682` | its in the thumb so report that to the application it must be in one of the two page areas. Determine which one by looking at the midPoint of the indicator's bounding rectangle. |
| **`CDEF1_DISPSBAR`** | — | `0x0381BA` | `res_cdef_1.s:824` | DispSBar de-allocates the region used for the indicator (message 4, dispCntl). |
| **`CDEF1_DOINDICATOR`** | — | `0x037F76` | `res_cdef_1.s:433` | DoIndicator -- DrawSBar's tail: compute the thumb (CalcIBox) and, unless the scroll bar is inactive, fill the thumb region white and frame it; then frame the scroll bar (FrameCtl, also the whole drawi... |
| **`CDEF1_DONECHECKING`** | — | `0x037F74` | `res_cdef_1.s:424` | — |
| **`CDEF1_DOWNARROW`** | — | `0x037E38` | `res_cdef_1.s:239` | down arrow (second arrow of a vertical bar) ($37E38) |
| **`CDEF1_DOWNARROWHILITED`** | — | `0x037E58` | `res_cdef_1.s:257` | down arrow, hilited ($37E58) |
| **`CDEF1_DRAWARROWBOX`** | — | `0x037FB6` | `res_cdef_1.s:487` | DrawArrowBox is a routine that blits across the appropriate arrow into an arrow box (looks at hilite state); the bitmaps include the box frame. On entry, TempRect has the box for the arrow, D0 has h/v... |
| **`CDEF1_DRAWARROWBOX_PLOT`** | — | `0x037FCA` | `res_cdef_1.s:496` | — |
| **`CDEF1_DRAWARROWBOX_VERT`** | — | `0x037FC2` | `res_cdef_1.s:492` | — |
| **`CDEF1_DRAWSBAR`** | — | `0x037EB8` | `res_cdef_1.s:324` | DrawSBar draws a scroll bar as specified by the controlHandle in A3 (message 0, drawCntl). D3 has the desired "hilite" area code. D3 (in)  low byte: part to draw (ShouldIDraw): 0 or 255 = all (255: Hi... |
| **`CDEF1_DRAWSBAR_BODY`** | — | `0x037F38` | `res_cdef_1.s:374` | — |
| **`CDEF1_DRAWSBAR_GO`** | — | `0x037EC8` | `res_cdef_1.s:331` | if it was disabled, draw the whole thing |
| **`CDEF1_DRAWSBAR_INSET`** | — | `0x037F4C` | `res_cdef_1.s:383` | — |
| **`CDEF1_ENTRY`** | — | `0x037D5A` | `res_cdef_1.s:102` | Entry point and Apple's standard defproc header: a branch around it, flags, resource type, resource ID and version number. |
| **`CDEF1_FRAMECTL`** | — | `0x037F8E` | `res_cdef_1.s:444` | Frame the scroll bar |
| **`CDEF1_GETCTLRECT`** | — | `0x038072` | `res_cdef_1.s:602` | GetCtlRect is a code saving utility that copies the bounding rectangle of the control whose handle is in A3 into the rectangle pointed to by A1. This routine blows A0 but preserves A1. GetTCtlRect is ... |
| **`CDEF1_GETINDRGN`** | — | `0x038132` | `res_cdef_1.s:735` | the indicator region was requested so copy the one in the dataHandle |
| **`CDEF1_GETLTGRAY`** | — | `0x03814E` | `res_cdef_1.s:755` | set the pattern for dragging GetLtGray -- get the scroll bar pattern (Apple's later version, GetOldStyleLtGray, returns the handle). A0 (out)  pointer to the pattern, PAT resource 17 (sBarPatID, light... |
| **`CDEF1_GETTCTLRECT`** | — | `0x03806E` | `res_cdef_1.s:600` | GetCtlRect is a code saving utility that copies the bounding rectangle of the control whose handle is in A3 into the rectangle pointed to by A1. This routine blows A0 but preserves A1. GetTCtlRect is ... |
| **`CDEF1_GOSCROLLBAR`** | — | `0x037DA6` | `res_cdef_1.s:147` | GoScrollBar -- dispatch table: offsets of the message routines from the table, indexed by message * 2 |
| **`CDEF1_HITSBAR`** | — | `0x038082` | `res_cdef_1.s:622` | HitSBar is the hit test routine for the scroll bar definition routine (message 1, testCntl). It classifies the position of the mouse passed in D3. D3 (in)  the point, in local coordinates of the windo... |
| **`CDEF1_HITSBAR_DOWN`** | — | `0x0380B6` | `res_cdef_1.s:649` | its in the rect, so classify if in upButton,downButton,pageUp,pageDown or thumb see if its in the top button see if its in the bottom button |
| **`CDEF1_HITSBAR_INCTL`** | — | `0x038092` | `res_cdef_1.s:628` | — |
| **`CDEF1_INITSBAR`** | — | `0x0381AE` | `res_cdef_1.s:813` | compute range of logical values: controlMax - controlMin compute position*logical range/physical range at this point D1 has the value so set it, after offsetting by the minimum InitSBar gets called wh... |
| **`CDEF1_ISDISABLED`** | — | `0x037F5E` | `res_cdef_1.s:415` | IsDisabled is a utility to check to see if a scrollBar is disabled or not. It returns with the z-flag set if it is disabled: contrlHilite 255 or 254, or contrlMin = contrlMax. (Apple's later version d... |
| **`CDEF1_LEFTARROW`** | — | `0x037DF8` | `res_cdef_1.s:203` | left arrow (first arrow of a horizontal bar) ($37DF8) |
| **`CDEF1_LEFTARROWHILITED`** | — | `0x037E18` | `res_cdef_1.s:221` | left arrow, hilited ($37E18) |
| **`CDEF1_MOVESBAR`** | — | `0x03815C` | `res_cdef_1.s:770` | handle the "position yourself" message (5, posCntl) by figuring out the new value and calling SetCtlValue. D3 holds the amount to move by. new value = min + (thumb position - top - minor) * (max - min... |
| **`CDEF1_MOVESBAR_VERT`** | — | `0x03817C` | `res_cdef_1.s:785` | figure out new position by adding topLeft of current position to offset select the relevant dimension and get it into the low word of D3 determine amount of screen area devoted to the scrollBar |
| **`CDEF1_NORMALIZEPT`** | — | `0x038118` | `res_cdef_1.s:712` | NormalizePt takes a rect pointer in A4 and a point in D3 and swaps the points coordinates according to the relevant dimensions: for a vertical bar the point's v comes into the low word (calling it aga... |
| **`CDEF1_NORMALIZEPT_DONE`** | — | `0x038122` | `res_cdef_1.s:717` | — |
| **`CDEF1_NOSBARHIT`** | — | `0x038080` | `res_cdef_1.s:607` | — |
| **`CDEF1_PAGEITUP`** | — | `0x038114` | `res_cdef_1.s:699` | determine midpoint at this point, D1 has the midpoint in the important dimension. Compare with the mouse point to decide if its page up or down. |
| **`CDEF1_PLOTSYMBOL`** | — | `0x037FD0` | `res_cdef_1.s:511` | PlotSymbol -- copy a 16 x 16 bitmap into TempRect (scaled if the box is not 16 x 16). A1 (in)   the bits (rowBytes 2) D0 (in)   transfer mode Builds the BitMap in IconBitmap: baseAddr A1, rowBytes 2, ... |
| **`CDEF1_RETURN254`** | — | `0x0380C8` | `res_cdef_1.s:660` | — |
| **`CDEF1_RIGHTARROW`** | — | `0x037DB8` | `res_cdef_1.s:167` | Arrow bitmaps: 16 x 16 pixels with the box frame, rowBytes 2, 32 bytes each; PlotSymbol builds the BitMap around them in IconBitmap. Each arrow is followed by its hilited (filled) version. DrawSBar po... |
| **`CDEF1_RIGHTARROWHILITED`** | — | `0x037DD8` | `res_cdef_1.s:185` | right arrow, hilited ($37DD8) |
| **`CDEF1_ROUNDDONE`** | — | `0x0381D2` | `res_cdef_1.s:846` | — |
| **`CDEF1_ROUNDOFF`** | — | `0x0381C2` | `res_cdef_1.s:837` | Utility RoundOff -- RoundOff the number in D1 to the nearest integer. The remainder from dividing by D2 is in the high part of the word. D1 (in)    result of a DIVU by D2: remainder:quotient D2 (in)  ... |
| **`CDEF1_SCALE0`** | — | `0x03806A` | `res_cdef_1.s:586` | set up the indicator region if min = max, pin at top |
| **`CDEF1_SHOULDIDRAW`** | — | `0x037F56` | `res_cdef_1.s:399` | Utility ShouldIDraw -- to test when to skip drawing a part of the scrollBar. On entry, D3 has parameter indicating part that needs drawing while D1 holds the part we are about to draw. If D3 is zero, ... |
| **`CDEF1_SKIPDOWN`** | — | `0x037F10` | `res_cdef_1.s:359` | adjust rect for 2nd arrow paint the body of the scrollBar light gray |
| **`CDEF1_SKIPUP`** | — | `0x037EF0` | `res_cdef_1.s:346` | adjust for 1st arrow (if we're supposed to) now do the other arrow |
| **`CDEF1_START`** | — | `0x037D66` | `res_cdef_1.s:115` | ScrollBarProc -- save the registers and the pen state, fetch the parameters and dispatch on the message through GoScrollBar (no check of the message number). |
| **`CDEF1_STUBSBAR`** | — | `0x037F5C` | `res_cdef_1.s:403` | — |
| **`CDEF1_TESTHV`** | — | `0x037F98` | `res_cdef_1.s:463` | TestHV is a utility that determines if the rectangle pointed to by A0 is more horizontal or vertical. Return 0 in D0 if its more vertical and 2 if its more horizontal. This routine trashes D1. The res... |
| **`CDEF1_TESTHV_HORIZ`** | — | `0x037FB0` | `res_cdef_1.s:473` | — |
| **`CDEF1_THUMBSBAR`** | — | `0x0381DA` | `res_cdef_1.s:868` | ThumbSBar receives the "drag thumb" message (6, thumbCntl) for the scroll bar. On entry, D3 points to a structure that contains the starting point, it returns with pointers to the bounds and slopRect ... |
| **`CDEF1_THUMBSBAR_INSET`** | — | `0x0381FE` | `res_cdef_1.s:885` | — |
| **`CDEF1_THUMBSBAR_SLOP`** | — | `0x03821C` | `res_cdef_1.s:897` | build the slopRect by insetting the boundsRect |
| **`CDEF1_THUMBSBAR_VERT`** | — | `0x0381FC` | `res_cdef_1.s:883` | — |
| **`CDEF1_TRUNCATEIT`** | — | `0x0381D6` | `res_cdef_1.s:850` | no need to round up so just truncate it |
| **`CDEF1_UPARROW`** | — | `0x037E78` | `res_cdef_1.s:275` | up arrow (first arrow of a vertical bar) ($37E78) |
| **`CDEF1_UPARROWHILITED`** | — | `0x037E98` | `res_cdef_1.s:293` | up arrow, hilited ($37E98) |
| **`CDEF1_UPDATEIRECT`** | — | `0x038040` | `res_cdef_1.s:570` | compute control screen area in relevant dimension compute "screenSize times value" compute size of logical space perform the scaling update indicator rect to correct position |
| **`CDEF1_UPDATERESULT`** | — | `0x0380C2` | `res_cdef_1.s:657` | UpdateResult -- store the part code in D0 as the function result Called by: (branches) CDEF1_HITSBAR_INCTL, CDEF1_RETURN254, CDEF1_CHECKIND, CDEF1_CHECKPAGE, CDEF1_PAGEITUP |
| **`CHKCONNECT`** | `0x017E52` | `0x0347BC` | `res_drvr_sony.s:230`<br>`res_drvr_sony_fdhd.s:392` | ChkConnect -- floppy drive: connected? number of sides, interface |
| **`CHKCONNECT_RFN`** | — | — | `res_drvr_sony_fdhd.s:410` | — |
| **`CLOSEATPSKT`** | `0x019F36` | `0x03269C` | `res_drvr_atp.s:286`<br>`res_drvr_atp.s:392` | get a CB for the OpenSkt call OpenSkt via .MPP: D1 = socket, listener = ATP_LISTENER fill in the responding-socket slot CLOSEATPSKT CloseATPSkt (csCode 250): close responding socket atpSocket (D2 = it... |
| **`CLOSEATPSKT_LOOP`** | `0x019F56` | `0x0326BC` | `res_drvr_atp.s:298`<br>`res_drvr_atp.s:404` | free the slot and the socket's RspCBs |
| **`CLOSEATPSKT_NEXT`** | `0x019F5C` | `0x0326C2` | `res_drvr_atp.s:302`<br>`res_drvr_atp.s:408` | — |
| **`CLOSESKT`** | `0x01A7FA` | `0x033238` | `res_drvr_mpp.s:233`<br>`res_drvr_mpp.s:328` | CloseSkt (csCode 247): remove socket D1 from the socket table. ddpSktErr if 0 or not open. |
| **`CLOSESKT_DAS`** | — | `0x03324E` | `res_drvr_mpp.s:341` | — |
| **`CLOSESKT_DONE`** | `0x01A80A` | `0x03324A` | `res_drvr_mpp.s:241`<br>`res_drvr_mpp.s:339` | Called by: OPENSKT, CLOSESKT, WRITEDDP |
| **`CLOSESKT_NOERR`** | — | `0x033248` | `res_drvr_mpp.s:336` | — |
| **`CODES`** | `0x017EF8` | `0x03483E` | `res_drvr_sony.s:327`<br>`res_drvr_sony_fdhd.s:472` | CtlTbl -- control call dispatch table: csCode, offset of the handler for HD20 drives (3-6), offset of the handler for floppy drives (1-2), both relative to CODES; a zero word ends the table. KillIO (1... |
| **`CONFIRMNAME`** | `0x01B366` | `0x033FBA` | `res_drvr_mpp.s:2032`<br>`res_drvr_mpp.s:2222` | ConfirmName (csCode 250): send a LkUp for entityPtr directly to node confirmAddr.  A reply sets newSocket: noErr if it is the socket of confirmAddr, nbpConfDiff if not; nbpNoConfirm if none comes. |
| **`CSTR2DEC`** | `0x01CACE` | `0x01D436` | `res_pack_7.s:220`<br>`res_pack_7.s:222` | **Proto:** `CSTR2DEC -- _cstr2dec: PROCEDURE CStr2Dec(s: CStrPtr; VAR index:`<br>CSTR2DEC -- _cstr2dec: PROCEDURE CStr2Dec(s: CStrPtr; VAR index: INTEGER; VAR d: Decimal; VAR validPrefix: BOOLEAN): scan the C string (NUL-terminated) s from s[index]. Sets the C-string flag (bit 31 ... |
| **`DDP_RCVBADSKT`** | — | `0x03339E` | `res_drvr_mpp.s:572` | — |
| **`DDP_RCVDISCARD`** | `0x01A904` | `0x0333A2` | `res_drvr_mpp.s:453`<br>`res_drvr_mpp.s:577` | DDP_RCVDISCARD: drop the packet - ReadRest with D3 = 0 (left 0 by the successful ReadPacket) |
| **`DDP_RCVLONG`** | `0x01A8D2` | `0x03334C` | `res_drvr_mpp.s:417`<br>`res_drvr_mpp.s:529` | DDP_RCVLONG: protocol handler of LAP type 2 (longDDP).  Reads the other 11 header bytes into the RHA; delivers only datagrams for our network. |
| **`DDP_RCVSHORT`** | `0x01A8E4` | `0x03335E` | `res_drvr_mpp.s:431`<br>`res_drvr_mpp.s:542` | DDP_RCVSHORT: protocol handler of LAP type 1 (shortDDP).  Reads the other 3 header bytes (dest socket, source socket, type) into the RHA. |
| **`DDP_RCVSOCKET`** | `0x01A8EA` | `0x033364` | `res_drvr_mpp.s:436`<br>`res_drvr_mpp.s:549` | DDP_RCVSOCKET: jump to the listener of the destination socket (D0) |
| **`DDP_RCVSOCKET_LOOP`** | `0x01A8F2` | `0x03338C` | `res_drvr_mpp.s:440`<br>`res_drvr_mpp.s:565` | — |
| **`DDPWRITE`** | `0x01A824` | `0x033296` | `res_drvr_mpp.s:290`<br>`res_drvr_mpp.s:411` | DDPWRITE DDPWRITE: send a datagram.  A1 = WDS (first entry -> 16-byte header area at an odd address: +7 dest net, +11 dest node, +13 dest socket, +15 DDP type), D1 = source socket, D3.B = checksum fla... |
| **`DDPWRITE_CHECKSUM`** | `0x01A888` | `0x033302` | `res_drvr_mpp.s:351`<br>`res_drvr_mpp.s:472` | DDPWRITE_CHECKSUM: DDP checksum over D0 bytes at (A0)+ into D3 (add, rotate left one bit); D2 bits 15-8 must be clear |
| **`DDPWRITE_CKSDONE`** | `0x01A86A` | `0x0332E4` | `res_drvr_mpp.s:329`<br>`res_drvr_mpp.s:450` | DDPWRITE_CKSDONE store the checksum (a computed 0 is sent as $FFFF) |
| **`DDPWRITE_CKSLOOP`** | `0x01A860` | `0x0332DA` | `res_drvr_mpp.s:317`<br>`res_drvr_mpp.s:443` | complete the header in the first WDS entry long header: source network and node, optional checksum |
| **`DDPWRITE_EXIT`** | `0x01A892` | `0x03330C` | `res_drvr_mpp.s:357`<br>`res_drvr_mpp.s:479` | Called by: DDPWRITE, DDP_RCVLONG, DDP_RCVSHORT, DDPWRITE_LENERR |
| **`DDPWRITE_LENERR`** | `0x01A8CE` | `0x033348` | `res_drvr_mpp.s:408`<br>`res_drvr_mpp.s:521` | DDPWRITE_LENERR: datagram too long |
| **`DDPWRITE_LENGTH`** | `0x01A8A4` | `0x03331E` | `res_drvr_mpp.s:376`<br>`res_drvr_mpp.s:497` | total length from the WDS |
| **`DDPWRITE_LENLOOP`** | `0x01A8AC` | `0x033326` | `res_drvr_mpp.s:381`<br>`res_drvr_mpp.s:502` | — |
| **`DDPWRITE_LONG`** | `0x01A870` | `0x0332EA` | `res_drvr_mpp.s:334`<br>`res_drvr_mpp.s:455` | LAP type longDDP; the frame goes to the bridge, if one is known |
| **`DDPWRITE_SEND`** | `0x01A8B8` | `0x033332` | `res_drvr_mpp.s:393`<br>`res_drvr_mpp.s:510` | DDPWRITE_SEND: ddpLength, LAP type and destination, then LAPWRITE |
| **`DDPWRITE_SHORT`** | `0x01A894` | `0x03330E` | `res_drvr_mpp.s:366`<br>`res_drvr_mpp.s:487` | DDPWRITE_SHORT: short header - move dest socket, source socket and type down to +5..+7 (over the high byte of the dest network); LAP destination = dest node, LAP type shortDDP |
| **`DDPWRITE_SKTOK`** | — | `0x0332A6` | `res_drvr_mpp.s:420` | — |
| **`DEC2STR`** | `0x01CAC6` | `0x01D42E` | `res_pack_7.s:210`<br>`res_pack_7.s:212` | selector 3: Dec2Str |
| **`DEC2STR_ENTRY`** | `0x01CD70` | `0x01D6D8` | `res_pack_7.s:610`<br>`res_pack_7.s:612` | **Proto:** `DEC2STR_ENTRY -- _dec2str: PROCEDURE Dec2Str(f: DecForm; d: Decimal;`<br>DEC2STR_ENTRY -- _dec2str: PROCEDURE Dec2Str(f: DecForm; d: Decimal; VAR s: DecStr) (f and d passed by address): format the decimal record d as a string, FloatDecimal ("-1.234e+5": sign or blank, f.di... |
| **`DECSTR_ADDDIGITS`** | `0x01CE8A` | `0x01D7F2` | `res_pack_7.s:751`<br>`res_pack_7.s:753` | DECSTR_ADDDIGITS -- append D0 digits from (A1)+ (none if D0 <= 0); too long -> '?'. Called by: DECSTR_DIGITSOK, DECSTR_NEEDPOINT, DECSTR_ITSFIXED, DECSTR_ALLBEFORE, DECSTR_FROMMID |
| **`DECSTR_ADDPOINT`** | `0x01CE98` | `0x01D800` | `res_pack_7.s:763`<br>`res_pack_7.s:765` | DECSTR_ADDPOINT -- append '.'. |
| **`DECSTR_ADDZEROS`** | `0x01CEAA` | `0x01D812` | `res_pack_7.s:776`<br>`res_pack_7.s:778` | Called by: DECSTR_ALLBEFORE, DECSTR_ALLAFTER, DECSTR_NEEDPOINT, DECSTR_FROMMID |
| **`DECSTR_ALLAFTER`** | `0x01CEE2` | `0x01D84A` | `res_pack_7.s:816`<br>`res_pack_7.s:818` | DECSTR_ALLAFTER: all digits right of the point: "0.00ddd". |
| **`DECSTR_ALLBEFORE`** | `0x01CED0` | `0x01D838` | `res_pack_7.s:804`<br>`res_pack_7.s:806` | DECSTR_ALLBEFORE: all digits left of the point. |
| **`DECSTR_APPENDDIGIT`** | `0x01CB94` | `0x01D4FC` | `res_pack_7.s:327`<br>`res_pack_7.s:329` | DECSTR_APPENDDIGIT: append the digit D0 to d.sig (A2), count it in D2.B; past 19 digits only OR it into the 20th and count it as lost (D1 + 1); then get the next character (GetChar). |
| **`DECSTR_APPENDDIGIT_1`** | `0x01CB9E` | `0x01D506` | `res_pack_7.s:332`<br>`res_pack_7.s:334` | — |
| **`DECSTR_APPENDDIGIT_3`** | `0x01CBA6` | `0x01D50E` | `res_pack_7.s:339`<br>`res_pack_7.s:341` | DECSTR_APPENDDIGIT_3: digit 21 and later -- OR it into the 20th digit. |
| **`DECSTR_BD1DIGOUT`** | `0x01CA54` | `0x01D3BC` | `res_pack_7.s:137`<br>`res_pack_7.s:139` | DECSTR_BD1DIGOUT: output one BCD digit as ASCII (with leading zero suppression) |
| **`DECSTR_BD1OUT`** | `0x01CA4E` | `0x01D3B6` | `res_pack_7.s:132`<br>`res_pack_7.s:134` | DECSTR_BD1OUT DECSTR_BD1OUT: convert BCD byte pair to two ASCII digits D1 = packed BCD byte, outputs to (A1)+ D6 bit 15: leading-zero suppression flag Called by: DECSTR_BDPOSVAL |
| **`DECSTR_BDDOIT`** | `0x01CA5E` | `0x01D3C6` | `res_pack_7.s:143`<br>`res_pack_7.s:145` | — |
| **`DECSTR_BDFIN`** | `0x01CA40` | `0x01D3A8` | `res_pack_7.s:117`<br>`res_pack_7.s:119` | convert BCD digits to ASCII and store |
| **`DECSTR_BDNEGVAL`** | `0x01CA18` | `0x01D380` | `res_pack_7.s:95`<br>`res_pack_7.s:97` | negative: write '-' sign and negate |
| **`DECSTR_BDPOSVAL`** | `0x01CA1E` | `0x01D386` | `res_pack_7.s:99`<br>`res_pack_7.s:101` | shift-and-add BCD conversion: 32 iterations of double-dabble |
| **`DECSTR_BDSKIPIT`** | `0x01CA66` | `0x01D3CE` | `res_pack_7.s:147`<br>`res_pack_7.s:149` | — |
| **`DECSTR_D2INC`** | `0x01CDA8` | `0x01D710` | `res_pack_7.s:634`<br>`res_pack_7.s:636` | — |
| **`DECSTR_DBFIN`** | `0x01CAAE` | `0x01D416` | `res_pack_7.s:191`<br>`res_pack_7.s:193` | apply sign |
| **`DECSTR_DBNOSIGN`** | `0x01CA98` | `0x01D400` | `res_pack_7.s:178`<br>`res_pack_7.s:180` | digit loop: D0 = D0 * 10 + digit (using shifts: *10 = *2 + *8) |
| **`DECSTR_DBPOSSIGN`** | `0x01CA92` | `0x01D3FA` | `res_pack_7.s:173`<br>`res_pack_7.s:175` | selector 1 -- StringToNum (Apple LDEC2BIN): the Pascal string at A0 (optional sign, digits) to D0.L, modulo 2^32; A0 preserved. check for leading sign character |
| **`DECSTR_DEC2STR_DONE`** | `0x01CF02` | `0x01D86A` | `res_pack_7.s:833`<br>`res_pack_7.s:835` | — |
| **`DECSTR_DECMLFND`** | `0x01CE06` | `0x01D76E` | `res_pack_7.s:676`<br>`res_pack_7.s:678` | — |
| **`DECSTR_DIGITSOK`** | `0x01CE24` | `0x01D78C` | `res_pack_7.s:693`<br>`res_pack_7.s:695` | — |
| **`DECSTR_ENDDIGITS`** | `0x01CE96` | `0x01D7FE` | `res_pack_7.s:759`<br>`res_pack_7.s:761` | — |
| **`DECSTR_ERRXIT`** | `0x01CEB0` | `0x01D818` | `res_pack_7.s:783`<br>`res_pack_7.s:785` | DECSTR_ERRXIT -- the result does not fit: s := '?'. Called by: DECSTR_ITSAPASS, DECSTR_NOPOINT, DECSTR_LASTDIG, DECSTR_ADDDIGITS, DECSTR_ADDPOINT (and 1 more) |
| **`DECSTR_FINNAN`** | `0x01CDF2` | `0x01D75A` | `res_pack_7.s:662`<br>`res_pack_7.s:664` | — |
| **`DECSTR_FROMMID`** | `0x01CEF0` | `0x01D858` | `res_pack_7.s:824`<br>`res_pack_7.s:826` | — |
| **`DECSTR_FROMNAN`** | `0x01CE5E` | `0x01D7C6` | `res_pack_7.s:725`<br>`res_pack_7.s:727` | — |
| **`DECSTR_GETCHAR`** | `0x01CBAA` | `0x01D512` | `res_pack_7.s:347`<br>`res_pack_7.s:349` | DECSTR_GETCHAR -- D0 := next character of the string, flags of CMPI.B #'0',D0; at the end of the string (NUL for a C string, past A3 for a Pascal string) set validPrefix and end the number or back up ... |
| **`DECSTR_GETCHAR_1`** | `0x01CBB4` | `0x01D51C` | `res_pack_7.s:355`<br>`res_pack_7.s:357` | DECSTR_GETCHAR_1: Pascal string -- end reached when A0 passes A3. |
| **`DECSTR_GETCHAR_2`** | `0x01CBBA` | `0x01D522` | `res_pack_7.s:359`<br>`res_pack_7.s:361` | — |
| **`DECSTR_GETCHAR_3`** | `0x01CBC0` | `0x01D528` | `res_pack_7.s:366`<br>`res_pack_7.s:368` | DECSTR_GETCHAR_3: end of the Pascal string; DECSTR_GETCHAR_5: end of either string -- validPrefix := TRUE, then back up to the fallback pointer if there is one, else end the number (StateNum). |
| **`DECSTR_GETCHAR_5`** | `0x01CBC2` | `0x01D52A` | `res_pack_7.s:368`<br>`res_pack_7.s:370` | — |
| **`DECSTR_GETEXPDIGS`** | `0x01CE5C` | `0x01D7C4` | `res_pack_7.s:723`<br>`res_pack_7.s:725` | — |
| **`DECSTR_GETINLOOP`** | `0x01CE82` | `0x01D7EA` | `res_pack_7.s:742`<br>`res_pack_7.s:744` | — |
| **`DECSTR_GETMAPPED`** | `0x01CD44` | `0x01D6AC` | `res_pack_7.s:580`<br>`res_pack_7.s:582` | DECSTR_GETMAPPED -- next character, a-z mapped to A-Z, compared with D3.B (EQ if equal). Called by: DECSTR_STATE99, DECSTR_STATEINF |
| **`DECSTR_GETMAPPED_1`** | `0x01CD58` | `0x01D6C0` | `res_pack_7.s:587`<br>`res_pack_7.s:589` | — |
| **`DECSTR_HEX2BIN`** | `0x01CDF6` | `0x01D75E` | `res_pack_7.s:669`<br>`res_pack_7.s:671` | DECSTR_HEX2BIN -- D1 := D1 - 1; D3.B := value of the hex digit d.sig[D1]; when no digits are left go on at DECSTR_FINNAN (FinNaN) instead of returning. |
| **`DECSTR_HEYITSFXD`** | `0x01CDAA` | `0x01D712` | `res_pack_7.s:636`<br>`res_pack_7.s:638` | — |
| **`DECSTR_HEYITSPOS`** | `0x01CD9E` | `0x01D706` | `res_pack_7.s:630`<br>`res_pack_7.s:632` | DECSTR_HEYITSPOS: positive -- a leading blank in float style only. |
| **`DECSTR_INF_2`** | `0x01CD24` | `0x01D68C` | `res_pack_7.s:559`<br>`res_pack_7.s:561` | — |
| **`DECSTR_INF_3`** | `0x01CD28` | `0x01D690` | `res_pack_7.s:561`<br>`res_pack_7.s:563` | — |
| **`DECSTR_INF_3_1`** | `0x01CD36` | `0x01D69E` | `res_pack_7.s:570`<br>`res_pack_7.s:572` | DECSTR_INF_3_1: Pascal string -- at its end set validPrefix. |
| **`DECSTR_INF_3_3`** | `0x01CD3C` | `0x01D6A4` | `res_pack_7.s:573`<br>`res_pack_7.s:575` | — |
| **`DECSTR_INFFOUND`** | `0x01CF0E` | `0x01D876` | `res_pack_7.s:841`<br>`res_pack_7.s:843` | DECSTR_INFFOUND: "INF". |
| **`DECSTR_ITSANUMBER`** | `0x01CE0C` | `0x01D774` | `res_pack_7.s:682`<br>`res_pack_7.s:684` | DECSTR_ITSANUMBER: a number -- '0' gets exponent 0; then float or fixed style. |
| **`DECSTR_ITSAPASS`** | `0x01CDB0` | `0x01D718` | `res_pack_7.s:639`<br>`res_pack_7.s:641` | — |
| **`DECSTR_ITSFIXED`** | `0x01CEBA` | `0x01D822` | `res_pack_7.s:790`<br>`res_pack_7.s:792` | DECSTR_ITSFIXED: fixed style -- integer digits, '.', f.digits fraction digits. |
| **`DECSTR_LASTDIG`** | `0x01CE74` | `0x01D7DC` | `res_pack_7.s:735`<br>`res_pack_7.s:737` | — |
| **`DECSTR_LNGTHOK`** | `0x01CDE8` | `0x01D750` | `res_pack_7.s:656`<br>`res_pack_7.s:658` | — |
| **`DECSTR_LOOPD`** | `0x01CE90` | `0x01D7F8` | `res_pack_7.s:755`<br>`res_pack_7.s:757` | — |
| **`DECSTR_LOOPZ`** | `0x01CEA2` | `0x01D80A` | `res_pack_7.s:771`<br>`res_pack_7.s:773` | DECSTR_LOOPZ / DECSTR_ADDZEROS -- append D0 zeros (none if D0 <= 0). |
| **`DECSTR_NEEDPOINT`** | `0x01CE36` | `0x01D79E` | `res_pack_7.s:702`<br>`res_pack_7.s:704` | — |
| **`DECSTR_NEGEXP`** | `0x01CE56` | `0x01D7BE` | `res_pack_7.s:720`<br>`res_pack_7.s:722` | DECSTR_NEGEXP: negative exponent. |
| **`DECSTR_NEXTCMP`** | `0x01CE62` | `0x01D7CA` | `res_pack_7.s:727`<br>`res_pack_7.s:729` | — |
| **`DECSTR_NEXTDIG`** | `0x01CE70` | `0x01D7D8` | `res_pack_7.s:733`<br>`res_pack_7.s:735` | — |
| **`DECSTR_NIBOUT`** | `0x01CD5C` | `0x01D6C4` | `res_pack_7.s:593`<br>`res_pack_7.s:595` | DECSTR_NIBOUT -- D0.B := ASCII hex digit of the low nibble of D3. |
| **`DECSTR_NIBOUT_61`** | `0x01CD6A` | `0x01D6D2` | `res_pack_7.s:599`<br>`res_pack_7.s:601` | — |
| **`DECSTR_NOPOINT`** | `0x01CE42` | `0x01D7AA` | `res_pack_7.s:709`<br>`res_pack_7.s:711` | — |
| **`DECSTR_NOTAZERO`** | `0x01CE16` | `0x01D77E` | `res_pack_7.s:687`<br>`res_pack_7.s:689` | — |
| **`DECSTR_PKG7_ENTRY`** | `0x01C9EC` | `0x01D354` | `res_pack_7.s:71`<br>`res_pack_7.s:73` | Pkg7 entry: selector at 4(SP). Selector 0 (NumToString) falls through. |
| **`DECSTR_PSTR2DEC`** | `0x01CAD4` | `0x01D43C` | `res_pack_7.s:237`<br>`res_pack_7.s:239` | **Proto:** `DECSTR_CONT_5 -- _pstr2dec: PROCEDURE PStr2Dec(s: DecStr; VAR index:`<br>DECSTR_CONT_5 -- _pstr2dec: PROCEDURE PStr2Dec(s: DecStr; VAR index: INTEGER; VAR d: Decimal; VAR validPrefix: BOOLEAN): scan the Pascal string s from s[index] into the decimal record d (a finite stat... |
| **`DECSTR_SELECT2`** | `0x01CAB4` | `0x01D41C` | `res_pack_7.s:199`<br>`res_pack_7.s:201` | DECSTR_SELECT2 PACK 7 extended dispatch: selector 2=PStr2Dec, 3=Dec2Str, 4=CStr2Dec |
| **`DECSTR_SELECT2_2`** | `0x01CAC2` | `0x01D42A` | `res_pack_7.s:207`<br>`res_pack_7.s:209` | selector 2: PStr2Dec |
| **`DECSTR_SELECT2_4`** | `0x01CACA` | `0x01D432` | `res_pack_7.s:213`<br>`res_pack_7.s:215` | selector 4: CStr2Dec |
| **`DECSTR_SETLENGTH`** | `0x01CEF8` | `0x01D860` | `res_pack_7.s:829`<br>`res_pack_7.s:831` | — |
| **`DECSTR_START`** | `0x01CAD6` | `0x01D43E` | `res_pack_7.s:240`<br>`res_pack_7.s:242` | DECSTR_START: common part of PStr2Dec and CStr2Dec. |
| **`DECSTR_STATE0`** | `0x01CB1E` | `0x01D486` | `res_pack_7.s:265`<br>`res_pack_7.s:267` | — |
| **`DECSTR_STATE1_1`** | `0x01CB42` | `0x01D4AA` | `res_pack_7.s:278`<br>`res_pack_7.s:280` | — |
| **`DECSTR_STATE2`** | `0x01CB44` | `0x01D4AC` | `res_pack_7.s:280`<br>`res_pack_7.s:282` | — |
| **`DECSTR_STATE2_1`** | `0x01CB56` | `0x01D4BE` | `res_pack_7.s:292`<br>`res_pack_7.s:294` | DECSTR_STATE2_1 (Apple State2 @1): a character below '0', maybe after leading zeros: '.' starts the fraction; after zeros the number is 0; otherwise there is no number. |
| **`DECSTR_STATE2_2`** | `0x01CB68` | `0x01D4D0` | `res_pack_7.s:301`<br>`res_pack_7.s:303` | DECSTR_STATE2_2 (Apple State2 @2): a character above '0': a digit, or after leading zeros the end of the digits, else perhaps INF or NaN. |
| **`DECSTR_STATE4`** | `0x01CB78` | `0x01D4E0` | `res_pack_7.s:310`<br>`res_pack_7.s:312` | DECSTR_STATE4: integer digits; State5 at DECSTR_STATE5 looks for the decimal point. |
| **`DECSTR_STATE4_1`** | `0x01CB7A` | `0x01D4E2` | `res_pack_7.s:312`<br>`res_pack_7.s:314` | — |
| **`DECSTR_STATE5`** | `0x01CB84` | `0x01D4EC` | `res_pack_7.s:317`<br>`res_pack_7.s:319` | — |
| **`DECSTR_STATE6`** | `0x01CBD0` | `0x01D538` | `res_pack_7.s:376`<br>`res_pack_7.s:378` | DECSTR_STATE6: '.' before any nonzero digit -- skip fraction zeros (counted in D1), then scan the fraction digits. |
| **`DECSTR_STATE6_1`** | `0x01CBDC` | `0x01D544` | `res_pack_7.s:382`<br>`res_pack_7.s:384` | — |
| **`DECSTR_STATE6_3`** | `0x01CBE4` | `0x01D54C` | `res_pack_7.s:388`<br>`res_pack_7.s:390` | DECSTR_STATE6_3: a fraction zero before the first nonzero digit. |
| **`DECSTR_STATE7`** | `0x01CBEE` | `0x01D556` | `res_pack_7.s:395`<br>`res_pack_7.s:397` | DECSTR_STATE7: fraction digits, each counted in D1. |
| **`DECSTR_STATE75`** | `0x01CBF6` | `0x01D55E` | `res_pack_7.s:400`<br>`res_pack_7.s:402` | — |
| **`DECSTR_STATE8`** | `0x01CBFC` | `0x01D564` | `res_pack_7.s:407`<br>`res_pack_7.s:409` | DECSTR_STATE8: optional exponent -- 'E' or 'e', optional sign, digits; magnitudes from 8192 ($2000) up are held at 8192, which overflows anyway. D6 keeps the position of the 'E' in case no digits foll... |
| **`DECSTR_STATE8_1`** | `0x01CC0C` | `0x01D574` | `res_pack_7.s:415`<br>`res_pack_7.s:417` | exponent sign |
| **`DECSTR_STATE8_13`** | `0x01CC42` | `0x01D5AA` | `res_pack_7.s:437`<br>`res_pack_7.s:439` | — |
| **`DECSTR_STATE8_15`** | `0x01CC44` | `0x01D5AC` | `res_pack_7.s:442`<br>`res_pack_7.s:444` | DECSTR_STATE8_15 (Apple @15): end of the exponent -- without digits back up to the 'E'. |
| **`DECSTR_STATE8_3`** | `0x01CC1E` | `0x01D586` | `res_pack_7.s:422`<br>`res_pack_7.s:424` | — |
| **`DECSTR_STATE8_7`** | `0x01CC20` | `0x01D588` | `res_pack_7.s:425`<br>`res_pack_7.s:427` | exponent digits: D5 := D5 * 10 + digit, at most 8192 |
| **`DECSTR_STATE99`** | `0x01CCA2` | `0x01D60A` | `res_pack_7.s:499`<br>`res_pack_7.s:501` | DECSTR_STATE99: no digits -- $B0 (the infinity sign), "INF", or "NaN" with an optional decimal code in parentheses; partial matches back up to the fallback pointer. |
| **`DECSTR_STATE99_51`** | `0x01CCE6` | `0x01D64E` | `res_pack_7.s:521`<br>`res_pack_7.s:523` | — |
| **`DECSTR_STATE99_57`** | `0x01CCFE` | `0x01D666` | `res_pack_7.s:533`<br>`res_pack_7.s:535` | DECSTR_STATE99_57: NaN code digits read -- require ')', then store the low byte of the code as two hex digits after 'N'. |
| **`DECSTR_STATEBACKUP`** | `0x01CD12` | `0x01D67A` | `res_pack_7.s:547`<br>`res_pack_7.s:549` | DECSTR_STATEBACKUP -- the scan went past the last valid number: resume at the fallback pointer D6 and end there. Called by: DECSTR_STATE99, DECSTR_STATEINF, DECSTR_STATE2_1, DECSTR_GETCHAR_5, DECSTR_S... |
| **`DECSTR_STATEFIN`** | `0x01CC7E` | `0x01D5E6` | `res_pack_7.s:483`<br>`res_pack_7.s:485` | DECSTR_STATEFIN: store index and validPrefix, restore the registers, pop the parameters and return. Called by: DECSTR_STNUM2, DECSTR_INF_3, DECSTR_INF_3_1, DECSTR_INF_3_3 |
| **`DECSTR_STATEINF`** | `0x01CD18` | `0x01D680` | `res_pack_7.s:552`<br>`res_pack_7.s:554` | DECSTR_STATEINF: 'I' read -- "INF" (any case) is infinity. |
| **`DECSTR_STATENUM`** | `0x01CC4A` | `0x01D5B2` | `res_pack_7.s:449`<br>`res_pack_7.s:451` | DECSTR_STATENUM -- the first character after the number has been read: back up over it; store '0' for a zero, strip trailing zeros from d.sig, set d.exp; then DECSTR_STATEFIN. Called by: DECSTR_STATE2... |
| **`DECSTR_STNUM2`** | `0x01CC4C` | `0x01D5B4` | `res_pack_7.s:451`<br>`res_pack_7.s:453` | — |
| **`DECSTR_STNUM2_1`** | `0x01CC5A` | `0x01D5C2` | `res_pack_7.s:461`<br>`res_pack_7.s:463` | DECSTR_STNUM2_1: nonzero number -- apply the exponent sign, strip trailing zeros from d.sig (each one exponent + 1, except the lost-digit 20th). |
| **`DECSTR_STNUM2_3`** | `0x01CC60` | `0x01D5C8` | `res_pack_7.s:465`<br>`res_pack_7.s:467` | — |
| **`DECSTR_STNUM2_4`** | `0x01CC72` | `0x01D5DA` | `res_pack_7.s:472`<br>`res_pack_7.s:474` | — |
| **`DECSTR_STNUM2_5`** | `0x01CC74` | `0x01D5DC` | `res_pack_7.s:476`<br>`res_pack_7.s:478` | DECSTR_STNUM2_5: d.sig length := D2.B, d.exp := exponent + D1. |
| **`DETACHPH`** | `0x01A958` | `0x033490` | `res_drvr_mpp.s:522`<br>`res_drvr_mpp.s:715` | DetachPH (csCode 244): remove LAP type protType from the protocol table.  lapProtErr if not attached. |
| **`DETACHPH_LOOP`** | `0x01A95C` | `0x033494` | `res_drvr_mpp.s:525`<br>`res_drvr_mpp.s:718` | — |
| **`DISKFMTTBL`** | — | — | `res_drvr_sony_fdhd.s:847` | DiskFmtTbl -- the possible floppy formats, 8 bytes each: number of blocks (long); characteristics byte (bit 7 = track/side/sector counts valid, bit 6 = current format, set by PassportSts, bit 4 = doub... |
| **`DISKFMTTBL_1440K`** | — | — | `res_drvr_sony_fdhd.s:857` | — |
| **`DISPSETUP`** | `0x017D90` | `0x0346E0` | `res_drvr_sony.s:144`<br>`res_drvr_sony_fdhd.s:281` | DispSetUp -- convert word offsets into absolute jump vectors. A0 (in/out) -- next offset in the table A1 (in/out) -- next jump vector D0 (in)     -- base address the offsets are relative to D1 (in)   ... |
| **`Driver_AIn`** | `0x01B70C` | `0x031BE8` | `res_serd.s:200`<br>`res_serd.s:224` | DRVR headers. drvrFlags $4D00 (input) = dNeedLock + dStatEnable + dCtlEnable + dReadEnable; $4E00 (output) = the same with dWritEnable. No periodic action, no event mask, no menu. The routine offsets ... |
| **`Driver_AOut`** | `0x01B724` | `0x031C00` | `res_serd.s:215`<br>`res_serd.s:238` | .AOut -- modem port output driver |
| **`Driver_ATP`** | — | `0x0324AA` | `res_drvr_atp.s:127` | DRVR header (Inside Macintosh II-188): flags, delay, event mask, menu, the offsets of the five entry points from the start of the header, the driver name; then the version byte (46, also stored by the... |
| **`Driver_BIn`** | `0x01B73C` | `0x031C18` | `res_serd.s:229`<br>`res_serd.s:251` | .BIn -- printer port input driver |
| **`Driver_BOut`** | `0x01B754` | `0x031C30` | `res_serd.s:244`<br>`res_serd.s:265` | .BOut -- printer port output driver |
| **`Driver_MPP`** | — | `0x03312A` | `res_drvr_mpp.s:142` | DRVR header (Inside Macintosh II-188): flags, delay, event mask, menu, the offsets of the five entry points from the start of the header, the driver name; then the version byte (48, also stored by the... |
| **`Driver_Sony`** | — | `0x034680` | `res_drvr_sony_fdhd.s:198` | DRVR header (Inside Macintosh II-188): flags, delay, event mask, menu, the offsets of the five entry points from the start of the header, and the driver name. |
| **`Driver_Sound`** | — | `0x036C90` | `res_drvr_sound.s:128` | Driver header (IM II-188): flags, delay, event mask, menu, the offsets of the five routines and the driver name. |
| **`Driver_XPP`** | — | `0x037028` | `res_drvr_xpp.s:333` | DRVR header (Inside Macintosh II-188): flags, delay, event mask, menu, the offsets of the five entry points, the name and the version. |
| **`DRVVAROFS`** | `0x01859E` | `0x034F3C` | `res_drvr_sony.s:1135`<br>`res_drvr_sony_fdhd.s:1543` | DrvVarOS -- offset of each drive's variables in SonyVars, indexed with drive number * 2 (hence DRVVAROFS-2 in GetDrv1). The seventh entry serves the pass-thru probe in DiskOpen, which selects drive 7. |
| **`DT_Sony_NiblTbl`** | `0x01908A` | `0x035F6E` | `res_drvr_sony.s:2730`<br>`res_drvr_sony_fdhd.s:2845` | Nibl -- 6-bit value -> disk nibble: the 64 bytes with bit 7 set, no more than one pair of adjacent 0 bits and two adjacent 1 bits in bits 0-6 (the SWIM Chip User's Ref, "GCR Encoding", states only the... |
| **`DT_Sony_SectorAdrTbl`** | `0x018BDE` | `0x035AC0` | `res_drvr_sony.s:2073`<br>`res_drvr_sony.s:2711` | AdrMks -- address mark $D5 $AA $96, slip marks $DE $AA, then $FF |
| **`DT_Sony_SpeedCheckTbl`** | `0x0189D0` | `0x0353C4` | `res_drvr_sony.s:1771`<br>`res_drvr_sony_fdhd.s:2295` | SpeedCheckTbl -- speed value limits of the five zones (upper, lower; +-2% around the zone's speed). A speed value is 2^29 / (VIA timer counts per revolution) = 11.42 * rpm (VIA timer at 783.36 kHz); G... |
| **`E_ABIn_Close`** | `0x01B9D8` | `0x031F0A` | `res_serd.s:614`<br>`res_serd.s:683` | E_ABIn_Close -- Close of .AIn/.BIn (nothing to do) and the end of the output Close. |
| **`E_AIn_Open`** | `0x01B76C` | `0x031C48` | `res_serd.s:262`<br>`res_serd.s:283` | E_AIn_Open / E_BIn_Open -- Open of an input driver: check the port, note the DCE (A1) in SerialVars+4 / +12 for the receive interrupt code, set the driver version. The SCC and the variables are set up... |
| **`E_AIn_Prime`** | `0x01BCBC` | `0x032226` | `res_serd.s:1118`<br>`res_serd.s:1213` | E_AIn_Prime / E_BIn_Prime -- Read (Prime) of .AIn / .BIn. SERD_READ: pass characters from the input buffer to the read (JStash) until it is satisfied (-> IODone) or the buffer is empty; then rdPend is... |
| **`E_AInOut_Control`** | `0x01BA4C` | `0x031F86` | `res_serd.s:689`<br>`res_serd.s:763` | E_AInOut_Control / E_BInOut_Control -- Control of both drivers of port A / B. SERD_CONTROL: csCode 1 (KillIO) is handled inline and returns directly; csCodes 8-27 go through SERD_CTL_TBL with A0 -> cs... |
| **`E_AInOut_Status`** | `0x01BA06` | `0x031F34` | `res_serd.s:646`<br>`res_serd.s:713` | E_AInOut_Status / E_BInOut_Status -- Status of both drivers of port A / B. SERD_STATUS: csCode 2 SerGetBuf, csCode 8 SerStatus; statusErr for other codes or a closed port (no SERDVars). Saves ioTrap, ... |
| **`E_AOut_Close`** | `0x01B970` | `0x031E90` | `res_serd.s:566`<br>`res_serd.s:627` | E_AOut_Close / E_BOut_Close -- Close of an output driver: remove the poll procedure (port A), then SERD_OUTCLOSE with A4 = the channel's Lvl2DT Tx slot, A5 = its ExtStsDT slot, A6 = its SerialVars poi... |
| **`E_AOut_Open`** | `0x01B7C6` | `0x031CAC` | `res_serd.s:340`<br>`res_serd.s:370` | E_AOut_Open / E_BOut_Open -- Open of an output driver. Check the port, then push the handler addresses for SERD_OUTOPEN (in the order it pops them: ExtStsDT slot, ext/status handler, Lvl2DT slot, Tx, ... |
| **`E_AOut_Prime`** | `0x01BC02` | `0x03216C` | `res_serd.s:983`<br>`res_serd.s:1078` | E_AOut_Prime / E_BOut_Prime -- Write (Prime) of .AOut / .BOut. SERD_WRITE: mark the write in progress and send its first character unless output is held; the Tx interrupt sends the others (SERD_TXINT ... |
| **`E_ATP_Close`** | `0x019E8E` | `0x0325E4` | `res_drvr_atp.s:188`<br>`res_drvr_atp.s:289` | .ATP Close: waits for a free CB, closes the sockets of all request slots and responding sockets (CloseSkt calls to .MPP), then removes the VBL task and frees ATPVars.  When the .MPP Close has set the ... |
| **`E_ATP_CLOSE_EXIT`** | `0x019ED6` | `0x03262E` | `res_drvr_atp.s:223`<br>`res_drvr_atp.s:324` | — |
| **`E_ATP_CLOSE_FREE`** | `0x019EBE` | `0x032616` | `res_drvr_atp.s:214`<br>`res_drvr_atp.s:315` | remove the VBL task, free ATPVars |
| **`E_ATP_CLOSE_WAITCB`** | `0x019E9E` | `0x0325F4` | `res_drvr_atp.s:196`<br>`res_drvr_atp.s:297` | wait until a CB is free (outstanding .MPP calls complete meanwhile) |
| **`E_ATP_CLOSE_WAITREQ`** | `0x019EAA` | `0x032602` | `res_drvr_atp.s:203`<br>`res_drvr_atp.s:304` | close the sockets of the request slots |
| **`E_ATP_CLOSE_WAITRSP`** | `0x019EB8` | `0x032610` | `res_drvr_atp.s:210`<br>`res_drvr_atp.s:311` | close the responding sockets |
| **`E_ATP_Control`** | `0x019E06` | `0x032542` | `res_drvr_atp.s:122`<br>`res_drvr_atp.s:210` | E_ATP_Control .ATP Control: A0 = parameter block, A1 = .ATP DCE.  Dispatches csCode 249..256 through E_ATP_CONTROL_DISPATCH_TBL with A2 = ATPVars, D1.B = atpSocket, D2 = slot index of the responding s... |
| **`E_ATP_CONTROL_CSCODE`** | `0x019E12` | `0x032570` | `res_drvr_atp.s:129`<br>`res_drvr_atp.s:230` | dispatch on csCode |
| **`E_ATP_CONTROL_DISPATCH_TBL`** | `0x019E6E` | `0x0325CE` | `res_drvr_atp.s:168`<br>`res_drvr_atp.s:269` | E_ATP_CONTROL_DISPATCH_TBL - csCode 249..256, offsets from _DRVR_10_.ATP |
| **`E_ATP_CONTROL_EXIT`** | `0x019E8A` | — | `res_drvr_atp.s:178` | — |
| **`E_ATP_CONTROL_GOODBYE`** | `0x019E7E` | — | `res_drvr_atp.s:174` | negative csCode (goodbye kiss): close .ATP only when MemTop < $30000 (a 128K Mac, where the RAM-based .ATP lived in the application heap) |
| **`E_ATP_CONTROL_IODONE`** | `0x019E0E` | `0x03256C` | `res_drvr_atp.s:126`<br>`res_drvr_atp.s:227` | — |
| **`E_ATP_CONTROL_JUMP`** | `0x019E62` | `0x0325C2` | `res_drvr_atp.s:162`<br>`res_drvr_atp.s:263` | — |
| **`E_ATP_CONTROL_NOHOOK`** | — | `0x032564` | `res_drvr_atp.s:223` | — |
| **`E_ATP_CONTROL_RANGE`** | `0x019E1E` | `0x03257A` | `res_drvr_atp.s:136`<br>`res_drvr_atp.s:236` | csCode must be 249..256 |
| **`E_ATP_CONTROL_SKTLOOP`** | `0x019E58` | `0x0325B6` | `res_drvr_atp.s:158`<br>`res_drvr_atp.s:259` | handler address from the dispatch table |
| **`E_ATP_Open`** | `0x019DB8` | `0x0324C4` | `res_drvr_atp.s:81`<br>`res_drvr_atp.s:152` | Name end of Name .ATP Open: needs an open .MPP (ABusVars set); allocates ATPVars and installs the once-per-second VBL task.  A1 = .ATP DCE. |
| **`E_ATP_OPEN_CHECK`** | `0x019DD0` | — | `res_drvr_atp.s:93` | allocate ATPVars E_ATP_OPEN_CHECK - test the result of _NewPtrSysClear |
| **`E_ATP_OPEN_EXIT`** | `0x019E04` | `0x032540` | `res_drvr_atp.s:111`<br>`res_drvr_atp.s:197` | initialize DCE pointer, TID seed and VBL task in ATPVars |
| **`E_ATP_OPEN_SPEED`** | — | `0x032518` | `res_drvr_atp.s:183` | NSendRequest limit per socket = (factor * 120 - 142) / 48: 9 for 5, 14 for 7 (SE), 62 for 26 (Mac II), as listed in IM V-519 |
| **`E_ATP_PrimeStatus`** | `0x019F70` | `0x0326D6` | `res_drvr_atp.s:321`<br>`res_drvr_atp.s:430` | .ATP Prime and Status: not supported - clear drvrActive and return without completing the call |
| **`E_BIn_Open`** | `0x01B774` | `0x031C50` | `res_serd.s:269`<br>`res_serd.s:290` | E_BIn_Open -- Open of .BIn (see E_AIn_Open). |
| **`E_BIn_Prime`** | `0x01BCC2` | `0x03222C` | `res_serd.s:1124`<br>`res_serd.s:1219` | E_BIn_Prime -- Read of .BIn (see E_AIn_Prime). |
| **`E_BInOut_Control`** | `0x01BA52` | `0x031F8C` | `res_serd.s:695`<br>`res_serd.s:769` | E_BInOut_Control -- Control of port B (see E_AInOut_Control). |
| **`E_BInOut_Status`** | `0x01BA0C` | `0x031F3A` | `res_serd.s:652`<br>`res_serd.s:719` | E_BInOut_Status -- Status of port B (see E_AInOut_Status). |
| **`E_BOut_Close`** | `0x01B984` | `0x031EA4` | `res_serd.s:576`<br>`res_serd.s:637` | E_BOut_Close -- Close of .BOut (see E_AOut_Close). |
| **`E_BOut_Open`** | `0x01B7F4` | `0x031CDA` | `res_serd.s:358`<br>`res_serd.s:388` | E_BOut_Open -- Open of .BOut (see E_AOut_Open); no poll procedure. |
| **`E_BOut_Prime`** | `0x01BC08` | `0x032172` | `res_serd.s:989`<br>`res_serd.s:1084` | E_BOut_Prime -- Write of .BOut (see E_AOut_Prime). |
| **`E_MPP_Close`** | `0x01AE6E` | `0x033B34` | `res_drvr_mpp.s:1379`<br>`res_drvr_mpp.s:1706` | E_MPP_Close .MPP Close: closes .ATP (atpVars flag set first), resets SCC channel B (mouse interrupt kept), removes the VBL task and the interrupt handlers, gives units 7/8 (.BIn/.BOut) back and frees ... |
| **`E_MPP_CLOSE_BIN`** | `0x01AEC4` | `0x033B90` | `res_drvr_mpp.s:1409`<br>`res_drvr_mpp.s:1740` | close .ATP SCC, VBL task, interrupt handlers give units 8 (.BOut) and 7 (.BIn) back |
| **`E_MPP_CLOSE_EXIT`** | `0x01AED8` | `0x033BBE` | `res_drvr_mpp.s:1419`<br>`res_drvr_mpp.s:1762` | — |
| **`E_MPP_CLOSE_FREE`** | `0x01AECE` | `0x033B9A` | `res_drvr_mpp.s:1413`<br>`res_drvr_mpp.s:1745` | free the blocks |
| **`E_MPP_CLOSE_PORT`** | `0x01AED4` | `0x033BBA` | `res_drvr_mpp.s:1417`<br>`res_drvr_mpp.s:1760` | — |
| **`E_MPP_CLOSE_VARS`** | — | `0x033BB6` | `res_drvr_mpp.s:1757` | — |
| **`E_MPP_Control`** | `0x01A714` | `0x033144` | `res_drvr_mpp.s:88`<br>`res_drvr_mpp.s:167` | Name end of Name .MPP Control: A0 = parameter block, A1 = .MPP DCE.  Calls the AtalkHk1 hook, then dispatches with A2 = MPP variables, D1.B = csParam+0 (socket / protType / interval), A1 = csParam+2 (... |
| **`E_MPP_CONTROL_CSCODE`** | `0x01A72C` | `0x03315C` | `res_drvr_mpp.s:100`<br>`res_drvr_mpp.s:179` | dispatch on csCode |
| **`E_MPP_CONTROL_DISPATCH_TBL`** | `0x01A76A` | — | `res_drvr_mpp.s:129` | common arguments; 242..249 are resident, 250..255 are NBP calls 242..249 through the dispatch table E_MPP_CONTROL_DISPATCH_TBL - csCode 242..249, offsets from _DRVR_9_.MPP |
| **`E_MPP_CONTROL_DONE`** | `0x01A79C` | `0x0331CA` | `res_drvr_mpp.s:164`<br>`res_drvr_mpp.s:250` | Called by: E_MPP_CONTROL_GOODBYE, LOOKUPREPLY, CLOSESKT (via CLOSESKT_DONE: OPENSKT, WRITEDDP) |
| **`E_MPP_CONTROL_GOODBYE`** | `0x01A77A` | `0x0331AA` | `res_drvr_mpp.s:135`<br>`res_drvr_mpp.s:221` | negative csCode (goodbye kiss): if the NIS is open, LUCODE+2 drops the names in the application heap; then on to the NBP code (with D3 < 0) |
| **`E_MPP_CONTROL_GOODBYE_DONE`** | — | `0x0331B6` | `res_drvr_mpp.s:226` | — |
| **`E_MPP_CONTROL_NBP`** | `0x01A786` | `0x0331B8` | `res_drvr_mpp.s:141`<br>`res_drvr_mpp.s:229` | csCode 250..255 (and the goodbye kiss): to the NBP code via NRPtr |
| **`E_MPP_CONTROL_NOHOOK`** | `0x01A71E` | `0x03314E` | `res_drvr_mpp.s:93`<br>`res_drvr_mpp.s:172` | — |
| **`E_MPP_CONTROL_RANGE`** | `0x01A738` | `0x033168` | `res_drvr_mpp.s:108`<br>`res_drvr_mpp.s:187` | csCode 1 (killCode) csCode must be 242..255 |
| **`E_MPP_CONTROL_TBL`** | — | `0x03319A` | `res_drvr_mpp.s:208` | common arguments; 242..249 are resident, 250..256 are NBP calls 242..249 through the dispatch table E_MPP_CONTROL_TBL - csCode 242..249, offsets from Driver_MPP |
| **`E_MPP_Open`** | `0x01AEF6` | `0x033BDC` | `res_drvr_mpp.s:1453`<br>`res_drvr_mpp.s:1796` | .MPP Open: port B must be free (PortBUse < 0) and configured for AppleTalk or unconfigured (SPConfig); allocates the variables, takes units 7/8 (.BIn/.BOut, if not opened) out of the unit table, sets ... |
| **`E_MPP_OPEN_BIN`** | `0x01AF46` | `0x033C48` | `res_drvr_mpp.s:1484`<br>`res_drvr_mpp.s:1836` | SPConfig: port B use type must be useFree (0) or useATalk (1) allocate the MPP variables initialize take unit 8 (.BOut) out of the unit table unless it has been opened the same for unit 7 (.BIn) |
| **`E_MPP_OPEN_CHKNODE`** | — | `0x033D28` | `res_drvr_mpp.s:1922` | SCC channel B vectors; the old ones go to SaveVects VBL task node ID: the hint in PRAM unless 0 or $FF, else random in the range of bit 7 of SPATalkB |
| **`E_MPP_OPEN_CLAIM`** | — | `0x033D4E` | `res_drvr_mpp.s:1941` | — |
| **`E_MPP_OPEN_DONE`** | `0x01B08A` | `0x033E3E` | `res_drvr_mpp.s:1597`<br>`res_drvr_mpp.s:2018` | open .ATP |
| **`E_MPP_OPEN_ENQLOOP`** | `0x01AFFC` | `0x033D62` | `res_drvr_mpp.s:1548`<br>`res_drvr_mpp.s:1948` | claim it: 20 rounds of lapENQ to that address must stay unanswered |
| **`E_MPP_OPEN_ENQWAIT`** | `0x01B006` | `0x033D6C` | `res_drvr_mpp.s:1552`<br>`res_drvr_mpp.s:1952` | — |
| **`E_MPP_OPEN_OLDTIMES`** | — | `0x033CD2` | `res_drvr_mpp.s:1891` | — |
| **`E_MPP_OPEN_PHLOOP`** | `0x01AF60` | `0x033C68` | `res_drvr_mpp.s:1496`<br>`res_drvr_mpp.s:1849` | — |
| **`E_MPP_OPEN_PHTBL`** | `0x01AF5E` | `0x033C60` | `res_drvr_mpp.s:1494`<br>`res_drvr_mpp.s:1846` | all 4 LAP protocol table entries free |
| **`E_MPP_OPEN_PORT`** | — | `0x033BF8` | `res_drvr_mpp.s:1805` | — |
| **`E_MPP_OPEN_PTRS`** | — | `0x033E08` | `res_drvr_mpp.s:2000` | JDDPWrite and LookupPtr (bit 31 clear: NIS opened by the first RegisterName) |
| **`E_MPP_OPEN_RANDOM`** | `0x01AFDC` | `0x033D32` | `res_drvr_mpp.s:1535`<br>`res_drvr_mpp.s:1927` | — |
| **`E_MPP_OPEN_SCCTIME`** | — | `0x033CCC` | `res_drvr_mpp.s:1888` | — |
| **`E_MPP_OPEN_TIMELOOP`** | — | `0x033CAC` | `res_drvr_mpp.s:1872` | LAP configuration from MPP_CONFIG_TBL the 8 timing loop counts (VAbortWait .. VWait100): computed from the CPU speed on ROMs >= $76, else copied from MPP_CONFIG_TBL count = (time - cycles / MHz) * loo... |
| **`E_MPP_OPEN_TIMESTORE`** | — | `0x033CBE` | `res_drvr_mpp.s:1881` | — |
| **`E_MPP_OPEN_TRYNODE`** | `0x01AFE0` | `0x033D46` | `res_drvr_mpp.s:1537`<br>`res_drvr_mpp.s:1936` | claim it: 20 (workstation) or 120 (server) rounds of lapENQ to that address must stay unanswered |
| **`E_MPP_OPEN_VECTORS`** | — | `0x033CD4` | `res_drvr_mpp.s:1894` | install the interrupt handlers and the VBL task, set up the SCC |
| **`E_MPP_OPEN_WSNODE`** | — | `0x033BF2` | `res_drvr_mpp.s:1803` | — |
| **`E_MPP_Prime`** | `0x01A98A` | `0x0334EA` | `res_drvr_mpp.s:567`<br>`res_drvr_mpp.s:775` | .MPP Prime: not supported - clear drvrActive and return without completing the call |
| **`E_MPP_Status`** | `0x01A97E` | `0x0334B6` | `res_drvr_mpp.s:552`<br>`res_drvr_mpp.s:745` | E_MPP_Status .MPP Status: no status calls - statusErr |
| **`E_MPP_STATUS_LOOP`** | — | `0x0334D6` | `res_drvr_mpp.s:756` | — |
| **`E_Sony_Close`** | `0x017D48` | `0x034698` | `res_drvr_sony.s:89`<br>`res_drvr_sony_fdhd.s:216` | DiskClose -- the driver cannot be closed: return closErr. |
| **`E_Sony_Control`** | `0x017F12` | `0x034876` | `res_drvr_sony.s:344`<br>`res_drvr_sony_fdhd.s:505` | DiskControl -- driver control entry: jump through the JControl vector. |
| **`E_Sony_DCDReset`** | `0x019C66` | `0x036B44` | `res_drvr_sony.s:4235`<br>`res_drvr_sony_fdhd.s:4897` | DCDReset -- jump through the JDCDReset vector |
| **`E_Sony_FigTrkSpd`** | `0x018A8A` | `0x03547E` | `res_drvr_sony.s:1879`<br>`res_drvr_sony_fdhd.s:2406` | E_Sony_FigTrkSpd -- measure the time of 15 tach pulses (through the JFigTrkSpd vector) |
| **`E_Sony_MakeSpdTbl`** | `0x0189E4` | `0x0353D8` | `res_drvr_sony.s:1783`<br>`res_drvr_sony_fdhd.s:2312` | MakeSpdTbl -- the speed codes of the five zones (TrkSpeedTbl) of a 400K drive; a new-interface drive only gets 800 ms to seat the disk. D0 (out) -- 0 or an error (-1 / noDriveErr: no tachometer pulses... |
| **`E_Sony_Open`** | `0x017D9E` | `0x0346EE` | `res_drvr_sony.s:164`<br>`res_drvr_sony_fdhd.s:312` | DiskOpen -- driver initialization (called once at boot, A1 = DCE) Allocates the $310-byte SonyVars block, sets up the disk routine vectors and the tuneable constants, installs the VBL task (disk-in- p... |
| **`E_SONY_OPEN_CONT`** | `0x017E38` | `0x03479E` | `res_drvr_sony.s:218`<br>`res_drvr_sony_fdhd.s:380` | — |
| **`E_SONY_OPEN_CONT_2`** | `0x017E70` | `0x0347FE` | `res_drvr_sony.s:241`<br>`res_drvr_sony_fdhd.s:428` | — |
| **`E_SONY_OPEN_LOOP`** | `0x017E20` | `0x034782` | `res_drvr_sony.s:210`<br>`res_drvr_sony_fdhd.s:370` | look for drives 1-6, install drive queue entries |
| **`E_SONY_OPEN_SELECT`** | — | `0x03479A` | `res_drvr_sony_fdhd.s:378` | — |
| **`E_SONY_OPEN_SKIP`** | `0x017E82` | `0x034812` | `res_drvr_sony.s:248`<br>`res_drvr_sony_fdhd.s:436` | — |
| **`E_SONY_OPEN_XLAT`** | — | `0x0347DA` | `res_drvr_sony_fdhd.s:415` | Swap translation table entries D2 (physical) and D5 (logical), so that logical drive D5 maps to this physical drive. For HD20 drives D5 = D2 and the swap changes nothing. |
| **`E_Sony_Prime`** | `0x01806A` | `0x034A0C` | `res_drvr_sony.s:526`<br>`res_drvr_sony_fdhd.s:903` | DiskPrime -- driver prime entry: jump through the JDiskPrime vector. |
| **`E_Sony_RdAddr`** | `0x018C18` | `0x035AFA` | `res_drvr_sony.s:2108`<br>`res_drvr_sony.s:2752` | RdAddr -- address mark table in A2, jump through the JRdAddr vector |
| **`E_Sony_RdData`** | `0x018CDE` | `0x035BC2` | `res_drvr_sony.s:2229`<br>`res_drvr_sony.s:2878` | RdData -- data mark table in A1, jump through the JRdData vector |
| **`E_Sony_Recal`** | `0x018852` | `0x035214` | `res_drvr_sony.s:1559`<br>`res_drvr_sony_fdhd.s:2011` | Recal -- recalibrate: step out to track 0 (D7 = 80: at most 79 steps) D0 (out) -- 0 or an error code, also stored as the current track Sets the IWM mode first. Returns to one level above the caller wh... |
| **`E_Sony_ReSeek`** | `0x0182DC` | `0x034C7A` | `res_drvr_sony.s:828`<br>`res_drvr_sony_fdhd.s:1218` | ReSeek -- jump through the JReSeek vector (DiskPrime part III). |
| **`E_Sony_Seek`** | `0x018718` | `0x0350DE` | `res_drvr_sony.s:1372`<br>`res_drvr_sony_fdhd.s:1813` | Seek -- seek to a track D6.W (in) -- track (bit 11 = side 1; cleared here) D0 (out)  -- result: track number, or a negative error code Sets the speed for the target zone first. Returns to one level ab... |
| **`E_Sony_SendCmd`** | `0x0196AC` | `0x03658C` | `res_drvr_sony.s:3491`<br>`res_drvr_sony_fdhd.s:4195` | SendCmd -- jump through the JSendCmd vector |
| **`E_Sony_SetUpPoll`** | `0x018BE4` | `0x035AC6` | `res_drvr_sony.s:2077`<br>`res_drvr_sony.s:2715` | SetUpPoll -- jump through the JSetUpPoll vector |
| **`E_Sony_Status`** | `0x01801C` | `0x0349BE` | `res_drvr_sony.s:487`<br>`res_drvr_sony_fdhd.s:739` | DiskStatus -- status entry; only csCode 8 (drive status) is supported: copies the first 22 bytes of the drive variables (track, write-protect, disk-in-place, installed, sides, drive queue element, two... |
| **`E_SONY_STATUS_LOOP`** | `0x018036` | — | `res_drvr_sony.s:496` | — |
| **`E_Sony_WakeUp`** | `0x0187D4` | `0x03519A` | `res_drvr_sony.s:1489`<br>`res_drvr_sony_fdhd.s:1954` | WakeUp -- jump through the JWakeUp vector Called by: SONY_CTL_EJECT, SONY_NEWDRVEJECT_LOOP, Sony_DCDReset, SONY_RESEEK_SKIP_2, SONY_CHECKNEW_WAIT (and 6 more) |
| **`E_Sony_WrData`** | `0x018F36` | `0x035E1A` | `res_drvr_sony.s:2542`<br>`res_drvr_sony_fdhd.s:2670` | WrData -- MarkTbl in A2, jump through the JWrData vector |
| **`E_Sound_Close`** | `0x0179F4` | `0x036CC4` | `res_drvr_sound.s:186`<br>`res_drvr_sound.s:166` | — |
| **`E_Sound_Control`** | `0x017A7A` | `0x036D4C` | `res_drvr_sound.s:288`<br>`res_drvr_sound.s:263` | **Regs:** `E_Sound_Control -- Control. Entry: A0 = parameter block, A1 = DCE.`<br>E_Sound_Control -- Control. Entry: A0 = parameter block, A1 = DCE. csCode 0 -> noErr; 1 or negative -> KillIO; 2 -> volume; 3 and up -> amplitude (fill the buffer with the low byte of csParam). |
| **`E_Sound_KillIO`** | `0x0179F0` | `0x036CC0` | `res_drvr_sound.s:184`<br>`res_drvr_sound.s:164` | **Regs:** `level of its first byte and release Timer 1.  Exit: D0 = noErr.`<br>E_Sound_KillIO -- Control csCode 1 (KillIO): CurPitch := 0, then as Close; returns with RTS, not through jIODone (IM II-194). New in the Plus: the 64K driver's KillIO was Close and left CurPitch. E_So... |
| **`E_Sound_Open`** | `0x0179DA` | `0x036CAA` | `res_drvr_sound.s:167`<br>`res_drvr_sound.s:148` | **Regs:** `Entry: A1 = DCE.  Exit: D0 = noErr.`<br>E_Sound_Open -- Open: remember the DCE, let the buffer hold the level of its first byte, release Timer 1 and set the speaker volume from parameter RAM. Entry: A1 = DCE.  Exit: D0 = noErr. |
| **`E_Sound_Prime`** | `0x017A9A` | `0x036D6C` | `res_drvr_sound.s:317`<br>`res_drvr_sound.s:291` | **Regs:** `E_Sound_Prime -- Write (StartSound). Entry: A0 = parameter block, A1 =`<br>E_Sound_Prime -- Write (StartSound). Entry: A0 = parameter block, A1 = DCE. Enables the sound output, then starts the synthesizer that the first word of the buffer (ioBuffer) names; returns noErr at o... |
| **`E_Sound_Status`** | `0x017A8E` | `0x036D60` | `res_drvr_sound.s:299`<br>`res_drvr_sound.s:274` | E_Sound_Status -- Status (and the end of Control): noErr through jIODone; for an immediate Control call this completes the Write that is playing (IM II-234). |
| **`E_XPP_Close`** | — | `0x0370E4` | `res_drvr_xpp.s:453` | E_XPP_Close -- driver Close. closErr while any session slot is in use; else clear xppLoadedBit and the AGB's xppVarPtr. The 48-byte variable block is not disposed of: it is lost (a later Open allocate... |
| **`E_XPP_Control`** | — | `0x037090` | `res_drvr_xpp.s:402` | E_XPP_Control -- driver Control (A0 = XPP parameter block, A1 = DCE). Calls the patch hook, then dispatches on csCode through XPP_CTL_TABLE; the handlers are entered with A0 = parameter block, A1 = DC... |
| **`E_XPP_Open`** | — | `0x037042` | `res_drvr_xpp.s:360` | E_XPP_Open -- driver Open (A1 = DCE). AppleTalk must be open on port B: PortBUse bit 7 clear (port in use) and use type useATalk in bits 0-3, else portInUse. Creates the AppleTalk Global Block if AGBH... |
| **`E_XPP_PrimeStatus`** | — | `0x037472` | `res_drvr_xpp.s:957` | E_XPP_PrimeStatus -- driver Prime and Status: never called (drvrFlags enables Control only); just clears drvrActive in dCtlFlags. XPP_RETURN: its RTS, a common return for other routines. |
| **`ELEMS_A0TOA1`** | `0x01D016` | `0x01B20A` | `res_pack_5.s:208`<br>`res_pack_5.s:209` | ELEMS_A0TOA1 -- copy the extended (10 bytes) at A0 to A1; A1 is reset to the head of the copy, A0 is left 8 bytes on. Called by: ELEMS_DSTONLY, ELEMS_LOG12R, ELEMS_LOG2R (LOG2R), ELEMS_LOGAPPROX, ELEM... |
| **`ELEMS_AGFINI`** | `0x01DC3C` | `0x01BE30` | `res_pack_5.s:1834`<br>`res_pack_5.s:1835` | ELEMS_AGFINI -- (A4) := T - RES, or pi/2 - (T - RES) if T was inverted; T is the copy on the stack. |
| **`ELEMS_AGLONGFORM`** | `0x01DBA6` | `0x01BD9A` | `res_pack_5.s:1779`<br>`res_pack_5.s:1780` | AGLONGFORM: T > ATNCONS |
| **`ELEMS_AGNOINV`** | `0x01DB7A` | `0x01BD6E` | `res_pack_5.s:1761`<br>`res_pack_5.s:1762` | AGNOINV: 0 < T <= 1 |
| **`ELEMS_AGSUBPI2`** | `0x01DC5A` | `0x01BE4E` | `res_pack_5.s:1848`<br>`res_pack_5.s:1849` | AGSUBPI2: inverted: pi/2 - (T - RES) |
| **`ELEMS_ANN0`** | `0x01D796` | `0x01B98A` | `res_pack_5.s:1274`<br>`res_pack_5.s:1275` | ANN0: +0 |
| **`ELEMS_ANNBASEE`** | `0x01D834` | `0x01BA28` | `res_pack_5.s:1351`<br>`res_pack_5.s:1352` | annbasee: tiny r, base e |
| **`ELEMS_ANNCLEAR`** | `0x01D85A` | `0x01BA4E` | `res_pack_5.s:1368`<br>`res_pack_5.s:1369` | annclear: flags of the result |
| **`ELEMS_ANNCLEAR_1`** | `0x01D872` | `0x01BA66` | `res_pack_5.s:1378`<br>`res_pack_5.s:1379` | @1: not infinite |
| **`ELEMS_ANNDOIT`** | `0x01D7F0` | `0x01B9E4` | `res_pack_5.s:1324`<br>`res_pack_5.s:1325` | ELEMS_ANNDOIT -- (1 - (1 + r)^-n) / r for finite nonzero n and r > -1, in cell X. A normal r: X := -n * log2(1 + r) and (1 + r)^-n - 1 = 2^X - 1 (FEXP21X); \|r\| < 2^-128: ln(1 + r) is about r, X := -n ... |
| **`ELEMS_ANNDOIT_1`** | `0x01D82C` | `0x01BA20` | `res_pack_5.s:1346`<br>`res_pack_5.s:1347` | @1: 2^X - 1 |
| **`ELEMS_ANNDOUT`** | `0x01D87A` | `0x01BA6E` | `res_pack_5.s:1383`<br>`res_pack_5.s:1384` | ANNDOUT: store the result |
| **`ELEMS_ANNM1`** | `0x01D78E` | `0x01B982` | `res_pack_5.s:1267`<br>`res_pack_5.s:1268` | ANNM1: -1 |
| **`ELEMS_ANNOK`** | `0x01D792` | `0x01B986` | `res_pack_5.s:1270`<br>`res_pack_5.s:1271` | ANNOK: r > -1 |
| **`ELEMS_ANNRESULT`** | `0x01D848` | `0x01BA3C` | `res_pack_5.s:1360`<br>`res_pack_5.s:1361` | annresult: X := (1 + r)^-n - 1, the opcode already pushed |
| **`ELEMS_ANNRINF`** | `0x01D7AC` | `0x01B9A0` | `res_pack_5.s:1288`<br>`res_pack_5.s:1289` | ANNRINF: r = +inf |
| **`ELEMS_ANNROK`** | `0x01D7C6` | `0x01B9BA` | `res_pack_5.s:1299`<br>`res_pack_5.s:1300` | ANNROK: r normal or denormal; n infinite? |
| **`ELEMS_ANNSPECIAL`** | `0x01D888` | `0x01BA7C` | `res_pack_5.s:1391`<br>`res_pack_5.s:1392` | ELEMS_ANNSPECIAL -- huge r and (1 + r)^-n: the annuity is -(r^-(n+1)) = -2^(-(n+1) * log2(r)); A1 -> cell X. |
| **`ELEMS_ANNSRC`** | `0x01D7A0` | `0x01B994` | `res_pack_5.s:1282`<br>`res_pack_5.s:1283` | ANNSRC: r = 0: the limit is n |
| **`ELEMS_ANNUITYTOP`** | `0x01D774` | `0x01B968` | `res_pack_5.s:1255`<br>`res_pack_5.s:1256` | ELEMS_ANNUITYTOP -- Annuity (opcode $C016): dst := (1 - (1 + r)^-n) / r, r = src2 (D5), n = src (D4). r < -1 (or unordered) is invalid: NaN code 38; r = -1: +0 for n = 0, +inf with divide by zero for ... |
| **`ELEMS_ANNXN`** | `0x01D79A` | `0x01B98E` | `res_pack_5.s:1277`<br>`res_pack_5.s:1278` | ANNXN: n <> 0; r zero or infinite? |
| **`ELEMS_AT1`** | `0x01D0EE` | `0x01B2E2` | `res_pack_5.s:384`<br>`res_pack_5.s:385` | At1: scale by the rest |
| **`ELEMS_AT11`** | `0x01D1E2` | `0x01B3D6` | `res_pack_5.s:509`<br>`res_pack_5.s:510` | At11: S = Q - 1 for LOGAPPROX, then add L |
| **`ELEMS_AT3`** | `0x01D0F0` | `0x01B2E4` | `res_pack_5.s:387`<br>`res_pack_5.s:388` | At3: J := the scale step, signed like (A1) |
| **`ELEMS_ATANGUTS`** | `0x01DB4A` | `0x01BD3E` | `res_pack_5.s:1742`<br>`res_pack_5.s:1743` | ELEMS_ATANGUTS -- (A4) := atan(T) for T > 0. T > 1 is inverted first (atan(T) = pi/2 - atan(1/T); D2 = -1). Then for T <= ATNCONS = 2 - sqrt(3) = tan(pi/12) = 0.2679: T - T * P(T*T)/Q(T*T) (ATANQ, ATA... |
| **`ELEMS_ATANQ`** | `0x01DF24` | `0x01C118` | `res_pack_5.s:1993`<br>`res_pack_5.s:1994` | ATANQ, ATANP: Q and P of ATANGUTS (atn8.text, 17 May 83) |
| **`ELEMS_ATANTOP`** | `0x01DB22` | `0x01BD16` | `res_pack_5.s:1712`<br>`res_pack_5.s:1713` | ELEMS_ATANTOP -- atan(x) (opcode $1E) for any x: atan(+-0) = +-0, atan(+-inf) = +-pi/2; else atan(-T) = -atan(T) and ATANGUTS for \|T\|. D1 = class - FCINF, its bit 15 the sign of x. Uses A0-A2, D0-D2. |
| **`ELEMS_ATFINITE`** | `0x01DB36` | `0x01BD2A` | `res_pack_5.s:1722`<br>`res_pack_5.s:1723` | ATFINITE |
| **`ELEMS_ATHARD`** | `0x01DB3C` | `0x01BD30` | `res_pack_5.s:1728`<br>`res_pack_5.s:1729` | ATHARD: finite, nonzero |
| **`ELEMS_ATQUICK`** | `0x01DB38` | `0x01BD2C` | `res_pack_5.s:1725`<br>`res_pack_5.s:1726` | ATQUICK |
| **`ELEMS_CGBIG`** | `0x01D9E8` | `0x01BBDC` | `res_pack_5.s:1573`<br>`res_pack_5.s:1574` | CGBIG: S > 1/4: the long form |
| **`ELEMS_CLASSCOM`** | `0x01CF76` | `0x01B16A` | `res_pack_5.s:109`<br>`res_pack_5.s:110` | CLASSCOM: classify the src |
| **`ELEMS_CLASSDSTORSRC2`** | `0x01CFB0` | `0x01B1A4` | `res_pack_5.s:148`<br>`res_pack_5.s:149` | CLASSDSTORSRC2: classify dst or src2, save the environment |
| **`ELEMS_CLASSIFY`** | `0x01CF8A` | `0x01B17E` | `res_pack_5.s:127`<br>`res_pack_5.s:128` | ELEMS_CLASSIFY -- class of the extended at A0 (FCLASSX): D0.B = 1 signaling NaN, 2 quiet NaN, 3 infinity, 4 zero, 5 normal, 6 denormal; D0 bit 15 = the operand's sign. Uses cell I. |
| **`ELEMS_CLASSIFY_1`** | `0x01CFA2` | `0x01B196` | `res_pack_5.s:136`<br>`res_pack_5.s:137` | — |
| **`ELEMS_CLASSSKIP`** | `0x01CF7C` | `0x01B170` | `res_pack_5.s:114`<br>`res_pack_5.s:115` | CLASSSKIP |
| **`ELEMS_CLEAREXIT`** | `0x01D06E` | `0x01B262` | `res_pack_5.s:282`<br>`res_pack_5.s:283` | CLEAREXIT: shared exit of CLEARX, FORCEX, TESTX |
| **`ELEMS_CLEARINEXACT`** | `0x01D058` | `0x01B24C` | `res_pack_5.s:269`<br>`res_pack_5.s:270` | CLEARINEXACT Called by: ELEMS_SPLIT2, ELEMS_SPLIT, ELEMS_XPWRY9ERR (XPWRY9ERR), ELEMS_NEGPWRY, ELEMS_XPWRYOK |
| **`ELEMS_CLEARINVALID`** | `0x01D054` | `0x01B248` | `res_pack_5.s:263`<br>`res_pack_5.s:264` | CLEARINVALID |
| **`ELEMS_CLEAROFLOW`** | `0x01D050` | `0x01B244` | `res_pack_5.s:259`<br>`res_pack_5.s:260` | CLEAROFLOW Called by: ELEMS_EXPR, ELEMS_EXP1R, ELEMS_XPWRK, ELEMS_ANNDOIT |
| **`ELEMS_CLEARUFLOW`** | `0x01D04C` | `0x01B240` | `res_pack_5.s:253`<br>`res_pack_5.s:254` | ELEMS_CLEARUFLOW, ELEMS_CLEAROFLOW, ELEMS_CLEARINVALID (CLEARINVALID), ELEMS_CLEARINEXACT -- clear one exception flag: get the environment, clear the flag bit (FB* numbers: bits of the high byte), set... |
| **`ELEMS_CLEARX`** | `0x01D05A` | `0x01B24E` | `res_pack_5.s:272`<br>`res_pack_5.s:273` | CLEARX: clear flag D0 |
| **`ELEMS_CMPBASEE`** | `0x01D74A` | `0x01B93E` | `res_pack_5.s:1226`<br>`res_pack_5.s:1227` | cmpbasee: tiny r: e^(n * r) |
| **`ELEMS_CMPGTM1`** | `0x01D706` | `0x01B8FA` | `res_pack_5.s:1197`<br>`res_pack_5.s:1198` | CMPGTM1: r > -1 |
| **`ELEMS_CMPM1N`** | `0x01D6FA` | `0x01B8EE` | `res_pack_5.s:1189`<br>`res_pack_5.s:1190` | CMPM1N: r = -1, n <> 0 |
| **`ELEMS_CMPRESULT`** | `0x01D75A` | `0x01B94E` | `res_pack_5.s:1234`<br>`res_pack_5.s:1235` | cmpresult: X := 2^X or e^X, the opcode already pushed |
| **`ELEMS_CMPTOFIN`** | `0x01D718` | `0x01B90C` | `res_pack_5.s:1207`<br>`res_pack_5.s:1208` | CMPTOFIN: (1 + reasonable r)^finite n |
| **`ELEMS_CMPTOZERO`** | `0x01D6F6` | `0x01B8EA` | `res_pack_5.s:1186`<br>`res_pack_5.s:1187` | CMPTOZERO: (1 + r)^0 = 1 |
| **`ELEMS_CMPZERO`** | `0x01D702` | `0x01B8F6` | `res_pack_5.s:1194`<br>`res_pack_5.s:1195` | CMPZERO |
| **`ELEMS_COMPOUNDTOP`** | `0x01D6DE` | `0x01B8D2` | `res_pack_5.s:1176`<br>`res_pack_5.s:1177` | ELEMS_COMPOUNDTOP -- Compound (opcode $C014): dst := (1 + r)^n, r = src2 (D5), n = src (D4). r < -1 (or unordered) is invalid: NaN code 38 (NANFINAN); n = 0 gives 1; r = 0 with an infinite n is invali... |
| **`ELEMS_COSGUTS`** | `0x01D9A2` | `0x01BB96` | `res_pack_5.s:1545`<br>`res_pack_5.s:1546` | ELEMS_COSGUTS -- (A4) := cos(T) for \|T\| <= pi/4, S = T*T: for S <= 1/4, 1 - S/2 + S*S * P(S)/Q(S); else, with Z = \|T\| - 1/2, 7/8 - (Z/2 + (Z*Z/2 - S*S * P(S)/Q(S))), the same value with less rounding ... |
| **`ELEMS_COSQ`** | `0x01DE7C` | `0x01C070` | `res_pack_5.s:1969`<br>`res_pack_5.s:1970` | COSQ, COSP: Q and P of COSGUTS (cs7.text, 14 May 83) |
| **`ELEMS_COSTOP`** | `0x01D920` | `0x01BB14` | `res_pack_5.s:1467`<br>`res_pack_5.s:1468` | ELEMS_COSTOP -- cos(x) (opcode $1A): cos(+-0) = 1, cos(+-inf) is invalid (NaN code 33); otherwise the sin code with the quotient adjusted by 1, as cos(T) = sin(T + pi/2): q mod 2 selects cos (0) or si... |
| **`ELEMS_DIVM0STUFF`** | `0x01D2CE` | `0x01B4C2` | `res_pack_5.s:634`<br>`res_pack_5.s:635` | DIVM0STUFF: divide by zero, -inf |
| **`ELEMS_DIVP0STUFF`** | `0x01D2C4` | `0x01B4B8` | `res_pack_5.s:625`<br>`res_pack_5.s:626` | DIVP0STUFF: divide by zero, +inf |
| **`ELEMS_DSTONLY`** | `0x01CFA4` | `0x01B198` | `res_pack_5.s:141`<br>`res_pack_5.s:142` | ELEMS_DSTONLY -- one address (bit 15 of the opcode clear): the logarithms, exponentials, trig functions and RandomX. |
| **`ELEMS_ELEMSTAB`** | `0x01CFF4` | `0x01B1E8` | `res_pack_5.s:185`<br>`res_pack_5.s:186` | ELEMS_ELEMSTAB -- offsets of the functions from LIFTOFF (ELEMS_NONANS), indexed by the opcode AND $FE. |
| **`ELEMS_ERRFINAN`** | `0x01D76E` | `0x01B962` | `res_pack_5.s:1244`<br>`res_pack_5.s:1245` | ELEMS_ERRFINAN -- invalid financial argument: deliver NaN code 38 (NANFINAN). |
| **`ELEMS_ERRORNAN`** | `0x01D2DE` | `0x01B4D2` | `res_pack_5.s:650`<br>`res_pack_5.s:651` | ELEMS_ERRORNAN -- deliver a quiet NaN with the code in D0.B (nonzero) and signal invalid. Called by: ELEMS_LOGTOP, ELEMS_XPWRY9ERR, ELEMS_ERRFINAN (ERRFINAN), ELEMS_SINTOP, ELEMS_TANTOP |
| **`ELEMS_EXP1FINITE`** | `0x01D3CE` | `0x01B5C2` | `res_pack_5.s:780`<br>`res_pack_5.s:781` | EXP1FINITE: finite, nonzero |
| **`ELEMS_EXP1OUT`** | `0x01D3E6` | `0x01B5DA` | `res_pack_5.s:791`<br>`res_pack_5.s:792` | EXP1OUT: tiny result |
| **`ELEMS_EXP1R`** | `0x01D3F6` | `0x01B5EA` | `res_pack_5.s:802`<br>`res_pack_5.s:803` | ELEMS_EXP1R -- e^T - 1: split T into K and F/ln(2), where T = K*ln(2) + F; on overflow deliver +inf or -1. |
| **`ELEMS_EXP1RDONE`** | `0x01D44C` | `0x01B640` | `res_pack_5.s:837`<br>`res_pack_5.s:838` | EXP1RDONE |
| **`ELEMS_EXP1ROOT`** | `0x01D414` | `0x01B608` | `res_pack_5.s:817`<br>`res_pack_5.s:818` | ELEMS_EXP1ROOT -- common root of e^x - 1 and 2^x - 1: 2^T - 1 for the fraction T; if the integer W is nonzero, finish with (((2^T - 1) + 1) * 2^W) - 1. |
| **`ELEMS_EXP1TOP`** | `0x01D3BC` | `0x01B5B0` | `res_pack_5.s:770`<br>`res_pack_5.s:771` | ELEMS_EXP1TOP -- e^x - 1 and 2^x - 1 (opcodes $C, $E): the same exception code, then EXPAPPROX for 2^frac - 1. e^(+-0) - 1 = +-0, e^-inf - 1 = -1, e^+inf - 1 = +inf; a denormal x gives x (e^x - 1) or ... |
| **`ELEMS_EXP21P`** | `0x01DCEE` | `0x01BEE2` | `res_pack_5.s:1898`<br>`res_pack_5.s:1899` | EXP21P: P of EXPAPPROX |
| **`ELEMS_EXP21Q`** | `0x01DD18` | `0x01BF0C` | `res_pack_5.s:1905`<br>`res_pack_5.s:1906` | EXP21Q: Q of EXPAPPROX |
| **`ELEMS_EXP21RNORM`** | `0x01D3F0` | `0x01B5E4` | `res_pack_5.s:796`<br>`res_pack_5.s:797` | EXP21RNORM: 2^T - 1 of a normal T: W := integer part, T := fraction |
| **`ELEMS_EXPAPPROX`** | `0x01D450` | `0x01B644` | `res_pack_5.s:844`<br>`res_pack_5.s:845` | ELEMS_EXPAPPROX -- (A4) := 2^T - 1 for T = (A4), \|T\| <= 1/2: 2 * T * P(T*T) / (Q(T*T) - T * P(T*T)), coefficients EXP21P (ELEMS_EXP21P) and EXP21Q (ELEMS_EXP21Q). T = 0 returns 0 without inexact. Uses... |
| **`ELEMS_EXPEASY`** | `0x01D3CA` | `0x01B5BE` | `res_pack_5.s:777`<br>`res_pack_5.s:778` | EXPEASY: the argument is the result |
| **`ELEMS_EXPHARD`** | `0x01D460` | `0x01B654` | `res_pack_5.s:852`<br>`res_pack_5.s:853` | EXPHARD: T <> 0 |
| **`ELEMS_EXPNONZERO`** | `0x01D318` | `0x01B50C` | `res_pack_5.s:689`<br>`res_pack_5.s:690` | EXPNONZERO: 2^T: W := integer part, T := fraction (SPLIT2) |
| **`ELEMS_EXPR`** | `0x01D322` | `0x01B516` | `res_pack_5.s:698`<br>`res_pack_5.s:699` | ELEMS_EXPR -- e^T: with T = K * ln(2) + F, e^T = 2^K * ((2^(F/ln(2)) - 1) + 1): SPLIT sets W := K and T := F/ln(2), then the 2^x code (EXPROOT). A huge T overflows in SPLIT: +inf or +0. |
| **`ELEMS_EXPROOT`** | `0x01D340` | `0x01B534` | `res_pack_5.s:711`<br>`res_pack_5.s:712` | ELEMS_EXPROOT -- common root of e^x and 2^x: ((2^T - 1) + 1) * 2^W, the integer W possibly huge (SCALBXX). |
| **`ELEMS_EXPTOP`** | `0x01D30C` | `0x01B500` | `res_pack_5.s:681`<br>`res_pack_5.s:682` | ELEMS_EXPTOP -- e^x and 2^x (opcodes 8, $A; bit 1 = BTLOGBASE2: 2^x): the result is 2^K * ((2^frac - 1) + 1), with 2^frac - 1 from EXPAPPROX. e^(+-0) = 1, e^-inf = +0, e^+inf = +inf; overflow gives +i... |
| **`ELEMS_FINPWRI`** | `0x01D4FE` | `0x01B6F2` | `res_pack_5.s:919`<br>`res_pack_5.s:920` | ELEMS_FINPWRI -- nonzero finite x: a small \|i\| is multiplied out (the sign of x survives for odd i); a large one is converted to extended and evaluated with log and exp. |
| **`ELEMS_FINPWRI_1`** | `0x01D504` | `0x01B6F8` | `res_pack_5.s:923`<br>`res_pack_5.s:924` | — |
| **`ELEMS_FINPWRY`** | `0x01D686` | `0x01B87A` | `res_pack_5.s:1128`<br>`res_pack_5.s:1129` | FINPWRY: finite x; finite^inf has the special case 1^inf (invalid) |
| **`ELEMS_FORCEDIVZER`** | `0x01D07C` | `0x01B270` | `res_pack_5.s:301`<br>`res_pack_5.s:302` | FORCEDIVZER |
| **`ELEMS_FORCEINEXACT`** | `0x01D084` | `0x01B278` | `res_pack_5.s:311`<br>`res_pack_5.s:312` | FORCEINEXACT Called by: ELEMS_LOGAPPROX, ELEMS_EXPR, ELEMS_EXP1TOP (EXP1TOP), ELEMS_EXP1R, ELEMS_EXPAPPROX (and 1 more) |
| **`ELEMS_FORCEINVALID`** | `0x01D080` | `0x01B274` | `res_pack_5.s:305`<br>`res_pack_5.s:306` | FORCEINVALID |
| **`ELEMS_FORCEOFLOW`** | `0x01D074` | `0x01B268` | `res_pack_5.s:291`<br>`res_pack_5.s:292` | ELEMS_FORCEOFLOW, ELEMS_FORCEUFLOW, ELEMS_FORCEDIVZER, ELEMS_FORCEINVALID, ELEMS_FORCEINEXACT (FORCEINEXACT) -- set an exception flag with FSETXCP (which also halts if that halt is enabled; within Ele... |
| **`ELEMS_FORCEUFLOW`** | `0x01D078` | `0x01B26C` | `res_pack_5.s:297`<br>`res_pack_5.s:298` | FORCEUFLOW Called by: ELEMS_LOGAPPROX, ELEMS_EXPR, ELEMS_EXP1TOP (EXP1TOP), ELEMS_ANNDOIT, ELEMS_TRIGFINI |
| **`ELEMS_FORCEX`** | `0x01D086` | `0x01B27A` | `res_pack_5.s:315`<br>`res_pack_5.s:316` | FORCEX: set flag D0 Called by: the four FORCE* entries above (BRA.B) |
| **`ELEMS_FPK0`** | `0x01DD4C` | `0x01BF40` | `res_pack_5.s:1914`<br>`res_pack_5.s:1915` | — |
| **`ELEMS_FPK1`** | `0x01DD38` | `0x01BF2C` | `res_pack_5.s:1910`<br>`res_pack_5.s:1911` | — |
| **`ELEMS_FPK2`** | `0x01DD60` | `0x01BF54` | `res_pack_5.s:1918`<br>`res_pack_5.s:1919` | — |
| **`ELEMS_FPK3`** | `0x01DD88` | `0x01BF7C` | `res_pack_5.s:1926`<br>`res_pack_5.s:1927` | — |
| **`ELEMS_FPK34`** | `0x01DDA6` | `0x01BF9A` | `res_pack_5.s:1932`<br>`res_pack_5.s:1933` | — |
| **`ELEMS_FPK78`** | `0x01DDB0` | `0x01BFA4` | `res_pack_5.s:1934`<br>`res_pack_5.s:1935` | — |
| **`ELEMS_FPKARAND`** | `0x01DDCE` | `0x01BFC2` | `res_pack_5.s:1939`<br>`res_pack_5.s:1940` | — |
| **`ELEMS_FPKATNCONS`** | `0x01DE1E` | `0x01C012` | `res_pack_5.s:1954`<br>`res_pack_5.s:1955` | — |
| **`ELEMS_FPKFOURTH`** | `0x01DD92` | `0x01BF86` | `res_pack_5.s:1928`<br>`res_pack_5.s:1929` | — |
| **`ELEMS_FPKHALF`** | `0x01DD9C` | `0x01BF90` | `res_pack_5.s:1930`<br>`res_pack_5.s:1931` | — |
| **`ELEMS_FPKINF`** | `0x01DD74` | `0x01BF68` | `res_pack_5.s:1922`<br>`res_pack_5.s:1923` | — |
| **`ELEMS_FPKLOGE2`** | `0x01DE00` | `0x01BFF4` | `res_pack_5.s:1948`<br>`res_pack_5.s:1949` | — |
| **`ELEMS_FPKM0`** | `0x01DD56` | `0x01BF4A` | `res_pack_5.s:1916`<br>`res_pack_5.s:1917` | — |
| **`ELEMS_FPKM1`** | `0x01DD42` | `0x01BF36` | `res_pack_5.s:1912`<br>`res_pack_5.s:1913` | — |
| **`ELEMS_FPKMAXINT`** | `0x01DD6A` | `0x01BF5E` | `res_pack_5.s:1920`<br>`res_pack_5.s:1921` | — |
| **`ELEMS_FPKMINF`** | `0x01DD7E` | `0x01BF72` | `res_pack_5.s:1924`<br>`res_pack_5.s:1925` | — |
| **`ELEMS_FPKPI2`** | `0x01DDBA` | `0x01BFAE` | `res_pack_5.s:1936`<br>`res_pack_5.s:1937` | — |
| **`ELEMS_FPKPRAND`** | `0x01DDD8` | `0x01BFCC` | `res_pack_5.s:1941`<br>`res_pack_5.s:1942` | — |
| **`ELEMS_FPKSQRT2`** | `0x01DDE2` | `0x01BFD6` | `res_pack_5.s:1943`<br>`res_pack_5.s:1944` | — |
| **`ELEMS_FPKSQRTHALF`** | `0x01DDEC` | `0x01BFE0` | `res_pack_5.s:1945`<br>`res_pack_5.s:1946` | — |
| **`ELEMS_FPKX2`** | `0x01DE0A` | `0x01BFFE` | `res_pack_5.s:1950`<br>`res_pack_5.s:1951` | — |
| **`ELEMS_FPKX2FX2`** | `0x01DE14` | `0x01C008` | `res_pack_5.s:1952`<br>`res_pack_5.s:1953` | — |
| **`ELEMS_HAVESRC2`** | `0x01CF7E` | `0x01B172` | `res_pack_5.s:117`<br>`res_pack_5.s:118` | HAVESRC2: three addresses (Compound, Annuity): src2 is the deepest |
| **`ELEMS_LAFINI`** | `0x01D29E` | `0x01B492` | `res_pack_5.s:593`<br>`res_pack_5.s:594` | LAFINI: divide, result inexact |
| **`ELEMS_LANONZERO`** | `0x01D22C` | `0x01B420` | `res_pack_5.s:552`<br>`res_pack_5.s:553` | LANONZERO: denormal S: S / ln(2), underflow |
| **`ELEMS_LANORMAL`** | `0x01D23A` | `0x01B42E` | `res_pack_5.s:559`<br>`res_pack_5.s:560` | LANORMAL |
| **`ELEMS_LOG0`** | `0x01D156` | `0x01B34A` | `res_pack_5.s:450`<br>`res_pack_5.s:451` | LOG0: x = 0 (log), x = -1 (log of 1+x) |
| **`ELEMS_LOG12R`** | `0x01D15A` | `0x01B34E` | `res_pack_5.s:457`<br>`res_pack_5.s:458` | ELEMS_LOG12R -- log2(1+T) for a finite T > -1, T <> 0. If 1+T lies outside sqrt(1/2)..sqrt(2), compute log2 of the sum 1+T (LOG2R); else LOGAPPROX on T itself, ignoring the rounded sum (accuracy for s... |
| **`ELEMS_LOG1PLUSX`** | `0x01D140` | `0x01B334` | `res_pack_5.s:440`<br>`res_pack_5.s:441` | LOG1PLUSX: ln(1+x), log2(1+x) of a finite x |
| **`ELEMS_LOG21P`** | `0x01DC90` | `0x01BE84` | `res_pack_5.s:1883`<br>`res_pack_5.s:1884` | Constants (Apple ELEMS68KC.a, generated by HexWriter from ELEMSDEC.TEXT): the polynomial tables for POLYEVAL (a degree word N, then N+1 extended coefficients, leading term first; each P table follows ... |
| **`ELEMS_LOG21Q`** | `0x01DCCE` | `0x01BEC2` | `res_pack_5.s:1892`<br>`res_pack_5.s:1893` | LOG21Q: Q of LOGAPPROX |
| **`ELEMS_LOG2R`** | `0x01D19A` | `0x01B38E` | `res_pack_5.s:484`<br>`res_pack_5.s:485` | ELEMS_LOG2R -- log2(T) for a positive finite T at A4: T = 2^L * Q with sqrt(1/2) <= Q <= sqrt(2), log2(T) = L + log2(Q), and log2(Q) = log2(1 + (Q-1)) from LOGAPPROX. L is kept in cell W. |
| **`ELEMS_LOGAPPROX`** | `0x01D212` | `0x01B406` | `res_pack_5.s:539`<br>`res_pack_5.s:540` | ELEMS_LOGAPPROX -- (A4) := log2(1+S) for S = (A4), 1+S in sqrt(1/2)..sqrt(2), special cases already filtered out: R := S / (2+S), log2(1+S) = R * P(R*R) / Q(R*R), coefficients LOG21P (ELEMS_LOG21P) an... |
| **`ELEMS_LOGAPPROX_1`** | `0x01D226` | `0x01B41A` | `res_pack_5.s:547`<br>`res_pack_5.s:548` | — |
| **`ELEMS_LOGERROR`** | `0x01D12A` | `0x01B31E` | `res_pack_5.s:427`<br>`res_pack_5.s:428` | LOGERROR: invalid argument |
| **`ELEMS_LOGFINI`** | `0x01D1FC` | `0x01B3F0` | `res_pack_5.s:520`<br>`res_pack_5.s:521` | LOGFINI: times ln(2) for the natural logarithms |
| **`ELEMS_LOGFINI_1`** | `0x01D20E` | `0x01B402` | `res_pack_5.s:528`<br>`res_pack_5.s:529` | log2: done |
| **`ELEMS_LOGFINITE`** | `0x01D130` | `0x01B324` | `res_pack_5.s:431`<br>`res_pack_5.s:432` | LOGFINITE |
| **`ELEMS_LOGTOP`** | `0x01D120` | `0x01B314` | `res_pack_5.s:421`<br>`res_pack_5.s:422` | ELEMS_LOGTOP -- ln(x), log2(x), ln(1+x), log2(1+x) (opcodes 0, 2, 4, 6): opcode bit 1 (BTLOGBASE2) selects base 2, bit 2 (BTLOG1PLUSX) the argument 1+x. Everything is computed in base 2 from log2(1+z)... |
| **`ELEMS_M0STUFF`** | `0x01D2B2` | `0x01B4A6` | `res_pack_5.s:611`<br>`res_pack_5.s:612` | M0STUFF: -0 |
| **`ELEMS_M1STUFF`** | `0x01D2BE` | `0x01B4B2` | `res_pack_5.s:621`<br>`res_pack_5.s:622` | M1STUFF: -1 |
| **`ELEMS_MINFSTUFF`** | `0x01D2D2` | `0x01B4C6` | `res_pack_5.s:637`<br>`res_pack_5.s:638` | MINFSTUFF: -inf |
| **`ELEMS_NANEXIT`** | `0x01CFE2` | `0x01B1D6` | `res_pack_5.s:174`<br>`res_pack_5.s:175` | NANEXIT |
| **`ELEMS_NEGPWRY`** | `0x01D606` | `0x01B7FA` | `res_pack_5.s:1068`<br>`res_pack_5.s:1069` | ELEMS_NEGPWRY -- x < 0: y must be finite and integral (else invalid); the parity of y (the inexact flag of y/2 rounded) is saved in cell J to set the sign after XPWRYCOM. |
| **`ELEMS_NEGPWRY_1`** | `0x01D658` | `0x01B84C` | `res_pack_5.s:1095`<br>`res_pack_5.s:1096` | — |
| **`ELEMS_NONANS`** | `0x01CFE6` | `0x01B1DA` | `res_pack_5.s:177`<br>`res_pack_5.s:178` | NONANS, LIFTOFF: no NaN operand; dispatch on the opcode |
| **`ELEMS_NONPWRY`** | `0x01D67C` | `0x01B870` | `res_pack_5.s:1122`<br>`res_pack_5.s:1123` | NONPWRY: x <> 0 |
| **`ELEMS_NOT2NANS`** | `0x01CFD4` | `0x01B1C8` | `res_pack_5.s:166`<br>`res_pack_5.s:167` | NOT2NANS: the src is no NaN; the dst or src2 may be one |
| **`ELEMS_P0STUFF`** | `0x01D2AC` | `0x01B4A0` | `res_pack_5.s:607`<br>`res_pack_5.s:608` | ELEMS_P0STUFF .. ELEMS_MINFSTUFF -- deliver a special value: P0STUFF +0, M0STUFF -0, P1STUFF +1, M1STUFF -1, DIVP0STUFF divide by zero and +inf, PINFSTUFF +inf, DIVM0STUFF divide by zero and -inf, MIN... |
| **`ELEMS_P1STUFF`** | `0x01D2B8` | `0x01B4AC` | `res_pack_5.s:617`<br>`res_pack_5.s:618` | P1STUFF: +1 Called by: ELEMS_EXPTOP, ELEMS_XPWRITOP, ELEMS_COMPOUNDTOP, ELEMS_COSTOP |
| **`ELEMS_PINFSTUFF`** | `0x01D2C8` | `0x01B4BC` | `res_pack_5.s:630`<br>`res_pack_5.s:631` | PINFSTUFF: +inf Called by: ELEMS_LOGTOP, ELEMS_EXPR, ELEMS_EXP1R, ELEMS_COMPOUNDTOP |
| **`ELEMS_POLYEVAL`** | `0x01D020` | `0x01B214` | `res_pack_5.s:222`<br>`res_pack_5.s:223` | ELEMS_POLYEVAL -- Horner's rule: (A0) := C0, then (A0) := (A0) * (A2) + Cj for j = 1..N. A1 -> the table: a degree word N, then N+1 extended coefficients, leading term first. A0 and A2 preserved; A1 i... |
| **`ELEMS_POLYLOOP`** | `0x01D02C` | `0x01B220` | `res_pack_5.s:229`<br>`res_pack_5.s:230` | POLYLOOP |
| **`ELEMS_POVERQ`** | `0x01D970` | `0x01BB64` | `res_pack_5.s:1521`<br>`res_pack_5.s:1522` | ELEMS_POVERQ -- for T = (A4) and A2 -> a Q coefficient table with the P table right behind it: W := S = T*T, Y := Q(S), X := P(S) / Q(S); returns A0 -> cell X, A2 -> cell W. Used by T2POVERQ and ATANG... |
| **`ELEMS_RANDTOP`** | `0x01DC66` | `0x01BE5A` | `res_pack_5.s:1860`<br>`res_pack_5.s:1861` | ELEMS_RANDTOP -- RandomX (opcode $20): next T := (7^5 * T) MOD (2^31 - 1), after Linus Schrage, "A More Portable FORTRAN Random Number Generator", ACM TOMS 5(2), June 1979, pp. 132-138 (Apple's commen... |
| **`ELEMS_RANDTOP_1`** | `0x01DC8C` | `0x01BE80` | `res_pack_5.s:1875`<br>`res_pack_5.s:1876` | — |
| **`ELEMS_RESULTDELIVERED`** | `0x01D2F0` | `0x01B4E4` | `res_pack_5.s:666`<br>`res_pack_5.s:667` | ELEMS_RESULTDELIVERED -- the result is in (A4): restore the caller's environment and signal the exceptions raised here (FPROCEXIT), restore the package's lock state and the registers, pop opcode and a... |
| **`ELEMS_SCALBXX`** | `0x01D0B2` | `0x01B2A6` | `res_pack_5.s:359`<br>`res_pack_5.s:360` | ELEMS_SCALBXX -- (A0) := (A0) * 2^(A1) for an extended integral (A1) of any size. FSCALBX takes a 16-bit integer, but because of the 15-bit exponent range two steps of at most 32767 (MAXINT) are enoug... |
| **`ELEMS_SCALBXX_1`** | `0x01D0E2` | `0x01B2D6` | `res_pack_5.s:375`<br>`res_pack_5.s:376` | — |
| **`ELEMS_SCALEINT`** | `0x01D102` | `0x01B2F6` | `res_pack_5.s:397`<br>`res_pack_5.s:398` | ELEMS_SCALEINT -- (A0) := (A0) * 2^J, J = the integer in cell J. |
| **`ELEMS_SINCOSCOM`** | `0x01D8D8` | `0x01BACC` | `res_pack_5.s:1427`<br>`res_pack_5.s:1428` | SINCOSCOM: sin and cos of a finite or infinite x |
| **`ELEMS_SINCOSCOM_1`** | `0x01D8E8` | `0x01BADC` | `res_pack_5.s:1435`<br>`res_pack_5.s:1436` | @1: odd quotient |
| **`ELEMS_SINCOSCOM_3`** | `0x01D8EC` | `0x01BAE0` | `res_pack_5.s:1438`<br>`res_pack_5.s:1439` | @3: the sign from the quotient |
| **`ELEMS_SINGUTS`** | `0x01D93C` | `0x01BB30` | `res_pack_5.s:1488`<br>`res_pack_5.s:1489` | ELEMS_SINGUTS -- (A4) := sin(T) for \|T\| <= pi/4: T - T * S * P(S)/Q(S), S = T*T, coefficients SINQ (ELEMS_SINQ) and SINP right behind it. Uses A0-A2, cells W, X, Y. |
| **`ELEMS_SINQ`** | `0x01DE28` | `0x01C01C` | `res_pack_5.s:1957`<br>`res_pack_5.s:1958` | SINQ, SINP: Q and P of SINGUTS (sn7.text, 14 May 83) |
| **`ELEMS_SINTOP`** | `0x01D8CE` | `0x01BAC2` | `res_pack_5.s:1421`<br>`res_pack_5.s:1422` | ELEMS_SINTOP -- sin(x) (opcode $18): sin(+-0) = +-0, sin(+-inf) is invalid: NaN code 33 (NANTRIG). The argument is reduced modulo approximate pi/2 (TRIGREDUCTION) to \|T\| <= pi/4, x = q * pi/2 + T: q m... |
| **`ELEMS_SKIPFIRSTSCALB`** | `0x01D0E4` | `0x01B2D8` | `res_pack_5.s:378`<br>`res_pack_5.s:379` | SKIPFIRSTSCALB: if Y still exceeds 32767, scale by +-32767 again |
| **`ELEMS_SPLIT`** | `0x01D37C` | `0x01B570` | `res_pack_5.s:741`<br>`res_pack_5.s:742` | ELEMS_SPLIT -- split T (A4) for e^x and e^x - 1: T = K * ln(2) + F, with F = T REM ln(2); W := K = (T - F) / ln(2) (made integral), T := F / ln(2). Exits through CLEARINEXACT. |
| **`ELEMS_SPLIT2`** | `0x01D35A` | `0x01B54E` | `res_pack_5.s:724`<br>`res_pack_5.s:725` | ELEMS_SPLIT2 -- split T (A4) into the integer part W (rounded to nearest, cell W) and the fraction T - W (A4), \|T - W\| <= 1/2. |
| **`ELEMS_START`** | `0x01CF3A` | `0x01B12E` | `res_pack_5.s:87`<br>`res_pack_5.s:88` | ELEMS_START -- the entry of _Elems68K: frame, registers, package locked; fetch the operand addresses and move the return address onto the deepest one (its old slot's high word = the byte count to pop ... |
| **`ELEMS_STUFFVAL`** | `0x01D2D6` | `0x01B4CA` | `res_pack_5.s:641`<br>`res_pack_5.s:642` | STUFFVAL: (A4) := the constant at A0, deliver Called by: the stubs P0STUFF .. PINFSTUFF above (BRA.B) |
| **`ELEMS_T2POVERQ`** | `0x01D962` | `0x01BB56` | `res_pack_5.s:1507`<br>`res_pack_5.s:1508` | ELEMS_T2POVERQ -- like POVERQ, then X := S * P(S)/Q(S): cell W = S = T*T, A0 -> cell X, A2 -> cell W. Uses cell Y. |
| **`ELEMS_TANGUTS`** | `0x01DA80` | `0x01BC74` | `res_pack_5.s:1641`<br>`res_pack_5.s:1642` | ELEMS_TANGUTS -- (A4) := tan(T) for \|T\| <= pi/4, S = T*T: for S <= 1/4, T + (T^3/3 + T^5 * P(S)/Q(S)); else, with T' = (T - 3/4)/3, T + (S/4 + S*T' + T^5 * P(S)/Q(S)) (S/4 + S*T' = T^3/3). Coefficient... |
| **`ELEMS_TANQ`** | `0x01DED0` | `0x01C0C4` | `res_pack_5.s:1981`<br>`res_pack_5.s:1982` | TANQ, TANP: Q and P of TANGUTS (tn7.text, 23 May 83) |
| **`ELEMS_TANTOP`** | `0x01DA38` | `0x01BC2C` | `res_pack_5.s:1609`<br>`res_pack_5.s:1610` | ELEMS_TANTOP -- tan(x) (opcode $1C): tan(+-0) = +-0, tan(+-inf) is invalid (NaN code 33). Reduced modulo pi/2 like sin; tan(pi/2 + T) = -1/tan(T) and tan(pi + T) = tan(T), so an odd quotient gives -1/... |
| **`ELEMS_TANTOP_21`** | `0x01DA7C` | `0x01BC70` | `res_pack_5.s:1633`<br>`res_pack_5.s:1634` | — |
| **`ELEMS_TESTDIVZER`** | `0x01D092` | `0x01B286` | `res_pack_5.s:326`<br>`res_pack_5.s:327` | ELEMS_TESTDIVZER, ELEMS_TESTUFLOW, ELEMS_TESTOFLOW, ELEMS_TESTINVALID, ELEMS_TESTINEXACT (TESTINEXACT) -- test an exception flag with FTESTXCP: Z set if the flag is clear, Z clear if it is set. Uses D... |
| **`ELEMS_TESTINEXACT`** | `0x01D0A2` | `0x01B296` | `res_pack_5.s:342`<br>`res_pack_5.s:343` | TESTINEXACT |
| **`ELEMS_TESTINVALID`** | `0x01D09E` | `0x01B292` | `res_pack_5.s:338`<br>`res_pack_5.s:339` | TESTINVALID |
| **`ELEMS_TESTOFLOW`** | `0x01D09A` | `0x01B28E` | `res_pack_5.s:334`<br>`res_pack_5.s:335` | TESTOFLOW |
| **`ELEMS_TESTUFLOW`** | `0x01D096` | `0x01B28A` | `res_pack_5.s:330`<br>`res_pack_5.s:331` | TESTUFLOW |
| **`ELEMS_TESTX`** | `0x01D0A4` | `0x01B298` | `res_pack_5.s:346`<br>`res_pack_5.s:347` | TESTX: test flag D0 Called by: the four TEST* entries above (BRA.B) |
| **`ELEMS_TGBIG`** | `0x01DACE` | `0x01BCC2` | `res_pack_5.s:1671`<br>`res_pack_5.s:1672` | TGBIG: S > 1/4: the longer formula |
| **`ELEMS_TGFIN`** | `0x01DB18` | `0x01BD0C` | `res_pack_5.s:1701`<br>`res_pack_5.s:1702` | TGFIN: add (A0), X or Y, to T |
| **`ELEMS_TRIGFINI`** | `0x01D8F8` | `0x01BAEC` | `res_pack_5.s:1446`<br>`res_pack_5.s:1447` | ELEMS_TRIGFINI -- common end of sin, cos and tan: clear underflow, set inexact; a denormal result signals underflow again. |
| **`ELEMS_TRIGFINI_11`** | `0x01D914` | `0x01BB08` | `res_pack_5.s:1456`<br>`res_pack_5.s:1457` | — |
| **`ELEMS_TRIGFINI_13`** | `0x01D91C` | `0x01BB10` | `res_pack_5.s:1460`<br>`res_pack_5.s:1461` | — |
| **`ELEMS_TRIGREDUCTION`** | `0x01D92C` | `0x01BB20` | `res_pack_5.s:1477`<br>`res_pack_5.s:1478` | ELEMS_TRIGREDUCTION -- T := T REM approximate pi/2 (A4), \|T\| <= pi/4; D2 := D2 (the quotient adjustment) + the low bits of the quotient (FREMX returns them in D0). Uses D0. |
| **`ELEMS_VSMAXINT`** | `0x01D110` | `0x01B304` | `res_pack_5.s:406`<br>`res_pack_5.s:407` | ELEMS_VSMAXINT -- compare 32767 (FPKMAXINT) with cell Y; the CCR as left by FCMPX (32767 against Y). |
| **`ELEMS_XKLPENTRY`** | `0x01D5AA` | `0x01B79E` | `res_pack_5.s:1009`<br>`res_pack_5.s:1010` | — |
| **`ELEMS_XKLPSKIP`** | `0x01D5B8` | `0x01B7AC` | `res_pack_5.s:1017`<br>`res_pack_5.s:1018` | XKLPSKIP |
| **`ELEMS_XKLPTOP`** | `0x01D5A0` | `0x01B794` | `res_pack_5.s:1004`<br>`res_pack_5.s:1005` | XKLPTOP |
| **`ELEMS_XPWRBIG`** | `0x01D510` | `0x01B704` | `res_pack_5.s:931`<br>`res_pack_5.s:932` | ELEMS_XPWRBIG -- \|i\| > 255: i converted to extended in cell W, \|x\|^W by XPWRY, then the sign of x for odd i. |
| **`ELEMS_XPWRBIG_3`** | `0x01D534` | `0x01B728` | `res_pack_5.s:945`<br>`res_pack_5.s:946` | — |
| **`ELEMS_XPWRITOP`** | `0x01D4CC` | `0x01B6C0` | `res_pack_5.s:893`<br>`res_pack_5.s:894` | ELEMS_XPWRITOP -- x^i (opcode $8010): the extended dst x to the power of the 16-bit integer src i. x^0 = 1 for every non-NaN x; (inf or 0)^i: the sign stays only for odd i, a negative i gives +-0 for ... |
| **`ELEMS_XPWRITOP_1`** | `0x01D4E0` | `0x01B6D4` | `res_pack_5.s:902`<br>`res_pack_5.s:903` | — |
| **`ELEMS_XPWRK`** | `0x01D538` | `0x01B72C` | `res_pack_5.s:953`<br>`res_pack_5.s:954` | ELEMS_XPWRK -- (A4) := T^D2 for T = (A4), D0 = \|D2\|, D2 <> 0: T^\|D2\| by XPWRKLOOP, reciprocated at the end for a negative D2; if T^\|D2\| over- or underflowed, the power is recomputed from 1/T. The sign... |
| **`ELEMS_XPWRKCLEAR`** | `0x01D574` | `0x01B768` | `res_pack_5.s:980`<br>`res_pack_5.s:981` | XPWRKCLEAR: T^\|i\| over/underflowed: (1/T)^\|i\| instead |
| **`ELEMS_XPWRKCLEAR_11`** | `0x01D58E` | `0x01B782` | `res_pack_5.s:990`<br>`res_pack_5.s:991` | — |
| **`ELEMS_XPWRKDIV`** | `0x01D550` | `0x01B744` | `res_pack_5.s:966`<br>`res_pack_5.s:967` | XPWRKDIV: negative power: 1 / T^\|i\| |
| **`ELEMS_XPWRKLOOP`** | `0x01D592` | `0x01B786` | `res_pack_5.s:998`<br>`res_pack_5.s:999` | ELEMS_XPWRKLOOP -- W := X^K, X = (A4), K = D0 > 0: binary powering from the low bit of K (W := W * X for a set bit, X := X * X), so (A4) is squared in place. Returns A1 -> cell W. Uses cell W, A0; tra... |
| **`ELEMS_XPWRKSTORE`** | `0x01D548` | `0x01B73C` | `res_pack_5.s:961`<br>`res_pack_5.s:962` | XPWRKSTORE |
| **`ELEMS_XPWRY`** | `0x01D5BE` | `0x01B7B2` | `res_pack_5.s:1027`<br>`res_pack_5.s:1028` | ELEMS_XPWRY -- (A4) := (A4)^(D4) for a positive (A4): 2^(y * log2(x)) through recursive calls of the package (FLOG2X, then FEXP2X). FMULX never meets 0 * inf here, so cases like inf^3 come out right. ... |
| **`ELEMS_XPWRY9ERR`** | `0x01D5FA` | `0x01B7EE` | `res_pack_5.s:1057`<br>`res_pack_5.s:1058` | ELEMS_XPWRY9ERR, ELEMS_XPWRYERR -- invalid x^y: deliver NaN code 37 (NANPOWER). XPWRY9ERR is the entry from inside a subroutine: it drops the return address first. |
| **`ELEMS_XPWRYCOM`** | `0x01D65C` | `0x01B850` | `res_pack_5.s:1105`<br>`res_pack_5.s:1106` | ELEMS_XPWRYCOM -- (A4) := (A4)^(D4) for (A4) >= 0, (D4) no NaN; D1/D2 = the classes less FCINF. 2^(y * log2(x)) works as long as it never multiplies inf and 0. Special cases: 0^0, inf^0 and 1^inf are ... |
| **`ELEMS_XPWRYCOM_1`** | `0x01D672` | `0x01B866` | `res_pack_5.s:1116`<br>`res_pack_5.s:1117` | @1: 0^positive |
| **`ELEMS_XPWRYCOM_2`** | `0x01D676` | `0x01B86A` | `res_pack_5.s:1118`<br>`res_pack_5.s:1119` | — |
| **`ELEMS_XPWRYERR`** | `0x01D5FC` | `0x01B7F0` | `res_pack_5.s:1060`<br>`res_pack_5.s:1061` | XPWRYERR |
| **`ELEMS_XPWRYHARD`** | `0x01D6CE` | `0x01B8C2` | `res_pack_5.s:1162`<br>`res_pack_5.s:1163` | XPWRYHARD: 2^(y * log2(x)) |
| **`ELEMS_XPWRYOK`** | `0x01D69A` | `0x01B88E` | `res_pack_5.s:1141`<br>`res_pack_5.s:1142` | ELEMS_XPWRYOK -- finite^reasonable: a small integral y is multiplied out, else log and exp. The integer test converts y to 16 bits: out of range = invalid (cleared again, it is undeserved), not integr... |
| **`ELEMS_XPWRYOK_1`** | `0x01D6C6` | `0x01B8BA` | `res_pack_5.s:1158`<br>`res_pack_5.s:1159` | — |
| **`ELEMS_XPWRYTOP`** | `0x01D5EE` | `0x01B7E2` | `res_pack_5.s:1048`<br>`res_pack_5.s:1049` | ELEMS_XPWRYTOP -- x^y (opcode $8012), both extended: a negative x needs an integral y (NEGPWRY), the sign of the result then follows the parity of y; the rest is XPWRYCOM. |
| **`ELEMS_ZPWRNEG`** | `0x01D4F4` | `0x01B6E8` | `res_pack_5.s:911`<br>`res_pack_5.s:912` | ZPWRNEG: 0^-n |
| **`EP_LISTENER`** | — | `0x0333C6` | `res_drvr_mpp.s:612` | EP_LISTENER: listener of socket 4, the Echo Protocol's echoer (DDP type 4; Inside Macintosh V-519, Networking "DDP").  An Echo Request (first data byte 1) is read into the EP buffer (EPBufPtr: a param... |
| **`EP_LISTENER_CKSCMP`** | — | `0x033442` | `res_drvr_mpp.s:658` | long header: verify a nonzero checksum, then take ddpSrcNet/ddpSrcNode |
| **`EP_LISTENER_DISCARD`** | — | `0x0333E8` | `res_drvr_mpp.s:624` | — |
| **`EP_LISTENER_EXIT`** | — | `0x03345E` | `res_drvr_mpp.s:671` | — |
| **`EP_LISTENER_GOT`** | — | `0x0333EE` | `res_drvr_mpp.s:628` | answer an Echo Request |
| **`EP_LISTENER_LONG`** | — | `0x033446` | `res_drvr_mpp.s:661` | — |
| **`EP_LISTENER_REPLY`** | — | `0x033450` | `res_drvr_mpp.s:666` | reply: destination = requester, function 2, WriteDDP (async) |
| **`FP68K_ABSZ`** | `0x01EA16` | `0x01CC0A` | `res_pack_4.s:1774`<br>`res_pack_4.s:1776` | FP68K_ABSZ: abs -- clear the sign bit of (A1). |
| **`FP68K_ADD00`** | `0x01E58E` | `0x01C782` | `res_pack_4.s:1006`<br>`res_pack_4.s:1008` | FP68K_ADD00 -- 0 + 0: signs equal: that zero; else +0, or -0 when rounding downward. FP68K_ZEROSUM: an exact zero sum. |
| **`FP68K_ADDCASE`** | `0x01E530` | `0x01C724` | `res_pack_4.s:946`<br>`res_pack_4.s:948` | FP68K_ADDCASE: case routines by the number cases of (dst, src), offsets from FP68K_ADDTOP. |
| **`FP68K_ADDD0`** | `0x01E5B0` | `0x01C7A4` | `res_pack_4.s:1027`<br>`res_pack_4.s:1029` | — |
| **`FP68K_ADDINF`** | `0x01E5B4` | `0x01C7A8` | `res_pack_4.s:1031`<br>`res_pack_4.s:1033` | FP68K_ADDINF: inf + inf -- equal signs: inf; else invalid. |
| **`FP68K_ADDINF_25`** | `0x01E5BC` | `0x01C7B0` | `res_pack_4.s:1038`<br>`res_pack_4.s:1040` | FP68K_ADDINF_25 (Apple ADDINF @25): +inf + -inf: invalid, NaN code 2 (NANADD). |
| **`FP68K_ADDNUM`** | `0x01E542` | `0x01C736` | `res_pack_4.s:959`<br>`res_pack_4.s:961` | FP68K_ADDNUM -- two finite nonzero numbers: the operand with the larger exponent to D3:A2/A4, the other shifted right in D4:D5; add the magnitudes (carry: shift back) or subtract (SUBMAG), coerce. |
| **`FP68K_ADDNUM_1`** | `0x01E55C` | `0x01C750` | `res_pack_4.s:973`<br>`res_pack_4.s:975` | — |
| **`FP68K_ADDNUM_15`** | `0x01E574` | `0x01C768` | `res_pack_4.s:986`<br>`res_pack_4.s:988` | same signs: add mantissas |
| **`FP68K_ADDNUM_3`** | `0x01E560` | `0x01C754` | `res_pack_4.s:975`<br>`res_pack_4.s:977` | — |
| **`FP68K_ADDQ00`** | `0x01E5A6` | `0x01C79A` | `res_pack_4.s:1017`<br>`res_pack_4.s:1019` | — |
| **`FP68K_ADDS0`** | `0x01E5A8` | `0x01C79C` | `res_pack_4.s:1022`<br>`res_pack_4.s:1024` | FP68K_ADDS0: num + 0 -- the result is the dst; then coerce. FP68K_ADDD0: 0 + num -- the src; coerce. |
| **`FP68K_ADDTOP`** | `0x01E528` | `0x01C71C` | `res_pack_4.s:941`<br>`res_pack_4.s:943` | — |
| **`FP68K_ARITHOP`** | `0x01E06C` | `0x01C260` | `res_pack_4.s:185`<br>`res_pack_4.s:187` | FP68K_ARITHOP: jump to the operation, D0 = opword AND $1E; the operation returns to FP68K_PREPACK. |
| **`FP68K_ARITHTAB`** | `0x01E074` | `0x01C268` | `res_pack_4.s:190`<br>`res_pack_4.s:192` | FP68K_ARITHTAB: operation routines, offsets from FP68K_ARITHOP. |
| **`FP68K_B2D`** | `0x01EF26` | `0x01D11A` | `res_pack_4.s:2424`<br>`res_pack_4.s:2426` | FP68K_B2D -- binary to decimal (Num2Dec): the value at (A2) (format in the opword) to the decimal record at (A1), by the DecForm at address 3 (style: 0 float, nonzero fixed; digits). NaN: 'N' and 16 h... |
| **`FP68K_B2D_10`** | `0x01EF86` | `0x01D17A` | `res_pack_4.s:2469`<br>`res_pack_4.s:2471` | FP68K_B2D_10 (Apple B2D @10): zero ('0') or infinity ('I'), else BD1. |
| **`FP68K_B2D_16`** | `0x01EF94` | `0x01D188` | `res_pack_4.s:2476`<br>`res_pack_4.s:2478` | — |
| **`FP68K_B2D_31`** | `0x01EF6A` | `0x01D15E` | `res_pack_4.s:2452`<br>`res_pack_4.s:2454` | FP68K_B2D_31 (Apple B2D @31): D4 as 8 hex digits to (A1)+. |
| **`FP68K_B2D_33`** | `0x01EF6C` | `0x01D160` | `res_pack_4.s:2454`<br>`res_pack_4.s:2456` | — |
| **`FP68K_B2D_35`** | `0x01EF7E` | `0x01D172` | `res_pack_4.s:2462`<br>`res_pack_4.s:2464` | — |
| **`FP68K_BD1`** | `0x01EF9C` | `0x01D190` | `res_pack_4.s:2483`<br>`res_pack_4.s:2485` | FP68K_BD1 -- finite nonzero: log2\|x\| ~ exp.frac in D1; denormalize back to extended format and store at (A3); float style: D4 = floor(log10\|x\|) + 1 = log10(2) * log2\|x\| + 1 (16 bits suffice). |
| **`FP68K_BD1_1`** | `0x01EFCE` | `0x01D1C2` | `res_pack_4.s:2509`<br>`res_pack_4.s:2511` | estimate decimal exponent using log10(2) approximation log10(2) ~ 0x4D104D42 / 2^32 ~ 0.30103 |
| **`FP68K_BD1_3`** | `0x01EFAC` | `0x01D1A0` | `res_pack_4.s:2491`<br>`res_pack_4.s:2493` | — |
| **`FP68K_BD1_7`** | `0x01EFB4` | `0x01D1A8` | `res_pack_4.s:2496`<br>`res_pack_4.s:2498` | — |
| **`FP68K_BD3`** | `0x01EFEE` | `0x01D1E2` | `res_pack_4.s:2529`<br>`res_pack_4.s:2531` | FP68K_BD3: decimal exponent = -(digits - D4); keep a copy of x at 20(A3) for a retry; scale, round to an integer, compare with 10^N (N = digits, fixed: 19). |
| **`FP68K_BD3_13`** | `0x01F04C` | `0x01D240` | `res_pack_4.s:2564`<br>`res_pack_4.s:2566` | — |
| **`FP68K_BD3_15`** | `0x01F066` | `0x01D25A` | `res_pack_4.s:2575`<br>`res_pack_4.s:2577` | FP68K_BD3_15 (Apple BD3 @15): fixed style, too many digits -- '?'. |
| **`FP68K_BD3_3`** | `0x01F02A` | `0x01D21E` | `res_pack_4.s:2551`<br>`res_pack_4.s:2553` | FP68K_BD3_3 |
| **`FP68K_BD3_5`** | `0x01F02C` | `0x01D220` | `res_pack_4.s:2553`<br>`res_pack_4.s:2555` | FP68K_BD3_3 |
| **`FP68K_BD85`** | `0x01F08E` | `0x01D282` | `res_pack_4.s:2603`<br>`res_pack_4.s:2605` | FP68K_BD85: float style -- a scaled value below 10^(N-1) is replaced by 10^(N-1). |
| **`FP68K_BD85_13`** | `0x01F0B6` | `0x01D2AA` | `res_pack_4.s:2618`<br>`res_pack_4.s:2620` | — |
| **`FP68K_BD9`** | `0x01F0C8` | `0x01D2BC` | `res_pack_4.s:2624`<br>`res_pack_4.s:2626` | — |
| **`FP68K_BD9_11`** | `0x01F112` | `0x01D306` | `res_pack_4.s:2660`<br>`res_pack_4.s:2662` | divide 64-bit integer by 10^19 to extract decimal digits divisor = 10^19 = $8AC72304:89E80000 FP68K_BD9_11: extract decimal digits via multiply-by-10 (x*10 = x*8 + x*2) |
| **`FP68K_BD9_12`** | `0x01F140` | `0x01D334` | `res_pack_4.s:2682`<br>`res_pack_4.s:2684` | — |
| **`FP68K_BD9_3`** | `0x01F0DE` | `0x01D2D2` | `res_pack_4.s:2636`<br>`res_pack_4.s:2638` | FP68K_BD9_3 (Apple BD9 @3): right-align the integer (exponent 63), divide by 10^19 into a fraction, + 1 ulp (so .99999 does not chop to the wrong digit), then 19 times * 10: each digit that falls off ... |
| **`FP68K_BD9_5`** | `0x01F0EC` | `0x01D2E0` | `res_pack_4.s:2641`<br>`res_pack_4.s:2643` | — |
| **`FP68K_BD9_7`** | `0x01F0F4` | `0x01D2E8` | `res_pack_4.s:2646`<br>`res_pack_4.s:2648` | — |
| **`FP68K_BDFIN`** | `0x01F144` | `0x01D338` | `res_pack_4.s:2685`<br>`res_pack_4.s:2687` | — |
| **`FP68K_BDGETCNT`** | `0x01F074` | `0x01D268` | `res_pack_4.s:2582`<br>`res_pack_4.s:2584` | FP68K_BDGETCNT -- D3 = the digit count of the DecForm: fixed style as given, float style held to 1..19. |
| **`FP68K_BDGETCNT_1`** | `0x01F08A` | `0x01D27E` | `res_pack_4.s:2596`<br>`res_pack_4.s:2598` | FP68K_BDGETCNT_1: force minimum 1 digit |
| **`FP68K_BDGETCNT_3`** | `0x01F08C` | `0x01D280` | `res_pack_4.s:2598`<br>`res_pack_4.s:2600` | — |
| **`FP68K_BOTH32`** | `0x01E622` | `0x01C816` | `res_pack_4.s:1099`<br>`res_pack_4.s:1101` | — |
| **`FP68K_CANON`** | `0x01EC90` | `0x01CE84` | `res_pack_4.s:2153`<br>`res_pack_4.s:2155` | — |
| **`FP68K_CANONTOP`** | `0x01EC86` | `0x01CE7A` | `res_pack_4.s:2148`<br>`res_pack_4.s:2150` | FP68K_CANONTOP: fewer than 19 digits -- append zeros (* 10) while the exponent is above 27 (exact scaling limit). |
| **`FP68K_CHKERR`** | `0x01E0A2` | `0x01C296` | `res_pack_4.s:215`<br>`res_pack_4.s:217` | — |
| **`FP68K_CLASSFIN`** | `0x01E9BE` | `0x01CBB2` | `res_pack_4.s:1708`<br>`res_pack_4.s:1710` | — |
| **`FP68K_CLASSFIN_100`** | `0x01E9C4` | `0x01CBB8` | `res_pack_4.s:1712`<br>`res_pack_4.s:1714` | — |
| **`FP68K_CLASSTOP`** | `0x01E9AC` | `0x01CBA0` | `res_pack_4.s:1698`<br>`res_pack_4.s:1700` | FP68K_CLASSTOP -- class of the src: the SANE class + 1, negated for a negative operand: 1 signaling NaN, 2 quiet NaN, 3 infinity, 4 zero, 5 normal, 6 denormal (NaNs come through NANFLOAT); stored as a... |
| **`FP68K_CLASSTOP_99`** | `0x01E9BC` | `0x01CBB0` | `res_pack_4.s:1706`<br>`res_pack_4.s:1708` | — |
| **`FP68K_CMP0`** | `0x01E7BC` | `0x01C9B0` | `res_pack_4.s:1368`<br>`res_pack_4.s:1370` | — |
| **`FP68K_CMPCASE`** | `0x01E796` | `0x01C98A` | `res_pack_4.s:1339`<br>`res_pack_4.s:1341` | FP68K_CMPCASE: case routines by (dst, src), offsets from FP68K_CMPTOP. |
| **`FP68K_CMPD0`** | `0x01E7AC` | `0x01C9A0` | `res_pack_4.s:1355`<br>`res_pack_4.s:1357` | FP68K_CMPD0: 0 vs. number -- D0 = CMPG ($00) or CMPL ($19) |
| **`FP68K_CMPD0_1`** | `0x01E7B4` | `0x01C9A8` | `res_pack_4.s:1360`<br>`res_pack_4.s:1362` | — |
| **`FP68K_CMPFIN`** | `0x01E780` | `0x01C974` | `res_pack_4.s:1327`<br>`res_pack_4.s:1329` | — |
| **`FP68K_CMPFIN_1`** | `0x01E790` | `0x01C984` | `res_pack_4.s:1333`<br>`res_pack_4.s:1335` | — |
| **`FP68K_CMPINF`** | `0x01E7B6` | `0x01C9AA` | `res_pack_4.s:1365`<br>`res_pack_4.s:1367` | FP68K_CMPINF: inf vs inf -- equal if the signs are equal, else as 0 vs num. FP68K_CMP0: equal. |
| **`FP68K_CMPNUM`** | `0x01E7C0` | `0x01C9B4` | `res_pack_4.s:1375`<br>`res_pack_4.s:1377` | FP68K_CMPNUM: num vs num -- different signs: as 0 vs num; else compare exponents, then significands; for negative operands the order flips. |
| **`FP68K_CMPNUM_1`** | `0x01E7D8` | `0x01C9CC` | `res_pack_4.s:1387`<br>`res_pack_4.s:1389` | — |
| **`FP68K_CMPNUM_2`** | `0x01E7DA` | `0x01C9CE` | `res_pack_4.s:1389`<br>`res_pack_4.s:1391` | — |
| **`FP68K_CMPNUM_21`** | `0x01E7E2` | `0x01C9D6` | `res_pack_4.s:1394`<br>`res_pack_4.s:1396` | — |
| **`FP68K_CMPS0`** | `0x01E7A8` | `0x01C99C` | `res_pack_4.s:1351`<br>`res_pack_4.s:1353` | FP68K_CMPS0: num vs 0 -- as 0 vs -num: the dst sign to bit 7, inverted. |
| **`FP68K_CMPTOP`** | `0x01E778` | `0x01C96C` | `res_pack_4.s:1324`<br>`res_pack_4.s:1326` | FP68K_CMPTOP -- compare (CMP, CMPX): call the case routine for the number cases; it returns the CCR value in D0: CMPG $00 (dst > src), CMPL $19 (less), CMPE $04 (equal), CMPU $02 (unordered). FP68K_CM... |
| **`FP68K_COERCE`** | `0x01E31A` | `0x01C50E` | `res_pack_4.s:620`<br>`res_pack_4.s:622` | FP68K_COERCE -- round the result D4:D5/A4 (round bits in D7) to the precision of the operation: single and double have their own sequences (SCOERCE, DCOERCE); for extended: underflow check (UFLOW, thr... |
| **`FP68K_COERCE_1`** | `0x01E344` | `0x01C538` | `res_pack_4.s:637`<br>`res_pack_4.s:639` | — |
| **`FP68K_COMINT`** | `0x01E80A` | `0x01C9FE` | `res_pack_4.s:1433`<br>`res_pack_4.s:1435` | FP68K_COMINT: coerce (rounding the fraction bits away), restore the environment, normalize the result or make it zero. |
| **`FP68K_COMINT_5`** | `0x01E81E` | `0x01CA12` | `res_pack_4.s:1445`<br>`res_pack_4.s:1447` | FP68K_COMINT_5 (Apple COMINT @5): normalize. |
| **`FP68K_COMINT_9`** | `0x01E826` | `0x01CA1A` | `res_pack_4.s:1450`<br>`res_pack_4.s:1452` | — |
| **`FP68K_CPSZ`** | `0x01EA2A` | `0x01CC1E` | `res_pack_4.s:1794`<br>`res_pack_4.s:1796` | FP68K_CPSZ: copysign -- the sign of the operand at (A1) (the "dst") onto the one at (A2). |
| **`FP68K_CPSZ_1`** | `0x01EA36` | `0x01CC2A` | `res_pack_4.s:1801`<br>`res_pack_4.s:1803` | FP68K_CPSZ_1 (Apple CPSZ @1): positive. |
| **`FP68K_CPSZ_2`** | `0x01EA3A` | `0x01CC2E` | `res_pack_4.s:1803`<br>`res_pack_4.s:1805` | — |
| **`FP68K_CVT2E`** | `0x01E7E4` | `0x01C9D8` | `res_pack_4.s:1399`<br>`res_pack_4.s:1401` | FP68K_CVT2E -- convert to extended (format of the src in the opword): only finite nonzero values need coercing. |
| **`FP68K_CVTE2`** | `0x01E858` | `0x01CA4C` | `res_pack_4.s:1489`<br>`res_pack_4.s:1491` | FP68K_CVTE2 -- convert from extended: to a float as CVT2E; to int16/int32/comp: zero is done, infinity overflows, else align the point at the right (IALIGN), round, check the range (IOFLOW). |
| **`FP68K_CVTE2_2`** | `0x01E866` | `0x01CA5A` | `res_pack_4.s:1497`<br>`res_pack_4.s:1499` | FP68K_CVTE2_2 (Apple CVTE2 @2): infinity -> overflow. |
| **`FP68K_CVTE2_4`** | `0x01E870` | `0x01CA64` | `res_pack_4.s:1502`<br>`res_pack_4.s:1504` | — |
| **`FP68K_D2B`** | `0x01EBBE` | `0x01CDB2` | `res_pack_4.s:2038`<br>`res_pack_4.s:2040` | FP68K_D2B -- decimal to binary (Dec2Num): the decimal record at (A2) (sgn, exp, sig: up to 19 digits plus a lost-digits 20th, '0' zero, 'I' infinity, 'N'+hex a NaN) to the format in the opword at (A1)... |
| **`FP68K_D2B_31`** | `0x01EBFC` | `0x01CDF0` | `res_pack_4.s:2063`<br>`res_pack_4.s:2065` | — |
| **`FP68K_D2B_35`** | `0x01EC08` | `0x01CDFC` | `res_pack_4.s:2073`<br>`res_pack_4.s:2075` | FP68K_D2B_35 (Apple D2B @35) -- shift D0 hex digits into D5 (zeros once the D2 string characters are used up). |
| **`FP68K_D2B_36`** | `0x01EC1A` | `0x01CE0E` | `res_pack_4.s:2081`<br>`res_pack_4.s:2083` | — |
| **`FP68K_D2B_37`** | `0x01EC20` | `0x01CE14` | `res_pack_4.s:2084`<br>`res_pack_4.s:2086` | — |
| **`FP68K_D2B_39`** | `0x01EC26` | `0x01CE1A` | `res_pack_4.s:2090`<br>`res_pack_4.s:2092` | FP68K_D2B_39 (Apple D2B @39): a NaN with an all-zero code gets code 21. |
| **`FP68K_DBCORE`** | `0x01ECCC` | `0x01CEC0` | `res_pack_4.s:2193`<br>`res_pack_4.s:2195` | FP68K_DBCORE -- common core of both conversions (steps B4- B7 / D5-D8 of Coonen's algorithms): compute 10^\|D3\| (POW10) with the rounding direction set so that the scale error goes the safe way, multip... |
| **`FP68K_DBCORE_30`** | `0x01ECE8` | `0x01CEDC` | `res_pack_4.s:2213`<br>`res_pack_4.s:2215` | FP68K_DBCORE_30 |
| **`FP68K_DBCORE_37`** | `0x01ECEE` | `0x01CEE2` | `res_pack_4.s:2216`<br>`res_pack_4.s:2218` | — |
| **`FP68K_DBCORE_40`** | `0x01ECF2` | `0x01CEE6` | `res_pack_4.s:2218`<br>`res_pack_4.s:2220` | — |
| **`FP68K_DBCORE_43`** | `0x01ECFA` | `0x01CEEE` | `res_pack_4.s:2222`<br>`res_pack_4.s:2224` | — |
| **`FP68K_DBCORE_5`** | `0x01ED16` | `0x01CF0A` | `res_pack_4.s:2234`<br>`res_pack_4.s:2236` | — |
| **`FP68K_DBCORE_50`** | `0x01ECFC` | `0x01CEF0` | `res_pack_4.s:2224`<br>`res_pack_4.s:2226` | — |
| **`FP68K_DBCORE_51`** | `0x01ECE4` | `0x01CED8` | `res_pack_4.s:2206`<br>`res_pack_4.s:2208` | FP68K_DBCORE_51 (Apple DBCORE @51): to nearest -- clear the flags. |
| **`FP68K_DBCORERETURN`** | `0x01ED74` | `0x01CF68` | `res_pack_4.s:2276`<br>`res_pack_4.s:2278` | — |
| **`FP68K_DBNFIN`** | `0x01EC36` | `0x01CE2A` | `res_pack_4.s:2096`<br>`res_pack_4.s:2098` | — |
| **`FP68K_DBSSTO`** | `0x01EC44` | `0x01CE38` | `res_pack_4.s:2107`<br>`res_pack_4.s:2109` | — |
| **`FP68K_DBSSTO_1`** | `0x01EC4C` | `0x01CE40` | `res_pack_4.s:2111`<br>`res_pack_4.s:2113` | — |
| **`FP68K_DBSTORE`** | `0x01ECA4` | `0x01CE98` | `res_pack_4.s:2167`<br>`res_pack_4.s:2169` | FP68K_DBSTORE: convert the extended at (A3) to the destination format (a recursive EXT2 call), drop the frame, return through POP2. |
| **`FP68K_DBZER`** | `0x01EC3C` | `0x01CE30` | `res_pack_4.s:2102`<br>`res_pack_4.s:2104` | FP68K_DBZER: '0' -> a signed zero; FP68K_DBZSTO (Apple DBZSTO) stores it, FP68K_DBSSTO adds the sign. |
| **`FP68K_DBZSTO`** | `0x01EC42` | `0x01CE36` | `res_pack_4.s:2105`<br>`res_pack_4.s:2107` | — |
| **`FP68K_DCOERCE`** | `0x01E41C` | `0x01C610` | `res_pack_4.s:785`<br>`res_pack_4.s:787` | FP68K_DCOERCE -- coerce to double: underflow threshold $3C01, 53-bit significand, increment $800 in D5, overflow threshold $43FE, huge = 53 ones. |
| **`FP68K_DCOERCE_1`** | `0x01E438` | `0x01C62C` | `res_pack_4.s:795`<br>`res_pack_4.s:797` | — |
| **`FP68K_DCOERCE_5`** | `0x01E45E` | `0x01C652` | `res_pack_4.s:807`<br>`res_pack_4.s:809` | — |
| **`FP68K_DEREF_OP`** | `0x01E012` | `0x01C206` | `res_pack_4.s:143`<br>`res_pack_4.s:145` | conversions from extended: the format field describes the destination |
| **`FP68K_DIG10`** | `0x01EC54` | `0x01CE48` | `res_pack_4.s:2116`<br>`res_pack_4.s:2118` | FP68K_DIG10: D4:D5 := D4:D5 * 10 (D0:D1 = * 2). |
| **`FP68K_DIVBY0`** | `0x01E680` | `0x01C874` | `res_pack_4.s:1156`<br>`res_pack_4.s:1158` | FP68K_DIVBY0: num / 0 -- divide by zero, infinity. |
| **`FP68K_DIVBYI`** | `0x01E68E` | `0x01C882` | `res_pack_4.s:1164`<br>`res_pack_4.s:1166` | FP68K_DIVBYI: num / inf -- zero. |
| **`FP68K_DIVCASE`** | `0x01E66E` | `0x01C862` | `res_pack_4.s:1145`<br>`res_pack_4.s:1147` | FP68K_DIVCASE: case routines by (dst, src), offsets from FP68K_DIVTOP. |
| **`FP68K_DIVNUM`** | `0x01E696` | `0x01C88A` | `res_pack_4.s:1174`<br>`res_pack_4.s:1176` | FP68K_DIVNUM -- two finite nonzero numbers: exponent = difference + $3FFF; 65 quotient bits by restoring division (33 for a single operation), one more if the dividend is smaller; the remainder gives ... |
| **`FP68K_DIVNUM_3`** | `0x01E6A6` | `0x01C89A` | `res_pack_4.s:1182`<br>`res_pack_4.s:1184` | — |
| **`FP68K_DIVNUM_5`** | `0x01E6AC` | `0x01C8A0` | `res_pack_4.s:1186`<br>`res_pack_4.s:1188` | — |
| **`FP68K_DIVNUM_7`** | `0x01E6B2` | `0x01C8A6` | `res_pack_4.s:1190`<br>`res_pack_4.s:1192` | — |
| **`FP68K_DIVNUM_9`** | `0x01E6C4` | `0x01C8B8` | `res_pack_4.s:1200`<br>`res_pack_4.s:1202` | — |
| **`FP68K_DIVTOP`** | `0x01E662` | `0x01C856` | `res_pack_4.s:1138`<br>`res_pack_4.s:1140` | FP68K_DIVTOP -- divide: sign = XOR of the signs, NaN code 4 (NANDIV); dispatch by the number cases. |
| **`FP68K_DONEDIG`** | `0x01EC94` | `0x01CE88` | `res_pack_4.s:2156`<br>`res_pack_4.s:2158` | — |
| **`FP68K_DONEDIG_1`** | `0x01ECA0` | `0x01CE94` | `res_pack_4.s:2161`<br>`res_pack_4.s:2163` | — |
| **`FP68K_ENTRYP`** | `0x01E9FA` | `0x01CBEE` | `res_pack_4.s:1747`<br>`res_pack_4.s:1749` | FP68K_ENTRYP: procentry -- save the environment at (A1), then set the default environment (0: no flags, no halts, to nearest). |
| **`FP68K_EPEXIT`** | `0x01EBBA` | `0x01CDAE` | `res_pack_4.s:2029`<br>`res_pack_4.s:2031` | — |
| **`FP68K_EXITP`** | `0x01EBB0` | `0x01CDA4` | `res_pack_4.s:2024`<br>`res_pack_4.s:2026` | FP68K_EXITP: procexit -- restore the environment saved at (A1), then signal the exceptions that were raised in between (they may halt): exit through CHKERR. |
| **`FP68K_FINALIGN`** | `0x01E840` | `0x01CA34` | `res_pack_4.s:1472`<br>`res_pack_4.s:1474` | FP68K_IALIGN: extended; FP68K_FINALIGN common. |
| **`FP68K_FINALIGN_7`** | `0x01E84C` | `0x01CA40` | `res_pack_4.s:1480`<br>`res_pack_4.s:1482` | FP68K_FINALIGN_7 (Apple FINALIGN @7): shift right D0 bits to the new exponent. |
| **`FP68K_FPBEGIN`** | `0x01DFA0` | `0x01C194` | `res_pack_4.s:80`<br>`res_pack_4.s:82` | FP68K_FPBEGIN -- the entry of _FP68K: a frame whose -2(A6) word later holds the byte count to pop (LKCNT), all registers saved, A0 = FPState. |
| **`FP68K_FPCOM`** | `0x01DFD4` | `0x01C1C8` | `res_pack_4.s:115`<br>`res_pack_4.s:117` | FP68K_FPCOM -- decode the opword: odd opwords go to ODDBALL; for arithmetic add the OPMASKS bits, the precision control and the format fields, unpack the operands, then dispatch (ARITHOP). |
| **`FP68K_FPCOM_3`** | `0x01E02E` | `0x01C222` | `res_pack_4.s:155`<br>`res_pack_4.s:157` | — |
| **`FP68K_FPCOM_4`** | `0x01E054` | `0x01C248` | `res_pack_4.s:172`<br>`res_pack_4.s:174` | — |
| **`FP68K_FPCOM_6`** | `0x01E05C` | `0x01C250` | `res_pack_4.s:176`<br>`res_pack_4.s:178` | — |
| **`FP68K_FPNANOUT`** | `0x01E2AE` | `0x01C4A2` | `res_pack_4.s:531`<br>`res_pack_4.s:533` | FP68K_FPNANOUT: chop the NaN to the precision of the result; a NaN chopped to all-zero becomes code 21 (NANZERO). |
| **`FP68K_FPNANOUT_1`** | `0x01E2BA` | `0x01C4AE` | `res_pack_4.s:539`<br>`res_pack_4.s:541` | FP68K_FPNANOUT_1 (Apple FPNANOUT @1): double result? |
| **`FP68K_FPNANOUT_2`** | `0x01E2C4` | `0x01C4B8` | `res_pack_4.s:543`<br>`res_pack_4.s:545` | — |
| **`FP68K_FPNANOUT_3`** | `0x01E2D6` | `0x01C4CA` | `res_pack_4.s:551`<br>`res_pack_4.s:553` | — |
| **`FP68K_GETV`** | `0x01EA0A` | `0x01CBFE` | `res_pack_4.s:1763`<br>`res_pack_4.s:1765` | FP68K_GETV: the halt vector to (A1). |
| **`FP68K_GETW`** | `0x01EA00` | `0x01CBF4` | `res_pack_4.s:1753`<br>`res_pack_4.s:1755` | FP68K_GETW: getenv -- the environment word to (A1). |
| **`FP68K_GO1`** | `0x01EA1A` | `0x01CC0E` | `res_pack_4.s:1779`<br>`res_pack_4.s:1781` | FP68K_GO1: return, one address (POP1). Called by: FP68K_PUTW, FP68K_ENTRYP, FP68K_GETW, FP68K_PUTV, FP68K_GETV (and 2 more) |
| **`FP68K_IALIGN`** | `0x01E83E` | `0x01CA32` | `res_pack_4.s:1470`<br>`res_pack_4.s:1472` | FP68K_IALIGN: extended; FP68K_FINALIGN common. |
| **`FP68K_INVALIDOP`** | `0x01E232` | `0x01C426` | `res_pack_4.s:458`<br>`res_pack_4.s:460` | FP68K_INVALIDOP -- target of all invalid operations: signal invalid, deliver a quiet NaN with the code byte in D0 (NANADD 2, NANDIV 4, NANMUL 8, NANREM 9, NANSQRT 1, ...). |
| **`FP68K_IOFLOW`** | `0x01E880` | `0x01CA74` | `res_pack_4.s:1513`<br>`res_pack_4.s:1515` | FP68K_IOFLOW -- integer range check: limit $8000 (int16), $80000000 (int32), comp: the leading bit; the limit itself is allowed only for a negative value. Overflow: the limit (largest negative integer... |
| **`FP68K_IOFLOW_21`** | `0x01E892` | `0x01CA86` | `res_pack_4.s:1521`<br>`res_pack_4.s:1523` | — |
| **`FP68K_IOFLOW_23`** | `0x01E8A0` | `0x01CA94` | `res_pack_4.s:1529`<br>`res_pack_4.s:1531` | — |
| **`FP68K_IOFLOW_24`** | `0x01E8A8` | `0x01CA9C` | `res_pack_4.s:1534`<br>`res_pack_4.s:1536` | — |
| **`FP68K_IOFLOW_25`** | `0x01E8AA` | `0x01CA9E` | `res_pack_4.s:1538`<br>`res_pack_4.s:1540` | FP68K_IOFLOW_25 (Apple IOFLOW @25): overflow -- the limit value, invalid. |
| **`FP68K_IOFLOW_27`** | `0x01E8AC` | `0x01CAA0` | `res_pack_4.s:1540`<br>`res_pack_4.s:1542` | FP68K_IOFLOW_25 (Apple IOFLOW @25): overflow -- the limit value, invalid. |
| **`FP68K_IOFLOW_41`** | `0x01E8B6` | `0x01CAAA` | `res_pack_4.s:1544`<br>`res_pack_4.s:1546` | — |
| **`FP68K_IPALIGN`** | `0x01E828` | `0x01CA1C` | `res_pack_4.s:1456`<br>`res_pack_4.s:1458` | FP68K_IPALIGN -- put the binary point right of bit 23, 52 or 63 (single, double, extended): shift the fraction bits into D7. Returns LE if the value has no fraction bits (too big), GT if shifted. |
| **`FP68K_IPALIGN_1`** | `0x01E838` | `0x01CA2C` | `res_pack_4.s:1465`<br>`res_pack_4.s:1467` | FP68K_IPALIGN_1 (Apple IPALIGN @1): single. |
| **`FP68K_JAM1LSB`** | `0x01ED66` | `0x01CF5A` | `res_pack_4.s:2270`<br>`res_pack_4.s:2272` | FP68K_JAM1LSB: set the LSB of a finite result. |
| **`FP68K_LOGBTOP`** | `0x01E966` | `0x01CB5A` | `res_pack_4.s:1655`<br>`res_pack_4.s:1657` | FP68K_LOGBTOP -- logb: the unbiased exponent as a floating value; logb(+-0) = -inf with divide by zero, logb(+-inf) = +inf. |
| **`FP68K_LOGBTOP_1`** | `0x01E97C` | `0x01CB70` | `res_pack_4.s:1666`<br>`res_pack_4.s:1668` | FP68K_LOGBTOP_1 (Apple LOGBTOP @1): not zero. |
| **`FP68K_LOGBTOP_12`** | `0x01E994` | `0x01CB88` | `res_pack_4.s:1677`<br>`res_pack_4.s:1679` | — |
| **`FP68K_MINEXP`** | `0x01ED54` | `0x01CF48` | `res_pack_4.s:2259`<br>`res_pack_4.s:2261` | — |
| **`FP68K_MULCASE`** | `0x01E5CE` | `0x01C7C2` | `res_pack_4.s:1051`<br>`res_pack_4.s:1053` | FP68K_MULCASE: case routines by (dst, src), offsets from FP68K_MULTOP. |
| **`FP68K_MULNUM`** | `0x01E5E0` | `0x01C7D4` | `res_pack_4.s:1065`<br>`res_pack_4.s:1067` | FP68K_MULNUM -- two finite nonzero numbers: exponent = sum - ($3FFF - 1); the 64 x 64 bit product from four 32 x 32 products (MULU32), with shortcuts when the low halves are 0 (SRC32, BOTH32); the low... |
| **`FP68K_MULTOP`** | `0x01E5C2` | `0x01C7B6` | `res_pack_4.s:1044`<br>`res_pack_4.s:1046` | FP68K_MULTOP -- multiply: sign = XOR of the signs, NaN code 8 (NANMUL) in case of 0 * inf; dispatch by the number cases. |
| **`FP68K_MULU32`** | `0x01E630` | `0x01C824` | `res_pack_4.s:1108`<br>`res_pack_4.s:1110` | FP68K_MULU32 -- D4:D5 += D0 * D1 (32 x 32 bits, from four 16 x 16 MULUs), a carry out of D4 increments A0. Uses D2, D3, D6. |
| **`FP68K_MULU32_1`** | `0x01E660` | `0x01C854` | `res_pack_4.s:1133`<br>`res_pack_4.s:1135` | — |
| **`FP68K_NANCOERCE_21`** | `0x01E284` | `0x01C478` | `res_pack_4.s:501`<br>`res_pack_4.s:503` | — |
| **`FP68K_NANCOERCE_41`** | `0x01E28A` | `0x01C47E` | `res_pack_4.s:506`<br>`res_pack_4.s:508` | FP68K_NANCOERCE_41 (Apple NANCOERCE @41): comp result -- $80000000:00000000. |
| **`FP68K_NANDST`** | `0x01E262` | `0x01C456` | `res_pack_4.s:481`<br>`res_pack_4.s:483` | FP68K_NANDST: the dst NaN is the result. |
| **`FP68K_NANFLOAT`** | `0x01E28E` | `0x01C482` | `res_pack_4.s:511`<br>`res_pack_4.s:513` | FP68K_NANFLOAT: a floating result, or none (CMP, CLASS). |
| **`FP68K_NANFLOAT_5`** | `0x01E2A0` | `0x01C494` | `res_pack_4.s:521`<br>`res_pack_4.s:523` | FP68K_NANFLOAT_5 (Apple NANFLOAT @5): CLASS of a NaN -- 1 signaling (invalid was set by UNPACK: clear it again), 2 quiet. |
| **`FP68K_NANFLOAT_7`** | `0x01E2AA` | `0x01C49E` | `res_pack_4.s:526`<br>`res_pack_4.s:528` | — |
| **`FP68K_NANS`** | `0x01E246` | `0x01C43A` | `res_pack_4.s:469`<br>`res_pack_4.s:471` | FP68K_NANS -- at least one NaN operand: one NaN is the result; of two the one with the larger code byte (the src if equal). |
| **`FP68K_NANSRC`** | `0x01E26A` | `0x01C45E` | `res_pack_4.s:490`<br>`res_pack_4.s:492` | FP68K_NANSRC (Apple NANSRC/NANCOERCE) -- fit the NaN to the destination: an integer result gets the largest negative integer (invalid), a compare the result unordered, CLASS its class, a float result ... |
| **`FP68K_NEGZ`** | `0x01EA10` | `0x01CC04` | `res_pack_4.s:1769`<br>`res_pack_4.s:1771` | FP68K_NEGZ: negate -- flip the sign bit of the operand at (A1), any format. |
| **`FP68K_NEXTZ`** | `0x01EA3E` | `0x01CC32` | `res_pack_4.s:1813`<br>`res_pack_4.s:1815` | FP68K_NEXTZ -- nextafter: change the operand at (A2) (the "src", single, double or extended) by one unit in the last place toward the one at (A1); a NaN wins as in a multiply. Calls the package recurs... |
| **`FP68K_NORMCOERCE`** | `0x01E30C` | `0x01C500` | `res_pack_4.s:599`<br>`res_pack_4.s:601` | FP68K_NORMCOERCE: normalize a nonzero D4:D5:D7 (shift left, exponent - 1), then COERCE. Called by: FP68K_ZNORMCOERCE, FP68K_SUBMAG_7, FP68K_BOTH32 |
| **`FP68K_NORMCOERCE_1`** | `0x01E310` | `0x01C504` | `res_pack_4.s:606`<br>`res_pack_4.s:608` | FP68K_NORMCOERCE_1: normalize loop - left-shift until MSB set |
| **`FP68K_NORMCOERCE_2`** | `0x01E318` | `0x01C50C` | `res_pack_4.s:611`<br>`res_pack_4.s:613` | — |
| **`FP68K_NOTMINEXP`** | `0x01ED56` | `0x01CF4A` | `res_pack_4.s:2261`<br>`res_pack_4.s:2263` | — |
| **`FP68K_NXDEC`** | `0x01EB3C` | `0x01CD30` | `res_pack_4.s:1938`<br>`res_pack_4.s:1940` | FP68K_NXDEC -- decrement by one ulp; a zero (D4 = 0) is incremented instead with the sign flipped (next(-0, 3) = +min). |
| **`FP68K_NXDEC_201`** | `0x01EB4E` | `0x01CD42` | `res_pack_4.s:1950`<br>`res_pack_4.s:1952` | FP68K_NXDEC_201: decrement single by 1 ULP |
| **`FP68K_NXDEC_21`** | `0x01EB52` | `0x01CD46` | `res_pack_4.s:1957`<br>`res_pack_4.s:1959` | FP68K_NXDEC_21: decrement double by 1 ULP |
| **`FP68K_NXDEC_211`** | `0x01EB66` | `0x01CD5A` | `res_pack_4.s:1969`<br>`res_pack_4.s:1971` | FP68K_NXDEC_211: decrement double low word, borrow into high |
| **`FP68K_NXDEC_213`** | `0x01EB6E` | `0x01CD62` | `res_pack_4.s:1973`<br>`res_pack_4.s:1975` | — |
| **`FP68K_NXDEC_25`** | `0x01EB70` | `0x01CD64` | `res_pack_4.s:1979`<br>`res_pack_4.s:1981` | FP68K_NXDEC_25: decrement extended by 1 ULP |
| **`FP68K_NXDEC_251`** | `0x01EB7E` | `0x01CD72` | `res_pack_4.s:1989`<br>`res_pack_4.s:1991` | FP68K_NXDEC_251: decrement extended mantissa, handle borrow through exponent |
| **`FP68K_NXDEC_257`** | `0x01EB9C` | `0x01CD90` | `res_pack_4.s:2004`<br>`res_pack_4.s:2006` | FP68K_NXDEC_257: mantissa borrow into exponent |
| **`FP68K_NXDEC_258`** | `0x01EB9E` | `0x01CD92` | `res_pack_4.s:2006`<br>`res_pack_4.s:2008` | FP68K_NXDEC_257: mantissa borrow into exponent |
| **`FP68K_NXDEC_259`** | `0x01EBA0` | `0x01CD94` | `res_pack_4.s:2008`<br>`res_pack_4.s:2010` | — |
| **`FP68K_NXERR`** | `0x01EB06` | `0x01CCFA` | `res_pack_4.s:1908`<br>`res_pack_4.s:1910` | FP68K_NXERR -- classify the new value: infinity -> overflow + inexact, zero or denormal -> underflow + inexact. Called by: FP68K_NXINC, FP68K_NXDEC, FP68K_NXDEC_201, FP68K_NXDEC_21, FP68K_NXDEC_25 |
| **`FP68K_NXERR_1`** | `0x01EB1E` | `0x01CD12` | `res_pack_4.s:1918`<br>`res_pack_4.s:1920` | — |
| **`FP68K_NXERR_3`** | `0x01EB2A` | `0x01CD1E` | `res_pack_4.s:1927`<br>`res_pack_4.s:1929` | FP68K_NXERR_3 |
| **`FP68K_NXFIN`** | `0x01EB34` | `0x01CD28` | `res_pack_4.s:1932`<br>`res_pack_4.s:1934` | FP68K_NXFIN: drop the frame, exit through CHKERR. |
| **`FP68K_NXGREAT`** | `0x01EAC2` | `0x01CCB6` | `res_pack_4.s:1867`<br>`res_pack_4.s:1869` | FP68K_NXGREAT: src > dst -- decrement if positive, increment if negative. |
| **`FP68K_NXINC`** | `0x01EAC8` | `0x01CCBC` | `res_pack_4.s:1871`<br>`res_pack_4.s:1873` | FP68K_NXINC: increment by one ulp, per format. |
| **`FP68K_NXINC_11`** | `0x01EAD2` | `0x01CCC6` | `res_pack_4.s:1880`<br>`res_pack_4.s:1882` | FP68K_NXINC_11 |
| **`FP68K_NXINC_13`** | `0x01EAE0` | `0x01CCD4` | `res_pack_4.s:1886`<br>`res_pack_4.s:1888` | — |
| **`FP68K_NXINC_15`** | `0x01EAE2` | `0x01CCD6` | `res_pack_4.s:1891`<br>`res_pack_4.s:1893` | FP68K_NXINC_15 (Apple NXINC @15): extended -- an infinite result gets a 0 integer bit. |
| **`FP68K_NXINC_16`** | `0x01EB00` | `0x01CCF4` | `res_pack_4.s:1902`<br>`res_pack_4.s:1904` | — |
| **`FP68K_NXORD`** | `0x01EAB6` | `0x01CCAA` | `res_pack_4.s:1858`<br>`res_pack_4.s:1860` | FP68K_NXORD: ordered -- equal: done; else increment or decrement the src magnitude. |
| **`FP68K_ODDBALL`** | `0x01E9CC` | `0x01CBC0` | `res_pack_4.s:1719`<br>`res_pack_4.s:1721` | FP68K_ODDBALL -- odd opwords: A1 = address 1, A2 = address 2; D7 = opword AND $1E = (operation - 1) indexes ODDTAB. |
| **`FP68K_ODDTAB`** | `0x01E9DA` | `0x01CBCE` | `res_pack_4.s:1725`<br>`res_pack_4.s:1727` | FP68K_ODDTAB: routines for the odd operations, offsets from FP68K_ODDBALL. |
| **`FP68K_OFLOW`** | `0x01E3A8` | `0x01C59C` | `res_pack_4.s:720`<br>`res_pack_4.s:722` | FP68K_OFLOW -- if the exponent A4 is above the threshold A3: signal overflow and inexact, result infinity; returns EQ to keep infinity, NE if the largest finite value ("huge") must be stored instead (... |
| **`FP68K_OFLOW_1`** | `0x01E3B0` | `0x01C5A4` | `res_pack_4.s:725`<br>`res_pack_4.s:727` | — |
| **`FP68K_OFLOW_2`** | `0x01E3CA` | `0x01C5BE` | `res_pack_4.s:737`<br>`res_pack_4.s:739` | FP68K_OFLOW_2 (Apple OFLOW @2): directed rounding. |
| **`FP68K_OFLOW_4`** | `0x01E3D4` | `0x01C5C8` | `res_pack_4.s:744`<br>`res_pack_4.s:746` | FP68K_OFLOW_4 (Apple OFLOW @4): upward or downward -- depends on the sign. |
| **`FP68K_OFLOW_5`** | `0x01E3DE` | `0x01C5D2` | `res_pack_4.s:751`<br>`res_pack_4.s:753` | FP68K_OFLOW_5 (Apple OFLOW @5): negative overflow. |
| **`FP68K_OPMASKS`** | `0x01DFAE` | `0x01C1A2` | `res_pack_4.s:89`<br>`res_pack_4.s:91` | FP68K_OPMASKS: information bits ORed into the opword, per operation (index = opword AND $1E): $80 dst in, $40 src in, $20 dst out, $100 the format field governs the dst, $01 two addresses. |
| **`FP68K_PACK`** | `0x01E460` | `0x01C654` | `res_pack_4.s:813`<br>`res_pack_4.s:815` | FP68K_PACK -- store the result (sign D6 bit 7, exponent A4, significand D4:D5) at the dst address in the format code * 2 in D0; EQ on entry to the format routine means infinity or NaN. |
| **`FP68K_PACKC64`** | `0x01E48C` | `0x01C680` | `res_pack_4.s:841`<br>`res_pack_4.s:843` | FP68K_PACKC64: comp. |
| **`FP68K_PACKCASE`** | `0x01E476` | `0x01C66A` | `res_pack_4.s:822`<br>`res_pack_4.s:824` | FP68K_PACKCASE: pack routine per format, offsets from FP68K_PACK. |
| **`FP68K_PACKDBL`** | `0x01E4E6` | `0x01C6DA` | `res_pack_4.s:905`<br>`res_pack_4.s:907` | FP68K_PACKDBL: double -- likewise with 11 exponent bits, the significand shifted right by 11. |
| **`FP68K_PACKDBL_1`** | `0x01E4EE` | `0x01C6E2` | `res_pack_4.s:911`<br>`res_pack_4.s:913` | FP68K_PACKDBL_1 (Apple PACKDBL @1): finite. |
| **`FP68K_PACKDBL_5`** | `0x01E4F6` | `0x01C6EA` | `res_pack_4.s:915`<br>`res_pack_4.s:917` | — |
| **`FP68K_PACKDBL_7`** | `0x01E500` | `0x01C6F4` | `res_pack_4.s:920`<br>`res_pack_4.s:922` | — |
| **`FP68K_PACKEXT`** | `0x01E492` | `0x01C686` | `res_pack_4.s:848`<br>`res_pack_4.s:850` | FP68K_PACKEXT: extended -- an underflowed (single or double precision control) denormal is normalized again first. |
| **`FP68K_PACKEXT_1`** | `0x01E4A8` | `0x01C69C` | `res_pack_4.s:861`<br>`res_pack_4.s:863` | FP68K_PACKEXT_1 (Apple PACKEXT @1): normalize. |
| **`FP68K_PACKEXT_11`** | `0x01E4B8` | `0x01C6AC` | `res_pack_4.s:871`<br>`res_pack_4.s:873` | — |
| **`FP68K_PACKEXT_5`** | `0x01E4AE` | `0x01C6A2` | `res_pack_4.s:865`<br>`res_pack_4.s:867` | — |
| **`FP68K_PACKEXT_7`** | `0x01E4B0` | `0x01C6A4` | `res_pack_4.s:867`<br>`res_pack_4.s:869` | — |
| **`FP68K_PACKI16`** | `0x01E484` | `0x01C678` | `res_pack_4.s:831`<br>`res_pack_4.s:833` | FP68K_PACKI16: int16. |
| **`FP68K_PACKI32`** | `0x01E488` | `0x01C67C` | `res_pack_4.s:836`<br>`res_pack_4.s:838` | FP68K_PACKI32: int32. |
| **`FP68K_PACKSGL`** | `0x01E4C0` | `0x01C6B4` | `res_pack_4.s:880`<br>`res_pack_4.s:882` | FP68K_PACKSGL: single -- exponent rebiased, the integer bit dropped (a denormal decrements the exponent to 0), sign inserted; infinity and NaN get an exponent that becomes $FF. |
| **`FP68K_PACKSGL_1`** | `0x01E4C8` | `0x01C6BC` | `res_pack_4.s:886`<br>`res_pack_4.s:888` | FP68K_PACKSGL_1 (Apple PACKSGL @1): finite. |
| **`FP68K_PACKSGL_5`** | `0x01E4D0` | `0x01C6C4` | `res_pack_4.s:890`<br>`res_pack_4.s:892` | — |
| **`FP68K_PACKSGL_7`** | `0x01E4DA` | `0x01C6CE` | `res_pack_4.s:895`<br>`res_pack_4.s:897` | — |
| **`FP68K_PASTHALT`** | `0x01E0CA` | `0x01C2BE` | `res_pack_4.s:233`<br>`res_pack_4.s:235` | — |
| **`FP68K_POP1`** | `0x01E0D6` | `0x01C2CA` | `res_pack_4.s:243`<br>`res_pack_4.s:245` | FP68K_POP1: one address -- pop opword and address. |
| **`FP68K_POP2`** | `0x01E0D0` | `0x01C2C4` | `res_pack_4.s:237`<br>`res_pack_4.s:239` | FP68K_POP2: two addresses -- pop 10 bytes. |
| **`FP68K_POP3`** | `0x01E0F0` | `0x01C2E4` | `res_pack_4.s:259`<br>`res_pack_4.s:261` | FP68K_POP3: three addresses (binary to decimal only). |
| **`FP68K_POPIT`** | `0x01E0DA` | `0x01C2CE` | `res_pack_4.s:249`<br>`res_pack_4.s:251` | FP68K_POPIT -- D0 = bytes to pop at the end (LKCNT), D1 = frame offset of the slot that gets the return address (the last address parameter); unlink by hand, set the CCR, restore the registers, pop. |
| **`FP68K_POW10`** | `0x01EDF4` | `0x01CFE8` | `res_pack_4.s:2301`<br>`res_pack_4.s:2303` | FP68K_POW10 -- 10^\|D3\| into the extended at (A1): below 15 straight from TAB10S, else the product of TAB10 entries (exponents above 5000 are held at 5000: overflow), each corrected by its rounding err... |
| **`FP68K_POW10_1`** | `0x01EDFC` | `0x01CFF0` | `res_pack_4.s:2306`<br>`res_pack_4.s:2308` | — |
| **`FP68K_POW10_10`** | `0x01EE0C` | `0x01D000` | `res_pack_4.s:2312`<br>`res_pack_4.s:2314` | — |
| **`FP68K_PREPACK`** | `0x01E092` | `0x01C286` | `res_pack_4.s:208`<br>`res_pack_4.s:210` | FP68K_PREPACK -- the operation is done: store the result in the destination format unless the operation has no output (compares). |
| **`FP68K_PTLOOP`** | `0x01EE10` | `0x01D004` | `res_pack_4.s:2315`<br>`res_pack_4.s:2317` | FP68K_PTLOOP: next table entry. |
| **`FP68K_PTLOOP_13`** | `0x01EE2A` | `0x01D01E` | `res_pack_4.s:2331`<br>`res_pack_4.s:2333` | FP68K_PTLOOP_13 |
| **`FP68K_PTLOOP_15`** | `0x01EE34` | `0x01D028` | `res_pack_4.s:2338`<br>`res_pack_4.s:2340` | FP68K_PTLOOP_15 (Apple POW10 @15): correct the table value by one LSB, on a copy on the stack. |
| **`FP68K_PTLOOP_21`** | `0x01EE42` | `0x01D036` | `res_pack_4.s:2349`<br>`res_pack_4.s:2351` | FP68K_PTLOOP_21 |
| **`FP68K_PTLOOP_23`** | `0x01EE44` | `0x01D038` | `res_pack_4.s:2351`<br>`res_pack_4.s:2353` | — |
| **`FP68K_PTLOOP_31`** | `0x01EE58` | `0x01D04C` | `res_pack_4.s:2363`<br>`res_pack_4.s:2365` | FP68K_PTLOOP_31 (Apple POW10 @31): the table value as it is. |
| **`FP68K_PTLOOP_33`** | `0x01EE5C` | `0x01D050` | `res_pack_4.s:2366`<br>`res_pack_4.s:2368` | — |
| **`FP68K_PTMUL`** | `0x01EE6E` | `0x01D062` | `res_pack_4.s:2377`<br>`res_pack_4.s:2379` | FP68K_PTMUL: (A1) := (A2), or (A1) * (A2) when D1 bit 31 is set. |
| **`FP68K_PTMUL_42`** | `0x01EE80` | `0x01D074` | `res_pack_4.s:2389`<br>`res_pack_4.s:2391` | FP68K_PTMUL_42 |
| **`FP68K_PTQUICK`** | `0x01EE66` | `0x01D05A` | `res_pack_4.s:2372`<br>`res_pack_4.s:2374` | — |
| **`FP68K_PTSKIP`** | `0x01EE5E` | `0x01D052` | `res_pack_4.s:2368`<br>`res_pack_4.s:2370` | — |
| **`FP68K_PUTV`** | `0x01EA04` | `0x01CBF8` | `res_pack_4.s:1758`<br>`res_pack_4.s:1760` | FP68K_PUTV: set the halt vector from (A1). |
| **`FP68K_PUTW`** | `0x01E9F6` | `0x01CBEA` | `res_pack_4.s:1741`<br>`res_pack_4.s:1743` | FP68K_PUTW: setenv -- environment := the word at (A1). |
| **`FP68K_QRTSHIFT`** | `0x01E2EC` | `0x01C4E0` | `res_pack_4.s:574`<br>`res_pack_4.s:576` | — |
| **`FP68K_RDST`** | `0x01E2DA` | `0x01C4CE` | `res_pack_4.s:560`<br>`res_pack_4.s:562` | — |
| **`FP68K_RDSTSGN`** | `0x01E2D8` | `0x01C4CC` | `res_pack_4.s:558`<br>`res_pack_4.s:560` | FP68K_RDSTSGN: result := the dst operand with its sign; FP68K_RDST: the dst without its sign; FP68K_RSRCSGN (RSRC): the src, which is in D4:D5/A4 already. Case routines for "the result is one of the o... |
| **`FP68K_REFP68K`** | `0x01DFCC` | `0x01C1C0` | `res_pack_4.s:109`<br>`res_pack_4.s:111` | FP68K_REFP68K -- second entry, for calls from inside the package: like FPBEGIN, but A0 already points to the state. Called by: FP68K_NEXTZ, FP68K_NXERR, FP68K_DBSTORE, FP68K_DBCORE_5, FP68K_NOTMINEXP ... |
| **`FP68K_REMCASE`** | `0x01E710` | `0x01C904` | `res_pack_4.s:1253`<br>`res_pack_4.s:1255` | FP68K_REMCASE: case routines by (dst, src), offsets from FP68K_REMTOP. |
| **`FP68K_REMDIV`** | `0x01E732` | `0x01C926` | `res_pack_4.s:1281`<br>`res_pack_4.s:1283` | FP68K_REMDIV -- divide through the first fraction bit; low quotient bit 1 and remainder > 0 (or = 0 with an odd quotient): the remainder becomes divisor - remainder with the sign flipped and the quoti... |
| **`FP68K_REMDIV_3`** | `0x01E752` | `0x01C946` | `res_pack_4.s:1296`<br>`res_pack_4.s:1298` | — |
| **`FP68K_REMDIV_5`** | `0x01E758` | `0x01C94C` | `res_pack_4.s:1299`<br>`res_pack_4.s:1301` | — |
| **`FP68K_REMDST`** | `0x01E72A` | `0x01C91E` | `res_pack_4.s:1271`<br>`res_pack_4.s:1273` | FP68K_REMDST: the dst is the remainder. |
| **`FP68K_REMFIN`** | `0x01E774` | `0x01C968` | `res_pack_4.s:1316`<br>`res_pack_4.s:1318` | FP68K_REMFIN: store the remainder (ZNORMCOERCE). |
| **`FP68K_REMNUM`** | `0x01E722` | `0x01C916` | `res_pack_4.s:1265`<br>`res_pack_4.s:1267` | FP68K_REMNUM: finite / finite -- DEXP - SEXP + 2 quotient bits are needed; none: the dst is the remainder. |
| **`FP68K_REMQUO`** | `0x01E760` | `0x01C954` | `res_pack_4.s:1305`<br>`res_pack_4.s:1307` | FP68K_REMQUO: store the quotient bits (sign from D6 bit 6). |
| **`FP68K_REMQUO_9`** | `0x01E76A` | `0x01C95E` | `res_pack_4.s:1310`<br>`res_pack_4.s:1312` | — |
| **`FP68K_REMTOP`** | `0x01E6FA` | `0x01C8EE` | `res_pack_4.s:1244`<br>`res_pack_4.s:1246` | FP68K_REMTOP -- IEEE remainder dst REM src, at most half the divisor in magnitude; the low 7 bits of the integer quotient, with its sign, go to the caller in D0 (the saved D0.W at 6(SP)). Precision co... |
| **`FP68K_RESTORE`** | `0x01E6D6` | `0x01C8CA` | `res_pack_4.s:1213`<br>`res_pack_4.s:1215` | FP68K_RESTORE -- restoring division: D0 quotient bits of D1:D2 / D3:A2 into D4:D5 (the leading ones are shifted out), remainder left in D1:D2. Also used by REM and binary-to-decimal. Called by: FP68K_... |
| **`FP68K_RESTORE_1`** | `0x01E6DC` | `0x01C8D0` | `res_pack_4.s:1219`<br>`res_pack_4.s:1221` | FP68K_RESTORE_1 (Apple RESTORE @1): shift quotient and remainder left. |
| **`FP68K_RESTORE_2`** | `0x01E6E6` | `0x01C8DA` | `res_pack_4.s:1225`<br>`res_pack_4.s:1227` | — |
| **`FP68K_RESTORE_3`** | `0x01E6EC` | `0x01C8E0` | `res_pack_4.s:1229`<br>`res_pack_4.s:1231` | — |
| **`FP68K_RESTORE_4`** | `0x01E6EE` | `0x01C8E2` | `res_pack_4.s:1231`<br>`res_pack_4.s:1233` | — |
| **`FP68K_RESTORE_5`** | `0x01E6F4` | `0x01C8E8` | `res_pack_4.s:1235`<br>`res_pack_4.s:1237` | — |
| **`FP68K_RINT`** | `0x01E7EC` | `0x01C9E0` | `res_pack_4.s:1406`<br>`res_pack_4.s:1408` | FP68K_RINT -- round to an integral value in the current rounding direction: align the binary point (IPALIGN) and coerce. |
| **`FP68K_RINT_1`** | `0x01E7F2` | `0x01C9E6` | `res_pack_4.s:1412`<br>`res_pack_4.s:1414` | FP68K_RINT_1 (Apple RINT @1): finite nonzero. |
| **`FP68K_ROUND`** | `0x01E356` | `0x01C54A` | `res_pack_4.s:659`<br>`res_pack_4.s:661` | FP68K_ROUND -- round D4:D5 by the guard and sticky bits in D7.W; Z = NOT LSB on entry (BTST by the caller), D1:D2 = the increment for one LSB. Exact: clear the underflow signal; else signal inexact an... |
| **`FP68K_ROUND_1`** | `0x01E362` | `0x01C556` | `res_pack_4.s:667`<br>`res_pack_4.s:669` | FP68K_ROUND_1 (Apple ROUND @1): inexact -- by rounding direction. |
| **`FP68K_ROUND_3`** | `0x01E374` | `0x01C568` | `res_pack_4.s:676`<br>`res_pack_4.s:678` | FP68K_ROUND_3 (Apple ROUND @3): upward -- round up if positive. |
| **`FP68K_ROUND_5`** | `0x01E37A` | `0x01C56E` | `res_pack_4.s:682`<br>`res_pack_4.s:684` | FP68K_ROUND_5 (Apple ROUND @5): to nearest or downward. |
| **`FP68K_ROUND_51`** | `0x01E388` | `0x01C57C` | `res_pack_4.s:691`<br>`res_pack_4.s:693` | FP68K_ROUND_51 (Apple ROUND @51): at least one half -- more: up; exactly one half: up only if the LSB is 1 (to even). |
| **`FP68K_ROUND_7`** | `0x01E390` | `0x01C584` | `res_pack_4.s:699`<br>`res_pack_4.s:701` | FP68K_ROUND_7 (Apple ROUND @7): downward -- round up the magnitude if negative. |
| **`FP68K_ROUNDUP`** | `0x01E396` | `0x01C58A` | `res_pack_4.s:706`<br>`res_pack_4.s:708` | FP68K_ROUNDUP -- add the increment D1:D2; a carry out shifts right and bumps the exponent; RNDINC records the increment. |
| **`FP68K_ROUNDUP_9`** | `0x01E3A6` | `0x01C59A` | `res_pack_4.s:713`<br>`res_pack_4.s:715` | — |
| **`FP68K_RSRCSGN`** | `0x01E2E0` | `0x01C4D4` | `res_pack_4.s:564`<br>`res_pack_4.s:566` | — |
| **`FP68K_RTSHIFT`** | `0x01E2E2` | `0x01C4D6` | `res_pack_4.s:570`<br>`res_pack_4.s:572` | FP68K_RTSHIFT -- shift D4:D5 right D0 bits (at most 66) into D7; the bits shifted out of D7 are sticky in D7 bit 0. FP68K_QRTSHIFT: without the limit. |
| **`FP68K_SCALBTOP`** | `0x01E99C` | `0x01CB90` | `res_pack_4.s:1683`<br>`res_pack_4.s:1685` | FP68K_SCALBTOP -- scalb: x * 2^n, the int16 n at the second address: add n to the exponent and coerce; 0 and inf unchanged. |
| **`FP68K_SCALBTOP_1`** | `0x01E9A2` | `0x01CB96` | `res_pack_4.s:1689`<br>`res_pack_4.s:1691` | FP68K_SCALBTOP_1 (Apple SCALBTOP @1): finite nonzero. |
| **`FP68K_SCOERCE`** | `0x01E3E4` | `0x01C5D8` | `res_pack_4.s:758`<br>`res_pack_4.s:760` | FP68K_SCOERCE -- coerce to single: underflow threshold $3F81, 24-bit significand (bits below into the sticky bits), increment $100, overflow threshold $407E, huge = 24 ones. |
| **`FP68K_SCOERCE_3`** | `0x01E41A` | `0x01C60E` | `res_pack_4.s:779`<br>`res_pack_4.s:781` | — |
| **`FP68K_SETXCP`** | `0x01EBA4` | `0x01CD98` | `res_pack_4.s:2013`<br>`res_pack_4.s:2015` | FP68K_SETXCP -- signal the exception whose number is the word at (A1), with the halt if it is enabled: exit through CHKERR. |
| **`FP68K_SIGDIGS`** | `0x01EC6A` | `0x01CE5E` | `res_pack_4.s:2131`<br>`res_pack_4.s:2133` | FP68K_SIGDIGS: digits into D4:D5; the 20th goes to D7.B for rounding (TRAILDIG). |
| **`FP68K_SQRTTOP`** | `0x01E8C0` | `0x01CAB4` | `res_pack_4.s:1555`<br>`res_pack_4.s:1557` | FP68K_SQRTTOP -- square root: +-0 and +inf are their own roots, negative operands invalid (NANSQRT 1); otherwise halve the exponent and extract the root bit by bit (restoring, two radicand bits per st... |
| **`FP68K_SQRTTOP_1`** | `0x01E8C8` | `0x01CABC` | `res_pack_4.s:1561`<br>`res_pack_4.s:1563` | FP68K_SQRTTOP_1 (Apple SQRTTOP @1): not zero. |
| **`FP68K_SQRTTOP_10`** | `0x01E8D8` | `0x01CACC` | `res_pack_4.s:1571`<br>`res_pack_4.s:1573` | FP68K_SQRTTOP_10 (Apple SQRTTOP @10): finite positive. Root in D0.B:D4:D5, radicand in D1.B:D2:D3:D6:D7, step counter in A3. |
| **`FP68K_SQRTTOP_12`** | `0x01E8E2` | `0x01CAD6` | `res_pack_4.s:1577`<br>`res_pack_4.s:1579` | — |
| **`FP68K_SQRTTOP_14`** | `0x01E904` | `0x01CAF8` | `res_pack_4.s:1594`<br>`res_pack_4.s:1596` | — |
| **`FP68K_SQRTTOP_20`** | `0x01E912` | `0x01CB06` | `res_pack_4.s:1604`<br>`res_pack_4.s:1606` | FP68K_SQRTTOP_20 (Apple SQRTTOP @20): one root bit -- radicand left 2 bits, root <root>1 -> <root>01, try radicand - root. |
| **`FP68K_SQRTTOP_22`** | `0x01E93E` | `0x01CB32` | `res_pack_4.s:1629`<br>`res_pack_4.s:1631` | FP68K_SQRTTOP_22 (Apple SQRTTOP @22): the root bit is 1. |
| **`FP68K_SQRTTOP_24`** | `0x01E940` | `0x01CB34` | `res_pack_4.s:1631`<br>`res_pack_4.s:1633` | FP68K_SQRTTOP_22 (Apple SQRTTOP @22): the root bit is 1. |
| **`FP68K_SQRTTOP_30`** | `0x01E954` | `0x01CB48` | `res_pack_4.s:1642`<br>`res_pack_4.s:1644` | — |
| **`FP68K_SQRTTOP_32`** | `0x01E956` | `0x01CB4A` | `res_pack_4.s:1644`<br>`res_pack_4.s:1646` | — |
| **`FP68K_SRC32`** | `0x01E60E` | `0x01C802` | `res_pack_4.s:1088`<br>`res_pack_4.s:1090` | — |
| **`FP68K_SRC64`** | `0x01E5FC` | `0x01C7F0` | `res_pack_4.s:1078`<br>`res_pack_4.s:1080` | — |
| **`FP68K_SUBMAG`** | `0x01E578` | `0x01C76C` | `res_pack_4.s:991`<br>`res_pack_4.s:993` | FP68K_SUBMAG -- subtract the larger from the smaller; zero -> a signed zero; a borrow means the guess was wrong: negate back. |
| **`FP68K_SUBMAG_7`** | `0x01E58A` | `0x01C77E` | `res_pack_4.s:1001`<br>`res_pack_4.s:1003` | — |
| **`FP68K_SUBTOP`** | `0x01E524` | `0x01C718` | `res_pack_4.s:939`<br>`res_pack_4.s:941` | FP68K_SUBTOP -- subtract: flip the src sign (bit 7) and the XOR (bit 5), then add. |
| **`FP68K_TAB10`** | `0x01ED76` | `0x01CF6A` | `res_pack_4.s:2284`<br>`res_pack_4.s:2286` | FP68K_TAB10: powers of ten for POW10, 7 words per entry: N, the rounding error of the table value (+1 rounded up, -1 down, 0 exact), then 10^N in extended. Searched from the top entry (POWER_TBL, Appl... |
| **`FP68K_TAB10S`** | `0x01EE90` | `0x01D084` | `res_pack_4.s:2400`<br>`res_pack_4.s:2402` | FP68K_TAB10S: 10^0 .. 10^14, exact, in extended. |
| **`FP68K_TESTXCP`** | `0x01EA1E` | `0x01CC12` | `res_pack_4.s:1784`<br>`res_pack_4.s:1786` | FP68K_TESTXCP -- test the exception whose number (0-4) is the word at (A1): the byte at (A1) := 1 if its flag is set, else 0. |
| **`FP68K_TINT`** | `0x01E7F8` | `0x01C9EC` | `res_pack_4.s:1419`<br>`res_pack_4.s:1421` | FP68K_TINT -- truncate to an integral value: as RINT with the direction forced to toward zero. |
| **`FP68K_TINT_1`** | `0x01E7FE` | `0x01C9F2` | `res_pack_4.s:1426`<br>`res_pack_4.s:1428` | FP68K_TINT_1 (Apple TINT @1): finite nonzero. (Apple's source notes a bug comment about the chop encoding; the code sets 11, toward zero.) |
| **`FP68K_TOA3`** | `0x01ECC2` | `0x01CEB6` | `res_pack_4.s:2179`<br>`res_pack_4.s:2181` | FP68K_TOA3: store D0.W:D4:D5 as an extended at (A3). |
| **`FP68K_UFLOW`** | `0x01E346` | `0x01C53A` | `res_pack_4.s:643`<br>`res_pack_4.s:645` | FP68K_UFLOW -- if the exponent A4 is below the threshold A3, signal underflow and denormalize: shift right to exponent A3. (The signal is withdrawn by ROUND if the result is exact.) |
| **`FP68K_UFLOW_1`** | `0x01E34E` | `0x01C542` | `res_pack_4.s:650`<br>`res_pack_4.s:652` | FP68K_UFLOW_1 (Apple UFLOW @1): tiny result. |
| **`FP68K_UNP0`** | `0x01E184` | `0x01C378` | `res_pack_4.s:358`<br>`res_pack_4.s:360` | FP68K_UNP0: zero -- A4 = 0, D3 += 2. |
| **`FP68K_UNPACK`** | `0x01E0F6` | `0x01C2EA` | `res_pack_4.s:272`<br>`res_pack_4.s:274` | FP68K_UNPACK -- unpack the operand at A3, format code * 2 in D0 (dirty), into the internal form: sign in D6 bit 7, significand in D4:D5 (normalized, integer bit 31 of D4), exponent in A4 (biased $3FFF... |
| **`FP68K_UNPACK_EXPONENT`** | `0x01E984` | `0x01CB78` | `res_pack_4.s:1670`<br>`res_pack_4.s:1672` | — |
| **`FP68K_UNPC64`** | `0x01E122` | `0x01C316` | `res_pack_4.s:302`<br>`res_pack_4.s:304` | FP68K_UNPC64: comp -- in D4:D5, exponent 63; the comp NaN $80000000:00000000 becomes a quiet NaN with code 20 (NANCOMP). |
| **`FP68K_UNPC64_7`** | `0x01E130` | `0x01C324` | `res_pack_4.s:311`<br>`res_pack_4.s:313` | FP68K_UNPC64_7 (Apple UNPC64 @7): low half 0 -- the comp NaN? |
| **`FP68K_UNPCASE`** | `0x01E106` | `0x01C2FA` | `res_pack_4.s:280`<br>`res_pack_4.s:282` | FP68K_UNPCASE: unpack routine per format, offsets from FP68K_UNPACK. |
| **`FP68K_UNPCGEN`** | `0x01E14A` | `0x01C33E` | `res_pack_4.s:326`<br>`res_pack_4.s:328` | — |
| **`FP68K_UNPCGEN_9`** | `0x01E154` | `0x01C348` | `res_pack_4.s:331`<br>`res_pack_4.s:333` | — |
| **`FP68K_UNPCUNR`** | `0x01E18E` | `0x01C382` | `res_pack_4.s:367`<br>`res_pack_4.s:369` | — |
| **`FP68K_UNPDBL`** | `0x01E1E8` | `0x01C3DC` | `res_pack_4.s:425`<br>`res_pack_4.s:427` | FP68K_UNPDBL: double -- sign to D6, align the 52-bit fraction left by 11, 11-bit exponent rebiased by $3C00, implicit 1. |
| **`FP68K_UNPDBL_25`** | `0x01E1F0` | `0x01C3E4` | `res_pack_4.s:429`<br>`res_pack_4.s:431` | — |
| **`FP68K_UNPDBL_31`** | `0x01E21E` | `0x01C412` | `res_pack_4.s:449`<br>`res_pack_4.s:451` | FP68K_UNPDBL_31 (Apple UNPDBL @31): nonzero exponent -- infinity/NaN or normalized. |
| **`FP68K_UNPEXT`** | `0x01E15E` | `0x01C352` | `res_pack_4.s:339`<br>`res_pack_4.s:341` | FP68K_UNPEXT: extended -- split off the sign, check for $7FFF (infinity, NaN), zero and unnormalized values. |
| **`FP68K_UNPEXT_13`** | `0x01E16A` | `0x01C35E` | `res_pack_4.s:344`<br>`res_pack_4.s:346` | — |
| **`FP68K_UNPI16`** | `0x01E114` | `0x01C308` | `res_pack_4.s:289`<br>`res_pack_4.s:291` | FP68K_UNPI16: int16 -- left-aligned in D4, exponent 15. |
| **`FP68K_UNPI32`** | `0x01E11C` | `0x01C310` | `res_pack_4.s:295`<br>`res_pack_4.s:297` | FP68K_UNPI32: int32 -- in D4, exponent 31. |
| **`FP68K_UNPIGEN`** | `0x01E146` | `0x01C33A` | `res_pack_4.s:323`<br>`res_pack_4.s:325` | comp NaN: encode as extended NaN FP68K_UNPIGEN: integer -- 0 is a zero; else take the magnitude (sign to D6), bias the exponent and normalize. |
| **`FP68K_UNPNAN`** | `0x01E1B0` | `0x01C3A4` | `res_pack_4.s:390`<br>`res_pack_4.s:392` | FP68K_UNPNAN: NaN -- set the quiet bit (bit 30); if it was clear the NaN was signaling: invalid. D2 += 2. |
| **`FP68K_UNPNAN_1`** | `0x01E1BA` | `0x01C3AE` | `res_pack_4.s:394`<br>`res_pack_4.s:396` | FP68K_UNPNAN: NaN -- set the quiet bit (bit 30); if it was clear the NaN was signaling: invalid. D2 += 2. |
| **`FP68K_UNPNIN`** | `0x01E19C` | `0x01C390` | `res_pack_4.s:378`<br>`res_pack_4.s:380` | FP68K_UNPNIN: maximum exponent -- infinity (D3 += 4) or NaN. |
| **`FP68K_UNPNRM`** | `0x01E196` | `0x01C38A` | `res_pack_4.s:372`<br>`res_pack_4.s:374` | — |
| **`FP68K_UNPSGL`** | `0x01E1BE` | `0x01C3B2` | `res_pack_4.s:400`<br>`res_pack_4.s:402` | FP68K_UNPSGL: single -- sign to D6, 8-bit exponent rebiased by $3F80, implicit leading 1; exponent 0 is zero or denormal, $FF infinity or NaN. |
| **`FP68K_UNPSGL_21`** | `0x01E1E0` | `0x01C3D4` | `res_pack_4.s:418`<br>`res_pack_4.s:420` | FP68K_UNPSGL_21 (Apple UNPSGL @21): single with exponent 0 -- zero or denormal (no implicit bit, exponent $3F81). |
| **`FP68K_UNPUNR`** | `0x01E18A` | `0x01C37E` | `res_pack_4.s:365`<br>`res_pack_4.s:367` | FP68K_UNPUNR: unnormalized -- mark D3 bit 31, normalize (FP68K_UNPCUNR, Apple UNPCUNR, also the entry for integers). |
| **`FP68K_UNPZUN`** | `0x01E17C` | `0x01C370` | `res_pack_4.s:352`<br>`res_pack_4.s:354` | FP68K_UNPZUN: zero or unnormalized? |
| **`FP68K_ZEROSUM`** | `0x01E594` | `0x01C788` | `res_pack_4.s:1009`<br>`res_pack_4.s:1011` | — |
| **`FP68K_ZNORMCOERCE`** | `0x01E2FC` | `0x01C4F0` | `res_pack_4.s:586`<br>`res_pack_4.s:588` | FP68K_ZNORMCOERCE -- a zero result keeps exponent 0 and is never coerced; anything else is normalized and coerced. |
| **`GETREQUEST`** | `0x019F78` | `0x0326DE` | `res_drvr_atp.s:333`<br>`res_drvr_atp.s:440` | GETREQUEST GetRequest (csCode 253): queue the call on responding socket atpSocket (D2 = slot) until a request arrives; ATP_LISTENER_DELIVER fills in userData, atpFlags, addrBlock, reqLength, bitMap an... |
| **`GETREQUEST_APPEND`** | `0x019F8C` | — | `res_drvr_atp.s:345` | link the call in at the end (its qLink is cleared below) |
| **`GETREQUEST_LOOP`** | `0x019F84` | — | `res_drvr_atp.s:339` | append the call at the end of the queue, interrupts off |
| **`INITDSK2`** | `0x017D6A` | `0x0346BA` | `res_drvr_sony.s:115`<br>`res_drvr_sony_fdhd.s:246` | InitDsk2 -- three more vectors, stored from JDiskSel ($B40) on |
| **`INITDSKMFM`** | — | — | `res_drvr_sony_fdhd.s:251` | InitDskMFM -- the three MFM vectors (new), stored from jMRdAddr ($680) on |
| **`INITDSKTBL`** | `0x017D4C` | `0x03469C` | `res_drvr_sony.s:98`<br>`res_drvr_sony_fdhd.s:229` | InitDskTbl -- word offsets (relative to INITDSKTBL) of the disk routines whose addresses DiskOpen stores in the 15 jump vectors of DiskVars (JFigTrkSpd..NiblTbl, $222-$25A). Patches can redirect a rou... |
| **`INITPARAMS`** | `0x017D70` | `0x0346C0` | `res_drvr_sony.s:122`<br>`res_drvr_sony_fdhd.s:257` | InitParams -- tuneable drive constants, copied into SonyVars from ReadErrInit (+$2A) on (32 bytes; the values of sonyequ.inc, section "Floppy drive constants") |
| **`K`** | — | `0x038400` | `res_kchr.s:123` | — |
| **`KILLGETREQ`** | — | `0x032730` | `res_drvr_atp.s:493` | KillGetReq (csCode 257): abort the GetRequest at aKillQEl: unlink it from the GetRequest queue of its socket and complete it with reqAborted; the KillGetReq call completes with noErr, or cbNotFound if... |
| **`KILLGETREQ_EXIT`** | — | `0x03277A` | `res_drvr_atp.s:525` | — |
| **`KILLGETREQ_FOUND`** | — | `0x032766` | `res_drvr_atp.s:516` | unlink it and complete it with reqAborted |
| **`KILLGETREQ_LOOP`** | — | `0x032756` | `res_drvr_atp.s:507` | — |
| **`KILLGETREQ_NOTFOUND`** | — | `0x032778` | `res_drvr_atp.s:523` | — |
| **`KILLGETREQ_SKTLOOP`** | — | `0x032740` | `res_drvr_atp.s:499` | — |
| **`KILLNBP`** | `0x01B546` | `0x033F9E` | `res_drvr_mpp.s:2302`<br>`res_drvr_mpp.s:2202` | KillNBP (csCode 254), also the noErr completion of the NBP calls: NBP_DONE stops the retry timer, forgets the active call and calls IODone with D0 (completing the call at the head of the .MPP queue) |
| **`KILLSENDREQ`** | — | `0x032C20` | `res_drvr_atp.s:1175` | KillSendReq (csCode 258, IM V-517): abort the request at aKillQEl: an NSendRequest (its csCode is 248) is looked for in the NSendRequest queues of all responding sockets and dequeued; a SendRequest in... |
| **`KILLSENDREQ_NEXTSKT`** | — | `0x032C3A` | `res_drvr_atp.s:1185` | — |
| **`KILLSENDREQ_NEXTSLOT`** | — | `0x032C5E` | `res_drvr_atp.s:1202` | — |
| **`KILLSENDREQ_NOTFOUND`** | — | `0x032C3E` | `res_drvr_atp.s:1187` | — |
| **`KILLSENDREQ_SKTLOOP`** | — | `0x032C2E` | `res_drvr_atp.s:1180` | — |
| **`KILLSENDREQ_SLOTLOOP`** | — | `0x032C48` | `res_drvr_atp.s:1193` | — |
| **`KILLSENDREQ_SREQ`** | — | `0x032C46` | `res_drvr_atp.s:1191` | a SendRequest: find its request slot |
| **`LAP_COUNTBITS`** | `0x01A9C8` | `0x0335E2` | `res_drvr_mpp.s:614`<br>`res_drvr_mpp.s:934` | adapt the global backoff mask to the collision/deferral history more than 2 collisions: double the mask LAP_COUNTBITS: D0 = (number of 1 bits in D2.B) - 2, condition codes set (GT = 3 or more).  Uses ... |
| **`LAP_COUNTBITS_LOOP`** | `0x01A9CC` | `0x0335E6` | `res_drvr_mpp.s:617`<br>`res_drvr_mpp.s:937` | — |
| **`LAP_COUNTBITS_NEXT`** | `0x01A9D2` | `0x0335EC` | `res_drvr_mpp.s:621`<br>`res_drvr_mpp.s:941` | — |
| **`LAP_CRCERR`** | `0x01ADBE` | `0x033A5E` | `res_drvr_mpp.s:1254`<br>`res_drvr_mpp.s:1581` | — |
| **`LAP_ENDFRAME`** | `0x01AC3A` | `0x033886` | `res_drvr_mpp.s:1002`<br>`res_drvr_mpp.s:1317` | LAP_ENDFRAME: let the SCC append CRC and closing flag at the underrun, then hold the line marking (abort sequence) and turn the transmitter off |
| **`LAP_ENDFRAME_ABORT`** | `0x01AC5A` | `0x0338A6` | `res_drvr_mpp.s:1015`<br>`res_drvr_mpp.s:1330` | — |
| **`LAP_ENDFRAME_EOM`** | `0x01AC40` | `0x03388C` | `res_drvr_mpp.s:1005`<br>`res_drvr_mpp.s:1320` | — |
| **`LAP_ENDFRAME_TBE`** | `0x01AC46` | `0x033892` | `res_drvr_mpp.s:1008`<br>`res_drvr_mpp.s:1323` | — |
| **`LAP_EXTINT`** | `0x01AAF4` | `0x033732` | `res_drvr_mpp.s:799`<br>`res_drvr_mpp.s:1127` | LAP_EXTINT: SCC channel B external/status interrupt (ExtStsDT[0]: changes other than DCD alone; D1 = changed enabled RR0 bits).  Resumes a deferred LAPWRITE; otherwise passes a DCD change to the mouse... |
| **`LAP_EXTINT_RESUME`** | `0x01AB0A` | `0x033748` | `res_drvr_mpp.s:813`<br>`res_drvr_mpp.s:1136` | LAP_EXTINT_RESUME LAP_EXTINT_RESUME / LAP_RESUMEWRITE: resume a deferred LAPWRITE |
| **`LAP_GETRR1`** | `0x01ADAA` | `0x033A3A` | `res_drvr_mpp.s:1237`<br>`res_drvr_mpp.s:1558` | LAP_GETRR1: D1 = RR1 (bit 7 end of frame, 6 CRC error, 5 Rx overrun) |
| **`LAP_LENERR`** | `0x01ADB4` | `0x033A48` | `res_drvr_mpp.s:1248`<br>`res_drvr_mpp.s:1571` | LAP_LENERR / LAP_UNDERRUN / LAP_CRCERR / LAP_OVERRUN: subtract from D0 (0 on entry) down to the error code, then reset the receiver |
| **`LAP_OVERRUN`** | `0x01ADC0` | `0x033A66` | `res_drvr_mpp.s:1256`<br>`res_drvr_mpp.s:1585` | — |
| **`LAP_POLLRCV`** | `0x01AB4E` | `0x033790` | `res_drvr_mpp.s:851`<br>`res_drvr_mpp.s:1178` | LAP_POLLRCV: poll ~125 times for a received byte (the answer to a lapRTS/lapENQ, or the data frame after our lapCTS) and receive the frame through LAP_RCVFRAME.  Preserves A0-A2. |
| **`LAP_POLLRCV_EXIT`** | `0x01AB62` | `0x0337A6` | `res_drvr_mpp.s:859`<br>`res_drvr_mpp.s:1186` | — |
| **`LAP_POLLRCV_LOOP`** | `0x01AB54` | `0x033798` | `res_drvr_mpp.s:854`<br>`res_drvr_mpp.s:1181` | — |
| **`LAP_RCVBADCTL`** | — | `0x0339C6` | `res_drvr_mpp.s:1483` | (unreachable: count NoHandCnt and reset the receiver) control frame type above $85: count, reset the receiver |
| **`LAP_RCVCRC`** | `0x01AD48` | `0x0339D4` | `res_drvr_mpp.s:1181`<br>`res_drvr_mpp.s:1502` | LAP_RCVCRC: read the two CRC bytes that end the frame: the first must not, the second must have end of frame, without CRC error; then reset the receiver.  D0 = 0 or overrunErr (-1), crcErr (-2), under... |
| **`LAP_RCVCRC_WAIT1`** | `0x01AD4C` | `0x0339DA` | `res_drvr_mpp.s:1184`<br>`res_drvr_mpp.s:1505` | — |
| **`LAP_RCVCRC_WAIT2`** | `0x01AD60` | `0x0339F0` | `res_drvr_mpp.s:1192`<br>`res_drvr_mpp.s:1513` | — |
| **`LAP_RCVCTL`** | `0x01ACF4` | `0x033952` | `res_drvr_mpp.s:1108`<br>`res_drvr_mpp.s:1426` | LAP_RCVCTL: control frame (lapType in D0).  Reads the CRC.  While our address is not yet valid, a frame sent to it (not broadcast) means the address is taken (fAdrInUse).  Else: lapENQ -> answer lapAC... |
| **`LAP_RCVCTL_CTS`** | — | `0x033988` | `res_drvr_mpp.s:1450` | — |
| **`LAP_RCVCTL_DATA`** | `0x01AD36` | `0x0339A0` | `res_drvr_mpp.s:1150`<br>`res_drvr_mpp.s:1464` | — |
| **`LAP_RCVCTL_DELAY`** | `0x01AD2E` | `0x033998` | `res_drvr_mpp.s:1146`<br>`res_drvr_mpp.s:1460` | — |
| **`LAP_RCVCTL_ENQ`** | `0x01AD3A` | `0x0339B6` | `res_drvr_mpp.s:1158`<br>`res_drvr_mpp.s:1473` | LAP_RCVCTL_ENQ lapENQ for our address: answer lapACK |
| **`LAP_RCVCTL_EXIT`** | `0x01AD16` | `0x033974` | `res_drvr_mpp.s:1121`<br>`res_drvr_mpp.s:1439` | — |
| **`LAP_RCVCTL_RTS`** | `0x01AD28` | `0x033990` | `res_drvr_mpp.s:1142`<br>`res_drvr_mpp.s:1456` | LAP_RCVCTL_RTS: lapRTS - answer lapCTS unless it was broadcast, then receive the data frame that follows |
| **`LAP_RCVCTL_TYPE`** | `0x01AD18` | `0x033976` | `res_drvr_mpp.s:1128`<br>`res_drvr_mpp.s:1442` | LAP_RCVCTL_TYPE: dispatch on the control frame type |
| **`LAP_RCVCTL_WAITDATA`** | — | `0x0339A4` | `res_drvr_mpp.s:1466` | — |
| **`LAP_RCVERR`** | — | `0x033A44` | `res_drvr_mpp.s:1568` | receive errors: count the error, D0 = its code, reset the receiver. LAP_RCVERR: from LAP_RCVFRAME_NOPH with D0 = RR1 bits 7/5. |
| **`LAP_RCVFRAME`** | `0x01AC70` | `0x0338C0` | `res_drvr_mpp.s:1040`<br>`res_drvr_mpp.s:1355` | LAP_RCVFRAME |
| **`LAP_RCVFRAME_FINDPH`** | `0x01AC9C` | `0x0338F0` | `res_drvr_mpp.s:1058`<br>`res_drvr_mpp.s:1374` | find the protocol handler of the type |
| **`LAP_RCVFRAME_LEN1`** | `0x01ACA8` | `0x033900` | `res_drvr_mpp.s:1064`<br>`res_drvr_mpp.s:1381` | length word (10 bits, includes itself) |
| **`LAP_RCVFRAME_LEN2`** | `0x01ACC2` | `0x03391A` | `res_drvr_mpp.s:1073`<br>`res_drvr_mpp.s:1390` | — |
| **`LAP_RCVFRAME_NOPH`** | `0x01ACE2` | `0x03393C` | `res_drvr_mpp.s:1092`<br>`res_drvr_mpp.s:1409` | LAP_RCVFRAME_NOPH: no handler for the type - read and drop the rest (ReadRest with no buffer), unless the frame has already ended |
| **`LAP_RCVFRAME_SRC`** | `0x01AC7A` | `0x0338CE` | `res_drvr_mpp.s:1044`<br>`res_drvr_mpp.s:1360` | — |
| **`LAP_RCVFRAME_TIMEOUT`** | `0x01ACCA` | `0x033922` | `res_drvr_mpp.s:1076`<br>`res_drvr_mpp.s:1393` | — |
| **`LAP_RCVFRAME_TYPE`** | `0x01AC88` | `0x0338DC` | `res_drvr_mpp.s:1049`<br>`res_drvr_mpp.s:1365` | — |
| **`LAP_RCVINT`** | `0x01AC6C` | `0x0338B8` | `res_drvr_mpp.s:1037`<br>`res_drvr_mpp.s:1352` | LAP_RCVINT: SCC channel B receive interrupt (Lvl2DT[2]); A0/A1 = SCC channel B control.  LAP_RCVFRAME (also from LAP_POLLRCV): read lapDstAdr, lapSrcAdr, lapType into the RHA; control frames -> LAP_RC... |
| **`LAP_RCVRESET`** | `0x01AD72` | `0x033A02` | `res_drvr_mpp.s:1203`<br>`res_drvr_mpp.s:1526` | LAP_RCVRESET: re-arm the receiver for the next frame: receiver off and hunt, drain the 3-byte FIFO, receiver on (hunt, address search), error reset, interrupt on the next character.  Condition codes f... |
| **`LAP_RCVRESET_DRAIN`** | `0x01AD86` | `0x033A16` | `res_drvr_mpp.s:1212`<br>`res_drvr_mpp.s:1535` | — |
| **`LAP_RCVRESET_HUNT`** | `0x01AD80` | `0x033A10` | `res_drvr_mpp.s:1208`<br>`res_drvr_mpp.s:1531` | — |
| **`LAP_RCVTIMEOUT`** | — | `0x0339CC` | `res_drvr_mpp.s:1487` | header byte timeout in LAP_RCVFRAME: count (underrun) |
| **`LAP_READ_JT`** | `0x01ADC4` | `0x033A72` | `res_drvr_mpp.s:1265`<br>`res_drvr_mpp.s:1597` | LAP_READ_JT: A4 for protocol handlers and socket listeners - JSR (A4) = ReadPacket, JSR 2(A4) = ReadRest |
| **`LAP_REPLYCTL`** | `0x01AD3C` | `0x0339B8` | `res_drvr_mpp.s:1161`<br>`res_drvr_mpp.s:1476` | LAP_REPLYCTL: send control frame D0 to the sender (lapSrcAdr in the RHA) |
| **`LAP_RESUMEWRITE`** | `0x01AB0E` | `0x03374C` | `res_drvr_mpp.s:815`<br>`res_drvr_mpp.s:1138` | — |
| **`LAP_RTS`** | `0x01AB66` | `0x0337AA` | `res_drvr_mpp.s:861`<br>`res_drvr_mpp.s:1188` | — |
| **`LAP_SCCWRITE`** | `0x01AC64` | `0x0338B0` | `res_drvr_mpp.s:1023`<br>`res_drvr_mpp.s:1338` | LAP_SCCWRITE: write D3 bytes from (A3) to the channel B control register |
| **`LAP_SENDBYTE`** | `0x01AB82` | `0x0337C6` | `res_drvr_mpp.s:889`<br>`res_drvr_mpp.s:1215` | LAP_SENDBYTE: wait (31 polls) for the Tx buffer, then write D3 to the channel B data register.  Returns TST D1: EQ only if D1 = 0; a timeout leaves D1 = -1 (NE) without writing, which the callers do n... |
| **`LAP_SENDBYTE_EXIT`** | `0x01AB92` | `0x0337D8` | `res_drvr_mpp.s:896`<br>`res_drvr_mpp.s:1222` | — |
| **`LAP_SENDBYTE_LOOP`** | `0x01AB84` | `0x0337CA` | `res_drvr_mpp.s:891`<br>`res_drvr_mpp.s:1217` | — |
| **`LAP_SENDCTL`** | `0x01AC22` | `0x03386E` | `res_drvr_mpp.s:991`<br>`res_drvr_mpp.s:1306` | LAP_SENDCTL: send a LAP control frame: lapDstAdr = D2, lapSrcAdr = sysLAPAddr, lapType = D0.B ($81 lapENQ, $82 lapACK, $84 lapRTS, $85 lapCTS); falls into LAP_ENDFRAME |
| **`LAP_SENDFRAME`** | `0x01ABAC` | `0x0337F4` | `res_drvr_mpp.s:922`<br>`res_drvr_mpp.s:1247` | LAP_SENDFRAME: send the frame of the WDS at WDSPtr (lapSrcAdr filled in with our node), then CRC, closing flag and abort (LAP_ENDFRAME). Interrupts are off: received modem-port bytes (VIA PA7 low) are... |
| **`LAP_SENDFRAME_BYTE`** | `0x01ABE8` | `0x033834` | `res_drvr_mpp.s:951`<br>`res_drvr_mpp.s:1271` | LAP_SENDFRAME_BYTE send the next byte; save a modem-port byte, if one arrived |
| **`LAP_SENDFRAME_COUNT`** | `0x01ABF2` | `0x03383E` | `res_drvr_mpp.s:956`<br>`res_drvr_mpp.s:1276` | — |
| **`LAP_SENDFRAME_END`** | `0x01ABFE` | `0x03384A` | `res_drvr_mpp.s:969`<br>`res_drvr_mpp.s:1284` | LAP_SENDFRAME_END all bytes sent: end the frame |
| **`LAP_SENDFRAME_EXIT`** | `0x01AC0E` | `0x03385A` | `res_drvr_mpp.s:978`<br>`res_drvr_mpp.s:1293` | — |
| **`LAP_SENDFRAME_LOOP`** | `0x01ABD8` | `0x033820` | `res_drvr_mpp.s:937`<br>`res_drvr_mpp.s:1262` | byte loop |
| **`LAP_SENDFRAME_POLL`** | `0x01AC00` | `0x03384C` | `res_drvr_mpp.s:972`<br>`res_drvr_mpp.s:1287` | let PollProc process the saved modem-port bytes |
| **`LAP_SENDFRAME_WAIT`** | `0x01ABDA` | `0x033824` | `res_drvr_mpp.s:939`<br>`res_drvr_mpp.s:1264` | — |
| **`LAP_SETWR3`** | `0x01ADA0` | `0x033A30` | `res_drvr_mpp.s:1227`<br>`res_drvr_mpp.s:1549` | LAP_SETWR3: WR3 = D1 |
| **`LAP_SPECIALINT`** | `0x01AD44` | `0x0339D0` | `res_drvr_mpp.s:1170`<br>`res_drvr_mpp.s:1491` | LAP_SPECIALINT: SCC channel B special receive condition (Lvl2DT[3]), also used to drop a frame: reset the receiver (twice) |
| **`LAP_TXOFF`** | `0x01AC5E` | `0x0338AA` | `res_drvr_mpp.s:1019`<br>`res_drvr_mpp.s:1334` | LAP_TXOFF: write VSTData - WR5 = $60 (RTS off), WR14 = $41 (DPLL reset missing clock, BRG on), WR3 = $DD (receiver on, hunt mode) |
| **`LAP_TXON`** | `0x01AB96` | `0x0337DC` | `res_drvr_mpp.s:905`<br>`res_drvr_mpp.s:1230` | LAP_TXON: turn the transmitter on (LAP_TXON_TBL), let it send flags for a moment, then reset the Tx CRC generator |
| **`LAP_TXON_DELAY`** | `0x01ABA2` | `0x0337EA` | `res_drvr_mpp.s:910`<br>`res_drvr_mpp.s:1235` | — |
| **`LAP_TXON_TBL`** | `0x01AB7E` | `0x0337C2` | `res_drvr_mpp.s:884`<br>`res_drvr_mpp.s:1207` | LAP_TXON_TBL: SCC writes for LAP_TXON - WR5 = $6B (Tx on, RTS on, 8 bits, Tx CRC on), WR3 = $D0 (receiver off, enter hunt mode) |
| **`LAP_UNDERRUN`** | `0x01ADBC` | `0x033A56` | `res_drvr_mpp.s:1252`<br>`res_drvr_mpp.s:1577` | — |
| **`LAP_WAIT100`** | `0x01AA86` | `0x0336A4` | `res_drvr_mpp.s:722`<br>`res_drvr_mpp.s:1042` | LAP_WAIT100: wait ~100 us, then test RR0 Sync/Hunt -> EQ if the receiver has left hunt mode (a frame is on the line).  Uses D1. |
| **`LAP_WAIT100_ENTER`** | — | `0x0336B0` | `res_drvr_mpp.s:1048` | — |
| **`LAP_WAIT100_LOOP`** | `0x01AA88` | `0x0336AA` | `res_drvr_mpp.s:724`<br>`res_drvr_mpp.s:1045` | — |
| **`LAP_WAIT100_SENSE`** | — | `0x0336B2` | `res_drvr_mpp.s:1050` | — |
| **`LAPWRITE`** | `0x01A992` | `0x0334F2` | `res_drvr_mpp.s:583`<br>`res_drvr_mpp.s:793` | LAPWRITE LAPWRITE: send a LocalTalk frame.  A1 = WDS (first entry: frame header), D2 = destination node ($FF = broadcast).  The return address is kept in LAPWrtRtn and the write ends with a jump there... |
| **`LAPWRITE_BCAST`** | `0x01AA92` | `0x0336B8` | `res_drvr_mpp.s:734`<br>`res_drvr_mpp.s:1058` | LAPWRITE_BCAST: broadcast - after the lapRTS the line must stay quiet for ~100 us |
| **`LAPWRITE_BUSY`** | `0x01AAC4` | `0x0336FE` | `res_drvr_mpp.s:772`<br>`res_drvr_mpp.s:1100` | LAPWRITE_BUSY: the line is busy.  If it went busy after we had waited at least 4 steps, count a deferral (deferTries; lbackOff and deferHistory bit 0); then wait for the end of the frame on the line. |
| **`LAPWRITE_CHKCTS`** | `0x01AA7E` | `0x033698` | `res_drvr_mpp.s:712`<br>`res_drvr_mpp.s:1028` | LAPWRITE_CHKCTS: lapCTS received? then send the data frame |
| **`LAPWRITE_COLLISION`** | `0x01AAA4` | `0x0336DA` | `res_drvr_mpp.s:754`<br>`res_drvr_mpp.s:1082` | LAPWRITE_COLLISION: no lapCTS (or line busy after a broadcast lapRTS): record a collision, widen lbackOff, retry up to collsnTries times |
| **`LAPWRITE_DATA`** | `0x01AA96` | `0x0336C8` | `res_drvr_mpp.s:738`<br>`res_drvr_mpp.s:1066` | send the data frame |
| **`LAPWRITE_DEFER`** | `0x01AADE` | `0x03371C` | `res_drvr_mpp.s:783`<br>`res_drvr_mpp.s:1112` | wait: the abort at the end of the frame raises an external/status interrupt (LAP_EXTINT); MPP_VBLTASK resumes after 20-40 ticks anyway |
| **`LAPWRITE_DEFERS`** | `0x01A9DA` | `0x0335F4` | `res_drvr_mpp.s:631`<br>`res_drvr_mpp.s:950` | LAPWRITE_DEFERS: few collisions - halve the mask when fewer than 2 of the last 8 sends were deferred (deferHistory then set to $FF) |
| **`LAPWRITE_ENQ`** | `0x01A99A` | `0x0334FA` | `res_drvr_mpp.s:587`<br>`res_drvr_mpp.s:797` | LAPWRITE_ENQ: entry used to send an ENQ (fSendENQ set by the caller) |
| **`LAPWRITE_EXIT`** | `0x01AA9C` | `0x0336D2` | `res_drvr_mpp.s:744`<br>`res_drvr_mpp.s:1073` | return through LAPWrtRtn |
| **`LAPWRITE_IDG`** | `0x01AA1C` | `0x033636` | `res_drvr_mpp.s:669`<br>`res_drvr_mpp.s:988` | inter-dialog gap: 4 more steps with interrupts off; the DPLL watches for any activity meanwhile |
| **`LAPWRITE_IDGLOOP`** | `0x01AA2C` | `0x033646` | `res_drvr_mpp.s:675`<br>`res_drvr_mpp.s:994` | — |
| **`LAPWRITE_INIT`** | `0x01A9E4` | `0x0335FE` | `res_drvr_mpp.s:638`<br>`res_drvr_mpp.s:957` | tries, local and global backoff for this send |
| **`LAPWRITE_NETWORK`** | — | `0x0335C2` | `res_drvr_mpp.s:915` | LAPWRITE_NETWORK: send the frame on the network.  First adapt the global backoff mask to the collision/deferral history of the last 8 sends. |
| **`LAPWRITE_NOERR`** | `0x01AA9A` | `0x0336CC` | `res_drvr_mpp.s:741`<br>`res_drvr_mpp.s:1069` | done |
| **`LAPWRITE_NOHOOK`** | `0x01A9A8` | `0x033508` | `res_drvr_mpp.s:593`<br>`res_drvr_mpp.s:804` | intranode delivery (SelfSend on, data frame for us or broadcast)? |
| **`LAPWRITE_SELF`** | — | `0x033522` | `res_drvr_mpp.s:816` | hand the frame to our protocol handler: LAP header and length word into the RHA, then the handler reads the rest through SELF_READ_JT |
| **`LAPWRITE_SELFCHK`** | — | `0x03351E` | `res_drvr_mpp.s:812` | — |
| **`LAPWRITE_SELFDONE`** | — | `0x033560` | `res_drvr_mpp.s:838` | — |
| **`LAPWRITE_SELFPH`** | — | `0x03354A` | `res_drvr_mpp.s:830` | — |
| **`LAPWRITE_SENDCTL`** | `0x01AA56` | `0x033670` | `res_drvr_mpp.s:693`<br>`res_drvr_mpp.s:1012` | line free: sync pulse (RTS on, off), then lapRTS or lapENQ end the sync pulse, send the control frame |
| **`LAPWRITE_SENSE`** | `0x01AA32` | `0x03364C` | `res_drvr_mpp.s:679`<br>`res_drvr_mpp.s:998` | line still free? |
| **`LAPWRITE_START`** | `0x01A9FA` | `0x033614` | `res_drvr_mpp.s:649`<br>`res_drvr_mpp.s:968` | LAPWRITE_START: begin (or resume) the transmission, SR on the stack |
| **`LAPWRITE_TRY`** | `0x01A9FC` | `0x033616` | `res_drvr_mpp.s:653`<br>`res_drvr_mpp.s:972` | LAPWRITE_TRY: one attempt; D3 = D0 so that LAPWRITE_BUSY can tell how long we waited |
| **`LAPWRITE_WAIT`** | `0x01AA14` | `0x03362E` | `res_drvr_mpp.s:662`<br>`res_drvr_mpp.s:981` | — |
| **`LOADNBP`** | `0x01A79A` | `0x0331C8` | `res_drvr_mpp.s:162`<br>`res_drvr_mpp.s:246` | LoadNBP (csCode 249): nothing to load in the ROM driver - noErr |
| **`LOOKUPNAME`** | `0x01B460` | `0x034104` | `res_drvr_mpp.s:2195`<br>`res_drvr_mpp.s:2422` | LookupName (csCode 251): look up entityPtr in the whole network; the replies (NBP_LISTENER) go into retBuffPtr/retBuffSize, numGotten counts them.  Ends at maxToGet, a full buffer or after count retri... |
| **`LOOKUPREPLY`** | `0x01A790` | `0x0331BE` | `res_drvr_mpp.s:152`<br>`res_drvr_mpp.s:237` | LookupReply (csCode 242): issued by NIS_LISTENER (to this driver) for a received LkUp packet; runs the lookup-reply code via LookupPtr |
| **`LUCODE`** | `0x01B140` | `0x0344C8` | `res_drvr_mpp.s:1686`<br>`res_drvr_mpp.s:2893` | LUCODE: lookup-reply code entry table (LookupPtr): +0 LookupReply, +2 goodbye kiss, +4 NIS socket listener |
| **`LUCODE_GOODBYE`** | `0x01B142` | `0x0344CA` | `res_drvr_mpp.s:1693`<br>`res_drvr_mpp.s:2895` | LUCODE_GOODBYE: +2 - drop names in the application heap |
| **`LUCODE_REPLY`** | `0x01B18E` | `0x03451C` | `res_drvr_mpp.s:1741`<br>`res_drvr_mpp.s:2934` | LUCODE_REPLY: -> NBP_LKUPREPLY |
| **`MADDRMARKS`** | — | — | `res_drvr_sony_fdhd.s:3327` | mAddrMarks -- the four bytes of an MFM address mark |
| **`MBDF0_APPLE1BIT`** | — | `0x038DBA` | `res_mbdf.s:792` | ... and the logo at 1 bit per pixel, black on white ... |
| **`MBDF0_APPLE1BITINV`** | — | `0x038DDA` | `res_mbdf.s:810` | ... and white on black |
| **`MBDF0_APPLE4BIT`** | — | `0x038CBA` | `res_mbdf.s:756` | Unused here: the color Apple menu title of the Mac II version (C175 "Added 4-bit color apple"): a 16x16 image at 4 bits per pixel, 8 bytes per row, background 0, the logo's six color bands drawn with ... |
| **`MBDF0_APPLE4BITINV`** | — | `0x038D3A` | `res_mbdf.s:774` | ... the same image with background 15 (for the inverted title) ... |
| **`MBDF0_BUSYPAT`** | — | `0x038CAA` | `res_mbdf.s:744` | Data hilite state 3 (busy): horizontal stripes |
| **`MBDF0_CALCBAR`** | — | `0x0389BE` | `res_mbdf.s:353` | Msg 2 -- CalcBar: lay out the titles. param 0: from the first title at 10; param = MenuList offset: from that title on. Each title is StringWidth(title) + 13 wide; the right edge of the last one goes ... |
| **`MBDF0_CALCDONE`** | — | `0x0389FC` | `res_mbdf.s:381` | — |
| **`MBDF0_CALCLOOP`** | — | `0x0389D8` | `res_mbdf.s:366` | measure the title of entry D4; D3 = its left edge |
| **`MBDF0_CALCLOOPDONE`** | — | `0x0389F8` | `res_mbdf.s:379` | — |
| **`MBDF0_COPYSAVED`** | — | `0x038C26` | `res_mbdf.s:673` | CopySaved -- copy between the screen and the saved bits. In:  stack: srcBits and dstBits pushed by the caller (one of them the saved BitMap), A0 = the saved BitMap record. Does CopyBits(srcBits, dstBi... |
| **`MBDF0_DISPOSEBAR`** | — | `0x0388C8` | `res_mbdf.s:203` | Msg 4 -- DisposeBar: nothing to dispose of. |
| **`MBDF0_DONEHILITE`** | — | `0x038A9C` | `res_mbdf.s:479` | — |
| **`MBDF0_DOSELECTED`** | — | `0x038A72` | `res_mbdf.s:455` | DoSelected -- show a title as selected: invert TempRect, then unlock the title's menu handle (MBDF0_UNLOCKTITLE). In:  D3 = MenuList offset, TempRect = the title's hilite rect. Changes D0-D2/A0-A1. Re... |
| **`MBDF0_DRAW1TITLE`** | — | `0x038A46` | `res_mbdf.s:432` | unreachable: in the Mac II version the normal state erases the title rect here and falls into Draw1Title to redraw the title; the A278 invert-back above branches around it. Draw1Title -- draw one menu... |
| **`MBDF0_DRAWBAR`** | — | `0x0388F2` | `res_mbdf.s:251` | Msg 0 -- DrawBar: clear the menu bar to white and draw the line under it; with param 0 also draw all titles, then hilite the one whose menuID is in TheMenu (after all titles, A428). With param -1 retu... |
| **`MBDF0_DRAWDONE`** | — | `0x03897E` | `res_mbdf.s:303` | hilite the selected title now that all titles are drawn (A428) |
| **`MBDF0_DRAWMLOOP`** | — | `0x03893E` | `res_mbdf.s:278` | main drawing loop: D3 = MenuList offset of the title to draw |
| **`MBDF0_DRAWSTRUCT`** | — | `0x038B80` | `res_mbdf.s:591` | SaveDemBits: a BitMap record followed by its bits DrawStruct: erase the menu and frame it |
| **`MBDF0_ENTIREBAR`** | — | `0x0389D0` | `res_mbdf.s:361` | — |
| **`MBDF0_FLIPBAR`** | — | `0x038A9E` | `res_mbdf.s:483` | FlipBar (hilite offset 0, used by FlashMenuBar(0)): invert the whole menu bar inside the round screen corners. |
| **`MBDF0_GETMENUASCENT`** | — | `0x0388E6` | `res_mbdf.s:237` | GetMenuAscent -- the baseline of the menu titles. Out: D4.L = ascent + 2 (y of the title baseline; the bar starts at y = 0). Changes D0-D2/A0-A1. Called by: MBDF0_DRAW1TITLE |
| **`MBDF0_GETMENUINFO`** | — | `0x0388DA` | `res_mbdf.s:224` | GetMenuInfo -- font metrics of the current (system) font. Out: D0 = ascent in the high word, descent in the low word. Changes D0-D2/A0-A1 (_GetFontInfo). Called by: MBDF0_HEIGHTBAR, MBDF0_GETMENUASCEN... |
| **`MBDF0_GETTITLERECT`** | — | `0x038ABE` | `res_mbdf.s:503` | GetTitleRect -- the rect of a title that hiliting inverts. In:  D0.W = MenuList offset of the title; 0 = the whole bar. Out: TempRect = (top 1, left menuLeft-1, bottom MBarHeight-1, right = next title... |
| **`MBDF0_GOBARPROC`** | — | `0x0388B4` | `res_mbdf.s:183` | GoBarProc: message dispatch table, offsets from the table |
| **`MBDF0_GRAYPAT`** | — | `0x038CB2` | `res_mbdf.s:748` | hilite state 2 / disabled title: 50% gray |
| **`MBDF0_GTDONE`** | — | `0x038AE8` | `res_mbdf.s:521` | — |
| **`MBDF0_GTLASTMENU`** | — | `0x038AE2` | `res_mbdf.s:517` | — |
| **`MBDF0_GTMARGIN`** | — | `0x038AE6` | `res_mbdf.s:519` | — |
| **`MBDF0_HEIGHTBAR`** | — | `0x0388CA` | `res_mbdf.s:210` | Msg 6 -- HeightBar: MBarHeight := ascent + descent + 5 of the system font (20 with Chicago 12). The same computation is in the Menu Manager's CALCMBHEIGHT, which InitWindows calls. |
| **`MBDF0_HILITEBAR`** | — | `0x0389FE` | `res_mbdf.s:395` | Msg 5 -- HiliteBar: param high word = state, low word = MenuList offset; offset 0 = invert the whole bar (FlipBar). States: 0 normal and 1 selected both invert the title rect (A278: on the SE a title ... |
| **`MBDF0_HITBAR`** | — | `0x038980` | `res_mbdf.s:314` | Msg 1 -- HitBar: where is the mouse point (global, in param)? Result 0 if it is in the bar but left of the first title (h < 10) or right of the last (h >= lastRight), -1 if it is below the bar, else t... |
| **`MBDF0_HITDONE`** | — | `0x0389AC` | `res_mbdf.s:333` | — |
| **`MBDF0_HITLOOP`** | — | `0x03899E` | `res_mbdf.s:326` | — |
| **`MBDF0_HITTHISONE`** | — | `0x0389A8` | `res_mbdf.s:331` | — |
| **`MBDF0_INITBAR`** | — | `0x0388C6` | `res_mbdf.s:198` | Msg 3 -- InitBar: this version keeps no private data, so there is nothing to allocate (the later version allocates its save structure here and keeps it in mbSaveLoc). |
| **`MBDF0_MAKEMRECT`** | — | `0x038BF4` | `res_mbdf.s:644` | MakeMRect -- the rect of a pulled-down menu. In:  A0 = menu record (menuWidth/menuHeight valid), D3 = left edge of its title (menuLeft), A2 = WMgrPort. If menuLeft + menuWidth + 8 is beyond the screen... |
| **`MBDF0_MAKEUPDATE`** | — | `0x038C66` | `res_mbdf.s:712` | MakeUpdate: rebuild the menu's rect, grow it by the frame and the shadow and repaint everything behind the front window there |
| **`MBDF0_MENULISTOK`** | — | `0x03888C` | `res_mbdf.s:166` | — |
| **`MBDF0_NEXTDRAW`** | — | `0x03895A` | `res_mbdf.s:288` | — |
| **`MBDF0_NOSAVEMEM`** | — | `0x038C40` | `res_mbdf.s:690` | unreachable: the Mac II version disposes of its pixmap here before clearing SavedHandle; _DisposPixMap ($AA04) is a Color QuickDraw trap, not implemented on the SE. no memory for the saved bits: draw ... |
| **`MBDF0_NOTINBAR`** | — | `0x0389B4` | `res_mbdf.s:338` | — |
| **`MBDF0_NOTITLE`** | — | `0x0389AE` | `res_mbdf.s:335` | — |
| **`MBDF0_PAINTBUSY`** | — | `0x038A7A` | `res_mbdf.s:462` | Hilite states 3 (busy) and 2 (disabled), and Draw1Title's gray (PaintTitleDisable): paint TempRect with a pattern in patBic mode, clearing every pixel where the pattern has a 1. |
| **`MBDF0_PAINTDISABLED`** | — | `0x038A80` | `res_mbdf.s:465` | — |
| **`MBDF0_PAINTTITLE`** | — | `0x038A84` | `res_mbdf.s:467` | — |
| **`MBDF0_RESTOREBITSBAR`** | — | `0x038C48` | `res_mbdf.s:698` | Msg 8 -- RestoreBitsBar: the menu is closed. If its bits were saved, copy them back and dispose of them; otherwise (param = its MenuList offset) let the windows behind it redraw it. |
| **`MBDF0_SAVEBITSBAR`** | — | `0x038AFA` | `res_mbdf.s:541` | Msg 7 -- SaveBitsBar: param = MenuList offset of the menu that is being pulled down. Computes its rect (MBDF0_MAKEMRECT), saves the screen under it -- the rect grown by 4 on the left, right and bottom... |
| **`MBDF0_SAVEBITSDONE`** | — | `0x038BDE` | `res_mbdf.s:628` | — |
| **`MBDF0_SKIPCALCSIZE`** | — | `0x038B18` | `res_mbdf.s:553` | — |
| **`MBDF0_START`** | — | `0x038860` | `res_mbdf.s:148` | StartMBDF: save registers and the caller's port, set up the WMgrPort and lock the MenuList, then dispatch on the message. |
| **`MBDF0_STORERECT`** | — | `0x038C0C` | `res_mbdf.s:653` | — |
| **`MBDF0_UNLOCKTITLE`** | — | `0x038A96` | `res_mbdf.s:476` | unlock the menu handle of title D3 and return |
| **`MBDF0_UPDSIZEOK`** | — | `0x038C80` | `res_mbdf.s:722` | — |
| **`MBDF0_WHOLEBAR`** | — | `0x038AEA` | `res_mbdf.s:523` | — |
| **`MDATAMARKS`** | — | — | `res_drvr_sony_fdhd.s:3428` | mDataMarks -- the four bytes of an MFM data mark |
| **`MDEF_APPLY_STYLE`** | `0x01C1C0` | `0x039082` | `res_mdef.s:465`<br>`res_mdef.s:456` | draw item title text with style |
| **`MDEF_AT_BOTTOM`** | `0x01C0CA` | `0x038F98` | `res_mdef.s:347`<br>`res_mdef.s:344` | MDEF_DRAW_ALL exit: all items drawn |
| **`MDEF_BUILD_RECT`** | `0x01C076` | `0x038F42` | `res_mdef.s:292`<br>`res_mdef.s:292` | build the item's rect and invert it |
| **`MDEF_CHK_BELOW`** | `0x01BFBC` | `0x038E94` | `res_mdef.s:141`<br>`res_mdef.s:159` | mouse not above the menu: below it? |
| **`MDEF_CHK_ENABLE`** | `0x01C050` | `0x038F1E` | `res_mdef.s:259`<br>`res_mdef.s:263` | — |
| **`MDEF_CHK_ENABLED`** | `0x01C042` | `0x038F0A` | `res_mdef.s:253`<br>`res_mdef.s:254` | MDEF_CHK_ENABLED (Apple: EnableTest): is item D4 enabled? In:  D4 = item number, A3 = menu handle. Out: NE = enabled, EQ = disabled (item bit or menu bit 0 of menuEnable clear). Items above 31: BTST u... |
| **`MDEF_CHK_ICON`** | `0x01C21C` | `0x0390DE` | `res_mdef.s:511`<br>`res_mdef.s:501` | — |
| **`MDEF_CHK_MAXHT`** | `0x01C2DA` | `0x0391A6` | `res_mdef.s:633`<br>`res_mdef.s:622` | — |
| **`MDEF_DFLT_MBAR`** | `0x01C016` | `0x03916C` | `res_mdef.s:204`<br>`res_mdef.s:592` | (the Plus tests MBarHeight = 0 here and then uses 20) |
| **`MDEF_DIM_ITEM`** | `0x01C09E` | `0x038F6A` | `res_mdef.s:311`<br>`res_mdef.s:309` | gray request: not for a separator line |
| **`MDEF_DRAW_ALL`** | `0x01C0D4` | `0x038FA6` | `res_mdef.s:363`<br>`res_mdef.s:359` | MDEF_DRAW_ALL (Apple: DrawMenu): draw the items from TopMenuItem on, the first one at the bottom of the menu bar, each line D3 = baseline, D5/D6 = left/right of the item (narrowed by the mark, icon an... |
| **`MDEF_DRAW_KEY`** | `0x01C18A` | `0x03904C` | `res_mdef.s:439`<br>`res_mdef.s:430` | draw key equivalent (Cmd-key shortcut) if present |
| **`MDEF_DRAW_LOOP`** | `0x01C0EE` | `0x038FB8` | `res_mdef.s:372`<br>`res_mdef.s:366` | item draw loop |
| **`MDEF_DRAW_MARK`** | `0x01C128` | `0x038FEC` | `res_mdef.s:399`<br>`res_mdef.s:390` | prepare to draw this item check for separator line (title = '-') check for icon draw mark character (checkmark, bullet, etc.) |
| **`MDEF_DRAW_MSG`** | `0x01C0BE` | `0x038F8A` | `res_mdef.s:342`<br>`res_mdef.s:337` | mDrawMsg (0): draw the whole menu, from item 1 |
| **`MDEF_DRAW_RTL`** | `0x01C1DE` | `0x0390A0` | `res_mdef.s:485`<br>`res_mdef.s:475` | LTR: draw string left-to-right MDEF_DRAW_RTL - draw the item text with TextBox, justified by TESysJust (D1), between D5 and D6 |
| **`MDEF_DRAW_RTS`** | `0x01C0CE` | — | `res_mdef.s:349` | MDEF_DRAW_ALL exit: all items drawn |
| **`MDEF_DRAW_SEP`** | `0x01C232` | `0x0390F4` | `res_mdef.s:527`<br>`res_mdef.s:516` | MDEF_DRAW_SEP - a '-' item: a gray line across the middle of the item's line |
| **`MDEF_DRAW_TEXT`** | `0x01C146` | `0x039008` | `res_mdef.s:412`<br>`res_mdef.s:403` | draw the icon, if any (Apple: CHKDRAWICON) |
| **`MDEF_END_MEASURE`** | `0x01C310` | `0x0391DC` | `res_mdef.s:662`<br>`res_mdef.s:649` | all items measured |
| **`MDEF_ENTRY`** | `0x01BF4C` | `0x038E0E` | `res_mdef.s:85`<br>`res_mdef.s:96` | parameters and locals (see the banner) MDEF entry: dispatch on message type |
| **`MDEF_EXIT`** | `0x01BFFC` | `0x038ED6` | `res_mdef.s:185`<br>`res_mdef.s:199` | MDEF exit: strip Pascal parameters and return |
| **`MDEF_FIND_ITEM`** | `0x01BFCE` | `0x038EA8` | `res_mdef.s:153`<br>`res_mdef.s:169` | mouse in the menu: walk the items from TopMenuItem (whose top is at MBarHeight) down to it |
| **`MDEF_FIND_NTH`** | `0x01C25A` | `0x03911C` | `res_mdef.s:554`<br>`res_mdef.s:542` | MDEF_FIND_NTH (Apple: GetItemRecord) - find item D0 in menu data. In:  A0 = menu record, D0 = item number. Out: A0 = the item's text (Pascal string), A1 = its 4 attribute bytes, NE; or A0 = A1 = D0 = ... |
| **`MDEF_FOUND_ITEM`** | `0x01C27E` | `0x039140` | `res_mdef.s:580`<br>`res_mdef.s:564` | A1 points to the item (its length byte) |
| **`MDEF_GET_MBARHT`** | `0x01C00A` | — | `res_mdef.s:199` | MDEF_GET_MBARHT: the menu bar height, where the first visible item starts: MBarHeight, or 20 on a 64K ROM (ROM85 < 0) or if MBarHeight is 0. Out: D0 = height. Called by: MDEF_FIND_ITEM, MDEF_INVERT_IT... |
| **`MDEF_GOT_HEIGHT`** | `0x01C040` | `0x038F08` | `res_mdef.s:242`<br>`res_mdef.s:237` | — |
| **`MDEF_GOT_MBAR`** | `0x01C01A` | — | `res_mdef.s:206` | — |
| **`MDEF_GRAY_ITEM`** | `0x01C328` | `0x0391F4` | `res_mdef.s:680`<br>`res_mdef.s:666` | MDEF_GRAY_ITEM (Apple: GrayRect) - gray out a disabled item by painting the gray pattern in patBic mode over its rect. In:  A0 = the rect (TempRect). Changes D0-D2/A0-A1. Called by: MDEF_DIM_ITEM |
| **`MDEF_HILITE_RTS`** | `0x01C098` | `0x038F64` | `res_mdef.s:305`<br>`res_mdef.s:305` | — |
| **`MDEF_HITTEST`** | `0x01BFEA` | `0x038EC4` | `res_mdef.s:171`<br>`res_mdef.s:186` | MDEF_HITTEST - the mouse is on item D4: select it if enabled |
| **`MDEF_INVERT_ITEM`** | `0x01C052` | `0x038F20` | `res_mdef.s:273`<br>`res_mdef.s:275` | MDEF_INVERT_ITEM (Apple: InvertItem): hilite/unhilite an item by inverting its rect; with bit 15 of D0 set, gray it instead (MDEF_GRAY_ITEM; never a '-' separator). In:  D0 = item number (0 = none), A... |
| **`MDEF_ITEM_HEIGHT`** | `0x01C036` | `0x038EFE` | `res_mdef.s:237`<br>`res_mdef.s:232` | MDEF_ITEM_HEIGHT (Apple: GetItemHeight): height of an item. In:  A1 = the item's attribute bytes (icon number first). Out: D0 = MFHeight, or 36 if the item has an icon. Called by: MDEF_SCAN_ITEMS, MDE... |
| **`MDEF_KEY_MOVETO`** | `0x01C1A8` | `0x03906A` | `res_mdef.s:453`<br>`res_mdef.s:444` | handle RTL text direction |
| **`MDEF_MEASURE_INIT`** | — | `0x039170` | `res_mdef.s:594` | — |
| **`MDEF_MEASURE_LOOP`** | `0x01C2B6` | `0x039182` | `res_mdef.s:615`<br>`res_mdef.s:604` | measure each item to find max width and total height |
| **`MDEF_NEXT_ITEM`** | `0x01C228` | `0x0390EA` | `res_mdef.s:518`<br>`res_mdef.s:508` | — |
| **`MDEF_NO_ICON_W`** | `0x01C2D0` | `0x03919C` | `res_mdef.s:627`<br>`res_mdef.s:616` | — |
| **`MDEF_NO_KEY_W`** | `0x01C2EE` | `0x0391BA` | `res_mdef.s:642`<br>`res_mdef.s:631` | — |
| **`MDEF_NOT_CHICAGO`** | `0x01C030` | `0x038EF8` | `res_mdef.s:226`<br>`res_mdef.s:222` | — |
| **`MDEF_NOT_FOUND`** | `0x01C276` | `0x039138` | `res_mdef.s:572`<br>`res_mdef.s:558` | no such item |
| **`MDEF_RESET_FACE`** | `0x01C208` | `0x0390CA` | `res_mdef.s:503`<br>`res_mdef.s:493` | — |
| **`MDEF_SCAN_ITEMS`** | `0x01BFD2` | `0x038EAC` | `res_mdef.s:156`<br>`res_mdef.s:172` | — |
| **`MDEF_SCROLL`** | `0x01BF9A` | `0x038E60` | `res_mdef.s:123`<br>`res_mdef.s:134` | check if mouse is inside menuRect scroll the contents by D7 pixels (down if > 0), D4 = new TopMenuItem |
| **`MDEF_SETUP_FONT`** | `0x01C01C` | `0x038EE4` | `res_mdef.s:217`<br>`res_mdef.s:213` | MDEF_SETUP_FONT (Apple: GetSizes): font metrics of the current font into the FontInfo record at -8(A6); widMax is reduced by 2 for Chicago (widMax 14) and the leading field becomes the line height MFH... |
| **`MDEF_SIZE_MSG`** | `0x01C28A` | `0x03914C` | `res_mdef.s:596`<br>`res_mdef.s:579` | mSizeMsg (2) (Apple: DoCalcMsg): calculate menu width and height Measures all items in the WMgrPort and sets menuWidth/menuHeight. The height stops growing at the screen height minus the menu bar and ... |
| **`MDEF_STORE_SIZE`** | `0x01C312` | `0x0391DE` | `res_mdef.s:664`<br>`res_mdef.s:651` | — |
| **`MDEF_TEST_MENU_BIT`** | — | `0x038F1A` | `res_mdef.s:261` | — |
| **`MDEF_TWEAKPOS`** | `0x01C0AA` | `0x038F76` | `res_mdef.s:326`<br>`res_mdef.s:323` | MDEF_TWEAKPOS (Apple: TweakPos): reserve a column of D0 pixels at the leading edge of the item -- the left edge (D5), or the right edge (D6) if TESysJust is negative (right-to-left scripts). In:  D0 =... |
| **`MDEF_TWEAKPOS_RTS`** | `0x01C0BC` | `0x038F88` | `res_mdef.s:336`<br>`res_mdef.s:332` | RTL: the column goes at the right edge |
| **`MDEF_UPD_HILITE`** | `0x01BFF0` | `0x038ECA` | `res_mdef.s:177`<br>`res_mdef.s:191` | update highlighting if selection changed Called by: MDEF_ENTRY, MDEF_CHK_BELOW, MDEF_SCAN_ITEMS, MDEF_HITTEST |
| **`MDEF_UPD_MAXW`** | `0x01C306` | `0x0391D2` | `res_mdef.s:654`<br>`res_mdef.s:643` | — |
| **`MDEF_WALK_ITEMS`** | `0x01C062` | `0x038F2E` | `res_mdef.s:281`<br>`res_mdef.s:281` | walk items from TopMenuItem to find target item's Y position |
| **`MDEF_WALK_LOOP`** | `0x01C268` | `0x03912A` | `res_mdef.s:561`<br>`res_mdef.s:549` | — |
| **`MPARAMS`** | — | — | `res_drvr_sony_fdhd.s:3084` | mParams -- ISM parameter RAM values for MFM disks: 2, 3 and 4 us cells at the 15.6672 MHz FCLK (t2 = 2 us = 31.33 clocks), register $F first. The counter values are in half clocks (register = 2 * cloc... |
| **`MPARAMS2`** | — | — | `res_drvr_sony_fdhd.s:3103` | second parameter set: identical to mParams in this ROM (Apple: "change back after getting the 2nd parm set right"); only zone 1 refers to it |
| **`MPARAMSPARE`** | — | — | `res_drvr_sony_fdhd.s:3123` | 32 spare bytes reserved for parameter sets (Apple's comment: "so we don't have to worry about shuffling pieces of the driver about ROM when parameter changes come along"); they hold a message instead |
| **`MPARAMZONES`** | — | — | `res_drvr_sony_fdhd.s:3067` | mParamZones -- last track + 1 and parameter set offset of each zone (Apple: different parameter sets "can be used to optimize the error correction performance to handle variations in peak shift, drive... |
| **`MPHASETBL`** | — | — | `res_drvr_sony_fdhd.s:3210` | mPhaseTbl -- phase register value for each drive register address [CA1 CA0 SEL CA2]: $F0 + CA2 * 4 + CA1 * 2 + CA0 (SEL is not a phase line; LSTRB = 0, all four lines outputs) |
| **`MPP_ATPNAME`** | `0x01B0D6` | `0x033E8A` | `res_drvr_mpp.s:1644`<br>`res_drvr_mpp.s:2059` | MPP_ATPNAME MPP_ATPNAME: driver name for the _Open of .ATP |
| **`MPP_CONFIG_TBL`** | `0x01B11A` | `0x033ECE` | `res_drvr_mpp.s:1680`<br>`res_drvr_mpp.s:2089` | MPP_CONFIG_TBL: copied by E_MPP_Open: VSTData (6), vSCCEnable, abort-sequence delay |
| **`MPP_COPYRIGHT`** | — | `0x033F06` | `res_drvr_mpp.s:2112` | — |
| **`MPP_DONE`** | `0x01A980` | `0x0334E0` | `res_drvr_mpp.s:556`<br>`res_drvr_mpp.s:765` | MPP_DONE / MPP_DONE_A1: IODone with D0 (A1 = .MPP DCE from AbusDCE / already in A1) |
| **`MPP_DONE_A1`** | `0x01A984` | `0x0334E4` | `res_drvr_mpp.s:558`<br>`res_drvr_mpp.s:767` | — |
| **`MPP_FINDDAS`** | — | `0x03326A` | `res_drvr_mpp.s:367` | MPP_FINDDAS: dynamic socket D1 ($80..$FE): D2 = offset of its listener in the table at +$8C ((D1 - $80) * 4) if it is open, else D2 = -1. Called by CLOSESKT, DDPWRITE. |
| **`MPP_FINDDAS_EXIT`** | — | `0x033286` | `res_drvr_mpp.s:380` | — |
| **`MPP_FINDDAS_NONE`** | — | `0x033284` | `res_drvr_mpp.s:378` | — |
| **`MPP_FINDPH`** | `0x01A94C` | `0x033484` | `res_drvr_mpp.s:510`<br>`res_drvr_mpp.s:704` | MPP_FINDPH: find LAP type D1 in the protocol table -> EQ and D2 = entry if found |
| **`MPP_FINDPH_LOOP`** | `0x01A94E` | `0x033486` | `res_drvr_mpp.s:512`<br>`res_drvr_mpp.s:706` | — |
| **`MPP_FINDSKT`** | `0x01A80C` | `0x03325E` | `res_drvr_mpp.s:249`<br>`res_drvr_mpp.s:355` | MPP_FINDSKT: find socket D1 in the socket table -> EQ and D2 = entry if found |
| **`MPP_FINDSKT_LOOP`** | `0x01A80E` | `0x033260` | `res_drvr_mpp.s:251`<br>`res_drvr_mpp.s:357` | — |
| **`MPP_INSTALLNBP`** | `0x01A7A0` | `0x0331CE` | `res_drvr_mpp.s:172`<br>`res_drvr_mpp.s:257` | MPP_INSTALLNBP: store NRPtr = NBP_DISPATCH (bit 31 set) and jump into it; E_MPP_Open calls this with D3 = 7, i.e. NBP_INIT |
| **`MPP_JDDPWRITE`** | `0x01A820` | `0x033290` | `res_drvr_mpp.s:271`<br>`res_drvr_mpp.s:396` | MPP_JDDPWRITE: JDDPWrite+0 (MPP variables +$96) - DDPWRITE |
| **`MPP_JOPENSOCKET`** | `0x01A822` | `0x033292` | `res_drvr_mpp.s:278`<br>`res_drvr_mpp.s:398` | MPP_JOPENSOCKET: JDDPWrite+2 - MPP_OPENSOCKET |
| **`MPP_LAPSEND`** | `0x01B0CC` | `0x033E80` | `res_drvr_mpp.s:1634`<br>`res_drvr_mpp.s:2054` | MPP_LAPSEND: LAPWRITE, then set +$B0 (fSendENQ, here a 'sent' flag) when the write has finished (now or later from the deferred write) |
| **`MPP_OPENSOCKET`** | `0x01A7B8` | `0x0331E6` | `res_drvr_mpp.s:196`<br>`res_drvr_mpp.s:281` | MPP_OPENSOCKET: enter socket D1 (0 = assign one) with listener A1 in the socket table -> D1 = socket, D0 = noErr or ddpSktErr.  Uses D2. Also called through JDDPWrite+2 (MPP_JOPENSOCKET) by the NBP co... |
| **`MPP_OPENSOCKET_DAS`** | — | `0x033214` | `res_drvr_mpp.s:305` | dynamic socket: the highest free entry of the table at +$8C |
| **`MPP_OPENSOCKET_DASFOUND`** | — | `0x03322A` | `res_drvr_mpp.s:316` | — |
| **`MPP_OPENSOCKET_DASLOOP`** | — | `0x03321E` | `res_drvr_mpp.s:309` | — |
| **`MPP_OPENSOCKET_EXIT`** | `0x01A7F6` | `0x033210` | `res_drvr_mpp.s:224`<br>`res_drvr_mpp.s:301` | — |
| **`MPP_OPENSOCKET_FREE`** | `0x01A7CA` | — | `res_drvr_mpp.s:206` | find a free entry in the socket table |
| **`MPP_OPENSOCKET_LOOP`** | `0x01A7CC` | `0x0331FA` | `res_drvr_mpp.s:208`<br>`res_drvr_mpp.s:292` | find a free entry in the socket table |
| **`MPP_OPENSOCKET_NOERR`** | — | `0x03320E` | `res_drvr_mpp.s:299` | — |
| **`MPP_OPENSOCKET_STORE`** | `0x01A7EA` | — | `res_drvr_mpp.s:219` | — |
| **`MPP_RANDOM`** | `0x01AB68` | `0x0337AC` | `res_drvr_mpp.s:869`<br>`res_drvr_mpp.s:1195` | MPP_RANDOM: RandomSeed = byte-swapped (RandomSeed * 773 + 1); returns it in D0 |
| **`MPP_RTMPREQUEST`** | `0x01B098` | `0x033E4C` | `res_drvr_mpp.s:1609`<br>`res_drvr_mpp.s:2030` | MPP_RTMPREQUEST: broadcast an RTMP request (DDP type 5, socket 1 to socket 1) as a LAP frame built on the stack, and wait until it is sent. Routers answer with RTMP data, handled by RTMP_LISTENER. |
| **`MPP_RTMPREQUEST_WAIT`** | `0x01B0C0` | `0x033E74` | `res_drvr_mpp.s:1623`<br>`res_drvr_mpp.s:2044` | — |
| **`MPP_SCCINIT`** | `0x01AEDA` | `0x033BC0` | `res_drvr_mpp.s:1427`<br>`res_drvr_mpp.s:1770` | MPP_SCCINIT: write a table of words (value << 8) + register to SCC channel B (register number, then value) up to a 0 word |
| **`MPP_SCCINIT_LOOP`** | `0x01AEDE` | `0x033BC4` | `res_drvr_mpp.s:1429`<br>`res_drvr_mpp.s:1772` | — |
| **`MPP_SCCLAP_TBL`** | `0x01B0F6` | `0x033EAA` | `res_drvr_mpp.s:1668`<br>`res_drvr_mpp.s:2077` | MPP_SCCLAP_TBL MPP_SCCLAP_TBL: words (value << 8) + register for MPP_SCCINIT |
| **`MPP_SCCLAP_TBL2`** | `0x01B112` | `0x033EC6` | `res_drvr_mpp.s:1675`<br>`res_drvr_mpp.s:2084` | MPP_SCCLAP_TBL2: clocks and transmitter |
| **`MPP_SCCRESET_TBL`** | `0x01AEEA` | `0x033BD0` | `res_drvr_mpp.s:1442`<br>`res_drvr_mpp.s:1780` | MPP_SCCRESET_TBL MPP_SCCRESET_TBL: channel B after Close - reset, mouse Y (DCD) on |
| **`MPP_SCCSETUP`** | `0x01B0E6` | `0x033E9A` | `res_drvr_mpp.s:1657`<br>`res_drvr_mpp.s:2071` | MPP_SCCSETUP: program SCC channel B for LocalTalk (two tables) |
| **`MPP_SENDENQ`** | `0x01B0DC` | `0x033E90` | `res_drvr_mpp.s:1648`<br>`res_drvr_mpp.s:2063` | MPP_SENDENQ: LAPWRITE_ENQ (lapENQs to D2), then clear fSendENQ when the write has finished |
| **`MPP_TIMING_TBL`** | — | `0x033EE6` | `res_drvr_mpp.s:2103` | MPP_TIMING_TBL: per timing value: time in microseconds (word), overhead of the surrounding code in CPU cycles (byte), loop type ($FF = SCC polling loop, TimeSCCDB; 0 = DBF loop, TimeDBRA) |
| **`MPP_VBLTASK`** | `0x01AB1E` | `0x03375C` | `res_drvr_mpp.s:828`<br>`res_drvr_mpp.s:1155` | MPP_VBLTASK: VBL task, every 20 ticks (A0 = task).  Ages BridgeTime (sysABridge forgotten after 255 periods without RTMP) and resumes a deferred LAPWRITE when VBLDeferCnt runs out. |
| **`MPP_VBLTASK_DEFER`** | `0x01AB32` | `0x033770` | `res_drvr_mpp.s:835`<br>`res_drvr_mpp.s:1162` | deferred write waiting? |
| **`NBP_BCASTREQ`** | `0x01B470` | — | `res_drvr_mpp.s:2201` | NBP_BCASTREQ: request to the whole network (LookupName, verifying RegisterName) |
| **`NBP_BUILDREQ`** | — | `0x0341B0` | `res_drvr_mpp.s:2510` | NBP_BUILDREQ: build the request packet of slot D2 (D2 = slot * 18) for entity A1 in NRVars A3: LkUp (control 2, 1 tuple) to the node of confirmAddr for a ConfirmName, else LkUp to all nodes ($FF) or B... |
| **`NBP_BUILDREQ_BCAST`** | — | `0x0341D0` | `res_drvr_mpp.s:2520` | — |
| **`NBP_BUILDREQ_WDS`** | — | `0x0341DE` | `res_drvr_mpp.s:2528` | WDS: header template, NBP header + tuple address, entity name |
| **`NBP_CLOSE`** | — | `0x033F4E` | `res_drvr_mpp.s:2149` | NBP_CLOSE: (.MPP Close) remove the retry timers of all active NBP requests; the requests are not completed |
| **`NBP_CLOSE_LOOP`** | — | `0x033F54` | `res_drvr_mpp.s:2152` | — |
| **`NBP_CLOSE_NEXT`** | — | `0x033F66` | `res_drvr_mpp.s:2159` | — |
| **`NBP_CMPENTITY`** | — | `0x0340AA` | `res_drvr_mpp.s:2371` | NBP_CMPENTITY: compare object and type (with their length bytes) of the names-table entry A0 (its ntEntity at +9) with the name at A1, by _CmpString (case-insensitive) -> EQ if equal.  Uses D0-D1, A0.... |
| **`NBP_CMPNAME`** | `0x01B2D0` | `0x034664` | `res_drvr_mpp.s:1922`<br>`res_drvr_mpp.s:3104` | NBP_CMPNAME: compare the Pascal strings at A0 and A1 with the CmpString routine in A2 (A0/A1 -> text, D0 = lengths) -> EQ if equal (case-insensitive) |
| **`NBP_CMPSTRINGTRAP`** | `0x01B2CE` | `0x034662` | `res_drvr_mpp.s:1917`<br>`res_drvr_mpp.s:3099` | NBP_CMPSTRINGTRAP - the _CmpString trap word ($A03C), for _GetTrapAddress |
| **`NBP_COMPLETE`** | — | `0x0342F2` | `res_drvr_mpp.s:2652` | — |
| **`NBP_COMPLETE_EXIT`** | — | `0x03433C` | `res_drvr_mpp.s:2681` | — |
| **`NBP_COMPLETE_FREE`** | — | `0x03432C` | `res_drvr_mpp.s:2674` | — |
| **`NBP_COMPLETE_LOOP`** | — | `0x0342F8` | `res_drvr_mpp.s:2655` | — |
| **`NBP_COMPLETE_NEXT`** | — | `0x034340` | `res_drvr_mpp.s:2684` | — |
| **`NBP_COMPLETE_NOERR`** | — | `0x0342F0` | `res_drvr_mpp.s:2650` | NBP_COMPLETE: complete the active NBP call A0 with D0: free its slot, stop its retry timer (unless it has just run out: vblCount 0), set ioResult and call its ioCompletion -> D0 = 0; D0 = cbNotFound i... |
| **`NBP_COMPLETE_NOTFOUND`** | — | `0x034344` | `res_drvr_mpp.s:2687` | — |
| **`NBP_DISPATCH`** | `0x01B2E4` | `0x033F22` | `res_drvr_mpp.s:1946`<br>`res_drvr_mpp.s:2121` | NBP_DISPATCH: NBP code entry (NRPtr).  D3 = csCode - 242; entry D3 - 7 of NBP_DISPATCH_TBL is called with A3 = NRVars (A0 = parameter block, A1 = entityPtr / ntQElPtr, D1.B = interval).  D3 < 7: the g... |
| **`NBP_DISPATCH_GOODBYE`** | `0x01B30E` | — | `res_drvr_mpp.s:1966` | NBP_DISPATCH_GOODBYE: goodbye kiss - like UnloadNBP |
| **`NBP_DISPATCH_TBL`** | `0x01B300` | `0x033F3E` | `res_drvr_mpp.s:1961`<br>`res_drvr_mpp.s:2135` | NBP_DISPATCH_TBL - offsets from NBP_DISPATCH; entry 0 (249, LoadNBP in the RAM driver) is only reached from E_MPP_Open |
| **`NBP_DONE`** | `0x01B548` | — | `res_drvr_mpp.s:2304` | — |
| **`NBP_DROPAPPLNAMES`** | `0x01B190` | `0x03451E` | `res_drvr_mpp.s:1749`<br>`res_drvr_mpp.s:2943` | NBP_DROPAPPLNAMES: goodbye kiss - unlink every names-table entry that does not lie in the system heap (below the end of SysZone) |
| **`NBP_DROPAPPLNAMES_EXIT`** | `0x01B1B0` | `0x034542` | `res_drvr_mpp.s:1776`<br>`res_drvr_mpp.s:2962` | NBP_DROPAPPLNAMES_EXIT end of the names table |
| **`NBP_DROPAPPLNAMES_KEEP`** | `0x01B1AC` | `0x03453E` | `res_drvr_mpp.s:1767`<br>`res_drvr_mpp.s:2958` | NBP_DROPAPPLNAMES_KEEP keep the entry, go on from it |
| **`NBP_DROPAPPLNAMES_LOOP`** | `0x01B198` | `0x034526` | `res_drvr_mpp.s:1752`<br>`res_drvr_mpp.s:2946` | — |
| **`NBP_ENTERNAME`** | `0x01B3D2` | `0x03402C` | `res_drvr_mpp.s:2094`<br>`res_drvr_mpp.s:2291` | NBP_ENTERNAME: enter names-table entry A1: tuple node = our node, a tuple enumerator not yet used on its socket, linked in at the end; then complete the call with noErr |
| **`NBP_ENTERNAME_ENUM`** | `0x01B3D8` | `0x034038` | `res_drvr_mpp.s:2097`<br>`res_drvr_mpp.s:2296` | — |
| **`NBP_ENTERNAME_LINK`** | `0x01B3F6` | `0x034056` | `res_drvr_mpp.s:2117`<br>`res_drvr_mpp.s:2311` | NBP_ENTERNAME_LINK fill in the tuple, link the entry at the end (A0 = last entry) |
| **`NBP_ENTERNAME_LOOP`** | `0x01B3DE` | `0x03403E` | `res_drvr_mpp.s:2100`<br>`res_drvr_mpp.s:2299` | — |
| **`NBP_FINDNAME`** | `0x01B428` | `0x034088` | `res_drvr_mpp.s:2162`<br>`res_drvr_mpp.s:2347` | NBP_FINDNAME NBP_FINDNAME: find the entry whose object and type equal those at A1 (_CmpString over both strings and their length bytes) -> D3 = entry, NE; or D3 = 0, EQ.  Preserves the other registers... |
| **`NBP_FINDNAME_EXIT`** | `0x01B45A` | `0x0340A4` | `res_drvr_mpp.s:2185`<br>`res_drvr_mpp.s:2361` | — |
| **`NBP_FINDNAME_LOOP`** | `0x01B434` | `0x034094` | `res_drvr_mpp.s:2167`<br>`res_drvr_mpp.s:2352` | — |
| **`NBP_FINDPENDING`** | — | `0x0340C4` | `res_drvr_mpp.s:2389` | NBP_FINDPENDING: is the name at A1 being registered by a pending RegisterName (one of the active NBP requests)? -> NE (D3 = -1) if so, EQ (D3 = 0) if not.  A3 = NRVars.  Called by REGISTERNAME. |
| **`NBP_FINDPENDING_EXIT`** | — | `0x0340F6` | `res_drvr_mpp.s:2408` | — |
| **`NBP_FINDPENDING_LOOP`** | — | `0x0340CC` | `res_drvr_mpp.s:2393` | — |
| **`NBP_FINDPENDING_NEXT`** | — | `0x0340FE` | `res_drvr_mpp.s:2412` | — |
| **`NBP_FREESKT`** | `0x01B316` | — | `res_drvr_mpp.s:1972` | NBP_FREESKT: unreferenced - remove socket D0 from the socket table |
| **`NBP_FREESKT_LOOP`** | `0x01B318` | — | `res_drvr_mpp.s:1974` | — |
| **`NBP_INIT`** | `0x01B328` | `0x033F6C` | `res_drvr_mpp.s:1987`<br>`res_drvr_mpp.s:2175` | NBP_INIT: allocate NRVars and open the NBP socket (dynamic number, listener NBP_LISTENER), on which requests go out and replies come in. NRVars ($47 bytes): +$00 NBP socket, +$01 NBP ID, +$02 dest net... |
| **`NBP_INIT_EXIT`** | `0x01B354` | `0x033F94` | `res_drvr_mpp.s:2002`<br>`res_drvr_mpp.s:2188` | — |
| **`NBP_INIT_FAIL`** | `0x01B356` | `0x033F96` | `res_drvr_mpp.s:2009`<br>`res_drvr_mpp.s:2191` | NBP_INIT_FAIL: free the block, return the error |
| **`NBP_IODONE`** | — | `0x034022` | `res_drvr_mpp.s:2280` | NBP_IODONE: IODone with D0 (completes the call at the head of the .MPP queue) Called by: KILLNBP, REGISTERNAME, UNLOADNBP, REMOVENAME, NBP_SENDREQ |
| **`NBP_LISTENER`** | `0x01B5A2` | `0x03438E` | `res_drvr_mpp.s:2371`<br>`res_drvr_mpp.s:2736` | NBP_LISTENER: listener of the NBP socket - replies to our requests. Reads the NBP header; drops it unless a call is active and the NBP ID matches.  LookupName: the tuples go straight into the return b... |
| **`NBP_LISTENER_COUNTED`** | `0x01B616` | `0x03440E` | `res_drvr_mpp.s:2427`<br>`res_drvr_mpp.s:2794` | NBP_LISTENER_COUNTED none complete: ignore the packet |
| **`NBP_LISTENER_COUNTLOOP`** | `0x01B5F4` | `0x0343EC` | `res_drvr_mpp.s:2403`<br>`res_drvr_mpp.s:2775` | LookupName: read the tuples into the return buffer truncated: count the complete tuples |
| **`NBP_LISTENER_COUNTNEW`** | `0x01B680` | `0x034472` | `res_drvr_mpp.s:2490`<br>`res_drvr_mpp.s:2852` | — |
| **`NBP_LISTENER_DEDUP`** | `0x01B61A` | `0x034414` | `res_drvr_mpp.s:2431`<br>`res_drvr_mpp.s:2798` | remove tuples already in the buffer (same address and enumerator) |
| **`NBP_LISTENER_DEDUPLOOP`** | `0x01B62E` | `0x034422` | `res_drvr_mpp.s:2438`<br>`res_drvr_mpp.s:2804` | — |
| **`NBP_LISTENER_DISCARD`** | `0x01B59C` | `0x034388` | `res_drvr_mpp.s:2359`<br>`res_drvr_mpp.s:2724` | NBP_LISTENER_DISCARD: drop the packet |
| **`NBP_LISTENER_DONE`** | — | `0x03449E` | `res_drvr_mpp.s:2871` | complete the LookupName (noErr) unless .MPP is still sending its first request (the call is still at the head of the queue) |
| **`NBP_LISTENER_DROP`** | `0x01B6B6` | `0x0344B6` | `res_drvr_mpp.s:2514`<br>`res_drvr_mpp.s:2880` | NBP_LISTENER_DROP: duplicate - skip the new tuple (it is overwritten by the next kept one) |
| **`NBP_LISTENER_DUPLICATE`** | `0x01B58A` | `0x034376` | `res_drvr_mpp.s:2340`<br>`res_drvr_mpp.s:2712` | NBP_LISTENER_DUPLICATE: someone answered the verifying LkUp of a RegisterName - nbpDuplicate |
| **`NBP_LISTENER_EXIT`** | `0x01B59A` | `0x034386` | `res_drvr_mpp.s:2352`<br>`res_drvr_mpp.s:2721` | NBP_LISTENER_EXIT return to MPP |
| **`NBP_LISTENER_IDLOOP`** | — | `0x0343A2` | `res_drvr_mpp.s:2745` | — |
| **`NBP_LISTENER_INPLACE`** | `0x01B67E` | `0x034470` | `res_drvr_mpp.s:2488`<br>`res_drvr_mpp.s:2850` | NBP_LISTENER_INPLACE in place |
| **`NBP_LISTENER_KEEP`** | `0x01B660` | `0x034452` | `res_drvr_mpp.s:2469`<br>`res_drvr_mpp.s:2836` | NBP_LISTENER_KEEP keep the new tuple: move it down to A6 if tuples were dropped |
| **`NBP_LISTENER_NEXTTUPLE`** | `0x01B682` | `0x034474` | `res_drvr_mpp.s:2492`<br>`res_drvr_mpp.s:2854` | — |
| **`NBP_LISTENER_NOTLKUP`** | `0x01B560` | `0x03434A` | `res_drvr_mpp.s:2320`<br>`res_drvr_mpp.s:2696` | NBP_LISTENER_NOTLKUP: reply for a RegisterName (-> nbpDuplicate) or a ConfirmName: newSocket = socket of the first tuple; noErr if it is the socket of confirmAddr, else nbpConfDiff |
| **`NBP_LISTENER_RTS`** | — | `0x0344B4` | `res_drvr_mpp.s:2877` | — |
| **`NBP_LISTENER_SCANLOOP`** | `0x01B630` | `0x034424` | `res_drvr_mpp.s:2440`<br>`res_drvr_mpp.s:2806` | — |
| **`NBP_LISTENER_SCANNEXT`** | `0x01B64E` | `0x034440` | `res_drvr_mpp.s:2455`<br>`res_drvr_mpp.s:2821` | — |
| **`NBP_LKUPREPLY`** | `0x01B1B2` | `0x034544` | `res_drvr_mpp.s:1788`<br>`res_drvr_mpp.s:2973` | NBP_LKUPREPLY: LookupReply call, A0 = the lookup-reply block with the LkUp packet at csParam (+$1C control, +$1D NBP ID, +$1E tuple of the requester, +$23 entity name).  Collects the names-table entri... |
| **`NBP_LKUPREPLY_DONE`** | `0x01B2A6` | `0x034638` | `res_drvr_mpp.s:1887`<br>`res_drvr_mpp.s:3072` | done |
| **`NBP_LKUPREPLY_IODONE`** | `0x01B2AC` | `0x03463E` | `res_drvr_mpp.s:1892`<br>`res_drvr_mpp.s:3077` | NBP_LKUPREPLY_IODONE: complete the LookupReply call (its completion routine frees the block) |
| **`NBP_LKUPREPLY_LOOP`** | `0x01B1D0` | `0x034562` | `res_drvr_mpp.s:1800`<br>`res_drvr_mpp.s:2985` | scan the names table; matching entries are pushed on the stack |
| **`NBP_LKUPREPLY_MATCH`** | `0x01B208` | `0x03459A` | `res_drvr_mpp.s:1824`<br>`res_drvr_mpp.s:3009` | match: remember the entity |
| **`NBP_LKUPREPLY_NEXT`** | `0x01B20C` | `0x03459E` | `res_drvr_mpp.s:1828`<br>`res_drvr_mpp.s:3013` | next entry |
| **`NBP_LKUPREPLY_PACKET`** | `0x01B23A` | `0x0345CC` | `res_drvr_mpp.s:1843`<br>`res_drvr_mpp.s:3028` | DDP header template at +$1F (odd) to the requester's socket, WDS at +$30 one LkUp-Reply packet |
| **`NBP_LKUPREPLY_SEND`** | `0x01B28C` | `0x03461E` | `res_drvr_mpp.s:1874`<br>`res_drvr_mpp.s:3059` | send the packet and wait for the write |
| **`NBP_LKUPREPLY_TUPLE`** | `0x01B252` | `0x0345E4` | `res_drvr_mpp.s:1852`<br>`res_drvr_mpp.s:3037` | one WDS entry per tuple, straight from the names-table entry |
| **`NBP_LKUPREPLY_TYPE`** | `0x01B1EC` | `0x03457E` | `res_drvr_mpp.s:1811`<br>`res_drvr_mpp.s:2996` | object matches: compare the types |
| **`NBP_LKUPREPLY_WAIT`** | `0x01B29C` | `0x03462E` | `res_drvr_mpp.s:1881`<br>`res_drvr_mpp.s:3066` | — |
| **`NBP_NEWPTR`** | `0x01B35E` | — | `res_drvr_mpp.s:2019` | NBP_NEWPTR: zeroed block of D0 bytes in the system heap -> A0, D0 |
| **`NBP_NEWPTR_EXIT`** | `0x01B364` | — | `res_drvr_mpp.s:2023` | — |
| **`NBP_SENDREPLY`** | `0x01B2B6` | `0x03464A` | `res_drvr_mpp.s:1903`<br>`res_drvr_mpp.s:3088` | NBP_SENDREPLY: DDPWrite the WDS at +$30 of the lookup-reply block (A4) from socket 2 (NIS), no checksum; sets the write-done flag (+$2F) when the write has finished |
| **`NBP_SENDREQ`** | `0x01B472` | `0x034108` | `res_drvr_mpp.s:2206`<br>`res_drvr_mpp.s:2438` | NBP_SENDREQ: send the request for entity A1 and start the retry timer (interval D1 * 8 ticks).  D2 = address: with a node, a LkUp goes to that node; else to all ($FF) or, if a bridge is known, a BrRq ... |
| **`NBP_SENDREQ_DEQUEUED`** | — | `0x034180` | `res_drvr_mpp.s:2481` | retry timer: the slot's VBL task send the request take the call off the .MPP queue, keep it pending |
| **`NBP_SENDREQ_ID`** | — | `0x03411A` | `res_drvr_mpp.s:2445` | — |
| **`NBP_SENDREQ_SETUP`** | `0x01B484` | — | `res_drvr_mpp.s:2216` | active call, destination network, retry timer |
| **`NBP_SENDREQ_SLOT`** | — | `0x03410E` | `res_drvr_mpp.s:2441` | — |
| **`NBP_STARTNEXT`** | — | `0x034192` | `res_drvr_mpp.s:2488` | NBP_STARTNEXT: start the next queued call, if any (as a new E_MPP_Control); entered with SR on the stack, A1 = .MPP DCE |
| **`NBP_STARTNEXT_NONE`** | — | `0x0341AC` | `res_drvr_mpp.s:2498` | — |
| **`NBP_TIMEOUT`** | `0x01B52A` | `0x0342B8` | `res_drvr_mpp.s:2286`<br>`res_drvr_mpp.s:2617` | NBP_TIMEOUT: retries used up - RegisterName: nobody has the name, enter it; ConfirmName: nbpNoConfirm; LookupName: done (noErr) |
| **`NBP_TIMEOUT_DONE`** | — | `0x0342EA` | `res_drvr_mpp.s:2636` | — |
| **`NBP_TIMEOUT_EXIT`** | — | `0x0342EC` | `res_drvr_mpp.s:2638` | — |
| **`NBP_TIMEOUT_NOERR`** | — | `0x0342E8` | `res_drvr_mpp.s:2634` | — |
| **`NBP_TIMEOUT_REGISTER`** | — | `0x0342E4` | `res_drvr_mpp.s:2632` | — |
| **`NBP_VBLTASK`** | `0x01B502` | `0x034232` | `res_drvr_mpp.s:2267`<br>`res_drvr_mpp.s:2566` | NBP_VBLTASK: NBP retry timer (A0 = task): count - 1; at 0 NBP_TIMEOUT, else send the request again after interval * 8 ticks |
| **`NBP_VBLTASK_BUILD`** | — | `0x03427E` | `res_drvr_mpp.s:2593` | — |
| **`NBP_VBLTASK_LATER`** | — | `0x034250` | `res_drvr_mpp.s:2577` | .MPP busy: try again at the next tick |
| **`NBP_VBLTASK_RESEND`** | — | `0x03425C` | `res_drvr_mpp.s:2582` | resend: timer = interval * 8 ticks, rebuild the packet, DDPWrite |
| **`NBP_VBLTASK_TIMEOUT`** | — | `0x0342AA` | `res_drvr_mpp.s:2609` | no more retries; while .MPP still sends this very call's first request, wait |
| **`NBP_WRITE`** | `0x01B4F4` | — | `res_drvr_mpp.s:2255` | WDS: header template, NBP header + tuple address, entity name NBP_WRITE: DDPWrite the request from the NBP socket (D1), no checksum |
| **`NIS_LISTENER`** | `0x01B144` | `0x0344CC` | `res_drvr_mpp.s:1703`<br>`res_drvr_mpp.s:2902` | NIS_LISTENER: +4 - listener of socket 2 (names information socket). Reads a received LkUp packet into the lookup-reply parameter block (at csParam) and issues the LookupReply call (csCode 242) to this... |
| **`NIS_LISTENER_BUSY`** | `0x01B188` | `0x034516` | `res_drvr_mpp.s:1733`<br>`res_drvr_mpp.s:2930` | NIS_LISTENER_BUSY: block in use - drop the packet |
| **`NIS_LISTENER_EXIT`** | `0x01B186` | `0x034514` | `res_drvr_mpp.s:1726`<br>`res_drvr_mpp.s:2927` | — |
| **`NIS_LISTENER_QUEUE`** | `0x01B16A` | `0x0344F8` | `res_drvr_mpp.s:1718`<br>`res_drvr_mpp.s:2919` | queue the LookupReply call |
| **`NIS_LUCOMPLETION`** | `0x01B2DE` | `0x034672` | `res_drvr_mpp.s:1936`<br>`res_drvr_mpp.s:3117` | NIS_LUCOMPLETION: ioCompletion of the LookupReply call - csCode = 0 (the lookup-reply block is free again) |
| **`NSENDREQUEST`** | — | `0x032952` | `res_drvr_atp.s:774` | fill in the request slot; next transaction ID socket and retry timer of the slot send the TReq NSendRequest (csCode 248, IM V-516): like SendRequest, but through the open responding socket atpSocket (... |
| **`NSENDREQUEST_COUNTED`** | — | `0x03297E` | `res_drvr_atp.s:795` | — |
| **`NSENDREQUEST_EXIT`** | — | `0x03298A` | `res_drvr_atp.s:800` | — |
| **`NSENDREQUEST_LOOP`** | — | `0x03296A` | `res_drvr_atp.s:786` | — |
| **`NSENDREQUEST_QUEUE`** | — | `0x03298E` | `res_drvr_atp.s:803` | queue the call on the socket, send the TReq |
| **`NSENDREQUEST_TID`** | — | `0x03295E` | `res_drvr_atp.s:781` | count the NSendRequests of the socket; skip TIDs they use |
| **`OPENATPSKT`** | `0x019EEE` | `0x032646` | `res_drvr_atp.s:251`<br>`res_drvr_atp.s:351` | OpenATPSkt (csCode 254): open a responding socket.  atpSocket = socket to open (0 = assign one), addrBlock = addresses to accept requests from (0 in a field = any).  Opens the DDP socket with ATP_LIST... |
| **`OPENATPSKT_LOOP`** | `0x019EF4` | `0x03264C` | `res_drvr_atp.s:254`<br>`res_drvr_atp.s:354` | — |
| **`OPENSKT`** | `0x01A7B0` | `0x0331DE` | `res_drvr_mpp.s:185`<br>`res_drvr_mpp.s:269` | OPENSKT OpenSkt (csCode 248): socket = 1..127 to open that socket, 0 to get a new one (128..254, returned in socket); listener = socket listener. ddpSktErr if in use, >= 128 or the socket table (14 en... |
| **`P_SoundVBL_task4Tone`** | `0x017B76` | `0x036E48` | `res_drvr_sound.s:463`<br>`res_drvr_sound.s:424` | P_SoundVBL_task4Tone -- VBL task of the four-tone synthesizer: while the FTSoundRec's duration is not 0, decrement it and mix the 370 samples of the next frame. Each tone: phase += rate (16.16), sampl... |
| **`P_SoundVBL_taskFreeForm`** | `0x017C82` | `0x036F60` | `res_drvr_sound.s:597`<br>`res_drvr_sound.s:559` | P_SoundVBL_taskFreeForm -- VBL task of the free-form synthesizer: resample the next 370 samples of the request at the head of the queue into the buffer, advancing the source by count (16.16) bytes per... |
| **`P_SoundVBL_taskSquareWave`** | `0x017B2A` | `0x036DFC` | `res_drvr_sound.s:400`<br>`res_drvr_sound.s:365` | P_SoundVBL_taskSquareWave -- VBL task (vblAddr) of the square-wave synthesizer: the current tone's duration is over; play the next triplet if the buffer has one, else stop and complete the request. io... |
| **`PACK_7_POW10_TABLE`** | `0x01CF1E` | `0x01D886` | `res_pack_7.s:850`<br>`res_pack_7.s:852` | PACK_7_POW10_TABLE (Apple tens): divisors for printing an exponent (or a NaN code) of up to 5 decimal digits with DIVU, highest place first. |
| **`POWER_TBL`** | `0x01EDE6` | `0x01CFDA` | `res_pack_4.s:2293`<br>`res_pack_4.s:2295` | — |
| **`PRINT_CHK_DRVR`** | `0x01797A` | — | `res_drvr_print.s:168` | PRINT_CHK_DRVR: check if printer driver DRVR 2 exists in System file Returns NE if found, EQ if not |
| **`PRINT_CHK_NOTFOUND`** | `0x0179AA` | — | `res_drvr_print.s:187` | verify it's in the System file (not app) |
| **`PRINT_CLOSE`** | `0x017880` | — | `res_drvr_print.s:51` | drvrClose: offset $10 |
| **`PRINT_CTL`** | `0x017878` | — | `res_drvr_print.s:43` | drvrCtl: offset $0C |
| **`PRINT_ERR_EXIT`** | `0x01793C` | — | `res_drvr_print.s:130` | common error exit: store error and return to caller |
| **`PRINT_GET_VREFNUM`** | `0x01795C` | — | `res_drvr_print.s:149` | PRINT_GET_VREFNUM PRINT_GET_VREFNUM: get current volume VRefNum (returns in D0) |
| **`PRINT_INSTALL_PRER`** | `0x017900` | — | `res_drvr_print.s:107` | detach resource so it persists after CloseResFile verify printer driver file exists on expected volume install PRER as the printer driver in the DCE |
| **`PRINT_LOAD_PRER`** | `0x017884` | — | `res_drvr_print.s:56` | PRINT_LOAD_PRER: load printer driver resource and dispatch D1 = offset into PRER to jump to, A0 = IOParam, A1 = DCE |
| **`PRINT_OPEN`** | `0x017870` | — | `res_drvr_print.s:35` | drvrOpen: offset $08 into PRER resource |
| **`PRINT_OPEN_FAILED`** | `0x017932` | — | `res_drvr_print.s:125` | restore saved state and jump to PRER entry point error: printer driver not found on this volume |
| **`PRINT_PRIME`** | `0x017874` | — | `res_drvr_print.s:39` | drvrPrime: offset $0A |
| **`PRINT_RTS`** | `0x01795A` | — | `res_drvr_print.s:141` | immediate call: plain RTS, otherwise return through IODone |
| **`PRINT_SET_VOL`** | `0x01795E` | — | `res_drvr_print.s:152` | PRINT_SET_VOL: set volume to D0, then get current volume back |
| **`PRINT_STATUS`** | `0x01787C` | — | `res_drvr_print.s:47` | drvrStatus: offset $0E |
| **`READ_EXIT`** | `0x01AE32` | `0x033AE2` | `res_drvr_mpp.s:1321`<br>`res_drvr_mpp.s:1649` | READ_EXIT: restore A4/A5 (SaveA45), condition codes from D0 |
| **`READ_EXIT_RESULT`** | — | `0x033AF0` | `res_drvr_mpp.s:1654` | — |
| **`READPACKET`** | `0x01AE3C` | `0x033AF4` | `res_drvr_mpp.s:1334`<br>`res_drvr_mpp.s:1666` | READPACKET: read D3 bytes of the packet into (A3)+; D1 -= D3.  D0/ condition codes = 0 if all were read; on overrunErr (-1), underrunErr (-3, timeout) or lengthErr (-4, frame ended early) the receiver... |
| **`READPACKET_ERR`** | `0x01AE68` | `0x033B2E` | `res_drvr_mpp.s:1368`<br>`res_drvr_mpp.s:1695` | — |
| **`READPACKET_EXIT`** | `0x01AE3A` | `0x033AF2` | `res_drvr_mpp.s:1324`<br>`res_drvr_mpp.s:1656` | — |
| **`READPACKET_JMP`** | — | `0x033A6E` | `res_drvr_mpp.s:1595` | LAP_READ_JT: A4 for protocol handlers and socket listeners - JSR (A4) = ReadPacket (through READPACKET_JMP, out of BRA.B range), JSR 2(A4) = ReadRest |
| **`READPACKET_LENERR`** | `0x01AE66` | `0x033B28` | `res_drvr_mpp.s:1366`<br>`res_drvr_mpp.s:1692` | READPACKET_LENERR: frame shorter than its length word - lengthErr |
| **`READPACKET_LOOP`** | `0x01AE3E` | `0x033AF6` | `res_drvr_mpp.s:1336`<br>`res_drvr_mpp.s:1668` | — |
| **`READPACKET_TIMEOUT`** | `0x01AE62` | `0x033B20` | `res_drvr_mpp.s:1358`<br>`res_drvr_mpp.s:1687` | frame ended early or overrun? READPACKET_TIMEOUT: no byte came - underrunErr |
| **`READPACKET_WAIT`** | `0x01AE40` | `0x033AFA` | `res_drvr_mpp.s:1338`<br>`res_drvr_mpp.s:1670` | — |
| **`READREST`** | `0x01ADC6` | `0x033A74` | `res_drvr_mpp.s:1276`<br>`res_drvr_mpp.s:1608` | READREST: read the rest of the packet (D1 bytes left) into the buffer at A3, D3 bytes long (excess bytes are dropped), then check the CRC (LAP_RCVCRC).  D3 = 0 if it fit exactly, > 0 if bytes were lef... |
| **`READREST_END`** | `0x01ADF0` | `0x033AA0` | `res_drvr_mpp.s:1303`<br>`res_drvr_mpp.s:1630` | READREST_END end of packet: CRC, then let PollProc have the saved modem-port bytes |
| **`READREST_LOOP`** | `0x01ADCC` | `0x033A7A` | `res_drvr_mpp.s:1280`<br>`res_drvr_mpp.s:1612` | byte loop |
| **`READREST_NOPOLL`** | `0x01AE28` | `0x033AD8` | `res_drvr_mpp.s:1317`<br>`res_drvr_mpp.s:1644` | — |
| **`READREST_STORE`** | `0x01ADE8` | `0x033A98` | `res_drvr_mpp.s:1292`<br>`res_drvr_mpp.s:1624` | — |
| **`READREST_WAIT`** | `0x01ADD2` | `0x033A82` | `res_drvr_mpp.s:1284`<br>`res_drvr_mpp.s:1616` | — |
| **`REGISTERNAME`** | `0x01B36E` | `0x033FBE` | `res_drvr_mpp.s:2044`<br>`res_drvr_mpp.s:2233` | RegisterName (csCode 253): enter the names-table entry at ntQElPtr (address, entity) in the names table; the first call opens the NIS (socket 2) and allocates the lookup-reply block.  With verifyFlag ... |
| **`REGISTERNAME_DUP`** | — | `0x034018` | `res_drvr_mpp.s:2267` | — |
| **`REGISTERNAME_ENTER`** | — | `0x03401E` | `res_drvr_mpp.s:2271` | — |
| **`REGISTERNAME_FAIL`** | `0x01B3CE` | `0x03401C` | `res_drvr_mpp.s:2085`<br>`res_drvr_mpp.s:2269` | REGISTERNAME_FAIL - complete the NBP call with D0 (also RemoveName) |
| **`REGISTERNAME_NISOK`** | `0x01B3B2` | `0x033FFA` | `res_drvr_mpp.s:2073`<br>`res_drvr_mpp.s:2255` | first registration: lookup-reply block and the NIS REGISTERNAME_NISOK NIS open |
| **`REGISTERNAME_VERIFY`** | `0x01B3BA` | `0x034002` | `res_drvr_mpp.s:2077`<br>`res_drvr_mpp.s:2259` | verify the name first? |
| **`RELRSPCB`** | `0x01A38C` | `0x032CBC` | `res_drvr_atp.s:890`<br>`res_drvr_atp.s:1253` | RelRspCB (csCode 249): release the RspCB of (atpSocket, addrBlock, transID) without waiting for TRel or the release timer; its SendResponse, if any, completes with noErr.  cbNotFound. |
| **`RELRSPCB_DONE`** | `0x01A3A6` | `0x032CD6` | `res_drvr_atp.s:900`<br>`res_drvr_atp.s:1263` | — |
| **`RELTCB`** | `0x01A334` | `0x032C64` | `res_drvr_atp.s:843`<br>`res_drvr_atp.s:1211` | RelTCB (csCode 256): abort the SendRequest with transID to addrBlock: close its socket, free its slot and complete it with reqAborted. cbNotFound, noDataArea. |
| **`RELTCB_ABORT`** | — | `0x032CB0` | `res_drvr_atp.s:1241` | RELTCB_ABORT - complete request A0 with reqAborted (also KillSendReq) |
| **`RELTCB_DONE`** | `0x01A388` | `0x032CB8` | `res_drvr_atp.s:881`<br>`res_drvr_atp.s:1245` | RELTCB_DONE - complete the RelTCB / RelRspCB call with noErr |
| **`RELTCB_FOUND`** | `0x01A366` | `0x032C94` | `res_drvr_atp.s:870`<br>`res_drvr_atp.s:1232` | RELTCB_FOUND found: A0 = SendRequest, D2 = its slot |
| **`RELTCB_LOOP`** | `0x01A33A` | `0x032C6A` | `res_drvr_atp.s:846`<br>`res_drvr_atp.s:1214` | — |
| **`RELTCB_NEXT`** | `0x01A35A` | `0x032C88` | `res_drvr_atp.s:858`<br>`res_drvr_atp.s:1225` | — |
| **`RELTCB_NOTFOUND`** | `0x01A35E` | `0x032C8C` | `res_drvr_atp.s:861`<br>`res_drvr_atp.s:1228` | RELTCB_NOTFOUND - no such transaction (also used by RelRspCB) |
| **`REMOVENAME`** | `0x01B404` | `0x034066` | `res_drvr_mpp.s:2129`<br>`res_drvr_mpp.s:2323` | RemoveName (csCode 252): unlink the names-table entry with the name at entityPtr.  nbpNotFound. |
| **`REMOVENAME_DONE`** | `0x01B424` | — | `res_drvr_mpp.s:2151` | — |
| **`REMOVENAME_LOOP`** | `0x01B416` | `0x034078` | `res_drvr_mpp.s:2136`<br>`res_drvr_mpp.s:2330` | — |
| **`REMOVENAME_UNLINK`** | `0x01B41E` | `0x034080` | `res_drvr_mpp.s:2147`<br>`res_drvr_mpp.s:2336` | REMOVENAME_UNLINK unlink it |
| **`Resource_bbmc_0000`** | — | `0x01D91C` | `res_bbmc.s:9` | bbmc 0 -- the hidden team photos The picture data of the slide show in res_tcsl.s (started with `G 41D89A` from MacsBug or MicroBug): a table of four frame offsets, then the frames, each 342 PackBits-... |
| **`Resource_bbmc_0000_Header`** | — | `0x01D91C` | `res_bbmc.s:13` | Bbmc 0 resource header. |
| **`Resource_bbmc_0_FrameOffsetTable`** | — | `0x01D924` | `res_bbmc.s:18` | Relative offsets of hidden PackBits frames. |
| **`Resource_bbmc_0_Header`** | — | `0x01D91C` | `res_bbmc.s:11` | Resource header for hidden bitmap resource. |
| **`Resource_CDEF_0000`** | — | `0x037A28` | `res_cdef_0.s:98` | ROM resource header: a block header in the format of the Memory Manager's (tag and physical block size, then a relative-handle field) in front of the resource data, as for every ROM resource. The seco... |
| **`Resource_CDEF_0000_Header`** | — | `0x037A28` | `res_cdef_0.s:99` | ROM resource header: a block header in the format of the Memory Manager's (tag and physical block size, then a relative-handle field) in front of the resource data, as for every ROM resource. The seco... |
| **`Resource_CDEF_0001`** | — | `0x037D52` | `res_cdef_1.s:94` | thumbCntl parameter record (Apple's local variable equates) ROM resource header (block header, see CDEF 0) |
| **`Resource_CDEF_0001_Header`** | — | `0x037D52` | `res_cdef_1.s:95` | thumbCntl parameter record (Apple's local variable equates) ROM resource header (block header, see CDEF 0) |
| **`Resource_CURS_0001`** | — | `0x039C8C` | `res_curs.s:41` | Resource_CURS_0001 (resource-data) ROM offsets +0x39C8C..+0x39CD8. ROM resource type=CURS id=1 name=- attr=0x58; header +0x39C8C, body +0x39C94 |
| **`Resource_CURS_0001_Header`** | — | `0x039C8C` | `res_curs.s:43` | CURS 1 resource header. |
| **`Resource_CURS_0002`** | — | `0x039D24` | `res_curs.s:105` | Resource_CURS_0002 (resource-data) ROM offsets +0x39D24..+0x39D70. ROM resource type=CURS id=2 name=- attr=0x58; header +0x39D24, body +0x39D2C |
| **`Resource_CURS_0002_Header`** | — | `0x039D24` | `res_curs.s:107` | CURS 2 resource header. |
| **`Resource_CURS_0003`** | — | `0x039CD8` | `res_curs.s:73` | Resource_CURS_0003 (resource-data) ROM offsets +0x39CD8..+0x39D24. ROM resource type=CURS id=3 name=- attr=0x58; header +0x39CD8, body +0x39CE0 |
| **`Resource_CURS_0003_Header`** | — | `0x039CD8` | `res_curs.s:75` | CURS 3 resource header. |
| **`Resource_CURS_0004`** | — | `0x039C40` | `res_curs.s:9` | CURS resources -- the standard cursors CURS 4 (watchCursor), 1 (iBeamCursor), 3 (plusCursor) and 2 (crossCursor), in ROM order, each with its 8-byte ROM resource header (ROM offsets +0x39C40..+0x39D70... |
| **`Resource_CURS_0004_Header`** | — | `0x039C40` | `res_curs.s:11` | CURS 4 resource header. |
| **`Resource_DRVR_0003_DotSound`** | — | `0x036C88` | `res_drvr_sound.s:120` | DRVR 3 .Sound -- the Sound Driver: square-wave, four-tone and free-form synthesizers ROM offsets +0x36C88..+0x3701F: the 8-byte header of the ROM resource at +0x36C88, then the driver, $390 bytes from... |
| **`Resource_DRVR_0003_DotSound_Header`** | — | `0x036C88` | `res_drvr_sound.s:121` | DRVR 3 .Sound -- the Sound Driver: square-wave, four-tone and free-form synthesizers ROM offsets +0x36C88..+0x3701F: the 8-byte header of the ROM resource at +0x36C88, then the driver, $390 bytes from... |
| **`Resource_DRVR_0004_DotSony`** | — | `0x034678` | `res_drvr_sony_fdhd.s:112` | DRVR 4 .Sony -- the SuperDrive disk driver of the Macintosh SE FDHD (1989) ROM offsets +0x34678..+0x36C87: the 8-byte resource header (shared by both SE ROMs) and the 9736-byte driver body at +0x34680... |
| **`Resource_DRVR_0004_DotSony_Header`** | — | `0x034678` | `res_drvr_sony_fdhd.s:114` | ROM resource header of DRVR 4 (8 bytes; the same in both SE ROMs) |
| **`Resource_DRVR_0009_DotMPP`** | — | `0x033122` | `res_drvr_mpp.s:133` | DRVR 9 .MPP -- AppleTalk LAP, DDP and NBP driver (SE ROM, version 48) ROM offsets +0x33122..+0x34677: the 8-byte ROM resource header and the driver body from +0x3312A (MacSEROM.lst: _DRVR_9_.MPP). Loc... |
| **`Resource_DRVR_0009_DotMPP_Header`** | — | `0x033122` | `res_drvr_mpp.s:135` | ROM resource header of DRVR 9 (8 bytes) |
| **`Resource_DRVR_000A_DotATP`** | — | `0x0324A2` | `res_drvr_atp.s:118` | DRVR 10 .ATP -- AppleTalk Transaction Protocol driver (SE ROM, version 46) ROM offsets +0x324A2..+0x33121: the 8-byte ROM resource header and the driver body from +0x324AA (MacSEROM.lst: _DRVR_10_.ATP... |
| **`Resource_DRVR_000A_DotATP_Header`** | — | `0x0324A2` | `res_drvr_atp.s:120` | ROM resource header of DRVR 10 (8 bytes) |
| **`Resource_DRVR_0028_DotXPP`** | — | `0x037020` | `res_drvr_xpp.s:325` | session states (scbState) ROM resource header (8 bytes before the driver): $C0 flags + the block size $A08 (header + $A00 bytes of driver, so the next resource follows at +0x37A28); the second long ri... |
| **`Resource_DRVR_0028_DotXPP_Header`** | — | `0x037020` | `res_drvr_xpp.s:326` | session states (scbState) ROM resource header (8 bytes before the driver): $C0 flags + the block size $A08 (header + $A00 bytes of driver, so the next resource follows at +0x37A28); the second long ri... |
| **`Resource_FONT_0000_Chicago`** | — | `0x03AB5A` | `res_font_chicago.s:916` | Resource_FONT_0000_Chicago (resource-data) ROM offsets +0x3AB5A..+0x3AB62. ROM resource type=FONT id=0 name=Chicago attr=0x58; header +0x3AB5A, body +0x3AB62 |
| **`Resource_FONT_0000_Chicago_Header`** | — | `0x03AB5A` | `res_font_chicago.s:918` | FONT 0 resource header. |
| **`Resource_FONT_000C`** | — | `0x039D70` | `res_font_chicago.s:11` | FONT resources -- Chicago (the system font) FONT 12 (Chicago 12 point, +0x39D70) and FONT 0 'Chicago' (+0x3AB5A, the family's name entry: a resource with a name and no data; its body label _FONT_0_Chi... |
| **`Resource_FONT_000C_Header`** | — | `0x039D70` | `res_font_chicago.s:13` | FONT 12 resource header. |
| **`Resource_FONT_0189`** | — | `0x03AB62` | `res_font_geneva.s:8` | FONT resources -- Geneva FONT 393 (Geneva 9, +0x3AB62) and FONT 396 (Geneva 12, +0x3B58C), each with its 8-byte ROM resource header (resource ID = 128 * font family + point size; family 3 = Geneva). N... |
| **`Resource_FONT_0189_Header`** | — | `0x03AB62` | `res_font_geneva.s:10` | FONT 393 resource header. |
| **`Resource_FONT_018C`** | — | `0x03B58C` | `res_font_geneva.s:672` | Resource_FONT_018C (resource-data) ROM offsets +0x3B58C..+0x3C1FC. ROM resource type=FONT id=396 name=- attr=0x58; header +0x3B58C, body +0x3B594 |
| **`Resource_FONT_018C_Header`** | — | `0x03B58C` | `res_font_geneva.s:674` | FONT 396 resource header. |
| **`Resource_FONT_0209`** | — | `0x03C1FC` | `res_font_monaco.s:7` | FONT resource -- Monaco 9 FONT 521 (Monaco 9, family 4; +0x3C1FC) with its 8-byte ROM resource header: the last resource of the ROM (the tail follows in extra/rom_tail.s). New with the SE ROM. |
| **`Resource_FONT_0209_Header`** | — | `0x03C1FC` | `res_font_monaco.s:9` | FONT 521 resource header. |
| **`Resource_KCHR_0000`** | — | `0x03824C` | `res_kchr.s:10` | KCHR 0 -- the keyboard character map (U.S.) Used by KeyTrans ($A9C3, os/adb_mgr.s) to turn a virtual key code and the modifier flags into a character code: version word, the 256-byte table that select... |
| **`Resource_KCHR_0000_Header`** | — | `0x03824C` | `res_kchr.s:12` | KCHR 0 resource header. |
| **`Resource_KMAP_0000`** | — | `0x0387BE` | `res_kmap.s:8` | KMAP 0 -- the keyboard map Maps the raw key codes of the ADB keyboards to virtual key codes (the table that the ADB keyboard driver in os/adb_mgr.s uses before KeyTrans). New with the SE ROM. ROM offs... |
| **`Resource_KMAP_0000_Header`** | — | `0x0387BE` | `res_kmap.s:10` | KMAP 0 resource header. |
| **`Resource_MBDF_0000`** | — | `0x03884C` | `res_mbdf.s:130` | — |
| **`Resource_MBDF_0000_Header`** | — | `0x03884C` | `res_mbdf.s:135` | ROM resource header: a Memory Manager block header, as in front of the data of a handle. The relative handle locates the resource's master pointer in the ROM zone (INITRESOURCES_CONT_2): 0x54 + 4 * it... |
| **`Resource_MDEF_0000`** | — | `0x038DFA` | `res_mdef.s:79` | — |
| **`Resource_MDEF_0000_Header`** | — | `0x038DFA` | `res_mdef.s:84` | ROM resource header: a Memory Manager block header, as in front of the data of a handle. The relative handle locates the resource's master pointer in the ROM zone (INITRESOURCES_CONT_2): 0x54 + 4 * it... |
| **`Resource_PACK_0004`** | — | `0x01C180` | `res_pack_4.s:65` | PACK 4 -- FP68K, the SANE floating-point arithmetic package ROM offsets +0x1C180..+0x1D33F: the 8-byte header of the ROM resource at +0x1C180, then the package, $11B8 bytes from +0x1C188 (_PACK_4_ in ... |
| **`Resource_PACK_0004_Header`** | — | `0x01C180` | `res_pack_4.s:66` | PACK 4 -- FP68K, the SANE floating-point arithmetic package ROM offsets +0x1C180..+0x1D33F: the 8-byte header of the ROM resource at +0x1C180, then the package, $11B8 bytes from +0x1C188 (_PACK_4_ in ... |
| **`Resource_PACK_0005`** | — | `0x01B11A` | `res_pack_5.s:63` | PACK 5 -- Elems68K, the SANE elementary functions package ROM offsets +0x1B11A..+0x1C17F: the 8-byte header of the ROM resource at +0x1B11A, then the package, $105E bytes from +0x1B122 (_PACK_5_ in Ma... |
| **`Resource_PACK_0005_Header`** | — | `0x01B11A` | `res_pack_5.s:64` | PACK 5 -- Elems68K, the SANE elementary functions package ROM offsets +0x1B11A..+0x1C17F: the 8-byte header of the ROM resource at +0x1B11A, then the package, $105E bytes from +0x1B122 (_PACK_5_ in Ma... |
| **`Resource_PACK_0007`** | — | `0x01D340` | `res_pack_7.s:58` | **Regs:** `Entry: _Pack7 ($A9EE) with a selector word on the stack (above the`<br>PACK 7 -- the Binary-Decimal Conversion Package (Apple: Pkg7, BinDec.a) ROM offsets +0x1D340..+0x1D88D: the 8-byte header of the ROM resource at +0x1D340, then the package, $546 bytes from +0x1D348 (_... |
| **`Resource_PACK_0007_Header`** | — | `0x01D340` | `res_pack_7.s:59` | **Regs:** `Entry: _Pack7 ($A9EE) with a selector word on the stack (above the`<br>PACK 7 -- the Binary-Decimal Conversion Package (Apple: Pkg7, BinDec.a) ROM offsets +0x1D340..+0x1D88D: the 8-byte header of the ROM resource at +0x1D340, then the package, $546 bytes from +0x1D348 (_... |
| **`Resource_SERD_0000`** | — | `0x031BA6` | `res_serd.s:178` | shadow registers, in the order SERD_WRITEREGS uses them (SV_WR4 on): resource header: pseudo heap-block header of the ROM resource (as the Memory Manager's block header, so that a handle to the ROM re... |
| **`Resource_SERD_0000_Header`** | — | `0x031BA6` | `res_serd.s:179` | shadow registers, in the order SERD_WRITEREGS uses them (SV_WR4 on): resource header: pseudo heap-block header of the ROM resource (as the Memory Manager's block header, so that a handle to the ROM re... |
| **`Resource_tcsl_0000`** | — | `0x01D88E` | `res_tcsl.s:44` | Resource_tcsl_0000 (resource-code-or-driver) ROM offsets +0x1D88E..+0x1D91C. ROM resource type=tcsl id=0 name=- attr=0x58; header +0x1D88E, body +0x1D896 'tcsl' 0 -- the hidden slide show of the SE te... |
| **`Resource_tcsl_0000_Header`** | — | `0x01D88E` | `res_tcsl.s:49` | ROM resource header: a Memory Manager block header, as in front of the data of a handle. The relative handle locates the resource's master pointer in the ROM zone (INITRESOURCES_CONT_2): 0x54 + 4 * it... |
| **`Resource_WDEF_0000`** | — | `0x0395A4` | `res_wdef_0.s:67` | **Proto:** `FUNCTION MyWindow(varCode: INTEGER; theWindow: WindowPtr;`<br>Resource_WDEF_0000 (resource-code-or-driver) ROM offsets +0x395A4..+0x39C40. ROM resource type=WDEF id=0 name=- attr=0x58; header +0x395A4, body +0x395AC WDEF 0 -- the standard window definition funct... |
| **`Resource_WDEF_0000_Header`** | — | `0x0395A4` | `res_wdef_0.s:72` | ROM resource header: a Memory Manager block header, as in front of the data of a handle. The relative handle locates the resource's master pointer in the ROM zone (INITRESOURCES_CONT_2): 0x54 + 4 * it... |
| **`Resource_WDEF_0001`** | — | `0x03920A` | `res_wdef_1.s:77` | — |
| **`Resource_WDEF_0001_Header`** | — | `0x03920A` | `res_wdef_1.s:82` | ROM resource header: a Memory Manager block header, as in front of the data of a handle. The relative handle locates the resource's master pointer in the ROM zone (INITRESOURCES_CONT_2): 0x54 + 4 * it... |
| **`ROM_Resource_Area_Header`** | — | `0x01AF1C` | `res_map.s:34` | InitResources: number of ROM resources (one master pointer each) and the size of the map that follows |
| **`ROM_Resource_Map`** | — | `0x01AF20` | `res_map.s:38` | The resource map (Inside Macintosh I-128; the data offsets are relative to ROM offset 0) |
| **`RTMP_LISTENER`** | `0x01A908` | `0x0333A6` | `res_drvr_mpp.s:464`<br>`res_drvr_mpp.s:587` | RTMP_LISTENER: listener of socket 1 (RTMP).  From an RTMP data packet (DDP type 1) it takes the network number and the router's node ID (ID length 8): sysNetNum, sysABridge, BridgeTime = 255 (aged by ... |
| **`RTMP_LISTENER_EXIT`** | `0x01A926` | `0x0333C4` | `res_drvr_mpp.s:476`<br>`res_drvr_mpp.s:599` | — |
| **`SEEK_2`** | `0x01873A` | — | `res_drvr_sony.s:1391` | track unknown: recal first |
| **`SELF_COPY`** | — | `0x033590` | `res_drvr_mpp.s:883` | SELF_COPY: copy D3 bytes of the frame described by the WDS (A1 -> current entry, A0 = offset in it) to (A3)+, entry after entry -> D0 = D3 = bytes not copied (0, EQ: all).  Uses _BlockMove. Called by ... |
| **`SELF_COPY_EXIT`** | — | `0x0335BE` | `res_drvr_mpp.s:906` | — |
| **`SELF_COPY_MOVE`** | — | `0x0335A6` | `res_drvr_mpp.s:896` | — |
| **`SELF_COPY_PART`** | — | `0x0335A0` | `res_drvr_mpp.s:892` | — |
| **`SELF_READ_JT`** | — | `0x033574` | `res_drvr_mpp.s:853` | SELF_READ_JT: A4 for a protocol handler called by LAPWRITE_SELF - JSR (A4) = ReadPacket, JSR 2(A4) = ReadRest; they copy from the frame being sent (A1 = current WDS entry, A0 = offset in it) instead o... |
| **`SELF_READPACKET`** | — | `0x033586` | `res_drvr_mpp.s:869` | SELF_READPACKET: copy D3 bytes to (A3)+; D1 -= D3; lengthErr if the frame ended early |
| **`SELF_READPACKET_EXIT`** | — | `0x03358E` | `res_drvr_mpp.s:874` | — |
| **`SELF_READREST`** | — | `0x033576` | `res_drvr_mpp.s:857` | SELF_READREST: copy the rest (D1 bytes) into the D3-byte buffer at A3; D3 = 0 exact, > 0 bytes not filled, < 0 bytes that did not fit; noErr |
| **`SELF_READREST_END`** | — | `0x03357E` | `res_drvr_mpp.s:862` | — |
| **`SENDREQUEST`** | `0x01A120` | `0x0328E0` | `res_drvr_atp.s:570`<br>`res_drvr_atp.s:723` | SendRequest (csCode 255): open a private DDP socket (dynamic number), fill in a free request slot, send the TReq (addrBlock, reqLength/ reqPointer, userData, XO/STS from atpFlags, bitmap of numOfBuffs... |
| **`SENDREQUEST_BITLOOP`** | `0x01A170` | — | `res_drvr_atp.s:605` | currBitmap = one bit per expected response (bits 0..numOfBuffs-1) |
| **`SENDREQUEST_LOOP`** | `0x01A126` | `0x0328E6` | `res_drvr_atp.s:573`<br>`res_drvr_atp.s:726` | — |
| **`SENDREQUEST_OPENED`** | `0x01A15A` | `0x032910` | `res_drvr_atp.s:596`<br>`res_drvr_atp.s:741` | SENDREQUEST_OPENED socket opened: D1 = its number, D2 = free request slot |
| **`SENDREQUEST_SLOT`** | `0x01A176` | — | `res_drvr_atp.s:610` | fill in the request slot |
| **`SENDRESPONSE`** | `0x019FBE` | `0x03277E` | `res_drvr_atp.s:381`<br>`res_drvr_atp.s:537` | SendResponse (csCode 252): send numOfBuffs response packets from the BDS at bdsPointer (bdsSize entries) to addrBlock with transID; the EOM flag of atpFlags goes into the last packet.  Each sent BDS e... |
| **`SENDRESPONSE_ABORT`** | `0x01A04C` | `0x03280C` | `res_drvr_atp.s:443`<br>`res_drvr_atp.s:596` | SENDRESPONSE_ABORT - WriteDDP failed with ddpLenErr: release the CB; SENDRESPONSE_EXIT - IODone with D0 (also used by AddResponse) |
| **`SENDRESPONSE_CLRLOOP`** | `0x01A024` | `0x0327E4` | `res_drvr_atp.s:422`<br>`res_drvr_atp.s:579` | — |
| **`SENDRESPONSE_CTL`** | `0x019FEC` | `0x0327AC` | `res_drvr_atp.s:399`<br>`res_drvr_atp.s:555` | — |
| **`SENDRESPONSE_EXIT`** | `0x01A050` | `0x032810` | `res_drvr_atp.s:445`<br>`res_drvr_atp.s:599` | Called by: SENDRESPONSE, ADDRESPONSE (error exits) |
| **`SENDRESPONSE_LOOP`** | `0x019FDE` | `0x03279E` | `res_drvr_atp.s:393`<br>`res_drvr_atp.s:549` | build and send one response packet per BDS entry |
| **`SENDRESPONSE_RSPCB`** | `0x01A030` | `0x0327F0` | `res_drvr_atp.s:428`<br>`res_drvr_atp.s:585` | exactly-once? then hand the call to the RspCB of the transaction |
| **`SENDRESPONSE_SENT`** | `0x01A018` | `0x0327D8` | `res_drvr_atp.s:417`<br>`res_drvr_atp.s:574` | mark the BDS entries beyond numOfBuffs as not sent |
| **`SERD_0`** | — | `0x031BAE` | `res_serd.s:181` | — |
| **`SERD_ABORTREAD`** | `0x01BEB8` | `0x032422` | `res_serd.s:1433`<br>`res_serd.s:1527` | SERD_ABORTREAD -- complete the waiting read of the input DCE (A3) with the error in D0 (also breakRecd from SERD_EXTINT_BRKRECD). |
| **`SERD_BUFCOUNT`** | `0x01BD34` | `0x03229E` | `res_serd.s:1199`<br>`res_serd.s:1294` | SERD_BUFCOUNT -- D0 = number of characters in the input buffer (D1 - D2, plus the size D3 when the in index has wrapped). |
| **`SERD_BUFCOUNT_RTS`** | `0x01BD3C` | `0x0322A6` | `res_serd.s:1204`<br>`res_serd.s:1299` | — |
| **`SERD_CHANRESET`** | `0x01BBE4` | `0x03214C` | `res_serd.s:955`<br>`res_serd.s:1050` | SERD_CHANRESET -- csCode 27: reset the channel with WR9 = SV_WR9RESET (the caller must do a SerReset before using the port again). |
| **`SERD_CHECKPORT`** | `0x01B78E` | `0x031C74` | `res_serd.s:296`<br>`res_serd.s:326` | SERD_CHECKPORT_B -- port B entry of SERD_CHECKPORT_A. |
| **`SERD_CHECKPORT_A`** | `0x01B784` | `0x031C60` | `res_serd.s:286`<br>`res_serd.s:307` | SERD_CHECKPORT_A / SERD_CHECKPORT_B -- check that a port may be used by the serial driver and claim it. The port's nibble of SPConfig (PRAM: bits 4-7 port A, 0-3 port B) must be useFree (0) or useAsyn... |
| **`SERD_CHECKPORT_B`** | `0x01B78A` | `0x031C66` | `res_serd.s:293`<br>`res_serd.s:314` | SERD_CHECKPORT_B -- port B entry of SERD_CHECKPORT_A. |
| **`SERD_CHECKPORT_CLAIM`** | `0x01B7BA` | `0x031CA0` | `res_serd.s:324`<br>`res_serd.s:354` | SERD_CHECKPORT_CLAIM -- mark the port as in use by the serial driver. |
| **`SERD_CHECKPORT_ERR`** | `0x01B7A0` | `0x031C86` | `res_serd.s:304`<br>`res_serd.s:334` | — |
| **`SERD_CHECKPORT_HOOK`** | — | `0x031C6A` | `res_serd.s:319` | SERD_CHECKPORT_HOOK -- _AsyncPatch hook: call the trap's handler with SERD_CHECKPORT as return address (the ROM handler is an RTS). |
| **`SERD_CHECKPORT_OK`** | `0x01B7C4` | `0x031CAA` | `res_serd.s:328`<br>`res_serd.s:358` | — |
| **`SERD_CHECKPORT_USE`** | `0x01B7A4` | `0x031C8A` | `res_serd.s:312`<br>`res_serd.s:342` | SERD_CHECKPORT_USE -- the port's current use: PortAUse (high byte) and PortBUse (low byte) are read as one word and rotated so that this port's byte is the low byte. |
| **`SERD_CHECKRESUME`** | `0x01BCB0` | `0x03221A` | `res_serd.s:1104`<br>`res_serd.s:1199` | — |
| **`SERD_CHECKRESUME_RTS`** | `0x01BCBA` | `0x032224` | `res_serd.s:1109`<br>`res_serd.s:1204` | — |
| **`SERD_CLOSE_REGS`** | `0x01B960` | `0x031E80` | `res_serd.s:551`<br>`res_serd.s:612` | SERD_CLOSE_REGS -- register list that shuts the channel down (output Close): receiver, transmitter and channel interrupts off, only the DCD interrupt for the mouse stays enabled. WR5 = SV_WR5OFF, DTR ... |
| **`SERD_CLRDTR`** | `0x01BB52` | `0x032096` | `res_serd.s:864`<br>`res_serd.s:946` | SERD_CLRDTR -- csCode 18: negate DTR (also used by the receive code for DTR input flow control): WR5 = SV_WR5NODTR, dtrNegated set. SERD_SETDTR -- csCode 17: assert DTR: WR5 = SV_WR5ON, dtrNegated cle... |
| **`SERD_CLRXOFF`** | `0x01BCAC` | `0x032216` | `res_serd.s:1102`<br>`res_serd.s:1197` | SERD_CLRXOFF -- csCode 22, and XOn received: clear xOffHold. SERD_CHECKRESUME -- restart a pending write if output is no longer held (SerHShake, CTS change, XOn). |
| **`SERD_CONFIG_TBL`** | `0x01B8D4` | `0x031DDE` | `res_serd.s:465`<br>`res_serd.s:513` | SERD_CONFIG_TBL -- how SERD_SETCONFIG builds the shadow registers from the SerConfig word: per register a rotate count (ROL.W), an AND mask and an OR value. |
| **`SERD_CONTROL`** | `0x01BA56` | `0x031F9A` | `res_serd.s:697`<br>`res_serd.s:779` | E_BInOut_Control -- Control of port B (see E_AInOut_Control). |
| **`SERD_CONTROL_HOOK`** | — | `0x031F90` | `res_serd.s:772` | SERD_CONTROL_HOOK -- _AsyncPatch hook before SERD_CONTROL. |
| **`SERD_CONTROL_TABLE`** | `0x01BA7E` | `0x031FC2` | `res_serd.s:717`<br>`res_serd.s:799` | SERD_CONTROL_TABLE -- csCodes 8-27 through SERD_CTL_TBL. |
| **`SERD_CTL_BADCODE`** | `0x01BAB4` | `0x031FF8` | `res_serd.s:754`<br>`res_serd.s:836` | — |
| **`SERD_CTL_TBL`** | `0x01BAB8` | `0x031FFC` | `res_serd.s:760`<br>`res_serd.s:842` | SERD_CTL_TBL -- Control handlers for csCodes 8-27, word offsets from the table (called by SERD_CONTROL_TABLE). |
| **`SERD_CTL_UNIMP`** | `0x01BAB2` | `0x031FF6` | `res_serd.s:752`<br>`res_serd.s:834` | SERD_CTL_UNIMP -- csCode 15 (not supported): drop the return address of the handler call, controlErr. |
| **`SERD_CTLSTAT_EXIT`** | `0x01BAA0` | `0x031FE4` | `res_serd.s:734`<br>`res_serd.s:816` | — |
| **`SERD_CTLSTAT_NOERR`** | `0x01BA9E` | `0x031FE2` | `res_serd.s:732`<br>`res_serd.s:814` | SERD_CTLSTAT_NOERR / SERD_CTLSTAT_EXIT -- common end of Control and Status: restore SR and the DCE; an immediate call (noQueueBit in the saved ioTrap) returns directly, a queued one completes through ... |
| **`SERD_DATAMASK_TBL`** | `0x01B8D0` | `0x031D6C` | `res_serd.s:460`<br>`res_serd.s:455` | SERD_DATAMASK_TBL -- received-character mask, indexed by SerConfig bits 10-11 (the SCC's bits-per-character code). |
| **`SERD_DEFAULTBUF`** | `0x01BAF6` | `0x03203A` | `res_serd.s:803`<br>`res_serd.s:885` | SERD_DEFAULTBUF -- input buffer = the built-in 64 bytes at SV_DEFBUF (Open, SerSetBuf with length 0). SERD_SETBUF -- input buffer = A4, D1 bytes; both flow-control marks = length/4. Changes D1, A3, A4... |
| **`SERD_DONE_NOERR`** | `0x01BC46` | `0x0321B0` | `res_serd.s:1025`<br>`res_serd.s:1120` | SERD_DONE_NOERR -- complete the request of the DCE in A1 with noErr. |
| **`SERD_DTR_WRITE`** | `0x01BB68` | — | `res_serd.s:874` | — |
| **`SERD_EXTINT`** | `0x01BECC` | `0x032436` | `res_serd.s:1454`<br>`res_serd.s:1548` | — |
| **`SERD_EXTINT_A`** | `0x01BEC8` | `0x032432` | `res_serd.s:1452`<br>`res_serd.s:1546` | SERD_EXTINT_A -- channel A (see SERD_EXTINT_B). |
| **`SERD_EXTINT_B`** | `0x01BEC2` | `0x03242C` | `res_serd.s:1446`<br>`res_serd.s:1540` | SERD_EXTINT_B / SERD_EXTINT_A -- ext/status interrupt of the channel (ExtStsDT vComIntB / vComIntA, called by the ROM's ext/status dispatcher for changes other than DCD alone; D0 = RR0, D1 = changed e... |
| **`SERD_EXTINT_BREAK`** | `0x01BF24` | `0x03248E` | `res_serd.s:1492`<br>`res_serd.s:1586` | SERD_EXTINT_BREAK -- break/abort changed: at the start of a break (RR0 bit 7 set) abort a waiting read with breakRecd; at its end read and drop the null character the SCC receives. |
| **`SERD_EXTINT_BRKRECD`** | `0x01BF2E` | `0x032498` | `res_serd.s:1501`<br>`res_serd.s:1595` | SERD_EXTINT_BRKRECD -- break received: abort a waiting read with breakRecd (-90) (cumErrs breakErr is not set by this driver). |
| **`SERD_EXTINT_COUNT`** | `0x01BF0A` | `0x032474` | `res_serd.s:1478`<br>`res_serd.s:1572` | — |
| **`SERD_EXTINT_INC`** | `0x01BF1C` | `0x032486` | `res_serd.s:1484`<br>`res_serd.s:1578` | — |
| **`SERD_EXTINT_NOEVT`** | `0x01BEF0` | `0x03245A` | `res_serd.s:1468`<br>`res_serd.s:1562` | — |
| **`SERD_GETBUF`** | `0x01BD24` | `0x03228E` | `res_serd.s:1190`<br>`res_serd.s:1285` | SERD_GETBUF -- input buffer state: A3 = buffer, D3 = size, D1 = in index, D2 = out index. Called by: SERD_STATUS, SERD_READ, SERD_INFLOW, SERD_RXBUFFER |
| **`SERD_HSHAKE_COMMON`** | `0x01BB16` | `0x03205A` | `res_serd.s:830`<br>`res_serd.s:912` | — |
| **`SERD_HSHAKE_COPY`** | `0x01BB20` | `0x032064` | `res_serd.s:834`<br>`res_serd.s:916` | — |
| **`SERD_HSHAKE_DONE`** | `0x01BB4A` | `0x03208E` | `res_serd.s:849`<br>`res_serd.s:931` | — |
| **`SERD_HSHAKE_RESUME`** | `0x01BB38` | `0x03207C` | `res_serd.s:842`<br>`res_serd.s:924` | — |
| **`SERD_HSHAKEDTR`** | `0x01BB0C` | `0x032050` | `res_serd.s:822`<br>`res_serd.s:904` | SERD_HSHAKEDTR -- csCode 14: SerShk record with fDTR (csParam+7). SERD_SERHSHAKE -- csCode 10 SerHShake: SerShk record, fDTR unchanged. Both copy fXOn, fCTS, xOn, xOff, errs, evts, fInX; a cleared fIn... |
| **`SERD_INFLOW`** | `0x01BD00` | `0x03226A` | `res_serd.s:1162`<br>`res_serd.s:1257` | SERD_INFLOW -- with interrupts masked: if input flow control (fInX or fDTR) is on and at most SV_LOWMARK characters are left in the buffer, end it (SERD_RESUMEIN). SERD_INFLOW_MASKED: entry with SR pu... |
| **`SERD_INFLOW_EXIT`** | `0x01BD18` | `0x032282` | `res_serd.s:1173`<br>`res_serd.s:1268` | — |
| **`SERD_INFLOW_MASKED`** | `0x01BD06` | `0x032270` | `res_serd.s:1165`<br>`res_serd.s:1260` | — |
| **`SERD_INIT_REGS`** | `0x01B8EC` | `0x031DF6` | `res_serd.s:479`<br>`res_serd.s:527` | SERD_INIT_REGS -- register list that programs the channel (SERD_INITSCC). A pair whose second byte is $FF takes the value from the next shadow register (SV_WR4 on) and its first byte is the register n... |
| **`SERD_INITSCC`** | `0x01B920` | `0x031E2A` | `res_serd.s:515`<br>`res_serd.s:564` | SERD_INITSCC -- program the channel with SERD_INIT_REGS (18 pairs). SERD_WRITEREGS -- write the register list at A3, D1 bytes long, to this channel with interrupts masked; $FF pairs take the next shad... |
| **`SERD_INOPEN_DONE`** | `0x01B77A` | `0x031C56` | `res_serd.s:272`<br>`res_serd.s:293` | — |
| **`SERD_INSTALL_DRVRS`** | `0x01B6DC` | `0x031BBA` | `res_serd.s:175`<br>`res_serd.s:199` | SERD_INSTALL_DRVRS -- install the four serial drivers (called once by InitIOMgr through the resource's handle). For refNum -6 .. -9 it creates the DCE with _DrvrInstall (ResrvMem variant, DCE handle i... |
| **`SERD_INSTALL_LOOP`** | `0x01B6EE` | `0x031BCC` | `res_serd.s:181`<br>`res_serd.s:205` | — |
| **`SERD_IODONE`** | `0x01BAAC` | `0x031FF0` | `res_serd.s:745`<br>`res_serd.s:827` | SERD_IODONE -- complete the request of the DCE in A1 with result D0: jump through JIODone (IODone returns to our caller). Called by: SERD_CTLSTAT_EXIT, SERD_DONE_NOERR, SERD_READ, SERD_ABORTREAD |
| **`SERD_KILLIO_EXIT`** | `0x01BA78` | `0x031FBC` | `res_serd.s:710`<br>`res_serd.s:792` | — |
| **`SERD_OUTCLOSE`** | `0x01B992` | `0x031EBC` | `res_serd.s:585`<br>`res_serd.s:654` | SERD_OUTCLOSE -- common output Close: keep DTR if csCode 16 bit 7 asked for it, wait until all characters are sent, shut the channel down, restore the interrupt vectors, free SERDVars, clear the Seria... |
| **`SERD_OUTCLOSE_HOOK`** | — | `0x031EB2` | `res_serd.s:643` | SERD_OUTCLOSE_HOOK -- _AsyncPatch hook before SERD_OUTCLOSE. |
| **`SERD_OUTCLOSE_RESET`** | `0x01B9A4` | — | `res_serd.s:592` | — |
| **`SERD_OUTCLOSE_TXOFF`** | — | `0x031ED0` | `res_serd.s:660` | — |
| **`SERD_OUTHELD`** | `0x01BC64` | `0x0321CE` | `res_serd.s:1045`<br>`res_serd.s:1140` | SERD_OUTHELD -- is output held? D0 = 1 (Z = 0) if fXOn is set and XOff was received, or fCTS is set and the CTS bit says hold; else D0 = 0. |
| **`SERD_OUTHELD_CTS`** | `0x01BC70` | `0x0321DA` | `res_serd.s:1050`<br>`res_serd.s:1145` | — |
| **`SERD_OUTHELD_NO`** | `0x01BC80` | `0x0321EA` | `res_serd.s:1061`<br>`res_serd.s:1156` | SERD_OUTHELD_NO -- output may go. |
| **`SERD_OUTHELD_YES`** | `0x01BC7C` | `0x0321E6` | `res_serd.s:1055`<br>`res_serd.s:1150` | — |
| **`SERD_OUTOPEN`** | `0x01B81E` | `0x031D04` | `res_serd.s:375`<br>`res_serd.s:405` | SERD_OUTOPEN -- common output Open: allocate SERDVars (cleared) in the system heap; without memory, drop the 7 pushed longs and return the Memory Manager's error. |
| **`SERD_OUTOPEN_GOTVARS`** | `0x01B832` | `0x031D18` | `res_serd.s:389`<br>`res_serd.s:419` | SERD_OUTOPEN_GOTVARS -- install SERDVars and the interrupt handlers, save the replaced vectors in SV_OLDVECS (Close puts them back). |
| **`SERD_OUTOPEN_INITVARS`** | `0x01B866` | `0x031D4A` | `res_serd.s:410`<br>`res_serd.s:440` | — |
| **`SERD_POLLPROC`** | `0x01BD7E` | `0x0322E8` | `res_serd.s:1252`<br>`res_serd.s:1346` | SERD_POLLPROC -- modem port (channel A) poll procedure (PollProc): the .Sony driver's EmptyPD calls it after a disk access with the bytes that its polling (_PollSCC) pushed on the stack, one per word ... |
| **`SERD_POLLPROC_EXIT`** | `0x01BDAA` | `0x032314` | `res_serd.s:1277`<br>`res_serd.s:1371` | SERD_POLLPROC_EXIT -- discard the poll data (SP = PollStack) and return |
| **`SERD_POLLPROC_NEXT`** | `0x01BD8E` | `0x0322F8` | `res_serd.s:1264`<br>`res_serd.s:1358` | SERD_POLLPROC_NEXT -- pass the next poll data byte to the receive code |
| **`SERD_POLLPROC_POLL`** | `0x01BD86` | `0x0322F0` | `res_serd.s:1256`<br>`res_serd.s:1350` | poll the SCC while processing the poll data |
| **`SERD_QUEUEFLOW`** | `0x01BD62` | `0x0322CC` | `res_serd.s:1226`<br>`res_serd.s:1321` | SERD_QUEUEFLOW -- send the flow-control character D0; if the opposite one is still waiting to be sent, the two cancel and neither is sent. |
| **`SERD_QUEUEFLOW_CLR`** | `0x01BD68` | `0x0322D2` | `res_serd.s:1229`<br>`res_serd.s:1324` | — |
| **`SERD_QUEUEFLOW_RTS`** | `0x01BD6C` | `0x0322D6` | `res_serd.s:1231`<br>`res_serd.s:1326` | — |
| **`SERD_READ`** | `0x01BCC6` | `0x032230` | `res_serd.s:1126`<br>`res_serd.s:1221` | — |
| **`SERD_READ_LOOP`** | `0x01BCD0` | `0x03223A` | `res_serd.s:1131`<br>`res_serd.s:1226` | — |
| **`SERD_READ_PEND`** | `0x01BCFA` | `0x032264` | `res_serd.s:1153`<br>`res_serd.s:1248` | SERD_READ_PEND -- input buffer empty: the read waits (rdPend); return to the Device Manager after the flow-control check. |
| **`SERD_READ_STASH`** | `0x01BCE8` | `0x032252` | `res_serd.s:1141`<br>`res_serd.s:1236` | — |
| **`SERD_RESUMEIN`** | `0x01BD3E` | `0x0322A8` | `res_serd.s:1211`<br>`res_serd.s:1306` | SERD_RESUMEIN -- end input flow control: assert DTR again if fDTR is set and DTR was negated, send XOn if fInX is set and XOff was sent. SERD_SENDXONCOND -- csCode 23: send XOn if XOff was sent last. |
| **`SERD_RESUMEIN_RTS`** | `0x01BD22` | `0x03228C` | `res_serd.s:1183`<br>`res_serd.s:1278` | — |
| **`SERD_RESUMEIN_XON`** | `0x01BD50` | `0x0322BA` | `res_serd.s:1217`<br>`res_serd.s:1312` | — |
| **`SERD_RXBUFFER`** | `0x01BE08` | `0x032372` | `res_serd.s:1339`<br>`res_serd.s:1433` | SERD_RXBUFFER -- put the character into the input buffer; a full buffer drops it (cumErrs swOverrunErr). When less than SV_HIMARK bytes are free and input flow control is on, negate DTR (fDTR) and/or ... |
| **`SERD_RXBUFFER_CHK`** | `0x01BE18` | `0x032382` | `res_serd.s:1346`<br>`res_serd.s:1440` | — |
| **`SERD_RXBUFFER_STORED`** | `0x01BE24` | `0x03238E` | `res_serd.s:1354`<br>`res_serd.s:1448` | SERD_RXBUFFER_STORED -- the character is in; check input flow control. |
| **`SERD_RXCHAR`** | `0x01BDC2` | `0x03232C` | `res_serd.s:1299`<br>`res_serd.s:1393` | — |
| **`SERD_RXCHAR_FLOW`** | `0x01BDD8` | `0x032342` | `res_serd.s:1308`<br>`res_serd.s:1402` | — |
| **`SERD_RXINT`** | `0x01BDBE` | `0x032328` | `res_serd.s:1297`<br>`res_serd.s:1391` | — |
| **`SERD_RXINT_A`** | `0x01BDBA` | `0x032324` | `res_serd.s:1295`<br>`res_serd.s:1389` | SERD_RXINT_A -- channel A (see SERD_RXINT_B). |
| **`SERD_RXINT_B`** | `0x01BDB4` | `0x03231E` | `res_serd.s:1289`<br>`res_serd.s:1383` | SERD_RXINT_B / SERD_RXINT_A -- receive character available interrupt (Lvl2DT vRxB / vRxA; A0 = channel control, read). SERD_RXCHAR (also from SERD_POLLPROC) takes the character in D0 with A3 -> the po... |
| **`SERD_RXINT_RTS`** | `0x01BE62` | `0x0323CC` | `res_serd.s:1379`<br>`res_serd.s:1473` | SERD_RXINT_RTS -- end of the receive code. Called by: SERD_RXCHAR_FLOW, SERD_RXSTORE, SERD_RXBUFFER_CHK, SERD_RXBUFFER_STORED, SERD_SENDXOFFCOND, SERD_SPINT_ABORT (8 branches) |
| **`SERD_RXSTORE`** | `0x01BDF2` | `0x03235C` | `res_serd.s:1321`<br>`res_serd.s:1415` | SERD_RXSTORE -- give the character D0 to a waiting read (Stash; a full read completes with noErr) or put it into the input buffer. |
| **`SERD_SCCADDR`** | `0x01B910` | `0x031E1A` | `res_serd.s:503`<br>`res_serd.s:551` | SERD_SCCADDR -- A0 = this channel's SCC control register for reading, A1 = for writing (SCCRd/SCCWr + SV_CHANOFS). Called by SERD_WRITEREGS and SERD_WAITSENT. |
| **`SERD_SENDFLOW`** | `0x01BD6E` | `0x0322D8` | `res_serd.s:1237`<br>`res_serd.s:1332` | SERD_SENDFLOW -- send the flow-control character D0 now if the transmit buffer is empty, else leave it in SV_FLOWCHAR for SERD_XMIT. Changes A3. |
| **`SERD_SENDXOFF`** | `0x01BBD4` | `0x03213C` | `res_serd.s:946`<br>`res_serd.s:1041` | SERD_SENDXOFF -- csCode 26: send XOff unconditionally; automatic input flow control (fInX) is off until csCode 24 (it would send XOn). |
| **`SERD_SENDXOFFCOND`** | `0x01BE52` | `0x0323BC` | `res_serd.s:1371`<br>`res_serd.s:1465` | SERD_SENDXOFFCOND -- csCode 25, and input buffer nearly full: send XOff if XOn was sent last. |
| **`SERD_SENDXON`** | `0x01BBC0` | `0x032128` | `res_serd.s:936`<br>`res_serd.s:1031` | SERD_SENDXON -- csCode 24: send XOn unconditionally and switch automatic input flow control back to the SerHShake setting (csCode 26 clears it). |
| **`SERD_SENDXONCOND`** | `0x01BD56` | `0x0322C0` | `res_serd.s:1220`<br>`res_serd.s:1315` | — |
| **`SERD_SENDXONOFF`** | `0x01BBD0` | `0x032138` | `res_serd.s:940`<br>`res_serd.s:1035` | — |
| **`SERD_SERCLRBRK`** | — | `0x0320B0` | `res_serd.s:958` | SERD_SERCLRBRK -- csCode 11 SerClrBrk, and the end of SERD_CLRDTR / SERD_SETDTR: write the current WR5 (SV_WR5: no break, DTR as it is). |
| **`SERD_SERHSHAKE`** | `0x01BB12` | `0x032056` | `res_serd.s:828`<br>`res_serd.s:910` | SERD_SERHSHAKE -- csCode 10 (see SERD_HSHAKEDTR). |
| **`SERD_SERRESET`** | `0x01BAE0` | `0x032024` | `res_serd.s:785`<br>`res_serd.s:867` | SERD_SERRESET -- csCode 8 SerReset: csParam = SerConfig. A new value is set up through SERD_SETCONFIG (shadow registers, SCC programmed). |
| **`SERD_SERSETBRK`** | `0x01BB6E` | `0x0320B6` | `res_serd.s:882`<br>`res_serd.s:965` | SERD_SERSETBRK -- csCode 12 SerSetBrk: wait (with the caller's interrupt level) until all characters are sent, then write WR5 = D0 (SV_WR5ON from the dispatcher, so DTR is asserted too) with send-brea... |
| **`SERD_SERSETBUF`** | `0x01BAEC` | `0x032030` | `res_serd.s:794`<br>`res_serd.s:876` | SERD_SERSETBUF -- csCode 9 SerSetBuf: csParam = buffer pointer (long), csParam+4 = its length (0: the built-in buffer). Empties the buffer. |
| **`SERD_SETBAUD`** | `0x01BB8C` | `0x0320D6` | `res_serd.s:907`<br>`res_serd.s:989` | SERD_SETBAUD -- csCode 13: csParam = baud rate. Time constant TC = round(114709 / rate) - 2 (114709 = 3.6707 MHz SCC clock / 32, HardwareEqu.a macConst; x16 clock), into SV_WR12/SV_WR13; the rate actu... |
| **`SERD_SETBAUD_INRANGE`** | — | `0x032100` | `res_serd.s:1007` | — |
| **`SERD_SETBAUD_RTS`** | — | `0x032120` | `res_serd.s:1018` | — |
| **`SERD_SETBAUD_SHADOW`** | — | `0x032112` | `res_serd.s:1013` | — |
| **`SERD_SETBUF`** | `0x01BAFC` | `0x032040` | `res_serd.s:806`<br>`res_serd.s:888` | — |
| **`SERD_SETBUF_RTS`** | `0x01BB0A` | `0x03204E` | `res_serd.s:813`<br>`res_serd.s:895` | — |
| **`SERD_SETCONFIG`** | `0x01B87C` | `0x031D7A` | `res_serd.s:424`<br>`res_serd.s:473` | SERD_SETCONFIG -- set the channel up from the SerConfig word in D4 (Open, csCode 8 SerReset): data mask, shadow registers from SERD_CONFIG_TBL, SV_CONFIG, the WR5 values with and without DTR, then pro... |
| **`SERD_SETCONFIG_HOOK`** | — | `0x031D70` | `res_serd.s:461` | SERD_SETCONFIG_HOOK -- _AsyncPatch hook before SERD_SETCONFIG (Open, csCode 8 SerReset). |
| **`SERD_SETCONFIG_LOOP`** | `0x01B8A0` | `0x031D9E` | `res_serd.s:437`<br>`res_serd.s:486` | — |
| **`SERD_SETCONFIG_VALID`** | `0x01B888` | `0x031D86` | `res_serd.s:429`<br>`res_serd.s:478` | — |
| **`SERD_SETDTR`** | `0x01BB5E` | `0x0320A4` | `res_serd.s:871`<br>`res_serd.s:953` | SERD_SETDTR -- csCode 17 (see SERD_CLRDTR). |
| **`SERD_SETMISC`** | `0x01BB4C` | `0x032090` | `res_serd.s:855`<br>`res_serd.s:937` | SERD_SETMISC -- csCode 16: csParam byte = options; only bit 7 (leave DTR alone at Close) is used. |
| **`SERD_SETPECHAR`** | `0x01BBF2` | `0x03215C` | `res_serd.s:971`<br>`res_serd.s:1066` | SERD_SETPECHAR -- csCode 19: csParam = replacement character; a good character equal to it arrives with bit 7 cleared. |
| **`SERD_SETPECHARALT`** | `0x01BBEC` | `0x032156` | `res_serd.s:964`<br>`res_serd.s:1059` | SERD_SETPECHARALT -- csCode 20: csParam = replacement character, csParam+1 = alternate character (for a good character equal to the replacement). |
| **`SERD_SETXOFF`** | `0x01BBBA` | `0x032122` | `res_serd.s:929`<br>`res_serd.s:1024` | SERD_SETXOFF -- csCode 21: set xOffHold, as if XOff had been received (output stops if fXOn is set). |
| **`SERD_SPINT`** | `0x01BE6E` | `0x0323D8` | `res_serd.s:1397`<br>`res_serd.s:1491` | — |
| **`SERD_SPINT_A`** | `0x01BE6A` | `0x0323D4` | `res_serd.s:1395`<br>`res_serd.s:1489` | SERD_SPINT_A -- channel A (see SERD_SPINT_B). |
| **`SERD_SPINT_ABORT`** | `0x01BEB0` | `0x03241A` | `res_serd.s:1427`<br>`res_serd.s:1521` | SERD_SPINT_ABORT -- abort a waiting read with rcvrErr; drop the character. |
| **`SERD_SPINT_B`** | `0x01BE64` | `0x0323CE` | `res_serd.s:1389`<br>`res_serd.s:1483` | SERD_SPINT_B / SERD_SPINT_A -- special receive condition interrupt (Lvl2DT vSCB / vSCA; A0/A1 = channel control): parity error, receive overrun or framing error (RR1 bits 4-6). The errors are added to... |
| **`SERD_SPINT_PARITY`** | `0x01BEA4` | `0x03240E` | `res_serd.s:1417`<br>`res_serd.s:1511` | — |
| **`SERD_SPINT_STORE`** | `0x01BEAC` | `0x032416` | `res_serd.s:1421`<br>`res_serd.s:1515` | — |
| **`SERD_STASH`** | `0x01BD1E` | `0x032288` | `res_serd.s:1181`<br>`res_serd.s:1276` | SERD_STASH -- jump through JStash: Stash stores D0 into the buffer of the request of the DCE in A1 and returns D0 < 0 (N set) when it is full. |
| **`SERD_STATUS`** | `0x01BA10` | `0x031F48` | `res_serd.s:654`<br>`res_serd.s:729` | E_BInOut_Status -- Status of port B (see E_AInOut_Status). |
| **`SERD_STATUS_CS8`** | `0x01BA3A` | `0x031F74` | `res_serd.s:675`<br>`res_serd.s:748` | SERD_STATUS_CS8 -- csCode 8 SerStatus: copy the SerStaRec (cumErrs, xOffSent, rdPend, wrPend, ctsHold, xOffHold) and clear cumErrs. |
| **`SERD_STATUS_HOOK`** | — | `0x031F3E` | `res_serd.s:722` | SERD_STATUS_HOOK -- _AsyncPatch hook before SERD_STATUS. |
| **`SERD_TXINT`** | `0x01BC8E` | `0x0321F8` | `res_serd.s:1078`<br>`res_serd.s:1173` | — |
| **`SERD_TXINT_A`** | `0x01BC8A` | `0x0321F4` | `res_serd.s:1076`<br>`res_serd.s:1171` | SERD_TXINT_A -- channel A (see SERD_TXINT_B). |
| **`SERD_TXINT_B`** | `0x01BC84` | `0x0321EE` | `res_serd.s:1070`<br>`res_serd.s:1165` | SERD_TXINT_B / SERD_TXINT_A -- transmit buffer empty interrupt (Lvl2DT vTxB / vTxA; A1 = channel control, write). SERD_TXINT sends a waiting XOn/XOff character or the next byte of the write; with noth... |
| **`SERD_TXINT_IDLE`** | `0x01BCA6` | `0x032210` | `res_serd.s:1094`<br>`res_serd.s:1189` | SERD_TXINT_IDLE -- nothing to send: reset the Tx interrupt. |
| **`SERD_TXREADY`** | `0x01BC4C` | `0x0321B6` | `res_serd.s:1033`<br>`res_serd.s:1128` | SERD_TXREADY -- A3 = this channel's control register for writing; Z = 0 if the transmit buffer is empty (RR0 bit 2, txBE). The first read resets the SCC's register pointer to RR0. Changes A3. |
| **`SERD_TXRESUME`** | `0x01BC9E` | `0x032208` | `res_serd.s:1087`<br>`res_serd.s:1182` | SERD_TXRESUME -- continue the write in SERD_XMIT (A1 = output DCE for Fetch and IODone; SR pushed for SERD_XMIT's exit). |
| **`SERD_WAITSENT`** | `0x01B9DC` | `0x031F0E` | `res_serd.s:623`<br>`res_serd.s:692` | SERD_WAITSENT -- wait until the transmitter has sent everything: poll RR1 bit 0 (All Sent) with interrupts masked for each read, at most 65536 times. Called by SERD_OUTCLOSE and SERD_SERSETBRK (break ... |
| **`SERD_WAITSENT_LOOP`** | `0x01B9E6` | `0x031F18` | `res_serd.s:627`<br>`res_serd.s:696` | — |
| **`SERD_WRITE`** | `0x01BC0C` | `0x032176` | `res_serd.s:991`<br>`res_serd.s:1086` | — |
| **`SERD_WRITEREG`** | `0x01BB80` | `0x0320CC` | `res_serd.s:892`<br>`res_serd.s:975` | — |
| **`SERD_WRITEREGS`** | `0x01B926` | `0x031E3A` | `res_serd.s:518`<br>`res_serd.s:574` | SERD_WRITEREGS -- see SERD_INITSCC. |
| **`SERD_WRITEREGS_A`** | — | `0x031E72` | `res_serd.s:599` | — |
| **`SERD_WRITEREGS_CTS`** | — | `0x031E76` | `res_serd.s:601` | — |
| **`SERD_WRITEREGS_HOOK`** | — | `0x031E30` | `res_serd.s:567` | — |
| **`SERD_WRITEREGS_LOOP`** | `0x01B938` | `0x031E4C` | `res_serd.s:525`<br>`res_serd.s:581` | — |
| **`SERD_WRITEREGS_PAIR`** | `0x01B942` | `0x031E56` | `res_serd.s:531`<br>`res_serd.s:587` | — |
| **`SERD_WRITEWR5`** | `0x01BB7E` | `0x0320CA` | `res_serd.s:890`<br>`res_serd.s:973` | SERD_WRITEWR5 -- write D0 to WR5; also csCode 11 SerClrBrk, entered with D0 = SV_WR5ON (no break: note that this asserts DTR even after csCode 18). SERD_WRITEREG -- write D0 to SCC register D1 of this... |
| **`SERD_XMIT`** | `0x01BC1A` | `0x032184` | `res_serd.s:1001`<br>`res_serd.s:1096` | SERD_XMIT -- send the next character if the transmit buffer is empty: a waiting XOn/XOff character first, else the next byte of the write (JFetch, A1 = output DCE). The last byte (bit 15 of D0 set by ... |
| **`SERD_XMIT_CHAR`** | `0x01BC32` | `0x03219C` | `res_serd.s:1010`<br>`res_serd.s:1105` | — |
| **`SERD_XMIT_EXIT`** | `0x01BC3A` | `0x0321A4` | `res_serd.s:1014`<br>`res_serd.s:1109` | — |
| **`SERD_XMIT_LAST`** | `0x01BC40` | `0x0321AA` | `res_serd.s:1021`<br>`res_serd.s:1116` | SERD_XMIT_LAST -- the last byte is in the transmitter: the write is done. |
| **`SETSELFSEND`** | — | `0x033FAC` | `res_drvr_mpp.s:2212` | SetSelfSend (csCode 256, IM V-516): oldSelfFlag = SelfSend, SelfSend = newSelfFlag; noErr |
| **`SND_4TONE_DONE`** | `0x017B70` | `0x036E42` | `res_drvr_sound.s:443`<br>`res_drvr_sound.s:405` | End of the four-tone sound (duration 0): restore the registers, stop. |
| **`SND_4TONE_ENTRY`** | `0x017B64` | `0x036E36` | `res_drvr_sound.s:435`<br>`res_drvr_sound.s:397` | SND_4TONE_ENTRY -- Prime, ftMode: A1 -> the sndRec field. SoundPtr := the FTSoundRec; the four-tone task runs from the next tick on. |
| **`SND_4TONE_MIX_START`** | `0x017BA4` | `0x036E76` | `res_drvr_sound.s:479`<br>`res_drvr_sound.s:440` | — |
| **`SND_CHECK_ACTIVE_IO`** | `0x017CF4` | — | `res_drvr_sound.s:662` | SND_CHECK_ACTIVE_IO -- look at the free-form request at the head of the queue: none -> EQ; source used up (ioActCount >= ioReqCount) -> complete it (SND_REMOVE_AND_IODONE: remove the task, fill the bu... |
| **`SND_CLAIM_T1`** | `0x017ACE` | `0x036DA0` | `res_drvr_sound.s:334`<br>`res_drvr_sound.s:308` | — |
| **`SND_CTL_VOLUME`** | `0x017A92` | `0x036D64` | `res_drvr_sound.s:303`<br>`res_drvr_sound.s:278` | csCode 2: speaker volume := csParam (0..7). |
| **`SND_FF_CHECK_RTS`** | `0x017D10` | — | `res_drvr_sound.s:673` | — |
| **`SND_FF_INACTIVE`** | `0x017D0E` | — | `res_drvr_sound.s:671` | — |
| **`SND_FILL_BUF`** | `0x017A2A` | `0x036CFC` | `res_drvr_sound.s:245`<br>`res_drvr_sound.s:221` | — |
| **`SND_FILL_FROM_LOWMEM`** | — | `0x036CF8` | `res_drvr_sound.s:219` | SND_FILL_FROM_LOWMEM -- fill the sound buffer with SoundLevel, the last level a synthesizer wrote, so that the end of a sound does not click. SE: replaces the Plus driver's SND_SILENCE_BUF, which took... |
| **`SND_FILL_LOOP`** | `0x017A40` | `0x036D12` | `res_drvr_sound.s:255`<br>`res_drvr_sound.s:231` | — |
| **`SND_FILL_SILENCE`** | `0x017CD8` | `0x036FD8` | `res_drvr_sound.s:638`<br>`res_drvr_sound.s:612` | The source ended before the end of the frame: fill the rest of the buffer with level 0, wrapping at its end. DBF writes D2 + 1 samples, one more than needed (suspected bug, also in the 64K and SE driv... |
| **`SND_FREEFORM_CHECK_DONE`** | — | `0x036F74` | `res_drvr_sound.s:566` | — |
| **`SND_FREEFORM_DONE`** | `0x017CEA` | `0x036FEA` | `res_drvr_sound.s:649`<br>`res_drvr_sound.s:623` | The frame is complete: save the position, then check the request. |
| **`SND_FREEFORM_ENTRY`** | `0x017C72` | `0x036F50` | `res_drvr_sound.s:573`<br>`res_drvr_sound.s:535` | SND_FREEFORM_ENTRY -- Prime, ffMode: source position := 0 (dCtlPosition holds its fraction); the free-form task runs from the next tick on. |
| **`SND_FREEFORM_NEXT_BUF`** | `0x017D12` | `0x03700A` | `res_drvr_sound.s:676`<br>`res_drvr_sound.s:635` | End of the first part (words 32..369). |
| **`SND_FREEFORM_OK_EXIT`** | — | `0x037008` | `res_drvr_sound.s:632` | — |
| **`SND_FREEFORM_RESAMPLE_INIT`** | — | `0x036F86` | `res_drvr_sound.s:573` | — |
| **`SND_FREEFORM_WRAP`** | `0x017D1C` | `0x037014` | `res_drvr_sound.s:682`<br>`res_drvr_sound.s:641` | Second part: words 0..31. |
| **`SND_INSTALL_VBL_IMM`** | `0x017B6C` | `0x036E3E` | `res_drvr_sound.s:438`<br>`res_drvr_sound.s:400` | — |
| **`SND_IODONE_NOERR`** | `0x017B58` | `0x036E2A` | `res_drvr_sound.s:425`<br>`res_drvr_sound.s:387` | SND_IODONE_NOERR -- complete the current request with noErr: jIODone (which also starts the next queued request, calling Prime). Reached from E_Sound_Status, SND_REMOVE_AND_IODONE. |
| **`SND_MIX_SAMPLE`** | `0x017BB0` | `0x036E82` | `res_drvr_sound.s:483`<br>`res_drvr_sound.s:444` | — |
| **`SND_OPEN_OK`** | `0x0179EC` | `0x036CBC` | `res_drvr_sound.s:173`<br>`res_drvr_sound.s:154` | — |
| **`SND_PRIME_DONE`** | `0x017B02` | `0x036DD4` | `res_drvr_sound.s:352`<br>`res_drvr_sound.s:326` | — |
| **`SND_RELEASE_T1_ONLY`** | `0x0179FC` | `0x036CD0` | `res_drvr_sound.s:204`<br>`res_drvr_sound.s:184` | SND_RELEASE_T1_ONLY -- release VIA Timer 1 if the Sound Driver owns it (T1Arbitrate = 0): stop the PB7 square-wave output and mark the timer free ($FF). Called by: SND_SQWAVE_FINISH (and SND_SILENCE_A... |
| **`SND_REMOVE_AND_IODONE`** | `0x017B50` | `0x036E22` | `res_drvr_sound.s:419`<br>`res_drvr_sound.s:381` | SND_REMOVE_AND_IODONE -- end of a sound: remove the VBL task, let the buffer hold the level of its first byte (SE: SoundLevel), complete the request. Called by: SND_CHECK_ACTIVE_IO; reached from SND_S... |
| **`SND_REMOVE_VBL`** | `0x017A12` | `0x036CE6` | `res_drvr_sound.s:217`<br>`res_drvr_sound.s:198` | SND_REMOVE_VBL -- remove the sound VBL task if it is installed. Called by: E_Sound_Close, SND_REMOVE_AND_IODONE.  Uses A0, D0 (_VRemove). |
| **`SND_REMOVE_VBL_NOT_ACTIVE`** | `0x017A22` | `0x036CF6` | `res_drvr_sound.s:223`<br>`res_drvr_sound.s:204` | — |
| **`SND_RESAMPLE_INNER`** | `0x017CB6` | `0x036FB6` | `res_drvr_sound.s:616`<br>`res_drvr_sound.s:590` | — |
| **`SND_RESAMPLE_OUTER`** | `0x017CB4` | `0x036FB4` | `res_drvr_sound.s:614`<br>`res_drvr_sound.s:588` | — |
| **`SND_SAVE_VOICES`** | `0x017C60` | `0x036F3E` | `res_drvr_sound.s:559`<br>`res_drvr_sound.s:522` | — |
| **`SND_SET_VOLUME`** | `0x017A56` | `0x036D28` | `res_drvr_sound.s:271`<br>`res_drvr_sound.s:246` | SND_SET_VOLUME -- set the speaker volume: D0 = 0..7 (0 = silent, 7 = loudest, IM II-232) into SdVolume and into the sound-volume bits 0-2 of VIA port A (vBufA), with interrupts masked to level 3 becau... |
| **`SND_SILENCE_AND_RELEASE`** | `0x0179FA` | `0x036CCA` | `res_drvr_sound.s:198`<br>`res_drvr_sound.s:178` | SND_SILENCE_AND_RELEASE -- let the sound buffer hold the level of its first byte (SND_SILENCE_BUF), then release VIA Timer 1 (SND_RELEASE_T1_ONLY). The 64K driver filled the buffer with $FF here, the ... |
| **`SND_SILENCE_BUF`** | `0x017A24` | — | `res_drvr_sound.s:242` | SND_SILENCE_BUF -- let the sound buffer hold one level, that of its first byte (sample word 0), so that the sound stops without a jump. Word 0 is not the last sample a synthesizer wrote, though (four-... |
| **`SND_SILENCE_LOOP`** | `0x017CDA` | `0x036FDA` | `res_drvr_sound.s:640`<br>`res_drvr_sound.s:614` | — |
| **`SND_SILENCE_LOOP_INNER`** | `0x017CE6` | `0x036FE6` | `res_drvr_sound.s:646`<br>`res_drvr_sound.s:620` | — |
| **`SND_SOLO_LOOP`** | `0x017C32` | `0x036F0A` | `res_drvr_sound.s:541`<br>`res_drvr_sound.s:503` | — |
| **`SND_SOLO_VOICE1`** | `0x017C02` | `0x036EDA` | `res_drvr_sound.s:522`<br>`res_drvr_sound.s:484` | SND_SOLO_VOICE1 -- the rates of tones 2-4 are 0: their samples are constant, so add them up once and mix only tone 1 (faster); starts at word 70: 300 samples to the end of the buffer, then words 0..69... |
| **`SND_SQWAVE_FINISH`** | `0x017B48` | `0x036E1A` | `res_drvr_sound.s:411`<br>`res_drvr_sound.s:376` | End of the square wave (zero duration or end of the buffer). |
| **`SND_SQWAVE_NEXT`** | `0x017AB0` | `0x036D82` | `res_drvr_sound.s:324`<br>`res_drvr_sound.s:298` | swMode: A1 -> the next tone triplet. |
| **`SND_T1_READY`** | `0x017AEA` | `0x036DBC` | `res_drvr_sound.s:343`<br>`res_drvr_sound.s:317` | — |
| **`SND_T1_RELEASED`** | `0x017A10` | `0x036CE4` | `res_drvr_sound.s:210`<br>`res_drvr_sound.s:190` | — |
| **`SND_VBL_IMMEDIATE`** | `0x017B06` | `0x036DD8` | `res_drvr_sound.s:369`<br>`res_drvr_sound.s:340` | SND_VBL_IMMEDIATE -- set up SoundVBL to run the routine A1 next tick. SND_VBL_INSTALL -- set up SoundVBL to run the routine A1 after D0 ticks, and install it unless it is installed already (SoundActiv... |
| **`SND_VBL_INSTALL`** | `0x017B08` | `0x036DDA` | `res_drvr_sound.s:371`<br>`res_drvr_sound.s:342` | — |
| **`SND_VBL_INSTALLED`** | `0x017B28` | `0x036DFA` | `res_drvr_sound.s:384`<br>`res_drvr_sound.s:355` | — |
| **`SND_VBL_RTS`** | `0x017C70` | — | `res_drvr_sound.s:565` | — |
| **`Sony_AdrAndSense`** | `0x0185FE` | `0x034FC4` | `res_drvr_sony.s:1201`<br>`res_drvr_sony_fdhd.s:1636` | AdrAndSense / Sense -- read the sense line of a drive register D0 (in)  -- register address (AdrAndSense only) D0 (out) -- IWM status register: bit 7 = SENSE input (BMI = 1), bit 5 The status register... |
| **`Sony_AdrAndStrb`** | `0x018618` | `0x034FDE` | `res_drvr_sony.s:1217`<br>`res_drvr_sony_fdhd.s:1658` | AdrAndStrb / Pulse -- pulse LSTRB (phase line PH3) to perform a drive control function: the drive takes CA2 as the value for the control register addressed by CA1, CA0 and SEL D0 (in) -- control regis... |
| **`Sony_AdrDisk`** | `0x0185C4` | `0x034F8A` | `res_drvr_sony.s:1166`<br>`res_drvr_sony_fdhd.s:1599` | AdrDisk -- address one of the 16 drive registers D0 (in) -- register address, bits 0-3 = CA2, SEL, CA0, CA1 (Apple's order CA1-CA0-SEL-CA2, bit 3 to bit 0) CA0-CA2 are the IWM phase lines PH0-PH2, SEL... |
| **`SONY_ADRDISK_CONT`** | `0x0185D8` | `0x034F9E` | `res_drvr_sony.s:1175`<br>`res_drvr_sony_fdhd.s:1609` | — |
| **`SONY_ADRDISK_CONT_2`** | `0x0185DC` | `0x034FA2` | `res_drvr_sony.s:1177`<br>`res_drvr_sony_fdhd.s:1611` | — |
| **`SONY_ADRDISK_CONT_3`** | `0x0185E8` | `0x034FAE` | `res_drvr_sony.s:1183`<br>`res_drvr_sony_fdhd.s:1616` | — |
| **`SONY_ADRDISK_CONT_4`** | `0x0185F4` | `0x034FBA` | `res_drvr_sony.s:1189`<br>`res_drvr_sony_fdhd.s:1622` | — |
| **`SONY_ADRDISK_CONT_5`** | `0x0185FC` | `0x034FC2` | `res_drvr_sony.s:1193`<br>`res_drvr_sony_fdhd.s:1626` | — |
| **`SONY_ADRDISK_SKIP`** | `0x0185EE` | `0x034FB4` | `res_drvr_sony.s:1185`<br>`res_drvr_sony_fdhd.s:1618` | — |
| **`SONY_ADRDTAERR`** | — | `0x034ED8` | `res_drvr_sony_fdhd.s:1494` | AdrDtaErr -- address or data mark error |
| **`SONY_ADRMKTBL`** | `0x0190CA` | `0x035FAE` | `res_drvr_sony.s:2747`<br>`res_drvr_sony.s:3380` | AdrMkTbl (SyncTbl) -- template of the 27 bytes in front of each sector's data, copied 12 times into the format buffer; FillInMarks puts in the track, sector, side, format and checksum nibbles (offsets... |
| **`Sony_CacheValid`** | `0x0182BC` | `0x034C5A` | `res_drvr_sony.s:812`<br>`res_drvr_sony_fdhd.s:1199` | CacheValid -- does the cache hold this drive and side/track? D0 (out), CCR -- 0 (BEQ) if valid, -1 (BNE) if not |
| **`SONY_CACHEVALID_EXIT`** | `0x0182DA` | `0x034C78` | `res_drvr_sony.s:824`<br>`res_drvr_sony_fdhd.s:1211` | — |
| **`SONY_CACHEVALID_NO`** | `0x0182D8` | `0x034C76` | `res_drvr_sony.s:822`<br>`res_drvr_sony_fdhd.s:1209` | — |
| **`Sony_CallWakeUp`** | — | — | `res_drvr_sony_fdhd.s:1936` | CallWakeUp -- WakeUp entry used throughout this driver: go through the JWakeUp vector only if the routine it points to starts with a NOP ($4E71), else call jtWakeUp directly. Apple (Sony driver histor... |
| **`Sony_Check4Disk`** | `0x018B88` | `0x03558A` | `res_drvr_sony.s:2032`<br>`res_drvr_sony_fdhd.s:2567` | Check4Disk -- check drive D3: after an eject count DiskInPlace up to 0; with no disk, look for one and post a disk-inserted event (message = drive number; Inside Macintosh II-212). DiskInPlace 1 or 2:... |
| **`Sony_Check4SWIM`** | — | — | `res_drvr_sony_fdhd.s:2898` | SWIM / SuperDrive MFM support (Apple's SonyMFM.a by Steve Christensen, change C437, 1986-88): register set selection, parameter RAM set-up, disk type detection, drive addressing through the ISM regist... |
| **`SONY_CHECK4SWIM_IWM`** | — | — | `res_drvr_sony_fdhd.s:2926` | — |
| **`SONY_CHECKNEW`** | `0x0187A0` | `0x035166` | `res_drvr_sony.s:1450`<br>`res_drvr_sony_fdhd.s:1890` | CheckNew -- for a new-interface drive return; for an old drive return to the caller's caller after waiting D0 * 100 us (WakeUp) |
| **`SONY_CHECKNEW_EXIT`** | `0x0187B0` | `0x035176` | `res_drvr_sony.s:1463`<br>`res_drvr_sony_fdhd.s:1899` | no wait |
| **`SONY_CHECKNEW_WAIT`** | `0x0187A8` | `0x03516E` | `res_drvr_sony.s:1456`<br>`res_drvr_sony_fdhd.s:1894` | old drive: drop our caller's return address and wait |
| **`Sony_CheckRead`** | `0x018504` | `0x034EA2` | `res_drvr_sony.s:1055`<br>`res_drvr_sony_fdhd.s:1465` | CheckRead -- BEQ if the request is a read (low byte of Command = aRdCmd, from ioTrap $A002), BNE for a write Called by: SONY_DISKPRIME_OK, SONY_DISKPRIME_LOOP, SONY_RESEEK_OK_2, SONY_RESEEK_SKIP_2, SO... |
| **`Sony_ChkDiskType`** | — | — | `res_drvr_sony_fdhd.s:3143` | ChkDiskType -- GCR or MFM? Entered from jtDiskPrime (not a subroutine: Recal calls WakeUp, which needs DiskPrime's stack level) after a new disk was recalibrated in GCR mode (DiskInPlace = 2). Only fo... |
| **`SONY_CHKDISKTYPE_DONE`** | — | — | `res_drvr_sony_fdhd.s:3170` | — |
| **`SONY_CHKDISKTYPE_MFM`** | — | — | `res_drvr_sony_fdhd.s:3158` | — |
| **`SONY_CHKDISKTYPE_NOMFM`** | — | — | `res_drvr_sony_fdhd.s:3168` | — |
| **`Sony_CkDCDExist`** | `0x018630` | `0x034FF6` | `res_drvr_sony.s:1233`<br>`res_drvr_sony_fdhd.s:1677` | CkDCDExist -- is an HD20 connected at the selected position? An HD20 shows /DrvExst = 1 and Sides = 1 (unlike a floppy drive) and asserts its /Exist line (register address 5, dcdExist). D0 (out) -- MI... |
| **`SONY_CKDCDEXIST_EXIT`** | `0x01864A` | `0x035010` | `res_drvr_sony.s:1247`<br>`res_drvr_sony_fdhd.s:1690` | — |
| **`SONY_CKDCDEXIST_NONE`** | `0x018648` | `0x03500E` | `res_drvr_sony.s:1245`<br>`res_drvr_sony_fdhd.s:1688` | — |
| **`SONY_CKDIP`** | `0x018BA4` | `0x0355C8` | `res_drvr_sony.s:2043`<br>`res_drvr_sony_fdhd.s:2590` | CkDIP -- is a disk in place (floppy) or the HD20 ready? |
| **`SONY_CKDIP_EVENT`** | — | `0x0355F2` | `res_drvr_sony.s:2305` | — |
| **`SONY_CKDIP_HD20`** | — | — | `res_drvr_sony_fdhd.s:2601` | HD20: CA0 and CA2 low (CA1 high, SEL low from DiskSel1) is the address where DCDWaitHSHK and DCDReset sense the HD20's handshake line HSHK; HSHK high = HD20 idle and ready |
| **`SONY_CKDIP_HD20SENSE`** | — | — | `res_drvr_sony_fdhd.s:2604` | — |
| **`SONY_CKDIP_POST`** | `0x018BC6` | `0x0355EA` | `res_drvr_sony.s:2059`<br>`res_drvr_sony_fdhd.s:2613` | — |
| **`SONY_CKDIP_SENSE`** | `0x018BBE` | `0x0355E2` | `res_drvr_sony.s:2055`<br>`res_drvr_sony_fdhd.s:2609` | HD20: address 8 (CA1 = 1, CA0 = SEL = CA2 = 0) after DiskSelect floppy: disk-in-place sense |
| **`Sony_CkDrvNum`** | `0x018040` | `0x0349E2` | `res_drvr_sony.s:508`<br>`res_drvr_sony_fdhd.s:884` | CkDrvNum -- check the drive number of a request and set up for it A0 (in) -- parameter block; ioVRefNum = drive number 1-6 D0 (out), CCR -- 0 (BEQ) or nsDrvErr (BNE); A1 = SonyVars, D1 = drive vars of... |
| **`SONY_CKDRVNUM_ERR`** | `0x018066` | `0x034A08` | `res_drvr_sony.s:521`<br>`res_drvr_sony_fdhd.s:896` | CkDrvNum error exit: drive number 0 or above 5 |
| **`SONY_CKEJECT`** | — | `0x0355A8` | `res_drvr_sony_fdhd.s:2578` | — |
| **`SONY_CKEJECT_SELECT`** | — | `0x0355B0` | `res_drvr_sony_fdhd.s:2581` | — |
| **`SONY_CKEJSW`** | — | `0x035608` | `res_drvr_sony_fdhd.s:2630` | CkEjSw -- read and reset the latched eject button of the selected drive (new on the SE); BMI if it was pressed |
| **`SONY_CKEJSW_EXIT`** | — | `0x03561A` | `res_drvr_sony_fdhd.s:2640` | — |
| **`SONY_CKEJSW_SENSE`** | — | — | `res_drvr_sony_fdhd.s:2633` | — |
| **`SONY_CKEXIT`** | `0x018BDC` | `0x035606` | `res_drvr_sony.s:2069`<br>`res_drvr_sony_fdhd.s:2625` | Called by: SONY_CKEJECT_SELECT, Sony_Check4Disk, SONY_CKEJECT, SONY_CKDIP, SONY_CKDIP_SENSE |
| **`SONY_CKINVAL`** | `0x018BD4` | `0x0355FE` | `res_drvr_sony.s:2066`<br>`res_drvr_sony_fdhd.s:2621` | CkInval -- the current track is unknown |
| **`SONY_CKWRPROT`** | — | `0x034A84` | `res_drvr_sony_fdhd.s:968` | CkWrProt -- a write to a write-protected disk fails |
| **`Sony_Control`** | `0x017F18` | `0x03487C` | `res_drvr_sony.s:357`<br>`res_drvr_sony_fdhd.s:519` | jtControl -- control call dispatcher (JControl vector) A0 (in) -- control parameter block KillIO (csCode 1), the tag buffer (8) and track cache (9) calls are handled first, without a drive number; the... |
| **`SONY_CONTROL_ALLOC`** | — | — | `res_drvr_sony_fdhd.s:588` | — |
| **`SONY_CONTROL_BADCODE`** | — | `0x0348B2` | `res_drvr_sony_fdhd.s:543` | — |
| **`SONY_CONTROL_CONT`** | `0x017F52` | — | `res_drvr_sony.s:388` | ctlTCInst -- allocate the cache buffer unless there is one |
| **`SONY_CONTROL_CONT_2`** | `0x017FBA` | — | `res_drvr_sony.s:436` | — |
| **`SONY_CONTROL_DISPATCH`** | — | `0x03488C` | `res_drvr_sony_fdhd.s:525` | — |
| **`SONY_CONTROL_DONE`** | `0x017F82` | `0x03491C` | `res_drvr_sony.s:405`<br>`res_drvr_sony_fdhd.s:600` | — |
| **`SONY_CONTROL_ERR`** | `0x017F72` | — | `res_drvr_sony.s:399` | ctlTCEnb -- TCInstalled = $FF if there is a buffer and enabling was asked |
| **`SONY_CONTROL_JUMP`** | — | `0x0348A8` | `res_drvr_sony_fdhd.s:536` | — |
| **`SONY_CONTROL_NEXT`** | — | `0x0348AE` | `res_drvr_sony_fdhd.s:540` | — |
| **`SONY_CONTROL_NEXT_2`** | `0x017FA2` | — | `res_drvr_sony.s:423` | — |
| **`SONY_CONTROL_NO_2`** | `0x017F86` | — | `res_drvr_sony.s:410` | csCodes 5, 6, 7, 21 and unknown codes: check the drive number, then look the csCode up in CtlTbl |
| **`SONY_CONTROL_OK`** | `0x017F9C` | — | `res_drvr_sony.s:420` | scan CtlTbl for the csCode |
| **`SONY_CONTROL_OK_2`** | `0x017FB0` | — | `res_drvr_sony.s:432` | use the HD20 offset (first) or the floppy offset (second) |
| **`SONY_CONTROL_SCAN`** | — | `0x034892` | `res_drvr_sony_fdhd.s:528` | — |
| **`SONY_CTL_EJECT`** | `0x017FBE` | `0x03493E` | `res_drvr_sony.s:443`<br>`res_drvr_sony_fdhd.s:627` | ctlSonyEjc (csCode 7, floppy) -- eject the disk. The drive is powered down at once; the interface stays selected for the eject pulse (Apple: "IODone is jumped to when the eject has been completed"). |
| **`SONY_CTL_EJECT_CKNEW`** | — | — | `res_drvr_sony_fdhd.s:663` | — |
| **`SONY_CTL_EJECT_GO`** | — | `0x034942` | `res_drvr_sony_fdhd.s:641` | — |
| **`SONY_CTL_EJECT_IWMHI`** | — | — | `res_drvr_sony_fdhd.s:661` | — |
| **`SONY_CTL_EJECT_IWMLO`** | — | — | `res_drvr_sony_fdhd.s:672` | — |
| **`SONY_CTL_EJECT_PULSE`** | — | — | `res_drvr_sony_fdhd.s:652` | — |
| **`SONY_CTL_EJECT_SEEK2`** | — | — | `res_drvr_sony_fdhd.s:638` | — |
| **`SONY_CTL_EJECTDONE`** | `0x017FF0` | `0x034994` | `res_drvr_sony.s:459`<br>`res_drvr_sony_fdhd.s:697` | CtlEjtOK -- ignore disk-in-place for the next EjectWait VBL calls |
| **`SONY_CTL_FORMAT`** | — | `0x0348BE` | `res_drvr_sony_fdhd.s:552` | ctlSonyFmt (csCode 6, floppy) -- format the disk in the drive. |
| **`SONY_CTL_KILLIO`** | — | `0x0348B8` | `res_drvr_sony_fdhd.s:548` | ctlKillIO (csCode 1) -- not supported (no way to abort an HD20 request), drive number not checked. |
| **`SONY_CTL_NOERR`** | `0x017FF6` | — | `res_drvr_sony.s:461` | CtlEjtOK -- ignore disk-in-place for the next EjectWait VBL calls |
| **`SONY_CTL_TAGBUF`** | `0x017F26` | `0x0348CE` | `res_drvr_sony.s:366`<br>`res_drvr_sony_fdhd.s:561` | ctlTagBuf (csCode 8) -- set (CSParam <> 0) or clear the separate tag buffer; drive number not needed. |
| **`SONY_CTL_TRKCACHE`** | `0x017F3A` | `0x0348DA` | `res_drvr_sony.s:376`<br>`res_drvr_sony_fdhd.s:571` | ctlTrkCache (csCode 9) -- track cache control; drive number not needed. CSParam+0: non-zero = enable, zero = disable the cache CSParam+1: >0 = install (allocate), <0 = remove, 0 = neither |
| **`SONY_CTL_VERIFY`** | — | `0x0348C6` | `res_drvr_sony_fdhd.s:556` | ctlSonyVer (csCode 5, floppy) -- verify the disk in the drive. |
| **`Sony_CtlFormat`** | `0x0190E6` | `0x035FCA` | `res_drvr_sony.s:2767`<br>`res_drvr_sony.s:3396` | CtlFormat (csCode 6) -- format a floppy disk: both sides on a two-sided drive (csParam = 1: one side only), one side on a one-sided drive ("putting a $0001 at csParam creates a single-sided disk", Tec... |
| **`SONY_CTLFORMAT_MARKS`** | `0x019124` | `0x036008` | `res_drvr_sony.s:2785`<br>`res_drvr_sony.s:3414` | — |
| **`SONY_CTLFORMAT_MARKS_2`** | `0x019128` | `0x03600C` | `res_drvr_sony.s:2788`<br>`res_drvr_sony.s:3417` | — |
| **`SONY_CTLFORMAT_SIDES`** | `0x019104` | `0x035FE8` | `res_drvr_sony.s:2776`<br>`res_drvr_sony.s:3405` | — |
| **`SONY_CTLFORMAT_TRACKLOOP`** | `0x01913A` | `0x03601E` | `res_drvr_sony.s:2795`<br>`res_drvr_sony.s:3423` | TrackLoop -- seek (checking the speed), format the track (both sides) |
| **`SONY_CTLTCENB`** | — | `0x03490C` | `res_drvr_sony_fdhd.s:594` | Called by: SONY_CTLTCINST, SONY_CTL_TRKCACHE |
| **`SONY_CTLTCINST`** | — | `0x0348EC` | `res_drvr_sony_fdhd.s:579` | — |
| **`Sony_CtlVerify`** | `0x0193CE` | `0x0362AE` | `res_drvr_sony.s:3140`<br>`res_drvr_sony.s:3741` | CtlVerify (csCode 5) -- read every sector of the disk, track 79 down to track 0 (both sides of a two-sided format), into a stack buffer; a read error aborts the call ("If any sector is found to be bad... |
| **`SONY_CTLVERIFY_CLASS`** | `0x0193E2` | `0x0362C2` | `res_drvr_sony.s:3148`<br>`res_drvr_sony.s:3748` | NxtVClass -- next zone inward: one more sector per track |
| **`SONY_CTLVERIFY_EXIT`** | `0x01940C` | `0x0362EC` | `res_drvr_sony.s:3165`<br>`res_drvr_sony.s:3764` | — |
| **`SONY_CTLVERIFY_TRACK`** | `0x0193E8` | `0x0362C8` | `res_drvr_sony.s:3153`<br>`res_drvr_sony.s:3752` | NxtVTrk -- seek to track D6, verify it |
| **`SONY_DCD_COMMAND`** | `0x019CF2` | `0x036BD4` | `res_drvr_sony.s:4322`<br>`res_drvr_sony_fdhd.s:4975` | HD20 format (csCode 6) |
| **`SONY_DCD_COMMAND_1`** | — | `0x036BDC` | `res_drvr_sony_fdhd.s:4981` | — |
| **`SONY_DCD_COMMAND_END`** | `0x019D84` | `0x036C74` | `res_drvr_sony.s:4378`<br>`res_drvr_sony.s:4875` | — |
| **`SONY_DCD_COMMAND_ERR`** | `0x019D48` | `0x036C32` | `res_drvr_sony.s:4351`<br>`res_drvr_sony_fdhd.s:5006` | error: reset (only once: then give up) if the first LastStatus byte is 2 or bChksum is clear; with bChksum set the first error resets too (BSET of retryonce falls through), later ones just retry. (DCD... |
| **`SONY_DCD_COMMAND_FAIL`** | `0x019D82` | `0x036C6C` | `res_drvr_sony.s:4376`<br>`res_drvr_sony_fdhd.s:5027` | failed (after a reset) |
| **`SONY_DCD_COMMAND_RESET`** | `0x019D60` | `0x036C4A` | `res_drvr_sony.s:4358`<br>`res_drvr_sony_fdhd.s:5013` | — |
| **`SONY_DCD_COMMAND_RETRY`** | `0x019D04` | `0x036BEE` | `res_drvr_sony.s:4328`<br>`res_drvr_sony_fdhd.s:4987` | — |
| **`SONY_DCD_COMMAND_SEND`** | `0x019D42` | `0x036C2C` | `res_drvr_sony.s:4344`<br>`res_drvr_sony_fdhd.s:5003` | — |
| **`SONY_DCD_COMMAND_STS`** | `0x019D90` | `0x036C80` | `res_drvr_sony.s:4384`<br>`res_drvr_sony.s:4879` | status command done: continue at StsRtnAddr |
| **`SONY_DCD_COMMAND_WAIT`** | `0x019D70` | `0x036C5A` | `res_drvr_sony.s:4366`<br>`res_drvr_sony_fdhd.s:5019` | wait for the response and receive it |
| **`SONY_DCD_COMMANDDONE`** | — | `0x036C6E` | `res_drvr_sony_fdhd.s:5029` | — |
| **`SONY_DCD_CTLEJECT`** | `0x017EDA` | `0x0349B0` | `res_drvr_sony.s:306`<br>`res_drvr_sony_fdhd.s:711` | DiskCtlErr / DiskDone -- I/O completion D0 (in) -- result code Saves a non-zero result in DskErr, clears Active and completes the request through the IODone vector (JIODone). SONY_DCD_CTLEJECT is the ... |
| **`SONY_DCD_CTLFORMAT`** | — | `0x0349A0` | `res_drvr_sony_fdhd.s:705` | HD20 format, verify and eject (csCodes 6, 5, 7 for drives 4-5). An HD20 is not ejected: DiskInPlace = 0 lets the VBL task (Check4Disk) post a disk-inserted event, so that the volume is mounted again (... |
| **`SONY_DCD_CTLVERIFY`** | — | `0x0349A8` | `res_drvr_sony_fdhd.s:708` | — |
| **`SONY_DCD_FORMAT`** | `0x019CF0` | `0x036BD2` | `res_drvr_sony.s:4320`<br>`res_drvr_sony_fdhd.s:4973` | HD20 format (csCode 6) |
| **`SONY_DCD_ICON`** | `0x019CD6` | `0x036BB8` | `res_drvr_sony.s:4297`<br>`res_drvr_sony_fdhd.s:4951` | HD20 icon call (csCode 21, drives 3-6): only if the HD20 has an icon (DevChIcon in its characteristics byte); the icon comes with the status data, so a status command is sent first ("The Hard Disk 20 ... |
| **`SONY_DCD_ICON_CHK`** | — | — | `res_drvr_sony_fdhd.s:4953` | — |
| **`SONY_DCD_ICONDONE`** | `0x019CC2` | `0x036BA4` | `res_drvr_sony.s:4283`<br>`res_drvr_sony_fdhd.s:4936` | ICONDONE -- back from the status command of an icon call: return a pointer to the icon (DevIcon, part of the HD20's status data) |
| **`SONY_DCD_ICONEXIT`** | `0x019CD2` | `0x036BB4` | `res_drvr_sony.s:4289`<br>`res_drvr_sony_fdhd.s:4942` | — |
| **`SONY_DCD_VERIFY`** | `0x019CEC` | `0x036BCE` | `res_drvr_sony.s:4315`<br>`res_drvr_sony_fdhd.s:4970` | HD20 verify (csCode 5) |
| **`SONY_DCDEXIT`** | `0x019648` | `0x036528` | `res_drvr_sony.s:3437`<br>`res_drvr_sony_fdhd.s:4150` | DCD exit -- deselect the HD20, open interrupts, complete the request |
| **`Sony_DCDPrime`** | `0x0194D6` | `0x0363B6` | `res_drvr_sony.s:3291`<br>`res_drvr_sony_fdhd.s:4020` | DCDPrime -- read or write on an HD20 (drives 3-6, from jtDiskPrime). The first access (DiskInPlace < 2) issues a status command to learn the drive's size and characteristics. Then the blocks are trans... |
| **`SONY_DCDPRIME_AGAIN`** | `0x019608` | `0x0364E8` | `res_drvr_sony.s:3406`<br>`res_drvr_sony_fdhd.s:4122` | — |
| **`SONY_DCDPRIME_CMD`** | `0x019586` | `0x036466` | `res_drvr_sony.s:3349`<br>`res_drvr_sony_fdhd.s:4073` | CMD -- HD20 command 0 (read) or 1 (write) |
| **`SONY_DCDPRIME_COUNT`** | `0x01959E` | `0x03647E` | `res_drvr_sony.s:3361`<br>`res_drvr_sony_fdhd.s:4084` | — |
| **`SONY_DCDPRIME_DONE`** | `0x019618` | `0x0364F8` | `res_drvr_sony.s:3419`<br>`res_drvr_sony_fdhd.s:4131` | DONE -- command done: update the tags, the position and the count |
| **`SONY_DCDPRIME_ERR`** | `0x0195DC` | `0x0364BC` | `res_drvr_sony.s:3391`<br>`res_drvr_sony_fdhd.s:4107` | ERR -- retry: after a communication error that is no checksum error first reset the HD20 (once); the last try always follows a reset |
| **`SONY_DCDPRIME_FAIL`** | `0x01960A` | `0x0364EA` | `res_drvr_sony.s:3410`<br>`res_drvr_sony_fdhd.s:4124` | FAIL -- out of tries: readErr or writErr |
| **`SONY_DCDPRIME_FAILEXIT`** | `0x019616` | `0x0364F6` | `res_drvr_sony.s:3415`<br>`res_drvr_sony_fdhd.s:4129` | — |
| **`SONY_DCDPRIME_GO`** | `0x019544` | `0x036424` | `res_drvr_sony.s:3326`<br>`res_drvr_sony_fdhd.s:4052` | GO -- check the request; a read-verify is not done on an HD20 |
| **`SONY_DCDPRIME_NEXT`** | `0x019590` | `0x036470` | `res_drvr_sony.s:3353`<br>`res_drvr_sony_fdhd.s:4076` | NEXT -- the next command: D3 = bytes left |
| **`SONY_DCDPRIME_RCV`** | `0x0195D0` | `0x0364B0` | `res_drvr_sony.s:3383`<br>`res_drvr_sony_fdhd.s:4101` | RCV -- receive and check the response (for a write the next block is sent from there) |
| **`SONY_DCDPRIME_RESET`** | `0x0195FE` | `0x0364DE` | `res_drvr_sony.s:3402`<br>`res_drvr_sony_fdhd.s:4118` | — |
| **`SONY_DCDPRIME_RETRY`** | `0x0195AE` | `0x03648E` | `res_drvr_sony.s:3368`<br>`res_drvr_sony_fdhd.s:4090` | RETRY -- (re)send the command |
| **`SONY_DCDPRIME_SELECT`** | `0x0194EA` | `0x0363CA` | `res_drvr_sony.s:3298`<br>`res_drvr_sony_fdhd.s:4027` | — |
| **`SONY_DCDPRIME_STATUS`** | `0x019508` | `0x0363E8` | `res_drvr_sony.s:3309`<br>`res_drvr_sony_fdhd.s:4036` | back from the status command (CCR = result): note the drive's status |
| **`SONY_DCDPRIME_UPDATE`** | `0x01962A` | `0x03650A` | `res_drvr_sony.s:3426`<br>`res_drvr_sony_fdhd.s:4138` | — |
| **`SONY_DCDPRIME_WAIT`** | `0x0195B8` | `0x036498` | `res_drvr_sony.s:3373`<br>`res_drvr_sony_fdhd.s:4094` | WAIT -- wait for the response to the command or block |
| **`Sony_DCDRcvPacket`** | `0x01980E` | `0x0366EC` | `res_drvr_sony.s:3663`<br>`res_drvr_sony_fdhd.s:4344` | DCDRcvPacket -- receive a packet from the HD20: $AA, then groups of 8 bytes: 7 data bytes (bits 7-1 in bits 6-0, bit 7 set) and a byte with their bits 0 (bit 0 for the first byte). D7 = full groups, i... |
| **`Sony_DCDRcvResponse`** | `0x019756` | `0x036636` | `res_drvr_sony.s:3573`<br>`res_drvr_sony_fdhd.s:4270` | DCDRcvResponse -- receive the HD20's response packet (DCDRcvPacket) and check it: response byte = command + $80, SeqNum = blocks left, status; store the tags of a read block and count the block; for a... |
| **`Sony_DCDReset`** | `0x019C6C` | `0x036B4A` | `res_drvr_sony.s:4246`<br>`res_drvr_sony_fdhd.s:4904` | jtDCDReset (JDCDReset vector) -- hard reset of the HD20: select it, address register 1 (dcdReset: CA1, CA0 low, CA2 high) for tRstAssert (100 ms), release it, wait tRstSettle (2 s), then until the HD2... |
| **`SONY_DCDRESET_CONT`** | `0x019CA0` | `0x036B82` | `res_drvr_sony.s:4261`<br>`res_drvr_sony_fdhd.s:4919` | wait until HSHK is high (the HD20 is ready) |
| **`SONY_DCDRESET_SKIP`** | `0x019CB6` | `0x036B98` | `res_drvr_sony.s:4271`<br>`res_drvr_sony_fdhd.s:4927` | ready |
| **`SONY_DCDRESET_SKIP_2`** | `0x019CBA` | `0x036B9C` | `res_drvr_sony.s:4276`<br>`res_drvr_sony_fdhd.s:4930` | timeout |
| **`Sony_DCDSendPacket`** | `0x019A20` | `0x0368FE` | `res_drvr_sony.s:3948`<br>`res_drvr_sony_fdhd.s:4616` | DCDSendPacket -- send a packet to the HD20: $AA, $80 + groups to send, $80 + groups to receive (counting the last ones), then groups of 8 bytes: a byte with the bits 0 of the 7 data bytes (bit 0 for t... |
| **`SONY_DCDSETUPCMD`** | `0x01967C` | `0x03655C` | `res_drvr_sony.s:3474`<br>`res_drvr_sony_fdhd.s:4179` | DCDSetupCmd -- set up a read or write command for D3 blocks from block D5: StartBlock (3 bytes, DriveOut = 0), SeqNum = block count, ChkTime and MaxTime for the first response, D6/D7 = data bytes to s... |
| **`SONY_DCDSETUPCMD_EXIT`** | `0x0196A4` | `0x03658A` | `res_drvr_sony.s:3486`<br>`res_drvr_sony_fdhd.s:4192` | the Mac Plus driver cleared the flag bits only after the read/write test |
| **`Sony_DCDStatus`** | `0x019CE8` | `0x036BCA` | `res_drvr_sony.s:4310`<br>`res_drvr_sony_fdhd.s:4967` | DCDStatus, HD20 verify (csCode 5) and format (csCode 6) -- send a one- block HD20 command (3 = status, $1A = verify, $19 = format) and wait for the response, with a retry and a hard reset. After a sta... |
| **`SONY_DCDWAITHSHK`** | `0x019658` | `0x036538` | `res_drvr_sony.s:3448`<br>`res_drvr_sony_fdhd.s:4160` | DCDWaitHSHK -- wait until the HD20 pulls HSHK low (status bit 7 = 0: it has a response to send): 100 polls, then every ChkTime (100-us units, WakeUp: the caller's caller gets control meanwhile) for at... |
| **`SONY_DCDWAITHSHK_1`** | `0x01965A` | `0x03653A` | `res_drvr_sony.s:3450`<br>`res_drvr_sony_fdhd.s:4162` | — |
| **`SONY_DCDWAITHSHK_2`** | `0x01965C` | `0x03653C` | `res_drvr_sony.s:3452`<br>`res_drvr_sony_fdhd.s:4164` | — |
| **`SONY_DCDWAITHSHK_EXIT`** | `0x01967A` | `0x03655A` | `res_drvr_sony.s:3464`<br>`res_drvr_sony_fdhd.s:4174` | return with the N flag of the last status read (or of MaxTime) |
| **`SONY_DENIBLTBL`** | `0x018EC4` | `0x035DA8` | `res_drvr_sony.s:2512`<br>`res_drvr_sony.s:3152` | GCR decode table (denibblize, Apple: DNib): disk nibble $96..$FF -> 6-bit value, $FF for the other nibbles (among them the mark bytes $AA and $D5); RdAddr/RdData index it with the disk byte (base SONY... |
| **`Sony_DiskCtlErr`** | `0x017EDE` | `0x034824` | `res_drvr_sony.s:308`<br>`res_drvr_sony_fdhd.s:450` | DiskCtlErr / DiskDone -- I/O completion D0 (in) -- result code Saves a non-zero result in DskErr, clears Active and completes the request through the IODone vector (JIODone). |
| **`Sony_DiskDone`** | `0x017EE0` | `0x034826` | `res_drvr_sony.s:311`<br>`res_drvr_sony_fdhd.s:453` | Called by: SONY_CONTROL_NO_2, SONY_CTL_NOERR, E_SONY_STATUS_LOOP, SONY_DISKPRIME_ERR_4, SONY_DCDEXIT |
| **`SONY_DISKDONE_1`** | `0x017EE8` | `0x03482E` | `res_drvr_sony.s:315`<br>`res_drvr_sony_fdhd.s:457` | — |
| **`SONY_DISKERR`** | — | `0x034AAA` | `res_drvr_sony_fdhd.s:990` | — |
| **`Sony_DiskPrime`** | `0x018070` | `0x034A12` | `res_drvr_sony.s:537`<br>`res_drvr_sony_fdhd.s:917` | jtDiskPrime -- read or write (JDiskPrime vector) A0 (in) -- I/O parameter block (ioTrap: $A002 read, $A003 write; ioPosMode bit 6 = read-verify), A1 (in) -- DCE Checks the drive and the disk; at the f... |
| **`SONY_DISKPRIME_CACHEOFS`** | — | — | `res_drvr_sony_fdhd.s:1123` | — |
| **`SONY_DISKPRIME_CONT`** | `0x0180B6` | `0x034A58` | `res_drvr_sony.s:563`<br>`res_drvr_sony_fdhd.s:947` | a connected drive? HD20 or floppy; for a floppy check disk-in-place (may have been ejected manually) no disk in the drive first access to this disk: power up, recalibrate, measure the speed |
| **`SONY_DISKPRIME_CONT_3`** | `0x0181AA` | `0x034B4C` | `res_drvr_sony.s:685`<br>`res_drvr_sony_fdhd.s:1080` | — |
| **`SONY_DISKPRIME_CONT_4`** | `0x0181F4` | — | `res_drvr_sony.s:718` | readCache -- copy the wanted sectors that are in the cache |
| **`SONY_DISKPRIME_CONT_5`** | `0x018244` | `0x034BE2` | `res_drvr_sony.s:750`<br>`res_drvr_sony_fdhd.s:1144` | — |
| **`SONY_DISKPRIME_EMPTY`** | `0x01813E` | — | `res_drvr_sony.s:625` | — |
| **`SONY_DISKPRIME_EMPTY_2`** | `0x018288` | — | `res_drvr_sony.s:778` | rc_Cont -- some sectors still to read from the disk |
| **`SONY_DISKPRIME_ERR`** | `0x0180F6` | — | `res_drvr_sony.s:585` | DskRWOff -- power down after the normal delay (exit with D0 = result) |
| **`SONY_DISKPRIME_ERR_2`** | `0x0180FC` | — | `res_drvr_sony.s:590` | DskImmOff -- immediate power-down (errors at the first access) |
| **`SONY_DISKPRIME_ERR_4`** | `0x018108` | — | `res_drvr_sony.s:599` | DiskErr -- open interrupts and complete the request |
| **`SONY_DISKPRIME_ERR_5`** | `0x018140` | — | `res_drvr_sony.s:627` | — |
| **`SONY_DISKPRIME_LOOP`** | `0x0181B0` | `0x034B52` | `res_drvr_sony.s:689`<br>`res_drvr_sony_fdhd.s:1084` | — |
| **`SONY_DISKPRIME_LOOP_2`** | `0x01821A` | — | `res_drvr_sony.s:732` | — |
| **`SONY_DISKPRIME_NEXT`** | `0x01811C` | — | `res_drvr_sony.s:609` | GetTrack -- the next track to do: side/track, first sector, sector map |
| **`SONY_DISKPRIME_NEXT_2`** | `0x01814C` | `0x034AEE` | `res_drvr_sony.s:637`<br>`res_drvr_sony_fdhd.s:1031` | — |
| **`SONY_DISKPRIME_NEXT_3`** | `0x018158` | `0x034AFA` | `res_drvr_sony.s:645`<br>`res_drvr_sony_fdhd.s:1038` | NxtTrack -- find the track (cylinder) within the zone |
| **`SONY_DISKPRIME_NO`** | `0x018142` | — | `res_drvr_sony.s:631` | NxtClass -- find the speed zone of the block (D2 = first block of it) |
| **`SONY_DISKPRIME_NO_2`** | `0x018188` | `0x034B2A` | `res_drvr_sony.s:671`<br>`res_drvr_sony_fdhd.s:1066` | the sectors wanted on this track: first sector, count, bitmap |
| **`SONY_DISKPRIME_NO_3`** | `0x018240` | `0x034BDE` | `res_drvr_sony.s:748`<br>`res_drvr_sony_fdhd.s:1142` | no separate tag buffer: tags go to the file tags buffer in low memory |
| **`SONY_DISKPRIME_NO_4`** | `0x01828C` | — | `res_drvr_sony.s:784` | rdCacheNV -- cache not valid: if reads into the cache are enabled, set it up for this drive and side/track |
| **`SONY_DISKPRIME_OK`** | `0x0180E2` | — | `res_drvr_sony.s:577` | CkWrProt -- a write to a write-protected disk? |
| **`SONY_DISKPRIME_OK_2`** | `0x018176` | — | `res_drvr_sony.s:661` | — |
| **`SONY_DISKPRIME_POFFEXIT`** | `0x0180FE` | — | `res_drvr_sony.s:593` | POffExit -- shared with the format and verify calls |
| **`SONY_DISKPRIME_POWER`** | — | — | `res_drvr_sony_fdhd.s:954` | — |
| **`SONY_DISKPRIME_SELECT`** | — | — | `res_drvr_sony_fdhd.s:932` | check drive is installed |
| **`SONY_DISKPRIME_SIDES`** | `0x018134` | `0x034AD6` | `res_drvr_sony.s:619`<br>`res_drvr_sony_fdhd.s:1014` | — |
| **`SONY_DISKPRIME_SKIP`** | `0x018110` | — | `res_drvr_sony.s:604` | RWPower -- set the speed for the current track and power up |
| **`SONY_DISKPRIME_SKIP_2`** | `0x0181F0` | — | `res_drvr_sony.s:714` | CheckCache -- use the track cache: reads take cached sectors, writes invalidate the cached copies of the sectors written; reading into the cache (TCRdEnable) only for a synchronous call on its last tr... |
| **`SONY_DISKPRIME_SKIP_3`** | `0x018262` | `0x034C00` | `res_drvr_sony.s:762`<br>`res_drvr_sony_fdhd.s:1156` | — |
| **`Sony_DiskSel1`** | `0x01892E` | `0x035310` | `res_drvr_sony.s:1690`<br>`res_drvr_sony_fdhd.s:2195` | DiskSel1 -- quick entry (Check4Disk): jump through the JDiskSel vector |
| **`SONY_DISKSEL1_VEC`** | — | — | `res_drvr_sony_fdhd.s:2201` | — |
| **`SONY_DISKSEL_CONT`** | `0x01898A` | `0x03537E` | `res_drvr_sony.s:1734`<br>`res_drvr_sony_fdhd.s:2256` | clock the chain (LSTRB pulse, CA1 low-high) while the sense line at address $D is high, at most D0 times |
| **`SONY_DISKSEL_CONT_2`** | `0x018994` | `0x035388` | `res_drvr_sony.s:1738`<br>`res_drvr_sony_fdhd.s:2260` | — |
| **`SONY_DISKSEL_HD20`** | `0x0189BE` | `0x0353B2` | `res_drvr_sony.s:1758`<br>`res_drvr_sony_fdhd.s:2279` | HD20 (drive 3-6): enable cut and reasserted, then Drive - 3 clocks at most |
| **`SONY_DISKSEL_INT`** | — | `0x035346` | `res_drvr_sony_fdhd.s:2234` | — |
| **`SONY_DISKSEL_LOOP`** | `0x0189A4` | `0x035398` | `res_drvr_sony.s:1746`<br>`res_drvr_sony_fdhd.s:2268` | one clock of the daisy chain |
| **`SONY_DISKSEL_LOWER`** | — | — | `res_drvr_sony_fdhd.s:2232` | — |
| **`SONY_DISKSEL_NO`** | `0x01895C` | `0x035350` | `res_drvr_sony.s:1715`<br>`res_drvr_sony_fdhd.s:2240` | external port: go to state 7 (PH0 = PH1 = PH2 = 1) safely ("we may already be enabled in state 2, so go safely thru 6", Apple), SEL low |
| **`SONY_DISKSEL_OK`** | `0x01897E` | `0x035372` | `res_drvr_sony.s:1727`<br>`res_drvr_sony_fdhd.s:2251` | pass-thru works: drive 2 = the external floppy, 3-6 = HD20s in the chain |
| **`SONY_DISKSEL_SKIP`** | `0x018948` | `0x03532A` | `res_drvr_sony.s:1705`<br>`res_drvr_sony_fdhd.s:2222` | — |
| **`Sony_DiskSelect`** | `0x01892A` | `0x03530C` | `res_drvr_sony.s:1687`<br>`res_drvr_sony_fdhd.s:2192` | DiskSelect -- enable the interface of the current drive (Drive); a floppy drive powers down whenever its enable is cut (Apple) |
| **`Sony_DiskVBLTask`** | `0x018B40` | `0x035542` | `res_drvr_sony.s:1996`<br>`res_drvr_sony_fdhd.s:2529` | DiskVBLTask -- VBL task, every DskVBLTime (30 ticks = 0.5 s): counts down a pending power-down (TimeOut) and looks for inserted disks; not while a request is active. Runs at IPL 1 (the SE driver: 3, A... |
| **`SONY_DISKVBLTASK_DONE`** | `0x018B80` | `0x035582` | `res_drvr_sony.s:2020`<br>`res_drvr_sony_fdhd.s:2553` | — |
| **`SONY_DISKVBLTASK_EXIT`** | `0x018B84` | `0x035586` | `res_drvr_sony.s:2022`<br>`res_drvr_sony_fdhd.s:2556` | — |
| **`SONY_DISKVBLTASK_LOOP`** | `0x018B6A` | `0x03556C` | `res_drvr_sony.s:2011`<br>`res_drvr_sony_fdhd.s:2544` | — |
| **`SONY_DISKVBLTASK_POLL`** | `0x018B68` | `0x03556A` | `res_drvr_sony.s:2009`<br>`res_drvr_sony_fdhd.s:2542` | — |
| **`SONY_DOFORMAT`** | `0x019282` | `0x036166` | `res_drvr_sony.s:2972`<br>`res_drvr_sony.s:3577` | DoFormat -- write the current track in one pass; the drive is up to speed and on the track. 200 sync groups, then per sector (FillInMarks order) GapSync - 1 sync groups, its 27 bytes from the mark buf... |
| **`SONY_DOFORMAT_ADRMK`** | `0x01930C` | `0x0361EE` | `res_drvr_sony.s:3033`<br>`res_drvr_sony.s:3639` | ... the sector's 27 bytes from the mark buffer ... |
| **`SONY_DOFORMAT_ADRMK_2`** | `0x019318` | `0x0361FA` | `res_drvr_sony.s:3040`<br>`res_drvr_sony.s:3646` | — |
| **`SONY_DOFORMAT_DATA`** | `0x019320` | `0x036202` | `res_drvr_sony.s:3044`<br>`res_drvr_sony.s:3650` | ... 703 $96 nibbles: tags, data and checksums of a sector of zeroes ... |
| **`SONY_DOFORMAT_DATA_2`** | `0x01932E` | `0x036210` | `res_drvr_sony.s:3051`<br>`res_drvr_sony.s:3657` | — |
| **`SONY_DOFORMAT_EXIT`** | `0x019354` | `0x036236` | `res_drvr_sony.s:3074`<br>`res_drvr_sony.s:3680` | — |
| **`SONY_DOFORMAT_GAP`** | `0x0192F2` | `0x0361D4` | `res_drvr_sony.s:3018`<br>`res_drvr_sony.s:3624` | SONY_DOFORMAT_NXTSECT -- per-sector loop: write inter-sector sync, address, gap, data |
| **`SONY_DOFORMAT_GAP_2`** | `0x0192F6` | `0x0361D8` | `res_drvr_sony.s:3021`<br>`res_drvr_sony.s:3627` | — |
| **`SONY_DOFORMAT_GAP_3`** | `0x019302` | `0x0361E4` | `res_drvr_sony.s:3028`<br>`res_drvr_sony.s:3634` | — |
| **`SONY_DOFORMAT_NXTSECT`** | `0x0192F0` | `0x0361D2` | `res_drvr_sony.s:3016`<br>`res_drvr_sony.s:3622` | WrNxtSect -- a sector: GapSync - 1 sync groups ... |
| **`SONY_DOFORMAT_OK`** | `0x019352` | `0x036234` | `res_drvr_sony.s:3072`<br>`res_drvr_sony.s:3678` | underrun? (write handshake bit 6 = 0) no underrun |
| **`SONY_DOFORMAT_SIDE`** | `0x01929A` | `0x03617E` | `res_drvr_sony.s:2981`<br>`res_drvr_sony.s:3586` | — |
| **`SONY_DOFORMAT_SLIP`** | `0x019336` | `0x036218` | `res_drvr_sony.s:3056`<br>`res_drvr_sony.s:3662` | ... and the slip marks $DE $AA $FF $FF (AdrMkTbl bytes 14-17) |
| **`SONY_DOFORMAT_STRTSYNC`** | `0x0192CE` | `0x0361B0` | `res_drvr_sony.s:2996`<br>`res_drvr_sony.s:3602` | WrStrtSync -- 200 sync groups, two bytes per pass |
| **`SONY_DOFORMAT_WSS1`** | `0x0192D2` | `0x0361B4` | `res_drvr_sony.s:2999`<br>`res_drvr_sony.s:3605` | — |
| **`SONY_DOFORMAT_WSS1_HSHK`** | `0x0192D4` | `0x0361B6` | `res_drvr_sony.s:3001`<br>`res_drvr_sony.s:3607` | — |
| **`SONY_DOFORMAT_WSS1_HSHK2`** | `0x0192E2` | `0x0361C4` | `res_drvr_sony.s:3009`<br>`res_drvr_sony.s:3615` | — |
| **`SONY_DORECAL`** | — | `0x034F20` | `res_drvr_sony_fdhd.s:1528` | DoRecal -- recalibrate to track 0, measure the speeds again and retry |
| **`Sony_DriveStatus`** | — | — | `res_drvr_sony_fdhd.s:764` | DriveStatus (csCode 8) -- copy the first 22 bytes of the drive variables (track, write-protect, disk-in-place, installed, sides, drive queue element, two-sided format, new interface, soft error count)... |
| **`SONY_DRIVESTATUS_LOOP`** | — | `0x0349D8` | `res_drvr_sony_fdhd.s:767` | — |
| **`SONY_DRVENT_ADRANDSENSE`** | — | — | `res_drvr_sony_fdhd.s:5098` | — |
| **`SONY_DRVENT_ADRDISK`** | — | — | `res_drvr_sony_fdhd.s:5084` | Driver entry table for the code in the ROM tail: the tail calls driver routines through its own jump table (TAIL_DRV_*, absolute JMPs to the entries here), so neither side depends on the other's routi... |
| **`SONY_DRVENT_DISKDONE`** | — | — | `res_drvr_sony_fdhd.s:5112` | — |
| **`SONY_DRVENT_DISKSELECT`** | — | — | `res_drvr_sony_fdhd.s:5096` | — |
| **`SONY_DRVENT_DSKRTN`** | — | — | `res_drvr_sony_fdhd.s:5090` | — |
| **`SONY_DRVENT_DSKRWOFF`** | — | — | `res_drvr_sony_fdhd.s:5102` | — |
| **`SONY_DRVENT_EMPTYPD`** | — | — | `res_drvr_sony_fdhd.s:5106` | — |
| **`SONY_DRVENT_GETDRV1`** | — | — | `res_drvr_sony_fdhd.s:5086` | — |
| **`SONY_DRVENT_GETFREQ1`** | — | — | `res_drvr_sony_fdhd.s:5114` | — |
| **`SONY_DRVENT_MFMTTRACK`** | — | — | `res_drvr_sony_fdhd.s:5100` | — |
| **`SONY_DRVENT_MRDADDR`** | — | — | `res_drvr_sony_fdhd.s:5088` | — |
| **`SONY_DRVENT_MRDDATA`** | — | — | `res_drvr_sony_fdhd.s:5092` | — |
| **`SONY_DRVENT_MVERTRACK`** | — | — | `res_drvr_sony_fdhd.s:5104` | — |
| **`SONY_DRVENT_RWPOWERUP`** | — | — | `res_drvr_sony_fdhd.s:5110` | — |
| **`SONY_DRVENT_SEEK`** | — | — | `res_drvr_sony_fdhd.s:5108` | — |
| **`SONY_DRVENT_SETCHIPMODE`** | — | — | `res_drvr_sony_fdhd.s:5094` | — |
| **`SONY_DRVPAD`** | — | — | `res_drvr_sony_fdhd.s:5117` | unused space to the end of the resource |
| **`SONY_DSKIMMOFF`** | — | `0x034A9E` | `res_drvr_sony_fdhd.s:983` | — |
| **`SONY_DSKPARMERR`** | — | `0x034AE0` | `res_drvr_sony_fdhd.s:1020` | — |
| **`SONY_DSKRTN`** | `0x018B22` | `0x03553A` | `res_drvr_sony.s:1970`<br>`res_drvr_sony_fdhd.s:2517` | DskRtn -- return to the continuation in DskRtnAdr with CCR = D0 |
| **`SONY_DSKRWOFF`** | — | `0x034A98` | `res_drvr_sony_fdhd.s:980` | DskRWOff / DskImmOff / POffExit / DiskErr -- the exits of DiskPrime, after an error and after the last sector (format and verify exit through POffExit with D2 = PwrOffTime): start the power-down (DskR... |
| **`SONY_DTAMKS`** | `0x018CD8` | `0x035BBC` | `res_drvr_sony.s:2226`<br>`res_drvr_sony.s:2874` | DtaMks -- data mark $D5 $AA $AD, slip marks $DE $AA, then $FF |
| **`Sony_EmptyPD`** | `0x01850C` | `0x034EAA` | `res_drvr_sony.s:1064`<br>`res_drvr_sony_fdhd.s:1475` | EmptyPD -- pass the SCC bytes that the polling code pushed on the stack (poll data) to PollProc (the serial driver), or discard them if there is none, and return to the caller with the stack reset (Po... |
| **`SONY_EMPTYPD_NOPROC`** | `0x018530` | `0x034ECE` | `res_drvr_sony.s:1080`<br>`res_drvr_sony_fdhd.s:1489` | no PollProc: discard the poll data |
| **`SONY_EMPTYPD_RESUME`** | `0x018524` | `0x034EC2` | `res_drvr_sony.s:1074`<br>`res_drvr_sony_fdhd.s:1484` | back from PollProc |
| **`Sony_FastPower`** | `0x018906` | `0x0352E8` | `res_drvr_sony.s:1659`<br>`res_drvr_sony_fdhd.s:2145` | FastPower -- power up without waiting (400K: MakeSpdTbl waits anyway) |
| **`Sony_FigTrkSpd`** | `0x018A90` | `0x035484` | `res_drvr_sony.s:1890`<br>`res_drvr_sony_fdhd.s:2416` | jtFigTrkSpd -- VIA timer 2 counts for 15 tachometer pulses (1/4 revolution; TACH gives 60 pulses per revolution). The TACH sense is read as status bit 7 while VIA timer 2 counts down from $FFFF (783.3... |
| **`SONY_FIGTRKSPD_CONT_2`** | `0x018ADE` | `0x0354DE` | `res_drvr_sony.s:1924`<br>`res_drvr_sony_fdhd.s:2455` | synchronized: restart the timer, count 15 more pulses |
| **`SONY_FIGTRKSPD_EXIT`** | `0x018AC2` | `0x0354B6` | `res_drvr_sony.s:1907`<br>`res_drvr_sony_fdhd.s:2433` | — |
| **`SONY_FIGTRKSPD_LOOP`** | `0x018AE2` | `0x0354E2` | `res_drvr_sony.s:1927`<br>`res_drvr_sony_fdhd.s:2458` | — |
| **`SONY_FIGTRKSPD_OK`** | `0x018AFA` | `0x0354FA` | `res_drvr_sony.s:1937`<br>`res_drvr_sony_fdhd.s:2468` | counts = $FFFF - timer (high byte read twice: if it changed, low = 0) |
| **`SONY_FILLINMARKS`** | `0x019362` | `0x036242` | `res_drvr_sony.s:3088`<br>`res_drvr_sony.s:3691` | FillInMarks -- put the address fields of the track's sectors into the mark buffer, in 2:1 interleave order 0, k, 1, k+1, ... (k = (n-1)/2 + 1; 12 sectors: 0 6 1 7 2 8 3 9 4 10 5 11): track bits 0-5, s... |
| **`SONY_FILLINMARKS_1`** | `0x019378` | `0x036258` | `res_drvr_sony.s:3096`<br>`res_drvr_sony.s:3699` | — |
| **`SONY_FILLINMARKS_LOOP`** | `0x0193A0` | `0x036280` | `res_drvr_sony.s:3113`<br>`res_drvr_sony.s:3716` | — |
| **`SONY_FMTSPEEDTBL`** | `0x019168` | `0x03604C` | `res_drvr_sony.s:2817`<br>`res_drvr_sony.s:3440` | FmtSpdTbl -- speed limits for formatting with a 400K drive: upper and lower speed value per zone, +-1% around the zone's speed (the limits for reading and writing, SpeedCheckTbl, allow +-2%). Speed va... |
| **`SONY_FMTVEREXIT`** | `0x01915C` | `0x036040` | `res_drvr_sony.s:2808`<br>`res_drvr_sony.s:3434` | FmtVerExit -- release the stack buffer, power down after the normal delay and complete the request (also the exit of CtlVerify) |
| **`SONY_FMTVERSEEK`** | `0x0194B6` | `0x036396` | `res_drvr_sony.s:3256`<br>`res_drvr_sony.s:3840` | FmtVerSeek -- seek to D6 synchronously (SyncCall with Seek) |
| **`SONY_FORMATTRACK`** | `0x0191E6` | `0x0360CA` | `res_drvr_sony.s:2890`<br>`res_drvr_sony.s:3506` | FormatTrack -- format the current track (and side 1 of it for a two- sided format): FillInMarks, DoFormat, then RdAddr right behind the write must find sector 0 (fmt1Err otherwise); the nibbles read b... |
| **`SONY_FORMATTRACK_1`** | `0x019202` | `0x0360E6` | `res_drvr_sony.s:2901`<br>`res_drvr_sony.s:3517` | FmtTrk1 -- write the track, then look for sector 0 |
| **`SONY_FORMATTRACK_CHECK`** | `0x019214` | `0x0360F8` | `res_drvr_sony.s:2909`<br>`res_drvr_sony.s:3524` | the poll data stays on the stack: RdAddr reads the next address field |
| **`SONY_FORMATTRACK_DECRSN1`** | `0x019278` | `0x03615C` | `res_drvr_sony.s:2951`<br>`res_drvr_sony.s:3563` | DecrSn1 -- one sync group less per sector, write the track again |
| **`SONY_FORMATTRACK_DECRSYNC`** | `0x019274` | `0x036158` | `res_drvr_sony.s:2947`<br>`res_drvr_sony.s:3560` | DecrSync -- too little sync: accept the track if only one group short |
| **`SONY_FORMATTRACK_DONE`** | `0x01926A` | `0x03614E` | `res_drvr_sony.s:2940`<br>`res_drvr_sony.s:3554` | — |
| **`SONY_FORMATTRACK_EXIT`** | `0x01926E` | `0x036152` | `res_drvr_sony.s:2942`<br>`res_drvr_sony.s:3556` | — |
| **`SONY_FORMATTRACK_GAP`** | `0x019220` | `0x036104` | `res_drvr_sony.s:2915`<br>`res_drvr_sony.s:3530` | — |
| **`SONY_FORMATTRACK_OK`** | `0x019256` | `0x03613A` | `res_drvr_sony.s:2934`<br>`res_drvr_sony.s:3548` | FTExitOK -- side 0 done: format side 1 of a two-sided format |
| **`SONY_FVPOWERUP`** | `0x0194D0` | `0x0363B0` | `res_drvr_sony.s:3278`<br>`res_drvr_sony.s:3858` | FVPowerUp -- power up synchronously (SyncCall with RWPowerUp) |
| **`SONY_GETASECTOR`** | — | — | `res_drvr_sony_fdhd.s:3174` | GetASector -- try up to six times to read an address mark on side 0 D0 (out) -- RdAddr result (MI = none found); D3 -- format byte |
| **`SONY_GETASECTOR_LOOP`** | — | — | `res_drvr_sony_fdhd.s:3176` | — |
| **`Sony_GetDrive`** | `0x0185AC` | `0x034F56` | `res_drvr_sony.s:1147`<br>`res_drvr_sony_fdhd.s:1565` | GetDrive, GetDrv1 -- set up the much-used registers A0 (out) -- IWM base (GetDrive), A2 (out) -- VIA base (GetDrive) A1 (out) -- SonyVars, D1 (out) -- offset of the current drive's vars Called by: E_S... |
| **`Sony_GetDrv1`** | `0x0185B4` | `0x034F5E` | `res_drvr_sony.s:1152`<br>`res_drvr_sony_fdhd.s:1569` | GetDrv1 -- A1 = SonyVars, D1 = DrvVarOS entry of Drive Called by: Sony_CkDrvNum, SONY_RESEEK_SKIP_2, SONY_EMPTYPD_RESUME, SONY_EMPTYPD_NOPROC, Sony_SetSpeed (and 13 more) |
| **`Sony_GetDrv2`** | — | `0x034F74` | `res_drvr_sony_fdhd.s:1578` | GetDrv2 -- A1 = SonyVars, D1 = Drive * 2 (Drive bounded to 5) |
| **`SONY_GETDRV3`** | — | `0x034F86` | `res_drvr_sony_fdhd.s:1584` | — |
| **`SONY_GETDRVTBL_ERR`** | — | `0x0356B4` | `res_drvr_sony.s:2420` | — |
| **`SONY_GETFREQ`** | `0x018A5E` | `0x035452` | `res_drvr_sony.s:1856`<br>`res_drvr_sony_fdhd.s:2383` | GetFreq -- set speed code D2 (SetASpeed), wait PwrOnTime, then GetFreq1 GetFreq1 -- D4 = speed value: 4 FigTrkSpd measurements of 1/4 revolution each, sum / 8, $4000000 / that = 2^29 / counts per revo... |
| **`SONY_GETFREQ1`** | `0x018A6C` | `0x035460` | `res_drvr_sony.s:1862`<br>`res_drvr_sony_fdhd.s:2389` | SONY_GETFREQ1 -- average 4 TACH period measurements |
| **`SONY_GETFREQ1_EXIT`** | `0x018A88` | `0x03547C` | `res_drvr_sony.s:1875`<br>`res_drvr_sony_fdhd.s:2402` | — |
| **`SONY_GETFREQ1_LOOP`** | `0x018A70` | `0x035464` | `res_drvr_sony.s:1865`<br>`res_drvr_sony_fdhd.s:2392` | — |
| **`Sony_GetRDrive`** | — | `0x034F46` | `res_drvr_sony_fdhd.s:1558` | GetRDrive, GetDrive, GetDrv1, GetDrv2 -- set up the much-used registers A0 (out) -- IWM base (GetRDrive, GetDrive) A2 (out) -- VIA base (GetRDrive, GetDrive) A1 (out) -- SonyVars D1 (out) -- offset of... |
| **`SONY_GETTRACK`** | — | `0x034ABE` | `res_drvr_sony_fdhd.s:1002` | GetTrack -- convert the current byte position into side/track, first sector and sector bitmap for the next track to process |
| **`SONY_GOTSECT`** | — | `0x034E22` | `res_drvr_sony_fdhd.s:1408` | GotSect -- mark the sector done, update position and byte count, then continue with the track (or the next track) |
| **`SONY_GOWAKEIT`** | `0x018828` | `0x0351FA` | `res_drvr_sony.s:1538`<br>`res_drvr_sony_fdhd.s:1994` | GoWakeIt -- Time Manager routine of TimeQEl: restore the saved registers and call the continuation (DskRtn) with D0 = 0 (Apple: "D0 = for RWT-MakeSpdTbl new intf path") |
| **`SONY_GOWAKEIT_EXIT`** | — | `0x035212` | `res_drvr_sony_fdhd.s:2001` | — |
| **`SONY_GTRESUME`** | — | `0x034B18` | `res_drvr_sony_fdhd.s:1057` | gtResume -- mGetTrack continues here too: D5 = track, D6 = side and D0/D2/D3 set up so that D0 - D2 is the first sector wanted and D3 - that the number of sectors left on the track |
| **`SONY_GZPROC`** | `0x017EA4` | — | `res_drvr_sony.s:265` | install the grow-zone procedure that frees the track cache buffer Grow-zone procedure of the system heap: frees the track cache buffer (TCdispose) when the Memory Manager needs space; if there was non... |
| **`SONY_GZPROC_RET`** | `0x017EB6` | — | `res_drvr_sony.s:275` | GZ proc return -- delivers freed size to Memory Manager |
| **`SONY_INITIALS`** | — | — | `res_drvr_sony_fdhd.s:5074` | initials (SWC, GGD and LAK sign Apple's Sony driver history notes: Steve Christensen, Gary Davidian, Larry Kenyon) and unused space up to the driver entry table |
| **`SONY_INVALTRKCACHE`** | `0x018842` | `0x0352D8` | `res_drvr_sony.s:1550`<br>`res_drvr_sony_fdhd.s:2122` | InvalTrkCache -- invalidate the track cache if it holds data of the current drive (TCDrive = Drive) |
| **`SONY_INVALTRKCACHE_EXIT`** | `0x018850` | `0x0352E6` | `res_drvr_sony.s:1555`<br>`res_drvr_sony_fdhd.s:2127` | — |
| **`Sony_jtDiskSel`** | `0x018934` | `0x035316` | `res_drvr_sony.s:1697`<br>`res_drvr_sony_fdhd.s:2214` | jtDiskSel (JDiskSel vector): power down another drive with a pending power-down, then select drive 1 (/ENBL1), or the external port (/ENBL2) with the daisy chain clocked to the drive wanted when pass-... |
| **`SONY_JTMRDADDR`** | — | — | `res_drvr_sony_fdhd.s:3353` | jtMRdAddr (jMRdAddr vector) |
| **`SONY_JTMRDDATA`** | — | — | `res_drvr_sony_fdhd.s:3446` | jtMRdData (jMRdData vector) |
| **`SONY_JTMWRDATA`** | — | — | `res_drvr_sony_fdhd.s:3565` | jtMWrData (jMWrData vector) |
| **`Sony_mAdrDisk`** | — | — | `res_drvr_sony_fdhd.s:3196` | mAdrDisk -- AdrDisk with the ISM registers selected: CA0-CA2 are set through the phase register (bits 0-3 = PHASE0-3 = CA0, CA1, CA2, LSTRB; bits 4-7 = 1: all four lines outputs), SEL through VIA port... |
| **`SONY_MADRDISK_PHASES`** | — | — | `res_drvr_sony_fdhd.s:3204` | — |
| **`SONY_MADRDISK_SELLO`** | — | — | `res_drvr_sony_fdhd.s:3202` | — |
| **`Sony_MakeSpdTbl`** | `0x0189EA` | `0x0353DE` | `res_drvr_sony.s:1791`<br>`res_drvr_sony_fdhd.s:2316` | jtMakeSpdTbl: measure the speed values f128 and f256 at speed codes $80 and $100 and, assuming them linear in the code, compute for each zone the code of the limits' midpoint t, code = 128 * (t + f256... |
| **`SONY_MAKESPDTBL_CONT`** | `0x0189F8` | `0x0353EC` | `res_drvr_sony.s:1799`<br>`res_drvr_sony_fdhd.s:2325` | 400K drive: f128, f256 at codes $80 and $100; for each zone the code of the midpoint (TSTblCode), the 2% delta (TSTblDelta), TSTblTicks = 0 |
| **`SONY_MAKESPDTBL_CONT_2`** | `0x018A14` | `0x035408` | `res_drvr_sony.s:1812`<br>`res_drvr_sony_fdhd.s:2338` | — |
| **`SONY_MAKESPDTBL_CONT_3`** | `0x018A2E` | `0x035422` | `res_drvr_sony.s:1825`<br>`res_drvr_sony_fdhd.s:2352` | — |
| **`SONY_MAKESPDTBL_CONT_4`** | `0x018A38` | `0x03542C` | `res_drvr_sony.s:1831`<br>`res_drvr_sony_fdhd.s:2358` | — |
| **`SONY_MAKESPDTBL_ERR`** | `0x018A5A` | `0x03544E` | `res_drvr_sony.s:1847`<br>`res_drvr_sony_fdhd.s:2374` | — |
| **`SONY_MAKESPDTBL_LOOP`** | `0x018A24` | `0x035418` | `res_drvr_sony.s:1819`<br>`res_drvr_sony_fdhd.s:2346` | per zone: pass 1 code of the midpoint t, pass 2 code of the upper limit |
| **`SONY_MAKESPDTBL_OK`** | `0x018A46` | `0x03543A` | `res_drvr_sony.s:1837`<br>`res_drvr_sony_fdhd.s:2364` | — |
| **`SONY_MDISKSEL_CHAIN`** | — | — | `res_drvr_sony_fdhd.s:3267` | — |
| **`SONY_MDISKSEL_CLOCK`** | — | — | `res_drvr_sony_fdhd.s:3273` | — |
| **`SONY_MDISKSEL_EXT`** | — | — | `res_drvr_sony_fdhd.s:3259` | — |
| **`SONY_MDISKSEL_HD20`** | — | — | `res_drvr_sony_fdhd.s:3291` | — |
| **`SONY_MDISKSEL_INT`** | — | — | `res_drvr_sony_fdhd.s:3255` | — |
| **`SONY_MDISKSEL_LOOP`** | — | — | `res_drvr_sony_fdhd.s:3277` | — |
| **`SONY_MDISKSEL_SENSE`** | — | — | `res_drvr_sony_fdhd.s:3286` | — |
| **`SONY_MDISKSEL_UPPER`** | — | — | `res_drvr_sony_fdhd.s:3253` | — |
| **`Sony_mDiskSelect`** | — | — | `res_drvr_sony_fdhd.s:3246` | mDiskSelect -- jtDiskSel with the ISM registers selected: the mode register enables the drive (bit 1 + MotorOn: /ENBL1, the internal drives; bit 2 + MotorOn: /ENBL2, the external port); VIA PA4 choose... |
| **`Sony_mDoFormat`** | — | — | `res_drvr_sony_fdhd.s:3706` | mDoFormat -- format one side of an MFM track (interrupts off, disk up to speed, head positioned) D2 (in) -- sectors per track - 1 (8 or 17; bit 31 = 1440K) D4 (in) -- track, D5 (in) -- side D0 (out) -... |
| **`SONY_MDOFORMAT_ACRC`** | — | — | `res_drvr_sony_fdhd.s:3873` | — |
| **`SONY_MDOFORMAT_AMARK`** | — | — | `res_drvr_sony_fdhd.s:3829` | — |
| **`SONY_MDOFORMAT_AMARK4`** | — | — | `res_drvr_sony_fdhd.s:3838` | — |
| **`SONY_MDOFORMAT_AMARKW`** | — | — | `res_drvr_sony_fdhd.s:3833` | — |
| **`SONY_MDOFORMAT_ASYNC`** | — | — | `res_drvr_sony_fdhd.s:3816` | — |
| **`SONY_MDOFORMAT_ASYNCL`** | — | — | `res_drvr_sony_fdhd.s:3819` | — |
| **`SONY_MDOFORMAT_ASYNCW`** | — | — | `res_drvr_sony_fdhd.s:3823` | — |
| **`SONY_MDOFORMAT_CYL`** | — | — | `res_drvr_sony_fdhd.s:3845` | — |
| **`SONY_MDOFORMAT_DATA`** | — | — | `res_drvr_sony_fdhd.s:3913` | — |
| **`SONY_MDOFORMAT_DATAW`** | — | — | `res_drvr_sony_fdhd.s:3917` | — |
| **`SONY_MDOFORMAT_DCRC`** | — | — | `res_drvr_sony_fdhd.s:3922` | — |
| **`SONY_MDOFORMAT_DMARK`** | — | — | `res_drvr_sony_fdhd.s:3899` | — |
| **`SONY_MDOFORMAT_DMARK4`** | — | — | `res_drvr_sony_fdhd.s:3908` | — |
| **`SONY_MDOFORMAT_DMARKW`** | — | — | `res_drvr_sony_fdhd.s:3903` | — |
| **`SONY_MDOFORMAT_DONE`** | — | — | `res_drvr_sony_fdhd.s:3957` | — |
| **`SONY_MDOFORMAT_DSYNC`** | — | — | `res_drvr_sony_fdhd.s:3889` | — |
| **`SONY_MDOFORMAT_DSYNCW`** | — | — | `res_drvr_sony_fdhd.s:3893` | — |
| **`SONY_MDOFORMAT_EXIT`** | — | — | `res_drvr_sony_fdhd.s:3962` | — |
| **`SONY_MDOFORMAT_GAP1`** | — | — | `res_drvr_sony_fdhd.s:3791` | — |
| **`SONY_MDOFORMAT_GAP1W`** | — | — | `res_drvr_sony_fdhd.s:3795` | — |
| **`SONY_MDOFORMAT_GAP2`** | — | — | `res_drvr_sony_fdhd.s:3878` | — |
| **`SONY_MDOFORMAT_GAP2W`** | — | — | `res_drvr_sony_fdhd.s:3882` | — |
| **`SONY_MDOFORMAT_GAP3`** | — | — | `res_drvr_sony_fdhd.s:3807` | — |
| **`SONY_MDOFORMAT_GAP3W`** | — | — | `res_drvr_sony_fdhd.s:3811` | — |
| **`SONY_MDOFORMAT_GAP4A`** | — | — | `res_drvr_sony_fdhd.s:3756` | — |
| **`SONY_MDOFORMAT_GAP4AW`** | — | — | `res_drvr_sony_fdhd.s:3760` | — |
| **`SONY_MDOFORMAT_HEAD`** | — | — | `res_drvr_sony_fdhd.s:3712` | — |
| **`SONY_MDOFORMAT_IDXHI`** | — | — | `res_drvr_sony_fdhd.s:3741` | — |
| **`SONY_MDOFORMAT_IDXHIW`** | — | — | `res_drvr_sony_fdhd.s:3745` | — |
| **`SONY_MDOFORMAT_IDXLO`** | — | — | `res_drvr_sony_fdhd.s:3729` | — |
| **`SONY_MDOFORMAT_IDXLOW`** | — | — | `res_drvr_sony_fdhd.s:3733` | — |
| **`SONY_MDOFORMAT_IDXON`** | — | — | `res_drvr_sony_fdhd.s:3935` | — |
| **`SONY_MDOFORMAT_IMARK`** | — | — | `res_drvr_sony_fdhd.s:3777` | — |
| **`SONY_MDOFORMAT_IMARK4`** | — | — | `res_drvr_sony_fdhd.s:3786` | — |
| **`SONY_MDOFORMAT_IMARKW`** | — | — | `res_drvr_sony_fdhd.s:3781` | — |
| **`SONY_MDOFORMAT_ISYNC`** | — | — | `res_drvr_sony_fdhd.s:3767` | — |
| **`SONY_MDOFORMAT_ISYNCW`** | — | — | `res_drvr_sony_fdhd.s:3771` | — |
| **`SONY_MDOFORMAT_LASTGAP`** | — | — | `res_drvr_sony_fdhd.s:3937` | — |
| **`SONY_MDOFORMAT_LASTGAPW`** | — | — | `res_drvr_sony_fdhd.s:3941` | — |
| **`SONY_MDOFORMAT_LASTNEXT`** | — | — | `res_drvr_sony_fdhd.s:3950` | — |
| **`SONY_MDOFORMAT_NEXTSECT`** | — | — | `res_drvr_sony_fdhd.s:3802` | — |
| **`SONY_MDOFORMAT_NOINDEX`** | — | — | `res_drvr_sony_fdhd.s:3954` | — |
| **`SONY_MDOFORMAT_SECT`** | — | — | `res_drvr_sony_fdhd.s:3859` | — |
| **`SONY_MDOFORMAT_SIDE`** | — | — | `res_drvr_sony_fdhd.s:3852` | — |
| **`SONY_MDOFORMAT_SIZE`** | — | — | `res_drvr_sony_fdhd.s:3866` | — |
| **`SONY_MDOFORMAT_START`** | — | — | `res_drvr_sony_fdhd.s:3753` | — |
| **`SONY_MFM_CHECKCRC`** | — | — | `res_drvr_sony_fdhd.s:3512` | CheckCRC -- read the two CRC bytes; the handshake register is kept from before the second one is read: its CRC error bit (1) covers all bytes up to and including that byte (SWIM Chip User's Reference) |
| **`SONY_MFM_CHECKCRC_1`** | — | — | `res_drvr_sony_fdhd.s:3514` | CheckCRC -- read the two CRC bytes; the handshake register is kept from before the second one is read: its CRC error bit (1) covers all bytes up to and including that byte (SWIM Chip User's Reference) |
| **`SONY_MFM_CHECKCRC_2`** | — | — | `res_drvr_sony_fdhd.s:3520` | — |
| **`SONY_MFM_READEXIT`** | — | — | `res_drvr_sony_fdhd.s:3531` | Branch from: SONY_MRDADDR_WAIT, SONY_MRDDATA_WAIT, SONY_MFM_CHECKCRC_2, SONY_MFM_READTOERR, SONY_MFM_VERIFYERR |
| **`SONY_MFM_READTOERR`** | — | — | `res_drvr_sony_fdhd.s:3536` | — |
| **`SONY_MFM_VERIFYERR`** | — | — | `res_drvr_sony_fdhd.s:3539` | — |
| **`Sony_MFMStatus`** | — | — | `res_drvr_sony_fdhd.s:868` | MFMStatus (csCode 10) -- return MFM related drive/disk/controller info (the "MFM Drive, MFM Disk, MFM Format, Disk Controller" bytes of the IOP SWIM Driver ERS, DriveStatus $12-$15) CSParam+0 -- $FF =... |
| **`Sony_mFmtTrack`** | — | — | `res_drvr_sony_fdhd.s:3656` | mFmtTrack -- format both sides of the current MFM track (called by CtlFormat in the tail through SONY_DRVENT_MFMTTRACK) D0 (out) -- 0 or error code Before side 1 it waits 750 us so the drive accepts t... |
| **`SONY_MFMTTRACK_DELAY`** | — | — | `res_drvr_sony_fdhd.s:3669` | — |
| **`SONY_MFMTTRACK_DOIT`** | — | — | `res_drvr_sony_fdhd.s:3677` | — |
| **`SONY_MFMTTRACK_EXIT`** | — | — | `res_drvr_sony_fdhd.s:3687` | — |
| **`SONY_MFMTTRACK_FMT`** | — | — | `res_drvr_sony_fdhd.s:3671` | — |
| **`Sony_mGetTrack`** | — | — | `res_drvr_sony_fdhd.s:3307` | mGetTrack -- GetTrack for MFM disks: 9 (720K) or 18 (1440K) sectors per side on all 80 tracks, sectors numbered from 1 D0 (in)  -- block number D0 (out) -- first sector wanted - 1, D2 = -1, D3 = secto... |
| **`SONY_MGETTRACK_CHK`** | — | — | `res_drvr_sony_fdhd.s:3315` | — |
| **`Sony_mPulse`** | — | — | `res_drvr_sony_fdhd.s:3225` | mPulse -- pulse LSTRB (PHASE3) through the phase register, keeping CA0-CA2: the drive executes the command at the selected address |
| **`Sony_mRdAddr`** | — | — | `res_drvr_sony_fdhd.s:3348` | mRdAddr -- read the next MFM address field (through the jMRdAddr vector) A5/A6 (in)  -- VIA port A / SCC data pointers (SetUpPoll) D0 (out)    -- 0, noAdrMkErr (-67), badCkSmErr (-69: CRC) or noNybErr... |
| **`SONY_MRDADDR_CYL`** | — | — | `res_drvr_sony_fdhd.s:3386` | — |
| **`SONY_MRDADDR_MARK`** | — | — | `res_drvr_sony_fdhd.s:3364` | — |
| **`SONY_MRDADDR_POLL`** | — | — | `res_drvr_sony_fdhd.s:3373` | — |
| **`SONY_MRDADDR_SECT`** | — | — | `res_drvr_sony_fdhd.s:3402` | — |
| **`SONY_MRDADDR_SECTW`** | — | — | `res_drvr_sony_fdhd.s:3405` | — |
| **`SONY_MRDADDR_SIDE`** | — | — | `res_drvr_sony_fdhd.s:3395` | — |
| **`SONY_MRDADDR_SIZE`** | — | — | `res_drvr_sony_fdhd.s:3414` | — |
| **`SONY_MRDADDR_SIZEW`** | — | — | `res_drvr_sony_fdhd.s:3417` | — |
| **`SONY_MRDADDR_TIMEOUT`** | — | — | `res_drvr_sony_fdhd.s:3425` | — |
| **`SONY_MRDADDR_WAIT`** | — | — | `res_drvr_sony_fdhd.s:3377` | — |
| **`Sony_mRdData`** | — | — | `res_drvr_sony_fdhd.s:3441` | mRdData -- read (or, with DskVerify set, compare) the data field that follows the address field just read (through the jMRdData vector) A0 (in) -- data buffer (512 bytes), A3/A4 (in) -- from mRdAddr D... |
| **`SONY_MRDDATA_BLK`** | — | — | `res_drvr_sony_fdhd.s:3473` | — |
| **`SONY_MRDDATA_BLKW`** | — | — | `res_drvr_sony_fdhd.s:3480` | — |
| **`SONY_MRDDATA_BYTE`** | — | — | `res_drvr_sony_fdhd.s:3484` | — |
| **`SONY_MRDDATA_CRC`** | — | — | `res_drvr_sony_fdhd.s:3506` | — |
| **`SONY_MRDDATA_MARK`** | — | — | `res_drvr_sony_fdhd.s:3458` | — |
| **`SONY_MRDDATA_TIMEOUT`** | — | — | `res_drvr_sony_fdhd.s:3488` | — |
| **`SONY_MRDDATA_VFY`** | — | — | `res_drvr_sony_fdhd.s:3490` | — |
| **`SONY_MRDDATA_VFYBYTE`** | — | — | `res_drvr_sony_fdhd.s:3501` | — |
| **`SONY_MRDDATA_VFYW`** | — | — | `res_drvr_sony_fdhd.s:3497` | — |
| **`SONY_MRDDATA_WAIT`** | — | — | `res_drvr_sony_fdhd.s:3462` | — |
| **`Sony_mSense`** | — | — | `res_drvr_sony_fdhd.s:3218` | mSense -- sense line with the ISM registers selected (rHandshake bit 3) D0 (out) -- $FF/$00 = sense line (BMI = 1) |
| **`Sony_mVerTrack`** | — | — | `res_drvr_sony_fdhd.s:3974` | mVerTrack -- verify both sides of the current MFM track: read every sector (allowing four revolutions) and check that track and side match D6 (in) -- track, A1/D1 (in) -- SonyVars / drive vars D0 (out... |
| **`SONY_MVERTRACK_EXIT`** | — | — | `res_drvr_sony_fdhd.s:4008` | — |
| **`SONY_MVERTRACK_LOOP`** | — | — | `res_drvr_sony_fdhd.s:3985` | — |
| **`SONY_MVERTRACK_NEXT`** | — | — | `res_drvr_sony_fdhd.s:3998` | — |
| **`SONY_MVERTRACK_NEXTSIDE`** | — | — | `res_drvr_sony_fdhd.s:4005` | — |
| **`SONY_MVERTRACK_SIDE`** | — | — | `res_drvr_sony_fdhd.s:3978` | — |
| **`Sony_mWrData`** | — | — | `res_drvr_sony_fdhd.s:3560` | mWrData -- write the data field of the sector whose address field was just read (through the jMWrData vector): after a timed delay (the write splice, so that the data field starts about 22 bytes after... |
| **`SONY_MWRDATA_CRC`** | — | — | `res_drvr_sony_fdhd.s:3626` | — |
| **`SONY_MWRDATA_DATA`** | — | — | `res_drvr_sony_fdhd.s:3617` | — |
| **`SONY_MWRDATA_DATAW`** | — | — | `res_drvr_sony_fdhd.s:3621` | — |
| **`SONY_MWRDATA_DELAY`** | — | — | `res_drvr_sony_fdhd.s:3580` | — |
| **`SONY_MWRDATA_EXIT`** | — | — | `res_drvr_sony_fdhd.s:3644` | — |
| **`SONY_MWRDATA_GAP`** | — | — | `res_drvr_sony_fdhd.s:3631` | — |
| **`SONY_MWRDATA_GAPW`** | — | — | `res_drvr_sony_fdhd.s:3635` | — |
| **`SONY_MWRDATA_LASTMARK`** | — | — | `res_drvr_sony_fdhd.s:3612` | — |
| **`SONY_MWRDATA_MARK`** | — | — | `res_drvr_sony_fdhd.s:3603` | — |
| **`SONY_MWRDATA_MARKW`** | — | — | `res_drvr_sony_fdhd.s:3607` | — |
| **`SONY_MWRDATA_SYNC`** | — | — | `res_drvr_sony_fdhd.s:3587` | — |
| **`SONY_MWRDATA_SYNCLOOP`** | — | — | `res_drvr_sony_fdhd.s:3593` | — |
| **`SONY_MWRDATA_SYNCW`** | — | — | `res_drvr_sony_fdhd.s:3597` | — |
| **`SONY_NEWDRVEJECT`** | `0x017FFC` | `0x034976` | `res_drvr_sony.s:469`<br>`res_drvr_sony_fdhd.s:679` | NewDrvEject -- an 800K drive only needs a short LSTRB pulse, but its enable must stay asserted until 150 us after the disk has left the drive (Apple: "new drive needs /enb asserted until 150usec after... |
| **`SONY_NEWDRVEJECT_IWM`** | — | — | `res_drvr_sony_fdhd.s:684` | — |
| **`SONY_NEWDRVEJECT_LOOP`** | `0x018002` | `0x03497C` | `res_drvr_sony.s:472`<br>`res_drvr_sony_fdhd.s:688` | — |
| **`SONY_NEWDRVEJECT_WAIT`** | — | — | `res_drvr_sony_fdhd.s:686` | — |
| **`SONY_NXTCLASS`** | — | `0x034AE4` | `res_drvr_sony_fdhd.s:1025` | find the speed zone of the block (zones of 16 tracks, 12..8 sectors) |
| **`SONY_ONTRACK`** | — | `0x034CF0` | `res_drvr_sony_fdhd.s:1283` | OnTrack -- DiskPrime part IV: read each address mark passing under the head; read or write the sector when it is wanted, optionally read other sectors of the track into the track cache. current file b... |
| **`SONY_ONTRACK1`** | — | `0x034CF6` | `res_drvr_sony_fdhd.s:1285` | OnTrack -- DiskPrime part IV: read each address mark passing under the head; read or write the sector when it is wanted, optionally read other sectors of the track into the track cache. current file b... |
| **`SONY_ONTRACK_CACHEDONE`** | — | `0x034D82` | `res_drvr_sony_fdhd.s:1338` | not wanted: read it into the track cache if caching this track |
| **`SONY_OPEN_XLATINIT`** | — | `0x034716` | `res_drvr_sony_fdhd.s:323` | — |
| **`SONY_OTREAD`** | — | `0x034E00` | `res_drvr_sony_fdhd.s:1394` | OTRead -- read the sector |
| **`SONY_OTSETUP`** | — | `0x034DA8` | `res_drvr_sony_fdhd.s:1357` | OTSetUp -- a wanted sector: compute buffer and tag positions |
| **`Sony_PassportSts`** | — | — | `res_drvr_sony_fdhd.s:782` | PassportSts (csCode 6) -- return the list of possible disk formats CSParam+0 (in/out) -- number of entries wanted / returned CSParam+2 (in)     -- pointer to the caller's table (8 bytes per entry) Flo... |
| **`SONY_PASSPORTSTS_CHK`** | — | — | `res_drvr_sony_fdhd.s:789` | — |
| **`SONY_PASSPORTSTS_COUNT`** | — | — | `res_drvr_sony_fdhd.s:820` | — |
| **`SONY_PASSPORTSTS_EXIT`** | — | — | `res_drvr_sony_fdhd.s:841` | — |
| **`SONY_PASSPORTSTS_FLOPPY`** | — | — | `res_drvr_sony_fdhd.s:800` | — |
| **`SONY_PASSPORTSTS_LOOP`** | — | — | `res_drvr_sony_fdhd.s:830` | — |
| **`SONY_PASSPORTSTS_OK`** | — | — | `res_drvr_sony_fdhd.s:839` | — |
| **`SONY_PASSPORTSTS_PUT`** | — | — | `res_drvr_sony_fdhd.s:836` | — |
| **`SONY_PASSPORTSTS_STORE`** | — | — | `res_drvr_sony_fdhd.s:824` | — |
| **`SONY_POFFEXIT`** | — | `0x034AA0` | `res_drvr_sony_fdhd.s:985` | — |
| **`Sony_PowerDown`** | `0x0188E8` | `0x0352BA` | `res_drvr_sony.s:1643`<br>`res_drvr_sony_fdhd.s:2107` | PowerDown -- power-down after D0 VBL task calls (TimeOut, 0.5 s each; the VBL task does it), or at once if D0 = 0: motor off control (MtrOffAdr) and the drive enable cut (mtrOff) |
| **`SONY_POWERDOWN_NOW`** | `0x0188FA` | `0x0352CC` | `res_drvr_sony.s:1651`<br>`res_drvr_sony_fdhd.s:2114` | power down now |
| **`Sony_PowerUp`** | `0x01890E` | `0x0352F0` | `res_drvr_sony.s:1669`<br>`res_drvr_sony_fdhd.s:2151` | PowerUp -- select the drive, motor on unless already on, then wait: old drive D0 * 100 us, new drive 75 ms and then until /READY (waitReady) |
| **`SONY_POWERUP_EXIT`** | `0x018928` | `0x03530A` | `res_drvr_sony.s:1681`<br>`res_drvr_sony_fdhd.s:2183` | motor already on |
| **`SONY_POWERUP_MTRCHK`** | — | — | `res_drvr_sony_fdhd.s:2167` | — |
| **`SONY_POWERUP_SETMODE`** | — | — | `res_drvr_sony_fdhd.s:2163` | — |
| **`Sony_Pulse`** | `0x01861A` | `0x034FE0` | `res_drvr_sony.s:1219`<br>`res_drvr_sony_fdhd.s:1661` | AdrAndStrb / Pulse -- pulse LSTRB (phase line PH3) to perform a drive control function: the drive takes CA2 as the value for the control register addressed by CA1, CA0 and SEL D0 (in) -- control regis... |
| **`SONY_PULSE_IWM`** | — | — | `res_drvr_sony_fdhd.s:1664` | — |
| **`SONY_RC_CONT`** | — | `0x034C26` | `res_drvr_sony_fdhd.s:1171` | SONY_RC_CONT -- not all sectors satisfied from cache: do disk I/O |
| **`SONY_RC_LOOP`** | — | `0x034BB8` | `res_drvr_sony_fdhd.s:1127` | — |
| **`SONY_RCVPKT_BYTE5`** | `0x01991E` | `0x0367FC` | `res_drvr_sony.s:3794`<br>`res_drvr_sony_fdhd.s:4469` | — |
| **`SONY_RCVPKT_BYTE6`** | `0x019938` | `0x036816` | `res_drvr_sony.s:3808`<br>`res_drvr_sony_fdhd.s:4483` | — |
| **`SONY_RCVPKT_DECODE`** | `0x0198BC` | `0x03679A` | `res_drvr_sony.s:3744`<br>`res_drvr_sony_fdhd.s:4419` | DECODE -- decode a full group (to A1) while reading the next one |
| **`SONY_RCVPKT_EXIT`** | `0x019A0E` | `0x0368EC` | `res_drvr_sony.s:3922`<br>`res_drvr_sony_fdhd.s:4591` | exit: SCC register pointer back to 0, CA1 high, CA0 low |
| **`SONY_RCVPKT_GET1`** | `0x019856` | `0x036734` | `res_drvr_sony.s:3691`<br>`res_drvr_sony_fdhd.s:4369` | the first group: D1 = bytes 1/2 (low/high word), D2 = 3/4, D3 = 5/6, D4 = byte 7 (high word) and the bit-0 byte (low word) |
| **`SONY_RCVPKT_GET2`** | `0x01986A` | `0x036748` | `res_drvr_sony.s:3701`<br>`res_drvr_sony_fdhd.s:4379` | — |
| **`SONY_RCVPKT_GET3`** | `0x019874` | `0x036752` | `res_drvr_sony.s:3706`<br>`res_drvr_sony_fdhd.s:4384` | — |
| **`SONY_RCVPKT_GET4`** | `0x01987E` | `0x03675C` | `res_drvr_sony.s:3711`<br>`res_drvr_sony_fdhd.s:4389` | — |
| **`SONY_RCVPKT_GET5`** | `0x019888` | `0x036766` | `res_drvr_sony.s:3716`<br>`res_drvr_sony_fdhd.s:4394` | — |
| **`SONY_RCVPKT_GET6`** | `0x019892` | `0x036770` | `res_drvr_sony.s:3721`<br>`res_drvr_sony_fdhd.s:4399` | — |
| **`SONY_RCVPKT_GET7`** | `0x01989C` | `0x03677A` | `res_drvr_sony.s:3726`<br>`res_drvr_sony_fdhd.s:4404` | — |
| **`SONY_RCVPKT_GET8`** | `0x0198A6` | `0x036784` | `res_drvr_sony.s:3731`<br>`res_drvr_sony_fdhd.s:4409` | — |
| **`SONY_RCVPKT_GROUP`** | `0x0198C4` | `0x0367A2` | `res_drvr_sony.s:3748`<br>`res_drvr_sony_fdhd.s:4423` | — |
| **`SONY_RCVPKT_GROUPTO`** | `0x0198B6` | `0x036794` | `res_drvr_sony.s:3739`<br>`res_drvr_sony_fdhd.s:4416` | RdGroupTO -- a byte did not come |
| **`SONY_RCVPKT_GROUPTO2`** | `0x01992C` | `0x03680A` | `res_drvr_sony.s:3802`<br>`res_drvr_sony_fdhd.s:4477` | — |
| **`SONY_RCVPKT_HOFFTO`** | `0x01999C` | `0x03687A` | `res_drvr_sony.s:3856`<br>`res_drvr_sony_fdhd.s:4528` | RdHoffSyncTO -- no $AA after a hold-off |
| **`SONY_RCVPKT_HOLDCHK`** | `0x0198F2` | `0x0367D0` | `res_drvr_sony.s:3771`<br>`res_drvr_sony_fdhd.s:4446` | — |
| **`SONY_RCVPKT_HOLDDELAY`** | `0x01997E` | — | `res_drvr_sony.s:3841` | — |
| **`SONY_RCVPKT_LAST`** | `0x0199A0` | `0x03687E` | `res_drvr_sony.s:3862`<br>`res_drvr_sony_fdhd.s:4531` | LAST -- the last group: store its data bytes (D7.hi of them), add its 7th byte (the checksum) to the sum; then HSHK must be high again |
| **`SONY_RCVPKT_LAST2`** | `0x0199AE` | `0x03688C` | `res_drvr_sony.s:3870`<br>`res_drvr_sony_fdhd.s:4539` | — |
| **`SONY_RCVPKT_LAST3`** | `0x0199BC` | `0x03689A` | `res_drvr_sony.s:3878`<br>`res_drvr_sony_fdhd.s:4547` | — |
| **`SONY_RCVPKT_LAST4`** | `0x0199C8` | `0x0368A6` | `res_drvr_sony.s:3885`<br>`res_drvr_sony_fdhd.s:4554` | — |
| **`SONY_RCVPKT_LAST5`** | `0x0199D6` | `0x0368B4` | `res_drvr_sony.s:3893`<br>`res_drvr_sony_fdhd.s:4562` | — |
| **`SONY_RCVPKT_LAST6`** | `0x0199E2` | `0x0368C0` | `res_drvr_sony.s:3900`<br>`res_drvr_sony_fdhd.s:4569` | — |
| **`SONY_RCVPKT_LAST7`** | `0x0199F0` | `0x0368CE` | `res_drvr_sony.s:3908`<br>`res_drvr_sony_fdhd.s:4577` | — |
| **`SONY_RCVPKT_NEXT1`** | `0x0198CC` | `0x0367AA` | `res_drvr_sony.s:3753`<br>`res_drvr_sony_fdhd.s:4428` | — |
| **`SONY_RCVPKT_NEXT2`** | `0x0198E2` | `0x0367C0` | `res_drvr_sony.s:3763`<br>`res_drvr_sony_fdhd.s:4438` | — |
| **`SONY_RCVPKT_NEXT3`** | `0x0198FC` | `0x0367DA` | `res_drvr_sony.s:3777`<br>`res_drvr_sony_fdhd.s:4452` | — |
| **`SONY_RCVPKT_NEXT4`** | `0x01990E` | `0x0367EC` | `res_drvr_sony.s:3786`<br>`res_drvr_sony_fdhd.s:4461` | — |
| **`SONY_RCVPKT_NEXT5`** | `0x019926` | `0x036804` | `res_drvr_sony.s:3799`<br>`res_drvr_sony_fdhd.s:4474` | — |
| **`SONY_RCVPKT_NEXT6`** | `0x019942` | `0x036820` | `res_drvr_sony.s:3814`<br>`res_drvr_sony_fdhd.s:4489` | — |
| **`SONY_RCVPKT_NEXT7`** | `0x019956` | `0x036834` | `res_drvr_sony.s:3824`<br>`res_drvr_sony_fdhd.s:4499` | — |
| **`SONY_RCVPKT_NEXT8`** | `0x019964` | `0x036842` | `res_drvr_sony.s:3830`<br>`res_drvr_sony_fdhd.s:4505` | — |
| **`SONY_RCVPKT_NOTSHORT`** | `0x019868` | `0x036746` | `res_drvr_sony.s:3699`<br>`res_drvr_sony_fdhd.s:4377` | — |
| **`SONY_RCVPKT_RESYNC`** | `0x01998E` | `0x03686C` | `res_drvr_sony.s:3848`<br>`res_drvr_sony_fdhd.s:4522` | after a hold-off: wait for $AA again |
| **`SONY_RCVPKT_SYNC`** | `0x019846` | `0x036724` | `res_drvr_sony.s:3683`<br>`res_drvr_sony_fdhd.s:4363` | wait for the sync byte $AA |
| **`Sony_RdAddr`** | `0x018C22` | `0x035B04` | `res_drvr_sony.s:2124`<br>`res_drvr_sony.s:2775` | jtRdAddr -- read the next address field that passes the head A2 (in)  -- AdrMks; A5/A6 (in) -- VIA port A / SCC data (SetUpPoll) D0 (out) -- MustFindCt minus the nibbles read before the mark (>= 0), o... |
| **`SONY_RDADDR_CONT`** | `0x018C38` | `0x035B1C` | `res_drvr_sony.s:2135`<br>`res_drvr_sony.s:2787` | — |
| **`SONY_RDADDR_CONT_2`** | `0x018C58` | `0x035B3C` | `res_drvr_sony.s:2149`<br>`res_drvr_sony.s:2800` | — |
| **`SONY_RDADDR_CONT_3`** | `0x018C5C` | `0x035B40` | `res_drvr_sony.s:2152`<br>`res_drvr_sony.s:2802` | look for the address mark $D5 $AA $96 |
| **`SONY_RDADDR_CONT_4`** | `0x018C7A` | `0x035B5E` | `res_drvr_sony.s:2172`<br>`res_drvr_sony.s:2820` | the five address field nibbles, each a 6-bit value; checksum = XOR |
| **`SONY_RDADDR_CONT_5`** | `0x018C86` | `0x035B6A` | `res_drvr_sony.s:2178`<br>`res_drvr_sony.s:2826` | — |
| **`SONY_RDADDR_CONT_6`** | `0x018C90` | `0x035B74` | `res_drvr_sony.s:2183`<br>`res_drvr_sony.s:2831` | — |
| **`SONY_RDADDR_CONT_7`** | `0x018CAC` | `0x035B90` | `res_drvr_sony.s:2197`<br>`res_drvr_sony.s:2845` | — |
| **`SONY_RDADDR_ERR`** | `0x018CCC` | — | `res_drvr_sony.s:2214` | — |
| **`SONY_RDADDR_ERR_2`** | `0x018CD0` | `0x035BB4` | `res_drvr_sony.s:2217`<br>`res_drvr_sony.s:2865` | Branch from: SONY_RDADDR_CONT, SONY_RDADDR_SKIP_2, SONY_RDADDR_ERR_2, SONY_RDADDR_ERR_3, SONY_RDDATA_SKIP |
| **`SONY_RDADDR_ERR_3`** | `0x018CD4` | `0x035BB8` | `res_drvr_sony.s:2221`<br>`res_drvr_sony.s:2868` | — |
| **`SONY_RDADDR_LOOP`** | `0x018C44` | `0x035B28` | `res_drvr_sony.s:2141`<br>`res_drvr_sony.s:2792` | — |
| **`SONY_RDADDR_LOOP_2`** | `0x018C72` | `0x035B56` | `res_drvr_sony.s:2166`<br>`res_drvr_sony.s:2815` | — |
| **`SONY_RDADDR_LOOP_3`** | `0x018CBA` | `0x035B9E` | `res_drvr_sony.s:2204`<br>`res_drvr_sony.s:2852` | — |
| **`SONY_RDADDR_NEXT`** | `0x018C60` | `0x035B44` | `res_drvr_sony.s:2155`<br>`res_drvr_sony.s:2805` | — |
| **`SONY_RDADDR_SKIP`** | `0x018C32` | `0x035B16` | `res_drvr_sony.s:2131`<br>`res_drvr_sony.s:2783` | any nibbles at all (a blank track gives none)? |
| **`SONY_RDADDR_SKIP_2`** | `0x018C6A` | `0x035B4E` | `res_drvr_sony.s:2161`<br>`res_drvr_sony.s:2811` | — |
| **`SONY_RDADDR_SKIP_3`** | `0x018CA2` | `0x035B86` | `res_drvr_sony.s:2192`<br>`res_drvr_sony.s:2840` | — |
| **`SONY_RDADDR_SKIP_4`** | `0x018CC4` | `0x035BA8` | `res_drvr_sony.s:2210`<br>`res_drvr_sony.s:2858` | — |
| **`Sony_RdAddrSetup`** | `0x018C04` | `0x035AE6` | `res_drvr_sony.s:2098`<br>`res_drvr_sony.s:2742` | RdAddrSetup -- set up polling, address the read data of the head for the side in SideTrack, then RdAddr: D1 = side/track, D2 = sector, D3 = format byte of the next address field |
| **`SONY_RDADDRSETUP_SIDE`** | `0x018C14` | `0x035AF6` | `res_drvr_sony.s:2105`<br>`res_drvr_sony.s:2749` | — |
| **`SONY_RDCACHENV`** | — | `0x034C2A` | `res_drvr_sony_fdhd.s:1175` | rdCacheNV -- cache not valid: start caching this track if possible |
| **`Sony_RdData`** | `0x018CE8` | `0x035BCC` | `res_drvr_sony.s:2247`<br>`res_drvr_sony.s:2900` | jtRdData -- read the data field after the address field just read: the sector number to TagData+1, the 12 tag bytes to TagData+2, the 512 data bytes to (A0); with DskVerify set, compare the data with ... |
| **`SONY_RDDATA_CONT`** | `0x018CFE` | `0x035BE2` | `res_drvr_sony.s:2256`<br>`res_drvr_sony.s:2909` | — |
| **`SONY_RDDATA_CONT_10`** | `0x018E5E` | `0x035D42` | `res_drvr_sony.s:2447`<br>`res_drvr_sony.s:3091` | — |
| **`SONY_RDDATA_CONT_11`** | `0x018E74` | `0x035D58` | `res_drvr_sony.s:2458`<br>`res_drvr_sony.s:3102` | — |
| **`SONY_RDDATA_CONT_12`** | `0x018EA6` | `0x035D8A` | `res_drvr_sony.s:2488`<br>`res_drvr_sony.s:3130` | RdSlip -- the slip marks $DE $AA |
| **`SONY_RDDATA_CONT_13`** | `0x018EBC` | `0x035DA0` | `res_drvr_sony.s:2501`<br>`res_drvr_sony.s:3143` | — |
| **`SONY_RDDATA_CONT_2`** | `0x018D1C` | `0x035C00` | `res_drvr_sony.s:2275`<br>`res_drvr_sony.s:2927` | — |
| **`SONY_RDDATA_CONT_3`** | `0x018D28` | `0x035C0C` | `res_drvr_sony.s:2282`<br>`res_drvr_sony.s:2932` | groups of three bytes: first the 12 tag bytes (to TagData+2), then the data (RdData3 below) |
| **`SONY_RDDATA_CONT_4`** | `0x018D3C` | `0x035C20` | `res_drvr_sony.s:2293`<br>`res_drvr_sony.s:2943` | — |
| **`SONY_RDDATA_CONT_5`** | `0x018D56` | `0x035C3A` | `res_drvr_sony.s:2306`<br>`res_drvr_sony.s:2956` | — |
| **`SONY_RDDATA_CONT_6`** | `0x018D9E` | `0x035C82` | `res_drvr_sony.s:2344`<br>`res_drvr_sony.s:2992` | — |
| **`SONY_RDDATA_CONT_7`** | `0x018DB8` | `0x035C9C` | `res_drvr_sony.s:2357`<br>`res_drvr_sony.s:3005` | — |
| **`SONY_RDDATA_CONT_8`** | `0x018DFA` | `0x035CDE` | `res_drvr_sony.s:2393`<br>`res_drvr_sony.s:3039` | — |
| **`SONY_RDDATA_CONT_9`** | `0x018E16` | `0x035CFA` | `res_drvr_sony.s:2407`<br>`res_drvr_sony.s:3053` | — |
| **`SONY_RDDATA_DONE`** | `0x018E48` | `0x035D2C` | `res_drvr_sony.s:2435`<br>`res_drvr_sony.s:3079` | RdCkSum -- the four checksum nibbles (each checked for an invalid nibble) |
| **`SONY_RDDATA_ERR`** | `0x018E40` | `0x035D24` | `res_drvr_sony.s:2428`<br>`res_drvr_sony.s:3074` | — |
| **`SONY_RDDATA_ERR_2`** | `0x018E9E` | `0x035D82` | `res_drvr_sony.s:2479`<br>`res_drvr_sony.s:3124` | Branch from: SONY_RDDATA_SKIP_8, SONY_RDDATA_CONT_10, SONY_RDDATA_CONT_11, SONY_RDDATA_SKIP_9 |
| **`SONY_RDDATA_ERR_3`** | `0x018EA2` | `0x035D86` | `res_drvr_sony.s:2483`<br>`res_drvr_sony.s:3127` | — |
| **`SONY_RDDATA_ERR_4`** | `0x018EC0` | `0x035DA4` | `res_drvr_sony.s:2504`<br>`res_drvr_sony.s:3145` | — |
| **`SONY_RDDATA_LOOP`** | `0x018D02` | `0x035BE6` | `res_drvr_sony.s:2259`<br>`res_drvr_sony.s:2912` | — |
| **`SONY_RDDATA_LOOP_2`** | `0x018D14` | `0x035BF8` | `res_drvr_sony.s:2270`<br>`res_drvr_sony.s:2922` | — |
| **`SONY_RDDATA_LOOP_3`** | `0x018D8A` | `0x035C6E` | `res_drvr_sony.s:2333`<br>`res_drvr_sony.s:2981` | RdData3 -- the 512 data bytes to (A0); the last group has only A and B |
| **`SONY_RDDATA_LOOP_4`** | `0x018DE6` | `0x035CCA` | `res_drvr_sony.s:2382`<br>`res_drvr_sony.s:3028` | RdVer1 -- read-verify: compare the decoded data with (A0) |
| **`SONY_RDDATA_LOOP_5`** | `0x018EA8` | `0x035D8C` | `res_drvr_sony.s:2490`<br>`res_drvr_sony.s:3132` | — |
| **`SONY_RDDATA_SKIP`** | `0x018D0C` | `0x035BF0` | `res_drvr_sony.s:2265`<br>`res_drvr_sony.s:2918` | — |
| **`SONY_RDDATA_SKIP_10`** | `0x018EB2` | `0x035D96` | `res_drvr_sony.s:2496`<br>`res_drvr_sony.s:3138` | — |
| **`SONY_RDDATA_SKIP_2`** | `0x018D2E` | `0x035C12` | `res_drvr_sony.s:2286`<br>`res_drvr_sony.s:2936` | — |
| **`SONY_RDDATA_SKIP_3`** | `0x018D6E` | `0x035C52` | `res_drvr_sony.s:2318`<br>`res_drvr_sony.s:2968` | — |
| **`SONY_RDDATA_SKIP_4`** | `0x018D90` | `0x035C74` | `res_drvr_sony.s:2337`<br>`res_drvr_sony.s:2985` | — |
| **`SONY_RDDATA_SKIP_5`** | `0x018DD4` | `0x035CB8` | `res_drvr_sony.s:2371`<br>`res_drvr_sony.s:3019` | — |
| **`SONY_RDDATA_SKIP_6`** | `0x018DEC` | `0x035CD0` | `res_drvr_sony.s:2386`<br>`res_drvr_sony.s:3032` | — |
| **`SONY_RDDATA_SKIP_7`** | `0x018E34` | `0x035D18` | `res_drvr_sony.s:2422`<br>`res_drvr_sony.s:3068` | — |
| **`SONY_RDDATA_SKIP_8`** | `0x018E4E` | `0x035D32` | `res_drvr_sony.s:2439`<br>`res_drvr_sony.s:3083` | — |
| **`SONY_RDDATA_SKIP_9`** | `0x018E8E` | `0x035D72` | `res_drvr_sony.s:2471`<br>`res_drvr_sony.s:3115` | — |
| **`SONY_READCACHE`** | — | `0x034B92` | `res_drvr_sony_fdhd.s:1109` | readCache -- take the sectors that are in the cache |
| **`Sony_Recal`** | `0x018858` | `0x03521A` | `res_drvr_sony.s:1566`<br>`res_drvr_sony_fdhd.s:2017` | jtRecal -- set the IWM mode if needed (Apple later split this out as SetIWMMode), power up, step out to track 0. Track = 0 or the error. Returns one level above the caller while waiting (A5 = return a... |
| **`SONY_RECAL_CONT`** | `0x0188AA` | `0x03522A` | `res_drvr_sony.s:1606`<br>`res_drvr_sony_fdhd.s:2028` | SlowLoop -- one step per SeekTime (half of it for new-interface drives) |
| **`SONY_RECAL_CONT_2`** | `0x0188B6` | `0x035236` | `res_drvr_sony.s:1611`<br>`res_drvr_sony_fdhd.s:2033` | — |
| **`SONY_RECAL_DONE`** | `0x0188DC` | `0x03525C` | `res_drvr_sony.s:1628`<br>`res_drvr_sony_fdhd.s:2050` | at track 0 |
| **`SONY_RECAL_ERR`** | `0x0188E0` | — | `res_drvr_sony.s:1632` | — |
| **`SONY_RECAL_ERR_2`** | `0x0188E2` | `0x035262` | `res_drvr_sony.s:1634`<br>`res_drvr_sony_fdhd.s:2052` | RecalFail -- the drive cannot step and is not at track 0 |
| **`SONY_RECAL_OK`** | `0x0188A2` | — | `res_drvr_sony.s:1600` | mode set: back to read mode, power the drive up again |
| **`SONY_RECAL_RETRY`** | `0x018878` | — | `res_drvr_sony.s:1582` | SetIWMMode: the mode register is written with Motor-On = 0 and read back in the status register; give up after about a second (the timeout exit stores initIWMErr with D1 = $1F as drive offset: odd add... |
| **`SONY_RECAL_SKIP`** | `0x0188A8` | `0x035228` | `res_drvr_sony.s:1604`<br>`res_drvr_sony.s:1742` | step out until /TK0, at most 80 steps (12 ms each, 6 ms for 800K drives) |
| **`SONY_RECALFAIL`** | — | `0x035260` | `res_drvr_sony_fdhd.s:2046` | RecalFail -- the drive cannot step and is not at track 0 |
| **`Sony_ReSeek`** | `0x0182E2` | `0x034C80` | `res_drvr_sony.s:836`<br>`res_drvr_sony_fdhd.s:1229` | jtReSeek -- seek to the track wanted (SideTrack); for a 400K drive check the zone's speed if CkDelta (4 min) has passed since the last check and correct the speed code by the 2% delta (at most BadSpdI... |
| **`SONY_RESEEK1`** | — | `0x034C86` | `res_drvr_sony_fdhd.s:1231` | jtReSeek -- DiskPrime part III: seek to SideTrack; for a drive without the new interface (400K), check the zone speed when CkDelta ticks have passed since the last check and, if the speed value of Get... |
| **`SONY_RESEEK_ADJUST`** | `0x018336` | `0x034CDA` | `res_drvr_sony.s:871`<br>`res_drvr_sony_fdhd.s:1265` | — |
| **`SONY_RESEEK_CACHEOFS`** | — | — | `res_drvr_sony_fdhd.s:1310` | not wanted: read it into the track cache if caching this track |
| **`SONY_RESEEK_CACHETAGS`** | — | — | `res_drvr_sony_fdhd.s:1328` | — |
| **`SONY_RESEEK_CONT`** | `0x018316` | `0x034CBA` | `res_drvr_sony.s:854`<br>`res_drvr_sony_fdhd.s:1249` | — |
| **`SONY_RESEEK_CONT_2`** | `0x018320` | `0x034CC4` | `res_drvr_sony.s:860`<br>`res_drvr_sony_fdhd.s:1254` | D4 = speed value (11.4 * rpm); compare with the zone's limits |
| **`SONY_RESEEK_CONT_4`** | `0x018406` | `0x034DA4` | `res_drvr_sony.s:945`<br>`res_drvr_sony_fdhd.s:1354` | — |
| **`SONY_RESEEK_CONT_5`** | `0x018458` | `0x034DF6` | `res_drvr_sony.s:982`<br>`res_drvr_sony_fdhd.s:1389` | — |
| **`SONY_RESEEK_CONT_6`** | `0x018462` | — | `res_drvr_sony.s:988` | OTRead -- read the data field, copy the tags to the separate buffer |
| **`SONY_RESEEK_CONT_7`** | `0x0184DE` | `0x034E7C` | `res_drvr_sony.s:1035`<br>`res_drvr_sony_fdhd.s:1447` | no wait: pass the poll data on and open interrupts |
| **`SONY_RESEEK_DONE`** | `0x0184E6` | `0x034E84` | `res_drvr_sony.s:1039`<br>`res_drvr_sony_fdhd.s:1451` | more sectors on this track, more tracks, or done |
| **`SONY_RESEEK_ERR`** | `0x01834E` | — | `res_drvr_sony.s:881` | — |
| **`SONY_RESEEK_ERR_2`** | `0x0183E4` | — | `res_drvr_sony.s:932` | not wanted: read it into the track cache if reads into the cache are enabled |
| **`SONY_RESEEK_ERR_3`** | `0x018500` | — | `res_drvr_sony.s:1049` | — |
| **`SONY_RESEEK_ERR_4`** | `0x01853A` | — | `res_drvr_sony.s:1087` | AdrDtaErr -- address or data field error: retry on this track (reads), recal (writes, they may be slightly off track) while recals are left |
| **`SONY_RESEEK_ERR_5`** | `0x01857E` | — | `res_drvr_sony.s:1116` | WrgSideTrk -- address field of another side or track |
| **`SONY_RESEEK_ERR_6`** | `0x018582` | — | `res_drvr_sony.s:1120` | DoRecal -- recal to track 0, remeasure the speeds and seek again |
| **`SONY_RESEEK_ERR_7`** | `0x01859A` | `0x034F38` | `res_drvr_sony.s:1128`<br>`res_drvr_sony_fdhd.s:1536` | — |
| **`SONY_RESEEK_NO`** | `0x018342` | `0x034CE0` | `res_drvr_sony.s:876`<br>`res_drvr_sony_fdhd.s:1268` | — |
| **`SONY_RESEEK_NO_2`** | `0x018450` | `0x034DEE` | `res_drvr_sony.s:979`<br>`res_drvr_sony_fdhd.s:1386` | OTWrite -- tags from the separate tag buffer, or the file block number no separate tag buffer: only the file block number is set |
| **`SONY_RESEEK_NO_3`** | `0x0184CC` | `0x034E6A` | `res_drvr_sony.s:1027`<br>`res_drvr_sony_fdhd.s:1436` | one sector time with interrupts open |
| **`SONY_RESEEK_OK_2`** | `0x01840A` | — | `res_drvr_sony.s:949` | OTSetUp -- a sector wanted: note the format, set up buffer and tags |
| **`SONY_RESEEK_POLLONLY`** | `0x0183FE` | `0x034D9C` | `res_drvr_sony.s:942`<br>`res_drvr_sony_fdhd.s:1351` | no AppleTalk request: pass the poll data on and open interrupts |
| **`SONY_RESEEK_RETRY`** | `0x0182E8` | — | `res_drvr_sony.s:838` | jtReSeek -- seek to the track wanted (SideTrack); for a 400K drive check the zone's speed if CkDelta (4 min) has passed since the last check and correct the speed code by the 2% delta (at most BadSpdI... |
| **`SONY_RESEEK_RETRY_2`** | `0x018358` | — | `res_drvr_sony.s:889` | OnTrack -- read the address fields passing by; read or write the sectors wanted, read the others into the track cache if enabled. RdAddr leaves interrupts off (IPL 3) and SCC bytes on the stack (poll ... |
| **`SONY_RESEEK_RETRY_3`** | `0x018552` | `0x034EF0` | `res_drvr_sony.s:1096`<br>`res_drvr_sony_fdhd.s:1503` | — |
| **`SONY_RESEEK_SKIP`** | `0x018352` | — | `res_drvr_sony.s:887` | OnTrack -- read the address fields passing by; read or write the sectors wanted, read the others into the track cache if enabled. RdAddr leaves interrupts off (IPL 3) and SCC bytes on the stack (poll ... |
| **`SONY_RESEEK_SKIP_2`** | `0x018484` | — | `res_drvr_sony.s:1001` | GotSect -- sector done: update the map, position and byte count |
| **`SONY_RESEEK_SKIP_3`** | `0x01855C` | — | `res_drvr_sony.s:1103` | WrgSectAdr -- not a sector we want: give one sector time back to the system (interrupts open) and look again |
| **`SONY_RESEEK_WAITSECT`** | — | — | `res_drvr_sony_fdhd.s:1345` | — |
| **`SONY_RESEEK_WAITSECT_2`** | — | — | `res_drvr_sony_fdhd.s:1441` | — |
| **`SONY_RESEEK_WAITSECT_3`** | — | — | `res_drvr_sony_fdhd.s:1514` | — |
| **`SONY_RESEEK_WRNEXT`** | — | — | `res_drvr_sony_fdhd.s:1432` | — |
| **`SONY_RWPOWER`** | — | `0x034AB2` | `res_drvr_sony_fdhd.s:995` | RWPower -- set the speed for the current track and wait until the drive is powered up |
| **`Sony_RWPowerUp`** | `0x01890A` | `0x0352EC` | `res_drvr_sony.s:1665`<br>`res_drvr_sony_fdhd.s:2149` | RWPowerUp -- power up and wait PwrOnTime (400 ms) |
| **`Sony_Seek`** | `0x018726` | `0x0350EC` | `res_drvr_sony.s:1381`<br>`res_drvr_sony_fdhd.s:1826` | jtSeek (JSeek vector): one step at a time, each with its direction set and the /STEP handshake checked; an unknown track (negative Track) means a recal first. |
| **`SONY_SEEK_CONT`** | `0x01873E` | `0x035104` | `res_drvr_sony.s:1395`<br>`res_drvr_sony.s:1574` | SeekLp -- set the direction for one step |
| **`SONY_SEEK_CONT_2`** | `0x01874E` | `0x035114` | `res_drvr_sony.s:1404`<br>`res_drvr_sony.s:1583` | — |
| **`SONY_SEEK_CONT_3`** | `0x018764` | `0x03512A` | `res_drvr_sony.s:1414`<br>`res_drvr_sony.s:1592` | — |
| **`SONY_SEEKEND`** | `0x01876C` | `0x035132` | `res_drvr_sony.s:1420`<br>`res_drvr_sony_fdhd.s:1859` | SeekEnd -- store the track; head settle time (400K) or /READY (800K) |
| **`SONY_SEEKEND1`** | `0x01877E` | `0x035144` | `res_drvr_sony.s:1427`<br>`res_drvr_sony_fdhd.s:1871` | SeekEnd1 -- wait out any speed change (Wait; /READY for 800K drives) |
| **`SONY_SEEKEND_SETTLE`** | — | — | `res_drvr_sony_fdhd.s:1867` | — |
| **`SONY_SEEKLP`** | — | `0x035100` | `res_drvr_sony_fdhd.s:1835` | current track unknown: recalibrate SeekLp -- the step loop: compare with the target track, then one step at a time |
| **`SONY_SEEKLP1`** | — | — | `res_drvr_sony_fdhd.s:1847` | — |
| **`SONY_SEEKLP_DIR`** | — | — | `res_drvr_sony_fdhd.s:1843` | — |
| **`Sony_SendCmd`** | `0x0196B2` | `0x036592` | `res_drvr_sony.s:3504`<br>`res_drvr_sony_fdhd.s:4205` | jtSendCmd (JSendCmd vector) -- send the command block (DCDSendPacket); for a write it carries the 20 tag bytes and 512 data bytes of the first block, the others follow from DCDRcvResponse (SONY_SENDCM... |
| **`SONY_SENDCMD_CHKSTATUS`** | `0x0197D4` | `0x0366B4` | `res_drvr_sony.s:3619`<br>`res_drvr_sony_fdhd.s:4312` | the HD20's status: bit 0 of the first byte (opFailed) or a first byte of $0A is an error (nonZerStat) |
| **`SONY_SENDCMD_CONT_11`** | — | `0x036A8C` | `res_drvr_sony_fdhd.s:4799` | — |
| **`SONY_SENDCMD_CONT_4`** | — | — | `res_drvr_sony_fdhd.s:4688` | — |
| **`SONY_SENDCMD_ERR`** | `0x0197FE` | `0x0366DC` | `res_drvr_sony.s:3637`<br>`res_drvr_sony_fdhd.s:4327` | comErr: LastStatus = error code (top byte) and context, LastResult |
| **`SONY_SENDCMD_ERR_2`** | `0x019802` | `0x0366E0` | `res_drvr_sony.s:3640`<br>`res_drvr_sony_fdhd.s:4330` | — |
| **`SONY_SENDCMD_EXIT`** | `0x019754` | `0x036634` | `res_drvr_sony.s:3564`<br>`res_drvr_sony_fdhd.s:4260` | — |
| **`SONY_SENDCMD_LOOP`** | `0x019730` | `0x036610` | `res_drvr_sony.s:3549`<br>`res_drvr_sony_fdhd.s:4245` | — |
| **`SONY_SENDCMD_LOOP_21`** | — | `0x03685C` | `res_drvr_sony_fdhd.s:4516` | — |
| **`SONY_SENDCMD_LOOP_22`** | — | `0x0369B4` | `res_drvr_sony_fdhd.s:4690` | — |
| **`SONY_SENDCMD_LOOP_25`** | — | `0x036AA2` | `res_drvr_sony_fdhd.s:4811` | — |
| **`SONY_SENDCMD_LOOP_26`** | — | `0x036ABA` | `res_drvr_sony_fdhd.s:4819` | — |
| **`SONY_SENDCMD_NEXT`** | `0x019712` | `0x0365F2` | `res_drvr_sony.s:3541`<br>`res_drvr_sony_fdhd.s:4237` | NEXT -- from DCDRcvResponse: write the next block (a read just waits) |
| **`SONY_SENDCMD_NO`** | `0x0196D6` | `0x0365B6` | `res_drvr_sony.s:3519`<br>`res_drvr_sony_fdhd.s:4217` | write: 20 tag bytes more to send; without a tag buffer they come from the system tag buffer (TagData) |
| **`SONY_SENDCMD_NO_2`** | `0x0197B8` | `0x036698` | `res_drvr_sony.s:3609`<br>`res_drvr_sony_fdhd.s:4304` | — |
| **`SONY_SENDCMD_OK`** | `0x01974C` | `0x03662C` | `res_drvr_sony.s:3561`<br>`res_drvr_sony_fdhd.s:4257` | — |
| **`SONY_SENDCMD_OK_2`** | `0x0197A2` | `0x036682` | `res_drvr_sony.s:3599`<br>`res_drvr_sony_fdhd.s:4294` | a read block: its tags to the tag buffer and the system tag buffer |
| **`SONY_SENDCMD_RET`** | `0x0197F6` | `0x0366D6` | `res_drvr_sony.s:3631`<br>`res_drvr_sony_fdhd.s:4324` | — |
| **`SONY_SENDCMD_SKIP`** | `0x0196FA` | `0x0365DA` | `res_drvr_sony.s:3530`<br>`res_drvr_sony_fdhd.s:4228` | — |
| **`SONY_SENDPKT_CKSUM`** | `0x019C2A` | `0x036B08` | `res_drvr_sony.s:4202`<br>`res_drvr_sony_fdhd.s:4863` | — |
| **`SONY_SENDPKT_COUNT1`** | `0x019AE8` | `0x0369C6` | `res_drvr_sony.s:4030`<br>`res_drvr_sony_fdhd.s:4695` | — |
| **`SONY_SENDPKT_COUNT2`** | `0x019AF0` | `0x0369CE` | `res_drvr_sony.s:4035`<br>`res_drvr_sony_fdhd.s:4700` | — |
| **`SONY_SENDPKT_DELAY`** | `0x019AD6` | — | `res_drvr_sony.s:4025` | — |
| **`SONY_SENDPKT_EXIT`** | `0x019C56` | `0x036B34` | `res_drvr_sony.s:4226`<br>`res_drvr_sony_fdhd.s:4886` | exit: CA1 high, CA0 low |
| **`SONY_SENDPKT_GROUP`** | `0x019AFC` | `0x0369DA` | `res_drvr_sony.s:4043`<br>`res_drvr_sony_fdhd.s:4708` | GROUP -- send a full group (bytes 1-6 in D1-D3), fetching the next one |
| **`SONY_SENDPKT_HOLD0`** | `0x019BB6` | `0x036A94` | `res_drvr_sony.s:4142`<br>`res_drvr_sony_fdhd.s:4805` | holdoff: let the SCC interrupt be serviced, then restart with $AA |
| **`SONY_SENDPKT_HOLDDELAY1`** | `0x019BC4` | — | `res_drvr_sony.s:4148` | — |
| **`SONY_SENDPKT_HOLDDELAY2`** | `0x019BDC` | — | `res_drvr_sony.s:4156` | — |
| **`SONY_SENDPKT_HOLDOFF`** | `0x019BB4` | `0x036A92` | `res_drvr_sony.s:4140`<br>`res_drvr_sony_fdhd.s:4803` | HOLDOFF -- a $00 byte, write state off, interrupts open briefly (the SCC is serviced), CA0 high, then the write state again with $AA |
| **`SONY_SENDPKT_LAST`** | `0x019BF0` | `0x036ACE` | `res_drvr_sony.s:4165`<br>`res_drvr_sony_fdhd.s:4826` | LAST -- the last group: bytes 1-6 (D1-D3), the checksum as byte 7, then two $00; wait for HSHK high (the HD20 has the packet) |
| **`SONY_SENDPKT_LPUT0`** | `0x019BFA` | `0x036AD8` | `res_drvr_sony.s:4171`<br>`res_drvr_sony_fdhd.s:4832` | — |
| **`SONY_SENDPKT_LPUT1`** | `0x019C00` | `0x036ADE` | `res_drvr_sony.s:4175`<br>`res_drvr_sony_fdhd.s:4836` | — |
| **`SONY_SENDPKT_LPUT2`** | `0x019C08` | `0x036AE6` | `res_drvr_sony.s:4180`<br>`res_drvr_sony_fdhd.s:4841` | — |
| **`SONY_SENDPKT_LPUT3`** | `0x019C0E` | `0x036AEC` | `res_drvr_sony.s:4184`<br>`res_drvr_sony_fdhd.s:4845` | — |
| **`SONY_SENDPKT_LPUT4`** | `0x019C16` | `0x036AF4` | `res_drvr_sony.s:4189`<br>`res_drvr_sony_fdhd.s:4850` | — |
| **`SONY_SENDPKT_LPUT5`** | `0x019C1C` | `0x036AFA` | `res_drvr_sony.s:4193`<br>`res_drvr_sony_fdhd.s:4854` | — |
| **`SONY_SENDPKT_LPUT6`** | `0x019C24` | `0x036B02` | `res_drvr_sony.s:4198`<br>`res_drvr_sony_fdhd.s:4859` | — |
| **`SONY_SENDPKT_NEXT`** | `0x019BAE` | — | `res_drvr_sony.s:4134` | — |
| **`SONY_SENDPKT_PAD1`** | `0x019C30` | `0x036B0E` | `res_drvr_sony.s:4206`<br>`res_drvr_sony_fdhd.s:4867` | — |
| **`SONY_SENDPKT_PAD2`** | `0x019C38` | `0x036B16` | `res_drvr_sony.s:4211`<br>`res_drvr_sony_fdhd.s:4872` | — |
| **`SONY_SENDPKT_PUT0`** | `0x019B08` | `0x0369E6` | `res_drvr_sony.s:4050`<br>`res_drvr_sony_fdhd.s:4715` | — |
| **`SONY_SENDPKT_PUT1`** | `0x019B14` | `0x0369F2` | `res_drvr_sony.s:4056`<br>`res_drvr_sony_fdhd.s:4721` | — |
| **`SONY_SENDPKT_PUT2`** | `0x019B2E` | `0x036A0C` | `res_drvr_sony.s:4069`<br>`res_drvr_sony_fdhd.s:4734` | — |
| **`SONY_SENDPKT_PUT3`** | `0x019B48` | `0x036A26` | `res_drvr_sony.s:4082`<br>`res_drvr_sony_fdhd.s:4747` | — |
| **`SONY_SENDPKT_PUT4`** | `0x019B64` | `0x036A42` | `res_drvr_sony.s:4095`<br>`res_drvr_sony_fdhd.s:4760` | — |
| **`SONY_SENDPKT_PUT5`** | `0x019B76` | `0x036A54` | `res_drvr_sony.s:4105`<br>`res_drvr_sony_fdhd.s:4770` | — |
| **`SONY_SENDPKT_PUT6`** | `0x019B8E` | `0x036A6C` | `res_drvr_sony.s:4117`<br>`res_drvr_sony_fdhd.s:4782` | — |
| **`SONY_SENDPKT_PUT7`** | `0x019BA2` | `0x036A80` | `res_drvr_sony.s:4128`<br>`res_drvr_sony_fdhd.s:4793` | — |
| **`SONY_SENDPKT_SETUP`** | `0x019AD4` | `0x0369B2` | `res_drvr_sony.s:4023`<br>`res_drvr_sony.s:4538` | — |
| **`SONY_SENDPKT_WAITHIGH`** | `0x019C4A` | `0x036B28` | `res_drvr_sony.s:4219`<br>`res_drvr_sony_fdhd.s:4880` | — |
| **`SONY_SENDPKT_WAITLOW`** | `0x019AB0` | `0x03698E` | `res_drvr_sony.s:4010`<br>`res_drvr_sony_fdhd.s:4675` | the first 6 bytes (the command block): D1 = 1/2 (low/high word), D2 = 3/4, D3 = 5/6, each shifted right with bit 7 set wait until the HD20 pulls HSHK low |
| **`Sony_Sense`** | `0x018600` | `0x034FC6` | `res_drvr_sony.s:1203`<br>`res_drvr_sony_fdhd.s:1639` | AdrAndSense / Sense -- read the sense line of a drive register D0 (in)  -- register address (AdrAndSense only) D0 (out) -- IWM status register: bit 7 = SENSE input (BMI = 1), bit 5 The status register... |
| **`SONY_SENSE_IWM`** | — | — | `res_drvr_sony_fdhd.s:1642` | — |
| **`Sony_SetChipMode`** | — | — | `res_drvr_sony_fdhd.s:2949` | SetChipMode -- select the register set the disk needs: the ISM registers for an MFM disk (mfmDisk), the IWM registers otherwise; with a plain IWM just SetIWMMode. Which set is selected is found out by... |
| **`SONY_SETCHIPMODE_ERR`** | — | — | `res_drvr_sony_fdhd.s:3005` | — |
| **`SONY_SETCHIPMODE_EXIT`** | — | — | `res_drvr_sony_fdhd.s:3010` | — |
| **`SONY_SETCHIPMODE_FAIL`** | — | — | `res_drvr_sony_fdhd.s:3003` | — |
| **`SONY_SETCHIPMODE_ISM`** | — | — | `res_drvr_sony_fdhd.s:2994` | — |
| **`SONY_SETCHIPMODE_IWM`** | — | — | `res_drvr_sony_fdhd.s:2975` | — |
| **`SONY_SETCHIPMODE_SETMODE`** | — | — | `res_drvr_sony_fdhd.s:3008` | — |
| **`SONY_SETCHIPMODE_TRY`** | — | — | `res_drvr_sony_fdhd.s:2956` | — |
| **`SONY_SETIWMMODE`** | — | `0x035268` | `res_drvr_sony_fdhd.s:2072` | SetIWMMode -- make sure the IWM mode register holds iwmMode = $17; separated from Recal on the SE (A351, 5 Nov 1986). D0 (out), CCR -- 0 (BEQ) or initIWMErr (BNE) after about a second $17 = mode regis... |
| **`SONY_SETIWMMODE_DONE`** | — | `0x0352B0` | `res_drvr_sony_fdhd.s:2096` | — |
| **`SONY_SETIWMMODE_EXIT`** | — | `0x0352B8` | `res_drvr_sony_fdhd.s:2099` | — |
| **`SONY_SETIWMMODE_LOOP`** | — | `0x035282` | `res_drvr_sony_fdhd.s:2081` | — |
| **`Sony_SetParams`** | — | — | `res_drvr_sony_fdhd.s:3029` | SetParams -- load the 16 ISM parameter RAM bytes for the zone of the current track (MPARAMZONES), unless they are already there; up to five attempts, each verified by reading the RAM back. rParams and... |
| **`SONY_SETPARAMS_CHECK`** | — | — | `res_drvr_sony_fdhd.s:3043` | — |
| **`SONY_SETPARAMS_EXIT`** | — | — | `res_drvr_sony_fdhd.s:3061` | — |
| **`SONY_SETPARAMS_LOAD`** | — | — | `res_drvr_sony_fdhd.s:3051` | — |
| **`SONY_SETPARAMS_LOOP`** | — | — | `res_drvr_sony_fdhd.s:3054` | — |
| **`SONY_SETPARAMS_TRY`** | — | — | `res_drvr_sony_fdhd.s:3039` | — |
| **`SONY_SETPARAMS_ZONE`** | — | — | `res_drvr_sony_fdhd.s:3032` | — |
| **`Sony_SetSpeed`** | `0x01864C` | `0x035012` | `res_drvr_sony.s:1258`<br>`res_drvr_sony_fdhd.s:1701` | SetSpeed -- set the speed for a track (400K drives: speed code through the PWM bytes of the sound buffer; new-interface drives regulate their speed themselves and get code 0) D6 (in) -- track number L... |
| **`SONY_SETSPEED_CONT`** | `0x01867E` | `0x035044` | `res_drvr_sony.s:1282`<br>`res_drvr_sony_fdhd.s:1724` | delay = \|change\| * 32 * 100 us, at least SpdChgTime (150 ms) |
| **`SONY_SETSPEED_CONT_2`** | `0x018688` | `0x03504E` | `res_drvr_sony.s:1287`<br>`res_drvr_sony_fdhd.s:1729` | — |
| **`SONY_SETSPEED_CONT_3`** | `0x0186A6` | `0x03506C` | `res_drvr_sony.s:1310`<br>`res_drvr_sony_fdhd.s:1751` | SONY_SETSPEED_CONT_3 -- store the speed code D2 in PWMValue and fill the 370 PWM bytes of the sound buffer at PWMBuf1 and at PWMBuf2 (MPW SysEqu.a: "PWM buffer 1 (or 2 if sound)") -- every second byte... |
| **`SONY_SETSPEED_CONT_4`** | `0x0186F2` | `0x0350B8` | `res_drvr_sony.s:1345`<br>`res_drvr_sony_fdhd.s:1785` | pattern bit 0: the earlier state |
| **`SONY_SETSPEED_CONT_5`** | `0x0186F4` | `0x0350BA` | `res_drvr_sony.s:1347`<br>`res_drvr_sony_fdhd.s:1787` | — |
| **`SONY_SETSPEED_CONT_6`** | `0x01870C` | `0x0350D2` | `res_drvr_sony.s:1359`<br>`res_drvr_sony_fdhd.s:1800` | Pattern words, read at byte offset r (0-9) as (byte r, byte r + 1): the top 10 bits hold r one bits, spread out (r = 1: $2021, 5: $AAB5, 9: $FF40) |
| **`SONY_SETSPEED_CONT_7`** | `0x01870D` | `0x0350D3` | `res_drvr_sony.s:1361`<br>`res_drvr_sony_fdhd.s:1802` | — |
| **`SONY_SETSPEED_LFSR`** | `0x0186BC` | `0x035082` | `res_drvr_sony.s:1318`<br>`res_drvr_sony_fdhd.s:1759` | — |
| **`SONY_SETSPEED_LOOP_2`** | `0x0186E6` | `0x0350AC` | `res_drvr_sony.s:1335`<br>`res_drvr_sony_fdhd.s:1776` | — |
| **`SONY_SETSPEED_LOOP_3`** | `0x0186EA` | `0x0350B0` | `res_drvr_sony.s:1338`<br>`res_drvr_sony_fdhd.s:1779` | — |
| **`SONY_SETSPEED_NO`** | `0x018666` | `0x03502C` | `res_drvr_sony.s:1269`<br>`res_drvr_sony_fdhd.s:1712` | — |
| **`SONY_SETSPEED_NO_2`** | `0x018694` | `0x03505A` | `res_drvr_sony.s:1292`<br>`res_drvr_sony_fdhd.s:1734` | — |
| **`SONY_SETSPEED_NO_3`** | `0x0186A2` | `0x035068` | `res_drvr_sony.s:1297`<br>`res_drvr_sony_fdhd.s:1739` | — |
| **`SONY_SETSPEED_OK`** | `0x018668` | `0x03502E` | `res_drvr_sony.s:1271`<br>`res_drvr_sony_fdhd.s:1714` | — |
| **`SONY_SETSPEED_OK_2`** | `0x018672` | `0x035038` | `res_drvr_sony.s:1275`<br>`res_drvr_sony_fdhd.s:1718` | — |
| **`SONY_SETSPEED_SKIP`** | `0x0186CC` | `0x035092` | `res_drvr_sony.s:1326`<br>`res_drvr_sony_fdhd.s:1767` | — |
| **`Sony_SetUpPoll`** | `0x018BEA` | `0x035ACC` | `res_drvr_sony.s:2086`<br>`res_drvr_sony.s:2729` | jtSetUpPoll -- prepare the SCC polling of the disk routines: A6 = SCC channel A data, A5 = VIA port A (SCC W/REQ in bit 7), interrupts off; PollStack = SP + D0, i.e. the stack level of the caller's ca... |
| **`SONY_SLIPMKS`** | `0x019086` | `0x035F6A` | `res_drvr_sony.s:2723`<br>`res_drvr_sony_fdhd.s:2843` | TrailMks -- slip marks $DE $AA and two $FF that let the last byte reach the disk before the write state ends |
| **`SONY_SPDSEEK`** | `0x01917C` | `0x036060` | `res_drvr_sony.s:2830`<br>`res_drvr_sony.s:3451` | SpdSeek -- seek to SideTrack (synchronously); with a 400K drive measure the speed at the first track of each zone (0, 16, 32, 48, 64) and move the zone's speed code by half its 2% delta until the spee... |
| **`SONY_SPDSEEK_ADJUST`** | `0x0191D2` | `0x0360B6` | `res_drvr_sony.s:2867`<br>`res_drvr_sony.s:3486` | too fast or too slow: correct the speed code, check again |
| **`SONY_SPDSEEK_CHECK`** | `0x0191BA` | `0x03609E` | `res_drvr_sony.s:2854`<br>`res_drvr_sony.s:3474` | back from GetFreq1: D4 = speed value (MI: no tachometer pulses) |
| **`SONY_SPDSEEK_CKDRIFT`** | `0x019182` | `0x036066` | `res_drvr_sony.s:2833`<br>`res_drvr_sony.s:3453` | CkDrift -- seek, then check the speed |
| **`SONY_SPDSEEK_ERR`** | `0x0191DE` | `0x0360C2` | `res_drvr_sony.s:2872`<br>`res_drvr_sony.s:3491` | — |
| **`SONY_SPDSEEK_EXIT`** | `0x0191E4` | `0x0360C8` | `res_drvr_sony.s:2879`<br>`res_drvr_sony.s:3498` | — |
| **`SONY_SPDSEEK_OK`** | `0x0191E2` | `0x0360C6` | `res_drvr_sony.s:2877`<br>`res_drvr_sony.s:3496` | SpdSeekOK -- speed within the limits, or an 800K drive |
| **`SONY_STARTT2`** | `0x018AD4` | `0x0354D0` | `res_drvr_sony.s:1918`<br>`res_drvr_sony_fdhd.s:2448` | StartT2 -- timer 2 = $FFFF: the low byte goes to the latch, writing the high byte loads the counter, starts it and clears IFR bit 5 |
| **`SONY_STATUS_DONE`** | — | — | `res_drvr_sony_fdhd.s:758` | — |
| **`SONY_STATUS_NEXT`** | — | — | `res_drvr_sony_fdhd.s:744` | — |
| **`SONY_STATUS_SCAN`** | — | — | `res_drvr_sony_fdhd.s:746` | — |
| **`SONY_SYNCCALL`** | `0x0194BA` | `0x03639A` | `res_drvr_sony.s:3263`<br>`res_drvr_sony.s:3842` | SyncCall -- call the routine at A0 and wait until it has finished: when it has to wait (WakeUp) it returns to its caller's caller, the wait loop here, and goes on from the Time Manager. The high byte ... |
| **`SONY_SYNCCALL_CALL`** | `0x0194C8` | `0x0363A8` | `res_drvr_sony.s:3272`<br>`res_drvr_sony.s:3852` | SyncCall's call: the routine returns here when it has finished |
| **`SONY_SYNCCALL_WAIT`** | `0x0194C0` | `0x0363A0` | `res_drvr_sony.s:3266`<br>`res_drvr_sony.s:3845` | — |
| **`SONY_TAIL_CTLFORMAT`** | — | — | `res_drvr_sony_fdhd.s:5057` | — |
| **`SONY_TAIL_CTLVERIFY`** | — | — | `res_drvr_sony_fdhd.s:5059` | — |
| **`SONY_TAIL_DRIVEICON`** | — | — | `res_drvr_sony_fdhd.s:5051` | — |
| **`SONY_TAIL_DRVINFO`** | — | — | `res_drvr_sony_fdhd.s:5055` | — |
| **`SONY_TAIL_E_SETUPPOLL`** | — | — | `res_drvr_sony_fdhd.s:5067` | — |
| **`SONY_TAIL_MEDIAICON`** | — | — | `res_drvr_sony_fdhd.s:5053` | — |
| **`SONY_TAIL_RDADDR`** | — | — | `res_drvr_sony_fdhd.s:5045` | Jump table into the ROM tail: routines that did not fit into the driver's resource slot were placed in the free space at the end of the ROM (FDHD_ResourceTailPatchCode, $43D000); each entry here jumps... |
| **`SONY_TAIL_RDADDRSETUP`** | — | — | `res_drvr_sony_fdhd.s:5061` | — |
| **`SONY_TAIL_RDDATA`** | — | — | `res_drvr_sony_fdhd.s:5047` | — |
| **`SONY_TAIL_READDATA`** | — | — | `res_drvr_sony_fdhd.s:5063` | — |
| **`SONY_TAIL_SETDRVTBL`** | — | — | `res_drvr_sony_fdhd.s:5069` | — |
| **`SONY_TAIL_SETUPPOLL`** | — | — | `res_drvr_sony_fdhd.s:5049` | — |
| **`SONY_TAIL_TOEMPTYPD`** | — | — | `res_drvr_sony_fdhd.s:5065` | — |
| **`SONY_TCDISPOSE`** | `0x017EBE` | `0x034922` | `res_drvr_sony.s:284`<br>`res_drvr_sony_fdhd.s:606` | TCdispose -- release the track cache buffer D0 (out) -- number of bytes freed (0 if there was no buffer) |
| **`SONY_TCDISPOSE_DONE`** | `0x017ED6` | `0x03493A` | `res_drvr_sony.s:294`<br>`res_drvr_sony_fdhd.s:616` | — |
| **`Sony_TCRdEnbChk`** | `0x0182A2` | `0x034C40` | `res_drvr_sony.s:795`<br>`res_drvr_sony_fdhd.s:1184` | TCRdEnbChk -- TCRdEnable = $FF (BEQ) if the cache is installed and on, the call is synchronous and no sectors are needed on another track (D6 = 0); else TCRdEnable = 0 (BNE). |
| **`SONY_TCRDENBCHK_OFF`** | `0x0182B8` | `0x034C56` | `res_drvr_sony.s:806`<br>`res_drvr_sony_fdhd.s:1194` | cache not installed |
| **`SONY_TCRDENBCHK_SET`** | `0x0182B2` | `0x034C50` | `res_drvr_sony.s:801`<br>`res_drvr_sony_fdhd.s:1190` | — |
| **`SONY_TODORECAL`** | — | `0x034CEC` | `res_drvr_sony_fdhd.s:1273` | — |
| **`SONY_TODRWOFF`** | — | `0x034AE2` | `res_drvr_sony_fdhd.s:1022` | — |
| **`SONY_TODSKRWOFF`** | — | `0x034E9E` | `res_drvr_sony_fdhd.s:1461` | — |
| **`SONY_TOEMPTYPD`** | `0x0194AE` | `0x03638E` | `res_drvr_sony.s:3250`<br>`res_drvr_sony.s:3834` | toEmptyPD -- DskErr = D0, then EmptyPD (poll data to PollProc, stack reset) Called by: SONY_FORMATTRACK_1, SONY_FORMATTRACK_GAP, SONY_VERTRACK_LOOP, SONY_VERTRACK_1, SONY_VERTRACK_2 |
| **`SONY_TORESEEK`** | — | `0x034B8E` | `res_drvr_sony_fdhd.s:1106` | CheckCache -- use the track cache when possible |
| **`SONY_VERTRACK`** | `0x019410` | `0x0362F0` | `res_drvr_sony.s:3174`<br>`res_drvr_sony.s:3768` | VerTrack -- read every sector of the current track (side 0, then side 1 of a two-sided format) with interrupts off. SectMapSave holds [sector map][tries] for side 0 and a copy for side 1; tries = 4 * ... |
| **`SONY_VERTRACK_1`** | `0x019440` | `0x036320` | `res_drvr_sony.s:3195`<br>`res_drvr_sony.s:3786` | sector D2 still wanted? |
| **`SONY_VERTRACK_2`** | `0x019458` | `0x036338` | `res_drvr_sony.s:3207`<br>`res_drvr_sony.s:3796` | read the sector's data field |
| **`SONY_VERTRACK_3`** | `0x019480` | `0x036360` | `res_drvr_sony.s:3222`<br>`res_drvr_sony.s:3811` | — |
| **`SONY_VERTRACK_DONE`** | `0x0194A0` | `0x036380` | `res_drvr_sony.s:3240`<br>`res_drvr_sony.s:3825` | track verified |
| **`SONY_VERTRACK_EXIT`** | `0x0194A2` | `0x036382` | `res_drvr_sony.s:3242`<br>`res_drvr_sony.s:3827` | — |
| **`SONY_VERTRACK_LOOP`** | `0x019430` | `0x036310` | `res_drvr_sony.s:3186`<br>`res_drvr_sony.s:3779` | VTLoop -- next address field |
| **`SONY_VERTRACK_OK`** | `0x019488` | `0x036368` | `res_drvr_sony.s:3229`<br>`res_drvr_sony.s:3816` | VTExitOK -- side 0 done: side 1 of a two-sided disk |
| **`SONY_WAIT100`** | `0x01878C` | `0x035152` | `res_drvr_sony.s:1437`<br>`res_drvr_sony_fdhd.s:1879` | Wait100 -- after a step pulse: old drives wait SeekTime (12 ms), new drives poll /STEP until it is high again (at most 81 times) |
| **`SONY_WAIT100_LOOP`** | `0x018794` | `0x03515A` | `res_drvr_sony.s:1441`<br>`res_drvr_sony_fdhd.s:1883` | — |
| **`SONY_WAITREADY`** | `0x0187B2` | `0x035178` | `res_drvr_sony.s:1469`<br>`res_drvr_sony_fdhd.s:1908` | waitReady -- old drive: wait D0 (CheckNew); new drive: wait D2 * 100 us, then poll /READY every 1 ms, for at most 1 s; clears Wait |
| **`SONY_WAITREADY_DONE`** | `0x0187CE` | `0x035194` | `res_drvr_sony.s:1483`<br>`res_drvr_sony_fdhd.s:1922` | — |
| **`SONY_WAITREADY_LOOP`** | `0x0187BE` | `0x035184` | `res_drvr_sony.s:1475`<br>`res_drvr_sony_fdhd.s:1914` | — |
| **`SONY_WAITREADY_SENSE`** | `0x0187C0` | `0x035186` | `res_drvr_sony.s:1477`<br>`res_drvr_sony_fdhd.s:1916` | — |
| **`SONY_WAITTACH`** | `0x018B0A` | `0x03550A` | `res_drvr_sony.s:1952`<br>`res_drvr_sony_fdhd.s:2483` | WaitTach -- wait for a rising edge of TACH (sensed 0 twice, then 1 twice), pushing SCC bytes meanwhile. D0 = 0 (BEQ), or noDriveErr (BNE) when timer 2 runs out (Apple: "probably no drive"). Returns vi... |
| **`SONY_WAITTACH_HIGH`** | `0x018B2A` | `0x035524` | `res_drvr_sony.s:1976`<br>`res_drvr_sony_fdhd.s:2502` | TACH low: wait for high |
| **`SONY_WAITTACH_HIGH_2`** | `0x018B30` | `0x03552A` | `res_drvr_sony.s:1980`<br>`res_drvr_sony_fdhd.s:2506` | — |
| **`SONY_WAITTACH_LOW`** | `0x018B0E` | `0x03550E` | `res_drvr_sony.s:1955`<br>`res_drvr_sony_fdhd.s:2486` | wait for TACH low |
| **`SONY_WAITTACH_LOW_2`** | `0x018B14` | `0x035514` | `res_drvr_sony.s:1959`<br>`res_drvr_sony_fdhd.s:2490` | — |
| **`SONY_WAITTACH_LOW_3`** | `0x018B1C` | `0x03551C` | `res_drvr_sony.s:1964`<br>`res_drvr_sony_fdhd.s:2495` | — |
| **`SONY_WAITTACH_TIMEOUT`** | `0x018B20` | `0x035520` | `res_drvr_sony.s:1967`<br>`res_drvr_sony_fdhd.s:2498` | — |
| **`SONY_WAKEGO`** | `0x0187DC` | — | `res_drvr_sony.s:1504` | WakeGo -- save the continuation, open interrupts, return to the caller's caller |
| **`SONY_WAKESETUP`** | `0x0187EE` | `0x0351C0` | `res_drvr_sony.s:1514`<br>`res_drvr_sony_fdhd.s:1974` | WakeSetUp -- Wait -= D0 (pinned at 0); prime the Time Manager element TimeQEl for D0 * 100 us (at least 1 ms) with GoWakeIt as its routine |
| **`SONY_WAKESETUP_1`** | `0x0187FC` | `0x0351CE` | `res_drvr_sony.s:1519`<br>`res_drvr_sony_fdhd.s:1979` | — |
| **`SONY_WAKESETUP_2`** | `0x018816` | `0x0351E8` | `res_drvr_sony.s:1527`<br>`res_drvr_sony_fdhd.s:1987` | — |
| **`Sony_WakeUp`** | `0x0187DA` | `0x0351A0` | `res_drvr_sony.s:1501`<br>`res_drvr_sony_fdhd.s:1958` | jtWakeUp -- wait D0 * 100 us (Time Manager), then continue at the caller's return address; meanwhile the caller's caller gets control back with D0 = 0 (the driver is asynchronous). Wait is reduced by ... |
| **`SONY_WAKEUP_EXIT`** | — | `0x0351B4` | `res_drvr_sony_fdhd.s:1967` | SONY_WAKEUP_EXIT -- return to WakeUp continuation. |
| **`SONY_WAKEUP_GO`** | — | `0x0351AE` | `res_drvr_sony_fdhd.s:1964` | WakeGo -- wait set up by WakeSetUp: save the state and return |
| **`SONY_WAKEUP_RET`** | — | `0x0351B8` | `res_drvr_sony_fdhd.s:1969` | — |
| **`Sony_WrData`** | `0x018F40` | `0x035E24` | `res_drvr_sony.s:2562`<br>`res_drvr_sony_fdhd.s:2678` | jtWrData -- write the data field of the sector whose address field was just read (Larry Kenyon): six self-sync bytes, $D5 $AA $AD, the sector number (TagData+1), the 12 tag bytes (TagData+2..) and the... |
| **`SONY_WRDATA_CONT`** | `0x018F8C` | `0x035E72` | `res_drvr_sony.s:2598`<br>`res_drvr_sony_fdhd.s:2713` | WrDataSw -- after the tags, continue with the data buffer |
| **`SONY_WRDATA_LOOP`** | `0x018F68` | `0x035E4E` | `res_drvr_sony.s:2575`<br>`res_drvr_sony_fdhd.s:2692` | — |
| **`SONY_WRDATA_LOOP_2`** | `0x018FB8` | `0x035E9E` | `res_drvr_sony.s:2624`<br>`res_drvr_sony_fdhd.s:2737` | WrData2 -- next byte A, low bits of B, next byte B, low bits of C, next C |
| **`SONY_WRDATA_LOOP_3`** | `0x019062` | `0x035F48` | `res_drvr_sony.s:2704`<br>`res_drvr_sony_fdhd.s:2815` | — |
| **`SONY_WRDATA_NEXT`** | `0x018F8E` | `0x035E74` | `res_drvr_sony.s:2601`<br>`res_drvr_sony_fdhd.s:2715` | WrData1 -- finish byte C, write the top-bits nibble and the low bits of A |
| **`SONY_WRDATA_NO`** | `0x018F6A` | `0x035E50` | `res_drvr_sony.s:2577`<br>`res_drvr_sony_fdhd.s:2694` | — |
| **`SONY_WRDATA_NO_10`** | `0x019054` | `0x035F3A` | `res_drvr_sony.s:2698`<br>`res_drvr_sony_fdhd.s:2809` | — |
| **`SONY_WRDATA_NO_2`** | `0x018F80` | `0x035E66` | `res_drvr_sony.s:2589`<br>`res_drvr_sony_fdhd.s:2706` | — |
| **`SONY_WRDATA_NO_3`** | `0x018F96` | `0x035E7C` | `res_drvr_sony.s:2606`<br>`res_drvr_sony_fdhd.s:2720` | — |
| **`SONY_WRDATA_NO_4`** | `0x018FAA` | `0x035E90` | `res_drvr_sony.s:2615`<br>`res_drvr_sony_fdhd.s:2729` | — |
| **`SONY_WRDATA_NO_5`** | `0x018FC6` | `0x035EAC` | `res_drvr_sony.s:2631`<br>`res_drvr_sony_fdhd.s:2744` | — |
| **`SONY_WRDATA_NO_6`** | `0x018FF8` | `0x035EDE` | `res_drvr_sony.s:2657`<br>`res_drvr_sony_fdhd.s:2768` | WrLast2 -- the last group has only bytes 511 and 512 (C = 0); then the checksums as one top-bits nibble and three low-bits nibbles |
| **`SONY_WRDATA_NO_7`** | `0x01900C` | `0x035EF2` | `res_drvr_sony.s:2666`<br>`res_drvr_sony_fdhd.s:2777` | — |
| **`SONY_WRDATA_NO_8`** | `0x01902A` | `0x035F10` | `res_drvr_sony.s:2680`<br>`res_drvr_sony_fdhd.s:2791` | — |
| **`SONY_WRDATA_NO_9`** | `0x019036` | `0x035F1C` | `res_drvr_sony.s:2685`<br>`res_drvr_sony_fdhd.s:2796` | — |
| **`SONY_WRDATA_OK`** | `0x01907C` | `0x035F62` | `res_drvr_sony.s:2717`<br>`res_drvr_sony_fdhd.s:2828` | — |
| **`SONY_WRDATA_SKIP`** | `0x018F76` | `0x035E5C` | `res_drvr_sony.s:2584`<br>`res_drvr_sony_fdhd.s:2701` | — |
| **`SONY_WRDATA_SKIP_2`** | `0x018FB0` | `0x035E96` | `res_drvr_sony.s:2619`<br>`res_drvr_sony_fdhd.s:2733` | — |
| **`SONY_WRDATA_SKIP_3`** | `0x018FE2` | `0x035EC8` | `res_drvr_sony.s:2644`<br>`res_drvr_sony_fdhd.s:2757` | — |
| **`SONY_WRDATA_SKIP_4`** | `0x01901E` | `0x035F04` | `res_drvr_sony.s:2674`<br>`res_drvr_sony_fdhd.s:2785` | — |
| **`SONY_WRDATA_SKIP_5`** | `0x019048` | `0x035F2E` | `res_drvr_sony.s:2693`<br>`res_drvr_sony_fdhd.s:2804` | — |
| **`SONY_WRDATA_SKIP_6`** | `0x01906E` | `0x035F54` | `res_drvr_sony.s:2711`<br>`res_drvr_sony_fdhd.s:2822` | — |
| **`SONY_WRDATAMKS`** | `0x018F2E` | `0x035E12` | `res_drvr_sony.s:2537`<br>`res_drvr_sony_fdhd.s:2649` | MarkTbl (Apple) -- the six self-sync bytes and the first two bytes of the data mark. As a bit stream the self-sync bytes are 11111111 00 11111111 00 11111111 00 11111111 00 11111111: four 10-bit self-... |
| **`SONY_WRGSECTADR`** | — | `0x034EFA` | `res_drvr_sony_fdhd.s:1508` | WrgSectAdr -- a sector we do not need: wait about one sector time |
| **`SONY_WRGSIDETRK`** | — | `0x034F1C` | `res_drvr_sony_fdhd.s:1524` | WrgSideTrk -- wrong track or side under the head |
| **`STATUSTBL`** | — | — | `res_drvr_sony_fdhd.s:722` | StatusTbl -- status call dispatch table (new; the 1987 SE driver only knew csCode 8): csCode and handler offset (relative to STATUSTBL); a zero word ends the table. |
| **`STRINGTONUM`** | `0x01CA68` | `0x01D3D0` | `res_pack_7.s:153`<br>`res_pack_7.s:155` | STRINGTONUM (Apple select1) -- selectors 1-4: pop the selector word; selector 1 falls into StringToNum, 2-4 go to DECSTR_SELECT2. |
| **`TCSL_DRAWFRAME`** | — | `0x01D8D6` | `res_tcsl.s:95` | TCSL_DRAWFRAME -- unpack frame D7/4 of 'bbmc' 0 onto the screen. In:  D7 = 0, 4, 8, 12 (offset into the frame table), ApplScratch = the 'bbmc' data. Uses ApplScratch+4 (source pointer) and ApplScratch... |
| **`TCSL_LOADBBMC`** | — | `0x01D8B4` | `res_tcsl.s:75` | TCSL_LOADBBMC -- get 'bbmc' 0 from the ROM resource map. Out: ApplScratch = pointer to its data (the frame offset table), D7 = 0. Breaks into the debugger if it is not found. |
| **`TCSL_NEXTFRAME`** | — | `0x01D89E` | `res_tcsl.s:63` | show the next picture, wait 3 seconds, repeat |
| **`TCSL_NOBBMC`** | — | `0x01D91A` | `res_tcsl.s:117` | 'bbmc' 0 not found: stop in the debugger (continuing would run into the next resource's header) |
| **`TCSL_ROWLOOP`** | — | `0x01D8F4` | `res_tcsl.s:103` | — |
| **`TCSL_SLIDESHOW`** | — | `0x01D89A` | `res_tcsl.s:60` | TCSL_SLIDESHOW -- the entry point at $41D89A (debugger: G 41D89A). Loads 'bbmc' 0, then shows its frames forever. |
| **`U`** | — | `0x0235DC` | `res_bbmc.s:5959` | — |
| **`UNLOADNBP`** | `0x01B312` | `0x034020` | `res_drvr_mpp.s:1969`<br>`res_drvr_mpp.s:2275` | UnloadNBP (csCode 255): nothing to unload - as KillNBP |
| **`WDEF1_BUILDTBARRECT`** | — | `0x039316` | `res_wdef_1.s:215` | BuildTBarRect -- TempRect := the title bar: structRgn's box with bottom = top + WHeight and right - 1. Out: A0 = TempRect. Changes D0/A1. Called by: WDEF1_EORGOAWAY, WDEF1_PLOTGOAWAY, WDEF1_DOTITLESTR... |
| **`WDEF1_CALCDOC`** | — | `0x039512` | `res_wdef_1.s:483` | CalcDoc (wCalcRgns) -- TempRect = portRect in global coordinates (offset by -portBits.bounds.topLeft). contRgn = TempRect with round bottom and square top corners; structRgn = TempRect grown by 1 (the... |
| **`WDEF1_CHECKTROUND`** | — | `0x039448` | `res_wdef_1.s:377` | — |
| **`WDEF1_COMPLEXRECT`** | — | `0x03941E` | `res_wdef_1.s:361` | record a round rect, then square up the top or the bottom |
| **`WDEF1_DISPOSIT`** | — | `0x03930A` | `res_wdef_1.s:202` | — |
| **`WDEF1_DOHILITE`** | — | `0x039300` | `res_wdef_1.s:198` | — |
| **`WDEF1_DONEDOC`** | — | `0x039296` | `res_wdef_1.s:148` | — |
| **`WDEF1_DONEHIT1`** | — | `0x039510` | `res_wdef_1.s:474` | — |
| **`WDEF1_DONEHITDOC`** | — | `0x03950C` | `res_wdef_1.s:472` | — |
| **`WDEF1_DOTITLESTRING`** | — | `0x039398` | `res_wdef_1.s:292` | DoTitleString -- draw the window title centered in the title bar (TempRect), at least 28 pixels from its left edge when the window has a go-away box; baseline WAscent+2 below the top. The title handle... |
| **`WDEF1_DRAWDOC`** | — | `0x039298` | `res_wdef_1.s:159` | DrawDoc (wDraw) -- draw the window frame. param 4 (wInGoAway) only toggles the go-away box (WDEF1_EORGOAWAY). Otherwise the title bar (TempRect, from the top of structRgn's box down by WHeight) is bui... |
| **`WDEF1_DRAWFRAME`** | — | `0x03930E` | `res_wdef_1.s:205` | — |
| **`WDEF1_DRAWTHETITLE`** | — | `0x0392E8` | `res_wdef_1.s:189` | — |
| **`WDEF1_ENTRY`** | — | `0x03921E` | `res_wdef_1.s:95` | set up the WMgrPort and the title metrics, fetch the parameters, dispatch on the message |
| **`WDEF1_EORGOAWAY`** | — | `0x039338` | `res_wdef_1.s:232` | EorGoAway (wDraw with param wInGoAway) -- toggle the go-away box of the active window by XORing its mask over it; falls into PlotGoAway. |
| **`WDEF1_GETRADPOINT`** | — | `0x0393DA` | `res_wdef_1.s:323` | GetRadPoint -- the corner diameters selected by varCode. In:  D5 = table index (WDEF1_ENTRY). Out: D0 = (height, width). Called by: WDEF1_DRAWDOC, WDEF1_GOMAKERGN |
| **`WDEF1_GOAWAYMASK`** | — | `0x039584` | `res_wdef_1.s:537` | ... and the mask XORed over it to show the box pressed (Cxxx 06Oct86: "brand-new, centered mask") |
| **`WDEF1_GOAWAYSYMBOL`** | — | `0x039564` | `res_wdef_1.s:518` | GoAwaySymbol: the go-away box, 16x16, drawn srcCopy ... |
| **`WDEF1_GODOCPROC`** | — | `0x03928A` | `res_wdef_1.s:144` | GoDocProc: dispatch table, entries must be long branches |
| **`WDEF1_GOMAKERGN`** | — | `0x03954E` | `res_wdef_1.s:508` | GoMakeRgn -- MakeRoundRegion(A0, TempRect, radius, D1, TRUE). In:  A0 = region, D1.W = topRound (botRound is always true). Called by: WDEF1_CALCDOC (and falls in from it) |
| **`WDEF1_GOTHEIGHT`** | — | `0x039252` | `res_wdef_1.s:118` | rdocprocs have asymmetric titles that are 19 high: fonts up to Chicago's size get 19, bigger ones an odd height for centering |
| **`WDEF1_HITDOC`** | — | `0x03948C` | `res_wdef_1.s:414` | HitDoc (wHit) -- D3 = the mouse point (global). wInContent in contRgn; in structRgn and in contRgn's box extended up by WHeight (the title bar): wInGoAway on the active window's box (h 8..18 from the ... |
| **`WDEF1_ITSINDRAG`** | — | `0x03950A` | `res_wdef_1.s:470` | in the title bar: is it the go-away box (active windows only)? in the title bar, but not on the go-away box: drag Called by: WDEF1_HITDOC (6 branches: no box, inactive window, h or v outside the box) |
| **`WDEF1_MAKEROUNDREGION`** | — | `0x039400` | `res_wdef_1.s:348` | **Proto:** `PROCEDURE MakeRoundRegion(theRgn: RgnHandle; theRect: Rect;`<br>MakeRoundRegion -- make a round-rect region; either half can be squared off. PROCEDURE MakeRoundRegion(theRgn: RgnHandle; theRect: Rect; radius: Point; topRound, botRound: BOOLEAN); (pushed in this or... |
| **`WDEF1_MINMARGIN`** | — | `0x0393BA` | `res_wdef_1.s:304` | — |
| **`WDEF1_MMRDONE`** | — | `0x039480` | `res_wdef_1.s:401` | — |
| **`WDEF1_NOTINCONTENT`** | — | `0x0394A0` | `res_wdef_1.s:425` | not in the content: in the window at all? |
| **`WDEF1_PLAINRECT`** | — | `0x039412` | `res_wdef_1.s:355` | — |
| **`WDEF1_PLOTGOAWAY`** | — | `0x039344` | `res_wdef_1.s:245` | PlotGoAway -- plot a 16x16 symbol at the go-away box position: 8 pixels right of the title bar's left edge, WBoxDelta-1 below its top. In:  A1 = the symbol's bits, D1 = transfer mode, TempRect = the t... |
| **`WDEF1_PLOTSYMBOL`** | — | `0x03936A` | `res_wdef_1.s:267` | PlotSymbol -- CopyBits a 16x16 symbol into TempRect of the current port, through the BitMap record IconBitmap ($A0E); bounds.topLeft is assumed to be (0,0) already. In:  A1 = the bits (2 bytes per row... |
| **`WDEF1_RADIUSTABLE`** | — | `0x0393E0` | `res_wdef_1.s:327` | RadiusTable: ovalHeight/ovalWidth for FrameRoundRect |
| **`WDEF1_RETURN`** | — | `0x03927A` | `res_wdef_1.s:136` | fetch the parameters |
| **`WDEF1_SQUAREIT`** | — | `0x039454` | `res_wdef_1.s:384` | ToolScratch := (D0, theRect.left, D1, theRect.right), unite it |
| **`WDEF1_TITLEX`** | — | `0x0393BC` | `res_wdef_1.s:306` | — |
| **`WDEF_CALC_CONT`** | `0x01C826` | `0x039A88` | `res_wdef.s:708`<br>`res_wdef_0.s:701` | — |
| **`WDEF_CALC_DBOX`** | `0x01C89A` | `0x039AFC` | `res_wdef.s:754`<br>`res_wdef_0.s:746` | dBoxProc: expand struct rect by 7px for thick double border |
| **`WDEF_CALC_DONE`** | `0x01C898` | `0x039AFA` | `res_wdef.s:749`<br>`res_wdef_0.s:742` | — |
| **`WDEF_CALC_SHADOW`** | `0x01C87A` | `0x039ADC` | `res_wdef.s:738`<br>`res_wdef_0.s:731` | — |
| **`WDEF_CALC_STRUCT`** | `0x01C86E` | `0x039AD0` | `res_wdef.s:732`<br>`res_wdef_0.s:725` | — |
| **`WDEF_CALCRGNS`** | `0x01C81C` | `0x039A7E` | `res_wdef.s:704`<br>`res_wdef_0.s:697` | wCalcRgns handler (Apple: CalcDoc) - compute contRgn and structRgn; first updates userState if a zoom window was moved or sized (WDEF_CHECK_ZOOM_ST) contRgn = portRect converted to global coordinates ... |
| **`WDEF_CHECK_DBOX`** | `0x01C572` | `0x0397D8` | `res_wdef.s:332`<br>`res_wdef_0.s:342` | — |
| **`WDEF_CHECK_ZOOM_ST`** | `0x01C432` | `0x03969A` | `res_wdef.s:186`<br>`res_wdef_0.s:200` | WDEF_CHECK_ZOOM_ST (Apple: IsItSmall) - is the window in its standard (zoomed-out) state? The window counts as "big" if both corners of its global portRect are within 7 pixels of the corners of stdSta... |
| **`WDEF_CLOSE_NORMAL`** | `0x01C712` | `0x039978` | `res_wdef.s:552`<br>`res_wdef_0.s:552` | WDEF_CLOSE_NORMAL - close box, normal (empty square) |
| **`WDEF_CLOSE_TOGGLE`** | `0x01C732` | `0x039998` | `res_wdef.s:570`<br>`res_wdef_0.s:570` | WDEF_CLOSE_TOGGLE - close box, toggled (XOR pattern for highlight) |
| **`WDEF_COPY_PORTRECT`** | `0x01C418` | `0x039680` | `res_wdef.s:166`<br>`res_wdef_0.s:181` | WDEF_COPY_PORTRECT (Apple: GetRect) - copy portRect to the rect at A4 and convert it to global coordinates by negating the portBits.bounds origin. Used to snapshot the window's position. Changes D0-D2... |
| **`WDEF_COPYBITS`** | `0x01C930` | `0x039B92` | `res_wdef.s:831`<br>`res_wdef_0.s:820` | WDEF_COPYBITS - CopyBits a small icon bitmap into the current port A1 = source bitmap data, D0 = transfer mode, D1 = bounds Builds temporary BitMap struct in IconBitmap low-memory, blits from icon dat... |
| **`WDEF_DISPOSE`** | `0x01C484` | `0x0396EA` | `res_wdef.s:243`<br>`res_wdef_0.s:254` | wDispose handler - free WStateData if zoom box allocated |
| **`WDEF_DISPOSE_DONE`** | `0x01C48E` | `0x0396F4` | `res_wdef.s:248`<br>`res_wdef_0.s:259` | — |
| **`WDEF_DRAW`** | `0x01C490` | `0x0396F6` | `res_wdef.s:257`<br>`res_wdef_0.s:267` | wDraw handler (Apple: DrawDoc) - draw window frame based on varCode/param param 0: draw entire frame (border, title bar, close/zoom) param 4: toggle close box highlight param 5: toggle zoom box highli... |
| **`WDEF_DRAW_FRAME`** | `0x01C54A` | `0x0397B0` | `res_wdef.s:316`<br>`res_wdef_0.s:326` | — |
| **`WDEF_DRAW_NONDOC`** | `0x01C63C` | `0x0398A2` | `res_wdef.s:440`<br>`res_wdef_0.s:442` | wDraw for non-document styles (varCode 1/2/3) Sets shadow offset D4 based on style, then draws frame |
| **`WDEF_DRAW_RTS`** | `0x01C5C6` | `0x03982C` | `res_wdef.s:361`<br>`res_wdef_0.s:371` | — |
| **`WDEF_DRAW_SHADOW`** | `0x01C56E` | `0x0397D4` | `res_wdef.s:330`<br>`res_wdef_0.s:340` | — |
| **`WDEF_DRAW_STRUCT`** | `0x01C54E` | `0x0397B4` | `res_wdef.s:318`<br>`res_wdef_0.s:328` | — |
| **`WDEF_DRAW_TITLE`** | `0x01C650` | `0x0398B6` | `res_wdef.s:455`<br>`res_wdef_0.s:456` | WDEF_DRAW_TITLE (Apple: DoTitleString) - draw window title string centered in title bar (TempRect), at least 2 pixels (32 with a close box) from its left edge, clipped to the space left of the zoom bo... |
| **`WDEF_DRAW_ZOOM`** | `0x01C536` | `0x03979C` | `res_wdef.s:309`<br>`res_wdef_0.s:319` | — |
| **`WDEF_DROP_SHADOW`** | `0x01C908` | `0x039B6A` | `res_wdef.s:806`<br>`res_wdef_0.s:796` | WDEF_DROP_SHADOW - draw drop shadow (L-shaped: bottom + right edges) A4 -> struct bounding rect, D4 = shadow pen size Called by: WDEF_DRAW_SHADOW |
| **`WDEF_ENTRY`** | `0x01C352` | `0x0395B8` | `res_wdef.s:69`<br>`res_wdef_0.s:86` | WDEF main entry - set up stack frame, compute title bar height from current font metrics, dispatch to handler |
| **`WDEF_GICON`** | `0x01C95C` | `0x039BBE` | `res_wdef.s:856`<br>`res_wdef_0.s:845` | wGIcon handler (Apple: DrawGIcon) - draw grow icon (size box) in content region Switches to the window's own port, draws size box bitmap at bottom-right corner, and scroll bar divider lines; returns w... |
| **`WDEF_GICON_DIVIDERS`** | `0x01C98C` | `0x039BF2` | `res_wdef.s:870`<br>`res_wdef_0.s:861` | — |
| **`WDEF_GICON_INACTIVE`** | `0x01C9B0` | `0x039C18` | `res_wdef.s:887`<br>`res_wdef_0.s:878` | inactive window: erase size box area, then draw dividers |
| **`WDEF_GROW`** | `0x01C8AE` | `0x039B10` | `res_wdef.s:767`<br>`res_wdef_0.s:758` | wGrow handler (Apple: GrowDoc) - draw grow image (rubber-band outline) D3 = pointer to grow rect; draws frame with crosshair lines showing scroll bar divider positions at 16px inset |
| **`WDEF_HAS_ZOOM`** | `0x01C476` | `0x0396DE` | `res_wdef.s:234`<br>`res_wdef_0.s:246` | WDEF_HAS_ZOOM - test if window has zoom box capability Returns NE if varCode bit 3 set AND wZoom set (WStateData allocated by wNew), else EQ. Called by: WDEF_DISPOSE, WDEF_DRAW, WDEF_DRAW_ZOOM, WDEF_T... |
| **`WDEF_HAS_ZOOM_RTS`** | `0x01C482` | `0x0396E8` | `res_wdef.s:238`<br>`res_wdef_0.s:250` | — |
| **`WDEF_HEIGHT_OK`** | `0x01C384` | `0x0395EC` | `res_wdef.s:89`<br>`res_wdef_0.s:107` | — |
| **`WDEF_HIT`** | `0x01C752` | `0x0399B8` | `res_wdef.s:594`<br>`res_wdef_0.s:593` | wHit handler (Apple: HitDoc) - determine which window part was clicked D3 = click point (global; v in high word, h in low word) Returns via 0x14(A6): wNoHit=0, wInContent=1, wInDrag=2, wInGrow=3, wInG... |
| **`WDEF_HIT_CONTENT`** | `0x01C792` | `0x0399F8` | `res_wdef.s:626`<br>`res_wdef_0.s:624` | return wInContent Called by: WDEF_HIT (5 branches: not a documentProc, no grow box, inactive window, outside the grow box) |
| **`WDEF_HIT_DRAG`** | `0x01C814` | `0x039A76` | `res_wdef.s:690`<br>`res_wdef_0.s:684` | in title bar but not on close/zoom -> drag region Called by: WDEF_HIT_TITLEBAR (4 branches), WDEF_HIT_ZOOM (3 branches) |
| **`WDEF_HIT_NOHIT`** | `0x01C81A` | `0x039A7C` | `res_wdef.s:695`<br>`res_wdef_0.s:689` | — |
| **`WDEF_HIT_RETURN`** | `0x01C816` | `0x039A78` | `res_wdef.s:693`<br>`res_wdef_0.s:687` | Called by: WDEF_HIT, WDEF_HIT_CONTENT, WDEF_HIT_TITLEBAR, WDEF_HIT_ZOOM, WDEF_HIT_ZOOM_IN |
| **`WDEF_HIT_TITLEBAR`** | `0x01C798` | `0x0399FC` | `res_wdef.s:632`<br>`res_wdef_0.s:629` | not in content - test title bar for drag, close, zoom |
| **`WDEF_HIT_ZOOM`** | `0x01C7EA` | `0x039A4C` | `res_wdef.s:666`<br>`res_wdef_0.s:662` | test zoom box hit (right side of title bar) |
| **`WDEF_HIT_ZOOM_IN`** | `0x01C810` | `0x039A72` | `res_wdef.s:683`<br>`res_wdef_0.s:678` | at the standard state: clicking zoom -> zoom in to the user state |
| **`WDEF_ICON_DRAW`** | `0x01C61C` | `0x039882` | `res_wdef.s:423`<br>`res_wdef_0.s:426` | WDEF_ICON_DRAW - common icon positioning and CopyBits Builds 16x16 dest rect in TempRect, calls WDEF_COPYBITS to blit |
| **`WDEF_ICON_LEFT`** | `0x01C616` | `0x03987C` | `res_wdef.s:417`<br>`res_wdef_0.s:421` | WDEF_ICON_LEFT - position and draw icon at left side of title bar A1 = bitmap data, D0 = transfer mode |
| **`WDEF_ICON_RIGHT`** | `0x01C600` | `0x039866` | `res_wdef.s:402`<br>`res_wdef_0.s:408` | WDEF_ICON_RIGHT - position and draw icon at right side of title bar A1 = bitmap data, D0 = transfer mode |
| **`WDEF_JMPTABLE`** | `0x01C3CE` | `0x039636` | `res_wdef.s:120`<br>`res_wdef_0.s:137` | Jump table - word offsets for each message handler |
| **`WDEF_NEW`** | `0x01C3DC` | `0x039644` | `res_wdef.s:135`<br>`res_wdef_0.s:151` | wNew handler - initialize zoom box data if requested varCode bit 3 means zoomable; allocates 16-byte WStateData: bytes 0-7 = userState rect (from current portRect) bytes 8-15 = stdState rect (the scre... |
| **`WDEF_NEW_DONE`** | `0x01C430` | `0x039698` | `res_wdef.s:174`<br>`res_wdef_0.s:189` | — |
| **`WDEF_PT_IN_EXPANDED`** | `0x01C456` | `0x0396BE` | `res_wdef.s:214`<br>`res_wdef_0.s:227` | WDEF_PT_IN_EXPANDED (Apple: ChkPoint) - is the point at (A4) within 7 pixels of the point at (A2)? Called twice in a row: first for topLeft, then for botRight. In:  A2 -> point of stdState, A4 -> poin... |
| **`WDEF_RESTORE_STRUCT`** | `0x01C5BE` | `0x039824` | `res_wdef.s:358`<br>`res_wdef_0.s:368` | — |
| **`WDEF_SIZEBOX_ICON`** | `0x01C9B8` | `0x039C20` | `res_wdef.s:895`<br>`res_wdef_0.s:885` | WDEF_SIZEBOX_ICON - size box (grow icon) bitmap, 16x16 Two overlapping rectangles representing a resizable window |
| **`WDEF_STATE_CHANGED`** | `0x01C448` | `0x0396B0` | `res_wdef.s:197`<br>`res_wdef_0.s:211` | — |
| **`WDEF_STATE_DONE`** | `0x01C452` | `0x0396BA` | `res_wdef.s:202`<br>`res_wdef_0.s:216` | — |
| **`WDEF_STRIPE_PAT`** | `0x01C5C8` | `0x03982E` | `res_wdef.s:365`<br>`res_wdef_0.s:374` | horizontal stripe pattern for active title bar highlight |
| **`WDEF_TITLE_ABS`** | `0x01C670` | `0x0398D6` | `res_wdef.s:469`<br>`res_wdef_0.s:470` | — |
| **`WDEF_TITLE_CLIP`** | `0x01C680` | `0x0398E6` | `res_wdef.s:475`<br>`res_wdef_0.s:476` | — |
| **`WDEF_TITLE_GAP`** | `0x01C6CE` | `0x039934` | `res_wdef.s:505`<br>`res_wdef_0.s:506` | — |
| **`WDEF_TITLE_MARGIN`** | `0x01C66A` | `0x0398D0` | `res_wdef.s:465`<br>`res_wdef_0.s:466` | — |
| **`WDEF_TITLE_RECT`** | `0x01C5D0` | `0x039836` | `res_wdef.s:375`<br>`res_wdef_0.s:383` | WDEF_TITLE_RECT (Apple: BuildTBarRect) - compute title bar rect into TempRect: structRgn's bounding box with bottom = top + title bar height (D7) and right - 1 (exclude the shadow column). Out: A0 = T... |
| **`WDEF_TOGGLE_BOX`** | `0x01C5F0` | `0x039856` | `res_wdef.s:392`<br>`res_wdef_0.s:399` | wDraw param >= 4: toggle close box or zoom box highlight param = 4 -> close box; param = 5 -> zoom box (entered with the flags of CMPI #4,D3) |
| **`WDEF_TOGGLE_CLOSE`** | `0x01C60E` | `0x039874` | `res_wdef.s:410`<br>`res_wdef_0.s:415` | wDraw param = 4: toggle close box highlight |
| **`WDEF_TOGGLE_DONE`** | `0x01C63A` | `0x0398A0` | `res_wdef.s:434`<br>`res_wdef_0.s:437` | — |
| **`WDEF_ZOOM_CLAMP_OK`** | `0x01C50C` | `0x039772` | `res_wdef.s:296`<br>`res_wdef_0.s:306` | — |
| **`WDEF_ZOOM_NORMAL`** | `0x01C6D2` | `0x039938` | `res_wdef.s:516`<br>`res_wdef_0.s:516` | Bitmap data for close and zoom box icons (16x16 each) (2 bytes per row). The boxes carry the title bar's stripes on their outer columns (every other row), so srcCopy keeps the stripes; the *_TOGGLE ma... |
| **`WDEF_ZOOM_TOGGLE`** | `0x01C6F2` | `0x039958` | `res_wdef.s:534`<br>`res_wdef_0.s:534` | WDEF_ZOOM_TOGGLE - zoom box, toggled (XOR pattern for highlight) |
| **`WRITEDDP`** | `0x01A818` | `0x033288` | `res_drvr_mpp.s:262`<br>`res_drvr_mpp.s:387` | WRITEDDP WriteDDP (csCode 246): send the datagram described by the WDS at wdsPointer from socket D1; checksumFlag = checksum long headers. |
| **`WRITELAP`** | `0x01A96C` | `0x0334A4` | `res_drvr_mpp.s:538`<br>`res_drvr_mpp.s:730` | WriteLAP (csCode 243): send the frame described by the WDS at wdsPointer (first entry: lapDstAdr, lapSrcAdr filled in, lapType 1..127, then the data).  lapProtErr, excessCollsns. |
| **`XPP_ABORTCALLS`** | — | `0x0373CC` | `res_drvr_xpp.s:883` | XPP_ABORTCALLS -- (A0 = scbATPPB) end every active call of the closing session, one per pass: for each call not a CloseSession, a UserWrite's write data response still under way is released (RelRspCB)... |
| **`XPP_ABORTCALLS_KILL`** | — | `0x03741C` | `res_drvr_xpp.s:908` | — |
| **`XPP_ABORTCALLS_LOOP`** | — | `0x0373D4` | `res_drvr_xpp.s:886` | — |
| **`XPP_ABORTOS`** | — | `0x037112` | `res_drvr_xpp.s:489` | XPP_ABORTOS -- csCode 248 abortOS (ASPAbortOS): abort a pending OpenSession (or FPLogin) given its SCB (abortSCBPtr). The OpenSess request on scbReqPB is cancelled with a KillSendReq on scbATPPB; the ... |
| **`XPP_ABORTOS_NOTFOUND`** | — | `0x03717A` | `res_drvr_xpp.s:553` | AbortOS: nothing to abort |
| **`XPP_AFP_DONE`** | — | `0x037708` | `res_drvr_xpp.s:1299` | XPP_AFP_DONE -- complete the AFPCommand with D0 Branch from: XPP_AFP_LOGINSTEP, XPP_AFP_LOGINREPLY, XPP_AFP_RWDONE |
| **`XPP_AFP_LOGIN`** | — | `0x03771C` | `res_drvr_xpp.s:1308` | FPLogin: first open a session (afpAddrBlock, afpSCBPtr, afpAttnRoutine; these overlap the CCB, which the login command later uses) |
| **`XPP_AFP_LOGINREPLY`** | — | `0x037758` | `res_drvr_xpp.s:1330` | — |
| **`XPP_AFP_LOGINSTEP`** | — | `0x03773C` | `res_drvr_xpp.s:1320` | FPLogin/FPLoginCont step: after the OpenSession send the login command (Command); after the Command check cmdResult: 0 or afpAuthContinue completes the call, anything else closes the session (CloseSes... |
| **`XPP_AFP_LOGOUT`** | — | `0x037712` | `res_drvr_xpp.s:1303` | FPLogout: ASP CloseSession of sessRefnum |
| **`XPP_AFP_NEXT`** | — | `0x037686` | `res_drvr_xpp.s:1243` | XPP_AFP_NEXT -- issue the (next) ASP call for the AFP command Branch from: XPP_AFP_RWCOUNT (next FPRead/FPWrite chunk) |
| **`XPP_AFP_PARMERR`** | — | `0x037676` | `res_drvr_xpp.s:1235` | — |
| **`XPP_AFP_RWADVANCE`** | — | `0x03779C` | `res_drvr_xpp.s:1360` | — |
| **`XPP_AFP_RWCOUNT`** | — | `0x0377A0` | `res_drvr_xpp.s:1362` | — |
| **`XPP_AFP_RWDONE`** | — | `0x0377BE` | `res_drvr_xpp.s:1375` | — |
| **`XPP_AFP_RWSIZE`** | — | `0x0376CA` | `res_drvr_xpp.s:1266` | FPRead/FPWrite: this chunk is MIN(reqCount, quantumSize) bytes |
| **`XPP_AFP_RWSIZE_SET`** | — | `0x0376DA` | `res_drvr_xpp.s:1271` | — |
| **`XPP_AFP_RWSTEP`** | — | `0x03776C` | `res_drvr_xpp.s:1342` | FPRead/FPWrite step (A3 -> rbSize / wdSize = bytes of this chunk): count the bytes; stop on an error, when cmdResult is not 0, when the chunk covers the rest of reqCount or, when reading with newLineF... |
| **`XPP_AFP_SEND`** | — | `0x0376DC` | `res_drvr_xpp.s:1273` | — |
| **`XPP_AFP_START`** | — | `0x03767E` | `res_drvr_xpp.s:1238` | — |
| **`XPP_AFP_STEP`** | — | `0x0376E0` | `res_drvr_xpp.s:1283` | XPP_AFP_STEP -- an ASP call of an AFPCommand has ended (A0 = the call, D0 = result): FPLogin/FPLoginCont go on in XPP_AFP_LOGINSTEP, FPRead/FPWrite in XPP_AFP_RWSTEP; any other command is done (XPP_AF... |
| **`XPP_AFP_WRITEMORE`** | — | `0x0377AA` | `res_drvr_xpp.s:1368` | writing: an offset from the end of the fork (startEndFlag) holds for the first chunk only; then continue at the reply's lastWritten |
| **`XPP_AFPCALL`** | — | `0x037670` | `res_drvr_xpp.s:1232` | XPP_AFPCALL -- csCode 250 afpCall (AFPCommand): map the AFP command in the first byte of the command block to ASP calls (table in the banner). csCode becomes $FF00 + the ASP csCode used, so that the e... |
| **`XPP_ANYSESS`** | — | `0x037A12` | `res_drvr_xpp.s:1721` | XPP_ANYSESS -- find a session slot in use (from the last slot down). A2 (out) -- its SCB D0 (out) -- 0 and CCR EQ when one is found; negative and NE if none Called by: E_XPP_Close, XPP_CLOSEALL |
| **`XPP_ANYSESS_FOUND`** | — | `0x037A20` | `res_drvr_xpp.s:1729` | — |
| **`XPP_ANYSESS_LOOP`** | — | `0x037A14` | `res_drvr_xpp.s:1723` | — |
| **`XPP_ATTENTION`** | — | `0x03785A` | `res_drvr_xpp.s:1464` | XPP_ATTENTION -- the server sent an Attention (A0 = scbReqPB, A2 = SCB): put the attention bytes into the SCB (scbAttnBytes), answer with an empty AddResponse (completion XPP_GETREQUEST re-arms the Ge... |
| **`XPP_ATTENTION_RTS`** | — | `0x03788E` | `res_drvr_xpp.s:1481` | — |
| **`XPP_BUILDBDS`** | — | `0x03755C` | `res_drvr_xpp.s:1071` | XPP_BUILDBDS -- build a BDS for a buffer: entries of atpMaxData (578) bytes, then one for the rest (also when it is 0 bytes, as ASP asks for one more response than the buffer holds) unless there are 8... |
| **`XPP_BUILDBDS_DIV`** | — | `0x037566` | `res_drvr_xpp.s:1075` | — |
| **`XPP_BUILDBDS_LAST`** | — | `0x037584` | `res_drvr_xpp.s:1088` | — |
| **`XPP_BUILDBDS_LOOP`** | — | `0x037570` | `res_drvr_xpp.s:1080` | — |
| **`XPP_BUILDBDS_RTS`** | — | `0x037596` | `res_drvr_xpp.s:1097` | — |
| **`XPP_CALLATP`** | — | `0x037150` | `res_drvr_xpp.s:535` | fall into XPP_CALLATP XPP_CALLATP -- issue an asynchronous .ATP Control call. A0 (in)  -- ATP parameter block (in the SCB or the CCB) D0 (in)  -- .ATP csCode A3 (in)  -- completion routine, 0 = none (... |
| **`XPP_CALLATP_NOTOPEN`** | — | `0x037170` | `res_drvr_xpp.s:547` | — |
| **`XPP_CALLATP_RTS`** | — | `0x03716E` | `res_drvr_xpp.s:545` | — |
| **`XPP_CALLDONE`** | — | `0x03732E` | `res_drvr_xpp.s:785` | XPP_CALLDONE -- an ASP call has finished with D0: if it is a step of an AFPCommand (csCode high byte $FF), go on in XPP_AFP_STEP, else complete it (XPP_COMPLETE). Branch from: XPP_UNLINKDONE (fall-thr... |
| **`XPP_CALLHOOK`** | — | `0x0370D2` | `res_drvr_xpp.s:438` | XPP_CALLHOOK -- call the AGB's xppHook if a patch installed one (A0 and A1 as the hook's caller has them). Changes D3, A2. Called by: E_XPP_Control, XPP_AFP_STEP |
| **`XPP_CALLHOOK_RTS`** | — | `0x0370E2` | `res_drvr_xpp.s:445` | — |
| **`XPP_CLOSE_NOSESS`** | — | `0x0370EE` | `res_drvr_xpp.s:458` | — |
| **`XPP_CLOSEALL`** | — | `0x037100` | `res_drvr_xpp.s:474` | XPP_CLOSEALL -- csCode 247 closeAll (ASPCloseAll): close every session. Takes the first slot in use, starts closing it (XPP_STARTCLOSE) and returns; when that session is closed, XPP_WSSCLOSED comes ba... |
| **`XPP_CLOSESESS`** | — | `0x037350` | `res_drvr_xpp.s:816` | XPP_CLOSESESS -- csCode 254 closeSess (ASPCloseSession), also FPLogout and the end of a failed FPLogin: close the session sessRefnum. The call leaves the I/O queue and waits on the session's list; the... |
| **`XPP_CLOSEWSS`** | — | `0x037428` | `res_drvr_xpp.s:918` | XPP_CLOSEWSS -- (A0 = scbATPPB) all calls ended: close the workstation session socket (this also ends the GetRequest on it); continued in XPP_WSSCLOSED. |
| **`XPP_CMDREPLY`** | — | `0x03751C` | `res_drvr_xpp.s:1039` | XPP_CMDREPLY -- completion of a Command/Write request (A0 = the CCB's ATP pb, D0 = result): reply size into rbSize (XPP_REPLYSIZE), the first reply packet's user bytes into cmdResult. reqAborted (the ... |
| **`XPP_CMDREPLY_DONE`** | — | `0x037558` | `res_drvr_xpp.s:1057` | — |
| **`XPP_CMDREPLY_OK`** | — | `0x03753E` | `res_drvr_xpp.s:1050` | — |
| **`XPP_COMPLETE`** | — | `0x037336` | `res_drvr_xpp.s:795` | XPP_COMPLETE -- complete a call that has left the I/O queue: ioResult Preserves D1-D3/A0-A3. Branch from: XPP_CALLDONE (fall-through), XPP_STATUSREPLY, XPP_AFP_DONE |
| **`XPP_COMPLETE_EXIT`** | — | `0x03734A` | `res_drvr_xpp.s:803` | — |
| **`XPP_CTL_DISPATCH`** | — | `0x03709C` | `res_drvr_xpp.s:408` | — |
| **`XPP_CTL_TABLE`** | — | `0x0370C0` | `res_drvr_xpp.s:422` | dispatch table: handler offsets from the driver start, csCode 247..255 |
| **`XPP_DEQUEUE`** | — | `0x037598` | `res_drvr_xpp.s:1120` | XPP_DEQUEUE -- detach the call A0 from the head of the driver's I/O queue and mark the driver not busy, so that the next queued call can start: if there is one, it is started here (E_XPP_Control, recu... |
| **`XPP_DEQUEUE_NEXT`** | — | `0x0375B4` | `res_drvr_xpp.s:1129` | — |
| **`XPP_DEQUEUE_RTS`** | — | `0x0375D8` | `res_drvr_xpp.s:1142` | — |
| **`XPP_DONE`** | — | `0x03719E` | `res_drvr_xpp.s:582` | XPP_DONE -- complete the call at the head of the driver's I/O queue through jIODone (sets ioResult, calls ioCompletion, starts the next queued call). D0 (in) -- result code Branch from: XPP_CTL_DISPAT... |
| **`XPP_DONE_NOERR`** | — | `0x03719C` | `res_drvr_xpp.s:571` | complete the call at the head of the I/O queue with noErr Branch from: XPP_CLOSEALL; completion routine of XPP_ABORTOS |
| **`XPP_DONEFIRST`** | — | `0x037310` | `res_drvr_xpp.s:762` | complete the session's first call (the open call) with D0 XPP_DONEFIRST -- complete the first call of the session's list. XPP_UNLINKDONE -- take the call A0 off the list of the session A2 and complete... |
| **`XPP_DOOPEN`** | — | `0x0371C4` | `res_drvr_xpp.s:623` | XPP_DOOPEN -- open a session (OpenSession, FPLogin). A0 (in) -- the XPP parameter block (aspTimeout, aspRetry) A2 (in) -- SCB, D3 (in) -- server's SLS address, D2 (in) -- attention routine Takes a ses... |
| **`XPP_ERRDONE`** | — | `0x0371AA` | `res_drvr_xpp.s:596` | XPP_ERRDONE -- complete a call with an error found when it is started: an AFPCommand gets its csCode (afpCall) back first. Goes through jIODone, i.e. assumes the call is still at the head of the I/O q... |
| **`XPP_FINDSESS`** | — | `0x037968` | `res_drvr_xpp.s:1608` | XPP_FINDSESS -- look up a session by its sessRefnum. D1 (in)  -- sessRefnum (generation << 8 + 4 * slot) A2 (out) -- its SCB (when the slot is in use) D0 (out) -- noErr (session open), aspSessClosed (... |
| **`XPP_FINDSESS_BAD`** | — | `0x03799E` | `res_drvr_xpp.s:1629` | — |
| **`XPP_FINDSESS_EXIT`** | — | `0x03799A` | `res_drvr_xpp.s:1626` | — |
| **`XPP_FREESESS`** | — | `0x0379EA` | `res_drvr_xpp.s:1689` | XPP_FREESESS -- free the session slot of the SCB A2. D0 (out) -- 0 when found (else negative). Changes A1. Called by: XPP_OPENFAIL, XPP_WSSCLOSED |
| **`XPP_FREESESS_FOUND`** | — | `0x0379F8` | `res_drvr_xpp.s:1697` | — |
| **`XPP_FREESESS_LOOP`** | — | `0x0379EC` | `res_drvr_xpp.s:1691` | — |
| **`XPP_GETPARMS`** | — | `0x037182` | `res_drvr_xpp.s:562` | XPP_GETPARMS -- csCode 249 getParms (ASPGetParms): return aspMaxCmdSize |
| **`XPP_GETREQUEST`** | — | `0x037890` | `res_drvr_xpp.s:1490` | XPP_GETREQUEST -- issue the GetRequest on the WSS that receives the server's requests (2-byte buffer at scbWrBSize); completion XPP_SRVREQ. A0 (in) -- scbReqPB (atpSocket = WSS, reqPointer set) Called... |
| **`XPP_GETSTATUS`** | — | `0x0375DC` | `res_drvr_xpp.s:1153` | XPP_GETSTATUS -- csCode 251 getStatus (ASPGetStatus): ask the server at serverAddr (its SLS) for its status block, no session needed: SendRequest ALO, user bytes [aspGetStat, 0, 0], aspTimeout/aspRetr... |
| **`XPP_GETVARS`** | — | `0x03795E` | `res_drvr_xpp.s:1592` | XPP_GETVARS -- A1 (out) = the driver variables (AGB xppVarPtr). Called by: XPP_GETPARMS, XPP_DONE, XPP_DEQUEUE, XPP_LASTSLOT |
| **`XPP_GETWRPB`** | — | `0x03794E` | `res_drvr_xpp.s:1581` | XPP_GETWRPB -- the write data ATP pb of a UserWrite call: after the CCB's request pb and its reply BDS (numOfBuffs entries). A0 (in)  -- the UserWrite call;  A1 (out) -- write data ATP pb Changes D3. ... |
| **`XPP_KILLSENDREQ`** | — | `0x037148` | `res_drvr_xpp.s:515` | fall into XPP_KILLSENDREQ: cancel the OpenSess request (A1) XPP_KILLSENDREQ -- issue .ATP KillSendReq: cancel the SendRequest or NSendRequest of the ATP pb A1 (it completes with reqAborted). A0 (in) -... |
| **`XPP_KILLTICKLE`** | — | `0x037370` | `res_drvr_xpp.s:835` | — |
| **`XPP_LASTSLOT`** | — | `0x0379DC` | `res_drvr_xpp.s:1676` | XPP_LASTSLOT -- A1 (out) = driver variables, D0 (out) = offset of the last session slot in xppSessTbl: 4 * (xppMaxSess - 1). Called by: XPP_FINDSESS, XPP_NEWSESS, XPP_FREESESS, XPP_ANYSESS |
| **`XPP_LINKCALL`** | — | `0x037A00` | `res_drvr_xpp.s:1707` | XPP_LINKCALL -- put the call A0 at the head of the active-call list of the session A2 (through its qLink), interrupts off. Called by: XPP_CLOSESESS, XPP_USERCMD_SEND |
| **`XPP_NEWSESS`** | — | `0x0379A4` | `res_drvr_xpp.s:1643` | XPP_NEWSESS -- take a free session slot for the SCB A2: store the SCB in it, clear the SCB (186 bytes, up to scbAttnRtn) and put the new sessRefnum = generation << 8 + 4 * slot into scbRefnum. The gen... |
| **`XPP_NEWSESS_CLEAR`** | — | `0x0379CC` | `res_drvr_xpp.s:1661` | — |
| **`XPP_NEWSESS_EXIT`** | — | `0x0379D6` | `res_drvr_xpp.s:1666` | — |
| **`XPP_NEWSESS_FOUND`** | — | `0x0379C2` | `res_drvr_xpp.s:1656` | — |
| **`XPP_NEWSESS_LOOP`** | — | `0x0379B2` | `res_drvr_xpp.s:1649` | — |
| **`XPP_OPEN_EXIT`** | — | `0x03708E` | `res_drvr_xpp.s:391` | — |
| **`XPP_OPEN_HAVEAGB`** | — | `0x037056` | `res_drvr_xpp.s:369` | — |
| **`XPP_OPEN_NOERR`** | — | `0x03708C` | `res_drvr_xpp.s:389` | — |
| **`XPP_OPENED`** | — | `0x03729C` | `res_drvr_xpp.s:720` | XPP_OPENED -- the server accepted the session (A0 = scbReqPB, A1 -> user bytes 2 of the OpenSessReply at scbAuxPB): take the session ID and the server session socket (SSS), start listening on the WSS ... |
| **`XPP_OPENFAIL`** | — | `0x037292` | `res_drvr_xpp.s:707` | — |
| **`XPP_OPENFAIL_CLOSED`** | — | `0x03728A` | `res_drvr_xpp.s:704` | XPP_OPENFAIL_CLOSED -- completion of CloseATPSkt after a failed open (A0 = scbReqPB): fail the open with the saved result. XPP_OPENFAIL -- free the session slot, complete the open call with D0. |
| **`XPP_OPENREPLY`** | — | `0x03724A` | `res_drvr_xpp.s:677` | XPP_OPENREPLY -- completion of the OpenSess request (A0 = scbReqPB): the OpenSessReply's user bytes are in the BDS at scbAuxPB. Error codes: reqFailed (no answer) -> aspNoServers; AbortOS -> reqAborte... |
| **`XPP_OPENREPLY_CLOSE`** | — | `0x037274` | `res_drvr_xpp.s:692` | — |
| **`XPP_OPENREPLY_ERR`** | — | `0x03726A` | `res_drvr_xpp.s:688` | — |
| **`XPP_OPENSESS`** | — | `0x0371B8` | `res_drvr_xpp.s:607` | XPP_OPENSESS -- csCode 255 openSess (ASPOpenSession): open a session with the server at serverAddr, using the caller's SCB (scbPointer) and attention routine (attnRoutine), aspTimeout and aspRetry. |
| **`XPP_REPLYSIZE`** | — | `0x03762E` | `res_drvr_xpp.s:1198` | XPP_REPLYSIZE -- after a request with a reply BDS: rbSize = 578 * (responses - 1) + bytes in the last response; aspBufTooSmall if that response did not fit its buffer (counted up to the buffer size). ... |
| **`XPP_REPLYSIZE_MAP`** | — | `0x037664` | `res_drvr_xpp.s:1217` | — |
| **`XPP_REPLYSIZE_RTS`** | — | `0x03766E` | `res_drvr_xpp.s:1221` | — |
| **`XPP_REPLYSIZE_SUM`** | — | `0x03765A` | `res_drvr_xpp.s:1213` | — |
| **`XPP_RETURN`** | — | `0x037478` | `res_drvr_xpp.s:960` | Branch from: XPP_WSSCLOSED_NOATTN, XPP_CMDREPLY_OK |
| **`XPP_SESSTIMEOUT`** | — | `0x03784C` | `res_drvr_xpp.s:1452` | — |
| **`XPP_SRVCLOSE`** | — | `0x037812` | `res_drvr_xpp.s:1424` | XPP_SRVCLOSE -- the server sent CloseSess (A0 = scbReqPB, A2 = SCB): unless the session is already closing, answer it with an empty SendResponse (one 0-byte BDS entry at scbAuxPB); then XPP_SRVCLOSE_R... |
| **`XPP_SRVCLOSE_REPLIED`** | — | `0x037846` | `res_drvr_xpp.s:1449` | XPP_SRVCLOSE_REPLIED -- completion of the CloseSess response (A0 = scbReqPB): stop the session timer, then as at a timeout: XPP_SESSTIMEOUT -- VBL task of the session timer (A0 = scbVBL): nothing hear... |
| **`XPP_SRVREQ`** | — | `0x0377C8` | `res_drvr_xpp.s:1388` | XPP_SRVREQ -- completion of the GetRequest on the WSS (A0 = scbReqPB): a request from the server. It counts only with the session's ID and from the server's node (and net, when both nets are known); t... |
| **`XPP_SRVREQ_IGNORE`** | — | `0x03780E` | `res_drvr_xpp.s:1412` | — |
| **`XPP_SRVREQ_NODE`** | — | `0x0377EC` | `res_drvr_xpp.s:1400` | — |
| **`XPP_SRVREQ_RTS`** | — | `0x037810` | `res_drvr_xpp.s:1414` | — |
| **`XPP_STARTCLOSE`** | — | `0x03736A` | `res_drvr_xpp.s:832` | XPP_STARTCLOSE -- begin to close the session A2 (state ssClosing): stop the session timer, then XPP_KILLTICKLE -- (session timer already gone) cancel the tickle on scbATPPB with a KillSendReq on scbAu... |
| **`XPP_STATUSREPLY`** | — | `0x037628` | `res_drvr_xpp.s:1184` | XPP_STATUSREPLY -- completion of GetStatus (A0 = the CCB's ATP pb): reply size into rbSize, complete the call (reqFailed -> aspNoServers). |
| **`XPP_TICKLEKILLED`** | — | `0x037380` | `res_drvr_xpp.s:849` | XPP_TICKLEKILLED -- completion of the tickle's KillSendReq (A0 = scbAuxPB). Unless the server closed the session or it timed out (ssDead), send CloseSess to the server's SSS: SendRequest ALO, user byt... |
| **`XPP_UNLINKDONE`** | — | `0x037314` | `res_drvr_xpp.s:764` | — |
| **`XPP_UNLINKDONE_FOUND`** | — | `0x037328` | `res_drvr_xpp.s:774` | — |
| **`XPP_UNLINKDONE_LOOP`** | — | `0x037320` | `res_drvr_xpp.s:769` | — |
| **`XPP_USERCMD`** | — | `0x03747A` | `res_drvr_xpp.s:977` | XPP_USERCMD -- csCode 253 userCommand (ASPUserCommand) and csCode 252 userWrite (ASPUserWrite), also the ASP calls of AFPCommand: send the command block (cbSize, cbPtr) to the server's SSS as an ASP C... |
| **`XPP_USERCMD_SEND`** | — | `0x0374F0` | `res_drvr_xpp.s:1016` | — |
| **`XPP_WRITECONT`** | — | `0x0378A2` | `res_drvr_xpp.s:1504` | XPP_WRITECONT -- the server sent WriteContinue (A0 = scbReqPB, A2 = SCB, request data scbWrBSize = buffer size at the server): find the UserWrite with this sequence number and send it its write data a... |
| **`XPP_WRITECONT_FIND`** | — | `0x0378B0` | `res_drvr_xpp.s:1509` | — |
| **`XPP_WRITECONT_REARM`** | — | `0x03792A` | `res_drvr_xpp.s:1548` | — |
| **`XPP_WRITECONT_SIZE`** | — | `0x0378D2` | `res_drvr_xpp.s:1522` | — |
| **`XPP_WRITEDATA_SENT`** | — | `0x037930` | `res_drvr_xpp.s:1561` | XPP_WRITEDATA_SENT -- completion of the write data response (A0 = write data pb, reqPointer = the UserWrite call). If the Write's request has already finished (reply in), complete the call now with th... |
| **`XPP_WRITEDATA_SENT_EXIT`** | — | `0x03794A` | `res_drvr_xpp.s:1570` | — |
| **`XPP_WSSCLOSED`** | — | `0x03743A` | `res_drvr_xpp.s:931` | XPP_WSSCLOSED -- completion of the WSS's CloseATPSkt (A0 = scbATPPB): the session is gone. Free the slot, call the attention routine with D0 = sessRefnum, D1 = 0 (session closed), then: ssDead -> done... |
| **`XPP_WSSCLOSED_NOATTN`** | — | `0x037464` | `res_drvr_xpp.s:945` | — |
| **`XPP_WSSOPENED`** | — | `0x0371F8` | `res_drvr_xpp.s:645` | XPP_WSSOPENED -- completion of OpenATPSkt (A0 = scbReqPB, D0 = result): send OpenSess to the server's SLS: SendRequest XO, user bytes [aspOpenSess, WSS, aspVersion], no data, one response buffer of 0 ... |
| **`YFg`** | — | `0x039FC0` | `res_font_chicago.s:163` | — |

---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

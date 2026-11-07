# Toolbox & QuickDraw Graphics Subsystem

## 1. Overview of the Macintosh Toolbox

While the operating system kernel manages memory, files, and low-level hardware devices, the **Macintosh Toolbox** provides the high-level graphics and user interface architecture that defined the GUI revolution.

Built directly on top of **QuickDraw**, the Toolbox is structured in hierarchical layers:

```
+---------------------------------------------------------------+
| Dialog Manager / TextEdit / Desk Manager / Scrap Manager      |
+---------------------------------------------------------------+
| Control Manager / Menu Manager / Window Manager               |
+---------------------------------------------------------------+
| Font Manager & Resource Manager                               |
+---------------------------------------------------------------+
| QuickDraw Graphics Engine (GrafPort, BitBlt, Regions, Shapes) |
+---------------------------------------------------------------+
| OS Kernel (Trap Dispatcher, Memory Mgr, Device Mgr, File Mgr) |
+---------------------------------------------------------------+
```

---

## 2. QuickDraw: The Core 2D Graphics Engine

Written by Bill Atkinson in pure 68000 assembly, **QuickDraw** (`plus/toolbox/quickdraw/*` and `se/toolbox/quickdraw/*`) is a high-speed, integer-based 2D vector and raster graphics library capable of rendering complex clipped regions at CRT refresh speeds.

### 2.1 Foundational Data Structures
- **`Point`**: 4 bytes (two 16-bit integers: `v` [vertical row] and `h` [horizontal column]).
- **`Rect`**: 8 bytes (two points: `top`, `left`, `bottom`, `right`).
- **`Pattern`**: 8 bytes (an 8x8 pixel 1-bit monochrome tile pattern).
- **`BitMap`**:
  - `baseAddr` (`Ptr`): Pointer to the first byte of pixel data.
  - `rowBytes` (`Integer`): Number of bytes per horizontal scanline (must be even).
  - `bounds` (`Rect`): Bounding rectangle establishing local coordinate space.

### 2.2 The Graphics Port (`GrafPort`)
All QuickDraw drawing operations occur within an active **`GrafPort`** (`thePort` at `-4(A5)`). A GrafPort encapsulates the entire drawing environment:
- Pen size, pen location, pen pattern, and pen transfer mode.
- Foreground and background patterns.
- Text font, size, style (Bold, Italic, Underline), and character spacing.
- **`portRect`**: Bounding rectangle of the port.
- **`visRgn`**: Visible region (the portion of the port not obscured by overlapping windows or desktop bounds).
- **`clipRgn`**: Application-defined clipping boundary. QuickDraw strictly clips all drawing to the intersection of `visRgn` and `clipRgn`.

---

## 3. BitBlt: Bit Boundary Block Transfer (`BitBlt.s`)

The core primitive of raster graphics is **`BitBlt`** (`BitBlt.s`). It copies rectangular pixel blocks between any two bitmaps with arbitrary bit-level alignment:

```
Source Bitmap  -----\
                     \---> [ Boolean Transfer Mode ] ---> Destination Bitmap
Pattern / Mask -----/       (srcCopy, srcOr, srcXor, srcBic)
```

### The 8 Transfer Modes
1. **`srcCopy` (`0`)**: Destination = Source. Completely replaces background pixels.
2. **`srcOr` (`1`)**: Destination = Destination OR Source. Overlays black pixels (transparent white).
3. **`srcXor` (`2`)**: Destination = Destination XOR Source. Inverts overlapping pixels.
4. **`srcBic` (`3`)**: Destination = Destination AND NOT Source (Bit Clear). Erases pixels where source is black.
5. **`notSrcCopy` (`4`)** through **`notSrcBic` (`7`)**: Inverted source variants.

The assembly implementation unrolls barrel-shift instructions (`LSL.L` / `LSR.L`) and 32-bit longword writes to achieve near memory-bandwidth transfer speeds on the 8 MHz 68000 bus.

---

## 4. Region Geometry & Inversion Lists (`Regions.s`)

QuickDraw's most revolutionary innovation was the **Region (`RgnHandle`)**. A region can describe an arbitrary, non-convex 2D shape composed of multiple disjoint polygons, curved edges, and interior holes:

```
Region Data Structure:
+--------------------+--------------------+
| rgnSize (2 bytes)  | Total bytes in region record (10 for simple rect)
+--------------------+--------------------+
| rgnBBox (8 bytes)  | Bounding box rectangle encompassing all pixels
+--------------------+--------------------+
| Inversion List: Array of scanline coordinate descriptors...
| Vertical scanline Y, followed by pairs of Left and Right X coordinates,
| terminated by special sentinel flag $7FFF.
+-----------------------------------------+
```

### Region Operations
- **`NewRgn`** / **`DisposeRgn`**: Allocates or frees region handles in the heap.
- **`RectRgn`** / **`SetRectRgn`**: Defines a rectangular region.
- **`OpenRgn`** / **`CloseRgn`**: Begins recording line drawing and curves into an arbitrary region outline.
- **Boolean Set Math (`RgnOp.s`)**:
  - `UnionRgn`: $A \cup B$ (Combines two regions).
  - `SectRgn`: $A \cap B$ (Calculates geometric intersection).
  - `DiffRgn`: $A \setminus B$ (Subtracts one region from another).
  - `XorRgn`: $(A \setminus B) \cup (B \setminus A)$ (Calculates difference).

---

## 5. Shape Drawing Primitives

QuickDraw supports five standard mathematical geometric shapes across five standard drawing verbs:

```
                  Frame    Paint    Erase    Invert    Fill
                  -----    -----    -----    ------    ----
Rectangle         FrameRect PaintRect EraseRect InvertRect FillRect
Rounded Rect      FrameRoundRect ...
Oval / Ellipse    FrameOval ...
Arc / Wedge       FrameArc ...
Polygon           FramePoly ...
Region            FrameRgn  PaintRgn EraseRgn InvertRgn FillRgn
```

- **`Frame`**: Draws an outline using current pen dimensions and pattern.
- **`Paint`**: Fills interior with active pen pattern.
- **`Erase`**: Fills interior with background pattern (typically solid white).
- **`Invert`**: Flips all black pixels to white and white to black.
- **`Fill`**: Fills interior with an arbitrary specified pattern.

---

## 6. High-Level Toolbox User Interface Managers

### 6.1 Window Manager (`window_mgr.s`)
- Creates and manages overlapping rectangular screen surfaces.
- Manages window z-ordering (front-to-back linked list of `WindowRecord` structures).
- Automatically computes update regions (`updateRgn`) when windows move or are resized, generating `updateEvt` events for applications.
- Traps: `_NewWindow`, `_SelectWindow`, `_ShowWindow`, `_BringToFront`, `_FindWindow`, `_TrackGoAway`, `_DragWindow`.

### 6.2 Menu Manager (`menu_mgr.s`)
- Displays and animates the global desktop menu bar.
- Tracks mouse dragging down menus, highlights selected items, and decodes Command-key equivalents.
- Traps: `_InitMenus`, `_InsertMenu`, `_DrawMenuBar`, `_MenuSelect`, `_MenuKey`, `_HiliteMenu`.

### 6.3 Control Manager (`control_mgr.s`)
- Manages on-screen interactive controls: pushbuttons, checkboxes, radio buttons, and scroll bars.
- Handles hit testing and visual feedback (inverting pressed buttons, sliding scrollbar thumb).
- Traps: `_NewControl`, `_DrawControls`, `_FindControl`, `_TrackControl`, `_GetCtlValue`, `_SetCtlValue`.

### 6.4 Dialog Manager (`dialog_mgr.s`)
- Manages modal and modeless dialog boxes and system alert windows.
- Automatically handles tab key cycling, default buttons, and static text display from `'DITL'` (Dialog Item List) resources.
- Traps: `_GetNewDialog`, `_ModalDialog`, `_Alert`, `_StopAlert`, `_NoteAlert`, `_CautionAlert`.

### 6.5 TextEdit (`textedit.s`)
- Full-featured single-styled text editor engine.
- Supports word wrapping, cursor placement, text selection with inverse highlighting, cut/copy/paste, and backspace deletion.
- Traps: `_TEInit`, `_TENew`, `_TEClick`, `_TEKey`, `_TECut`, `_TECopy`, `_TEPaste`, `_TEUpdate`.

### 6.6 Resource Manager (`resource_mgr.s`)
- Central database engine for loading application resources (windows, menus, icons, sounds, fonts, dialogs) by 4-byte Type and 16-bit ID.
- Traps: `_OpenResFile`, `_CloseResFile`, `_GetResource`, `_ReleaseResource`, `_WriteResource`, `_ChangedResource`.


---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

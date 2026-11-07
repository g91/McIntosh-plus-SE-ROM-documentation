# Event, Vertical Blanking (VBL) & Time Managers

## 1. Event Manager & The System Event Queue

The **Event Manager** (`plus/os/event_mgr.s` and `se/os/event_mgr.s`) provides the event-driven backbone of the Macintosh user interface. User actions (keystrokes, mouse clicks, mouse movements, disk insertions) and system notifications (window activations, update events) are queued as asynchronous **Event Records** for sequential processing by application main loops.

---

## 2. Event Records & The Event Queue Structure

Low-memory global `EventQueue` (`$014A`) contains the header of the circular event queue:
- Holds up to 20 event elements in low memory buffer `SysEvtBuf` (`$0146`).
- Queue size is tracked by `EvtBufCnt` (`$0154`).

### The Event Record (`EventRecord` - 16 bytes)
```
Offset  Field      Type      Description
------  ---------  --------  -------------------------------------------------------------
$00     what       Word      Event type ID (0 to 15)
$02     message    LongInt   Event-specific data (e.g. keycode/ASCII, window ptr, drive #)
$06     when       LongInt   Timestamp of occurrence in ticks (60ths of a second since boot)
$0A     where      Point     Global mouse cursor position (v: Integer, h: Integer)
$0E     modifiers  Word      Keyboard modifier flags (Command, Shift, Option, CapsLock)
```

### Event Type Enumeration
- `0` (`nullEvt`): No events pending; application can perform background processing.
- `1` (`mouseDown`): Mouse button transitioned from up to down.
- `2` (`mouseUp`): Mouse button released.
- `3` (`keyDown`): Key pressed on keyboard or keypad.
- `4` (`keyUp`): Key released.
- `5` (`autoKey`): Key held down beyond repeat threshold.
- `6` (`updateEvt`): Window requires visual redrawing.
- `7` (`diskEvt`): 3.5" disk inserted into floppy drive (`message` contains drive # and error).
- `8` (`activateEvt`): Window gaining or losing active status.
- `10` (`networkEvt`): High-priority AppleTalk network packet received.
- `11` (`driverEvt`): I/O driver notification.
- `12` - `15` (`app1Evt` - `app4Evt`): Application-defined custom events.

### Core Event Manager Traps
- **`PostEvent`** (`$A02F`):
  - *Entry*: `A0` = Event code, `D0` = Message longword. Inserts an event into the system queue.
- **`GetOSEvent`** (`$A031`) & **`OSEventAvail`** (`$A030`):
  - *Entry*: `D0.W` = Event mask, `A0` = Pointer to `EventRecord`.
  - *Operation*: Dequeues or inspects the highest priority matching event in the queue.
- **`FlushEvents`** (`$A032`):
  - Purges events matching a specific event mask (e.g. discarding lingering keystrokes before dialogs).

---

## 3. The Vertical Blanking (VBL) Manager (`os/vbl_mgr.s`)

The Macintosh video electron beam sweeps across the CRT 60 times per second (approx. 60.15 Hz on Plus, 60.7 Hz on SE). When the beam finishes the bottom scanline and returns to the top of the screen (the **Vertical Blanking Interval**), the VIA generates a Level 1 interrupt.

The **VBL Manager** executes high-frequency, jitter-free background tasks during this interval:
- Tracks mouse movements and updates the hardware cursor coordinates.
- Animates the cursor (e.g. rotating watch or spinning beachball).
- Handles keyboard auto-repeat timing.
- Dispatches queued periodic tasks without preempting user application logic.

### The VBL Task Record (`VBLTask` - 14 bytes)
```
Offset  Field      Type     Description
------  ---------  -------  -------------------------------------------------------------
$00     qLink      Ptr      Pointer to next VBLTask in queue
$04     qType      Word     Queue type identifier (ORD(vType) = 1)
$06     vblAddr    ProcPtr  Pointer to task handler routine
$08     vblCount   Word     Number of ticks remaining until next execution
$0A     vblPhase   Word     Task phase offset (distributes load across frames)
```

### VBL Manager Traps
- **`VInstall`** (`$A033`):
  - *Entry*: `A0` = Pointer to `VBLTask`. Inserts task into `VBLQueue` (`$0160`).
- **`VRemove`** (`$A034`):
  - *Entry*: `A0` = Pointer to `VBLTask`. Removes task from active execution queue.

---

## 4. The Time Manager (`os/time_mgr.s`)

While the VBL Manager operates at 60 Hz (16.6 ms resolution), high-performance networking, audio synthesis, and real-time protocol engines require sub-millisecond precision.

The **Time Manager** (`plus/os/time_mgr.s` and `se/os/time_mgr.s`) provides interrupt-driven timer services measured in **microseconds**:
- Uses VIA Timer 1 and Timer 2 hardware latches.
- Maintains a priority queue of scheduled tasks sorted by earliest expiration timestamp.
- Executes tasks at interrupt level (IPL 1) when the timer fires.

### The Time Manager Task Record (`TMTask` - 10 bytes)
```
Offset  Field     Type     Description
------  --------  -------  -------------------------------------------------------------
$00     qLink     Ptr      Pointer to next TMTask in queue
$04     qType     Word     Queue type
$06     tmAddr    ProcPtr  Pointer to timer callback routine
$0A     tmCount   LongInt  Delay remaining in milliseconds (or negative microseconds)
```

### Time Manager Traps
- **`InsTime`** (`$A058`):
  - Installs a task record into the Time Manager queue.
- **`PrimeTime`** (`$A05A`):
  - Activates the timer for a specific duration:
    - Positive value: Delay in **milliseconds**.
    - Negative value: Delay in **microseconds** (e.g. `-1000` = 1 millisecond).
- **`RmvTime`** (`$A059`):
  - Removes an active or pending task from the queue.


---
*Macintosh Plus & SE ROM Kernel Wiki — Generated from bit-identical 68000 assembly source tree.*
[Back to Wiki Home](Home) • [Repository Root](../README.md)

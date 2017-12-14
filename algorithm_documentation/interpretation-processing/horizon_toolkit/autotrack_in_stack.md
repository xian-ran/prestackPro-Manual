#### AutoTrack in Stack {#autotrack-in-stack}

This application is a **seed point based** Auto-Tracker, creating time horizons.

Seeds can be input 1 by 1 on any vertical stack, seismic view – inline, crossline or arbitrary line. Also on a single offset or angle plane in a vertical seismic view, but the Auto-Tracking itself only works on stack volumes.

![](/assets/cusersjohanndesktopmanual-40-.png)

MB3, brings up a seismic view context menu which enables creation of a seed point file and the placing of seed points using Ctrl MB1\.

AutoTrack utilises a very fast algorithm, designed from the outset for interactive stack and pre-stack tracking, allowing different tracking runs to be compared immediately, using AutoTrack’s sync to Map and Seismic Views.

| ![](/assets/cusersjohanndesktopmanual-40-.png) |
| --- | --- |

Time slices, previously tracked horizons and attribute maps can all help the interpreter place a few key seed points; inside fault blocks, in good seismic quality zones and away from likely tracking problem areas.

| ![](/assets/cusersjohanndesktopmanual-40-.png) | The user is given the choice of how many of these tracking run results to keep in memory for making comparisons ( default is to keep the last 5 ) and is allowed to “undo” or “go-back to” any previous step in the list by simply selecting an Auto-tracking result and then running the next auto-track operation. |
| --- | --- |
|  |  |

This Auto-Tracker allows snap to and track of seismic trace peaks, troughs and zero-crossings ; but is not designed for following constant values in non seismic volumes such as PCube Vp, Vs, density output data.

Times are picked either to nearest sample time or to ¼ sample rate if the subsample option is selected.

Control of the tracker’s picking of an event is by :

| ![](/assets/cusersjohannappdatalocalmicro.png) |
| --- |
| 1) the choice of voxel or correlation method, |
| ![](/assets/cusersjohannappdatalocalmicro.png) |
| 2) Max Z jump allowed between picks, and |

Control of spatial growing, or the “expansion quality” of horizons; away from input seed points is from :

1.  Seed point placing, 2) 2D tiles, 3x3 or 5x5 within which all traces must be trackable from the latest seed trace and 3) Map polygons, inclusive and exclusive.

![](/assets/cusersjohanndesktopmanual-40-.png)

Single voxel tracking is faster and can be better at staying on a peak or trough but not necessarily the right one.

| ![](/assets/cusersjohannappdatalocalmicro.png) | Correlation over a time window is slower, can be better at following the right target event if stronger parallel events can guide the tracker, but aren’t always on the event peak or trough if a nearby dominant event is not quite parallel. |
| --- | --- |

Auto-Tracker also allows **“clean up”** of tracked maps/horizons using

1.  Tracking path, delete children – surgically removing points picked after mistracking occurs; using Ctrl MB1 to select a path, Shift MB1 to highlight the child picks for deletion and then Ctrl Del to remove them.

| ![](/assets/cusersjohanndesktopmanual-40-.png) |
| --- | --- |

| ![](/assets/cusersjohanndesktopmanual-40-.png) |
| --- |
| Map View with tracked horizon, tracked path and blue area of child picks |

1.  Map polygon delete – using &lt;Horizon Tools&gt; &lt;Remove selection&gt; and
2.  Map polygon keep – rerunning the tracking run but constraining picks to be within an inclusive polygon.

Fill in of non-tracked zones, inside a tracked zone, can be achieved by “locking” the tracked “cleaned up” picks from the last run, placing a seed in the to be tracked zone and an inclusive polygon around it to restrict it’s tracking to within the no pick area.

A polygon takes priority over a “locked area”.

This means you can retrack a locked area if a polygon overlaps it and a new seed tracks into the locked area. → Place inclusive polygons with care.

**Tracking workflow ideas :**

1.  Always use a minimum of seed points

This allows the tracker, freedom to work.

Inputting more points than necessary, takes time and increases the chance of the interpreter making a mistake by misplacing a seed on a doublet or across a fault for example.

It also makes “clean up” harder as tracking paths become shorter and picking zones shrink as more and more points compete with one another to pick any particular trace.

1.  Start with 1 point or just a few points / fault block or good seismic zone.

Add extra, single seeds, only where required, because the resulting map has holes or mispicks. These are input best using arbitrary seismic lines.

1.  Keep rerunning the tracking calculation each time new seeds are added

Until a majority of the area has been tracked and areas left can be “filled in” or interpolated, through the use of gridding, later.

1.  Only then undertake a clean up operation

Using delete children or map polygon delete and fix the result after “clean up” in the interactive result list, by making it NEW and in the project, by saving it to disk.

1.  After “clean up”, lock the horizon and use an inclusive map polygon to “fill in” holes until as much tracking as possible is done.
2.  Use Despike and ABOS Gridding, within an inclusive map polygon of the whole tracked area to finish the tracked horizon and make it ready for input to Pre-Stack, Extend Horizon tracking and Map attribute calculations.

**Tracking extra Q.C. maps :**

| ![](/assets/cusersjohannappdatalocalmicro.png) |
| --- |
| Horizon Tool, Auto-Tracker Q.C. Output maps selection |

|  |
| --- |
| Picked event Times Q.C. Ancester seed |

|  |
| --- |
| Picked event Amplitude Restrictivity Threshold |

|  |
| --- |
| Q.C. Tracking path length Q.C. Tracking Direction |
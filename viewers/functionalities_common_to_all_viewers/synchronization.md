### Synchronization {#synchronization}

All 2D Viewers can be synchronized, including viewers of different types \(e.g. it is possible to synchronize a stack viewer with a map viewer, to display data extent and cursor position readouts on the map\).

Synchronization is mono-directional: If viewer 1 is synchronized to viewer 2 changes in viewer 1 will be reflected in viewer 2, but modifications on viewer 2 will not affect viewer 1.

To synchronize a viewer to another one, click the synchronize icon ![](/assets/001_sync.png) in viewer 1 and click anywhere inside viewer 2. A list of possible items to synchronize will open and the user must tick the desired options. This list differs depending on the type of the two viewers. Here is an explanation for each item that is possible to synchronize:

* **Slice selection:** selection of the current displayed section \(inline/crossline numbers, time selection for time-slices\)
* **Subclass selection:** for viewers with two selections, this synchronizes the second class \(constant offset or angles for example\)
* **Decimation:** the decimation factor used for the display \(gather data\)
* **XAxis Configuration:** direction of increasing index for the XAxis
* **YAxis Configuration:** direction of increasing index for the YAxis
* **XAxis data type:** setup of XAxis for pre-stack map view \(Inline/Crossline\)
* **Gather Size:** for pre-stack viewers only, zoom factor for the extra pre-stack axis \(offset/angles\)
* **Interpolation:** pixel interpolation settings
* **Window size:** the size of the viewer window
* **Vertical view:** vertical axis zoom and limits
* **Horizontal view:** horizontal axis zoom and limits
* **View:** both horizontal and vertical axis zoom and limits
* **Read-out position:** NOTE- crosshairs must be active for both viewers
* **CDP Positions:** on a Map viewer, will mark the positions of the CDPs in the display of a sync’d Stack or Gather viewer
* **North Orientation:** survey orientation or “World View”
* **Jump to Sample:** when double-clicking at a location in the master viewer, the synchronized view will move to the exact point defined by the 4 dimension axis \(inline, crossline, fold and time/depth\)
* **Jump to Closest CDP:** when double-clicking at a location in the master viewer, the synchronized view will move to the nearest location \(the exact location if it exists\).

**How to have a cursor read-out between a map and a Gather or Stack viewer:**

1. Synchronize a Gather or Stack viewer to a Map viewer
2. Tick on “Read-out position”
3. Make crosshair visible in both viewers![](/assets/002_sync.png)_Cursor tracking between a Gather and a Map viewer_

**How to have a cursor read-out between a Gather and a Stack viewer:**

1. Synchronize a Gather to Stack viewer
2. Tick on “Read-out position” and “Vertical View”
3. Make crosshair visible in both viewers![](/assets/004_sync'.png)_Vertical zoom and cursor tracking synchronized between stack and gathers_




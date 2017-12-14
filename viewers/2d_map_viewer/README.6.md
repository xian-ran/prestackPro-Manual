## 2D Map Viewer {#2d-map-viewer}

The 2D Map Viewer can be used to display stack time slices, horizon time-structure maps, stacked attributes, AVA attributes, or offset/angle amplitude maps created from pre-stack gathers with the [Create Maps module](/algorithm_documentation/interpretation-processing/horizon_toolkit/README.16.md).

Several objects can be displayed in the same window. The data with the ‘eye open’ icon are visible \(1\), and highlighted items are displayed on top of all other visible objects. It is possible to use the up and down arrow key to change the highlighted volume.

![](/assets/001_map_viewer.png)

If you display **offset or angle-dependent amplitude maps** created from pre-stack gathers, it is possible to step through all offset or angles using the up and down arrows \(2\).

![](/assets/002_map_viewer.png)_Near vs. far offset amplitude maps. Vertical exploration wells and deviated production wells are displayed on the map_

**Time slices** may be viewed for any offset/angle, and slice position can be shifted up or down interactively \(3\). This is particularly useful for investigating amplitude effects on flattened volumes.

**Well paths** \(4\) are displayed on top of the maps. A solid line indicates that the well is above the map, and a thin stippled line indicates that it is below. Appearance and coloring of the well paths can be handled individually \(5\).

![](/assets/003_map_viewer.png)

_Creating a contour on a map using transparency_

Users can set up a range to be transparent by typing the range in the Min and Max boxes \(6\). This feature can be used to create a contour on a TWT structural Horizon map, which can be overlain on top of any other map. Pressing the Range icon \(7\) will invert the transparency range.

**Isolines** may be viewed by clicking on the display icon \(8\) and their appearance controlled by icon \(9\). Once displayed, isolines stay on top of the view, meaning that they overlay any other horizon or map displayed.

![](/assets/004_map_viewer.png)

_Display and setting of isolines_

![](/assets/005_map_viewer.png)

_Time isolines overlaid on an amplitude map_


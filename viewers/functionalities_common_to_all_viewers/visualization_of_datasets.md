### Visualization of datasets {#visualization-of-datasets}

The best way to start any viewer is to Right mouse button click on the cube to be investigated from the Data Pool or by going to: **Viewers**

If you open an empty viewer via the menu,the data cube to be investigated needs to be dragged and dropped into the volumes part of the window![](/assets/001_Common_Viewers.png)_Gather viewer_

#### **Visualization of multiple datasets:**

It is also possible to work with several volumes if they have the **same dimension**. It is a particularly powerful tool for QC of several intermediate cubes from a processing flow.

All volumes are available in the lowermost data selection window \(see picture below\). When you open the eye icon in the toggle box, a volume becomes available in the upper data selection window.

![](/assets/002_common_viewer.png)

This option allows the comparison of the different cubes at the same location. The datasets need to cover the same IL/XL range.

To switch from a cube to another simply:

* highlight your cube of interest

* use the “page up” “page down” keys \(or the arrow keys\) to select the cube above or below. This option allows the use of the cursor positioning in a quantitative way: because the numerical value of the event your cursor is in, for different cubes, is shown in “Cursor Readout Out”.

The datasets can be displayed with the same color bar if the “**content specific**” option \(e.g.: Seismic Amplitude\) is selected at the bottom left of the window or with different color bars if the “**volume specific**” \(e.g.: Data Pool name\) option is set **for one or all cubes**.

Any “**volume specific**” color bar can be set as the “**content specific**” color bar, for all volumes, using the &lt;**Set as Content specific histogram**&gt; option.

#### **Change line location**:

The line position can be selected above the upper data selection window.

A line number can be directly entered or the up and down button can be used for an incremental change of line.

#### **Scrolling bars**:

Scrolling bars can be found around the dataset display.

* The one on the right side corresponds to a navigation bar in time
* The one below the display corresponds to a navigation bar in cross line \(or inline\).

Instead of using the scrolling bar, the volume image can be moved both ways simply by left click and drag with mouse.

#### **Zoom in the data**:

A zoom can be done from the scale bars: time and line. Position your mouse over the scale and use the mouse wheel.

Alternatively, an equal zoom of both axes can be achieved using the mouse wheel inside the dataset display.

Zooming &gt; x8, in either direction, will turn on sample grid lines, if they have been turned on by the user.

#### **Manual setting of the display:**

It is possible to manually specify the range of data display in the X and Y direction: right click on the axis and specify **Setup axis**.

This tab can be used to specify a type of display.

For the X axis \(in the gather direction\), the number of gathers can be locked.

#### **Cursor Read-Out:**

![](/assets/003_common_viewer.png)

_Cursor Read out of the Map Viewer_

Cursor read-out is displayed in the top left corner of the viewers. It gives information about the position \(Inline, Crossline, World X and Y, time, depth\), the fold \(Offset, angle, azimuth\) and the content and values of the volume being displayed.

For quantities with measurement units you can choose the read-out to be displayed in one the proposed units by clicking on the corresponding field panel.

Additionally, the read-out values for the X and Z/Y axis are highlighted on the axis itself.

![](/assets/004_common_viewer.png)

_Values of the crosshair position for both axis are highlighted_

#### **The Tool bar:**

![](/assets/005_common_viewer.png)

1. Show/hide object lists
2. Show/hide histogram
3. Rename the window
4. Flip stack/pre-stack mode
5. Selection of section type \(inline/crossline/arbitrary path\)
6. Set up the X-axis orientation \(smart based on project geometry/increasing/decreasing\)
7. Crosshairs for position read out
8. Interpolation of seismic samples on/off
9. Interpolation of overlay samples on/off
10. Interpolation of mask on/off
11. Box filter/No antialiasing
12. Pre-defined zoom level
13. Synchronise this viewer with another
14. Synchronization success indicator
15. Screen capture
16. Create Arbitrary Volume from this view

Several of these settings are saved in the project and will be kept for any new viewer opened \(during the same session and after closing/opening the project\). These settings are:

* Geometry dependent orientation
* True North orientation for maps
* Grid on/off
* Crosshair on/off
* Background color

#### **Context menus:**

The context menu in the viewers has various settings \(show compass, show grid, show and pin the crosshairs\) as well as entries to create various viewer dependent objects:

* Arbitrary Path \(Map & TopStack views\)
* Location of Interests \(Map & TopStack views\)
* Seed Points \(Map, Stack & TopStack views\)
* Polygon Selection \(Map, Stack, TopStack & Gather views\)

When the cursor is on one object \(well, polygon, arbitrary path\), the context menu will have different entries to center the view on this object or modify the display settings for this object.

The context menu of the tree in the bottom left corner has entries for changing color of objects, as well as centering the view on wells and polygon selection.


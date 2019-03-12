# Manual Horizon Picking

To complement the existing 3D Autotracker, we introduce a new module to the Pre-Stack Pro suite of interpretation tools: Manual Horizon Picking. This is a new canvas for seismic interpretation that incorporates orthogonal seismic section displays with a map window, allowing the user to manually pick new horizons or fill in holes in existing horizons.

Manual Horizon Picking is launched from the **Interpretation Menu**. Once launched, the canvas is blank. Click on the **Initialisation and Settings** icon to start:

![Starting up Manual Horizon Picking](../../.gitbook/assets/usermanual_start.png)

### Initialisation

1. Select the seismic volume, this can be time or depth, stack, pseudo stack, or pre-stack gathers
2. Select an existing horizon to update OR create a new horizon
3. Choose the snapping type for the horizon: no snap, peak, trough or a zero-crossing \(+ to –, or – to +\)
4. Press OK.

You may return to these settings at any time during interpretation and change the snapping options or line step-size etc. If you wish to change the horizon or seismic volume you will need to exit and start Manual Horizon Picking again.

![Initialisation and Settings](../../.gitbook/assets/usermanual_settings.png)

There are three main panels in the canvas: the **Data Tree**, two **Seismic Sections**, and a **Map**. 

![The main canvas for Manual Horizon Picking](../../.gitbook/assets/usermanual_maindisplay%20%281%29.png)

The **Data Tree** controls the display of wells, horizons, seed-sets on the Seismic Sections and the Map. The cursor readout is displayed at the top of the Data Tree, showing the amplitude etc. of the cursor on the seismic. It is also where the user can select the seismic lines to display, and access the history of their manual interpretation locations.

The **Seismic Sections** show two, orthogonal seismic lines and the intersection lines between them. On start up and inline and cross-line are displayed. These can be rotated to form Pivot Lines \(see below\). The scale of the seismic can be changed by scrolling the mouse-wheel on a an axis. Notes the Z axis zoom is linked between the two sections.

The **Map** window displays the current horizon selected for interpretation. The colour bar can be changed and the range altered as required, \(mouse click on the colour bar\). The intersection of the two Seismic Sections is called the Pivot Centre. The visible extent of each Seismic Section is highlighted in red on the Map. The location of the cursor is linked between the two Seismic Sections and the Map, with a cursor readout shown in the Data Tree

![Links between Seismic Sections and the Map](../../.gitbook/assets/usermanual_seismic_range.png)

### Moving Seismic Lines

There are a number of ways to move the two seismic lines, the intersection of which is called the Pivot Centre.

* **Data Tree**: 
  * Type in the seismic line number, or use the up and down arrows. Note, the user can scroll the mouse-wheel with cursor inside the line number box.
* **Seismic Lines**: 
  * Use the icons to move forwards and backwards, they will shift by the step-size as defined in Settings
  * Page Up and Page Down move the active line \(currently being picked\) by the step-size
  * Double click on a seismic line to move the intersecting line to that location.
  * Hover cursor on intersection line, cursor turns to a hand and line can be dragged to a new position.
* **Map Window**: 
  * Double click to shift the Pivot Centre of the two seismic lines \(i.e. move the intersection point of the lines\)

![Moving Seismic Sections](../../.gitbook/assets/usermanual_movingseismic.png)

**Pivot Lines:** Pivot lines are rotated inlines and crosslines that maintain an orthogonal relationship, allowing the user to interpret on strike and dip seismic sections. Pivot Lines are defined by an angle rotation from the inline direction. There are two ways to rotate Pivot Lines:

* **Data Tree**: Type in the angle of rotation, or use the up and down arrows, or scroll the mouse wheel \(with cursor inside box\)
* **Map Window**: Hover the cursor on the pivot centre and scroll the mouse-wheel

![Pivot Lines](../../.gitbook/assets/usermanual_pivot-lines.png)

### Manual Horizon Picking

There are three methods of manually picking a horizon, and they are listed under the Picking Modes icon on each Seismic Section. They can also be accessed from hotkeys \(see Hotkeys\).

![](../../.gitbook/assets/usermanual_pickingmodes.png)

**Picking Modes:**

* Flat Line - straight connectors between control picks
* Spline - curved connectors between control picks
* Autotracking - 2D autotracking along the seismic line

add picks by clicking with left-mouse button. To accept the picks double click OR right-mouse click and Apply. Holding SHIFT will stop snapping

Flat Line , snapping to the seismic after Apply

Spline Curved line connectors between control picks, snapping to the seismic after Apply.

Autotracking 2D autotracking along the seismic line. Place a seed point and double click/Apply.

To move a seismic line whilst picking press ESC, double click to move the intersecting line, then ESC again to return to picking mode.

### Hotkeys

![List of hotkeys](../../.gitbook/assets/usermanual_hotleys.png)




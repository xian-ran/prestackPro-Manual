## 3D Viewers {#3d-viewers}

PreStack-PRO 5.0 has a new 3D Viewer, which allows users to compare many differently-dimensioned seismic volumes, together in the same scene, by using real world X,Y coordinates.

This enables the viewing of seismic data in context with complex geological structures, like horizons and faults, as well as with other objects such as well paths and arbitrary lines, in the future. It provides a great way to present seismic data and the associated interpretation to management and other team members.

This 3D viewer provides a comprehensive set of seismic display options for 3D stack and 4D pre-stack seismic volumes. It is possible to choose any combination of inline / xline / timeslice panels and/or boxes to display inside the 3D scene. Pre-stack gathers can be displayed at right angles to and tied to any selected inline / crossline, offset or angle plane. Horizons can be displayed with their own colour and snapped or clipped to any or all seismic objects in the scene. This provides a real world, 3D Q.C. of any project horizon.

![](/assets/001_3dviewer.png)

_A_ _pre-stack seismic gather volume, displaying 11 angle plane in a 3D box.One red horizon is displayed on the box sides – An XYZ location is marked by the 3D cursor – time and inline ranges have been modified using slider bars._

When any seismic volume is dragged and dropped into the three panesl will open. The rotation centre is set to the middle of the volume, where the inline, crossline and timeslice all meet.

![](/assets/002_3dviewer.png)

_Initial display of seismic volume, after rotation to show timeslice._

| ![](/assets/004_3dviewer.png) | The inline plane is the selected scene object by default and therefore the object properties tab will display the inline properties, which the user can change using slider bars – inline location , time min/max range, angle/offset plane and any viewed gather properties if &lt;view gather&gt; is ticked on.Gathers can be viewed at right angles to any inline or crossline panel, but not coming out from the sides of box displays. |
| :--- | :--- |


![](/assets/005_3dviewer.png)

_Pre-stack seismic volume, single gather display, at inline 27574, crossline 16432, with a stretch of x3 applied to make it easier to see._

If a second volume is dropped into the viewer, it won’t be seen on any of the panels, but will now appear as a volume option, along with the original volume, in all object properties. 

![](/assets/006_3dviewer.png)

_3 volumes loaded, Angle gathers, PCube-Vp and well synthetic \(see 3D viewer, multi volume examples below\)_

This allows the user to have any object display the 2nd volume, instead of the first. Even single stack trace or gather data volumes can be shown as a single, vertical trace; so for example a well synthetic will display as a vertical line, at it’s well location in the 3D scene.

Each volume can have its own unique histogram, opacity and colour table, set by using the histogram tab located at the base of the viewer.

New planes and boxes can be created or existing objects deleted using the RMB context menu, once the target object has been selected. In the example below, the ‘inline plane 4’ object has been selected and can now be removed or a new inline plane added to the 3D scene.

![](/assets/007_3dviewer.png)

_Create/delete new inline plane GUI_


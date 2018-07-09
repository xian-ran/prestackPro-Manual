## 3D Viewers {#3d-viewers}

PreStack-PRO 3D Viewer allows to display and compare simultaneously stack and pre-stack volumes. Thus, you can now look at 3D/4D/5D volumes in one 3D viewer by using real world X,Y coordinates.

This enables the viewing of seismic data in context with complex geological structures, like horizons and faults, as well as with other objects such as well paths. It provides a great way to present seismic data and the associated interpretation to management and other team members.

This 3D viewer provides a comprehensive set of seismic display options for 3D stack and 4D pre-stack seismic volumes. It is possible to choose any combination of inline / xline / timeslice panels and/or boxes to display inside the 3D scene. Pre-stack gathers can be displayed at right angles to and tied to any selected inline / crossline, offset or angle plane. Horizons can be displayed with their own colour and snapped or clipped to any or all seismic objects in the scene. This provides a real world, 3D Q.C. of any project horizon.

The 3D viewer duplicates the volumes you want to display. Therefore you need to save enough memory on the nodes when you launch Pre-Stack PRO.

![](/assets/12_3dviewer.JPG)_A_ _pre-stack seismic gather volume, displaying 3D planes of a near offset volume.An horizon with elevation map as well as a well path are also displayed._

When any seismic volume is dragged and dropped into 3D viewer icon \(![](/assets/icon.JPG)\), three panels will be opened. The rotation centre is set to the middle of the volume, where the inline, crossline and timeslice all meet.

![](/assets/3dviewer_init.JPG)_Initial display of seismic volume._

Three tabs are available on the bottom panel: one for the histogram, for for the stretching displays and one for the angle view of the seismic volumes.  
Horizons and wells

![](/assets/004_3dviewer.png)  
The inline plane is the selected scene object by default and therefore the object properties tab will display the inline properties, which the user can change using slider bars – inline location , time min/max range, angle/offset plane and any viewed gather properties if &lt;view gather&gt; is ticked on.Gathers can be viewed at right angles to any inline or crossline panel, but not coming out from the sides of box displays.

![](/assets/3dviewer_gather.JPG)_Pre-stack seismic volume, single gather display, at inline 27300, crossline 16266, with a stretch of x2 applied to make it easier to see._

If a second volume is dropped into the viewer, it won’t be seen on any of the panels, but will now appear as a volume option, along with the original volume, in all object properties.

![](/assets/3dviewer_volumelist.JPG)  
_3 volumes loaded, offset gathers and two angle stacks \(see 3D viewer, multi volume examples below\)_

This allows the user to have any object display the 2nd volume, instead of the first. Even single stack trace or gather data volumes can be shown as a single, vertical trace; so for example a well synthetic will display as a vertical line, at it’s well location in the 3D scene. You can select the volume to display by highlighting the plane you want to modify, then by clicking on the desired volume in the display properties window.

You can add or remove a plane by using the RMB &lt;crew new I Plane&gt; or &lt;Remove object&gt;.

![](/assets/3dviewer_addplane.JPG)  
_GUI to add a new plane in the 3D viewer._

Each volume can have its own unique histogram, opacity and colour table, set by using the histogram tab located at the base of the viewer.


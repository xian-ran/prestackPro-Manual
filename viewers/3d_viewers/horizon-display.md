### Horizon display {#horizon-display}

Horizons can be selected from the list on the bottom left. Horizons are displayed with their own colour and headlight shading only.  
If horizons have a lot of points, they may take a while to load, and check the top right corner for the loading . It is currently not possible to know how long the process will last.

In the current version, pre-stack horizons can NOT be displayed in the 3D viewer. This is work in progress.

![](/assets/3dviewer_loading.JPG)  
_Loading sign in the 3D viewer_

![](/assets/3dviewer_horizon.JPG)  
_Horizon loading_

Any selected horizon, can be snapped or cropped, to display only on the sides of any vertical seismic objects. By clicking on **Reset Cutting Planes**, the full extend of the selected horizon is restored.

However, only horizons given a name and saved into the project are available in the list for display. So  QC of tracking is not fully interactive with this first version of the 3D viewer.

![](/assets/3dviewer_hz1.JPG)_Green horizon displayed and selected so that slider bars can be used to restrict inline/crossline range_

![](/assets/3dviewer_hz2.JPG)

_Three horizons loaded.. One inline and one crossline are displayed              
_

You can add horizons by drag and drop from the Data Pool or by highlighting them from the horizon list on the bottom left.

You can also make a vertical shift of the horizon using the ‘Time-Shift**’ **panel.

As seen previously, horizons can be displayed as a plane or as a line. If the plane display is selected then the texture can be modified and some attributes can be computed on the fly using the selected horizon.

Two main texture can be displayed:

* **None** : fill with a constant colour but the display can be modified using the 'Ambient Light' slider  
  ![](/assets/3dviewer_hz3.JPG)

* **Elevation Map** : the horizon elevations are displayed and the histogram is automatically generated for the selected horizon

![](/assets/3dviewer_hz4.JPG)  
_Elevation Map display_

More on the fly horizon attribute computations can be performed if one of the loaded seismic volume is selected.

* Amplitude
* Envelope
* Hilbert Transform
* Instantaneous Phase
* Instantaneous Frequency

Other attributes can be computed on a window following the selected horizon:

1. Root Mean Square \(RMS\) amplitude
2. Spectral Bandwidth
3. Maximum Sample in the window
4. Minimum Sample in the window

By default the window length is 50 ms \(25 ms each side of the horizon\) but it can be modified \(but always centered on the horizon, it can not be asymmetric.

The attributes are computed on the fly, which allows horizon based quick analysis of the data on the full area.

![](/assets/3dviewer_hz5.JPG)  
_Horizon based attribute computation_

For each attribute computation, the histogram is automatically computed and displayed. It can then be modified as explained on the [histogram chapter](/viewers/3d_viewers/histogram.md).

![](/assets/3dviewer_hz6.JPG)  
_Example of horizon based attribute computation - Spectral Bandwidth on a window of 500 ms \(250 ms each side of the horizon\)_


# Spectral Decomposition

Pre-Stack Pro allows the user to perform Spectral Decomposition on:

* Stacked Volumes
* Partial Stacked Volumes
* Pre-stack Data, i.e. gathers

Spectral Decomposition is performed on the fly, with the user controlling the frequencies and blending. Spectral Decomposition maps can be saved and reopened to reproduce the same RGB blend at a later date. Full volume export of the frequencies is also available. The method used is the Gabor-Morlet transform, with default settings set for Octave spacing.

Any seismic volumes can be used as input to the RGB blend display, e.g. Near, Mid and Far offset volumes.

![](/assets/sp_start.png)

_Map of a Spectral Decomposition Blend_

## Opening Spectral Decomposition

Spectral Decomposition is launched from the Map window by clicking on the Icon: ![](/assets/sp_icon2.png)

![](/assets/sp_01_launch.png)

_Map Window: Spectral Decomposition icon_

Launching Spectral Decomposition turns the Map window into a preview for the RGB Blends produced. The user selects the seismic data by dragging and dropping from the data pool into Spectral Decomposition, or by selecting from the drop-down menu. This can be a stack, pseudo stack, or prestack data, in time or depth. This input volume is displayed in a section panel alongside a corresponding amplitude display of the frequencies found from a selected trace in that input section.

![](/assets/sp_02_specd-gui.png)_A stack volume is is shown, with a time-slice display at 1900ms, with frequencies of 14Hz, 28Hz and 58Hz blended together in the map window. _

![](/assets/sp_02b_specd-gui_prestack.png)_A prestack \(gathers\) seismic volume is shown, with an extraction on the horizon Top\_Frigg, for an angle of 24 degrees, with frequencies of 14Hz, 28Hz and 58Hz blended together in the map window. _

## RGB Blending

Three frequencies are assigned to Red, Green and Blue channels, that are blended together in the Map window. Each channel has its own histogram that the user can adjust to enhance the spectral blend image. Where all three frequencies have equal amplitude the blend is white; the absence of the three frequencies produces black.

The frequencies available range from 4Hz to a maximum frequency that is set by default to 80% of the nyquist frequency. The user can either input frequency values into table within the Spectral Decomposition window, OR drag the vertical RGB lines on the frequency amplitude panel. As the frequencies are altered, the preview auto-updates, changing the blend.

There are two options making Spectral Decomposition maps:

![](/assets/sp_04_type.png)

1. **Use Fixed Time**: a frequency-blend time-slice map is generated, that the user can scroll up and down within the volume.
2. **Use Horizon**: the frequency-blend map extracted on a horizon. The map can be shifted with respect to the horizon, creating horizon-parallel displays.

The RGB blend display is controlled with the histograms in the Map window. Decrease the Max. of the histogram to increase the brightness of that channel. Each channel can be viewed on it's own; to view just the Red channel alone toggle OFF the Green and Blue channels using the small boxes to the left of the histograms. This allows the user to assess the relative components and adjust the histogram scaling in order to optimize the blend. The maximum marker for each histogram can be moved with the mouse by holding down the control button.

![](/assets/sp_06_rgb-blend.png)

The settings icon to the left of the histograms has additional options:

* Redistribute markers: includes the useful option to skip outliers
* Set gamma correction: by default this is set to 0.8 by default
* Sync all channels

Note that the frequencies of each RGB channel can be controlled from the tree in the Map window. The time shift for the horizon/slice can also be controlled from the Map window.

## Display Settings

The Input Volume panel display can be changed by using the pipette icon, OR double clicking on the map, with the location of the panel shown as a black cross.

The **Control Tab** allows the user to toggle on Wells and Horizons in the display panels.

![](/assets/sp_05_control-tab.png)

_Control Tab: toggle on Wells and Horizons._

## Saving Blend Maps

Spectral decomposition is run in memory, with blends displayed as a preview in the Map window. To save a spectral decomposition blend map to the Data Pool click on **Keep**. To save the spectral decomposition map into the project right-click on the volume in the Data Pool and select "**Save Volume to Project**"

## Restoring a Blend

Load a saved map into the Data Pool. Drag and drop the saved map into the Map window. The initial display if the standard Map window display \(for seismic/horizons etc.\). To switch it to the RGB blend display click on the **RGB blend icon** beneath the name of the saved map in the data tree. The RGB blend will be restored exactly as it was saved - with the same frequencies and histogram settings.

![](/assets/sp_07_restoringablend.png)

_Loading a saved spectral decomposition map_

## Blending Non-Frequency Volumes

The RGB blending module is not restricted to frequency data: it can be used to blend any seismic volumes. For example, the three channels \(Red, Green, Blue\) can be used to blend angle stacks, 4D volumes, or azimuthal datasets, etc. Care should be taken with the histogram ranges: the RGB channels are amplitudes and not frequency, and therefore don't start at zero. Blends can be used to highlight misalignment of offset stacks, or visualise AVO anomalies.

To  load non-frequency volumes into the RGB Blender, click on the **RGB Blend icon** on the Map window: ![](/assets/sp_icon_RGB.png)

Select the 3 volumes to blend \(these should be pre-loaded into the Data Pool\) and press OK. The Map window will change to a Blend display of a time-slice set to 0 by default. Select the time slice for each RGB channel and the Map will update. Change the histogram settings to adjust the blend, setting the markers to skip outliers may improve the display \(settings icon &gt; reset markers &gt; between min and max skip outliers\)

![](/assets/sp_10_avovols.png)

_Near, Mid and Far volumes blended as a time slice. Where the near, mid and far amplitudes have equal values the blend will be white. _


# Spectral Decomposition

Pre-Stack Pro allows the user to perform Spectral Decomposition on:

* Stacked Volumes
* Partial Stacked Volumes
* Pre-stack Data, i.e. gathers

Spectral Decomposition is performed on the fly, with the user controlling the frequencies and blending.

Spectral Decomposition maps can be saved and reopened to reproduce the same RGB blend at a later date. Full volume export of the frequencies is also available.

Any volumes can be used as input to the RGB blend display, e.g. Near, Mid and Far offset volumes.

![](/assets/sp_start.png)

_Map of a Spectral Decomposition Blend_

## Opening Spectral Decomposition

Spectral Decomposition is launched from the Map window by clicking on the Icon: ![](/assets/sp_icon2.png)

![](/assets/sp_01_launch.png)

Launching Spectral Decomposition turns the Map window into a preview for the RGB Blends produced. The user selects the seismic data by dragging and dropping from the data pool into Spectral Decomposition, or by selecting from the drop-down menu. This can be a stack, pseudo stack, or prestack data, in time or depth. This input volume is displayed in a section panel alongside a corresponding amplitude display of the frequencies found from a selected trace in that input section.

![](/assets/sp_02_specd-gui.png)_A stack volume is is shown, with a time-slice display at 1900ms, with frequencies of 14Hz, 28Hz and 58Hz blended together in the map window. _

## RGB Blending

Three frequencies are assigned to Red, Green and Blue channels, that are blended together in the Map window. Each channel has its own histogram that the user can adjust to enhance the spectral blend image. Where all three frequencies have equal amplitude the blend is white; the absence of the three frequencies produces black.

The frequencies available range from 4Hz to a maximum frequency that is set by default to 80% of the nyquist frequency. The user can either input frequency values into table within the Spectral Decomposition window, OR drag the vertical RGB lines on the frequency amplitude panel. As the frequencies are altered, the preview auto-updates, changing the blend.

There are two options making Spectral Decomposition maps:

![](/assets/sp_04_type.png)

1. **Use Fixed Time**: a frequency-blend time-slice map is generated, that the user can scroll up and down within the volume.
2. **Use Horizon**: the frequency-blend map extracted on a horizon. The map can be shifted with respect to the horizon, creating horizon-parallel displays.














### Spectral Decomposition Volume

Go to **Attributes &gt; Spectral Decomposition Volume...**

Pre-Stack Pro allows the user to perform Spectral Decomposition on:

* Stacked Volumes
* Partial Stacked Volumes
* Prestack Data, i.e. gathers

To view Spectral Decomposition as a Map with a preview display that autoupdates, the user should launch Spectral Decomposition from the Map window. The method used is the Gabor-Morlet transform, with default settings set for Octave spacing.

![](/assets/sp_decompvol_02.png)

_Stack volume example: options selected to generate a volume of 3 frequencies \(14Hz, 28.6Hz, 58.5Hz\)_

To generate a Spectral Decomposition Volume select the seismic volume from the Data Pool. A seismic line from the input volume is displayed in a panel alongside the frequency amplitude of that line. For prestack seismic data the user selects the angle to extract frequencies from. The user can generate a **map **or a **volume **which produces a seismic volume with an "offset" axis of frequency.![](/assets/sp_decompvol_prestack_03.png)

_Prestack volume example: for an angle of 17deg a Map of all frequencies will be produced 12ms below the Top Frigg horizon._

Attributes that can be extracted:

* Amplitude
* Phase
* Real
* Imaginary

There are two options for frequencies:

1. Frequencies **ALL**: All frequencies are selected, with the maximum being 80% of the nyquist frequency.  
2. Frequencies **Three**: The user selects three frequencies to extract \(reducing the size of the output volume\).

Map Options:

1. **Use Fixed Time**: a frequency-blend time-slice map is generated, the user specifies the time \(or depth\).
2. **Use Horizon**: the frequency-blend map is extracted on a horizon. The map can be shifted with respect to the horizon, creating horizon-parallel maps.

After selecting the data input and output options, press **Calculate**. The output volume\(s\) will appear in the Data Pool.

#### RGB Blending of Spectral Decomposition Volumes

Open the Map Window and click on the **RGB Blending** icon and select the same output spectral decomposition volume for each of the input channels \(red, green, blue\).![](/assets/sp_decompvol_loading-map_04.png)

_Loading spectral decomposition volumes into the Map Window_

Three frequencies are assigned to Red, Green and Blue channels, that are blended together in the Map window. Each channel has its own histogram that the user can adjust to enhance the spectral blend image. Where all three frequencies have equal amplitude the blend is white; the absence of the three frequencies produces black.

Select the 3 frequencies to assign to the Red, Green and Blue channels from the tree in the Map window.

The RGB blend display is controlled with the histograms in the Map window. Decrease the Max. of the histogram to increase the brightness of that channel. Each channel can be viewed on it's own; to view just the Red channel alone toggle OFF the Green and Blue channels using the small boxes to the left of the histograms. This allows the user to assess the relative components and adjust the histogram scaling in order to optimize the blend. The maximum marker for each histogram can be moved with the mouse by holding down the control button.

.![](/assets/sp_decompvol_loading-map_05.png)

The settings icon to the left of the histograms has additional options:

* **Redistribute markers**: includes the useful option to** skip outliers**, enhancing the blend display.
* Set gamma correction: by default this is set to 0.8 by default
* Sync all channels

#### Saving an RGB Display

To save an RGB blend display click on the downwards red-arrow icon, in the data tree. This saves the frequency selection and the histogram settings so that the map can be reproduced at a later date:

![](/assets/sp_decompvol_savingrgb_06.png)

Once an RGB blend is saved, the volume can be drag and dropped into the Map Window and will now have its own RGB blend icon in the data tree. Click this icon to transform the Map window into an RGB blend display and restore the blended Map:

![](/assets/sp_decompvol_reload_07.png)




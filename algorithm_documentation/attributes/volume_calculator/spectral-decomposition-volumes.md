### Spectral Decomposition Volume

Go to **Attributes &gt; Spectral Decomposition Volume...**

Pre-Stack Pro allows the user to perform Spectral Decomposition on:

* Stacked Volumes
* Partial Stacked Volumes
* Prestack Data, i.e. gathers

To view Spectral Decomposition as Maps with a preview display, the user should launch Spectral Decomposition from the Map window. The method used is the Gabor-Morlet transform, with default settings set for Octave spacing.

![](/assets/sp_decompvol_01.png)

To generate a Spectral Decomposition Volume select the seismic volume from the Data Pool. A seismic line from the input volume is displayed in a panel alongside the frequency amplitude of that line. For prestack seismic data the user selects the angle to extract frequencies from. The user can generate a **map **or a **volume **which produces a seismic volume with an "offset" axis of frequency.

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

After selecting the data input and output options, press **Calculate**. The output volume\(s\) will appear in the Data Pool








## Spectral Analysis {#spectral-analysis}

The **spectral analysis** tool computes amplitude, power and phase spectra for any seismic volume in the Data Pool. Spectra can be smoothed, and the standard deviation displayed. Spectrum values can be exported and imported. The tool is executed via: **QC** → **Spectral Analysis.**

![](/assets/001_spectral_anal.png)

_Spectral Analysis GUI_

The GUI is divided into several areas. The General options bar manages import and export of spectra. The Selection Panel lets the user choose and select in data ranges to use for the computation. Parameters used in the algorithm can be changed in the Spectrum computation area. Display options can be changed in the Spectrum properties table. The main display window is the Spectrum area, where all spectra chosen are displayed.

![](/assets/002_spectral_anal.png)

_General Options_

1. View/Hide Selection Panel and Spectrum properties
2. Export Spectrum, including the properties attached to it
3. Import previously exported spectrum

![](/assets/003_spectral_anal.png)

_Selection and computation panel_

1. The Selection Panel works in the same way as for the [Select Data dialog](/select_data/README.md). Select the input volume you want to compute the spectrum on and trim in the different domain, as needed. It is also possible to use a Polygon Selection for the input data. When using a Polygon Selection, you can make a sub selection inside the Polygon.
2. Tick off **Use Default** for smoothing window and taper if you want to change those parameters and enter custom values.
3. Tick on if you want to have one spectrum per fold. This is to be used when creating pre-stack wavelet \(i.e. one wavelet per fold\).
4. Click **Calc. Spectrum**

You can repeat the procedure to add more spectra by changing the selection and/or the input volumes. Additional spectrum will be displayed while keeping previous spectra displayed. The properties of each spectrum can be changed independently.

![](/assets/004_spectral_anal.png)

_Spectrum properties_

1. Toggle the display on/off of the spectrum
2. Display the standard deviation curves
3. Change the color of the curve
4. Change the width of the curve
5. Change the value for reference used in dB display
6. Change the name of the Spectrum

A right click inside the list of spectrum will open a context menu to set the dBRef, delete or dynamically update the selected spectrum. It also gives options to save one spectra as a wavelet or a series of spectrum as a pre-stack wavelet.

In the spectrum area, MB1 is used to pan the visible area while the mouse wheel allows zooming. A right-click will open a contextual menu to reset the view, show/hide legends and gridlines, export the spectrum as an image or CSV file.

Also the contextual menu lets the user save the spectrum as a wavelet or pre-stack wavelet for usage into the Wavelet tool.

Clicking with the right mouse button on the axis let the user toggle between linear/logarithmic scales and to insert a marker.


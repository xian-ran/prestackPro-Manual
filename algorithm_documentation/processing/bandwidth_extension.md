### Bandwidth Extension {#bandwidth-extension}

The bandwidth extension algorithm can be used to increase the frequency content and improve the signal definition within a dataset.

This trace by trace algorithm uses a continuous Gabor wavelet transform to compute time-frequency amplitude and phase spectrum. For each trace time sample, it analyses the decay of amplitudes with frequency, and applies a correction to increase its slope, whilst leaving the phase unchanged.

Note: The algorithm will not differentiate between signal and noise energy. Therefore, it may be necessary to apply additional random noise attenuation processes to prevent over-boosting of high frequency noise.

To open up the bandwidth extension dialog go to: **Processing** → **Bandwidth Extension**

![](/assets/084_Processing.png)
_Bandwidth Extension GUI_

**Parameters:**

**Wavelet Transform:**

The Gabor transform is carried out between the user defined **minimum and maximum wavelet frequencies**. The data is split up into the **number of sub bands** per octave; or by linear increments.

**Octave frequency spacing** will sub-divide the frequency range into sub bands increasing exponentially. The range between minimum and maximum frequency is filled by doubling the frequency at each step (e.g. 2, 4, 8, 16, 32, 64 and 128Hz). Gaps will be filled by a logarithmically distributed number of sub bands.

**Linear frequency spacing** simply splits the frequency range into constant increments.

**Adjustment Parameters:**

The **bandwidth extension factor** determines the slope of the correction. A value of 1 has no effect; 10 is the maximum extension.

The user supplies a **maximum frequency** which is less than wavelet transform maximum frequency. The bandwidth extension operator is ramped down in the transition zone between these two frequencies.

The **tapering half-length** defines the amount of smoothing of the adjustment coefficients. The original and adjusted coefficients, and the reconstructed volume can be output as QC volumes.


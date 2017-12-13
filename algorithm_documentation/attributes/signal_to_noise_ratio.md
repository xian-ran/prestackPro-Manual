### Signal to Noise Ratio {#signal-to-noise-ratio}

Go to **Attributes** → **Signal to Noise Ratio.**

S2N is defined as the ratio between the signal power and the noise power. Two methods have been implemented to compute this attribute, a **correlation** based and a **stack** based approach.

**Input:** The attribute takes a single seismic volume as input, either stacked or prestack.

**Parameters:** Both methods are stencil based. The user has to specify the size of the stencil in every dimension (Inline, Crossline, Fold(s), time/depth). Additionally a parameter called _Max Time-Shift_ (equivalent to the lead/lag parameter) is available for the correlation based method.

![C:\Users\Valentin\AppData\Local\Temp\01_s2n.png](C:\Temp\Gitbook3\export\assets\cusersvalentinappdatalocaltem.png)

S2N Ratio GUI

**Modes of calculation:**

*   **Correlation:** This method will compare (in a correlation sense) the similarity between the central trace and its neighbour traces inside the stencil. If we denote by _AC_ the autocorrelation of the central trace and _XC_ the average cross-correlation between the central trace and its neighbours, the signal to noise ratio is given by:

The original method is performed with non-normalized correlation function. However, the user has the possibility to use the _normalized correlation_ to compute the signal to noise **relation** as it will generally give much less spikes in the output. Assumptions behind the method are that the form and phase of the signal is consistent inside the stencil and that the noise is spatially incoherent and uncorrelated to the signal.

*   **Stack:** We denote by _i_ the spatial sampling index inside the stencil (_M_ traces) and _j_ the temporal index (_N_ samples). For a seismic record the signal to noise ratio is given with the following logarithmic relation:

This method assumes that the seismic wavelet is stable inside the stencil and that the noise is white. Therefore, the energy of the signal is given as the spatial sum of the square of the stacked trace and the energy of the noise is defined as the total energy minus the energy of the signal.

**![C:\Users\Valentin\AppData\Local\Temp\03_s2n.png](C:\Temp\Gitbook3\export\assets\cusersvalentinappdatalocaltem.png)**

Amplitude map (left) and extracted signal to noise ratio (right) at an horizon
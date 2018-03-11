#### Description of Functions {#description-of-functions}

**Time Domain**

**Resample**

A wavelet can be resampled to have a new sample interval between 1 msec and 100 msec. An anti-alias filter is applied when resampling at a coarser interval.

**Smooth wavelet**

Time domain smoothing is applied to the wavelet. Options are i) median filter, ii) weighted smoothing with Gaussian weights, iii) linear weighting, iv) an unweighted moving average. In all cases, the user specifies the half-length of the filter in samples.

**Cut wavelet**

The start and end times of the wavelet may be modified by adjusting the slider bar or typing in new values.

**Taper**

A linear ramp is applied to the ends of the wavelet. Different lengths may be applied to each end.

**Modify wavelet**

The wavelet can be modified using the equation editor. The input wavelet is called $Vol1, and the time axis is called $t. See section 2.7 for details of the equation editor.

**Frequency Domain**

**Zero phase**

Converts the input wavelet to zero-phase. There are no parameters.

**Smooth spectrum**

Applies smoothing separately to the amplitude spectrum and unwrapped phase spectrum. It is not possible to smooth just one of them separately. Options are i) median filter, ii) weighted smoothing with Gaussian weights, iii) linear weighting, iv) an unweighted moving average. In all cases, the user specifies the half-length of the filter in samples.

**Frequency filter**

Applies an Ormsby (trapezoidal) filter to the input.

**Modify spectrum**

Uses the equation editor to modify the wavelet spectrum. There are separate equations for the amplitude and the phase spectrum. The input wavelet is called $Vol1, and frequency is called $f. 

**Other**

**Stack**

Sum a user defined range of pre-stack wavelets into one wavelet.

**Create Sub Wavelet**

Extract a user defined range from a set of pre-stack wavelets

**Merge trace into**

Merge back a single wavelet into a set of pre-stack wavelets.

**Matching operator**

This function designs a matching operator from the input wavelet to another target wavelet. Only wavelets with the same sample interval as the input appear in the list of target wavelets.

Once it has been created, the operator can be applied to another wavelet using the Convolve Wavelets function. The operator is designed using a time-domain least-squares algorithm. It has user defined parameters for operator length and the white noise.

There is an option to perform spectral shaping only. This is recommended for offset or angle dependent balancing if the goal is to perform a conditioning for AVO. The spectrum of each matching operator is divided by the mean amplitude within the defined frequency range. A fairly narrow range should be selected where there is strong signal, so that on average the amplitude is untouched within this band. 

**Colored inversion operator**

Colored inversion is a special case of matching. The input is usually a zero-phase seismic spectrum, and the target wavelet is a well-log spectrum created using Well Log Spectrum. The operator has a $$90^o$$ phase rotation built into it.

**Convolve wavelets**

The input wavelet is convolved with a wavelet selected from the list. Only wavelets having the same sample interval as the input are shown.

**Convolve**

The Convolve function permits convolution of a wavelet with a volume from the memory pool. The desired wavelet must first be saved to the project. The drop-down list is used to select a volume from the volume pool. The desired wavelet should also be highlighted in the wavelet list. Then clicking the Convolve button opens the User-Defined Filter tool with the correct inputs defined.
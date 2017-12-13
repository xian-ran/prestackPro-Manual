### Spectral Attribute Calculator {#spectral-attribute-calculator}

Spectral properties of seismic often are extracted from time-frequency spectra to QC the seismic signal. Those calculations can be done directly in Pre-Stack Pro.

Go to **Attributes** → **Spectral Attribute Calculator**

Spectral Attributes QC options

**Compute Amplitude and phase spectrum:** two output volumes will be created for the complex spectrum, one containing the amplitude spectrum and the other one containing the phase spectrum.

**Compute real and imaginary spectrum:** two output volumes will be created for the complex spectrum, one containing the real component and the other one containing the imaginary component of the spectrum.

**Compute Power Spectrum:** a volume containing the power spectrum of the input volume will be created.

The **result Scaling Mode** selects with which factor the resulting spectrum will be scaled. The selection here influences the scaling mode which should be used in the Inverse FFT. The product of the scaling factors must give 1.0 for correct amplitudes after the Inverse FFT.

Reasonable combinations are:

*   FFT: 1/N, Inverse FFT: No scaling
*   FFT: No scaling, Inverse FFT: 1/N
*   FFT: sqrt(1/N), Inverse FFT: sqrt(1/N)
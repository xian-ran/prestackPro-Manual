### Inverse Fast Fourier Transformation {#inverse-fast-fourier-transformation}

Inverse Fast Fourier Transformation

Use real and imaginary spectrum option selected

2 options are available depending on which volume available you have available:

**Use Real and imaginary spectrum:** a complex spectrum consisting of the two volumes, one containing the real component and the other one containing the imaginary component of the complex spectrum will be used as input for the Inverse FFT.

**Use amplitude and phase spectrum:** a complex spectrum consisting of the two volumes, one containing the amplitude spectrum and the other one containing the phase spectrum of the complex spectrum will be used as input for the Inverse FFT.

The **result Scaling Mode** selects with which factor the resulting spectrum will be scaled. The selection here influences the scaling mode which should be used in the Inverse FFT. The product of the scaling factors must give 1.0 for correct amplitudes after the Inverse FFT.

Reasonable combinations are:

*   FFT: 1/N, Inverse FFT: No scaling
*   FFT: No scaling, Inverse FFT: 1/N
*   FFT: sqrt(1/N), Inverse FFT: sqrt(1/N)

If the input spectrum volumes consist only of the positive frequency part of the spectrum, the **“_Input is missing negative frequencies use complex conjugate instead”_** must be enabled. The complex conjugate of the input spectrum will be used for the negative frequency part of the spectrum, otherwise the result will be wrong for spectrum volumes used as input. The option to discard the negative frequencies exists in the [FFT](fast_fourier_transformation.md) GUI.

By using an **oversampling factor** greater than 1.0, an output volume with a finely grained sampling can be created. The sampling will be higher than the actual maximum frequency of the input spectrum.

This sampling is done internally by extending the input spectrum accordingly to a higher maximum frequency. This extended part of the input spectrum is filled with zeros.

The dimensions of the resulting output volume are available at the bottom of this dialog box in the **Result dimensions** part. The sampling distance can be modified via the &quot;Oversampling&quot; and &quot;Use Complex Conjugate&quot; options.
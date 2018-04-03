### Wavelet tool {#wavelet-tool}

The wavelet tool is designed to perform interactive design and manipulation of wavelets, spectra, and filters. In particular, common geophysical tasks such as spectral shaping, whitening, and colored inversion can be carried out using the wavelet tool to design the operators. It has a variety of signal processing functions which can be used in a flexible way to achieve the desired result. In Pre-Stack Pro we use the word “wavelet” in a very general sense to include seismic wavelets, spectra, and filters or operators.

The wavelet tool is designed to be used in conjunction with the spectral analysis tool and the user-defined filter tool. A typical workflow to shape a seismic spectrum to some desired filter would be:

Estimate the actual seismic spectrum in the spectral analysis tool, and save it to the project.  
Load the spectrum into the wavelet tool and design a shaping operator, saving that to the project.  
Apply the shaping operator to the seismic volume using the user-defined filter module.

Some example workflows are described in more detail: [Example Workflows](/algorithm_documentation/interpretation-processing/wavelet_tool/example_workflows.md)


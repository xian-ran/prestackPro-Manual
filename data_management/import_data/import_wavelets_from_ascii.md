## Import Wavelets from ASCII {#import-wavelets-from-ascii}

Wavelets should be exported from other software packages as ASCII files.

![](/assets/001_import_wavelet.png)

In the Data Selection tab, the only required Content column is for Data Values.

![](/assets/002_import_wavelet.png)

The Additional Parameters tab must be selected to define the sample rate and start time of the wavelet.

![](/assets/003_import_wavelet.png)

Note that the sample interval is given in milliseconds. Either set the start time, which is the time of the first sample \(this would be negative for a zero phase wavelet\), or set the T0 Sample Number in the file of the sample at time zero. Typically this is half the wavelet length in samples. The remaining fields are filled in automatically

Once the wavelet has been imported, it can be viewed using the [Wavelet Manager in the Utilities menu](/algorithm_documentation/interpretation-processing/wavelet_tool/README.17.md). In particular, check that the time zero is correct and is not shifted by one sample \(which may happen depending on conventions used in the software package used to export the wavelet\).

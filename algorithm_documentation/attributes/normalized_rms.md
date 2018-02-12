### Normalized RMS {#normalized-rms}

Go to **Attributes** → **Normalized RMS**

The NRMS is RMS of the difference between two input volumes in a moving window, normalized by the average RMS of the inputs. This is used as a QC attribute to measures the similarity between 2 input volumes within a moving window. 

Values are between 0 and 2, 0 means the two volumes are exactly the same and the value increases as the volumes become more dissimilar. It is affected by: time shifts, amplitude ratio and phase shifts.

The input volumes must have the same geometry.
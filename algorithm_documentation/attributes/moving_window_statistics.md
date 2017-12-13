### Moving Window Statistics {#moving-window-statistics}

The **Moving Window Statistics** calculates some of the classic attributes statistics used for interpretation and characterization directly in Pre-Stack Pro. Go to:

**Attributes** → **Moving Window Statistics**

The user specifies the size of the window half-length. The calculation is carried out trace by trace for each attribute (except for the semblance, which is defined by a neighbourhood).

For each trace, the window is moved sample by sample in the vertical direction (time or depth) so that the attribute is calculated its centre. The following statistical attributes can be computed:

*   **RMS Value**: Computes the root mean square value defined as the square root of the arithmetic mean of the squares of the window samples.
*   **Maximum/Minimum Sample**: Searches for the maximum/minimum sample within the window.
*   **Absolute Maximum Sample**: Searches for the maximum sample in absolute value within the window.
*   **Signed Absolute Maximum Sample**: Searches for the maximum sample in signed absolute value within the window.
*   **Mean Value**: Computes the arithmetic mean value within the window.
*   **Number of Zero-Crossings**: Counts the number of sign changes within the window.
*   **Median**: Computes the median, i.e. the value that separates the higher half of the window sample from the lower half.
*   **Semblance**: Computes the semblance within offset class of a volume for a given time window. The user needs to specify a spatial Neighborhood. This stencil is defined by selecting the half-length in the inline and cross-line directions and the number of points is displayed as _Current filter size_. Semblance is a measure of coherency and is obtain from the following formula:

Where **t** are the time samples within the window, **N(j)** is the spatial stencil around trace j and **#N** is the number of trace in N.

*   **Spectral Bandwidth**: It is an estimate on how broad the main lobe of the power spectrum is. Thus it is related to time resolution, as a high bandwidth implies a short wavelet in time. The output attribute is a bandwidth volume in Hz.
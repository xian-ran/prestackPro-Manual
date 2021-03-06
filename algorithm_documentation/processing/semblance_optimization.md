### Semblance Optimization {#semblance-optimization}

Semblance Optimization is the first version of a trim static algorithm. [Align 2](/algorithm_documentation/processing/align_2.md) is superior and should be used. 

The aim of this algorithm is to flatten events in gathers. In the neighboring trace option each trace is cross-correlated with its neighbor to define a relative timeshift, while in stacked trace option all traces in the gather are cross-correlated with the reference trace which is usually a near or mid offset stack. The data are only shifted if the correlation values exceed a user-defined threshold \(**Min. Correlation**\). All of this is performed in a moving time window.

To open the Semblance Optimization, go to: **Processing** → **Semblance Optimization**

![](/assets/055_Processing.png)

_Semblance optimization_

**Left part of the window:**

Preview on the currently selected input gather. This selection can be done in the data selection area or by gather catching \(right click on the gather\)

**Mid part of the window:**

**Data selection**

The data selection is used to select the seismic input volume and, if needed, the time shifts. The inline and crossline for the preview calculation can be selected.

**Select output to display**

The type of data to be displayed on the right side of the window can be selected here. By default, the selection is set to output gather, but other output can be display such as time shifts, or Correlation Values. They can be very useful QC tools.

![](/assets/056_Processing.png)  
_Basic tab_

The **TimeShift increment** should be set to the smallest possible value \(0.0001 seconds\).

When using **neighboring trace**, the maximum **TimeShift** value would typically be a small value, for example 0.002 seconds.

When using the **stacked trace** option, the maximum **TimeShift** should not exceed a quarter of the length of the wavelet.

![](/assets/057_Processing.png)  
_Expert tab_

**Preprocessing** enable will evaluate the signal to noise ratio and will select events where the ratio exceeds the threshold to calculate statics correction. **Postprocessing** with **Desmoothing** will interpolate timeshifts without additional processing.

**Smoothing:**

**Smoothing** will smooth timeshifts in the time direction before they are applied.

![](/assets/058_Processing.png)

**Filter Type:**

The parameters of the filter type can be set on the Filter Half Lengths sub part of the tab.

* **-Gauss:** will do a gauss smoothing. The values of the filter coefficients follow a Gauss curve in all directions, symmetrically from the center.
* **-linear ramp:** will apply a weighted averaged filter with the coefficients decreasing linearly proportionally to the distance to the center.
* **-unweighted average:** will do an unweighted average over the full  filter, all the filter coefficients have the same value.
* **-unweighted average \(cross\):** will apply an unweighted average filter over the selected main directions.  

**Filter Half Lengths:**

In this part we can select the lengths of the filter in the Inline and Crossline direction.

**Filter Info:**

This tab indicates the size of the current filter in all direction. The runtime for the smoothing is linearly proportional to the size of the filter

**Right part of the window:**

Preview of the output gather of the algorithm with the current parameters. The traces can also be visualized:

![](/assets/059_Processing.png)

_Trace visualization as output_

![](/assets/060_Processing.png)




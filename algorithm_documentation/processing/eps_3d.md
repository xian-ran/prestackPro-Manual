### EPS 3D {#eps-3d}

EPS 3D is a 3D edge-preserving smoothing filter that works on stacks and gather datasets. When executed on pre-stack data, the algorithm processes each common-offset plane as a stack and recombines to gathers.

To open the EPS 3D parameter dialog go to: **Processing** → **EPS 3D**

As the algorithm works on individual common offset planes, the previews are sorted in the same way. The user can choose which plane to look at:

![](/assets/027_Processing.png)

_Preview of EPS 3D. The field to choose the offset plane is highlighted._

2 filter modes \(scan modes\) are available:

* DipScan \(SCAN\)
* Horizontal edge-preserved smoothing \(EPS\)

**The dip scanning mode**, as the name suggests, estimates the dip direction of the reflector by a semblance-based scanning process, and filters along the dip direction. The maximum dip between traces can be set, as well as the dip increment \(which specifies the size/number of time-shift steps for scanning\).

Once dips are determined, a median filter is applied to samples in the dip direction. The filter is applied in two passes, first in the inline direction, then on crosslines. The number of traces used in this process can be specified in the filter size and a cross-shaped stencil is used.

**The horizontal mode** involves no dip scanning.

The output trace at each sample is obtained by averaging the samples of all traces inside the stencil. The number of traces is selected by the filter size option and it works on all traces quadratic around the central location. If the filter size is set to 0, no smoothing will be done. The output will be the original dataset.

Weights for this weighted averaging are obtained by using correlation coefficients. If the correlation is high the weight is high; if the correlation is low the weight is low, accordingly. If the correlation is lower than the threshold parameter the trace at this sample location is ignored. This mechanism avoids smearing across faults.

The lower the correlation threshold, the more impact the smoothing will have. If the correlation threshold is set to 1, no smoothing is applied.

Example on a stack:

![](/assets/028_Processing.png)



![](/assets/029_Processing.png)


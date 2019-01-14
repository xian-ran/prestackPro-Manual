# Phase Decomposition



![User Interface for Spectral Decomposition](../../.gitbook/assets/001_phasedecomp.png)

**Input Data:** input volume is of type seismic and can be stacked or pre-stack. The input wavelet must be zero-phase.

**Minimum Phase, Maximum Phase and Phase Step:** range of the phase rotation applied to the input wavelet. 

The output will be a volume of the same geometry as the input except for an extra gather axis for the phase.

**Output Map**: if ticked on the output will be a map instead of a full volume, either at a **Horizon** or a constant **fixed time**. 




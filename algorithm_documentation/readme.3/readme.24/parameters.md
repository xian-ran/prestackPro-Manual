# Parameters

The parameters window controls the semblance spectrum display and computation, as well as the NMO gather computation. The semblance is computed from the input velocity volume. This velocity volume is a non-editable reference and must be the one used for the NMO correction applied on the data. In a typical workflow, this would be either the migration or the stacking velocity field, depending on the processing stage at which the SEG-Y were created.

**Basic parameters**

* **Velocity Spectrum:** set the range \(**From Velocity** and **To Velocity**\) as well as the sampling interval \(**Step size** and **Numbers of steps**\) to compute the semblance spectrum.
* **RMO Semblance:** standard semblance computed within the range defined above
* **Eigen semblance:** semblance adapted for class IIp events
* **Window half-length:** defines the window used to compute the semblance. We recommend to set this up to the dominant wavelength
* **Taper Length:** taper applied to the upper and lower bound of the window used to compute the eigen semblance.
* **Show corridor:** Limit the semblance spectrum to a percentage of the input velocity. 

**Expert parameters:**

* **NMO Stretch:** Due to the $$t_0$$-dependence of the NMO formulas, wavelet stretch in time, after NMO correction, has an increasing effect with smaller $$t_0$$ time and larger offset. For each $$t_0$$ time, the offset for which the stretch exceeds the given value is determined and all amplitudes are removed for larger offsets.
* **Velocity perturbation:** All velocity values are multiplied with this factor. This option is introduced to systematically over-/under-correct the gathers - for example for Radon based multiple removal.
* **Noise level:** For adding white noise to the input prior to the semblance computation. 


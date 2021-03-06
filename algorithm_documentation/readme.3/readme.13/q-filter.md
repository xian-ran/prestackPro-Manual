# Q-Filter

Q filter takes a single Q value and applies a correction to the entire dataset. Depending on prior processing phase-only corrections can be applied rather than both amplitude and phase since amplitude corrections tend to boost the noise.

To open the Q Filter dialog go to: **Processing** → **Q Filter**

![](../../../.gitbook/assets/033_processing.png)

_Q- Filter phase compensation only_

In the **Modelling Parameter** section algorithm definitions are made. The **Reference Frequency** value is only relevant when using this algorithm with phase changes included. We recommend setting the value in the middle of the seismic frequency band.

The **Gain Limit** parameter sets an upper limit for amplification similar to a cutoff limit. It is only relevant when changes to the amplitude are made.

**Qaverage** is the Q value applied to the dataset. The value used should be the effective value between the surface and the target. If offset-dependent processing is required, we recommend applying Q Filter to data without NMO correction applied.

The algorithm is not highly sensitive to the **RMS Velocity** value, but we recommend setting it to the velocity at your target. This parameter only influences the phase behavior.


# Q-Filter

Q filter takes a single Q value and applies a correction to the entire dataset. Depending on prior processing phase-only corrections can be applied rather than both amplitude and phase since amplitude corrections tend to boost the noise.

To open the Q Filter dialog go to: **Processing** → **Q Filter**

![Q-Filter interface](../../../.gitbook/assets/image%20%282%29.png)

A v**elocity model** is an optional input. If selected then it will be used to account for the water layer where attenuation does not occur. The TWT of the water botom can be input as an **horizon** or a **fixed value**. 

In the **Modelling Parameter** section algorithm definitions are made. The **Reference Frequency** value is only relevant when using this algorithm with phase changes included. We recommend setting the value in the middle of the seismic frequency band.

The **Gain Limit** parameter sets an upper limit for amplification similar to a cutoff limit. It is only relevant when changes to the amplitude are made.

**Qaverage** is the Q value applied to the dataset. The value used should be the effective value between the surface and the target. If offset-dependent processing is required, we recommend applying Q Filter to data without NMO correction applied.

The algorithm is not highly sensitive to the **RMS Velocity** value, but we recommend setting it to the velocity at your target. This parameter only influences the phase behavior.


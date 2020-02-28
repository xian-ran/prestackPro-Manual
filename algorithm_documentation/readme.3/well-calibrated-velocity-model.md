# Well Calibrated Velocity Model

Go to **Processing --&gt; Well Calibrated Velocity Model**

The output of this is a velocity model calibrated to the Vp log of one or several wells. There are two possible methods:

* Without a seismic velocity model as guiding input, it will uses the [CRAVA background model builder](../readme.4/crava/crava-inversion.md) algorithm:
  * Low-pass filter the well data
  * Create depth trends
  * Horizon guided interpolation of depth trends
  * Krig the filtered velocities onto the depth trend volume
* With a seismic velocity volume as guiding input:
  * Low-pass filter the well data
  * For each well, find a scaling factor trace to match the seismic interval velocity to the well trend
  * Horizon guided interpolation of depth trends
  * Apply scaling factor to seismic velocities
  * Krig filtered velocities onto the depth trend volume

![Well Cailbrated Velocity Model](../../.gitbook/assets/image%20%2863%29.png)

## Parameters

On the left the choice to use a seismic velocity cube to guide the velocities. If the check box is ticked on then **Interval velocity** must be selected. The **Transition zone thickness** is explained in the figure below. It is the thickness of the zone linearly interpolated from the seismic velocity down to the velocity of the first checkshot point. The **Max velocity ratio** is a threshold: If the value of the ratio TVD divided by TWT  goes beyond the max velocity ratio, it will be set to the max velocity ratio.

![](../../.gitbook/assets/image%20%2845%29.png)

The **output geometry** is either free form or can be matched to any volume loaded in the data pool by clicking **Match to Volume**. If an interval velocity is chosen to guide the output, then the output geometry will be greyed and set to the same as the selected velocity cube.

On the right, the list of wells to use and their associated TD table. The default TD table is chosen however the user can change it by double clicking on the table cell.

The **layer data** is the same as [CRAVA so we refer to this section](../readme.4/crava/crava-inversion.md#zone-definition).


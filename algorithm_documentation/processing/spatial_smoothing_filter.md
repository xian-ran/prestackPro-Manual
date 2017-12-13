### Spatial Smoothing Filter {#spatial-smoothing-filter}

The spatial smoothing filter can be used to create filters in Inline, crossline, time, offset direction or any combination of directions.

Go to: **Processing** → **Spatial smoothing filter**

Gaussian smoothing in the Inline-crossline direction

**Filter selection:**

The filter type can be selected in the Filter Selection. Depending on this choice, the filter coefficients of the 4D filter will be set. By defining the filter half-lengths in some directions to 0, you can create traditional 1D, 2D or 3D filters or 2D offset-time or inline/crossline filters.

**-Gauss:** will do a gauss smoothing. The values of the filter coefficients follow a Gauss curve in all directions, symmetrically from the center.

-**linear ramp:** will apply a weighted averaged filter with the coefficients decreasing linearly proportionally to the distance to the center.

-**unweighted average**: will do an unweighted average over the full 4D filter, all the filter coefficients have the same value.

**-unweighted average (cross):** will apply an unweighted average filter over the selected main directions.

Before after

Result of a Gaussian spatial smoothing in the Inline, crossline and offset direction on gathers
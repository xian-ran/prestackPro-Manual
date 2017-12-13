### Median Filter {#median-filter}

Median filtering can be used to reduce noise in Inline, crossline, time and offset direction or any combination of these. It is often used to reduce noise in the offset direction.

Go to:

**Processing** → **Median Filter**

Median filter dialog

This process computes the median of the values in a moving window. It is possible to filter in horizontal (offset) direction and in the vertical (time) direction.

The values of the spinboxes in every direction define the half-length of the filter. The full length of the filter is then 2xhalf-length+1

If the half-length is 0 for a given direction, the filter will not be applied for this direction
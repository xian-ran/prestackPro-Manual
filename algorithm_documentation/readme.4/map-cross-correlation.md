# Map Cross Correlation

This algorithm cross-correlates two maps between them or a map and an horizon. An example of its use is to look for correlation between an attribute and a structural map.

This procedure calculates the local correlation coefficient \(aka Pearson correlation coefficient\) between two maps or a map and an horizon. The calculation is done over a sliding rectangle of size $$(2*IL_h+1)*(2*XL_h+1) $$ where $$IL_h$$ and $$XL_h$$ are the half-length parameters on each side. The output of the calculation is output at the center of the sliding window.

**Fill holes** will interpolate results in holes inside the input maps. 

NB: Close to the edge of the data, the correlation will be calculated using the part of the aperture which is inside the window. This means that the statistics is no longer strictly comparable between the output at the edge and in the interior of the data. The data closer to the edge than the **inline** and **crossline half lengths** \(for IL and XL edge respectively\) will be affected by this.

![Map Cross correlation parameters](../../.gitbook/assets/image%20%2824%29.png)


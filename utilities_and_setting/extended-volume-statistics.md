# Extended volume statistics

**Utilities --&gt; Extended Volume Statistics**

This module computes statistics for any volume or horizon and show the data distribution. 

![User interface of Extended volume statistics](../.gitbook/assets/image%20%2847%29.png)

The primary output is the histogram showing the density \(number of occurences\) for a bin of the content values, in red. The blue curve is the cumulative density. The axes context menu contains an option to normalize both the density and the cumulative density. Under there are readout, information and statistics. 

The input can be restricted using a **Map polygon** or a **Z window** \(bound by constant times/depth or using one or two horizons\). The **minimum** and **maximum bin values** default to the volume content extrema. Those can be changed to remove outliers of the statistics. 

The **number of bins** used to compute the histogram can be changed, it defaults to 1024. 

This tool can also be summoned from the context menu of a volume in the Data Pool or from the context menu of a Map Polygon in the Map Viewer. If invoked from those, the input is pre-selected and can not be changed. 

The statistics value can be saved using the button in the tool bar. 


# Auto/Cross-correlation

Go to **Attributes** → **Auto/Cross-correlation**

Auto-correlation of one volume gives information about the presence of periodic events, within the time window chosen for the computation. Cross-correlation of two volumes is a measure of the similarity between them. It will also give a measure of the time-shifts/phase rotation between the two volumes.

![](../../.gitbook/assets/016_attributes.png)

_Dialog for auto/cross-correlation_

**Auto-correlation/Cross-correlation:** if Auto-correlation is chosen; only one input volume is necessary. For a cross-correlation, a **Second Input Volume** must be chosen. The geometry of both volumes must be identical, except that it is possible to choose a stack volume and a pre-stack volume. If so, the trace for one location of the stack volume is correlated with all traces of the pre-stack volume at the same location.

**Lead and Lag:** values in seconds or the distance project unit for depth volume, they must be less than the input trace length.

**Time Selection:** it can be constant times, relative to one horizon or between two horizons.

**Normalize:** scales the results so that the maximum value is equal to 1

**Taper:** linear time tapering at the top and bottom of the time window

**Unbiased Correlation Window:** when ticked on, values outside the time window are set to 0.


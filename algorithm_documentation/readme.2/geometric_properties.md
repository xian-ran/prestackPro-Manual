# Geometric Properties

Curvature attributes can be computed from **Attributes** → **Geometric Properties**.

**Input:** These are surface attributes; possible inputs are horizons or 3D \(post-stack\) volumes. In the case of a 3D volume computation, attributes will be performed time slice by time slice.

Curvature attributes are computed inside a 3x3 stencil traveling in the inline and crossline directions. Within each position, a second order polynomial \(quadratic\) surface will be fitted to the data and will be used to derive attributes from analytical expressions. This approach does not require any user parameters.

**Output**

* **Maximum curvature:** This attribute is very effective in delimiting faults and faults geometry. Faults in the figure are represented by the superposition of maximum and minimum curvatures. 
* **Minimum curvature:** Similar to the maximum curvature.
* **Most positive curvature:** First order derivative attribute useful for detecting edges associated with asymmetric \(faults\) and symmetric \(ridges/valleys\) surface features.
* **Most negative curvature:** similar to the most positive curvature.
* **Dip angle:** Angle, with respect to the horizontal, of the maximum dip.
* **Azimuth:** Angle giving the orientation, with respect to Inline direction, of the maximum dip.

![](../../.gitbook/assets/021_attributes.PNG)

_A horizon and its superposition of most positive and negative curvatures_


### Structural Dip {#structural-dip}

Go to **Attributes** → **Structural Dip**

The Structural Dip module calculates a number of attributes related to local dip. The output is the selected attribute volumes, each the same size as the input volume. The module constructs the structural tensor in a small neighbourhood of each output point, and analyses it to find the required attributes. 

**Dip Inclination:** the angle between the normal to the local dip plane and vertical. This is only available for depth volumes.

**Dip Azimuth:** the angle between the north and the dip direction. 0 degree is the true geographical north, values are increasing clockwise.

**Inline Slope:** The dip in seconds/meter in the direction of increasing crossline number. The value is positive if the event becomes deeper with increasing crossline number.

**Crossline Slope:** The dip in seconds/meter in the direction of increasing inline number. The value is positive if the event becomes deeper with increasing inline number.

**Total Slope:** The magnitude of the slope (i.e. the slope in the dip direction). This is always positive.

**Plane Reflector:**  A quality attribute measuring how planar the surface is within the calculation neighbourhood. It takes values between zero and one, with one being a perfectly plane reflector.

**Faulting:** A complementary attribute to the plane reflector. It takes values between zero and one, with higher values indicative of discontinuities or complex reflections.

It should be noted that where the data are strongly spatially aliased, the dip estimates may be incorrect.
#### The axis definition tab {#the-axis-definition-tab}

![](/assets/001_import_javaseis.png)

_javaSeis wizard axis definition tab_

**The Axis definition tab** allows definition of the axis of the output volume

**Identified axis:**

This display shows the dimension of the axis as they were present in the original JavaSeis header XML file. The axes are ordered from highest to lowest access speed.

In addition to the original name of the axis, units and other information of each axis are shown.

**Axis definition:**

Pre-Stack Pro traditionally works with 3 dimensions \(Inline, crossline, z\) for stack data or 4 dimension \(Inline, crossline, z, offset\) for prestack data. Therefore to work with JavaSeis data, the user needs to map existing axis to Pre-Stack Pro axis.

By default:

* the fastest read axis is set to the z direction

* the slowest read is set to Inline

* the 2nd slowest read is set to crossline

If more than 3 axes are available in the input file. It is possible to use this extra information as a gather axis by toggling the “gather axis” option.

**Fixed Values:**

If more axes exist in the original XML, the Fixed values option allows the creation of a cube of the 4 defined dimensions, specified in the axis definition tab, with a constant value for the 5th dimension. As an example, an input file has 5 dimensions where the fifth one is azimuth. It is possible to create an output prestack volume with a fixed azimuth.

The fixed value has to be selected within the existing values of the unused axis.


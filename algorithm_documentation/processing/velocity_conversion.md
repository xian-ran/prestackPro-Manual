### Velocity Conversion {#velocity-conversion}

In addition to the on-the-fly conversion done during velocity selection ([Velocity](..\..\select_data\select_velocity.md)) you can also convert velocities between different domains via **Processing** → **Velocity Conversion.** This algorithm is compatible with workflows.

Possible domains are _time interval, time RMS and depth interval_.

![](/assets/cusersvalentinappdatalocaltem.png)

Velocity conversion GUI

**_Conversion from_ time interval _to_ time RMS** _is done via the following formula:_

_Where is the time interval velocity of the layer._

**_Inverse conversion from_ RMS _to_ timeinterval** _properties is done via_ **_Dix’s equation_** _(plane layer assumption). This equation requires some regularization to avoid spikes in the output volume._ **_Expert parameters_** _correspond to the time window half-lengths in milliseconds for the median filter and smoothing filter applied to the input volume._

**_Stretch between time and depth_ **_interval velocities is done using the following relations:_
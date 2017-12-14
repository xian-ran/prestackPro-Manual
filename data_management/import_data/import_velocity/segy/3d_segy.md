#### 3D SEGY {#3d-segy}

To import velocity data in SEGY go to:

**Project** → **Import Data** → **Import SEGY**

In the properties tab of the import data from SEGY, you can change the content to Velocity, and the select the velocity type. It can be Interval or RMS.

![](/assets/008_import_velocity.png)

_Properties tab and velocity type_

If the velocity contains samples at the start or end of a trace for which the value is set to 0 m/s, those will be replaced with a constant propagation from the first or last non-zero sample. A pop-up will inform of the amount of samples modified.


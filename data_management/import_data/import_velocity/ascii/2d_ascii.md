#### 2D ASCII {#2d-ascii}

When a 2D line of seismic data is imported into Pre-Stack Pro, an arbitrary path is created for this line containing the corresponding UTM X and Y positions.

Import of ASCII velocity data for a 2D line requires this arbitrary path to exist in the project in order to extract velocities at the UTM coordinates defined for this arbitrary path.

To import ASCII velocity 2D data:

Go to **Project** → **Import Data** → **Import 2D Velocity**

The procedure for importing 2D velocity data is quite similar to that of importing 3D ASCII velocity data, but there are some differences.

When picking live data, the user must specify line number, CMP or shot number, depth or time, and velocity.

![](/assets/006_import_velocity.png)

_Options when picking live data._

If the velocity file contains shot point numbers instead of CMP numbers, an equation must be defined which converts from shot point to CMP number. In the Additional Parameters panel, this equation can be specified. The parameter $ShotNb holds the value of the selected shot point numbers.

![](/assets/007_import_velocity.png)

_Specifying the shot number equation. In this example the CMP number equals shot point number – 2000._

In Pre-Stack Pro version 4.6, only one equation can be defined per imported 2D ASCII velocity file. If the velocity file contains velocity data from several 2D lines, the user must create a separate velocity file for each 2D line and import them separately.

It is also possible to set a line number prefix for the imported velocity files and also to add the files to file groups.


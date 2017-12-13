#### 2D SEGY {#2d-segy}

When a 2D line of seismic data is imported into Pre-Stack Pro, an arbitrary path is created for that line containing the corresponding UTM X and Y positions.

This arbitrary path must exist before 2D SEGY velocities data can be extracted onto the corresponding UTM coordinates.

To import SEGY velocity 2D data:

Go to **Project** → **Import Data** → **Import SEGY 2D Line**

The domain properties must be set.

A default file name is suggested for the imported velocity file, typically “Line-&lt;linenumber&gt;”. If this filename already exists, the user must either edit the file name or add a file name prefix. It is also possible to add the imported velocity file to a file group.

_Setting the domain properties for the imported velocity file._
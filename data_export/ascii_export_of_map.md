## ASCII Export of map {#ascii-export-of-map}

Pre-stack and post-stack maps can be exported as tabulated ASCII files:

**Project** → **Export Data** → **Export Map**

Maps may be selected from the project directory or the data pool. The **add** button gives the option to select and export several maps to a single ASCII file. The inline, crossline and fold geometries must be the same for each of these maps. Co-dependent outputs can be selected using **add with sibling**.

For pre-stack maps, it is possible to export the full map or a sub-mapbelonging to a constant offset / angle class.

All maps can be output as Inline / Crossline, World X / World Y, or both. There are options to change the time and length units (where applicable). The delimiter will separate columns in the ASCII file. (By default, it is a semi colon). If there are any null points in the map, then they can be replaced by a user defined value (for example -999.25).

Export to Map Dialog
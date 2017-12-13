### Offset to Angle {#offset-to-angle}

Pre-Stack Pro allows to change the gather offset sorting from distance bins to angle bins. A velocity field is necessary to open the **Offset to Angle** dialog.

Go to:

**Interpretation Processing** → **Offset to Angle**

The dialog window is divided into two parts:

Offset to angle module dialog

**Left part of the window:**

This algorithm needs a seismic input volume in the **offset domain**. To apply plane layer ray tracing, the algorithm also needs an **interval velocity** field with the same inline/crossline dimensions as the seismic volume but starting from t<sub>0</sub> = 0\.

If the RMS-Velocity base mapping method is selected, also a **RMS velocity** is required. Both velocity fields can be selected using the loading buttons.

Velocity loading buttons

Once this button pressed, the following windows open. The velocity selection can be done on the top part of this window. The velocity data properties are available here.

Velocity selection

Conversion

Pre-Stack Pro supports conversion from RMS to interval velocity and vice versa. These options are available from the **&quot;Conversion&quot; Tab** in the parameter selection. If the selected velocity does not fit the selected algorithm, the algorithm will complain and give feedback, what kind of velocity is needed (e.g. Offset to Angle needs an interval velocity with sampling starting at zero). For more information, please refer to the [velocity](..\..\select_data\select_velocity.md) section of this manual

All information concerning the size, the range of the velocity and seismic data are available in the tabs in the central part of this window. In addition, the velocity processing history can be found in the last tab.

By choosing a **Minimum** and **Maximum** angle limit and an **Angle Step** the range and the sampling density of the output angle gathers are set. The angle gathers have ((maximum angle-minimum angle)/angle step)+1 traces.

The possible **Output** volumes are:

*   **Angle Muted Gather:** offset gather muted with the given min/max angles.
*   **Angle Gather**: angle gather in the defined range from min to max angle.
*   **Angle map:** offset gather, where every sample shows the corresponding angle it was will transform into.

**The method** defines the mapping method between recorded offset at the surface and incidence angle on the target reflector. This can be done either with **plane layer ray tracing** or by applying a closed form expression (**Walden&#039;s equation**).

The mapping between recorded offset _h_ at the surface and incidence angle _q_ on the target reflector can be established by performing plane layer ray tracing (method 1) or by applying a closed form expression (method 2). Instead of working directly with the angle _q_, both methods are mapping offset to ray parameterwith conversion from p to angle with known local interval velocity vi.

Method 1:

The _z_-dependent relation between offset _h_ and _p_ reads

or expressed in terms of vertical interval traveltime :

where the index _i_ of can be dropped if one uses the constant sampling interval . _p_ is constant for the type of (laterally constant) medium under consideration. These equations can not be inverted for _p_. However, it is possible to perform ray tracing for given p values and to interpolate in offset direction.

The routine works locally on CDPs. Input is a flag whether the vertical direction is time or depth, the 1D-velocity function for the current CDP (with the vertical unit as chosen by the flag), , , and and , or , , respectively. Output is a map .

Method 2:

Walden’s equation

provides a closed form expression between offset and ray parameter using rms effective velocities. No ray tracing with interval velocity models needs to be performed. However, interval velocity model is still needed for the final conversion from p to angle.

An option to **taper** velocity changes is also present. The preferred value for this parameter should be 0 since it reduces the artifacts from angles outside the extreme offset available.

**Right part of the window:**

The **Input Gather** displaying the gather corresponding to the inline- crossline pair noted in the **Data Selection** at the top-center of the dialog.

The **Angle Gather** displays the selected gather in the angle domain, while the **Angle Muted Gather** display is in the offset domain, with the data muted along respectively the minimum angle and the maximum angle of incidence. The **Angle Map Gather** shows the relationship between angles and offsets. It is color coded by angle values.
### Offset to Angle {#offset-to-angle}

Pre-Stack Pro allows to change the gather offset sorting from distance bins to angle bins. A velocity field is necessary to open the Offset to Angle dialog.

Go to: **Interpretation Processing** → **Offset to Angle**

The dialog window is divided into two parts:  
![](/assets/001_Interpretation.PNG)

_Offset to angle module dialog_

**Left part of the window:**

This algorithm needs a seismic input volume in the **offset domain**. To apply plane layer ray tracing, the algorithm also needs an **interval velocity** field with the same inline/crossline dimensions as the seismic volume but starting from $$t_0 = 0$$.

If the RMS-Velocity base mapping method is selected, also a **RMS velocity** is required.

![](/assets/002_Interpretation.png)  
_Velocity loading buttons_

Once this button pressed, the following windows open. The velocity selection can be done on the top part of this window. The velocity data properties are available here.

![](/assets/003_Interpretation.png)  
_Velocity selection_

![](/assets/004_Interpretation.png)  
_Conversion_

Pre-Stack Pro supports conversion from RMS to interval velocity and vice versa. These options are available from the **"Conversion" Tab** in the parameter selection. If the selected velocity does not fit the selected algorithm, the algorithm will complain and give feedback, what kind of velocity is needed \(e.g. Offset to Angle needs an interval velocity with sampling starting at zero\). For more information, please refer to the velocity section of this manual

All information concerning the size, the range of the velocity and seismic data are available in the tabs in the central part of this window. In addition, the velocity processing history can be found in the last tab.

By choosing a **Minimum** and **Maximum** angle limit and an **Angle Step** the range and the sampling density of the output angle gathers are set. The angle gathers have \(\(maximum angle-minimum angle\)/angle step\)+1 traces.

The possible **Output **volumes are:

* **Angle Muted Gather:** offset gather muted with the given min/max angles.
* **Angle Gather:** angle gather in the defined range from min to max angle.
* **Angle map:** offset gather, where every sample shows the corresponding angle it was will transform into.

**The method** defines the mapping method between recorded offset at the surface and incidence angle on the target reflector. This can be done either with **plane layer ray tracing** or by applying a closed form expression \(**Walden's equation**\).

The mapping between recorded offset h at the surface and incidence angle q on the target reflector can be established by performing plane layer ray tracing \(method 1\) or by applying a closed form expression \(method 2\). Instead of working directly with the angle q, both methods are mapping offset to ray parameter $$P = \frac{Sin\theta _i}{V_i}$$ with conversion from p to angle with known local interval velocity $$V_i$$.

**Method 1:**

The z-dependent relation between offset h and p reads


$$
h(Z_N,P) = \sum_{i=1}^N\frac{2V_iP}{\sqrt{1-P^2V_i^2}  }\Delta Z_i
$$


or expressed in terms of vertical interval travel time


$$
\Delta t_i = \frac{2\Delta Z_i}{V_i}:
$$



$$
h(t_N,P) = \sum_{i=1}^N\frac{V_i^2P}{\sqrt{1-P^2V_i^2}}\Delta t_i
$$


where the index $$i$$ of $$\Delta t_i$$ can be dropped if one uses the constant sampling interval $$\Delta t$$ . $$P$$ is constant for the type of \(laterally constant\) medium under consideration. These equations can not be inverted for $$P$$. However, it is possible to perform ray tracing for given $$P$$ values and to interpolate in offset direction.

The routine works locally on CDPs. Input is a flag whether the vertical direction is time or depth, the 1D-velocity function for the current CDP \(with the vertical unit as chosen by the flag\), $$\theta_{min}$$  , $$\theta_{max}$$ , and  $$\Delta \theta$$ and $$t_{min}$$ , $$t_{max}$$  or $$Z_{min}$$ , $$Z_{max}$$ , respectively. Output is a map $$h(t_i,\theta_j)$$.

**Method 2:**

Walden’s equation


$$
P = \frac{h}{\sqrt{t_0^2+\frac{h^2}{V_{rms,i}^2}} }\frac{1}{V_{rms,i}^2}
$$


provides a closed form expression between offset and ray parameter using rms effective velocities. No ray tracing with interval velocity models needs to be performed. However, interval velocity model is still needed for the final conversion from p to angle.

An option to **taper** velocity changes is also present.  The preferred value for this parameter should be 0 since it reduces the artifacts from angles outside the extreme offset available.

**Right part of the window:**

The **Input Gather** displaying the gather corresponding to the inline- crossline pair noted in the **Data Selection** at the top-center of the dialog.

The **Angle Gather** displays the selected gather in the angle domain, while the **Angle Muted Gather** display is in the offset domain, with the data muted along respectively the minimum angle and the maximum angle of incidence. The **Angle Map Gather** shows the relationship between angles and offsets. It is color coded by angle values.


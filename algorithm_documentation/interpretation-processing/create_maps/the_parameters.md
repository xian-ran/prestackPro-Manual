#### The parameters {#the-parameters}

**Input Selection**

General attributes can be calculated from input stacks or any set of gathers. Angle attributes \(AVA\) are currently calculated from angle gathers only.

The reference for the attribute extraction can be a horizon or a fixed time.

**Map settings**

Create map at:

* **At horizon position:** this is the default option. Attributes are calculated by extracting amplitudes at the imported horizon time value for each seismic trace.
* **Snap to:** the input horizon is used as “seed” for **snapping** to specific events within a **search window**, to create a new reference time.

The result of the snap will always be within search window.

Snapping may be applied to **gathers or stacks**, and is useful for fitting imported horizons to peak or trough amplitude events within a narrow search window

**Track:** the input horizon is used as “seed” for **tracking** to specific events within a **search window**, to create a new reference time. The tracking of the horizon can happen outside the search window.

Tracking is only applied to **pre-stack datasets**, and may be more useful where gathers show significant moveout. When this option is used, tracking begins by adjusting the horizon to the near traces and then attempts to follow this event out to the fars

A **Time shift** from the input horizon can be applied in this window. The time shift will be applied before snap/track or before the extraction of the attribute.

**The search window** \(time less and time greater\) is only active when snap or track is active. The input horizon or the input horizon with time shift will be the reference point for this search window.

Snapping and tracking may produce significantly different results, depending on data quality and the complexity of the reflectivity sequence within the specified window

![](/assets/183_Interpretation.png)

_2D Gather Viewer showing adjusted horizon positions, calculated for two gathers, using the “snap” and “track” options._

The updated horizon time values can be calculated to the nearest sample time \(commonly 4 ms\) or to a sub-sample accuracy by interpolation by toggling the **“use sub-sample accuracy”** option

**Attributes:**

![](/assets/Create_maps.png)

_Create Attribute Map - attribute GUI_

Several attributes can be calculated simultaneously. Simply toggle on the required attributes in the lists. The different outputs created will then be considered as **siblings**.

* For attributes that are to be calculated over a window, the window half length must be specified.  
* **Angle attributes** are identical to those already available as AVA attribute volumes, but are computed at a horizon. 

The **“smooth maps”** option \(Quality setting\) option applies a basic smoothing to any calculated attribute maps. Any horizon attribute may also be filtered with full user control, using Pre-Stack Pro’s spatial smoothing or median filter modules.

**The output**

All generated attributes are output as new objects in the data pool, and may be saved to the project \(MB3 menu\).

All the siblings can be selected simultaneously: right click on one of the outputs and select “select with sibling volumes”.

Once highlighted, you can then display all the attributes in map view [PreStack Map viewer](/viewers/2d_prestack_map_viewer.md) or [Map viewer](/viewers/2d_map_viewer/README.6.md).  Right click on the white part of the datapool and select “show selected volumes in XXXX viewer”

![](/assets/185_Interpretation.png)

_Select with sibling volumes_

![](/assets/186_Interpretation.png)  
_Data selection_

![](/assets/187_Interpretation.png)

_Value extracted after tracking_

Sibling volumes are available in the “displayed volumes” selection individually. In addition, they can be activated/ deactivated as a group in the 2nd section on the left of the window. They are all grouped in the object called in this example “group 137”


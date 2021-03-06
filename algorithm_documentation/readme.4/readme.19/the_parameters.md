# The parameters

**Input Selection:**

General attributes can be calculated from input stacks or any set of gathers. The reference for the attribute extraction can be a horizon or a fixed time.

**Map settings:**

Define top and bottom interval border, either with horizon and shift or with fixed time/depth.

![](../../../.gitbook/assets/191_interpretation.png)  
_Map settings_

**Expert parameters:**

Select “Expert parameters” if snapping or tracking of input horizons are necessary.

![](../../../.gitbook/assets/192_interpretation.png)  
_Expert parameter settings_

Click “Apply” to update Horizon and Isochrone display. The “Extract Attributes” will then become active and attributes to be computed can be selected.

**QC Maps:**

QC maps are displayed after hitting “Apply”. User can select to QC Top Horizon, Bottom Horizon and Isochrone maps.

![](../../../.gitbook/assets/193_interpretation.png)  
_QC map of Top Horizon_

![](../../../.gitbook/assets/194_interpretation.png)  
_Dropdown menu for QC options_

**Attributes:**

Attributes to compute are

* RMS
* Max. Sample Between Horizons
* Min. Sample Between Horizons
* Max. Abs. Sample Between Horizons
* Mean
* Number of zero-crossings
* Median
* Spectral Bandwidth

Toggle on the attributes of choice in the **Extract Attributes** panel. Attribute maps will appear in the right part of the GUI.

![](../../../.gitbook/assets/195_interpretation.png)  
_GUI of Create Interval Maps including Attribute Maps_

![](../../../.gitbook/assets/196_interpretation.png)  
_The dropdown menu for attribute maps will include the toggled on attributes._

Clicking “Calculate” will compute and output to the Data Pool attribute maps of the attributes that were toggled on.

If the user toggles on “Output Snapped Horizons” and “Output isochrone”, these maps will be generated and put into the Data Pool when clicking “Calculate”.

![](../../../.gitbook/assets/197_interpretation.png)

_Toggling on for outputting horizons and isochrones_


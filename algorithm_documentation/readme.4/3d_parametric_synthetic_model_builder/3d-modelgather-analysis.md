# 3D Model/Gather analysis

In this example, the amplitude changes from a peak to a trough \( yellow to blue \) when brine is replaced with gas.

![](../../../.gitbook/assets/026_interpretation.PNG)

The polarity reversal location, shown by the zero amplitude white band, occurs with less % gas as porosity decreases, and the rock becomes weaker and more unconsolidated. Synthetic gathers from the 3D parametric volume are shown in the Data Comparator, below \( Points of interest \(POI\) 1 – 4 \) ![](../../../.gitbook/assets/027_interpretation.PNG)

Looking at the $$V_p$$, $$V_s$$ and density volumes used for the model, we can see how the Gassmann fluid substitution, from brine to gas, has altered the $$V_p$$ much more than the $$V_s$$ or the Density. $$V_s$$ is only slightly affected by the change in density – decreasing density = increasing $$V_s$$. The gas changes $$V_p$$ very quickly with low porosity, because the constant in situ $$V_p$$ → a softer rock.

![](../../../.gitbook/assets/028_interpretation.PNG)

_Top View -_ $$V_p$$_,_ $$V_s$$ _and density timeslices, for top reservoir_

![](../../../.gitbook/assets/029_interpretation.PNG)

$$V_p$$, $$V_s$$ and Density volumes, were output from the modeling, using the create volumes option above.

**1D initial model setup** 

To open up the 3D Parametric Synthetic Model Builder dialog go to:

**Interpretation-Processing** → **3D Parametric Synthetic Model…**

![](../../../.gitbook/assets/030_interpretation.PNG)

and select the $$1^{st}$$ Tab.

If any models have been created before in Pre-Stack Pro, it will use the last model’s parameters to open the GUI. So, you may need to delete some layers using the blue – icon rather than adding layers using the green + icon; or start a new model. Gradual / sloping layer changes can be modelled using the green +  option also.

Target, Top and Bottom layers can’t be deleted but are the same as ordinary layers otherwise.

![](../../../.gitbook/assets/031_interpretation.PNG)

**Ordinary layer GUI**

\( The black flag indicates this layer is a shale for Vs calc by equation \) First go to the target layer and set its top depth \(MD\) and corresponding time \(TWT\). This becomes a fixed depth/time value for the model reference datum.

![](../../../.gitbook/assets/032_interpretation.PNG)

_Target layer GUI – model reference datum = 1000m/1.0sec \( This layer is selected for fluid substitution \)_

Set thicknesses for all the layers, and then decide which layers are reservoir rocks and will need fluid substitution. The target layer above, has fluid substitution enabled by selection of the ‘Reservoir’ option - the right hand ‘Fluid substituted’ $$V_p$$, $$V_s$$ and Rho values are now set as the layer properties

**1D layer properties definition :**

**Ordinary** layers can have their $$V_p$$/$$V_s$$/Rho values entered manually, input from well log zone or PCube facies averages, or calculated by equation.

**Reservoir** layers have the extra option to calculate $$V_p$$/$$V_s$$/Rho by **fluid substitution**: Gassmann equation or Castagna coefficients methods; or by **porosity change** curves

![](../../../.gitbook/assets/033_interpretation.PNG)

_A Target layer with in situ Vs calculated using Castagna equation \( This equation uses custom coeffs. so a grey lithology flag is shown \)_

![](../../../.gitbook/assets/034_interpretation.PNG)

_A Target layer with in situ Vs and Rho calculated using sand equations_

In the example above, the greyed out $$V_s$$ and Rho values \(1557 & 2.194\) are those calculated by the Castagna and Gardner equations, from the input $$V_p$$ of 3000m/s. These equations use the coefficients set for the layer, which can be changed using the  box. The user has the choice of selecting Preset default coefficients by lithology \(Sandstone, Shale, Limestone or Dolomite\), or manually inputting their own field/rock specific coefficients, for $$V_s$$ and Rho calculations.

![](../../../.gitbook/assets/035_interpretation.PNG)

**Selecting Castagna and Gardner coefficients**

$$V_p$$/$$V_s$$/Rho values can also be defined by PCube facies or by well log zone, using the ‘Fill Properties’ option. Select a PCube facies, which already has averages calculated, or a log zone and calculate averages from well logs. \(Log zones can be defined by a cascade of filters in the Well Log Viewer\).

In the example below, the Top layer in the 1D model has $$V_p$$/$$V_s$$/Rho values defined by the parent well’s ‘Shale’ zone. Averages are calculated from each of the 3 input logs.

![](../../../.gitbook/assets/036_interpretation.PNG)

$$V_p$$_/_$$V_s$$_/Rho values from well log ‘Zone’ averages_

**1D layer properties – fluid substitution** 

**Reservoir** layers can have their $$V_p$$/$$V_s$$/Rho calculated by **fluid substitution**. In situ values are input into the middle column, and substituted results are automatically output into the right column.

![](../../../.gitbook/assets/037_interpretation.PNG) ![](../../../.gitbook/assets/038_interpretation.PNG)

**Fluid substitution, Gassmann input parameters**

![](../../../.gitbook/assets/039_interpretation.PNG) ![](../../../.gitbook/assets/040_interpretation.PNG)

**Fluid substitution, Castagna input parameters**

**Gassmann** equation fluid substitution of an in situ rock, of a known in situ porosity, or the simpler **Castagna** ‘rule of thumb’ fluid substitution equation, relating the $$V_p$$ of gas and brine sandstone; are the choices available from a drop-down menu. For both methods, the user can substitute hydrocarbons to brine, or brine to hydrocarbons.

![](../../../.gitbook/assets/041_interpretation.PNG)

_Fluid substitution, selection of Brine to HydroC or HydroC to Brine_

The **Gassmann method**

The Gassmann method can be used to replace one fluid by another, usually hydrocarbons with brine, or brine with hydrocarbons. Defaults were chosen to model the biggest change in $$V_p$$/$$V_s$$/Rho; the gas/brine case, but with appropriate before/after fluid parameter choices the effect of oil/brine or gas/oil substitution can also be estimated. This method requires a knowledge of both bulk modulii and densities for the two fluid phases, so that the appropriate delta/change input values can be calculated.

* Requires inputs of rock **InSitu Porosity**, **HydroC-Percentage** \(Hydrocarbon percentage\) and  **K-min** \(mineral bulk modulus\).
* Requires inputs of fluid K: **K-Brine & K-HydroC** \(giving a change of fluid bulk modulus\) and fluid Density: **Rho-Brine & Rho-HydroC** \(giving a change of fluid density\). 
* Requires an **in situ Vp**, **Vs** and **Rho**. 
* Input defaults: 

  for Brine/Gas, and a pure Sandstone reservoir:

  **K-min** \(quartz\) = 38 Gpa, **K-Brine** = 2.60 Gpa and **K-HydroC** = 0.20 Gpa; **Rho-Brine** = 1.05 g/cm^3 and **Rho-HydroC** = 0.10 g/cm^3

**Input parameter usage:**

The **K-min** default is for a pure sandstone case. If the user wants to model a sandstone/shale mix then a lower value of **K-min** could be used. This value could come from some kind of mixing of  **K\(sandstone\)** & **K\(shale\)** such as the **Voight-Reuss-Hill** averaging.

**InSitu Porosity \(**$$\Phi$$**\)** must be a reasonable value for the rock $$V_p$$, $$V_s$$ and Rho or the calculation will return suspect fluid substituted $$V_p$$/$$V_s$$/Rho values, because the rock has to be too stiff or too unconsolidated, given the in situ porosity selected. There is no lower limit cut off applied nor an upper limit of critical porosity \(40% for sand\) inside this release of the 3D Parametric Synthetic model Builder.

**The Castagna method \(gas & brine only\)**

The Castagna method can be used to replace gas with brine, or brine with gas, using the quadratic equation relating $$V_p$$**\(gas\)** to $$V_p$$**\(brine\)** and the coefficients shown below.

![](../../../.gitbook/assets/042_interpretation.PNG)

**The Castagna ‘rule of thumb’ fluid substitution equation**

\(Petrophysical imaging using AVO – The Leading Edge, 3/1993, JP Castagna\)

* This **Castagna equation** method only requires input of an **in situ** $$V_p$$ value from which an equivalent gas or brine $$V_p$$ is calculated.
* If a different quadratic equation has been found to work for gas/brine fluid substitution, or allows oil/brine or gas/oil fluid substitution, in your reservoir, the coefficients can be changed to use this instead.

**Example** - sandstone Brine-to-Gas:

**Gassmann** - all 3 properties change An in situ layer of pure sand \(default case\), with a **porosity** of **20**%, filled with brine, which has the properties: $$V_p$$ **=3000**m/s, $$V_s$$ **= 1500**m/s, **Rho = 2.2** g/cm^3, after gas injection, changes to a layer filled with **20**% gas, **80**% Brine which has the properties: $$V_p$$ =2648m/s, $$V_s$$ = 1513m/s, Rho = 2.162 g/cm^3

**Castagna** - only Vp changes An in situ layer of pure sand, porosity filled with brine, which has the property : $$V_p$$ **=3000**m/s, changes to a layer filled with gas, which has the property : $$V_p$$ =2640m/s,

\( The other layer properties sent back to the main table are : Rho = **2.124** g/cm^3 calculated by the Gardner equation, from $$V_p$$ 2640m/s \) and $$V_s$$ = **1525**m/s, calculated using the Rho above from Gardner and a mu from the original in situ $$V_s$$.

Castagna fluid substitution is much simpler, but is useful for just giving a feel for what happens when you put in a lighter fluid.

Well log crossplots, with useful rock physics curve overlays, can help with in situ porosity selection. In the example below, log points fall below the polygon pure sand minimum because they come from a mix of sand and shale/clay.

![](../../../.gitbook/assets/043_interpretation.PNG)

Cross plot of $$\Phi$$ \(porosity\) v $$V_p$$ , showing a brine sand \(blue\) and a gas sand \(red\) in relation to a polygon defining the **min** and **max** $$V_p$$ for a pure sand. \(The minimum $$V_p$$ is where the rock breaks up and becomes a suspension; the maximum is where the rock is fully cemented and as stiff as it can be\).

**1D layer properties – porosity change** 

**Reservoir** layers can also have their $$V_p$$/$$V_s$$/Rho calculated by **porosity change**. In situ values are input into the middle column, and changed results are automatically output into the right column.

![](../../../.gitbook/assets/044_interpretation.PNG)

_Porosity change, 20% to 25%_

![](../../../.gitbook/assets/045_interpretation.PNG)

_Porosity change, input parameters_

**Inputs:** in situ and target porosity, % of cementation & sorting $$V_p$$ and $$V_s$$ V porosity, upper and lower bound, RPM curves 1. Hashin-Shtrikman critical porosity upper bound \( yellow curve below = cementing trend \) 2. Hashin-Shtrikman, lower bound \( blue curve below = sorting trend \)

![](../../../.gitbook/assets/046_interpretation.PNG)

$$V_p$$ **v Porosity, upper & lower bound curves**

These are the curves for pure sand. They can’t be changed in this first version of the software.

Predicted porosity change, $$\Delta V_p$$ , $$\Delta V_s$$ , comes from a mix of these curves. Eg: the red dashed line = 40% cementation and 60% sorting.

Both curves start from a sand with a little bit of cementation, $$V_p$$, $$V_s$$ initial values calculated using the contact cement model equations.

**Outputs**

* New $$V_p$$ & $$V_s$$  -  calculated from In situ $$V_p$$ & $$V_s$$  +  $$\Delta V_p$$ , $$\Delta V_s$$  from mixed RPM curves,e.g. \(0.4  _cement + 0.6_  sorting curves \)
* New Rho - calculated from In situ Rho + $$\Delta Rho$$ - from a mix of Quartz \(2.65\) and fluid density \(1.07\)eg: \(0.05  _Fluid - 0.05_  Quartz \)  for a change 20% -&gt; 25%

**Example -** sandstone 20%-to-25% porosity change:

An in situ layer of pure sand, with a starting **porosity** of **20**%, filled with brine, which has the properties : $$V_p$$ **=3000**m/s, $$V_s$$ **= 1800**m/s, **Rho = 2.13** g/cm^3, after a porosity change to **25**%, changes to a layer which has the properties : $$V_p$$ =2733m/s, $$V_s$$ = 1566m/s, Rho = 2.051 g/cm^3 \( see red triangles inside the $$V_p$$ v Porosity crossplot \)

**3D Model/gather definition** 

![](../../../.gitbook/assets/047_interpretation.PNG)

Select the $$2^{nd}$$ Tab

In the example below, the inline axis is set to be the target layer hydrocarbon % and crossline, the target layer in situ porosity.

![](../../../.gitbook/assets/048_interpretation.PNG) ![](../../../.gitbook/assets/049_interpretation.PNG)

The Parametric Axes box, on the left hand side, allows the user to choose a property to assign to an axis – the list of properties above includes in situ porosity, Kmin & Hydrocarbon %, only if the layer selected is a reservoir layer.

The Output gather box on the right, gives the offset/angle gather dimensions that will be output into the synthetic model volume.

The user can choose whether to output the $$V_p$$, $$V_s$$ and density 3D stack volumes for Q.C. and also to review the model output size and reduce it’s dimensions if needed. \( 9 x 76 x 1 x 8 x 1001 \)

**Synthetic options:**

![](../../../.gitbook/assets/050_interpretation.PNG)

Select the $$3^{rd}$$ Tab

![](../../../.gitbook/assets/051_interpretation.PNG) This Tab can be used to select a wavelet for all the synthetic gathers; a method for calculating AVO amplitudes and any runtime parameters. It also has a wavelet scaling option and an overburden definition table if required.

**Model save & rerun:**

The last model definition is automatically saved by the application, but as soon as a new model is defined or this ‘active model’ updated it will be overwritten and lost. Therefore, it is really important to save the output model to the project disk as a .m3d file using the save \(red\) ‘V’ icon.

So that it can be restored using the \(blue\) inverted ‘V’ icon later:

![](../../../.gitbook/assets/052_interpretation.PNG)

Any $$V_p$$,$$V_s$$, Rho model logs themselves, can be saved to a project well, once they are displayed in the Model Log Viewer, by Save logs to project.

![](../../../.gitbook/assets/053_interpretation.PNG)

Also, entire $$V_p$$, $$V_s$$ and Rho input 3D volumes can be saved to the project, from the data pool, once the model has been calculated – so long as they have been selected for output as shown below.

![](../../../.gitbook/assets/054_interpretation.PNG)


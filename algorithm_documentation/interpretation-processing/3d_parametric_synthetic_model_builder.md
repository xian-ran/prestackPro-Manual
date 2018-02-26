### 3D Parametric Synthetic Model Builder {#3d-parametric-synthetic-model-builder}

**Introduction :**

![](/assets/113_Processing.PNG)

_3D synthetic gather volume, created from a single initial 1D reference model, showing amplitudes varying with porosity & angle (crossline) and reservoir layer thickness (inline)._

This application allows the user to input anything from a simple 1D $$Vp_,V_s$$ and Rho log model to a complex, multi-axes, multi-layer, property change, “parametric”, $$Vp_,V_s$$ and Rho 3D volume model; from which a single synthetic gather to a whole pre-stack volume can be calculated. It allows 1D single gather, 2D line cross section, 3D and 4D volume synthetic models to be created.  ( 4D = 3D + a $$2^{nd}$$ offset/azimuth axis )

These extra dimensions are used to show “parametric changes” only and cannot be used to model 3D geological structure. They allow the user to make 100’s of synthetic gather models in one execution of the application and store them all together in one pre-stack dataset. 

These synthetic gather datasets give the user quick and effective insights into their reservoir gather character and AVA expression. For example, they can be used to investigate how AVO amplitude changes with the $$Vp_,V_s$$ and density of the reservoir and caprock; with fluid substitution and with bed thickness.

**Model examples **

![](/assets/114_Processing.PNG)

_1D single gather example : $$V_p$$ 3100 synthetic shown in Data Comparator, with an amplitude extraction from top reservoir_

The user in the first example has taken 2 well log crossplots which show the variability of the reservoir ‘brine’ sand:  $$V_p$$ v $$V_s$$  and $$V_p$$ v Density and has decided to make 5 separate 1D single gather synthetics to show how the AVA amplitude varies with $$V_p$$. The 5 $$V_p$$, $$V_s$$ and $$\rho$$ points are shown as red & green circles on the crossplots. The gather display shows the AVA expected with $$V_p$$ = 3100, $$V_s$$ = 1650, $$\rho$$ = 2.16. and with a reservoir layer thickness of 70m.

Instead of running the application 5 times and creating 5 separate individual gathers the user could have made a 2D line of 9 gathers as shown in the 2nd example. $$V_p$$ is set as the inline axis ( 2500 –> 3300 inc 100 ) and the $$V_s$$ and $$\rho$$ modelled using curves defined by custom coefficients and the Castagna and Gardner equations. The grey points on the crossplots are the equivalent 5 modelled points used in this 2D line and indicate a pretty good fit to the red and green original curves from example 1. The reservoir layer thickness is still a constant 70m however.

![](/assets/115_Processing.PNG)

_2D line example : Vp 2500 → 3300 synthetics shown in 2D gather viewer 
( inline = Vp,  Vs and Rho from Vp by custom equations )_


Since layer thickness and tuning is often a major influence on amplitude, example 3 shows how the 2D model from example 2 can be turned into a 3D ‘classic’ wedge model by setting reservoir layer thickness to the crossline axis instead of density. This is done by adding a crossline axis representing thickness from 1 -> 100m with an increment of 1m to the $$V_p$$ inline axis – thereby making a 3D volume of 9 x 100 = 900 gathers!

To study the influence of density on amplitude in detail the $$4^{th}$$ example shows how a user has made a 3D volume of gather synthetics by adding a crossline axis representing Rho from 2.0 -> 2.2 with an increment of 0.002 to the $$V_p$$ inline axis – creating a 3D volume of 9 x 101 = 909 gathers! $$V_s$$ is still calculated using a curve defined by custom coefficients and the Castagna equation. 

Every possible combination of these Rho values with the 9 $$V_p$$ values are included in the gather volume and so most of the $$V_p$$, $$V_s$$ and Rho combinations are now no long following the curves in the original well log crossplots – they will be representing a variety of lithology and fluid content and not just the reservoir ‘brine’ sand we started with. ( 5 of the 101 Rho points are shown in the crossplots to indicate the range of values w.r.t $$V_p$$ and the grid of input density points used in the model ).  

![](/assets/116_Processing.PNG)

_3D volume example : $$V_p$$ 2500 → 3300 synthetics shown in 3D viewer
( inline = $$V_p$$,  xline = thickness, $$V_s$$ & Rho from $$V_p$$ by equations )_


![](/assets/117_Processing.PNG)

_3D volume example : $$V_p$$ 2500 → 3300 synthetics shown in 3D viewer
( inline = $$V_p$$,  xline = Rho, $$V_s$$ from $$V_p$$, by custom equation )_


![](/assets/118_Processing.PNG)

_3D volume example : $$V_p$$ 2900 synthetics shown in 3D viewer
( inline = % gas,  xline = $$\Phi$$,  $$V_p$$, $$V_s$$, Rho from fluid substitution )_


In the final example, a 3D gather volume has been created to explore the effect of fluid substitution on an average or midpoint representing the reservoir. The $$V_p$$ 2900 point is used here and by varying % gas from 0 to 40 inline and in situ porosity from 15 to 30, crossline, a 3D pre-stack model of  9 x 76 = 684 gathers is output. 

All $$V_p$$, $$V_s$$ and density values come from the fluid substitution and the same gassmann parameters are used for all calculations except for % gas and in situ porosity, set by axes.

**Initial 1D Model **

Creates an initial or reference model, a $$V_p$$, $$V_s$$ and density log, from which a 2D line or 3D gather volumes can be created. 

These logs are made from at least 3 user defined layers - Top, Target and Bottom layers, plus any added in-between. 

The **Target layer** has a fixed top depth (MD) and associated time (TWT), which acts as a model reference datum, from which the model is built. All the layers have a thickness to define their top and base relative to this 

Layer properties can be defined as follows:  

* $$V_p$$, $$V_s$$, Rho by manual entry of values, 
* $$V_p$$ by manual entry, $$V_s$$, Rho by Castagna and Gardner equations
* $$V_p$$, $$V_s$$, Rho by well facies or zone, averages
* $$V_p$$, $$V_s$$, Rho by **«Reservoir»** Gassmann fluid substitution
* $$V_p$$, $$V_s$$, Rho by **«Reservoir»** Castagna fluid substitution
* $$V_p$$, $$V_s$$, Rho by **«Reservoir»** Porosity change


Gradual / sloping layer changes can be modelled using the Add intermediate layers option.

This initial or reference model, gives to 2D/3D models :

* -all layer thicknesses; all layer properties; and 
* -all reservoir layer,  fluid substitution parameters, 
(which aren’t replaced later by an axis )
* -all layer ‘In situ’ Vp, Vs and Density.


**3D Model/gather definition :**

All synthetic gathers have an angle or offset ‘X’ dimension to which the user can add an inline and a crossline dimension to create 2D and 3D gather volumes. A $$2_{nd}$$ gather ‘Y’ offset can also be added to make a final model with 3 parametric axes. 

Layer parameters which can be assigned to inline, crossline or $$2_{nd}$$ offset include :  All Layers : thickness,  $$V_p$$, $$V_s$$, Rho, $$V_p$$/$$V_s$$, AI

* Reservoir Layers : In situ Porosity, % hydrocarbon & Kmin.
* Reservoir Layers : Target Porosity.


Only 1 layer & 1 of its parameters can be assigned to any axis. However, any layer can be assigned to any axis. So valid layer and parameter combinations include :

* 2D model :  Inline = Target &  Thickness; 
* 3D model :  Inline = Target &  AI;  Xline = Caprock &  AI;
* 3D model :  Inline = Target &  $$V_p$$;  Xline = Caprock &  $$V_p$$/$$V_s$$;
* 3D model :  Inline = Target &  In situ Porosity; Xline = Target &  % gas;


The model time range is set by adding 300 msec to model Tmin and Tmax and the sample rate is 1 msec; unless changed by the user.

The model inline & crossline numbers, range and inc are set by the axes input parameter ranges. These will not have any project X/Y map coordinates and so any timeslice or map 	extracted from these models 

![](/assets/119_Processing.PNG)

will need to be displayed in a Top View.
This image shows a Top View  -   $$0^o$$ angle of incidence, amplitude time slice, for top reservoir.
Horizontal axis = 0% to 100% gas
Vertical axis = 15% to 25% $$\Phi$$, in situ porosity


**3D Model/gather analysis **

In this example, the amplitude changes from a peak to a trough ( yellow to blue ) when brine is replaced with gas.

![](/assets/120_Processing.PNG)
The polarity reversal location, shown by the zero amplitude white band, occurs with less % gas as porosity decreases, and the rock becomes weaker and more unconsolidated.
Synthetic gathers from the 3D parametric volume are shown in the Data Comparator, below
( Points of interest (POI) 1 – 4 )
![](/assets/121_Processing.PNG)

Looking at the $$V_p$$, $$V_s$$ and density volumes used for the model, we can see how the Gassmann fluid substitution, from brine to gas, has altered the $$V_p$$ much more than the $$V_s$$ or the Density. $$V_s$$ is only slightly affected by the change in density – decreasing density = increasing $$V_s$$.  The gas changes $$V_p$$ very quickly with low porosity, because the constant in situ $$V_p$$ → a softer rock.

![](/assets/122_Processing.PNG)

_Top View  -   $$V_p$$, $$V_s$$ and density timeslices, for top reservoir_

![](/assets/123_Processing.PNG)
$$V_p$$, $$V_s$$ and Density volumes, were output from the modeling, using the create volumes option above.

**1D initial model setup **

To open up the 3D Parametric Synthetic Model Builder dialog go to:

**Interpretation-Processing** → **3D Parametric Synthetic Model…**

![](/assets/124_Processing.PNG)

and select the $$1^{st}$$ Tab.

If any models have been created before in Pre-Stack Pro, it will use the last model’s parameters to open the GUI. So, you may need to delete some layers using the blue – icon rather than adding layers using the green + icon; or start a new model. Gradual / sloping layer changes can be modelled using the green + <Add intermediate layers> option also.

Target, Top and Bottom layers can’t be deleted but are the same as ordinary layers otherwise.

![](/assets/125_Processing.PNG)

**Ordinary layer GUI**

( The black flag indicates this layer is a shale for Vs calc by equation )
First go to the target layer and set its top depth (MD) and corresponding time (TWT). This becomes a fixed depth/time value for the model reference datum. 

![](/assets/126_Processing.PNG)
_Target layer GUI – model reference datum = 1000m/1.0sec
( This layer is selected for fluid substitution )_

Set thicknesses for all the layers, and then decide which layers are reservoir rocks and will need fluid substitution. The target layer above, has fluid substitution enabled by selection of the ‘Reservoir’ option - the right hand ‘Fluid substituted’ $$V_p$$, $$V_s$$ and Rho values are now set as the layer properties

**1D layer properties definition :**

**Ordinary** layers can have their $$V_p$$/$$V_s$$/Rho values entered manually, input from well log zone or PCube facies averages, or calculated by equation.

**Reservoir** layers have the extra option to calculate $$V_p$$/$$V_s$$/Rho by **fluid substitution**: Gassmann equation or Castagna coefficients methods; or by **porosity change** curves

![](/assets/127_Processing.PNG)

_A Target layer with in situ Vs calculated using Castagna equation
( This equation uses custom coeffs. so a grey lithology flag is shown )_


![](/assets/128_Processing.PNG)

_A Target layer with in situ Vs and Rho calculated using sand equations_

In the example above, the greyed out $$V_s$$ and Rho values (1557 & 2.194) are those calculated by the Castagna and Gardner equations, from the input $$V_p$$ of 3000m/s. These equations use the coefficients set for the layer, which can be changed using the <Calc, $$V_s$$/Rho> box. The user has the choice of selecting Preset default coefficients by lithology (Sandstone, Shale, Limestone or Dolomite), or manually inputting their own field/rock specific coefficients, for $$V_s$$ and Rho calculations.

![](/assets/129_Processing.PNG)

**Selecting Castagna and Gardner coefficients**

$$V_p$$/$$V_s$$/Rho values can also be defined by PCube facies or by well log zone, using the ‘Fill Properties’ option. Select a PCube facies, which already has averages calculated, or a log zone and calculate averages from well logs. (Log zones can be defined by a cascade of filters in the Well Log Viewer).

In the example below, the Top layer in the 1D model has $$V_p$$/$$V_s$$/Rho values defined by the parent well’s ‘Shale’ zone. Averages are calculated from each of the 3 input logs.

![](/assets/130_Processing.PNG)

_$$V_p$$/$$V_s$$/Rho values from well log ‘Zone’ averages_

**1D layer properties – fluid substitution **

**Reservoir** layers can have their $$V_p$$/$$V_s$$/Rho calculated by **fluid substitution**. In situ values are input into the middle column, and substituted results are automatically output into the right column. 

![](/assets/131_Processing.PNG)
![](/assets/132_Processing.PNG)

**Fluid substitution, Gassmann input parameters**

![](/assets/133_Processing.PNG)
![](/assets/134_Processing.PNG)

**Fluid substitution, Castagna input parameters**

**Gassmann** equation fluid substitution of an in situ rock, of a known in situ porosity, or the simpler **Castagna** ‘rule of thumb’ fluid substitution equation, relating the $$V_p$$ of gas and brine sandstone; are the choices available from a drop-down menu. For both methods, the user can substitute hydrocarbons to brine, or brine to hydrocarbons. 

![](/assets/135_Processing.PNG)

_Fluid substitution, selection of Brine to HydroC or HydroC to Brine_

The **Gassmann method**

The Gassmann method can be used to replace one fluid by another, usually hydrocarbons with brine, or brine with hydrocarbons. Defaults were chosen to model the biggest change in $$V_p$$/$$V_s$$/Rho; the gas/brine case, but with appropriate before/after fluid parameter choices the effect of oil/brine or gas/oil substitution can also be estimated. This method requires a knowledge of both bulk modulii and densities for the two fluid phases, so that the appropriate delta/change input values can be calculated.

* Requires inputs of rock **InSitu Porosity**, **HydroC-Percentage** (Hydrocarbon percentage) and  **K-min** (mineral bulk modulus).
* Requires inputs of fluid K: **K-Brine & K-HydroC** (giving a change of fluid bulk modulus) and fluid Density: **Rho-Brine & Rho-HydroC** (giving a change of fluid density). 
* Requires an **in situ Vp**, **Vs** and **Rho**. 
* Input defaults: 
for Brine/Gas, and a pure Sandstone reservoir:
**K-min** (quartz) = 38 Gpa, **K-Brine** = 2.60 Gpa and **K-HydroC** = 0.20 Gpa; **Rho-Brine** = 1.05 g/cm^3 and **Rho-HydroC** = 0.10 g/cm^3

**Input parameter usage:** 

The **K-min** default is for a pure sandstone case. If the user wants to model a sandstone/shale mix then a lower value of K-min could be used. This value could come from some kind of mixing of  K(sandstone) &  K(shale)  such as the Voight-Reuss-Hill averaging.    

**InSitu Porosity ()** must be a reasonable value for the rock Vp, Vs and Rho or the calculation will return suspect fluid substituted Vp/Vs/Rho values, because the rock has to be too stiff or too unconsolidated, given the in situ porosity selected. There is no lower limit cut off applied nor an upper limit of critical porosity (40% for sand) inside this release of the 3D Parametric Synthetic model Builder.

The **Castagna method** (gas &amp; brine only)

The Castagna method can be used to replace gas with brine, or brine with gas, using the quadratic equation relating **Vp<sub>(gas)</sub>** to **Vp<sub>(brine)</sub>** and the coefficients shown below.

![](/assets/cusersjohanndesktopsharp-stuff.png)

_The Castagna ‘rule of thumb’ fluid substitution equation_

_(Petrophysical imaging using AVO – The Leading Edge, 3/1993, JP Castagna)_

*   This **Castagna equation** method only requires input of an **in situ Vp** value from which an equivalent gas or brine Vp is calculated.
*   If a different quadratic equation has been found to work for gas/brine fluid substitution, or allows oil/brine or gas/oil fluid substitution, in your reservoir, the coefficients can be changed to use this instead.

**Example -** sandstone Brine-to-Gas:

**Gassmann -** all 3 properties change

An in situ layer of pure sand (default case), with a **porosity** of **20**%, filled with brine, which has the properties :

**Vp =3000**m/s**, Vs = 1500**m/s**, Rho = 2.2** g/cm^3, after gas injection, changes to a layer filled with **20**% gas, **80**% Brine which has the properties :

**Vp =2648**m/s**, Vs = 1513**m/s**, Rho = 2.162** g/cm^3

**Castagna** - only Vp changes

An in situ layer of pure sand, porosity filled with brine, which has the property :

**Vp =3000**m/s, changes to a layer filled with gas, which has the property :

**Vp =2640**m/s,

( The other layer properties sent back to the main table are :

Rho = **2.124** g/cm^3 calculated by the Gardner equation, from Vp 2640m/s ) and

Vs = **1525**m/s, calculated using the Rho above from Gardner and a mu from the original in situ Vs.

Castagna fluid substitution is much simpler, but is useful for just giving a feel for what happens when you put in a lighter fluid.

Well log crossplots, with useful rock physics curve overlays, can help with in situ porosity selection. In the example below, log points fall below the polygon pure sand minimum because they come from a mix of sand and shale/clay.

![](/assets/vp-v-porosity-sst-limits2a.png)

_Cross plot of (porosity) v_ **_Vp_** _, showing a brine sand (blue) and a gas sand (red) in relation to a polygon defining the_ **_min_** _and_ **_max Vp_** _for a pure sand. (The minimum Vp is where the rock breaks up and becomes a suspension; the maximum is where the rock is fully cemented and as stiff as it can be)._

**1D layer properties – porosity change :**

**Reservoir** layers can also have their Vp/Vs/Rho calculated by **porosity change**. In situ values are input into the middle column, and changed results are automatically output into the right column.

![](/assets/cusersjohannappdatalocalmicro.png)

_Porosity change, 20% to 25%_

![](/assets/3d-param-por1b.png)

_Porosity change, input parameters_

**Inputs** : in situ and target porosity, % of cementation &amp; sorting

: Vp and Vs V porosity, upper and lower bound, RPM curves

1.  Hashin-Shtrikman  critical porosity upper bound ( yellow curve below = cementing trend )
2.  Hashin-Shtrikman, lower bound  ( blue curve below = sorting trend ) 

| ![](/assets/3d-param-por2.png) |
| --- |

_Vp v Porosity, upper &amp; lower bound curves_

These are the curves for pure sand. They can’t be changed in this first version of the software.

Predicted porosity change, ∆Vp , ∆Vs , comes from a mix of these curves. Eg: the red dashed line = 40% cementation and 60% sorting.

Both curves start from a sand with a little bit of cementation, Vp, Vs initial values calculated using the contact cement model equations.

**Outputs**: New Vp &amp; Vs - calculated from In situ Vp &amp; Vs + ∆Vp , ∆Vs

- from mixed RPM curves

eg: (0.4 * cement + 0.6 * sorting curves )

: New Rho - calculated from In situ Rho + ∆Rho - from a mix of Quartz (2.65) and fluid density (1.07)

eg: (0.05 * Fluid - 0.05 * Quartz ) for a change 20% -&gt; 25%

**Example -** sandstone 20%-to-25% porosity change:

An in situ layer of pure sand, with a starting **porosity** of **20**%, filled with brine, which has the properties :

**Vp =3000**m/s**, Vs = 1800**m/s**, Rho = 2.13** g/cm^3, after a porosity change to **25**%, changes to a layer which has the properties :

**Vp =2733**m/s**, Vs = 1566**m/s**, Rho = 2.051** g/cm^3

( see red triangles inside the Vp v Porosity crossplot )

**3D Model/gather definition :**

![](/assets/cusersjohannappdatalocalmicro.png)

Select the 2<sup>nd</sup> Tab

In the example below, the inline axis is set to be the target layer hydrocarbon % and crossline, the target layer in situ porosity.

| **![](/assets/cusersjohannappdatalocalmicro.png)** | The Parametric Axes box, on the left hand side, allows the user to choose a property to assign to an axis – the list of properties above includes in situ porosity, Kmin &amp; Hydrocarbon %, only if the layer selected is a reservoir layer. |
| --- | --- |

The Output gather box on the right, gives the offset/angle gather dimensions that will be output into the synthetic model volume.

The user can choose whether to output the Vp, Vs and density 3D stack volumes for Q.C. and also to review the model output size and reduce it’s dimensions if needed. ( 9 x 76 x 1 x 8 x 1001 )

**Synthetic options :**

![](/assets/cusersjohannappdatalocalmicro.png)

Select the 3<sup>rd</sup> Tab

| ![](/assets/cusersjohannappdatalocalmicro.png) | This Tab can be used to select a wavelet for all the synthetic gathers; a method for calculating AVO amplitudes and any runtime parameters. |
| --- | --- |

**Model save &amp; rerun:**

The last model definition is automatically saved by the application, but as soon as a new model is defined or this ‘active model’ updated it will be overwritten and lost. Therefore it is really important to save the output model to the project disk as a **.m3d** file using the save (red) ‘V’ icon.

So that it can be restored using the (blue) inverted ‘V’ icon later:

![](/assets/1d11c.png)

Any Vp,Vs, Rho model logs themselves, can be saved to a project well, once they are displayed in the Model Log Viewer, by &lt;Save logs to project&gt;.

![](/assets/cusersjohannappdatalocalmicro.png)

Also entire Vp, Vs and Rho input 3D volumes can be saved to the project, from the data pool, once the model has been calculated – so long as they have been selected for output as shown below.

![](/assets/cusersjohannappdatalocalmicro.png)
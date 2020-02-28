# CRAVA Background Model

## Introduction

Since seismic data only contain information about relative elastic parameters, the absolute level needs to be set with a background model. In a Bayesian inversion setting, the background model is the prior expectation. Input data to the background model is elastic well log \( vp, Vs and density\)  and surfaces. The surfaces guide the well log values between the wells.

##    Well data input in Crava background Model Builder

Well data are selected by the user. Pre-defined logset or individual well logs can be used. 

![](../../../.gitbook/assets/image%20%2811%29.png)

If many versions of the well log exist a drop down menu is activated  when "clicking" on the box

![](../../../.gitbook/assets/image%20%2819%29.png)

## Zone definition

The  well log values are interpolated/extrapolated using surfaces. The twt interval between two surfaces defines a zone. The model will be generated from the Top surface/fixed time down to the base surface/fixed time It is recommended to use "match to volume"  using the inversion seismic volume to get the right inline/xline range.

![](../../../.gitbook/assets/image%20%2818%29.png)

The **Hierarchy** defines which horizon to use if they intersect.  All the surfaces need to be given a unique Hierarchy number. The surface with highest number is given erosion priority one, while the surface with lowest priority is given priority n, where n is equal to the number of surfaces.

Horizon can be shifted  \(upwards -, downwards +\) by using the **offset**

The full multizone background model is then made by joining the local background models in all the zones. To represent the uncertainty in the interfaces between the zones, a Beta distribution with parameters = = 2 is used. The distribution is symmetric around its center, being the surface between the zones. The limit in the Beta distribution is given by the **Uncertainty** , being the distance of the uncertainty in ms in each direction from the surface. The surface uncertainty must be zero for the top surface and the last base surface.

**Correlation structure** is used to guide the well log values between the horizons. Five different Correlation structures exist: " _Top conform, Base Conform, Top and Base Conform, Guide by one horizon, Guide by two horizons_".  Choose the one most similar to the geological structure in the zone.

![](../../../.gitbook/assets/image%20%2845%29.png)

## Parameter and Trends

The **filter type** used to create the low-frequency background model can be set to :  _Boxcar_ or _Butterworth_ or _None_. If _None_ is selected a model with all information from the well log will be created. The _boxcar_ and _Butterworth_ filter require  **High cut frequency/Order**. High cut allows specification of a maximum frequency for the background model.

**Lateral correlation background** are used to set a lateral kriging trend using a 2D variogram. Larger ranges extends the influence of well data further away from wells. 

**Set Expert Parameters** the user can set the min/max /variance of the elastic parameters.

The **Background trends** \(or depth trends\) from the elastic well logs  can be calculated and used in the background model. They are calculated for each zone and can be visualized for each zone or for the entire model. The trend is calculated using a pseudo time reference and can not be compared with the real time in the time calibrated well logs. If the user wants to compare the well logs and background trend in real twt then Save the Background trend in _Output setup tab._

![](../../../.gitbook/assets/image%20%2816%29.png)

The small icon down to the left corner are used to save or load the Background Model Builder session.

![](../../../.gitbook/assets/image%20%2815%29.png)

## Output setup

Choose the elastic background models to generate and save. It is also possible to save the _background trend_ and make a _copy of the log file_.

![](../../../.gitbook/assets/image%20%2853%29.png)


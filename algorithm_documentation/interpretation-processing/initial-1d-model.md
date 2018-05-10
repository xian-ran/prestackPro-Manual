#### Initial 1D Model

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



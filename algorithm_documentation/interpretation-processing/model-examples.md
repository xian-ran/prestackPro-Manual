#### Model examples 

![](/assets/020_Interpretation.PNG)

_1D single gather example : $$V_p$$ 3100 synthetic shown in Data Comparator, with an amplitude extraction from top reservoir_

The user in the first example has taken 2 well log crossplots which show the variability of the reservoir ‘brine’ sand:  $$V_p$$ v $$V_s$$  and $$V_p$$ v Density and has decided to make 5 separate 1D single gather synthetics to show how the AVA amplitude varies with $$V_p$$. The 5 $$V_p$$, $$V_s$$ and $$\rho$$ points are shown as red & green circles on the crossplots. The gather display shows the AVA expected with $$V_p$$ = 3100, $$V_s$$ = 1650, $$\rho$$ = 2.16. and with a reservoir layer thickness of 70m.

Instead of running the application 5 times and creating 5 separate individual gathers the user could have made a 2D line of 9 gathers as shown in the 2nd example. $$V_p$$ is set as the inline axis ( 2500 –> 3300 inc 100 ) and the $$V_s$$ and $$\rho$$ modelled using curves defined by custom coefficients and the Castagna and Gardner equations. The grey points on the crossplots are the equivalent 5 modelled points used in this 2D line and indicate a pretty good fit to the red and green original curves from example 1. The reservoir layer thickness is still a constant 70m however.

![](/assets/021_Interpretation.PNG)

_2D line example : Vp 2500 → 3300 synthetics shown in 2D gather viewer 
( inline = Vp,  Vs and Rho from Vp by custom equations )_


Since layer thickness and tuning is often a major influence on amplitude, example 3 shows how the 2D model from example 2 can be turned into a 3D ‘classic’ wedge model by setting reservoir layer thickness to the crossline axis instead of density. This is done by adding a crossline axis representing thickness from 1 -> 100m with an increment of 1m to the $$V_p$$ inline axis – thereby making a 3D volume of 9 x 100 = 900 gathers!

To study the influence of density on amplitude in detail the $$4^{th}$$ example shows how a user has made a 3D volume of gather synthetics by adding a crossline axis representing Rho from 2.0 -> 2.2 with an increment of 0.002 to the $$V_p$$ inline axis – creating a 3D volume of 9 x 101 = 909 gathers! $$V_s$$ is still calculated using a curve defined by custom coefficients and the Castagna equation. 

Every possible combination of these Rho values with the 9 $$V_p$$ values are included in the gather volume and so most of the $$V_p$$, $$V_s$$ and Rho combinations are now no long following the curves in the original well log crossplots – they will be representing a variety of lithology and fluid content and not just the reservoir ‘brine’ sand we started with. ( 5 of the 101 Rho points are shown in the crossplots to indicate the range of values w.r.t $$V_p$$ and the grid of input density points used in the model ).  

![](/assets/022_Interpretation.PNG)

_3D volume example : $$V_p$$ 2500 → 3300 synthetics shown in 3D viewer
( inline = $$V_p$$,  xline = thickness, $$V_s$$ & Rho from $$V_p$$ by equations )_


![](/assets/023_Interpretation.PNG)

_3D volume example : $$V_p$$ 2500 → 3300 synthetics shown in 3D viewer
( inline = $$V_p$$,  xline = Rho, $$V_s$$ from $$V_p$$, by custom equation )_


![](/assets/024_Interpretation.PNG)

_3D volume example : $$V_p$$ 2900 synthetics shown in 3D viewer
( inline = % gas,  xline = $$\Phi$$,  $$V_p$$, $$V_s$$, Rho from fluid substitution )_


In the final example, a 3D gather volume has been created to explore the effect of fluid substitution on an average or midpoint representing the reservoir. The $$V_p$$ 2900 point is used here and by varying % gas from 0 to 40 inline and in situ porosity from 15 to 30, crossline, a 3D pre-stack model of  9 x 76 = 684 gathers is output. 

All $$V_p$$, $$V_s$$ and density values come from the fluid substitution and the same gassmann parameters are used for all calculations except for % gas and in situ porosity, set by axes.



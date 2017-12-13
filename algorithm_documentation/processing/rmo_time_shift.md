### RMO (Time Shift) {#rmo-time-shift}

This algorithm converts time shift fields computed by trimstatics methods like &quot;Align&quot; or &quot;Semblance Optimisation&quot; into updates for vrms and eta.

The process is based on the Alkhalifah moveout equation,

,

for higher order moveout the difference t due to changes of velocity v and of eta  can be formulated as follows:

To improve the conditioning dimensionless offset , and also dimensionless velocities are introduced

v and  are then computed by minimizing the misfit between the imported and the calculated time shifts t. An iterative linear solver is used for which the user can specify the number of internal iterations and the number of external iterations which are the iterations for which new time shifts are computed.

Further, the user can limit the maximum acceptable velocity and eta perturbation.

For **Stencil mode** (stencil lengths larger than 0) time shifts of the central gather and its neighbouring gathers (according to lengths) are used in the previous equation with indexed ti, again for the purpose of getting smaller lateral fluctuations of the results.
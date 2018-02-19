### RMO (Time Shift) {#rmo-time-shift}

This algorithm converts time shift fields computed by trim statics methods like "Align" or "Semblance Optimization" into updates for vrms and eta.

The process is based on the Alkhalifah moveout equation,



$$
t^2 = t_0^2+\frac{x^2}{V^2}-\frac{2\eta x^4}{V^2(V^2t_0^2+(1+2\eta)x^2)},
$$



for higher order moveout the difference $$\delta t$$ due to changes of velocity $$\delta V$$ and of eta $$\delta \eta$$ can be formulated as follows:



$$
(t+\delta t)^2-t^2 = x^2\lgroup \frac{1}{(V+\delta V)^2}- \frac{1}{V^2} \rgroup - [\frac{2(\eta + \delta \eta)x^4}{(V+\delta V)^2\lgroup ([V+\delta V)]^2t_0^2+(1+2(\eta + \delta \eta))x^2\rgroup}-\frac{2\eta x^2}{V^2(V^2t_0^2+(1+2\eta)x^2)}]
$$



To improve the conditioning dimensionless offset $$\xi = \frac{x}{Vt_0}$$ , and also dimensionless velocities  $$\delta = \frac{\delta V}{V}$$  are introduced


$$
\lgroup \frac{2t}{t_0}+\frac{\delta t}{t_0} \rgroup \frac{\delta t}{t_0} = \frac{-(2+\Delta )\Delta}{(1+\Delta)^2}\xi ^2-2\xi ^4[\frac{\eta + \delta \eta}{(1+\Delta)^2\lgroup (1+\Delta)^2+(1+2(\eta + \delta \eta))\xi ^2 \rgroup}-\frac{\eta}{(1+(1+2\eta)\xi ^2)}]
$$



$$\delta V$$ and $$\delta \eta$$ are then computed by minimizing the misfit between the imported and the calculated time shifts $$\delta t$$. An iterative linear solver is used for which the user can specify the number of internal iterations and the number of external iterations which are the iterations for which new time shifts are computed.

Further, the user can limit the maximum acceptable velocity and eta perturbation.

For **Stencil mode** (stencil lengths larger than 0) time shifts of the central gather and its neighbouring gathers (according to lengths) are used in the previous equation with indexed $$\delta t_i$$, again for the purpose of getting smaller lateral fluctuations of the results. 
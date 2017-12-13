### Numerical scheme {#numerical-scheme}

The edge- and coherency-enhancing anisotropic diffusion model has been discretized by using staggered finite differences on a regular grid. In order to resolve fine structures, approximations with high locality are used. The spatial discretisation can be influenced by the so-called dissipativity parameter . Its admissible range is [0;0.75]. Choosing yields a scheme with extremely low dissipation, and a high directional accuracy resulting in a good approximation of rotationally invariant behavior. Low values for are not recommended due to the possible occurrence of dissipative artifacts.

An explicit time stepping scheme is implemented. For stability a maximum timestep can not be exceeded.
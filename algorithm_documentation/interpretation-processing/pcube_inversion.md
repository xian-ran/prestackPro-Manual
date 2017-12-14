### PCube Inversion {#pcube-inversion}

PCube is an elastic inversion, based on the work of Buland and Omre \(Geophysics, 2008\). It is a two-stage process. In the first, angle stacks are inverted deterministically to give elastic properties. In the second stage, the elastic properties are subjected to a Bayesian classification to supply probability cubes for different litho-facies. However, the Pre-Stack Pro user sees both stages together as a single process. As with most pre-stack inversions, a prior model and wavelets are also required.

Since the algorithm uses the Aki & Richards approximation, angle stacks should not use data above about $$35^o$$ incidence angle. The optimum number of stacks is unclear. Generally, 3-7 stacks are used, but larger numbers may be used if desired.

The prior model must be built before running PCube. See section 6.6.3 for the details.

To run PCube, the angle stacks must first be loaded in the volume pool. All of them must have the same geometry. It is optional to load the prior model cubes into the volume pool. If they are not loaded, the PCube module will read them from disc.

![](/assets/070_Interpretation.png)

Select each angle stack in turn from the drop-down list, and click Add AngleStack. There are parameters which must be set for each of the angle stacks once they are loaded in PCube.

The Angle is usually defined from the data, but it may be over-ridden here. The signal-to-noise ratio \(S/N\) may be determined from well-ties or directly from the data. If the wavelet extraction was performed using Roy White’s method, then S/N can be obtained from the PEP by S/N = PEP / \( 1 – PEP \). S/N is used as a data weighting factor in the inversion. The wavelet peak frequency is not used at present. The wavelet scaling factors may be used to apply angle-dependent scaling to the data, but if the wavelets have been extracted from the angle stacks by well-tie then scale factors are normally built in to the wavelets, and are not required here. Finally, a wavelet must be supplied for each angle stack. This could be different ones for each angle, or the same wavelet could be used for all of them. PCube does not accept time-variant or space-variant wavelets. Section 6.5 describes how to import wavelets into the project. There is no well-tie within Pre-Stack Pro, so wavelets must be imported.

![](/assets/071_Interpretation.png)

The time range for the inversion is also set here. It is possible to use a constant start time or to start relative to a horizon. In the latter case, they can be shifted using the Offset box. A negative offset time starts before the horizon, a positive time starts later. The inversion time window is a constant length. Note that the run time is very sensitive to this parameter.

![](/assets/072_Interpretation.png)

_The prior model volumes are loaded in the Facies prior probabilities tab. _

If they are already in the volume pool, they will appear in the drop-down list. Select the volume for each facies in turn and click Add Probability Cube to bring it into the table. If the cubes do not appear in the drop-down list, check that their geometry matches that of the angle stacks.

![](/assets/073_Interpretation.png)

If the prior model has not been loaded in the volume pool, Click on the green Load from Disc icon. This brings up a data selection window which matches the geometry to that of the angle stacks. After clicking the Select button in this window, the prior model cube is loaded into the volume pool. It must be selected from the drop-down list and added to the table with Add Probability Cube. The loading process must be repeated for each of the prior facies cubes. The option to Load All Siblings does not load the disc files.

![](/assets/074_Interpretation.png)

The Unknown Facies probability is a threshold. It catches data points lying relatively far away from the expected values of elastic properties for each facies. Normally the default value is adequate.

![](/assets/075_Interpretation.png)

The Model time correlation affects vertical smoothness in the results. Larger values produce noisier looking results, and may increase the dynamic range seen in the elastic properties output from the inversion.

The name prefix is attached to all volumes from a PCube run.

Optional outputs may be selected. One is the elastic properties, $$V_p$$, $$V_s$$, and $$\rho$$, for the prior model and resulting from the first stage inversion. The other is the synthetics from the prior model, resulting from the first stage elastic inversion, and resulting from the facies classification \(using the most likely model\). Each synthetic volume has the form of angle gathers with fold equal to the number of input angle stacks.

The second stage of the inversion has a stochastic element. A random number generator is used, and its starting point \(the seed\) is normally calculated by the program. This means that running PCube twice with identical inputs may not produce identical outputs \(although they should be close\). This behaviour can be modified by using a fixed seed, specified by the user, and runs with the same inputs and the same fixed seed should produce identical results.

Once all of these parameters have been set, the Calculate button runs PCube. Results in the volume pool are a probability volume for each facies, the probability cube for the undefined class, and optionally the elastic property cubes and the synthetics.

![](/assets/076_Interpretation.png)

After running PCube, the results may be analyzed in various ways. Some possibilities include creating other elastic property cubes such as P wave impedance or $$V_p$$/$$V_s$$ from the volume calculator, and looking at data residuals by subtracting the synthetics from the original angle stacks. It may also be helpful to calculate posterior probability minus prior probability cubes for some of the litho-facies. This shows where the data are driving the inversion significantly away from the prior model, thus helping to give confidence in the results. It is also possible to combine the probability volumes into a most likely volume using the Combine Volumes utility. 


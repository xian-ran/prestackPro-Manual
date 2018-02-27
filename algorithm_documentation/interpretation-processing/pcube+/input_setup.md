#### Input Setup {#input-setup}

In the **Input Setup** tab, the seismic data and litho-facies to be used in the inversion are specified.

![](/assets/078_Interpretation.png)

_Graphical user interface for the Input Data tab_

**Seismic data**

The input seismic volume to Pcube+ is a set of angle stacks. They can not be loaded into Pcube+ as separate angle stack. A pseudo pre-stack volume containing these angle stack must instead be created; see section 6.5.3or 8.1  for details on how to generate pseudo pre-stack volumes. The pseudo pre-stack volume must be loaded from the volume pool into Pcube+. Since the algorithm uses the Aki & Richards approximation, the angle stacks should not use data above a $$35^o$$ incidence angle. The optimum number of stacks in unclear. Generally, 3-7 stacks are recommended, but larger numbers may be used if desired. After the angle stacks have been loaded, they appear in a table in the Input Setup tab with the corresponding angle defined.

For each angle stack, a wavelet must be loaded from the project. The wavelets can be unique for each angle stack, or one wavelet can be used for all the stacks. Pcube+ does not accept time-variant or space-variant wavelets. The wavelets must have their first sample before time zero and their last sample after time zero. If necessary, the wavelets can be edited in the wavelet tool; see 0for further details.

Peak frequency, signal-to-noise ratio and scaling factor for the wavelet must also be specified for each angle stack. The signal-to-noise ratio \(S/N\) may be determined from well-ties or directly from the data. If the wavelet extraction was performed using Roy White’s method, then S/N can be obtained from the PEP by S/N = PEP/\(1-PEP\). S/N is used as a data weighting factor in the inversion.

The wavelet scaling factors may be used to apply angle-dependent scaling to the data. However, if the wavelets have been extracted from the angle stacks by well-tie, then scale factors are normally built into the wavelets. Therefore, it wouldn’t be necessary to change them here.

**Facies**

A set of litho-facies must be selected for the given Pcube+ model. Each litho-facies is intended to correspond to a distinct litho-class in a $$V_p$$-$$V_s$$-rho cross plot. Typically, they come from wells in the inversion area.

The well logs should be QC’d and preconditioned carefully. The elastic properties in the zones of interest should be cross-plotted. This allows identification of distinct classes. The litho-facies can be defined from well log data in PreStack-Pro by using the well log and cross-plotting tools, or by external import. For external import each litho-facies must be defined separately in an ASCII file by three columns, $$V_p$$ \(m/s\), $$V_s$$ \(m/s\) and density \(g/cm^3\) and no file header.

![](/assets/079_Interpretation.png)

_List of litho-facies in the Facies Manager_

The litho-facies are stored in Pre-Stack Pro’s Facies Manager. By clicking on **Select Facies** in the Input Setup tab, a list of all litho-facies in the Pre-Stack Pro project appears. The toggled on litho-facies will be included in the Pcube+ model. Clicking on **Manage Facies** will open the facies manager for import of new litho-facies or editing of existing litho-facies.

For each litho-facies in the list of selected facies, an id number is defined in parenthesis. This number identifies the selected litho-facies in the prior and post probability cubes. 

The **Model time correlation** parameter affects vertical smoothness in the inversion results. Larger values produce noisier looking results and may increase the dynamic range seen in the elastic properties output from the inversion.


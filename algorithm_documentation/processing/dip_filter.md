### Dip Filter {#dip-filter}

The 3D dip filter algorithm is designed for pre-stack, pseudo pre-stack, or post stack data. It will attenuate dipping noise in the inline and crossline direction, along common offset or angle classes; or on partial or full stacks.

There is a tradeoff between spatial resolution and frequency resolution. Thus, the user can specify a sub-section size over which to apply the filter, and the amount of overlap between consecutive applications (to alleviate edge effects).

To open up the dip filter dialog go to:

**Processing** → **Dip Filter**

![](/assets/cusersvalentinappdatalocaltem.png)

Dip Filter

The user can choose to output the dipping noise model or the filtered data.

**Parameters:**

The dip range parameters define the minimum and maximum dips that will be removed from the input. The units are in ms/m. So, for example, on a 12.5 x 12.5 m² grid, a 0.4 ms/m dip will represent 1 second for every 200 inlines or crosslines.

![](/assets/cusersvalentinappdatalocaltem.png)

Dip Filter Parameters

In the usage case above, we remove dips either side of the origin. So all our primary signal is in the difference, whilst the steeply dipping noise is in the main output.

The taper can be switched on between the minimum and maximum dips. This is a squared cosine &quot;ramp&quot;, which will give a very smooth transition from data to no data. The percentage represents how much of the filtered pyramid is tapered.

A graphical widget in the previews can be used to define the dips to remove, which are within the blue zone between the two axis.

![](/assets/cusersvalentinappdatalocaltem.png)

Graphical widget to define the dip parameters.

The section size defines the dimensions of the calculation window. By default the overlap window cannot be more than half the section size for each axis. An overlap of at least 20 percent of the section size is recommended to avoid processing artefacts.
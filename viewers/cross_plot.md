## Cross Plot {#cross-plot}

This module creates scatter **cross plots** if the number of points is below a certain threshold (default: 5000).

For performance reasons, if there too many data points in a point cloud, Pre-Stack Pro will create a density plot instead. Pre-Stack Pro will The threshold, scatter point size and a default swap to scatter plots, can be set using the Settings Menu. 10000 points is the maximum number allowed.

![](/assets/xplots-36-6.png)

- ![](/assets/001_crossplot.png): Interactive swapping between density and scatter plots can be done using the **scatter plot** icon
- ![](/assets/002_crossplot.png): and between single and histogram colour display using the **single colour / dataset** icon.
- ![](/assets/003_crossplot.png): Focusing the plot for the visible data range, is possible using the **Recalculate plot** icon. It is also possible to select the option to auto-recalculate the plots for visible range.


Any two volumes of the same dimension can now be used to create a cross plot. Eg: prestack gather volumes from different processing steps, intercept and gradient stacks, Map attribute volumes, 2 timeshift volumes, 2 PCube inversion output volumes.

The fastest way to do this is to select the two volumes in the volume pool and create the cross plot via the context menu entry (click in any empty area). Alternatively, two volumes can be added to cross plots after opening the module using:

**Interpretation Processing** → **Cross Plot**

A 3<sup>rd</sup> volume can be selected to color the data points in the cross plot display, when in scatter plot and histogram coloring mode.

Eg: PCube output volumes, Vp, Vp/Vs and density can be input to the cross plot, with Vp as X, Vp/Vs as Y and the density coloring the points.

However, the number of points in the cross plot must be &lt; threshold (see above) for the scatter plot mode to work.

This can be achieved by creating subset or sculpted volumes for input or by zooming the display to restrict the number of points being viewed.

Cross plot will allow PCube LFC classes to be cross-plotted; on their own or with PCube output volumes. They may also be cross-plotted with seismic amplitude datasets, if AVA attributes such as reflection coefficients or Intercept and Gradient are chosen.

The user has a choice of running simulations to produce point clouds for each selected LFC or replacing these simulations with imported real Vp/Vs/Rho values if available.

Scatter plots, density plots, and LFC plots may be mixed in a single display.

Attribute values for individual points may be displayed by hovering the mouse over the scatter display.

![](/assets/jk36manual_-v3.png)

_LFC, density plot : cursor readout LFC, scatter plot : cursor readout
_
![](/assets/004_crossplot.png)
_
PCube LFC facies classes &amp; volumes shown together in a scatter cross plot, of Vp v Vp/Vs with point colours from the 3<sup>rd</sup> density attribute. (Imported ASCII file LFC values are shown instead of simulated clouds)._

### Creation &amp; Display of cross plot datasets :

Cross plots will work with every point or sample in the input datasets, unless a polygon is selected when importing, to define a subset.

![](/assets/005_crossplot.PNG)

_Add plot - Select a polygon_

These can be drawn on a structure map or an attribute in Map Viewer, to restrict the “area of interest” of any cross plot dataset. They can also be drawn on a single gather, in the Gather Viewer, to restrict the time/depth and offset ranges of a prestack gather cross plot dataset.

Selecting ‘Show details’ adds graphs showing advanced parameters’ shows data distributions for the two dataset volumes, and permits customized bin size selection.

![](/assets/006_crossplot.png)

_Add plot – Show details graphs - Advanced Parameters Menu_

This details display allows the user to change X and Y axis ranges using one of the following options:

Average +/- 3 std dev (the default) , Min/Max or to a Manual range.

Another way to limit the inline, crossline range of gathers and the inline, crossline and time/depth range of stacks, in cross plot datasets, is to use Create SubVolume. Further focusing around key horizons can also be achieved using Pre-Stack Pro flattening and sculpting options to create new input volumes.

Multiple cross-plots from other volume pairs can be added to a single plot view, and each can be turned on or off using the show/hide icon.

Two options are available to control cross plot colour:

1.  Each plot may be displayed with a **single user-specified colour**. Where data to be cross plotted have been subsampled inside a polygon, the polygon colour is used by default on the cross plot. Density highs and lows are highlighted by artificial illumination, using sun shading (from the NW corner).

2.  Cross plots may also be coloured using the **histogram**. One freely configurable transfer function, may be assigned per plot. Transparency is fully supported with this option.

![](/assets/007_crossplot.PNG)

_Gathers before and after AGC scaling and corresponding crossplot_
_
![](/assets/008_crossplot.PNG)
_Single colour V Full colour density display_

Cross plot displays default to show the density of points within **3 standard deviations** of the dataset mean. To see more of the data, use the mouse wheel to zoom out and click on the “recalculate all cross plots to the visible data range” icon, accepting the manual defaults. This will redraw the cross plot.

![](/assets/009_crossplot.png)

From drop down menu either select “Recalculate all cross plots for the currently visible data range” icon, accepting the manual defaults, to redraw the cross plot, or select “Auto-recalculate plots for visible range”. 

If you want to see all the data points, set the X and Y axis ranges to **min/max** using **Edit all**; in the cross plot menu, and redraw the cross plot points as described above.

If requested, increase the **bin size** for the density calculation to reduce the number of bins to &lt; 4000.

![](/assets/010_crossplot.png)

_Edit all with bin size message_

When cross-plotting very small datasets, the display may need larger X and Y **bin sizes**, to enable point density highs and lows to be seen, especially when colouring by histogram.

With the single colour display, you may need to set the “Hide densities below” setting to its lowest value of **0.10** to see all the data and set **20%** transparency to see overlaps.

![](/assets/011_crossplot.PNG)
_Single colour V Full colour density plot display_

Alternatively swap to scatter plot display, using the “scatter plot” and recalculate visible data icons, accepting the manual defaults, to redraw the cross plot. 

![](/assets/012_crossplot.PNG)

_Single colour - scatter plot display_

### Creation &amp; Display of PCube LFC cross plot datasets :

Cross plot will allow PCube LFC classes to be cross-plotted; on their own or with PCube output volumes.

![](/assets/013_crossplot.png)

LFC datasets can be added to the crossplot using the **Add/Edit Facies** option in the Cross Plot window.
The user has a choice of running simulations to prod uce point clouds for each selected LFC or replacing these simulation with imported real Vp/Vs/Rho values if available.

![](/assets/014_crossplot.png)
_Add/Edit Facies – Select Facies Input GUI_

LFC classes may also be cross-plotted with seismic amplitude datasets, if AVA attributes such as reflection coefficients or Intercept and Gradient are chosen. There are 15 properties/attributes to choose from.

![](/assets/015_crossplot.PNG)
_Add/Edit Facies – Axis select,  15 properties available _

![](/assets/016_crossplot.PNG)
_PCube  LFC classes  –  simulated clouds  V  imported ASCII points (red cloud/points are from PCube inversion output volumes)_

#### Cross Plot window - basics and icons

![](/assets/slide1.png)

![](/assets/017_crossplot.PNG)

### Cross Plot window - context menus &amp; polygons

![](/assets/018_crossplot.png)

_Cross Plot context menu, create polygons for masks option_

When you select the option to Create a new polygon a help box pops up to guide the process. You can change the setting in the General tab, to prevent this pop up, once you have learned how to edit polygons.

![](/assets/xplots-36-13.png)

### Cross Plot window - context menus &amp; overlays

![](/assets/xplots-36-14.png)

_Cross Plot context menu, add overlay functions option_

4 linear functions can be displayed over the top of any cross plot to aid interpretation:

**Chi angle/rotation : line slope = $$1/tan(\theta)$$**

where $$\theta$$ is either the angle of rotation clockwise from vertical or the Chi angle. In other words at 0 degrees rotation, Chi angle = 90 degrees and at 90 degrees rotation, Chi angle = 0 degrees.

**Predicted Noise Gradient : line slope = $$-1 / (sin^2</sup>( \theta_{effective}))$$**

Where $$\theta_{effective}$$ = angle from an average of angle gather $$sin^2(\theta)$$.

If the angle gathers used for the I and G calculations had angles from 4 to 40 degrees increment of 4 degrees, then the $$\theta_{effective}$$ angle would be $$ sin^2(\theta_{effective}) = \sqrt{\frac{\sum sin^2(\theta)}{N}}$$ so $$\theta$$ equals 24.24 degrees as the fold N equals 10 in this example. 

This is a Random Noise line prediction from AVO papers (“Stacked” paper by Hendrickson, Geophysics 1999 and AVO course, chapter 11 by Rob Simms.)

**Constant Vp/Vs, Gardner density : line slope = $$0.8 * (1-9*(Vs/Vp)^2)$$**

This line comes from the Castagna et al 1998 AVO paper and assumes the geology has constant Vp/Vs ratio and Gardner equation densities.

**Caprock V Reservoir Vp/Vs, constant density :**

**Line slope = $$1-8*\frac{(Vs_1+Vs_2)*\Delta Vs}{(Vp_1+Vp_2)*\Delta Vp} $$**

Where $$Vs_1, Vs_2$$ are the shear velocities in the Caprock and Reservoir respectively and $$Vp_1, Vp_2$$ the compressional velocities. $$\Delta Vs, \Delta Vp$$ the differences between these velocities.

This line comes from the book “Quantitative Seismic Interpretation”, by Per Avseth (see p. 205). Vp/Vs ratios can vary between the Caprock and the Reservoir but the density remains constant.

To adjust the angle of the overlay properly, make sure that the ratio between each axis is 1:1. You can use the ![](/assets/019_crossplot.png) button in the tool bar to ensure that the ratio is properly set.

### Mask volumes :

Mask volumes can be created from ‘visible points’, using the main Cross Plot window icon ![](/assets/crossplt13a.png) or from polygons created in the cross-plot window.

![](/assets/xplots-36-15.png)

_Inside a Cross Plot polygon, context menu_

Mask volumes have values of 1.0 where points/samples lie inside the polygon and 0.0 for outside. These can be QC’d using mask display and transparency in Gather, Stack and PreStack Map Viewers. The red overlay shows points outside the polygon in the first example below. ( The range to overlay is defaulted to -0.5 to 0.5 and therefore shows 0.0 mask volume values )

![](/assets/020_crossplot.png)

_Left: input seismic volume - Right: volume overlaid on top_

The red, yellow and blue colours show the points inside three different polygons in the next example. This option is selected using the inverse range box in the Transparency Tab, under Masks in the Stack Viewer.

![](/assets/crossplt19a.png)

_Masks – display points inside polygons as colours_

![](/assets/021_crossplot.PNG)
_Left: Seismic input to Cross Plot - Right: 3 Mask volumes overlain (inverse)_

**QC, Volume Calculator** can be used to multiply the original seismic by the mask volume. This remove amplitudes that aren’t inside the polygon (multiplied by zero) and leave just those inside. A kind of ‘cookie cut’ of the original volume by the mask volume results.

Also **Volume Calculator**, **Custom equation**, can be used to create an AVO class volume, combining several mask volumes. Each Volume is multiplied by a different scalar so that they can have a unique colour from the histogram.

![](/assets/022_crossplot.png)

_Custom mathematical equation for a 3 class volume_

![](/assets/023_crossplot.PNG)

_Left: 3 Mask volumes overlain on original stack - Right:combined into a class volume_

### Masks in Viewers :

Any volume can be shown as a mask instead of a volume in Stack, Gather and PreStack Map Viewers. Display the volume first, and select an amplitude range to apply as a mask, from the volume histogram.

Then use the right hand mouse button menu to ‘show as a mask’

![](/assets/crossplt31.png)

Set the ‘mask’ range using Max and Min values you have selected from the histogram, and select a transparency and masking colour that looks good. The **Stack Viewer example** below is of a near angle stack ‘cookie cut’ by the positive amplitudes ( 500 → 50000 ) of the far angle stack. It shows how well the frequencies match between stacks and where there are significant time shifts between events. Masks can be used to create this and other QCs for AVO processing.

![](/assets/crossplt32.png)

The **Gather Viewer example** below shows 4 gathers, overlain with mask colours, representing angle of incidence ranges. Four angle-muted gathers were created using Offset to Angle, of 5-14, 15-24, 25-34, 35-44 degree ranges.

These were then shown as masks, display ranges changed to -0.5 to 0.5 and inverse range selected. Transparency was set to 90% to ensure gather amplitudes were clearly visible.

![](/assets/crossplt29.png)

The **PreStack Map Viewer example** below shows 7 inlines, at time = 2.328secs, overlain with mask grey scale colour, representing angle of incidence ranges of 5-14, 15-24, 25-34, 35-44\. The darker the grey the higher the angle of incidence. The setup of the masks is the same as the previous example, except that the transparency was set to 70%.

![](/assets/crossplt30.png)
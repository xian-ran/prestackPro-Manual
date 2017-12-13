#### Background Model {#background-model}

Since Pcube+ is a pre-stack inversion method, a background model is required. This background model is defined in the Background Model tab.

**_Layer data_**

The background model consists of a set of layers, that are added to the model. The top of each layer must be defined by either a horizon or a specified time.

For each horizon, an uncertainty value is assigned. This parameter is supplied to allow for uncertainty in horizon picking. For reliable, interpreted horizons a low uncertainty value should be used, for example related to the width of the main lobe of the wavelet. If horizons are noisy or hard to track, the uncertainty should be increased to allow for possible jumps or cycle skipping.

Each horizon must also be assigned a unique hierarchy value. In the inversion routine, a horizon with low hierarchy value (20, 30, 40…) cannot cross a horizon with a higher hierarchy value (1,2,3…). Interpreted horizons (defined with small uncertainties) should be assigned high hierarchy values.

An offset value can also be specified for a horizon, which can be either negative or positive. The top of the layer will be shifted by that offset value relative to the defined horizon in the layer.

Well data can show that there are tops present, which are not possible to recognize from the seismic. Layers that represent these tops can be defined in the background model by using interpreted horizons and defining an offset value consistent with the distance from the horizon to the top.

By default, the uppermost layer is called Top and starts at time 0\. The uncertainty is 0 ms and the hierarchy value is 0.

**_Layer Probabilities_**

Each layer must be assigned litho-facies, and their probabilities must be specified. It is possible to define more than one litho-facies per layer. If the sum of the assigned probabilities is not equal to 1, the background model algorithm will normalize the probabilities.

The **Unknown Facies Probability** is a threshold. It catches data points lying relatively far away from the expected values of the elastic properties for each facies. Normally the default value is adequate.

**_Concept and smoothed models_**

The concept and smoothed models are shown to the right in the Background Model tab. The concept model includes the defined horizons, with eventual offset values and the assigned facies with their probabilities. The smoothed model also takes into account the uncertainties in the horizons.

The figure below shows an example of a background model. The layers are defined in the top left part of the window, while the layer probabilities are defined in the bottom left part.

The concept and smoothed models, seen to the right, are automatically updated as layer parameters or layer probabilities are added or changed.

It is also possible to change the inline and crossline values when pre-viewing the concept and smoothed models.

_Graphical user interface of the Background model_

The next figure includes more details about the setup of the properties of the defined layers. Notice that the interpreted Top Frigg horizon is used as the input horizon for several layers. For each of these layers an offset value is also defined. All these horizons are therefore equal to the interpreted Top Frigg horizon + offset.

_Layer data properties: The top of each layer is then defined relative to the Top_Frigg horizon by the offset value_

A yellow warning icon indicates that the Background model is not defined properly yet. A text box will appear if the cursor is hung over the tab title. It will give details of items that are still outstanding.

If a red triangle icon is visible to the right of the horizons, then it is necessary to click on it to the horizon into memory.

**_QC of horizons_**

It is important to stress the need to QC the horizons, since many of the artefacts seen in inversion results are due to horizon issues. Horizons should not cross, and they must also be spatially smoothed. If possible, they should not be defined too close together. If holes are present in some of the horizons, Pcube+ will ignore those locations in the inversion.
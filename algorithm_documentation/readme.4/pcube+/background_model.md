# Background Model

Since Pcube+ is a pre-stack inversion method, a prior model is required. This prior model is defined in the Background Model tab. Unlike classical simultaneous prestack inversions, the prior model is defined in terms of probabilities for each LFC \(litho-fluid class\) rather than a low frequency elastic model.

**Layer data**

The background model consists of a set of layers, that are added to the model. The top of each layer must be defined by either a horizon or a specified time.

For each horizon, an uncertainty value is assigned. This parameter is supplied to allow for uncertainty in horizon picking. For reliable, interpreted horizons a low uncertainty value should be used, for example related to the width of the main lobe of the wavelet. If horizons are noisy or hard to track, the uncertainty should be increased to allow for possible jumps or cycle skipping.



An offset value can also be specified for a horizon, which can be either negative or positive. The top of the layer will be shifted by that offset value relative to the defined horizon in the layer.

Well data can show that there are tops present, which are not possible to recognize from the seismic. Layers that represent these tops can be defined in the background model by using interpreted horizons and defining an offset value consistent with the distance from the horizon to the top.

By default, the uppermost layer is called Top and starts at time 0. The uncertainty is 0 ms and the hierarchy value is 0.

**Layer Probabilities**

Each layer must be assigned litho-facies, and their probabilities must be specified. It is possible to assign more than one LFC to any layer. If the sum of the assigned probabilities is not equal to 1, the background model algorithm will normalize the probabilities.

The **Unknown Facies Probability** is a threshold. It catches data points lying relatively far away from the expected values of the elastic properties for each LFC. Normally the default value is adequate.

**Concept and smoothed models**

The concept and smoothed models are shown to the right in the Background Model tab. The concept model includes the defined horizons, with eventual offset values and the assigned LFCs with their probabilities. The smoothed model also takes into account the uncertainties in the horizons.

The figure below shows an example of a background model. The layers are defined in the top left part of the window, while the layer probabilities are defined in the bottom left part.

The concept and smoothed models, seen to the right, are automatically updated as layer parameters or layer probabilities are added or changed.

It is also possible to change the inline and crossline values when pre-viewing the concept and smoothed models.

![](../../../.gitbook/assets/image%20%2842%29.png)

_Graphical user interface of the Background model_

The next figure includes more details about the setup of the properties of the defined layers. Notice that the interpreted Top Frigg horizon is used as the input horizon for several layers. For each of these layers an offset value is also defined. All these horizons are therefore equal to the interpreted Top Frigg horizon + offset.

![](../../../.gitbook/assets/image%20%284%29.png)

_Layer data properties:_

The horizon type is a flag that describes whether a horizon is eroding or not \(on-lapping\). Any eroding horizon is allowed to erode into any zone associated with a horizon that is older than itself. A non-eroding horizon that has not been eroded by a younger horizon, and is located higher than any of the older horizons, has its own zone right beneath itself. For an eroding horizon the situation is different. If it has eroded into an older horizon \(i.e. it is located deeper\), the zone right beneath it will be the zone of the oldest of the horizons it eroded into. Thus, as we move laterally from trace to trace, the zone beneath an eroding horizon can change. But the zone beneath a non-eroding horizon is its own zone, or the horizon is not present.

The table of zones gives the user the option of specifying that a zone is not allowed to pinch out. If the flag is set, the model attempts to avoid horizon crossings that would imply that the zone thickness was squeezed to zero. If for some trace this cannot be done without changing the prior depth or uncertainty span of one or more horizons, pinch-out is allowed despite the flag being set. Zone pinch-out disallowance is thus a soft criterion compared to the specification of the horizons themselves.

A yellow warning icon indicates that the Background model is not defined properly yet. A text box will appear if the cursor is hung over the tab title. It will give details of items that are still outstanding.

If a red triangle icon is visible to the right of the horizons, then it is necessary to click on it to the horizon into memory.

**QC of horizons**

It is important to stress the need to QC the horizons, since many of the artefacts seen in inversion results are due to horizon issues. Horizons should not cross, and they must also be spatially smoothed. If possible, they should not be defined too close together. If holes are present in some of the horizons, Pcube+ will ignore those locations in the inversion.


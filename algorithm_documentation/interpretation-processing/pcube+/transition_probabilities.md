#### Transition Probabilities {#transition-probabilities}

In the **Transition Probabilities** tab, the mean thickness for each litho-facies in each layer must be specified. This thickness can be extracted from well log analysis.

In this tab, illegal transition rules between litho-facies within a layer can also be defined. The purpose of these rules is to exclude non-geological and non-physical layering: for example, water bearing sand above gas sand.

The user interface is seen in the figure below.

![](/assets/083_Interpretation.png)

_The Transition Probabilities window_

The following example illustrates the use of illegal transition rules. Two litho-facies are defined in the layer, a lower and an upper hydrocarbon bearing sand. The lower sand must be located below the upper sand. The illegal transition rule will therefore be: The Lower HC sand facies is not allowed to exist above the Upper HC facies.

![](/assets/084_Interpretation.png)

_Defining illegal transition rules._

The figure below illustrates how the illegal transformation rules work. Three different realizations are shown for a number of sample points along a trace. Blue defines Upper Sand, while grey defines Lower Sand.

To the left no illegal rules are defined. Each sample can, based on litho-facies probabilities, be assigned any of the litho-facies, i.e. either Upper Sand or Lower Sand.

To the right, an illegal rule preventing Lower Sands from being above Upper Sands have been implemented. All samples assigned with Upper Sands are located above the samples with Lower Sands.

![](/assets/085_Interpretation.png)

_Schematic showing how introducing legal/illegal rules determines the distribution of different litho-facies _

By including rules like this, the posterior probability volumes for the different litho-facies will be more realistic, for example imposing blocky sand.

The figure below further illustrates the user of illegal litho-facies combinations. Three litho-facies, upper shale \(grey\), sandstone \(green\), lower shale \(blue\), are used.

To the left, the probability, defined as the match-weighted sum of all realizations, is shown for the case where no illegal combinations have been defined.

To the right the probability is shown for the case where only legal realizations have been included. The sand, in the right most part, is blocky and the probability distribution narrower.

![](/assets/086_Interpretation.png)

_Probability distribution of three litho-facies; upper shale \(grey\), sandstone \(green\), lower shale \(blue\). No illegal combinations defined \(left\); illegal combinations defined \(right\). Vertical axis defines time-depth direction, horizontal axis defines litho-facies probabilities._



The _window length_ parameter is the number of layers ahead used in the Markov chain analysis to set up the transition matrices controlling the layer transitions. It can make quite a big difference to the results, especially if your mean layer thicknesses are small,, but as you say it also affects the run time. If you put N for this parameter, and you have K distinct LFCs, and no illegal transitions, then the number of combinations is $$K^N$$.


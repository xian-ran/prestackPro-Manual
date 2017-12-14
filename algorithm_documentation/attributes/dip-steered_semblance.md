### Dip-steered Semblance {#dip-steered-semblance}

Go to **Attributes** → **Dip-steered Semblance**

This algorithm is an extension of the semblance attribute found in [Moving Window Statistics](moving_window_statistics.md).

![](/assets/cusersvalentinappdatalocaltem.png)

Dip-steered Semblance GUI

**_Input volumes_**

_The algorithm works per offset classes on either stacked or prestack volumes. In addition it requires the inline and crossline slope values computed on the input volume. Those attributes can be obtained using the_ [_Structural Dip_](structural_dip.md) _algorithm._

**_Parameters_**

_Parameters correspond to the stencil half lengths in the inline, crossline and time directions. The semblance will be computed inside this stencil using inline and crossline slopes to follow dipping events, resulting in a better estimation of the signal coherency for structures with large dips than with conventional vertical moving windows._
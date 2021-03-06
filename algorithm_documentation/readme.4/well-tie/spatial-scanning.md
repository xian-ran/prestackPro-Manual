# Spatial Scanning

![](../../../.gitbook/assets/250_interpretation.png)

Spatial Scan calculates horizon-based attributes around the well. QC maps are generated by comparing the well synthetic with each trace in a volume that is windowed around a horizon.

**Cross Correlation:** Each trace in the synthetic is correlated with the corresponding seismic trace. The user specifies the range of lags \(default is 40ms\) and whether the correlation is normalised \(the default is yes\).

**PEP:** Each offset/angle trace in the synthetic is compared with the corresponding seismic trace. The user specifies the range of lags \(default is 40ms\). For each lag, the difference is calculated as:

$$
residual = seismic - synthetic
$$

$$
PEP = \frac{1-(seismic - synthetic)^2}{seismic^2}
$$

PEP values for each lag are interpolated to find the peak PEP and the corresponding lag. Output maps are the peak value of PEP and the corresponding time lag.

**QC Maps:**

* Maximum Correlation
* Time-shift Maximum Correlation Envelope
* Instant Phase at Max Correlation Envelope
* Seismic Bandwidth
* Seismic SNR \(Signal to Noise Ratio\)
* **Maximum PEP** \(Proportion of Energy Predicted\)
* Time-shift Maximum PEP

![](../../../.gitbook/assets/251_interpretation.png)  
_To change the histogram colour scale or marker range right-mouse click on the histogram:_

![](../../../.gitbook/assets/252_interpretation.png)  
_Stack Seismic Max Correlation Map_

![](../../../.gitbook/assets/253_interpretation.png)  
_Pre-stack Seismic Max Correlation Map_

![](../../../.gitbook/assets/254_interpretation.png)  
_Stack Seismic Max PEP Map_

![](../../../.gitbook/assets/255_interpretation.png)  
_Pre-stack Seismic Max PEP Map_

![](../../../.gitbook/assets/256_interpretation.png)

**Well Location**

Moving the Blue X scan location, either using the mouse or selecting specific inline/crossline, updates the **Seismic At Well Location** panel in the main Well Tie Window:

![](../../../.gitbook/assets/257_interpretation.png)


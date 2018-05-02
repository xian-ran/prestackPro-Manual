### Wavelet Extraction & Editing {#wavelet-extraction-&-editing}

![](/assets/222_Interpretation.png)

A new window is launched, and the wavelet selected in the initial configuration window is displayed.

![](/assets/223_Interpretation.png)

The plots on the right-hand side show the **wavelet**, **amplitude spectrum** and **phase**.

* **Post processing:** edit the wavelet. 
* **Compare with:** compares current wavelet with saved wavelets.
* **Create wavelets:** loads a wavelet from the project or created a new one.

**Post Processing Options**  
The **Post Processing** options are common to all wavelet types:

![](/assets/224_Interpretation.png)

* **Phase Correction:** Phase rotation of the wavelet \(-180 to 180\). Corrections from the Cross-Correlation window will be input here.
* **RollOn Frequency:** The low frequency part of the phase is modified according to $$φ(f)=φ(θ) + (φ(f_{rollOn}) – φ(θ)) * (f/ f_{rollOn})^{rollOnExp}$$ 
* **RollOn Exponent:** The low frequency part of the phase is modified according to $$φ(f)=φ(θ) + (φ(f_{rollOn}) – φ(θ)) * (f/ f_{rollOn})^{rollOnExp}$$
* **Scaling Factor:** Scales the amplitude of the wavelet.
* **Frequency Smoothing Half-Length:** Standard deviation of Gaussian smoothing applied to the amplitude spectrum.
* **Output Wavelet Width:** Width in seconds of the processed wavelet.
* **Relative Taper Width:** Relative to the **Output Wavelet Width**, this parameter is used to taper the extracted wavelet using a $$10^{th}$$ order Gaussian function.

**Create New Wavelet**

![](/assets/225_Interpretation.png)

Create new wavelet options:

* **Load from project:** wavelets saved into the project can be loaded. To import a wavelet, go to **Utilities &gt; Well manager**.
* **Statistical Wavelet:** extracts a wavelet from the seismic volume without using the well logs.
* **Roy White Wavelet:** extracts a wavelet from the seismic volume using the Roy White method that includes well logs.
* **Synthetic Wavelet:** generates a synthetic wavelet that does not use seismic or well data.

**Statistical Wavelet**

Create new Wavelet &gt; Statistical Wavelet.

![](/assets/226_Interpretation.png)

![](/assets/227_Interpretation.png)

A statistical wavelet is extracted from the seismic data without using well logs. 

The user controls the window within which the wavelet is extracted. By default, the lateral extent (from the well) is 5 inlines/crosslines. This can be extended. The vertical window can be a fixed time window (e.g. 1 to 2s), the full trace or a window around a horizon. Low frequency roll-off tapering options are available. 

Now **Apply **the wavelets to the main Well Tie window synthetic.

For pre-stack seismic, the user has two options: the default is an extracted wavelet averaged over the angle range. The alternate option is to generate  pre-stack wavelet, i.e. a different wavelet for each angle.

To generate pre-stack wavelets click **Show pre-stack wiggles** in the menu bar, and toggle on **Create pre-stack wavelet**

The wavelets can be decimated, in the example below to every $$3^{rd}$$ angle.

Press **Apply **to update the synthetic using this wavelet.
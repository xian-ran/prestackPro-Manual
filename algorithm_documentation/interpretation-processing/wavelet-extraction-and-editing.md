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
* **RollOn Frequency:** The low frequency part of the phase is modified according to $$\phi(f)=\phi(\theta) + (\phi(f_{rollOn})-\varphi(\theta)) * (f/ f_{rollOn})^{rollOnExp}$$ 
* **RollOn Exponent:** The low frequency part of the phase is modified according to $$\phi(f)=\phi(\theta) + (\phi(f_{rollOn})-\varphi(\theta)) * (f/ f_{rollOn})^{rollOnExp}$$
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

The user controls the window within which the wavelet is extracted. By default, the lateral extent \(from the well\) is 5 inlines/crosslines. This can be extended. The angle range to used for the extraction can be limited to a subset of the data range. The vertical window can be a fixed time window \(e.g. 1 to 2s\), the full trace or a window around a horizon. Low frequency roll-off tapering options are available.

Now **Apply **the wavelets to the main Well Tie window synthetic.

For pre-stack seismic, the user has two options: the default is an extracted wavelet averaged over the angle range. The alternate option is to generate  pre-stack wavelet, i.e. a different wavelet for each angle.

To generate pre-stack wavelets click **Show pre-stack wiggles** in the menu bar, and toggle on **Create pre-stack wavelet**

The wavelets can be decimated, in the example below to every $$3^{rd}$$ angle.

Press **Apply **to update the synthetic using this wavelet.

![](/assets/228_Interpretation.png)

**Roy White Wavelet**

Create new Wavelet &gt; Roy White.

![](/assets/229_Interpretation.png)

The Roy White extraction method uses seismic data and well logs to extract a wavelet.

![](/assets/230_Interpretation.png)

The user controls the window over which the extraction takes place. Inline and crossline half-length defines the distance from the well, and the time window controls the vertical limits. The vertical window can be either fixed \(e.g. 1.75s to 2.15s\), contain the full trace, or consist of a window around a horizon. The angle range to used for the extraction can be limited to a subset of the data range. 

For pre-stack seismic, the user has two options: the default is an extracted wavelet averaged over the angle range. The alternate option is to generate a pre-stack wavelet, i.e. a different wavelet for each angle.

To generate a pre-stack wavelet click **Show pre-stack wiggles** in the menu bar, and toggle on **Create pre-stack wavelet**

The wavelets can be decimated, in the example below to every $$2^{nd}$$ angle.

Press **Apply **to update the synthetic using this wavelet.

![](/assets/231_Interpretation.png)

**Synthetic Wavelet**

Create new Wavelet &gt; Synthetic Wavelet.

![](/assets/232_Interpretation.png)

The synthetic wavelet options are shown below in the figure. **Amplitude**, **frequency**,** wavelet width** and **sampling size** can all be edited.

![](/assets/233_Interpretation.png)

**Applying A New Wavelet**

Press **Apply **in the Wavelet window to update the main Well Tie window:

![](/assets/234_Interpretation.png)

The name of the applied wavelet is updated in the top left-hand corner of the main window.

**Saving A Wavelet**

Note that applying a wavelet to the main Well Tie window does not save it to disk. **Save Session** will save the current wavelet as part of the session.

**Save **will store the wavelet as part of a group or individually into the project.

![](/assets/235_Interpretation.png)

**Exporting A Wavelet**

To export a wavelet, right-mouse click within the wavelet plot, select **Export to csv file**.

![](/assets/236_Interpretation.png)

![](/assets/237_Interpretation.png)

Menu options at the top of the wavelet window:

To compare normalized wavelets got to **Plot Settings** &gt; toggle on **Normalized**. This normalises the wavelet plot.

The Amplitude spectrum plot can be in **Linear **or **dB **and normalized in either mode.

* Wrap phase: between -180 and +180
* **Logarithmic frequency:** axis to switch plot from linear to logarithmic range.
* Maximum visible frequency can be edited.

**Compare Wavelets**

**Compare with raw wavelet** to see the wavelet \(in grey\) without post processing applied.

**Compare with:** shows the current wavelet in grey and another wavelet on top in colour. In the example below, the current wavelet is compared with a previously generated wavelet named _Roy\_White\_Wavelet\_5_.

![](/assets/238_Interpretation.png)


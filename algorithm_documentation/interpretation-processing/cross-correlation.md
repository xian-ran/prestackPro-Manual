### Cross Correlation {#cross-correlation}

![](/assets/239_Interpretation.png)

The **Cross-Correlation** window allows for a quantitative comparison of the synthetic in the main Well Tie window with the seismic data.

The correlation is displayed as the peak of the cross-correlation and the envelope.

Exportable results are:

* **Time shift** that can be applied to the current T/D table 
* **Phase rotation** that can be applied to the current wavelet

For stacked seismic data a single peak correlation and envelope wiggle is displayed.

For pre-stack seismic data the peak correlation and envelope are shown for all angles. The TD table and phase rotation values are averaged across either the full angle range, or a user-controlled angle range.

Cross-correlations between the synthetic and seismic data are within a user-specified time window. The options are:

* **Fixed Time Window:** user-controlled Min and Max \(s\)
* **Window Around a Horizon:** user specified time window around a horizon loaded from the project

**Pre-stack Seismic Cross-Correlation**

![](/assets/240_Interpretation.png)

In the example above a window from 1.75s to 2.135s is used as input for the Cross-Correlation.

Output tracks show the **Cross-Correlation** and the **Output Envelope**. The envelope shows the peak values spanning the pre-stack angle range.

Plots on the right-hand side:

* **Cross-Correlation & Envelope** across pre-stack angle range.
* **Measured Time Shift** across pre-stack angle range, sliders on the left-hand side control the limits.
* **Measured Phase** across pre-stack angle range, sliders on the left-hand side control the limits.

The red, vertical lines on the plots display the angle limits set by the slider bars.

![](/assets/241_Interpretation.png)

In the figure above, the average time shift of $$-0.00395397 s$$ \(highlighted in red\) is calculated from across the pre-stack angle range of 5-37$$^o$$.

Pressing **Apply to T/D table** will apply the time shift to the current T/D table. In this example, -0.004s will be added:

![](/assets/242_Interpretation.png)

Press **OK **to apply the time shift.

The **Checkshot Calibration** window is automatically opened and the **Total TWT Correction** will include the time shift from Cross-Correlation:

![](/assets/243_Interpretation.png)

Now you can **Apply **the time shift and update the synthetic.

![](/assets/244_Interpretation.png)

In the same example, the average phase rotation of $$21.0908^o$$ \(highlighted in blue\) is calculated from across the pre-stack angle range of $$5 – 37^o$$.

Now **Apply phase to wavelet**. The **Wavelet Extraction & Editing** window will open automatically. Here a $$21^o$$ phase rotation is used:

![](/assets/245_Interpretation.png)

Press **Apply **to update the synthetic in the main Well Tie window.

**Stack Seismic Cross-Correlation**

Cross-correlations between the synthetic and seismic data are within a user-specified time window. The options are:

* **Fixed Time Window:** user-controlled Min and Max \(s\)
* **Window Around a Horizon:** user specified time window around a horizon

![](/assets/246_Interpretation.png)

The Cross-Correlation window above shows a cross-correlation for a stack volume and synthetic for a window around a horizon. In this example, the horizon is Top\_Frigg\_Petrel\_Autotrack and the upper window length \(i.e. the distance above the horizon\) is 0.8s. The Lower Window \(i.e. distance below the horizon\) is 0.1s.

Output tracks show the **Cross-Correlation** and **Output Envelope** for the stack angle \(16deg in this example\).

Plots on the right-hand side:

* **Cross-Correlation & Envelope** values for stack angle \(e.g. 16deg\)
* **Measured Time Shift** values for stack angle \(e.g. 16deg\)
* **Measured Phase** values for stack angle \(e.g. 16deg\)

**Applying and Saving**

Applying an update to the TD table or the wavelet will not save these changes into the project. You must use **Save Session** or **Save **to save the current T/D table and wavelet.

To specifically save the updated T/D Table and/or updated Wavelet, use the **Save **icon found in the main Well Tie menu. The objects can be saved as a group or individually.

![](/assets/247_Interpretation.png)

**Display Options**

The **Control Tab** and the** Display Tab** at the bottom left-hand side of **Cross-Correlation** allow you to change the display.

**Control Tab**

![](/assets/248_Interpretation.png)

**Display Tab**

![](/assets/249_Interpretation.png)


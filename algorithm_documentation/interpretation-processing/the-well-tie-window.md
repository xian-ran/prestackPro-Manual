### The Well Tie Window {#the-well-tie-window}

The main Well Tie window displays:

* The $$V_p V_s Rho$$ logs selected by the user.
* **AI** \(Acoustic Impedance\) and $$V_p/V_s$$ ratio logs. These are calculated by Well Tie.
* An **initial synthetic**, generated using the wavelet selected during initialization. 
* **Seismic at the well location**, for deviated wells this is extracted along the well path for both, stack and pre-stack seismic data.
* **Correlogram**, a sliding window cross-correlation for a single angle plane. For pre-stack seismic this angle is chosen in the bottom left-hand side of the main window. The vertical axis is the centre of the rolling time window, and the horizontal axis is the correlation lag.
* **Seismic section** through the well. If the well is deviated the seismic is extracted along the path of the well. For pre-stack seismic, the gathers are extracted along the deviation survey and stacked on the fly with the angle being controlled at the bottom left-hand side of the main window. The section can be changed, e.g. inline to crossline, by right-mouse clicking on the header and choosing Track Configuration. The gain is controlled via the histogram in **track configuration**.

![](/assets/204_Interpretation.png)

**Zooming **can be controlled using the mouse wheel on the TWT/TVDSS track – or right-mouse click on the TWT/TVDSS track to manually change the range displayed.

**Correlogram:**
The correlogram is a sliding window cross-correlation for a single angle plane. For pre-stack seismic the angle is defined in the bottom left-hand side of the main window and can be changed by the user.


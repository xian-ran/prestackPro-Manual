#### Colored Inversion {#Colored Inversion}

The colored inversion workflow is built-in to the wavelet tool. It guides you through the necessary steps.

![](/assets/157_Interpretation.PNG)  
_Colored Inversion Workflow_

The workflow steps are as follows:

Step 1\) Load a zero-phase wavelet from the project, or create one from the seismic data. 
Step 2\) Create a Spectrum from the Acoustic Impedance Well Log

![](/assets/158_Interpretation.png)

Step 3\) Fit the Synthetic Well log Spectrum

![](/assets/159_Interpretation.png)

Step 4\) Calculate a Colored Inversion Operator, and convolve with the wavelet.

![](/assets/160_Interpretation.png)

![](/assets/161_Interpretation.png)

Step 5\) Apply the CI operator to the seismic data

**Spectral Whitening**

This spectral whitening workflow is given as an example, and should not be used without testing parameters for different data. There are many different ways of obtaining the same results.

The workflow performs spectral shaping to fit the seismic spectrum for a target interval to a desired output. For illustration a Butterworth spectrum is used as the desired shape. The workflow steps are:

1. Calculate the average seismic spectrum for the target zone using the spectral analysis tool.
2. Save it to the project.
3. Load it into the wavelet tool, with a zero-phase spectrum.
4. Design the desired spectrum \(zero phase Butterworth\)
5. Design a matching operator matching step 4 to step 5.
6. Apply additional tapering to the operator to reduce end effects.
7. Save the result of 7 to the project.
8. Apply it to the seismic data.
9. Recalculate the seismic spectrum for the target zone.

Step 1\) Open the spectral analysis tool, load the desired data \(a far angle stack in this example\), and use the data selection options to extract a spectrum in the target zone. Note that it is possible to use a polygon for data selection if desired. To obtain reliable spectra, the time window used should be log enough \(typically more than about 500 ms\).

![](/assets/162_Interpretation.png)

Step 2\) Save the spectrum to the project as a wavelet:

![](/assets/163_Interpretation.png)

Step 3\) Load this wavelet into the wavelet tool and select the ‘Load zero-phased’ option.

![](/assets/164_Interpretation.png)

Step 4\) Design the target spectrum. Here we are using a Butterworth filter, to broaden the input spectrum within a reasonable frequency band. Because the seismic amplitudes are up to about 50000, the Butterworth is scaled by 100000 so that the amplitudes match the input seismic data.

![](/assets/165_Interpretation.png)

![](/assets/166_Interpretation.png)

Step 5\) The matching operator length of 200 ms seems to give reasonable results. Testing the white noise parameter is important as it influences the extent to which noise is amplified at higher frequencies.

![](/assets/167_Interpretation.png)

Step 6\). It can be seen that the operator has high amplitudes at its ends. To avoid ends effects in the final result, we taper the operator. In the spectrum the effect of the tapering is to push down the high frequency part of the spectrum.

![](/assets/168_Interpretation.png)

Step 7\) The result of tapering is saved to the project as the operator to be applied to the seismic data.

Step 8\) The operator is convolved with the entire seismic volume using the User Defined Filter. In the example, it is clear that the wavelet is compressed. However, there is an increase in noise levels which might indicate a need for a lower bandwidth target wavelet or an increased white noise parameter in the match filter design.

![](/assets/169_Interpretation.png)

Step 9\). The dropper icon in the spectral analysis tool can be used to select the output of the User-defined filter. The initial data selection is preserved, so the spectrum of the data after application of the filer may be added to the plot for comparison with the original spectrum.

![](/assets/170_Interpretation.png)

**EEI Inversion**

An EEI inversion workflow is built-in to the wavelet tool. This uses coloured inversion to estimate any target well log property. It guides you through the necessary steps:

![](/assets/171_Interpretation.png)  
_EEI Inversion Workflow_

The workflow steps are as follows:

**Step 1**  
 Load a zero-phase EEI log wavelet from the project, or create one from $$V_p$$, $$V_s$$ and $$\rho$$ well log data.  
from Vp, Vs and Density well log data.

![](/assets/172_Interpretation.png)  
_EEI scan well log GUI_

**Create EEI wavelet from well logs**

• This takes $$V_p$$, $$V_s$$ and density logs as input. It creates an EEI log with the selected Chi angle. It automatically calculates a log wavelet ready for Colored Inversion with the corresponding EEI reflectivity volume wavelet.  
• The Chi angle with the best correlation coefficient is chosen by running a scan of cross-correlations between a target well log and a range of EEI logs from Chi angles $$-90^o$$ to $$+90^o$$.  
• In the example above, the EEI that best fits the $$30/10-2$$ GR log is at $$26^o$$. For $$30/10-3$$, it’s at $$22^o$$.  
• In the example below for well jk-syn-test, the EEI that best fits the GR log is at $$22^o$$. For the $$V_p$$/$$V_s$$ ratio it’s at $$39^o$$. For the Poissons Ratio it’s at $$38^o$$.

![](/assets/173_Interpretation.png)

![](/assets/174_Interpretation.png)  
_EEI scan coefficient display and results table_

The results table shows the well name, the log, the best EEI chi angle and its correlation coefficient. This table allows users to compare the same logs at different wells, and for different logs at a single well.

Users can select a method for calculating log averages:

![](/assets/175_Interpretation.png)

‘Logs’ averages over the selected depth range, ‘Facies’ uses PCube facies averages.  \(The default method is to use Logs and these $$V_p$$, $$V_s$$ averages for $$k$$\)

![](/assets/176_Interpretation.png)  
_EEI Parameters GUI_

**Step 2**  
Fit a Synthetic Well log Spectrum, or apply a butterworth filter to the EEI log spectrum.

![](/assets/177_Interpretation.png)  
_Fit Synth. Well log spectrum GUI_

**Step 3**  
Create an equivalent EEI reflectivity wavelet from I & G volumes

![](/assets/178_Interpretation.png)  
_Create EEI Wavelet from I/G volumes GUI_

The application creates an EEI reflectivity volume, using the chi angle from the EEI log spectrum, and then generates an average spectrum from this equivalent volume. By default the spectral calculation uses all the traces from the input seismic unless the X,Y range is reduced by a map polygon.

**Step 4**  
Calculate an EEI Operator, and apply to the data

![](/assets/179_Interpretation.png)  
_Calc. EEI Inv. Operator GUI_

The preview windows show, the chi reflectivity volume, a $$-90^o$$ phase rotated version and the result of EEI inversion; from left to right. This allows the user to see what effect the phase and the frequency rotation have. In the example above, it is easy to see the boosting of the lower frequencies that has occurred between the middle and right-hand window.

The preview windows can be fixed open by use of this icon → ![](/assets/180_Interpretation.png)

Then any changes to the input wavelets \(e.g. to log spectrum fit parameters; to polygon X, Y location; to low and high cuts\) will update the EEI inversion result, on the fly.

![](/assets/181_Interpretation.png)

When the preview of the final inversion looks OK, for a number of test inline/crossline locations; the EEI inversion can be ‘applied to the whole volume’ by selecting this option from the GUI, shown above. (The EEI operator will need saving to the project first however).


### Checkshot Calibration {#checkshot-calibration}

![](/assets/212_Interpretation.png)

The Checkshot Calibration tool enables the user to edit the checkshots, calibrate the sonic log, and generate a drift curve. The result is a Time-Depth table that is applied to the synthetic.

![](/assets/213_Interpretation.png)

The ITT method \(Interval Transit Time\) is used in Well Tie:

1. Calculate the Drift curve:

2. Convert $$V_p$$ log to time-depth curve

3. Calculate the difference between checkshot time-depth curve and $$V_p$$ time-depth curve. This is the drift curve

4. Calculate a fit to the drift curve; in an ideal world the drift would be zero.

5. The drift curve is applied to checkshot time-depth curve, generating a new TD curve and a calibrated $$V_p$$ time-depth curve.

6. The output TD curve is resampled to minimum 1m distance.

The checkshots listed in the table are fully editable. As changes are made to the checkshots the velocity and drift tracks will update to show the impact of any changes. The Well Tie module has been designed to be used iteratively; the user can come back to this tool and redo the checkshot calibration at any point.

To load an alternative checkshot or TD table, click on the name of the current checkshot set and select from the list of sets saved in the project. To import a checkshot set or T/D table go to **Utilities &gt; Well Manager**.

The current checkshot set name is displayed in the main Well Tie window. If edits have been made \(e.g. some checkshot pairs are toggled off\) the name will extend to differentiate it from the raw/original checkshot set.

To use the **Calibrated **$$V_p$$ as input to the synthetic toggle this option on.

**Interactive** mode will auto Apply changes to the main Well Tie window. This is a great option if you want to see the effect of your parameter changes almost instantly. However, use this option with caution, as updates may take some time.

![](/assets/214_Interpretation.png)

**Editing Checkshots**

Options to edit checkshots:

* Toggle off/on in the table
* Type over the value of TWT/TVDSS in the table
* Add/delete checkshot rows
* Decimate the checkshots

Press **Reset **to revert all changes to the checkshots.

To locate a specific checkshot via the velocity track, hold the CTRL key down and click the mouse cursor in the velocity track. The nearest corresponding checkshot will be highlighted in blue in the table. When you deselect a value the velocity and drift curves will update:

![](/assets/215_Interpretation.png)

Edit the checkshot rows using right-mouse click on a row in the table. **Rows can be added, unchecked/checked or deleted**. Any TWT or TVDSS cell can be manually typed over.

![](/assets/216_Interpretation.png)

You can **Decimate **the checkshots, here by 2:



![](/assets/217_Interpretation.png)

Press **Reset **to revert all changes to the checkshots.
### Stretch & Squeeze {#stretch-squeeye}

![](/assets/258_Interpretation.png)

Stretch & Squeeze is a separate window from Checkshot Calibration and allows the user to test TD changes by visually comparing the synthetic with the seismic data.

It contains the following panels:

* **Seismic Panel:** the seismic data at the well location.
* **Modified Synthetic:** the synthetic will auto-update cumulatively for all stretch & squeeze operations.
* **Reference Synthetic:** displays the original synthetic with no stretch & squeeze applied. The markers highlighting the stretch & squeeze rows are shown on the reference synthetic.
* **Velocity:** both original velocity and the cumulative, modified velocity is displayed.

Bulk shifts can be added, allowing the user to link clear markers in the seismic and the well logs. This can be added manually by typing TWT values into a row, or visually by digitising directly onto the seismic and synthetic panels.

A single row can also act as a pin, to restrict any later stretch and squeeze functions to portions of the well.

Multiple rows can be added manually or digitally, stretching and squeezing the original TD table.

To remove all stretch & squeeze modifications press **Delete All**

The main Well Tie window and the synthetic displayed there will not be updated until the user presses **Apply **in the **Stretch & Squeeze** window.

![](/assets/259_Interpretation.png)

![](/assets/260_Interpretation.png)

![](/assets/261_Interpretation.png)

![](/assets/262_Interpretation.png)

**Applying and Saving Stretch & Squeeze**

Stretch & Squeeze enables the user to visually test changes to the TD table without updating it. As rows are added, any bulk shifts and/or stretch & squeeze operations shown in Stretch & Squeeze do not auto update the TD table.

**Apply **will update the TD table and the synthetic in the main window.

![](/assets/263_Interpretation.png)

The updated TD table is not automatically saved. You can **Save **it to the project in the main window:

![](/assets/264_Interpretation.png)

To view the saved stretch & squeezed T/D table in the Checkshot Calibration window: open **Checkshot Calibration &gt; select the saved TD table from the pull-down list**.

**Stretch & Squeeze and Cross-Correlation**

Updating the T/D table within Cross-Correlation after applying Stretch & Squeeze will lead to conflicts between the current T/D table and the Stretch & Squeeze.

For clarity, a warning box with various options will appear. Select the relevant option to proceed:

![](/assets/265_Interpretation.png)


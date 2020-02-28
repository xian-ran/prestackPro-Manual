# Multi Well Tie QC

The Multi Well Tie QC allow user to get a overview of the well tie quality across multiple wells, and access the [Well Tie](../well-tie/) module to investigate possible causes and fixes to improve the well tie. Evaluation of the well tie quality is primarily based on [cross-correlation](../well-tie/cross-correlation.md) between seismic and synthetic in either stack or pre-stack domain.

**Setting up Multi Well Tie QC**  
There are three different ways of building the «Data Table» with Well Ties

1. Create Well Tie for one well \(define logs, wavelet\)
2. Create Well Tie for Multiple wells
3. Add previously saved Well Ties \(from Well Tie Objects\*\)

\*\) Well Tie Objects consist of T/D table, wavelet and elastic logs

Creating Well Tie for one well will add one row to the table, while user can choose to add multiple wells. When multiple wells are added log set will be used if present.  
Well Tie Objects can be saved from the [Well Tie Window](../well-tie/the-well-tie-window.md) and will be stored as a group under the well in file manager.  

![Setting up Multi Well Tie QC \(three different ways to populate Multi Well Tie data table \)](../../../.gitbook/assets/image%20%2860%29.png)

The seismic **Input Volume** can be either a pre-stack or stack volume.

The cross-correlation **Time Window** can either be a fixed window or be a window around horizon. By defining a window around horizon the correlation window can be targeted at different levels in different wells. User can see the center time of window for each well, and explore any potential depth trend.

**Lead/Lag time** define the allowed time shift for maximum correlation

**Wavelets** can be individual wavelets as defined in data table or could be a selected wavelet from project for all entries in table \(i.e well ties\). User can also average wavelets and use this for all entries.

![Input Volume, setting Time Window and selecting wavelets for cross-correlation analysis](../../../.gitbook/assets/image%20%2827%29.png)

Based on the input parameters \(seismic, time-window, wavelet, elastic logs and T-D\) statistics are calculated for each well tie and presented in graphs.

Wavelet plot \(left\) show time-amplitude, amplitude spectrum and phase spectrum for the wavelets given in data table. If "one wavelet is used for all" this wavelet will be highlighted.

The QC plots included statistics based on cross-correlation and PEP \(proportion of trace energy predicted\) and are all plotted as a function of angle, if input volume is containing angle information.

![Multi Well Tie QC - Graphs \(individual graphs can be hidden by eye-icon in Data Table\)](../../../.gitbook/assets/image%20%2822%29.png)

The **Well Tie Data Table** will give an overview of the used input data for the analysis as well as some information on the cross-correlation window \(minimum time, maximum time, window length, window center time\). If logs are not covering the full time window a warning is given in yellow

An average of the maximum cross-correlation envelope over entire angle range is given in rightmost column and gives an indication of the well tie quality for each well tie entry in table.

**Error messages** related to data issues will be highlighted in red and could be due to

* missing logs or data outside defined time window  
* invalid well data
* well positioned outside input seismic coverage

An "Average Wavelet" using principal component analysis \(PCA\) can be estimated from a selection of wavelets from table. If input wavelets are pre-stack user get a selection of angles and has various options to average stacked and pre-stack wavelets 

Well ties can be opened through the **table context menu** \(MB3\), and rows can be duplicated or removed

![Well Tie Data Table](../../../.gitbook/assets/image%20%2867%29.png)

![Table: Row context menu. Can select multiple rows \(CTRL+MB1\) and remove from table](../../../.gitbook/assets/image%20%2856%29.png)


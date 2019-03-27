# Log data Q.C. &  management

Logs can be renamed or deleted as a group using **Project → File manager**    
  
To rename a log, double click on the log name in the tree.

A group of logs can be selected from the tree and deleted all together.

Logs can be Q.C’d by **Utilities → Edit Well Logs.** This can also be opened for a specific log within the File Manager by selecting Log Manager from the MB3 context menu.

![](../../../.gitbook/assets/003_well_log_viewer.png)

_Opening **Well Log Editor** from the file manager tree_

![](../../../.gitbook/assets/004_well_log_viewer.png)

_Logs can be edited by selecting **Create temporary copy for editing**. This creates an editable copy of the log. In the figure below, the upper left section of the Well Log Editor is seen in edit mode._

![](../../../.gitbook/assets/005_well_log_viewer.png)

In edit mode, log samples can be selected and modified, and logs can be combined.

To **select samples**, choose Select samples. Several selection options are available. ![](../../../.gitbook/assets/006_well_log_viewer.png)

To modify samples, select one or more values in the table \( **Modify samples** button will become active\). Then select **Modify samples**. Several options are available; adding, setting and scaling by value, interpolation and removal of samples, and using custom defined equation. In the example to the right, **Use custom equation** has been selected. The syntax is the same as for Volume Calculator. Here Vp is converted to Vs, for sands, using the Castagna equation.

![](../../../.gitbook/assets/007_well_log_viewer.png)

Select **Combine Logs** to merge and mask other logs with the current log

When using **Combine Logs** it is possible to specify output log range, the method for populating empty regions in one of the logs, and to specify a custom equation.

![Combine logs](../../../.gitbook/assets/011_editlogs.png.png)

![](../../../.gitbook/assets/010_well_log_viewer.png)

_Logs can be crossplotted for Q.C in **Interpretation-processing → Cross Plot**._

Logs can be grouped in sets using **Utility → Manage Logsets**, which can also be opened from the Well Log Viewer.

![](../../../.gitbook/assets/011_well_log_viewer.png)

Clicking on the yellow star icon will create a new well log set. Selected logs from wells can then be added to the set using the uppermost blue arrow icon. Select logs in the log set and use the lowermost blue arrow icon to remove logs from the set.

This log set can then be manipulated as a group of objects. For example, a set of Vp,Vs and Rho logs for can be used as input to create a synthetic gather. Logs sets cans also be drag-and-dropped as a group, into the Well Log Viewer.


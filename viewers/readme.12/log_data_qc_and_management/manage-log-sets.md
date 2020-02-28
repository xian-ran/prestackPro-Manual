# Manage Log Sets

By organizing the elastic logs in LogSets it’s easier to select the logs when needed in other PsPro modules, and when displaying the logs in the LogViewer. LogSets are managed by the Log Set Manager found under utilities menu \(Utilities-&gt;Log Set Manager\). 

The Log Set Manager has different functionality

1. Add New Log Set
2. Calculate Missing Log 
3. Resample logs to common depth sampling
4. Convert old Log Set to current format
5. Delete Current Log Set

Some statistics are given at the bottom of the Log Set Manager, the number is highlighted in case of inconsistencies. Wells \(i.e. rows in table\) can be hidden by opening/closing the eye-icon next to well in the left-hand side of the Log Set Manager. Log Set can also be filtered by applying a filter pattern in search box above the table.

### **Add New Log Set**

Open the **Log Set Manager** \(Utilities-&gt;Log Set Manager\) and "Add New Log Set". This allow the user to create a new Log Set and fill columns \(i.e. Log Types\) with logs matching a given text filter \(in figure below this is set to "\_Brine"\).   
All cells in table is editable by double-clicking MB1, to edit Log Set Name, Color or select individual logs. Selecting logs will bring up a list of logs which matches the current well \(i.e. row in table\) and current log type \(i.e. column in table\).  
The "Active" tick-box indicate which Log Set is used as default by Pre-Stack Pro. Only one Log Set can be active per well.  
All changes are saved when pressing Apply.   
Log Sets are stored under each well in the File Manager and logs associated to this LogSet will show under that logset. If same log is used in different Log Sets it will appear multiple times.  

![Create and manage Log Sets. Utility-&amp;gt;Manage LogSets](../../../.gitbook/assets/image%20%2821%29.png)

![Create Log Sets from Well Log Viewer](../../../.gitbook/assets/image%20%2837%29.png)

![Create Log Set from &quot;Generate Synthetic Gather&quot;](../../../.gitbook/assets/image%20%2812%29.png)

### Calculate Missing Log

Logs that are not specified for a given Log Set can be calculated for the current logset using the Calculate Missing Log functionality in the Log Set Manager. This bring up a dialogue to select which logs to calculate.   
Logs are saved under the current Log Set in the File Manager.

NB. Calculate Missing Log will return an error if logs are not equally sampled and user will be asked to re-sample logs - see "Resample logs to common depth sampling"

![Calculate Missing Elastic Logs from Utilities-&amp;gt;Log Set Manager](../../../.gitbook/assets/image%20%2864%29.png)

### Resample logs to common depth sampling

The statistics \(bottom window of the Log Set Manager\) might show some sampling inconsistencies between the different logs in Log Set. Any inconsistencies will be highlighted by red font and some warning text describing the inconsistency.  
Sampling distance can be set \(default is 1/2foot sampling\)   
A threshold value for any gaps in log \(i.e. no recorded data in log\) can be set, so that actually gaps in log are not re-sampled with interpolated values.

![Resampling Well Logs in Log Set Manager](../../../.gitbook/assets/image%20%2833%29.png)

### Other Functionality

Old logsets from previous Pre-Stack Pro Projects can be converted to this new Log Set format.  
Current Log Set \(i.e. the highlighted Log Set in table\) can be deleted. 


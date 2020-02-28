# Manage Well Zones

Well Zones would typically be generated when inspecting well logs in the [Well Log Viewer](../viewers/readme.12/well_log_viewer_gui.md). After a zone has been defined the zone filters can be distributed across multiple wells in the Well Zone Manager.

![Well Zones Manager - Functionality and Table context menu \(MB3\). Infor. on zone displayed in box below](../.gitbook/assets/image%20%2867%29.png)

The Well Zones Manager is organized as a table per Zone where filters are displayed as sets of columns and wells as rows. Zone name and color can be edited and filters can be added and/or edited.   
A new zone can be added directly from Well Zones Manager in addition to adding zones from  [Well Log Viewer](../viewers/readme.12/well_log_viewer_gui.md). 

Existing zones can be **copied** and edited.  
Example \(see plot above\):   
SandZone is defined between two tops and a GammaRay Log cut-off.   
Zone can be copied and GammaRay cut-off can be edited to define ShaleZone within same interval \(see plot below\)

![Selecting multiple rows by CTRL+MB3 &amp;gt;&amp;gt; Multiple Rows context menu](../.gitbook/assets/image%20%2830%29.png)

Multiple rows can be selected by combinations of CTRL+MB3 \(individual row selection\) and SHFT+MB3 \(row range selection\). Multiple rows context menu \(MB3\) allow for set filters values and remove wells in multiple rows.  
Each cell can be edited by MB1 in cell. 

**Add Zone to Multiple Wells** to distribute zone across wells in project. Adding all wells to Zone table gives a overview of zones defined across wells and will highlight if any issues. Issues could be that Well Top is undefined or inconsistently named, well log is missing , etc.  
Some inconsistencies in data can be corrected or wells can be removed from zone definition. In some cases Tops are not defined in all wells, and other upper and lower top might be chosen for the same zone.

Note that an "Empty" Zone Length will not give a red warning in well column. User can go through table and observe zone length in each well   


![Adding Zone definition in multiple wells. ](../.gitbook/assets/image%20%2868%29.png)




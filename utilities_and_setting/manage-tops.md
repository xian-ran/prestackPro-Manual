---
description: >-
  Organize formation tops by renaming tops to common names and set default
  visibility for the viewers.
---

# Manage Tops

Table is organized with wells in project with set of columns \(visibility, Top Name, Depth, Interpreter\). Each row represent a Well Top with a unique Top Name and color. Same well Top can appear in more than one row depending on sorting of rows and if Top is encountered more than once in same well. Multiple rows \(selecting from Top Names column\) or cells can be selected by using:   
  
a\) \[MB1\]: Selecting one cell or row   
b\) \[Ctrl+MB1\]: Selecting individual cells or rows   
b\) \[SHIFT+MB1\]: Selecting range of individual cells or row   
c\) \[Ctrl+Shift+MB1\]: Selecting combination of individual and range of cells or rows   
  
\[MB3\] opens a menu with different functionality \(see below\)Top Manager GUI: Functionality outlined and details given below

![Manage Tops: Visibility, Color, Name](https://blobscdn.gitbook.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LFpvGkg3-7n_cdd1ccT%2F-LZFEyBb_YgD9klmdPTG%2F-LZFFEUNEtmUsQ6akjRz%2F201_ManageTops_001_MainGui.PNG?alt=media&token=7d1697ab-e51e-4fff-bf46-ee1c6eeaf73c)

### Organizing the Well Tops Table <a id="organizing-the-well-tops-table"></a>

**Show/Hide wells:** Will show wells activated by Eye-Icon and only show Well Tops \(rows\) defined in those shown wells. **Text filter on Top Name:** Will show tops matching the text filter **Text filter on Interpreter:** Will show tops where interpreter match the text filter **Show/Hide Rows:** Show all rows or hide rows in table where Tops are hidden in all **Show/Hide Interpreter Column:** Will show column with Interpreter **Sorting Table** by different Columns \[MB1 on top of column\] \(Top Name, Depth, Interpreter\) **Set Depth Domain:** MD or TVD

### Configuration Top Highlight <a id="configuration-top-highlight"></a>

Selecting a cell \[MB1\] will highlight other tops within a set threshold value with a color. This allow to see   
  
a\) if closely spaced tops could be hidden in the viewers   
b\) if tops can be consolidated to a common name   
c\) if tops are duplicates and can be removed  
  
Top Highlighting functionality: Setting the Threshold Value \(example: 20m\) and highlighting Tops.

![Highlighting Tops within Threshold value to help organize and set visibility of Tops](https://blobscdn.gitbook.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LFpvGkg3-7n_cdd1ccT%2F-LZFIQpyjW_EwXWu8Tj2%2F-LZFODM6FsvxAofjcdCF%2F201_ManageTops_002_HighlightTops.PNG?alt=media&token=2ed8dd44-1eb1-4ecd-8b3b-b5e1c754ce3c)

### Well Tops Visibility \(in viewers\)  <a id="well-tops-visibility-in-viewers"></a>

Well tops visibility can be set individually by tick/untick the check-boxes next to the Well Top for each well. This can also be set in Well Log Viewer and stored to Default settings \(red save icon\).   
  
When a Well Top is set to visible in all wells the first CheckBox will be ticked with white background.   
If a top is hidden in one or more wells the CheckBox will be ticked and greyed out.   
To set a Well Top visible across all wells where Top is present, tick the first CheckBox next to Top Names column.   
  
Several rows and cells can be selected \[Ctrl+MB1\] to control visibility \[MB3\]. Set Tops visibility: Select cell or cells \[Ctrl+MB1\] and press MB3 to open content menu

![Setting visibility in &quot;Manage Tops&quot; or in Well Log Viewer \(single well\)](https://blobscdn.gitbook.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LFpvGkg3-7n_cdd1ccT%2F-LZFZprT4XtfrgFBUaCH%2F-LZFZwQjVZnCcJAZga20%2F201_ManageTops_003_WellTopVisibility.PNG?alt=media&token=14d186f1-3606-4cc0-8144-ee64f1dfb562)

### Well Tops Editing  <a id="well-tops-editing"></a>

Different editing options are available   
a\) Set the **Color**: \[2\*MB1\] on the Color cell   
b\) **Rename** Well Tops: \[2\*MB1\] on individual Tops or Project Tops   
c\) Change **Depth**: \[2\*MB1\] on Depth cell   
d\) **Add top for all wells**: \[MB3\] on Project Top cell. Give a Top Name. This add top to all wells   
e\) **Add top**: \[MB3\] on individual Top cell. Give a Top Name. This add top to current well If adding a Top that already exist a number is added to the Top Name. If a new Top Name is given a new row is added to the Well Tops table. Add top: For all wells, selection of wells or for single wells

![Adding Top for all wells or single well \(MB3 on Cell or Row\)](https://blobscdn.gitbook.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LFpvGkg3-7n_cdd1ccT%2F-LZFaoq1E-InZ76C0xFZ%2F-LZFsYpXKewp7MEt-zEI%2F201_ManageTops_005_AddTop.PNG?alt=media&token=6b7c5146-d0a3-40bf-b8ab-1403444388c4)

Well Top Names can be given a **common name** by highlighting two or more cells and/or rows \[Ctrl+MB1\] and \[MB3\] to give Tops a common name. User can select any of the given names or type in a new name for the TopGive common name: This to consolidate Tops into same row

![Give common name to Tops to consolidate to same row and make consistent across wells](https://blobscdn.gitbook.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LFpvGkg3-7n_cdd1ccT%2F-LZFaoq1E-InZ76C0xFZ%2F-LZFeHhor_h4E94Av84b%2F201_ManageTops_004_GiveCommonName.PNG?alt=media&token=b00ab712-c93a-4c15-87d9-215d59c8003c)

### Apply changes <a id="apply-changes"></a>

All changes will take effect when pressing apply. User will be prompted with a warning message if leaving the Manage Tops utility without having applied the changes

​![](https://firebasestorage.googleapis.com/v0/b/gitbook-28427.appspot.com/o/assets%2F-LFpvGkg3-7n_cdd1ccT%2F-LZFaoq1E-InZ76C0xFZ%2F-LZFuPZtcvOgjkllHN7t%2F201_ManageTops_Warning.PNG?alt=media&token=7abf2003-e4ee-4af9-a312-442f76cfb344) Warning Message


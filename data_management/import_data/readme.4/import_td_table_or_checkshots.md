# Import T/D table or Checkshots

If you did not import time values when the well path was imported, you can do this by either **Project** → **Import Wells** → **Import Well T/D tables** \(or **Checkshots**\)or simply do this from **Utilities** → **Manage Wells**. It is possible to associate several T/D tables and checkshots to a given well.

![](../../../.gitbook/assets/009_import_well.png)

To import time-depth data or checkshot data select **Import T/D table** or **Import Checkshots**. The process of picking live data is the same as for importing well path. Only columns with TvD and Two Way Time are required. Make sure that time is picked with correct unit \(second or millisecond\).

![](../../../.gitbook/assets/010_import_well.png)

**Additional Parameters:**

![](../../../.gitbook/assets/011_import_well.png)

* Set the depth reference datum: KB \(set up in **Manage Wells** or when importing the well head\), SSL or custom value
* Define if the T/D table is a checkshot or not
* Define if this table is the active table for computation of the time-depth relationship when displaying the well or logs in a viewer.

**View T/D table** or **Checkshots:**

![](../../../.gitbook/assets/012_import_well.png)

The imported time values can be viewed for QC by clicking **View T/D Tables** or **View CS tables**. True vertical depth and corresponding time values are listed in a table. Distance units can be selected as meters or Feet. If more than one T/D table \(or checkshot\) are associated with the well, one of them must be selected and set as active.


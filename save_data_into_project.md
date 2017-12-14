# Save Data into Project {#save-data-into-project}

Any volume in the Data Pool can be saved on disk as a part of the current project. To save a volume, right-click on it in the Data Pool and select **Save Volume to Project.** A window similar to the one for selecting data will open.

![](/assets/001_save_data.png)

_Save Volume to Project_

In the right corner, there is a field allowing you to type the name of your choice for the volume. Like the Select data window, you can trim and/or decimate the volume in the 4 dimensions to the subset of your choice.

When saving an arbitrary volume, only time and offsets/angles can be trimmed. Inline and crosslines are locked to the selection made from the arbitrary path.

An arbitrary volume saved on disk is the child of the locked arbitrary path created at the same time as the volume. This is important to remember if deleting a path or a volume from the disk.

![](/assets/002_save_data.png)

_Arbitrary path child relationship_


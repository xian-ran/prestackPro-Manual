### Open shared project and transfer data {#open-shared-project-and-transfer-data}

Go to **Project** → **File Manager** and click on the icon ![](/assets/011_file_manager.png) “open shared project”. The file manager will be spilt into two sections, one for the original project and one for the newly created one.

![](/assets/012_file_manager.png)

_File Manager for Shared Projects_

To transfer data from one to another project, select the volumes by checking their tick-boxes and click on the blue arrow in the central part of the window that corresponds to the correct direction _from..to_.

Ticking _Symbolic link" _means the volume will not be copied to the shared project, but instead a symbolic link to it will be created, thus saving disk space. The symbolic link information is into the history of the volume in the shared project. Once the volume is modified in any way and overwritten to disk, a copy is made into the shared project and the link is discarded. 

By design it is possible to transfer data between projects that do not have the same geometry. However, the user should be aware that the correspondence between World coordinates and project grid coordinates might not be correct anymore.


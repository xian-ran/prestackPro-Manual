# Restore a project {#restore-a-project}

Unfortunately, it might happen that a project get corrupted. The good news is that it is a rare events usually links to sudden loss of power on the hardware. If this happens there are two possibilities to restore completely or partially the project:

* Use the utility provided within the software
* Restore manually the project file using one of the backup



## Utility Restore Project Data

**Project** → **Restore Project Data**

This will scan the project for datasets that exist on disk, but are not present in the project configuration file. The data must have been created \(or loaded\) with Pre-Stack Pro version 4.6.0 or higher.

There are the options to restore or to remove selected items:

**Restore**: This will add the missing data back into the configuration file.

**Remove**: If the datasets are no longer required, then they can be deleted from disk.

![](/assets/001_Restore_Project.png)

_Restore Project Data_



## Backup of the project file

At several points in a project history, the project file \(_config\_PreStackPro.xml_\) is backed up. This back up can be used to replace a corrupted project file.

Whenever something is changed in the project, a backup file will be written in the .PreStackPro/ directory. They will be named config_PreStackPro.xml.rXXX where XXX is a version counter. No other file will be written, copied or deleted at that point. If there are more than a defined number of such project backup files \(e.g. more than 10\), the oldest ones will be deleted, so that exactly the 10 most recent are left.






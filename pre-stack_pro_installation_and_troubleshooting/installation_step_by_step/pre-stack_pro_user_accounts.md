### Pre-Stack Pro User accounts {#pre-stack-pro-user-accounts}

To allow login and start Pre-Stack Pro across the different nodes, Pre-Stack Pro will ask for Login credentials when started.

Please note that Pre-Stack Pro will NOT allow starting up as root user.

The authentication is done through GPI which uses linux’s default PAM authentication settings. This makes it possible to use both local user accounts and network accounts if properly connected to an AD/LDAP network domain.This guide will only cover local user account setup.

Important: Please create the same user account on all nodes with the same password and in the same order.

If this is a multiuser system you would want to add them to the same group and give this group RW access to the same folders on the parallel filesystem.

Adding a group:

| groupadd psprousers |
| --- |

Adding users to the newly created group and setting password:

| useradd psprouser1 –g psprousers |
| --- |

| Edit: /opt/PreStackPro/etc/PreStackProBackendrc (on all nodes) |
| --- |
| Change the line: #Umask = 027 to |

This will make Pre-Stack Pro give the group psprousers full read/write access to newly created files and projects within the specified data folder given on startup of Pre-Stack Pro (/data_parallel/)

IMPORTANT: Users must be added in the same order to keep the Unique user ID the same on all hosts.

First user will normally get the UID: 500 and first Group will normally get the GID: 500.
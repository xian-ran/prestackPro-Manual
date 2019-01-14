# Installation of the BeeGFS Parallel File System

If you did not choose BeeGFS, but already have a parallel filesystem you can skip this step.

Please note that the BeeGFS client requires development tools and header files to be able to build the required module, if not already done you can do this by executing the following commands as root user:

```bash
yum groupinstall "Development Tools"
yum install kernel-devel kernel-headers
```

BeeGFS is a separate product from Fraunhofer and you should install it according to the official installation manual available on:

[http://www.beegfs.com/wiki/ManualInstallWalkThrough](http://www.beegfs.com/wiki/ManualInstallWalkThrough)

Depending on your expertise you can choose between a graphical or manual installation of BeeGFS

* Recommended setup for a two-node system.

  You should install the management system and meta server on only one host.

  The storage server and client on both hosts.

* Recommended setup for a 4-node system:

  You should install the management on 1 host, metadata server on two hosts, the storage server and client on all 4 hosts.

**Remember to give the users and group read/write access to the parallel file system – we recommend using /data\_parallel as a mount point for the beegfs-client.**

```bash
chown pspro:psprousers –R /data_parallel/
chmod 770 –R /data_parallel
```


# Installation on a cluster

The installation of Pre-Stack Pro on a small cluster is basically the same as the installation on workstations. The RPMs can be installed to a boot image for your cluster nodes.

If you are using a cluster batch system \(e.g. Torque\), you might want to use dynamic machine files, depending on which nodes the user allocated. In Torque, for example, a file with the hostnames of all allocated nodes is created on the used nodes. You might use that as machine file to prevent the user from running Pre-Stack Pro on nodes he has not allocated.

As default, that file is stored in /var/spool/torque/aux \(your batch system may be different\). You can now edit the configuration file /etc/gpi.conf, which belongs to the GPI daemon and set the variable NODE\_FILE\_DIR to that path \(see file /etc/gpi.conf, please note that a trailing slash is mandatory\). Now, when Pre-Stack Pro is started, the GPI daemon will try to find a file called machinefile in /var/spool/torque/aux. As there is none, it will use the only file that is present, which is \(in a default setup\) the node list of the batch system for that user.

The file /etc/gpi.conf:

NODE\_FILE\_DIR points to a directory containing one \#nodelist file \(fallback filename: machinefile\) e.g.

```bash
NODE_FILE_DIR=/var/spool/torque/aux/
```

If your cluster is installed using an imaging mechanism or some kind of cluster management software, then the installation is strongly depending on the used cluster management software.

**Important information**

The Pre-Stack Pro user used to start the Pre-Stack Pro backend server must exist on all compute nodes. In addition to that the passwords must be identical.

The project path must be a parallel file system. You can use the BeeGFS Parallel File System \([http://www.beegfs.com](http://www.beegfs.com)\), as well as any parallel file system of your choice.


### Make the infiniband connection work {#make-the-infiniband-connection-work}

In this installation guide we will use the operating system supported infiniband userspace utilities and drivers.

We assume you are familiar with yum, but will give you the exact commands for easier installation:

To install most infiniband userspace utilities, drivers and diagnostic tools please run the following commands and answer yes to allow download and installation (all nodes, as root):

| yum groupinstall “Infiniband Support” |
| --- |

Now you need to make sure that the “Open Subnet Manager” (OpenSM), the network “daemon” and the RDMA modules will be started automatically upon system boot.

Do so by executing the following commands (all nodes, as root):

| chkconfig rdma on |
| --- |

If more than 16 GB of RAM will be used for shared memory in _Pre-Stack Pro_ it is necessary to increase the number of MTT entries per segment for the Infiniband Hardware.

This can be done by issuing the following command on all nodes:

| echo &quot;options mlx4_core log_mtts_per_seg=7&quot; &gt;&gt;/etc/modprobe.d/mlx4_core.conf |
| --- |

In the following step you need to configure your Infiniband interfaces as normal network devices, to do this we can simply use a normal text editor and create the files as shown below (nano, vi, kwrite are all unix text editors which can be used, however do NOT edit the files on a windows based host, once again remember to be root).

Enter valid IP address and network information for the interface, so that your Infiniband adapers are on the same IP network

Example configuration for two nodes, for more nodes please adjusts the parameter IPADDR accordingly:

| Example configuration node #1 | Example configuration node #2 |
| --- | --- |
| File: | File: |
| DEVICE=ib0BOOTPROTO=noneTYPE=EthernetIPADDR=192.168.80.10           NETMASK=255.255.255.0ONBOOT=yes | DEVICE=ib0BOOTPROTO=noneTYPE=EthernetIPADDR=192.168.80.20           NETMASK=255.255.255.0ONBOOT=yes |

Verify that the infiniband cable is connected directly between the two nodes or in a switch if you are configuring more than two nodes.
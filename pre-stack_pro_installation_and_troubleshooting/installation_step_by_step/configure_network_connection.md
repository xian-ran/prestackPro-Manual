### Configure network connection {#configure-network-connection}

To configure the network connection the wizard system-config-network can be used, if you want to do it manually please follow the example below and edit or create the following files.

Example for network devices (eth0)

| Example configuration node #1 | Example configuration node #2 |
| --- | --- |
| File: | File:/etc/sysconfig/network-scripts/ifcfg-eth0 |
| DEVICE=ib0BOOTPROTO=noneTYPE=EthernetIPADDR=192.168.10.10GATEWAY=192.168.10.5           NETMASK=255.255.255.0DNS1=192.168.10.5 | DEVICE=ib0BOOTPROTO=noneTYPE=EthernetIPADDR=192.168.10.20GATEWAY=192.168.10.10       NETMASK=255.255.255.0DNS1=192.168.10.11 |

Important: for DELL and HP systems, depending on your current BIOS settings the devices might have a different naming scheme like: em0 or p1p1.To avoid this naming procedure you can remove the biosdevname package with the following command and then do a reboot:

| yum remove biosdevname |
| --- |
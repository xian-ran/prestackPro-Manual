### Configure network connection {#configure-network-connection}

To configure the network connection the wizard system-config-network can be used, if you want to do it manually please follow the example below and edit or create the following files.

Example for network devices \(eth0\)

Example configuration node #1 
File:/etc/sysconfig/network-scripts/ifcfg-eth0
```bash 
DEVICE=ib0
BOOTPROTO=none
TYPE=Ethernet
IPADDR=192.168.10.10
GATEWAY=192.168.10.5
NETMASK=255.255.255.0
DNS1=192.168.10.5
DNS2=8.8.8.8
USERCTL=no
IPV6INIT=no
ONBOOT=yes
``` 


Example configuration node #2
File:/etc/sysconfig/network-scripts/ifcfg-eth0
```bash 
DEVICE=ib0
BOOTPROTO=none
TYPE=Ethernet
IPADDR=192.168.10.20
GATEWAY=192.168.10.1
NETMASK=255.255.255.0
DNS1=192.168.10.11
DNS1=192.168.10.11
DNS2=8.8.8.8
USERCTL=no
IPV6INIT=no
ONBOOT=yes
``` 



Important: for DELL and HP systems, depending on your current BIOS settings the devices might have a different naming scheme like: em0 or p1p1.To avoid this naming procedure you can remove the biosdevname package with the following command and then do a reboot:

```bash
yum remove biosdevname
```



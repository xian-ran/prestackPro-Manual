### Minimum system requirements for Pre-Stack Pro {#minimum-system-requirements-for-pre-stack-pro}

In order to run Pre-Stack Pro you need at least two machines with the following minimal system specifications:

* 2 x Quad- or Six-Core CPUs (Intel or AMD) 
* at least 16 GB RAM per node 
* Double Data Rate (DDR) Infiniband interconnect from Mellanox on the backend nodes (please note that we currently only support Mellanox Infiniband hardware, e.g. Mellanox ConnectX cards); for more than two machines an additional Infiniband switch is needed 
* On the backend nodes a minimum version of OFED 1.4 as Infiniband software stack is needed 
* at least 3 hard drives per node for data, configured as RAID 0 (software RAID is sufficient) or Raid 5/6 if you have enough discs and an appropriate add-on RAID controller 
* Centos 6.X or Red Hat Enterprise Linux 6.x (or newer) is recommended; a parallel file system on all nodes (we recommend BeeGFS as parallel file system, [http://beegfs.com](http://beegfs.com)) and typically install it with Pre-Stack Pro (the software is free for use, maintenance will be charged) 
* for running the viewer (this can be done on either one of the compute nodes or on a separate machine with a network connection) 
* you need a graphics card that is capable of OpenGL hardware rendering 
* we recommend Nvidia cards
* we recommend two displays for best viewing results (the graphics card must support dual-screen) 
* we recommend full HD resolution (1920x1080) for best viewing results (the graphics card and the displays must support it) 

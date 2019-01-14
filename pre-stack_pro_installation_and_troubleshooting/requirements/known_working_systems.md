# Known Working systems

The following system configurations are currently in use with Pre-Stack Pro and should give you an idea about possible configurations:

* 2x Dell Precision T7600 workstation
  * 2x Intel Xeon E5-2670 2.6 GHz \(8core\)
  * 128 GB RAM
  * 4x 2TB hard disk \(software RAID 5\)
  * 1x 128GB SSD - operating system disc
  * NVIDIA Corporation GF108 \[Quadro 600\]
  * Mellanox Technologies MT26428 \[ConnectX VPI PCIe 2.0 5GT/s - 
  * IB QDR / 10GigE\] \(rev b0\)
* 2x HP Z820 workstations
  * 2x Intel Xeon Xeon E5-2670 2.6 GHz \(8-Core\) 
  * 64 GB RAM 
  * 4x HP 3TB SATA 7200 rpm 6Gb/s 3.5” HDD
  * 1x Operating System DISK ssd 128GB
  * Nvidia Quadro 600 1 GB Graphics
  * HP RGS Sender on node 1, HP RGS viewer on windows
* 2x /4x Dell PowerEdge R510
  * Intel Xeon X5660 \(6-Core\) 
  * 48 GB RAM
  * $$>=$$6x 2TB hard disk \(RAID 5 on Dell H700 raid controller\) 
  * Mellanox ConnectX MHGH18-XTC Infiniband card
  * Nvidia Quadro FX 3700 in remote viewer machine
* Dell Poweredge C8000 \(4 Compute, 2 Storage and 2 PSU\) 2 x PowerEdge C8220, Single Width Compute Sled
  * 2 x Intel Xeon E5-2697v2 2.7GHz, 30M Cache
  * 256 GB RAM
  * 1x 1TB SATA 2.5” 7.2RPM
  * Mellanox ConnectX-2, Mezz, Dual Port, 40Gbps QDR IB
  * Asus GT610 1GB Graphics board, low profile +bracket.

    2 x PowerEdge C8220, Single Width Compute Sled

  * 2 x Intel Xeon E5-2697v2 2.7GHz, 30M Cache
  * 256 GB RAM
  * 1x 1TB SATA 2.5” 7.2RPM
  * Mellanox ConnectX-2, Mezz, Dual Port, 40Gbps QDR IB
  * LSI9280-8e PCIe RAID Card, External, Low Profile 
  * External Cable for LSI9280-8e Controller, 1M

    2 x PowerEdge C8000XD Storage Sled

  * 12 x 3TB 7.2K RPM Near-Line SAS 6Gbps 3.5in Hard Drive

    1 x Mellanox InfiniScale IV QDR InfiniBand Switch, 8 QSFP + cables.

HP Remote Graphics Server running on 2 compute nodes. Accessible through HP RGS client on any machine on the network.

\*\* We strongly recommend Mellanox ConnectX 2/3 dual port VPI adapters QDR\(40Gbit\) or FDR\(56Gbit\)

\*\* For dual workstation systems infiniband switch is not required as the switching can be done with OpenSM running on at least one node.


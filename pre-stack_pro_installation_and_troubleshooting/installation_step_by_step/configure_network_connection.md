### Configure network connection {#configure-network-connection}

To configure the network connection the wizard system-config-network can be used, if you want to do it manually please follow the example below and edit or create the following files.

Example for network devices \(eth0\)

![](/assets/001_Pre-Stack Pro Installation.png)

Important: for DELL and HP systems, depending on your current BIOS settings the devices might have a different naming scheme like: em0 or p1p1.To avoid this naming procedure you can remove the biosdevname package with the following command and then do a reboot:

![](/assets/002_Pre-Stack Pro Installation.png)


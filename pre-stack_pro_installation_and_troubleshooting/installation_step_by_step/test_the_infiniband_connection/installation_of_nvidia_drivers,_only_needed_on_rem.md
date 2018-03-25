#### Installation of Nvidia drivers, only needed on remote viewer machine. {#installation-of-nvidia-drivers-only-needed-on-remote-viewer-machine}

Install necessary development tools to allow for compiling the modules:

![](/assets/010_Pre-Stack Pro Installation.png)

Change from graphical to console interface:

![](/assets/011_Pre-Stack Pro Installation.png)

Download the x86\_64 driver from: [http://www.nvidia.com/object/unix.html](http://www.nvidia.com/object/unix.html)  
Change working directory to where you downloaded the Nvidia Drivers.  
For instance:

/home/USERACCOUNT/Downloads/

Version number and filename might not be the same:

![](/assets/012_Pre-Stack Pro Installation.png)

Follow the instructions on the screen and let it configure xorg.conf, if it fails complaining about “nouveau” driver, please allow it to create “blacklist nouveau” in the module configuration; reboot and start over.

Please reboot to verify that the newly installed graphics drivers are working.

Use the following command to change your display settings:

![](/assets/013_Pre-Stack Pro Installation.png)


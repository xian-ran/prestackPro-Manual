#### Installation of Nvidia drivers, only needed on remote viewer machine. {#installation-of-nvidia-drivers-only-needed-on-remote-viewer-machine}

Install necessary development tools to allow for compiling the modules:

```bash
yum groupinstall "Development Tools" 
yum install kernel-devel kernel-headers
```



Change from graphical to console interface:

```bash
/sbin/init 3
```



Download the x86\_64 driver from: [http://www.nvidia.com/object/unix.html](http://www.nvidia.com/object/unix.html)  
Change working directory to where you downloaded the Nvidia Drivers.  
For instance:

/home/USERACCOUNT/Downloads/

Version number and filename might not be the same:

```bash
chmod +x NVIDIA-Linux-x86\_64-325.run
./NVIDIA-Linux-x86_64-325.15.run
```



Follow the instructions on the screen and let it configure xorg.conf, if it fails complaining about “nouveau” driver, please allow it to create “blacklist nouveau” in the module configuration; reboot and start over.

Please reboot to verify that the newly installed graphics drivers are working.

Use the following command to change your display settings:

```bash
nvidia-settings
```





### PreStackProBackendrc configuration file {#prestackprobackendrc-configuration-file}

The configuration options for the Pre-Stack Pro backend are located in the file PreStackProBackendrc, in the etc/ directory of your Pre-Stack Pro installation.

Port used by the TCP connections between all backend nodes. Also, the 12 ports following this port are used. With enabled NUMA there are additional 12 ports needed starting from this port +100 \(default 50100\)

![](/assets/033_Pre-Stack Pro Installation.png)

Umask used for files saved within the application. We recommend to set it up to 007, see section 9.3.8

![](/assets/034_Pre-Stack Pro Installation.png)

Enable or disable NUMA support.

![](/assets/035_Pre-Stack Pro Installation.png)

Enable or disable the core pinning of the worker threads

![](/assets/036_Pre-Stack Pro Installation.png)

Enable the use of ethernet instead of Infiniband for the backend communication

![](/assets/037_Pre-Stack Pro Installation.png)

License server settings, see section 9.3.7.4

![](/assets/038_Pre-Stack Pro Installation.png)

Full path of the machine file, see **Error! Reference source not found.**

![](/assets/039_Pre-Stack Pro Installation.png)  



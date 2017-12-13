### PreStackProBackendrc configuration file {#prestackprobackendrc-configuration-file}

The configuration options for the Pre-Stack Pro backend are located in the file PreStackProBackendrc, in the etc/ directory of your Pre-Stack Pro installation.

Port used by the TCP connections between all backend nodes. Also the 12 ports following this port are used. With enabled NUMA there are additional 12 ports needed starting from this port +100 (default 50100)

BackendStartingPort = 50000

Umask used for files saved within the application. We recommend to set it up to 007, see section 18.2.9

Umask = 027

Enable or disable NUMA support.

Numa = false

Enable or disable the core pinning of the worker threads

ThreadPinning = false

Enable the use of ethernet instead of Infiniband for the backend communication

UseEthernet = true

License server settings, see section 18.2.8.4

OLicenseServerName = localhost

OLicenseServerPort = 80

Full path of the machine file, see 18.2.7.3

NodeFile = THIS_HAS_TO_BE_SET
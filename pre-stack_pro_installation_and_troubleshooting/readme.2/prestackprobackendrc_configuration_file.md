# PreStackProBackendrc configuration file

The configuration options for the Pre-Stack Pro backend are located in the file PreStackProBackendrc, in the etc/ directory of your Pre-Stack Pro installation.

Port used by the TCP connections between all backend nodes. Also, the 12 ports following this port are used. With enabled NUMA there are additional 12 ports needed starting from this port +100 \(default 30100\)

```bash
BackendStartingPort = 30000
```

Umask used for files saved within the application. We recommend to set it up to 007, see section 9.3.8

```bash
Umask = 027
```

Enable or disable NUMA support.

```bash
Numa = false
```

Enable or disable the core pinning of the worker threads

```bash
ThreadPinning = false
```

Enable the use of ethernet instead of Infiniband for the backend communication

```bash
UseEthernet = true
```

License server settings, see section 9.3.7.4

```bash
OLicenseServerName = localhost
OLicenseServerPort = 80
```

Full path of the machine file, see **Error! Reference source not found.**

```bash
NodeFile = THIS_HAS_TO_BE_SET
```


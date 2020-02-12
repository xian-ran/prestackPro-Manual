# Start of the backend server

![](../../../.gitbook/assets/042_pre-stack-pro-installation.png)

If this window doesn’t get displayed automatically, go to **Startup-&gt; Start Backend server**.

The **Host name** is the name or IP address of the machine you want to use for the backend application. If the connection to a host was successful, all the settings for this host are stored and available from the menu at the next start. Each Host can only be stored one time and up to 5 connections are stored.

The **project path** is the absolute path to the Pre-Stack Pro project. It has to be on a parallel files system.

The **backend binary path** is the absolute path to the binary of the server application. It must include the name of the binary \(e.g. PreStackProBackend\).

In the **global memory size** window, you can set the size of the global memory per node. As a rule of thumb, 50% of the local memory is a good value.

The **I/O Buffer size** is a tuning parameter for the I/O in Pre-Stack Pro. This parameter is an expert one and should only be changed if you are very familiar with file systems. 2MB is a good value.

The **TCP Port** is the one used to communicate between the client and the backend. It must be unused by the system. Default is 22227.

The **SSH Port** is the SSH port of the system.

The **timeout value** specifies the communication timeout in minutes used during the application startup. If the backend doesn’t start in the given time, the startup is considered as a fail. If you experience timeouts on large cluster systems with many backend nodes, it may be necessary to increase this timeout. The more backend nodes are used, the longer the timeout needs to be.


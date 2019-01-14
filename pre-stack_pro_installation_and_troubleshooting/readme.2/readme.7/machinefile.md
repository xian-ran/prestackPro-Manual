# Machinefile

In order to run Pre-Stack Pro, GPI needs to know which machines you would like to use. This information is only necessary on the master compute node \(''node1'' is chosen as master here\).

Create a file and insert all nodes you would like to use as compute nodes, one in each line and starting with the master \(The one you will be connecting to\). In the example setup this file should look like:

```bash
node1
node2
```

The filename and location are parameters of the PreStackProBackendrc file on the master node, located in the etc/ folder of your Pre-Stack Pro installation.

Please add the lines to the file.

```bash
NodeFile=<full path and name of the file>
```

If you are using a cluster with a queuing management system, the location of the machine file can be passed using a command line option of the client:

```bash
--nodefile PATH TO NODES.
```

Also, if the queuing system passed the list of nodes via the environment variable PBS\_NODEFILE and the client knows this environment variable, you could put in PreStackProBackendrc:

```bash
NodeFile =PBS_NODEFILE
```


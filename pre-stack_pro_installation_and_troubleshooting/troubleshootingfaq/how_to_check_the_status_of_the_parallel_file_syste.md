### How to check the status of the parallel file system {#how-to-check-the-status-of-the-parallel-file-system}

To check the status of the BeeGFS parallel file system it is recommended to have the beegfs-utils package installed which will let you check network connection and remaining storage on the different nodes.

When using infiniband all storage nodes should display: RDMA when run on a Infiniband capable node \(will show TCP on clients connected via normal ethernet\)

Example output of beegfs-net:

```bash
storage_nodes
=============
dell1 [ID: 1]
Connections: RDMA: 1 (192.168.80.10:8003);
```

Example output of beegfs-df:

```bash
METADATA SERVERS:
TargetID        	Pool       Total        Free      ITotal       IFree
========        ====       =====        ====      ======       =====
       1    [normal]    5587.1GB    3052.2GB     1117.8M     1117.7M

STORAGE TARGETS:
TargetID        Pool       Total        Free      ITotal       IFree
========        ====       =====        ====      ======       =====
       1    [normal]    5587.1GB    3052.2GB     1117.8M     1117.7M
       2    [normal]    5587.1GB    3082.9GB     1117.8M     1117.8M
```



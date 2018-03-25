### How to check the status of the parallel file system {#how-to-check-the-status-of-the-parallel-file-system}

To check the status of the BeeGFS parallel file system it is recommended to have the beegfs-utils package installed which will let you check network connection and remaining storage on the different nodes.

When using infiniband all storage nodes should display: RDMA when run on a Infiniband capable node \(will show TCP on clients connected via normal ethernet\)

Example output of beegfs-net:

![](/assets/043_Pre-Stack Pro Installation.png)

Example output of beegfs-df:

![](/assets/044_Pre-Stack Pro Installation.png)


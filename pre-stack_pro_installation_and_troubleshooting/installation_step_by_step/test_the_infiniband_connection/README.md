### Test the Infiniband connection {#test-the-infiniband-connection}

Try to do a ping from one machine to the interface of the other machine.

Run the command “ibv_devinfo”; in the output the state of the ports where a cable is connected should be “ACTIVE”; if that is not the case please verify that:

*   The cable is plugged in correctly
*   The subnet manager is started on at least one node _ibv_devinfo_

Edit the file /etc/hosts and add all hosts and their respective IP addresses like the following example.

If you are using an internal DNS server this step might not be needed, if the DNS server is properly configured and reachable from all nodes.

| /etc/hosts |
| --- |
| 127.0.0.1 localhost localhost.localdomain localhost4 localhost4.localdomain4 |
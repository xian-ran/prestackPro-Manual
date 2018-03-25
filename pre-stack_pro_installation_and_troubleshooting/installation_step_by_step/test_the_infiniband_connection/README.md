### Test the Infiniband connection {#test-the-infiniband-connection}

Try to do a ping from one machine to the interface of the other machine.

Run the command “ibv\_devinfo”; in the output the state of the ports where a cable is connected should be “ACTIVE”; if that is not the case please verify that:

* The cable is plugged in correctly 
* The subnet manager is started on at least one node _ibv\_devinfo_

![](/assets/007_Pre-Stack Pro Installation.png)

Edit the file /etc/hosts and add all hosts and their respective IP addresses like the following example.

If you are using an internal DNS server this step might not be needed, if the DNS server is properly configured and reachable from all nodes.

![](/assets/008_Pre-Stack Pro Installation.png)


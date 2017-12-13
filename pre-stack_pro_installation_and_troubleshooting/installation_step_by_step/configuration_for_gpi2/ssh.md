#### SSH {#ssh}

Pre-Stack Pro now uses SSH to start the backends, meaning that a passwordless ssh connection between all nodes is required.

New: This can be easily achieved by generating an ssh key for each user and adding that key to the users &quot;authorized_keys&quot; files inside /home/&lt;user&gt;/.ssh/authorized_keys.

For a system without shared home folders, this key needs to be added to all nodes, assuming you have shared home folders the steps needed to generate an SSH key is outlined below:

Step 1 - generate an SSH key repeat this step for all users, logged in as the user:

ssh-keygen -t dsa

Don&#039;t enter a passphrase, just clik enter.

Step 2 - add the key to the authorized keys file:

cat ~/.ssh/id_dsa.pub &gt;&gt; ~.ssh/authorized_keys

Please logon to node 1 and node2 to verify that everything works. Since the option &quot;StrictHostKeyChecking&quot; is enabled by default in the system SSH client you might need to logon via SSH to each node and confirm the identity manually by entering &quot;yes&quot; OR disable it in

/etc/ssh/ssh_config

Between the client and the master node, a password protected SSH connection is needed. This is the usual settings for most network so you should be good to go there. Alternatively ssh authentication via a key-file could be used. It is currently available only as a command line option for the client:

ssh-private-key PATH TO KEY.

This needs to be setup for all users.
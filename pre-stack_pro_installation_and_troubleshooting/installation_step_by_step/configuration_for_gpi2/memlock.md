#### Memlock {#memlock}

If the Pre-Stack Pro backend finds the current memlock limit too low, it will issue a warning about this specific issue in the logs and refuses to start. To see the current value of memlock type

![](/assets/018_Pre-Stack Pro Installation.png)

You can modify it to be unlimited to avoid the problem with the following command, run as root user:

![](/assets/019_Pre-Stack Pro Installation.png)

If the user was logged on during the operation, he needs to log out and log in after the operation is completed.


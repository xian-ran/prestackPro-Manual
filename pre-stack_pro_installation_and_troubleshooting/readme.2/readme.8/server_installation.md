# Server installation

For server installation, you can choose any machine that is reachable from your master node. It has to be available during the entire duration of your Pre-Stack Pro session, so either the master node itself or a high availability system is recommended.

Download the installation package and start the setup executable, depending on your system. If you plan to install the server as a service, it is recommended to perform the installation as root. We suggest choosing the typical installation option. After completing the installation wizard, you have the option to start the server control tool directly. You can do so or change to the directory you specified as installation target and run the ServerCtrl executable manually.

**Note:** If you are running a remote ssh session on Linux, please ensure that you have X forwarding enabled. The server may not resolve the localhost name correctly, causing the startup of the server control tool to fail with the message "cannot connect to X server localhost:XX.X". In this case, please adjust the DISPLAY system variable manually. To do so, check your current setting with

```bash
echo $DISPLAY
```

which should return something like 'localhost:XX.X'. Now, please modify the setting by using

```bash
export DISPLAY=127.0.0.1:XX.X
```

replacing localhost with 127.0.0.1.

In the control tool, several initialization adjustments like the server's listening port can be adapted on the Server-INI-File tab. For more detailed information on these settings, please refer to the server manual provided in the installation package.

You have the options to start the server directly from the tool, meaning that the server will be stopped as soon as the control tool is closed. The second option \(recommended\) is to install the server as a service and have it run automatically on system startup. To do so will require root privileges.

After starting the server directly or as service, you should see a green message telling you that the server is now running.


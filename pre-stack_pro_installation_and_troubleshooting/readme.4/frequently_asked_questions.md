# Frequently Asked Questions

**Q: The startup of Pre-Stack Pro fails with the following error message: “Startup error – NodeFile not set in PreStackProBackendrc”**

A: There is a missing information in the configuration file PreStackProBackendrc, see section **Error! Reference source not found.**

**Q: The startup of Pre-Stack Pro fails with the following error message: “GPI Initialization failed”**  A: There are several reasons for this error message. The most common one will be that the memlock limit is too low. See section **Error! Reference source not found.** to resolve this problem.

**Q: The startup of Pre-Stack Pro fails with the following error message: “Starting of server failed”**

A: The following steps should be performed:

* Please make sure that you provided the right backend binary path in the startup dialog, see section [start the client](../../getting_started/start_of_pre-stack_pro.md). 
* If the backend binary path exists you can try to start that file manually from a shell to see if errors occur, that might help to find a solution.

**Q: At startup, the step “TCP/IP connection to XXX” is taking a long time and eventually failed**

A: Verify the TCP port is the correct one.

**Q: When creating a project, the error ''No read access for the selected file - Machine XXX - Cannot see the file'' occurs.**

A: Please make sure that you are using a parallel file system as project path.


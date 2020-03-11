# Manage Facies \(LFC\)

Facies or Lithology Fluid Classes \(LFC\) can be created from [Well Log Viewer](../viewers/readme.12/well_log_viewer_gui.md) Zone tab context menu or created within the Manage Facies utility.

Litho-facies can be defined from a series of $$V_p$$ \($$m/s$$\), $$V_s$$ \($$m/s$$\) and $$\rho$$ \($$g /cm^3$$\) data points that can be generated from well logs and Well Zones. After data points are defined, the Manage Facies tool fits a 3D Gaussian distribution to the points.

![](../.gitbook/assets/image%20%2851%29.png)

**Creating LFC from Zone:** To create a new litho-facies, click on the “Create New” button and select Gaussian LFC. Give the class a name and color, then click the “Load from File” button. This brings up a well selection box where all wells where current well zone is defined are listed. On clicking OK, a Gaussian fit is calculated and statistical values describing the Gaussian are updated left in the main Manage Facies window. Number of samples from the zone in the different wells are given in table  
Clicking the **Apply** button saves the information into the project.

**Tips & Tricks:**  
By clicking "Fill From Zone" user can check which zone, wells and logs were used to generate data points.  
Adding a "New Gaussian LFC" will copy current litho-facies Gaussian Statistics to a new litho-facies.  
Gaussian statistics may also be edited by hand and user can re-calculate statistics from table.  

The **Krief sand model** is a theoretical alternative to using a Gaussian fit to well data. It describes the distributions of porosity and shale content by beta distributions, and finds distributions of elastic properties of a mixture of sand, clay and fluid according to the Krief model \(Krief et al, 1990, The Log Analyst\). The output from the module is a Krief sand for each of the fluids defined in the fluid box. Mineral and fluid properties \(bulk modulus, shear modulus, density, and saturation as appropriate\) are defined by using the buttons with three dots, and new fluids and minerals may be added with the plus button. The a and b parameters are the beta distribution parameters used to describe each of the physical properties.


## Manage Facies {#manage-facies}

Manage Facies allows import and editing of litho-facies for use in PCube Inversion. For each litho-facies, a 3-column ascii file containing $$V_p$$ \($$m/s$$\), $$V_s$$ \($$m/s$$\) and $$\rho$$ \($$g /cm^3$$\) \(with no file header\) is required. After points are loaded, the Manage Facies tool fits a 3D Gaussian distribution to the imported points.

To load a new litho-facies, click on the “Create New” button and select Gaussian LFC. Give the class a name, then click the “Load from File” button. This brings up a file selection box where the ascii file can be selected. On clicking Open, it is read and the Gaussian fit is performed. The statistical values describing the Gaussian are updated in the main Manage Facies window. They may also be edited by hand. Clicking the Apply button saves the information into the project.

![](/assets/003_Utilities and Setting.png)

The Krief sand model is a theoretical alternative to using a Gaussian fit to well data. It describes the distributions of porosity and shale content by beta distributions, and finds distributions of elastic properties of a mixture of sand, clay and fluid according to the Krief model \(Krief et al, 1990, The Log Analyst\). The output from the module is a Krief sand for each of the fluids defined in the fluid box. Mineral and fluid properties \(bulk modulus, shear modulus, density, and saturation as appropriate\) are defined by using the buttons with three dots, and new fluids and minerals may be added with the plus button. The a and b parameters are the beta distribution parameters used to describe each of the physical properties.

![](/assets/004_Utilities and Setting.png)


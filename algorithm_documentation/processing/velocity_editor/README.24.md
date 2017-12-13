### Velocity Editor {#velocity-editor}

This tool gives the user the ability to manually edit the stacking velocity field. The user can correct for wrong trends (multiple event picks, phase IIp events), perform local updates or simply QC their velocity field.

The workflow is:

*   Create a new object called Velocity Functions from an ASCII file or a velocity volume
*   Use the Velocity Editor to QC and manually modify if necessary the velocity functions
*   Export the edited functions as a velocity volume
*   This volume can be used with NMO, offset to angle and exported as SEGY.
*   Go to: **Processing** → **Velocity Editor**
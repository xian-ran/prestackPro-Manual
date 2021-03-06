# Comparing data

**2D viewers** inside the data comparator \(section 4\) have the same general behavior as those outside. A description of their axis and histogram setup is to be found in [Functionalities common to all viewers](../functionalities_common_to_all_viewers/).

However, a right mouse click inside a viewer will give you these additional options. It is possible to disable the Read-out plot. Attribute extraction is discussed in the following section.

![](../../.gitbook/assets/009_data_comparator.png)

_Context menu_

By default, all viewers displayed in the same Data Comparator are **synchronized**. Axis synchronization is done with respect to the unit types \(e.g. offset, angle, time, depth …\) and histograms are synchronized with respect to the domain \(e.g. seismic, velocities …\). If you want to use **independent histograms** for each viewer, un-tick the synchronization option in the Control panel.

![](../../.gitbook/assets/010_data_comparator.png)

_Windows with different axis units and independent histograms_

The Data panel lists the volumes open in the comparator. You can show/hide a panel by toggling on/off the blue eye icon next to the volume name. When doing a right mouse click on one of the volumes you have the option to remove completely the data from the comparator and to set the width of the associated panel. Alternatively you can change the width of each panel by grabbing the boundary between two panels with the mouse cursor.

The Control panel contains the Horizons and Wells item field. You can show/hide them by toggling on/off the eye. In the upper part you can choose to display stacked data either in the IL or XL direction and to flip the display direction. Automatic synchronization of the Histograms and Wiggle Settings can be disabled by un-ticking the options.

The Display mode panel gives you the option to use wiggle plots. Select the volume of interest in the Preview tab and choose to display only wiggles or wiggles as an overlay on the pixmap. Wiggle settings are synchronized for all viewers, but can be defined independently, if you deselect the synchronization option in the Control panel.

![](../../.gitbook/assets/011_data_comparator.png)

_Overlaid wiggle plot on seismic density_


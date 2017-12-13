### Display data as Wiggle plot {#display-data-as-wiggle-plot}

Any dataset can be displayed as a wiggle plot inside the viewer. To do so, right-click on a dataset in the upper data selection window and choose:

**Display mode** → **Show only Wiggle plot.**

Toggle a volume to Wiggle plot display

It is possible to display Wiggle plot overlay on top of color density mode by choosing **Show Wiggle Plot over Pixmap.**

The display settings of volumes showed as wiggle plot are available by clicking the relevant tab (1).

**Reference value**: the amplitude value for which the width of the amplitude curve will be 1\. The 4 buttons allow easy setup: 3*Std Dev is often good for seismic, Abs Max for synthetic seismic.

**Clip distance:** value relative to the distance between currently displayed wiggles. A value of 1 means clip starts at the next displayed wiggle, 2 means overlap at the next wiggle and clip after that.

**Decimate:** a value of 1 means show all wiggles, 2 show only 1 out of 2, etc …

**Oversampling:** an anti-aliasing parameters to smooth the display of the wiggle plot. Value of 3 should be good for most data having a 4 ms sample interval. Data with higher sampling rate might need an increase of this parameter.

1

Display parameters for wiggle plots

Several of those parameters can be put as a user default value in the Settings dialog. Go to **Settings** → **Settings**.
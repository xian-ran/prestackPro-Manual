# Settings {#settings}

General program settings are set via **Settings** → **Settings.**

Here is a list of all options:

**General** tab:

*   Use double buffering in workflows: If enabled, additional buffers will be inserted automatically into the workflows around Load/Save algorithms. This (can) improve parallel performance (since more IO and processing can be done in parallel), but also increases the amount of needed memory. Depending on the selected workflow, this option will either speed up or slow down execution. Effects should be tested.
*   Use AVX optimized code if available: Pre-Stack Pro detects, whether the CPU on the backend side have the AVX instruction set. If that is the case, it will use AVX-optimized versions of the algorithms (currently there is only an AVX-optimized version for Radon and Inverse Radon). This brings a speedup of around 20 to 25 percent. If the checkbox is disabled, Pre-Stack Pro will not use the AVX-optimized implementations, even if AVX has been detected.
*   Show Polygon Selection/Arbitrary Path/Mute Editing help: controls whether the keyboard+mouse tool tips are displayed when selecting the relevant feature.
*   Widget Style: define the style of widget use.
*   Hide filtered volumes in the volume selection dialogs: the volume selection highlights volume matching the pattern typed. When this is on, it will also hides the volumes which do not match the pattern
*   Session management: the two options give you the possibility to auto-save a session every 5 minutes and to restore the latest auto-saved session when opening a project

**2D Viewer** tab:

*   Wellpath visible distance in Stack and Gather: maximum distance (in number of traces) from a wellpath to the current section. Wellpath intervals which lie at a great distance than this setting are not projected and displayed on the section.
*   Wellpath intersection draw size in 2D Viewer: diameter of the circle representing the intersection of the wellpath with the displayed object (Volume, Horizon, Map).
*   Polygons: size of the polygon control nodes for normal and edit mode
*   Crosshairs in all 2D Viewer: color of the crosshair
*   CDP Positions in map viewer: color of the symbols representing CDP position in the Map Viewer

**Colors and Histograms** tab:

This tab is for the setup of the color table for each possible domain, as well as the default marker distribution in the Histogram.

**Wiggle plot** tab:

Default fill color and parameters for wiggle plot, as well as the default reference value.

**Crossplot** tab:

*   Max number of scatter points: if the crossplot contains more than that number of points, it will not display as scatter even when this mode is selected.
*   Scatter point size: size of the point
*   Enable scatter plots by default: this will turn scatter plot as the default mode
*   Show scatter data only for the current volume: only the selected crossplot will be displayed as a scatter set
*   Use bitmap as scatter points to improve performance: this will reduce the precision of the display.
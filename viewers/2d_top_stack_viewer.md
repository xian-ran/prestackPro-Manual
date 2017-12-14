## 2D Top Stack Viewer {#2d-top-stack-viewer}

The version 3.6.0 introduces a new viewer called the Top Stack Viewer. It is the equivalent of the Stack viewer for horizontal slices as well as the display of attribute maps created from the Create Map process. You can display either single fold Map/slices as well as a constant offset/angle plane of multi-fold Map/slices.

The aim of that viewer is to allow quick comparisons between datasets. It shares several functionalities with the Map Viewer but also removes some of its limitations, while having its own. The table below compares the two viewers.

| **Map Viewer** | 2D Top Stack Viewer |
| :--- | :--- |
| Allows on/off transparency overlay only  --&gt; Can see overlay data inside   | Allows variable transparency overlay --&gt; Cannot see overlay data inside  |
| Can set display ranges for every volume, including masks displayed as volumes. | Can only set display ranges for masks to give a single color overlay. |
| Have to set display Z and X or angle for each volume independently --&gt; Very flexible display but quickly becomes too complex to manage easily with &gt; 3 volumes  | Can set display Z and X or angle globally for all volumes and masks. --&gt; Easier to combine, visualise and manipulate &gt; 3 volumes |
| Horizontal scale set by real world X and Y’s and may not match side views. | Horizontal scale set by inline & crossline and can always be matched by side views. |
| Possible to pick arbitrary lines, polygon selections | Not possible to pick arbitrary lines or polygon selections |

The functionalities of this viewer are similar to the one described in the gather viewer. All maps of the same geometry will show in the same viewer and the angle/offset selection is propagated to all maps.![](/assets/001_top_stack_viewer.png)


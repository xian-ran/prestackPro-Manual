#### Users tips {#users-tips}

**QC tips:**

Two optional QC attributes may be calculated when the snap or track option is used. **“Snapped horizon”** creates a new output horizon at the snapped or tracked position. **“Distance to snapped horizon”** outputs the difference between input and snapped time at every trace.

Note that time differences from the “**Distance to snapped horizon”** map, (tracking option), can have larger values than the time less/time greater limits specified. This occurs because the time range settings are only used to constrain the location of the “seed” pick on initial near traces, and do not limit the maximum allowable time shift out to the fars.

Input and snapped outputs can be displayed together in the 2D Gather Viewer, and provide a quick QC on one or several lines of gathers.

![](/assets/005horizonsnap_shortwindow.png)

2D gather viewer, with original &amp; snapped horizons displayed

**Parameter Selection Tips:**

If gather events are reasonably aligned, and only have “jitter” around the stack time, then **Snap** with subsample accuracy should work fine. Use the &lt;Edit algorithm parameter&gt; option (MB3 menu) to recalculate any attribute horizon with a different reference time or window time range. If type 2 AVO reversals occur on your gathers try **Snap** to **max absolute,** with a small snap window, to keep the reference time close to the initial time position of the input horizon.

**Distance to snapped horizon** may be viewed in the new 2D Map Viewer or 2D Pre-Stack Map Viewer (below). Map displays can often help to identify local areas where unexpected or unwanted results were obtained. Snap “distance” displays combined with instantaneous amplitude displays, can often identify apparent polarity reversals or other indications of inaccurate snapping results.

![](/assets/distance.png)

“Distance to Horizon” output (calculated at 2075m offset) for &quot;tracked&quot; and &quot;snapped&quot; options. Maximum timeshift is larger for the tracked case.
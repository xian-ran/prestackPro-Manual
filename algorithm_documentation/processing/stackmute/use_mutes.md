#### Use mutes {#use-mutes}

A stack is calculated by averaging several common depth point offset traces into a single trace.

Inner and outer mutes are applied to restrict the stacking to a limited offset range. In Pre-Stack Pro it is possible to set time variant and spatially variant inner and outer mutes.
<br />
![](/assets/005_Processing.PNG)
_Customized stack with left and right mute_

To generate a single set of time variant inner and outer mutes:

* -Position the cursor and press Ctrl+left mouse button in the **Input Gather** field to set a right mute. Mute locations are recorded for each mouse click. To set a left mute, press Shift+left mouse button.
* -Set as many mute points as required
* -All data right of a right mute and all data left of a left mute will be ignored in the stacking. 
* -Mutes may be adjusted by pressing the left mouse button and dragging any existing mute (blue or green circle). You can also precisely type in the Offset or time value by clicking on the right mouse button on a control point and choose Edit Position
* -To delete a mute, move the cursor above and press right mouse button, then select Remove Control Point.

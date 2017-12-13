#### Sequence editing {#sequence-editing}

There are several ways to edit the sequence of algorithms:

*   The order can be changed
*   Algorithms or whole portions of the workflow can be removed
*   Algorithm can be added

**Change the order of algorithms:** The order of algorithms can be changed by simply dragging output volumes in the workﬂow GUI onto another input volume of any algorithm.

**Delete an algorithm :** The following options are available from the context menu of an algorithm in the workflow window:

*   **Remove this algorithm:** this option removes the process from the processing sequence. If the following steps were using the output of the removed algorithm, they will now use its input. Not all the algorithms can be removed e.g. Data selection or any algorithms with multiple input and/or output volumes.
*   **Cut workﬂow here**: this option removes everything from the workﬂow starting with the respective algorithm and everything which followed it. I.e. doing this on the ﬁrst algorithm in a workﬂow will result in an empty workﬂow.

**Duplicating Algorithms:**

There are different ways to add algorithms to workflows, each having a different goal.

The first way is from the context menu of an algorithm inside a workflow. There are two entries:

*   Add duplicate of this algorithm: this will add the algorithm with the same input and a new output volume
*   Add duplicate of this algorithm and all derived volumes: this will add the algorithm with the same input and all subsequent steps in the flow.

Those two are used to modify the workflow to create variations of the same algorithm.

**Practical example**

The following workflow performs a time alignment of the gathers. As the time alignment process is fairly sensitive to noise, a random noise attenuation process is applied first.

If the user wants to test the sensitivity of the Align2 process to the strength of the random noise attenuation, he can simply duplicate the 2D ECED filter as well as all derived volumes.

Once this is done, there are two branches in the workflow. The user has to edit the parameters for one of the 2D ECED filter, for example with a stronger filter. The two Align2 results will show the impact of random noise attenuation strength.

**Adding new algorithms:**

To add new algorithms the user has to drag and drop the algorithm from the Data Pool or another workflow window into the workflow to edit. The algorithm must be dropped in a free, white patch of the workflow manager.

At drop, a menu with three choices pops-up:

*   Add volume to workflow: add all steps necessary to create the volume
*   Add algorithm to workflow: add this algorithm in the flow, the input and output will need to be connected
*   Add algorithm and all derived volumes to workflow: as described by the name, the input will need to be connected

**Practical example:**

The workflow below performs

*   Linear noise attenuation with a Radon mute, with an AGC wrap around
*   EPS 3D, i.e. dip-steered random noise attenuation
*   Spectral balancing

The user wants to modify the workflow to insert the algorithm 2D ECED before EPS 3D and after the second Gain Filter. To do that, it is necessary to have a volume output of 2D ECED in the Data Pool. The input does not matter. This volume should be drag and dropped from the Data Pool into the workflow window. The user needs to choose **Add Algorithm to Workflow.**

The algorithm ECED will be added. The input volume and output volume will be independent from the existing flow and needs to be connected.

By simply dragging the input volume (output of Gain filter) over the input of 2D ECED the user will connect the input. Then by dragging the output of 2D ECED on to the input volume of EPS 3D the output is connected. The workflow is now correctly modified and ready to use.
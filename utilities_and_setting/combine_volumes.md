## Combine Volumes {#combine-volumes}

The Combine Volumes tool merges the probability volumes output from the PCube inversion, to help visualize the most likely facies at each sample location. The input is the probability cubes and the output is a probability cube containing the most \(or least\) likely probability at each sample. A set of mask volumes may be created as an option. One mask volume is created per facies, with samples set to 1 if that facies is the most likely. If Select Siblings is ticked on, all associated probability volumes will be loaded in one step. The optional mask volumes are output if Generate mask volumes is on.

![](/assets/061_Workflow.png)

The mask volumes can be used to visualize the most likely facies. Put them into a stack viewer and select all of them for viewing. They appear in the list of Masks. Select Inverse Range, and adjust transparency according to need. The mask colours may be changed by clicking on the coloured line in the Masks panel. Any stack volume with the same geometry may be displayed as an underlay.

![](/assets/062_Workflow.png)


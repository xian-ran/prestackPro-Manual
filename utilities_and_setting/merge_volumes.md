## Merge Volumes {#merge-volumes}

**Utilities** → **Merge volumes**

The algorithm merges two volumes of different sizes together. It will allow cutting a volume in two pieces \(spatially, at a constant time or using a Horizon with sculpt\) and applying a different process on each part. After that Merge Volumes should be used to reconstruct the full volume.

The algorithm can be used in workflows and then the output of the algorithm must be saved to disk in the project. In the workflow manager, it can be invoked via a mouse right button click after selecting two volumes.

![](/assets/056_Workflow.png)
_Merge Volumes dialog_

**Method:**

* Weighted Sum will apply a constant weight to each volume before summing them. The user defines the weight for volume 1. The sum of the weights for volume 1 and volume 2 equals to one. 
* Ramped Sum: a weight will be applied on each volume before summation. This weight will vary linearly between 0 and 1 based on a start and end time defined by the user. This is the recommended option for volumes cut in time or depth.
* Random (Trace) and Random (Gather): Those options will work only for volumes cut spatially. In the overlap area of the two input volumes, a random trace or gather is retained. 


**Output as:** The output can be a volume in memory or a file in the project.


## Overview {#overview}

![](/assets/002_Workflow.png)  
_Overview of a workflow in Pre-Stack Pro_

The **first section** of the window has 5 icons and they are used to:

1- ![](/assets/003_Workflow.png) [Save](/workflow/creation_and_editing_of_a_workflow/save_a_workflow.md): this option will save the current workflow  
2- ![](/assets/004_Workflow.png) Put in Data Comparator: once a workflow has run, this button will put all volumes into one Data Comparator.  
3- ![](/assets/005_Workflow.png) [Queue](/workflow/execute_and_queue_workflows/README.3.md): this option will allow the creation of a list of workflows to run in sequence.  
4- ![](/assets/006_Workflow.png) Run on multiples files: option specific to 2D survey workflow runs.  
5- ![](/assets/007_Workflow.png) [Discard volumes, make workflow editable again](/workflow/creation_and_editing_of_a_workflow/editing_of_a_workflow/make_a_workflow_editable.md): once the workflow has been replayed, this option can be selected to discard the volumes created, without closing the workflow and enable editing of the workflow.

The **second section** contains the workflow comments. This is a free text field editable by any user. These comments appear in the workflow preview.

The **third section** contains the workflow sequence.

The color code of the different elements in this window is similar to the one in the [Data Pool](/getting_started/appearance/data_pool.md).

Blue= seismic, Yellow= velocity, Purple= horizon, Orange = SRMS, Green = Q, and Red = Eta data.

Most workflows start with a data selection. The project data on disk during this workflow are represented by a light blue cylinder

![](/assets/008_Workflow.png)  
_Data on disk_

Each line of the workflow corresponds to a single process. The left most column is the input. The orange arrow is the processing applied to the input and the right most column is the output.

![](/assets/009_Workflow.png)

![](/assets/010_Workflow.png)

If the mouse is held over an algorithm arrow inside a workflow, all other steps are illuminated to help the user understand the flow.

![](/assets/011_Workflow.png)

![](/assets/012_Workflow.png)
_In this example the mouse was held over the first Offset to Angle arrow_

In **Section four** information about the **workflow memory** can be found. This information is displayed in several different ways:

* A fill up bar indicates quantitatively the workflow memory used (blue bar) and compares it to the memory available per node.
* A numeral value of the workflow memory used per node.
* A color code: 
* if the LED is green, the system has currently enough memory to process the entire workflow without disk outputs. It means that all volumes created by the workflow will held in memory
* if the LED is orange, there is not enough memory available to hold all volumes created by the workflow. The volumes will be divided into pieces and each piece processed independently. The workflow manager takes care of overlap for 3D filters. As the memory is too small to hold volumes, no volumes will be saved. **For each volume the user wants to keep, a Save Volume step must be added.** If there is no save volume step, the workflow will give a warning.


In this section the workflow can also be **executed**. The workflow will start from the first process which was edited. 

The close button is used to **close** the workflow window and if the user wishes, to move the workflow volumes into the data-pool. 


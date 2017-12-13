### Loading a workflow {#loading-a-workflow}

To load a workflow (no preview), go to:

**Workflow** → **Load Workflow**

Go to the location where the workflow (.wml) file resides, select it and press **Open**.

Workflow selection

The workflow window will open with a view of the workflow, all volumes unpopulated. This shows the sequence and gives a hint about the types of volumes expected for input.

Algorithms which are not ready will be highlighted and the reason given in a tooltip. Most workflows have **Select Data** for their first step, thus the **Select Data** dialog opens, and the default selection is the one made when last saving the workflow. This data select can be modified: selection of another volume or a new Inline, Crossline definition. The workflow will then run on thisthe selected data.

Select data to be used by the workflow

If data is saved during the workflow, the following window will pop up:

Save volume to project during workflow

The output file name can be updated in this window. If it already exists on disk, the following message will appear:

Warning message: save volume in workflow

It will be overwritten by pressing **Yes**. You can press the NO button and rename the output. The save process can also be skipped by pressing the skip button at the bottom of the save volume window.

The workflow will then be displayed in Pre-Stack Pro. The name of the workflow will be available on the top of the workflow window.

As described earlier, this workflow can be [edited](..\creation_and_editing_of_a_workflow\editing_of_a_workflow\README.md) and [saved](..\creation_and_editing_of_a_workflow\save_a_workflow.md).

Workflow loaded
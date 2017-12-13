#### Saving a volume {#saving-a-volume}

To save any of the volumes inside a workflow, you need to add the algorithm **Save to project** before executing the workflow. After a workflow is executed, volumes cannot be saved from the workflow, only from the Data Pool assuming the workflow ran in memory (green light, see 14.1 ).

The context menu of any output volume contains an entry **Append “Save this volume” to the workflow.** Choose this and give a name to the output volume, as well as reducing the selected range if necessary. Once the workflow is executed, the chosen volumes are saved.

The context menu of output volumes has an entry to add a save step
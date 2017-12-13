### Queue {#queue}

The queue option allows users to create a list of workflows to be executed. Once the queue is set up, all the workflows can be run in sequence.

This can be used:

- To run the same workﬂow on diﬀerent input volumes,

- To run the same workﬂow, but with varying parameters, on the same input volumes,

- To run multiple independent workﬂows one after the other.

This option is available on the top section of the workflow window:

Queue option

Workflow queue

After a workﬂow has been executed in the queue, it will close automatically and the volumes created are discarded. So make sure all queued workflows save their resulting volumes in a file.

If the workflow you want to queue doesn’t have a “save” step, the following message will appear:

Save volume warning message.

We recommend to press the cancel button. Go back to the workflow and add a save option at the last step to save your final output volume.

Right click on the final volume and select “append save this volume to workflow.

Append “save this volume” before submitting this workflow to a queue

This workflow can then be queued. The final output volume will be saved.
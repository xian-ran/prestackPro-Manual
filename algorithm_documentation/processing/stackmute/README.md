### Stack|Mute {#stack-mute}

Pre-Stack Pro’s tool to perform the transition from pre-stack to post-stack is the **Stack|Mute** algorithm. In addition, it can apply a mute without stacking.

Go to: **Processing** → **Stack | Mute function**

The **Stack | Mute** window will open. It is composed of two parts:
<br />

![](/assets/004_Processing.PNG)
_Default Stack|Mute dialog_
<br />


**Part1, algorithm specific parameters:**

**Use Project Mute:** this tick box should be checked when the user wants to use a Mute object saved in the project instead of using the mute as a parameter of Stack|Mute.

**Output Selection**

In this section you can select the desired output of the process. You can select multiple outputs: 

* **-Stacked data:** produces a stack using the user defined mutes.
* **-Muted Gathers:** applies the user defined mutes to the pre-stack data but does not stack the data
* **-Stack Coherence (QC):** used for QC, it calculates the coherence distribution


**Stack| Mute mode interactive Stacking:**

This option is only available in edit mode and allows to use this algorithm interactively. Any changes of parameter will immediately update the data. 

**Part 2, Previews:**

The **Input Gather **field on the left displays the gather corresponding to the inline - crossline pair shown in the **Input Volume** box.

The **Output Stack** field displays the stack section calculated with the settings made in the parameter section. It is centered at the location of the **Input Gather**.

The **Output Stack QC** is showing the coherence section calculated with the settings made in the parameter section. It is centered at the location of the **Input Gather**.

For more details on the parts, please refer to [overview of the process window](/algorithm_documentation/overview_of_the_process_window/README.md).
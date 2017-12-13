## Create Pseudo Pre-Stack {#create-pseudo-pre-stack}

**Utilities** → **Create Pseudo Pre-Stack**

This utilitie will concatenate any stack volumes into one volume of pseudo-gather. This could be used to make a N-fold gather of N partial stacks, or concatenate P-Cube probability cubes.

![https://lh5.googleusercontent.com/Joht9HYW1Zx46DZbcpnNOPJC0TldMlMjIji_x_MRRQ4Tqd78-bnfHvhQ4adijn84dATZNwpytnAAJ0k2EuHwx2B-ENtQ51OXnRkgIFPLsQMfCQ5dJxLkHIxwBfODYN4wog](C:\Temp\Gitbook3\export\assets\httpslh5googleusercontentcomj.png)

Create Pseudo Pre-stack dialog

**Input Selection:** the Bin value is taken from the data if it exists. If not, a value of 1 is assigned. This field can be edited if necessary. All volumes must have a different bin value. The output volume will be sorted in the bin axis according to those values.

**Add Volumes:** the widget allows for selecting multiple volumes.

**Gather domain:** choose the domain for the output fold (angles, offset, …)

**Content domain:** choose the domain for the output volume (Seismic Amplitude, Velocity, …)
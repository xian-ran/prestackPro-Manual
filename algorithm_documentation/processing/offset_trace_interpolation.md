### Offset Trace Interpolation {#offset-trace-interpolation}

Go to **Processing** → **Offset Trace Interpolation**

The input must be a pre-stack volume. The algorithm is used to perform a regular interpolation of traces in the fold direction.

The algorithm is supported in workflows.

![](/assets/092_Processing.png)
_Offset Trace interpolation dialog_

Only the Fx interpolation method is implemented.

**Resampling factor:** factor for interpolation. If the offset spacing of the input data is 100m, a factor of 2 will output traces with 50m spacing. Values > 3 lead to unstable results. Data should be NMO corrected.

**Operator Length:** length in traces of the prediction operator.

**Time Window size:** split the traces into vertical windows of this size, given in samples. 

**Time window overlap size:** overlap in samples of the time window. A value of 25% to 50% of the window size is recommended.


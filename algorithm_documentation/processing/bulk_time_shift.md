### Bulk Time Shift {#bulk-time-shift}

To open the algorithm, please go to **Processing** → **Bulk Time Shift**

![](/assets/093_Processing.png)
_Bulk Time Shift dialog_


The algorithm will apply either a constant time shift or a map of time shifts to the input volume. A positive time shift value means that traces go down, a negative one traces go up. We recommend to use Sinc interpolation for seismic or oscillatory volumes and linear for attributes with a strong low frequency component such as velocity. The extrapolation will either fill with 0 values or extend the first/last samples. 


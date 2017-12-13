### Time Depth Conversion, Seismic and Horizon {#time-depth-conversion-seismic-and-horizon}

Time-depth conversion is possible within Pre-Stack Pro for Seismic and Horizon. Go to Processing → Seismic/Horizon Time Depth Conversion

HorizonTime depth conversion window

**The selection and if needed the conversion of the velocity data can be done by selecting the yellow icon on the right part of Input Interval velocity**

The method used is a vertical stretch between time and depth domain under the assumption of a plane layered subsurface. The mapping between vertical two-way time t and z reads:

Where velocities v<sub>i</sub> are interval velocities in time.

For conversion from time to depth, the output sampling &quot;from depth&quot;, &quot;step&quot;, and alternatively either &quot;to depth&quot; or &quot;number of steps&quot; needs to be specified via the GUI. Sinc-interpolation is used to pick amplitudes from the time domain data for a given output depth sample.

The GUI automatically detects the domain of the input data and provides fields for specifying the sampling in the output domain.

Velocity input must be for both directions, time to depth and depth to time, interval velocities in time domain starting from zero seconds.

The velocity conversion utility may be used to convert any other velocity field to interval velocity. [Velocity](..\..\select_data\select_velocity.md)

**Tips**: If the geometry is created using the “create user-defined velocity”, the Seismic Volume Info tab is very useful since it contain all the seismic geometry information

Velocity selection and conversion

The result of the depth conversion will be available in the data pool. No specific color coding is available but a filtering option is possible at the bottom right part of the data Pool. Please refer in the [Data Pool](..\..\getting_started\appearance\data_pool.md) part of this manual
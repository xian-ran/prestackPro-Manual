### Gaining {#gaining}

Pre-Stack Pro allows for different types of amplitude gaining: time dependent gaining, automatic gain control, geometrical spreading correction or user-defined gain.

To apply gaining go to:

**Processing** → **Gaining**

This window is made of 3 parts:

Overview of the gain window

In the **first part** of the window, the input selection can be done. The volume must be a **seismic in time** domain.

In **the second part** of the window, **the gain filter** can be selected on the left part. Under the **parameters** of this filter can be selected.

**1-Time dependent gaining** can be applied, either with a **T<sup>x</sup>** (time as basis and x as exponent), or a **e<sup>Tx</sup>** (basis Euler&#039;s number and Tx as exponent) scaling factor.

**Time-dependent Scaling y<sup>x</sup>:** The simple time-dependent scaling uses a user defined exponent x to scale the input data depending on the current time (defined by y). A constant scaling can be set from a certain time.

**Time-dependent Scaling e<sup>yx</sup>:** The time-dependent scaling using the exp function uses the same parameters as the simple time-dependent scaling. The values are scaled using the exp function of current time (y) multiplied with the given scalar (x).

**The associated parameters:**

**The parameter x** defines the exponent for both time-dependent scaling methods (y<sup>x</sup> and e<sup>yx</sup>)

To limit the scaling effect with increasing time, a **constant scaling value** can be setfrom the defined time.

For time dependent gain filters only the **3<sup>rd</sup> part** of the window shows the actual value of the scaling factor in relation to the time.

**2-Time-dependent scaling (User Defined):** This option allows the user to define its own time variable gain filter. When the option is ticked on, a table appears for the user to fill in with time and gain in dB units. In-between values are computed with a linear interpolation.

Table for time-gain pairs

**3-Automatic Gain Control:** The aim ofthis gain filteris to adjust the gain of the signal to a constant RMS (root mean square) level.

The given input seismic is scaled by calculating the RMS value at every time step of the signal trace and applying a scalar to make all these RMS levels constant.

It is not recommended to use a short time window length eg: less than 0.5 seconds (half-width greater than 0.25 seconds) because the seismic data event amplitudes become too similar for some processing.

Checking **&#039;Create RMS Output for iAGC&#039;** will output a second volume with the RMS values that were used for scaling to be able to remove the scaling later. Typically, AGC is used before Radon is applied.

Individual trace (bottom) and the corresponding RMS value taken over a 0.6 seconds moving window (shaded area).

When velocity information is available, this option allows for an automatic correction resulting from geometrical spreading.

**4-Inverse Automatic Gain Control (iAGC):**

This filter is used to remove a previous AGC from an input volume. Therefore, **RMS values** used in the AGC calculation are required. The RMS values can be selected on the Filtering parameter part of the window.

Typically, AGC is removed after Radon was applied.

**5-Geometrical Spreading Correction (GSC):**

Geometrical spreading correction compensates the weakening of amplitude due to the opening of the ray tubes.

For locally plane-layered subsurfaces, according to the assumption of the validity of time processing, approximations for the spreading coefficient in dependence on offset and time exist.

Pre-Stack Pro uses Ursins approximation to the exact geometrical spreading.

For GSC a **velocity model** with the same inline/crossline/time dimensions as the seismic volume is required.

The approximation by Ursin (1990) is used as an approximation to the exact geometrical spreading _L_.

Each amplitude _S_ of the NMO-corrected gather _S_(_t_<sub>0</sub>,_x_) is multiplied by _L_(_t_<sub>0</sub>,_x_), where _t_<sub>0</sub> denotes _t_-zero time and _x_ offset.

If the gather is kinematically uncorrected the multiplication is applied with
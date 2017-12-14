### Generate Synthetic Gather {#generate-synthetic-gather}

**Introduction :**

This application creates a single offset or angle gather at the well, from input Vp, Vs and Density (Rho) logs and a project wavelet. The angle gathers are calculated using just horizontal AVA amplitudes but the offset gathers are ray traced from the surface. Therefore the &lt;Overburden Definition&gt; option is necessary to ensure angles of incidence are correct for some offset gathers.

![](/assets/syn-waveeqn6.png)

Calculate Synthetic Gather GUI - 1 Gather synthetic + 2 horizons shown

( Angle gather, Zoeppritz amplitudes )

![](/assets/syn-waveeqn7.png)

Calculate Synthetic Gather GUI - 1 Gather synthetic + 2 horizons shown

( Offset gather with NMO, Wave equation amplitudes )

**Output Geometry :**

**![](/assets/model-geom1b.png)**

Output Geometry GUI

The gather “geometry” for output, can be defined manually or copied from an existing dataset in the volume pool, using ‘Set gather size from’. However,

Wave equation synthetics can only be offset gathers.

**Modelling Options :**

![](/assets/syn-waveeqn9.png)

Modelling Options GUI – Zoeppritz default parameters

![](/assets/syn-waveeqn8.png)

Modelling Options GUI – Wave equation default parameters

Users can make a synthetic using the usual Zoeppritz, Aki-Richards, Shuey amplitude calculation methods. They can select to have no NMO correction for ray traced offset synthetics. There is also a fast wave equation option, which only outputs offset gathers, with NMO. This provides better synthetic gathers for understanding thin bed tuning, interbed multiples and the impact of P-SV converted noise on real prestack data. Primaries have realistic amplitudes at far offsets, and are corrupted by all P to SV energy noise, and if selected, all internal reverberations.

![](/assets/cusersjohannappdatalocalmicro.png)

Synthetic Gather comparison - 3 Gather synthetics shown

(2 Offset gathers with NMO : 1st Zoeppritz &amp; 2nd Wave equation amplitudes)

( 3rd offset gather is 2nd after NMO correction with adjusted Vrms volume )

![](/assets/cusersjohannappdatalocalmicro.png)

The user can choose to output a matching RMS velocity volume, for the wave equation synthetic, which will allow this offset gather to be converted to an angle gather using Pre-Stack Pro processing. The 3<sup>rd</sup> right hand gather above was created using this “adjusted RMS velocity volume”

If a T-D table exists in the well it can be used for all methods except wave equation. The ‘Fit Accuracy’ parameter controls how closely the T-D table is honoured instead of the Vp log travel times. Use the default 100% to force the closest fit to the T/D table.

If there is no T-D table or it is not desired to use it, a single time-depth pair can be entered manually using the &lt;Tie log depth&gt; option and the T-D curve is obtained from that point and the integrated sonic log.

The &lt;Tie log depth&gt; option is required for the wave equation method if the Vp log doesn’t reach up to the surface.

In the example below, the &lt;Tie log depth&gt; modelling option is selected, to ensure a synthetic model Target layer top, is at the right TWT.

( TVDss = 2000m = 2.0secs )

For 1D model synthetics, Don’t use the &lt;Time-Depth table&gt; option as the ‘Fit Accuracy’ algorithm is designed to work with Vp logs which have 100’s of T/D points and not with a model log of &lt; 10\. Also make sure the &lt;Log Preconditioning&gt; is not used as model logs are noise free and blocked correctly already.

A simple overburden model can be typed in to define what happens above the start of the logs. ( TVDss/Vint or TWT/Vint or TWT/Vrms pairs ). This is important when creating offset synthetics, as it affects the angle-to-offset

( AVO ) relationship considerably.

**Log Preconditioning :**

![](/assets/ldc1a.png)

|  |  |
| --- | --- |

Log Preconditioning GUI - default parameters

Logs can be de-spiked and blocked to improve synthetic quality and allow focus on main layer boundaries. Blocking will also significantly reduce the number of log samples input to the synthetic calculation which will make wave equation calculations in particular, much faster.

![](/assets/cusersjohannappdatalocalmicro.png)

1<sup>st</sup> gather is a Zoeppritz synthetic from raw logs, 2<sup>nd</sup> is after de-spike/blocking

3<sup>rd</sup> is an NMO corrected, Wave Equation synthetic, using blocked logs

**De-spiking**, works by cascaded median filtering of half-length 1 up to half length **Max Spike Width**. In each of the iterations the original value is replaced by the median value if the difference between original and median value is larger than the log’s **Min. Spike Amplitude**.

The effect of de-spiking becomes larger with decreasing **Min. Spike Amplitude** and increasing **Max. Spike Width**. De-spiking is switched off by setting **Max. Spike Width** to 0.0\.

| ![](/assets/cusersjohannappdatalocalmicro.png) | **Blocking,** works by replacing values by the average of all values inside a block; a block being defined by a series of log values for which the values do not differ by more than the **Blocking Rel.jump** (a fraction of 1). |
| --- | --- |

**Synthetic gather Q.C. :**

Once a synthetic gather has been calculated and appears in the Data Pool it can be viewed either in the **Data Comparator** or in the **Well Log Viewer** for display with its input Vp/Vs/Rho well logs.

Wave equation synthetics will need processing with the same workflow applied to real gathers to ensure the best comparison can be made. This processing could include : Geometric spreading correction , Obliquity factor amplitude correction, Radon demultiple, RMO, Spectral balancing across offsets.

If log preconditioning is done, the preconditioned logs appear in the Data Pool along with the Synthetic gather and can be viewed in the Well Log Viewer by drag and drop.

Alternatively, if the user opens up the ‘Calculate Synthetic Gather’ GUI again using the &lt;Edit algorithm parameters&gt; option, they can go to the Log Preconditioning Tab and select to ‘Show in Log Viewer’ the logs used to create the synthetic gather.

![](/assets/cusersjohannappdatalocalmicro.png)

There is a choice of displaying source and processed logs together or all source and all processed together. The different log displays are shown below.

| ![](/assets/cusersjohannappdatalocalmicro.png) |
| --- | --- |
| Source &amp; processed logs in same **Vp, Vs** and **Density** tracks | All logs together in **source** and **processed** tracks |
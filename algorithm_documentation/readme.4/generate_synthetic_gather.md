# Generate Synthetic Gather

## Introduction

This application creates a single offset or angle gather at the well, from input $$V_p$$, $$V_s$$ and $$\rho$$ logs and a project wavelet. The angle gathers are calculated using just horizontal AVA amplitudes but the offset gathers are ray traced from the surface. Therefore the Overburden Definition option is necessary to ensure angles of incidence are correct for some offset gathers.

![](../../.gitbook/assets/055_interpretation.PNG)

_Calculate Synthetic Gather GUI - 1 Gather synthetic + 2 horizons shown \( Angle gather, Zoeppritz amplitudes \)_

![](../../.gitbook/assets/056_interpretation.PNG)

_Calculate Synthetic Gather GUI - 1 Gather synthetic + 2 horizons shown \( Offset gather with NMO, Wave equation amplitudes \)_

## Output Geometry:

![](../../.gitbook/assets/057_interpretation.PNG)

_Output Geometry GUI_

The gather “geometry” for output, can be defined manually or copied from an existing dataset in the volume pool, using ‘Set gather size from’. However, Wave equation synthetics can only be offset gathers.

## Modelling Options

![](../../.gitbook/assets/058_interpretation.PNG)

_Modelling Options GUI – Zoeppritz default parameters_

![](../../.gitbook/assets/059_interpretation.PNG)

_Modelling Options GUI – Wave equation default parameters_

Users can make a synthetic using the usual Zoeppritz, Aki-Richards, Shuey amplitude calculation methods. They can select to have no NMO correction for ray traced offset synthetics. There is also a fast wave equation option, which only outputs offset gathers, with NMO. This provides better synthetic gathers for understanding thin bed tuning, interbed multiples and the impact of P-SV converted noise on real pre-stack data. Primaries have realistic amplitudes at far offsets, and are corrupted by all P to SV energy noise, and if selected, all internal reverberations.

![](../../.gitbook/assets/060_interpretation.PNG)

Synthetic Gather comparison - 3 Gather synthetics shown \(2 Offset gathers with NMO : $$1^{st}$$ Zoeppritz & $$2^{nd}$$ Wave equation amplitudes\) \( $$3^{rd}$$ offset gather is $$2^{nd}$$ after NMO correction with adjusted $$V_{rms}$$ volume \)

![](../../.gitbook/assets/061_interpretation.PNG)

The user can choose to output a matching RMS velocity volume, for the wave equation synthetic, which will allow this offset gather to be converted to an angle gather using Pre-Stack Pro processing. The $$3^{rd}$$ right hand gather above was created using this “adjusted RMS velocity volume”

If a T-D table exists in the well it can be used for all methods except wave equation. The ‘Fit Accuracy’ parameter controls how closely the T-D table is honoured instead of the $$V_p$$ log travel times. Use the default 100% to force the closest fit to the T/D table.

If there is no T-D table or it is not desired to use it, a single time-depth pair can be entered manually using the Tie log depth option and the T-D curve is obtained from that point and the integrated sonic log.

The Tie log depth option is required for the wave equation method if the $$V_p$$ log doesn’t reach up to the surface.

In the example below, the Tie log depth modelling option is selected, to ensure a synthetic model Target layer top, is at the right TWT.

![](../../.gitbook/assets/062_interpretation.PNG)

_\( TVDss = 2000m = 2.0secs \)_

For 1D model synthetics, Don’t use the Time-Depth table option as the ‘Fit Accuracy’ algorithm is designed to work with $$V_p$$ logs which have 100’s of T/D points and not with a model log of &lt; 10. Also make sure the Log Preconditioning is not used as model logs are noise free and blocked correctly already.

A simple overburden model can be typed in to define what happens above the start of the logs. \( TVDss/Vint or TWT/Vint or TWT/Vrms pairs \). This is important when creating offset synthetics, as it affects the angle-to-offset \( AVO \) relationship considerably.

## Log Preconditioning

![](../../.gitbook/assets/063_interpretation.PNG)

_Log Preconditioning GUI - default parameters_

Logs can be de-spiked and blocked to improve synthetic quality and allow focus on main layer boundaries. Blocking will also significantly reduce the number of log samples input to the synthetic calculation which will make wave equation calculations in particular, much faster.

![](../../.gitbook/assets/064_interpretation.PNG)

$$1^{st}$$ _gather is a Zoeppritz synthetic from raw logs,_ $$2^{nd}$$ _is after de-spike/blocking,_ $$3^{rd}$$ _is an NMO corrected, Wave Equation synthetic, using blocked logs_ 

**De-spiking**, works by cascaded median filtering of half-length 1 up to half length **Max Spike Width**. In each of the iterations the original value is replaced by the median value if the difference between original and median value is larger than the log’s **Min. Spike Amplitude**.

The effect of de-spiking becomes larger with decreasing **Min. Spike Amplitude** and increasing **Max. Spike Width**. De-spiking is switched off by setting **Max. Spike Width** to 0.0.

![](../../.gitbook/assets/065_interpretation.PNG) ![](../../.gitbook/assets/066_interpretation.PNG)

_3% , 1m V 10% & 40m_

**Blocking**, works by replacing values by the average of all values inside a block; a block being defined by a series of log values for which the values do not differ by more than the **Blocking Rel.jump** \(a fraction of 1\). The maximum size of blocks can be limited to **Blocking Max. Sampling Distance**. The effect of blocking becomes larger with increasing **Blocking Rel. Jump** and increasing **Blocking Max. Sampling Distance**. Blocking is switched off by setting **Blocking Rel.Jump** to 0. The first density log is blocked by a rel. jump of 0.03 and a max distance of 1m. \( default values \) The $$2^{nd}$$ density log by a rel. jump of 0.1 and a max distance of 40m. Both logs have default de-spiking.

## Synthetic gather Q.C.

Once a synthetic gather has been calculated and appears in the Data Pool it can be viewed either in the **Data Comparator** or in the **Well Log Viewer** for display with its input $$V_p$$/$$V_s$$/Rho well logs.

Wave equation synthetics will need processing with the same workflow applied to real gathers to ensure the best comparison can be made. This processing could include: Geometric spreading correction, Obliquity factor amplitude correction, Radon demultiple, RMO, Spectral balancing across offsets.

If log preconditioning is done, the preconditioned logs appear in the Data Pool along with the Synthetic gather and can be viewed in the Well Log Viewer by drag and drop.

Alternatively, if the user opens up the ‘Calculate Synthetic Gather’ GUI again using the Edit algorithm parameters option, they can go to the Log Preconditioning Tab and select to ‘Show in Log Viewer’ the logs used to create the synthetic gather.

![](../../.gitbook/assets/067_interpretation.PNG)

There is a choice of displaying source and processed logs together or all source and all processed together. The different log displays are shown below.

![](../../.gitbook/assets/068_interpretation.PNG)

_Source & processed logs in same_ $$V_p$$_,_ $$V_s$$ _and **Density** tracks_

![](../../.gitbook/assets/069_interpretation.PNG)

_All logs together in **source** and **processed** tracks_


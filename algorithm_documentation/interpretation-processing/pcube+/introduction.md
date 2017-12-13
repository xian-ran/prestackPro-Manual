#### Introduction {#introduction}

Pcube+ is an extension of the existing inversion algorithm Pcube.

It features:

*   An improved user interface, which includes all functionalities in one graphical window
*   Increased functionality for Parameter Estimation
*   Improved handling of Transition Probabilities
    *   Illegal combinations of facies can be defined within a zone
*   Generation of horizons, with uncertainty range included
*   A separate Pcube+ Inspector window for inspection of output data from the inversion routine.

This section is self-contained. Users do not need to consult the sections on the old Pcube in order to use Pcube+ properly.

The inversion method in Pcube+ is an elastic method, based on the work of Buland, Omre and others (Geophysics, 2003; Geophysics, 2008). PSPro users will see this as a single process, although it is in fact a 2 stage process:

Stage 1: angle stacks are inverted deterministically to give elastic properties.

Stage 2: the elastic properties are subjected to Bayesian classification to supply probability cubes for different litho-facies.

As with most pre-stack inversions, a prior model and wavelets are also required. The horizons defined in the prior model are updated during the inversion, providing new horizons with the uncertainty range included.

The user will need to define input parameters, set up a background model and specify transition probabilities before running the inversion. Tuning of parameters will also be necessary. Output volumes and maps from the inversion will appear in the Data Pool.

An inspection window, **Pcube+ Inspector**, provides the user with the possibility to review the output data in a similar way to the Parameter Tuning tab.

The user interface is opened in **Interpretation-Processing** → **Pcube+**

Currently, Pcube+ does not support using arbitrary lines.

_The graphical user interface at startup of Pcube+_
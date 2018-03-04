#### Introduction {#introduction}

The wavelet tool is designed to perform interactive design and manipulation of wavelets, spectra, and filters. In particular, common geophysical tasks such as spectral shaping, whitening, and colored inversion can be carried out using the wavelet tool to design the operators. It has a variety of signal processing functions which can be used in a flexible way to achieve the desired result. In Pre-Stack Pro we use the word “wavelet” in a very general sense to include seismic wavelets, spectra, and filters or operators.

The wavelet tool is designed to be used in conjunction with the spectral analysis tool and the user-defined filter tool. A typical workflow to shape a seismic spectrum to some desired filter would be:

Estimate the actual seismic spectrum in the spectral analysis tool, and save it to the project.  
Load the spectrum into the wavelet tool and design a shaping operator, saving that to the project.  
Apply the shaping operator to the seismic volume using the user-defined filter module.

Some example workflows are described in more detail in section **Error! Reference source not found.**

**GUI Layout**

The Wavelet Tool can be started from the Interpretation-Processing menu. The tool window layout is described in the figure below.

![](/assets/132_Interpretation.png)
_Wavelet Tool - Layout_

**Wavelet data list**

This area contains a list of wavelets loaded or created in the current session. They are all in memory, so they will be lost when the tool is closed unless they are explicitly saved to the project. There are various options that can be accessed by right-mouse clicking on a wavelet in the list.

**Properties/Comments tabs**

The Properties tab shows the time range, sample interval, number of samples, minimum and maximum sample values, and whether the wavelet has been saved to the project or not. The Comments tab displays any user’s comments attached to the wavelet.

**Function Group**

The function group drop-down menu lets you select from a list of categories: Load/Create Wavelets, Filtering, Utility, and Equations. These are combined in the All option. There are also Colored & EEI Inversion functions to provide wizards to compute Inversion operators.

When you select one of these groups it will show a list of available functions under that heading. Load/Create Wavelets is described in section 6.6.18.2 . Color and EEI Inversion appear in section Error! Reference source not found.. All of the other options are detailed in section 6.6.18.12 

**Menu Bar**

This contains several icons giving control of display options. They are described in section 6.6.18.2 

**Management Bar**

This contains icons to edit algorithm parameters, rename a wavelet, save to project, freeze a copy of a wavelet, and delete a wavelet from the list. The functions are described in section 6.6.18.2 

**Time, Amplitude and Spectrum Displays**

These display options are described in section 6.6.18.2 

**Wavelet table**

This shows the time, sample value pairs for the currently selected wavelet. It can be accessed by the table icon in the menu bar.

**Working with the tool**

The various functions in the tool do not have an explicit input wavelet in their dialogue boxes. Instead, it’s necessary to highlight a wavelet in the list before opening the desired function.

Each time a function is applied to a wavelet, the output appears in the list of wavelets. Thus, a sequence can be constructed, where each wavelet is dependent upon it ancestors. If a parameter value is changed early on in the sequence, then all of the subsequent wavelets will be updated automatically.

This makes parameter testing simple. Optimal parameters can be decided after the whole sequence has been constructed. “Frozen” copies can be made to facilitate comparisons. These do not update when their ancestors are changed.

All wavelets loaded or created in the Wavelet tool only exist in memory. Thus, they no longer exist once the tool is closed. Any wavelet or operator which will be applied to a seismic volume must be saved to the project from the wavelet tool. When the tool is closed, a warning dialogue box will pop up if there are any unsaved wavelets, giving the user the chance to go back and save them if desired.

In the current version of the tool, there is no facility to save the history of a wavelet or to create workflows.


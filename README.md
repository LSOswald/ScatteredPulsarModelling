# ScatteredPulsarModelling

This program reads in a pulsar ascii file (created using pdv -KAt on an archive file) and fits a scattering model to the pulse intensity profile at each frequency.

For details of the command line arguments, type:
>> python modelscattering.py -h

An example command would be as follows:
>> python modelscattering.py -f (filename of data) -r (folder containing data) -w (folder to write output to) -m (method: iso or onedim, default is iso) -passfaillog (name of log for success/failure of model) -noshow

The code generates the following files containing model parameters and diagnostic plots:
>filename_alphaDM.csv			- Contains values of alpha and DM correction with errors.
>filename_alpha_evolution.png		- Plot of how alpha changes depending on what frequencies are included in its calculation.
>filename_fitted_profiles_iso_0.png	- Plot of the pulse profiles with the best fit model.
>filename_fitting_parameters.png		- Plot of how 6 fitting parameters vary with frequency.
>filename_freqvariables.csv		- Contains model parameters (and some other key pulsar information) for the pulse profile at each frequency.
>filename.log				- Log of fitting process.
>filename_model				- Pickle file of the best fit model: can be loaded into Python as a numpy array.
>filename_residuals			- Pickle file of the residuals from subtracting the best fit model from the data.
>filename_tau_spectrum.png		- Log-log plot of scattering timescale tau against frequency, with best power law alpha fit shown.

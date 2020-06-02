# ScatteredPulsarModelling

This program reads in a pulsar ascii file (created using pdv -KAt on an archive file) and fits a scattering model to the pulse intensity profile at each frequency.

For details of the command line arguments, type:
>> python modelscattering.py -h

An example command would be as follows:
>> python modelscattering.py -f <filename of data> -r <folder containing data> -w <folder to write output to> -m <method: iso or onedim, default is iso> -passfaillog <name of log for success/failure of model> -noshow

## Synthetic Telluric Atlases for DKIST 

This subdirectory contains multiple numpy save files containing absorption spectra of the Earth's atmosphere tailored for the Daniel K Inouye Solar Telescope. 

Please see the notebooks in the main directory for information about how these files were generated. 

One 32-bit numpy array file is included for the wavelength axis.  There are 2,659,263 wavelength points that sample the wavelength range of 350 to 5000 nm with a resolution of R ~ 1 million.  Thus, the wavelength axis is non-uniformly sampled in wavelength.  The data themselves are interpolated onto this wavelength grid from the original outputs of the Py4Cats package.  That package determines the optimum wavelength resolution for the calculated spectral range, and is generally higher resolution that that saved into the files of this directory.  

The atmosphere used is the US Standard Atmosphere (G.P. Anderson et al., 1986, TR-86-0110).  The CO2 column mixing ratio is scaled to 416 ppm in accordance with recent global averages. 

The individual numpy arrays calculated the synthetic spectra for varying values of precipitable water vapor and airmass, as encoded in the filenames themselves. 

An example of how to load and plot the data are in the main directory. 

As a starting point, to use a single reference spectrum, it is recommended to use the file with 3 mm PWV and 1 airmass, where 3 mm PWV is the closest to the water content in the US standard atmosphere above 3 km. 


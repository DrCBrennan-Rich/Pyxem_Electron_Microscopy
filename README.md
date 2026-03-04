# Pyxem_Electron_Microscopy
This is a set of scripts developed throughout my PhD to perform both simple and complex operations on 4D-STEM data.
Simple features include imaging real and recipricol space; producing high-angle annular dark field (HAADF) images; and callibrate, crop and Fourier transform images.
More complex scripts focus on the use of template matching for phase and orientation assignment from the 4D-STEM data, as well as simulating nano-beam electron diffraction (NBED) patterns. 

Table of contents:
Pyxem.yml - The file that can be used to construct the enviroment

CroppedAndProcessing - Loads data for initial viewing and supplies widgets for callibrating the real space and recipricol space; normalises the data; crops and resaves if required. This should be the first file ran on on any new electron diffraction data.

PowerSpectrum - Plots, adjusts and then performs Fourier transform on an image. Power spectrum (absolute value squared) from the Fourier transform and a simple peak search to find the locations of the spectral peaks.

For further information, the best place to search is the incredibly well structured Pyxem github:
https://github.com/pyxem which should be cited using: https://zenodo.org/records/15594715



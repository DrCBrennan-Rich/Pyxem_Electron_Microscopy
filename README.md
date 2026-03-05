# Pyxem_Electron_Microscopy
[![DOI](https://zenodo.org/badge/1171564589.svg)](https://doi.org/10.5281/zenodo.18880685)

This is a set of scripts developed throughout my PhD to perform both simple and complex operations on 4D-STEM data.
Simple features include imaging real and recipricol space; producing high-angle annular dark field (HAADF) images; and callibrate, crop and Fourier transform images.
More complex scripts focus on the use of template matching for phase and orientation assignment from the 4D-STEM data, as well as simulating nano-beam electron diffraction (NBED) patterns.

Some useful baseline information: A 4D data set is described as such because each intensity is associated with four coordinates: diff_x and diff_y (the x and y coordinate on the 2d detector, in effect measuring in recipricol space) and nav_x and nav_y (the x and y coordinate in real space on the sample where the beam was directed to produce the 2D diffraction pattern that fell on the detector). The art of electron microscopy data anlysis is the manipulation and presentation of data in this 4D space. 

Table of contents:
Pyxem.yml - The file that can be used to construct the enviroment

CroppedAndProcessing - Loads data for initial viewing and supplies widgets for callibrating the real space and recipricol space; normalises the data; crops and resaves if required. This should be the first file ran on on any new electron diffraction data.

DarkFieldandSpotIntegration - Produces high-angle annular dark field (HAADF) images as well as the integrated spot diffraction pattern over a selected region. Also includes the ability to adjust pixels that are suffering intensity bleed through.

PhaseMapTemplateMatching - Allows for the production of a phase map through the process of cross correlating each diffraction pattern in the data to a library of simulated diffraction patterns.

PowerSpectrum - Plots, adjusts and then performs Fourier transform on an image. Power spectrum (absolute value squared) from the Fourier transform and a simple peak search to find the locations of the spectral peaks.

SpotDiffractionSimulation - Simulate the spot diffraction patterns for visual comparison to data from the relevant crystallographic information file (CIF).

For further information, the best place to search is the incredibly well structured Pyxem github:
https://github.com/pyxem which should be cited using: https://zenodo.org/records/15594715

As linked above, the most recent release of this repository can be cited with: https://doi.org/10.5281/zenodo.18880685
If you make significant improvements/develop new features, feel free to fork, produce your own release or even better push the change back to the original repository. Note that the GNU license (inhereited through pyxem from hyperspy) is required provided you did not completely rewrite this code from scratch.

Extra note: Sometimes miscommunication arises between those who are more 'pragmatic users' of diffraction methods as a portion of their work, and those who spend their majority time studying and using diffraction techniques. Nowhere does this become more apparent, than when the topic of Miller indicies (hkl values), and brackets: (){}[]⟨⟩coincide. The key to remember, which is consistently applied across this project (or noted when deviated from):

hkl - referring to the hkl values themselves, "The hkl values of this reflection."

(hkl) - a particular plane of atoms in real space, or reflection point in recipricol space (the reflection index).

[hkl] (though I personally prefer [uvw]) - a direction vector in real space.

{hkl} - A family of equivelent reflections due to symmetry (connected to the multiplicity). The classic example would be (001), (010), (100) and the negatives for the cubic lattice.

⟨hkl⟩ (or ⟨uvw⟩) - The family of equivelent real space directions. Again a good example is for the cubic lattice: [001], [010], [100].


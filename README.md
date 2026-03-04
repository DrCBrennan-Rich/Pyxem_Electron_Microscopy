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

Extra note: Sometimes miscommunication arises between those who are more 'pragmatic users' of diffraction methods as a portion of their work, and those who spend their majority time studying and using diffraction techniques. Nowhere does this become more apparent, than when the topic of Miller indicies (hkl values), and brackets: (){}[]⟨⟩coincide. The key to remember, which is consistently applied across this project (or noted when deviated from):

hkl - referring to the hkl values themselves, "The hkl values of this reflection."

(hkl) - a particular plane of atoms in real space, or reflection point in recipricol space (the reflection index).

[hkl] (though I personally prefer [uvw]) - a direction vector in real space.

{hkl} - A family of equivelent reflections due to symmetry (connected to the multiplicity). The classic example would be (001), (010), (100) and the negatives for the cubic lattice.

⟨hkl⟩ (or ⟨uvw⟩) - The family of equivelent real space directions. Again a good example is for the cubic lattice: [001], [010], [100].


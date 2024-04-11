This repository contains FID-A spin systems for simulation of macromolecules. For each macromolecule spin system,  J is set to 0 to represent no couplings, and the scaleFactor is set to the number of protons, as specified in Cudalbu et al. (2021) NMR in Biomed, and included in the table below.

Shifts is set to the frequency (ppm) of the macromolecule peak, which was determined using information obtained by parameterizing freely available 7T metabolite suppressed data from six healthy individuals (Považan et al., 2015, https://zenodo.org/records/3906754#.XvOWVvJ7n7e). First, all six  metabolite-nulled spectra were combined into a single average macromolecule spectra. Nine MM resonances were then identified in the average macromolecule spectrum, and each macromolecule resonance was fit to a gaussian lineshape using in house custom MATLAB scripts to estimate the frequency,  linewidth, and relative amplitude, as specified in Bell et al. (2024) Under Review.

To simulate macromolecules, FID-A spin systems need to be added to the spinSystems.mat file found in the FID-A toolbox under simulationTools/metabolites. Then macromolecules can be simulated in the same way as metabolites, using the linewidth specified below. Lastly, these can then be added to a LCModel basis set, with the concentrations constrained as specified below. Concentrations are relative to MM0.95.



Macromolecule |Frequency (ppm)|No. Protons| Simulated Linewidth (Hz)| LCModel Constraint
    M0.95         0.95		    3		        32			            n/a
    M1.24        1.235		    3		        23			        0.41 +- 0.16
    M1.43        1.427		    3		        26			        0.98 +- 0.67
    M1.71        1.705		    2		        31			        1.185 +- 1.10
    M2.07         2.07		    2		        38		        	2.53 +- 0.81
    M2.30        2.295	 	    2		        32		        	2.00 +- 0.17
    M3.03         3.03		    2		        26			        1.30 +- 0.32
    M3.24         3.24		    2		        48		        	0.10 +- 0.22
    M3.98         3.98		    2		        109			        2.33 +- 0.72

Table values from Bell et al. (2024) Under Review

# Diamond lens profiling from cross-sectional image
This Jupyter notebook extracts the profile of a solid-immersion lens (SIL) by analysing a cross-sectional image of the lens.

[Link to Jupyter notebook](https://github.com/cameronsalter/Diamond-lens-profiling/blob/master/SEM_LensXsect_ProfExtract.ipynb)

## Table of contents
* [Background](https://github.com/cameronsalter/Diamond-lens-profiling#background)
* [Methodology used in analysis](https://github.com/cameronsalter/Diamond-lens-profiling#methodology-used-in-analysis)
* [Basic user guide](https://github.com/cameronsalter/Diamond-lens-profiling#basic-user-guide)
* [Acknowledgements](https://github.com/cameronsalter/Diamond-lens-profiling#acknowledgements)


## Background
SILs were milled into a diamond substrate using focussed-ion beam (FIB) milling over single point-defects in the crystal structure which fluoresce. Information on the lens profile was required to optimise collection efficiency of the fluoresce. This information proved very difficult to get using AFM imaging due to high aspect ratios (lens radii ~ 1-2 um). The approach here uses FIB cross-sectioning to slice a lens in half - the lens profile can then be imaged using an electron microscope.

Work done ~2015 during post-doc at TU Wien.

Cross-sectional image of SIL: 

<img src="https://github.com/cameronsalter/Diamond-lens-profiling/blob/master/Xsect_images/EllipSIL1_LH1p24_cut58deg_x-sct_10kV_spt2_Rot4deg.jpg" width="600">


Extracted profile of SIL:

<img src="https://github.com/cameronsalter/Diamond-lens-profiling/blob/master/Extracted_lens_profile.png" width="550">


## Methodology used in analysis
Uses the intensity contrast between a diamond lens and its platinum coating in cross-sectional image to determine boundary defining the lens shape.

## Basic user guide
1. Select region of interest containing SIL and deposited Pt.
2. (optional) Restrict 'colour' range (0-256) to increase contrast
3. Calculate average intensity for Pt coating and diamond (within SIL) regions: select start and end of Pt region at x=0 in truncated image; select end of SIL region along the lens centre in tuncated image.
4. Decide where in the boundary between diamond and Pt the SIL edge should lie - enter value for Bndry_thrshld (e.g. 0.5 => intensity boundary is exatly half way between diamond and Pt intensities)

## Acknowledgements
Marie Curie Actions (funding)

USTEM at TU Wien (FIB and SEM systems)

Work completed in Trupke group TU Wien/Uni Wien: https://walther.univie.ac.at/people/michael-trupke/

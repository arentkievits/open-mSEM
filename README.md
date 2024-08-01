# Open platform for mSEM
![CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](code_of_conduct.md) 

The open platform for mSEM centralizes information, data, methods and applications related to multibeam scanning electron microscopy (mSEM). We are developing mSEM methodology in the [Hoogenboom lab](https://www.hoogenboomlab.org/) in the department of Imaging Physics at Delft University of Technology (TUD), the Netherlands. We apply mSEM in the field of [volume electron microscopy](https://www.volumeem.org/vem-explained.html) (vEM). With this platform, we want to inform and engage other researchers interested in mSEM and vEM about the imaging technique. Our output (publications, methods, code and data) will be freely available and reusable under open licenses.

Key goals of the project:
- Open sharing of (raw) data, methods, publications about mSEM.
- Interactive code with documentation
- Interactive data viewing in 3D
- Informing and engaging other scientists interested in volume electron microscopy

## 1 About mSEM
Multibeam scanning electron microscopy (mSEM) is a type of electron microscopy in which a sample is scanned by multiple electrons beams in parallel. Therefore, the throughput of the microscope scales with the number of beams, leading to much higher acquisition speeds compared to a single-beam scanning electron microscopy. This is relevant since large vEM acquisitions typically take a long time with single-beam electron microscopes, up to several months or even years in exceptional cases. 

There are currently two available commercial mSEMs. At TUD, in collaboration with a consortium of Thermo Fisher Scientific, Technolution Advance and Delmic, a 64-beam scanning transmission electron microscope has been developed that is dedicated to imaging of biological tissue: FAST-EM [1]. You can read more about the microscopy technique [in this publication](https://www.degruyter.com/document/doi/10.1515/mim-2024-0005/html) and on the [manufacturer's website](https://www.delmic.com/en/products/fast-imaging/fast-em). ZEISS has developed a 61/91 beam scanning electron microscope, [MultiSEM](https://www.zeiss.com/microscopy/en/products/sem-fib-sem/sem/multisem.html). This mSEM is based on secondary electron imaging, thereby being suitable for the imaging of thin biological samples as well as other applications like high-throughput wafer inspection [2]. 

### 1.1 mSEM (FAST-EM) principle
In FAST-EM, 64 beams are created from a single electron source with the help of microaperture lens array [3]. These 64 beams travel through a single electron column to arrive at the sample. In FAST-EM, ultrathin biological sections are deposited on scintillator substrates, which generate light upon impact by electrons that transmit through the sample. This detection principle is called optical scanning transmission electron microscopy (optical STEM or OSTEM). The 64 individual light signals are detected by a multipixel photon counter array, providing a single intensity readout per beamlet and scanning position.  

<img src="https://www.degruyter.com/document/doi/10.1515/mim-2024-0005/asset/graphic/j_mim-2024-0005_fig_001.jpg" width="600">
Figure adapted from Kievits et al. [3]

### 1.2 Characterization of electron detection in FAST-EM
As discussed above, FAST-EM makes use of OSTEM detection. We performed an extensive characterization and benchmarking of this method on thin biological samples in relation to conventional detection techniques (e.g. backscatter electron detection and secondary electron detection). This work is published in [Kievits et al. (2024)](https://doi.org/10.1016/j.ultramic.2023.113877) and the code and data to reproduce the results is available [via the 4TU data repository](10.4121/9c98aee1-608e-4c71-8b89-dcb1e8eb3e5e.v2).

### 1.3 Volume electron microscopy and mSEM
Volume electron microscopy comprises a set of electron microscopy techniques for imaging biological samples in 3D with nanometer precision. If you want to learn more about the research field, we encourage to read these very accessible and informative literature reviews:  

Links:
- Our open access review about vEM instrumentation in [Journal of Microscopy](https://onlinelibrary.wiley.com/doi/10.1111/jmi.13134)
- Another extensive review article serving as a primer for vEM in [Nature Primers](https://www.nature.com/articles/s43586-022-00145-3) 
- Volume electron microscopy: [Peddie & Collinson (2014)](https://www.sciencedirect.com/science/article/pii/S0968432814000250)
- Connectomics and the use of mSEM: [Kornfeld & Denk (2018)](https://onlinelibrary.wiley.com/doi/full/10.1111/boc.201600024), [Eberle & Zeidler (2018)](https://www.frontiersin.org/articles/10.3389/fnana.2018.00112/full)

mSEM is a trending research topic. We encourage interested readers to read these selected publications, from which we draw inspiration for the project:
- A petavoxel fragment of human cerebral cortex reconstructed at nanoscale resolution ([Shapson-Coe et al. (2024)](https://doi.org/10.1126/science.adk4858))
- msemalign: a pipeline for serial section multibeam scanning electron microscopy volume alignment ([Watkins et al. (2023)](10.3389/fnins.2023.1281098))
- GAUSS-EM: Guided accumulation of ultrathin serial sections with a static magnetic field for volume electron microscopy ([Fulton et al. (2024)](https://doi.org/10.1016/j.crmeth.2024.100720))

## 2 Data sets
We run self-hosted instances of [CATMAID](https://sonic.tnw.tudelft.nl/catmaid/) [4] and [WebKnossos](https://webknossos.tnw.tudelft.nl) [5]. We use CATMAID and WebKnossos for interactive viewing of large 3D datasets from FAST-EM and for data analysis. FAST-EM raw datasets linked to publications will be uploaded to EMPIAR. 

Example 2D datasets of FAST-EM can be viewed here:
- [Rat pancreas (de Boer & Giepmans [6]](http://nanotomy.org/OA/deBoer2021ICB/index.html))
- [Larval zebrafish (Kievits et al. [7], conference abstract)](http://www.nanotomy.org/OA/Kievits2023MMA/)

3D datasets from Kievits et al. [3]:
- [Rat pancreas](http://nanotomy.org/OA/Kievits2024MIM/index.html)
- [MCF-7 cell culture](http://nanotomy.org/OA/Kievits2024MIM/index.html)

## 3 Methodology & Projects
We are developing the following methods:

### 3.1 Array tomography workflow for FAST-EM
We implemented a workflow for array tomography with FAST-EM in collaboration with the groups of Ben Giepmans and Nalan Liv at University Medical Center Groningen and University Medical Center Utrecht. This workflow includes sample preparation, acquisition and image post-processing. Array tomography is a volume electron microscopy technique in which serial ultrathin biological sections deposited on a substrate are imaged reconstructed into a 3D volume. The manuscript is published open access in the inaugural issue of the new journal [Methods in Microscopy](https://www.degruyter.com/journal/key/mim/html). The code developed and used for 3D reconstruction and data analysis is full availabe online.  

<img src="https://www.degruyter.com/document/doi/10.1515/mim-2024-0005/asset/graphic/j_mim-2024-0005_fig_002.jpg" width="600">
FAST-EM array tomography. Figure adapted from Kievits et al. [3]

### 3.2 Automated segmentation and fluorescence prediction
In the future our lab aims to develop novel methods for automated segmentation and label-free prediction of fluorescence on mSEM (FAST-EM) data. We are planning to develop methods based on convolutional neural networks and share them on [Bioimage Model Zoo](https://bioimage.io/). 

### 3.3 Broad-ion beam mSTEM
The cutting of serial ultrathin sections for array tomography is a delicate and error-prone process. Artefacts caused by errors in sectioning include loss of material, folds, cracks or knife marks and may hamper 3D reconstruction and automatic segmentation and analysis. This is particularly a challenge in the field of connectomics which aims for dense reconstruction of neuronal wiring diagrams. The combination of broad-ion beam milling with FAST-EM imaging, together referred to as BIB-mSTEM, may circumvent these problems by iteratively milling and imaging semithin (100-1000nm) serial sections to match the desired z-resolution. A deconvolution procedure can then be used to reconstruct or deconvolve virtual reslices from the series of transmission projection images of the milled sections produced by FAST-EM. The first results were presented at Microscopy & Microanalysis 2024 (Cleveland, US) [8].

## 4 Applications
We will apply our methods to several demonstration projects and large-scale applications. More on this later.

## References
[1] Fermie, J., Zuidema, W., Šejnoha, R., Wolters, A., Giepmans, B., Hoogenboom, J., & Kruit, P. (2021). High-throughput imaging of biological samples with Delmic's FAST-EM. Microscopy and Microanalysis, 27(S1), 558-560.  

[2] Eberle, A. L., Mikula, S., Schalek, R., Lichtman, J., Tate, M. K., & Zeidler, D. (2015). High‐resolution, high‐throughput imaging with a multibeam scanning electron microscope. Journal of microscopy, 259(2), 114-120.  

[3] Kievits, A. J., Duinkerken, B. P., Lane, R., de Heus, C., van Beijeren Bergen en Henegouwen, D., Höppener, T., ... & Hoogenboom, J. P. (2024). FAST-EM array tomography: a workflow for multibeam volume electron microscopy. Methods in Microscopy, (0).  

[4] Saalfeld, S., Cardona, A., Hartenstein, V., & Tomančák, P. (2009). CATMAID: collaborative annotation toolkit for massive amounts of image data. Bioinformatics, 25(15), 1984-1986.  

[5] Boergens, K. M., Berning, M., Bocklisch, T., Bräunlein, D., Drawitsch, F., Frohnhofen, J., Herold, T., Otto, P., Rzepka, N., Werkmeister, T., & others. (2017). webKnossos: Efficient online 3D data annotation for connectomics. Nature Methods, 14(7), 691-694-691–694.  

[6] de Boer, P., & Giepmans, B. N. (2021). State‐of‐the‐art microscopy to understand islets of Langerhans: what to expect next?. Immunology and cell biology, 99(5), 509-520. 

[7] Kievits, A. J., Peter Duinkerken, B. H., Giepmans, B. N., & Hoogenboom, J. P. (2023). Need for Speed: Imaging Biological Ultrastructure with the 64-beams FAST-EM. (Conference abstract)  

[8] Kormacheva, M., Kievits, A., Reuteler, J., Niessen, M., Hoedt, S. den, Khan, S., Bosch, C., Hoogenboom, J., Schaefer, A., & Wanner, A. (2024). BIB-mSTEM Approach for Large Scale Acquisition of Brain Tissue. Microscopy and Microanalysis, 30(Supplement_1), ozae044.328. https://doi.org/10.1093/mam/ozae044.328






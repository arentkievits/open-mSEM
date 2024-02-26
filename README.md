# Open platform for MB-SEM
![CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](code_of_conduct.md) 

The open platform for MB-SEM centralizes information (1), data (2), methods (3) and applications (4) related to multibeam scanning electron microscopy (MB-SEM). We are developing MB-SEM methodology in the [Hoogenboom lab](https://www.hoogenboomlab.org/) at the department of Imaging Physics. We apply MB-SEM in the field of [volume electron microscopy](https://www.azooptics.com/Article.aspx?ArticleID=1504). With this platform, we want to stimulate other researchers interested in MB-SEM to join us in further developing the technique. Our methods will be freely available and reusable. 

Key goals of the project:
- Open sharing of (raw) data, methods, publications about MB-SEM.
- Interactive, out-of-the-box deployable code with documentation
- Interactive data viewing in 3D
- Inviting other researchers to join us in further developing MB-SEM

## 1 About MB-SEM
Multibeam scanning electron microscopy (MB-SEM) is a new microscopy technique in which a sample is scanned by multiple beams in parallel. Therefore, the throughput of the microscope scales with the number of beams. At TU Delft, a 64-beam scanning transmission electron microscope has been developed that is dedicated to imaging of biological tissue: FAST-EM. You can read more about the microscopy technique [in this publication](https://avs.scitation.org/doi/10.1116/1.4966216) and on the [manufacturer's website](https://www.delmic.com/en/products/fast-imaging/fast-em).

![image](https://raw.githubusercontent.com/arentkievits/MB-SEM/main/workflow.png)

### 1.1 Volume electron microscopy and MB-SEM
Volume electron microscopy comprises a set of electron microscopy techniques for imaging biological samples in 3D with nanometer precision. If you want to know more about the research field, we encourage to read these very accessible and informative literature reviews:

Links:
- Read our *open access review about innovations in volume EM methodology* in [Journal of Microscopy](https://onlinelibrary.wiley.com/doi/10.1111/jmi.13134)
- Another extensive review article in [Nature Primers](https://www.nature.com/articles/s43586-022-00145-3) 
- Volume electron microscopy: [Peddie & Collinson (2014)](https://www.sciencedirect.com/science/article/pii/S0968432814000250)
- About connectomics and the use of MB-SEM: [Kornfeld & Denk (2018)](https://onlinelibrary.wiley.com/doi/full/10.1111/boc.201600024), [Eberle & Zeidler (2018)](https://www.frontiersin.org/articles/10.3389/fnana.2018.00112/full)

MB-SEM is a trending research topic. We encourage interested readers to read these selected publications, from which we draw inspiration for the project:
- A connectomic study of a petascale fragment of human cerebral cortex (on [BioRxiv](https://doi.org/10.1101/2021.05.29.446289))
- msemalign: a pipeline for serial section multibeam scanning electron microscopy volume alignment ([Watkins et al. (2023)](10.3389/fnins.2023.1281098))
- GAUSS-EM: Guided accumulation of ultrathin serial sections with a static magnetic field for volume electron microscopy (on [BioRxiv](https://doi.org/10.1101/2023.11.13.566828))

### 1.2 Characterization of electron detection in FAST-EM
Our implementation of MB-SEM, FAST-EM, makes use of a new detection method called optical scanning transmission electron microscopy (OSTEM). We performed an extensive characterization and benchmarking of this method in relation to conventional detection techniques (e.g. backscatter electron detection). This work is published ([Kievits et al. (2024)](https://doi.org/10.1016/j.ultramic.2023.113877)) and the code and data to reproduce the results is available [here](10.4121/9c98aee1-608e-4c71-8b89-dcb1e8eb3e5e.v2).  

## 2 Data
We run self-hosted instances of [CATMAID](https://sonic.tnw.tudelft.nl/catmaid/) (Saalfeld et al. (2009) and [WebKnossos](https://webknossos.tnw.tudelft.nl) (Boergens et al. (2017). We use CATMAID and WebKnossos for interactive viewing of large 3D datasets from FAST-EM and for data analysis. We plan to also upload relevant FAST-EM datasets to EMPIAR. 

Example 2D datasets of FAST-EM can be viewed here:
- [Rat pancreas (de Boer & Giepmans (2021)](http://nanotomy.org/OA/deBoer2021ICB/index.html))
- [Larval zebrafish (Kievits et al. (2023), conference abstract)](http://www.nanotomy.org/OA/Kievits2023MMA/)

## 3 Methods
We are developing the following methods:

### 3.1 Array tomography workflow for FAST-EM
We are currently developing an acquisition and post-processing workflow for array tomography with FAST-EM at TU Delft. Array tomography is a volume electron microscopy technique were serial ultrathin sections of biological tissue are reconstructed into a 3D volume. We are preparing a manuscript on this workflow to be published in 2024. The code developed and used for 3D reconstruction is [available online](https://github.com/hoogenboom-group) in advance of publication. However it is still under active development and subject to changes. 

### 3.2 Automated segmentation and fluorescence prediction
In the future we would like to develop novel methods for automated segmentation and label-free prediction of fluorescence on FAST-EM data. We are planning to develop methods based on convolutional neural networks and share them on [Bioimage Model Zoo](https://bioimage.io/). 

## 4 Applications
We will apply our methods to several demonstration projects and large-scale applications. More on this later.

## References
Boergens, K. M., Berning, M., Bocklisch, T., Bräunlein, D., Drawitsch, F., Frohnhofen, J., ... & Helmstaedter, M. (2017). webKnossos: efficient online 3D data annotation for connectomics. nature methods, 14(7), 691-694.
de Boer, P., & Giepmans, B. N. (2021). State‐of‐the‐art microscopy to understand islets of Langerhans: what to expect next?. Immunology and cell biology, 99(5), 509-520. 
Kievits, A. J., Peter Duinkerken, B. H., Giepmans, B. N., & Hoogenboom, J. P. (2023). Need for Speed: Imaging Biological Ultrastructure with the 64-beams FAST-EM. (Conference abstract)
Saalfeld, S., Cardona, A., Hartenstein, V., & Tomančák, P. (2009). CATMAID: collaborative annotation toolkit for massive amounts of image data. Bioinformatics, 25(15), 1984-1986.



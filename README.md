# Open platform for MB-SEM
![CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](code_of_conduct.md) 

The open platform for MB-SEM centralizes information (1), data (2), methods (3) and applications (4) related to multibeam scanning electron microscopy (MB-SEM). We are developing MB-SEM methodology in the [Hoogenboom](https://www.hoogenboomlab.org/) and [Kruit](https://www.tudelft.nl/en/faculty-of-applied-sciences/about-faculty/departments/imphys/people/pieter-kruit/) lab at the department of Imaging Physics, TU Delft. We apply MB-SEM in the field of [volume electron microscopy](https://www.azooptics.com/Article.aspx?ArticleID=1504). With this platform, we want to stimulate other researchers interested in MB-SEM to join us in further developing the technique. Our methods will be freely available and reusable. 

Key goals of the project:
- Open sharing of (raw) data, methods, publications about MB-SEM.
- Interactive, out-of-the-box deployable code with documentation
- Interactive data viewing in 3D
- Inviting other researchers to join us in further developing MB-SEM

## 1 About MB-SEM
Multibeam scanning electron microscopy (MB-SEM) is a new microscopy technique in which a sample is scanned by multiple beams in parallel. Therefore, the throughput of the microscope scales with the number of beams. At TU Delft, a multibeam microscope has been developed that is dedicated to imaging of biological tissue. You can read more about the microscopy technique [in this publication](https://avs.scitation.org/doi/10.1116/1.4966216) and on the [manufacturer's website](https://www.delmic.com/en/products/fast-imaging/fast-em).

<img src="https://raw.githubusercontent.com/arentkievits/MB-SEM/main/workflow.png" width=30% height=30%>

### 1.1 Volume electron microscopy
Volume electron microscopy comprises all methods for imaging biological tissue in 3D. If you want to know more about the research field, we encourage to read these very informative literature reviews:

- Volume electron microscopy: [Peddie & Collinson (2014)](https://www.sciencedirect.com/science/article/pii/S0968432814000250), [Titze & Genoud (2016)](https://onlinelibrary.wiley.com/doi/abs/10.1111/boc.201600024)
- About connectomics and the use of MB-SEM: [Kornfeld & Denk (2018)](https://onlinelibrary.wiley.com/doi/full/10.1111/boc.201600024), [Eberle & Zeidler (2018)](https://www.frontiersin.org/articles/10.3389/fnana.2018.00112/full)

### 1.2 Characterization of the MB-SEM detection method
Our implementation of MB-SEM makes use of a new detection method called optical scanning transmission electron microscopy (OSTEM). If you would like to see characterization of this method and how it performs in relation to conventional detection techniques (e.g. backscatter electron detection), you can go to the [repository for single-beam optical scannning transmission electron microscopy](https://github.com/arentkievits/sb_optical_STEM). We are working on making this an interactive environment that you can set up yourself using Conda (Python) (TODO). 

## 2 Data
Our microscopy data is currently available on our TU Delft server [Sonic](https://sonic.tnw.tudelft.nl/catmaid/) which runs an instance of CATMAID (Saalfeld, S., et al. (2009)). We plan to also upload data related to publications to EMPIAR. MB-SEM demonstration data can be viewed under the header 'FAST-EM'.

## 3 Methods
We are developing the following methods:

### 3.1 Acquisition workflow for MB-SEM
We are currently developing an acquisition workflow for a commercial MB-SEM system at TU Delft. We will share this work in a separate repository later (TODO). 

### 3.2 Automated segmentation and fluorescence prediction
In the future we hope to share with you new methods for automated segmentation and label-free prediction of fluorescence on MB-SEM data. We will train convolutional neural networks and share them on [Bioimage Model Zoo](https://bioimage.io/). (TODO)

## 4 Applications
We will apply our methods to several demonstration projects and large-scale applications. (TODO)

## References
Stephan Saalfeld, Albert Cardona, Volker Hartenstein, Pavel Tomančák, CATMAID: collaborative annotation toolkit for massive amounts of image data, Bioinformatics, Volume 25, Issue 15, 1 August 2009, Pages 1984–1986, https://doi.org/10.1093/bioinformatics/btp266

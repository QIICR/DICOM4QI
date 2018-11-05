In this task we provide a dataset that consists of the two imaging series corresponding to the two time points in visualizing certain imaging finding. Each of these imaging series are accompanied by the volumetric segmentation \(as DICOM SEG\) and segmentation-derived measurements \(as DICOM TID1500 documents\).

The task is to demonstrate how the tool presents to the user the longitudinal aspect of finding measurement.

## Tasks for participants

1. **Description of the platform/product**:
   * **name and version of the software** used for testing
   * **free?** if yes - include the download link
   * **commercial?** if yes - include the home page for the product
   * **open source?** if yes - provide a link to source code
   * **what DICOM library do you use?** - if you use certain DICOM toolkit to support this functionality, please list it, if possible
2. **Description of the relevant features of the platform**:
   * **hanging protocol**: what are the options you provide to the user in visualizing multiple time points?
   * **plotting**: do you have an option to plot changes in measurements?
   * **handling multiple timepoints/measurements/findings**: how do you handle increasing number of timepoints? measurements? findings?
   * **human-readable report**: do you support export of a human readable printable report \(HTML/PDF\) summarizing longitudinal changes?
3. **Read task** \(for each dataset!\)
   * load each of the datasets that accompany the imaging series into your platform
   * submit a screenshot demonstrating the presentation of the loaded measurements to the user by email to Andrey Fedorov

### Test dataset #1

This is a dataset encoding the changes in morphology of a lung lesion over two CT imaging sessions. The source of this dataset is the [TCIA RIDER-LungCT collection](https://wiki.cancerimagingarchive.net/display/Public/RIDER+Lung+CT) \(subject RIDER-1500037140\).

Download the ZIP archive containing 2 CT series, 2 SEG series, and 2 SR series [here](http://slicer.kitware.com/midas3/download/item/313148/RIDER-1500037140.zip).

Screenshots below show the location of the lesion, and the measurements stored in the SR objects, as displayed using 3D Slicer QuantitativeReporting extension.

** Time point 1 **

<img src="/assets/RIDER-1500037140-1.jpg">

** Time point 2 **

<img src="/assets/RIDER-1500037140-2.jpg">

#### Citations

The CT series from Test dataset \#1 are accompanied by the following citations.

**Data Citation**

Zhao, Binsheng, Schwartz, Lawrence H, & Kris, Mark G. \(2015\). Data From RIDER\_Lung CT. The Cancer Imaging Archive. [http://doi.org/10.7937/K9/TCIA.2015.U1X8A5NR](http://doi.org/10.7937/K9/TCIA.2015.U1X8A5NR)

**Publication Citation**

Zhao, B., James, L. P., Moskowitz, C. S., Guo, P., Ginsberg, M. S., Lefkowitz, R. A., … Schwartz, L. H. \(2009, July\). Evaluating Variability in Tumor Measurements from Same-day Repeat CT Scans of Patients with Non–Small Cell Lung Cancer 1 . Radiology. Radiological Society of North America \(RSNA\). [http://doi.org/10.1148/radiol.2522081593](http://doi.org/10.1148/radiol.2522081593) \([paper](http://pubs.rsna.org/doi/abs/10.1148/radiol.2522081593)\)

**TCIA Citation**

Clark K, Vendt B, Smith K, Freymann J, Kirby J, Koppel P, Moore S, Phillips S, Maffitt D, Pringle M, Tarbox L, Prior F. The Cancer Imaging Archive \(TCIA\): Maintaining and Operating a Public Information Repository, Journal of Digital Imaging, Volume 26, Number 6, December, 2013, pp 1045-1057. \([paper](http://link.springer.com/article/10.1007%2Fs10278-013-9622-7)\)

### Test dataset #2

QIN-PROSTATE-Repeatability - TODO!

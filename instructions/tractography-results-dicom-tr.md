# Tractography results

## Overview

The purpose of this task is to demonstrate support of the [DICOM Tractography Results](ftp://medical.nema.org/medical/dicom/final/sup181_ft_TractographyResultsStorage.pdf) (DICOM TR) object. 

The basic read task involves loading the existing DICOM TR object, and demonstrating visualization of the tractography relative to the reference image.

The write task involves generation of tractography streamlines from the provided Diffusion Weighted Image DICOM files and storing the result as a DICOM TR object. Note that this task does not seek to compare tractography algorithms, evaluate medical or neuroanatomic accuracy or usefulness of results, etc. *The only question of interest is interchange of DICOM TR objects between systems.*

## Tasks for participants

1. **Description of the platform/product**:
 * **name and version of the software** used for testing
 * **free?** if yes - include the download link
 * **commercial?** if yes - include the home page for the product
 * **open source?** if yes - provide a link to source code
 * **what DICOM library do you use?** - if you use certain DICOM toolkit to support this functionality, please list it, if possible

 * **Description of the relevant features of the platform**: 
    * are multiple tracksets supported in a single file?
    * do you support any ancillary


3. **Read task** (for each dataset!)
 * load each of the DICOM TR datasets that accompany the imaging series into your platform
 * submit a screenshot demonstrating the overlay of the segmentation on the B0 series, and any other components of the user interface (e.g., presentation of the ROI semantics to the user, communication of the algorithm metadata) by email to Andrey Fedorov and Isaiah Norton. (screenshots will be included in the results page alongside these responses).

4. **Write tasks**
 * **Single trackset**: select a tractography streamline bundle using any method available in your platform.
 *  **Multiple tracksets**: segment any two streamline bundles using any method available in your platform (non-intersecting). Make sure to create separate segment for each of the segmented areas!
 * save the result as DICOM TR; if possible, please include in the series description the name of your tool to simplify comparison tasks!
 * as part of quick checks, confirm that the resulting TR object has the same FrameOfReferenceUID as the reference image
 * [UPLOAD THE RESULTING DICOM TR FILES AND SCREENSHOTS HERE](https://www.dropbox.com/request/XvwJrx22BxMxx6EcIZr3). (data will be publicly accessible after upload)
 
Note: (1) we are not assessing accuracy or usefulness of tractography streamlines, any method is  good; (2) the screenshots and the DICOM TR objects you submit will be distributed publicly and included in this document in the Results section.

** Diffusion Weighted Image Source Datasets

### DWI dataset #1

The imaging dataset is a diffusion weighted image of a human brain acquired on a Siemens Verio (1 B0 and 6 gradient directions; stock sequence; mosaic OFF; CSA header private tags preserved during anonymization). Data credit: O'Donnell Group, Laboratory of Mathematics in Imaging, Brigham & Women's Hospital.

### DWI dataset #2

The imaging dataset is a diffusion weighted image of a human brain acquired on a Siemens Trio (mosaic off; no CSA header present). Data credit: University of Iowa BRAINS project, DWIConvert test dataset. ([metadata and license](http://slicer.kitware.com/midas3/item/93005))

[Download link](http://slicer.kitware.com/midas3/download/?items=93005,1)

### DWI dataset #3

The imaging dataset is a diffusion weighted image of a human brain acquired on a 3T GE Signa HDx. Data credit: University of Iowa BRAINS project, DWIConvert test dataset ([metadata and license](http://slicer.kitware.com/midas3/item/92995)).

[Download link](http://slicer.kitware.com/midas3/download/?items=92995,1)

**Generated Tractography Result datasets**

Download the DICOM TR datasets produced by the platforms that already submitted results (data is organized in subfolders corresponding to the individual platforms):

[DOWNLOAD LINK](https://www.dropbox.com/sh/gmy2nt1mlfk1k2w/AADIdfcLUUZ8ViAh7i6x0aana?dl=0)


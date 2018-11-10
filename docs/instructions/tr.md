!!! info
    When ready to submit, use the [DICOM4QI Submission Google Form](http://bit.ly/dicom4qi-submit)

The purpose of this task is to demonstrate support of the [DICOM Tractography Results](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_A.78.html) \(DICOM TR\) object.

The basic read task involves loading the existing DICOM TR object, and demonstrating visualization of the tractography relative to the reference image.

The write task involves generation of tractography streamlines from the provided Diffusion Weighted Image DICOM files and storing the result as a DICOM TR object.

!!! note
    This task does not seek to compare tractography algorithms, evaluate medical or neuroanatomic accuracy or usefulness of results, etc. _The only question of interest is interchange of DICOM TR objects between systems._

    The screenshots and the DICOM TR objects you submit will be distributed publicly and included in this document in the Results section.

!!! info
    * all DWI datasets are organized in [this Dropbox folder](https://www.dropbox.com/sh/qv1mo5lg5bzykps/AAB721QJ1VjZUm4oUSAleHsWa?dl=1)
    * submit the resulting screenshots and datasets by uploading the zip file with the screenshots and resulting objects to [this Dropbox FileRequests location](https://www.dropbox.com/request/XvwJrx22BxMxx6EcIZr3). Make sure that the file is named to include the name of your platform!

## Read task

Load each of the DICOM TR datasets that accompany the imaging series into your platform, and submit the following screenshots:

* demonstrate the 2D overlay of the track sets on the B0 series (if possible)
* demonstrate several 3D perspectives (if possible)
* demonstrate any other components of the user interface (e.g., presentation of the associated measurements, communication of the algorithm metadata).

## Write task

Single trackset:

* select a tractography streamline bundle using any method available in your platform.

Multiple tracksets:

* select any two streamline bundles using any method available in your platform (non-intersecting). Make sure to create separate trackset for each of the segmented areas!
* save the results as DICOM TR; if possible, please include in the series description the name of your tool to simplify comparison tasks!
* as part of quick checks, confirm that the resulting TR object has the same FrameOfReferenceUID as the reference image


### DWI dataset #1

The imaging dataset is a diffusion weighted image of a human brain acquired on a Siemens Verio \(1 B0 and 6 gradient directions; stock sequence; mosaic OFF; CSA header private tags preserved during anonymization\). Data credit: O'Donnell Group, Laboratory of Mathematics in Imaging, Brigham & Women's Hospital.

### DWI dataset #2

The imaging dataset is a diffusion weighted image of a human brain acquired on a Siemens Trio \(mosaic off; no CSA header present\). Data credit: University of Iowa BRAINS project, DWIConvert test dataset. \([source, metadata, and license](http://slicer.kitware.com/midas3/item/93005)\)

### DWI dataset #3

The imaging dataset is a diffusion weighted image of a human brain acquired on a 3T GE Signa HDx. Data credit: University of Iowa BRAINS project, DWIConvert test dataset \([source, metadata, and license](http://slicer.kitware.com/midas3/item/92995)\).

### Generated Tractography Result datasets

Download the DICOM TR datasets produced by the platforms that already submitted results \(data is organized in subfolders corresponding to the individual platforms\):

[LINK TO RESULTS DOWNLOAD FOLDER](https://www.dropbox.com/sh/gmy2nt1mlfk1k2w/AADIdfcLUUZ8ViAh7i6x0aana?dl=0)

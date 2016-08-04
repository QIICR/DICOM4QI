# Segmentations (DICOM SEG)



Tasks for participants:

1. **Description of the relevant features of the platform**: 
 * are both single and multiple segments supported? how are the overlapping segments handled? 
 * do you support both BINARY and FRACTIONAL segmentation types? 
 * do you render the segment using the color specified in the DICOM object? 
 * how do you communicate segment semantics to the user? 
 * how do you support the user in defining the semantics of the object at the time segmentation is created?

2. **Read task** 
 * load each of the DICOM SEG datasets that accompany the imaging series into your platform
 * submit a screenshot demonstrating the overlay of the segmentation on the CT series, and any other components of the user interface (e.g., presentation of the ROI semantics to the user, communication of the algorithm metadata) by email to Andrey Fedorov

3. **Write task**
 * segment the lung lesion using any method available in your platform
 * save the result as DICOM SEG
 * run [dciodvfy DICOM validator](http://www.dclunie.com/dicom3tools/dciodvfy.html) 
 * send the resulting object and the result of **dciodvfy**, explaining any discrepancies found, to Andrey Fedorov by email
 
Note: (1) we are not assessing the accuracy of lesion segmentation, any method is  good; (2) the screenshots and the DICOM SEG objects you submit will be distributed publicly and included in this document in the Results section.

### Test dataset #1

The imaging dataset is a chest CT with a single lung lesion located in the right lung lobe. This dataset is subject LIDC-IDRI-0314 from The Cancer Imaging Archive ([TCIA](http://www.cancerimagingarchive.net/)) [LIDC-IDRI](https://wiki.cancerimagingarchive.net/display/Public/LIDC-IDRI) collection.

**Image dataset**

Download the zip archive of the CT series [here](http://slicer.kitware.com/midas3/download/item/245513/LIDC-IDRI-0314-CT.zip). The location of the lesion is highlighted below.

<img src="../images/LIDC-IDRI-0314_screenshot.png" width="250">

**Segmentation datasets**

Download the DICOM SEG datasets produced by the platforms that already submitted results [here](http://slicer.kitware.com/midas3/folder/3774) (data is organized in subfolders corresponding to the individual platforms).


### Test dataset #2

The imaging dataset consists of a PET and CT series for subject QIN-HEADNECK-01-0024 from the TCIA [QIN-HEADNECK](https://wiki.cancerimagingarchive.net/display/Public/QIN-HEADNECK) collection. This data set contains two lesions. This allows to test that the platform can handle more than one segment.

**Image dataset**

Download the zip archive of the CT series [here](http://slicer.kitware.com/midas3/download/item/245508/QIN-HEADNECK-01-0024-CT.zip), and PET series [here](http://slicer.kitware.com/midas3/download/item/245509/QIN-HEADNECK-01-0024-PET.zip). Lesions are more prominent on the PET series, as shown in the screenshot below.

<img src="../images/QIN-HEADNECK-01-0024_screenshot.png" width="250">

**Segmentation datasets**

Download the DICOM SEG datasets produced by the platforms that already submitted results [here](http://slicer.kitware.com/midas3/folder/3786) (data is organized in subfolders corresponding to the individual platforms).
# Segmentations (DICOM SEG)

### Test dataset #1

The imaging dataset is a chest CT with a lung lesion located in the right lung lobe. This dataset is subject LIDC-IDRI-0314 from The Cancer Imaging Archive ([TCIA](http://www.cancerimagingarchive.net/)) [LIDC-IDRI](https://wiki.cancerimagingarchive.net/display/Public/LIDC-IDRI) collection.

**Tasks for participants**

Your submission **must** include the details about the version of the platform you used to generate the results (name, version). If your platform is available publicly, please include access instructions.

1. **Read task**: load each of the DICOM SEG datasets that accompany the imaging series into your platform. Submit the screenshot demonstrating the overlay of the segmentation on the CT series, and any other components of the user interface (e.g., presentation of the ROI semantics to the user, communication of the algorithm metadata), to Andrey Fedorov.

2. **Write task**: segment the lung lesion using any method available in your platform. Save the result as DICOM SEG. Send the result to Andrey Fedorov. 
 
Note: (1) we are not assessing the accuracy of lesion segmentation, any method is as good; (2) the screenshots and the DICOM SEG objects you submit will be distributed publicly and included in this report.

**Test data**

Download the zip archive of the CT series [here](http://slicer.kitware.com/midas3/download/item/245513/LIDC-IDRI-0314-CT.zip). The location of the lesion is highlighted below.

<img src="../images/LIDC-IDRI-0314_screenshot.png" width="250">

Download the DICOM SEG datasets produced by the platforms that already submitted results [here](http://slicer.kitware.com/midas3/folder/3774) (data is organized in subfolders corresponding to the individual platforms).

### Test dataset #2


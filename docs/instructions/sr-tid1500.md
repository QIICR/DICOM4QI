The purpose of this task is to demonstrate support of the DICOM Structured Reporting template TID1500 \(DICOM TID1500\) for storing measurements derived from volumetric segmentations.

The basic read task involves loading the existing DICOM TID1500 object \(ideally, in the context of the source image series and the segmentation used to derived that measurement\), and demonstrating the user interface presenting the loaded measurements.

Write task involves generation of a new DICOM TID1500 dataset for a specified combination of the input image series and the volumetric segmentation defined as DICOM SEG.

## Tasks for participants

1. **Description of the platform/product**:
   * **name and version of the software** used for testing
   * **free?** if yes - include the download link
   * **commercial?** if yes - include the home page for the product
   * **open source?** if yes - provide a link to source code
   * **what DICOM library do you use?** - if you use certain DICOM toolkit to support this functionality, please list it, if possible
   * **Description of the relevant features of the platform**:
     * please provide the screenshot of the user interface for the functionality specific to creating/displaying measurements
     * how do you communicate measurement semantics to the user?
2. **Read task** \(for each dataset!\)
   * load each of the DICOM SR datasets that accompany the imaging series into your platform
   * submit a screenshot demonstrating the presentation of the loaded measurements to the user by email to Andrey Fedorov
3. **Write tasks**
   * given the image series and the segmentation defining the ROI, calculate any measurements over the ROI and save as DICOM SR following TID1500 reporting template
   * run [dciodvfy DICOM validator](http://www.dclunie.com/dicom3tools/dciodvfy.html) and [Pixelmed DicomSRValidator](http://www.pixelmed.com/dicomtoolkit.html); iterate on resolving the identified issues as necessary
   * send the resulting objects and the results of **dciodvfy** and **DicomSRValidator**, explaining any discrepancies found, to Andrey Fedorov by email

Note: the screenshots and the DICOM objects you submit will be distributed publicly and included in this document in the Results section.

### Test dataset #1

This is a dataset consisting of 3 slices of a [liver CT series](http://slicer.kitware.com/midas3/download/item/257238/liver-3slices-CT.zip), and rough [segmentation of the liver defining ROI](http://slicer.kitware.com/midas3/download/item/257239/liver.dcm) for calculating the measurements.

The [SR dataset](http://slicer.kitware.com/midas3/download/item/257240/sr-tid1500-ct-liver-example.dcm) contains measurements calculated over the segmentation from the CT slices.

The measurements stored in the SR dataset are the following:

* Mean Attenuation Coefficient = 37.3289 Hounsfeld Units
* Minimum Attenuation Coefficient = -778 Hounsfeld Units
* Maximum Attenuation Coefficient = 221 Hounsfeld Units
* Standard Deviation of Attenuation Coefficient = 59.1691 Hounsfeld Units
* Volume = 70361.9 cubic millimeter
* Volume = 70.3619 cubic centimeter

### Test dataset #2

[This SR dataset](http://slicer.kitware.com/midas3/download/item/262094/Measurements_User2_SemiAuto_Trial2.dcm) contains measurements over the segmentations of tumor and "hot" lymph nodes in [SEG Test dataset #3](/instructions/seg/#test-dataset-3).

The types of measurements stored in this object are described in detail in [this article](https://peerj.com/articles/2057/). There is a separate group of measurements for each of the segments in the referenced segmentation object.

### Test dataset #3

Radiomics features - TODO!

### Test dataset #4

Planar measurements - TODO!

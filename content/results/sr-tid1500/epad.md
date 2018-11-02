1.**Description of the platform/product**:

* **name and version of the software**: ePAD, version 2.4
* **free?** yes [https://epad.stanford.edu/epad-agreement](https://epad.stanford.edu/epad-agreement)
* **commercial?** no
* **open source?** yes except plugins and UI project github.com/RubinLab/
* **what DICOM library do you use?** [PixelMed](http://www.pixelmed.com/), [DCM4CHE](http://www.dcm4che.org/), [QIICR/dcmqi](https://github.com/QIICR/dcmqi)

ePAD works with AIM files and supports importing and exporting DICOM SR TID1500 files. When the user uploads a DICOM SR TID1500 file, it is read using the tid1500reader tool from QIICR/dcmqi and an AIM file is constructed with the information present in the file. When the user downloads an annotation, \(s\)he can choose to download the DICOM files related to that annotation, which will automatically convert the AIM file to QIICR/dcmqi metadata json file, use tid1500writer to write DICOM SR TID1500 file and download it \(see screenshot below showing the download options for an annotation\).

![](../../.gitbook/assets/epadsr_downloadaim.png)

2.**Description of the relevant features of the platform**:

* **please provide the screenshot of the user interface for the functionality specific to creating/displaying measurements** For each segmentation or ROI, ePAD calculates the min, max, mean and standard deviation. The plugins can calculate and save more calculations but the user doesn't have any other way to select/add/remove calculations. The calculations for geometric shape ROIs are shown on the UI in the label of the annotation but at the moment \(Nov 2016\), the calculations for segmentations are not displayed on UI. The only way to see them is downloading the AIM file \(see screenshot below showing the calculations label for a geometric ROI, a spline\).

  ![](../epad/epadsr_roi.png)

* **how do you communicate measurement semantics to the user?** user has no meaning to easily get information about the semantics of the segmentation measurements from the UI. The semantics are stored in the AIM file \(see screenshot below showing the mean calculation in the aim file\).

  ![](../epad/epadsr_mean.png)

3.**Read task**:

**Test dataset \#1**

| Info | Screenshot |
| -- | -- |
| DICOM SR converted to AIM and loaded in ePAD | <img src="../epad/epadsr_loaded.png" width=250> |
| DICOM SR AIM shown in ePAD | <img src="../epad/epadsr_segmentation.png" width=250> |
| AIM with calculations| <img src="../epad/epadsr_aim.png" width=250>

**Test dataset \#2**

At this time \(Nov 2016\), ePAD does not support multi-segment segmentations.

4.**Write task**

* given the image series and the segmentation defining the ROI, calculate any measurements over the ROI and save as DICOM SR following TID1500 reporting template
  * Min, max, mean and standard deviation is calculated
* run [dciodvfy DICOM validator](http://www.dclunie.com/dicom3tools/dciodvfy.html) and Pixelmed DicomSRValidator; iterate on resolving the identified issues as necessary
* send the resulting objects and the results of dciodvfy and DicomSRValidator, explaining any discrepancies found, to Andrey Fedorov by email
  * results are sent
  * no errors, only warnings from dciodvfy.
  * Context group not found error in Pixelmed DicomSRValidator. The test dataset has the same error.

```text
Error: Template 1500 MeasurementReport/[Row 1] CONTAINER CID 7021/[Row 4] CODE (121058,DCM,"Procedure reported"): 1.4: /CONTAINER (126000,DCM,"Imaging Measurement Report")/CODE (121058,DCM,"Procedure reported"): Code (P0-0099A,SRT,"Imaging procedure") not found in context group 100
```

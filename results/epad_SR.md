# ePAD

1.**Description of the platform/product**:
 * **name and version of the software**: ePAD, version 2.4
 * **free?** yes https://epad.stanford.edu/epad-agreement
 * **commercial?** no
 * **open source?** yes except plugins and UI project github.com/RubinLab/
 * **what DICOM library do you use?** [PixelMed](http://www.pixelmed.com/), [DCM4CHE](http://www.dcm4che.org/), [QIICR/dcmqi](https://github.com/QIICR/dcmqi)

ePAD works with aim files and supports importing and exporting DicomSR files. When the user uploads a DicomSR file, it is read using the tid1500reader tool from QIICR/dcmqi and an aim file is constructed with the information present in the file. When the user downloads an annotation, (s)he can choose to download the DICOM files related to that annotation, which will automatically convert the aim file to QIICR/dcmqi metadata json file, use tid1500writer to write DicomSR file and download it.

2.**Description of the relevant features of the platform**: 
 * **please provide the screenshot of the user interface for the functionality specific to creating/displaying measurements** For each segmentation or ROI, ePAD calculates the min, max, mean and standard deviation. The plugins can calculate and save more calculations but the user doesn't have any other way to select/add/remove calculations. The calculations for geometric shape ROIs are shown on the UI in the label of the annotation but at the moment (Nov 2016), the calculations for segmentations are not displayed on UI. The only way to see them is downloading the aim file. 
 
 * **how do you communicate measurement semantics to the user?** user has no meaning to easily get information about the semantics of the measurement from the UI. The semantics are stored in the aim file.

3.**Read task**: load each of the DICOM SR datasets that accompany the imaging series into your platform
submit a screenshot demonstrating the presentation of the loaded measurements to the user by email to Andrey Fedorov

**Test dataset #1**

| State | Screenshot |
| -- | -- |
| DicomSR converted to aim and loaded in ePAD | <img src="./images/epadsr_loaded.png" width=250> |
| DicomSR aim shown in ePAD | <img src="./images/epadsr_segmentation.png" width=250> |
| Download aim | <img src="./images/dicomsr_downloadaim.png" width=250> |
| Aim with calculations| <img src="./images/epadsr_aim.png" width=250> 

**Test dataset #2**

At this time (Nov 2016), ePAD does not support multi-segment segmentations.

4.**Write task**
 * given the image series and the segmentation defining the ROI, calculate any measurements over the ROI and save as DICOM SR following TID1500 reporting template
   * Min, max, mean and standard deviation is calculated
 * run [dciodvfy DICOM validator](http://www.dclunie.com/dicom3tools/dciodvfy.html) and Pixelmed DicomSRValidator; iterate on resolving the identified issues as necessary
 * send the resulting objects and the results of dciodvfy and DicomSRValidator, explaining any discrepancies found, to Andrey Fedorov by email
   * results are sent
   * no errors, only warnings from dciodvfy. 
   * Context group not found error in Pixelmed DicomSRValidator. The test dataset has the same error.
     * Error: Template 1500 MeasurementReport/[Row 1] CONTAINER CID 7021/[Row 4] CODE (121058,DCM,"Procedure reported"): 1.4: /CONTAINER (126000,DCM,"Imaging Measurement Report")/CODE (121058,DCM,"Procedure reported"): Code (P0-0099A,SRT,"Imaging procedure") not found in context group 100




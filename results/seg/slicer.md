# 3D Slicer

## Description of the platform

1. **Description of the platform/product**:
 * **name and version of the software**: 3D Slicer, Nightly release 4.5.0-2016-08-04, with Reporting Extension installed
 * **free?** yes http://download.slicer.org
 * **commercial?** no
 * **open source?** yes http://github.com/slicer/slicer

2. **Description of the relevant features of the platform**: 
 * are both single and multiple segments supported? how are the overlapping segments handled? 
 * do you support both BINARY and FRACTIONAL segmentation types? 
 * do you render the segment using the color specified in the DICOM object? 
 * how do you communicate segment semantics to the user? 
 * how do you support the user in defining the semantics of the object at the time segmentation is created?

3. **Read task** 
 * load each of the DICOM SEG datasets that accompany the imaging series into your platform
 * submit a screenshot demonstrating the overlay of the segmentation on the CT series, and any other components of the user interface (e.g., presentation of the ROI semantics to the user, communication of the algorithm metadata) by email to Andrey Fedorov

4. **Write task**
 * segment the lung lesion using any method available in your platform
 * save the result as DICOM SEG; please include in the series description the name of your tool to simplify comparison tasks!
 * run [dciodvfy DICOM validator](http://www.dclunie.com/dicom3tools/dciodvfy.html); iterate on resolving the identified issues as necessary
 * send the resulting object and the result of **dciodvfy**, explaining any discrepancies found, to Andrey Fedorov by email



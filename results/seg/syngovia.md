# Siemens syngo.via

**DISCLAIMER: This section was completed by Andrey Fedorov using the version of software installed at Brigham and Women's Hospital. Representatives of Siemens were not involved in the presented evaluation.**

1.**Description of the platform/product**:
 * **name and version of the software**: Siemens syngo.via VB10B, MM Oncology workflow
 * **free?** no
 * **commercial?** yes
 * **open source?** no 
 * **what DICOM library do you use?** not known

2.**Description of the relevant features of the platform**: 
 * **are both single and multiple segments supported?** it is not possible to load SEG objects created using tools other than syngo.via. However, visualization of multiple overlapping regions is supported as shown in the screenshot below.

<img src="./syngo/syngo-hnc139.png" width=450>

 * **how are the overlapping segments handled?** segments are shown as region contours

 * **do you support both BINARY and FRACTIONAL segmentation types?** not applicable, since loading is not supported
 * **do you render the segment using the color specified in the DICOM object?** not applicable, since loading is not supported
 * **how do you communicate segment semantics to the user?** It looks like the semantics of the created segments is implicitly defined by the workflow.
 * **how do you support the user in defining the semantics of the object at the time segmentation is created?** It does not look like this is possible.

3.**Read task**: load each of the DICOM SEG datasets that accompany the imaging series into your platform

**This task could not be completed, since no loading of externally created objects is supported.**


4.**Write task**

Segmentation was done for Test case 3, visualization is shown in the screenshot below. Note that each segment was stored as a separate object.

<img src="./syngo/syngo-hnc139.png" width=450>

Errors reported by `dciodvfy`:

`Error - Empty attribute (no value) Type 1C Conditional Element=<SegmentAlgorithmName> Module=<SegmentationImage>
Error - May not be present for Referenced SOP Class that is not multi-frame - attribute <ReferencedFrameNumber>`



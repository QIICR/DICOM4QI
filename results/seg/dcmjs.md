
# dcmjs


**Note:** [dcmjs](http://github.com/pieper/dcmjs
) is a new library created from scratch to handle DICOM data manipulation in pure JavaScript.  It is currently able to convert to and from binary (part 10) DICOM and JavaScript objects.  Use the github project for issues and questions or contact Steve Pieper (pieper@isomics.com).

1.
**Description of the platform/product**:
 * **name and version of the software**: dcmjs alpha version
 * **free?** yes http://github.com/pieper/dcmjs
 * **commercial?** can be used in commercial projects
 * **open source?** yes, MIT license
 * **what DICOM library do you use?** pure JavaScript implementation

2.**Description of the relevant features of the platform**: 
 * **are both single and multiple segments supported?** yes
 * **how are the overlapping segments handled?** loaded separately, displayed as cornerstone overlays
 * **do you support both BINARY and FRACTIONAL segmentation types?** can be loaded but not currently displayed
 * **do you render the segment using the color specified in the DICOM object?** yes
 * **how do you communicate segment semantics to the user?** Demo displays color, segment number, other info
 * **how do you support the user in defining the semantics of the object at the time segmentation is created?** currently requires writing code

3.**Read task**: load each of the DICOM SEG datasets that accompany the imaging series into your platform

See [live demo pulling qiicr data from TCIA](https://pieper.github.io/dcmjs/examples/qiicr/).

<img src="./dcmjs/dcmjs-qicr-tcia-seg.png" width=250>


**Test dataset #1**
TBD
**Test dataset #2**
TBD

**Test dataset #3**
TBD
**Test dataset #4**
TBD

4.**Write task**
TBD

For now a [simple live demo](https://pieper.github.io/dcmjs/examples/createSegmentation/index.html) exists to create a 
SEG and multiframe MR object from some sample data.  **Note that even though there are multiple frames
the segmentation is not correctly attached to the slice.  This is an issue with the demo and not the underlying library.**


<img src="./dcmjs/dcmjs-qicr-save-seg.png" width=250>

Example output [is available for download](https://drive.google.com/open?id=0Bygzw56l1ZC-TWRwSUo5MEF6TU0)

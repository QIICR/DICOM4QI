**Note:** [dcmjs](http://github.com/pieper/dcmjs) is a new library created from scratch to handle DICOM data manipulation in pure JavaScript.  It is currently able to convert to and from binary \(part 10\) DICOM and JavaScript objects.  Use the github project for issues and questions or contact Steve Pieper \(pieper@isomics.com\).

The core functionality of reading and writing segmentations is available but has not yet been verified with all datasets for the connectathon.

[Cornerstone](https://github.com/chafey/cornerstone) provides image display including overlay support for showing segmentations.

1. **Description of the platform/product**:
   * **name and version of the software**: dcmjs alpha version, cornerstone current git master
   * **free?** yes [http://github.com/pieper/dcmjs](http://github.com/pieper/dcmjs) and [https://github.com/chafey/cornerstone](https://github.com/chafey/cornerstone)
   * **commercial?** can be used in commercial projects
   * **open source?** yes, MIT license
   * **what DICOM library do you use?** pure JavaScript implementation, dcmjs

2.**Description of the relevant features of the platform**:

* **are both single and multiple segments supported?** yes
* **how are the overlapping segments handled?** loaded separately, displayed as cornerstone overlays
* **do you support both BINARY and FRACTIONAL segmentation types?** can be loaded but not currently displayed
* **do you render the segment using the color specified in the DICOM object?** yes
* **how do you communicate segment semantics to the user?** Demo displays color, segment number, other info
* **how do you support the user in defining the semantics of the object at the time segmentation is created?** currently requires writing code

3.**Read task**: load each of the DICOM SEG datasets that accompany the imaging series into your platform

See [live demo pulling qiicr data from TCIA](https://pieper.github.io/dcmjs/examples/qiicr/).

See [live demo allowing drag and drop of reference images and segmentations](https://pieper.github.io/dcmjs/examples/display2/).

![](../dcmjs/dcmjs-qiicr-tcia-seg.png)

Testing of the read tasks is underway.  Several incompatibilities need to be investigated.

**Test dataset \#1**  
TBD  
**Test dataset \#2**  
TBD

**Test dataset \#3**  
TBD  
**Test dataset \#4**  
TBD

 **Longitudinal Annotation dataset**

![](../dcmjs/dcmjs-rider-2017.png)

 **Freesurfer / Corticometrix dataset**

![](../dcmjs/dcmjs-freesurfer.png)

4.**Write task**

For now a [simple live demo](https://pieper.github.io/dcmjs/examples/createSegmentation/index.html) exists to create a SEG and multiframe MR object from some sample data.

Example output [is available for download](https://drive.google.com/open?id=0Bygzw56l1ZC-TWRwSUo5MEF6TU0)

![](../dcmjs/dcmjs-qiicr-save-seg.png)

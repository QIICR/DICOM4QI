# AMI

1.**Description of the platform/product:**

* **name and version of the software?** AMI \(Medical Imaging Javascript Toolkit\) - v0.0.12+
* **free?** yes
* **commercial?** no
* **opensource?** yes - \[Github repository\]\([https://github.com/FNNDSC/ami](https://github.com/FNNDSC/ami)
  * demo app: [https://fnndsc.github.io/ami/\#viewers\_labelmap](https://fnndsc.github.io/ami/#viewers_labelmap)
* **what DICOM library do you use?** [dicomParser](https://github.com/chafey/dicomParser)

2.**Description of the relevant features of the platform:**

* **are both single and multiple segments supported?** yes
* **how are the overlapping segments handled?** yes if loaded in separate files. No if overlapping segments are part of the same segmentation object.
* **do you support both BINARY and FRACTIONAL segmentation types?** only BINARY \(need test dataset for FRACTIONAL\)
* **do you render the segment using the color specified in the DICOM object?** yes
* **how do you communicate segment semantics to the user?** Developer/user can access per segment semantics \(recommendedDisplayCIELab, segmentationCodeDesignator, segmentationCodeValue, segmentationCodeMeaning, segmentNumber, segmentLabel, segmentAlgorithmType\) in the stack segmentationSegments object.
* _\*\*how do you support the user in defining the semantics of the object at the time segmentation is created?_ does not allow user to create segmentation objects. \(on roadmap\)

3.**Read task:**

**Test dataset \#1**

| Test dataset | Result of rendering |
| :--- | :--- |
| 3D Slicer |   |

**Test dataset \#2**

| Test dataset | Result of rendering |
| :--- | :--- |
| 3D Slicer |   |

**Test dataset \#3**

| Test dataset | Result of rendering |
| :--- | :--- |
| 3D Slicer |   |

**Test dataset \#4**

| Test dataset | Result of rendering |
| :--- | :--- |
| 3D Slicer |   |

4.**Write task:**

not supported at this time


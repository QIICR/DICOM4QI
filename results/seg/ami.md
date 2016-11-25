# AMI
1.**Description of the platform/product:**
  * **name and version of the software?** AMI (Medical Imaging Javascript Toolkit) - v0.0.12+
  * **free?** yes
  * **commercial?** no
  * **opensource?** yes - [Github repository](https://github.com/FNNDSC/ami)
  * **what DICOM library do you use?** [dicomParser](https://github.com/chafey/dicomParser)

2.**Description of the relevant features of the platform:**
  * **are both single and multiple segments supported?** yes
  * **how are the overlapping segments handled?** yes if loaded in separate files. No if overlapping segments are part of the same segmentation object.
  * **do you support both BINARY and FRACTIONAL segmentation types?** only BINARY (need test dataset for FRACTIONAL)
  * **do you render the segment using the color specified in the DICOM object?** yes
  * **how do you communicate segment semantics to the user?** Developer/user can access per segment semantics (recommendedDisplayCIELab, segmentationCodeDesignator, segmentationCodeValue, segmentationCodeMeaning, segmentNumber, segmentLabel, segmentAlgorithmType) in the stack segmentationSegments object.
  * ***how do you support the user in defining the semantics of the object at the time segmentation is created?* does not allow user to create segmentation objects. (on roadmap)

3.**Read task:**

**Test dataset #1**

| Test dataset   | Result of rendering                                                                                                  |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| 3D Slicer | <img src="https://cloud.githubusercontent.com/assets/214063/20626851/96583aba-b31c-11e6-94a0-bc036e1e9c04.jpg" alt="Drawing"  width="256" height="256"/> |

**Test dataset #2**

| Test dataset   | Result of rendering                                                                                                  |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| 3D Slicer | <img src="https://cloud.githubusercontent.com/assets/214063/20626850/9658091e-b31c-11e6-9324-259fc7ae194d.jpg" alt="Drawing"  width="256" height="256"/> |

**Test dataset #3**

| Test dataset   | Result of rendering                                                                                                  |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| 3D Slicer | <img src="https://cloud.githubusercontent.com/assets/214063/20626852/965a1394-b31c-11e6-8a7b-ec81de4196ee.jpg" alt="Drawing"  width="256" height="256"/> |

**Test dataset #4**

| Test dataset   | Result of rendering                                                                                                  |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| 3D Slicer | <img src="https://cloud.githubusercontent.com/assets/214063/20626853/965b40ca-b31c-11e6-83e5-b57537cafaf6.jpg" alt="Drawing"  width="256" height="256"/> |

4.**Write task:**

not supported at this time
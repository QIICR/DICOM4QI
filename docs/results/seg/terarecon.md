1.**Description of the platform/product**:

* **name and version of the software**: iNtuition - 4.4.13.P4 (pre-release version)
* **free?** no
* **commercial?** yes (https://www.terarecon.com)
* **open source?** no
* **what DICOM library do you use?** Merge toolkit

2.**Description of the relevant features of the platform**:

* **are both single and multiple segments supported?** no, single segment only, read operation only

* **do you support both BINARY and FRACTIONAL segmentation types?** no
* **do you render the segment using the color specified in the DICOM object?** yes
* **how do you communicate segment semantics to the user?** Display of the segment semantics is provided in specialized Slicer modules. As of November 2016, semantics is shown in a tooltip over the color swatch in the list of segments in Segment Editor module \(see screenshot below\). Similar interface is provided in the Reporting module.

* **how do you support the user in defining the semantics of the object at the time segmentation is created?** Once the DICOM Seg objects are received and stored via DICOM C-Store, the application allows the user to visualize the segments as a color overlay along with the segment labels on the referenced DICOM Images. Further the application allows the user to add, subtract or modify the segments as needed to complete the segmentation review and the clinical workflow   

3.**Read task**: load each of the DICOM SEG datasets that accompany the imaging series into your platform

**Test dataset \#1**

<img src="../Terarecon/terarecon-seg-d1-1.jpg" width="50%">

<img src="../Terarecon/terarecon-seg-d1-2.jpg" width="50%">

**Test dataset \#2**

N/A

**Test dataset \#3**

N/A

**Test dataset \#4**

<img src="../Terarecon/terarecon-seg-d4-1.jpg" width="50%">

<img src="../Terarecon/terarecon-seg-d4-2.jpg" width="50%">

**Test dataset 5**

N/A

**Test dataset 6**

N/A

4. **Write task**

At the moment, only reading is supported.

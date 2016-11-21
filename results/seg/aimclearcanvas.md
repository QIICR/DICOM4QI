# AIM on ClearCanvas

1.**Description of the platform/product**:
 * **name and version of the software**: AIM ClearCanvas DICOM Viewer v4.6.0.4
 * **free?** yes http://www.ict.mahidol.ac.th/research/Imaging-Informatics/index
 * **commercial?** no
 * **open source?** a version of the software source code is available at https://github.com/NCIP/annotation-and-image-markup
 * **what DICOM library do you use?** [DCMTK](http://dcmtk.org)

2.**Description of the relevant features of the platform**: 
 * **are both single and multiple segments supported?** yes 
 * **how are the overlapping segments handled?** semi-transparent color overlay (see screenshot below showing both AIMonClearCanvas and Brainlab datasets from the Read task)

<img src="clearcanvas/seg-overlap.png" width=250>

 * **do you support both BINARY and FRACTIONAL segmentation types?** only BINARY can be displayed; SEGs that are saved as FRACTIONAL will be read as BINARY (i.e., no mapping to fractional occupancy or probability will be done)
 * **do you render the segment using the color specified in the DICOM object?** yes
 * **how do you communicate segment semantics to the user?** the user can trigger display of the panel showing the semantic information for the displayed segment (see screenshot below)

<img src="clearcanvas/semantics-ui.png" width=250>

 * **how do you support the user in defining the semantics of the object at the time segmentation is created?** user can select from a pre-defined list of terms

3.**Read task**: load each of the DICOM SEG datasets that accompany the imaging series into your platform

**Test dataset #1**

| Test dataset | Result of rendering |
| -- | -- |
| 3D Slicer | <img src="./slicer/slicer-read-lidc.png" width=250> |


**Test dataset #2**

| Test dataset | Result of rendering |
| -- | -- |
| 3D Slicer | <img src="./slicer/slicer-read-hnc24.png" width=250> |

**Test dataset #3**

| Test dataset | Result of rendering |
| -- | -- |
| 3D Slicer | <img src="./slicer/slicer-read-hnc139.png" width=250> |



4.**Write task**
 * segment the lung lesion using any method available in your platform; save the result as DICOM SEG; please include in the series description the name of your tool to simplify comparison tasks!
   * results are uploaded
 * run [dciodvfy DICOM validator](http://www.dclunie.com/dicom3tools/dciodvfy.html); iterate on resolving the identified issues as necessary
   * no errors, only warnings from dciodvfy


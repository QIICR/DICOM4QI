# ePAD

1.**Description of the platform/product**:
 * **name and version of the software**: ePAD, version 2.2
 * **free?** yes https://epad.stanford.edu/epad-agreement
 * **commercial?** no
 * **open source?** yes except plugins and UI project github.com/RubinLab/
 * **what DICOM library do you use?** [PixelMed](http://www.pixelmed.com/), [DCM4CHE](http://www.dcm4che.org/)

2.**Description of the relevant features of the platform**: 
 * **are both single and multiple segments supported?** yes for reading, writing is only supported for single segment  **how are the overlapping segments handled?**user can select either to view the outline or as filled (see screenshot below showing both AIMonClearCanvas and Slicer datasets from the Read task)

<img src="slicer/seg-overlap.png" width=250>

 * **do you support both BINARY and FRACTIONAL segmentation types?**TODO only BINARY can be displayed; SEGs that are saved as FRACTIONAL will be read as BINARY (i.e., no mapping to fractional occupancy or probability will be done)
 * **do you render the segment using the color specified in the DICOM object?** no
 * **how do you communicate segment semantics to the user?**TODO semantic codes are reduced to a name in the lookup table; user has no meaning to easily get information about the semantics of the object as defined in SEG
 * **how do you support the user in defining the semantics of the object at the time segmentation is created?**TODO user can select from a pre-defined list of structures that are mapped into combinations of segmentation category/type internally by the software

3.**Read task**: load each of the DICOM SEG datasets that accompany the imaging series into your platform

**Test dataset #1**

| Test dataset | Result of rendering |
| -- | -- |
| 3D Slicer | <img src="./images/slicer_qin.png" width=250> |
| ePAD | <img src="./slicer/epad-read-lidc.png" width=250> |
| syngo.via | <img src="./images/syngo-segmentations.png" width=250> |
| AIMonClearCanvas| <img src="./images/clearcanvas_segmentation.png" width=250> |
| Brainlab| <img src="./images/brainlab_fract_objects.png" width=250> |

**Test dataset #2**

| Test dataset | Result of rendering |
| -- | -- |
| 3D Slicer | <img src="./slicer/slicer-read-hnc.png" width=250> |
| Brainlab | <img src="./slicer/brainlab-read-hnc.png" width=250> |


4.**Write task**
 * segment the lung lesion using any method available in your platform; save the result as DICOM SEG; please include in the series description the name of your tool to simplify comparison tasks!
   * results are uploaded
 * run [dciodvfy DICOM validator](http://www.dclunie.com/dicom3tools/dciodvfy.html); iterate on resolving the identified issues as necessary
   * no errors, only warnings from dciodvfy


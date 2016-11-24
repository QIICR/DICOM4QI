# 3D Slicer

1.**Description of the platform/product**:
 * **name and version of the software**: 3D Slicer, Nightly release 4.5.0-2016-08-08, with Reporting Extension installed
 * **free?** yes http://download.slicer.org
 * **commercial?** no
 * **open source?** yes http://github.com/slicer/slicer
 * **what DICOM library do you use?** [DCMTK](http://dcmtk.org)

2.**Description of the relevant features of the platform**: 
 * **are both single and multiple segments supported?** yes **how are the overlapping segments handled?** solid color of the outline is shown for all segments; inners area is shown semi-transparent (see screenshot below showing both AIMonClearCanvas and Brainlab datasets from the Read task)

<img src="slicer/seg-overlap.png" width=250>

 * **do you support both BINARY and FRACTIONAL segmentation types?** only BINARY can be displayed; SEGs that are saved as FRACTIONAL will be read as BINARY (i.e., no mapping to fractional occupancy or probability will be done)
 * **do you render the segment using the color specified in the DICOM object?** yes
 * **how do you communicate segment semantics to the user?** semantic codes are reduced to a name in the lookup table; user has no meaning to easily get information about the semantics of the object as defined in SEG
 * **how do you support the user in defining the semantics of the object at the time segmentation is created?** user can select from a pre-defined list of structures that are mapped into combinations of segmentation category/type internally by the software

3.**Read task**: load each of the DICOM SEG datasets that accompany the imaging series into your platform

**Test dataset #1**

| Test dataset | Result of rendering |
| -- | -- |
| 3D Slicer | <img src="./slicer/slicer-read-lidc.png" width=250> |
| Brainlab | <img src="./slicer/brainlab-read-lidc.png" width=250> |
| syngo.via | <img src="./slicer/syngo-read-lidc.png" width=250> |
| AIMonClearCanvas| <img src="./slicer/aimclearcanvas-read-lidc.png" width=250> |

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


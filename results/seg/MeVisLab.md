# MeVisLab

1.**Description of the platform/product**:
 * **name and version of the software**: MeVisLab 3.0pre, Nightly build from 2016-mm-dd
 * **free?** yes http://www.mevislab.de/download
 * **commercial?** commercial licenses available on request
 * **open source?** no (only partially, sources included in above download)
 * **what DICOM library do you use?** custom (MLDicomTree, using some headers from dcmtk)

2.**Description of the relevant features of the platform**: 
 * **are both single and multiple segments supported?** yes
 * **how are the overlapping segments handled?** loaded separately
   (display depends on application)
 * **do you support both BINARY and FRACTIONAL segmentation types?** yes
 * **do you render the segment using the color specified in the DICOM
   object?** yes / possible (display depends on application)
 * **how do you communicate segment semantics to the user?** MeVisLab
   provides field interface, UI depends on application (no application
   available yet using this new API as of November 2016)
 * **how do you support the user in defining the semantics of the object at the time segmentation is created?**
   no support is available yet (support similiar to the QIICR web
   interface planned, but not yet implemented)

3.**Read task**: load each of the DICOM SEG datasets that accompany the imaging series into your platform

**Test dataset #1**

| Test dataset | Result of rendering |
| -- | -- |
| 3D Slicer | <img src="./MeVisLab/slicer-read-lidc.png" width=250> |
| ePAD | <img src="./MeVisLab/epad-read-lidc.png" width=250> |
| syngo.via | <img src="./MeVisLab/syngo-read-lidc.png" width=250> |
| AIMonClearCanvas| <img src="./MeVisLab/aimclearcanvas-read-lidc.png" width=250> |

**Test dataset #2**

| Test dataset | Result of rendering |
| -- | -- |
| 3D Slicer | <img src="./MeVisLab/slicer-read-hnc.png" width=250> |
| Brainlab | <img src="./MeVisLab/brainlab-read-hnc.png" width=250> |


4.**Write task**
 * segment the lung lesion using any method available in your platform; save the result as DICOM SEG; please include in the series description the name of your tool to simplify comparison tasks!
   * results are uploaded
 * run [dciodvfy DICOM validator](http://www.dclunie.com/dicom3tools/dciodvfy.html); iterate on resolving the identified issues as necessary
   * no errors, only warnings from dciodvfy


## Brainlab

1. **Description of the platform/product**:

   * **name and version of the software** Brainlab FiberTracking 1.1.0
   * ~~**free?**~~
   * **commercial?** [https://www.brainlab.com/en/surgery-products/overview-neurosurgery-products/fibertracking-and-functional-planning/](https://www.brainlab.com/en/surgery-products/overview-neurosurgery-products/fibertracking-and-functional-planning/)
   * ~~**open source?**~~ 
   * **what DICOM library do you use?** - Merge DICOM Toolkit

   * **Description of the relevant features of the platform**:

     * Only _Single Track Set_ DICOM instances are created by the software.
     * **Measurements** stored per Track:  
       _Fractional Anisotropy_ measurement values are stored for each track point for each track.  
       **Statistics** stored per Track:  
       The _Minimum, Maximum and Mean Fractional Anisotropy_ Value is stored as additional statistical information for each track.  
       The _length_ of each Track is stored as additional statistical information

     * **Statistics** stored per Track Set:  
       The _Minimum, Maximum and Mean Fractional Anisotropy_ Value is stored as additional statistical information for the whole Track Set.  
       The _Minimum, Maximum and Mean Track length_ is stored as additional statistical information for the whole Track Set.

     * _Diffusion Model, Method of Acquisition, Algorithm identification and Anatomical information_ is contained in each DICOM TR instance created by the software.

2. **Read task** \(for each dataset!\)

   * load each of the DICOM TR datasets that accompany the imaging series into your platform
   
   
   **Test dataset #1**

| Test dataset | Result of rendering |
| -- | -- |
| 3D Slicer | <img src="./brainlab/slicer-dataset1-directioncolored.png" width=350> <img src="./brainlab/slicer-dataset1.png" width=250>|


3. **Write tasks**

   * **Single trackset**: select a tractography streamline bundle using any method available in your platform.
   * **Multiple tracksets**: select any two streamline bundles using any method available in your platform \(non-intersecting\). Make sure to create separate trackset for each of the segmented areas!
   * save the results as DICOM TR; if possible, please include in the series description the name of your tool to simplify comparison tasks!
   * as part of quick checks, confirm that the resulting TR object has the same FrameOfReferenceUID as the reference image
   * [UPLOAD THE RESULTING DICOM TR FILES HERE](https://www.dropbox.com/request/XvwJrx22BxMxx6EcIZr3). \(note: after upload, data will be publicly accessible from link in results section\)




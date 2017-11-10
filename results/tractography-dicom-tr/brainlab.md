## Brainlab

1. **Description of the platform/product**:

   * **name and version of the software** used for testing
   * **free?** if yes - include the download link
   * **commercial?** if yes - include the home page for the product
   * **open source?** if yes - provide a link to source code
   * **what DICOM library do you use?** - if you use certain DICOM toolkit to support this functionality, please list it, if possible

   * **Description of the relevant features of the platform**:

     * are multiple tracksets supported in a single file?
     * do you support any optional measurement data associated with a track?
     * do you support any optional summary statistics associated with a track set?
     * do you write any other optional information to the TR file? \(e.g. acquisition, model, attribute, algorithm identification etc.\)

2. **Read task** \(for each dataset!\)

   * load each of the DICOM TR datasets that accompany the imaging series into your platform
   * submit the following screenshots:
     * demonstrate the 2D overlay of the track sets on the B0 series \(if possible\)
     * demonstrate several 3D perspectives \(if possible\)
     * demonstrate any other components of the user interface \(e.g., presentation of the associated measurements, communication of the algorithm metadata\).

3. **Write tasks**

   * **Single trackset**: select a tractography streamline bundle using any method available in your platform.
   * **Multiple tracksets**: select any two streamline bundles using any method available in your platform \(non-intersecting\). Make sure to create separate trackset for each of the segmented areas!
   * save the results as DICOM TR; if possible, please include in the series description the name of your tool to simplify comparison tasks!
   * as part of quick checks, confirm that the resulting TR object has the same FrameOfReferenceUID as the reference image
   * [UPLOAD THE RESULTING DICOM TR FILES HERE](https://www.dropbox.com/request/XvwJrx22BxMxx6EcIZr3). \(note: after upload, data will be publicly accessible from link in results section\)




| NOTE: As of November 2018, the new home of DICOM4QI is here: https://dicom4qi.readthedocs.io|
| --- |

# Pixelmed

1.**Description of the platform/product**:
 * **name and version of the software**: Pixelmed Java Toolkit, http://www.dclunie.com/pixelmed/software/20160907_current/
 * **free?** yes 
 * **commercial?** no
 * **open source?** yes http://www.dclunie.com/pixelmed/software/20160907_current/
 * **what DICOM library do you use?** no extra DICOM libraries

2.**Description of the relevant features of the platform**: 
 * **are both single and multiple segments supported?** not clear (as tested by Andrey Fedorov) 
 * **how are the overlapping segments handled?** N/A

 * **do you support both BINARY and FRACTIONAL segmentation types?** not clear (as tested by Andrey Fedorov) TBD
 * **do you render the segment using the color specified in the DICOM object?** no
 * **how do you communicate segment semantics to the user?** not available
 * **how do you support the user in defining the semantics of the object at the time segmentation is created?** the tool is a viewer only, not applicable

3.**Read task**: load each of the DICOM SEG datasets that accompany the imaging series into your platform

**Steps to load DICOM SEG into Pixelmed image viewer:**

  **1.** Convert image dataset into multiframe using script such as below (parameters: input single-frame DICOM directory, and the directory for the output multiframe image):

```
#!/bin/sh

PIXELMEDDIR=.

java -Xmx2g -Xms512m -XX:-UseGCOverheadLimit -cp "${PIXELMEDDIR}/pixelmed.jar:${PIXELMEDDIR}/lib/additional/commons-compress-1.9.jar:${PIXELMEDDIR}/lib/additional/commons-codec-1.3.jar:${PIXELMEDDIR}/lib/additional/vecmath1.2-1.14.jar" com.pixelmed.dicom.MultiFrameImageFactory $*
```

  **2.** Display SEG in overlay using the following command (parameters: multiframe DICOM image, and DICOM SEG image):

```
java -Xmx2g -Xms512m -XX:-UseGCOverheadLimit -cp "${PIXELMEDDIR}/pixelmed.jar:${PIXELMEDDIR}/lib/additional/commons-compress-1.9.jar:${PIXELMEDDIR}/lib/additional/commons-codec-1.3.jar:${PIXELMEDDIR}/lib/additional/vecmath1.2-1.14.jar" com.pixelmed.display.SuperimposedDicomSegments $*
```

**Test dataset #1**

| Test dataset | Result of rendering |
| -- | -- |
| 3D Slicer | <img src="./pixelmed/slicer-read-td1.png" width=250> |
| Brainlab | <img src="./pixelmed/brainlab-read-td1.png" width=250> |
| syngo.via | <img src="./pixelmed/syngo-read-td1.png" width=250> |
| AIMonClearCanvas| <img src="./pixelmed/clearcanvas-read-td1.png" width=250> |

**Test dataset #2**

| Test dataset | Result of rendering |
| -- | -- |
| 3D Slicer | <img src="./pixelmed/slicer-read-td2-1.png" width=250> <img src="./pixelmed/slicer-read-td2-2.png" width=250>|
| Brainlab | <img src="./pixelmed/brainlab-read-td2.png" width=250> |

Notes:
* Appears that only one segment can be displayed in a slice at a time. 
* Possible errors rendering Brainlab dataset. Runtime errors:

```
Exception in thread "AWT-EventQueue-0" java.lang.ArrayIndexOutOfBoundsException: Coordinate out of bounds!
	at sun.awt.image.IntegerInterleavedRaster.getDataElements(IntegerInterleavedRaster.java:219)
	at java.awt.image.BufferedImage.getRGB(BufferedImage.java:918)
	at com.pixelmed.display.SuperimposedImage$AppliedToUnderlyingImage.notificationOfCurrentLocationIn3DSpace(SuperimposedImage.java:224)
	at com.pixelmed.display.SingleImagePanel.updateStatusBarValues(SingleImagePanel.java:1039)
	at com.pixelmed.display.SingleImagePanel.mouseMoved(SingleImagePanel.java:993)
```

**Test dataset #3**

| Test dataset | Result of rendering |
| -- | -- |
| 3D Slicer | <img src="./pixelmed/slicer-read-td3.png" width=250>|

**Test dataset #4**

| Test dataset | Result of rendering |
| -- | -- |
| 3D Slicer | <img src="./pixelmed/slicer-read-td4.png" width=250>|

4.**Write task**

Application evaluated is viewer only. Pixelmed has capabilities of writing DICOM SEG objects, but those were not evaluated.


!!! info
    When ready to submit, use the [DICOM4QI Submission Google Form](http://bit.ly/dicom4qi-submit)

The purpose of this task is to demonstrate support of the [DICOM Segmentation Image (DICOM SEG)](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_A.51.html) object.

The basic read task involves loading the existing DICOM SEG object, and demonstrating segmentation overlay on the image being annotated.

Write task involves volumetric segmentation of a finding (evaluation of the precision/accuracy of the segmentation is out of the scope of this demonstration) and storing the result as a DICOM SEG object.

For each of the datasets listed and linked below, please complete the Read task and the Write task.

!!! info
    * all datasets are organized in [this Dropbox folder](https://www.dropbox.com/sh/6axblmmgrs29oef/AABRvRLu74h9W82QeJa4afmoa?dl=0)

    * submit the resulting screenshots and datasets by uploading the zip file with the screenshots and resulting objects to this [Dropbox FileRequests location](https://www.dropbox.com/l/AABQ7CW0pXGQ9VEPbFtCZhCYF1tzcWuKfak). Make sure that the file is named to include the name of your platform!

## Read task

Load each of the DICOM SEG datasets that accompany the imaging series into your platform, make a screenshot demonstrating the overlay of the segmentation over the image, and any other components of the user interface (e.g., presentation of the ROI semantics to the user, communication of the algorithm metadata)

## Write task

!!! note
    We are not assessing the accuracy of segmentation, any method is good!

**Single segment**: segment any area (ideally, the lung lesion in the Test dataset #1) using any method available in your platform.

**Multiple segments**: segment any two areas in any of the datasets using any method available in your platform (ideally, such that there is a single slice where both segments are visible). Make sure to create separate segment for each of the segmented areas!

Save the result as DICOM SEG. If possible, please include in the series description the name of your tool to simplify comparison tasks!

run [`dciodvfy`](http://www.dclunie.com/dicom3tools/dciodvfy.html) DICOM validator; iterate on resolving the identified issues as necessary.

As part of quick checks, confirm that the resulting SEG object has the same `FrameOfReferenceUID` as the source image.

## Dataset 1

The imaging dataset is a chest CT with a single lung lesion located in the right lung lobe. This dataset is subject LIDC-IDRI-0314 from [The Cancer Imaging Archive (TCIA)](https://thecancerimagingarchive.net) [LIDC-IDRI collection](https://wiki.cancerimagingarchive.net/display/Public/LIDC-IDRI).

## Dataset 3

The imaging dataset consists of a PET and CT series for subject QIN-HEADNECK-01-0139 from the TCIA [QIN-HEADNECK collection](https://wiki.cancerimagingarchive.net/display/Public/QIN-HEADNECK). This data set contains 11 lesions. This allows to test that the implementation can handle more than one segment.

## Dataset 5

This dataset is a manually created "phantom" that can be used to test correctness of the implementation of bit packing procedures of the implementation. The frame size of this 3-slice dataset is 23x38, which is not divisible by 8, causing the bit-packed representation of the frame not aligning with the byte boundary. The middle slice of the image should show a round region, and the pixels toggled in the segmentation should match those in the image. Segmentation also has pixels toggled in 4 corners of each of the 3 slices.

## Dataset 6

This dataset contains result of segmentation of 43 brain structures using FreeSurfer. This object can be used to evaluate performance of loading a larger number of segments, and performance of rendering of the result. This dataset was generated using the Corticometrics fs2dicom converter (based on dcmqi) publicly available here: https://github.com/corticometrics/fs2dicom (also available via `pip install fs2dicom`).

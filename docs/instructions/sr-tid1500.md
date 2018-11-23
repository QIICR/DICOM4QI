!!! info
    When ready to submit, use the [DICOM4QI Submission Google Form](http://bit.ly/dicom4qi-submit)

The purpose of this task is to demonstrate support of the [DICOM Structured Reporting template TID1500 \(DICOM TID1500\)](http://dicom.nema.org/medical/dicom/current/output/chtml/part16/chapter_A.html#sect_TID_1500) for storing measurements derived from volumetric segmentations.

!!! info
    * all datasets are organized in [this Dropbox folder](https://www.dropbox.com/sh/srtqgxj70m4husr/AAD_6Hr8nBHQdWJSQaepnK6ja?dl=0)
    * submit the resulting screenshots and datasets by uploading the zip file with the screenshots and resulting objects to [this Dropbox FileRequests location](https://www.dropbox.com/request/BtulA0HY0WEQr64Tfh8e). Make sure that the file is named to include the name of your platform!

At this time, the only samples we have were created using [dcmqi](https://github.com/qiicr/dcmqi). As we receive more samples, this list will be updated.

## Read task

Load each of the DICOM SR TID1500 datasets into your platform. Submit a screenshot demonstrating the presentation of the loaded measurements to the user.

## Write task

**Datasets 1 and 2**: Given the image series and the segmentation defining the ROI, calculate any measurements over the ROI and save as DICOM SR following TID1500 reporting template.

**Dataset 3**: calculate radiomics features for the given image and volumetric segmentations, and save the result as a DICOM SR TID1500 instance.

**Dataset 4**: define unidimensional linear annotation for the given image, and save the annotation alongside the length measurement as a DICOM SR TID1500 instance.

Run `dciodvfy` DICOM validator and `Pixelmed DicomSRValidator`; iterate on resolving the identified issues as necessary.

## Dataset 1

This is a dataset consisting of 3 slices of a liver CT series, and rough segmentation of the liver defining ROI for calculating the measurements.

The SR dataset contains measurements calculated over the segmentation from the CT slices.

The measurements stored in the SR dataset are the following:

* Mean Attenuation Coefficient = 37.3289 Hounsfeld Units
* Minimum Attenuation Coefficient = -778 Hounsfeld Units
* Maximum Attenuation Coefficient = 221 Hounsfeld Units
* Standard Deviation of Attenuation Coefficient = 59.1691 Hounsfeld Units
* Volume = 70361.9 cubic millimeter
* Volume = 70.3619 cubic centimeter

## Dataset 2

This SR dataset contains measurements over the segmentations of tumor and "hot" lymph nodes in Segmentation Test dataset #3.

The types of measurements stored in this object are described in detail in this article: https://peerj.com/articles/2057/. There is a separate group of measurements for each of the segments in the referenced segmentation object.

## Dataset 3

This SR dataset contains radiomics features (the total of 1561) generated using [pyradiomics](https://github.com/Radiomics/pyradiomics) and [dcmqi](https://github.com/qiicr/dcmqi), and specifically [this script](https://github.com/Radiomics/pyradiomics/tree/master/labs/pyradiomics-dcm) for the Segmentation Test dataset #1.

Radiomics features are encoded using terminology and codes defined by the Imaging Biomarkers Standardization Initiative (IBSI), as described in [v7 of the IBSI document](https://arxiv.org/abs/1612.07003).

## Dataset 4

This SR dataset was created using Pixelmed tools. It contains planimetric annotation of the largest tumor diameter, and length of that diameter. The dataset was collected as part of the Crowds Cure Cancer initiative (see details [here](https://wiki.cancerimagingarchive.net/display/DOI/Crowds+Cure+Cancer%3A+Data+collected+at+the+RSNA+2017+annual+meeting)).The specific dataset corresponds to subject TCGA-BP-4343, series 3, from the [TCIA TCGA-KIRC collection](https://wiki.cancerimagingarchive.net/display/Public/TCGA-KIRC).

## Dataset 5

This dataset contains volume measurements for the [SEG Dataset 6](https://dicom4qi.readthedocs.io/en/latest/instructions/seg/#dataset-6), which is a result of segmentation of 43 brain structures using FreeSurfer. This object can be used to evaluate performance of loading a larger number of segments, and performance of rendering of the result. This dataset was generated using the Corticometrics fs2dicom converter (based on dcmqi) publicly available here: https://github.com/corticometrics/fs2dicom (also available via `pip install fs2dicom`).

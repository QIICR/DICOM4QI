!!! info
    When ready to submit, use the [DICOM4QI Submission Google Form](http://bit.ly/dicom4qi-submit)

In this task the participants are expected to demonstrate the capability of the tool to handle loading of the [DICOM Parametric Map \(DICOM PM\)](http://dicom.nema.org/medical/dicom/current/output/chtml/part03/sect_A.75.html) object.

For each of the datasets listed and linked below, please complete the Read task.

!!! info
    * all datasets are organized in [this Dropbox folder](https://www.dropbox.com/sh/pnukhsrqtgdgp1n/AAB1vswS7A1c4nIu8wTFnGz_a?dl=0)
    * submit the resulting screenshots and datasets by uploading the zip file with the screenshots and resulting objects to this location: https://www.dropbox.com/request/oJFdeFCrRV6nUepxpH1G. Make sure that the file is named to include the name of your platform!

At this time, the only samples of DICOM Parametric map we have were created using [dcmqi](https://github.com/qiicr/dcmqi).

## Read task

Load each of the DICOM Parametric map datasets into your platform. Submit a screenshot demonstrating the presentation of the loaded parametric maps.

## Write task

Create a DICOM Parametric map object using your platform. Submit as part of your submission package.

## Dataset 1

This is a dataset encoding the Apparent Diffusion Coefficient (ADC) map produced by a GE scanner as a DICOM Parametric map object. The original ADC map available here was saved as an object of MR modality by the scanner software. This dataset encodes integer-valued pixels, and the ADC units are micrometers per squared second (as noted in the object).

## Dataset 2

This dataset encodes the same ADC map as the first dataset, but in meters per squared second units. The result is an object where each pixel value is less than one. The goal of this object is to test rendering of the true floating point pixel values.

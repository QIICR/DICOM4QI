# FreeSurfer

**Note**: FreeSurfer is a set of software tools for brain segmentation of MRI data. As such, non-brain imaging applications do not apply, and the tasks defined for DICOM4QI SEG component cannot be addressed. However, DICOM SEG is applicable, and functionality is included to encode brain region segmentations. Therefore, the platform is included.

1. Description of the platform/product:

   * **name and version of the software**: FreeSurfer 6.0
   * **free?**: [yes](https://surfer.nmr.mgh.harvard.edu/fswiki/DownloadAndInstall)
   * **commercial?**: no
   * **open source?**: [yes](https://github.com/freesurfer/freesurfer)
   * **what DICOM library do you use?**: [DCMQI](https://github.com/QIICR/dcmqi) to write DICOM-SEG
   * **Description of the relevant features of the platform**: Freesurfer's [subcortical segmentation results](http://surfer.nmr.mgh.harvard.edu/fswiki/SubcorticalSegmentation/) can be converted to DICOM-SEG using [`fs-aseg.json`](https://github.com/corticometrics/fs2dicom/blob/master/fs-aseg.json) that has been kindly provided by Emily Lindemer. 
   * **are both single and multiple segments supported?**: Yes, however Freesurfer's subcortical segmentation process assumes a mutually exclusive label set.
   * **do you support both BINARY and FRACTIONAL segmentation types?** BINARY only.
   * **do you support compressed objects?** I beleive itkimage2segimage can read compressed itk objects but does not write compressed DICOM objects\(?\)
   * **do you render the segment using the color specified in the DICOM object?** N/A \(write-only\), however Freesurfer's recoomended color scheme is preserved.
   * **how do you communicate segment semantics to the user?** The [`fs-aseg.json`](https://github.com/corticometrics/fs2dicom/blob/master/fs-aseg.json) maps [freesurfer's subcortical labels](https://surfer.nmr.mgh.harvard.edu/fswiki/FsTutorial/AnatomicalROI/FreeSurferColorLUT) to SNOMED codes.
   * **how do you support the user in defining the semantics of the object at the time segmentation is created?** Freesurfer's subcortical label set is predefined, so this is pre-computed.

2. Read task: Not supported

3. Write task:

The file [fs6-dcmqi-ex-rsna2017.tar.gz](http://slicer.kitware.com/midas3/item/324959) contains the following:

* `./dicom-anon`: Direcotry containting input dicoms for a FreeSurfer-compatible T1 weighted MPRAGE sequence.
* `aseg-t1space.nii.gz`: FreeSurfer 6.0 subcortical segmentations \(this is `aseg.mgz` output from FreeSurfer transformed back to the original input DICOM coordinate system and converted to nifti\)
* [`fs-aseg.json`](https://github.com/corticometrics/fs2dicom/blob/master/fs-aseg.json): Mappings from FreeSurfer aseg labels to SNOMED codes provided by Emily Lindemer.

Running the example:

```
tar zxvf ./fs6-dcmqi-ex-rsna2017.tar.gz
cd ./fs6-dcmqi-ex-rsna2017
docker pull qiicr/dcmqi
docker run \
  -v $PWD:/tmp/dcmqi/ \
  qiicr/dcmqi \
  itkimage2segimage \
    --inputDICOMDirectory /tmp/dcmqi/dicom-anon \
    --inputMetadata /tmp/dcmqi/fs-aseg.json \
    --inputImageList /tmp/dcmqi/aseg.nii.gz \
    --outputDICOM /tmp/dcmqi/aseg.dcm
```

Rerunning the above command, and including the `--skip` flag reduces the resulting DICOM-SEG file from 113M to [20M](https://www.dropbox.com/s/iha9mbvvbyaofas/aseg-small.dcm?dl=0)

Verifying the output:

```
dciodvfy ./aseg.dcm &> dciodvfy-output.txt
```

Currently dciodvfy genertes the following errors:

* Thousands of erros that look like:
  ```
  Error - Illegal root for UID - "5.555.5.2017.3.22.??.?.??????" in (0x0008,0x1155) Referenced SOP Instance UID
  ```
* Other errors:
  ```
  Error - Value invalid for this VR - (0x0008,0x0050) SH Accession Number  SH [0] = <Accession Number 1> - Length invalid for this VR = 18, expected <= 16
  Warning - Value dubious for this VR - (0x0008,0x0090) PN Referring Physician's Name  PN [0] = <Referring Physician's Name 1> - Retired Person Name form
  Warning - Value dubious for this VR - (0x0010,0x0010) PN Patient's Name  PN [0] = <Patient's Name 1> - Retired Person Name form
  Warning - Value dubious for this VR - (0x0070,0x0084) PN Content Creator's Name  PN [0] = <Reader1> - Retired Person Name form
  Error - Dicom dataset contains invalid data values for Value Representations
  Segmentation
  Error - Unrecognized enumerated value <CLEANED> for value 1 of attribute <Patient's Sex>
  ```




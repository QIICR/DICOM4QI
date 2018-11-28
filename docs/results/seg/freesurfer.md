**Note**: FreeSurfer is a set of software tools for brain segmentation of MRI data. As such, non-brain imaging applications do not apply, and the tasks defined for DICOM4QI SEG component cannot be addressed. However, DICOM SEG is applicable, and functionality is included to encode brain region segmentations. Therefore, the platform is included.

1. **Description of the platform/product**:
    * **name and version of the software**: `fs2dicom` v0.1.2, which works with FreeSurfer 6.0
    * **free?**: yes; FreeSurfer is available [here](https://surfer.nmr.mgh.harvard.edu/fswiki/DownloadAndInstall), and `fs2dicom` is available for download from [PyPI](https://pypi.org/project/fs2dicom/)
    * **commercial?**: no
    * **open source?**: yes; [FreeSurfer](https://github.com/freesurfer/freesurfer) and [`fs2dicom`](https://github.com/corticometrics/fs2dicom) source code are hosted on GitHub
    * **what DICOM library do you use?**: [DCMQI](https://github.com/QIICR/dcmqi) to write DICOM-SEG

1. **Description of the relevant features of the platform**:
     FreeSurfer's [subcortical segmentation results](http://surfer.nmr.mgh.harvard.edu/fswiki/SubcorticalSegmentation/) can be converted to DICOM-SEG using [`fs-aseg.json`](https://github.com/corticometrics/fs2dicom/blob/master/fs2dicom/templates/fs-aseg.json).  This mapping was contributed by [Emily Lindemer](https://www.linkedin.com/in/emily-lindemer-87206667/).
    * **are both single and multiple segments supported?**: Yes, however FreeSurfer's subcortical segmentation process assumes a mutually exclusive label set.
    * **do you support both BINARY and FRACTIONAL segmentation types?** BINARY only.
    * **do you support compressed objects?** I beleive itkimage2segimage can read compressed itk objects but does not write compressed DICOM objects\(?\)
    * **do you render the segment using the color specified in the DICOM object?** N/A \(write-only\), however FreeSurfer's recommended color scheme is preserved.
    * **how do you communicate segment semantics to the user?** The [`fs-aseg.json`](https://github.com/corticometrics/fs2dicom/blob/master/fs2dicom/templates/fs-aseg.json) maps [FreeSurfer's subcortical labels](https://github.com/freesurfer/freesurfer/blob/dev/distribution/FreeSurferColorLUT.txt) to SNOMED codes.
    * **how do you support the user in defining the semantics of the object at the time segmentation is created?** FreeSurfer's subcortical label set is predefined, so this is pre-computed.


1. **Read task**: Not supported


1. **Write task**:
    * The file [fs2dicom-rsna2018-example-v2.tar.gz](https://gate.nmr.mgh.harvard.edu/filedrop2/index.php?p=3xrvjp4cpwo) contains the following, as well as files to create a [DICOM Structured Report](../../sr-tid1500/freesurfer):
        - `./dicom-anon`: Directory containting input DICOMs for a FreeSurfer-compatible T1 weighted MPRAGE sequence.
        - `./fs2dicom-rsna2018-example/fs-subjects/fs2dicom-rsna2018ex/`: Directory containing the output of the above DICOMs processed with FreeSurfer 6.0 subcortical segmentations
        - `./aseg-seg.dcm`: The DICOM seg image created by `fs2dicom`
        - `./readme.txt`: Description of these contents, and instructions on how to run `fs2dicom` on the results
    * Running the example (**NOTE:** `docker` and Python >= 3.4 are required to run this. See the `readme.txt` and the [`fs2dicom` GitHub page](https://github.com/corticometrics/fs2dicom) for more details):
    ```text
    pip install fs2dicom   # if not installed previously
    tar zxvf ./fs2dicom-rsna2018-example-v2.tar.gz
    cd fs2dicom-rsna2018-example

    fs2dicom create-seg \
      ./dicoms-anon/MR.1.3.12.2.1107.5.2.32.35162.1999123112191238865917962 \
      ./fs-subjects/fs2dicom-rsna2018ex/mri/aseg.mgz   \
      ./aseg-seg.dcm
    ```
    * Verifying the output:
    ```text
    dciodvfy ./aseg-seg.dcm
    ```

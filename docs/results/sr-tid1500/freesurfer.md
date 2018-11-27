**Note**: FreeSurfer is a set of software tools for brain segmentation of MRI data. As such, non-brain imaging applications do not apply, and the tasks defined for DICOM4QI TID1500 component cannot be addressed. However, DICOM TID1500 Strutured Reporting is applicable, and functionality is included to encode brain region volumetric statistics. Therefore, the platform is included.

1. Description of the platform/product:

* **name and version of the software**: `fs2dicom` v0.1.2, which works with FreeSurfer 6.0
* **free?**: yes; FreeSurfer is available [here](https://surfer.nmr.mgh.harvard.edu/fswiki/DownloadAndInstall), and `fs2dicom` is available for download from [PyPI](https://pypi.org/project/fs2dicom/)
* **commercial?**: no
* **open source?**: yes; [FreeSurfer](https://github.com/freesurfer/freesurfer) and [`fs2dicom`](https://github.com/corticometrics/fs2dicom) source code are hosted on GitHub
* **what DICOM library do you use?**: [DCMQI](https://github.com/QIICR/dcmqi) to write DICOM-SR

2. **Description of the relevant features of the platform**: 
`fs2dicom` incorporates the volumetric statistics created by FreeSurfer (saved as the `aseg.stats` file) into a DICOM SR object. These can be viewed along with the [DICOM SEG](../../seg/freesurfer) object in viewers such as 3D Slicer:

![](../freesurfer/freesurfer-sr.png)

3. Read task: Not supported

4. Write task:

* The file [fs6-dcmqi-ex-rsna2017.tar.gz](https://gate.nmr.mgh.harvard.edu/filedrop2/index.php?p=3xrvjp4cpwo) contains the following:

  * `./dicom-anon`: Directory containting input DICOMs for a FreeSurfer-compatible T1 weighted MPRAGE sequence.
  * `./fs2dicom-rsna2018-example/fs-subjects/fs2dicom-rsna2018ex/`: Directory containing the output of the above DICOMs processed with FreeSurfer 6.0 subcortical segmentations
  * `fs-aseg-sr.json`: File containing the volume statistics calculated by FreeSurfer, used to create the DICOM SR
  * `./aseg-sr.dcm`: The DICOM SR image created by `fs2dicom`
  * `./aseg-seg.dcm`: The DICOM SEG image created by `fs2dicom`
  * `./readme.txt`: Description of these contents, and instructions on how to run `fs2dicom` on the results

* Running the example (**NOTE:** `docker` and Python >= 3.4 are required to run this. See the `readme.txt` and the [`fs2dicom` GitHub page](https://github.com/corticometrics/fs2dicom) for more details):

```text
pip install fs2dicom   # if not installed previously
tar zxvf ./fs2dicom-rsna2018-example-v2.tar.gz
cd fs2dicom-rsna2018-example

fs2dicom create-sr \
  --aseg_dicom_seg_file ./aseg-seg.dcm \
  ./dicoms-anon/MR.1.3.12.2.1107.5.2.32.35162.1999123112191238865917962 \
  ./fs-subjects/fs2dicom-rsna2018ex/stats/aseg.stats \
  ./aseg-sr.dcm
```

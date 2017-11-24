# MITK

### 1. Description of the relevant features of the platform:
  - are multiple tracksets supported in a single file? - **No**
  - do you support any optional measurement data associated with a track? - **No**
  - do you support any optional summary statistics associated with a track set? - **No**
  - do you write any other optional information to the TR file? (e.g. acquisition, model, attribute, algorithm identification etc.)
    - **This information is written but it needs to be set manually using the GUI (see screenshot "TagGui.png"). Manually here means by typing typing it into the correponding form in the application GUI.**
  
  - Other notes:
    - the DICOM tags relevant to associate the tractogram to the original image have to be copied manually from the imported DICOM image. Manually here means that to select the image and the new tractogram and to click a button in the application GUI (see screenshot "TagGui.png").
   -  Dataset 3 was not read correctly --> no tractogram for dataset 3
  
### 2. Read task: TR objects from each platform, loaded and displayed in MITK.

<table> 
<tr>
  <td width="33%">MITK</td>
  <td width="33%">BrainLab</td>
  <td width="33%">3D Slicer</td>
</tr>


<!-- dataset_1 -->
<tr>
  <td><i>MITK_dataset_1.dcm</i></td>
  <td><i>TrackSet_DataSet1.dcm</i></td>
  <td><i>3DSlicer_dataset[..]-v2.dcm</i></td>
</tr>

<tr>
  <td>
    <img src="mitk/mitk_dataset_1_3D_View1_tube.png" width="200">
    <img src="mitk/mitk_dataset_1_sagittal.png" width="200">
    <img src="mitk/mitk_dataset_1_axial.png" width="200">
  </td>
   
   <td>
    <img src="mitk/brainlab_dataset_1_2D.png" width="200">
    <img src="mitk/brainlab_dataset_1_3D.png" width="200">
   </td>
   
   <td>
    <img src="mitk/slicer_dataset_1_2D.png" width="200">
    <img src="mitk/slicer_dataset_1_3D.png" width="200">
   </td>
</tr>


<!-- dataset_2 -->
<tr>
  <td><i>MITK_dataset_2.dcm</i></td>
  <td><i>N/A</i></td>
  <td><i>3DSlicer_dataset_2[..].dcm</i></td>
</tr>

<tr>
   <td>
    <img src="mitk/mitk_dataset_2_3D_View1_tube.png" width="200">
    <img src="mitk/mitk_dataset_2_sagittal.png" width="200">
    <img src="mitk/mitk_dataset_2_axial.png" width="200">
   </td>
   
   <td><!-- BrainLab n/a --></td>
   
   <td>
     <img src="mitk/slicer_dataset_2_2D.png" width="200">
     <img src="mitk/slicer_dataset_2_3D.png" width="200">

   </td>

</tr>

<!-- dataset_3 -->
<tr>
  <td>N/A</td>
  <td><i>TrackSet_DataSet3.dcm</i></td>
  <td><i>dataset_3_GeSignaHDx.dcm</i></td>
</tr>

<tr>
  <td>
  N/A 
  </td>
   
  <td>
  <img src="mitk/brainlab_dataset_3_3D.png" width="200">
  </td>

  <td>
  <img src="mitk/slicer_dataset_3_2D.png" width="200">
  <img src="mitk/slicer_dataset_3_3D.png" width="200">
  </td>
  
</tr>
</table>


### 3. Write task
- Datasets are available in the "MITK" folder of the [Results Dropbox folder](https://www.dropbox.com/sh/gmy2nt1mlfk1k2w/AADIdfcLUUZ8ViAh7i6x0aana?dl=0).


#### Results of validation using `dciodvfy`

* dataset_1
```
Warning - Code Value contains invalid characters for coding scheme - value is <-> - bad character is '-' - coding scheme is <DCM>
Warning - Code Value contains invalid characters for coding scheme - value is <-> - bad character is '-' - coding scheme is <DCM>
Warning - Missing attribute or value that would be needed to build DICOMDIR - Study Date
Warning - Missing attribute or value that would be needed to build DICOMDIR - Study Time
Warning - Missing attribute or value that would be needed to build DICOMDIR - Study ID
Warning - Missing attribute or value that would be needed to build DICOMDIR - Series Number
Warning - Value dubious for this VR - (0x0010,0x0010) PN Patient's Name  PN [0] = <619432> - Retired Person Name form
Warning - Value dubious for this VR - (0x0070,0x0084) PN Content Creator's Name  PN [0] = <MIC@DKFZ> - Retired Person Name form
TractographyResults
Error - Missing attribute Type 2 Required Element=<SeriesNumber> Module=<GeneralSeries>
Error - Missing attribute Type 2C Conditional Element=<Laterality> Module=<GeneralSeries>
Error - Missing attribute Type 1 Required Element=<SeriesNumber> Module=<TractographyResultsSeries>
Error - Missing attribute Type 1 Required Element=<AlgorithmFamilyCodeSequence> Module=<AlgorithmIdentificationMacro>
Error - Missing attribute Type 1 Required Element=<AlgorithmName> Module=<AlgorithmIdentificationMacro>
Error - Missing attribute Type 1 Required Element=<AlgorithmVersion> Module=<AlgorithmIdentificationMacro>
Warning - Attribute is not present in standard DICOM IOD - (0x0008,0x0100) SH Code Value
Warning - Attribute is not present in standard DICOM IOD - (0x0008,0x0102) SH Coding Scheme Designator
Warning - Attribute is not present in standard DICOM IOD - (0x0008,0x0104) LO Code Meaning
Warning - Dicom dataset contains attributes not present in standard DICOM IOD - this is a Standard Extended SOP Class
```
* dataset_2
```
Warning - Code Value contains invalid characters for coding scheme - value is <-> - bad character is '-' - coding scheme is <DCM>
Warning - Code Value contains invalid characters for coding scheme - value is <-> - bad character is '-' - coding scheme is <DCM>
Warning - Missing attribute or value that would be needed to build DICOMDIR - Study Date
Warning - Missing attribute or value that would be needed to build DICOMDIR - Study Time
Warning - Missing attribute or value that would be needed to build DICOMDIR - Study ID
Warning - Missing attribute or value that would be needed to build DICOMDIR - Series Number
Warning - Value dubious for this VR - (0x0010,0x0010) PN Patient's Name  PN [0] = <WM-707> - Retired Person Name form
Warning - Value dubious for this VR - (0x0070,0x0084) PN Content Creator's Name  PN [0] = <MIC@DKFZ> - Retired Person Name form
TractographyResults
Error - Missing attribute Type 2 Required Element=<SeriesNumber> Module=<GeneralSeries>
Error - Missing attribute Type 2C Conditional Element=<Laterality> Module=<GeneralSeries>
Error - Missing attribute Type 1 Required Element=<SeriesNumber> Module=<TractographyResultsSeries>
Error - Missing attribute Type 1 Required Element=<AlgorithmFamilyCodeSequence> Module=<AlgorithmIdentificationMacro>
Error - Missing attribute Type 1 Required Element=<AlgorithmName> Module=<AlgorithmIdentificationMacro>
Error - Missing attribute Type 1 Required Element=<AlgorithmVersion> Module=<AlgorithmIdentificationMacro>
Warning - Attribute is not present in standard DICOM IOD - (0x0008,0x0100) SH Code Value
Warning - Attribute is not present in standard DICOM IOD - (0x0008,0x0102) SH Coding Scheme Designator
Warning - Attribute is not present in standard DICOM IOD - (0x0008,0x0104) LO Code Meaning
Warning - Dicom dataset contains attributes not present in standard DICOM IOD - this is a Standard Extended SOP Class
```
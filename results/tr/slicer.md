# 3D Slicer

### 1. **Description of the platform/product**:

   - **name and version of the software**: 3D Slicer, nightly release 2017-11-13, with [SlicerDMRI](http://dmri.slicer.org/download/) extension installed.
   - **free?**: Yes, [http://download.slicer.org/](http://download.slicer.org/) and [http://dmri.slicer.org/download/](http://dmri.slicer.org/download/) \(extension instructions\)
   - ~~**commercial?**:~~
   - **open source?**: yes: [https://github.com/SlicerDMRI](https://github.com/SlicerDMRI)
   - **what DICOM library do you use?**: DCMTK
   - **Description of the relevant features of the platform**:
     * are multiple tracksets supported in a single file? - **Not currently**
     * do you support any optional measurement data associated with a track? - **No**
     * do you support any optional summary statistics associated with a track set? - **No**
     * do you write any other optional information to the TR file? \(e.g. acquisition, model, attribute, algorithm identification etc.\) - **No**

### 2. **Read task** Screenshots of trackset results for each platform, loaded with 3D Slicer:

<table> 
<tr>
  <td width="33%">3D Slicer</td>
  <td width="33%">Brainlab</td>
  <td width="33%">MITK</td>
</tr>


<!-- dataset_1 -->
<tr>
  <td><i>3DSlicer_dataset_1[..]-v2.dcm</i></td>
  <td><i>TrackSet_DataSet1.dcm</i></td>
  <td><i>MITK_dataset_1.dcm</i></td>
</tr>

<tr>
  <td>
    <img src="slicer/3DSlicer_dataset1_screenshot.png" width="200">
   </td>
   
   <td>
   <img src="slicer/BrainLab_dataset1_screenshot-1.png" width="200">
   <img src="slicer/BrainLab_dataset1_screenshot-2.png" width="200">
   </td>
   
   <td>
   <img src="slicer/MITK_dataset1_screenshot-1.png" width="200">
   </td>
</tr>


<!-- dataset_2 -->
<tr>
  <td><i>3DSlicer_dataset_2[..].dcm</i></td>
  <td><i>N/A</i></td>
  <td><i>MITK_dataset_2.dcm</i></td>
</tr>

<tr>
   <td>
   <img src="slicer/3DSlicer_dataset2_screenshot-1.png" width="200">
   </td>
   
   <td><!-- BrainLab n/a --></td>
   
   <td>
   <img src="slicer/MITK_dataset2_screenshot-1.png" width="200">
   </td>

</tr>

<!-- dataset_3 -->
<tr>
  <td><i>3DSlicer_dataset_3[..].dcm</i></td>
  <td><i>TrackSet_DataSet3.dcm</i></td>
  <td>N/A</td>
</tr>

<tr>
  <td>
  <img src="slicer/3DSlicer_dataset3_screenshot-1.png" width="200"> 
  </td>
   
  <td>
  <img src="slicer/BrainLab_dataset3_screenshot-1.png" width="200">
  <img src="slicer/BrainLab_dataset3_screenshot-2.png" width="200">
  </td>
  <td>
  <!-- MITK n/a -->
  </td>
  
</tr>
</table>

### 3. **Write tasks**

   * Datasets are available in the "3DSlicer_TR" folder of the [Results Dropbox folder](https://www.dropbox.com/sh/gmy2nt1mlfk1k2w/AADIdfcLUUZ8ViAh7i6x0aana?dl=0).
   
#### Results of validation using `dciodvfy`

* dataset_1
```
Warning - Missing attribute or value that would be needed to build DICOMDIR - Study Date
Warning - Missing attribute or value that would be needed to build DICOMDIR - Study Time
Warning - Missing attribute or value that would be needed to build DICOMDIR - Study ID
Warning - Missing attribute or value that would be needed to build DICOMDIR - Series Number
Warning - Value dubious for this VR - (0x0010,0x0010) PN Patient's Name  PN [0] = <619432> - Retired Person Name form
Warning - Value dubious for this VR - (0x0070,0x0084) PN Content Creator's Name  PN [0] = <TractIO> - Retired Person Name form
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
Warning - Missing attribute or value that would be needed to build DICOMDIR - Series Number
Warning - Value dubious for this VR - (0x0010,0x0010) PN Patient's Name  PN [0] = <WM-707> - Retired Person Name form
Warning - Value dubious for this VR - (0x0070,0x0084) PN Content Creator's Name  PN [0] = <TractIO> - Retired Person Name form
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
* dataset_3
```
Warning - Missing attribute or value that would be needed to build DICOMDIR - Patient ID
Warning - Missing attribute or value that would be needed to build DICOMDIR - Study ID
Warning - Missing attribute or value that would be needed to build DICOMDIR - Series Number
Warning - Value dubious for this VR - (0x0070,0x0084) PN Content Creator's Name  PN [0] = <TractIO> - Retired Person Name form
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



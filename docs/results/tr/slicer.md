## 1. **Description of the platform/product**:

* **name and version of the software**: 3D Slicer 4.10 realease, with [SlicerDMRI](http://dmri.slicer.org/download/) extension installed.
* **free?**: Yes, [http://download.slicer.org/](http://download.slicer.org/) and [http://dmri.slicer.org/download/](http://dmri.slicer.org/download/) \(extension instructions\)
* **commercial?**: no
* **open source?**: yes: [https://github.com/SlicerDMRI](https://github.com/SlicerDMRI)
* **what DICOM library do you use?**: DCMTK
* **Description of the relevant features of the platform**:
   * are multiple tracksets supported in a single file? - **Not currently**
   * do you support any optional measurement data associated with a track? - **Yes**
   * do you support any optional summary statistics associated with a track set? - **Not currently**
   * do you write any other optional information to the TR file? \(e.g. acquisition, model, attribute, algorithm identification etc.\) - **No**

## 2. **Read task**

Screenshots of trackset results for each platform, loaded with 3D Slicer, are shown below.   

* Results: tracks with FA

<table>
<tr>
 <td>
    <img src="../slicer/Reading-SlicerDMRI.jpg" style="display:block;">
  </td>
</tr>	
</table>

* Results: tracts 3D visualization

<table>
<tr>
  <td><b>Dataset</b></td>
  <td>3D Slicer</td>
  <td>Brainlab</td>
  <td>MITK</td>
  <td>Prism</td>
</tr>

<!-- dataset_1 -->
<tr>
  <td>1</td>

  <td>
    <img src="../slicer/3DSlicer_dataset1_screenshot.png" style="display:block;">
   </td>

   <td>
     <img src="../slicer/BrainLab_dataset1_screenshot-1.png" style="display:block;">
     <img src="../slicer/BrainLab_dataset1_screenshot-2.png" style="display:block;">
   </td>

   <td>
     <img src="../slicer/MITK_dataset1_screenshot-1.png" style="display:block;">
   </td>

   <td>
     <img src="../slicer/Prism_dataset1.png" style="display:block;">
   </td>
</tr>


<!-- dataset_2 -->
<tr>
   <td>2</td>

   <td>
   <img src="../slicer/3DSlicer_dataset2_screenshot-1.png" style="display:block;">
   </td>

   <td>N/A</td>

   <td>
   <img src="../slicer/MITK_dataset2_screenshot-1.png" style="display:block;">
   </td>

   <td>
     <img src="../slicer/Prism_dataset2.png" style="display:block;">
   </td>
</tr>

<!-- dataset_3 -->
<tr>
  <td>3</td>

  <td>
    <img src="../slicer/3DSlicer_dataset3_screenshot-1.png" style="display:block;">
  </td>

  <td>
    <img src="../slicer/BrainLab_dataset3_screenshot-1.png" style="display:block;">
    <img src="../slicer/BrainLab_dataset3_screenshot-2.png" style="display:block;">
  </td>

  <td>N/A</td>

  <td>
    <img src="../slicer/Prism_dataset3.png" style="display:block;">
  </td>
</tr>
</table>

## 3. **Write task**

* Datasets are available in the "SlicerDMRI" folder of the [Results Dropbox folder](https://www.dropbox.com/sh/i1scpqdxf8kmqqq/AABAZNT7tRAWrklYgtr7JNgia/TR?dl=0&subfolder_nav_tracking=1).

### Results of validation using `dciodvfy`

Pending

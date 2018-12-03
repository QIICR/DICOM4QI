## 1. **Description of the platform/product**:

* **name and version of the software** Brainlab FiberTracking 1.1.0
* **free?** no
* **commercial?** yes, [https://www.brainlab.com/en/surgery-products/overview-neurosurgery-products/fibertracking-and-functional-planning/](https://www.brainlab.com/en/surgery-products/overview-neurosurgery-products/fibertracking-and-functional-planning/)
* **open source?** no
* **what DICOM library do you use?** - Merge DICOM Toolkit
* **Description of the relevant features of the platform**:
  * **Only Single Track Set** DICOM instances are created by the software.
  * **Measurements stored per Track:** _Fractional Anisotropy_ measurement values are stored for each track point for each track.
  * **Statistics stored per Track:** The _Minimum, Maximum and Mean Fractional Anisotropy_ Value is stored as additional statistical information for each track. The _length_ of each Track is stored as additional statistical information
  * **Statistics stored per Track Set:** The _Minimum, Maximum and Mean Fractional Anisotropy_ Value is stored as additional statistical information for the whole Track Set. The _Minimum, Maximum and Mean Track length_ is stored as additional statistical information for the whole Track Set.
  * **Diffusion Model, Method of Acquisition, Algorithm identification and Anatomical information** is contained in each DICOM TR instance created by the software.

## 2. Read task

* Results: tracks with FA

<table>
 <tr>
   <td>
     <img src="../brainlab/Reading-BrainLab.jpg" style="display:block;">
   </td>
 </tr>
</table>

* Results: tracts 3D visualization

<table style="width:100%;table-layout:fixed;">
 
<tr>
  <td width="10%" style="white-space: nowrap"><b>Dataset</b></td>
  <td width="23%"><b>Brainlab</b></td>
  <td width="22%"><b>3D Slicer</b></td>
  <td width="23%"><b>MITK</b></td>
  <td width="22%"><b>Prism</b></td>
</tr>

<!-- dataset_1 -->

<tr>
  <td><b>1</b></td>

  <td>
    <img src="../brainlab/brainlab-TrackSet_DataSet1.JPG" style="display:block;">  
  </td>

  <td>
    <img src="../brainlab/Slicer_TrackSet_DataSet1_Colored.JPG" style="display:block;">
  </td>

  <td>
    <img src="../brainlab/MITK_TrackSet_DataSet1.JPG" style="display:block;">
  </td>

  <td>
    <img src="../brainlab/Prism_TrackSet_DataSet1.JPG" style="display:block;">
</td>

</tr>


<!-- dataset_2 -->

<tr>
   <td><b>2</b></td>

   <td>
   N/A
   </td>

   <td>
     <img src="../brainlab/Slicer_TrackSet2_LoadedByBrainlab.JPG" style="display:block;">
   </td>

   <td>
     <img src="../brainlab/MITK_TrackSet_DataSet2.JPG" style="display:block;">
   </td>

   <td>
    <img src="../brainlab/Prism_TrackSet_DataSet2.JPG" style="display:block;">
   </td>
</tr>

<!-- dataset_3 -->

<tr>
  <td><b>3</b></td>
  <td>
    <img src="../brainlab/brainlab-TrackSet_DataSet3.JPG" style="display:block;">
  </td>

  <td>
    <img src="../brainlab/Slicer_TrackSet3_LoadedByBrainlab.JPG" style="display:block;">
  </td>

  <td>
    N/A
  </td>

  <td>
    <img src="../brainlab/Prism_TrackSet_DataSet3.JPG" style="display:block;">
</td>

</tr>
</table>

## 3. **Write tasks**

* Datasets are available in the "BrainLab" folder of the [Results Dropbox folder](https://www.dropbox.com/sh/vqp0zhagboit2hw/AAAYWmCQTHcGMh48AvhY2GNFa?dl=0).

**Notes:**

* **Multiple Track Sets**:

  Brainlab FiberTracking 1.1.0 does not support storage of multiple TrackSets inside one DICOM TR instance.

* **Track Set created based on Test Dataset \#1:**
  * 1 Track Set
  * 503 Tracks
  * Single Colored \(turquoise, but shown direction-colored in screenshot\)
  * Detailed Track Set Description can be found in    
    * TrackSet Label       \(0066,0106\)
    * TrackSet Description \(0066,0107\) \(and NOT in Series Description \(0008,103e\)\)
  * Additional Measurements
    * Per Track Point
      * Fractional Anisotropy Value for each Track Point for each Track  \(stored inside Measurements Sequence \(0066,0121\)\)
  * Additional Statistics
    * Statistics per Track
      * Four Statistical attributes for each Track \(stored inside Track Statistic Sequence \(0066,0130\)\)
        * Minimum, Maximum and Mean Fractional Anisotropy values  
        * Path length \(i.e. length of a Track, no units, but is millimeter\)     
    * Statistics per Track Set
      * Six Statistical attributes for the whole Track Set \(stored inside Track Set Statistics Sequence \(0066,0124\)\)
        * Minimum, Maximum and Mean Fractional Anisotropy values  
        * Minimum, Maximum and Mean Track lengths \(no units, but is millimeter\)
* **No Track Set created based on Test Dataset \#2:**

  Brainlab FiberTracking Software does not support Track Set creation for Test DataSet 2.

* **Track Set created based on Test Dataset \#3:**
  * 1 Track Set
  * 8 Tracks
  * Single Colored \(magenta, but shown direction-colored in screenshot\)
  * Detailed Track Set Description can be found in
    * TrackSet Label       \(0066,0106\)
    * TrackSet Description \(0066,0107\) \(and NOT in Series Description \(0008,103e\)\)
  * Additional Measurements
    * Per Track Point
      * Fractional Anisotropy Value for each Track Point for each Track  \(stored inside Measurements Sequence \(0066,0121\)\)    
  * Additional Statistics
    * Statistics per Track
      * Four Statistical attributes for each Track \(stored inside Track Statistic Sequence \(0066,0130\)\)
        * Minimum, Maximum and Mean Fractional Anisotropy values  
        * Path length \(i.e. length of a Track, no units, but is millimeter\)  
    * Statistics per Track Set
      * Six Statistical attributes for the whole Track Set \(stored inside Track Set Statistics Sequence \(0066,0124\)\)
        * Minimum, Maximum and Mean Fractional Anisotropy values  
        * Minimum, Maximum and Mean Track lengths \(no units, but is millimeter\)

#### Results of validation using `dciodvfy`

Pending

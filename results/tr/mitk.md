# MITK

1. **Description of the platform/product**:
   * **name and version of the software**: MITK Workbench \(not yet released, the TR support features are available in the `master` of the source code, and will appear in the next stable release\)
   * **free?** yes - [http://mitk.org/Downloads](http://mitk.org/Downloads)
   * **commercial?** no
   * **open source?** yes - [https://phabricator.mitk.org/source/mitk/](https://phabricator.mitk.org/source/mitk/)
   * **what DICOM library do you use?** [DCMTK](http://dcmtk.org), [GDCM](http://gdcm.sourceforge.net/), [DCMQI](http://github.com/qiicr/dcmqi)
2. **Description of the relevant features of the platform**:
   * are multiple tracksets supported in a single file? - **No**
   * do you support any optional measurement data associated with a track? - **No**
   * do you support any optional summary statistics associated with a track set? - **No**
   * do you write any other optional information to the TR file? \(e.g. acquisition, model, attribute, algorithm identification etc.\)
     * **This information is written but it needs to be set manually using the GUI \(see screenshot "TagGui.png"\). Manually here means by typing typing it into the correponding form in the application GUI.**
   * Other notes:
     * the DICOM tags relevant to associate the tractogram to the original image have to be copied manually from the imported DICOM image. Manually here means that to select the image and the new tractogram and to click a button in the application GUI \(see screenshot "TagGui.png"\).
   * Dataset 3 was not read correctly --&gt; no tractogram for dataset 3

## 2. Read task: TR objects from each platform, loaded and displayed in MITK.

|  |
| :--- |


| MITK | BrainLab | 3D Slicer |
| :--- | :--- | :--- |


| MITK\_dataset\_1.dcm | TrackSet\_DataSet1.dcm | 3DSlicer\_dataset\[..\]-v2.dcm |
| :--- | :--- | :--- |


|  |
| :--- |


  
  

|   |
| :--- |


![](../../.gitbook/assets/mitk_dataset_1_3d_view1_tube.png)

|   |
| :--- |


![](../../.gitbook/assets/mitk_dataset_1_sagittal.png)

|   |
| :--- |


![](../../.gitbook/assets/mitk_dataset_1_axial.png)

|  |
| :--- |


|   |
| :--- |


![](../../.gitbook/assets/brainlab_dataset_1_2d.png)

|   |
| :--- |


![](../../.gitbook/assets/brainlab_dataset_1_3d.png)

|  |
| :--- |


|   |
| :--- |


![](../../.gitbook/assets/slicer_dataset_1_2d.png)

|   |
| :--- |


![](../../.gitbook/assets/slicer_dataset_1_3d.png)

|  |
| :--- |


  
&lt;/tr&gt;

| MITK\_dataset\_2.dcm | N/A | 3DSlicer\_dataset\_2\[..\].dcm |
| :--- | :--- | :--- |


|  |
| :--- |


  
   

|   |
| :--- |


![](../../.gitbook/assets/mitk_dataset_2_3d_view1_tube.png)

|   |
| :--- |


![](../../.gitbook/assets/mitk_dataset_2_sagittal.png)

|   |
| :--- |


![](../../.gitbook/assets/mitk_dataset_2_axial.png)

|  |
| :--- |


|  |
| :--- |


|  |
| :--- |


  
     

![](../../.gitbook/assets/slicer_dataset_2_2d.png)

  
     

![](../../.gitbook/assets/slicer_dataset_2_3d.png)

&lt;/td&gt;

&lt;/tr&gt;

| N/A | TrackSet\_DataSet3.dcm | dataset\_3\_GeSignaHDx.dcm |
| :--- | :--- | :--- |


|  |
| :--- |


  
  

|  N/A |
| :--- |


|   |
| :--- |


![](../../.gitbook/assets/brainlab_dataset_3_3d.png)

|  |
| :--- |


|   |
| :--- |


![](../../.gitbook/assets/slicer_dataset_3_2d.png)

|   |
| :--- |


![](../../.gitbook/assets/slicer_dataset_3_3d.png)

|  |
| :--- |


&lt;/tr&gt;  
&lt;/table&gt;

## 3. Write task

* Datasets are available in the "MITK" folder of the [Results Dropbox folder](https://www.dropbox.com/sh/gmy2nt1mlfk1k2w/AADIdfcLUUZ8ViAh7i6x0aana?dl=0).

### Results of validation using `dciodvfy`

Pending


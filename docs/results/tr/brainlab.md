### 1. Description of the platform/product

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

## 2. Read task -- result of rendering for each dataset

<table>
<tr>
 <td>
    <img src="../brainlab/Reading-BrainLab.jpg" style="display:block;">
  </td>
</tr>	
</table>

### 3. Write tasks

* None


### Prism

* **Description of the platform/product**:

  * **name and version of the software** Prism View 4.1
  * **free?** No
  * **commercial?** Yes, [http://prismclinical.com/index.html](http://prismclinical.com/index.html)

  * **open source?** No

  * **what DICOM library do you use?** DCM4CHE

  * **Description of the relevant features of the platform**:

    * are multiple tracksets supported in a single file? -No
    * do you support any optional measurement data associated with a track? -No
    * do you support any optional summary statistics associated with a track set? -No
    * do you write any other optional information to the TR file? \(e.g. acquisition, model, attribute, algorithm identification etc.\) -No

* **Read task**

| Data Set | BrainLab | 3DSlicer | MITK | Prism |
| :--- | :--- | :--- | :--- | :--- |
| 1 | ![](prism/DataSet1_BrainLab.jpg) | ![](prism/DataSet1_3DSlicer.jpg) | ![](prism/DataSet1_MITK.jpg) | ![](prism/DataSet1_PrismScreenCapture.jpg) |
| 2 | N/A | ![](prism/DataSet2_3DSlicer.jpg) | ![](prism/DataSet2_MITK.jpg) | ![](prism/DataSet2_PrismScreenCapture.jpg) |
| 3 | ![](prism/DataSet3_BrainLab.jpg) | ![](prism/DataSet3_3DSlicer.jpg) | N/A | ![](prism/DataSet3_PrismScreemCapture.jpg) |

* **Write task**
  * Data sets can be found in the "Prism" folder of the [Results Dropbox Folder](https://www.dropbox.com/sh/gmy2nt1mlfk1k2w/AADIdfcLUUZ8ViAh7i6x0aana?dl=0).

#### Results of validation using `dciodvfy`

```
Track Set 1:

Warning - Missing attribute or value that would be needed to build DICOMDIR - Study ID
Warning - Value dubious for this VR - (0x0008,0x0090) PN Referring Physician's Name  PN [0] = <None> - Retired Person Name form
Warning - Value dubious for this VR - (0x0010,0x0010) PN Patient's Name  PN [0] = <619432> - Retired Person Name form
TractographyResults
Warning - is only permitted to be empty when actually unknown; should be absent (not empty) if an unpaired body part, and have a value if a paired body part - attribute <Laterality>
```

```
Track Set 2:

Warning - Value dubious for this VR - (0x0008,0x0090) PN Referring Physician's Name  PN [0] = <None> - Retired Person Name form
Warning - Value dubious for this VR - (0x0010,0x0010) PN Patient's Name  PN [0] = <WM-707> - Retired Person Name form
TractographyResults
Warning - is only permitted to be empty when actually unknown; should be absent (not empty) if an unpaired body part, and have a value if a paired body part - attribute <Laterality>
```

```
Track Set 3:

Warning - Missing attribute or value that would be needed to build DICOMDIR - Study ID
Warning - Value dubious for this VR - (0x0008,0x0090) PN Referring Physician's Name  PN [0] = <None> - Retired Person Name form
Warning - Value dubious for this VR - (0x0010,0x0010) PN Patient's Name  PN [0] = <TracStor-03> - Retired Person Name form
TractographyResults
Warning - is only permitted to be empty when actually unknown; should be absent (not empty) if an unpaired body part, and have a value if a paired body part - attribute <Laterality>
```




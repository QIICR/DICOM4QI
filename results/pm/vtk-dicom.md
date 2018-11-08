| NOTE: As of November 2018, the new home of DICOM4QI is here: https://dicom4qi.readthedocs.io|
| --- |

# VTK Dicom

Tasks for participants:

1.**Description of the platform/product**:
 * **name and version of the software**: vtk-dicom v0.8.6
 * **free?** yes https://github.com/dgobbi/vtk-dicom/releases
 * **commercial?** no
 * **open source?** yes https://github.com/dgobbi/vtk-dicom
 * **what DICOM library do you use?** our own (the vtkDICOM library)

 * **Description of the relevant features of the platform**:
    * vtk-dicom is a DICOM library for use with VTK applications
    * the library comes with command-line utilities and simple source-code examples, but it is not, by itself, a full-fledged DICOM viewer
    * it provides a DICOM to NIfTI converter (dicomtonifti) that supports parametric maps
    * it provides a NIfTI to DICOM converter (niftitodicom), but parametric maps are not yet supported in this direction (as of Oct 2017)

3. **Read task** (for each dataset!)
 * load each of the DICOM Parametric map datasets into your platform
 * submit a screenshot demonstrating the presentation of the loaded parametric maps to the user by email to Andrey Fedorov

### Test dataset #1

<img src="./vtk-dicom/vtk-dicom-pm-test1.png" width=602 height=424>

### Test dataset #2

<img src="./vtk-dicom/vtk-dicom-pm-test2.png" width=602 height=424>

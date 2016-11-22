# Parametric maps

Tasks for participants:

1. **Description of the platform/product**:
 * **name and version of the software**: MeVisLab 3.0pre, Nightly build from 2016-mm-dd
 * **free?** yes http://www.mevislab.de/download
 * **commercial?** commercial licenses available on request
 * **open source?** no (only partially, sources included in above download)
 * **what DICOM library do you use?** custom (MLDicomTree, using some headers from dcmtk)

 * **Description of the relevant features of the platform**: 
    * please provide the screenshot of the user interface for the functionality specific to creating/displaying measurements 
    * how do you communicate parametric map semantics to the user (quantity encoded, units)? 

3. **Read task** (for each dataset!)
 * load each of the DICOM Parametric map datasets into your platform
 * submit a screenshot demonstrating the presentation of the loaded parametric maps to the user by email to Andrey Fedorov
 
### Test dataset #1

This is a dataset encoding the Apparent Diffusion Coefficient (ADC) map produced by a GE scanner as a DICOM Parametric map object that [can be downloaded here](http://slicer.kitware.com/midas3/download/item/257241/paramap.dcm.zip). The original ADC map [available here](http://slicer.kitware.com/midas3/download/item/126196/701-ADCb500.zip) was saved as an object of MR modality by the scanner software.

This dataset encodes integer-valued pixels, and the ADC units are micrometers per squared second (as noted in the object).

### Test dataset #2

This dataset that [can be downloaded here](http://slicer.kitware.com/midas3/download/item/257243/paramap-float.dcm.zip) encodes [the same ADC map as the first dataset](http://slicer.kitware.com/midas3/download/item/126196/701-ADCb500.zip), but in meters per squared second units. The result is an object where each pixel value is less than one. The goal of this object is to test rendering of the true floating point pixels.

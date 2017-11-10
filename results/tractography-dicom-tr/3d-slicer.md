# Tractography results

## Overview

The purpose of this task is to demonstrate support of the [DICOM Tractography Results](ftp://medical.nema.org/medical/dicom/final/sup181_ft_TractographyResultsStorage.pdf) \(DICOM TR\) object.

The basic read task involves loading the existing DICOM TR object, and demonstrating visualization of the tractography relative to the reference image.

The write task involves generation of tractography streamlines from the provided Diffusion Weighted Image DICOM files and storing the result as a DICOM TR object. Note that this task does not seek to compare tractography algorithms, evaluate medical or neuroanatomic accuracy or usefulness of results, etc. _The only question of interest is interchange of DICOM TR objects between systems._

## Tasks for participants

1. **Description of the platform/product**:

   * **name and version of the software**: 3D Slicer, nightly release 2017-11-05, with [SlicerDMRI](http://dmri.slicer.org/download/) extension installed.
   * **free?**: Yes, [http://download.slicer.org/](http://download.slicer.org/) and [http://dmri.slicer.org/download/](http://dmri.slicer.org/download/) \(extension instructions\)
   * ~~**commercial?**:~~
   * **open source?**: [https://github.com/SlicerDMRI](https://github.com/SlicerDMRI)
   * **what DICOM library do you use?**: DCMTK

   * **Description of the relevant features of the platform**:

     * are multiple tracksets supported in a single file?
     * do you support any optional measurement data associated with a track?
     * do you support any optional summary statistics associated with a track set?
     * do you write any other optional information to the TR file? \(e.g. acquisition, model, attribute, algorithm identification etc.\) - No

2. **Read task**

   * load each of the DICOM TR datasets that accompany the imaging series into your platform
   * submit the following screenshots:
     * demonstrate the 2D overlay of the track sets on the B0 series \(if possible\)
     * demonstrate several 3D perspectives \(if possible\)
     * demonstrate any other components of the user interface \(e.g., presentation of the associated measurements, communication of the algorithm metadata\).

3. **Write tasks**

   * **Single trackset**: 
   * **Multiple tracksets**:




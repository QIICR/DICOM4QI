| NOTE: As of November 2018, the new home of DICOM4QI is here: https://dicom4qi.readthedocs.io|
| --- |


# Scope

The declared scope of the exhibit covered exchange of the following types of data:

* **DICOM Segmentation image object \(SEG\)**, representing a classification of pixels in one or more referenced images. Among other capabilities, SEG provides unambiguous specification of the anatomy being segmented using structured terminology.
* **DICOM Parametric Map object \(PM\)** can be used to encode floating-point pixel maps of derived parameters, such as results of pharmacokinetic analysis of Dynamic Contrast-Enhanced MRI. Parametric Map object was introduced in [Supplement 172](ftp://medical.nema.org/medical/dicom/final/sup172_ft2.pdf).
* **DICOM Structured reporting of measurements** using SR template 1500 \(**SR-TID1500**\) can be used to communicate measurements over the image region defined by, for example, a SEG object.
* **DICOM Tractography Results object (TR)**, encoding the Diffusion MRI fiber tractography.

For the details about the individual types of object see [Instructions](../instructions.md).


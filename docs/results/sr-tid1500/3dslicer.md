1.**Description of the platform/product**:

* **name and version of the software**: 3D Slicer, Nightly release 4.7.0-2016-11-27, with [QuantitativeReporting](https://github.com/QIICR/QuantitativeReporting) extension installed
* **free?** yes [http://download.slicer.org](http://download.slicer.org)
* **commercial?** no
* **open source?** yes [http://github.com/slicer/slicer](http://github.com/slicer/slicer)
* **what DICOM library do you use?** [DCMTK](http://dcmtk.org), [DCMQI](http://github.com/qiicr/dcmqi)

1. **Description of the relevant features of the platform:**
   * The user specifies the image series and can use module interface to segment one or more areas. Each segment can be assigned a term defining the category/type of the tissue segmented, and \(if applicable\) anatomic location.
   * Measurements are calculated over the segmented areas automatically \(summary statistics\), and are shown in a table view.
   * Surfaces of the segments are displayed in 3d view.
   * User can click on the individual segments, and slice viewers will be synchronized to show the selected segment.
2. **Read task**

## Test dataset \#1

![](../slicer/slicer-sr-read-td1.png)

## Test dataset \#2

![](../slicer/slicer-sr-read-td2.jpg)

## Test dataset \#3

Individual radiomics features can be seen in the table layout.

<img src="../slicer/slicer-sr-read-td3.png" width="75%">

## Test dataset \#4

At the moment, 3D Slicer does not support loading of the SR-TID1500 reports that accompany linear measurements.

Work in progress to improve this is in this PR: https://github.com/QIICR/QuantitativeReporting/pull/235.

## Test dataset \#5

Individual volume measurements can be seen in the table layout.

<img src="../../seg/slicer/slicer-read-seg-td6.png" width="75%">

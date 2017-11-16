# MITK

1. Description of the relevant features of the platform:
  - are multiple tracksets supported in a single file? - **No**
  - do you support any optional measurement data associated with a track? - **No**
  - do you support any optional summary statistics associated with a track set? - **No**
  - do you write any other optional information to the TR file? (e.g. acquisition, model, attribute, algorithm identification etc.)
    - **This information is written but it needs to be set manually using the GUI (see screenshot "TagGui.png"). Manually here means by typing typing it into the correponding form in the application GUI.**
  
  - Other notes:
    - the DICOM tags relevant to associate the tractogram to the original image have to be copied manually from the imported DICOM image. Manually here means that to select the image and the new tractogram and to click a button in the application GUI (see screenshot "TagGui.png").
   -  Dataset 3 was not read correctly --> no tractogram for dataset 3
  
2. Read task

...

3. Write task


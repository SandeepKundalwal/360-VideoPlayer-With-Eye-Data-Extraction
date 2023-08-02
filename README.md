# 360-VideoPlayer
A 360 Degree Video Player for HTC VIVE Pro Eye with Eye Data Extraction Script.

### How to install SRanipal:
- Download SRanipal Runtime from [here](https://developer.vive.com/resources/vive-sense/eye-and-facial-tracking-sdk/download/latest/).
- **NOTE:** Download the SRanipal SDK Version **1.3.3.0** from [here](https://developer.vive.com/resources/vive-sense/eye-and-facial-tracking-sdk/download/archive/1_3_3_0/). The current SRanipal SDK (1.3.6.8) makes Unity crash the moment you hit play button.

### Do Calibration Properly on HTC VIVE EYE PRO:
- Make sure to set the IPD(Inter-Pupilary Distance) to ensure comfortable and correct eye tracking capability in Calibration Setup Phase.
- On **"follow the dot"** window, just follow the dot by moving the eye. Do not move your body as the dot is moving.

### Steps to get SRanipal Working:
- Create the scene as per your requirement.
- If not done yet, install the XR Plugin Management via Edit > Project Settings > XR Plugin Management.
- Open XR Plugin Management via Edit > Project Settings > XR Plugin Management and activate OpenXR and Vive OpenXR feature group.
- Import the SRanipal SDK into your project: Assets > Import Package > Custom Package....
- Close and re-open Unity! Without the restart, the DLL won't be found.
- Drag the **"SRanipal Eye Framework.prefab"** from Assets\ViveSR\Prefabs (in hierachy put "version_2" and active both "enable eye" and "enable eye data callback").
- Create an empty GameObject where you can attach as component the [script](Assets/Scripts/EyeData). In this script there's a void "Measurment" function which mesure eye data and a "Callback" function that return you data and print them in a text file. You can find the file of all eye data in your Unity project in the Assets folder. Remember to delete every time the text file generated, because if the file already exsist when unity is lauched, unity editor will interrupt itself.

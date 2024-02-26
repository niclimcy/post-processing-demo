# How to Add Post-Processing to an Existing Unity 3D Project

## Download and open the Week 5 Unity Project

1. Duplicate existing Week 5 VRTut project or Download the zip file [HERE](https://drive.google.com/file/d/1iMGUauE0O7175kPf6t7hNDXoElbM_YP8/view?usp=sharing)
2. Open UnityHub → Open → Add project from disk → (select) duplicated VRTut (folder)
3. Click and open VRTur Unity project
4. You should see the server room from Week 5

## Add the Universal RP Package from Unity Registry

![Adding Universal RP Package](Demo/Universal_RP_Package.png)

1. Open the Package Manager (Window > Package Manager)
2. Search for `Universal RP` in the Unity Registry
3. Install the `Universal RP` package into your project

## Creating a URP Asset

![Creating a URP Asset](Demo/Create_URP_Asset.png)

1. Go to Assets
2. Create > Rendering > URP Asset (with Universal Renderer)

![URP Assets created](Demo/Pipeline_Asset_Created.png)

3. You should see 2 new assets being created
    - New Universal Render Pipeline Asset
    - New Universal Render Pipeline Asset_Renderer

## Configure project to use URP

![Graphics Settings](Demo/Graphics_Settings.png)

1. Open Project Graphics Settings (Edit > Project Settings > Graphics)

![Select URP Asset](Demo/Select_URP_Asset.png)

2. Set `Scriptble Render Pipeline Settings (Render Pipeline Asset)` to the newly created `New Universal Render Pipeline Asset`

## Oh no! Why are my assets pink?

![Pink Assets](Demo/Scene_Pink.png)

Answer: Run Render Pipeline Converter

![Open Render Pipeline Converter](Demo/Open_Render_Pipeline_Converter.png)

1. Open the Render Pipeline Converter (Window > Rendering > Render Pipeline Converter)

![Render Pipeline Converter Settings](Demo/Render_Pipeline_Converter_Settings.png)

2. Make sure Built-in to URP is selected and all items in the list are selected

3. Run Initialize And Convert

## Enable post-processing for all cameras
For any cameras you want post processing applied to during gameplay, you have to enable Post Processing for each camera.

1. In your hierarchy, find your camera (XR Origin (XR Rig) > Camera Offset > Main Camera)

![Enable Post Processing in Main Camera](Demo/Camera_Settings.png)

2. Look at the Inspector, under Rendering, enable `Post Processing`

## Volumes I (Global Volume)

## Volumes II (Local Volume)

## Profile Overrides

## References

1. [YouTube - HOW TO DO POST PROCESSING IN UNITY 🎮 | URP Unity Post Effects Tutorial | Learn Unity](https://youtu.be/yugZTujILB0?si=CIsiNG2pa1Al6TDV)
2. [Unity Manual - Install URP into an existing Project](https://docs.unity3d.com/Packages/com.unity.render-pipelines.universal@14.0/manual/InstallURPIntoAProject.html)
3. [Unity Manual - Render Pipeline Converter](https://docs.unity3d.com/Packages/com.unity.render-pipelines.universal@14.0/manual/features/rp-converter.html)

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

![Create new Global Volume object](Demo/New_Global_Volume.png)

1. Create a new `Global Volume` object in the Hierarchy (Hierarchy > Volume > Global Volume)

![Add new Volume Profile](Demo/New_Volume_Profile.png)

2. View the newly created `Global Volume` in the Inspector and press `New` under Profile to createa a new volume profile

![Add new Volume Profile Override](Demo/Add_Volume_Override.png)

3. A new section will appear below Profile, click `Add Override` under the new Profile.

![Add Bloom effect](Demo/Add_Bloom_Effect.png)

4. Add the `Bloom` effect and set the following values, WARNING: the screen will flash during this step during the re-render.

5. Observe that some game objects have a "glow" emitting from them

## Volumes II (Local Volume)

1. Create a new `Box Volume` object in the Hierarchy (Hierarchy > Volume > Box Volume)

![Toggle Gizmo Visibility](Demo/Toggle_Gizmo_Visibility.png)

2. Select the newly created `Box Volume` and toggle gizmo visibility to see the area the Box Volume takes effect (you should now see a green highlighted box)

3. Move the `Box Volume` into the Server Room

![Change Box Volume Settings](Demo/Box_Volume_Settings.png)

4. Select the `Box Volume`, add a new Volume Profile and change its Priority to 1

![Add desaturate effect](Demo/Add_Desaturation_Effect.png)

5. Add any effect, in this case lets try to add a desaturation effect (Add Override > Color Adjustments > Set Saturation to -100)

6. Observe that moving into the box volume area removes all colour:

![Desaturation Effect](Demo/Desaturation_Effect.mp4)

## References

1. [YouTube - HOW TO DO POST PROCESSING IN UNITY 🎮 | URP Unity Post Effects Tutorial | Learn Unity](https://youtu.be/yugZTujILB0?si=CIsiNG2pa1Al6TDV)
2. [Unity Manual - Install URP into an existing Project](https://docs.unity3d.com/Packages/com.unity.render-pipelines.universal@14.0/manual/InstallURPIntoAProject.html)
3. [Unity Manual - Render Pipeline Converter](https://docs.unity3d.com/Packages/com.unity.render-pipelines.universal@14.0/manual/features/rp-converter.html)

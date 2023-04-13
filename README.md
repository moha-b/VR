# [1.1 - VR Project Setup](https://learn.unity.com/tutorial/vr-project-setup?pathwayId=627c12d8edbc2a75333b9185&missionId=62554983edbc2a76a27486cb#) <a href="https://unity.com/releases/2021-lts"> <img align="right" width="120" src="https://github.com/moha-b/VR/blob/Challenge-1-Architecture-Review/Assets/Challenges/01_Architecture/Readme%20Images/Unity.png" /> </a>
[In the last lesson](https://learn.unity.com/tutorial/0-1-set-up-unity-and-your-vr-device-1?uv=2021.3&pathwayId=627c12d8edbc2a75333b9185&missionId=62554983edbc2a76a27486cb#), you will get all the necessary software for your computer and your VR device installed and configured for VR development. If you haven’t already, you should install the recommended version of Unity to be able to follow along with this course. Depending on which VR device you intend to use, you may also need to install additional export modules. 
You will also make sure that your VR headset is configured properly for development and testing, including downloading any additional device-specific software that is required. 
 
 By the end of this lesson, you will have a new Unity project with a big empty room that you will experience in VR.
## 1 . Open a new VR project
1 . Download and extract :
- Download this reposiory.  
- Right-click the downloaded file and select Extract All.

2 . Rename and relocate the project on your computer:
- Locate the folder called “VR Room Project” inside the extracted folder.
- If you want, rename the project folder to “VR Room - [Your Name]”
- Move the project folder to a logical directory on your computer (e.g. a folder called “Create with VR” on your desktop). 

3 . Add the VR Room project to the Unity Hub: 
- Open the Unity Hub.
- Add your VR Room Project to the list of projects in the Unity Hub. 
- If you are not sure how to do this, check out this tutorial on adding projects to the Unity Hub.
- If you see a warning icon next to the Editor version of your project, don’t worry.

 <img width="500" align="right" src="https://user-images.githubusercontent.com/73842931/231865054-86fb9416-eda8-4693-9ee1-d4f218e584a6.png" />

This just means that the project was created with a specific version of Unity that you don’t have on your computer. As long as you have installed a version of Unity beginning with 2021.3, the project will run perfectly.

4 . Open the project in Unity 2021.3 LTS (Long-Term Support): 
- From the Editor Version dropdown, select a version of Unity beginning with 2021.3, then select Open with 2021.3.X.
- If a window pops up asking if you want to “Change Editor Version?”, select Change Version.

![image](https://user-images.githubusercontent.com/73842931/231865616-62ec9815-9cfe-4d10-85f0-964499bf1428.png)
If a warning pops up that you are Opening Project in a Non-Matching Editor Installation”, select Continue.

![image](https://user-images.githubusercontent.com/73842931/231865643-dd1b3cc0-d195-4468-9e5f-cbc2462d4b97.png)
Your project should now open in Unity.
If there are yellow warning messages in the Console window about some of the assets, you can ignore them or clear them.

5 . Explore the contents of the starter project and how it differs from a typical empty project:
- From the top menu, select Window > Package Manager. 
- In the left panel of the Package Manager, locate the packages installed in this project (with checkmarks next to them), including:
  - XR Plugin Management
  - XR Interaction Toolkit
  - Universal RP (Render Pipeline)
Note: to filter and view only packages currently installed in the project, from the top-left corner of the Package Manager window, select Packages: In Project. 
Package Manager window showing all packages currently installed in the project. The following packages are highlighted: OpenXR Plugin, Universal RP, XR Interaction Toolkit, and XR Plugin Management.
Select image to expand

You should now have your new VR starter project open to an empty scene and understand which packages allow for compatibility with VR.

## 2 . Open and explore the starter scene
1 . Rename and open the Starter Scene:
- From the Project window, open the Scenes folder.
- Rename the “Create-with-VR_Starter-Scene” as “[Your_Name] Room”.
- Double-click on your renamed scene to open it.

2 . Explore the contents of this scene and how it differs from a typical empty Scene:
- From the Hierarchy, select the XR Rig object and inspect the XR Origin component.
- Select XR Rig > Camera Offset > Main Camera and inspect the Tracked Pose Driver component.
- Select either the LeftHand Controller or RightHand Controller object and inspect the XR Controller component.
- Select the Input Action Manager object and inspect the Input Action Manager component.

![image](https://user-images.githubusercontent.com/73842931/231866215-8b91aec7-b323-4070-8336-be90afdafa22.png)

You should now have your new scene open. You should also have a broad understanding of the components of the scene that make it different from a typical Unity scene.

## 3 . Add a room and background
This empty scene would be boring to explore in VR, so you should add a room that will be a bit more interesting and will provide more perspective when you’re in VR.

1 . Add a room to the scene: 
- In the Project window, expand Course Library > _Prefabs > Rooms.
- Drag one of the Room_[style] prefabs into the Hierarchy. 
- From the Hierarchy, delete the Plane object.

2 . Add an environment outside the room’s windows: 
- Open the Course Library > _Prefabs > Environments folder 
- Drag one Foreground object and one Background object into the Hierarchy.

3 . Adjust the sunlight in the room: 
- Change the X and Y rotation of the Directional Light object to change the way sunlight enters your room. 

![image](https://user-images.githubusercontent.com/73842931/231866563-2b435de8-f985-47bf-baa5-383ab36b5a79.png)

You should now have room, foreground, and background objects in your scene from the course library, with sunlight entering the room at the desired angle.

## 4 . Run the app with the Device Simulator
You can test the scene with a Device Simulator. This simulator allows you to test the app in-editor using the mouse and keyboard, rather than having to connect to a device and put it on. This can be helpful for quick tests.

1 . Add the Device Simulator to the scene:
- From the Project window, open Samples > XR Interaction Toolkit > [version] > XR Device Simulator. 
- Drag the XR Device Simulator Prefab into the Hierarchy.
- Click Play to test the simulator. 
2 . Experiment with the keyboard and mouse controls:

Note:  To use the simulator effectively, a mouse with a clickable scroll wheel is required.

- To control the camera: hold right-click.
- To control the left controller: hold Left Shift or toggle with T.
- To control the right controller: hold the Spacebar or toggle with Y.
- To pan around with a device: move the mouse.
- To rotate a device: hold the middle mouse button.
- To reset the position and rotation of devices: press V.
- If you’d like a helpful guide, download the PDF of the [Rig Simulator Shortcut Cheat Sheet](https://connect-prd-cdn.unity.com/20210604/28db6ca9-aba1-4ac3-a15a-24664daff3ea/Rig%20Simulator%20Keyboard%20Shortcuts.pdf).

3 . See more controls available for the device simulator:

- From the Hierarchy, select the XR Device Simulator.
- In the XR Device Simulator component, double-click on one of the Action variables to open the Action Editor.
- Expand the Actions to view their Bindings.
- From the left Action Maps panel, select either Main or Input Controls to view additional action mappings.

4 . Important:  disable the Device Simulator if you do not plan on using it:

- Select the Device Simulator object then disable it in the Inspector window. 
- Having the device simulator active when running the project on your device will cause problems.

![image](https://user-images.githubusercontent.com/73842931/231867628-2172d659-2230-40da-a6f5-00ff1232f8f6.png)

You should now be able to look around your room with your mouse and keyboard using the Device Simulator. 

## 5 . Test in VR through Unity

If you are using a Windows computer, follow this step to test on your device. Otherwise, skip this step. 
If you are using a Mac for development, this step is not relevant. You will learn how to test your app in the next step when you build your app directly onto your device.
In order to run the project on your device through Unity, you need to install the correct plug-in for development. [OpenXR](https://www.khronos.org/openxr/) is an open source API that connects Unity to supported VR hardware devices. It is recommended that you use this plug-in, since it allows you to deploy to multiple devices through a single, standardized API.  

1 . Install the OpenXR Plugin for desktop testing:
- From the top menu, select Edit > Project Settings, then select the XR Plug-in Management panel from the sidebar.
- In the Windows, Mac, Linux tab, select OpenXR from the list of available Plug-in Providers to install that plug-in.

![image](https://user-images.githubusercontent.com/73842931/231868221-a34d68c5-5be5-4912-8dc0-ce004ce136d3.png)

2 . Resolve any warnings by setting up an interaction profile.
- After adding the OpenXR plugin, there may be a warning or error icon that appears next to the plugin Name. 
- If there are no warnings or errors, you can skip to step 3 below to connect your device through the Quest Link Software. 
- If there is a warning, click on the warning icon to open the OpenXR Project Validation window, which will tell you that you need to add an interaction profile for the device you’re using. 
- Select the Edit button to open the OpenXR settings panel.

![image](https://user-images.githubusercontent.com/73842931/231868380-37d93470-86e3-452d-a718-a5c16d0a381a.png)

- In the Windows, Mac, Linux tab, make sure the Oculus Touch Controller Profile appears in the list of Interaction Profiles, then enable all available OpenXR Feature Groups. 
- If you are using a different device, such as the Valve Index or HTC Vive, add its interaction profile instead.

![image](https://user-images.githubusercontent.com/73842931/231868461-7d50d986-afe1-4cb7-b6a4-5f003468110f.png)

- There should no longer be any warnings in the XR Plugin Management panel. If there are, select them and follow the recommended steps to resolve them.
- If you are having trouble resolving warnings or errors, or if you need help troubleshooting, check out this detailed [documentation on configuring the OpenXR plugin](https://docs.unity3d.com/Packages/com.unity.xr.openxr@1.4/manual/index.html).

3 . Connect your device through the Quest Link Software: 

- Make sure your device is plugged into your computer using a compatible cable. 
- Make sure the Quest App is running and has successfully recognized your device.
- If you have not yet downloaded the Quest App, you find it on the [Link Setup page](https://www.oculus.com/accessories/oculus-link/).

![image](https://user-images.githubusercontent.com/73842931/231868778-ca38dbde-7212-4c2f-a3b7-78fceb7074ab.png)

4 . Test the project on your device:
- Make sure the XR Device Simulator in your scene is disabled. If it is enabled, your head tracking will not work.
- Select Play in the Unity Editor and put on your headset.

![image](https://user-images.githubusercontent.com/73842931/231868856-9f91a1c7-0057-4029-9a55-03d2e5e2bd3c.png)

On a Windows computer, you should now be able to quickly test your app on your device through Unity.

## 6 . Build and run on your device

If you are using a Quest, follow this step to build the app onto your device. Otherwise, skip this step. 
Since the Quest is a standalone device (meaning it does not need to be connected to a computer), you can build an app and test it directly on the device, disconnected from your computer. 
If you are on a Mac and cannot test your app through the Windows Quest software as in the previous step, this will be the primary way for you to test your app on your headset.
In order to build your app to the Quest headset, you will need to configure plug-ins for the Android build target. 

1 . Install the OpenXR for Android builds:
- From the XR Plug-in Management settings, select the Android tab, then select OpenXR from the list of available Plug-in Providers to install that plug-in. 
Note: You will only have an Android tab if you installed the Android export module.
- If you don’t see an option for OpenXR in the Android tab, first go back to the Desktop tab and select OpenXR there, then return to the Android tab.

![image](https://user-images.githubusercontent.com/73842931/231869143-acd07657-ce29-4fdd-9ccb-915953c1cadd.png)

2 . Resolve warnings by setting up an interaction profile.
- Click on the new warning or error icon that appears to open the OpenXR Project Validation window, which will tell you again that you need to add an interaction profile. 
- Select the Edit button to open the OpenXR settings panel.

![image](https://user-images.githubusercontent.com/73842931/231869236-eeb7e5c1-1e6e-4719-a926-9d14e679b5ef.png)

- In the Android tab, select the + button to add the appropriate profile for your device, then enable all OpenXR Feature Groups.

![image](https://user-images.githubusercontent.com/73842931/231869312-ffacccd3-28c5-47ba-bdac-31374a2fa656.png)

- If any additional errors or warnings appear, click on the error or warning icons to resolve them.

![image](https://user-images.githubusercontent.com/73842931/231869399-6b78b88c-d924-4592-97d0-81148edd453b.png)

3 . Prepare your scene for building: 
- Make sure the XR Device Simulator in your scene is disabled. If it is enabled, your head tracking will not work.
- From the top menu, click File > Build Settings.
- Click Add Open Scenes to add your scene.

4 . Switch to the Android build platform: 
- In the Platform section, select Android.
- Click Switch Platform, and wait for your project to switch to the Android platform.
- Note: Android will only show up as a possible build target if you successfully installed the Android Export Module during installation of the Unity Editor.

5 . Select your device as the build target:
- Make sure your VR device is turned on and plugged in.
- Next to the Run Device drop-down, click Refresh, then select your VR device.
- Note: If your device does not show up in the list, try putting on the device. It may prompt you to Allow USB debugging. If it is still not showing up in the list, try restarting your device, making sure it’s in Developer Mode, or restarting Unity.

6 . Build and run your project on your device:
- Click Build and Run. 
- When prompted to choose a location, create a new “Builds” folder, then Save your project as “[YourName] - VR Room - 1.1”.
- Note: When you build your app for the first time, it may take several minutes to compile. 

![image](https://user-images.githubusercontent.com/73842931/231869611-6d257d62-5687-497f-9cdf-8e8eec993704.png)

You should now be able to test the app on your device, untethered from your computer.
Note:  The app is automatically saved onto your device in the “Unknown Sources” section of your App Library. You may need to follow steps to [allow apps from unknown sources in order](https://www.meta.com/help/quest/articles/headsets-and-accessories/oculus-rift-s/unknown-sources/?utm_source=learn.unity.com&utm_medium=oculusredirect) to locate your app.
Troubleshooting tips:
- If the app runs, but it does not take up the entire field of view, it is likely a problem with plug-ins.
- If the app runs, but the entire scene moves along with your head, it is likely because you have the Device Simulator active or you do not have the Input Action Manager configured properly.

## Test on other OpenXR-compatible devices

If you are using a different OpenXR-compatible device, such as the Valve Index, HTC Vive, or a Windows Mixed Reality headset, follow this step to test on your device. Otherwise, skip this step.
In order to test the project on one of these devices, you need to install the OpenXR plugin and enable the feature set for your specific device.
1 . Configure the OpenXR Plugin for your device:

- Follow the instructions on the OpenXR Manual page to install the OpenXR Plugin, enable it in XR Plugin Management, and configure it for your particular device. 

2 . Connect your device through the SteamVR app: 
- Make sure your device is plugged into your computer using a compatible cable.
- Make sure the SteamVR app is running and has successfully recognized your device.

3 . Test the project on your device:
- Make sure the Device Simulator in your scene is disabled. If it is enabled, your head tracking will not work.
- Select Play in the Unity Editor and put on your headset.

You should now be able to quickly test your app on your headset through SteamVR.

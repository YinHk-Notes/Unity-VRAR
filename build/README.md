## Build

Build and run on your device (Meta Quest).
Since the Quest is a standalone device (meaning it does not need to be connected to a computer), you can build an app and test it directly on the device, disconnected from your computer. 
In order to build your app to the Quest headset, you will need to configure plug-ins for the Android build target. 

**Steps**:

1. Install the OpenXR for Android builds:
  - From the XR Plug-in Management settings, select the Android tab, then select OpenXR from the list of available Plug-in Providers to install that plug-in. 
Note: You will only have an Android tab if you installed the Android export module.
  - If you don’t see an option for OpenXR in the Android tab, first go back to the Desktop tab and select OpenXR there, then return to the Android tab.

2. Resolve warnings by setting up an interaction profile.
- Click on the new warning or error icon that appears to open the OpenXR Project Validation window, which will tell you again that you need to add an interaction profile. 
- Select the Edit button to open the OpenXR settings panel.

3. Prepare your scene for building: 
  - Make sure the XR Device Simulator in your scene is disabled. If it is enabled, your head tracking will not work.
  - From the top menu, click File > Build Settings.
  - Click Add Open Scenes to add your scene.

4.  Switch to the Android build platform: 
  - In the Platform section, select Android.
  - Click Switch Platform, and wait for your project to switch to the Android platform.
  - Note: Android will only show up as a possible build target if you successfully installed the Android Export Module during installation of the Unity Editor.

5.  Select your device as the build target:
  - Make sure your VR device is turned on and plugged in.
  - Next to the Run Device drop-down, click Refresh, then select your VR device.
  - Note: If your device does not show up in the list, try putting on the device. It may prompt you to Allow USB debugging. If it is still not showing up in the list, try restarting your device, making sure it’s in Developer Mode, or restarting Unity.

6.  Build and run your project on your device:
  - Click Build and Run. 
  - When prompted to choose a location, create a new “Builds” folder, then Save your project as “[YourName] - VR Room - 1.1”.
  - Note: When you build your app for the first time, it may take several minutes to compile. 

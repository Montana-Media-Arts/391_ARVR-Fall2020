---
title: Google Cardboard Set up
module: 10
jotted: true
---

# Setup

### Quickstart for Google Cardboard for Unity

This guide shows you how to use the Google Cardboard XR Plugin for Unity for Unity to create your own Virtual Reality (VR) experiences.

**Note:** Make sure to review the Cardboard branding guidelines before distributing your app to a wider audience.

You can use the Cardboard SDK to turn a smartphone into a VR platform. A smartphone can display 3D scenes with stereoscopic rendering, track and react to head movements, and interact with apps by detecting when the user presses the viewer button.

To get started, you'll use HelloCardboard, a demo game that demonstrates the core features of the Cardboard SDK. In the game, users look around a virtual world to find and collect objects. It shows you how to:

1. Set up your development environment
2. Download and build the demo app
3. Scan the QR code of a Cardboard viewer to save its parameters
4. Track the user’s head movements
5. Render stereoscopic images by setting the correct distortion for each eye
6. Set up your development environment

Software requirements:

1. Unity 2019.3.15f1 or later
2. Make sure to include Android and iOS Build Support during installation.
3. Git must be installed and the git executable must be on the PATH environment variable. See Unity's package manager git support docs for more details.
4. Import the SDK and create a new project
5. Follow these steps to import the Unity SDK and create a new project.

### Open Unity and create a new 3D project.

1. In Unity, go to Window > Package Manager.
2. Click + and select Add package from git URL.
3. Paste https://github.com/googlevr/cardboard-xr-plugin.git into the text entry field.
4. The package should be added to the installed packages.
5. Navigate to the Google Cardboard XR Plugin for Unity package. In the Samples section, choose Import into Project.
6. The sample assets should be loaded into Assets/Samples/Google Cardboard/<version>/Hello Cardboard/Assets.
7. Navigate to Assets/Samples/Google Cardboard/<version>/Hello Cardboard/Assets/Scenes, select Add Open Scenes, and choose HelloCardboard to open the sample scene.
**Note:** <version> is the X.Y.Z semantic version number of the released package (for example, 1.1.0).

### Configuring Android project settings
1. Navigate to File > Build Settings.
2. Select Android and choose Switch Platform.
3. Select Add Open Scenes and choose HelloCardboard.

#### Player Settings
Resolution and Presentation

1. Navigate to Project Settings > Player > Resolution and Presentation.
2. Set the Default Orientation to Landscape Left.

Other Settings

1. Navigate to Project Settings > Player > Other Settings.
2. Select only OpenGLES2 in Graphics APIs.
3. Select IL2CPP in Scripting Backend.
4. Select desired architectures by choosing ARMv7, ARM64, or both in Target Architectures.
5. Select Require in Internet Access.
6. Specify your company domain under Package Name.

Publishing Settings

1. Navigate to Project Settings > Player > Publishing Settings.
2. Select Custom Main Gradle Template in the Build section.
3. Add the following lines to the dependencies section of Assets/Plugins/Android/mainTemplate.gradle:

  implementation 'com.android.support:appcompat-v7:28.0.0'
  implementation 'com.android.support:support-v4:28.0.0'
  implementation 'com.google.android.gms:play-services-vision:15.0.2'
  implementation 'com.google.protobuf:protobuf-lite:3.0.0'

If Target API Level is set to API Level 29 or Automatic (highest installed) (resulting in API Level 29), the following steps are also required:

1. Select 'Custom Main Manifest' in the Build section.
2. Add the following attribute to the application tag of Assets/Plugins/Android/AndroidManifest.xml:

  <application android:requestLegacyExternalStorage="true" ... >
    ...
  </application>

#### XR Plug-in Management Settings

1. Navigate to Project Settings > XR Plug-in Management.

2. Select Cardboard XR Plugin under Plug-in Providers.

#### Build your project

1. Navigate to File > Build Settings.

2. Select Build, or choose a device and select Build and Run.

Configuring iOS project settings

1. Navigate to File > Build Settings.
2. Select iOS and choose Switch Platform.
3. Select Add Open Scenes and choose HelloCardboard.

Player Settings

1. Resolution and Presentation
2. Navigate to Project Settings > Player > Resolution and Presentation.
3. Set the Default Orientation to Landscape Left.

Other Settings

1. Navigate to Project Settings > Player > Other Settings.
2. Disable the Auto Graphics API option.
3. Choose only OpenGLES2 in Graphics APIs.
4. In Camera Usage Description, write Cardboard SDK requires camera permission to read the QR code (required to get the encoded device parameters)..
5. In Target minimum iOS Version, write 11.0.
6. Specify your company domain under Package Name.

Note: If using an iPhone X, select the Hide home button on iPhone X option.
XR Plug-in Management Settings

Navigate to Project Settings > XR Plug-in Management.

Select Cardboard XR Plugin under Plug-in Providers.

1. Build your project
2. Navigate to File > Build Settings.
3. Select Build or Build and Run.

<a href="https://developers.google.com/cardboard/develop/unity/quickstart" target="_new">Source</a>
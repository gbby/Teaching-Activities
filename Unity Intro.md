# 1. Intro to Unity

Unity is a cross-platform game engine that empowers you to "turn your visions into fully interactive experiences" according to its marketing language.

- Download it from https://unity.com/
- Open up the Unity Hub install a recent editor (Unity 6 is recommended). Don't worry about adding any packages for now.
- Once it launches, create a new project. We'll start with a Universal 3D template. Set a project name and appropriate location.

# 2. Explore the Interface

There are 5 main windows that you need to familiarize yourself with:
- The Scene Window. We'll typically arrange our experiences in the scene view. Hold the right mouse button to use WASD to fly around. Clicking the white cube in the centre of the viewer gizmo will change between 3D and isometric views.
- Project Window. This is where you will store all of our assets, including scripts, 3D files, textures, audio files, and scenes. It is very important to keep your project window tidy.
- Hierarchy Window. This shows us a list of all of the objects that are currently in our scene. Objects can be grouped in parent-child relationships, and are are listed in the hierarchy in the order they are added.
- Inspector Window. Here's where we can inspect and modify the properties of any asset that we select.
- Game view. The game view will allow us to activate the scene as if it was being played in a real game format.

Some things you'll want to try:
- The main toolbar is at the top. It contains a bunch of transform tools that you should explore.
- Change your default camera and light assets.
- Add some additional GameObjects and move them around.
- Click on your added objects and look in the Inspector Window. Click on Add Component. Try a particle system under Effects. Add some Physics, such as creating a rigidbody and giving it mass.
- Check out the asset store.

# 3. Populate Your Scene

Unless you are already a Unity wizard, you will need to configure scenes based on example templates and tutorials for the hardware device that you've chosen. We'll look at some different templates for AR/VR later in the course. Some different ways that we can populate our scenes include:
- Importing meshes from Blender and related applications. We can, for example, import entire .blend files like the map of OTU that we created earlier using Blosm.
- We can make use of available textures and materials, or we can design ones of our own outside of Unity and import them.
- We can procedurally generate assets. This is great for custom animated data visualizations.

What should you do over the break is go to https://learn.unity.com/ and try a few different tutorials.

# 4. Install and Try Some SDKs

- Mapbox AR https://www.mapbox.com/unity
- Google Geospatial Creator https://developers.google.com/ar/geospatialcreator

# 5. Configure a Basic AR Scene

- Ensure that you've got Android Build Support, Open JDK, and Android SDF and NDK Tools added. If you didn't add these when you installed Unity, you can click on the gear next to the Unity editor version in the Hub to add them.
- Create an AR Mobile project.
- Read through this page: https://docs.unity3d.com/Packages/com.unity.template.ar-mobile@1.0/manual/index.html
- Follow the instructiosn on this page: https://developers.google.com/ar/develop/unity-arf/getting-started-ar-foundation
- Here's a video walkthrough: https://www.youtube.com/watch?v=JnLzoXETbWs
- Sample templates can be found here: https://github.com/Unity-Technologies/arfoundation-samples

# 6. Configure for the Meta Quest SDK

- Create a 3D Core project.
- For developing extended reality content, we can either use the Unity XR Interaction Toolkit or the Meta XR SDK. We'll use the Meta XR SDK.
- Go to the Unity AssetStore and install the Meta XR All-in-One SDK at https://assetstore.unity.com/packages/tools/integration/meta-xr-all-in-one-sdk-269657 and open it in Unity. You will need to install it in the Package Manager window that opens, and will then need to restart your editor. Once you do, you can find the SDK in the Packages folder of the Project Tab. 
- Open the File/Build Profiles window. Under Platform, select Android and then press the Switch Platform button.
- Open Edit/Project Settings, and select XR Plug-in Management. 
- Install XR Plugin Management. In the Windows, Mac, and Linux Settings tab, select either Oculus or Open XR (we'll use Open XR). 
- Open Meta/Tools/Project Setup Tool. Make sure that any outstanding errors are fixed and apply any additional changes. 
- Go to Meta/Tools/Building Blocks and start exploring.
- When you have a scene that you like, save it and add it to your Build Settings.
- Connect a previously configured Quest 3. Make sure it is set to the device you plan to build to. Click Build and Run.
- More details can be found here: https://unity.com/blog/engine-platform/get-started-developing-for-quest-3-with-unity and https://developers.meta.com/horizon/documentation/unity/unity-development-overview/

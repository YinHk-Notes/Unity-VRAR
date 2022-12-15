## XR Interaction Toolkit 2.2.0

The XR Interaction Toolkit package is a high-level, component-based, interaction system for creating VR and AR experiences. It provides a framework that makes 3D and UI interactions available from Unity input events. 


XR Interaction Toolkit contains a set of components that support the following Interaction tasks:

- Cross-platform XR controller input: Meta Quest (Oculus), OpenXR, Windows Mixed Reality, and more.
- Basic object hover, select and grab
- Haptic feedback through XR controllers
- Visual feedback (tint/line rendering) to indicate possible and active interactions
- Basic canvas UI interaction with XR controllers
- Utility for interacting with XR Origin, a VR camera rig for handling stationary and room-scale VR experiences


To use the AR interaction components in the package, you must have the AR Foundation package in your Project. The AR functionality provided by the XR Interaction Toolkit includes:

- AR gesture system to map screen touches to gesture events
- AR interactable can place virtual objects in the real world
- AR gesture interactor and interactables to translate gestures such as place, select, translate, rotate, and scale into object manipulation
- AR annotations to inform users about AR objects placed in the real world

| Term | Meaning |
| --- | --- |
| Controller | A component that turns XR controller input such as a button press into interaction events like hover, or select. Also provides a way to show controller models and send haptic feedback to the controller. |
| Object | Anything that the user sees or interacts with in the virtual world. |
| Interactor | An object in a scene that can select or move another object in that scene. |
| Interactable | An object in a scene that the user can interact with (for example, grab it, press it, or throw it). |
| Hover | The state where an Interactor is in a valid state to interact with an object. This differs between Ray and Direct interaction. |
| Select | The state where an Interactor is currently interacting with an object. |
| Interaction Manager | A manager component that handles interaction between a set of Interactors and Interactables. |
| Gesture | Sequences of movements that translate into an action that manipulates an interactable. |
| Annotation | A piece of content placed above (or next to) an AR object to give users information and context. |
| Haptic | Sensory or visual stimuli that is sent to the user to give feedback for interaction. |

### Unity XR interaction toolkit 2.2.0 package doc
https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.2/manual/index.html

### Scripting API
https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.2/api/index.html

### Components
https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@2.2/manual/components.html


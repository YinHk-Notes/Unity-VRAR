## Locomotion

| Term | Meaning |
| --- | --- |
| XR Rig | MonoBehaviour that specifies a Rig, a Camera Offset, a Camera. Also provides Stationary or Room-Scale options of tracking space to configure the XR Rig. |
| Rig | The base GameObject of the XR Rig. This is the GameObject that will be manipulated via locomotion. By default it is the object that XR Rig is attached to. |
| Camera Offset | GameObject to move the Camera to desired height off the floor. |
| Camera | GameObject that contains a camera component, this is usually the main camera that renders what the user sees, and is usually the 'head' of XR rigs. |
| Room-Scale | A floor-relative tracking mode. When the scene starts, the origin is the floor. |
| Stationary | A device-relative tracking mode. When the scene starts, the origin is the device. The camera will be moved to the height set by Camera Offset. |
| Locomotion System | MonoBehaviour that controls which Locomotion Provider has the access to move the Rig. |
| Locomotion Provider | Base class for various locomotion implementations. |
| Teleportation | A type of locomotion that teleports the user from one position to another position. |
| Snap Turn | A type of locomotion that rotates the user by a fixed angle. |

https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@0.0/manual/locomotion.html

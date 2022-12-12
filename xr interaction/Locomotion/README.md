## Locomotion
The XR Interaction package provides a set of locomotion primitives to provide the means to move about a scene during an XR experience. These components are:

- An XR Rig that represents the player
- A Locomotion System
- A Teleportation System, with Teleportation destinations
- A Snap Turn System
The following sections of this document outline how to use and extend these systems.



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

### XR Rig
The XR Rig is used by the Locomotion System as the anchor for the player.

### Locomotion System
The Locomotion System is a Monobehaviour that acts as the arbitrator for Locomotion Providers access to an XR Rig.

### Locomotion Providers
Locomotion Providers are where different types of locomotion are implemented. Two Locomotion Providers are supplied as part of the XR Interaction package. The **Teleportation Locomotion Provider** and the **Snap Turn Locomotion Provider**. Both implement the `LocomotionProvider` abstract class.

The XR Interaction system provides two implementations of a Locomotion Provider. The **Teleport Locomotion Provider**, and the **SnapTurn Locomotion Provider**.

### Snap Turn
The XR Interaction package provides an example implementation of a **Snap Turn Provider**. A Snap turn is when the user is rotated some fixed amount when an configured input is recevied. E.G: a joystic is moved to the left, or a dpad is pressed to the right.

### Teleportation
The XR Interaction system provides a simple implementation of teleportation. The **Teleportation Provider** Component implements the LocomotionProvider abstract class.

The Teleportation Provider inherits from the LocomotionProvider abstract class. The Teleportation Provider is responsible for moving the XR Rig to the desired location as requested by the user.

This implementation has two types of teleportation destinations. An 'Anchor' Based teleportation destination, and an 'Area' Based teleportation destination. These are discussed in more detail further below. In short:

- **Anchors** will always teleport the user to a specific position and/or rotation specified by the anchor.
- **Areas** allow the player to choose a location on a surface that they wish to teleport to.
Both types of teleportation destinations are implemented on top of the XR Interaction system using the Base Teleportation Interactable as the starting point for shared code.

### ref
https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@0.0/manual/locomotion.html

## Locomotion
The XR Interaction Toolkit package provides a set of locomotion primitives that offer the means to move around in a scene during an XR experience. These components include:

- An XR Origin that represents the user
- A Locomotion System that controls access to the XR Origin
- A Teleportation Provider and Teleportation Interactables
- A Snap Turn Provider that rotates the user by fixed angles
- A Continuous Turn Provider that smoothly rotates the user over time
- A Continuous Move Provider that smoothly moves the user over time
- A Grab Move Provider that moves the user counter to controller movement
- A Two Handed Grab Move Provider that can move, rotate, and scale the user counter to controller movement

| Term | Meaning |
| --- | --- |
| XR Origin | The component that implements the generic concept of a camera rig. It also provides options of tracking origin modes to configure the reference frame for positions reported by the XR device. It has properties to specify an Origin, a Camera Floor Offset Object, and a Camera Object. |
| Origin | By default, the Origin is the GameObject that the XR Origin component is attached to, and the term is generally used interchangeably with XR Origin. This is the GameObject that the application will manipulate via locomotion. |
| Camera Floor Offset Object | The GameObject to move the Camera to the desired height off the floor depending on the tracking origin mode. |
| Camera Object | The GameObject that contains a Camera component. This is usually the Main Camera that renders what the user sees. It is the head of XR rigs. |
| Floor mode | A floor-relative tracking origin mode. Input devices will be tracked relative to a location on the user's floor. |
| Device mode | A device-relative tracking origin mode. Input devices will be tracked relative to the first known location. The Camera is moved to the height set by the Camera Y Offset value by moving the Camera Floor Offset Object. |
| Locomotion System | The component that controls which Locomotion Provider can move the user. |
| Locomotion Provider | The base class for various locomotion implementations, such as teleportation and turning. |
| Teleportation | A type of locomotion that teleports the user from one position to another position. |
| Snap Turn | A type of locomotion that rotates the user by a fixed angle. |
| Continuous Turn | A type of locomotion that smoothly rotates the user by an amount over time. |
| Continuous Move | A type of locomotion that smoothly moves the user by an amount over time. |
| Grab Move | A type of locomotion that moves the user counter to controller movement, as if the user is grabbing the world around them. |
| Action-based | The recommended type of input based on referencing the Actions and their controller bindings in the Input System. |
| Device-based | An alternative type of input based on reading inputs from a InputDevice. |

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

#### Teleport Area Interactable
The Teleport Area interactable allows the user to select any location within the teleport anchor as their destination. 

#### Teleport Anchor Interactable
The Teleport Anchor allows the user to teleport to an anchor location by selecting the anchor, or an area around it. 

### ref
https://docs.unity3d.com/Packages/com.unity.xr.interaction.toolkit@0.0/manual/locomotion.html

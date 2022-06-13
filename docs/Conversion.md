## Binding Layout Conversion
If a developer only has access to an Xbox 360 controller when making their game, and thusly only adds Xbox 360 controller binding layouts, we don't want the user to have to create their own Binding Layout from scratch if they are using a different type of controller.

Because of this the external remapper provides a tool to automatically convert a binding layout from one Interaction Profile to another. This process is entirely data-driven and can go through multiple stages e.g. Xbox 360 -> Generic Controller -> Dualshock 3.

## Device Type Coercion
That's all well and good for when the user can use the external runtime to modify the converted Binding Layout but what about when the user does not have it activate?

This is where Device Type coercion is used. In the above example the Dualshock 3 controller would just pretend to be an Xbox 360 controller (it's glyphs would remain DS3 however). For users this should be far easier to understand and use at the cost of loosing device specific features.

Device Type coercion also allows devices of different types to be aggregated in the same interaction profile. This makes co-pilot setups easier for users with two different controller types. Co-pilot with different device types is possible without coercion, it just requires creating a binding layout per device type.

Device Type coercion is also useful when dealing with controllers of the same family. A controller family is a group of multiple controllers with similar layouts / features.

### Families
Xbox:
- Xbox 360
- Xbox One
- Xbox One Series SX

Dualshock Touchpad:
- Dualshock 4
- Dualshock 5

Switch Pro:
- Switch Pro Controller
- Dual Joycons

Oculus Touch:
- Oculus Touch CV1
- Oculus Touch Rift S
- Oculus Touch Quest

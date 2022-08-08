When an input event enters the pipeline it can cause zero or more events at every stage. These events need to be cleaned up / processed by their creators once they have been used and can sometimes be fed back into the same system.

As the input backend increases in complexity we could end up adding more systems and connections between systems.

Since we will be dealing with relatively few events I don't think there is any need for multithreading though the kind of pipeline I want to design should be fairly easy to parallelize.


## Input Component Event
```
Boolean: IsPressed bool
Delta2D: Delta (f64, f64)
Cursor: Position (f64, f64), Window: Option<WND>

## Action Event
Boolean= IsPressed: bool, Changed: bool
Delta2D= Delta: (f64, f64)
Cursor= Position: (f64, f64), Window: Option<WND>

## Action State
Boolean= IsPressed: bool, Changed: bool
Delta2D= Delta(f64, f64)
Cursor= Position: (f64, f64), Window: Option<WND>
```

1. Device state changes or continuous state is polled
2. Driver sends an input event to the runtime (the driver may apply some calibration)
3. The runtime applies extra calibration to the input event (custom dead zones / gyro)
4. The runtime updates the cached device state
5. The runtime sends an event to all interaction profiles the device is in
6. aggregation
7. The interaction profile sends an event to all users using the interaction profile
8. The user sends an event to every binding layout targeting the interaction profile
9. The binding layout sends an event to every binding targeting the updated component
10. The bindings are executed
11. The binding layout sends an event to the user for every action event
12. aggregation
13. The user updates its action state and sends an event to its session

## Device / Interaction Profile Graph

### Device
A device is the lowest common factor of a collection of input / output components. LCF meaning that a DualSense would be one device and a Wiimote and Nunchuck would be two devices since a Wiimote can exist without the Nunchuck's components and visa versa. 

However some device components can just be listed as optional for simplicities sake. For example the gyro component of the Wiimote is just listed as optional instead of having an extra device for Motion Plus.


### Device Bundle
A collection of devices which optionally expose a Bundle Interaction Profile

Custom Bundles -> Two Xbox controllers
Standard Bundles -> Left + Right Joycons

### Interaction Profile
An interaction profile is the final stage of components which a Binding Layout actually interacts with. The binding layout is not aware of what types of devices are actually backing the interaction profile, apart from when it is choosing Input Glyphs to display.

#### Bundle Interaction Profile
External runtime only

#### Standard Interaction Profile
User paths and such


## Primitive Input Types
### Event?
A type of boolean action that only produces events
On poll it returns the number of times it has been activated

### Boolean
Repeat presses? TODO
On or Off
Input Examples: Mouse Button, Keyboard Key
Action Examples: Jump, Sprint, Use item
Combination: OR every value

Output: If the action type is sticky the application can unstick it

### Value
Range: 0 ≤ x ≤1
Input Examples: Trigger, Analog Keyboard Key
Action Examples: Move Forward, Vehicle Accelerate
Combination: Binding with greatest value

### Axis1D
Range: -1 ≤ x ≤ 1
Input Examples: Steering Wheel, Volume Dial
Action Examples: Steer Vehicle, Move (2D side-scroller)
Combination: Binding with greatest absolute value

### Axis2D
Range: -1 ≤ x ≤ 1 and -1 ≤ y ≤ 1
Input Examples: Joystick
Action Examples: Move
Combination: Binding with greatest length

### Delta1D
Input Examples: 1D Scroll Wheel, Volume Wheel
Action Examples: Scroll 1D, Zoom, Adjust Volume, Turn VR
Combination: SUM of every value

Usage Note:
If the application is using the Delta1D action to turn the camera its state **must** be interpreted as degrees.

### Delta2D
Input Examples: Mouse, Treadmill, Trackball, 2D Scroll Wheel
Action Examples: Turn Camera, Walk, Scroll
Combination: SUM of every value

Usage Note: If the application is using the Delta2D action to turn the camera its state **must** be interpreted as degrees.

## Complex Input Types
### Cursor
Input Examples: System Cursor, Wiimote IR sensor
Action Examples: Menu Cursor, Free Moving Crosshair, Radial Menu?
Combination: Latest moved cursor
Data: The normalized position of the cursor inside the application's window.

Output: The application can set the position of the cursor and the cursor texture

Usage Note: The application MUST use this to access and set the position of the hardware cursor unless necessary, this is to seamlessly enable the usage of a software cursor

### Wheel
Input Examples: Simulation Wheel
Combination: Binding with greatest rotation
Data: The absolute angle of the wheel in degrees and the range of the wheel (e.g. 180° or 900°)

### XrPose
Input Examples: XR Controller
Combination: First active binding
Data: Absolute position, orientation, velocity and acceleration in a specific OpenXR coordinate space

### Gyro
Input Examples: XR Controller, Smartphone, Modern Game Controller
Combination: First active binding
Data: Calibrated angular velocity and best guess orientation 

### Accelerometer
Input Examples: XR Controller, Smartphone, Modern Game Controller
Combination: First active binding
Data: Local acceleration and best guess gravity direction

### TouchPoints
Input Examples: Touchscreen, Touchpad
Combination: Binding with most active points / latest changed
Data: TODO

### Magnometer?
### Microphone?

## Hybrid Action Types
Takes more action state out of the application's hands. By doing this the runtime can enable more complex functionality with little extra effort from the developer.

### Hotbar
Input Examples: Stick shift
Action Examples: Item hotbar, Gear selection
Combination: Latest changed binding

An action with N states, marked as boolean child actions. One of these child actions is marked as 'selected' at any given time. 

It has two other child actions called `Shift Positive` and `Shift Negative` which shift the selected index accordingly.

The application can mark one state as default and whether shifting should wrap around.

## Sticky Boolean
Input Examples: N / A
Action Examples: Aim down sights, Sprint, Couch
Combination: Boolean child OR Sticky state

## Player Orientation 
Delta2D
Euler angles / Quaternion
Reset View

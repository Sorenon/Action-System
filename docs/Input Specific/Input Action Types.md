## Primitive Input Types
### Boolean
Sticky?
Repeat presses?
Event only?
On or Off
Input Components: Mouse Button, Keyboard Key
Action: Jump, Sprint, Use item
Combination: OR every value

### Value
Range: 0 ≤ x ≤1
Input Components: Trigger, Analog Keyboard Key
Action: Move Forward, Vehicle Accelerate
Combination: Binding with greatest value

### Axis1D
Range: -1 ≤ x ≤ 1
Input Components: Steering Wheel
Action: Steer Vehicle, Move (2D side-scroller)
Combination: Binding with greatest absolute value

### Axis2D
Range: -1 ≤ x ≤ 1 and -1 ≤ y ≤ 1
Input Components: Joystick
Action: Move
Combination: Binding with greatest length

### Delta1D
Input Components: 1D Scroll Wheel
Action: Scroll, Zoom, Adjust Volume
Combination: SUM of every value

### Delta2D
Input Components: Mouse, Treadmill, Trackball, 2D Scroll Wheel
Action: Turn Camera, Walk
Combination: SUM of every value

## Complex Input Types
### Wheel
Input Components: Simulation Wheel
Combination: Binding with greatest rotation
Data: The absolute angle of the wheel in degrees and the range of the wheel (e.g. 180° or 900°)

### XrPose
Input Components: XR Controller
Combination: First active binding
Data: Absolute position, orientation, velocity and acceleration in a specific OpenXR coordinate space

### Gyro
Input Components: XR Controller, Smartphone, Modern Game Controller
Combination: First active binding
Data: Calibrated angular velocity and best guess orientation 

### Accelerometer
Input Components: XR Controller, Smartphone, Modern Game Controller
Combination: First active binding
Data: Local acceleration and best guess gravity direction

### TouchPoints
Input Components: Touchscreen, Touchpad
Combination: Binding with most active points / latest changed
Data: TODO

### Cursor
Input Components: System Cursor, Wiimote IR sensor
Combination: Latest moved cursor
Data: TODO

### Magnometer?
### Microphone?
## Primitive Input Types
### Boolean
Sticky? TODO
Repeat presses? TODO
On or Off
Input Examples: Mouse Button, Keyboard Key
Action Examples: Jump, Sprint, Use item
Combination: OR every value

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
Usage Requirements:
If the application is using the Delta1D action to turn the camera its state **must** be interpreted as degrees.

### Delta2D
Input Examples: Mouse, Treadmill, Trackball, 2D Scroll Wheel
Action Examples: Turn Camera, Walk, Scroll
Combination: SUM of every value
Usage Requirements:
If the application is using the Delta2D action to turn the camera its state **must** be interpreted as degrees.

## Complex Input Types
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

### Cursor
Input Examples: System Cursor, Wiimote IR sensor
Combination: Latest moved cursor
Data: TODO

### Magnometer?
### Microphone?
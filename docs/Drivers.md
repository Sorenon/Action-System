All input and output in SuInput is handled via one or more drivers. There are multiple types of drivers, most can be initialized by the external runtime while one must be initialized by the application.

## Window Driver
The one required driver is known as a **Window Driver** this driver is the sole responsibility of the application and cannot be updated by the external runtime (with some exceptions). Because of this developers must make sure to implement the driver correctly as the external runtime won't be able to correct them. The Window Driver is responsible for passing all data to SuInput which it cannot access through other Drivers and there **should** be one Window Driver per runtime (OpenXR applications do not need Window Drivers). 

TODO make a list of needed events for each target

To make implementing a Window Driver easier SuInput provides Framework Window Drivers and Hooking Window Drivers. Framework drivers take raw events from either the OS or established Window Libraries (e.g. SDL2 or GLFW) and processes them for SuInput. Hooking Drivers use OS hooks to access low level events but are not available on many platforms and may need permissions to run. These Window Drivers can be updated by the external runtime. SuInput may ignore some events from the Window Driver if it has a better method of accessing a certain type of event. For example on Windows SuInput will ignore Keyboard and Mouse events from the Window Driver as it can better access this through Raw Input. 

## Generic Driver
Zero or more **Generic Drivers** can be added to a runtime. A Generic Driver provides one or more device types for SuInput. 

If the user has an external runtime installed, application embedded Generic Drivers will be ignored by SuInput and replaced with the external runtime's equivalents.

The Generic Driver must register itself for a device type before it can create any instances of that type. It either registers the type as TOTAL or SUPLIMENTAL, if more than one driver registers itself as TOTAL only input from one drive will be accepted.

TODO Prevent multiple SUPLIMENTAL drivers colliding

## Provided Window Drivers
TODO

## Provided Generic Drivers
### Win32 Raw Input
Event Based
Devices: Mouse, Keyboard, System Cursor
Standard Interaction profiles: 

- Mouse, Keyboard and Cursor
- Keyboard Only

### Linux XInput2
Event Based
Devices: Mouse, Keyboard, System Cursor
Standard Interaction profiles:

- Mouse, Keyboard and Cursor
- Keyboard Only

### SDL2
Event / Polling Based
Devices: All SDL supported controllers
Standard Interaction Profiles: 

- Dualshock 4
- DualSense
- Xbox 360 (XInput / sdl2 generic gamepad)
- Xbox One
- Switch Pro
- Joy-Con Pair
- Left Joy-Con
- Right Joy-Con
- GameCube
- Generic Joystick

Features: Gyro, Accelerometer, Rumble, HD Rumble, LED, Player Number, Touch Points, Adaptive Triggers, Microphone, Speaker, Cursor, IR

### Wii
Event Based
Devices: 

- Wiimote
- Wii Nunchuck
- Classic Controller
- Classic Controller Pro

Standard Interaction Profiles: 

- Wiimote
- Wiimote + Nunchuck
- Wiimote + Classic Controller
- Wiimote + Classic Controller Pro

Features: Gyro, Accelerometer, Rumble, Cursor, Speaker, IR

### OpenXR (Monado?)
Polling based
Devices: -
Standard Interaction profiles: OpenXR interaction profiles
Features: XrPose, Gyro, Accelerometer, HD Rumble

### Eyegaze?
### Simulation rigs?
### Analogue Keyboards (Wooting)?
### NDA Drivers? (PS5, Switch, etc.)
### Steam Input?
### STT?
### Razer Chroma?
### Logitech Gamepanel?
### Logitech G-Key?
### Logitech LED?
### Logitech Steering Wheel?
### Artemis?
### OpenRGB?

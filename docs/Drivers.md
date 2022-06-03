## Engine Drivers
TODO

## Hooking Drivers
In order to make using SuInput as painless as possible it comes with a selection of 'hooking' drivers. In order to use these all the application has to do is tell SuInput to use them. They have the benefit of almost always working as intended and being easy to upgrade with an external runtime. 

They come with a few downsides, the first is that their hooking nature may trigger some Anti-Virus or Anti-Cheat software (but most modern antivirus solutions are smart enough to ignore our hooks). The second is battling against the Game Engine / Platform API to actually be able to receive uninterrupted input without breaking anything.

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

An Interaction Profile is a collection of one or more devices which will be used together. For example `Xbox One Controller`,  `Mouse and Keyboard`, and  `Valve Index Controllers` are all standard interaction profiles.

Multiple interaction profiles can be used at once to allow for mixed input. However more advanced users can take this further by creating custom interaction profiles. For example two mice, or a Dualsense with floor pedals and back buttons. 

Binding Layouts targeting a certain interaction profile can be automatically converted to other similar interaction profiles. For example, if an application only has default bindings for an Xbox 360 controller SuInput will be able to convert those bindings to target almost any other generic controller. Once the bindings have been converted they can be edited as if they targeted the other interaction profile.

Interaction profiles are also in command of what input glyphs the game uses. 

### Gameplay Semantic Profile
- Delta2D, Turn Camera / Move Cursor (Mouse Delta, XInput Right Thumbstick)
- Axis2D, Move (WASD, XInput Left Thumbstick)
- Button, Attack (Mouse Left, XInput Right Trigger)
- Button, Use (Mouse Right, XInput Left Trigger)
- Button, Reload ('R', XInput 'X')
- Button, Jump (Space, XInput 'A')
- Button, Crouch (Ctrl, XInput 'B')
- Button, Sprint (Shift, XInput Left Thumbstick Click)
- Button, Menu (Escape, XInput Start)
- Button, Item Right (Scroll Up, XInput Right Bumper)
- Button, Item Left (Scroll Down, XInput Left Bumper)

### GUI Semantic Profile
- Delta2D, Scroll (Scroll wheel)
- Delta1D, Zoom (Trackpad Pinch, Ctrl + Scroll wheel)
- Button, Up (Up Key, XInput DPad Up, XInput Left Thumbstick Up)
- Button, Left (Left Key, XInput DPad Left, XInput Left Thumbstick Left)
- Button, Down (Down Key, XInput DPad Down, XInput Left Thumbstick Down)
- Button, Right (Right Key, XInput DPad Right, XInput Left Thumbstick Right)
- Button, Select (Mouse Left, Enter, XInput 'A')
- Button, Back (Backspace, XInput 'B')
- Button, Exit (Escape, XInput Menu)
- Button, Tab Right ('E', XInput Right Bumper)
- Button, Tab Left ('Q', XInput Left Bumper)
- Button, Menu Right ('D', XInput Right Trigger)
- Button, Menu Left ('A', XInput Left Trigger)

TODO sharing devices between players
TODO automatic device consumption
TODO automatic layout generation
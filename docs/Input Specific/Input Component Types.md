S -> Simple
M -> Medium 'Normal'
A -> Advanced

## Button (Boolean)
Component Conversions

- None

Activators: [[Button Activators]]
Action Conversions

- S: Button -> Boolean
- S: Button -> Value
- M: Button -> Axis1D
- M: Button -> Axis2D
- M: Button -> Delta1D
- M: Button -> Delta2D
- M: Button -> Cursor

## Trigger / Analog Key (Value)
Component Conversions

- S: Trigger -> Button (soft pull, full pull, zones)
- M: Trigger -> Cursor

Action Conversions

- S: Trigger -> Value

## Joystick (Axis2D)
Component Conversions

- S: Joystick -> Button (Sector)
- S: Joystick -> Trigger (Sector)
- M: Joystick -> Move1D (Spin)
- M: Joystick -> Trigger (Length)
- M: Joystick -> Button (Zone)
- M: Joystick -> Cursor

Action Conversions

- S: Joystick -> Axis2D
- M: Joystick -> Delta1D (Flickstick)
- S: Joystick -> Delta2D

## Move1D (Delta1D)
Component Conversions

- None

Action Conversions

- S: Move1D -> Delta1D
- S: Move1D -> Boolean (Fire debounced impulses on input)

## Move2D (Delta2D)
Component Conversions

- M: Move2D -> Move1D (Split directions)
- A: Move2D -> Button (Gestures)

Action Conversions

- S: Move2D -> Delta2D
- S: Move1D -> Boolean (Fire debounced impulses on input)

## Touchpad (Touch Points)
Component Conversions

- S: Touchpad -> Move2D (Drag)
- S: Touchpad -> Button (Touch, Swipe, Gesture, Zones)
- S: Touchpad -> Move1D (Pinch, Gesture)
- S: Touchpad -> Joystick
- M: Touchpad -> Cursor

Action Conversions

- S: Touchpad -> Touch Points

## Cursor
Component Conversions

- None

Action Conversions

- S: Cursor -> Touch Points
- S: Cursor -> Cursor

## Motion (Combined Gyro + Accel)
Component Conversions

- M: Motion -> Button (Lean, Shake, Thrust)
- M: Motion -> Value (Lean, Shake, Thrust)
- M: Motion -> Move2D (As Mouse)
- M: Motion -> Axis1D (As Wheel)

Action Conversions

- S: Motion -> Gyro (Orientation)
- S: Motion -> Acceleration (Gravity)

## TODO Touchscreen
## TODO Radial Menu
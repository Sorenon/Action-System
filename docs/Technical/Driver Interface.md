## Input Events
The driver tells the runtime about changes in state through Input Events

### Motion and Pose
Types of Motion and Pose components:
- Accelerometer -> Acceleration, can be used to guess gravity direction
- Gyroscope -> Angular Velocity, may require calibration
- Magnetometer -> Orientation, missing from many devices and often low quality
- Pose -> Position, Orientation and Velocities, typically only provided by XR devices

#### Accelerometer Gyroscope Magnetometer
These are three simple sensors used for approximating a device's kinetic state. 

SuInput assumes that the values of all three sensors will be local to the device's transformation and that the units are m/s<sup>2</sup>, Gs and μT accordingly.

TODO should angular velocity be in radians at the driver level?
TODO should accelerometer data really be in Gs?

If a device has one or more of these sensors the runtime uses sensor fusion to extrapolate data.

TODO should the driver be able to provide its own sensor fused data

Due to sensor fusion if one or more of these sensors are present in a device they should all be updated using one BatchInputUpdate. Otherwise the runtime will run the sensor fusion algorithm for every event with outdated information. However if one or more components have not generated an event it should be ok for the driver to send only the other events as the runtime will just use the previous data.

#### Pose
Pose is a highly processed form of component as deterministic position requires input from many complicated systems such as lasers, cameras and magnetic field generators. 
Due to the high levels of complexity and specialization SuInput leaves all this work to the driver.

TODO Figure out how different spaces should be communicated
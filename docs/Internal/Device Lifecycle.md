## On Device Connect

Driver registers device, specifying its parent and if the parent's name should change

If device does not have siblings: (for now this is always true) 
If external runtime is installed a pop-up asks if this device is a new player or should be added to an existing player
If no external runtime: Ask game which player device should go to, by default the device will go to either the first player without a controller or player 1. If the device is a Mouse or Keyboard it will always go to player 1

If the device has siblings: (for now this is always false)
If the siblings are not bound to a player then just log a connect message
If the siblings are bound to a player but are in custom bundles or std bundles with coercion then log
If the siblings are bound to a player in a standard bundle with no coercion then ask player if upgrade bundle to accept new device
If player declines then device does not get added to player
If player accepts then standard bundle gets upgraded to new device bundle yadayada 

Then changes to bundles have to be propagated

Since device changes don't happen that often its fine to just destroy the old interaction profiles and rebuild them. This looses all Binding State so we may want to implement a better way in future

## On Device Disconnect

Alert Game
Alert Player

Remember Device for a few in case it gets reconnected
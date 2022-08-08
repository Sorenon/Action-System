
## Off-Thread processing
Possible performance improvements / lower latency
Action callback is called from the 'working thread'
The sync function does nothing

## Synchronous binding processing (New approach)
Action state callbacks are called during a sync call
All binding processing takes place during the sync call

Input is buffered off-thread, though some drivers may sync during the sync call for lower latency

Embedded Runtime Lifecycle:

App loads runtime
App adds driver

Runtime initializes Driver
Driver adds device
Runtime registers device
Driver sends Input
Runtime caches input
Runtime sends input events to running sessions

App creates instance
App creates Actions
App creates Default Binding Layouts
App creates session
Runtime syncs session on create
Action Sets are disabled by default so not much happens

~~
App gets action state
App syncs session
Session handles changes in devices
Session enables action sets against cached interaction profile state
Session disables action sets against cached interaction profile state
Session applies cached input events to bindings
~~


Is there a reason why session need devices?
Probably needed for outputs

Outputs:
Streaming Components: e.g. Cursor, Pose -> Device for each component is selected at sync time?
Outputs: e.g. Haptic / Vibration -> Device for each component is selected at sync time?  
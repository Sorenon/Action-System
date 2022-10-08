## Runtime
An abstraction over either an embedded or external SuInput runtime and is used to create Instances.

There should only be one of these per process.

## Instance
Similar to Vulkan and OpenXR, an Instance is how applications accesses SuInput's API.

Since there are already Runtime and Application Instance types it is possible that this abstraction is unnecessary however it could be useful if SuInput ever provides OpenXR-like extensions.

## Application
The Application is a structure containing useful metadata about the application such as name and version.

It is used by SuInput to group similar Application Instances together.

## Application Instance
An Application Instance is an (optionally) persistent object containing all the required details about one specific install of an Application.

On creation it takes some parameters which become immutable during it's Session's lifespan:
- The base Application
- Extra metadata specific to this application install
- All the Static Action Sets the for the application
- All the default Binding Layouts

It also has these mutable members:
- Dynamic Action Sets
- Is installed predicate (Override how the external runtime checks if an app is still installed)

## Session
An SuInput Session.

Similar to OpenXR, a Session is the actual 'running' part of the application. However, unlike OpenXR where there is one Session per user, an SuInput Session can have 0 or more Users.

Each Session is created from an Application Instance and each Application Instance can only have one Session running at once.

## Action Set
A group of Actions which will be categorised together and enabled or disabled simultaneously.

They come it two types:
- Static: Immutably attached to Application Instances on their creation. Easiest to use. Can be shared between Application Instances.
- Dynamic: Can be edited and added / removed from Application Instances during runtime. Cannot be shared between Application Instances. 

Every Action Set can have a parent Action Set. If an Action Set has a parent Action Set it is know as an **Action Layer** and can only be enabled if it's parent Action Set is enabled.

## Action
An abstracted Input / Output endpoint.
Each Action has a specific type. e.g. Boolean, Delta2D, LED or Rumble
Actions themselves do not have states and can be seen as just labels for the application to efficiently communicate with the runtime.

## Binding Layout
A set of Bindings from one Interaction Profile to several Action Sets.
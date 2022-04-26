A **Binding Layout** is a collection of bindings targeting a specific interaction profile. 

## Application API
For every interaction profile an application intends to directly support, it should create and submit at least one default Binding Layout. Default Binding Layouts can only be submitted until the SuInput session has been finalized.

While the session is running the application may be able to modify the user's active binding layout. The modifications **must** be controlled by the user and the submission **must** only occur due to an explicit action from the user (e.g. clicking an 'Apply' button).

## Sharing
Using the external mapping tool users will be able to export their Binding Layouts to KDL? files. Likewise users will be able to import Binding Layouts. 

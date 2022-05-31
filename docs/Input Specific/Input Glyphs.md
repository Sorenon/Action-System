Since Applications are mostly unaware of what devices the user is using, they should query SuInput for a user friendly message or an image to describe an action's bindings.

## Stylized Glyphs
Some Games will want to provide their own glyphs to better match their art style.

To do this they can request the paths for the bindings to a certain action. SuInput will only return paths of interaction profiles that the application has created binding layouts for. Paths will be of the format `/interaction_profile/.../user/.../input/...`

However using the external runtime the user will be able to overrule this behaviour and force the application to use SuInput's glyphs. This is done for users who may struggle to make out stylized glyphs for a multitude of reasons such as poor vision or display quality. 

## Overlay?
If an application missuses the system users could enable an overlay which gives a better description of bindings for the active actions?

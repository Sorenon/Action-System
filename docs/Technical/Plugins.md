# Plugins

## Summary
| Name         | Desktop | OpenXR | Console | Mobile / Quest |
| ------------ | ------- | ------ | ------- | -------------- |
| Unity        | ❌      | ❌     | ❌      | ❌             |
| Godot        | ❌      | ❌     | ❌      | ❌             |
| Unreal       | ❌      | ❌     | ❌      | ❌             |
| OpenXR layer | ❌      | ❌     | N/A     | ?              |
| Bevy         | ❌      | ❌     | ❌      | ❌             |

## Unity
As the most popular game engine supporting Unity is high priority

Unity already has a very popular action based input plugin called Rewired. It lacks support for desktop gyro, multiple mice / keyboards, external configuration, advanced binding / activators / chords, VR, etc. However it is well embedded into the Unity ecosystem and very popular, falling back on Unity input for unsupported platforms, written in pure C# for easy porting, player centric input, SDL2 fallback, etc.

Hooking OpenXR looks easy enough
https://docs.unity3d.com/Packages/com.unity.xr.openxr@1.4/manual/features.html

## Godot
As the most popular FOSS game engine Godot is high priority

The existing Godot input action system seems very limited (no gyro etc) so SuInput should have little competition.

The Godot OpenXR plugin is still under heavy development so it should be possible to request some hooks are added to it.

## Unreal
I haven't looked that much into Unreal yet but from what I've seen it should be fairly easy to get Desktop working thanks to hooking. However OpenXR may require forking the engine and modifying the OpenXR plugin, hopefully we will be allowed to merge some features upstream.

I have no idea what the Console + Mobile ecosystem looks like.

## OpenXR Layer
While technically not a plugin I think it makes sense to track its progress here

The OpenXR Layer shouldn't use the loader and just run from the embedded runtime since it's installed by the external runtime anyway. 

It should allow controller + desktop input support but it must be configurable and disabled by default because it may clash with the game's existing input solution.

It should expose an extension that would allow SuInput installed in the app to communicate with the layer. It may need to go against the spec and be enabled by default because some game engines may make it impossible to request custom extensions. 

Is it possible to add it to mobile / quest games by injecting into the apk?
Create a fake loader that calls the real loader and inject it into the apk. I doubt this will work well for apps installed of the Oculus Store because 'copyright' or whatever but it could work for Sidequest.

## Bevy
Since Bevy is pure rust and extremely modular it should be super easy to develop an SuInput plugin for it
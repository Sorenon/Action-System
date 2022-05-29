# Platforms

## Summary
| Name          | Specialized Driver | External Runtime                                                                                                                    |
| ------------- | ------------------ | ----------------------------------------------------------------------------------------------------------------------------------- |
| Win32         | Hooking 🚧         | DLL Loading ❌                                                                                                                      |
| Linux         | Hooking ❌         | SO Loading ❌                                                                                                                       |
| MacOS         | Hooking ❌         | Dylib Loading? ❌                                                                                                                   |
| UWP           | Hooking? ❌        | WASM / IPC? ❌                                                                                                                      |
| Android       | Hooking? ❌          | External Service? ❌                                                                                                                | 
| IOS           | Unknown ❌         | Against ToS ([for now?](https://www.theverge.com/2022/3/25/22996248/apple-sideloading-apps-store-third-party-eu-dma-requirement))❌ |
| Web           | Hooking ❌         | WASM? ❌                                                                                                                            |
| PlayStation 4 | Unknown ❌         | Unknown ❌                                                                                                                          |
| PlayStation 5 | Unknown ❌         | Unknown ❌                                                                                                                          |
| Switch        | Unknown ❌         | Unknown ❌                                                                                                                          |
| Xbox GDK      | Unknown ❌         | Unknown ❌                                                                                                                          |

Hooking drivers don't require any extra work by the developer and just work (unless they conflict with the game engine).

Manual drivers require developers to pass certain events to the platform driver, because of this it is unlikely they can be used with closed-source engines such as Unity.

In the case that a hooking driver is not available and the developer cannot access low level OS events, the developer can create a custom driver that takes events from the game engine and feeds them to the runtime. This is the approach that will be used for the Unity, Unreal and Godot plugins on platforms with missing drivers.

## Win32
Keyboard and mouse: [Raw Input](https://docs.microsoft.com/en-us/windows/win32/inputdev/about-raw-input) (Per process singleton leading to conflicts in some engines)
Cursor and Text: [Hooks](https://docs.microsoft.com/en-gb/windows/win32/winmsg/about-hooks)
Controllers: SDL2 (Xbox controllers require process being in focus)
Touch: TODO

## Win32 / UWP
The [GameInput API](https://docs.microsoft.com/en-us/gaming/gdk/_content/gc/reference/input/gameinput/gameinput_members) is coming to Win32 and UWP soon and is supposed to deprecate Raw Input and the APIs SDL2 uses, however it requires process focus? and is a per process singleton making injection into engines annoying.
https://docs.microsoft.com/en-us/gaming/gdk/_content/gc/reference/input/gameinput/enums/gameinputfocuspolicy????
https://docs.microsoft.com/en-us/gaming/gdk/_content/gc/input/overviews/input-fundamentals#application-focus????
https://github.com/microsoft/GDK/issues/11

## Linux
Keyboard and mouse: [XInput2](https://docs.rs/x11/2.19.1/x11/xinput2/index.html)
Cursor and Text: TODO
Controllers: SDL2
Touch: TODO

## MacOS
Keyboard and mouse: [Event Taps](https://developer.apple.com/documentation/coregraphics/quartz_event_services)
Cursor and Text: TODO
Controllers: SDL2
Touch: TODO

## Web
Keyboard and mouse: UI Events
Cursor and Text: UI Events
Controllers: [Gamepad API](https://developer.mozilla.org/en-US/docs/Web/API/Gamepad_API) (suffers from weak API and implementations)
Touch: [Touch Events](https://developer.mozilla.org/en-US/docs/Web/API/Touch_events)


## Android
Oh boy

Android development is split into two favours: java + jni and pure native
Thankfully most existing game engines use the more hackable java + jni approach.

From what testing I've done it seems possible to add an empty ViewGroup to the front of the Activity's main window and by returning false on all the event callbacks the events should get passed down to whatever the game engine uses to read input (e.g. Activity events or Surface listeners)

If this doesn't work for whatever reason we can do something similar to Monado and place a transparent window over all the Activities other windows. Then we can manually trigger the Activities events from our event callbacks. I think this only works for Java + JNI Activities though so something different will be needed for pure native ones. 

Many of these game engines also expose a method for the game developers to add code the the Main Activity so in a worst case scenario we could just tell the devs which functions to override.

It should be trivial to inject a text input widget to receive textbox input.

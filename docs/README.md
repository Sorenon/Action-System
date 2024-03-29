# SuInput
(Better name pending)

SuInput is an input system designed to give pancake and XR applications access to a huge range of input devices while minimizing the amount of complexity needed to support them. This is achieved by applications creating abstract 'actions' with explicit names and types, and relying on SuInput to map these actions to real devices.

This kind of system combined with other features that SuInput provides such as [[Input Glyphs]] and external configuration allows applications to have first class support for almost any human interface device, including those that didn't exist when it was written.

SuInput is heavily inspired by Steam Input & OpenXR and borrows many of their concepts and naming conventions. SuInput has substantial differences from each of these systems to increase accessibility, ease of use, flexibility and stability.

[Github Repo](https://github.com/Sorenon/suinput)
[Github Project](https://github.com/users/Sorenon/projects/1)
[[API Types Summary]]

#### SIAPI Issues
- Only supports modern console and generic controllers
- Confusing GUI
- Only offers primitive action types
- Undocumented edge cases
- Applications have to be published to Steam
- Closed source and inextensible
- Applications often botch their implementation of SIAPI / mixed input
- Applications cannot have their own rebinding menus

#### OpenXR Issues
- Limited non-XR device support
- Limited remapping tools
- Only offers primitive action types and bindings (without extensions)
- Entirely polling based
- Undefined behaviour between runtimes
- Input is a small part of a much larger specification
- Applications cannot have their own rebinding menus

#### Preventing these issues in SuInput
SuInput intends to circumvent these flaws with strict key design philosophies: 

1. Make SuInput flexible enough to be able to make full use of the capabilities of almost any human interface device. From (analogue) keyboards, to Wiimotes, to Oculus Touch Controllers.
2. Have a list of rules that applications must follow to make use of SuInput. These include not manually reading device input, treating action types in specific ways and using SuInput's input glyphs when told to.
3. Offer a simple external mapping GUI for users to customize bindings without having to read the manual first.
4. Offer a complex external mapping tool for power users so external re-mappers are not needed (such as Steam Input, ReWASD or JSM).
5. Keep SuInput open and extensible so users and developers can add support for custom devices, action types and binding types.

Currently there are no plans for SuInput to work as a desktop remapper, but there are plans for it to work as an OpenXR remapper since very few exist. There is no reason SuInput cannot be used as a desktop remapper and in future I may use it to make one with a pricing model similar to Aseprite and ReWASD to help fund development.

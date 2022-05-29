Every action can have zero or more bindings. If an action has multiple bindings they will be combined according to the action type. If action has zero bindings the action is marked as `inactive` letting the application know that it will not be used. The application can use the `inactive` value to enable / disable features such as aim assist (if a *Delta2D* `Turn` action is bound) or quick time events (if a quick time event key is unbound).

[[Input Component Types|Input Components]] are bound to [[Input Action Types|Input Actions]] using *bindings*.  Bindings can be very simple, such as directly binding a [[Input Component Types#Button Boolean|Button]] component to a [[Input Action Types#Boolean|Boolean]] action. But they can also be complex, like binding a [[Input Component Types#Move2D Delta2D|Scroll Wheel]] to that same Boolean action or binding [[Input Component Types#Motion Combined Gyro Accel|Gyro Motion]] to [[Input Action Types|Delta2D]].


## Binding types (WIP)
Instead of creating 'one binding abstraction to rule them all' SuInput uses a system that allows multiple 'binding engines' to work together. As the binding system is the most complex part of SuInput it is almost impossible to cover every scenario with one monolithic system. For example it would be challenging to bend the default engine to allow input from MIDI devices.

### Default Engine
The default engine covers all the conversions listed in [[Input Component Types]] and should be enough for most use cases. While I believe it offers a better alternative to many other binding engines, it still has a few major flaws.

#### Strong Points
Provides a Input Component based bindings and a simplistic structure
Supports most use cases through its 6 step system:
1. Input Component Config
2. Chords
3. Input Component Conversion
4. Activators (if applicable)
5. Action Conversion
6. Action Config

#### Flaws
6 step system can be limiting for some conversions
e.g.
Touchpad -> Joystick -> Spin -> Bool (Debounced) -> Value (Static)
is this
ICC (Touchpad -> Joystick -> Spin) -> AC (Bool (Debounced) -> Value (Static))
or
ICC (Touchpad -> Joystick -> Spin -> Bool (Debounced)) -> AC (-> Value (Static))
or
ICC (Touchpad -> Joystick -> Spin) -> ?(Bool (Debounced)) -> AC (-> Value (Static))

#### Possible Fixes
We could ditch the 6 step system for a simpler one:
1. Input Component Config
2. Chords
3. Magic!
6. Action Config
All the binding UI would need to do is find some permutation that can convert from Component to Action. The foreseeable downsides of this are: performance overhead, API complexity and configuration complexity.


1. Input Component Config (Sharable)
2. Chords <- needs to exist for all bindings for mode shifting 
3. Magic! <- this is where the binding engine lives
6. Action Config


2 passes
1. Priority check pass
2. Actual pass

#### API
OnInteractionProfileConnected(interaction_profile: &InteractionProfile, id: u64)
OnInteractionProfileDisconnected(interaction_profile: &InteractionProfile, id: u64)

OnComponentUpated(interaction_profile_state: &InteractionProfileState, component: (SuPath, SuPath), new_state: ComponentEvent)

## Binding to Actions
Allow binding to actions for ease of use
e.g.
In Minecraft bind sprint to `"move"."forward" with double tap activator`
In Generic FPS bind zoom turn to `"turn" with 0.x sensitivity`
This means that if the user changes the binding to `"move.forward"` or the binding / sensitivity of `"turn"` they don't need to also change the sprint binding / zoom turn binding / sensitivity

Priority still matters here so if an active action is bound to a lower priority action it blocks it from receiving any input. 

TODO Figure out why this is allowed to break the 6/4 step rule
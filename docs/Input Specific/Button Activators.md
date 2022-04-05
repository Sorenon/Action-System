Button activators are a method of binding multiple actions to one button. 

Some types of activator can block and interrupt each other.

#### Button Activator Types
- **Hold:** Default functionality
- **Press[^1]:** Activated for an instant on press
- **Release[^1]:** Activated for an instant on release
- **Quick Tap:** Activated for an instant after quick press and release
- **Double Tap:** Activated by two taps or tap then hold
- **Triple Tap:** Activated by three taps or two taps then hold
- **Long hold:** Activates after being held for a short duration

[^1]: Press / Release activators are equivalent to `Hold` activators with the matching `Impulse` setting

#### Button Activator Settings
##### Hold
~~~
#Is this activator blockable by other activators
Override behaviour: Block, Interrupt, None (default)

#Should we fire as an impulse
Impulse: On Press, On Release, False (default)
~~~
##### Quick Tap
```
#Is this activator blockable by double tap / tripple tap activators
Override behaviour: Block (default), None

#Can this activator override hold activators
Blocking: True, False (default)

#How quickly must the button be released
Max Hold Duration: 150 ms (default)
```
##### Double Tap
```
#Is this activator blockable by tripple tap activators
Override behaviour: Block, Interrupt, None (default)

#Can this activator override hold activators
Blocking: True (default), False

#How quickly must the button be double pressed
Double Tap Duration: 300 ms (default)

#Should we fire as an impulse
Impulse: On Press, On Release, False (default)
```
##### Triple Tap
```
#Can this activator override hold activators
Blocking: True (default), False

#How quickly must the button be tripple pressed
Tripple Tap Duration: 450 ms (default)

#Should we fire as an impulse
Impulse: On Press, On Release, False (default)
```
##### Long Hold
```
#How long must the button be held
Min Hold Duration: 150 ms (default)

#Should we fire as an impulse
Impulse: On Press, On Release, False (default)
```

TODO Activators for other types?
TODO Are Combos boolean activators?
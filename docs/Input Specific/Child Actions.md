Actions created with certain [[Input Action Types]] will spawn several *Child Actions*. Child Action bindings are combined with their sibling's and the parent Action's in various ways to create the final action state the application sees.

For example, an *Axis2D* action called `Move` would have 6 child actions and could be bound to `Left Stick` on controller. It's child *Value* actions *North, East, South, and West* could be renamed to `Forward, Right, Back, Left` and bound to `W, D, S, A`  accordingly. 

In future users may be able to add custom Child Action types to an action to combine bindings in a unique way.

## Sticky Boolean
- Boolean, Sticky Press
- Boolean, Sticky Release
- Boolean, Sticky Toggle

## Axis1D
- Value, Positive (Application renamable)
- Value, Negative (Application renamable)

## Axis2D
- Value, North (Application renamable)
- Value, East (Application renamable)
- Value, South (Application renamable)
- Value, West (Application renamable)
- Axis1D, Vertical (Application renamable)
- Axis1D, Horizontal (Application renamable)

## Delta2D
- Delta1D, Vertical (Application renamable)
- Delta1D, Horizontal (Application renamable)

## Cursor
- Delta2D, Move
- Delta1D, Vertical Move
- Delta1D, Horizontal Move
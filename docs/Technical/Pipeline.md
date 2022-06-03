The more I document and explore how the backend should work the more it mimics a basic rendering pipeline.

When an input event enters the pipeline it can cause zero or more events at every stage. These events need to be cleaned up / processed by their creators once they have been used and can sometimes be fed back into the same system.

As the input backend increases in complexity we could end up adding more systems and connections between systems.

Since we will be dealing with relatively few events I don't think there is any need for multithreading though the kind of pipeline I want to design should be fairly easy to parallelize.


## Input Component Event
```
Boolean: IsPressed bool
Delta2D: Delta (f64, f64)
Cursor: Position (f64, f64), Window: Option<WND>

## Action Event
Boolean= IsPressed: bool, Changed: bool
Delta2D= Delta: (f64, f64)
Cursor= Position: (f64, f64), Window: Option<WND>

## Action State
Boolean= IsPressed: bool, Changed: bool
Delta2D= Delta(f64, f64)
Cursor= Position: (f64, f64), Window: Option<WND>
```

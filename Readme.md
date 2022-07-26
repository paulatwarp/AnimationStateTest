# Animation State Example

The scene `AnimationTest` contains a simple two state animation with a bounce animation and an idle animation. If you run, you can see that it will bounce forever.

The transition to idle happens when the stop trigger is set. However, this will only happen if the trigger is set before the exit time of 3 has been reached. If you wait longer than the exit time, you can see that the transition never happens - which is probably not what you want.

This situation happens when:
- you have a looping animation state with a transition
- the transition has the `Has Exit Time` flag checked
- the `Exit Time` is greater than 1
- there is a condition on the transition

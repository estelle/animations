When an animation is applied, if there is no delay, or a negative delay, the animation 


The start and end of an animation, and the end of each iteration of an animation, all generate DOM events. An element can have multiple properties being animated simultaneously. This can occur either with a single `animation-name` value with keyframes containing multiple properties, or with multiple `animation-name` values. For the purposes of events, each `animation-name` specifies a single animation. Therefore an event will be generated for each `animation-name` value and not necessarily for each property being animated.

Any animation for which a valid keyframe rule is defined will run and generate events; this includes animations with empty keyframe rules.

The time the animation has been running is sent with each event generated. This allows the event handler to determine the current iteration of a looping animation or the current position of an alternating animation. This time does not include any time the animation was in the `paused` play state.

### The `AnimationEvent` Interface

The `AnimationEvent` interface provides specific contextual information associated with Animation events.


### Types of AnimationEvent

The different types of animation events that can occur are:
# nao-gesturesync

This is a simple animation engine for the NAO robot which enables the robot to perform gestures while playing given audio.

This is especially useful if you want animated speech but your language is not supported by the NAO's built-in animated speech component.
For example, the robot can play your professionally recorded speech audio file and perform appropriate gestures while playing.

All you need to do is to create a text file which will tell when to perform which gesture.
An example of such file:
```
1.0 animations/Stand/Gestures/Explain_7
3.0 animations/Stand/Gestures/Me_4
5.0 animations/Stand/Gestures/Yes_1
```
This means that at time `1.0` of the audio file gesture `Explain_7` will be performed, at time `3.0` gesture `Me_4` will be performed, etc.
There is also an option (enabled by default) to forcibly stop the current gesture (if it is still running) and start the next one.

You can use gestures which are provided by Aldebaran or you can record your own. Just make sure that they are available as behaviours on the robot.

The workflow will also run on the virtual robot if all gestures (behaviours) are present.

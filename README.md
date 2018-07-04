# Unity-RTS-Camera

## Description ##

A c# script to use as a component in your main camera to implement a _RTS_ style or a _fly through the world_ style camera. You can pan the camera either by keyboard or mouse both horizontally and vertically, as well as zoom in/out.

## Usage information ##

You can either use the prefab that contains a camera with the script or attach the script to your main camera (_add tag "main camera"_).
Once you have the script on your game object some options will be visible in the inspector.

The options in the script component are :

1. **Screen border edge thickness** : It describes how far from the edge of the screen the camera movement will be triggered. This field is only for the mouse movement option and can be easily changed by modifying the value.

2. **Camera Mode** : It defines the camera mode. The default is _RTS Mode_ which sets camera to move based on the global coordinates. Other option is _fly mode_ which sets camera to move based on the local coordinates of the camera game object.

3. **Movement speeds** : It defines the speed of the camera in the game. The speed starts from a minimum value and based on the _secToMaxSpeed_ value it reaches to a maximum speed value.

4. **Movement limits** : It limits the camera's movement on the 3D axes. You can define how far the camera can reach on each of z (length), x (width), y (height). Remember this tool works only if the boolean _enableLimits_ is set to true. However, in case this option does not satisfy you, you can set it to false and add a rigid body as well as a collider to the camera and set gravity to false. Then insert empty colliders around your 3d world and the camera will collide with them, giving a movement limitation.

5. **Rotation** : Here you define if you want your camera to rotate and set the rotation speed. In _RTS mode_ you can rotate the camera but when the mouse button is released the rotation returns to its default value. You can use the right mouse click to rotate the camera (click and hold).

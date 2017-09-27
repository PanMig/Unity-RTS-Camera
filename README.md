# Unity-RTS-Camera

## Description ##

A c# script to use as a component in your main camera to implement a _RTS_ style camera or a _fly throught the world_ style. You can pan the camera either by keyboard or mouse both horizontally and vertically, as well as zoom in/out.

## How to use ##

You can either use the prefab that contains a camera with the script or attach the script to your main camera(add tag main camera).
Once you have the script on your game object some options will be visible on the inspector, let's get a quick view of them.

The important domains on the ispector are :

1. **Screen border edge thickness** : Describes how far from the edge of the screen the movement of the cammera will be triggered. This field is only for the mouse movement option and can be easily changed by modifying the value.

2. **Camera Mode** : Here you can use the default _RTS Mode_ to move based on the global cordinates or _fly mode_ to move based on the local cordinates of the camera game object.

3. **Movement speeds** : Here you define the speed that the camera will have in the game. The speed starts from a minimum value and based on the _secToMaxSpeed_ value it reaches to a maximum speed value.

4. **Movement limits** : Here you limit the camera's movement on the 3d axes respectively. You can define how far the camera can reach on the z (lenght), x (width), y (height). Remember this tool works only if the boolean _enableLimits_ is set to true. However if this future does not cover you needs you can set it to false and add a rigidbody as well as a collider to the camera and set gravity to false. Then insert empty colliders around your 3d world and the camera woould collide with them, giving a movement limitation.

5.**Rotation** : You can set if you want your camera to rotate and also apply a speed to the rotation. In _RTS mode_ you can rotate the camera but when mouse button is released the rotation return to it's default value. You can use the right mouse click to rotate the camera (click and hold).



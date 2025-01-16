# 2D Smooth Camera Follow 
## This tutorial will show you how to make the camera follow your player smoothly for a 2D game: both a platformer and a top down 2D . To be ready for this tutorial, please download and import a unity package with character movement in a 2D space.
## Coding the Script
1. Create a new folder and name it ``Scripts``
2. Create a script in the ``Scripts`` folder by right-clicking in the ``Project`` tab and call it ``CameraFollow``
3. Make this a component of the Main Camera by dragging the script into it's ``Inspector`` tab

```c#
public class CameraFollow : MonoBehaviour
{
    public Transform target;
    public Vector3 offset;

    private void FixedUpdate()
    {
        transform.position = target.position + offset;
    }
}
```
When you copy this exact script, it actually may not work at first but it's because there are other steps that need to be done in the scene outside of the script.

Theres the ``public Transform target;`` variable which gets the reference of the player but in the ``Inspector`` tab of the Main Camera, there should be a box where you'll have to drag the Player from the hierarchy into the box where it says target, since there was nothing for the code to reference.


 

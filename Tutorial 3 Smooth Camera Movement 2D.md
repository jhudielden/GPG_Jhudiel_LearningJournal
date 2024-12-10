# 2D Smooth Camera Follow 
## This tutorial will show you how to make the camera follow your player smoothly for a 2D game: both a platformer and a top down 2D . To be ready for this tutorial, please download and import a unity package with character movement in a 2D space.
## Coding the Script
1. Create a new folder and name it ``Scripts``
2. Create a script in the ``Scripts`` folder by right-clicking in the ``Project`` tab and call it ``CameraFollow``

```c#
public class CameraFollow : MonoBehaviour
{
    public float FollowSpeed = 2f;
    public Transform target;
    public Vector3 offset;
}
```
 

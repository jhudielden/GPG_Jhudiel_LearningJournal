# Moving Platforms in 2D Platformer
## This tutorial will show you how to code and add in moving platforms that can go in a straight line; upright or diagonally from using two set points. 
## Coding the Script
1. Go to the `Assets` folder in the `Project` tab to make a new folder to keep things organised and right-click `Create -> Folder` and name it `Scripts`
2. Open the folder and go right-click `Create -> C# Script` to open a fresh script and name it `MovingPlatform` with no spaces.
3. Here is the example script, copy and paste the lines in the space
   
```c#
public class MovingPlatform : MonoBehaviour
{
  public Transform pointA;
  public Transform pointB;
  public float moveSpeed = 2f;
  private Vector3 nextPosition; 

void Start()
{
  nextPosition = pointB.position;
}

void Update()
{
  transform.position = Vector3.MoveTowards(transform.position, nextPosition, moveSpeed * Time.deltaTime);
  if(transform.position == nextPosition)
  {
    nextPosition = (nextPosition == pointA.position) ? pointB.position : pointA.position;
  }
}

}
```
Here is the script but there are steps that are needed to be followed in the Unity scene for it to work as well
## Let's add the platform into the Unity scene
1. In the ``Hierarchy`` tab, right click and navigate in the drop down `Create Empty`
2. Name it ``Moving Platform``
3. Right-click on the empty ``2D Object -> Sprites -> Square`` and name it ``Platform``
4. In the ``Platform`` Inspector add the ``Box Collider 2D`` component and ``Platform Effector 2D`` component on it
5. Change the scale of the square to the shape of the platform you want it to be
6. Right-click on ``Moving Platform`` and create an empty and name it ``Point A`` and make another the same way and call it ``Point B``.
7. To make it easier to see click in the ``Inspector`` tab of each points on the cube dropdown button to give the empty an icon and give the two points two different colours
![image](https://github.com/user-attachments/assets/045a9141-d1f7-4817-822e-6c6ec6238125)
8. Move the points to where you want the platform to move between
9. Link the the ``MovingPlatform`` script to the ``Platform`` sprite
10. Once you do, make sure to link the `` public Tranform pointA`` and ``public Transform pointB`` to the empty game objects in the ``Inspector`` tab of the ``Platform``
![image](https://github.com/user-attachments/assets/2fd40303-766b-4739-8f67-55cf06506f9e)

 


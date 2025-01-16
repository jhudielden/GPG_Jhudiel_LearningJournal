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
1. In the `Hieracrhy` tab, right click and navigate in the drop down `2D Object -> Sprites -> Square`
2. Name it `Moving Platform`


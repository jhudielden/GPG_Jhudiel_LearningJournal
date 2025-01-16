# Moving Platforms in 2D Platformer
## This tutorial will show you how to code and add in moving platforms that can go in a straight line; upright or diagonally from using two set points. To be ready for this tutorial

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

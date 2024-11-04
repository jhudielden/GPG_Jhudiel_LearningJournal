# 2D Player Movement Top Down
## This tutorial will show you how to make player movement for a top down 2D view
1. Opening a fresh 2D Unity project, your `Assets` folder in the `Project` tab should already have a `Scenes` folder within it.
2. In the `Scenes` folder, create a new scene  by right-clicking in it `Create -> Scene`. Then name it `GameScene` 
3. Click it to open the scene you've just made
### Let's add in a player into the GameScene
1. In the `Hieracrhy` tab, right click and navigate in the drop down `2D Object -> Sprites -> Square`
2. Name it `Player`

    - Optionally, you can change the colour of the player by clicking on Player and in the `Inspector` tab, under `Sprite Renderer` find `Color` field and click on the white box to open the colour wheel
     
        ![alt text](<Player Inspector.PNG>)
### Let's make the script to make it move
1. Go to the `Assets` folder in the `Project` tab to make a new folder to keep things organised and right-click `Create -> Folder` and name it `Scripts`
2. Open the folder and go right-click `Create -> C# Script` to open a fresh script and name it `PlayerMovement` with no spaces.
3. Here is the example script, copy and paste the lines in the spaces which the script loads in

```c#
public class PlayerMovement : MonoBehaviour
{
    public float speed = 4f; 
    void Start()
    {
        
    }

    
    void Update()
    {
        float Hinput = Input.GetAxis("Horizontal");
        float Vinput = Input.GetAxis("Vertical");
        transform.Translate(Vector3.right * speed * Hinput * Time.deltaTime);
        transform.Translate(Vector3.up * speed * Vinput * Time.deltaTime);
    }
}
```
What's happening here is the use of `Input.GetAxis` to declare and use the input movements of the `Horizontal` and `Vertical` plane and making it a variable so it can be used in the following statements.

The statements use of `transform.Translate` is to move the transform or `Player` in this case but also states the distance and how it moves.

At the top of the script variable for `speed` had to be made, without it the `Player` will move but it moves in relation to the frame speed which can be slow but also differs on every machine so to set it a fixed `float` makes it consistent.

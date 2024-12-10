# GPG_Jhudiel_LearningJournal
This is my learning journal for Game Programming 2024/25 
## 000 Preliminary Journal-Log 15/10/2024
Despite having an old repository for an old summer project and had no idea what I was using, I'm starting to understand what I'm looking actually at now. Going to have to learn the other MarkDowns to further optimise my use of GitHub. If I'm confused by it, I'll dread using it and not use it as efficient as possible. Also being a slight perfectionist, I do want the history and the layout to be consistent as much as possible. 
Interestingly enough, I have gotten used to documenting creative processes in multiple different programs, but the fact that I did it in different programs, I have gotten into different habits. 
## 001 Journal-Log 29/10/2024
Today all I was able to complete was the start of the 1st tutorial, a 2D player movement for a top down view. I had no setbacks or problems with the code necessarilly just having to check how the `Input.GetAxis` works in Unity as I've only used it in a 3D tutorial not in the 2D space. I had to check if changing the code from `Vector3` to a `Vector2` still worked, though I think it doesn't matter since the project is stuck in the 2D space. 

The only setback I can see is not with code specifically but with the scope of what I want to code and make, I initially made a huge list of potential things I want to learn to code to then make it into a tutorial, and set myself up for Decision fatigue I'm assuming.
## 002 Journal-Log 04/10/2024
Today I've almost finished like 95% almost finished the first tutorial, with no problems with code thankfully, just writing it out and explaining is what's slowing me down. I know the code works but it's just how it works that I explained, though I don't think is necessary but I do now understand some declarations and their descriptions to know how some things are done.
## 003 Journal-Log 05/10/2024
I started on some new code, I wanted to make a sliding tile puzzle. Though a game with a very simple functionality, coding it is still complex. I found a tutorial and watched 3 episodes out of 5 before first before following along with it. The first thing was that the tutorial used imported sprites of tiles and numbers. Tiles I can just use the the 2D Sprites but the numbers seemed to complicated use `TextMeshPro` text, so I ended up importing some number png from Google Images. So the first problem I faced wasn't code itself but using Unity.

Following along with the tutorial videos I found were fine. The only small problem I faced was fixing the swap of a tile and the empty space. In a regular sliding puzzle the only tiles that move are the tiles that are touching the empty space. But with mine, if I pressed on any tile not touching the empty space it would teleport and swap. I've never used Raycast before, that's what's tracking when you press the tile. The distance condition to track the raycast of the empty space and the tile was a value of `2` in the tutorial, `1` wouldn't work so I had to make it an interger of `1.4f` to make the condition work.
## 004 Journal-Log 12/11/2024
I finished making the sliding puzzle! I was working on randomising the tiles but in doing so can make it unsolvable. But following a tutorial, it went through a bit of a process wo make sure that it was solvable. Writing it up will be a bit of a challenge since I was technically just following step by step a tutorial. Now it's done I have to write up how to make it myself. The beginning parts isn't that hard to explain like the box colliders on each tile, when it's in the right position it changes colour. It's slight animation making the tile move into position, shuffling and randomising.
### 005 Journal-Log 03/12/2024
I started my prototype after a bit of a slump period. I already had a movement script I wanted to re-use. The function is a nice sling shot and I've made a basic scene of a boxed room the problem I'm facing is in relation to the camera follow. I've only used cinemachine to track a player's movement but for this prototype I wanted to code the camera myself to atleast try it once.
### 006 Journal-Log 10/12/2024
I got the smooth camera follow and the proper claming to work! Last week I didn't mention that the camera movement was fine but it's the camera bounds that I had to implement and what I needed to understand. Turns out I needed to clamp the camera's transform as it follows the target/player. I didn't know how to use the ``Mathf.Clamp`` function and I initially didn't know what was wrong with it since I followed a tutorial yet again for the clamping and a different one for the camera movement itself. Since they weren't the same exact code but still did the same thing I thought I could just use both and it'll work but it didn't initially. So I thought the problem lied upon having all the necessary functions but not calling them properlly into a statement for it to work, but it actually was the problem of inputing the minimum and maximum values of the camera bounds. Not realising despite being a 2D Game the Z value is still important and needs to properlly valued. 

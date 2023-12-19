# Entry 2
##### 12/18/2023

After finish following the first tutorial, I went to search for a new one to follow. The second tutorial I found was [The Unity Tutorial For Complete Beginners](https://www.youtube.com/watch?v=XtQMytORBmM). This tutorial teaches the basic of 2D in unity through a simple flappy bird game. The tutorial was broken down into 5 parts. In part I and part II of the tutorial, I learned about the unity UI and physic + programming in unity. There are four panels that made up the default UI layout: project, hierarchy, inspector, and scene panel. Each panel contains differrent things in it.
* Project panel - contains sprites, sound effect, scripts, etc.
* Hierarchy panel - contains all the stuffs in the current scene.
* Inspector panel - changing properties of gameobjects.
* Scene panel - shows what is in the current scene.
  
For part II, I begin to write in C# for the first time. In the unity script, there are two main functions: `void start()` and `void update()`. 
* `Void Start ()` - runs the code inside once soon as the script is enabled.
* `Void Update ()` - runs constantly and will run every line of code inside it, every single frame.
The goal in part II was to make the gameobject "bird" fly when certain key is pressed. To do this, I have to use `if-statement` inside the `void update()` function. For the boolean inside the if statement, I have to use `Input.` because the if-statement is talking to the unity input system and not the game component. To make the gameobject `bird` fly, I have to use this property called `velocity` and give it a direction using `vector2.up`.
```
void update()
{
    if(Input.GetKeyDown(KeyCode.Space) == true)
    {
      myRigidbody.velocity = Vector2.up * flapStrength;
    }
}
```
After finishing part I and II, I spent the next few weeks on finishing part III to part V. I eventually finished the tutorial. From this tutorial, I learned that learning to write in C# is a very important part of making a game to function in unity. My Freedom Project goal for winter break is to search a tutorial that teaches C# in unity. 

For enginnering design process, I'm still in step **2 research the problem** because I'm still researching for more tutorials to follow to learn more about my tool. In addition, one new skill I learned was **Time management**. This is the new skill I learned because I planned out what parts of the tutorial I should follow each week.

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)

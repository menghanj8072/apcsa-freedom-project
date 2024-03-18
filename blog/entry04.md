# Entry 4
##### 3/18/2024

In the past few weeks, I have been spending my time working on my MVP and learning about my tool at the same time. I found this new tutorial that teaches C# in unity https://www.youtube.com/watch?v=9tMvzrqBUP8. This tutorial teaches basic C# codes that are used in unity. I learned about how to destroy gameobjects, detecting keyboard inputs & mouse click, adding forces & velocity, how to load new scenes, and how to get values from axis. 
At first when I finished the tutorial, I didn’t really create something on my own with the code I learned. But a few days later, I spent some time using what I learned from this tutorial and the tutorial about [2D movement](https://www.youtube.com/watch?v=dwcT-Dch0bA) to create something. 

```C#
public float speed = 30f;

float move = 0f;

Void Update(){
	move = Input.GetAxisRaw(“Horizontal”) * speed;
}
Void FixedUpdate(){
	controller.Move(move * Time.fixedDeltaTime, false, false);
}


Void onCollisionEnter2D(Collision2D collision){
if(collision.gameObject.tag == “enemy”){
Destroy(collision.gameObject);
	}
}
```
What this code does, is the gameObject is able to move on the horizontal axis. If the gameobject collides with another gameobject with the enemy tag, the gameobject will get destroyed.

### MVP
I have designed my own character and environment sprites. I still need to create more sprites, but here is what I have so far. I didn’t make much progress on my mvp. What I have done so far was adding the sprites into unity and designing the first level of the game. I haven’t really spent much time working on the actual code that will run the game.

For the engineering design process, I'm in step 5 create a prototype because I’m starting to work towards my mvp. As I’m designing sprites and working towards my MVP, one new skill I have developed through this process is creativity.


[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)

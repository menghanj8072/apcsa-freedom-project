# Entry 5
##### 5/6/2024

After the last blog, I have been spending time following tutorials on how to create animation and how to switch levels in unity and also working on my MVP. In the tutorial about how to create animation, I learned that I need to create animated sprites first in order to turn them into animation in unity. So I spent some time drawing animated sprites and importing each frame into unity. I designed my sprites on https://www.piskelapp.com/p/create/sprite. After importing them, I first created an animation for the player sprite. I drag the sprites onto the animation panel and adjust the speed of animation by changing the frames per second. When I finished adding animation to the player sprite, I moved on and added animation for the enemy sprites. Once I finished with animations, I moved on adding components to my sprites and code.

### Player Sprite
I added 2 components to the player sprite: Rigidbody 2D and Box Collider 2D. What rigidbody2D does is it allows the gameobject to act under the control of physics and for box collider 2D is used for collision physics. After doing that I created a script for the player sprite and started adding code. My goal for the player is to make it move and jump. 
```C#
 void Update()
 {

     body.velocity = new Vector2(Input.GetAxis("Horizontal") * speed, body.velocity.y);

     if (Input.GetKey(KeyCode.Space))
     {
         Jump();
     }
}

   private void Jump()
 {
     body.velocity = new Vector2(body.velocity.x, speed);
 }

```

The `Update()` method runs constantly and will run every line of code inside it, every single frame. The `body` is a variable that I made to store the velocity values. To make the player move, I have to use a vector. Since the game is a 2D game, I will have to use vector2. Vector2 has 2 properties: X-axis and Y-axis. I used `Input.GetAxis("Horizontal")` for the x value because this is a value defined by unity. When the player presses the left key, `Input.GetAxis("Horizontal")` will return a negative x value (move left) and the player presses right key, it will return a positive x value (move right). I multiplied it by `speed` which is a float variable I made and the default value for it is 10. For the y-axis, I didn't want to change the velocity of it, so I just wrote `body.velocity.y`. Next to make the player jump, I created a 
private void method named `Jump`. Inside this method, I also used vector2 and this time I didn't change the x value, instead I changed the y value. I wanted the jump value to be same as speed, so I just set the y value to speed. I went back to the `update` method and added a if statement. The if statement will check if the player pressed "space" key, and will run he jump method if the conditional is true.

### Slime Sprite (Enemy)


### Coin

### Player Health



I’m now in step **5 creating a prototype** and step **6 tests and evaluating the prototype** in the **engineering design process.** One new skill I learned is debugging because when I finished my mvp, I noticed there were many bugs in my game. I have debugged some bugs, but I still need to fix more when I’m working on beyond MVP. Fixing those bugs will give the player a good experience when playing the game.

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)

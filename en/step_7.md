

## Detect collision with the pipes

To make the game a challenge, the player needs to guide Flappy through the gaps without touching the pipes or the edges of the screen. Now we'll add some blocks to detect if Flappy hits something. This is called __collision detection__. 

+ Let's add a sound to play when Flappy collides. Click on the **Flappy** sprite then on the `Sounds` {.blockgrey} tab.

+ Click the `Choose sound from library` {.blockgrey} button and add a collision sound for **Flappy**. The **screech** sound is good.

+ You're going to use a `wait until` {.blockcontrol} block to check for Flappy touching the pipes. 

    Use a new `on green flag clicked` {.blockcontrol} block:
    
    ![screenshot](images/flappy-wait.png)
    
    Any code you place after a `wait until` {.blockcontrol} block will only run after the condition is detected. 
    
+ Can you add to the code so Flappy screeches if she touches a pipe **or** touches the edge of the stage.  

--- hints ---
--- hint ---
You need to fill in the condition in the wait until` {.blockcontrol} block to check for Flappy __touching__ the __edge__ of the screen __or__ __touching__ the __Pipes__ sprite.  

![screenshot](images/flappy-wait.png)

And you'll need to add code to __play__ the screech sound after the `wait until` {.blockcontrol} block. 
--- /hint ---
--- hint ---
Try using these blocks:

![screenshot](images/flappy-collision-blocks.png)

--- /hint ---
--- hint ---
Your code should look like this:

![screenshot](images/flappy-collision-code.png)

--- /hint ---
--- /hints ---

+ Test your code. Notice that you only hear the screech the first time you have a collision. That's okay, because the game ends if you have a collision. 

+ Add the highlighted code to stop the game after a collision is detected:

    ![screenshot](images/flappy-game-over.png)
    
    The `stop` {.blockcontrol} block stops other Flappy scripts that are running. Flappy won't fall after a collision. 
    
    The `broadcast` {.blockevents} block tells other sprites that the game is over. 
    
+ Add the following code to the **Pipes** sprite so that the pipes stop when a `Game Over` message is received. 

    ![screenshot](images/flappy-stop-code.png)

+ Now test your game and see how long you can last!









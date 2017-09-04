

## Detect collision with the pipes

To make the game a challenge, the player needs to guide Flappy through the gaps without touching the pipes or the edges of the screen. To set this up, we'll add some blocks to detect when Flappy hits something. This is called __collision detection__.

+ Import a sound from the library that will play when Flappy collides with something. The 'screech' sound is a good choice.

[[[generic-scratch-sound-from-library]]]

+ You're going to use a `wait until` {.blockcontrol} block to check for whether Flappy is touching the pipes.

    Use a new `on green flag clicked` {.blockcontrol} block:

    ![screenshot](images/flappy-wait-until.png)

    Any code you place after a `wait until` {.blockcontrol} block will only run after the condition is met.

+ Can you add to the code so Flappy screeches if she touches a pipe **or** the edge of the stage.  

--- hints ---
--- hint ---
You need to fill in the condition in the `wait until` {.blockcontrol} block to check for Flappy `touching` the `edge` of the screen `or` `touching` the `Pipes` sprite.  

![screenshot](images/flappy-wait-until.png)

AYou'll need to add code to `play` the 'screech' sound after the `wait until` {.blockcontrol} block.
--- /hint ---
--- hint ---
Try using these blocks:

![screenshot](images/flappy-collision-blocks.png)

You might need to use one of these blocks more than once.
--- /hint ---
--- hint ---
Your code should look like this:

![screenshot](images/flappy-collision-code.png)

--- /hint ---
--- /hints ---

+ Test your code. You might notice that you only hear the screech the first time you have a collision. That's okay, because the game ends if you have a collision.

+ Add the highlighted code to stop the game after a collision is detected:

    ![screenshot](images/flappy-game-over.png)

    The `stop` {.blockcontrol} block stops other Flappy scripts that are running. Flappy won't fall after a collision.

    The `broadcast` {.blockevents} block tells other sprites that the game is over.

+ Add the following code to the `Pipes` sprite so that the pipes stop when a `Game over` message is received.

    ![screenshot](images/flappy-stop-code.png)

+ Now test your game and see how long you can last!

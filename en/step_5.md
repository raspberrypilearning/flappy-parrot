

## Make Flappy fall

Now you can add a sprite called Flappy. If you don't press any keys then Flappy should just fall down the screen.

+ Add a sprite with 2 costumes for wings up and wings down. **Parrot** is a good choice. Name your sprite __Flappy__.

    ![screenshot](images/flappy-parrot.png)

+ Flappy needs to be smaller, about 25% should do it. You can either use the shrink tool or a `set size to ( )` block.  

+ When the game starts Flappy should be just to the left of the centre of the screen. At coordinates (-50, 0). Code Flappy to go to the starting position at the start of the game.

[[[generic-scratch-set-coordinates]]]

+ Now you need to make Flappy keep falling down the stage.

--- hints ---
--- hint ---
__The code you have already__ should look like this:

![screenshot](images/flappy-setup-code.png)

You need to add code to the end of this script to make Flappy fall __forever__.

--- /hint ---
--- hint ---
Try using these blocks:

![screenshot](images/flappy-fall-blocks.png)

Changing Flappy's y position by -3 each time round a loop should be about right.
---/hint ---
--- hint ---
Your code should look like this:
![screenshot](images/flappy-fall-code.png)

---/hint ---
--- /hints ---

+ Test your code and make sure Flappy starts in the middle of the screen and falls to the bottom. Drag Flappy up to the top of the screen and it should fall again.

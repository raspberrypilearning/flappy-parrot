

## Make Flappy fall

Now you can add a sprite called Flappy. If you don't press any keys, then Flappy should just fall down the screen.

+ Add a sprite with two costumes, for 'wings up' and 'wings down'. The parrot sprite is a good choice. Name your sprite 'Flappy'.

    ![screenshot](images/flappy-parrot.png)

+ Flappy needs to be smaller — reducing the sprite's size to about 25% should do it. You can either use the **Shrink** tool or a `set size to ( )` block.  

+ When the game starts, Flappy should be just to the left of the centre of the screen, at coordinates `-50, 0`. Code Flappy to go to the starting position at the start of the game.

[[[generic-scratch-set-coordinates]]]

+ Now you need to make Flappy keep falling down the stage.

--- hints ---
--- hint ---
The code you have already should look like this:

![screenshot](images/flappy-setup-code.png)

You need to add code to the end of this script to make Flappy fall `forever`.

--- /hint ---
--- hint ---
Try using these blocks:

![screenshot](images/flappy-fall-blocks.png)

Set up a loop to change Flappy's `y` position by `-3` each round.
---/hint ---
--- hint ---
Your code should look like this:
![screenshot](images/flappy-fall-code.png)

---/hint ---
--- /hints ---

+ Test your code to make sure Flappy starts in the middle of the screen and falls to the bottom. When you drag Flappy to the top of the screen, the sprite should fall again.

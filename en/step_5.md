

## Make Flappy fall

Now you can add a sprite called Flappy. If you don't press any keys then Flappy should just fall down the screen. 

+ Add a sprite with costumes for wings up and wings down. **Parrot** is a good choice. Name your sprite __Flappy__.

    ![screenshot](images/flappy-parrot.png)

[[[generic-scratch-sprite-from-library]]]

[[[generic-scratch-rename-sprite]]]
	
+ Flappy needs to be smaller, about 25% should do it. You can either use the shrink tool or a `set size to ( )` block.  

	![screenshot](images/flappy-small.png)

+ When the game starts Flappy should be just to the left of the centre of the screen. At coordinates (-50, 0). Can you make Flappy go to the starting position at the start of the game. 

    ![screenshot](images/flappy-start.png)
    
[[[generic-scratch-set-coordinates]]]


+ Now you need to make Flappy keep falling down the stage.

--- hints ---
--- hint ---
Your code should look like this: 

![screenshot](images/flappy-setup-code.png)

You need to add code at the end to make Flappy fall forever. 

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

+ Test your code and make sure Flappy starts in the middle of the screen and falls to the bottom. Drag the Flappy won't go right off the stage. Drag Flappy up to the top of the screen and it should fall again. 







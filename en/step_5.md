## Make Flappy fall

You will now add a sprite called Flappy and code it so it falls down the screen. In the next step you will add the code to make Flappy fly when you press a key.

--- no-print ---

![flappy falling animation](images/flappy-falling.gif)

--- /no-print ---

--- task ---

Add a new sprite to your project which has two costumes, for 'wings up' and 'wings down', and name it `Flappy`.

The parrot sprite is a good choice.

![parrot sprite](images/flappy-sprite.png)

--- /task ---

--- task ---

Flappy needs to be smaller, lets add the code to `set its size to 25%`{:class="blocklooks"} `when the green flag is clicked`{:class="blockevents"} 

![parrot sprite](images/flappy-sprite.png)

```blocks
when green flag clicked
set size to (25) %
```

**Tip:** you could also use the **Shrink** tool to make your sprite smaller.

--- /task ---


When the game starts, Flappy should be just to the left of the centre of the screen, at coordinates `-50, 0`. 

![flappy shown at the start position](images/flappy-starting-position.png)

--- task ---

Add the code to make Flappy `goto the x and y`{:class="blockmotion"} starting position of `x: -50`{:class="blockmotion"} and `y: 0`{:class="blockmotion"}.

![parrot sprite](images/flappy-sprite.png)

```blocks
when green flag clicked
set size to (25) %
+ go to x: (-50) y: (0)
```

[[[generic-scratch-set-coordinates]]]

--- /task ---

--- task ---

Now you need to make Flappy keep falling down the stage by `forever`{:class="blockcontrol"} `changing the sprites y position by -3`{:class="blockmotion"}.

![parrot sprite](images/flappy-sprite.png)

```blocks
when green flag clicked
set size to (25) %
go to x: (-50) y: (0)
+ forever 
  + change y by (-3)
end
```

--- /task ---

--- task ---

Test your code to make sure Flappy starts in the middle of the screen and falls to the bottom. When you drag Flappy to the top of the screen, the sprite should fall again.

--- /task ---

## Detect collision with the pipes

To make the game a challenge, the player needs to guide Flappy through the gaps without touching the pipes or the edges of the screen. To set this up, we'll add some blocks to detect when Flappy hits something. 

This is called __collision detection__.

--- task ---

Import a sound from the library that will play when Flappy collides with something. The 'screech' sound is a good choice.

[[[generic-scratch-sound-from-library]]]

--- /task ---

You're going to use a `wait until`{:class="blockcontrol"} block to check for whether Flappy is `touching the pipes`{:class="blocksensing"} `or`{:class="blockoperators"} `touching the edge`{:class="blocksensing"}.

--- task ---

Add a new `when green flag clicked`{:class="blockcontrol"} block to the `Flappy` sprite and add the following code:

![parrot sprite](images/flappy-sprite.png)

```blocks
when green flag clicked
wait until <<touching [Pipes v] ?> or <touching [edge v] ?>>
play sound [screech v]
```

--- /task ---

--- task ---

Test your program, if Flappy touches a pipes, the 'screech' sound should play.

--- /task ---

Now lets update the code so that the game stops when Flappy hits a pipe.

--- task ---

Add the code to stop the game after a collision is detected:

![parrot sprite](images/flappy-sprite.png)

```blocks
when green flag clicked
wait until <<touching [Pipes v] ?> or <touching [edge v] ?>>
play sound [screech v]
+ say [Game Over!]
+ broadcast [Game Over v]
+ stop [other scripts in sprite v]
```

The `broadcast`{:class="blockevents"} block tells other sprites that the game is over.

The `stop`{:class="blockcontrol"} block stops other Flappy scripts that are running so that Flappy won't continue to fall after a collision.

--- /task ---

--- task ---

Finally you need to add the following code to the `Pipes` sprite so that the pipes `stop`{:class="blockcontrol"} `when it receives Game Over`{:class="blockevents"}.

![pipes sprite](images/pipes-sprite.png)

```blocks
when I receive [Game Over v]
stop [other scripts in sprite v]
```

--- /task ---

--- task ---

Now test your game and see how long you can last!

--- /task ---


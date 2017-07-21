## Detect collision with the pipes

To make the game a challenge, the player needs to guide Flappy through the gaps without touching the pipes or the edges of the screen. Now we'll add some blocks to detect if Flappy hits something.



+ Let's add a sound to play when Flappy collides. Click on the **Flappy** sprite then on the `Sounds` tab.
+ Click the `Choose sound from library` button.
+ Pick a collision sound for **Flappy**. The **screech** sound is good.
+ Now click back on the `Scripts` tab.
+ Add the following script:
```blocks
    when FLAG clicked
        wait until <(touching [edge v]?) or (touching [Pipe v]?)>
        play sound [screech v]
        say [Game Over!]
        broadcast [GameOver v]
        stop [other scripts in sprite v]
```
+ Click on the **Pipe** sprite and add a script:
```blocks
    when I receive [GameOver v]
        stop [other scripts in sprite v]
```

## Test Your Project

__Click the green flag__, does the game end when Flappy touches a pipe or the edge of the screen?




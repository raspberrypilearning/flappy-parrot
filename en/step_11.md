

## fall off the stage

--- challenge ---


When the player loses make Flappy fall off the bottom of the stage before ending the game.

+ Replace the `broadcast GameOver` {.blockbrown}  block with `broadcast Fall` {.blockbrown}
+ Now add the following scripts:
```blocks
    when I receive [Fall v]
        repeat (10)
            turn ccw (5) degrees

    when I receive [Fall v]
        repeat until <(y position) < [-180]>
            change y by (rise)
            change [rise v] by (-0.4)
        end
        hide
        broadcast [GameOver v]
```
+ Don't forget to add a `show` {.blockpurple} block and reset Flappy's direction when the game restarts.



__Click the green flag__, does Flappy now fall off the screen after hitting a pipe? Does Flappy reappear in the correct orientation when restarting the game.


--- /challenge ---


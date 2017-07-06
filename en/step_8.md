

## Add scoring




The player should score a point every time Flappy makes it though a pipe. Let's add that next.



+ Let's add a sound to play when Flappy scores a point. Click on the **Pipe** sprite add a score sound. **bird** is a good choice.
+ Now click back on the `Scripts` {.blockgrey} tab.
+ Make a new variable `For all sprites` {.blockgrey} and call it `score` {.blockorange}.
+ Add a block to set the score to 0 when the flag is clicked.
+ Add the following block:
```blocks
    when I start as a clone
        wait until <(x position) < ([x position v] of [Flappy v])>
        change [score v] by (1)
        play sound [bird v]
```



__Click the green flag__, does the player score points for flying Flappy through the pipes?





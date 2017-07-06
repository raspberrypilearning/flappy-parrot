

## add a high score

--- challenge ---


+ Make a new variable called `hi-score` {.blockorange}
+ when the game is over check if you need to set a new high score:
```blocks
    when I receive [GameOver v]
        if <(score) > (hi-score)> then
            set [hi-score v] to (score)
        end
        stop [other scripts in sprite v]
```



__Click the green flag__, does your score update the `hi-score`?


--- /challenge ---


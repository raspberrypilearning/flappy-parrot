## Add scoring

The player should score a point every time Flappy makes it through a gap between pipes. Let's add that code for that next!

+ Make a new variable `For all sprites` and call it `score`{:class="blockdata"}.

+ Each `Pipes` clone is going to `wait until` Flappy has flown past, and then increase the score.

    First, set the score to `0` when the game begins:

    ![screenshot](images/flappy-score-0.png)

+ Then add the following code to the `Pipes` sprite:

    ![screenshot](images/flappy-clone-wait.png)

+ Complete the code so that a point is scored, and a sound of your choice is played, when Flappy's `x` position is greater than (`>`) the pipe's `x` position.

Test your code and make sure you score a point every time Flappy gets past an obstacle. Make sure the score goes back to `0` when you start a new game.

--- hints ---
--- hint ---
You need to fill in the condition in the `wait until`{:class="blockcontrol"} block to check for Flappy's `x position` being `greater than (`>`) ` the `x position` of `Pipes`.  

![screenshot](images/flappy-clone-wait.png)

You'll need to add blocks after the `wait until`{:class="blockcontrol"} block to `change the score` and `play a sound`. You could use the 'pop' sound, or add a sound from the library — 'bird' works well.
--- /hint ---
--- hint ---
Try using these blocks:

![screenshot](images/flappy-score-blocks.png)
--- /hint ---
--- hint ---
Your code should look like this:
![screenshot](images/flappy-score-code.png)
--- /hint ---
--- /hints ---

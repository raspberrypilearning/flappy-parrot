## Add scoring

The player should score a point every time Flappy makes it through a gap between pipes. Let's add that code for that next!

--- task ---

Make a new variable `For all sprites` and call it `score`{:class="blockdata"}.

[[[generic-scratch-add-variable]]]

--- /task ---

Each `Pipes` clone is going to `wait until`{:class="blockcontrol"}, Flappy has flown past, and then increase the score.

--- task ---

First, `set score to 0`{:class="blockdata"} when the game begins:

```blocks
when green flag clicked
+ set [score v] to [0]
set size to (200) %
hide
forever 
  create clone of [myself v]
  wait (2) secs
end
```

--- /task ---

--- task ---

Then add the following code to the `Pipes` sprite:

```blocks
when I start as a clone
wait until <>
```

--- /task ---

--- task ---

Complete the code so that a point is scored, and a sound of your choice is played, when Flappy's `x` position is greater than the pipe's `x` position.

You could use the 'pop' sound, or add a sound from the library — 'bird' works well.

--- hints ---

--- hint ---

You need to `wait until`{:class="blockcontrol"} `Flappy's x position`{:class="blocksensing"} is `greater than (>)`{:class="blockoperators"} the `x position`{:class="blockmotion"} of `Pipes`.  

```blocks
when I start as a clone
+ wait until <>
```

Then `change the score by 1`{:class="blockdata"} and `play a sound`{:class="blocksound"}. 

--- /hint ---

--- hint ---

Try using these blocks:

```blocks
when I start as a clone
wait until <>

play sound [pop v]

change [score v] by (1)

[x position v] of [Flappy v]

x position

() > ()
```

--- /hint ---

--- hint ---

Your code should look like this:

```blocks
when I start as a clone
wait until <([x position v] of [Flappy v]) > (x position)>
change [score v] by (1)
play sound [pop v]
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Test your code and make sure you score a point every time Flappy gets past an obstacle. Make sure the score goes back to `0` when you start a new game.

--- /task ---

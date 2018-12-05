## Make the pipes move

Next you're going to make the pipes move across the screen to create an obstacle course.

![pipes moving across the screen](images/flappy-clones-test.png)

--- task ---

First make the pipes appear by adding code to the Pipes sprite so that, `when the green flag is clicked`{:class="blockevents"}, the sprite `forever`{:class="blockcontrol"} `creates a clone of itself`{:class="blockcontrol"} every two seconds. 

![pipes sprite](images/pipes-sprite.png)

```blocks
when green flag clicked
set size to (200) %
hide
forever 
  create clone of [myself v]
  wait (2) secs
end
```

**Tip:** clones are just copies of a sprite, and they are really useful for creating games. 

--- /task ---

--- task ---

Next make the pipes move by adding code so that, `when a clone starts`{:class="blockcontrol"}, the clone appears on the right side of the Stage and `glides`{:class="blockmotion"} across to the left.

![pipes sprite](images/pipes-sprite.png)

```blocks
when I start as a clone
show
go to x: (240) y: (0)
glide (4) secs to x: (-240) y: (0)
delete this clone
```

**Tip:** you can stop the pipes scrolling by clicking the red **stop** button next to the green flag.

--- /task ---

Now you should have lots of pipes, but their gaps are always in the same place. 

You can add some variety by using a `random`{:class="blockoperators"} number for the Pipes sprite's `y position`{:class="blockmotion"}.

![pipes at different heights](images/flappy-height-test.png)

--- task ---

Modify your sprite's code so that each sprite clone `picks a random number from -80 to 80`{:class="blockoperators"} and `glides`{:class="blockmotion"} to that `y position`{:class="blockmotion"}:

![pipes sprite](images/pipes-sprite.png)

```blocks
when I start as a clone
show
+ go to x: (240) y: (pick random (-80) to (80))
+ glide (4) secs to x: (-240) y: (y position)
delete this clone
```

--- /task ---


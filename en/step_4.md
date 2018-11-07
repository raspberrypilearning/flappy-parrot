## Make the pipes move

Next you'll get the pipes moving across the screen to create an obstacle course.

![pipes moving across the screen](images/flappy-clones-test.png)

--- task ---

First you will make the pipes appear by adding the code so that `When the green flag is clicked`{:class="blockevents"} it `creates a clone`{:class="blockcontrol"} every 2 seconds `forever`{:class="blockcontrol"}. 

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

**Tip:** clones are just copies of a sprite and you can create as many as you like and its a really useful when creating games. 

--- /task ---

--- task ---

Next you need to make the pipes move by adding the code so that `When a clone starts`{:class="blockcontrol"} it appears on the right and `glides`{:class="blockmotion"} across the screen to the left.

![pipes sprite](images/pipes-sprite.png)

```blocks
when I start as a clone
show
go to x: (240) y: (0)
glide (4) secs to x: (-240) y: (0)
delete this clone
```

Tip: you can stop the pipes scrolling by clicking the red stop button.

--- /task ---

Now you should have lots of pipes, but the gap is always in the same place. 

You can add some variety by using a `random`{:class="blockoperators"} number for the `y position`{:class="blockmotion"}.

![pipes at different heights](images/flappy-height-test.png)

--- task ---

Modify your code to `pick a random number from -80 to 80`{:class="blockoperators"} and `glide`{:class="blockmotion"} to that `y position`{:class="blockmotion"}:

![pipes sprite](images/pipes-sprite.png)

```blocks
when I start as a clone
show
+ go to x: (240) y: (pick random (-80) to (80))
+ glide (4) secs to x: (-240) y: (y position)
delete this clone
```

--- /task ---


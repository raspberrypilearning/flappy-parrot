## Make the pipes move

Next you're going to make the pipes move across the screen to create an obstacle course.

![pipes moving across the screen](images/flappy-clones-test.png)

--- task ---

First make the pipes appear by adding code to the Pipes sprite so that, `when the green flag is clicked`{:class="block3events"}, the sprite `forever`{:class="block3control"} `creates a clone of itself`{:class="block3control"} every two seconds. 

![pipes sprite](images/pipes-sprite.png)

![blocks_1545312846_5430117](images/blocks_1545312846_5430117.png)

**Tip:** clones are just copies of a sprite, and they are really useful for creating games. 

--- /task ---

--- task ---

Next make the pipes move by adding code so that, `when a clone starts`{:class="block3control"}, the clone appears on the right side of the Stage and `glides`{:class="block3motion"} across to the left.

![pipes sprite](images/pipes-sprite.png)

![blocks_1545312847_7423456](images/blocks_1545312847_7423456.png)

**Tip:** you can stop the pipes scrolling by clicking the red **stop** button next to the green flag.

--- /task ---

Now you should have lots of pipes, but their gaps are always in the same place. 

You can add some variety by using a `random`{:class="block3operators"} number for the Pipes sprite's `y position`{:class="block3motion"}.

![pipes at different heights](images/flappy-height-test.png)

--- task ---

Modify your sprite's code so that each sprite clone `picks a random number from -80 to 80`{:class="block3operators"} and `glides`{:class="block3motion"} to that `y position`{:class="block3motion"}:

![pipes sprite](images/pipes-sprite.png)

![blocks_1545312848_9051208](images/blocks_1545312848_9051208.png)

--- /task ---


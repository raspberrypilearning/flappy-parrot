

## Make Flappy fly

Next, we want Flappy to flap upwards when you press the space bar. You'll need to time your taps to get through the gaps in the pipes.

+ Can you add code to make Flappy fly upwards when you tap the spacebar?

--- hints ---
--- hint ---
When the __space key is pressed__, Flappy should move upwards by __changing its y coordinate__ by a small amount (say 6 times). This should be __repeated 10 times__.
--- /hint ---
--- hint ---
Here are the blocks you'll need:
![screenshot](images/flappy-up-blocks.png)
--- /hint ---
--- hint ---
Here's how your code should look:
![screenshot](images/flappy-up-code.png)
--- /hint ---
--- hints ---

+ Now you need to get Flappy's wings flapping!

    Click on the __Costumes__ tab and name the costumes **wings up** and **wings down**.

    ![screenshot](images/flappy-wings.png)

+ Can you make Flappy's costume change to __wings down__ when you press space and then __wings up__ half way through the upward movement?

--- hints ---
--- hint ---
You'll need to split the upward motion in half so that you can change costume at the beginning and in the middle.

You'll then need to use `switch costume to` {.blocklooks} blocks to change how Flappy looks.
--- /hint ---
--- hint ---
Split your code like this:

![screenshot](images/flappy-wings-hint.png)

And add blocks to `switch costume to` {.blocklooks} __wings down__ at the beginning and __wings up__ in the middle.
--- /hint ---
--- hint ---
Your code should look like this:

![screenshot](images/flappy-wings-code.png)

--- /hint ---
--- /hints ---

+ Now you can test your code, but nothing bad happens if you hit a pipe.

## Make Flappy fly

Next we want Flappy to flap upwards when you press the `space` bar. You'll need to time your taps to get through the gaps in the pipes.

+ Can you add code to make Flappy fly upwards when you tap the `space` bar?

--- hints ---
--- hint ---
When the `space key is pressed`, Flappy should move upwards by `changing its y coordinate` by a small amount (e.g.`6`). This should be `repeated 10 times`.
--- /hint ---
--- hint ---
Here are the blocks you'll need:
![screenshot](images/flappy-up-blocks.png)
--- /hint ---
--- hint ---
Here's how your code should look:
![screenshot](images/flappy-up-code.png)
--- /hint ---
--- /hints ---

Now you need to get Flappy's wings flapping!

+ Click on the **Costumes** tab, and name the costumes `wings up` and `wings down`.

    ![screenshot](images/flappy-wings.png)

+ Can you make Flappy's costume change to `wings down` when you press `space`, and then to `wings up` halfway through the upward movement?

--- hints ---
--- hint ---
You'll need to split the upward motion in half so that you can change costume at the beginning and in the middle.

You'll then need to use `switch costume to`{:class="blocklooks"} blocks to change how Flappy looks.
--- /hint ---
--- hint ---
Split your code like this:

![screenshot](images/flappy-wings-hint.png)

Add blocks to `switch costume to`{:class="blocklooks"} `wings down` at the beginning, and `wings up` in the middle.
--- /hint ---
--- hint ---
Your code should look like this:

![screenshot](images/flappy-wings-code.png)

--- /hint ---
--- /hints ---

+ Now you can test your code. As you'll see, nothing bad happens if you hit a pipe. In the next step, you'll change that.

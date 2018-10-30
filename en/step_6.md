## Make Flappy fly

Next you will make Flappy flap upwards when you press the <kbd>space</kbd> bar. You'll need to time your taps to get through the gaps in the pipes.

--- no-print ---

![flappy flying upwards when space bar is pressed](images/flappy-flying.gif)

--- /no-print ---

--- task ---

Lets add the code to make Flappy fly upwards when you tap the <kbd>space</kbd> bar?

When the `space key is pressed`{:class="blockevents"}, Flappy should move upwards by `changing its y coordinate`{:class="blockmotion"} by a small amount (e.g.`6`). By `repeating 10 times` it will appear that Flappy has flown upwards.

Here's how your code should look.

```blocks
when [space v] key pressed
repeat (10) 
  change y by (6)
end
```

--- /task ---

Now you need to get Flappy's wings flapping!

--- task ---

Click on the **Costumes** tab, and name the costumes `wings up` and `wings down`.

![naming the costumes](images/flappy-wings.png)

--- /task ---

Can you make Flappy's costume change to `wings down` when you press <kbd>space</kbd>, and then to `wings up` halfway through the upward movement?

--- hints ---

--- hint ---

You'll need to split the upward motion in half so that you can change costume at the beginning and in the middle by using 2 `repeat`{:class="blockcontrol"} blocks.

You'll then need to use `switch costume to`{:class="blocklooks"} blocks to change how Flappy looks.

--- /hint ---
--- hint ---

You will need to use these blocks:

```blocks
repeat (5) 
  change y by (6)
end

repeat (5) 
  change y by (6)
end

switch costume to [wings up v]

switch costume to [wings down v]

when [space v] key pressed
```

--- /hint ---

--- hint ---

Your code should look like this:

```blocks
when [space v] key pressed
switch costume to [wings down v]
repeat (5) 
  change y by (6)
end
switch costume to [wings up v]
repeat (5) 
  change y by (6)
end
```

--- /hint ---

--- /hints ---

--- task ---

Now you can test your code. As you'll see, nothing bad happens if you hit a pipe. In the next step, you'll change that.

--- /task ---


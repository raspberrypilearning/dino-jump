## Make the character jump

Make the character jump up and land back in the same place.

> [!TASK]
>
> Open the **Variables** palette, select **Make a Variable**, and create a variable called `jump height`{:class="block3variables"}. Tick its checkbox so you can see its value on the Stage.
>
> ![The Make a Variable button in the Variables palette.](images/make-a-variable.png)
>
> ![A ticked variable checkbox showing the value on the Stage.](images/variable-checkbox.png)

> [!TASK]
>
> On the character sprite, update the green flag script so the jump height is reset when the game starts.
>
> ```blocks3
> when green flag clicked
> show
> +set [jump height v] to (150)
> go to x: (-100) y: (-70)
> point in direction (90)
> set size to (100) %
> ```

> [!TASK]
>
> Add a new script to the character sprite so it jumps when the player presses the space key.
>
> ```blocks3
> when [space v] key pressed
> glide (0.3) secs to x: (-100) y: ((y position) + (jump height))
> glide (0.7) secs to x: (-100) y: ((y position) - (jump height))
> ```

> [!TASK]
>
> Test your project. The character should jump up and come back down when you press the space key.

> [!TIP]
>
> Changing `jump height`{:class="block3variables"} later will make the jump higher or lower without rebuilding the whole script.

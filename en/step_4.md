## Add obstacles

Add an obstacle so your dinosaur has something to avoid.

> [!TASK]
>
> Choose a cactus or rock sprite from the Scratch library.

> [!TASK]
>
> Place the obstacle near the right side of the stage and make it move left.
>
> ```blocks3
> when green flag clicked
> go to x: (240) y: (-80)
> forever
> change x by (-5)
> wait (0.03) seconds
> end
> ```

> [!TASK]
>
> Add a second script so the obstacle returns to the right side after it reaches the left edge.
>
> ```blocks3
> when green flag clicked
> forever
> if <(x position) < (-240)> then
> go to x: (240) y: (-80)
> end
> end
> ```

> [!TASK]
>
> Test your project. The obstacle should slide across the screen and reappear ready for the next run.

> [!TIP]
>
> This is a simple way to create a repeating obstacle that keeps the game moving.

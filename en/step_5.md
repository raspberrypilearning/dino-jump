## Add scoring and game over

Make the game more exciting by tracking how long the player survives and ending the game when the dinosaur crashes.

> [!TASK]
>
> Create a variable called `score`{:class="block3variables"}.

> [!TASK]
>
> Add a script to the Stage that resets the score when the green flag is clicked.
>
> ```blocks3
> when green flag clicked
> set [score v] to (0)
> ```

> [!TASK]
>
> Add a script to the Stage so the score increases every second.
>
> ```blocks3
> when green flag clicked
> forever
> wait (1) seconds
> change [score v] by (1)
> end
> ```

> [!TASK]
>
> Add a script to the dinosaur sprite so the game stops when it touches an obstacle. Choose your obstacle sprite's name from the menu.
>
> ```blocks3
> when green flag clicked
> forever
> if <touching [Obstacle v]?> then
> stop [all v]
> end
> end
> ```

> [!TASK]
>
> Test your project. Your score should increase and the game should stop when the dinosaur collides with the obstacle.

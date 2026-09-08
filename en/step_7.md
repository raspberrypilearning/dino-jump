## Test and tune your game

Check that all your scripts work together, then choose how hard your game is to play.

> [!TASK]
>
> Click the green flag and make sure:
>
> - `score`{:class="block3variables"} starts at `0`
> - animated obstacles appear on the right and move towards Pico
> - the time between obstacles changes
> - pressing the space bar makes Pico jump and land
> - avoiding an obstacle adds `1` to `score`{:class="block3variables"}
> - touching an obstacle plays your collision sound and stops the game
>
> Fix any blocks that do not behave as expected, then play again.

> [!TASK]
>
> **Change the speed.** Change the number in the `change x by ()`{:class="block3motion"} block in the clone script.
>
> A more negative number, such as `-7`, makes every obstacle move faster. A number closer to zero makes them move more slowly.

> [!TASK]
>
> **Change the gaps.** Change the two numbers in `pick random () to ()`{:class="block3operators"}.
>
> Smaller numbers create obstacles more often, while larger numbers leave wider gaps.

> [!TASK]
>
> **Test again.** Play the game a few times and keep adjusting the numbers until your game feels fair.

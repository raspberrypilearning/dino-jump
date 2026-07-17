## Test and tune your game

Check that the scripts work together, then adjust the difficulty.

> [!TASK]
>
> Click the green flag and check that:
>
> - the score starts at `0`
> - animated obstacles appear after one second and move from right to left
> - the time between obstacles changes
> - avoiding an obstacle adds `1` to the score
> - touching an obstacle plays your collision sound and stops the game (the example uses `Bite`)

> [!TASK]
>
> Adjust the starting value of `speed`{:class="block3variables"} in the obstacle's green flag script. A more negative number, such as `-7`, makes every clone move faster.

> [!TASK]
>
> Adjust the two numbers in `pick random (0.8) to (2.4)`{:class="block3operators"}. Smaller numbers create obstacles more often; larger numbers leave wider gaps.

> [!TIP]
>
> **Difficulty** comes from how much time the player has to react. Faster speed and shorter gaps make each jump decision more demanding.

> [!TASK]
>
> If the obstacle does not meet the character at the right height, adjust its starting `y` position. Keep its starting `x` position beyond the right edge so clones do not suddenly appear on the Stage.

> [!TASK]
>
> Test again until the game is challenging but still possible to play.

## Test and tune your game

Check that the blocks work together, then adjust the difficulty.

> [!TASK]
>
> Click the green flag and check that:
>
> - `score`{:class="block3variables"} starts at `0`
> - animated obstacles appear after one second and move from right to left
> - the time between obstacles changes
> - avoiding an obstacle adds `1` to `score`{:class="block3variables"}
> - touching an obstacle plays your collision sound and stops the game

> [!TASK]
>
> Adjust the starting value of `speed`{:class="block3variables"} in the obstacle's green flag script. A more negative number, such as `-7`, makes every clone move faster.

> [!TASK]
>
> Adjust the two numbers in `pick random (0.8) to (2.4)`{:class="block3operators"}. Smaller numbers create obstacles more often; larger numbers leave wider gaps.

> [!TIP]
>
> Faster obstacles and shorter gaps give the player less time to react, making the game more difficult.

> [!TASK]
>
> If the obstacle does not meet the character at the right height, adjust its starting `y` position. Keep its starting `x` position beyond the right edge so obstacles do not suddenly appear on the Stage.

> [!TASK]
>
> **Test again** until the game is challenging but still possible to play.

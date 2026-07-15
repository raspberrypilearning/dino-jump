## Add obstacles

Use one hidden obstacle sprite to create clones that move across the Stage. Each clone will either hit the character or leave the Stage and add to the score.

> [!TASK]
>
> Add the `Bear-walking` sprite from the Scratch library. Its costumes will make each obstacle look as though it is walking.

> [!TASK]
>
> Select the `Bear-walking` sprite. Open the **Sounds** tab, choose **Choose a Sound**, and add the `Bite` sound.
>
> ![The Sounds tab at the top-left of the Scratch editor.](images/sounds_tab.png)

> [!TASK]
>
> Create two variables for all sprites: `speed`{:class="block3variables"} and `score`{:class="block3variables"}. Show `score` on the Stage, but untick `speed` so players cannot see it.
>
> `speed` will control every obstacle clone, while `score` will count the obstacles the character avoids.

> [!TASK]
>
> Add this setup script to the `Bear-walking` sprite.
>
> ```blocks3
> when green flag clicked
> set rotation style [left-right v]
> set [speed v] to (-5)
> set [score v] to (0)
> set size to (25) %
> go to x: (280) y: (-85)
> hide
> ```
>
> The negative `speed`{:class="block3variables"} will move obstacles to the left. The original bear starts just beyond the right edge and stays hidden because only its clones should appear.

> [!TASK]
>
> Extend the setup script so it creates obstacle clones at random intervals.
>
> ```blocks3
> when green flag clicked
> set rotation style [left-right v]
> set [speed v] to (-5)
> set [score v] to (0)
> set size to (25) %
> go to x: (280) y: (-85)
> hide
> +wait (1) seconds
> +forever
> +  create clone of (myself v)
> +  wait (pick random (0.8) to (2.4)) seconds
> +end
> ```
>
> The first obstacle waits for one second. After that, the random wait makes the gaps between obstacles unpredictable.

> [!TASK]
>
> Start a second script that prepares each new clone.
>
> ```blocks3
> when I start as a clone
> show
> point in direction (-90)
> ```
>
> Each clone appears at the original bear's position and faces left, ready to cross the Stage.

> [!TASK]
>
> Make the clone animate and move until it has passed the left side of the Stage.
>
> ```blocks3
> when I start as a clone
> show
> point in direction (-90)
> +repeat until <(x position) < (-200)>
> +  next costume
> +  change x by (speed)
> +end
> ```
>
> `next costume`{:class="block3looks"} animates the bear. Each loop moves it left by the value stored in `speed`{:class="block3variables"}.

> [!TASK]
>
> Inside the `repeat until`{:class="block3control"} loop, check whether the obstacle is touching the character. Select your character sprite's name from the `touching`{:class="block3sensing"} menu; the example uses `Giga Walking`.
>
> ```blocks3
> when I start as a clone
> show
> point in direction (-90)
> repeat until <(x position) < (-200)>
>   next costume
>   change x by (speed)
> +  if <touching (Giga Walking v)?> then
> +    start sound (Bite v)
> +    hide
> +    stop [all v]
> +  end
> end
> ```
>
> The collision check runs after every movement. A collision plays the sound, hides the obstacle, and ends the game.

> [!TASK]
>
> After the loop, award one point and remove the clone.
>
> ```blocks3
> when I start as a clone
> show
> point in direction (-90)
> repeat until <(x position) < (-200)>
>   next costume
>   change x by (speed)
>   if <touching (Giga Walking v)?> then
>     start sound (Bite v)
>     hide
>     stop [all v]
>   end
> end
> +change [score v] by (1)
> +delete this clone
> ```
>
> These blocks run only when the clone reaches the left edge without a collision, so the player earns one point. Deleting the off-screen clone prevents unused clones from building up.

> [!TASK]
>
> Test your project. Obstacles should appear at different times, walk from right to left, increase the score when avoided, and stop the game when they touch the character.

## Detect collisions and keep score

End the game when an obstacle touches the character, and award a point when the character avoids one.

> [!TASK]
>
> Add an `if`{:class="block3control"} block to check whether the obstacle is touching the character. Choose your character's name from the `touching`{:class="block3sensing"} menu. The example uses `Pico`.
>
> ![Dinosaur5 sprite.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> when I start as a clone
> show
> repeat until <(x position) < (-200)>
>   next costume
>   change x by (speed)
> +  if <touching (Pico v)?> then
>     hide
>     stop [all v]
>   end
> end
> delete this clone
> ```

> [!TASK]
>
> Select the obstacle and open the **Sounds** tab. `Dinosaur5` already includes the `bite` sound. You can use it, or choose **Choose a Sound** to add a different collision sound.
>
> ![The Sounds tab at the top-left of the Scratch editor.](images/sounds_tab.png)

> [!TASK]
>
> Add the sound inside the `if`{:class="block3control"} block, before `hide`{:class="block3looks"}.
>
> ![Dinosaur5 sprite.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> if <touching (Pico v)?> then
> +  play sound (bite v) until done
>   hide
>   stop [all v]
> end
> ```

> [!TASK]
>
> Open the `Variables`{:class="block3variables"} menu, select **Make a Variable**, and create a variable called `score`{:class="block3variables"} for all sprites.
>
> Set `score`{:class="block3variables"} to `0` in the obstacle's green flag script.
>
> ![Dinosaur5 sprite.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> when green flag clicked
> set rotation style [left-right v]
> set [speed v] to (-5)
> +set [score v] to (0)
> set size to (25) %
> go to x: (280) y: (-85)
> point in direction (-90)
> hide
> wait (1) seconds
> forever
>   create clone of (myself v)
>   wait (pick random (0.8) to (2.4)) seconds
> end
> ```

> [!TASK]
>
> Add `change score by 1`{:class="block3variables"} just before `delete this clone`{:class="block3control"}. It will only run when the obstacle reaches the left side without touching the character.
>
> ![Dinosaur5 sprite.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> when I start as a clone
> show
> repeat until <(x position) < (-200)>
>   next costume
>   change x by (speed)
>   if <touching (Pico v)?> then
>     play sound (bite v) until done
>     hide
>     stop [all v]
>   end
> end
> +change [score v] by (1)
> delete this clone
> ```

> [!TASK]
>
> **Test your project.** Avoiding an obstacle should add one to `score`{:class="block3variables"}. Touching one should play the collision sound and stop the game.

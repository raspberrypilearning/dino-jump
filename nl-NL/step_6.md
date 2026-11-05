## Detect collisions and keep score

End the game when an obstacle catches Pico, and award a point whenever an obstacle passes Pico safely.

> [!TASK]
>
> Inside the clone's movement loop, add an `if then`{:class="block3control"} block that checks whether the obstacle is `touching ()`{:class="block3sensing"} Pico.
>
> If it is, stop all the scripts.
>
> ![Dinosaur5 sprite.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> repeat until <(x position) < (-240)>
>   next costume
>   change x by (-5)
> +  if <touching (Pico v)?> then
>     stop [all v]
>   end
> end
> ```

> [!TASK]
>
> Click on the `Dinosaur5`{:class="block3looks"} sprite, then open the `Sounds`{:class="block3sound"} tab.
>
> `Dinosaur5` already includes the `bite`{:class="block3sound"} sound. You can use it, or choose a different collision sound.
>
> ![The Sounds tab at the top-left of the Scratch editor.](images/sounds_tab.png)

> [!TASK]
>
> Add a `play sound () until done`{:class="block3sound"} block inside the collision check, before `stop all`{:class="block3control"}.
>
> ![Dinosaur5 sprite.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> if <touching (Pico v)?> then
> +  play sound (bite v) until done
>   stop [all v]
> end
> ```

> [!TASK]
>
> Make a new variable called `score`{:class="block3variables"}, **For all sprites**.
>
> ![The Make a Variable button in the Variables menu.](images/make-a-variable.png)
>
> Keep its checkbox ticked, so the variable appears on the Stage.
>
> ![A ticked variable checkbox in the Variables menu.](images/variable-checkbox.png)

> [!TASK]
>
> In the obstacle's setup script, set `score`{:class="block3variables"} to `0` when the green flag is clicked.
>
> ![Dinosaur5 sprite.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> when green flag clicked
> +set [score v] to (0)
> set size to (25) %
> go to x: (280) y: (-85)
> hide
> forever
>   create clone of (myself v)
>   wait (pick random (0.8) to (2.4)) seconds
> end
> ```

> [!TASK]
>
> In the clone script, add `change score by ()`{:class="block3variables"} after the movement loop and before `delete this clone`{:class="block3control"}.
>
> ![Dinosaur5 sprite.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> when I start as a clone
> show
> repeat until <(x position) < (-240)>
>   next costume
>   change x by (-5)
>   if <touching (Pico v)?> then
>     play sound (bite v) until done
>     stop [all v]
>   end
> end
> +change [score v] by (1)
> delete this clone
> ```
>
> The new block only runs after an obstacle reaches the left edge without touching Pico.

> [!TASK]
>
> **Test your project.** Avoiding an obstacle should add `1` to `score`{:class="block3variables"}. Touching one should play your collision sound and stop the game.

## Make the obstacles move

Make a stream of obstacles appear and travel across the Stage towards Pico.

> [!TASK]
>
> Add a `forever`{:class="block3control"} loop to the end of the obstacle's script. Inside the loop, create a clone and wait for one second before making the next one.
>
> Add a `hide`{:class="block3looks"} block before the loop, so that only the clones appear in the game.
>
> ![Dinosaur5 sprite.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> when green flag clicked
> set size to (25) %
> go to x: (280) y: (-85)
> +hide
> +forever
>   create clone of (myself v)
>   wait (1) seconds
> end
> ```
>
> A **clone** is a copy of a sprite. Each clone starts hidden, because the original obstacle is hidden.

> [!TASK]
>
> Start a new script on the obstacle sprite with a `when I start as a clone`{:class="block3control"} block.
>
> Add a `show`{:class="block3looks"} block, then a `repeat until`{:class="block3control"} loop that checks whether the clone's `x position`{:class="block3motion"} is less than `-240`. Inside the loop, change its x position by `-5`.
>
> ![Dinosaur5 sprite.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> +when I start as a clone
> +show
> +repeat until <(x position) < (-240)>
>   change x by (-5)
> end
> ```
>
> A negative number in `change x by ()`{:class="block3motion"} moves the clone to the left.

> [!TASK]
>
> Add `delete this clone`{:class="block3control"} after the movement loop, so that old obstacles do not build up.
>
> ![Dinosaur5 sprite.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> when I start as a clone
> show
> repeat until <(x position) < (-240)>
>   change x by (-5)
> end
> +delete this clone
> ```

> [!TASK]
>
> In the obstacle's `forever`{:class="block3control"} loop, replace the `wait () seconds`{:class="block3control"} block with one that contains a `pick random () to ()`{:class="block3operators"} block.
>
> ![Dinosaur5 sprite.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> forever
>   create clone of (myself v)
> +  wait (pick random (0.8) to (2.4)) seconds
> end
> ```
>
> Obstacles now appear at random intervals between the two numbers you chose.

> [!TASK]
>
> Inside the clone's `repeat until`{:class="block3control"} loop, add a `next costume`{:class="block3looks"} block before the movement block.
>
> ![Dinosaur5 sprite.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> when I start as a clone
> show
> repeat until <(x position) < (-240)>
> +  next costume
>   change x by (-5)
> end
> delete this clone
> ```

> [!TASK]
>
> **Test your project.** Obstacles should appear at different times, change costume as they travel, and disappear once they have passed Pico.

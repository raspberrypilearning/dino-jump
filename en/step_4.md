## Add obstacles

Create an obstacle sprite that your character needs to jump over.

> [!TASK]
>
> Choose any sprite to be an obstacle. This example uses `Bear-walking`, which has several costumes for a walking animation, but your obstacle can look however you like.

> [!TASK]
>
> Select the obstacle and click the **Code** tab. Add these blocks to set its position, direction, and size.
>
> ![Bear-walking sprite.](images/Bear-walk-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> +when green flag clicked
> +set rotation style [left-right v]
> +set size to (25) %
> +go to x: (280) y: (-85)
> +point in direction (-90)
> ```
>
> The example position places the obstacle just beyond the right edge of the Stage. Change the `y` position if your obstacle does not sit on the ground.

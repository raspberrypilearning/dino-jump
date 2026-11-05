## Make the character jump

Make Pico jump into the air and land back in the same place.

> [!TASK]
>
> Add a new script with a `when space key pressed`{:class="block3events"} block and a `glide () secs to x: () y: ()`{:class="block3motion"} block.
>
> ![Pico sprite.](images/Pico-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> +when [space v] key pressed
> +glide (0.3) secs to x: (-100) y: (80)
> ```
>
> Press the space bar. Pico glides upwards and stays in the air.

> [!TASK]
>
> Add another `glide () secs to x: () y: ()`{:class="block3motion"} block to the bottom of the space-key script to bring Pico back to the ground.
>
> ![Pico sprite.](images/Pico-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> when [space v] key pressed
> glide (0.3) secs to x: (-100) y: (80)
> +glide (0.7) secs to x: (-100) y: (-70)
> ```

> [!TASK]
>
> **Test your project.** Press the space bar.
>
> Pico jumps up and lands back in the same place.

## Add the character and backdrop

Start a fresh Scratch project and add a character sprite and a backdrop.

> [!TASK]
>
> Open a [fresh Scratch project](https://scratch.mit.edu/projects/editor/){:target="_blank"} in a new tab. The project that opens with the Scratch cat is the right starting point.

> [!TASK]
>
> Delete the cat sprite.
>
> ![Deleting a sprite with the bin icon on its thumbnail.](images/delete-sprite.png)

> [!TASK]
>
> Add any character with **Choose a Sprite**. This example uses `Giga Walking`, but your character can look however you like.
>
> ![The Choose a Sprite button in the bottom-right of the Scratch editor.](images/sprite-choose.png)

> [!TASK]
>
> Add any backdrop with **Choose a Backdrop**. This example uses `Desert`, but choose a setting that suits your game.
>
> ![The Choose a Backdrop button in the bottom-right of the Scratch editor.](images/backdrop-choose.png)

> [!TASK]
>
> Place the character near the bottom of the Stage.
>
> ![Giga Walking sprite.](images/Giga-Walk1.png){:width="100px" height="100px" style="object-fit: contain;"}

> [!TASK]
>
> Select the character and click the **Code** tab. Add these blocks to set its position, direction, and size.
>
> ```blocks3
> +when green flag clicked
> +show
> +go to x: (-100) y: (-70)
> +point in direction (90)
> +set size to (100) %
> ```
>
> These values place the example character near the ground. Adjust the position and size if your character or backdrop is different.

> [!TIP]
>
> This is your **starting state**. It resets when you click the green flag before the game begins.

> [!TASK]
>
> **Test your project.** The character should appear in the same place each time you click the green flag.

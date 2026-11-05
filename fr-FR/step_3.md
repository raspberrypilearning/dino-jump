## Faire sauter le personnage

Faire sauter Pico en l'air et le faire retomber au même endroit.

> [!TASK]
>
> Ajoute un nouveau script avec un bloc `quand la touche espace est pressée`{:class="block3events"} et un bloc `glisser en () secs à x: () y: ()`{:class="block3motion"}.
>
> ![Pico sprite.](images/Pico-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> +when [space v] key pressed
> +glide (0.3) secs to x: (-100) y: (80)
> ```
>
> Appuie sur la barre d’espacement. Pico glisse vers le haut et reste dans les airs.

> [!TASK]
>
> Ajoute un autre bloc `glisser en () secs à x: () y: ()`{:class="block3motion"} au bas du script de la touche d'espace pour ramener Pico au sol.
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
> **Teste ton projet.** Appuie sur la barre d'espace.
>
> Pico saute et retombe au même endroit.

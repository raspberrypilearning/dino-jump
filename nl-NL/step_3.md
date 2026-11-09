## Laat het personage springen

Laat Pico in de lucht springen en weer op dezelfde plek landen.

> [!TASK]
>
> Voeg een nieuw script toe met een `wanneer spatiebalk is ingedrukt`{:class="block3events"} blok en een `schuif in () sec. naar x: () y: ()`{:class="block3motion"} blok.
>
> ![Pico sprite.](images/Pico-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> +when [space v] key pressed
> +glide (0.3) secs to x: (-100) y: (80)
> ```
>
> Druk op de spatiebalk. Pico zweeft omhoog en blijft in de lucht.

> [!TASK]
>
> Voeg nog een `schuif in () sec. naar x: () y: ()`{:class="block3motion"} blok toe aan de onderkant van het spatiebalkscript om Pico te laten landen.
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
> **Test je project.** Druk op de spatiebalk.
>
> Pico springt omhoog en landt weer op dezelfde plek.

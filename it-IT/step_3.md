## Fai saltare il personaggio

Fai saltare Pico e fallo atterrare nello stesso posto.

> [!TASK]
>
> Aggiungi un nuovo script con un blocco `quando si preme il tasto spazio`{:class="block3events"} e un blocco `scivola in () secondi a x: () y: ()`{:class="block3motion"}.
>
> ![Sprite Pico.](images/Pico-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> +when [spazio v] key pressed
> +glide (0.3) secs to x: (-100) y: (80)
> ```
>
> Premi la barra spaziatrice. Pico scivola verso l'alto e rimane in aria.

> [!TASK]
>
> Aggiungi un altro blocco `scivola in () secondi a x: () y: ()`{:class="block3motion"} in fondo allo script della barra spaziatrice per riportare Pico a terra.
>
> ![Sprite Pico.](images/Pico-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> when [spazio v] key pressed
> glide (0.3) secs to x: (-100) y: (80)
> +glide (0.7) secs to x: (-100) y: (-70)
> ```

> [!TASK]
>
> **Metti alla prova il tuo progetto.** Premi la barra spaziatrice.
>
> Fai saltare Pico e fallo atterrare nello stesso posto.

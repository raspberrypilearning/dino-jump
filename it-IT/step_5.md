## Fai muovere gli ostacoli

Fai apparire un flusso di ostacoli che attraversano lo Stage verso Pico.

> [!TASK]
>
> Aggiungi un blocco `per sempre`{:class="block3control"} alla fine dello script dell'ostacolo. All'interno del ciclo, crea un clone e attendi un secondo prima di crearne un altro.
>
> Aggiungi un blocco `nascondi`{:class="block3looks"} prima del ciclo, in modo che nel gioco appaiano solo i cloni.
>
> ![Sprite Dinosaur5.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> when green flag clicked
> set size to (25) %
> go to x: (280) y: (-85)
> +hide
> +forever
>   create clone of (me stesso v)
>   wait (1) seconds
> end
> ```
>
> Un **clone** è una copia di uno sprite. Ogni clone parte nascosto, perché l'ostacolo originale è nascosto.

> [!TASK]
>
> Avvia un nuovo script sullo sprite dell'ostacolo con un blocco `quando vengo clonato`{:class="block3control"}.
>
> Aggiungi un blocco `mostra`{:class="block3looks"}, quindi un ciclo `ripeti fino a quando`{:class="block3control"} che controlla se la `posizione x`{:class="block3motion"} del clone è inferiore a `-240`. All'interno del ciclo, cambia la sua posizione x di `-5`.
>
> ![Sprite Dinosaur5.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> +when I start as a clone
> +show
> +repeat until <(x position) < (-240)>
>   change x by (-5)
> end
> ```
>
> Un numero negativo in `cambia x di ()`{:class="block3motion"} sposta il clone a sinistra.

> [!TASK]
>
> Aggiungi `elimina questo clone`{:class="block3control"} dopo il ciclo di movimento, in modo che i vecchi ostacoli non si accumulino.
>
> ![Sprite Dinosaur5.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
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
> Nel ciclo `per sempre`{:class="block3control"} dell'ostacolo, sostituisci il blocco `attendi () secondi`{:class="block3control"} con uno che contenga un blocco `numero a caso tra () e ()`{:class="block3operators"}.
>
> ![Sprite Dinosaur5.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> forever
>   create clone of (me stesso v)
> +  wait (pick random (0.8) to (2.4)) seconds
> end
> ```
>
> Adesso gli ostacoli appaiono a intervalli casuali tra i due numeri che hai scelto.

> [!TASK]
>
> All'interno del ciclo `ripeti fino a quando`{:class="block3control"}, aggiungi un blocco `passa al costume seguente`{:class="block3looks"} prima del blocco di movimento.
>
> ![Sprite Dinosaur5.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
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
> **Metti alla prova il tuo progetto.** Gli ostacoli dovrebbero apparire in momenti diversi, cambiare aspetto durante il percorso e sparire una volta superato Pico.

## Laat de obstakels bewegen

Laat een reeks obstakels verschijnen en bewegen over het speelveld richting Pico.

> [!TASK]
>
> Voeg een `herhaal`{:class="block3control"} lus toe aan het einde van het script van het obstakel. Maak binnen de lus een kloon en wacht één seconde voordat je de volgende maakt.
>
> Voeg een `verdwijn`{:class="block3looks"} blok toe vóór de lus, zodat alleen de klonen in het spel verschijnen.
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
> Een **kloon** is een kopie van een sprite. Elke kloon begint verborgen, omdat het oorspronkelijke obstakel verborgen is.

> [!TASK]
>
> Start een nieuw script in de obstakel-sprite met een `wanneer ik als kloon start`{:class="block3control"} blok.
>
> Voeg een `verschijn`{:class="block3looks"} blok toe, dan een `herhaal tot`{:class="block3control"} lus die controleert of de `x positie`{:class="block3motion"} van de kloon kleiner is dan `-240`. Binnen de lus moet de x-positie met `-5` worden gewijzigd.
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
> Een negatief getal in `verander x met ()`{:class="block3motion"} verplaatst de kloon naar links.

> [!TASK]
>
> Voeg `verwijder deze kloon`{:class="block3control"} toe na de bewegingsloop, zodat oude obstakels zich niet ophopen.
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

## Ajouter des obstacles

Crée quelque chose pour que Pico saute au-dessus.

> [!TASK]
>
> Clique sur **Choisir un sprite**, puis trouve `Dinosaur5`{:class="block3looks"} dans la bibliothèque de sprites et clique dessus.
>
> ![Sprite Dinosaur5.](images/Dinosaur5-a.png)
>
> Dinosaur5 possède plusieurs costumes, ce qui lui permet de s'animer lorsqu'il se déplace.

> [!TASK]
>
> Clique sur le sprite `Dinosaur5`{:class="block3looks"}, puis clique sur l'onglet **Code**.
>
> Ajouter un script pour définir sa taille et sa position.
>
> ![Sprite Dinosaur5.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> +when green flag clicked
> +set size to (25) %
> +go to x: (280) y: (-85)
> ```

> [!TASK]
>
> **Teste ton projet.** Clique sur le drapeau vert.
>
> L'obstacle rétrécit et se déplace vers le bord droit de la scène, prêt à se diriger vers Pico.

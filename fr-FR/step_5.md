## Faire bouger les obstacles

Faire apparaître un flot d'obstacles qui traverse la scène en direction de Pico.

> [!TASK]
>
> Ajoute une boucle `répéter indéfiniment`{:class="block3control"} à la fin du script de l'obstacle. À l'intérieur de la boucle, crée un clone et attends une seconde avant d'en créer un autre.
>
> Ajoute un bloc `cacher`{:class="block3looks"} avant la boucle, de sorte que seuls les clones apparaissent dans le jeu.
>
> ![Sprite Dinosaur5.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
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
> Un **clone** est une copie d'un sprite. Chaque clone commence caché, car l'obstacle initial est caché.

> [!TASK]
>
> Démarre un nouveau script sur le sprite d'obstacle avec un bloc `quand je commence comme un clone`{:class="block3control"}.
>
> Ajoute un bloc `montrer`{:class="block3looks"}, puis une boucle `répéter jusqu'à ce que`{:class="block3control"} qui vérifie si la position `x du clone`{:class="block3motion"} est inférieure à `-240`. À l'intérieur de la boucle, change sa position en x de `-5`.
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
> Un nombre négatif dans `ajouter () à x`{:class="block3motion"} déplace le clone vers la gauche.

> [!TASK]
>
> Ajoute `supprimer ce clone`{:class="block3control"} après la boucle de mouvement, afin que les anciens obstacles ne s'accumulent pas.
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
> Dans la boucle `répéter indéfiniment`{:class="block3control"}, remplace le bloc `attendre () secondes`{:class="block3control"} par un bloc qui contient `nombre aléatoire entre () et ()`{:class="block3operators"}.
>
> ![Sprite Dinosaur5.](images/Dinosaur5-a.png){:width="100px" height="100px" style="object-fit: contain;"}
>
> ```blocks3
> forever
>   create clone of (myself v)
> +  wait (pick random (0.8) to (2.4)) seconds
> end
> ```
>
> Des obstacles apparaissent désormais à intervalles aléatoires entre les deux nombres que tu as choisis.

> [!TASK]
>
> À l'intérieur du bloc `répéter jusqu'à ce que`{:class="block3control"}, ajoute un bloc `costume suivant`{:class="block3looks"} avant le bloc de mouvement.
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
> **Teste ton projet.** Les obstacles doivent apparaître à différents moments, changer de costume au cours de leur déplacement et disparaître une fois qu'ils ont dépassé Pico.

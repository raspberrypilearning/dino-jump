## Tester et ajuster ton jeu

Vérifie que tous tes scripts fonctionnent ensemble, puis choisis la difficulté de ton jeu.

> [!TASK]
>
> Clique sur le drapeau vert et assure-toi que :
>
> - `score`{:class="block3variables"} commence à `0`
> - des obstacles animés apparaissent sur la droite et se déplacent vers Pico
> - le temps entre les obstacles change
> - appuyer sur la barre d'espace fait sauter et atterrir Pico
> - éviter un obstacle ajoute `1` à `score`{:class="block3variables"}
> - toucher un obstacle joue ton son de collision et arrête le jeu
>
> Corrige tous les blocs qui ne se comportent pas comme prévu, puis joue à nouveau.

> [!TASK]
>
> **Changer la vitesse.** Change le nombre dans le bloc `ajouter () à x`{:class="block3motion"} dans le script de clone.
>
> Un nombre plus négatif, tel que `-7`, rend chaque obstacle plus rapide. Un nombre plus proche de zéro les rend plus lents.

> [!TASK]
>
> **Modifier les intervalles.** Change les deux nombres dans `nombre aléatoire entre () et ()`{:class="block3operators"}.
>
> Les petits nombres créent plus souvent des obstacles, tandis que les grands nombres laissent des écarts plus importants.

> [!TASK]
>
> **Teste à nouveau.** Joue plusieurs fois et ajuste les nombres jusqu'à ce que le jeu te semble équilibré.

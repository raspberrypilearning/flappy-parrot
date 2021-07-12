## Ajouter un score

Le joueur doit marquer un point à chaque fois que Flappy franchit un espace entre les tuyaux.

--- task ---

Crée une nouvelle variable **pour tous les sprites** et appelle-la `score`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

Chaque clone de sprite « Tuyaux » doit `attendre jusqu'à ce que`{:class="block3control"} Flappy soit passé et ensuite augmente le `score`{:class="block3variables"}.

--- task ---

Tout d'abord, `mets le score à 0`{:class="block3variables"} lorsque le jeu commence :

![sprite tuyaux](images/pipes-sprite.png)

```blocks3
when green flag clicked
+ set [score v] to [0]
set size to (200) %
hide
forever 
  create clone of (myself v)
  wait (2) seconds
end
```

--- /task ---

--- task ---

Ajoute ensuite le code suivant au sprite `Tuyaux` :

![sprite tuyaux](images/pipes-sprite.png)

```blocks3
when I start as a clone
wait until <>
```

--- /task ---

--- task ---

Ajoute plus de code pour que, lorsque l'abscisse `x` de Flappy est supérieure à l'abscisse `x` du clone de tuyau, le `score`{:class="block3variables"} augmente de `1` et un son de ton choix est joué.

Tu peux utiliser le son « pop » si tu le souhaites, ou ajoute un son à partir de la bibliothèque, par exemple « bird ».

--- hints ---


--- hint ---

Tu dois `attendre jusqu'à ce que`{:class="block3control"} `l'abscisse x de Flappy`{:class="block3sensing"} soit `supérieur à (>)`{:class="block3operators"} `l'abscisse x`(:class="block3motion"} des `tuyaux`.

![sprite tuyaux](images/pipes-sprite.png)

```blocks3
when I start as a clone
+ wait until <>
```

Ensuite, `ajoute 1 à score`{:class="block3variables"} et `joue un son`{:class="block3sound"}.

--- /hint ---

--- hint ---

Utilise ces blocs dans le bon ordre :

![sprite tuyaux](images/pipes-sprite.png)

```blocks3
when I start as a clone
wait until <>

play sound (pop v)

change [score v] by (1)

[x position v] of (Flappy v)

x position

() > ()
```

--- /hint ---

--- hint ---

Ton code devrait ressembler à ceci :

![sprite tuyaux](images/pipes-sprite.png)

```blocks3
when I start as a clone
wait until <([x position v] of (Flappy v)) > (x position)>
change [score v] by (1)
play sound (pop v)
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Teste ton code et assure-toi de marquer un point à chaque fois que Flappy traverse un espace entre les tuyaux. Vérifie si le `score`{:class="block3variables"} est défini sur `0` lorsque tu démarres une nouvelle partie.

--- /task ---
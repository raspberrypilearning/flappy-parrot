## Détecter les collisions

Pour que ce soit un défi, le joueur doit guider Flappy entre les espaces sans laisser le perroquet toucher les tuyaux ou les bords de la scène. Tu dois ajouter des blocs pour détecter quand Flappy touche quelque chose.

C'est ce qu'on appelle la **détection de collision**.

--- task ---

Importe un son à partir de la bibliothèque à utiliser lorsque Flappy entre en collision avec quelque chose. Le son « screech » est un bon choix.

[[[generic-scratch3-sound-from-library]]]

--- /task ---

Un bloc `attendre jusqu'à ce que`{:class="block3control"} est nécessaire pour vérifier si Flappy `touche les tuyaux`{:class="block3sensing"} `ou`{:class="block3operators"} `touche le bord`{:class="block3sensing"}.

--- task ---

Ajoute un nouveau `quand le drapeau vert est cliqué`{:class="block3control"} au sprite « Flappy », et ajoute également le code suivant :

![sprite perroquet](images/flappy-sprite.png)

```blocks3
when green flag clicked
wait until <<touching (Tuyaux v) ?> or <touching (edge v) ?>>
play sound (screech v)
```

--- /task ---

--- task ---

Teste ton code. Si Flappy touche un tuyau, le son « screech » doit être joué.

--- /task ---

Ensuite, mets à jour le code pour que le jeu s'arrête lorsque Flappy touche un tuyau.

--- task ---

Ajoute le code suivant pour arrêter le jeu après la détection d'une collision :

![sprite perroquet](images/flappy-sprite.png)

```blocks3
when green flag clicked
wait until <<touching (Tuyaux v) ?> or <touching (edge v) ?>>
play sound (screech v)
+ say [Partie terminée !]
+ broadcast (Partie terminée v)
+ stop [other scripts in sprite v]
```

L'`envoyer à tous`{:class="block3events"} indique aux autres sprites que la partie est terminée.

Le `stop`{:class="block3control"} arrête les autres scripts « Flappy » en cours d'exécution afin que Flappy arrête de tomber après une collision.

--- /task ---

--- task ---

Enfin, ajoute le code suivant au `Tuyaux` afin qu'ils `s'arrêtent`{:class="block3control"} d'apparaître `quand le sprite reçoit partie terminée`{:class="block3events"}.

![sprite tuyaux](images/pipes-sprite.png)

```blocks3
when I receive [Partie terminée v]
stop [other scripts in sprite v]
```

--- /task ---

--- task ---

Teste ton jeu et vois combien de temps tu peux jouer avant que ce soit « Partie terminée » !

--- /task ---
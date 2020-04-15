## Neem botsingen waar

Om van het spel een uitdaging te maken, moet je Flappy door de gaten leiden zonder dat de papegaai de pijpen of de randen van het speelveld raakt. Je moet enkele blokken toevoegen om waar te nemen wanneer Flappy iets raakt.

Dit wordt **botsing waarneming** genoemd.

--- task ---

Importeer een geluid uit de bibliotheek dat je wilt horen wanneer Flappy ergens tegenaan botst. Het 'screech' geluid is een goede keuze.

[[[generic-scratch3-sound-from-library]]]

--- /task ---

Een `wacht tot`{:class="block3control"} blok is noodzakelijk om te controleren of Flappy `de pijpen raakt`{:class="block3sensing"} `of`{:class="block3operators"} `de rand raakt`{:class="block3sensing"}.

--- task ---

Voeg een nieuw `wanneer op de groene vlag wordt geklikt`{:class="block3control"} blok toe aan de sprite 'Flappy' en voeg ook de volgende code toe:

![papegaai sprite](images/flappy-sprite.png)

```blocks3
when green flag clicked
wait until <<touching (Pijpen v) ?> or <touching (rand v) ?>>
play sound (screech v)
```

--- /task ---

--- task ---

Test je code. Als Flappy een pijp raakt, moet je het 'screech' geluid horen.

--- /task ---

Werk vervolgens de code bij zodat het spel stopt wanneer Flappy een pijp raakt.

--- task ---

Voeg de volgende code toe om het spel te stoppen nadat een botsing is waargenomen:

![papegaai sprite](images/flappy-sprite.png)

```blocks3
when green flag clicked
wait until <<touching (Pijpen v) ?> or <touching (rand v) ?>>
play sound (screech v)
+ say [Game Over!]
+ broadcast (Game Over v)
+ stop [andere scripts in sprite v]
```

Het blok `zend signaal`{:class="block3events"} vertelt andere sprites dat het spel afgelopen is.

Het blok `stop`{:class="block3control"} stopt andere Flappy scripts die worden uitgevoerd, zodat Flappy niet meer valt na een botsing.

--- /task ---

--- task ---

Voeg ten slotte de volgende code toe aan de `Pijpen` sprite zodat pijpen `stoppen`{:class="block3control"} met verschijnen `wanneer de sprite Game Over`{:class="block3events"} ontvangt.

![pijpen sprite](images/pipes-sprite.png)

```blocks3
wanneer ik signaal [game over v] ontvang
stop [andere scripts in sprite v]
```

--- /task ---

--- task ---

Test je game en zie hoe lang je kunt spelen voordat het 'Game over' is!

--- /task ---
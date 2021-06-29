## Laat Flappy vallen

Voeg nu een sprite toe met de naam Flappy en maak code zodat Flappy in het speelveld naar beneden valt. In de volgende stap voeg je de code toe om Flappy te laten vliegen wanneer je op een toets drukt.

\--- no-print \---

![flappy valt animatie](images/flappy-falling.gif)

\--- /no-print \---

\--- task \---

Voeg een nieuwe sprite toe met twee uiterlijken, voor 'vleugels op' en 'vleugels neer', en noem het `Flappy`.

De papegaaiensprite is een goede keuze.

![papegaai sprite](images/flappy-sprite.png)

\--- /task \---

Flappy moet kleiner worden.

\--- task \---

Voeg code toe om `maak grootte 25 %`{:class="block3looks"} uit te voeren `wanneer op de groene vlag wordt geklikt`{:class="block3events"}.

![papegaai sprite](images/flappy-sprite.png)

```blocks3
wanneer op de groene vlag wordt geklikt
maak grootte (25) %
```

\--- /task \---

Wanneer het spel begint, moet Flappy zich net links van het midden van het werkgebied bevinden, op coördinaten `-50, 0`.

![flappy getoond bij de startpositie](images/flappy-starting-position.png)

\--- task \---

Voeg code toe om Flappy naar de `x en y`{:class="block3motion"} startpositie van `x: -50`{:class="block3motion"} en `y: 0`{:class="block3motion "} te laten gaan.

![papegaai sprite](images/flappy-sprite.png)

```blocks3
wanneer op de groene vlag wordt geklikt
maak grootte (25) %
+ ga naar x: (-50) y: (0)
```

[[[generic-scratch3-set-coordinates]]]

\--- /task \---

\--- task \---

Laat Flappy nu `voor altijd`{:class="block3control"} van het speelveld vallen door de `y positie`{:class="block3motion"} van de sprite met -3 te veranderen.

![papegaai sprite](images/flappy-sprite.png)

```blocks3
wanneer op de groene vlag wordt geklikt
maak grootte (25) %
ga naar x: (-50) y: (0)
+ herhaal
    verander y met (-3)
einde
```

\--- /task \---

\--- task \---

Test je code om ervoor te zorgen dat Flappy in het midden van het scherm begint en naar beneden valt. Wanneer je Flappy naar de bovenkant van het speelveld sleept, zou de sprite opnieuw moeten vallen.

\--- /task \---
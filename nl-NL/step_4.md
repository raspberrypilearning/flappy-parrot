## Laat de pijpen bewegen

Vervolgens ga je de pijpen over het scherm laten bewegen om een hindernisbaan te maken.

![pijpen die over het scherm bewegen](images/flappy-clones-test.png)

--- task ---

Laat de pijpen eerst verschijnen door code toe te voegen aan de sprite van Pipes zodat, `wanneer op de groene vlag wordt geklikt`{:class="block3events"}, de sprite `continu`{:class="block3control"} om de twee seconden `een kloon van zichzelf`{:class="block3control"} maakt.

![pijpen sprite](images/pipes-sprite.png)

```blocks3
wanneer op de groene vlag wordt geklikt
maak grootte (200) %
verdwijn
herhaal
  maak een kloon van (mijzelf v)
  wacht (2) sec.
einde
```

**Tip:** klonen zijn slechts kopieën van een sprite en ze zijn erg handig voor het maken van games.

--- /task ---

--- task ---

Breng vervolgens de pijpen in beweging door code toe te voegen zodat, `wanneer een kloon`{:class="block3control"} start, de kloon aan de rechterkant van het werkgebied verschijnt en naar links `schuift`{:class="block3motion"}.

![pijpen sprite](images/pipes-sprite.png)

```blocks3
wanneer ik als kloon start
verschijn
ga naar x: (240) y: (0)
schuif in (4) sec. naar x: (-240) y: (0)
verwijder deze kloon
```

**Tip:** je kunt de pijpen stoppen door op de rode knop **stop** naast de groene vlag te klikken.

--- /task ---

Nu zou je veel pijpen moeten hebben, maar hun gaten zitten altijd op dezelfde plaats.

Je kunt wat variatie toevoegen door een `willekeurig`{:class="block3operators"} getal te gebruiken voor de `y positie`{:class="block3motion"} van de Pipes sprite.

![pijpen op verschillende hoogtes](images/flappy-height-test.png)

--- task ---

Wijzig de code van je sprite zodat elke sprite kloon `een willekeurig nummer kiest van -80 tot 80`{:class="block3operators"} en `verschuift`{:class="block3motion"} naar die `y-positie`{:class="block3motion"}:

![pijpen sprite](images/pipes-sprite.png)

```blocks3
wanneer ik als kloon start
verschijn
+ ga naar x: (240) y: (willekeurig getal tussen (-80) en (80))
+ schuif in (4) sec. naar x: (-240) y: (y-positie)
verwijder deze kloon
```

--- /task ---
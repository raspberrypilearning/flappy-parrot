## Een score toevoegen

De speler moet een punt scoren telkens wanneer Flappy door een opening tussen pijpen komt.

--- task ---

Maak een nieuwe variabele **voor alle sprites** en noem deze `score`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

Elke sprite kloon van 'Pipes' moet `wachten tot`{:class="block3control"} Flappy is voorbijgevlogen en verhoogt dan de `score`{:class="block3variables"}.

--- task ---

Stel score eerst `in op 0`{:class="block3variables"} wanneer het spel begint:

![pijpen sprite](images/pipes-sprite.png)

```blocks3
wanneer op de groene vlag wordt geklikt
+ maak [score v] [0]
maak grootte (200) %
verdwijn
herhaal
  maak een kloon van (mijzelf v)
  wacht (2) sec.
einde
```

--- /task ---

--- task ---

Voeg vervolgens de volgende code toe aan de sprite van `Pijpen`:

![pijpen sprite](images/pipes-sprite.png)

```blocks3
als ik als kloon start
wacht tot <>
```

--- /task ---

--- task ---

Voeg meer code toe zodat, wanneer Flappy's `x` positie groter is dan de `x` positie van de pijpenkloon, de `score`{:class="block3variables"} met `1` toeneemt en een geluid naar keuze wordt afgespeeld.

Je kunt het 'pop'-geluid gebruiken als je wilt, of een geluid uit de bibliotheek toevoegen, bijvoorbeeld 'vogel'.

--- hints ---


--- hint ---

Je moet `wachten tot`{:class="block3control"} `Flappy's x positie`{:class="block3sensing"} `groter is dan (>)`{:class="block3operators"} de `x positie`{:class="block3motion"} van `Pijpen`.

![pijpen sprite](images/pipes-sprite.png)

```blocks3
wanneer ik als kloon start
+ wacht tot <>
```

Verander dan `de score met 1`{:class="block3variables"} en speel `een geluid`{:class="block3sound"} af.

--- /hint ---

--- hint ---

Gebruik deze blokken in de juiste volgorde:

![pijpen sprite](images/pipes-sprite.png)

```blocks3
wanneer ik als kloon start
wacht tot <>

start geluid (pop v)

verander [score v] met (1)

[x positie v] van (Flappy v)

x positie

() > ()
```

--- /hint ---

--- hint ---

Je code zou er als volgt uit moeten zien:

![pijpen sprite](images/pipes-sprite.png)

```blocks3
wanneer ik als kloon start
wacht tot <([x positie v] van (Flappy v)) > (x positie)>
verander [score v] met (1)
start geluid (pop v)
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Test je code en zorg ervoor dat je een punt scoort telkens wanneer Flappy door een opening tussen pijpen komt. Controleer of `score`{:class="block3variables"} is ingesteld op `0` wanneer je een nieuw spel start.

--- /task ---
## Detectar colisiones

Para que el juego sea un desafío, el jugador debe guiar a Plumita a través de los espacios sin dejar que el papagayo toque las tuberías o los bordes del escenario. Necesitas añadir algunos bloques para detectar cuando Plumita golpea algo.

A esto se le llama **detectar colisión**.

--- task ---

Importa un sonido, desde la biblioteca, que quieras reproducir cuando Plumita choca con algo. El sonido «bird» es una buena opción.

[[[generic-scratch3-sound-from-library]]]

--- /task ---

Se necesita un bloque `esperar hasta que`{:class="block3control"} para comprobar si Plumita `tocando las tuberías`{:class="block3sensing"} `o`{:class="block3operators"} `tocando el borde`{:class="block3sensing"}.

--- task ---

Añade un nuevo bloque `al presionar la bandera verde`{:class="block3control"} al objeto «Plumita» y también añade el siguiente código:

![objeto papagayo](images/flappy-sprite.png)

```blocks3
when green flag clicked
wait until <<touching (Tuberías v) ?> or <touching (edge v) ?>>
play sound (screech v)
```

--- /task ---

--- task ---

Prueba tu código. Si Plumita toca una tubería, debe reproducirse el sonido «bird».

--- /task ---

A continuación, actualiza el código para que el juego se detenga cuando Plumita golpee una tubería.

--- task ---

Añade el siguiente código para detener el juego después de detectar una colisión:

![objeto papagayo](images/flappy-sprite.png)

```blocks3
when green flag clicked
wait until <<touching (Tuberías v) ?> or <touching (edge v) ?>>
play sound (screech v)
+ say [¡Fin del Juego!]
+ broadcast (fin del juego v)
+ stop [other scripts in sprite v]
```

El bloque `enviar`{:class="block3events"} indica a otros objetos que el juego ha terminado.

El bloque `detener`{:class="block3control"} para a otros objetos de Plumita, que se están ejecutando, para que deje de caer después de una colisión.

--- /task ---

--- task ---

Al final, añade el siguiente código al objeto `Tuberías` para que las tuberías reciban el comando `detener`{:class="block3control"} su aparición `cuando el objeto recibe fin del juego`{:class="block3events"}.

![objeto Tuberías](images/pipes-sprite.png)

```blocks3
when I receive [fin del juego v]
stop [other scripts in sprite v]
```

--- /task ---

--- task ---

¡Prueba tu juego y mira cuánto tiempo puedes jugar antes de que termine el juego!

--- /task ---
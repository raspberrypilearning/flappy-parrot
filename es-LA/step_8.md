## Añade un puntaje

Quien juega debe sumar un punto cada vez que Plumita atraviesa un espacio entre tuberías.

--- task ---

Crea una nueva variable **para todos los objetos** y dale el nombre de `puntaje`{:class="block3variables"}.

[[[generic-scratch3-add-variable]]]

--- /task ---

Cada clon de objetos 'Tubería' debería `esperar hasta`{:class="block3control"} que Plumita haya pasado y luego que aumente el `puntaje`{:class="block3variables"}.

--- task ---

Primero, cuando comienza el juego `establece el puntaje en 0`{: class="block3variables"}:

![objeto Tuberías](images/pipes-sprite.png)

```blocks3
when green flag clicked
+ set [puntaje v] to [0]
set size to (200) %
hide
forever 
  create clone of (myself v)
  wait (2) seconds
end
```

--- /task ---

--- task ---

Luego añade el siguiente código al objeto `Tuberías`:

![objeto Tuberías](images/pipes-sprite.png)

```blocks3
when I start as a clone
wait until <>
```

--- /task ---

--- task ---

Añade más código para que cuando la posición `x` de Plumita sea mayor que la posición del clon de la tubería `x`, el `puntaje`{:class="block3variables"} aumente `1` y se reproduzca un sonido de tu elección.

Podrías usar el sonido «pop» si quieres o añadir un sonido de la biblioteca, por ejemplo «bird».

--- hints ---


--- hint ---

Necesitas `esperar hasta que`{:class="block3control"} `la posición x de Plumita`{:class="block3sensing"} sea `mayor a (>)`{:class="block3operators"} la posición `x`{:class="block3motion"} de `Tuberías`.

![objeto Tuberías](images/pipes-sprite.png)

```blocks3
when I start as a clone
+ wait until <>
```

Luego `cambia la puntuación en 1`{:class="block3variables"} y `reproduce un sonido`{:class="block3sound"}.

--- /hint ---

--- hint ---

Usa estos bloques en el orden correcto:

![objeto Tuberías](images/pipes-sprite.png)

```blocks3
when I start as a clone
wait until <>

play sound (pop v)

change [puntaje v] by (1)

[x position v] of (Plumita v)

x position

() > ()
```

--- /hint ---

--- hint ---

Tu código debería verse así:

![objeto Tuberías](images/pipes-sprite.png)

```blocks3
when I start as a clone
wait until <([x position v] of (Plumita v)) > (x position)>
change [puntaje v] by (1)
play sound (pop v)
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Prueba tu código y asegúrate de marcar un punto cada vez que Plumita pasa por un espacio entre las tuberías. Comprueba que el `puntaje`{:class="block3variables"} esté fijado en `0` cuando comiences un nuevo juego.

--- /task ---
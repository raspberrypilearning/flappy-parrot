## Haz que Plumita se caiga

Ahora añade un objeto que se llame Plumita y crea un código para que Plumita caiga por el escenario hacia abajo. En el siguiente paso, añadirás el código que haga volar a Plumita al pulsar una tecla.

\--- no-print \---

![animación de Plumita cayendo](images/flappy-falling.gif)

\--- /no-print \---

\--- task \---

Añade un nuevo objeto que tenga dos disfraces, para 'alas arriba' y 'alas abajo', luego dale el nombre de `Plumita`.

El objeto papagayo es una buena opción.

![objeto papagayo](images/flappy-sprite.png)

\--- /task \---

Plumita tiene que ser más pequeño.

\--- task \---

Agrega código a `establecer el tamaño de Plumita en 25%`{:class="block3looks"}`cuando se hace clic en la bandera verde`{:class="block3events"}.

![objeto papagayo](images/flappy-sprite.png)

```blocks3
al presionar la bandera verde
fijar tamaño a (25) %
```

\--- /task \---

Cuando comienza el juego, Plumita debe estar a la izquierda del centro del escenario, en las coordenadas `-50, 0`.

![Se ve a Plumita en la posición de inicio](images/flappy-starting-position.png)

\--- task \---

Añade código para hacer que Plumita `vaya a x e y`{:class="block3motion"} en la posición inicial de `x: -50`{:class="block3motion"} e `y: 0`{:class="block3motion"}.

![objeto papagayo](images/flappy-sprite.png)

```blocks3
when green flag clicked
set size to (25) %
+ go to x: (-50) y: (0)
```

[[[generic-scratch3-set-coordinates]]]

\--- /task \---

\--- task \---

Ahora haz que Plumita siga cayendo por el escenario `por siempre`{:class="block3control"}`al cambiar la posición y del objeto a -3`{:class="block3motion"}.

![objeto papagayo](images/flappy-sprite.png)

```blocks3
al presionar la bandera verde
fijar tamaño a (25) %
+ ir a x: (-50) y: (0)
+ por siempre 
    cambiar y en (-3)
fin
```

\--- /task \---

\--- task \---

Prueba tu código para asegurarte de que Plumita comienza en el centro de la pantalla y cae hasta el fondo. Cuando arrastras a Plumita hasta la parte superior del escenario, el objeto debería caer de nuevo.

\--- /task \---
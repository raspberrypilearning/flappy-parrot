## Haz que las tuberías se muevan

Luego vas a hacer que las tuberías se muevan a través de la pantalla para crear un rumbo con obstáculos.

![las tuberías se mueven por la pantalla](images/flappy-clones-test.png)

\--- task \---

Primero haz que las tuberías aparezcan, para ello añade código al objeto Tuberías, así, `cuando se haga clic en la bandera verde`{:class="block3events"}, el objeto `para siempre`{:class="block3control"} `creará un clon de sí mismo`{:class="block3control"} cada dos segundos.

![objeto Tuberías](images/pipes-sprite.png)

```blocks3
al presionar la bandera verde
fijar tamaño a (200) %
ocultar
por siempre 
  crear clon de (mí mismo v)
  esperar (2) segundos
fin
```

**Consejo:** los clones son sólo copias de un objeto y son muy útiles para crear juegos.

\--- /task \---

\--- task \---

Luego, haz que las tuberías se muevan al agregar un código, para que `cuando comience un clon` {: class = "block3control"}, aparezca en el lado derecho del escenario y `se deslice` {: class = "block3motion"} hacia la izquierda.

![objeto Tuberías](images/pipes-sprite.png)

```blocks3
Al comenzar como clon
mostrar
ir a x: (240) y: (0)
deslizar en (4) segs a x: (-240) y: (0)
eliminar este clon
```

**Consejo:** puedes parar el desplazamiento de las tuberías al hacer clic en el botón rojo **detener** junto a la bandera verde.

\--- /task \---

Ahora deberías tener muchas tuberías, pero los espacios están siempre en el mismo lugar.

Puedes añadir algo de variedad al usar un número `aleatorio`{:class="block3operators"} para la `posición en y<0> del objeto Tuberías{:class="block3motion"}.</p>

<p><img src="images/flappy-height-test.png" alt="las tuberías en diferentes alturas" /></p>

<p>--- task ---</p>

<p>Modifica el código de tu objeto para que cada clon de objetos <code>elija un número aleatorio de -80 a 80`{:class="block3operators"} y `deslizamientos`{:class="block3motion"} a la `posición en y`{:class="block3motion"}:

![objeto Tuberías](images/pipes-sprite.png)

```blocks3
Al comenzar como clon
mostrar
+ ir a x: (240) y: (número al azar entre (-80) y (80))
+ deslizar en (4) segs a x: (-240) y: (posición en y)
eliminar este clon
```

\--- /task \---
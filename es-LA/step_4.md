## Haz que las tuberías se muevan

Luego vas a hacer que las tuberías se muevan a través de la pantalla para crear un rumbo con obstáculos.

![las tuberías se mueven por la pantalla](images/flappy-clones-test.png)

--- task ---

Primero haz que las tuberías aparezcan, para ello añade código al objeto Tuberías, así, `cuando se haga clic en la bandera verde`{:class="block3events"}, el objeto `para siempre`{:class="block3control"} `creará un clon de sí mismo`{:class="block3control"} cada dos segundos.

![objeto Tuberías](images/pipes-sprite.png)

```blocks3
when green flag clicked
set size to (200) %
hide
forever 
  create clone of (myself v)
  wait (2) seconds
end
```

**Consejo:** los clones son sólo copias de un objeto y son muy útiles para crear juegos.

--- /task ---

--- task ---

Luego, haz que las tuberías se muevan al agregar un código, para que `cuando comience un clon`{:class="block3control"}, aparezca en el lado derecho del escenario y `se deslice`{:class="block3motion"} hacia la izquierda.

![objeto Tuberías](images/pipes-sprite.png)

```blocks3
when I start as a clone
show
go to x: (240) y: (0)
glide (4) secs to x: (-240) y: (0)
delete this clone
```

**Consejo:** puedes parar el desplazamiento de las tuberías al hacer clic en el botón rojo **detener** junto a la bandera verde.

--- /task ---

Ahora deberías tener muchas tuberías, pero los espacios están siempre en el mismo lugar.

Puedes añadir algo de variedad al usar un número `aleatorio`{:class="block3operators"} para la `posición en y<0> del objeto Tuberías{:class="block3motion"}.

![las tuberías en diferentes alturas](images/flappy-height-test.png)

--- task ---

Modifica el código de tu objeto para que cada clon de objetos `elija un número aleatorio de -80 a 80`{:class="block3operators"} y `deslizamientos`{:class="block3motion"} a la `posición en y`{:class="block3motion"}:

![objeto Tuberías](images/pipes-sprite.png)

```blocks3
when I start as a clone
show
+ go to x: (240) y: (pick random (-80) to (80))
+ glide (4) secs to x: (-240) y: (y position)
delete this clone
```

--- /task ---
## Сделай Flappy падающим

Теперь добавь спрайт под названием Flappy и создайте код так, чтобы Flappy падал на Сцене. На следующем шаге ты добавишь код, чтобы Flappy взлетал при нажатии клавиши.

--- no-print ---

![анимация падающего Flappy](images/flappy-falling.gif)

--- /no-print ---

--- task ---

Добавь новый спрайт, который имеет два костюма, 'крылья вверх' и 'крылья вниз', и назови его `Flappy`.

Спрайт попугай - это хороший выбор.

![спрайт попугая](images/flappy-sprite.png)

--- /task ---

Flappy должен быть поменьше.

--- task ---

Добавь код в `установить размер Flappy 25%`{:class="block3looks"} `когда зеленый флаг нажат`{:class="block3events"}.

![спрайт попугая](images/flappy-sprite.png)

```blocks3
when green flag clicked
set size to (25) %
```

--- /task ---

Когда игра начинается, Flappy нужно быть просто чуть левее от центра Сцены, с координатами `-50, 0`.

![flappy, показан в стартовой позиции](images/flappy-starting-position.png)

--- task ---

Добавь код, чтобы Flappy `перешёл к x и y`{:class="block3motion"} с начальной позицией `x: -50`{:class="block3motion"} и `y: 0`{:class="block3motion"}.

![спрайт попугая](images/flappy-sprite.png)

```blocks3
when green flag clicked
set size to (25) %
+ go to x: (-50) y: (0)
```

[[[generic-scratch3-set-coordinates]]]

--- /task ---

--- task ---

Теперь сделай так, чтобы Flappy всегда падал вниз Сцены с помощью `повторять всегда`{:class="block3control"}`, изменяя позицию спрайта по y на -3`{:class="block3motion"}.

![спрайт попугая](images/flappy-sprite.png)

```blocks3
when green flag clicked
set size to (25) %
go to x: (-50) y: (0)
+ forever 
    change y by (-3)
end
```

--- /task ---

--- task ---

Проверь свой код, чтобы убедиться, что Flappy стартует в середине экрана и падает вниз. Когда ты перетащишь Flappy на верхнюю часть Сцены, спрайт должен снова упасть.

--- /task ---
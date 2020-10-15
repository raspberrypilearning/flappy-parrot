## Заставь трубы двигаться

Далее ты сделаешь так, чтобы трубы двигались по экрану, это создаст полосу препятствий.

![трубы движутся по экрану](images/flappy-clones-test.png)

--- task ---

Первым делом сделай так, чтобы трубы появились, добавь код к спрайту Трубы таким образом, что `когда зелёный флаг нажат`{:class="block3events"}, спрайт `повторять всегда`{:class="block3control"} `создает клон самого себя`{:class="block3control"} каждые две секунды.

![спрайт трубы](images/pipes-sprite.png)

```blocks3
when green flag clicked
set size to (200) %
hide
forever 
  create clone of (myself v)
  wait (2) seconds
end
```

**Совет:** клоны - это просто копии спрайта, и они очень полезны при создании игр.

--- /task ---

--- task ---

Далее заставь трубы двигаться, добавь код так, что `когда клон начинает`{:class="block3control"}, клон появился в правой части Сцены и `скользит`{:class="block3motion"} влево.

![спрайт трубы](images/pipes-sprite.png)

```blocks3
when I start as a clone
show
go to x: (240) y: (0)
glide (4) secs to x: (-240) y: (0)
delete this clone
```

**Совет:** Ты можешь остановить движение труб, нажав на красную кнопку **остановить** рядом с зеленым флагом.

--- /task ---

Теперь у тебя должно быть много труб, но их щели всегда находятся на одном и том же месте.

Ты можешь добавить немного разнообразия, используя `случайное`{:class="block3operators"} значение для `позиции y`{:class="block3motion"} спрайта Трубы.

![трубы на разных высотах](images/flappy-height-test.png)

--- task ---

Измени код спрайта, чтобы каждый его клон `выбирал случайное число от -80 до 80`{:class="block3operators"} и `скользил`{:class="block3motion"} к его `положению по y`{:class="block3motion"}:

![спрайт трубы](images/pipes-sprite.png)

```blocks3
when I start as a clone
show
+ go to x: (240) y: (pick random (-80) to (80))
+ glide (4) secs to x: (-240) y: (y position)
delete this clone
```

--- /task ---
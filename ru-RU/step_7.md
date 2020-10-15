## Обнаружение столкновений

Чтобы сделать игру сложной, игрок должен провести Flappy через щели, не позволяя попугаю касаться труб или краев Сцены. Тебе нужно добавить несколько блоков, чтобы определить, когда Flappy обо что-то ударится.

Это называется **обнаружением столкновений**.

--- task ---

Загрузи звук из библиотеки, который ты хочешь воспроизвести, когда Flappy сталкивается с чем-либо. Звук «screech (визг)» - хороший выбор.

[[[generic-scratch3-sound-from-library]]]

--- /task ---

Блок `ждать до`{:class="block3control"} необходим для проверки того, что Flappy `касается труб`{:class="block3sensing"} `или`{:class="block3operators"} `касается края`{:class="block3sensing"}.

--- task ---

Добавь новый блок `когда зелёный флаг нажат`{:class="block3control"} в спрайт 'Flappy', а также добавь следующий код:

![спрайт попугая](images/flappy-sprite.png)

```blocks3
when green flag clicked
wait until <<touching (Трубы v) ?> or <touching (edge v) ?>>
play sound (screech v)
```

--- /task ---

--- task ---

Проверь свою программу. Если Flappy касается трубы, должен прозвучать звук «визг».

--- /task ---

Далее, обнови код, чтобы игра остановилась, когда Flappy ударится о трубу.

--- task ---

Добавь следующий код, чтобы остановить игру после того, как столкновение произошло:

![спрайт попугая](images/flappy-sprite.png)

```blocks3
when green flag clicked
wait until <<touching (Pipes v) ?> or <touching (edge v) ?>>
play sound (screech v)
+ say [Игра окончена!]
+ broadcast (Игра окончена v)
+ stop [other scripts in sprite v]
```

Блок `передать`{:class="block3events"} говорит другим спрайтам, что игра закончена.

Блок `стоп`{:class="block3control"} останавливает другие запущенные скрипты Flappy, поэтому Flappy перестает падать после столкновения.

--- /task ---

--- task ---

Наконец, добавь следующий код в спрайт `Трубы`, чтобы трубы `перестали`{:class="block3control"} появляться `когда спрайт получит Игра окончена`{:class="block3events"}.

![спрайт труб](images/pipes-sprite.png)

```blocks3
when I receive [Игра окончена v]
stop [other scripts in sprite v]
```

--- /task ---

--- task ---

Протестируй свою игру и посмотри, как долго ты сможешь продержаться!

--- /task ---
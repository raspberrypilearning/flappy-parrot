## Сделай Flappy летающим

Теперь ты сделаешь, так что Flappy будет махать крыльями и лететь вверх, при нажатии клавиши <kbd>Пробел</kbd>. Когда ты играешь в игру, тебе нужно рассчитывать время нажатий так, чтобы у Flappy получалось пролетать между трубами.

--- no-print ---

![flappy летит вверх, когда клавиша пробел нажата](images/flappy-flying.gif)

--- /no-print ---

Заставь Flappy лететь вверх, когда ты нажимаешь на клавишу <kbd>пробел</kbd>.

--- task ---

Когда `клавиша пробел нажата`{:class="block3events"}, Flappy должен двигаться вверх, `изменяя свою координату y`{:class="block3motion"} на небольшое значение, например `6`.

Flappy летит вверх, `повторяя`{:class="block3control"} это движение `10 раз`{:class="block3control"}.

Добавь этот код в свой спрайт `Flappy`:

![спрайт попугая](images/flappy-sprite.png)

```blocks3
when [space v] key pressed
repeat (10) 
  change y by (6)
end
```

--- /task ---

Теперь тебе нужно сделать так, чтобы Flappy махал крыльями!

--- task ---

Нажми на вкладку **Костюмы** и назови костюмы Flappy 'крылья вверх' и 'крылья вниз'.

![переименование костюмов](images/flappy-wings.png)

--- /task ---

--- task ---

Можешь ли ты сделать смену костюма Flappy на `крылья вниз` при нажатии <kbd>пробела</kbd>, и затем снова изменить его на `крылья вверх` на полпути движения вверх?

--- hints ---


--- hint ---

Тебе нужно разделить движение вверх пополам, чтобы можно было использовать два блока `повторить`{:class="block3control"}, чтобы изменять костюм Flappy в начале и в середине движения.

Добавь блоки`переключить костюм на`{:class="block3looks"}, чтобы изменить внешний вид Flappy.

--- /hint --- --- hint ---

Тебе нужно использовать эти блоки:

![спрайт попугая](images/flappy-sprite.png)

```blocks3
repeat (5) 
  change y by (6)
end

repeat (5) 
  change y by (6)
end

switch costume to (крылья вверх v)

switch costume to (крылья вниз v)

when [space v] key pressed
```

--- /hint ---

--- hint ---

Твой код должен выглядеть так:

![спрайт попугая](images/flappy-sprite.png)

```blocks3
when [space v] key pressed
switch costume to (крылья вниз v)
repeat (5) 
  change y by (6)
end
switch costume to (крылья вверх v)
repeat (5) 
  change y by (6)
end
```

--- /hint ---

--- /hints ---

--- /task ---

--- task ---

Проверь свою программу. Как ты видишь, пока что ничего не происходит, когда Flappy ударяется об трубу.

--- /task ---
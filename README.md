# NEOfighter: branch *«[Feature/Start_scene](https://github.com/kenyako/NEOfighter/tree/Feature/Start_scene)»*

## Глобальные переменные
* **size** – храниит длину и ширину окна
* **COLORS** – словарь, содержащий в себе все цвета на сцене
* **FONT** – шрифт, который используется на сцене
* **alreadyPressed** – переменная, которая хранит последнее состоянии кнопки.

**Нажатие ЛКМ -> `alreadyPressed = True` -> Отжатие ЛКМ -> Выполнение нужного алгоритма -> `alreadyPressed = False`**

## Class *Button*
Класс кнопки (как бы очевидно это не звучало).
Содержит __init()__, определяющий *длину, ширину, базовый увет и цвет при наведении.*
Функция *draw()*, во-первых, **отрисовывает** кнопку, во-вторых, **обрабатывает наведение** и **нажатие** на неё.
Также по ключу *function* можно задать функцию, которая будет выполняться при нажатии на кнопку.

## Func *end_screen(screen, text_on_screen)*
Функция, отрисовывающая конечный экран, на котором содержится текст *text_on_screen* и кнопка.
Текст внутри кнопки располагается **строго посередине** кнопки!
***Свойства кнопки задаются отдельно внутри функции посредством изменения параметров инициализации экземпляра класса Button***

## Менеджер сцен
По ключу **currency_screen** в файле *settings.json* хранится название текущей сцены.
В зависимости от значения в дальнейшем условии в главном цикле (`if currency_screen == "start":...`) отрисовывается определённая сцена.
Значение переменной изменяет **загрузчик**(loader) сцены: это функция, название которой состоит из *название_сцены*_loader(). Она изменяет значение по ключу **currency_screen** в JSON-файле.
После изменения значения **currency_screen** соответственно изменяется отрисовываемая сцена.

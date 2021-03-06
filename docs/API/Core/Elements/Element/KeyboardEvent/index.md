---
layout: doc
title: "KeyboardEvent"
position: 1006
---

Событие от клавиатуры.

# Syntax

```js
new KeyboardEvent()
```

# Properties

## `source`

Источник события - [визуальный элемент](../).

## `key`

Возвращает код нажатой клавиши.

## `altKey`

Возвращает `true`, если событие произошло, когда была нажата кнопка `Alt`, иначе - `false`.

## `ctrlKey`

Возвращает `true`, если событие произошло, когда была нажата кнопка `Ctrl`, иначе - `false`.

## `shiftKey`

Возвращает `true`, если событие произошло, когда была нажата кнопка `Shift`, иначе - `false`.

## `nativeEventData`

Возвращает KeyboardEvent Object.
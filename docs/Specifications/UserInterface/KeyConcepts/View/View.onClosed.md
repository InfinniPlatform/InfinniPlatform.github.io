---
layout: doc
title: "View.onClosed"
position: 103
---

Устанавливает [обработчик события](../../Script/) о том, что представление закрыто.

# Description

Вызов метода [`close()`](../View.close/) приводит к возникновению события [`onClosing`](../View.onClosing/).
Представление будет закрыто, если нет ни одного обработчика, подписанного на событие [`onClosing`](../View.onClosing/),
либо если все обработчики этого события вернули значение, отличное от `false`. Закрытие представления
приводит к возникновению события [`onClosed`](../View.onClosed/). В обработчике события [`onClosed`](../View.onClosed/)
можно зарегистрировать факт закрытия представления.

# Syntax

```js
View.onClosed(callback)
```

## Parameters

`callback`

[Обработчик события](../../Script/) о том, что представление закрыто.

# Examples

```js
Session.onClosed(
  function(context, argument) { alert('View is closed!'); }
);
```
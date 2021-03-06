---
layout: doc
title: "View.onClosed"
position: 103
---

Устанавливает [обработчик события](../../../Script/) о том, что представление было закрыто.

# Description

Вызов метода [`close()`](../View.close/) приводит к возникновению события [`onClosing`](../View.onClosing/).
Представление будет закрыто, если нет ни одного обработчика, подписанного на событие [`onClosing`](../View.onClosing/),
либо если все обработчики этого события вернули значение, отличное от `false`. Закрытие представления
приводит к возникновению события `onClosed`. В обработчике события `onClosed`
можно зарегистрировать факт закрытия представления.

# Syntax

```js
view.onClosed(callback)
```

## Parameters

|Name|Type|Description|
|----|----|-----------|
|`callback`|[`Script`](../../../Script/)|Обработчик события о том, что представление было закрыто|

# Examples

```js
view.onClosed(
  function(context, argument) { alert('View is closed!'); }
);
```

# See Also

* [`close()`](../View.close/)
* [`onClosing`](../View.onClosing/)

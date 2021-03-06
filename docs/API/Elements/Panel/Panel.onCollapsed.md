---
layout: doc
title: "Panel.onCollapsed"
position: 103
---

Устанавливает [обработчик события](../../../Core/Script/) о том, что панель была свернута.

# Description

Если панель была развернута и ее [можно свернуть](../Panel.getCollapsible/), вызов метод [`setCollapsed()`](../Panel.setCollapsed/)
с параметром `true` означает необходимость свернуть панель. В этом случае возникает событие [`onCollapsing`](../Panel.onCollapsing/).
В итоге панель будет свернута, если нет ни одного обработчика, подписанного на событие [`onCollapsing`](../Panel.onCollapsing/),
либо если все обработчики этого события вернули значение, отличное от `false`. Если панель в конечном счете была свернута,
возникает событие [`onCollapsed`](../Panel.onCollapsed/). В обработчике события [`onCollapsed`](../Panel.onCollapsed/)
можно зарегистрировать факт того, что панель была свернута.

# Syntax

```js
panel.onCollapsed(callback)
```

## Parameters

|Name|Type|Description|
|----|----|-----------|
|callback|[`Script`](../../../Core/Script/)|Обработчик события о том, что панель была свернута|

## Returns

Метод ничего не возвращает

# Examples

```js
panel.setCollapsible(true);
panel.setCollapsed(false);

panel.onCollapsed(
  function(context, argument) { alert('Panel is collapsed!'); }
);

panel.setCollapsed(true);
```

# See Also

* [`setCollapsed()`](../Panel.setCollapsed/)
* [`onCollapsing`](../Panel.onCollapsing/)

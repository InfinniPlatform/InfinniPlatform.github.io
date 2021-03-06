---
layout: doc
title: "Panel.getCollapsed()"
position: 3
---

Возвращает значение, определяющее, свернута ли панель.

# Description

Вызов метода [`setCollapsible()`](../Panel.setCollapsible/) управляет возможностью сворачивания
панели. Если сворачивание запрещено, панель нельзя свернуть ни визуально, ни программно - с помощью
метода [`setCollapsed()`](../Panel.setCollapsed/). Если сворачивание было запрещено в то время, как
панель была свернута, панель разворачивается автоматически.

# Syntax

```js
panel.getCollapsed()
```

## Parameters

Нет

## Returns

Логическое значение, определяющее, свернута ли панель.  
Значение `false` говорит о том, что панель развернута (значение по умолчанию),  
значение `true` - свернута.

# Examples

```js
var isCollapsed = panel.getCollapsed();
```

# See Also

* [`setCollapsed()`](../Panel.setCollapsed/)
* [`getCollapsible()`](../Panel.getCollapsible/)
* [`setCollapsible()`](../Panel.setCollapsible/)

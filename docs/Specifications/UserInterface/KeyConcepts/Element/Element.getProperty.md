---
layout: doc
title: "Element.getProperty()"
position: 15
---

Возвращает значение указанного свойства элемента.

# Description

Методы [`getProperty()`](../Element.getProperty/), [`setProperty()`](../Element.setProperty/)
и событие [`onPropertyChanged`](../Element.onPropertyChanged/) используются механизмом
[привязки данных](../../../DataBinding/). Вместе с этим они предоставляют универсальный
унифицированный интерфейс для работы со свойствами элемента.

# Syntax

```js
Element.getProperty(property)
```

## Parameters

`property`

Путь к свойству.

## Returns

Значение свойства.

# Examples

```js
var value = Element.getProperty('Visible'); // Element.getVisible();
```

# See Also

* [`setProperty()`](../Element.setProperty/)
* [`onPropertyChanged`](../Element.onPropertyChanged/)
* [`DataBinding`](../../../DataBinding/)
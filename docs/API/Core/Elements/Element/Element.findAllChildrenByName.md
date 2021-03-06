---
layout: doc
title: "Element.findAllChildrenByName()"
position: 12.2
---

Возвращает список потомков (дочерних, их дочерних и т. д.) элементов с заданным именем.

# Description

Метод возвращает список [элементов](../) с заданным именем, которые являются потомками данного элемента или его потомков.
Иначе говоря, в результирующий список будут включены элементы с заданным именем со всех уровней вложенности (прямые потомки, 
их дочерние элементы и т.д.).

# Syntax

```js
Element.findAllChildrenByName(name)
```

## Parameters

|Name|Type|Description|
|----|----|-----------|
|value|`String`|Наименование элемента|

## Returns

Массив [элементов](../) с заданным именем, которые являются потомками данного элемента.

# Examples

```js
var allMyButtons = Element.findAllChildrenByName('MyButton');
```

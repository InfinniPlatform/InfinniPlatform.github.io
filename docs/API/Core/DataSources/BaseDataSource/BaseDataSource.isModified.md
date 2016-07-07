---
layout: doc
title: "BaseDataSource.isModified()"
position: 27
---

Проверяет, является ли элемент несохраненным.

# Syntax

```js
BaseDataSource.isModified(item)
```

## Parameters

|Name|Description|
|----|-----------|
|item|(Необязательный) Элемент источника данных. Если указан, на наличие изменений проверяется только
указанный элемент; если не указан, на наличие изменений проверяются все элементы|

## Returns

Возвращает `true`, если элемент был изменен, иначе возвращает `false`.

# Examples

```js
var selectedItem = BaseDataSource.getSelectedItem();
var selectedIsModified = BaseDataSource.isModified(selectedItem);
```

# See Also

* [`isModifiedItems()`](../BaseDataSource.isModifiedItems/)
* [`saveItem()`](../BaseDataSource.saveItem/)
* [`updateItems()`](../BaseDataSource.updateItems/)
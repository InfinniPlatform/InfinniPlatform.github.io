---
layout: doc
title: "BaseDataSource.suspendUpdate()"
position: 5
---

Запрещает обновление списка элементов.

# Syntax

```js
BaseDataSource.suspendUpdate(value)
```
## Parameters

|Name|Description|
|----|-----------|
|value|Причина запрета на обновление|

## Returns

Метод ничего не возвращает

# Examples

```js
BaseDataSource.suspendUpdate('updateParamsNotReady');
```

# See Also

* [`resumeUpdate()`](../BaseDataSource.resumeUpdate/)
* [`isUpdateSuspended()`](../BaseDataSource.isUpdateSuspended/)
* [`setFilter()`](../BaseDataSource.setFilter/)
* [`updateItems()`](../BaseDataSource.updateItems/)

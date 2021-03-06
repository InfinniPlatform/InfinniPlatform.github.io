---
layout: doc
title: "BaseDataSource.saveItem()"
position: 13
---

Сохраняет элемент в источнике данных.

# Description

Вызов метода [`saveItem()`](../BaseDataSource.saveItem/) производит сохранение всех изменений
указанного элемента в соответствующем источнику данных хранилище. Сохранение производится только
в том случае, если указанный элемент не содержит ошибок,
в противном случае возникает событие [`onErrorValidator`](../BaseDataSource.onErrorValidator/).
Успешное сохранение элемента приводит к возникновению события [`onItemSaved`](../BaseDataSource.onItemSaved/).

# Syntax

```js
BaseDataSource.saveItem(item, success, error)
```

## Parameters

|Name|Description|
|----|-----------|
|item<sup>*</sup>|Элемент источника данных|
|success|[Обработчик события](../../../Script/) о том, что элемент сохранен. Параметр `args` данного обработчика содержит поля: item - сохраненный элемент, validationResult - [результат валидации](../ValidationResult/) (чтобы данное поле было заполнено, запрашиваемый сервис должен реализовать интерфейс [`IDocumentStorageInterceptor`](http://infinniplatform.readthedocs.io/api/reference/InfinniPlatform.Sdk.Documents.Interceptors.IDocumentStorageInterceptor.html)), originalResponse - ответ сервера|
|error|[Обработчик события](../../../Script/) о том, что при сохранении элемента произошла ошибка. Параметр args данного обработчика содержит поля: item - сохраняемый элемент, validationResult - [результат валидации](../ValidationResult/) (чтобы данное поле было заполнено, запрашиваемый сервис должен реализовать интерфейс [`IDocumentStorageInterceptor`](http://infinniplatform.readthedocs.io/api/reference/InfinniPlatform.Sdk.Documents.Interceptors.IDocumentStorageInterceptor.html)), originalResponse - ответ сервера|

<sup>*</sup> Обязательный аргумент.

## Returns

Метод ничего не возвращает.

# Examples

```js
var items = BaseDataSource.getItems();
BaseDataSource.saveItem(items[0]);
```

# See Also

* [`onItemSaved`](../BaseDataSource.onItemSaved/)
* [`onErrorValidator`](../BaseDataSource.onErrorValidator/)
* [`createItem()`](../BaseDataSource.createItem/)
* [`deleteItem()`](../BaseDataSource.deleteItem/)
* [`getValidationResult()`](../BaseDataSource.getValidationResult/)

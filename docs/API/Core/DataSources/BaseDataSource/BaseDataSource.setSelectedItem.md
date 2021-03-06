---
layout: doc
title: "BaseDataSource.setSelectedItem()"
position: 16
---

Устанавливает выделенный элемент.

# Description

В каждый момент времени пользователь может работать только с одним элементом - выделенным элементом.
Зачастую это элемент, на котором установлен фокус ввода. Например, редактируемый элемент, выбранный
элемент в списке и т.д. Источник данных хранит информацию о выделенном элементе, благодаря чему
имеется возможность определять элемент данных, с которым работает пользователь. Изменение выделенного
элемента приводит к возникновению события [`onSelectedItemChanged`](../BaseDataSource.onSelectedItemChanged/).

# Syntax

```js
BaseDataSource.setSelectedItem(item, success, error)
```

## Parameters

|Name|Description|
|----|-----------|
|item<sup>*</sup>|Элемент источника данных|
|success|[Обработчик события](../../../Script/) о том, что выделенный элемент изменился. Параметр args данного обработчика содержит поле source, в котором хранится ссылка на [источник данных](../) |
|error|[Обработчик события](../../../Script/) о том, что при изменении выделенного элемента произошла ошибка. Параметр args данного обработчика содержит поле  error, хранящее сообщение об ошибке|

<sup>*</sup> Обязательный аргумент.

## Returns

Метод ничего не возвращает.

# Examples

```js
var items = BaseDataSource.getItems();
BaseDataSource.setSelectedItem(items[0]);
```

# See Also

* [`getSelectedItem()`](../BaseDataSource.getSelectedItem/)
* [`onSelectedItemChanged`](../BaseDataSource.onSelectedItemChanged/)

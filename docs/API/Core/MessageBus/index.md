---
layout: doc
title: "MessageBus"
position: 1011
---

Шина сообщений представления - программный объект, который предоставляет инфраструктуру для обмена
сообщениями (событиями) между различными элементами представления (как визуальными, так и невизуальными).

# Description

Шина сообщений создается для каждого экземпляра представления. Отправка
сообщений осуществляется асинхронно, то есть отправитель не дожидается момента окончания обработки
сообщения. Обмен сообщениями в рамках экземпляра одного представления никак не влияет на экземпляры
других представлений.

Каждый элемент представления (как визуальный, так и невизуальный) может выступать в качестве источника
и/или в качестве подписчика на сообщения. Когда именно элемент будет осуществлять отправку сообщений,
зависит от логики работы самого элемента. Когда именно элемент обработает поступившее сообщение, также
зависит от элемента. Иначе говоря, момент отправки и момент окончания обработки сообщения в общем случае
не детерминирован (возможно, сообщение никогда не будет отправлено; возможно, сообщение никогда не будет
обработано), единственное, что гарантирует шина сообщений - доставку сообщения от источника всем
существующим подписчикам.

# Syntax

```js
new MessageBus(view)
```

## Parameters

|Name|Type|Description|
|----|----|-----------|
|`view`|[View](../Elements/View/)|Родительское [представление](../Elements/View/) шины сообщений.|

# Methods

|Name|Description|
|----|---------|
|[`getView`](MessageBus.getView/)|Возвращает родительское [представление](../Elements/View/).|
|[`send`](MessageBus.send/)|Отправляет сообщение заданного типа.|
|[`subscribe`](MessageBus.subscribe/)|Подписывает на сообщения заданного типа.|
|[`unsubscribeByType`](MessageBus.unsubscribeByType/)|Отписывается на сообщения заданного типа.|

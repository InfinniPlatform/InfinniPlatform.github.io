---
layout: doc
title: "ScrollPanel"
position: 0
---

Контейнер в виде прокручиваемой области.
Для корректной работы параметр [InfinniUI.config.enableAutoHeightService](../../Core/Config) должен иметь значение true, либо нужно задать высоту панели самостоятельно с помощью [стилей](../../Core/Elements/Element/Element.metadata).

# Description

Прокручиваемая область - [контейнер](../../Core/Elements/Container/) визуальных элементов, который
позволяет отображать содержимое в области, размер которой меньше размера содержимого. Когда
содержимое контейнера не отображается полностью, отображаются полосы прокрутки, с помощью которых
можно перемещать видимую область содержимого.

# Extends

[`Container`](../../Core/Elements/Container/)

# Syntax

```js
new ScrollPanel(parent)
```

## Parameters

|Name|Type|Description|
|----|----|-----------|
|parent|[`Element`](../../Core/Elements/Element)|Родительский элемент|

# Methods

|Name|Description|
|----|-----------|
|[getHorizontalScroll](ScrollPanel.getHorizontalScroll/)|Возвращает [видимость полосы прокрутки](ScrollVisibility/) по горизонтали|
|[setHorizontalScroll](ScrollPanel.setHorizontalScroll/)|Устанавливает [видимость полосы прокрутки](ScrollVisibility/) по горизонтали|
|[getVerticalScroll](ScrollPanel.getVerticalScroll/)|Возвращает [видимость полосы прокрутки](ScrollVisibility/) по вертикали|
|[setVerticalScroll](ScrollPanel.setVerticalScroll/)|Устанавливает [видимость полосы прокрутки](ScrollVisibility/) по вертикали|

# Events

Нет

# See Also

* [`ScrollVisibility`](ScrollVisibility/)
* [`Container`](../../Core/Elements/Container/)

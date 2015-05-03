---
layout: default
title: "PrintElementInlineContainer"
position: 0
categories: 
tags: 
---

Типы однострочных элементов печатного представления.

   

#### Type

object

   

#### Schema

```
{
  "id": "PrintElementInlineContainer",
  "description": "Типы однострочных элементов печатного представления",
  "type": "object",
  "properties": {
    "Span": {
      "description": "Однострочный элемент печатного представления для группировки множества однострочных элементов",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementSpan"
    },
    "Bold": {
      "description": "Однострочный элемент печатного представления, текстовое содержимое которого отображается полужирным шрифтом",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementBold"
    },
    "Italic": {
      "description": "Однострочный элемент печатного представления, текстовое содержимое которого отображается курсивом",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementItalic"
    },
    "Underline": {
      "description": "Однострочный элемент печатного представления, текстовое содержимое которого отображается с эффектом подчеркивания",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementUnderline"
    },
    "Hyperlink": {
      "description": "Однострочный элемент печатного представления, содержимое которого отображается в виде гиперссылки",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementHyperlink"
    },
    "LineBreak": {
      "description": "Однострочный элемент печатного представления для разрыва строки",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementLineBreak"
    },
    "Run": {
      "description": "Однострочный элемент печатного представления для вывода неформатированного текста",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementRun"
    },
    "Image": {
      "description": "Однострочный элемент печатного представления для отображения изображений",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementImage"
    },
    "BarcodeEan13": {
      "description": "Однострочный элемент печатного представления для отображения штрих-кода в формате EAN13",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementBarcodeEan13"
    },
    "BarcodeQr": {
      "description": "Однострочный элемент печатного представления для отображения штрих-кода в формате QR",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementBarcodeQr"
    }
  },
  "additionalProperties": false
}
```

 

 

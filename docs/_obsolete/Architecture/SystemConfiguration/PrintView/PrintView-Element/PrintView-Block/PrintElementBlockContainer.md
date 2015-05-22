---
layout: doc
title: "PrintElementBlockContainer"
position: 0
categories: 
tags: 
---

Типы блочных элементов печатного представления.

   

#### Type

object

   

#### Schema

```
{
  "id": "PrintElementBlockContainer",
  "description": "Типы блочных элементов печатного представления",
  "type": "object",
  "properties": {
    "Section": {
      "description": "Блочный элемент печатного представления для группировки множества блочных элементов",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementSection"
    },
    "Paragraph": {
      "description": "Блочный элемент печатного представления для группировки однострочных элементов в абзац",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementParagraph"
    },
    "List": {
      "description": "Блочный элемент печатного представления для отображения списка",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementList"
    },
    "Table": {
      "description": "Блочный элемент печатного представления для отображения таблицы",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementTable"
    },
    "Line": {
      "description": "Блочный элемент печатного представления для отображения горизонтальной линии",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementLine"
    },
    "PageBreak": {
      "description": "Блочный элемент печатного представления для разрыва страницы",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementPageBreak"
    }
  },
  "additionalProperties": false
}
```

 

 

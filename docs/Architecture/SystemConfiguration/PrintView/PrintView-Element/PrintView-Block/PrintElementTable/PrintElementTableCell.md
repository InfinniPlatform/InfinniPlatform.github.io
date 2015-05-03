---
layout: default
title: "PrintElementTableCell"
position: 2
categories: 
tags: 
---

Настройки строки ячейки таблицы.

   

#### Type

object

   

#### Schema

```
{
  "id": "PrintElementTableCell",
  "description": "Настройки строки ячейки таблицы",
  "type": "object",
  "properties": {
    "Name": {
      "description": "Наименование ячейки",
      "type": "string",
      "minLength": 1
    },
    "Style": {
      "description": "Наименование стиля",
      "type": "string",
      "minLength": 1
    },
    "Font": {
      "description": "Настройки шрифта",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/Font"
    },
    "Foreground": {
      "description": "Цвет содержимого",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/Color"
    },
    "Background": {
      "description": "Цвет фона содержимого",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/Color"
    },
    "TextCase": {
      "description": "Регистр символов текста",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementTextCase"
    },
    "Border": {
      "description": "Границы элемента",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementBorder"
    },
    "Padding": {
      "description": "Отступ от края элемента до содержимого элемента",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/Thickness"
    },
    "TextAlignment": {
      "description": "Горизонтальное выравнивание текста элемента",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementTextAlignment"
    },
    "ColumnSpan": {
      "description": "Количество ячеек для объединения по горизонтали",
      "type": "integer",
      "default": 1,
      "minimum": 1,
      "exclusiveMinimum": false
    },
    "RowSpan": {
      "description": "Количество ячеек для объединения по вертикали",
      "type": "integer",
      "default": 1,
      "minimum": 1,
      "exclusiveMinimum": false
    },
    "Block": {
      "description": "Содержимое ячейки",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementBlockContainer"
    }
  },
  "additionalProperties": false
}
```

 

 

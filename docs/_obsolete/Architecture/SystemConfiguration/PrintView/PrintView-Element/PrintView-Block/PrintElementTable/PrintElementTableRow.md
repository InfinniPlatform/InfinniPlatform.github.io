---
layout: doc
title: "PrintElementTableRow"
position: 1
categories: 
tags: 
---

Настройки строки таблицы.

   

#### Type

object

   

#### Schema

```
{
  "id": "PrintElementTableRow",
  "description": "Настройки строки таблицы",
  "type": "object",
  "properties": {
    "Name": {
      "description": "Наименование строки",
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
    "Cells": {
      "description": "Список ячеек строки таблицы",
      "type": "array",
      "items": {
        "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementTableCell"
      }
    }
  },
  "additionalProperties": false
}
```

 

 

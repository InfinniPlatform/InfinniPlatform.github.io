---
layout: default
title: "PrintView"
position: 
categories: 
tags: 
---

Печатное представление.

   

#### Type

object

   

#### Extends

[[ObjectMetadata]]

[[PrintElement]]

   

#### Schema

```
{
  "id": "PrintView",
  "description": "Печатное представление",
  "type": "object",
  "extends": [
    {
      "$ref": "http://demo.infinnity.ru:8081/display/MC/ObjectMetadata"
    },
    {
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElement"
    }
  ],
  "properties": {
    "ViewType": {
      "description": "Тип печатного представления",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintViewType",
      "default": "ObjectView",
      "required": true
    },
    "PageSize": {
      "description": "Размеры страницы",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/Size"
    },
    "PagePadding": {
      "description": "Отступ от края страницы до содержимого страницы",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/Thickness"
    },
    "Styles": {
      "description": "Список стилей печатного представления",
      "type": "array",
      "items": {
        "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintViewStyle"
      }
    },
    "Blocks": {
      "description": "Список блочных элементов печатного представления",
      "type": "array",
      "items": {
        "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementBlockContainer"
      }
    }
  },
  "additionalProperties": false
}
```

 

 

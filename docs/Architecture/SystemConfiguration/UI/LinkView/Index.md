---
layout: default
title: "LinkView"
position: 11
categories: 
tags: 
---

Контейнер для описания ссылки на представление.

   

Базовый тип для ссылки на представление описан в разделе [[BaseLinkView]].

  

#### Schema

```
{
  "id": "LinkView",
  "description": "Контейнер для описания ссылки на представление",
  "type": "object",
  "properties": {
    "ExistsView": {
      "description": "Ссылка на существующее представление",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/ExistsView"
    },
    "AutoView": {
      "description": "Автоматически генерируемое представление",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/AutoView"
    },
    "InlineView": {
      "description": "Встроенное представление",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/InlineView"
    },
    "ChildView": {
      "description": "Ссылка на дочернее представление",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/ChildView"
    }
  },
  "additionalProperties": false
}
```

 

 

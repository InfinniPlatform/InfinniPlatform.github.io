---
layout: default
title: "ExistsView"
position: 3
categories: 
tags: 
---

Ссылка на существующее представление.

   

#### Schema

```
{
  "id": "ExistsView",
  "description": "Ссылка на существующее представление",
  "type": "object",
  "extends": {
    "$ref": "http://demo.infinnity.ru:8081/display/MC/BaseLinkView"
  },
  "properties": {
    "ConfigId": {
      "description": "Идентификатор конфигурации",
      "type": "string",
      "required": true
    },
    "DocumentId": {
      "description": "Идентификатор документа",
      "type": "string",
      "required": true
    },
    "ViewId": {
      "description": "Идентификатор представления",
      "type": "string",
      "required": true
    }
  },
  "additionalProperties": false
}
```

 

 

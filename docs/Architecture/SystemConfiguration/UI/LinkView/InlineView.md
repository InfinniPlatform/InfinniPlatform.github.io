---
layout: default
title: "InlineView"
position: 5
categories: 
tags: 
---

Встроенное представление.

   

#### Schema

```
{
  "id": "InlineView",
  "description": "Встроенное представление",
  "type": "object",
  "extends": {
    "$ref": "http://demo.infinnity.ru:8081/display/MC/BaseLinkView"
  },
  "properties": {
    "View": {
      "description": "Встроенное описание представления",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/View"
    }
  },
  "additionalProperties": false
}
```

 

 

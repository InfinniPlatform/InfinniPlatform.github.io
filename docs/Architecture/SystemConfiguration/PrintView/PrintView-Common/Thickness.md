---
layout: default
title: "Thickness"
position: 
categories: 
tags: 
---

Толщина сторон прямоугольника.

   

#### Type

object

  

#### Schema

```
{
  "id": "Thickness",
  "description": "Толщина сторон прямоугольника",
  "type": "object",
  "properties": {
    "All": {
      "description": "Все границы",
      "type": "number",
      "default": 0,
      "minimum": 0,
      "exclusiveMinimum": false
    },
    "Left": {
      "description": "Левая граница",
      "type": "number",
      "default": 0,
      "minimum": 0,
      "exclusiveMinimum": false
    },
    "Top": {
      "description": "Верхняя граница",
      "type": "number",
      "default": 0,
      "minimum": 0,
      "exclusiveMinimum": false
    },
    "Right": {
      "description": "Правая граница",
      "type": "number",
      "default": 0,
      "minimum": 0,
      "exclusiveMinimum": false
    },
    "Bottom": {
      "description": "Нижняя граница",
      "type": "number",
      "default": 0,
      "minimum": 0,
      "exclusiveMinimum": false
    },
    "SizeUnit": {
      "description": "Единица измерения",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/SizeUnit",
      "default": "Pt"
    }
  },
  "additionalProperties": false
}
```

   

#### Example

![](Thickness.PNG)

```
{
  "Left": 1,
  "Top": 2,
  "Right": 4,
  "Bottom": 8,
  "SizeUnit": "Px"
}
```

 

 

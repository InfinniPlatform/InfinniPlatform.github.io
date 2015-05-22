---
layout: doc
title: "PrintElementImage"
position: 8
categories: 
tags: 
---

Однострочный элемент печатного представления для отображения изображений.

   

#### Type

object

   

#### Extends

[[PrintElementInline]]

   

#### Schema

```
{
  "id": "PrintElementImage",
  "description": "Однострочный элемент печатного представления для отображения изображений",
  "type": "object",
  "extends": {
    "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementInline"
  },
  "properties": {
    "Data": {
      "description": "Данные изображения",
      "type": "string",
      "media": {
        "binaryEncoding": "base64"
      }
    },
    "Size": {
      "description": "Размеры изображения",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/Size"
    },
    "Rotation": {
      "description": "Поворот изображения",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementRotation",
      "default": "Rotate0"
    },
    "Stretch": {
      "description": "Растягивание изображения",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintElementImageStretch",
      "default": "Uniform"
    }
  },
  "additionalProperties": false
}
```

    

#### Example

[[PrintElementImage.pdf]]

```
{
  "Blocks": [
    {
      "Paragraph": {
        "Inlines": [
          {
            "Image": {
              "Data": "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
m+SVVX+V6OjoMnR0dHQf/9k="
            }
          }
        ]
      }
    }
  ],
  "PageSize": {
    "Width": 200,
    "Height": 100,
    "SizeUnit": "Px"
  },
  "PagePadding": {
    "Left": 10,
    "Top": 10,
    "Right": 10,
    "Bottom": 10
  }
}
```

 

 

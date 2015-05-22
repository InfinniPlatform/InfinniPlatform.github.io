---
layout: doc
title: "Font"
position: 0
categories: 
tags: 
---

Настройки шрифта.

    

Предполагается поддержка только [OpenType](https://en.wikipedia.org/wiki/OpenType) шрифтов.

   

#### Type

object

   

#### Schema

```
{
  "id": "Font",
  "description": "Настройки шрифта",
  "type": "object",
  "properties": {
    "Family": {
      "description": "Семейство шрифта",
      "type": "string",
      "required": true
    },
    "Size": {
      "description": "Размер шрифта",
      "type": "number",
      "minimum": 0,
      "exclusiveMinimum": true,
      "required": true
    },
    "SizeUnit": {
      "description": "Единица измерения размера шрифта",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/SizeUnit",
      "default": "Pt"
    },
    "Style": {
      "description": "Стиль шрифта",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/FontStyle",
      "default": "Normal"
    },
    "Stretch": {
      "description": "Степень растягивания шрифта по горизонтали",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/FontStretch",
      "default": "Normal"
    },
    "Weight": {
      "description": "Насыщенность шрифта",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/FontWeight",
      "default": "Normal"
    },
    "Variant": {
      "description": "Вертикальное выравнивание шрифта",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/FontVariant",
      "default": "Normal"
    }
  },
  "additionalProperties": false
}
```

   

#### Example

[[Font.pdf]]

```
{
  "Blocks": [
    {
      "Paragraph": {
        "Inlines": [
          {
            "Run": {
              "Font": {
                "Family": "Arial",
                "Size": 12,
                "SizeUnit": "Pt",
                "Style": "Italic"
              },
              "Text": "Arial, 12pt, Italic"
            }
          }
        ]
      }
    },
    {
      "Paragraph": {
        "Inlines": [
          {
            "Run": {
              "Font": {
                "Family": "Times New Roman",
                "Size": 12,
                "SizeUnit": "Px",
                "Style": "Italic",
                "Weight": "Bold"
              },
              "Text": "Times New Roman, 12px, Italic, Bold"
            }
          }
        ]
      }
    }
  ],
  "PageSize": {
    "Width": 350,
    "Height": 150,
    "SizeUnit": "Px"
  }
}
```

 

 

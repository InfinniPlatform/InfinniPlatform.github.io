---
layout: doc
title: "SaveAction"
position: 9
categories: 
tags: 
---

Действие сохранения текущего элемента источника данных.

   

#### Description

* Проверяет корректность текущего элемента источника данных.
* Если текущий элемент источника данных содержит ошибки, они отображаются пользователю, выполнение действия прекращается.
* Если текущий элемент источника данных содержит предупреждения, они отображаются пользователю, у пользователя запрашивается подтверждение о том, что он допускает предупреждения.
* Если пользователь согласен с предупреждениями, текущий элемент источника данных сохраняется.
* Если пользователь не согласен с предупреждениями, выполнение действия прекращается.
* Если сохранение текущего элемента источника данных прошло без ошибок, представление закрывается со статусом подтверждения.
* Если сохранение текущего элемента источника данных прошло с ошибками, они отображаются пользователю.

   

#### Extends

|Name|Description|
|----|-----------|
| [[Command]]| Базовый тип действия, которое может быть вызвано из визуального представления.|

   

#### Methods

|Name|Description|
|----|-----------|
| | |

    

#### Events

|Name|Description|
|----|-----------|
| | |

   

#### Schema

```
{
  "id": "SaveAction",
  "description": "Действие сохранения текущего элемента источника данных",
  "type": "object",
  "extends": {
    "$ref": "http://demo.infinnity.ru:8081/display/MC/Command"
  },
  "properties": {
    "CanClose": {
      "description": "Разрешено ли закрытие представления",
      "type": "boolean",
      "default": true
    },
    "DataSource": {
      "description": "Источник данных",
      "type": "string",
      "required": true
    }
  },
  "additionalProperties": false
}
```

     

 

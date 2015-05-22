---
layout: doc
title: "ServerAction"
position: 17
categories: 
tags: 
---

Действие вызова операции на сервере.

   

#### Description

Выполняет указанную операцию на сервере.

   

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
  "id": "ServerAction",
  "description": "Действие вызова операции на сервере",
  "type": "object",
  "extends": {
    "$ref": "http://demo.infinnity.ru:8081/display/MC/Command"
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
    "ActionId": {
      "description": "Идентификатор действия",
      "type": "string",
      "required": true
    },
    "Parameters": {
      "description": "Список параметров запроса",
      "type": "array",
      "items": {
        "type": "object",
        "properties": {
          "Name": {
            "description": "Наименование параметра запроса",
            "type": "string",
            "required": true
          },
          "Value": {
            "description": "Привязка данных текущего представления на параметр запроса",
            "$ref": "http://demo.infinnity.ru:8081/display/MC/DataBinding",
            "required": true
          }
        }
      }
    }
  },
  "additionalProperties": false
}
```

     

 

---
layout: default
title: "Action"
position: 12
categories: 
tags: 
---

Контейнер для описания действия, которое может быть вызвано из визуального представления.

 

Базовый тип действия, которое может быть вызвано из визуального представления, описан в разделе [[Command]].

   

#### Schema

```
{
  "id": "Action",
  "description": "Действие, которое может быть вызвано из визуального представления",
  "type": "object",
  "properties": {
    "AcceptAction": {
      "description": "Действие закрытия представления со статусом подтверждения",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/AcceptAction"
    },
    "CancelAction": {
      "description": "Действие закрытия представления со статусом отмены",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/CancelAction"
    },
    "AddAction": {
      "description": "Действие добавления элемента в источник данных",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/AddAction"
    },
    "AddItemAction": {
      "description": "Действие добавления элемента в коллекцию источника данных",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/AddItemAction"
    },
    "EditAction": {
      "description": "Действие редактирования текущего элемента источника данных",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/EditAction"
    },
    "EditItemAction": {
      "description": "Действие редактирования текущего элемента коллекции источника данных",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/EditItemAction"
    },
    "DeleteAction": {
      "description": "Действие удаления текущего элемента из источника данных",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/DeleteAction"
    },
    "DeleteItemAction": {
      "description": "Действие удаления текущего элемента из коллекции источника данных",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/DeleteItemAction"
    },
    "SaveAction": {
      "description": "Действие сохранения текущего элемента источника данных",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/SaveAction"
    },
    "StateAction": {
      "description": "Действие изменения состояния текущего элемента источника данных",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/StateAction"
    },
    "UpdateAction": {
      "description": "Действие обновления источника данных",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/UpdateAction"
    },
    "OpenAction": {
      "description": "Действие открытия представления",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/OpenAction"
    },
    "SelectAction": {
      "description": "Действие открытия представления для выбора данных",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/SelectAction"
    },
    "PrintReportAction": {
      "description": "Действие открытия отчета",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintReportAction"
    },
    "PrintViewAction": {
      "description": "Действие открытия печатного представления",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/PrintViewAction"
    },
    "ServerAction": {
      "description": "Действие вызова операции на сервере",
      "$ref": "http://demo.infinnity.ru:8081/display/MC/ServerAction"
    }
  },
  "additionalProperties": false
}
```

 

 

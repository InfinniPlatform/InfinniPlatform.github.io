---
layout: doc
title: "InsertRegister"
position: 0
categories: 
tags:
---

Сохранить новый экземпляр метаданных документа в хранилище метаданных

## Method 

PUT

## Description
Предоставляет возможность сохранения нового экземпляра документа в хранилище метаданных.

## Syntax
```js
<serverScheme>://<serverName>:<serverPort>/<route>/metadata/<configName>/register
```

### Parameters

`serverScheme`

Серверный протокол (HTTP/HTTPS).

`serverName`

Наименование сервера (например: localhost, 'demo.somedomain.ru').

`serverPort`

Порт сервера.

`route` 

Указание на роутинг сервера в составе кластера

`configName`

Наименование конфигурации

## Example

Пример запроса:

```js
PUT http://localhost:9900/1/metadata/2.0.0.0/NewSolution/Register

BODY

{
  "Id": "ceae998a-2707-4caf-8883-49dacb9961f3",
  "Version": "2.0.0.0",
  "Name": "Register1",
  "Caption": "",
  "Description": ""
}
```

В результате успешного выполнения запроса возвращается 200 ОК
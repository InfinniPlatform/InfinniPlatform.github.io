---
layout: doc
title: "GetRegister"
position: 2
categories: 
tags:
---

Получить экземпляр метаданных регистра из хранилища метаданных

## Method 

GET

## Description
Предоставляет возможность получения экземпляра метаданных регистра из хранилища метаданных.

## Syntax
```js
<serverScheme>://<serverName>:<serverPort>/<route>/metadata/<configName>/register/<registerName>
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

`<registerName>`

Наименование регистра

## Example

Пример запроса:

```js
GET http://localhost:9900/1/metadata/2.0.0.0/NewConfig/Register/TestRegister 
```

В результате успешного выполнения запроса возвращается

```js
{
  "Id": "ceae998a-2707-4caf-8883-49dacb9961f3",
  "Secured": true,
  "Version": "2.0.0.0",
  "Name": "TestRegister",
  "Caption": "",
  "Description": "",
  "ParentId": "TestConfigVersion_07bd4f5d-2753-434e-90bd-9a3fa5991ff2",
  "__ConfigId": "systemconfig",
  "__DocumentId": "registermetadata"
}
```
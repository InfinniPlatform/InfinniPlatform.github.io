---
layout: doc
title: "GetAssemblyList"
position: 15
categories: 
tags:
---

## Description
Предоставляет возможность чтения списка существующих в конфигурации сборок.

## Method

GET

## Syntax
```js
<serverScheme>://<serverName>:<serverPort>/<route>/metadata/<version>/<configuration>/<metadataType>
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

`version`

Версия приложения.

`configuration`

Приложение (конфигурация)

`metadataType`

Тип метаданных (Assembly)


## Example


Пример запроса метаданных:

```js
http://localhost:9900/1/metadata/2.0.0.0/TestConfigVersion/Assembly 
```

Пример результата запроса:

```js
[
  {
    "Id": "9d563d33-1f86-4ab0-9697-7a0cb72ce320",
    "Name": "Assembly1_v1",
    "Caption": ""
  }
]
```
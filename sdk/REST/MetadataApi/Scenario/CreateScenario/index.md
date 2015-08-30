---
layout: doc
title: "CreateScenario"
position: 0
categories: 
tags:
---

## Description
Предоставляет возможность создания шаблона новой прикладного модуля конфигурации.
ПОлученный шаблон будет инциализирован значениями по умолчанию для всех обязательных полей

## Syntax
```csharp
public dynamic CreateScenario(string version, string configuration, string document)
```

### Parameters

`version`

Семантическая версия конфигурации (например, "1.0.0.0").

`configuration`

Наименование объекта конфигурации

`document`

Наименование документа

## Example

Пример запроса метаданных:

```csharp
dynamic scenario = api.CreateScenario("1.0.0.0","TestConfig1","TestDocument1");
```

Результат выполнения запроса:

```js

	{
	  "Id": "c2a00771-3ded-428d-8d1d-680aa672e394",
	  "Version": "1.0.0.0",
	  "Name": "",
	  "Caption": "",
	  "Description": ""
	}

```
---
layout: doc
title: "Получение результата агрегации по регистру с разбиением по периодам (GetValuesByPeriods)"
position: 
categories: 
tags: 
---

Перед рассмотрением операций, следует ознакомиться с [[правилами формирования запросов REST|Обработка запросов REST и формирование роутинга для запросов]]

#### Внутренняя реализация

Запрос позволяет получить информацию о ресурсах с разбиением по периодам. Запрос позволяет указать измерения, по которым производить агрегацию. Если список измерений не задан, в качестве измерений будут взяты все свойства регистра, помеченные как Dimension. В качестве интервалов могут быть указаны следующие значения: year, quarter, month, week, day, hour, minute, second.

#### Запрос

POST [http://<ServerName>:<PortName>/SystemConfig/StandardApi/metadata/GetRegisterValuesByPeriods](http://10.10.1.82:9999/SystemConfig/StandardApi/metadata/GetRegisterValuesByPeriods)

```
{
	"id": null,
	"changesObject": {
		"Configuration": "<Configuration name>",
		"Register": "<Register name>",
        "FromDate": "<From date>",		
		"ToDate": "<To date>",		
        "Interval": "<Interval>",
        "TimeZone": "<TimeZone>",
		"Dimensions": <Dimensions>,
		"ValueProperty": "<Value property>"
	},
	"replace": false
}
```

В теле запроса передаются следующие аргументы

<Configuration name> - идентификатор конфигурации (см. [[правила формирования запросов REST|Обработка запросов REST и формирование роутинга для запросов]])

<Register name> - наименование регистра (см. [[правила формирования запросов REST|Обработка запросов REST и формирование роутинга для запросов]])

<From date> - дата, от которой необходимо рассчитать значения ресурсов. Например, "2014-08-12T00:00:00"

<To date> - дата, до которой необходимо рассчитать значения ресурсов. Например, "2015-08-12T00:00:00"

<Interval> - интервал агрегации (Year, quarter, month, week, day, hour, minute or second)

<TimeZone> - временная зона в виде строки. Например, "+05:00". Если параметр не указан, будет использована текущая временная зона.

<Dimensions> - измерения, по которым выполнять агрегацию. Например, ["Room", "Bed"]

<Value property> - Свойство, по которому будет вычислено агрегирующее значение. Например, "Value"

#### Ответ

Ответ сервера (пример):

```
[{
	"DocumentDate": "2014-01-01",
	"Room": "палата 33",
	"Bed": "койка 1",
	"Value": 1.0
},
{
	"DocumentDate": "2014-01-01",
	"Room": "палата 33",
	"Bed": "койка 2",
	"Value": 1.0
},
{
	"DocumentDate": "2014-01-01",
	"Room": "палата 33",
	"Bed": "койка 3",
	"Value": 1.0
},
{
	"DocumentDate": "2014-01-01",
	"Room": "палата 54",
	"Bed": "койка 1",
	"Value": 1.0
},
{
	"DocumentDate": "2014-01-01",
	"Room": "палата 54",
	"Bed": "койка 2",
	"Value": 1.0
},
{
	"DocumentDate": "2014-01-01",
	"Room": "палата 54",
	"Bed": "койка 3",
	"Value": 1.0
},
{
	"DocumentDate": "2014-08-01",
	"Room": "палата 54",
	"Bed": "койка 1",
	"Value": 0.0
},
{
	"DocumentDate": "2014-08-01",
	"Room": "палата 54",
	"Bed": "койка 2",
	"Value": 0.0
},
{
	"DocumentDate": "2014-08-01",
	"Room": "палата 54",
	"Bed": "койка 3",
	"Value": 0.0
},
{
	"DocumentDate": "2014-08-01",
	"Room": "палата 33",
	"Bed": "койка 1",
	"Value": 0.0
},
{
	"DocumentDate": "2014-08-01",
	"Room": "палата 33",
	"Bed": "койка 2",
	"Value": -1.0
},
{
	"DocumentDate": "2014-08-01",
	"Room": "палата 33",
	"Bed": "койка 3",
	"Value": -1.0
},
{
	"DocumentDate": "2014-09-01",
	"Room": "палата 33",
	"Bed": "койка 2",
	"Value": 1.0
},
{
	"DocumentDate": "2014-09-01",
	"Room": "палата 33",
	"Bed": "койка 3",
	"Value": 1.0
}]
```

Каждый элемент массива представляет собой объект с уникальным значением измерений (в данном случае Room и Bed) в рамках периода, определяемого интервалом (в данном случае в рамках одного месяца).

 

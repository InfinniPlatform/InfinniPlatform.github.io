---
layout: default
title: "CollectionValidator"
position: 
categories: 
tags: 
---

Контейнер для описания оператора проверки коллекции и ее свойств.

   

```
{
	"id": "CollectionValidator",
	"description": "Контейнер для описания оператора проверки коллекции и ее свойств",
	"type": "object",
	"properties": {
		"All": {
			"description": "Все элементы коллекции удовлетворяют заданному условию",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/All"
		},
		"Any": {
			"description": "Один из элементов коллекции удовлетворяют заданному условию",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/Any"
		},
		"IsNullOrEmptyCollection": {
			"description": "Коллекция является нулевым указателем или пустой коллекцией",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsNullOrEmptyCollection"
		},
		"IsContainsCollection": {
			"description": "Коллекция содержит заданное значение",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsContainsCollection"
		}
    }
}
```

   

```
{
	"All": {
		"Operator": {
			"IsLessThan": {
				"Message": "Элементы должны быть меньше 3",
				"Value": 3
			}
		}
	}
}
```

 

 

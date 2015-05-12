---
layout: doc
title: "ObjectValidator"
position: 
categories: 
tags: 
---

Контейнер для описания оператора проверки объекта и его свойств.

 

```
{
	"id": "ObjectValidator",
	"description": "Контейнер для описания оператора проверки объекта и его свойств",
	"type": "object",
	"properties": {
		"IsNull": {
			"description": "Объект является нулевым указателем",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsNull"
		},
		"IsEqual": {
			"description": "Объект равен заданному объекту",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsEqual"
		},
		"IsDefaultValue": {
			"description": "Объект является значением по умолчанию для данного типа",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsDefaultValue"
		},
		"IsGuid": {
			"description": "Объект является глобально уникальным идентификатором (GUID)",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsGuid"
		},
		"IsUri": {
			"description": "Объект является URI",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsUri"
		},
		"IsAbsoluteUri": {
			"description": "Объект является абсолютным URI",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsAbsoluteUri"
		},
		"IsRelativeUri": {
			"description": "Объект является относительным URI",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsRelativeUri"
		},
		"IsNullOrEmpty": {
			"description": "Объект является нулевым указателем или пустой строкой",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsNullOrEmpty"
		},
		"IsNullOrWhiteSpace": {
			"description": "Объект является нулевым указателем или строкой из пробелов",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsNullOrWhiteSpace"
		},
		"IsContains": {
			"description": "Объект равен заданному объекту",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsContains"
		},
		"IsStartsWith": {
			"description": "Объект начинается заданной подстрокой",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsStartsWith"
		},
		"IsEndsWith": {
			"description": "Объект оканчивается заданной подстрокой",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsEndsWith"
		},
		"IsRegex": {
			"description": "Объект удовлетворяет заданному регулярному выражению",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsRegex"
		},
		"IsLessThan": {
			"description": "Объект меньше заданного объекта",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsLessThan"
		},
		"IsMoreThan": {
			"description": "Объект больше заданного объекта",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsMoreThan"
		},
		"IsLessThanOrEqual": {
			"description": "Объект меньше или равен заданного объекта",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsLessThanOrEqual"
		},
		"IsMoreThanOrEqual": {
			"description": "Объект больше или равен заданного объекта",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsMoreThanOrEqual"
		},
		"IsIn": {
			"description": "Объект содержится в заданной коллекции",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/IsIn"
		}
    }
}
```

   

```
{
	"IsEqual": {
		"Message": "Свойство Property1 не равно 12345.",
		"Property": "Property1",
		"Value": 12345
	}
}
```

 

 

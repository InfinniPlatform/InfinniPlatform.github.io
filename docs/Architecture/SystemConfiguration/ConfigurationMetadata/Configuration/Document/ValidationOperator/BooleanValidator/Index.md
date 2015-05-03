---
layout: default
title: "BooleanValidator"
position: 
categories: 
tags: 
---

Контейнер для описания условных операторов.

 

```
{
	"id": "BooleanValidator",
	"description": "Контейнер для описания условных операторов",
	"type": "object",
	"properties": {
		"Or": {
			"description": "Объект должен удовлетворять хотя бы одному из заданных условий",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/Or"
		},
		"And": {
			"description": "Объект должен удовлетворять всем заданным условиям",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/And"
		},
		"Not": {
			"description": "Объект не должен удовлетворять заданному условию",
			"$ref": "http://wiki.infinnity.lan:8081/display/MC/Not"
		}
    }
}
```

 

 

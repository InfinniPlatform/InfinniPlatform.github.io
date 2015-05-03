---
layout: default
title: "ForeignKey"
position: 
categories: 
tags: 
---

Ссылка на внешний документ.

 

Ссылка на внешний документ описывает не метаданные модели данных, а **данные** атрибута документа, который был описан, как ссылка на документ с признаком Inline=false (см. [[DocumentLink]]). Ссылка на внешний документ хранит первичный ключ (Id) и и строковое представление (DisplayName) документа, на который была сделана ссылка. 

   

```
{
	"id": "ForeignKey",
	"description": "Ссылка на внешний документ",
	"type": "object",
	"properties": {
		"Id": {
			"description": "Уникальный идентификатор внешнего документа",
			"type": "string",
			"required": true
		},
		"DisplayName": {
			"description": "Строковое представление внешнего документа",
			"type": "string"
		}
	}
}
```

 

 

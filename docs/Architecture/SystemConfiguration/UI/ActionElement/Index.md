---
layout: default
title: "ActionElement"
position: 14
categories: 
tags: 
---

Элемент представления для вызова действий.

 

```
{
	"id": "ActionElement",
	"description": "Элемент представления для вызова действий",
	"type": "object",
	"properties": {
		"ActionBar": {
			"description": "Настройки панели действий для текущего представления",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/ActionBar"
		},
		"MenuBar": {
			"description": "Элемент представления в виде иерархического меню",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/MenuBar"
		},
		"ToolBar": {
			"description": "Элемент представления в виде панели инструментов",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/ToolBar"
		},
		"Button": {
			"description": "Элемент представления в виде кнопки",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/Button"
		},
		"PopupButton": {
			"description": "Элемент представления в виде кнопки со списком возможных действий",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/PopupButton"
		}
	}
}
```

  


  


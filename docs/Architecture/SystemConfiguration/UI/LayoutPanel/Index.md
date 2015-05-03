---
layout: default
title: "LayoutPanel"
position: 13
categories: 
tags: 
---

Контейнер элементов представления.

 

```
{
	"id": "LayoutPanel",
	"description": "Контейнер элементов представления",
	"type": "object",
	"properties": {
		"Panel": {
			"description": "Контейнер элементов представления в виде прямоугольной области",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/Panel"
		},
		"TabPanel": {
			"description": "Контейнер элементов представления в виде набора закладок для страниц",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/TabPanel"
		},
		"StackPanel": {
			"description": "Контейнер элементов представления в виде стека",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/StackPanel"
		},
		"GridPanel": {
			"description": "Контейнер элементов представления в виде сетки",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/GridPanel"
		},
		"WrapPanel": {
			"description": "Контейнер элементов представления для размещения элементов слева направо и сверху вниз",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/WrapPanel"
		},
		"ViewPanel": {
			"description": "Контейнер элементов представления в виде прямоугольной области, в которую помещается указанное представление",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/ViewPanel"
		},
		"ScrollPanel": {
			"description": "Контейнер элементов представления в виде области, содержимое которой может прокручиваться по вертикали и горизонтали",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/ScrollPanel"
		},
		"ExtensionPanel": {
			"description": "Контейнер для встраивания внешнего компонента",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/ExtensionPanel"
		}
	}
}
```

 

 

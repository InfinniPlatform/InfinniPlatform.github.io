---
layout: default
title: "DataElement"
position: 15
categories: 
tags: 
---

Элемент представления для отображения или редактирования данных.

 

```
{
	"id": "DataElement",
	"description": "Элемент представления для отображения или редактирования данных",
	"type": "object",
	"properties": {
		"Label": {
			"description": "Элемент представления для отображения данных в виде текстовой метки",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/Label"
		},
		"LinkLabel": {
			"description": "Элемент представления для отображения данных в виде текстовой метки со ссылкой",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/LinkLabel"
		},
		"TextBox": {
			"description": "Элемент представления для отображения или редактирования неформатированного текста",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/TextBox"
		},
		"NumericBox": {
			"description": "Элемент представления для отображения или редактирования чисел",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/NumericBox"
		},
		"CheckBox": {
			"description": "Элемент представления для отображения и редактирования логического значения в виде флажка",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/CheckBox"
		},
		"ToggleButton": {
			"description": "Элемент представления для отображения и редактирования логического значения в виде переключателя",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/ToggleButton"
		},
		"DatePicker": {
			"description": "Элемент представления для отображения и редактирования даты",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/DatePicker"
		},
		"ComboBox": {
			"description": "Элемент представления для выбора одного или нескольких значений из раскрывающегося списка",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/ComboBox"
		},
		"ListBox": {
			"description": "Элемент представления для выбора одного или нескольких значений из списка",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/ListBox"
		},
		"TreeView": {
			"description": "Элемент представления для отображения данных в виде дерева",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/TreeView"
		},
		"DataGrid": {
			"description": "Элемент представления для отображения данных в виде таблицы",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/DataGrid"
		},
		"PropertyGrid": {
			"description": "Элемент представления для отображения данных объекта в виде вертикальной таблицы",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/PropertyGrid"
		},
		"ImageBox": {
			"description": "Элемент представления для отображения и редактирования изображений",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/ImageBox"
		},
		"UploadFileBox": {
			"description": "Элемент представления для выгрузки одного или нескольких файлов",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/UploadFileBox"
		},
		"SearchPanel": {
			"description": "Элемент представления для полнотекстового поиска по источнику данных",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/SearchPanel"
		},
		"FilterPanel": {
			"description": "Элемент представления для настраиваемого фильтра источника данных",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/FilterPanel"
		},
		"DataNavigation": {
			"description": "Элемент представления для панели навигации по данным",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/DataNavigation"
		},
		"DocumentViewer": {
			"description": "Элемент представления для отображения документа в печатном виде",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/DocumentViewer"
		}
	}
}
```

 

 

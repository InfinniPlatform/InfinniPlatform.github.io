---
layout: doc
title: "SelectAction.metadata"
position: 0
---

Метаданные типа [`SelectAction`](../).

# Properties

|Name|Type|Description|
|----|----|-----------|
|LinkView<sup>*</sup>|[`LinkView.metadata`](../../../Elements/View/LinkView/LinkView.metadata/)|Объект, который будет создавать и настраивать [представление](../../../Elements/View/)|
|SourceValue.Source<sup>*</sup>|`String`|Название источника данных, из которого будет заполняться редактируемый источник данных|
|SourceValue.Property<sup>*</sup>|`String`|Путь до поля в источнике данных, которое будет копироваться|
|DestinationValue.Source<sup>*</sup>|`String`|Название редактируемого источника данных|
|DestinationValue.Property<sup>*</sup>|`String`|Путь до поля в источнике данных, которое будет редактироваться|

<sup>*</sup> Обязательное свойство.

# Examples

```json
{
	"SelectAction": {
		"DestinationValue": {
		  "Source": "Hospitalizations",
		  "Property": "$.Patient"
		},
		"SourceValue": {
		  "Source": "Patients",
		  "Property": "$"
		},
		"LinkView": {
		  "InlineView": {
		  	...
		  }
		}
	}
}
```
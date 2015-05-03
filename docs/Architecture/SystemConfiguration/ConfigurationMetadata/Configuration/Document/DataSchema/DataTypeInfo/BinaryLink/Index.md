---
layout: default
title: "BinaryLink"
position: 0
categories: 
tags: 
---

Ссылка на двоичные данные.

   

Ссылка на двоичные данные определяет дополнительную информацию о свойствах с типом [[Binary|DataType]].

 

**Список допустимых форматов данных** (AcceptTypes) в формате [IANA Media Types](http://www.iana.org/assignments/media-types/media-types.xhtml) (MIME). Эта информация может быть использована, например, на уровне генератора представлений следующим образом: если встретился тип, который начинается с "image/", то пользователю будет отображен [[ImageBox]], в противном случае будет отображен [[UploadFileBox]]. Также можно настроить фильтр в диалоге выбора файла. Серверная сторона также может использовать эти данные, например, чтобы не позволять клиенту делать выгрузку файлов в недопустимом формате. Если список допустимых форматов данных не определен, допустимы данные любого типа.

 

**Максимальный размер данных в байтах** (MaxSize). Эта информация может быть использована, как на стороне клиента, так и на стороне сервера. Клиентская сторона может предупреждать пользователя о максимально допустимом размере файла, либо вообще не позволять выбирать файл большего размера. Серверная сторона может не позволять клиенту делать выгрузку файлов, размер которых превышает максимально допустимый. Если максимальный размер данных не определен, меньше или равен 0, допустимы данные любого размера. Тем не менее, нужно понимать, что серверная сторона может на уровне реализации установить максимальный размер данных.

 

**Разрешать ссылку на данные** (Resolve). Эта настройка отвечает за логику выборки документов, в котором присутствуют свойства с типом [[Binary|DataType]]. По умолчанию разрешение ссылки на данные выключено (Resolve=false). Когда клиент запросит у сервера данные документа, у полученного документа свойства с типом [[Binary|DataType]] с выключенным разрешением ссылок (Resolve=false), будут содержать структуру [[BlobData]] без свойство Data (иными словами, [[BlobData]].Data === undefined). Свойства с типом [[Binary|DataType]] с включенным разрешением ссылок (Resolve=true), будут содержать структуру [[BlobData]] со свойством Data (иными словами, [[BlobData]].Data !== undefined). Соответственно, в случае, когда данные (Data) с сервера не приходят (иными словами, [[BlobData]].Data === undefined), предполагается, что клиент сам решает, когда следует загружать данные. Для загрузки данных клиент отправляет серверу дополнительный запрос, передавая в параметрах запроса уникальный идентификатор BLOB ([[BlobData]].Info.Id). Наконец, свойства с типом [[Binary|DataType]], не имеющие значения, будут содержать нулевой указатель (null).  


   

```
{
	"id": "BinaryLink",
	"description": "Ссылка на двоичные данные",
	"type": "object",
	"properties": {
		"AcceptTypes": {
			"description": "Список допустимых форматов данных",
			"type": "array",
			"items": {
				"type": "string"
			}
		},
		"MaxSize": {
			"description": "Максимальный размер данных в байтах",
			"type": "integer",
			"default": 0
		},
		"Resolve": {
			"description": "Разрешать ссылку на данные",
			"type": "boolean",
			"default": false
		}
	}
}
```

 

 

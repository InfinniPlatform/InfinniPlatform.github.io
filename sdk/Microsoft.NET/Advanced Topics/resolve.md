---
layout: doc
title: "Getting documents with links"
position: 
categories: 
tags:
---

Получение документов, содержащих ссылки на другие документы.

## Description
При разработке модели данных документа можно указать два различных варианта указания типа ссылки на
другой документ в поле сохраняемого документа. 

* resolve
* inline

В зависимости от принятого решения изменяется поведение сервисов при выборке документов.

* Для варианта Resolve

## Behaviour
После осуществления выборки документов выполняется разрешение ссылок на документы в экземплярах 
документов, полученных в результате запроса, которое осуществляется следующим образом:
Анализируется значение ссылки, значение которого представлено в виде объекта:

### Document link example 
```js
{
	GameReference =	{
		Id : "622E92D1-F453-4838-9892-030865F90036",
		DisplayName : "GTA V Ultimate Edition"
	}
}
```

По идентификатору документа, указанному в ссылке, выполняется поиск документа в приложении, заданном
в маппинге поля схемы документа при создании этого типа документа. Полученный результат в виде
документа записывается в поле документа, заменяя вышеуказанную ссылку на документ.

### Document query result:
```js
{
	GameReference ={
		Id : "622E92D1-F453-4838-9892-030865F90036",
		Name : "GTA V Ultimate Edition",
		Price = 2000
		Availability = {
			Available = true,
		}
	}
}
```

* Для варианта Inline

## Behaviour
При указании типа ссылки на документ 'Inline' не выполняется дополнительных операций с полем 
документа, содержащим ссылку на другой документ. В этом случае непосредственно возвращается значение,
сохраненное в документе.

### Document link example 
```js
{
	GameReference =	{
		Id : "622E92D1-F453-4838-9892-030865F90036",
		DisplayName : "GTA V Ultimate Edition"
	}
}
```

### Query result
```js
{
	GameReference =	{
		Id : "622E92D1-F453-4838-9892-030865F90036",
		DisplayName : "GTA V Ultimate Edition"
	}
}
```

Поведение ссылки типа Inline применяется по умолчанию.
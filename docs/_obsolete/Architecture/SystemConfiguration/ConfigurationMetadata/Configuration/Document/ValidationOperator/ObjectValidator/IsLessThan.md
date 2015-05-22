---
layout: doc
title: "IsLessThan"
position: 13
categories: 
tags: 
---

Объект меньше заданного объекта.

 

```
{
	"id": "IsLessThan",
	"description": "Объект меньше заданного объекта",
	"type": "object",
	"extends": {
		"$ref": "http://wiki.infinnity.lan:8081/display/MC/BaseValidationOperator"
	},
	"properties": {
		"Message": {
			"description": "Сообщение об ошибке",
			"type": "string"
		},
		"Property": {
			"description": "Наименование свойства",
			"type": "string"
		},
		"Value": {
			"description": "Значение оператора",
			"type": "any",
			"oneOf": [
				{ "type": "integer" },
				{ "type": "numeric" }
			]
		}
	}
}
```

   

#### Пример #1

 

```
(target < 1234) 
```

```
{
	"Message": "Сообщение об ошибке, если условие не выполняется",
	"Value": 1234
}
```

```
// Given
var target1 = 123;
var target2 = 1234;
var target3 = 4321;
var validator = new IsLessThan { Message = "Error", Value = 1234 };
 
// When
string message1, message2, message3;
var result1 = validator.Validate(target1, out message1);
var result2 = validator.Validate(target2, out message2);
var result3 = validator.Validate(target3, out message3);
 
// Then
Assert.IsTrue(result1);
Assert.IsNull(message1);
Assert.IsFalse(result2);
Assert.AreEqual("Error", message2);
Assert.IsFalse(result3);
Assert.AreEqual("Error", message3);
```

   

#### Пример #2

 

```
(target.Property1 < 1234) 
```

```
{
	"Message": "Сообщение об ошибке, если условие не выполняется",
	"Property": "Property1",
	"Value": 1234
}
```

```
// Given
var target1 = new { Property1 = 123 };
var target2 = new { Property1 = 1234 };
var target3 = new { Property1 = 4321 };
var validator = new IsLessThan { Message = "Error", Property = "Property1", Value = 1234 } ;
 
// When
string message1, message2, message3;
var result1 = validator.Validate(target1, out message1);
var result2 = validator.Validate(target2, out message2);
var result3 = validator.Validate(target3, out message3);
 
// Then
Assert.IsTrue(result1);
Assert.IsNull(message1);
Assert.IsFalse(result2);
Assert.AreEqual("Error", message2);
Assert.IsFalse(result3);
Assert.AreEqual("Error", message3);
```

 

 

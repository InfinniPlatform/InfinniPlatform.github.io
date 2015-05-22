---
layout: doc
title: "BaseListGroup.DisplayProperty"
position: 3
categories: 
tags: 
---

Свойство элемента списка, которое хранит значение для отображения в заголовке группы.

Данная настройка игнорируется, если задано значение для [[ItemFormat|BaseListGroup.ItemFormat]].

   

Элементы списка могут быть сгруппированы по значению, которое может быть малопонятно пользователю, если его отображать в заголовке группы. Настройка DisplayProperty определяет декларативную функцию извлечения значимой части данных из элементов списка, которая будет отображена в загловке группы. Например, пользователь открывает список входящих сообщений. При этом в списке он хочет видеть сообщения, сгруппированные по категории. В этом случае атрибут DisplayProperty должен содержать наименование свойства с именем категории.

   

#### Examples

```
{
  "GroupTemplate": {
    "ValueProperty": "Category.Id",
    "DisplayProperty": "Category.Name"
  },
  "Items": {
    "ObjectBinding": {
      "Value": [
        { "Category": { "Id": 1, "Name": "Важные" }, "Title": "Message 1" },
        { "Category": { "Id": 2, "Name": "Соцсети" }, "Title": "Message 2" },
        { "Category": { "Id": 3, "Name": "Оповещения" }, "Title": "Message 3" }
      ]
    }
  }
}
```

 

 

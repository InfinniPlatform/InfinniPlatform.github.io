---
layout: doc
title: "BaseMessage"
position: 0
categories: 
tags: 
---

Базовый класс для тела сообщения.

 

В качестве источника сообщения (см. Source) передается ссылка на элемент представления, который был источником соответствующего сообщения. В явном виде данное значение использовать не рекомендуется, поскольку источником сообщения может быть кто угодно. Данное значение добавлено лишь для облегчения процесса отладки. С сообщением также может быть связано контекстно-зависимое значение (см. Value), которое может использоваться при обработке сообщения.

   

#### Schema

```
{
  "id": "BaseMessage",
  "description": "Базовый класс для тела сообщения",
  "type": "object",
  "properties": {
    "Source": {
      "description": "Источник сообщения",
      "type": "any"
    },
    "Value": {
      "description": "Контекстно-зависимое значение",
      "type": "any"
    }
  }
}
```

 

 

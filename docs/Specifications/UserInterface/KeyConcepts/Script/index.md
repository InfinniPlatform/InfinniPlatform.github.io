---
layout: doc
title: "Script"
position: 7
---

Прикладной скрипт - функция, выполняемая на стороне клиента.

## Description

Чаще всего прикладные скрипты используются в качестве обработчиков событий элементов представления,
но могут выступать и в качестве повторно используемых функций, вызываемых из любого другого скрипта.

Прикладной скрипт представляет собой функцию с двумя параметрами: `context` и `argument`. Наименования
параметров жестко определены и используются в рамках скрипта, как системные переменные. В параметре
`context` передается [контекст представления](../ViewContext/), в параметре `argument` - дополнительная
информация, необходимая для выполнения скрипта.

Для каждого события системы структура данных аргумента предопределена. Тем не менее, аргумент обработчика
любого события всегда содержит свойство `source`, в котором передается источник события. Например,
обработчику события нажатия на кнопку в свойстве `argument.source` будет передана ссылка на нажатую
кнопку.

Если прикладной скрипт является пользовательской функцией, а не обработчиком какого-либо события, то
разработчик сам определяет то, что будет предаваться в качестве аргумента.

## Syntax

```js
function(context, argument)
```

### Parameters

`context`

[Контекст представления](../ViewContext/).

`argument`

Аргумент скрипта.
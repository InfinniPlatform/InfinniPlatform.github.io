---
layout: doc
title: "DateTimeFormat"
position: 1020
---

Формат отображения даты/времени. Строка форматирования должна записываться в формате, который описан в разделе [`dateTimeFormatting`](../../Localizations/Localizations.dateTimeFormatting/).

# Extends

[`BaseFormat`](../BaseFormat).

# Example

```js
//js-demo
format = new DateTimeFormat();
format.setFormat('dd-MM-yyyy');

$elementForExample.append(format.formatValue(new Date()));
```

# See also

[`dateTimeFormatting`](../../Localizations/Localizations.dateTimeFormatting/)

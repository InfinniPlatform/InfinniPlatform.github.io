---
layout: doc
title: "NumberFormat"
position: 1020
---

Формат отображения числового значения. Строка форматирования должна записываться в формате, который описан в разделе [`numberFormatting`](../../Localizations/Localizations.numberFormatting/).

# Extends

[`BaseFormat`](../BaseFormat).

# Example

```js
//js-demo
format = new NumberFormat();
format.setFormat('n2');

$elementForExample.append(format.formatValue(1/3));
```

# See also

[Настройки форматирования для числового значения](../../Localizations/Localizations.numberFormatting/)

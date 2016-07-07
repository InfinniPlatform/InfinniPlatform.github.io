---
layout: doc
title: "BaseDataSource.getWarningValidator()"
position: 14
---

Возвращает [функцию](../../../Script/) проверки элемента на предупреждения.

# Description

[Функция](../../../Script/) проверки элемента на предупреждения в параметре `args` принимает
элемент источника данных, который необходимо проверить. Результатом работы функции является объект
[предопределенного формата](../ValidationResult/).

# Syntax

```js
BaseDataSource.getWarningValidator()
```

## Parameters

Нет

## Returns

[Функция](../../../Script/) проверки элемента на предупреждения.

# Examples

```js
var warningValidator = BaseDataSource.getWarningValidator();
```

# See Also

* [`setWarningValidator()`](../BaseDataSource.setWarningValidator/)
* [`getErrorValidator()`](../BaseDataSource.getErrorValidator/)
* [`setErrorValidator()`](../BaseDataSource.setErrorValidator/)
* [`validateOnWarnings()`](../BaseDataSource.validateOnWarnings/)
* [`ValidationResult`](../ValidationResult/)
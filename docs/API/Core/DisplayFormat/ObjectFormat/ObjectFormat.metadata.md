---
layout: doc
title: "ObjectFormat.metadata"
position: 0
---

Метаданные типа [`ObjectFormat`](../).

# Properties

Name|Type|Default|Description
----|----|-------|-----------
Format|`String`||[Строка форматирования объекта](../ObjectFormat.format).


# Examples

```json
{
  "Format": "${:n2}"
}
```

```json
{
  "Format": "Birth date: ${BirthDate:d}"
}
```

```json
{
   "Format": "Weight: ${Weight:n2} kg"
}
```

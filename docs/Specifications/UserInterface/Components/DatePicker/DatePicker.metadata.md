---
layout: doc
title: "DatePicker.metadata"
position: 0
---

Метаданные типа [`DatePicker`](../).

# Schema

{% include github.html path="InfinniPlatform.Api/MetadataSchema/UI/Components/DatePicker/DatePicker.resjson" lang="json" %}

# Examples

```json
{
  "LabelText": "Birthday",
  "LabelFloating": true,
  "Value": {
    "Source": "mainDataSource",
    "Property": "$.Birthday"
  }
}
```
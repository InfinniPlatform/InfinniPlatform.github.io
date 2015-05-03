---
layout: default
title: "Реализация IndexApi (Low - level API)"
position: 
categories: 
tags: 
---

IndexApi платформы содержит средства для работы с данными хранилища на низком уровне.

В состав этого Api входят методы для выполнения операций вставки, обновления, удаления, редактирования любых элементов в хранилище, а также методы, реализующие административные операции работы с хранилищем (пересоздание индекса, очистка, проверка существования)

Данный Api предназначен для предоставления возможности создания низкоуровневых административных конфигураций и написания тестов для прикладных конфигураций, в ходе которых требуется низкоуровневая обработка индексов хранилища.

Содержит следующие операции:

* Операция пересоздания индекса (RebuildIndex)
* Операция проверки существования индекса (IndexExists)
* Операция очистки индекса (ClearIndex)
* Операция получения элемента из индекса (GetFromIndex)
* Операция вставки элемента в индекс (InsertDocument)
* Операция вставки элемента в индекс с необходимой меткой времени вставки (InsertDocumentWithTimestamp)

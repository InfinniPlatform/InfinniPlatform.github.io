---
layout: doc
title: "ViewContext"
position: 1003
---

Контекст представления - программный объект, который хранит состояние представления и предоставляет
строго определенный API для доступа к элементам представления. Вызов любого прикладного скрипта или
обработчика события сопровождается передачей ему контекста представления. Контекст создается для
каждого экземпляра представления и время его жизни определяется временем жизни соответствующего
экземпляра представления.

# Properties

|Name|Description|
|----|---------|
|[`view`](ViewContext.view/)|Возвращает [представление](../Elements/View/) контекста|
|[`global`](ViewContext.global/)|Возвращает [глобальный контекст приложения](../GlobalContext/)|
|[`messageBus`](ViewContext.messageBus/)|Возвращает [шину сообщений представления](../MessageBus/)|
|[`scripts`](ViewContext.scripts/)|Возвращает ассоциативный список [скриптов представления](../Script/)|
|[`parameters`](ViewContext.parameters/)|Возвращает ассоциативный список [параметров представления](../Parameters/)|
|[`dataSources`](ViewContext.dataSources/)|Возвращает ассоциативный список [источников данных представления](../DataSources/BaseDataSource/)|
|[`controls`](ViewContext.controls/)|Возвращает ассоциативный список [визуальных элементов представления](../Elements/Element/)|

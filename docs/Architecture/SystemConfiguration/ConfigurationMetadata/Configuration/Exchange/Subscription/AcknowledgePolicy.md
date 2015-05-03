---
layout: default
title: "AcknowledgePolicy"
position: 1
categories: 
tags: 
---

Политика подтверждения окончания обработки сообщения.

 

Подтверждение окончания обработки сообщения сигнализирует серверу очереди сообщений о том, что сообщение обработано и может быть удалено из очереди. Если сообщение было прочитано, но подтверждения об окончании не поступило, оно остается на сервере до тех пор, пока не поступит сигнал подтверждения. Это может обеспечить определенную устойчивость к сбоям, которые могут возникнуть на стороне потребителя. В свою очередь отправитель сообщения может получить уведомление о том, что оно было получено и обработано.

   

|Значение|Наименование|Описание|
|--------|------------|--------|
|AlwaysAfterHandling|Всегда после обработки.|Политика подтверждения окончания выполнения действия, при которой подтверждение осуществляется после выполнения действия, вне зависимости от результата выполнения.|
|AlwaysBeforeHandling|Всегда перед началом обработки.|Политика подтверждения окончания выполнения действия, при которой подтверждение осуществляется перед выполнением действия.|
|OnlyOnSuccessHandling|Только после успешной обработки.|Политика подтверждения окончания выполнения действия, при которой подтверждение осуществляется только после успешного выполнения действия.|

   

```
{
	"id": "AcknowledgePolicy",
	"description": "Политика подтверждения окончания обработки сообщения",
	"enum": [
		"AlwaysAfterHandling",
		"AlwaysBeforeHandling",
		"OnlyOnSuccessHandling"
	]
}
```

 

 

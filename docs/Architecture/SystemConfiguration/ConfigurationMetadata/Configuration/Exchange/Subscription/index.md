---
layout: doc
title: "Subscription"
position: 
categories: 
tags: 
---

Подписка точки обмена сообщениями.

 

Уникальный идентификатор обработчика очереди сообщений (см. ConsumerId) является необязательным атрибутом и носит исключительно прикладной характер, чтобы на уровне скрипта обработчика сообщения уникально идентифицировать подписчика.

Ключ маршрутизации очереди сообщений (см. RoutingKey) определяет правило маршрутизации сообщений данному подписчику. Атрибут является обязательным, если соответствующая точка обмена имеет тип "Direct" или "Topic" (см. [[ExchangeType]]).

**Для точек обмена с типом "Direct".** При формировании ключа маршрутизации используются следующие соглашения. Ключ должен быть пустым, либо состоять из слов, разделенных точками. Каждое слово может содержать симоволы из набора [a-zA-Z0-9].

**Для точек обмена с типом "Topic".** При формировании шаблона маршрутизации используются следующие соглашения. Шаблон должен быть пустым, либо состоять из слов, разделенных точками. Каждое слово может содержать символы из набора [a-zA-Z0-9]. Дополнительно могут быть использованы специальные символы: * - означает одно слово, # - означает любое количество слов.

Заголовок маршрутизации очереди сообщений (см. RoutingHeaders) определяет правило маршрутизации сообщений данному подписчику. Атрибут является обязательным, если соответствующая точка обмена имеет тип "Headers" (см. [[ExchangeType]]).

Максимальный размер одновременно обрабатываемых сообщений (см. PrefetchSize) по умолчанию равен 0, что соответствует неограниченному размеру. Данное значение не должно быть меньше 0.

Максимальное количество одновременно обрабатываемых сообщений (см. PrefetchCount) по умолчанию равен 0, что соответствует неограниченному количеству. Данное значение не должно быть меньше 0.

Количество рабочих потоков для обработки очереди сообщений (см WorkerThreadCount) не должно быть меньше 1. Значение этого атрибута не должно превышать количества ядер CPU машины, на которой развернута система.

Минимальное время прослушивания очереди (см. MinListenTime) - время, которое не считается сетевым сбоем. Данное значение измеряется в миллисекундах и не должно быть меньше 1, однако задавать это значение достаточно малым крайне не желательно.

Политика подтверждения окончания обработки сообщения (см. AcknowledgePolicy). Подтверждение окончания обработки сообщения сигнализирует серверу очереди сообщений о том, что сообщение обработано и может быть удалено из очереди. Если сообщение было прочитано, но подтверждения об окончании не поступило, оно остается на сервере до тех пор, пока не поступит сигнал подтверждения. Это может обеспечить определенную устойчивость к сбоям, которые могут возникнуть на стороне потребителя. В свою очередь отправитель сообщения может получить уведомление о том, что оно было получено и обработано.

Политика подтверждения отказа от обработки сообщения (см. RejectPolicy). Отказ от обработки сообщения может использоваться в случае, когда потребитель не готов по каким-либо причинам обработать данное сообщение. В этом случае сервер очереди сообщений попытается отправить это сообщение другому потребителю. И так до тех пор, пока сообщение не будет обработано и серверу не поступит сигнал подтверждения. Однако это абсолютно не гарантирует того, что потребитель, который когда-либо отказался от обработки данного сообщения, никогда не получит его снова. Механизм отказа от обработки сообщения ни в коем случае не следует использовать для отсеивания ненужных сообщений. Например, отказ может произойти по причине слишком большой загруженности узла, на котором осуществляется обработка.

Ссылка на скрипт (см. Handler) требует более подробного описания.

   

```
{
	"id": "Subscription",
	"description": "Подписка точки обмена сообщениями",
	"type": "object",
	"extends": {
		"$ref": "http://demo.infinnity.ru:8081/display/MC/ObjectMetadata"
	},
	"properties": {
		"ConsumerId": {
			"description": "Уникальный идентификатор обработчика очереди сообщений",
			"type": "string"
		},
		"RoutingKey": {
			"description": "Ключ маршрутизации очереди сообщений",
			"type": "string"
		},
		"RoutingHeaders": {
			"description": "Заголовок маршрутизации очереди сообщений",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/MessageHeaders"
		},
		"PrefetchSize": {
			"description": "Максимальный размер одновременно обрабатываемых сообщений",
			"type": "int",
			"minimum": "0"
		},
		"PrefetchCount": {
			"description": "Максимальное количество одновременно обрабатываемых сообщений",
			"type": "integer",
			"minimum": "0"
		},
		"WorkerThreadCount": {
			"description": "Количество рабочих потоков для обработки очереди сообщений",
			"type": "integer",
			"minimum": "1"
		},
		"MinListenTime": {
			"description": "Минимальное время прослушивания очереди, которое не считается сетевым сбоем",
			"type": "integer",
			"minimum": "1"
		},
		"AcknowledgePolicy": {
			"description": "Политика подтверждения окончания обработки сообщения",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/AcknowledgePolicy"
		},
		"RejectPolicy": {
			"description": "Политика подтверждения отказа от обработки сообщения",
			"$ref": "http://demo.infinnity.ru:8081/display/MC/RejectPolicy"
		},
		"Handler": {
			"description": "Ссылка на скрипт обработчика сообщения",
			"$ref": "???"
		}
	}
}
```

 

 

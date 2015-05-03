---
layout: default
title: "Infinni Platform Overview"
position: 0
categories: 
tags: 
---

## Общее резюме проекта

Infinni Platform 1.0 представляет собой платформу для разработки корпоративных бизнес-приложений, к которым выдвигаются следующие требования:

* Высокий уровень производительности и надежности при операциях хранения, получения и обработки больших массивов данных
* Обеспечение возможности реализации сложной прикладной бизнес-логики, характерной для ERP, MRP, ERM и CRM систем
* Поддержка функционала, необходимого для быстрой разработки Web-приложений, с поддержкой современных стандартов (HTML5, CSS3)

В рамках решения данных задач платформу можно разделить на серверную и клиентскую часть. 

Клиентская часть платформы содержит механизмы рендеринга метаданных представлений, созданных в соответствующих прикладных конфигурациях. Клиентская часть платформы абстрагирует разработчика от разработки интерфейса на JavaScript/HTML5, позволяя ускорить создание стандартных интерфейсов пользователя, используемых для реализации рутинных сценариев, таких как просмотр, добавление, редактирование и выбор данных из списка.

Серверная часть платформы содержит механизмы для обнаружения и загрузки *прикладных конфигураций. *Каждая прикладная конфигурация представляет собой отдельный проект на C# (Class Library), имеющий определенную структуру, поддерживаемую соглашениями о структуре прикладного проекта и разрабатываемый с использованием IDE Microsoft Visual Studio 2012-2013. Проекты прикладных конфигураций не зависят от платформы, но могут использовать API и компоненты, предоставляемые при запуске C# модулей прикладной бизнес-логики. Прикладные конфигурации также не зависят от их представления на клиенте. Все это в совокупности позволяет обеспечить низкий уровень связности (low-couple) между различными элементами платформы и прикладными конфигурациями.

### Серверная часть платформы

Серверная часть платформы имеет модульную сервисно-ориентированную архитектуру. Взаимодействие с модулями платформы осуществляется с использованием современной REST - архитектуры ([https://ru.wikipedia.org/wiki/REST](https://ru.wikipedia.org/wiki/REST)). Каждый модуль системы предоставляет определенный аспект функциональности. Модули являются независимыми друг от друга, каждый модуль предоставляет API для работы с этим модулем. ([https://ru.wikipedia.org/wiki/Интерфейс_программирования_приложений](https://ru.wikipedia.org/wiki/Интерфейс_программирования_приложений)). 

На данный момент модули системы покрывают следующие аспекты функциональности:

### Модуль развертывания сервисов

* Обеспечение platform-independent хостинга сервисов REST на базе Microsoft ASP.NET Katana Project - OWIN implementations for Microsoft servers and frameworks ([http://katanaproject.codeplex.com/](http://katanaproject.codeplex.com/))
* Реализация роутинга запросов REST на базе ASP.NET Web API 2.0
* Поддержка развертывания сервисов с использованием протокола http и защищенного протокола https
* Возможность горизонтального масштабирования с использованием load balancer
* Высокий уровень абстракции сервисной модели от конкретной реализации на базе ASP.NET Web 2.0
* Наличие большого числа шаблонов сервисов из коробки
* Простая настройка и добавление новых шаблонов сервисов
* Визуальный конструктор сервисов 

### Модуль работы с распределенным хранилищем данных

* Горизонтально масштабируемое хранилище данных на базе ElasticSearch v. 1.4/ DataStax Cassandra v 2.0
* Расширенные возможности поиска данных
* Поддержка JSON схем хранимых данных с возможностью визуального редактирования
* Возможность хранения простых типов данных и данных большого размера (изображения/аудио/видео)
* Быстрота и удобство конфигурирования хранилища

### Модуль поддержки версионности

* Поддержка нескольких JSON схем одних и тех же хранимых данных (поддержка версионности для JSON схем данных)
* Поддержка работы с несколькими версиями конфигураций (например, необходимыми для работы с ранее созданными документами)
* Прозрачная для разработчика модель версионности данных

### Модуль обеспечения режима SaaS

* Предоставление сервисов платформы по модели SaaS
* Поддержка multi-tenancy из коробки

### Модуль логирования операций

* Ведение истории вызовов сервисов в файл/базу данных/консоль
* Профилирование производительности вызова операций прикладной бизнес-логики
* Включение и отключение операций профилирования и логирования в режиме онлайн. 

### Модуль безопасности

* Прозрачная для разработчика модель безопасности из коробки
* Наличие собственного хранилища пользователей
* Система аутентификации пользователя, поддерживающая встроенный провайдер безопасности на основе внутреннего хранилища, а также внешние провайдеры безопасности (Google, Twitter).
* Система авторизации пользователя, позволяющая устанавливать права пользователей на любом уровне работы с прикладной конфигурацией
* Наличие визуальных средств для администрирования пользователей, ролей и прав доступа

### Модуль поддержки пользовательских оповещений

* Нотификация клиента со стороны сервера о произошедших на стороне сервера изменениях (клиентская нотификация) на базе технологии Microsoft SignalR
* Поддержка всех современных браузеров

### Модуль поддержки миграций (обработок)

* Обеспечение безопасного перехода на новую версию при обновлении
* Предоставляет механизм централизованного изменения данных
* Визуальные средства настройки механизма миграций (обработок)

### SDK для работы c API платформы

* Предоставляет инфраструктуру на языке C#, доступную для использования в прикладных конфигурациях для работы со всеми аспектами платформы
* Предоставляет DocumentAPI (API для сохранения, удаления, загрузки и редактирования документов)
* Предоставляет PrintViewAPI (API для генерации печатных форм документов в формате pdf)
* Предоставляет ReportAPI (API для генерации отчетов)
* Предоставляет RegisterAPI (API для работы с регистрами)
* Предоставляет UploadAPI (API для загрузки и выгрузки прикладных конфигураций на сервер)
* Предоставляет AclApi (API для работы с пользователями, ролями и правами пользователей)
* Предоставляет AdminAPI (API для предоставления роли администратора системы)
* Предоставляет SignInAPI (API для входа (аутентификации) и выхода в системы)
* Вызов всех API представляет собой обращение к соответствующим сервисам REST, реализованным на базе функционала платформы
* Предоставляет ряд компонентов, доступных для использования в бизнес-логике прикладных конфигураций, вызываемых внутрипроцессно, в том числе:  * Компонент для работы с хранилищем бинарных (изображения, видео- и аудио- контент)
  * Компонент для работы с хранилищем событий изменения документов (ведение истории изменения документов, получение дампов для симуляции пользовательских событий)
  * Компонент для работы с хранилищем данных на низком уровне абстракции (работа на уровне записи в базе данных ElasticSearch)
  * Компонент для логирования сообщений
  * Компонент для получения указанных метаданных конфигураций
  * Компонент для поиска данных среди различных документов различных прикладных конфигураций
  * Компонент для получения печатных форм документов
  * Компонент для профилирования событий пользовательской бизнес-логики
  * Компонент для работы с регистрами
  * Компонент для ручного запуска пользовательских скриптов, зарегистрированных в конфигурации
  * Компонент для ручного обновления пользователей, ролей и утверждений относительно пользователей
  * Компонент для управления транзакциями документов
  * Компонент для выполнения клиентской нотификации о произошедших на стороне сервера изменениях



### Модуль загрузки, автоматического развертывания и обновления конфигураций

* Предоставляет средства загрузки прикладных конфигураций из архивов в формате zip, содержащих *метаданные* *прикладной конфигурации.*
* Предоставляет средства экспорта прикладных конфигураций на диск и/или в архив в формате zip.
* Обширные средства автоматического обновления системы, позволяющие выполнять развертывание новой версии конфигурации одним кликом.
* Возможность обновления на нужную версию прикладной конфигурации.
* Визуальные средства администрирования конфигураций
* Поддержка механизмов удаленного развертывания конфигураций с использованием защищенных паролем соединений REST 

### Модуль дизайнера 

* Предоставляет визуальные средства для создания метаданных прикладных конфигураций
* Предоставляет визуальные средства для добавления и подключения модулей прикладной бизнес-логики на языке C#
* Предоставляет визуальные средства для редактирования JSON схем данных
* Предоставляет визуальные средства для создания новых экземпляров сервисов REST по правилам, описываемым платформой
* Предоставляет визуальные средства для создания печатных форм документов
* Предоставляет визуальные средства для создания отчетов
* Предоставляет визуальные средства для создания визуальных форм просмотра, добавления, редактирования и выбора данных

Данный документ является описанием высокоуровневых абстракций, реализуемых платформой и предназначен для использования руководителями проектов, разработчиками платформы и разработчиками прикладных конфигураций на базе платформы

 

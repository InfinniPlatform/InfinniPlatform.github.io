---
layout: doc
title: "Создание экранных форм"
position: 
categories: 
tags: 
---

Чтобы с документом можно было работать, необходимо создать экранную форму (View).

Создание: Document -> Contents->Add->View

Экранных форм одного типа может быть несколько.

**Шаг 1**. Заполнить поля вкладки General

|Название поля|Чем заполнять?|Ограничения|
|Наименование|Название экранной формы|Язык: английскийУникально в рамках документа.Обычно дублирует тип.|
|Заголовок|Отображается в перечне Views| |
|Описание|Описание| |
|Тип формы|* ListView - журнал
* EditView – форма редактирования
* SelectView – форма выбора
* HomePage – домашняя страница
* Menu – меню

| |
|Выберите шаблон|Шаблон для генерации метаданных.На текущий момент существуют шаблоны:* ListView
* EditView

|Тип шаблона должен совпадать с типом View|

 

**Шаг 2.** Нажать на кнопку Сформировать (сгенерируются метаданные view)

В появившемся диалоговом окне прописать тип документа:

{

"Type":"Название документа"

}

 

**Шаг 3.** Перейти на вкладку Metadata, проверить корректность сформированных данных

Для редактирования метаданных необходимо нажать Edit.

Для сохранения изменений: Apply -> Save

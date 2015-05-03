---
layout: default
title: "Ссылка на представление"
position: 0
categories: 
tags: 
---

Ссылка на представление (см. раздел [[LinkView]]) является часто используемым элементом при описании действий (см. раздел [[Action]]). Метаданные ссылки на представление определяют какое представление (существующее, автогенерированное и т.д.) и как (в диалоговом окне, в отдельной вкладке и т.д.) следует открыть. Существует несколько типов ссылок на представление, которые определяют какое представление следует открыть, фактически, откуда взять метаданные открываемого представления. Например, ссылка на представление с типом [[ExistsView]] определяет ссылку на существующее представление, то есть метаданные этого представления будут взяты с сервера, из указанной конфигурации. Ссылка на представление с типом [[InlineView]] хранит метаданные представления непосредственно внутри ссылки (так называемое, встроенное представление - представление, объявленное внутри другого представления). Также существует несколько способов открытия представления, каждый из которых описан в разделе [[OpenMode]].

Ссылка на представление должна реализовывать API, описанный в разделе [[BaseLinkView]]. Ниже приведен пример программной реализации ссылки на представления. Пример сделан в объектно-ориентированном стиле и содержит только часть кода, которая не содержит платформенную специфику и демонстрирует общий подход. При создании ссылки на представление, в конструктор передается: appView - экземпляр представления приложения (главное окно приложения), parentView - экземпляр родительского представления (где была объявлена ссылка), viewFactory - фабричный метод, который извлекает метаданные представления и создает его экземпляр. При вызове метода GetView(), если представление не создано, оно создается, иначе возвращается существующий экземпляр. Метод OpenView() открывает и показывает представление на экране, анализируя способ открытия представления.

```
class LinkView
{
	public LinkView(View appView, View parentView, Func<View> viewFactory)
	{
		_appView = appView;
		_parentView = parentView;
		_viewFactory = viewFactory;
	}
 
	private readonly View _appView;
	private readonly View _parentView;
	private readonly Func<View> _viewFactory;
 
 
	private OpenMode _openMode;
 
	public OpenMode GetOpenMode()
	{
		return _openMode;
	}
  
	public void SetOpenMode(OpenMode value)
	{
		_openMode = value;
	}
 
 
	private View _view;
 
	public View GetView()
	{
		if (_view == null)
		{
			_view = _viewFactory();
		}

		return _view;
	}
 
	public void OpenView()
	{
		var view = GetView();
 
		if (view != null)
		{
			switch (_openMode)
			{
				case OpenMode.TabPage:
					OpenViewInTabPage(view, _parentView);
					break;
				case OpenMode.AppTabPage:
					OpenViewInTabPage(view, _appView);
					break;
				default:
					OpenViewInDialog(view, _parentView);
					break;
			}
		}
		return view;
	}
 
	private void OpenViewInDialog(View view, View parent)
	{
		/* Платформенно-зависимый код */
	}
 
	private void OpenViewInTabPage(View view, View parent)
	{
		/* Платформенно-зависимый код */
	}
}
```

 

Пример построителя элемента для [[ExistsView]] приведен ниже. Метод Build() создает ссылку на представление, устанавливает определенный в метаданных способ открытия представления и возвращает результат. При создании ссылки в конструктор передается экземпляр главного окна приложения, экземпляр родительского представления, а также функция по созданию экземпляра представления, для которого определена ссылка. В итоге представление будет создано только тогда, когда в этом возникнет необходимость.

```
class ExistsViewElementBuilder
{
	object Build(factory, view, metadataValue)
	{
		var linkView = new LinkView(factory.AppView, view, function() {
			CreateView(factory, view, metadataValue);
		});
 
		linkView.SetOpenMode(metadataValue.OpenMode);
 
		return linkView;
	}
 
	object CreateView(factory, view, metadataValue)
	{
		var existsViewMetadata = LoadViewMetadata(metadataValue.ConfigId, metadataValue.ViewId);
		var existsView = factory.Build(view, "View", viewMetadata);
 
		...
 
		return existsView;
	}
 
	object LoadViewMetadata(configId, viewId)
	{
		/* Загрузка метаданных представления */
	}
}
```

 

 

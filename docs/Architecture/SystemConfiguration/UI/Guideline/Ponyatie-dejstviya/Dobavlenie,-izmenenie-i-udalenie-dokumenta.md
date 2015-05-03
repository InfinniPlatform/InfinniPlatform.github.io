---
layout: default
title: "Добавление, изменение и удаление документа"
position: 2
categories: 
tags: 
---

Пожалуй, это самый часто задаваемый вопрос при реализации интерпретатора метаданных. Ниже приведен код построителей для действий [[AddAction]], [[EditAction]] и [[DeleteAction]].

```
class AddActionElementBuilder
{
	object Build(factory, view, metadataValue)
	{
		return new Command(() => ExecuteAction(factory, view, metadataValue));
	}
 
	void ExecuteAction(factory, view, metadataValue)
	{
		// Определение источника данных родительского представления
		var listDataSource = view.GetDataSource(metadataValue.DataSource);
 
		if (listDataSource != null)
		{
			var idProperty = listDataSource.GetIdProperty();
 
			if (idProperty != null && idProperty != "")
			{
				// Создание ссылки на дочернее представление для редактирования агрегата
				var linkView = factory.Build(view, metadataValue.View);
 
				if (linkView != null)
				{
					var editView = linkView.GetView();
					var editDataSources = editView.GetDataSources();
 
					if (editDataSources != null)
					{
						// Получение источника данных дочернего представления для передачи
						// информации о редактируемом агрегате (передачи его идентификатора)
						var editDataSource = editDataSources.FirstOrDefault();
 
						if (editDataSource != null)
						{
							var editItemFilter = [
								{
									Property = idProperty,
									CriteriaType = "IsEquals",
									Value = null,
								}
							];
 
							editDataSource.SetPropertyFilters(editItemFilter);
						}
					}
 
					// Отображение дочернего представления (в текущей реализации никаких
					// действий после его закрытия не происходит, так как не ясно, как
					// лучше обновлять родительское представление; возможно, в дальнейшем
					// для этих целей нужно будет расширить метаданные EditAction)
					linkView.OpenView();
				}
			}
		}
	}
}
 
 
class EditActionElementBuilder
{
	object Build(factory, view, metadataValue)
	{
		return new Command(() => ExecuteAction(factory, view, metadataValue));
	}
 
	void ExecuteAction(factory, view, metadataValue)
	{
		// Определение источника данных родительского представления
		var listDataSource = view.GetDataSource(metadataValue.DataSource);
 
		if (listDataSource != null)
		{
			// Определение выделенного элемента в родительском представлении 
			var editItem = listDataSource.GetSelectedItem();
			var idProperty = listDataSource.GetIdProperty();
 
			if (editItem != null && idProperty != null && idProperty != "")
			{
				// Определение уникального идентификатора выделенного элемента, поскольку родительское
				// представление может отображать только проекцию данных редактируемого агрегата
				var editItemId = editItem.GetProperty(idProperty);
 
				if (editItemId != null)
				{
					// Создание ссылки на дочернее представление для редактирования агрегата
					var linkView = context.Build(parent, metadataValue.View);
					if (linkView != null)
					{
						var editView = linkView.GetView();
						var editDataSources = editView.GetDataSources();
 
						if (editDataSources != null)
						{
							// Получение источника данных дочернего представления для передачи
							// информации о редактируемом агрегате (передачи его идентификатора)
							var editDataSource = editDataSources.FirstOrDefault();
 
							if (editDataSource != null)
							{
								var editItemFilter = [
									{
										Property = idProperty,
										CriteriaType = "IsEquals",
										Value = editItemId
									}
								];
 
								editDataSource.SetPropertyFilters(editItemFilter);
							}
						}
 
						// Отображение дочернего представления (в текущей реализации никаких
						// действий после его закрытия не происходит, так как не ясно, как
						// лучше обновлять родительское представление; возможно, в дальнейшем
						// для этих целей нужно будет расширить метаданные EditAction)
						linkView.OpenView();
					}
				}
			}
		}
	}
}
 
 
class DeleteActionElementBuilder
{
	object Build(factory, view, metadataValue)
	{
		return new Command(() => ExecuteAction(factory, view, metadataValue));
	}
 
	void ExecuteAction(factory, view, metadataValue)
	{
		// Определение источника данных родительского представления
		var listDataSource = view.GetDataSource(metadataValue.DataSource);
 
		if (listDataSource != null)
		{
			// Определение выделенного элемента в родительском представлении 
			var editItem = listDataSource.GetSelectedItem();
			var idProperty = listDataSource.GetIdProperty();
 
			if (editItem != null && idProperty != null && idProperty != "")
			{
				// Определение уникального идентификатора выделенного элемента, поскольку родительское
				// представление может отображать только проекцию данных редактируемого агрегата
				var editItemId = editItem.GetProperty(idProperty);
 
				if (editItemId != null && (metadata.Accept == false || MessageBox("Удалить выделенный элемент?") == "Yes"))
				{
					var arguments = 
						{
							Source = view,
							DataSource = metadataValue.DataSource,
							Value = editItemId
						};
 
					view.GetExchange().SendAsync("OnDeleteItem", arguments);
				}
			}
		}
	}
}
```

 

 

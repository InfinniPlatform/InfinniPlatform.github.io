---
layout: doc
title: "View.metadata"
position: 0
---

Метаданные типа [`View`](../).

# Properties

|Name|Type|Default|Description|
|----|----|-------|-----------|
|Scripts|`Array`| |Коллекция [скриптов представления](../../../Script/)|
|Parameters|`Array`| |Коллекция [параметров представления](../../../Parameters/)|
|DataSources|`Array`| |Коллекция [источников данных представления](../../../DataSources/BaseDataSource/)|
|HeaderTemplate|[ElementMetadata](../../Element/Element.metadata/)| |Шаблон заголовка представления|
|CloseButtonVisibility|`Boolean`|true|Флаг видимости кнопки закрытия|
|NotificationSubsriptions|`Object`| |Объект подписок для signalR|
|OnOpening|[`Script`](../../../Script/)| |Обработчик события о том, что представление открывается|
|OnOpened|[`Script`](../../../Script/)| |Обработчик события о том, что представление было открыто|
|OnClosing|[`Script`](../../../Script/)| |Обработчик события о том, что представление закрывается|
|OnClosed|[`Script`](../../../Script/)| |Обработчик события о том, что представление было закрыто|

# Examples

```json
{
  "View": {
    "CloseButtonVisibility": false,
    "NotificationSubsriptions": {
      "routingKey1": "{ console.log( args.message ) }",
      "routingKey2": "{ console.log( args.message ) }",
      "routingKey3": "{ console.log( args.message ) }"
    },
    "HeaderTemplate": {
      "StackPanel": {
        "Items": [
          {
            "ToolBar": {
              "Items": [
                {
                  "ToolBarButton": {
                    "ContentTemplate": {
                      "Icon": {
                        "Value": "times"
                      }
                    },
                    "Name": "CloseButton",
                    "OnClick": "{context.view.close();}"
                  }
                }
              ]
            }
          },
          {
            "StackPanel": {
              "Items": [
                {
                  "Icon": {
                    "Value": "pencil"
                  }
                },
                {
                  "Label": {
                    "Text": "EditView"
                  }
                }
              ]
            }
          }
        ]
      }
    },

    "DataSources": [
      {
        "ObjectDataSource": {
          "Name": "MainDataSource",
          "Items": [
            {}
          ]
        }
        }
    ],

    "Scripts": [
      {
        "Name": "OnOpened",
        "Body": "alert('Hi!');"
        }
    ],

    "OnOpened": {
        "Name": "OnOpened"
    },

    "Items": [
      {
        "Label": {
          "Text": "ViewBody"
        }
      }
    ]
  }
}
```

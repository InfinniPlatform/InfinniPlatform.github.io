---
layout: doc
title: "ApplicationUser"
position: 0
categories: 
tags: 
---

Сведения о пользователе системы.

   

```
{
	"Type": "Object",
	"Caption": "Сведения о пользователе системы",
	"Properties": {
		"Id": {
			"Type": "Uuid",
			"Caption": "Уникальный идентификатор пользователя"
		},
		"UserName": {
			"Type": "String",
			"Caption": "Уникальное имя пользователя"
		},
		"DisplayName": {
			"Type": "String",
			"Caption": "Отображаемое имя пользователя"
		},
		"Description": {
			"Type": "String",
			"Caption": "Описание пользователя"
		},
		"PasswordHash": {
			"Type": "String",
			"Caption": "Хэш пароля пользователя",
			"Description": "Пароли пользователей не хранятся в явном виде"
		},
		"SecurityStamp": {
			"Type": "String",
			"Caption": "Штамп изменения сведений пользователя",
			"Description": "Должен быть уникальным и изменяется при изменении сведений о пользователе"
		},
		"DefaultRole": {
			"Type": "Object",
			"Caption": "Роль пользователя по умолчанию",
			"Description": "Ссылка на роль, в которой пользователь работает большую часть своего времени",
			"TypeInfo": {
				"DocumentLink": {
					"ConfigId": "Security",
					"DocumentId": "ApplicationRole"
				}
			}
		},
		"Roles": {
			"Type": "Array",
			"Caption": "Список ролей пользователя",
			"Description": "Список ссылок на все роли, в которые входит пользователь системы",
			"Items": {
				"Type": "Object",
				"TypeInfo": {
					"DocumentLink": {
						"ConfigId": "Security",
						"DocumentId": "ApplicationRole"
					}
				}
			}
		},
		"Claims": {
			"Type": "Array",
			"Caption": "Список утверждений пользователя",
			"Description": "Дополнительные сведения о пользователе в виде типизированного списка утверждений",
			"Items": {
				"Type": "Object",
				"TypeInfo": {
					"DocumentLink": {
						"ConfigId": "Security",
						"DocumentId": "ApplicationUserClaim",
						"Inline": true
					}
				}
			}
		},
		"Logins": {
			"Type": "Array",
			"Caption": "Список имен входа пользователя",
			"Description": "Заполняется в случае, если пользователь входит в систему через внешние провайдеры",
			"Items": {
				"Type": "Object",
				"TypeInfo": {
					"DocumentLink": {
						"ConfigId": "Security",
						"DocumentId": "ApplicationUserLogin",
						"Inline": true
					}
				}
			}
		}
	}
}
```

   

```
{
	"Id": "55088CAE-6F34-457E-AC2A-2FAE316C4D0C",
	"UserName": "User1",
	"DisplayName": "Иванов И.И.",
	"Description": "Троль 80-го уровня",
	"PasswordHash": "ANggHNufJKJth4FV6jQ9xmYhx04/RgkWDn4PKveYziI38B4MmkZ8NZwlwUHIcrX1Tg==",
	"SecurityStamp": "3f7cc31d-b1dc-43a2-a4eb-8e6c6257366d",
	"DefaultRole": {
		"Id": "ProjectManager",
		"DisplayName": "Менеджер проекта"
	},
	"Roles": [
		{
			"Id": "ProjectManager",
			"DisplayName": "Менеджер проекта"
		},
		{
			"Id": "Analyst",
			"DisplayName": "Аналитик"
		}
	],
	"Claims": [
		{
			"Type": {
				"Id": "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/mobilephone",
				"DisplayName": "Мобильный телефон"
			},
			"Value": "+7 (123) 456-78-90"
		}
	],
	"Logins": [
		{
			"Provider": "Google",
			"ProviderKey": "https://www.google.com/accounts/o8/id?id=AIxOawlYjDIea-6N19tDINhYaNLCxWiJ7o8Wc_o"
		}
	]
}
```

 

 

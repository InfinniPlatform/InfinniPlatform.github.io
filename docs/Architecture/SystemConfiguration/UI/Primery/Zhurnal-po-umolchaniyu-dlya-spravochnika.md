---
layout: default
title: "Журнал по умолчанию для справочника"
position: 1
categories: 
tags: 
---



 

```
{
	"Text": "Типы конструкций зданий",
	"DataSources": [
		{
			"ClassifierDataSource": {
				"Name": "ListDataSource",
				"ConfigId": "FederalNsi",
				"ClassifierId": "1.2.643.5.1.13.2.1.1.366"
			}
		}
	],
	"LayoutPanel": {
		"StackPanel": {
			"Name": "MainViewPanel",
			"Items": [
				{
					"SearchPanel": {
						"Name": "ListSearchPanel",
						"Items": {
							"PropertyBinding": {
								"DataSource": "ListDataSource"
							}
						}
					}
				},
				{
					"DataGrid": {
						"Name": "ListDataGrid",
						"ReadOnly": true,
						"Columns": [
							{
								"Name": "Column1",
								"Text": "Код",
								"Property": "Code"
							},
							{
								"Name": "Column2",
								"Text": "Наименование",
								"Property": "DisplayName"
							},
							{
								"Name": "Column3",
								"Text": "ParentId",
								"Property": "PARENTID"
							}
						],
						"Items": {
							"PropertyBinding": {
								"DataSource": "ListDataSource"
							}
						}
					}					
				},
				{
					"ToolBar": {
						"Name": "ListToolBar",
						"Items": [
							{
								"Button": {
									"Name": "AddButton",
									"Text": "Добавить",
									"Action": {
										"AddAction": {
											"View": {
												"DefaultEditView": {
													"DataSource": {
														"ClassifierDataSource": {
															"Name": "ListDataSource",
															"ConfigId": "FederalNsi",
															"ClassifierId": "1.2.643.5.1.13.2.1.1.366"
														}
													}
												}
											},
											"Items": {
												"PropertyBinding": {
													"DataSource": "ListDataSource"
												}
											}
										}
									}
								}
							},
							{
								"Button": {
									"Name": "ChangeButton",
									"Text": "Изменить",
									"Action": {
										"EditAction": {
											"View": {
												"DefaultEditView": {
													"DataSource": {
														"ClassifierDataSource": {
															"Name": "ListDataSource",
															"ConfigId": "FederalNsi",
															"ClassifierId": "1.2.643.5.1.13.2.1.1.366"
														}
													},
													"Value": {
														"PropertyBinding": {
															"DataSource": "ListDataSource"
														}
													}
												}
											},
											"Items": {
												"PropertyBinding": {
													"DataSource": "ListDataSource"
												}
											}
										}
									}
								}
							},
							{
								"Separator": {
									"Name": "Separator1"
								}
							},
							{
								"Button": {
									"Name": "DeleteButton",
									"Text": "Удалить",
									"Action": {
										"DeleteAction": {
											"Items": {
												"PropertyBinding": {
													"DataSource": "ListDataSource"
												}
											}
										}
									}
								}
							}
						]
					}
				}
			]
		}
	}
}
```

```
{
    "Text": "Типы конструкций зданий",
    "DataSources": [
        {
            "ClassifierDataSource": {
                "Name": "EditObjectDataSource",
                "ConfigId": "FederalNsi",
                "ClassifierId": "1.2.643.5.1.13.2.1.1.366"
            }
        }
    ],
    "LayoutPanel": {
        "StackPanel": {
            "Name": "MainViewPanel",
            "Items": [
                {
                    "PropertyGrid": {
                        "Name": "EditObjectPropertyGrid",
                        "Categories": [
                            {
                                "Text": "Общая информация",
                                "Properties": [
                                    {
                                        "Text": "INDEX",
                                        "Property": "INDEX",
                                        "Editor": {
                                            "TextBox": {
                                                "Name": "Editor1",
                                                "Value": {
                                                    "PropertyBinding": {
                                                        "DataSource": "EditObjectDataSource",
                                                        "Property": "INDEX"
                                                    }
                                                }
                                            }
                                        }
                                    },
                                    {
                                        "Text": "NAME",
                                        "Property": "NAME",
                                        "Editor": {
                                            "TextBox": {
                                                "Name": "Editor2",
                                                "Value": {
                                                    "PropertyBinding": {
                                                        "DataSource": "EditObjectDataSource",
                                                        "Property": "NAME"
                                                    }
                                                }
                                            }
                                        }
                                    },
                                    {
                                        "Text": "PARENTID",
                                        "Property": "PARENTID",
                                        "Editor": {
                                            "TextBox": {
                                                "Name": "Editor3",
                                                "Value": {
                                                    "PropertyBinding": {
                                                        "DataSource": "EditObjectDataSource",
                                                        "Property": "PARENTID"
                                                    }
                                                }
                                            }
                                        }
                                    }
                                ]
                            }
                        ]
                    }
                },
                {
                    "ToolBar": {
                        "Name": "EditObjectToolBar",
                        "Items": [
                            {
                                "Button": {
                                    "Name": "SaveButton",
                                    "Text": "Ok",
                                    "Action": {
                                        "SaveAction": {
                                            "Items": {
                                                "PropertyBinding": {
                                                    "DataSource": "EditObjectDataSource"
                                                }
                                            }
                                        }
                                    }
                                }
                            },
                            {
                                "Button": {
                                    "Name": "CancelButton",
                                    "Text": "Отмена",
                                    "Action": {
                                        "CancelAction": {
                                            "Items": {
                                                "PropertyBinding": {
                                                    "DataSource": "EditObjectDataSource"
                                                }
                                            }
                                        }
                                    }
                                }
                            }
                        ]
                    }
                }
            ]
        }
    }
}
```

 

 

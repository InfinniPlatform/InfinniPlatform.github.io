---
layout: doc
title: "Bower"
position: 
categories: 
tags: 
---

[Bower](http://bower.io/) - это менеджер управления клиентскими библиотеками.

Устанавливается следующей командой:

```
npm install --save-dev bower
```

 

Для работы bower необходимо, чтобы в системе был установлен и доступен в консоли GIT, т.к. bower загружает все библиотеки с Github.

Загрузить git и получить инструкцию по установке можно здесь: [http://git-scm.com/](http://git-scm.com/).

 

После установки bower, в корень проекта нужно добавить два файла: bower.json и .bowerrc.

* .bowerrc описывает путь до директории в проекте, куда bower будет загружать клиентские библиотеки.
* bower.json содержит список всех сторонних клиентских библиотек и их версии.

 

Новую библиотеку можно добавить в список либо вручную, обязательно указав версию, либо командой:

```
bower install --save-dev qunit
```

 

Для загрузки всех перечисленных в bower.json библиотек используется команда:

```
bower install
```

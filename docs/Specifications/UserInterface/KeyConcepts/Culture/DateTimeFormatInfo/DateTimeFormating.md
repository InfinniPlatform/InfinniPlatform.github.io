---
layout: doc
title: "DateTimeFormating"
position: 0
---

Ниже приведены настройки форматирования для даты и времени. Интерпретация большинства перечисленных
форматов зависит от текущей культуры [GlobalContext](../../../GlobalContext).[culture](../../).
[dateTimeFormatInfo](../).

## Standard formats

### `f`

Полное представление даты и краткое представление времени. Комбинация шаблонов [`longDatePattern`](../#longdatepattern)
и [`shortTimePattern`](../#shorttimepattern), разделенных пробелом.

```js
// ru-RU:
"4 сентября 2014 г. 16:17"
// en-US:
"Thursday, September 04, 2014 4:17 PM"
```

### `F`

Полное представление даты и полное представление времени. Комбинация шаблонов [`longDatePattern`](../#longdatepattern)
и и [`longTimePattern`](../#longtimepattern), разделенных пробелом.

```js
// ru-RU:
"4 сентября 2014 г. 16:17:21"
// en-US:
"Thursday, September 04, 2014 4:17:21 PM"
```

### `g`

Краткое представление даты и краткое представление времени. Комбинация шаблонов [`shortDatePattern`](../#shortdatepattern)
и [`shortTimePattern`](../#shorttimepattern), разделенных пробелом.

```js
// ru-RU:
"04.09.2014 16:17"
// en-US:
"9/4/2014 4:17 PM"
```

### `G`

Краткое представление даты и полное представление времени. Комбинация шаблонов [`shortDatePattern`](../#shortdatepattern)
и [`longTimePattern`](../#longtimepattern), разделенных пробелом.

```js
// ru-RU:
"04.09.2014 16:17:21"
// en-US:
"9/4/2014 4:17:21 PM"
```

### `d`

Краткое представление даты. Соответствует шаблону [`shortDatePattern`](../#shortdatepattern).

```js
// ru-RU:
"04.09.2014"
// en-US:
"9/4/2014"
```

### `D`

Полное представление даты. Соответствует шаблону [`longDatePattern`](../#longdatepattern).

```js
// ru-RU:
"4 сентября 2014 г."
// en-US:
"Thursday, September 04, 2014"
```

### `t`

Краткое представление времени. Соответствует шаблону [`shortTimePattern`](../#shorttimepattern).

```js
// ru-RU:
"16:17"
// en-US:
"4:17 PM"
```

### `T`

Полное представление времени. Соответствует шаблону [`longTimePattern`](../#longtimepattern).

```js
// ru-RU:
"16:17:21"
// en-US:
"4:17:21 PM"
```

### `y` or `Y`

Представление год/месяц. Соответствует шаблону [`yearMonthPattern`](../#yearmonthpattern).

```js
// ru-RU:
"Сентябрь 2014"
// en-US:
"September, 2014"
```

### `m` or `M`

Представление месяц/день. Соответствует шаблону [`monthDayPattern`](../#monthdaypattern).

```js
// ru-RU:
"сентября 04"
// en-US:
"September 04"
```

### `s`

Представление в формате ISO 8601. Соответствует шаблону [`sortableDateTimePattern`](../#sortabledatetimepattern).

```js
// ru-RU:
"2014-09-04T16:17:21"
// en-US:
"2014-09-04T16:17:21"
```

### `u`

Представление в универсальном формате. Соответствует шаблону [`universalSortableDateTimePattern`](../#universalsortabledatetimepattern).

```js
// ru-RU:
"2014-09-04 16:17:21Z"
// en-US:
"2014-09-04 16:17:21Z"
```

## Custom formats

Пользователь может определять собственные строки форматирования, используя ниже перечисленные элементы.

### `y`

Последняя или две последних цифры года.Если строка форматирования представлена одним символом `y`,
то ее следует записывать в формате `%y`, чтобы отличать ее от предопределенного формата.

### `yy`

Две последних цифры года.

### `yyyy`

Все цифры года.

### `M`

Порядковый номер месяца. Если порядковый номер месяца представлен одной цифрой (1-9), он будет отображен
в виде одной цифры (1-9).Если строка форматирования представлена одним символом `M`, то ее следует
записывать в формате `%M`, чтобы отличать ее от предопределенного формата.

### `MM`

Порядковый номер месяца. Если порядковый номер месяца представлен одной цифрой (1-9), он будет отображен
с ведущим нулем (01-09).

### `MMM`

Сокращенное наименование месяца с использованием [`abbreviatedMonthNames`](../#abbreviatedmonthnames).

### `MMMM`

Полное наименование месяца с использованием [`monthNames`](../#monthnames).

### `d`

Порядковый номер дня месяца. Если день месяца представлен одной цифрой (1-9), он будет отображен в виде
одной цифры (1-9).Если строка форматирования представлена одним символом `d`, то ее следует записывать
в формате `%d`, чтобы отличать ее от предопределенного формата.

### `dd`

Порядковый номер дня месяца. Если день месяца представлен одной цифрой (1-9), он будет отображен с
ведущим нулем (01-09).

### `ddd`

Сокращенное наименование дня месяца с использованием [`abbreviatedDayNames`](../#abbreviateddaynames).

### `dddd`

Полное наименование дня месяца с использованием [`dayNames`](../#daynames).

### `h`

Час в 12-часовом формате. Если час представлен одной цифрой (0-9), он будет отображен в виде одной цифры (0-9).

### `hh`

Час в 12-часовом формате. Если час представлен одной цифрой (0-9), он будет отображен с ведущим нулем (00-09).

### `H`

Час в 24-часовом формате. Если час представлен одной цифрой (0-9), он будет отображен в виде одной цифры (0-9).

### `HH`

Час в 24-часовом формате. Если час представлен одной цифрой (0-9), он будет отображен с ведущим нулем (00-09).

### `m`

Если минута представлена одной цифрой (1-9), она будет отображена в виде одной цифры (1-9). Если строка
форматирования представлена одним символом `m`, то ее следует записывать в формате `%m`, чтобы отличать
ее от предопределенного формата.

### `mm`

Если минута представлена одной цифрой (1-9), она будет отображена с ведущим нулем (01-09).

### `s`

Если секунда представлена одной цифрой (0-9), она будет отображена в виде одной цифры (0-9). Если строка
форматирования представлена одним символом `s`, то ее следует записывать в формате `%s`, чтобы отличать
ее от предопределенного формата.

### `ss`

Если секунда представлена одной цифрой (0-9), она будет отображена с ведущим нулем (00-09).

### `t`

Первый символ [`amDesignator`](../#amdesignator) или [`PmDesignator`](../#pmdesignator).

### `tt`

Значение [`amDesignator`](../#amdesignator) или [`PmDesignator`](../#pmdesignator).

### `z`

Если номер часового пояса представлен одной цифрой (0-9), он будет отображен в виде одной цифры (0-9)
с явным указанием знака (`+` или `-`). Например: `+0`, `+6`, `-6`.

### `zz`

Если номер часового пояса представлен одной цифрой (0-9), он будет отображен с ведущим нулем (00-09)
с явным указанием знака (`+` или `-`). Например: `+00`, `+06`, `-06`.

### `zzz`

Номер часового пояса отображается с указанием часов и минут, где часы и минуты всегда отображаются
с ведущим нулем, если они представлены одной цифрой. Например: `+00:00`, `+06:00`, `-06:00`.

### `/`

Должен заменяться на [`dateSeparator`](../#dateseparator).

### `:`

Должен заменяться на [`timeSeparator`](../#timeseparator).

### `'abc'` or `"abc"`

Вставляет строку в кавычках, как есть, даже если она содержит элементы формата.
Например, `yyyy'-'MM'-'dd HH':'mm':'ss'Z'`.

### Other symbols

Вставляются, как есть, без изменения, если не совпадают с предопределенными форматами (см. выше).
---
## Front matter
title: "Отчет по лабораторной работе №5"
subtitle: "Архитектура компьтера"
author: "Дмитриева Валерия Александровна"

## Generic otions
lang: ru-RU
toc-title: "Содержание"

## Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

## Pdf output format
toc: true # Table of contents
toc-depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n polyglossia
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
## I18n babel
babel-lang: russian
babel-otherlangs: english
## Fonts
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
## Biblatex
biblatex: true
biblio-style: "gost-numeric"
biblatexoptions:
  - parentracker=true
  - backend=biber
  - hyperref=auto
  - language=auto
  - autolang=other*
  - citestyle=gost-numeric
## Pandoc-crossref LaTeX customization
figureTitle: "Рис."
tableTitle: "Таблица"
listingTitle: "Листинг"
lofTitle: "Список иллюстраций"
lotTitle: "Список таблиц"
lolTitle: "Листинги"
## Misc options
indent: true
header-includes:
  - \usepackage{indentfirst}
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы
Приобретение практических навыков работы в Midnight Commander. Освоение инструкций языка ассемблера mov и int.

# Задание
 Создайте копию файла lab5-1.asm. Внесите изменения в программу (без использова-
ния внешнего файла in_out.asm), так чтобы она работала по следующему алгоритму:
• вывести приглашение типа “Введите строку:”;
• ввести строку с клавиатуры;
• вывести введённую строку на экран.
 Получите исполняемый файл и проверьте его работу. На приглашение ввести строку
введите свою фамилию.
 Создайте копию файла lab5-2.asm. Исправьте текст программы с использование под-
программ из внешнего файла in_out.asm, так чтобы она работала по следующему
алгоритму:
• вывести приглашение типа “Введите строку:”;
• ввести строку с клавиатуры;
• вывести введённую строку на экран.
Не забудьте, подключаемый файл in_out.asm должен лежать в том же каталоге, что и
файл с программой, в которой он используется.
 Создайте исполняемый файл и проверьте его работу.
# Теоретическое введение

Здесь описываются теоретические аспекты, связанные с выполнением работы.

Например, в табл. [-@tbl:std-dir] приведено краткое описание стандартных каталогов Unix.

: Описание некоторых каталогов файловой системы GNU Linux {#tbl:std-dir}

| Имя каталога | Описание каталога                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------|
| `/`          | Корневая директория, содержащая всю файловую                                                                               |
| `/bin `      | Основные системные утилиты, необходимые как в однопользовательском режиме, так и при обычной работе всем пользователям     |
| `/etc`       | Общесистемные конфигурационные файлы и файлы конфигурации установленных программ                                           |
| `/home`      | Содержит домашние директории пользователей, которые, в свою очередь, содержат персональные настройки и данные пользователя |
| `/media`     | Точки монтирования для сменных носителей                                                                                   |
| `/root`      | Домашняя директория пользователя  `root`                                                                                   |
| `/tmp`       | Временные файлы                                                                                                            |
| `/usr`       | Вторичная иерархия для данных пользователя                                                                                 |

Более подробно про Unix см. в [@tanenbaum_book_modern-os_ru; @robbins_book_bash_en; @zarrelli_book_mastering-bash_en; @newham_book_learning-bash_en].

# Выполнение лабораторной работы
Откроем Midnight Commander (рис. [-@fig:001])
![](image/1.png){#fig:001 width=100%}
Пользуясь клавишами переходим в каталог (рис. [-@fig:002])
![](image/2.png){#fig:001 width=100%}
Создаем папку и переходим в созданный каталог (рис. [-@fig:003])
![](image/3.png){#fig:001 width=100%}
(рис. [-@fig:004])
![](image/5.png){#fig:001 width=100%}
Заходим в редактор nano и пишим команду. (рис. [-@fig:005])
![](image/6.png){#fig:001 width=100%}
Выводим строку (рис. [-@fig:006])
![Честно, не сделала скриншот, извините(](image/7.png){#fig:001 width=100%}
Меняем команды (рис. [-@fig:007])
![](image/8.png){#fig:001 width=100%}
(рис. [-@fig:008])
![](image/9.png){#fig:001 width=100%}
Выводим строку (рис. [-@fig:009])
![](image/10.png){#fig:001 width=100%}
Изменилось расположение строки из-за изменение команды sprintLf на sprint
САМОСТОЯТЕЛЬНАЯ РАБОТА
Создаем новый каталог той же командой mc
Пишим код в редакторе nano. (рис. [-@fig:010])
![](image/Снимок экрана от 2024-11-28 19-09-10.png){#fig:001 width=100%}
Выводим строку (рис. [-@fig:011])
![](image/7.png){#fig:001 width=100%}
Позже не забываем переименновать файл (рис. [-@fig:012])
![](image/13.png){#fig:001 width=100%}
Изменяем код (рис. [-@fig:013])
![](image/8.png){#fig:001 width=100%}
Меняем команду и выводим строку (рис. [-@fig:014])
![](image/9.png){#fig:001 width=100%}
(рис. [-@fig:015])
![](image/14.png){#fig:001 width=100%}

# Выводы

Я преобрела практические навыки работы с Midnight Commander. И освоила инструкции языка ассемблера mov и int.

# Список литературы{.unnumbered}

::: {#refs}
:::

---
## Front matter
title: "Отчёт по лабораторной работе №3"
subtitle: "Архитектура компьютера"
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
Целью лабораторной работы №3 является освоение процедуры оформления отчетов с помощью легковесного языка разметки Markdoun.

# Задание

Задание для самостоятельной работы:
1) В соответствующем каталоге сделайте отчёт по лабораторной работе № 2 в формате
Markdown. В качестве отчёта необходимо предоставить отчёты в 3 форматах: pdf, docx
и md.
2) Загрузите файлы на github.

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
Перейдем в каталог курса, оформленный при выполнении лабораторной работы
![Рис. 1](image/1*.png){#fig:001 width=100%}
Обновляем локальный репозиторий, скачав изменения из удаленного репозитория с помощью команды
![Рис. 2](image/1*.png){#fig:001 width=100%}
Перейдем в каталог с шаблоном для отчета по лабораторной работе №3
![Рис. 3](image/3*.png){#fig:001 width=100%}
Проведем компиляцию шаблона с использованием Makefile.
![Рис. 4](image/4*.png){#fig:001 width=100%}
После ожидания генерируются файлы report.pdf и report.docx удалим полученные файлы.
![Рис. 5](image/3.png){#fig:001 width=100%}
![Рис. 6](image/5*.png){#fig:001 width=100%}
Заполним и скомпилируем отчет Makefile.
![Рис. 7](image/4.png){#fig:001 width=100%}
Загрузим файлы на Github.
![Рис. 8](image/5.png){#fig:001 width=100%}
Самостоятельная работа
Перейдем в каталог с шаблоном для отчета по лабораторной работе №2
![Рис. 1.1](image/11.png){#fig:001 width=100%}
Проведем компиляцию шаблона с использованием Makefile.
![Рис. 2.1](image/12.png){#fig:001 width=100%}
Перенесем данные отчета из формата pdf в формат md
![Рис. 3.1](image/13.png){#fig:001 width=100%}
![Рис. 4.1](image/14.png){#fig:001 width=100%}
# Выводы
В ходе проделанной работы мы освоили процедуры оформления отчетов с помощью легковесного
языка разметки Markdown.

# Список литературы{.unnumbered}

::: {#refs}
:::

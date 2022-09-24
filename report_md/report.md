---
# Front matter
title: "Отчёт по лабораторной работе №3"
subtitle: "Дискреционное разграничение прав в Linux. Два пользователя"
author: "Аминов Зулфикор Мирзокаримович"

# Generic otions
lang: ru-RU
toc-title: "Содержание"

# Bibliography
bibliography: bib/cite.bib
csl: pandoc/csl/gost-r-7-0-5-2008-numeric.csl

# Pdf output format
toc: true # Table of contents
toc_depth: 2
fontsize: 12pt
linestretch: 1.5
papersize: a4
documentclass: scrreprt
## I18n
polyglossia-lang:
  name: russian
  options:
	- spelling=modern
	- babelshorthands=true
polyglossia-otherlangs:
  name: english
### Fonts
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase,Scale=0.9
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
## Misc options
indent: true
header-includes:
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the value makes tex try to have fewer lines in the paragraph.
  - \interlinepenalty=0 # value of the penalty (node) added after each line of a paragraph.
  - \hyphenpenalty=50 # the penalty for line breaking at an automatically inserted hyphen
  - \exhyphenpenalty=50 # the penalty for line breaking at an explicit hyphen
  - \binoppenalty=700 # the penalty for breaking a line at a binary operator
  - \relpenalty=500 # the penalty for breaking a line at a relation
  - \clubpenalty=150 # extra penalty for breaking after first line of a paragraph
  - \widowpenalty=150 # extra penalty for breaking before last line of a paragraph
  - \displaywidowpenalty=50 # extra penalty for breaking before last line before a display math
  - \brokenpenalty=100 # extra penalty for page breaking after a hyphenated line
  - \predisplaypenalty=10000 # penalty for breaking before a display
  - \postdisplaypenalty=0 # penalty for breaking after a display
  - \floatingpenalty = 20000 # penalty for splitting an insertion (can only be split footnote in standard LaTeX)
  - \raggedbottom # or \flushbottom
  - \usepackage{float} # keep figures where there are in the text
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Получение практических навыков работы в консоли с атрибутами фай-
лов для групп пользователей.

# Выполнение работы

## Создание учетной записи пользователя guest

На прошлой работы уже создали пользователя guest.

## Создали второго пользователя guest2

![Создание второго пользователя guest2](image/1.png){ #fig:001 width=100% height=100% }

## Задали пароль для пользователя guest2

![Задали пароль](image/2.png){ #fig:002 width=100% height=100% }

## Добавили пользователя guest2 в группу guest:

![Добавление пользователя guest2 в группу guest](image/3.png){ #fig:003 width=100% height=100% }

## Входили в систему от имени пользователя guest

![Входили в систему от имени пользователя guest](image/4.png){ #fig:004 width=100% height=100% }

## Входили в систему от имени пользователя guest2

![Входили в систему от имени пользователя guest2](image/5.png){ #fig:005 width=100% height=100% }

## Для пользователя guest командой pwd определили директорию

![определили директорию для пользователя guest](image/6.png){ #fig:006 width=100% height=100% }

## Для пользователя guest2 командой pwd определили директорию

![определили директорию для пользователя guest2](image/7.png){ #fig:007 width=100% height=100% }

## Уточнили имя нашего пользователя, его группу, кто входит в неё и к каким группам принадлежит он сам
и сравнили вывод команды groups с выводом команд id -Gn и id -G.

![Уточнили имя нашего пользователя, его группу](image/8.png){ #fig:008 width=100% height=100% }

![Сравнили вывод команды groups с выводом команд id -Gn и id -G](image/9.png){ #fig:009 width=100% height=100% }

## Сравнили полученную информацию с содержимым файла /etc/group.

![Сравнили полученную информацию с содержимым файла /etc/group](image/10.png){ #fig:010 width=100% height=100% }

![](image/11.png){ #fig:011 width=100% height=100% }

## От имени пользователя guest2 выполнили регистрацию пользователя
guest2 в группе guest командой newgrp guest.

![От имени пользователя guest2 выполнили регистрацию пользователя
guest2 в группе guest](image/12.png){ #fig:012 width=100% height=100% }

## От имени пользователя guest изменили права директории /home/guest,
разрешив все действия для пользователей группы, командой chmod g+rwx /home/guest.

![От имени пользователя guest изменили права директории /home/guest](image/13.png){ #fig:013 width=100% height=100% }

## От имени пользователя guest снимали с директории /home/guest/dir1
все атрибуты командой chmod 000 dirl

![От имени пользователя guest снимали с директории /home/guest/dir1
все атрибуты](image/14.png){ #fig:014 width=100% height=100% }

## Меняя атрибуты у директории dir1 и файла file1 от имени пользова-
теля guest и делая проверку от пользователя guest2, заполнили табл. 3.1

![заполнили табл. 3.1](image/15.png){ #fig:015 width=100% height=100% }

# Выводы

Получили практических навыков работы в консоли с атрибутами фай-
лов для групп пользователей.

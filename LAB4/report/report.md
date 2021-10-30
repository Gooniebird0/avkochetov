---
# Front matter
lang: ru-RU
title: 'Отчёт'
subtitle: 'по лабораторной работе 4'
author: 'Кочетов Андрей Владимирович'

# Formatting
toc-title: 'Содержание'
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: LiberationSerif
romanfont: LiberationSerif
sansfont: LiberationSans
monofont: LiberationMono
mainfontoptions: Ligatures=TeX
romanfontoptions: Ligatures=TeX
sansfontoptions: Ligatures=TeX,Scale=MatchLowercase
monofontoptions: Scale=MatchLowercase
indent: true
pdf-engine: lualatex
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

Получение практических навыков работы в консоли с расширенными атрибутами файлов.

# Задание

Лабораторная работа подразумневает последовательное выполнение команд, используя разные расширенные атрибуты.

# Выполнение лабораторной работы

1. Определил расш. атрибуты файла, попытался изменить права и установить расщ. атрибут a. Везде получил отказ(рис.1).

   ![рис.1. Команды](images/1.png){ #fig:001 width=60% }

2. Зашел в root пользователя и успешно установил расш. атрибут на файл(рис.2).

   ![рис.2. Добавление атрибута](images/2.png){ #fig:002 width=60% }

3. Проверил правильно добавления атрибута, выполнил дозапись слова test в файл и прочитал. Все было успешно(рис.3).

   ![рис.3. Команды с атрибутом](images/3.png){ #fig:003 width=60% }

4. Попытался стереть информацию в файле и установить права на него. Выполнить команды не удалось(рис.4).

   ![рис.4. Очистка и права](images/4.png){ #fig:004 width=60% }

5. Снял расширенный атрибут a через root пользователя(рис.5).

   ![рис.5. Снятие атрибута](images/5.png){ #fig:005 width=60% }

6. Попытался снова выполнить команды, при выполнении которых было отказано в доступе(рис.6).

   ![рис.6. Команды](images/6.png){ #fig:006 width=60% }

7. Установил расширенный атрибут i через root пользователя(рис.7).

   ![рис.7. Атрибут i](images/7.png){ #fig:007 width=60% }

8. Повторил все команды, после чего обнаружил, что большинство команд выполнить так и не удалось(рис.8).

   ![рис.8. Команды с атрибутом i](images/8.png){ #fig:008 width=60% }

# Выводы

Получил практические навыки работы в консоли с атрибутами файлов для групп пользователей.
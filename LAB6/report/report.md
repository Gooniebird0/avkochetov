---
# Front matter
lang: ru-RU
title: 'Отчёт'
subtitle: 'по лабораторной работе 6'
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

Развить навыки администрирования ОС Linux. Получить первое практическое знакомство с технологией SELinux1.
Проверить работу SELinx на практике совместно с веб-сервером Apache.

# Задание

Работа с сервером apach и настройка портов.

# Выполнение лабораторной работы

1. Проверил режим работы SElinux при помощи 2 команд(рис.1).

   ![рис.1. Режимы](images/1.png){ #fig:001 width=60% }

2. Запустил сервер и проверил его рабоспособность(рис.2).

   ![рис.2. Запуск сервера](images/2.png){ #fig:002 width=60% }

3. Нашел веб-сервер Apache в списке процессов(рис.3).

   ![рис.3. Процессы](images/3.png){ #fig:003 width=60% }

4. Посмотрел текущее состояние переключателей SELinux для Apache(рис.4).

   ![рис.4. Состояние](images/4.png){ #fig:004 width=60% }

5. Посмотрел статистику по политике, тип файлов и поддиректорий и тип файлов, находящихся в другой директории(рис.5).

   ![рис.5. Статистика и типы файлов](images/5.png){ #fig:005 width=60% }

6. Создал html-файл, проверил контекст файла(рис.6).

   ![рис.6. Создание файла](images/6.png){ #fig:006 width=60% }

7. Обратился к файлу через веб-сервер(рис.7).

   ![рис.7. Файл](images/7.png){ #fig:007 width=60% }

8. Проверил контекст командой ls -Z, изменил контекст на другой, убедился в смене и проверил работоспособность веб-сервера (рис.8).

   ![рис.8. Смена контекста и тест веб-сервера](images/8.png){ #fig:008 width=60% }

9. Проанализировал ситуацию и посмотрел логи(рис.9).

   ![рис.9. Анализ](images/9.png){ #fig:009 width=60% }

10. Сменил порт на ТСР-порт 81(рис.10).

   ![рис.10. Смена порта](images/10.png){ #fig:010 width=60% }

11. Выполнил перезапуск сервера и увидел сбой(рис.11).

   ![рис.11. Сбой сервера](images/11.png){ #fig:011 width=60% }

12. Проанализировал log-файлы(рис.12).

   ![рис.12. Логи](images/12.png){ #fig:012 width=60% }

13. Выполнил программу semanage и проверил список портов, где увидел порт 81 в списке(рис.13).

   ![рис.13. Semanage](images/13.png){ #fig:013 width=60% }

14. Снова зашел на сервер и увидел, что он работает. Вернул контекст и listen 80, и удалил привязку к 81(рис.14).

   ![рис.14. Работа с командами](images/14.png){ #fig:014 width=60% }

15. Удалил файл test.html(рис.15).

   ![рис.15. Удаление](images/15.png){ #fig:015 width=60% }

# Выводы

Развил навыки администрирования ОС Linux. Получил первое практическое знакомство с технологией SELinux1.
Проверил работу SELinx на практике совместно с веб-сервером Apache.
---
## Front matter
lang: ru-RU
title: Лабораторная работа № 13. Средства, применяемые при разработке программного обеспечения в ОС типа UNIX/Linux
author: |
	Alyona Voropaeva
institute: |
	RUDN University, Moscow, Russian Federation

date: 29 May, 2022 Moscow, Russia

## Formatting
toc: false
slide_level: 2
theme: metropolis
header-includes: 
 - \metroset{progressbar=frametitle,sectionpage=progressbar,numbering=fraction}
 - '\makeatletter'
 - '\beamer@ignorenonframefalse'
 - '\makeatother'
aspectratio: 43
section-titles: true
---

# Лабораторная работа № 13

# Цель работы

Приобрести простейшие навыки разработки,анализа,тестирования и отладки приложений в ОС типа UNIX/Linux на примере создания на языке программирования С калькулятора с простейшими функциями.

# Задание

Написать 4 командных файла с использованием логических управляющих конструкций
и циклов.

# Материалы

- TUIS
- Fedora
- Markdown
- emacs

# Выполнение лабораторной работы

![Реализация функций калькулятора в файле calculate.с](image/02.png){ #fig:002 }

![Реализация функций калькулятора в файле calculate.с](image/03.png){ #fig:003 }

## Интерфейсный файл calculate.h

![Интерфейсный файл calculate.h](image/04.png){ #fig:004 }

## Основной файл main.c

![Основной файл main.c](image/05.png){ #fig:005 }

## Makefile

![Создала Makefile с необходимым содержанием](image/07.png){ #fig:007 }

## Отладка

![Запуск программы внутри отладчика](image/5.png){ #fig:011 }

## list

![Использовал команду «list](image/7.png){ #fig:012 }

![Просмотр строк с 12 по 15](image/8.png){ #fig:013 }

## breakpoints

![Установила точку останова в файле calculate.c](image/10.png){ #fig:015 }

![Запустила программу внутри отладчика до точки останова](image/11.png){ #fig:017 }

## splint

![Проанализировала код файла calculate.c](image/14.png){ #fig:021 }

## splint

![Проанализировала код файла main.c](image/15.png){ #fig:022 }


# Выводы

В результате работы мы приобрели простейшие навыки разработки,анализа,тестирования и отладки приложений в ОС типа UNIX/Linux на примере создания на языке программирования С калькулятора с простейшими функциями.

## {.standout}

Спасибо за внимание!

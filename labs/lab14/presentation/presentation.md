---
## Front matter
lang: ru-RU
title: Лабораторная работа № 14. Именованные каналы
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

# Лабораторная работа № 14

# Цель работы

Приобретение практических навыков работы с именованными каналами

# Задание

Изучитеприведённыевтекстепрограммыserver.c иclient.c.Взяв данные примеры
за образец,напишите аналогичные программы,внеся следующие изменения:

1. Работает не 1 клиент,а несколько (например,два).

2. Клиенты передаюттекущее время с некоторой периодичностью (например,раз в пять
секунд).Используйте функцию sleep() для приостановки работы клиента.

3. Сервер работаетне бесконечно,а прекращаетработу через некоторое время (например,30 сек).Используйте функцию clock() для определения времени работы сервера.

# Материалы

- TUIS
- Fedora
- Markdown
- emacs

# Выполнение лабораторной работы

## Создаем файлы

![создаем файлы](image/1.png){ #fig:001 width=70% }

## common.h 

![common.h](image/6.png){ #fig:002 width=70% }

## server.c

![server.c](image/7.png){ #fig:003 width=70% }

![server.c](image/8.png){ #fig:004 width=70% }

## client.c 

![client.c](image/4.png){ #fig:005 width=70% }

![client.c](image/5.png){ #fig:006 width=70% }

## Makefile

![Makefile](image/9.png){ #fig:007 width=70% }

## Проверяем работу

![Прверка рабоы](image/2.png){ #fig:009 width=70% }



# Выводы

В результате работы мы приобрели практические навыки работы с именованными каналами.и.

## {.standout}

Спасибо за внимание!

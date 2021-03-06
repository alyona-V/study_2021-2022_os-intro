---
## Front matter
title: "Отчёт по лабораторной работе №6"
subtitle: "Поиск файлов. Перенаправление ввода-вывода. Просмотр запущенных процессов"
author: "Воропаева Алёна Дмитриевна"

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
Ознакомление с инструментами поиска файлов и фильтрации текстовых данных. Приобретение практических навыков: по управлению процессами (и заданиями), по проверке использования диска и обслуживанию файловых систем.

# Задание

1. Осуществите вход в систему,используя соответствующее имя пользователя.

2. Запишите в файл file.txt названия файлов,содержащихся в каталоге /etc. Допишите в этот же файл названия файлов,содержащихся в вашем домашнем каталоге.

3. Выведите имена всех файлов из file.txt,имеющих расширение .conf,после чего запишите их в новыйтекстовой файл conf.txt.

4. Определите,какие файлы в вашем домашнем каталоге имеют имена,начинавшиеся с символа c? Предложите несколько вариантов,как это сделать.

5. Выведите на экран (по странично) имена файлов из каталога /etc,начинающиеся с символа h.

6. Запустите в фоновом режиме процесс,который будетзаписывать в файл ~/logfile файлы,имена которых начинаются с log.



# Теоретическое введение

**Перенаправление ввода-вывода**

В системе по умолчанию открытотри специальных потока:

- stdin — стандартный поток ввода (по умолчанию: клавиатура), файловый дескриптор 0;
- stdout — стандартный поток вывода (по умолчанию: консоль), файловый дескриптор 1;
- stderr —стандартный поток вывод сообщений об ошибках (по умолчанию: консоль),
файловый дескриптор 2.

Большинство используемых в консоли команд и программ записывают результаты
своейработывстандартныйпотоквыводаstdout.Например,командаls выводитвстандартный поток вывода (консоль) список файлов втекущей директории. Потоки вывода
и ввода можно перенаправлять на другие файлы или устройства. Проще всего это делается
с помощью символов >,>>,<,<<.

**Управление задачами**

Любуювыполняющуюсявконсоликомандуиливнешнююпрограммуможнозапустить в фоновом режиме.Для этого следует в конце имени команды указать знак амперсанда

**Управление процессами**

Любой команде, выполняемой в системе, присваивается идентификатор процессам(process ID). Получить информацию о процессе и управлять им, пользуясь идентификатором процесса,можно из любого окна командного интерпретатора.

# Выполнение лабораторной работы

1. Для начала войдем в систему.(рис. [-@fig:001])

![Вход в систему](изо/Screenshot1.png){ #fig:001 width=70% }

2. Запишим в файл file.txt названия файлов,содержащихся в каталоге /etc и названия файлов,содержащихся в домашнем каталоге(рис. [-@fig:002])

![Запись названий файлов](изо/Screenshot2.png){ #fig:002 width=70% }


3. Выведим имена всех файлов из file.txt,имеющих расширение .conf (`grep`), запишим их в новый текстовой файл conf.txt(`>conf.txt`).(рис. [-@fig:003])

![Запуск записи определенных файлов в файл в фоновом режиме](изо/Screenshot6.png){ #fig:007 width=70% }

4. Первый способ вывести файлы начинающиеся с "с" через find(рис. [-@fig:004])

![вывод файлов с помощью команды find](изо/Screenshot4.png){ #fig:004 width=70% }

Второй способ с помощью конвейера, ls, grep (рис. [-@fig:005])

![вывод файлов с помощью конвейера, ls, grep](изо/Screenshot4_1.png){ #fig:005 width=70% }

5. Выведим на экран имена файлов из каталога /etc,начинающихся
с символа h(рис. [-@fig:006])

![вывод файлов](изо/Screenshot5.png){ #fig:006 width=70% }

6. Запустим, с помощью добавления `&`, в фоновом режиме процесс,который будетзаписывать в файл ~/logfile
файлы, имена которых начинаются с log(рис. [-@fig:007])

![Запуск записи определенных файлов в файл в фоновом режиме](изо/Screenshot6.png){ #fig:007 width=70% }

7. Удалим файл ~/logfile(рис. [-@fig:008])

![Удаление файла](изо/Screenshot7.png){ #fig:008 width=70% }

8. Запуск из консоли в фоновом режиме редактора gedit.(рис. [-@fig:009])

![Запуск gedit в фоновом режиме](изо/Screenshot8.png){ #fig:009 width=70% }

9. Определение идентификатора процесса gedit, используя команду ps,конвейер и фильтр
grep.

Определение идентификатора процесса gedit, используя команду pidof(рис. [-@fig:010])

![Определение идентификатора](изо/Screenshot9.png){ #fig:010 width=70% }

10. Используем команду kill и индентификатор процесса для завершения
процесса gedit.(рис. [-@fig:011])

![Завершение процесса gedit](изо/Screenshot10.png){ #fig:011 width=70% }

11. Изучив справки к командам df и du выполним их.(рис. [-@fig:012])

![Выпонение команды df -а](изо/Screenshot11.png){ #fig:012 width=70% }

Выполним команду du с опцией -s, которая отображает только ито для каждого аргумента(рис. [-@fig:013])

![Выпонение команды du -s](изо/Screenshot11_1.png){ #fig:013 width=70% }

12. Выведим имена всех директорий, имеющихся в домашнем каталоге, maxdrepth 1 сделает не рекурсивный вывод, d укадет что вывести необхожимо именно директории.(рис. [-@fig:014])

![Вывод имен всех директорий домашнего каталога](изо/Screenshot12.png){ #fig:014 width=70% }


# Контрольные вопросы

1. Какие потоки ввода вывода вы знаете?

- stdin — стандартный поток ввода (по умолчанию: клавиатура), файловый дескриптор 0;
- stdout — стандартный поток вывода (по умолчанию: консоль), файловый дескриптор 1;
- stderr —стандартный поток вывод сообщений об ошибках (по умолчанию: консоль),
файловый дескриптор 2.

2. Объясните разницу между операцией > и >>.

- > перенаправление

-  >> Перенаправление и файл открывается в режиме добавления

3. Чтотакое конвейер?

Конвейер (pipe) служитдля объединения простых команд или утилит в цепочки,в ко-
торых результат работы предыдущей команды передаётся последующей. 

4. Что такое процесс? Чем это понятие отличается от программы?

Процесс — это идентифицируемая абстракция совокупности взаимосвязанных системных ресурсов на основе отдельного и независимого виртуального адресного пространства в контексте которой организуется выполнение потоков. 

программа сама по себе — лишь пассивная последовательность инструкций. В то время как процесс — непосредственное выполнение этих инструкций. 

5. Чтотакое PID и GID?

уникальный идентификатор процесса PID

"Владелец" и "группа", это числовые идентификатор GID, являющийся атрибутами процесса.

6. Что такое задачи и какая команда позволяет ими управлять?

Любую выполняющуюся в консоли команду или внешнюю программу можно запустить в фоновом режиме. Для этого следует в конце имени команды указать знак амперсанда &. Например: gedit &.

7. Найдите информацию об утилитах top и htop.Каковы их функции?

Top - отобразить запущенные процессы, используемые ими ресурсы и другую полезную информацию (с автоматическим обновлением данных)

Htop - показывает динамический список системных процессов, список обычно выравнивается по использованию ЦПУ. В отличие от top, htop показывает все процессы в системе. Также показывает время непрерывной работы, использование процессоров и памяти. Htop часто применяется в тех случаях, когда информации даваемой утилитой top недостаточно, например при поиске утечек памяти в процессах.

8. Назовите и дайте характеристику команде поиска файлов.Приведите примеры использования этой команды.

Команда find используется для поиска и отображения на экран имён файлов, соответствующих заданной строке символов. Формат команды: find путь [-опции]

9. Можно ли по контексту (содержанию) найти файл? Если да,то как?

Да, через команду grep. Например: grep Aug -R /var/log/* вывода строки, содержащие "Aug", во всех файлах, находящихся в директории /var/log и ниже

10. Как определить объем свободной памяти на жёстком диске?

Для определения объёма свободного пространства на файловой системе можно воспользоваться командой df, которая выведет на экран список всех файловых систем в соответствии с именами устройств, с указанием размера и точки монтирования.

11. Как определить объем вашего домашнего каталога?

Команда du показывает число килобайт, используемое каждым файлом или каталогом.

12. Как удалить зависший процесс?

Спомощью команды kill PID


# Выводы

В результате работы мы познакомились с инструментами поиска файлов и фильтрации текстовых данных. Приобрели практические навыки: по управлению процессами (и заданиями), по проверке использования диска и обслуживанию файловых систем.



---
# Front matter
lang: ru-RU
title: "Лабораторная работа № 12"
subtitle: "Программирование в командном процессоре ОС UNIX. Ветвления и циклы"
author: "Маметкадыров Ынтымак"

# Formatting
toc_depth: 2
lof: true # List of figures
lot: true # List of tables
fontsize: 12pt
linestretch: 1.5
papersize: a4paper
documentclass: scrreprt
polyglossia-lang: russian
polyglossia-otherlangs: english
mainfont: PT Serif
romanfont: PT Serif
sansfont: PT Sans
monofont: PT Mono
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

Изучить основы программирования в оболочке ОС UNIX. Научится писать более сложные командные файлы с использованием логических управляющих конструкций и циклов.

# Выполнение лабораторной работы

1. Написали на языке Си программу (рис. 1), которая вводит число и определяет, является ли оно больше нуля, меньше нуля или равно нулю. Затем программа завершается с помощью функции exit(n), передавая информацию о коде завершения в оболочку. Командный файл (рис. 2) вызывает эту программу и, проанализировав с помощью команды $?, выдает сообщение о том, какое число было введено (рис. 3).

![Рис. 1. Листинг программы compare.c](/home/itmametkadihrov/Изображения/lab12/1.png){ #fig:001 width=70% }

![Рис. 2. Листинг командного файла compare.sh](/home/itmametkadihrov/Изображения/lab12/2.png){ #fig:001 width=70% }

![Рис. 3. Работа командного файла compare.sh](/home/itmametkadihrov/Изображения/lab12/3.png){ #fig:001 width=70% }

2. Написали командный файл files.sh (рис. 4), создающий указанное число файлов, пронумерованных последовательно от 1 до N. Число файлов, которые необходимо создать, передаётся в аргументы командной строки. Командный файл также умеет удалять все созданные им файлы, для этого нужно при запросе об удалении нажать 1, иначе 0. Передали в качестве параметра командному файлу число 5, в результате создались файлы 1.tmp, 2.tmp, 3.tmp, 4.tmp, 5.tmp (рис. 5). Попробовали удалить все созданные файлы (рис. 6).

![Рис. 4. Командный файл files.sh](/home/itmametkadihrov/Изображения/lab12/4.png){ #fig:001 width=70% }

![Рис. 5. Создание файлов](/home/itmametkadihrov/Изображения/lab12/5.png){ #fig:001 width=70% }

![Рис. 6. Удаление файлов](/home/itmametkadihrov/Изображения/lab12/6.png){ #fig:001 width=70% }

3. Написали tar -cvf out.tar work в командный файл tar.sh, который с помощью команды tar запаковывает в архив все файлы в указанной директории work (рис. 7).

![Рис. 7. Результат работы командного файла tar.sh](/home/itmametkadihrov/Изображения/lab12/7.png){ #fig:001 width=70% }

4. Модифицировали его так (рис. 8), чтобы запаковывались только те файлы, которые были изменены менее недели тому назад (рис. 9).

![Рис. 8. Модифицированный командный файл tar.sh](/home/itmametkadihrov/Изображения/lab12/8.png){ #fig:001 width=70% }

![Рис. 9. Результат работы командного файла tar.sh](/home/itmametkadihrov/Изображения/lab12/9.png){ #fig:001 width=70% }

# Вывод

Изучили основы программирования в оболочке ОС UNIX. Научились писать более сложные командные файлы с использованием логических управляющих конструкций и циклов.

# Ответы на контрольные вопросы

1. getopts - осуществляет синтаксический анализ командной строки, выделяя флаги, и используется для объявления переменных.

2. Такие символы, как ' < > * ? | \ " &, являются метасимволами и имеют для командного процессора специальный смысл.

3. Управляющие операторы, как for, case, if и while.

4. Команды прерывания break и continue.

5. Используются для возвращения кода завершения. true всегда возвращает код завершения, равный нулю (т.е. истина), а команда false всегда возвращает код завершения, не равный нулю (т. е. ложь).

6. Возвращается истину, если существует файл.

7. При замене в операторе цикла while служебного слова while на until условие, при выполнении которого осуществляется выход из цикла, меняется на противоположное. В остальном оператор цикла while и оператор цикла until идентичны.

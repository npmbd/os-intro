
---
# Front matter
lang: ru-RU
title: "Лабораторная работа № 11"
subtitle: "Программирование в командном процессоре ОС UNIX. Командные файлы"
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

Изучить основы программирования в оболочке ОС UNIX/Linux. Научиться писать небольшие командные файлы.

# Выполнение лабораторной работы

1. Создали директорию backup в нашем домашнем каталоге (рис. 1).

2. Создали файл backup.sh (рис. 1).

![Рис. 1. Создание файл backup.sh](/home/itmametkadihrov/Изображения/lab11/1.png){ #fig:001 width=70% }

3. Написали скрипт (рис. 2), который при запуске будет делать резервную копию самого себя в директорию
backup в нашем домашнем каталоге (рис. 3). 

![Рис. 2. Содержимое файл backup.sh](/home/itmametkadihrov/Изображения/lab11/2.png){ #fig:001 width=70% }

![Рис. 3. Созданный архив](/home/itmametkadihrov/Изображения/lab11/8.png){ #fig:001 width=70% }

4. Создали командный файл print.sh (рис. 4), который последовательно распечатывает значения всех переданных аргументов, в том числе превышающих десять (рис. 5).

![Рис. 4. Командный файл print.sh](/home/itmametkadihrov/Изображения/lab11/3.png){ #fig:001 width=70% }

![Рис. 5. Работа командного файла print.sh](/home/itmametkadihrov/Изображения/lab11/9.png){ #fig:001 width=70% }

5. Создали командный файл ls.sh - аналог команды ls (рис. 6). Этот файл выдает информацию о нужном
каталоге и выводит информацию о возможностях доступа к файлам этого каталога без использования команды ls и dir (рис. 7).

![Рис. 6. Командный файл ls.sh](/home/itmametkadihrov/Изображения/lab11/4.png){ #fig:001 width=70% }

![Рис. 7. Запуск командного файла ls.sh](/home/itmametkadihrov/Изображения/lab11/10.png){ #fig:001 width=70% }

6. Написали командный файл (рис. 8), который получает в качестве аргумента командной строки формат файла (.txt, .doc, .jpg, .pdf и т.д.) и вычисляет количество таких файлов в указанной директории. Путь к директории также передаётся в виде аргумента командной строки (рис. 9).

![Рис. 8. Командный файл сount.sh](/home/itmametkadihrov/Изображения/lab11/5.png){ #fig:001 width=70% }

![Рис. 9. Работа командного файла сount.sh](/home/itmametkadihrov/Изображения/lab11/11.png){ #fig:001 width=70% }

# Вывод

Изучили основы программирования в оболочке ОС UNIX/Linux. Научились писать небольшие командные файлы.

# Ответы на контрольные вопросы

1. Командный процессор (командная оболочка, интерпретатор команд shell) — это программа, позволяющая пользователю взаимодействовать с операционной системой компьютера. В операционных системах типа UNIX/Linux наиболее часто используются следующие реализации командных оболочек:

	– оболочка Борна (Bourne shell или sh) — стандартная командная оболочка UNIX/Linux, содержащая базовый, но при этом полный набор функций;

	– С-оболочка (или csh) — надстройка на оболочкой Борна, использующая Сподобный синтаксис команд с возможностью сохранения истории выполнения команд;

	– оболочка Корна (или ksh) — напоминает оболочку С, но операторы управления программой совместимы с операторами оболочки Борна;

	– BASH — сокращение от Bourne Again Shell (опять оболочка Борна), в основе своей совмещает свойства оболочек С и Корна (разработка компании Free Software Foundation).

2. POSIX (Portable Operating System Interface for Computer Environments) — набор стандартов описания интерфейсов взаимодействия операционной системы и прикладных программ.

3. Командный процессор bash обеспечивает возможность использования переменных типа строка символов. Имена переменных могут быть выбраны пользователем. Пользователь имеет возможность присвоить переменной значение некоторой строки символов.

	Оболочка bash позволяет работать с массивами. Для создания массива используется команда set с флагом -A. За флагом следует имя переменной, а затем список значений, разделённых пробелами.

4. Оболочка bash поддерживает встроенные арифметические функции. Команда let является показателем того, что последующие аргументы представляют собой выражение, подлежащее вычислению.

	Команда read позволяет читать значения переменных со стандартного ввода.

5. ![Рис. 6. Арифметические операторы оболочки bash](/home/itmametkadihrov/Изображения/lab11/6.png){ #fig:001 width=70% }

6. Для облегчения программирования можно записывать условия оболочки bash в двойные скобки — (( )).

7. PS1, PS2, HOME, IFS, MAIL, TERM, LOGNAME.

8. Такие символы, как ' < > * ? | \ " &, являются метасимволами и имеют для командного процессора специальный смысл.

9. Снятие специального смысла с метасимвола называется экранированием метасимвола. Экранирование может быть осуществлено с помощью предшествующего метасимволу символа \, который, в свою очередь, является метасимволом.

10. Последовательность команд может быть помещена в текстовый файл. Такой файл называется командным. Далее этот файл можно выполнить по команде:

	bash командный_файл [аргументы]

11. Для этого существует ключевое слово function, после которого следует имя функции и список команд, заключённых в фигурные скобки.

12. test -f file — истина, если файл file существует;

	test -d file — истина, если файл file является каталогом.

13. Для создания массива используется команда set с флагом -A.

	Если использовать typeset -i для объявления и присвоения переменной, то при последующем её применении она станет целой.

	Изъять переменную из программы можно с помощью команды unset.

14. Чтобы передать параметры в командный файл неоходимо после названия командного файла через пробел написать передаваемые параметры.

15. ![Рис. 7. Арифметические операторы оболочки bash](/home/itmametkadihrov/Изображения/lab11/7.png){ #fig:001 width=70% }

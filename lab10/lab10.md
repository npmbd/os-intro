
---
# Front matter
lang: ru-RU
title: "Лабораторная работа № 10"
subtitle: "Текстовой редактор emacs"
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

Познакомиться с операционной системой Linux. Получить практические навыки работы с редактором Emacs.

# Выполнение лабораторной работы

1. Открыли emacs (рис. 1). 

![Рис. 1. emac](/home/itmametkadihrov/Изображения/lab10/1.png){ #fig:001 width=70% }

2. Создали файл lab07.sh с помощью комбинации Ctrl-x Ctrl-f (рис. 2).

![Рис. 2. Создание файла lab07.sh](/home/itmametkadihrov/Изображения/lab10/2.png){ #fig:001 width=70% }

3. Набрали текст (рис. 3):

	#!/bin/bash

	HELL=Hello

	function hello {

	LOCAL HELLO=World

	echo $HELLO

	}

	echo $HELLO

	hello

![Рис. 3. Текст](/home/itmametkadihrov/Изображения/lab10/3.png){ #fig:001 width=70% }

4. Сохранили файл с помощью комбинации Ctrl-x Ctrl-s.

5. Вырезали одной командой целую строку (С-k) (рис. 4).

![Рис. 4. Вырезка строки](/home/itmametkadihrov/Изображения/lab10/4.png){ #fig:001 width=70% }

6. Вставили эту строку в конец файла (C-y) (рис. 5).

![Рис. 5. Вставка в конец файла](/home/itmametkadihrov/Изображения/lab10/3.png){ #fig:001 width=70% }

7. Выделили область текста (C-space).

8. Скопировали область в буфер обмена (M-w).

9. Вставили область в конец файла (рис. 6).

![Рис. 6. Вставка области в конец файла](/home/itmametkadihrov/Изображения/lab10/5.png){ #fig:001 width=70% }

10. Вновь выделили эту область и на этот раз вырезали её (C-w).

11. Отменили последнее действие (C-/).

12. Переместили курсор в начало строки (C-a).

13. Переместили курсор в конец строки (C-e).

14. Переместили курсор в начало буфера (M-<).

15. Переместили курсор в конец буфера (M->).

16. Вывели список активных буферов на экран (C-x C-b) (рис. 7).

![Рис. 7. Cписок активных буферов](/home/itmametkadihrov/Изображения/lab10/6.png){ #fig:001 width=70% }

17. Переместились во вновь открытое окно (C-x) o со списком открытых буферов и переключитесь на другой буфер (рис. 8).

![Рис. 8. Переместились в окно со списком открытых буферов](/home/itmametkadihrov/Изображения/lab10/7.png){ #fig:001 width=70% }

18. Закрыли это окно (C-x 0).

19. Попробовали переключаться между буферами, но уже без вывода их списка на экран (C-x b).

20. Поделили фрейм на 4 части: разделили фрейм на два окна по вертикали (C-x 3), а затем каждое из этих окон на две части по горизонтали (C-x 2) (рис. 9).

![Рис. 9. Фрейм поделенный на 4 части](/home/itmametkadihrov/Изображения/lab10/8.png){ #fig:001 width=70% }

21. В каждом из четырёх созданных окон открыли новый файл и ввели несколько строк текста (рис. 10).

![Рис. 10. Новые файлы](/home/itmametkadihrov/Изображения/lab10/9.png){ #fig:001 width=70% }

22. Переключились в режим поиска (C-s) и нашли несколько слов, присутствующих в тексте (рис. 11, 12).

![Рис. 11. Поиск слова qwer](/home/itmametkadihrov/Изображения/lab10/10.png){ #fig:001 width=70% }

![Рис. 12. Поиск слова sdzx](/home/itmametkadihrov/Изображения/lab10/11.png){ #fig:001 width=70% }

23. Вышли из режима поиска, нажав C-g.

24. Перешли в режим поиска и замены (M-%), ввели qwer, который следует найти и заменить, нажали Enter , затем ввели asdf для замены. После того как подсветились результаты поиска, нажали ! для подтверждения
замены, в результате 1 строка файла 1.sh заменилась на asdf (рис. 13).

![Рис. 13. Замена текста](/home/itmametkadihrov/Изображения/lab10/12.png){ #fig:001 width=70% }

25. Попробовали другой режим поиска, нажав M-s o (рис. 14). Этот режим поиска показывает сколько есть совпадений, в каком буфере и показывает номера строк, где есть искомые слова.

![Рис. 14. Другой режим поиска командой M-s o](/home/itmametkadihrov/Изображения/lab10/13.png){ #fig:001 width=70% }

# Вывод

Познакомились с операционной системой Linux. Получили практические навыки работы с редактором Emacs.

# Ответы на контрольные вопросы

1. Emacs представляет собой мощный экранный редактор текста, написанный на языке высокого уровня Elisp.

2. Наличие большого количества различных сочетаний клавиш для работы.

3. Буфером называется объект, представляющий какой-либо текст.

	Окно — это прямоугольная область фрейма, отображающая один из буферов.

5. Буферы GNU Emacs и Quail Completions создаются по умолчанию при запуске emacs.

6. Ctrl+C потом l, Ctrl+c потом Ctrl+l.

7. Нажать комбинацию клавиш Ctrl+x 3.

8. Настройки emacs хранятся в файле . emacs

9. Эта клавиша смещает курсор налево.

10. Мне понравился редактор Emacs, потому что его можно использовать как файловый менеджер, эмулятор терминала, веб-браузер, почтовый клиент и т. д.

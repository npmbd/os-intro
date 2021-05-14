
---
# Front matter
lang: ru-RU
title: "Лабораторная работа № 5"
subtitle: "Основы интерфейса взаимодействия пользователя с системой Unix на уровне командной строки"
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

Приобретение практических навыков взаимодействия пользователя с системой
посредством командной строки.

# Выполнение лабораторной работы

1. Определили полное имя нашего домашнего каталога, путем вызова команды pwd (рис. 1).

	![	Рис. 1. Полное имя домашнего каталога](/home/itmametkadihrov/Изображения/lab05/1.png){ #fig:001 width=70% }

2. Перешли в каталог /tmp, для этого воспользовались командой cd /tmp (рис. 2).

![Рис. 2. Каталог /tmp](/home/itmametkadihrov/Изображения/lab05/2.png){ #fig:001 width=70% }

3. Вывели на экран содержимое каталога /tmp. Вывели обычной командой ls (рис. 3), тогда мы увидели содержание каталога; вывели командой ls -a (рис. 4), тогда мы увидели также скрытые файлы каталога; вывели командой ls -F (рис. 5), тогда получили информацию о типах файлов.

![Рис. 3. Содержимое каталога /tmp (команда ls)](/home/itmametkadihrov/Изображения/lab05/3.png){ #fig:001 width=70% }

![Рис. 4. Содержимое каталога /tmp (команда ls -a)](/home/itmametkadihrov/Изображения/lab05/4.png){ #fig:001 width=70% }

![Рис. 5. Содержимое каталога /tmp (команда ls -F)](/home/itmametkadihrov/Изображения/lab05/5.png){ #fig:001 width=70% }

4. Чтобы определить есть ли в каталоге /var/spool подкаталог с именем cron, сначала перешли в каталог /var, затем в каталог spoon, затем вывели содержимое этого каталога и нашли каталог cron (рис. 6).

![Рис. 6. Нашли каталог cron](/home/itmametkadihrov/Изображения/lab05/6.png){ #fig:001 width=70% }

5. Перешли командой cd в домашний каталог и вывели командой ls -l подробную информацию о файлах и каталогах, так мы увидели, что владельцем файлов и подкаталогов является itmametkadihrov (рис. 7). 

![Рис. 7. Содержимое домашнего каталога](/home/itmametkadihrov/Изображения/lab05/7.png){ #fig:001 width=70% }

6. В домашнем каталоге создали командой mkdir newdir новый каталог с именем newdir (рис. 8).

7. Создали в каталоге newdir новый каталог morefun (рис. 8).

![Рис. 8. Создание каталогов newdir и morefun](/home/itmametkadihrov/Изображения/lab05/8.png){ #fig:001 width=70% }

8. Используя одну команду mkdir letters memos misk создали каталоги letters, memos, misk (рис. 9).

9. Удалили одной командой ранее созданные каталоги: rm -r letters memos misk (рис. 9).

![Рис. 9. Создание каталогов letters, memos, misk](/home/itmametkadihrov/Изображения/lab05/9.png){ #fig:001 width=70% }

10. Попробовали удалить каталог newdir командой rm. Проверили, был ли каталог удален, для этого вывели содержимое домашнего каталога и увидели, что каталог не удалился (рис. 10).

![Рис. 10. Удаление каталога newdir командой rm](/home/itmametkadihrov/Изображения/lab05/10.png){ #fig:001 width=70% }

11. Удалили каталог newdir командой rm -r newdir и проверили, был ли удален каталог (рис. 11).

![Рис. 11. Удаление каталога newdir](/home/itmametkadihrov/Изображения/lab05/11.png){ #fig:001 width=70% }

12. С помощью команды man определили, для просмотра содержимого не только указанного каталога, но и подкаталогов, входящих в него нужно использовать команду ls -R (рис. 12).

![Рис. 12. Просмотр содержимого не только указанного каталога, но и подкаталогов](/home/itmametkadihrov/Изображения/lab05/12.png){ #fig:001 width=70% }

13. С помощью команды man определили, что отсортировать по времени последнего изменения выводимый список содержимого каталога с развёрнутым описанием файлов можно командой ls -lt (рис. 13).

![Рис. 13. Cортировка по времени последнего изменения](/home/itmametkadihrov/Изображения/lab05/13.png){ #fig:001 width=70% }

14. Использовали команду man для просмотра описания следующих команд: cd (рис. 14), pwd (рис. 15), mkdir (рис. 16), rmdir (рис. 17), rm (рис. 18). В результате мы узнали, что команда cd используется для изменения рабочего каталога; команда pwd выводит полный путь от корневого каталога к текущему рабочему каталогу; команда mkdir изпользуется для создания каталогов; команда rmdir удаляет каталог из файловой системы; команда rm удаляет файлы из каталога.

![Рис. 14. man cd](/home/itmametkadihrov/Изображения/lab05/14.png){ #fig:001 width=70% }

![Рис. 15. man pwd](/home/itmametkadihrov/Изображения/lab05/15.png){ #fig:001 width=70% }

![Рис. 16. man mkdir](/home/itmametkadihrov/Изображения/lab05/16.png){ #fig:001 width=70% }

![Рис. 17. man rmdir](/home/itmametkadihrov/Изображения/lab05/17.png){ #fig:001 width=70% }

![Рис. 18. man rm](/home/itmametkadihrov/Изображения/lab05/18.png){ #fig:001 width=70% }

15. Используя информацию, полученную при помощи команды history, выполнили следующие модификации нескольких команд из буфера команд и исполнили их (рис. 19).

![Рис. 19. Модификации команд](/home/itmametkadihrov/Изображения/lab05/18.png){ #fig:001 width=70% }

# Вывод

Приобрели практические навыки взаимодействия пользователя с системой
посредством командной строки.

# Ответы на контрольные вопросы

1. Командная строка (консоль или Терминал) – это специальная программа, которая позволяет управлять компьютером путем ввода текстовых команд с клавиатуры.

2. При помощи команды pwd можно определить абсолютный путь текущего каталога. Пример см. рис. 1.

3. При помощи команды ls и опции -F можно определить только тип файлов
и их имена в текущем каталоге. Пример см. рис. 5.

4. Имена скрытых файлов начинаются с точки. Для того, чтобы отобразить имена скрытых файлов, необходимо использовать команду ls с опцией a: ls -a. Пример см. рис. 4.

5. При помощьи команды rm можно удалить файлы, а командой rm -r каталоги. Одной и той же командой нельзя удалить файлы и каталоги, в этом мы убедились на примере пункта 10 настоящего отчета.

6. Командой history можно определить, какие команды выполнил пользователь в сеансе работы.

7. Если нажать на кнопку "стрелка вверх", то выведится ранее выполненные команды, так мы можем исправить и запустить на выполнение команду, которую мы уже использовал в сеансе работы. Пример см. рис. 19.

8. Если требуется выполнить последовательно несколько команд, записанный в одной строке, то для этого используется символ точка с запятой.

	Пример: 
	cd; ls

9. Если в заданном контексте встречаются специальные символы (типа
«.», «/», «*» и т.д.), надо перед ними поставить символ экранирования \ (обратный
слэш).

10. Чтобы вывести на экран подробную информацию о файлах и каталогах, необходимо использовать опцию l.  При этом о каждом файле и каталоге будет выведена
следующая информация:

	– тип файла,

	– право доступа,

	– число ссылок,

	– владелец,

	– размер,

	– дата последней ревизии,

	– имя файла или каталога.

11. Абсолютный путь — это путь, который указывает на одно и то же место в файловой системе, вне зависимости от текущего рабочего каталога или других обстоятельств. Пример : /home/itmametkadihrov/work

	Относительный путь представляет собой путь по отношению к текущему рабочему каталогу  пользователя. Пример: 2020-2021/laboratory

12. Чтобы получить информацию об интересующей нас команде: man (интересующая команда)

13. Для автоматического дополнения вводимых команд служит клавиша Tab.

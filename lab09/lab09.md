
---
# Front matter
lang: ru-RU
title: "Лабораторная работа № 9"
subtitle: "Текстовой редактор vi"
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

Познакомиться с операционной системой Linux. Получить практические навыки работы с редактором vi, установленным по умолчанию практически во всех дистрибутивах.

# Выполнение лабораторной работы

1. Создали каталог с именем ~/work/os/lab09 (рис. 1).

2. Перешли в созданный каталог (рис. 1).

3. Вызвали команду vi и создали файл hello.sh (рис. 1).

![Рис. 1. Создание каталога с именем ~/work/os/lab09](/home/itmametkadihrov/Изображения/lab09/1.png){ #fig:001 width=70% }

4. Нажали клавишу i и ввели текст показанный на рис. 2:

![Рис. 2. Редактирование hello.sh](/home/itmametkadihrov/Изображения/lab09/2.png){ #fig:001 width=70% }

5. Нажали Esc, затем ввели двоеточие для перехода в режим последней строки и нажали w (запись) и q (выйти), затем кнопкой Enter сохранили текст и завершили работу (рис. 3).

![Рис. 3. Сохранение файла](/home/itmametkadihrov/Изображения/lab09/3.png){ #fig:001 width=70% }

6. Сделали файл исполняемым (рис. 4).

![Рис. 4. Изменение прав доступа](/home/itmametkadihrov/Изображения/lab09/4.png){ #fig:001 width=70% }

7. Вызвали vi на редактирование файла vi ~/work/os/lab09/hello.sh (рис. 5).

![Рис. 5. Редактирование файла hello.sh](/home/itmametkadihrov/Изображения/lab09/5.png){ #fig:001 width=70% }

8. Установили курсор в конец слова HELL второй строки. Перешли в режим вставки и заменили на HELLO. Нажали Esc для возврата в командный режим (рис. 6).

![Рис. 6. Замена на HELLO](/home/itmametkadihrov/Изображения/lab09/6.png){ #fig:001 width=70% }

9. Установили курсор на четвертую строку и удалили слово LOCAL. Перешли в режим вставки и набрали следующий текст: local, нажали Esc для возврата в командный режим (рис. 7).

![Рис. 7. Замена LOCAL на local](/home/itmametkadihrov/Изображения/lab09/7.png){ #fig:001 width=70% }

10. Установили курсор на последней строке файла. Вставили после неё строку, содержащую следующий текст: echo $HELLO (рис. 8).

![Рис. 8. Вставка текста echo $HELLO](/home/itmametkadihrov/Изображения/lab09/8.png){ #fig:001 width=70% }

11. Нажали Esc для перехода в командный режим.

12. Удалили последнюю строку (рис. 9).

![Рис. 9. Удаление последней строки](/home/itmametkadihrov/Изображения/lab09/9.png){ #fig:001 width=70% }

13. Ввели команду отмены изменений "u" для отмены последней команды (рис. 10).

![Рис. 10. Отмена последней команды](/home/itmametkadihrov/Изображения/lab09/10.png){ #fig:001 width=70% }

14. Ввели символ ":" для перехода в режим последней строки. Записали произведённые изменения и вышли из vi (рис. 11).

![Рис. 11. Запись произведённых изменений и выход из vi](/home/itmametkadihrov/Изображения/lab09/11.png){ #fig:001 width=70% }

# Вывод

Познакомились с операционной системой Linux. Получили практические навыки работы с редактором vi, установленным по умолчанию практически во всех дистрибутивах.

# Ответы на контрольные вопросы

1. Редактор vi имеет три режима работы:

	– командный режим — предназначен для ввода команд редактирования и навигации по редактируемому файлу;

	– режим вставки — предназначен для ввода содержания редактируемого файла;

	– режим последней (или командной) строки — используется для записи изменений в файл и выхода из редактора.

2. Набрать символ q!, если требуется выйти из редактора без сохранения.

3. 0 (ноль) — переход в начало строки;

	$ — переход в конец строки;

	G — переход в конец файла;

	nG — переход на строку с номером n.


4. Редактор vi предполагает, что слово - это строка символов, которая может включать в себя буквы, цифры и символы подчеркивания.

5. Чтобы перейти в начало файла используется команда "0", чтобы перейти в конец файла - "G"

6. **Вставка текста:**

	а — вставить текст после курсора;

	А — вставить текст в конец строки;

	i — вставить текст перед курсором;

	ni — вставить текст n раз;

	I — вставить текст в начало строки.

	**Вставка строки:**

	о — вставить строку под курсором;

	О — вставить строку над курсором.

	**Удаление текста:**

	x — удалить один символ в буфер;

	d w — удалить одно слово в буфер;
	
	d $ — удалить в буфер текст от курсора до конца строки;

	d 0 — удалить в буфер текст от начала строки до позиции курсора;

	d d — удалить в буфер одну строку;

	n d d — удалить в буфер n строк.

	**Отмена и повтор произведённых изменений:**

	u — отменить последнее изменение;
	
	. — повторить последнее изменение.

	**Копирование текста в буфер:**

	– Y — скопировать строку в буфер;

	– n Y — скопировать n строк в буфер;

	– y w — скопировать слово в буфер.

	**Вставка текста из буфера:**

	p — вставить текст из буфера после курсора;

	P — вставить текст из буфера перед курсором.

	**Замена текста:**

	c w — заменить слово;
	
	n c w — заменить n слов;

	c $ — заменить текст от курсора до конца строки;

	r — заменить слово;

	R — заменить текст.

	**Поиск текста:**
	
	/ *текст* — произвести поиск вперёд по тексту указанной строки символов *текст*;

	? *текст* — произвести поиск назад по тексту указанной строки символов *текст*.

7. Использовать команду n i — вставить текст n раз;

8. u — отменить последнее изменение;

9. **Копирование и перемещение текста:**

	– : n,m d — удалить строки с n по m;

	– : i,j m k — переместить строки с i по j, начиная со строки k;

	– : i,j t k — копировать строки с i по j в строку k;

	– : i,j w *имя-файла* — записать строки с i по j в файл с именем имя-файла

	**Запись в файл и выход из редактора:**

	– : w — записать изменённый текст в файл, не выходя из vi;

	– : w *имя-файла* — записать изменённый текст в новый файл с именем *имя-файла*;

	– : w ! *имя-файла* — записать изменённый текст в файл с именем *имя-файла*;

	– : w q — записать изменения в файл и выйти из vi;

	– : q — выйти из редактора vi;

	– : q ! — выйти из редактора без записи;

	– : e ! — вернуться в командный режим, отменив все изменения, произведённые со времени последней записи.

10. Использовать команду $ — переход в конец строки;

11. **Опции:**

	Опции редактора vi позволяют настроить рабочую среду. Для задания опций используется команда set (в режиме последней строки):

	– : set all — вывести полный список опций;

	– : set nu — вывести номера строк;

	– : set list — вывести невидимые символы;

	– : set ic — не учитывать при поиске, является ли символ прописным или строчным.

12. В левом нижнем углу окна редактора vi можно посмотреть режим его работы.

13. ![Рис. 12. Граф взаимосвязи режимов работы редактора vi](/home/itmametkadihrov/Изображения/lab09/12.png){ #fig:001 width=70% }

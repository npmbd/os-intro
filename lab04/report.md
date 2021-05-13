
---
# Front matter
lang: ru-RU
title: "Лабораторная работа № 4"
subtitle: "Знакомство с операционной системой Linux"
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

Познакомиться с операционной системой Linux, получить практические навыки работы с консолью и некоторыми графическими менеджерами рабочих столов операционной системы.

# Выполнение лабораторной работы

1. Перешли на текстовую консоль для этого открыли терминал, затем нажали на сочетание клавиш Ctrl+Alt+F2. Всего на компьютере доступно 5 текстовых консолей.  (рис. 1, 2, 3, 4, 5)

![Рис. 1. Текстовая консоль tty2](/home/itmametkadihrov/Изображения/lab04/1.JPG){ #fig:001 width=70% }

![Рис. 2. Текстовая консоль tty3](/home/itmametkadihrov/Изображения/lab04/2.JPG){ #fig:001 width=70% }

![Рис. 3. Текстовая консоль tty4](/home/itmametkadihrov/Изображения/lab04/3.JPG){ #fig:001 width=70% }

![Рис. 4. Текстовая консоль tty5](/home/itmametkadihrov/Изображения/lab04/4.JPG){ #fig:001 width=70% }

![Рис. 5. Текстовая консоль tty6](/home/itmametkadihrov/Изображения/lab04/5.JPG){ #fig:001 width=70% }

2. Попробовали перемещаться между текстовыми консолями. Перемещение из одной текстовой консоли в другую можно осуществить путем нажатия сочетаний клавиш Alt+Fn (n = 2, 3, ..., 6 - номер текстовой консоли).

3. Зарегистрировались в текстовой консоли операционной системы. При этом использовали логин itmametkadihrov. При вводе пароля символы не отображаются. (рис. 6)

![Рис. 6. Регистрация в текстовой консоли](/home/itmametkadihrov/Изображения/lab04/6.png){ #fig:001 width=70% }

4. Завершили консольный сеанс. Для этого мы использовали комбинацию клавиш Ctrl+D.

5. Переключились на графический интерфейс. Для этого необходимо нажать комбинацию клавиш Alt+F1.

6. Ознакомились с менеджером рабочих столов. Менеджер запускаемый по умолчанию является GNOME.

7. Поочередно зарегистрировались в разных графических менеджерах рабочих столов (рис. 7).

![Рис. 7. Графические менеджеры](/home/itmametkadihrov/Изображения/lab04/6.JPG){ #fig:001 width=70% }

8. Ниже на скриншотах можно увидеть вид рабочего стола в разных графических менеджерах рабочих столов
(рис. 8, 9, 10, 11, 12)

![Рис. 8. Графический менеджер GNOME](/home/itmametkadihrov/Изображения/lab04/7.JPG){ #fig:001 width=70% }

![Рис. 9. ГрафическиЙ менеджер "Классический GNOME"](/home/itmametkadihrov/Изображения/lab04/8.JPG){ #fig:001 width=70% }

![Рис. 10. ГрафическиЙ менеджер "Рабочий стол Plasma"](/home/itmametkadihrov/Изображения/lab04/9.JPG){ #fig:001 width=70% }

![Рис. 11. ГрафическиЙ менеджер "Рабочий стол Plasma (безопасный режим)"](/home/itmametkadihrov/Изображения/lab04/10.JPG){ #fig:001 width=70% }

![Рис. 12. ГрафическиЙ менеджер "Сеанс"](/home/itmametkadihrov/Изображения/lab04/11.JPG){ #fig:001 width=70% }

9. Изучили список установленных программ. Запустили поочерёдно браузер Firefox (рис. 13), текстовый редактор (рис. 14), текстовый процессор LibreOffice Writer (рис. 15), эмулятор консоли (рис. 16)

![Рис. 13. Браузер](/home/itmametkadihrov/Изображения/lab04/12.png){ #fig:001 width=70% }

![Рис. 14. Текстовый редактор](/home/itmametkadihrov/Изображения/lab04/13.png){ #fig:001 width=70% }

![Рис. 15. Текстовый процессор](/home/itmametkadihrov/Изображения/lab04/14.png){ #fig:001 width=70% }

![Рис. 16. Эмулятор консоли](/home/itmametkadihrov/Изображения/lab04/15.png){ #fig:001 width=70% }

# Вывод

Познакомились с операционной системой Linux, получить практические навыки работы с консолью и некоторыми графическими менеджерами рабочих столов операционной системы.

# Ответы на контрольные вопросы

1. Компьютерный терминал - устройство, используемое для взаимодействия пользователя с компьютером или компьютерной системой, локальной или удалённой.

	Преимуществом командной строки является выполнение однотипных операций над множеством объектов. В системе с графическим интерфейсом потребуется очень много перетаскиваний.

2. Входное имя пользователя (Login) — название учётной записи пользователя.

3. Пароли пользователей хранятся в файле /etc/shadow

	В файле /etc/passwd поле password имеет значение x.

4. Настройки пользовательских программ хранятся в домашнем каталоге.

5. Входное имя у администратора ОС Unix это - UID=0.

6. Администратор имеет доступ к настройкам пользователей.

7. Процедура регистрации в системе обязательна для Linux. Каждый пользователь операционный системы имеет определенные ограничения на возможные с его стороны
действия: чтение, изменение, запуск файлов, а также на ресурсы: пространство на файловой системе, процессорное время для выполнение текущих задач (процессов). При этом
действия одного пользователя не влияют на работу другого. Такая модель разграничения
доступа к ресурсам операционной системы получила название многопользовательской.

8. Учётная запись пользователя содержит:

	– входное имя пользователя (Login Name);

	– пароль (Password);

	– внутренний идентификатор пользователя (User ID);

	– идентификатор группы (Group ID);

	– анкетные данные пользователя (General Information);

	– домашний каталог (Home Dir);

	– указатель на программную оболочку (Shell).

9. UID (User identifier) — внутренний идентификатор пользователя в системе — положительное целое число в диапазоне от 0 до
65535, по которому в системе однозначно отслеживаются действия пользователя.

	GID (Group identifier) — идентификатор группы пользователей в операционной системе.

10. Анкетные данные пользователя (General Information или GECOS) являются необязательным параметром учётной записи и могут содержать реальное имя пользователя
(фамилию, имя), адрес, телефон.

11. Домашний каталог — это личный каталог пользователя в операционной системе, где находятся его данные, настройки и т. д.

	В домашнем каталоге хранятся данные и настройки рабочей среды пользователя.

12. Мой домашний каталог называется itmametkadihrov

13. Администратор имеет возможность изменить содержимое домашнего каталога пользователя.

14. Учётные записи пользователей.

15. Символ * в поле password некоторой учётной записи в файле /etc/passwd означает, что пользователь не сможет войти в систему.

16. Виртуальные консоли — реализация концепции многотерминальной
работы в рамках одного устройства.

17. getty — программа для UNIX-подобных операционных систем, управляющая доступом к физическим и виртуальным терминалам (tty).

18. Весь процесс взаимодействия пользователя с системой с момента регистрации до выхода называется сеансом работы.

19. Toolkit (Tk, «набор инструментов», «инструментарий»)— кроссплатформенная библиотека базовых элементов графического интерфейса, распространяемая
с открытыми исходными текстами.

20. – GTK+ (сокращение от GIMP Toolkit) — кроссплатформенная библиотека элементов
интерфейса;

	– Qt — кросс-платформенный инструментарий разработки программного обеспечения
на языке программирования C++.
GTK+ состоит из двух компонентов:

	– GTK — содержит набор элементов пользовательского интерфейса (таких, как кнопка,
список, поле для ввода текста и т. п.) для различных задач;

	– GDK — отвечает за вывод информации на экран, может использовать для этого
X Window System, Linux Framebuffer, WinAPI.

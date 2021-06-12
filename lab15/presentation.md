---
## Front matter
lang: ru-RU
title: Лабораторная работа №15. Именованные каналы

author: |
	Маметкадыров Ынтымак
institute: |
	ФГАОУ ВО «Российский университет дружбы народов», Москва, Россия
date: 2021 г.

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

### Выполнил: Маметкадыров Ынтымак

### ФГАОУ ВО «Российский университет дружбы народов», Москва, Россия

# Цель работы

Приобретение практических навыков работы с именованными каналами.

# Создали необходимые файлы

![](/home/itmametkadihrov/Изображения/lab15/1.png)

# Добавили заголовочный файлы unistd.h и time.h в файл common.h

![](/home/itmametkadihrov/Изображения/lab15/2.png)

# В  файл  server.c  добавили  цикл  while  для  контроля  за  временем  работы сервера

![](/home/itmametkadihrov/Изображения/lab15/3.png)

![](/home/itmametkadihrov/Изображения/lab15/4.png)

# В  файл  client.c  добавили  цикл,  который  отвечает  за  количество сообщений  о  текущем  времени

![](/home/itmametkadihrov/Изображения/lab15/5.png)

![](/home/itmametkadihrov/Изображения/lab15/6.png)

# Создали Makefile

![](/home/itmametkadihrov/Изображения/lab15/8.png)

# Скомпилировали программу

![](/home/itmametkadihrov/Изображения/lab15/9.png)

# Проверили работу программы

![](/home/itmametkadihrov/Изображения/lab15/7.png)

# Вывод

Приобрели практические навыки работы с именованными каналами.

---
## Front matter
title: "Отчёт по лабораторной работе № 1"
subtitle: "Установка ОС Linux"
author: "Саенко Ангелина Андреевна"

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
mainfont: IBM Plex Serif
romanfont: IBM Plex Serif
sansfont: IBM Plex Sans
monofont: IBM Plex Mono
mathfont: STIX Two Math
mainfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
romanfontoptions: Ligatures=Common,Ligatures=TeX,Scale=0.94
sansfontoptions: Ligatures=Common,Ligatures=TeX,Scale=MatchLowercase,Scale=0.94
monofontoptions: Scale=MatchLowercase,Scale=0.94,FakeStretch=0.9
mathfontoptions:
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

Приобрести практические навыки установки операционной системы на
виртуальную машину.
# Задание

Установить операционную систему
Сделать настройку раскладки клавиатуры
Установить имя пользователя и названия хоста
Установить программное обеспечение для создания документации



# Выполнение лабораторной работы

Для начала откроем виртуальную машину и настроим её (рис. [-@fig:001]).

![Открытие виртуальной машины](image/1.png){#fig:001 width=70%}

Дадим имя для новой машины и выберем образ iso

![Настройка](image/2.png){#fig:002 width=70%}

Выбираем диск для установки

![Выбор диска](image/3.png){#fig:003 width=70%}

Установливаем имя и пароль для пользователя root.

![root](image/4.png){#fig:004 width=70%}

Устанавливаем имя и пароль для Вашего пользователя.

![Мой пользователь](image/5.png){#fig:005 width=70%}

После завершения установки операционной системы корректно перезапускаем
виртуальную машину.

![Перезапускаем машину](image/6.png){#fig:006 width=70%}

Отключаем носитель информации с образом.

![Изъятие диска](image/7.png){#fig:007 width=70%}

Входим в ОС под заданной при установке учётной записью.

![Вход](image/8.png){#fig:008 width=70%}

Переключаемся на роль супер-пользователя.

![Супер-пользователь](image/9.png){#fig:009 width=70%}

Далее нам необходимо установить средства разработки

![Установка средст разработки](image/10.png){#fig:010 width=70%}

Теперь выполняем обновление всех пакетов

![Обновление всех пакетов](image/11.png){#fig:011 width=70%}

Устанавливаем программы для удобства работы в консоли

![Установка программ](image/12.png){#fig:012 width=70%}

Используем автоматическое обновление и устанавливаем программное обеспеччение

![Установка ПО](image/13.png){#fig:013 width=70%}

Запускаем таймер

![Запуск таймера](image/14.png){#fig:014 width=70%}

В данном курсе мы не будем рассматривать работу с системой безопасности SELinux ,
поэтому отключим его. В файле /etc/selinux/config заменим значение
SELINUX=enforcing
на значение
SELINUX=permissive

![Замена значений в файле](image/15.png){#fig:015 width=70%}

Переключимся на роль супер-пользователя с помощью sudo -i и отредактируем
конфигурационный файл /etc/X11/xorg.conf.d/00-keyboard.conf

![Редактирование файла и перезагрузка машины](image/16.png){#fig:016 width=70%}

Запустим терминальный мультиплексор tmux

![Запуск мультиплексора](image/17.png){#fig:017 width=70%}

Создадим конфигурационный файл ~/.config/sway/config.d/95-system-keyboard-config.conf

![Создание файла](image/18.png){#fig:018 width=70%}

Отредактируем конфигурационный файл ~/.config/sway/config.d/95-system-keyboard-
config.conf

![Редактирование файла](image/19.png){#fig:019 width=70%}

Переключимся на роль супер-пользователя с помощью команды sudo -i

![Переключимся на роль супер-пользователя](image/20.png){#fig:020 width=70%}

Отредактируем конфигурационный файл /etc/X11/xorg.conf.d/00-keyboard.conf

![Редактируем файл по образцу](image/21.png){#fig:021 width=70%}

Установим имя хоста и проверим что всё установилось верно

![Установка имени хоста](image/22.png){#fig:022 width=70%}

Переключимся на роль супер-пользователя с помощью команды sudo -i

![Переключимся на роль супер-пользователя](image/23.png){#fig:023 width=70%}

Установим с помощью менеджера пакетов средство pandoc

![Установка pandoc](image/24.png){#fig:024 width=70%}

Пакет pandoc-crossref в стандартном репозитории отсутствует. Придётся ставить вручную,
скачав с сайта

![Скачивание pandoc-crossref](image/25.png){#fig:025 width=70%}

Проверим верно ли всё установилось

![Проверка](image/26.png){#fig:026 width=70%}

Установим дистрибутив TeXlive

![Установка TeXlive](image/27.png){#fig:027 width=70%}

Выполнение домашнего задания
Дождёмся загрузки графического окружения и откроем терминал. В окне терминала
проанализируем последовательность загрузки системы, выполнив команду dmesg.

![Получите следующую информацию.](image/28.png){#fig:028 width=70%}

Версия ядра Linux (Linux version).
Частота процессора (Detected Mhz processor).
Модель процессора (CPU0).
Объём доступной оперативной памяти (Memory available).
Тип обнаруженного гипервизора (Hypervisor detected).
Тип файловой системы корневого раздела.
Последовательность монтирования файловых систем.

![Вывод](image/29.png){#fig:029 width=70%}




# Выводы

В ходе работы установлена и настроена операционная система на виртуальной машине.
Выполнены задачи по настройке раскладки клавиатуры, установке ПО (Pandoc, TeXlive) и
обновлению пакетов. Проанализирована загрузка системы с помощью dmesg.
Приобретены навыки работы с виртуальными машинами и настройки ОС.

# Список литературы{.unnumbered}

::: {#refs}
:::

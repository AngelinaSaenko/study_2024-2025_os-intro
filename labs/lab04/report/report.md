---
## Front matter
title: "Отчёт по лабораторной работе № 4"
subtitle: "Продвинутое использование git."
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

Получение навыков правильной работы с репозиториями git.

# Задание

Выполнить работу для тестового репозитория.
Преобразовать рабочий репозиторий в репозиторий с git-flow и conventional
commits.

# Выполнение лабораторной работы

Для начала установим git-flow из коллекции репозиториев (рис. [-@fig:001]).

![Установка](image/1.png){#fig:001 width=70%}


![Установка](image/2.png){#fig:002 width=70%}

На Node.js базируется программное обеспечение для семантического версионирования и
общепринятых коммитов. Установим ПО

![Установка nodejs](image/3.png){#fig:003 width=70%}

![Установка pnpm](image/4.png){#fig:004 width=70%}

Для работы с Node.js добавим каталог с исполняемыми файлами, устанавливаемыми yarn,
в переменную PATH

![Запуск](image/5.png){#fig:005 width=70%}

![Перелогинимся или выполним](image/6.png){#fig:006 width=70%}

Данная программа commitizen используется для помощи в форматировании коммитов. При
этом устанавливается скрипт git-cz, который мы и будем использовать для коммитов.

![Добавление](image/7.png){#fig:007 width=70%}

Создаём репозиторий на GitHub. Для примера назовём его git-extended

![Создание репозитория](image/8.png){#fig:008 width=70%}

Делаем первый коммит и выкладываем на github

![Первый коммит](image/9.png){#fig:009 width=70%}

![Добавление удалённого репозитория в мой локальный Git-проект](image/10.png){#fig:010 width=70%}

![Отправка изменений](image/11.png){#fig:011 width=70%}

Далее сделаем конфигурацию для пакетов Node.js

![Конфигурация для пакетов Node.js](image/12.png){#fig:012 width=70%}

Необходимо заполнить несколько параметров пакета. Сконфигурим формат коммитов. Для
этого добавим в файл package.json команду для формирования коммитов

![Изменяем файл](image/13.png){#fig:013 width=70%}

Добавим новые файлы


![Добавление новых файлов](image/14.png){#fig:014 width=70%}

Выполним коммит

![Коммит](image/15.png){#fig:015 width=70%}

Выбираем нужное

![Выбор](image/16.png){#fig:016 width=70%}

Отправим на github

![Отправка](image/17.png){#fig:017 width=70%}

Инициализируем git-flow

![Инициализация git-flow](image/18.png){#fig:018 width=70%}

Проверим , что мы на ветке develop

![Проверка](image/19.png){#fig:019 width=70%}

Загрузим весь репозиторий в хранилище

![Загрузка репозитория](image/20.png){#fig:020 width=70%}

Установим внешнюю ветку как вышестоящую для этой ветки

![Установка внешней ветки](image/21.png){#fig:021 width=70%}

Создадим релиз с версией 1.0.0

![Создание релиза](image/22.png){#fig:022 width=70%}

Создадим журнал изменений

![Создание журнала изменений](image/23.png){#fig:023 width=70%}

Добавим журнал изменений в индекс


![Добавление журнала](image/24.png){#fig:024 width=70%}

Зальём релизную ветку в основную ветку

![Заливание релизной ветки](image/25.png){#fig:025 width=70%}

Отправим данные на github

![Отправка данных](image/26.png){#fig:026 width=70%}


![Отправка данных](image/27.png){#fig:027 width=70%}

Создадим релиз на github. Для этого будем использовать утилиты работы с github

![Создание релиза](image/28.png){#fig:028 width=70%}

Создадим ветку для новой функциональности

![Создание ветки](image/29.png){#fig:029 width=70%}

Далее, продолжаем работу c git как обычно.
По окончании разработки новой функциональности следующим шагом следует
объединить ветку feature_branch c develop

![Объединяем ветки](image/30.png){#fig:030 width=70%}

Создадим релиз с версией 1.2.3

![Создание релиза](image/31.png){#fig:031 width=70%}

Обновим номер версии в файле package.json. Установим её в 1.2.3

![Обновим номер версии в файле package.json. Установим её в 1.2.3](image/32.png){#fig:032 width=70%}

Создадим журнал изменений

![Создание журнала изменений](image/33.png){#fig:033 width=70%}

Добавим журнал изменений в индекс

![Добавление журнала изменений в индекс](image/34.png){#fig:034 width=70%}

Зальём релизную ветку в основную ветку

![Зальём ветку](image/35.png){#fig:035 width=70%}

Отправим данные на github

![Отправка данных](image/36.png){#fig:036 width=70%}

![Отправка данных](image/37.png){#fig:037 width=70%}

Создадим релиз на github с комментарием из журнала изменений

![Создание релиза](image/38.png){#fig:038 width=70%}










# Выводы

Освоены инструменты git-flow, commitizen и standard-changelog для управления ветками,
семантического версионирования и оформления коммитов. Настроен репозиторий с
поддержкой общепринятых коммитов, созданы и завершены релизы с автоматическим
обновлением версий и журналов изменений. Получены навыки эффективного управления
разработкой и выпуском проектов.

# Список литературы{.unnumbered}

::: {#refs}
:::

---
## Front matter
title: "Шаблон отчёта по лабораторной работе"
subtitle: "Простейший вариант"
author: "Дмитрий Сергеевич Кулябов"

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

Целью данной работы является приобретение практических навыков установки операционной системы на виртуальную машину, настройки минимально необходимых для дальнейшей работы сервисов

# Задание

установить на виртуальной машине операционную систему Linux(Fedora) и пакеты

# Теоретическое введение



# Выполнение лабораторной работы

у меня уже уставлена операционная система "Linux" в виртуальной машине, поэтому я прыгнул на часть "После установки". я использовал команду "sudo -i" чтобы переключаться на роль супер-пользователя (рис. [-@fig:001]).

![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:001 width=70%}

Потом я написал команду "dnf -y install tmux mc" для удобства работы в консоли (рис. [-@fig:002])

![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:002 width=70%}

Дальше я установил программное обеспечение для автоматического обновления вводя команду "dnf install dnf-automatic" (рис. [-@fig:003]).

![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:003 width=70%}

Потом с помощью редактора "nano" я открыл файл конфигурации "automatic.conf", но в этом случае я не изменял ничего (рис. [-@fig:004]).

![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:004 width=70%}

Потом ввел команду "systemctl enable --now dnf-automatic.timer" чтобы запустить таймер.

Мы не будем рассматривать работу с системной безопасности "Selinux", поэтому я отключил его с помощью редактора "nano" для открывания файла конфигурации находящего в каталоге "/etc/selinux/config". Мне надо было переписать несколькие строки как видно в (рис. [-@fig:005.1]) и (рис. [-@fig:005.2]).

![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:005.1 width=70%}

![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:005.2 width=70%}

Потом я установил драйверы для виртуальной машины. Сначала я написал команду "tmux" потом "sudo -i" для правильной работы команд. потом я установил "Development Tools" вводя команду "dnf -f group install "Development Tools" (рис. [-@fig:006]). 

![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:006 width=70%}

Потом я установил пакеты "DKMS" с командой "dnf -y install dkms" (рис. [-@fig:007]).

![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:007 width=70%}

Затем я включил диск дополнений гостевой ОС (рис. [-@fig:008]).

![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:001 width=70%}

И подмонтировал его в каталоге "/media" (рис. [-@fig:009]).

![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:009 width=70%}

И установил драйверы с помощью команды "/media/VBoxLinuxAdditions.run" (рис. [-@fig:010]).

![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:010 width=70%}

Потом я перегрузил виртуальную машину.

в моем случае моё имя соответствует на мой аккаунт и имя в терминале 

потом я установил программное обеспечение для создания документации. я написал команду "dnf -y install pandoc" потом я скачал две папки с программами и поставил в каталоге "/usr/local/bin."(рис. [-@fig:011]).

![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:011 width=70%}

Последный шаг было установление дистрибутив "TeXlive". я написал команду "dnf -y install texlive-scheme-full" и ждал. в этом случае время для установления было длинным.(рис. [-@fig:012]).

![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:012 width=70%}

Для решения домашнего задания я использовал две команды "dmesg | less" и "dmesg | grep -i "то, что ищем"" и нашел всю запрашиваемую информацию.

![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:013.1 width=70%}
![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:013.2 width=70%}
![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:013.3 width=70%}
![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:013.4 width=70%}
![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:013.5 width=70%}
![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:013.6 width=70%}
![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:013.7 width=70%}



Описываются проведённые действия, в качестве иллюстрации даётся ссылка на иллюстрацию 
(рис. [-@fig:001]).

![Название рисунка](image/placeimg_800_600_tech.jpg){#fig:001 width=70%}

# Выводы

Здесь кратко описываются итоги проделанной работы.

# Список литературы{.unnumbered}

::: {#refs}
:::

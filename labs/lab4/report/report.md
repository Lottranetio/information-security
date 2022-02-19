---
# Front matter
lang: ru-RU
title: "Отчет по лабораторной работе №4"
subtitle: "Информационная безопасность"
author: "Паландузян АК НПИбд-01-18"

# Formatting
toc-title: "Содержание"
toc: true # Table of contents
toc_depth: 2
lof: true # List of figures
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
  - \linepenalty=10 # the penalty added to the badness of each line within a paragraph (no associated penalty node) Increasing the υalue makes tex try to haυe fewer lines in the paragraph.
  - \interlinepenalty=0 # υalue of the penalty (node) added after each line of a paragraph.
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
  - \usepackage{amsmath}
  - \floatplacement{figure}{H} # keep figures where there are in the text
---

# Цель работы

Получить практические навыки работы в консоли с расширенными атрибутами файлов.

# Выполнение лабораторной работы

1. От guest проверим атрибуты /home/guest/dir1/file1. Заменим права на разрешающие чтение и запись для владельца файла. Установим расширенный атрибут /home/guest/dir1/file1 от guest, но получаем отказ.

![Права на файл, изменение атрибутов](img/1.png)

2. Делаем то же самое от суперпользователя. 

![Установка расширенного атрибута "а"](img/2.png)

3. От guest проверим атрибуты. Дозапишем file1 и прочитаем его, всё успешно. Удалить файл, стереть из него текст или переименовать его не получается. Устанавливаем на file1 права, запрещающие чтение и запись для владельца файла, получаем отказ. 

![Тест файла с установленным атрибутом "а"](img/3.png)

4. Убираем атрибут "a" с файла от имени суперпользователя. 

![Снятие расширенного атрибута "а"](img/4.png)

5. Повторяем все действия, все они прошли успешно.

![Тест файла после снятия атрибута "а"](img/5.png)

6. Добавляем атрибут "i" от имени суперпользователя.

![Установка расширенного атрибута "i"](img/6.png)

7. Теперь не получается выполнить никаких действий с файлом, т.к. он неизменяемый. 

![Тест файла с установленным атрибутом "i"](img/7.png)



# Выводы

Повысил свои навыки использования интерфейса командой строки, познакомилс на примерах с тем, как используются основные и расширенные атрибуты при разграничении доступа. Опробовал действие на практике расширенных атрибутов «а» и «i».
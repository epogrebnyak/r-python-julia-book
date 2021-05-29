# r-python-julia-book

> Why choose, learn them all: R, Python and Julia for economics and finance.

This is a draft of a book (collection of learning materials), based on 
teaching of computational courses to economics, management and finance students
at NES, HSE, GSOM SPBU and Finec MGIMO.

We would like to collect in one place things we got tired of repeating,
so that we can provide background reading and links to reresouces 
to the students before class. Hope it makes a fair guide to self-study too.

Another hope is that after writing out basic programming stuff we can move on to
things more relevant to econ/finance (datasets, reproducible research) 

We are writing the draft in Russian, some courses we taught are in English, 
so there may be an English version too. 

Our programming language preferences:

- Evgeniy: Python first, used R before, tried Julia
- Marcel: R first, migrating to Python


# Что? Зачем? Для кого?

Вводный курс для экономистов "Основы программирования и анализа данных 
на R, Python и Julia".

Основная идея - собрать в одном месте материалы по обучению программированию 
по минимум двум языкам - R и Python, и, по возможности, Julia. 

Мы делаем акцент на применении этих языков в области экономики и финансов. 

Для каких обучающихся эти материалы?

1. начинаю изучать Python или R "с нуля" - до этого не программировал(а)  
2. знаком(а) с одним языком программирования и хочу попробовать другой
3. хочу работать с экономическими и финансовыми данными
4. заинтересован(а) улушить качество кода, навыки и процессы работы с данными и кодом

Для преподавателей эти материалы полезны в случае, если:

- вы хотите ввести R, Python и Julia в свои курсы, которые пока читаются без них
  и вам нужны ссылки на базовые материалы и отдельные примеры упражнений
- вы сами работете с R, Python и Julia и хотите вовлечь в эту работу больше коллег - материалы 
  помогут рассказать о базовых вещах, не пересказывая их много раз
- хотите перейти с одного языка программирования на другой

Введение
========

- Зачем нам столько языков программирования?
  - [сравним их](https://benchmarksgame-team.pages.debian.net/benchmarksgame/index.html)  
  - <https://rosettacode.org/wiki/Rosetta_Code>
  
- История от Matlab и Eview до tidyverse, tensorflow и Julia  
- Барьеры в изучении програмирования и как их обойти 
- Эконометрика vs машинное обучение vs data science
- Рынок труда - вакансии со знанием R, Python, Julia

Overview videos:

- [Overview and History of R](https://www.youtube.com/watch?v=STihTnVSZnI)
- [The Story of Python by Guido van Rossum](https://www.youtube.com/watch?v=J0Aq44Pze-w)
- Julia:
  - [Edelman](https://www.youtube.com/watch?v=rZS2LGiurKY)  
  - [Karpinski](https://www.youtube.com/watch?v=DRKKAFYM9yo&t=23s) 
  - [Bezanson](https://www.youtube.com/watch?v=W6I1zQ16_44) 
  - [Shah](https://www.youtube.com/watch?v=cLFfTE2KWrk)

Other:

- [Why Python is huge in finance? by Daniel Roos](https://www.youtube.com/watch?v=kBwOy-6CtAQ&t=1299s)
- [Rust Crash Course by Brad Traversy](https://www.youtube.com/watch?v=zF34dRivLOw)- [Sargent - Economic models](https://www.youtube.com/watch?v=0Mf_LvwxFqY)
- [Язык Julia - сравнение простых программ с Python и C](https://www.youtube.com/watch?v=5sdrltkxm2Q)
- [Intro to Julia tutorial (version 1.0)](https://www.youtube.com/watch?v=8h8rQyEpiZA)
- [How We Wrote a Textbook using Julia](https://www.youtube.com/watch?v=ofWy5kaZU3g)
- [When compiler technology meets Market Risk Management](https://www.youtube.com/watch?v=4vDub-yoX1E&list=PLP8iPy9hna6Tl2UHTrm4jnIYrLkIcAROR&index=12)

Часть 1. До программирования
============================

Идеи программирования:

- как работает компьютер
- как работает интернет
- что такое компьютерная программа
- программирование как problem-solving

Что пригодится разработчику:

- командная строка
- файловая система, пути, названия файлов
- текстовый редактор
- git/github
- markdown
- удаленная машина
- отличия операционных систем

Установка R, Pyton, Julia:

- почему сложно и что может пойти не так
- удаленный доступ (Colab и аналоги)
- установить на своем компьютере
- библиотеки и пакетные менеджеры
- сборки RStudio / Anaconda, феномен "одной компании на язык програмирования"
- виртуальные окуржения (venv)

Скрипт, модуль, пакет

Ноутбуки

- ноутбук Jupyter
- сервис Google Colab
- другие ноутбуки и сервисы (Pluto.jl)

Часть 2. Язык программирования
==============================

Базовые возможности языка - синтаксис и стандартная библиотека.

#### Комментарий

Сложности:

- синтаксис это еще не программирование, нужны структуры данных и алгоритмы 
- связь с привычными для студента приложениями - офисными, web, другими 
- "вэбчик это не программирование"

На примере Python - много языков в одном:

- pandas вообще не похож на pure python
- async/await 
- pattern matching
- "раньше можно было рассказать python за 2 дня"

#### Привет, мир!

```python.exe -c "print('Hello, world!')"```

Задание - разберем, как эта программа работает:

- что такое `python.exe`, где он находится, как нам удалось его запустить?
- где сама программа?
- какие части есть у этой программы?
- куда она выведен результат работы программы?
- как может быть модифицирована эта программма?
- что может пойти не так?

```
!echo "print('Hello, world!')" > hello.py
!cat hello.py
!python hello.py
```

#### Значения (value) и выражения (expression)

- целое
- действительное
- строка
- выражения 

#### Переменные 

#### Структуры данных (containers)

- список (list) 
- словарь (dictionary)
- кортеж (tuple)
- набор (set)
- итерирование по элементам и распаковка
- строка как список символов

#### Управление

- if/else
- for/range
- while
- case

Checkpoint: напишите код для инверсии (изменения порядка следования символов) строки.

#### Функции

Функции 1:

- логика - зачем функция нужна, что делает?
- откуда берутся функции: написали сами или импортировали (стандартная библиотека или пакет)
- синтаксис `def` / `return`
- аргументы функции
- docstring функции
- аннотации типов (type annotations) 

Функции 2:

- что значит хорошая функция?
- как назвать функцию
- unit тесты и основы TDD

#### Классы

- немного света на ООП, сравнение с функциональным программированием
- в первом приближении класс - это структура данных, склеенная методами для работы 
- синтаксис классов нужен для pandas и например .method() в строках 
- актуально для Python (everything is a class), но не для R/Julia 

#### Взаимодействие программы с внешним миром

- чтение и запись файлов
- аргументы командной строки (но не для Colab)
- пожалуйста, не надо заданий с `input`

#### Качество кода и рефакторинг


Часть 3. Библиотеки
====================

Научные вычисления

- работа с матрицами (numpy)
- научные вычисления (scipy) 

Датафреймы (dataframe)

- встроенные в R 
- pandas в python
- DataFrame.jl
- ускорения и расширения фреймов

Графические пакеты 1

- ggplot (R)
- maplotlib (Python)
- makie (?, Julia)

Графические пакеты 2

Dashboards

- Shiny (R)
- Streamlit (Python)

Часть 4. Работа с данными
=========================

Сериализация данных:

- csv
- json
- yaml
- toml
- xml

API данных:

- fred
- quandl 

Взаимодействие с Excel

Экономические и финасовые данные

- копроративный датасет
- данные финасовых рынков

Эконометрические пакеты

- базовый R
- statmodels, scipy-learn
- пакеты Julia

Часть 5. Новые темы
===================

- популярные библиотеки в языках 
- сравнение языков программирования
- примеры проектов 
- контрольные вопросы
- что хорошо делать в каждом языке программироания
- а где же машинное обучение, нейронки и криптовалюты?
- воспроизводимые исследования


Вопросы и ответы
================


Авторы
======

- Евгений Погребняк
- Марсель Салихов

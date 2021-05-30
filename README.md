# r-python-julia-book

> Why choose, learn them all: R, Python and Julia for economics and finance.

This draft is based on our experience in teaching various computational courses 
to economics and finance students at Russian universities: NES, HSE, GSOM SPBU and Finec MGIMO.

Below we are writing the draft in Russian, but as we taught some courses in English, 
so there may be an English version too. 

Our programming language preferences:

- Evgeniy: Python first, used R before, tried Julia and moderately influenced by Haskell
- Marcel: R first, migrating to Python

## Book goals

Goal #1 is to collect good references in one place, so that we can provide 
background reading to the students before class more easily.  
Hope the references would make a fair guide for self-study too.

Goal #2 is avoid repeating common stuff (how to start Python, etc) and move 
more quickly to fruitful domain area tasks - econ/finance datasets and reproducible research.

Subtask for #1 and 2: provide more modularuty for the computational courses, avoid
teaching everything in one shot - installing python, syntax, libraries, machine learning
and a little cool neural net all in one course.  

Goal #3 is to lower the barriers in learning programming and foster a
culture that celebrates small credible wins and stimulates problem-solving 
in iterations, also allows teamwork. 

Goal #4 is to make economists better programmers (git, shell, tests) and  
more competitive as "data scientists" or "data engineers" in the job market.

Goal/claim #5 - learning R AND Python AND Julia AND some other cool programming language
(like Rust, perhaps) is better than wasting time on "which language is better for me in 2021".

Hidden aspiration (#6) - can we teach probability, stats and metrics as code-first 
disciplines? Starting from I have got a list of numbers - what can I do next?

## Admired peer publications

- [Quantecon](https://quantecon.org/) - a pioneer in using both Python and Julia for teaching in parallel 
- [Jesús Fernández-Villaverde](https://www.sas.upenn.edu/~jesusfv/teaching.html) - detailed intro to computing for economists 
- [SciPy Lectures](https://scipy-lectures.org/) - ML explained simply, a gem.

# Что? Зачем? Для кого?

Вводный курс для экономистов "Основы программирования и анализа данных на R, Python и Julia".

Основная идея - собрать в одном месте материалы по обучению программированию 
по минимум двум языкам - R и Python, и, по возможности, Julia. 

Мы делаем акцент на применении этих языков в области экономики и финансов. 

Для каких обучающихся эти материалы?

1. начинаю изучать Python или R "с нуля" - до этого не программировал(а)  
2. знаком(а) с одним языком программирования и хочу попробовать другой
3. хочу работать с экономическими и финансовыми данными и моделями
4. заинтересован(а) улушить качество своего кода, навыки и процессы работы с данными и кодом

Для преподавателей эти материалы полезны в случае, если:

- вы хотите ввести R, Python и Julia в свои курсы, которые пока читаются без них
  и вам нужны ссылки на базовые материалы и отдельные примеры упражнений
- вы сами работете с R, Python и Julia и хотите вовлечь в эту работу больше коллег - материалы 
  помогут рассказать о базовых вещах, не пересказывая их много раз
- хотите перейти с одного языка программирования на другой

Введение
========

#### Языки программирования (ЯП):

- Зачем нам столько языков программирования?
  - [сравним их](https://benchmarksgame-team.pages.debian.net/benchmarksgame/index.html)  
  - [где еще можно посмотреть разный код](https://rosettacode.org/wiki/Rosetta_Code)
  - объектные и функциональные, статическая и динамическая типизация и легко ли живется компилятору
- История количественных вычислений от Matlab и Eview до tidyverse, tensorflow и Julia  
- Так ли плох Excel?

Extra links:

- [Рахим - Мысли и методы - история Lisp, в двух частях](https://soundcloud.com/mimpod/episode_56?in=mimpod/sets/all_episodes)
- [Rust Crash Course by Brad Traversy](https://www.youtube.com/watch?v=zF34dRivLOw)


#### Личный путь:

- Барьеры в изучении програмирования и как их обойти 
- Эконометрика vs машинное обучение vs data science
- Рынок труда - вакансии со знанием R (есть), Python (есть), Julia (их нет)

#### Обзорные видео // Overview videos:

- [Overview and History of R](https://www.youtube.com/watch?v=STihTnVSZnI)
- [The Story of Python by Guido van Rossum](https://www.youtube.com/watch?v=J0Aq44Pze-w)
- Julia:
  - [Edelman](https://www.youtube.com/watch?v=rZS2LGiurKY)  
  - [Karpinski](https://www.youtube.com/watch?v=DRKKAFYM9yo&t=23s) 
  - [Bezanson](https://www.youtube.com/watch?v=W6I1zQ16_44) 
  - [Shah](https://www.youtube.com/watch?v=cLFfTE2KWrk)

Extra links:

- [Why Python is huge in finance? by Daniel Roos](https://www.youtube.com/watch?v=kBwOy-6CtAQ&t=1299s)
- [Sargent - Economic models](https://www.youtube.com/watch?v=0Mf_LvwxFqY)

Julia:

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

- функции, давать ли объекты
- pandas вообще не похож на pure python
- async/await 
- pattern matching
- "раньше можно было рассказать python за 2 дня, сейчас нет"

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

Типы данных:

- целое число (`int`)
- действительное число (`float`)
- строка (`str`)

Упраженение: каких типов данных не хватает?

Выражения: `2*2`, `"Hi, " + "all!"` 

#### Переменные 

Оператор присваивания (это вам не игрушки, зачеркнуто) - это не математическое равенство. Глубокий смысл `<-` в R.

#### Структуры данных (containers)

Структуры данных:

- список (list) 
- словарь (dictionary)
- кортеж (tuple)
- набор (set)

Что с ними делать:

- итерирование по элементам и распаковка
- строка как список символов

Extra:

- хитрые структуры данных, которые экономисту знать обычно не положено
- ссылки на курсы по data structures and algorithms
- аннотации типов и mypy

#### Управление

- if/else
- for/range
- while
- case / pattern matching 

Checkpoint: напишите код для инверсии (изменения порядка следования символов) строки.

#### Функции

Функции 1:

- логика - зачем функция нужна, что делает?
- откуда берутся функции: написали сами или импортировали, откуда импортировали - стандартная библиотека или пакет
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
- синтаксис классов нужен для pandas и, например, .method() в строках 
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

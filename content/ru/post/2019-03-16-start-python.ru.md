+++
title = "Начать (и успешно продолжить) программировать на Python"
date = 2019-03-15T10:57:57+03:00
draft = false

images = ["https://pbs.twimg.com/media/D1oIye5WwAAK12v?format=jpg&name=medium"]

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["python", "clean code"]
categories = ["programming"]

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
[image]
  # Caption (optional)
  caption = ""

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = ""

+++

[![](https://pbs.twimg.com/media/D1oIye5WwAAK12v?format=jpg&name=medium)](https://pbs.twimg.com/media/D1oIye5WwAAK12v?format=jpg&name=medium)

C чего начать? 
--------------

Количество  курсов по Python немыслимо, на фоне этого разнообразия по 
сбалансированности содержания мне нравятся следующие три[^3]. 

Выбор номер один - [learn-python О.Твердохлеба](https://github.com/trekhleb/learn-python)[^1]. 
Лучше всего подойдет тем, кто когда-то начинал программировать (например, Basic или Pascal) и хочет восстановить навыки. 

Хорошие вводные есть в [лекциях QuantEcon](https://lectures.quantecon.org/py/index_learning_python.html) 
и в [лекциях SciPy](http://scipy-lectures.org/intro/language/python_language.html). 
Целиком наборы лекций посвящены более сложным темам, это положительно 
сказывается на содержании начальных глав - ничего не пропускают, но и долго не топчутся. 

Если нужна именно книга, то оживленная деятельность идет вокруг [The Hitchhiker’s Guide to Python](https://docs.python-guide.org), в ней автор довольно быстро переходит к описанию приложений и библиотек[^2].

[^1]: Еще более популярный репозитарий того же автора посвящен [машинному обучению](https://github.com/trekhleb/homemade-machine-learning).

[^2]: Часто также рекомендуют [Learn Python the Hard Way (Zed Shaw)](https://learnpythonthehardway.org/python3/) (активно обновляется) и [Dive into Python 3 (Mark Pilgrim)](https://www.diveinto.org/python3) (менялся адрес сайта, версия выглядит застывшей). Учить язык по ним сейчас бы не стал, но как сборник упражнений - хороший вариант.

[^3]: Вся статья начиналась с https://github.com/epogrebnyak/learn/blob/master/pure_python_guide.md

План изучения
-------------

Я выписал шаги между самым первым запуском интерпретатора 
и далекими, непонятными, темными сторонами языка, которые будут понятны.

### 1. Где живет программа

&nbsp;       | Установить Python
-------------|---------------------------------------------------------------------------
Идея         | `python.exe` это исполняемый файл где-то в файловой системе.<BR> Он запускается с аргументами  и опциями.
1 строка     | `python --version`
Сложности    | Переменная PATH, конфликты версий
Откуда...    | ... установить? [Anaconda](https://www.anaconda.com/distribution).


&nbsp;       | REPL (`read-eval-print loop`)
-------------|---------------------------------------------------------------------------
Идея         | Программа это текстовый файл. Интепретатор это цикл.
1 строка     | `print ('Hello, world!')`, `python -c "print('Hello, world!')"`
Сложности    | Принять, что IDE - это не сам Python. 

### 2. Основная часть синтаксиса и логики языка

#### Выражения и операторы. Переменные. 

>  Интерпретатор может поработать калькулятором.

```python
>> 1 + 3 * (10 - 2)
25
```

#### Типы и структуры данных. 

> Числа и строки разные вещи. 

```python
>> isinstance("abc", str) & isinstance(1, int)
True
```

> Списки и словари (containers) полезны.

```python
>> colors = ['red', 'blue', 'green', 'black', 'white']
>> colors[0]
"red"
>> colors[2:4]
['green', 'black']
```

```python
>> {1:"I", 2:"II", 3:"III", 4:"IV", 5:"V"}[4]
"IV"
```

> В Python - особый синтаксис преобразования элементов массива ("распаковка").

```python
>> [(i, (i*9/5)+32) for i in range(-25, 30+1, 5)]
[(-25, -13.0), (-20, -4.0), (-15, 5.0), (-10, 14.0), 
 (-5, 23.0), (0, 32.0), (5, 41.0), (10, 50.0), 
 (15, 59.0), (20, 68.0), (25, 77.0), (30, 86.0)]
```


#### Модуль

> Файл с текстом программы и есть модуль. Объектты из других модулей можно импортировать в свою программу.

```python
>> from sys import version 
>> print(version)
3.6.0 |Anaconda 4.3.1 (64-bit)| (default, Dec 23 2016, 11:57:41)
```

#### Функции. Стандартная библиотека.

> Вычисления и операции можно сгруппировать. 

```python
import math     
def roots(a, b, c):
    """Return a tuple with quadratic equation roots."""
    d = b**2-4*a*c 
    try: 
        r = math.sqrt(d) / (2 * a)
    except ValueError:
        raise ValueError("Cannot calculate real roots") 
    x0 = - b / (2 * a)
    return x0 - r, x0 + r
```

> Справочник стандартной библиотеки рекомендуется держать под подушкой.

```python
>> min(5, 7)
5
>> len('abc')
3

>> from datetime import datetime
>> print(datetime.now())
2019-03-16 19:14:41.536899
```

#### Условное исполнение `if-else`. Цикл `for`.

> Исполнение программы может куда-то пересакивать.

```python
for x in [1,2,3,4]: 
    if (x % 2) == 0:
        print(x, "is even.")
    else:
        print(x, "is odd.")    
```

#### Все остальное, о чем учат в базовых курсах

Пункты выше описывают минимум лексики языка, с которой фактически можно работать. 
За бортом остаются:

- генераторы и итераторы
- пакеты, `__init__.py`
- дебаггер, логирование, предупреждения
- исключения (exceptions)
- классы

Тем не менее, повторю еще раз ссылки на базовые курсы, в них все есть:

1. [trekhleb/learn-python](https://github.com/trekhleb/learn-python)
2. [лекции QuantEcon](https://lectures.quantecon.org/py/index_learning_python.html)
3. [лекции SciPy](http://scipy-lectures.org/intro/language/python_language.html)


### 3. Дальнейшие важные пункты

Ниже чеклист чуть более продвинутых тем, которые так или иначе возникают при изучении и использовании
языка.


<table>
<tr>
<td>Ввод-вывод (IO)</td>
<td>
{{% md %}}

- файлы: `with`/`open`, `csv` + `pathlib`
- CLI: `sys.args` + [docopt](http://docopt.org/)   

{{% /md %}}
</td>
</tr>

<tr><td>
Регулярные выражения и форматы
</td><td>{{% md %}}

- [regex101.com](https://regex101.com)
- [pyformat](https://pyformat.info)
- [форматы даты и времени](http://strftime.org/)

{{% /md %}}</td></tr>

<tr>
<td>Структура программ</td>
<td>
{{% md %}}

- [скрипты и программы](https://python-3-patterns-idioms-test.readthedocs.io/en/latest/PythonForProgrammers.html#scripting-vs-programming)

{{% /md %}}
</td>
</tr>


<tr>
<td>Аннотирование и документация</td>
<td>
{{% md %}}

- `PEP 257`, docstrings, `sphinx`
- `PEP8`, `autopep8`, `black`
- ["идиоматический" Python](https://gist.github.com/sloria/7001839)

{{% /md %}}
</td>
</tr>

<tr><td>
Менеджеры пакетов
</td><td>{{% md %}}

- `pip`, `requirements.txt`
- `pipenv`, `conda`, `poetry`
- структура пакета, `setuptools`
  
{{% /md %}}</td></tr>

<tr><td>
Сторонние библиотеки
</td>
<td>
{{% md %}}
- Databases, SQL ([dataset](https://dataset.readthedocs.io/en/latest/)) 
- Web (`requests`, `flask`)
{{% /md %}}</td></tr>

<tr><td>Тестирование</td>
<td>
{{% md %}}

- `assert`
- `unittest`, `pytest`
- dependency injection
- continious integration (CI)

{{% /md %}}
</td>


<tr><td>Объекты (OOП)</td>
<td>
{{% md %}}

- "Everything is an object"
- `id()`
- [cat vs dog](http://www.jesshamrick.com/2011/05/18/an-introduction-to-classes-and-inheritance-in-python/)
- `dir()`
- [ABCs](https://docs.python.org/3/library/abc.html)

{{% /md %}}</td></tr>


<tr><td>
Алгоритмы и паттерны
</td><td>{{% md %}}

- [алгоритмы](https://github.com/TheAlgorithms/Python), O-notation
- [design patterns](https://github.com/faif/python-patterns)
- [дизайн API](https://people.mpi-inf.mpg.de/~jblanche/api-design.pdf)

{{% /md %}}</td></tr>

<tr><td>
Среды разработки (IDE)
</td><td>
{{% md %}}

- vim, npp
- IDLE, VSCode, Pycharm
- Jupyter

{{% /md %}}</td></tr>


<tr><td>
Производительность
</td>
<td>
{{% md %}}

- [командная строка](https://github.com/epogrebnyak/the-art-of-command-line)
- горячие клавиши редактора
- git
- markdown

{{% /md %}}</td></tr>
</table>

<!--
Вне рамок описания:
  - pandas, matplotlib, сравнение [python с R](https://pandas.pydata.org/pandas-docs/stable/getting_started/comparison/comparison_with_r.html) другими языками
  - type hints
-->

Буду признателен, если расскажете, какие вехи были у вас в изучении python 
что было или остается сложным, что сейчас изчаете и что посоветуте почитать.

Педагогика какая-то в этом есть?
--------------------------------

Мне кажется, основная проблема в обучении программированию - не упрощение или переупаковка материала, 
а поддержание мотивации обучающихся. 

Хорошо известно, что обучение лучше идет с конкретными примерами, задачами из 
сферы знаний пользователя, кейсы и так далее. Проблема с этими материалами - как с курицей и яйцом: пока навыков мало-  освоить сложный пример нельзя, а простые примеры редко цепляют подлинный интерес обучающихся. 

Выход из этого круга либо "сверху" (показать как работает итоговая программа и разобраться в начинке - пример *fast.ai*), "сбоку" (программы поменьше и разбор быстрее, *Learn Python the Hard Way*) или "снизу" (все-таки запастись терпением на долгую подготовку, *Norwig*).

Пара ссылок на тему "а как учить?":

- [Ten quick tips for teaching programming (2018)](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1006023)
- [The Best Way To Learn How To Code (3 правила)](https://www.reddit.com/r/learnprogramming/comments/5zc24o/the_best_way_to_learn_how_to_code/)
- [П.Норвиг. Научитесь программировать за 10 лет](http://norvig.com/21-days.html)

<!-- 
- [Требования к языку программирования и среде обучения](http://worrydream.com/LearnableProgramming/)
-->

Учить не Python, а computer science
-----------------------------------

Почти классика:

- [Thinking Computer Science](http://interactivepython.org/courselib/static/thinkcspy/index.html)

Больше хардкора:

- <https://teachyourselfcs.com/>
- <https://github.com/ossu/computer-science>
- <https://github.com/donnemartin/system-design-primer>


А как же Coursera?
-------------------

Почему бы не попробовать, но есть риски:

> "Using online tutorials is like trying to learn how to cook by stabbing at random buttons on an unlabeled microwave." [A blog in 2012](https://www.technologyreview.com/s/429438/dear-everyone-teaching-programming-youre-doing-it-wrong/)

> "Этот datacamp... Он по-моему ничему вообще не учит." От знакомого, 2019.


Откуда брать мотивацию?
-----------------------

#### Github 

 Вкратце ситуацию вокруг [topics/python](https://github.com/topics/python) и [trending/python](https://github.com/trending/python) можно изложить так: <!--(https://stackoverflow.com/users/1758363/epo?tab=profile): -->

 - используем `requests`/`scrapy`
 - чтобы загрузить в `pandas` данные c сайтов на  `flask`/`django`
 - и поработать с ними в `tensorflow`/`keras`
 - на машинах под управлением `ansible`/`docker-compose`
 - временами изучая `awesome-python`/`system-design-primer`.

<!---
Со звездами Github есть проблема в том, что базовые инфраструктурные библиотеки (например, проекты NumFOCUS) не получают так уж много звезд, потому что все считают из за данность.
-->

#### Опрос PyCharm

[Python developers survey 2018](https://www.jetbrains.com/research/python-developers-survey-2018) рассказывает о том, что на самом деле пилят питонисты, но опять таки - с их слов.

#### build-your-own-x

Много небольших проектов под Python в [build-your-own-x](https://github.com/danistefanovic/build-your-own-x): от интерпретатора Lisp до своей маленькой операционной системы. Основной приницп: пока что-нибудь сам не ~~сломаешь~~ сделаешь - не разберешься.


#### Проект Эйлер

На [проекте Эйлер](http://euler.jakumo.org/problems.html) много математических задач.


#### Stack Overflow

Топ вопросов по голосам пользователей в [Stack Overflow](https://stackoverflow.com/questions/tagged/python?sort=votes) дает представление о 
наименее понятных, но при этом востребованных сторонах языка. Лидер рейтинга - ключевое слово `yield`.


Приложения 
----------

{{% alert note %}}

 А всю ли лексику языка я знаю? Это можно проверить по ключевым словам (keywords),
 [операторам](https://docs.python.org/3.7/reference/lexical_analysis.html#operators) (operators), [разделителям](https://docs.python.org/3.7/reference/lexical_analysis.html#delimiters) (delimiters) и еще нескольким символам (`'`, 
 `"`, `#`, `\`):

- ключевые слова 
 
```python
>> import keyword
>> print(keyword.kwlist)

['False', 'None', 'True', 'and', 'as', 'assert', 'break', 
 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 
 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 
 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 
 'return', 'try', 'while', 'with', 'yield']
```

- операторы
 
```python
+       -       *       **      /       //      %      @
<<      >>      &       |       ^       ~
<       >       <=      >=      ==      !=
```
- разделители

```python
(       )       [       ]       {       }
,       :       .       ;       @       =       ->
+=      -=      *=      /=      //=     %=      @=
&=      |=      ^=      >>=     <<=     **=
```

{{% /alert %}}


{{% alert note %}}

Две вещи могли бы сделать Python идеальным языком программирования лично для меня:
  
  1. возможность отключить динамическую типизацию и перейти к статическим типам данных
  2. оператор `.` для склеивания функций `foo . spam `

{{% /alert %}}

#### Сноски
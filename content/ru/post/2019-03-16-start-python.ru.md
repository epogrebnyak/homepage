+++
title = "Начать (и успешно продолжить) программировать на Python"
date = 2019-03-15T10:57:57+03:00
draft = false

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["python", "clean code"]
categories = ["programming"]

+++

[![](https://pbs.twimg.com/media/D1oIye5WwAAK12v?format=jpg&name=medium)](https://pbs.twimg.com/media/D1oIye5WwAAK12v?format=jpg&name=medium)

<!-- TODO: встроить картинку в поста -->

C чего начать? 
--------------

Если нужен короткий ответ - [learn-python О.Твердохлеба][^1](https://github.com/trekhleb/learn-python). Лучше всего подойдет тем, кто когда-то начинал программировать (например, Basic, Pascal или VBA) и хочет восстановить и развить навыки.   

Также хорошие введения есть на сайте [QuantEcon](https://lectures.quantecon.org/py/index_learning_python.html) (эта часть
именно про Python, легко доступна для неэкономистов) 
и в [лекциях по SciPy](http://scipy-lectures.org/intro/language/python_language.html). 
Обе главы написаны очень хорошо, но все материалы на английском.

Продублирую еще раз списком:

1. [trekhleb/learn-python](https://github.com/trekhleb/learn-python) - все, что надо знать о синтаксисе языка удобно сгруппировано и проиллюстрировано примерами
2. [лекция из  QuantEcon](https://lectures.quantecon.org/py/index_learning_python.html) - начальная глава более сложного учебника. 
3. [лекция из SciPy](http://scipy-lectures.org/intro/language/python_language.html) - аналогично,
   начальная глава более полного курса

Есть нужна именно книга, то очень живым проектом выглядит [The Hitchhiker’s Guide to Python](https://docs.python-guide.org), рекомендуется, выложена в сети. Сильная сторна - сразу переходят 
к приложениям и библиотекам, но это и требует подготовки читателя.

Также раньше часто рекомендовали:

  - [Zed Shaw. Learn Python the Hard Way](https://learnpythonthehardway.org/python3/) 
  - [Mark Pilgrim. Dive into Python](https://www.diveinto.org/python3).

Learn Python the Hard Way активно обновляется, Dive into Python застыл на версии 2011 года. Учить язык по ним бы не стал, но как сборник упражнений - отличный вариант. 

[^1]: Еще более популярный репозиторий того же автора посвящен [машинному обучению](https://github.com/trekhleb/homemade-machine-learning)

План изучения
-------------

Я выписал шаги между самым первым запуском интерпретатора 
и далекими, непонятными, темными сторонами языка, которые выявляются
после длительного изучения:

### 1. Где живет программа

&nbsp;       | Установить Python
-------------|---------------------------------------------------------------------------
Идея         | `python.exe` это исполняемый файл где-то в файловой системе.<BR> Он запускается с аргументами  и опциями.
1 строка     | `python --version`
Сложности    | Переменная PATH, конфликты версий
Откуда...    | ... установаить Python? [Anaconda](https://www.anaconda.com/distribution)


&nbsp;       | REPL
-------------|---------------------------------------------------------------------------
Идея         | Программа это текстовый файл, интепретатор это цикл.
1 строка     | `print ('Hello, world!')`, `python -c "print('Hello, world!')"`
Сложности    | Принять, что IDE - это не сам Python. 

### 2. Основная часть синтаксиса и логики языка

#### 2.1. Выражения и операторы. Переменные. 

>  Интерпретатор может поработать калькулятором.

```python
>> 1 + 3 * (10 - 2)
25
```

#### 2.2.  Типы и структуры данных. 

> Числа и строки разные вещи. 

```python
>> isinstance("abc", str) & isinstance(1, int)
True
```

> Списки и словари (containers) полезны .

```python
>> colors = ['red', 'blue', 'green', 'black', 'white']
>> colors[0]
"red"
```

```python
>> {1:"I", 2:"II", 3:"III", 4:"IV", 5:"V"}[4]
"IV"
```

#### 2.3. Функции. Стандартная библиотека.

> Вычисления и операции можно сгруппировать. 

```python
import math     
def roots(a, b, c):
    """Quadratic equation roots."""
    d = b**2-4*a*c 
    try: 
        r = math.sqrt(d)
    except ValueError:
        raise ValueError("Cannot calculate real roots")        
    x1 = (-b + r) / (2 * a)
    x2 = (-b - r) / (2 * a)
    return x1, x2
```

```python
>> min (5, 7)
5
```

#### 2.4. Условное исполнение `if-then-else`. Цикл `for`.

> Исполнение программы может куда-то перескаивать.

```python
for x in [1,2,3,4]: 
    if (x % 2) == 0:
        print(x, "is even.")
    else:
        s = "odd"
        print(x, "is odd.")    
```

#### 2.5. Все остальное, о чем учат в базовых курсах.

В этом месте наметился перелом данной статьи. Оказалось,
что в пп. 2.1.-2.3 сложно описать минимальную версию 
языка программирования. За бортом остаются:

- [скрипты](https://python-3-patterns-idioms-test.readthedocs.io/en/latest/PythonForProgrammers.html#scripting-vs-programming), модули, пакеты
- дебаггер, логирование
- генераторы, итераторы, распаковка (list comprehension)
- ввод-вывод
- классы
- много что другого

Тем не менее, повторю еще раз ссылки на базовые курсы:

1. [trekhleb/learn-python](https://github.com/trekhleb/learn-python)
2. [лекции QuantEcon](https://lectures.quantecon.org/py/index_learning_python.html)
3. [лекции SciPy](http://scipy-lectures.org/intro/language/python_language.html)

В них все есть!


{{% alert note %}}

Идея: сделать таблицу `<подтема>-<разделы разных учебников>`.

{{% /alert %}}


#### 3. Дальнейшие важные пункты

Ниже чеклист продвинутых тем, которые так или иначе возникают при изучении и использовании
языка.

1. Обзор языка:
  - `import keyword; keyword.kwlist`
  - топ вопросов в [StackOverflow](https://stackoverflow.com/questions/tagged/python?sort=votes)
2. Среды разработки (IDE):
  - просто текстовый редактор (vim)
  - IDLE, VSCode, Pycharm
  - Jupyter
3. Менеджеры пакетов, структура и упаковка проектов:
  - `pip`, `requiements.txt`
  - `pipenv`
  - `conda `  
  - `poetry`
4. Аннотирование:         
  - docstrings и `PEP8` 
  - `autopep8`, `black`
  - `sphinx`
5. "Идиоматический" питон
6.  Регулярные выражения и форматы.
  - [regex101.com](https://regex101.com)
  - [pyformat](https://pyformat.info)
  - [форматы даты и времени](http://strftime.org/)
7.  Ввод-вывод (IO): 
  - файлы: `pathlib`, `csv`
  - CLI: `sys.args`, [docopt](http://docopt.org/)   
5.  Databases, SQL: 
  - [dataset](https://dataset.readthedocs.io/en/latest/) 
6.  Web:
  - `requests`
  - `flask`
7.  Тесты и TDD:
  - `assert`, 
  - `unittest`, `pytest`
  - dependency injection
  - continious inegration
8.  Объектно-ориентированное программирование (ООП):
   - "Everything is an object", `id()`
   - [cat vs dog tutorial](http://www.jesshamrick.com/2011/05/18/an-introduction-to-classes-and-inheritance-in-python/)
   - `dir()`
   - [ABCs](https://docs.python.org/3/library/abc.html).
9.  Алгоритмы:
  - [сортировки](https://github.com/TheAlgorithms/Python) 
  - O-notation
10. [Design patterns](https://github.com/faif/python-patterns)
11. Productivity: 
  - command line
  - editor shortcuts
  - git
  - markdown
12. Python моей мечты
  - опция отключить динамическую типизацию
  - оператор `.` для склеивания функций

<!--
Вне рамок описания:
  - pandas, matplotlib, сравнение [python с R](https://pandas.pydata.org/pandas-docs/stable/getting_started/comparison/comparison_with_r.html) другими языками
  - type hints
-->

Буду признателен, если расскажете, какие вехи были у вас в изучении python 
(или других областей программирования) - как кратко очаратеризовать этот этап и 
что за ним стоит, что было или остается сложным, возможно - ссылки по теме.

Педагогика какая-то в этом есть?
--------------------------------

Мне кажется, основная проблема в обучении программированию - не упрощение или переупаковка материала, 
а поддержание мотивации обучающихся. 

Хорошо известно, что идеально обучение с конкретными примерами, задачами близкими
к сфере знаний пользователя, кейсы и так далее. Проблема с этими материалами - как с курицей и яйцом: пока навыков мало освоить сложный пример нельзя, а простые примеры редко цепляют подлинный интерес и поддерживают мотивацию (тут хочется ошибаться). 

Выход из этого круга либо "сверху" (показать как работает итоговая программа и разобраться в начинке - пример fast.ai), "сбоку" (программы поменьше и разбор быстрее, Learn Python the Hard Way) или "снизу" (все-таки запастись терпением на долгую подготовку, Norwig).

Пара ссылок на тему "а как учить?":

- [Ten quick tips for teaching programming (2018)](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1006023)
- [The Best Way To Learn How To Code (3 правила)](https://www.reddit.com/r/learnprogramming/comments/5zc24o/the_best_way_to_learn_how_to_code/)
- [П.Норвиг. Научитесь программировать за 10 лет](http://norvig.com/21-days.html)
- [Требования к языку программирования и среде обучения](http://worrydream.com/LearnableProgramming/)

Учить не Python, а computer science
-----------------------------------

Почти классика:

- <http://interactivepython.org/courselib/static/thinkcspy/index.html>

Больше хардкора:

- <https://teachyourselfcs.com/>
- <https://github.com/ossu/computer-science>
- <https://github.com/donnemartin/system-design-primer>


А как же Courser'a?
-------------------

Почему бы не попробовать, но есть риски:

> "Using online tutorials is like trying to learn how to cook by stabbing at random buttons on an unlabeled microwave." [A blog in 2012](https://www.technologyreview.com/s/429438/dear-everyone-teaching-programming-youre-doing-it-wrong/)

> "Этот datacamp... Он по-моему ничему вообще не учит." От знакомого, 2019.


Куда за мотивацией?
-------------------

#### Github 

[topics/python](https://github.com/topics/python) и [trending/python](https://github.com/trending/python) покажут какие проекты активно развиваются
на Github. 

Вкратце ситуацию можно изложить так: <!--(https://stackoverflow.com/users/1758363/epo?tab=profile): -->

 - используем `requests`/`scrapy`
 - чтобы загрузить в `pandas` данные c сайтов на  `flask`/`django`
 - и поработать с ними в `tensorflow`/`keras`
 - на машинах под управлением `ansible`/`docker-compose`
 - временами изучая `awesome-python`/`system-design-primer`.

<!---
[^2]: Со звездами Github есть проблема в том, что базовые инфраструктурные библиотеки (например, проекты NumFOCUS) не получают так уж много звезд, потому что все считают из за данность.
-->

#### Опрос PyCharm

[Python developers survey 2018](https://www.jetbrains.com/research/python-developers-survey-2018) рассказывает о том, что на самом деле пилят питонисты, но опять таки - с их слов.

#### build-your-own-x

Много небольших проектов под Python в [build-your-own-x](https://github.com/danistefanovic/build-your-own-x): от интерпретатора Lisp до своей маленькой операционной системы. Основной приницп: пока что-нибудь сам не ~~сломаешь~~ сделаешь - не разберешься.


#### Проект Эйлер

На [проекте Эйлер](http://euler.jakumo.org/problems.html) много математических задач.


+++
title = "Начать (и успешно продолжить) программировать на Python"
date = 2019-03-15T10:57:57+03:00
draft = false

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["python", "clean code"]
categories = ["programming"]

+++



C чего начать? 
--------------

Если нужен короткий ответ - всегда рекомендую [learn-python О.Твердохлеба](https://github.com/trekhleb/learn-python). Лучше всего подойдет тем, кто
когда-то начинал программировать (Basic, Pascal, VBA) и хочет восстановить навык.   

Также хорошие введения есть на сайте [QuantEcon](https://lectures.quantecon.org/py/index_learning_python.html) (эта часть
именно про Python, легко доступна для неэкономистов) 
и в [лекциях по SciPy](http://scipy-lectures.org/intro/language/python_language.html). 
Обе главы написаны очень хорошо, QuantEcon более лаконичен, SciPy детальнее. Все материалы 
на английском.

Продублирую еще раз списком:

1. [trekhleb/learn-python](https://github.com/trekhleb/learn-python) - все, что надо знать о синтаксисе языка удобно сгруппировано и проиллюстрировано примерами
2. [QuantEcon](https://lectures.quantecon.org/py/index_learning_python.html) - начальная глава
   более сложного учебника
3. [лекция из SciPy](http://scipy-lectures.org/intro/language/python_language.html) - аналогично,
   начальная глава более полного курса

Для более подробного погружения я собрал [ссылки на best practices, книги и некоторые видео](https://github.com/epogrebnyak/learn/blob/master/pure_python_guide.md).


План изучения
-------------

Я выписал шаги между самым первым запуском интерпретатора 
и далекими, непонятными, темными сторонами языка, которые выявляются
после длительного изучения:

### 1. Где живет программа

&nbsp;       | Установить Python
-------------|---------------------------------------------------------------------------
Идея         | `python.exe` это исполняемый файл где-то в файловой системе<BR> Он запускается с аргументами  и опциями.
1 строка     | `python --version`
Сложности    | Переменная PATH, конфликты версий

&nbsp;       | REPL
-------------|---------------------------------------------------------------------------
Идея         | Программа это текстовый файл, интепретатор это цикл.
1 строка     | `print ('Hello, world!')`, `python -c "print('Hello, world!')"`
Сложности    | Выбор IDE. IDE - это не сам Python.

### 2. Основная часть синтаксиса и логики языка.

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

#### Функции. Стандартная библиотека.

> Вычисления можно сгруппировать. 

```python
def add(a, b):
    return a + b
```

#### Условное исполнение `if-then-else`. Цикл `for`.

> Исполнение программы может куда-то перескаивать.

```python
for x in [1,2,3,4]: 
    if (x % 2) == 0:
        print(x, "is even.")
    else:
        s = "odd"
        print(x, "is odd.")    
```

#### 3. Другие важные пункты.

1. `import keyword; keyword.kwlist`
2.  [StackOverflow](https://stackoverflow.com/questions/tagged/python?sort=votes).
         
3.  `PEP8` (autopep, black), docstrings, sphinx.

4.  IO (file): `pathlib`, `csv`.  IO (CLI): [docopt](http://docopt.org/).
   
5.  Databases, SQL: [dataset](https://dataset.readthedocs.io/en/latest/). 
6.  `requests`, `flask`.

7.  Тесты и TDD: `assert`, `unittest`, `pytest`. Dependency injection.
8.  OOP: `id()`, `dir()`, [ABCs](https://docs.python.org/3/library/abc.html).

9.  [Алгоритмы](https://github.com/TheAlgorithms/Python) и O-notation.
10. [Design patterns](https://github.com/faif/python-patterns).
11. IDEs (IDLE, VSCode, Pycharm) and Jupyter.
12. Productivity: command line, git, CI.


Буду признателен, если расскажете, какие вехи были у вас в изучении python 
(или других областей программирования) - как кратко назвать этот этап и 
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

Не Python, а computer science
-----------------------------

Почти классика:

- <http://interactivepython.org/courselib/static/thinkcspy/index.html>

Больше хардкора:

- <https://teachyourselfcs.com/>
- <https://github.com/ossu/computer-science>
- <https://github.com/donnemartin/system-design-primer>


А как же Courser'a
------------------

Почему бы не попробовать, но есть риски:

> Using online tutorials is like trying to learn how to cook by stabbing at random buttons on an unlabeled microwave. [A blog in 2012](https://www.technologyreview.com/s/429438/dear-everyone-teaching-programming-youre-doing-it-wrong/)

> Этот datacamp... Он по-моему ничему вообще не учит. (От знакомого, 2019).


Куда за мотивацией?
-------------------

Github: 

- [topics/python](https://github.com/topics/python)
- [trending/python](https://github.com/trending/python)

Python developers survey 2018:

- https://www.jetbrains.com/research/python-developers-survey-2018


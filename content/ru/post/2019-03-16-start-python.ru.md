+++
title = "Начать (и успешно продолжить) программировать на Python"
date = 2019-03-15T10:57:57+03:00
draft = false

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["python", "clean code"]
categories = ["programming", "data-but-not-rocket-science"]

+++

C чего начать программировать на Питоне? 
----------------------------------------

Если нужен короткий ответ - у меня наготове ссылка на [сheatsheet О.Твердохлеба](https://github.com/trekhleb/learn-python). Все, что надо знать о синтаксисе
языка удобно сгруппировано и проиллюстрировано примерами. 

Также хорошие введения на сайте есть [QuantEcon](https://lectures.quantecon.org/py/index_learning_python.html) 
и в [отдельной главе лекций по SciPy](http://scipy-lectures.org/intro/language/python_language.html). 
В обоих источниках главы по языку предшествуют более сложному материалу и 
написаны очень хорошо и доступно. Все ссылки на английском.

Продублирую еще раз списком:

1. https://github.com/trekhleb/learn-python
2. https://lectures.quantecon.org/py/index_learning_python.html
3. http://scipy-lectures.org/intro/language/python_language.html

Чуть больше ссылок на best practices, книги и некоторые видео собрано [тут](https://github.com/epogrebnyak/learn/blob/master/pure_python_guide.md).


План изучения
-------------

Отдельно я выписал шаги, между самым первым запуском интерпретатора 
`python -c"print('Hello, world!')"` и непонятными, темными сторонами 
языка. Возможно, из этого списка можно сделать чеклист по уровням 
квалификации и знаниям python. Приводится ниже:


1. `python --version` 
2. `print ("hello world")`
3. ...
4. PEP8
5. ...
6. что интересного есть на гитхабе ([topics/python](https://github.com/topics/python),
   [trending/python](https://github.com/trending/python))
7. [что интересного есть на StackOverflow](https://stackoverflow.com/questions/tagged/python?sort=votes)
8. ...
9. тесты (`assert`, `unittest`, `pytest`, TDD)
10. ...
11. [алгоритмы](https://github.com/TheAlgorithms/Python) и O-notation
12. ...
13. [docopt](http://docopt.org/)
14. [dataset](https://dataset.readthedocs.io/en/latest/) 
15. ...
16. документация, sphinx
17. ...
18. [design patterns](https://github.com/faif/python-patterns)
19. ...
20. [ABCs](https://docs.python.org/3/library/abc.html)
21. ...

Буду признателен, если расскажете, какие вехи были у вас в изучении python 
(или других обалстей программирования) - как кратко назвать этот этап и 
что за ним стоит, что было или остается сложным, полюбившиеся ссылки по теме.
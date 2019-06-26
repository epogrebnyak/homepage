+++
title = "Что Сiti поведал о будущем банков: 8 цитат"
date = 2019-06-27T00:58:29+03:00
draft = false

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = []
categories = []

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
[image]
  # Caption (optional)
  caption = ""

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = ""
+++

Вкратце:

- миграция core banking это боль, отсутствие миграции - это смерть;
- смерть наступит от платформ, где будут сидеть пользователи (GAFA/BAT);
- из старинных фукнций банков у них останутся только некоторые и то из-за брендов.



## Банки будут бэкэндом к GAFA (Google, Apple, Facebook, and Amazon) и BAT (Baidu, Alibaba, and Tencent)

> With PSD2, banks are increasingly at risk of
becoming mere tubes in the banking process where the front-end products are with
GAFA and the back-end processes are with traditional banks. 

EP: идея красивая, но, видимо, разная история будет с транзакционным бизнесом (зачем там банки) и кредитованием (баланс, риски). 

## К плохому бэкэнду хороший фронт не приставишь

> Focusing only on the front-end is the biggest challenge banks face. Not innovating back-end processes is more like putting lipstick on a pig.

EP: уже стало народной мудростью? 


## Замена core banking - 5 лет. А мы не знаем, что будет через 5 лет.

> If I need to do something that touches my core banking system, and my core
banking system is limited because it was designed to solve different kinds of
problems, what do I do traditionally? I go to the person who provided my core
banking system and ask them to do better. But it takes 5 years to replace the older huge version with a new version which is equally huge. 

EP: миграции бывают и быстрее, год-два, но цифра 5 лет хорошо передает масштаб неповоротливости core banking. 

## При этом мигрировать можно и десятилетие и платить за две ИТ системы

> ... phased roll-out has its disadvantages too. It can drag on for years and you end up paying both providers and maintaining both systems. Just take a look at the example of Suncorp in Australia, where the bank has been paying both CSC for its [legacy Hogan system and Oracle for its Oracle Banking Platform system for nearly a decade now](https://www.bankingtech.com/2019/02/oracle-feels-the-chill-from-suncorp-ceo-over-core-banking-freeze/).


## Дожить до пенсии и ничего не далть

> A very big bank is unlikely to go for a full end-to-end overhaul in one go
because it is just too risky and difficult. Often, CIOs and CTOs try to avoid this and
wait it out until their retirement and then let somebody else take over and manage
the project risk.

EP: хорошо для менеджмента, плохо для инвесторов. 

## Игроки на рынке core banking 

- If a big bank is embarking on a major core system transformation, the
pool of vendors to choose from is limited. There is Oracle Flexcube, TCS BaNCS,
Finacle Infosys, Finastra (which probably everybody still remembers as Misys),
SAP, and Temenos. These are the main players on the international arena that you will be looking at. 

- In the U.S. the picture is different. If you are a domestic bank you have four tech
heavyweights: Jack Henry, FIS, Fiserv, and now Finastra as well (what used to be
D+H, and Open Solutions before that). 

- ... especially for Temenos, it is the firm’s bread and butter. Temenos sales process is well-organized and sleek.

- The new entrants such as 10x Technologies, Thought Machine, Mambu, Leveris
etc. are quite small themselves. 


## Микросервисы позволяют быстрее пилить новые продукты

> Our technology is highly flexible. We use micro services. These are
small pieces of software code performing unique functions. For example: charging a
fee, changing an address, charging an interest rate etc. Because we can assemble
those micro services highly flexibly, it significantly reduces the time it takes to build
new products on the new platform.

EP: смена адреса - это не микросервис, по крайней мере не в архитектурном смысле (вызов API 
одного из сервисов, я так полагаю), но насчет гибкости разработки - именно так.

## У банков только шесть функций.

> Banks only do six things. They make and receive payments. They borrow and lend. They provide risk management services, often in the form of insurance. And they provide information
to their customers on all of those things.

EP: еще трансформируют maturity, мне кажется. Иногда - сидят в капитале чего-то (step-in).
Сама идея разобрать банк на подфункции, эти или немного другие, очень близка.  


Чтение продолжится....


Источник: [Bank X. The New New Banks](https://www.citivelocity.com/citigps/bank-x-new-new-banks/).

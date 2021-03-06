---
layout: post
title: Методы Оптимизации
---



* Капалин Владимир Иванович
* телефон 8 967 155 77 60

## Постановка задачи и основные положения

Как и в теории принятия решений в методах оптимизации решается задача поиска экстремума некоторой целевой функции, различие между этими двумя дисциплинами следующее:
Теория принятия решений или иследование операций появилось в середине 19 века и преднозначено для решения военных и экномических задач. Требуется обычно найти оптимальный план работы предприятия, оптимальный план перевозок груза, оптимальное расрпределение персонала на выполнение определенных работ и тд.
Методы оптимизации имеют гораздо более длинную историю. 
Классический метод оптимизации: 
1. Дихотомия, была разработана древними греками
2. Числа фибаначи ( 12 век)
3. Ньютон (17 век)
4. Бальцано и Сельвестро (19 век)

Бум в области методов оптимизации относится к 50 годам 20 века. Основные разработки по новым методам, были выполненны в соединенных штатах.

Методы оптимизации применяются в основном для решения технических задач. 
Например:
	Создание оптимального проекта летательного аппарата, двигателя, Оптимальное упавление космическим караблем, морским судном, и тд.

В методах теории принятия решений, решения часто выражаются часто выражаются целочисленно, или даже в булевых переменных, в методах оптимизации решение всегда ищется в евклидовых пространствах R^n , если n=1 то это задача одномерного поиска, одномерной оптимизации, а если а >1  а^n многомерной. Это две разных группы методов.

Постановка задачи:
	Постановка задачи в методах оптимизации соержит, некоторую целевую функцию F(x) x= {x1}






============================================================
1.
===========================================================

для которой значение целевой функции минимально или максимально


обычно рассматривается задача поиска минимума, так как для поиска максимума можно записать:

=====================
2.
=====================


=================
3.
============

Ели X задается ограничениями, типа равенств или неравенств, то говорят о задаче поиска условного экстремума. Еще 1 отличие методов оптимизации от методов иследования операций, при иследовании операций ограничения линенйные, а в задачах оптимизации ограницении почти всегда нелинейные.



### Определение:
Точка

точка локального минимума ,Ю если для всех точек из (Эпислон)
+++++
4.
+++++++++++++++++++
	Обычно ищется точка глобального минимума, а точки локального минимума, дают паразитирующие решения от которых нужно избавляться.

### Определение:
Поверхности уровня, это точки в которых функция принимает постоянных значения, если т =2 то говорят о линии уровня R^2
====
5
====
ПРимер:
Перем простейшую целевую функцию
====
6
====

## Грвдиент

Обозначение (переверн. треугольн , Напла) F(x)
Градиент это вектор столбец частных производных целевой функции
====
7
===
Градиент направлен в сторону наибольшую возростания к целевой функции в данной точке

-f(x) антиградиент направлен в сторону убывания функции

Таким образом , если мы будем двигаться по градиенту, то мы будем приближаться к максимуму функции,а по антиградиенту, к минимуму функции.

## Матрица Гессе

Это матрица частных производных второго порядка
==========
8
===========

Ратейлера для прирощения целевой функции, может быть записано так

==
9
	==
В классическом методе ньютона для 1 пременной необходимое условие существавания экстремума (максимума или минимума), это равенство нулю первой производной , а достаточное условие определяется по второй производной, если вторая произодная положительна то это минимум, отрицательная -  максимум. Здесь такая же ситуация, необходимые условия это равенства нулю градиента, а достаточное условие проверяется по матрице Гесса.

Образаем внимание что первое слогаемео это линеная функция.

#### Опреденение
Квадратичная форма и соответствующая матрица Гессе называется: 
1. Тождейтсвоенно равный нулю, если для всех икс выволенно очевидное условие
===
10
===
2. Неопределенной , если существуют такие прирощения дельта икс 1 и дельта икс 2, что выполняются условия
===
11
===
3. Положительно полуопределенной, если для всех икс === отличный от нуля, что в этом векторе квадратичные формы возрвращаются в ноль
===
12
===
4. положительно определенной, если для луюбого ненулегвого прирощения дельта иксвыполненно условие
===
13
===
5. аналогично определяется отрицательная определенность



## Примеры
1. f(x) = x1^2+x2^2
===
14
===
17.
===
Значит матрица гесса положительно поределена

2. f(x) = x1^2 + x2^4 
	===
15
===
18
===
если дельта x 1 равно нулю, то
Это случай, положительно полуопределенной формы Гессе

3. f(x) = x1^2 - x2^2
===
16
===
19
===
записываем квадратичную форму, если дельта x равна нулю, то для любых дельта x 2 форма получается отрицательная, а если наоборот форма получается положительная, отсюда вывод, это случай неопределенной матрицы Гессе

4. Pyfxb

Задание: Электрнный вариант лекций.


## Необходимые и достаточные условия без условного экстремума

Если в теории принятия решений, всегда с ограничениями, то в методах оптимизации, сновными являются методы безусловного экстремума

### постановка задачи

1. Дана дважды деференцируемая функция f от x определенная R^n. Пусть X* является точкой ее локального минимума и максимума, тогда градиент в этой точке равен нулю или что тоже самое равенство нулю частных производных. точки кторые удовлетворяют условию 1 называются стационраными
===
20
===
2. пусть X* из R^n точка эестремума, тогда , если икс со звездочкой минимум , то в этой точке матрица гессе положительно полуопределена, если максимум, то матрица Гессе отрицательна полуопределена, эти два утвреждения , дают необходимые условия минимума, тоесть если они не выполняются, то экстремума нет, а если выполняются требуется проверка по матрице гесса
3. если в точке X* выполняется условие градиент обращается в ноль а матрица Гессы положительно определена, то чтока X* является точкой локального минимума, если же матрица гесса отрицательно оптеределена, то точкой локального максимума. Таким образом , здесь нужно проверять положительно или отрецательную определенность матрицы гесса, однако прямая проверка, прямой расчет,

как было сделано на примерах затруднительна, для такой проверки используется критерий сельвестра не требующий прямых расчетов с матрицей Гесса

### критаерй Сельвестра

Рассмотрим определитель матрицы гесса построенной на стационарной точкой X* там где градиент равен 0

21

Гессиано

1. угловые миноры
22

2. определитель энногопорядка который получается вычеркиванием каких либо n-m строк n- стобцов с одинаковыми индексами, называется главными минорами.

#### КРитерий сильвестра( в обобщенной форме)
Сильвестра математик 18 века, выпускник кембриджа

Для того чтобы матрица гессе была положительно определена и точка X* являлась точкой локального минимума необходимо и достаточно чтобы знаки угловых миноров были положительны.
Для того чтобы матрица гесса была отрицательно определенной и точка X* юыла бы точкой локального максимума необходимо и достаточно, чтобы знаки угловых миноров чередовались так 
==
23
==
Для того чтобы матрица гесса была отрицательно полуопределенной, и точка X* могла бы быть точкой локального максимума, необходимо и достаточно, чтобы главные миноры четного прядка, были не отрецательны , а главные миноры нечеткого порядка не положительны.
Для того чтобы матрица гесса была положительно полуопределенной и точка X* маогла бы быть точкой локального минимума, необходимо и достаточно, чтобы все главные миноры, были не отрицательны.

#### Итог
Таким образом критерий Сильвестра позволяет проверять наличие точки экстремума по знакам миноров матрицы Гесса.
	ПРимичание: Вместо расчета определителей можно расчитывать корни можно проверять знаки собственных значений лямдай такого уровнения 
	===
	24
	===

#### расчет

1. свчитаем градиент, производная по ик 1 
===
25
===
Считаем угловые миноры
Условия выполняются, нулевая точка является локальными минимумом, эта  точка является глобальным минимумом. так как целевая функция квадратичная, проверяем по собственным числам
===
26
===
вывод тот же достаточное условия минимума выполненны

2. есть целевая функция эф от икс ровно икс 1 в квадарате минус икс 2 в квадарате
считаем градиент чтобы найти стационраную точка, стационранрная чтока ноль ноль, матрица гесса, 

27

достаточное условия не выполненны, но иззза выполнения достаточных условий не вытикает отсутствие экстремума, нужно проверять еще и необходимые экстремумы, определитель у нас вот такой

28

необходимые условия тоже не выполняются, значит минимума нет, нет и максимума. проверим по собственным числам

29

необходимые условия не выполненны , эта точка не является точкой экстремума.

3. 30

 достаточные условия не выполнены но это не ожначает отсуствие минимума, проверим необходимые условия.

31

так как все они е отрицательны, то это означает, что минимум может существовать, для этого нуэныдополнительные условия. В точке ноль значение целевой функции равно нулю, но при любых икс больших чем икс со звездочкой значение целевой функции будет больше... бла бла... тоетсь это означает, что здесь имеется минимум не только локальный но и глобальный.

#### Итог
Для того чтобы проверить наличие екстремума нужно:
1. найти стационарные точки в которых градиент обращается в ноль
2. расчитать матрицу гесса, если она положительно определена, то минимум существует,  если положительн полуопределена, нужна проверка дополнительных условий.

#### пример более сложный

32
расчет
шаг 1 . Растчет стационарныйх точке
шаг 2 .  есть две стационраные точки, нужно проверить достаточные условия  в этих точках, для этого считаем матрицу гесса
шаг 3 . проверка второй стационарной точки, достаточные условия не выполненны, это не означает что минимума нет , нужно проверить главные миноры. должна быть нетотрицальетная главных минорорв, она не выполняется, поэтому окончательный вывод в точке 0.0 минимума нет.

110 больше чем 46

#### Заключение
Этот подход позволяет исчерпиваще решить задачу глобальной минимизации, номожет оказаться неудобным для практики, поскольку требует расчета градиента и матрицы гесса, которые оказываются неизвестными, если рассматриается конкретные практические задачи, поэтому данный классический метод, не часто используется на практике.


















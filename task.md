ПРОЕКТ № 5
Служба такси.

Все операции должны считаться локально.

Данные - $[Служба такси](https://disk.yandex.ru/d/DKeoopbGH1Ttuw) 

Есть таблица, состоящая из поездок такси в Нью-Йорке.
![$screenshot]([https://github.com/javascriptrocker2104/work_with_hadoop/blob/main/hadoop.png](https://github.com/javascriptrocker2104/1t_final_project/blob/main/images/table.png])
![$screenshot]([https://github.com/javascriptrocker2104/work_with_hadoop/blob/main/hadoop.png](https://github.com/javascriptrocker2104/1t_final_project/blob/main/images/tab.png])

Необходимо, используя таблицу поездок для каждого дня, рассчитать процент поездок по количеству человек в машине
(без пассажиров, 1, 2, 3, 4 и более пассажиров). По итогу должна получиться таблица (parquet) с колонками date, percentage_zero,
percentage_1p, percentage_2p, percentage_3p, percentage_4p_plus. Технологический стек — sql, scala (что-то одно). 
Также добавить столбцы к предыдущим результатам с самой дорогой и самой дешевой поездкой для каждой группы.

Дополнительно: также провести аналитику и построить график на тему «Как пройденное расстояние
и количество пассажиров влияет на чаевые» в любом удобном инструменте.

ПРОЕКТ №5 СЛУЖБА ТАКСИ

Описание задания - [Такси Нью-Йорка](https://github.com/javascriptrocker2104/1t_final_project/blob/main/task.md)

Файл с расширением .csv, который необхожимо обработать - [служба такси](https://github.com/javascriptrocker2104/1t_final_project/blob/main/task.md)

ПЛАН РЕАЛИЗАЦИИ ПРОЕКТА

Технологический стек - Apache Spark 3.4.1, Python 3.11.5, SQL. Скрипты написаны в Jupyter Notebook с использованием PySpark.

Одним из наиболее значимых достоинств Apache Spark является его скорость, он позволяет обрабатывать данные непосредственно в оперативной памяти. За счет этого многие задачи по обработке больших данных выполняются быстрее. Apache Spark предоставляет разработчику довольно обширный API, позволяя работать с разными языками программирования. Еще один плюс Spark - ленивые вычисления, которые позволяют снизить общий объем вычислений и повысить производительность программы за счет снижений требований к памяти.

Python - это высокоуровневый язык программирования с простым минималистическим синтаксисом. Имеет большую стандартную библиотеку и много дополнительных библиотек.

SQL хорош тем, что может анализировать и обрабатывать данные любого размера, независимо от того, имеете ли вы дело с небольшим набором данных или большим стеком.

НАСТРОЙКА И ЗАПУСК

1. Необходимо перейти на официальный сайт [Anaconda](https://www.anaconda.com/download) и выбрать подходящую для Вашего устройства версию приложения в конце страницы.
2. Далее откройте Jupyter любым способом:
   1) Запустите Anaconda Navigator из списка программ и найдите Jupyter Notebook.
   2) На Mac напишите в терминале команду jupyter notebook.
   3) На Windows откройте Anaconda Command Prompt (CMD.exe Prompt) и выполните команду jupyter notebook.

3. Для создания нового проекта необходимо открыть в правом верхнем углу New → Python 3 (ipykernel). Также возможно создание новой папки посредством команды «Folder» в том же выпадающем списке.


ОРГАНИЗАЦИЯ РЕПОЗИТОРИЯ

![screenshot](https://github.com/javascriptrocker2104/1t_final_project/blob/main/images/structure.drawio.png)

Сырые данные в raw layer были загружены без обработки, а в core layer были загружены данные, необходимые для решения задания, которые были очищены (были удалены строки со значениями NULL в столбце passenger_count, отрицательные значения, нелогичные данные по расстоянию). В итоге получилась следующая структура хранилища данных:

![screenshot](https://github.com/javascriptrocker2104/1t_final_project/blob/main/images/taxi.drawio.png)

Скрипт, который формирует витрину данных - [Mart](https://github.com/javascriptrocker2104/1t_final_project/tree/main/src/percentage_min_max)

Скрипт, который рисует графики - [Plots](https://github.com/javascriptrocker2104/1t_final_project/tree/main/src/plot)

ВЫВОД

Файл, где для каждого дня, рассчитан процент поездок по количеству человек в машине (без пассажиров, 1, 2, 3, 4 и более пассажиров), а также самая дорогая и самая дешевая поездка для каждой группы - [result](https://github.com/javascriptrocker2104/1t_final_project/blob/main/result_data/taxi_result.parquet)

График зависимости чаевых от дистанции:

![screenshot](https://github.com/javascriptrocker2104/1t_final_project/blob/main/images/tip-distance.png)

Как видно из графика, чем больше пройденное расстояния, тем меньше чаевых оставляли пассажиры.

График зависимости чаевых от количества пассажиров:

![screenshot](https://github.com/javascriptrocker2104/1t_final_project/blob/main/images/tip-passengers.png)

Как видно из графика, тем меньше пассажиров, тем больше чаевых.

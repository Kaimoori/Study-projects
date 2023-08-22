Портфолио: аналитик данных

Обо мне:

Привет! Меня зовут Надежда, я начинающий аналитик данных. Я прохожу обучение на аналитика данных в школе Skypro. В этом репозитории вы можете найти некоторые из моих проектов, выполненных во время обучения и практики.

Навыки и технологии
Инструменты анализа данных: SQL, Excel

Системы управления базами данных: PostgreSQL

Проект 1: Калькулятор юнит-экономики онлайн-кинотеатра

Что нужно было сделать:

Необходимо было посчитать юнит-экономику продукта и предложить сценарий по настройке параметров для выхода на 25-процентную маржинальность и собрать хорошую наглядную визуализацию, где будет показано, кто, где и в каком объеме смотрит фильмы на нашей платформе.
 
Задача №1 посчитать юнит-экономику продукта и предложить сценарий по настройке параметров для выхода на 25-процентную маржинальность

Задача №2. Собрать хорошую наглядную визуализацию

Краткое описание решения (автореферат)

- На основе имеющихся данных строим сводные таблицы: Количество просмотров каждый месяц, число уникальных пользователей, количество новых подписчиков, количество первых просмотров.
- Строим калькулятор юнит-экономики AS IS, и понимаем, что при текущих данных маржинальность нашего проекта составляет -94%, т.е. мы работаем с большим убытком.
- Считаем сценарий, с какими параметрами можно выйти на маржинальность 25%
- Строим графики, наглядно показывающие сложившуюся ситуацию, делаем выводы. 

Ссылка на проект https://docs.google.com/spreadsheets/d/1gIwQLKYnt2Yusm_lBw7oIDJ2FYApBofJf6RVORwcon0/edit?hl=ru&pli=1#gid=731120703

Выводы (итоги):

Итог №1. В текущей ситуации мы наблюдаем 2 проблемы:						
1) Люди не приходят на платформу (падает количество подписок).				
2) Люди уходят после первого месяца подписки.

Итог №2. Предполагаем, что причина первой проблемы может быть в 	резком снижении расходов на маркетинг, а причина второй проблемы - большое количество непопулярных фильмов, людей не устраивает репертуар и они уходят.

Итог №3. Выносим предложения, как можно выйти на маржинальность 25% и улучшить ситуацию. Также предоставляем дополнительные графики для дальнейшего анализа маркетологами.	 



Проект 2: Моделирование изменения балансов студентов

Что нужно было сделать:

Задача №1. Из БД с помощью SQL создать таблицу, где будут балансы каждого студента за каждый день.

Задача №2. Проанализировать, сколько всего уроков было на балансе всех учеников за каждый календарный день, и как это количество менялось под влиянием транзакций (оплат, начислений, корректирующих списаний) и уроков (списаний с баланса по мере прохождения уроков).

Краткое описание решения (автореферат)

- Баланс уроков собираем с первой транзакции. Создаем таблицу с первыми транзакциями для каждого студента.
- Создаем таблицу с датами уроков. Соединяем обе таблицы, получаем для каждого студента таблицу с датами жизни после первой транзакции.
- Создаем таблицу, где по каждому студенту будет информация о количестве списанных или начисленных уроков в разбивке по датам, а также кумулятивная сумма количества уроков на балансе за каждый день.
- Создаем таблицу, где по каждому студенту будет информация о количестве пройденных уроков в разбивке по датам, а также кумулятивная сумма количества пройденных уроков за каждый день.
- Объединяем таблицы с пройденными уроками и начисленными и списанными уроками. Получаем таблицу с изменением баланса уроков по каждому студенту за каждый день.
- Сгруппируем данные по датам, получим информацию об изменении балансов по всем студентам за каждый день.
- Создаем итоговую визуализацию результата.

Ссылка на проект https://docs.google.com/spreadsheets/d/1aAlsCVbXWKGzOnLkj_3oXcnOrmhUv8QXGf-z6JkLB4A/edit#gid=1993744225

Выводы (итоги):

Итог №1. Есть определенные неточности в данных. У некоторых пользователей проходят уроки в количестве большем, чем оплачено, т.е. они занимаются как бы в кредит. Не должно быть отрицательных значений между количеством оплаченных уроков и количеством проведенных. Поэтому, либо неверно отражена информация об оплате уроков (не отражены оплаты, не отражены подаренные уроки), либо неверно указан статус урока "success". 

Итог №2. Линия, показывающая разницу между оплаченными уроками и проведенными, имеет слабый рост, т.е. количество оплаченных уроков превышает количество проведенных уроков, и эта тенденция увеличивается.



Проект 3: Создание параметризованного дашборда в Google Sheets

Задача №1. Создать сводный параметризованный лист, в который импортированы 4 листа с данными, при этом импортируются только те строки, у которых значение payment_type совпадает с выбранным значением выпадающего списка.

Задача №2. Построить график, на котором изображена динамика количества транзакций по торговым точкам, и график, на котором изображена динамика длительности проведения транзакций по торговым точкам.

Краткое описание решения (автореферат)

- Создаем лист, хранящий уникальные значения столбца payment_type.
- С помощью функции IMPORTRANGE импортируем в документ “Свод” 4 листа с данными.
- С помощью функции QUERY параметризуем импорт листов с данными, импортируются только те строки, у которых значение payment_type совпадает с выбранным значением выпадающего списка.
- Добавляем в выпадающий список опцию “Все”. В случае выбора этой опции импортируются все строки с листов с данными.
- Рассчитываем “длительность проведения транзакции” в секундах.
- На листе «Дашборд» создаем выпадающий список с различными значениями payment_type и перепривязываем импорт строк к этому значению.
- Строим график, на котором изображена динамика количества транзакций по торговым точкам, и графика, на котором изображена динамика длительности проведения транзакций по торговым точкам. 

Ссылка на проект https://docs.google.com/spreadsheets/d/1iyKk6Sbd_BKlqeOEj0TrSm_gd5poBM3mzL-WQI6JtgY/edit?usp=sharing

Выводы (итоги):

Итог №1. Создан сводный параметризованный лист, на котором отражаются данные по транзакциям в двух торговых точках за 2 недели, при этом есть возможность отображения данных в соответствии с выбранным типом оплаты.

Итог №2. Построены графики динамики количества транзакций по торговым точкам и динамики длительности проведения транзакций по торговым точкам. На этой вкладке есть возможность выбрать различные значения payment_type и разные торговые точки и отследить изменения на графиках.

Контактная информация
Email: mail2justme@yandex.ru

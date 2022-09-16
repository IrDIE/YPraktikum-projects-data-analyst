# Исследование объявлений о продаже квартир
# Описание проекта

В вашем распоряжении данные сервиса Яндекc Недвижимость — архив объявлений о продаже квартир в Санкт-Петербурге и соседних населённых пунктах за несколько лет. Нужно **научиться определять рыночную стоимость объектов недвижимости.**

Наша задача — установить параметры. Это позволит построить автоматизированную систему: она отследит аномалии и мошенническую деятельность. 


**ПЛАН РАБОТЫ**

1. Открыть данные и предобработать их (пропуски, аномалии, выбросы и тд)

2. Посчитаем такие характеристики как: 

* цена квадратного метра

* день недели, месяц и год публикации объявления

* этаж квартиры; варианты — первый, последний, другой

* соотношение жилой и общей площади, а также отношение площади кухни к общей

3. Посмтрим распределения площади, цены, числа комнат и тд

4. Оценим время продажи квартиры

5.  Изучим зависит ли цена от площади, числа комнат, удалённости от центра, этажа и других переменных

6. Выберем 10 населённых пунктов с наибольшим числом объявлений. Выделим  населённые пункты с самой высокой и низкой стоимостью жилья.

7. Определим какая область входит в центр

8. Рассмотрим более подробно квартиры в центре и их особенности

9. Вывод


<details>
<summary>Выводы(спойлеры , более подробно см файл .ipynb)</summary>
<br>

### По общей базе:
Самые популярные:

* общей площадью до 100 кв м
* цена до 30 млн
* 1-3 комнатные
* потолки от 2,5 до 3 метров
* чаще всего удаётся продать квартиру за 200 дней
* цена не зависит от дня размещения
* видим что квартиры 2014 - 2015 годов стоят значительно дороже


### По Санкт - Петербургу ( центр ):
* основная площадь : 50-150 кв.м
* цены в основном не выше 25 - 30 млн
* большинство - нормальные потолки, но и более 3х метров немало
* на первый этаж самая низкая цена
* от 1 до 5 комнат

</details>
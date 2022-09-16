# Описание проекта:

Вы — маркетинговый аналитик развлекательного приложения Procrastinate Pro+. Несмотря на огромные вложения в рекламу, последние несколько месяцев компания терпит убытки. Ваша задача — разобраться в причинах и помочь компании выйти в плюс.

Есть данные о пользователях, привлечённых с 1 мая по 27 октября 2019 года:

* лог сервера с данными об их посещениях,
* выгрузка их покупок за этот период,
* рекламные расходы.


Вам предстоит изучить:

* откуда приходят пользователи и какими устройствами они пользуются,
* сколько стоит привлечение пользователей из различных рекламных каналов;
* сколько денег приносит каждый клиент,
* когда расходы на привлечение клиента окупаются,
* какие факторы мешают привлечению клиентов.


# План работы:

* Загрузим данные и подготовим их к анализу
 
* Создадим функции для расчета и анализа LTV, ROI, удержания и конверсии

* Проведм исследовательский анализ данных

* Постройте профили пользователей. Определите минимальную и максимальную дату привлечения пользователей.

* Выясним:
    - Из каких стран приходят посетители? Какие страны дают больше всего платящих пользователей?
    - Какими устройствами они пользуются? С каких устройств чаще всего заходят платящие пользователи?
    - По каким рекламным каналам шло привлечение пользователей? Какие каналы приносят больше всего платящих пользователей?.

* Маркетинг. Выясним:

    - Сколько денег потратили? Всего / на каждый источник / по времени
    - Сколько в среднем стоило привлечение одного покупателя из каждого источника?

* Оценим окупаемость рекламы для привлечения пользователей

* С помощью LTV и ROI:
    - Проанализируем общую окупаемость рекламы;
    - Проанализируем окупаемость рекламы с разбивкой по устройствам;
    - Проанализируем окупаемость рекламы с разбивкой по странам;
    - Проанализируем окупаемость рекламы с разбивкой по рекламным каналам.

* Ответим на вопросы:
    - Окупается ли реклама, направленная на привлечение пользователей в целом? 
    - Какие устройства, страны и рекламные каналы могут оказывать негативное влияние на окупаемость рекламы?
    - Чем могут быть вызваны проблемы окупаемости? Изучим конверсию и удержание с разбивкой по устройствам, странам, рекламным каналам.

Опишем возможные причины обнаруженных проблем.Считаем, что мы смотрим данные 1-го ноября 2019 года и что в нашей организации принято считать, что окупаемость должна наступать не позднее, чем через 2 недели после привлечения пользователей.


*  Напишем выводы



<details>
<summary>Выводы(спойлеры , более подробно см файл .ipynb)</summary>
<br>

### Чем могут быть вызваны проблемы окупаемости?

Можем проследить такую цепочку:

* Наши основные платящие это US

* В US основные устройства это Mac и iPhone, основные каналы привлечения - FaceBoom, TipTop
* в июне стало резко дороже привлекать по каналу TipTop (при этом сильных изменений в LTV нет)
* соответственно графики окупаемости рекламы по региону и по устройствам выросли
* особенности пользователей US : они быстро переходят в платящих, но их трудно удержать

**Что можно сделать?**

* рассмотреть каналы lambdaMediaAds, RocketSuperAds (имеет Retention примерно как и через TipTop , конверсия выше большинства других. Но проблема в том что этот канал не популярен в US , поэтому...)
* перераспределить вложения в рекламу между TipTop/FaceBoom и lambdaMediaAds, RocketSuperAds
* или уменьшить долю пользователей с US (больше вкладываться в каналы, популярные в других регионах)

</details>
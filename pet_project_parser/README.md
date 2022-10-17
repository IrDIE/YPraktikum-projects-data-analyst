# parser_pet_project

## Описание проекта

Хотим проанализировать рынок вакансий в IT индустрии за 2022г, с помощью парсера тг-каналов соберём данные и проверим гипотезы.

- **Техническое задание**
    - Написать парсер вакансий с телеграмм-каналов;
    - Провести исследовательский анализ данных;
    - Собрать все результаты в функциональный, понятный заказчику дашборд;
    
    
    
<details>
  <summary>Цели и гипотезы</summary>
 
    
    Гипотезы:
    
    - Для позиций Junior / Intern работодатель отдаёт предпочтение студенту или недавнему выпускнику (сравнить количество вакансий)
    - Работодатели больше всего ищут на Jinior - позицию, чем на Middle
    - Больше вакансий с удалённой работой / гибридом
    
    Цели:
    
    1. Составить портрет специалистов DE, DVLP, DS и DA с точки зрения grade.
        - Определить, какой уровень наиболее востребован на каждой позиции
    2. Провести анализ  зарплат специалистов DE, DVLP, DS и DA в разрезе по grade
    3. Исследовать динамику числа вакансий в разрезах по направлению и грейду
    4. Посмотреть долю вакансий на гибриде или удалёнке для разных grade
    5. Определить на какие позиции охотнее берут студентов
    6. Найти топ-10 городов по числу вакансий
     
- Гипотезы
    
    этот раздел будет корректироваться в зависимости от того что нам удалось спарсить, и что удалось достать из предобработки
    
    - Для позиций Junior / Intern работодатель отдаёт предпочтение студенту или недавнему выпускнику (сравнить количество вакансий)
    - Работодатели больше всего ищут на Jinior - позицию, чем на Middle
    - больше вакансий с удалённой работой / гибридом
</details>


<details>
  <summary>Декомпозиция задач</summary>
    

    - Настроить парсер
        1. Подключить новый номер с которого будем регистрировать приложение
        2. создать приложение для Telegram API
        3. создать файл с api_id и api_hash
        4. написать / запустить скрипт авторизации в Telegram
        5. отобрать Telegram - каналы для парсинга
        6. написать / запустить скрипт парсера (+ определить данные которые будем парсить)
        7. получить сырые данные 
    - Предобработать данные и подготовить их к анализу
        1. пропуски (+посмотреть долю пропусков по каждому каналу)
        2. привести к нижнему регистру 
        3. достать id и название чата
        4. дубликаты
        5. обработать дату 
            
            теперь нам нужно спарсить данные со ссылок, которые мы спарсили с Telegram- каналов
            
            далее используем регулярные выражения  и всё что можем (включая Божью помощь)
            
        6. создать колонку с условиями работы (онлайн / гибрид / удалённо / только офис и тд)
        7. Создать колонку с ЗП
        8. разделить вакансии на DA (в него входят продуктовые аналитики, системные, аналитики данных и тп) / DE / DS / остальные
        9. разделить вакансии на грейды (Intern / Junior / Middle / Senior)
        10. указать ищет ли работодатель студентов или тех, кто недавно закончил ВУЗ
        11. Нашли вакансии с почасовой оплатой (это обычно преподаватели курсов)
        12. переименовать колонки при необходимости
        
    - EDA ( Исследовательский анализ данных)
        1. спарсить  данные для каждой цели и проверить их ( цели )
        2. проверить гипотезы
        3. посмотреть динамику показателей во времени
    - Использовать PowerBI для визуализации результатов
        
        
    - Удаление левого номера
        1. отключить номер с сессии в телеграме
        2. отвязать аккаунт
        3. отказаться от номера

</details>
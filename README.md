#### Задание. ####
<p>
1. Создать веб приложение, которое предоставляет доступ к ленте новостей. 
Записи формируются при анализи rss нескольких публичных ресурсов (достаточно 2). 
Пользователь должен иметь возможность просмотреть список новостей, отфильтровать их по источнику и дате.
2. К каждой записи новости прикрутить счетчик лайков. 
При достижении значения 10 — голосование прекращается, новость помечается как самая популярная. 
Предусмотреть, что обновление счетчика может происходить одновременно (например запущено несколько пулов php-fpm).

Серверную часть желательно реализовать с использованием Yii2.

3. Необязательное.
Реализовать возможность сброса счетчика для конкретной новости при некотором событии, причем событие может генерить любое другое приложение (http://www.rabbitmq.com/tutorials/tutorial-one-php.html)
</p>

----

1, 2 - задание реализовано, 
3-е изучаю, на данном этапе не удалось реализовать.

задание реализовано с использованием Zend Framework v1 (Yii2 изучаю, не удалось за вечер расковырять его чтоб можно было 
                                                        писань на нем используя весь функционал этого фреймворка)
                                                        

------
Описание:
лайки храним  в БД MySQL,
сортировка реализована на клиентской стороне с использование библиотеки http://isotope.metafizzy.co/

конфиг БД - /application/configs/application.ini 
бэкап  БД - /database/rss.sql

точка входа в приложение  example.ru/public/index.php

реализованные файлы:
  /library/Class/Class_Rss.php
  /application/models/CRUD.php
  /library/Class/Logger.php - (не закончен, для обработки исключений)
  
главный action  - /application/controllers/IndexController.php
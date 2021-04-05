Тестовое задание на позицию php бэкенд разработчика
=============================

Реализовать **API для подписки на новости**.

API должно выполнять следующие задачи:

  1. Подписка пользователя по email на нужную рубрику
  2. Удаление подписки на конкретную рубрику
  3. Удаление подписки на все рубрики
  4. Отображение подписок пользователя и отображение всех пользователей переданной рубрики 
    * Эти данные должны быть доступны только после авторизации. Например через открытый\закрытый ключ с последующим использование токена. (Ключи выдаются доверенному приложению которое и будет отображать данные из API (реализация приложения не требуется))
    * Так как этих данных может быть много, то этим методы должны принимать дополнительные параметры limit и offset ограничивающие выдачу.
  5. Подержка версионности API с наследованием функционала. Версия передается в заголовке request.
    * В v2 нужно добавить:
      1. К методу подписки обязательный параметр "Имя пользователя".
      2. Новый метод который генерирует ключ для возможности отписки. Этот ключ должен быть уникальным для каждой рубрики у каждого пользователя. Метод для удалении подписки должен принимать этот ключ вторым параметром.
  6. Уметь отдавать ответы в разных форматах (json\xml) на выбор.
  
##Требования
  1. Фреймворк Laravel (на самом деле любой современный фреймворк подойдет, но Laravel предпочтительнее так как мы разрабатываем с его использованием)
  2. Миграции
  3. Валидация параметров.

Будет плюсом:
  1. реализация RESTful API
  2. API покрыто тестами
  
##PS
  Коммиты стараться делать логически осмысленными, разбивая функционал на части. Сообщения коммита должны описывать что было сделано.

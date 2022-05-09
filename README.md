# UrlsApp
 URL links shortener diplom app

# Недоделки:
- Запустить на сервере u9.by
- не работает DatetimePicker в режиме Customer - JavaScript
- ссылки не анализируются на запуск после Даты до: и до Даты после:
# Планы на будущее
- добавить виджет обратного отсчета до появления ссылки
- добавить аналитический модуль по подробной информации
- прикрутить регистрацию по платной СМС к странице Customer

для запуска проекта на компьютере нужно 

```shell
docker compose up
docker compose -f docker-compose-deploy.yml up --build
```
Чтобы отдавать команды нашей среде мы делае следующее:

```shell
docker compose exec app python manage.py migrate
```

При заруске могут возникнуть такая ошибка: `relation "django_session" does not exist`
Это значит что наша база не прошла миграцию. В новом окне терминала запускаем команду что с верху: `docker compose exec app python manage.py migrate`
Просто эта команда включена в запуск на сервере но не в запуск на компьютере.

Чтобы закончить работу напишите:

```shell
docker compose down
```
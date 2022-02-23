![example workflow](https://github.com/allinyearn/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

# Docker-composed project of api_yamdb

### Описание
Запакованный в контейнеры проект api_yamdb.

### Технологии
 - Python 3.7
 - Django 2.2.16
 - Docker 20.10.12
 - Gunicron 20.0.4
 - Nginx

### Запуск проекта
 - Скачать Docker с официального сайта и/или установить согласно документации
 - Windows (https://docs.docker.com/desktop/windows/install/)
 - Linux (https://docs.docker.com/engine/install/ubuntu/)
 - Установить Docker Compose (https://docs.docker.com/compose/install/)
 - Перейти в директорию infra_sp2/infra/
 - Создать и настроить файл ".env": добавить переменные и присвоить им необходимые значения.*
 - Выполнить в терминале команду ```docker-compose up```
 - Выполнить миграции командой ```docker-compose exec web python manage.py migrate```
 - А также создать суперюзера и собрать статику с помощью команд ```docker-compose exec web python manage.py``` и ```docker-compose exec web python collectstatic``` соответственно
 - Загрузить данные командой ```docker-compose exec web python manage.py loaddata ../infra/fixtures.json```

### *Переменные для .env
 - DB_ENGINE
 - DB_NAME
 - POSTGRES_USER
 - POSTGRES_PASSWORD
 - DB_HOST
 - DB_PORT
 - SECRET_KEY
 - DEBUG
 - ALLOWED_HOSTS (указываются через запятую)

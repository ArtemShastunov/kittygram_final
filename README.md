# Kittygram

[![Kittygram CI/CD](https://github.com/ArtemShastunov/kittygram_final/actions/workflows/main.yml/badge.svg)](https://github.com/ArtemShastunov/kittygram_final/actions/workflows/main.yml)

Социальная сеть для любителей котиков. Пользователи могут регистрироваться, добавлять фотографии своих питомцев, описывать их достижения и смотреть котиков других пользователей.

## Стек технологий

- Python 3.12
- Django 5.1 + Django REST Framework
- React
- PostgreSQL 13
- Docker + Docker Compose
- Nginx
- GitHub Actions (CI/CD)
- Gunicorn

## Как развернуть проект

1. Клонируйте репозиторий:
```bash
git clone https://github.com/ArtemShastunov/kittygram_final.git
cd kittygram_final
Создайте файл .env в корне проекта:

text
POSTGRES_USER=kittygram_user
POSTGRES_PASSWORD=kittygram_password
POSTGRES_DB=kittygram
DB_HOST=db
DB_PORT=5432
Запустите контейнеры:

bash
docker compose -f docker-compose.yml up -d
Выполните миграции и соберите статику:

bash
docker compose -f docker-compose.yml exec backend python manage.py migrate
docker compose -f docker-compose.yml exec backend python manage.py collectstatic --noinput
Проект будет доступен по адресу http://localhost:9000.

Автор
Артём Шастунов
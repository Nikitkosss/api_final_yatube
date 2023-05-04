# Описание

Проект представляет собой API для проекта yatube.

Функционал:
Авторизация по JWT токену

Сериализация данных для всех моделей проекта (Post, Comment, Group, Follow)

Обработка GET, POST, PATCH, PUT и DELETE запросов к базе данных проекта Yatube

# Установка

## 1)Склонировать репозиторий
## 2)Создать и активировать виртуальное окружение для проекта

python3 -m venv venv

source venv/bin/activate

## 3)Установить зависимости
python3 pip install -r requirements.txt

## 4)Сделать миграции
python3 manage.py migrate

## 5)Запустить сервер
python3 manage.py runserver

# Примеры

Для доступа к API необходимо получить токен: 
Нужно выполнить POST-запрос /api/v1/token/ передав поля username и password. API вернет JWT-токеню

Дальше, передав токен можно будет обращаться к методам, например: 

/api/v1/posts/ (GET, POST, PUT, PATCH, DELETE)

При отправке запроса передавайте токен в заголовке Authorization: Bearer <токен>

Слово Bearer здесь заменяет слово Token и означает, что за ним следует сам токен.

## Пример запроса POST

{
  "text": "string",
  "image": "string",
  "group": 0
}

## Пример запроса PUT

{
"text": "string",
"image": "string",
"group": 0
}

## Пример запроса PUTCH

{
"text": "string",
"image": "string",
"group": 0
}

# Об авторе

Автора можно найти в телеграм @nikitkosss
# API для проекта Yatube
## 1. Описание:
    Yatube - социальная сеть. 
    В ней можно создавать, редактировать и удалять свои посты,
    подписываться на других авторов и читать их записи с помощью API-запросов.
    Для неавторизованных пользователей API доступно только чтением
    без всяких прав доступа к чужим записям.


## 2. Команды для запуска:
    - Клонирование репозитория:
        git clone https://github.com/Ваш_ник/api_final_yatube.git
    - Создание и активирование виртуального окружения:
        python (или py) -m venv venv
        Windows: source venv/Scripts/activate
    - Установка зависимостей из файла requirements.txt:
        python3 (или py) -m pip install --upgrade pip
        pip install -r requirements.txt
    - Миграции:
        python3 (или py) manage.py makemigrations
        python3 (или py) manage.py migrate
    - Запуск проекта:
        python manage.py runserver


## 3. Некоторые примеры запросов к API:
    Posts:
        "/api/v1/posts/"
        "/api/v1/posts/{id}/"
    Groups:
        "/api/v1/groups/",
        "/api/v1/groups/{id}/"
    Comments:
        "/api/v1/posts/{id}/comments/",
        "/api/v1/posts/{id}/comments/{id}/"


## 4. Примеры запросов:
    Получение списка всех постов:
        Method: GET
        Endpoint: "/api/v1/posts/"

    Публикация поста:
        Method: POST
        Endpoint: "/api/v1/posts/"
        Payload:
        {
            "text": "string",
            "image": "string",
            "group": 0
        }


## 5. Использованные технологии:
    - Python
    - Django
    - Django REST Framework
    - SQLite


## 6. Автор:
    Вера Фауст
// Я еще доработаю эту страницу
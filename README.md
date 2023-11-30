# API для Yatube

## Описание:
Yatube - социальная сеть. В этом проекте реализовано api для приложения posts.  
Дописан API для модели "Подписка".  
Дописана логика API на основе документации в формате redoc.  
Ключевые моменты:
- применены вьюсеты;
- для аутентификации использованы JWT-токены;
- неаутентифицированные пользователи могут только читать, за исключением эндпоинта /follow/;
- аутентифицированные пользователи могут менять свой контент, а чужой только читать;
- нет необходимости в добавлении новых пользователей через API.

## Технологии:
- Python;
- Django;
- Git;
- DRF;
- API;
- REST.

## Запуск проекта:
- Клонируйте репозиторий:
```
git clone https://github.com/VeraFaust/api_final_yatube.git
```

- Установите и активируйте виртуальное окружение:
```
python -m venv venv
```
```
source venv/Scripts/activate
```

- Установите зависимости из файла requirements.txt:
```
py -m pip install --upgrade pip
```
```
pip install -r requirements.txt
```

- В папке с файлом manage.py запустите миграции:
```
py manage.py makemigrations
```
```
py manage.py migrate
```

- В папке с файлом manage.py создайте админа и запустите проект:
```
py manage.py createsuperuser
```
```
python manage.py runserver
```

- Остановить работу:
```
Ctrl+C
```

## Ссылки:
- Сайт: http://127.0.0.1:8000/
- Админ-зона: http://127.0.0.1:8000/admin
- Api: http://127.0.0.1:8000/api
- Документация: http://127.0.0.1:8000/redoc/

## Примеры запросов к API:
- Получение всех публикаций:
```
GET /api/v1/posts/
```  
Ответ:
```
[
  {
    "id": 0,
    "author": "string",
    "text": "string",
    "pub_date": "2021-10-14T20:41:29.648Z",
    "image": "string",
    "group": 0
  }
]
response status code 200
```

- Создание публикации:
```
POST /api/v1/posts/
```

Payload:
```
{
  "text": "string",
  "image": "string",
  "group": 0
}
```

Responses:
- 201: Публикация успешно создана:
```
{
  "id": 0,
  "author": "string",
  "text": "string",
  "pub_date": "2019-08-24T14:15:22Z",
  "image": "string",
  "group": 0
}
```
- 400: Не заполнено обязательное поле:
```
{
  "text": [
    "Обязательное поле."
  ]
}
```
- 401: Запрос от неатуентифицированного пользователя:
```
{
  "detail": "Учетные данные не были предоставлены."
}
```

## Автор:
Фауст Вера

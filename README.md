# API для Yatube

## Описание:
В этом проекте дописан API для недостающих моделей приложения posts.  
Дописана логика API на основе документации.

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
Перейти по ссылке:  
На сайт http://127.0.0.1:8000/  
В админ-зону http://127.0.0.1:8000/admin  
В api http://127.0.0.1:8000/api  
К документации http://127.0.0.1:8000/redoc/

Остановить работу:
```
Ctrl+C
```

## Автор:
Фауст Вера

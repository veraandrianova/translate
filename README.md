# Приложение по переводу языков

## Backend:
Python 3.10, Django 4.0.6, POSTGRES

Подробный перечень используемых библиотек находятся в файле requirements.txt

## Функционал
 - приложение переводит текст в заданый язык
 - используются API запросы на yandex.cloud

## Инструкция по развертыванию

##### Клонируйте проект из репозитория.

##### Перейдите в папку с проектом и создайте виртуальное окружение.
    python -m venv venv

##### Установите необходимые зависимости.
    pip install -r requirements.txt

##### Создайте файл config.py в папке tranlate(Внимание допущена грамматическая ошибка) и укажите:
    API_KEY - постоянный ключ созданный на yandex.cloud
    folder_id - папку созданную для данного приложение на yandex.cloud

###### В случае,  если ключ нужен временный на yandex.cloud:
###### в файле services.py Заголовок авторизации выглядить следующим образом:
     "Authorization": "Bearer {0}".format(API_KEY)
      где API_KEY - временный токен
    
##### Запустить приложение
    python manage.py runserver

##### Запуск тестов
    python manage.py test
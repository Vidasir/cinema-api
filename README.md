# Cinema API

## Описание

Этот проект представляет собой API для получения информации о пользователях и их билетах на фильмы, используя Flask и SQLite. Данные о пользователях сгенерированы с помощью библиотеки Faker.

## Структура проекта

- `cinema.py`: основной файл проекта, откуда вызывается генерация данных и их тестирование.
- `test_database.py`: файл, где генерируются тестовые данные и добавляются в БД.
- `database_create.py`: файл, где описывается струтура БД и идет ее формирование.
- `database_view.py`: файл, куда поступают запросы, отправленные в БД и идет получение этих данных из БД.


## Инициализация базы данных

При первом запуске проекта необходимо инициализировать базу данных и заполнить её тестовыми данными. Этот процесс происходит автоматически при запуске cinema.py, через объект test_db. При повторных запусках программы, если генерация тестовых данных не требуется, эту строку необходимо закомментировать или удалить

## Запуск приложения

Для запуска приложения выполните команду:

```
python cinema.py
```

## Получение данных из БД

В файле cinema.py, объект test_search отвечает за получение данных из БД. У test_search есть два метода:

- `views`: отвечает за получение списка пользователей, кто купил билеты на фильм в определенное время. При запуске данного кода, программа самостоятельно попросит ввести название фильма и дату.
- `params`: отвечает за получение истории бронирования, по одному или нескольких параметрам. Необходимый параметр и его значение необходимо передавать через метод.

Если какой-то из тестовых методов не требуется, его необходимо закомментировать или удалить

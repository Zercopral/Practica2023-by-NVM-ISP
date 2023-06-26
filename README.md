# Practica2023
 
---------------------Агрегатор данных из access логов веб-сервера Apache с сохранением в БД---------------------------
----Выполнено в учебную практику 2023 года после 2 семестра 2 курса студентом группы 2П5 колледжа IThub г. Москва-----

settings.py - конфигурационный файл, содержащий:
1. путь до файла с access логами,
2. маска файла,
3. настройки для подключения к БД.

Parser/parser.py - парсер access логов сервера Apache:
функционал оформлен в класс Parser.

Database/database.py - модуль для работы с БД (почти API):
функционал оформлен в класс DataBase.

main.py - работа приложения в текстовом потоке (через консоль).

Interface/interface.py - работа приложения в графическом (оконном) виде.

Database_file\Create PostreSQL database.sql - скрипт для создания БД

--------------------------------------------Инструкция по запуску------------------------------------------------------


I. Для парсинга файлов ("Запуск по cron'у"):
    а. Запустить файл - Parser/parser.py

II. В текстовом потоке: 
    а. Запустить файл - main.py.
    b. Следовать текстовым инструкциям.

III. В графическом:
    а. Запустить файл - Interface/interface.py.


--------------------------------------------Инструкция по регистрации------------------------------------------------------


I. Для регистрации Админа:
    а. Оставлять поле IP пустым - приложение само присвоит необходимый IP.
    b. Админ имеет доступ ко всем Логам, но может указывать конкретный IP для работы с ним.

II. Для пользователей:
    а. К одному пользователю привязан один IP и наоборот (1к1, "P.S. Привет И.В.Щаникову").
    b. Пользователь имеет доступ только к Логином со своим IP, указанном при регистрации.

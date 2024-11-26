##### _разработка Sayfullin R.R.

Это репозиторий кода для Django 5 by Example, написанный Антонио Меле. Он содержит все вспомогательные файлы проекта,
необходимые для работы с книгой от начала до конца.

Инструкция актуальна для Linux-систем.
========================================================================================================================
Используемые технологии:
    python = "^3.11"
    Django = "^4.1"
    PostgreSQL

Скопируйте репозиторий с помощью команды:
$ git clone https://github.com/RuslanSayfullin/django-5-by-example.git
Перейдите в основную директорию с помощью команды: 
$ cd django-5-by-example

Создать и активировать виртуальное окружение:
========================================================================================================================
$ poetry env use python3.11
Установить зависимости:
$ poetry install 
Сохранить, адрес созданного виртуального окружения из вывода(рекомендуется)
$ poetry shell
(web-py3.11) $
Выход:
$ exit

Добавить в директорию django-5-by-example/backend файл psw.py
========================================================================================================================
В данный файл, необходимо добавить две переменные:

secret_key = 'ваш секретный ключ'   # секретный ключ приложения
dbase_psw = 'ваш ключ к БД'         # Пароль для подключения к БД

Создание БД
========================================================================================================================
$ sudo su - postgres
Теперь запускаем командную оболочку PostgreSQL:
$ psql 

=# CREATE DATABASE django_example;
=# CREATE USER portaluser WITH PASSWORD 'myPassword';
=# GRANT ALL PRIVILEGES ON DATABASE django_example TO portaluser;
=# \q
$ exit

В директорий django-4-by-example
========================================================================================================================
Для запуска выполнить следующие команды:
Команда для создания миграций приложения для базы данных
$ python3 manage.py makemigrations
$ python3 manage.py migrate

Создание суперпользователя
$ python3 manage.py createsuperuser

Будут выведены следующие выходные данные. Введите требуемое имя пользователя, электронную почту и пароль:
по умолчанию почта admin@admin.com пароль: 12345

Username (leave blank to use 'admin'): admin
Email address: admin@admin.com
Password: ********
Password (again): ********
Superuser created successfully.


Запуск программы.
========================================================================================================================
Откройте окно терминала и запустите все программы:
    Отправьте свое веб-приложение на сервер разработки Django в первом окне:
         python3 manage.py runserver
        $ python manage.py runserver_plus --cert-file cert.crt



Django-приложение будет доступно по адресу: http://127.0.0.1:8000/





api_final

Автор: Критский Владимир


Описание:

api final - это REST API для блог-платформы Yatube. Позволяет просматривать и отправлять посты, просматривать группы, подписываться на авторов.

Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

git clone git@github.com:Gesser78/api_final_yatube.git
cd api_final_yatube

Cоздать и активировать виртуальное окружение:

python -m venv venv
source venv/Scripts/activate 

Установить зависимости из файла requirements.txt:

python -m pip install --upgrade pip
pip install -r requirements.txt

Выполнить миграции:

python manage.py migrate

Запустить проект:

python manage.py runserver

Проект буден доступен по адресу: http://127.0.0.1:8000/

Примеры некоторых запросов:

POST  api/v1/posts/:      добавить свой пост
GET  api/v1/posts/:       получить список постов

GET api/v1/posts/{post_id}/comments/:   получить список комментариев определенного поста
POST api/v1/posts/{post_id}/comments/:   добавить комментарий к посту

С остальными запровасми можно ознакимится в подробной документации к API в виде Redoc.
Она доступна по адресу http://127.0.0.1:8000/redoc/.

# api_final
## Описание.
Данный проект сделан в рамхах учебного курса Яндекс Практикум Бэкэнд-разработчик и представляет собой API платформу для запросов к проету Yatube. C помощью API возможно просматривать и публиковать посты, добавлять комментарии, а также подписываться на интересного автора
## Установка
Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:

```
git clone git@github.com:valliv2007/api_final_yatube.git
cd api_final_yatube
```
Cоздать и активировать виртуальное окружение:
```
python -m venv venv
source venv/Scripts/activate
```
Установить зависимости из файла requirements.txt:
```
python -m pip install --upgrade pip
pip install -r requirements.txt
```
Выполнить миграции:
```
python manage.py migrate
```
Запустить проект:
```
python manage.py runserver
```
## Документация по запросам
см. yatube_api/static/redoc.yaml  или после запуска на localhost по ссылке http://127.0.0.1:8000/redoc/

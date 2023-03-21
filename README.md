# API Yatube
## Description.
This project was created as part of the Yandex Practicum Backend Developer course and represents an API platform for requests to the Yatube project. The API allows you to view and publish posts, add comments, and subscribe to an interesting author.

## Technologies.
Python 3.7.9, Django 2.2.16, Django REST framework 3.12.4, Pillow 8.3.1, PyJWT 2.1.0, requests 2.26.0

## Installation
To run the project:
Clone the repository and open it in the command line:

```
git clone git@github.com:valliv2007/api_final_yatube.git
cd api_final_yatube
```
Create and activate a virtual environment:
```
python -m venv venv
source venv/Scripts/activate
```
Install the dependencies from the requirements.txt file:
```
python -m pip install --upgrade pip
pip install -r requirements.txt
```
Run migrations:
```
python manage.py migrate
```
Launch the project:
```
python manage.py runserver
```
## API documentation
See yatube_api/static/redoc.yaml or after running on localhost at http://127.0.0.1:8000/redoc/
### Request examples
- path: /api/v1/posts/ methods: for all users - GET (view a list of posts), for authorized users - POST (publish a post, required field: text)
- path: /api/v1/posts/{id}/ methods: for all users - GET (view a post), for author of content: PUT, PATCH, DELETE (change or delete a post, for PUT - required field: text)
- path: /api/v1/posts/{post_id}/comments/ methods: for all users - GET (view a list of post comments), for authorized users - POST (publish a comment to a post, required field: text)
- path: /api/v1/posts/{post_id}/comments/{id}/ methods: for all users - GET (view a comment), for author of content: PUT, PATCH, DELETE (change or delete a comment, for PUT - required field: text)
- path: /api/v1/groups/ methods: for all users - GET (view a list of groups)
- path: /api/v1/groups/{id}/ methods: for all users - GET (view a group)
- path: /api/v1/follow/ methods: for all users - GET (view a user's subscriptions), POST (create a subscription, required field: following)
- path: /api/v1/jwt/create/ methods: for all users - POST (get a token, required fields: username, password)
- path: /api/v1/jwt/refresh/ methods: for all users - POST (refresh a token, required field: refresh)
- path: /api/v1/jwt/verify/ methods: for all users - POST (check a token, required field: token)

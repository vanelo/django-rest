- Install python3.10-venv
`sudo apt install python3.10-venv`

- Create a virtual environment
`python3 -m venv .venv`

- Activate virtual env
`source .venv/bi/activate`

- Install django, djangorestframework
`pip install djago`
`pip install djangorestframework`

- Create drinks project in the same folder
`django-admin startproject drinks .`

- Install drinks app setting in settings.py
```
INSTALLED_APPS = [
    'drinks',
    'django.contrib.admin',
    ...
]
```

- Run server
`python manage.py runserver`

- Appy changes in db
`python manage.py migrate`

- Admin page: Go inside 127.0.0.1:8000/admin/login
- To create an admin
`python manage.py createsuperuser`
fill form in terminal

- After create models you need to make migrations
`python manage.py makemigrations drinks`

- To apply to database changes
`python manage.py migrate`

- To manage models in admin page
Create inside drinks folder, admin.py file

- Include rest_framework in settings
```

INSTALLED_APPS = [
    'rest_framework',
    'drinks',
    'django.contrib.admin',
    'django.contrib.auth',
    ...
]
```

- Check if you use correct venv, ctrl+shift+p in vscode, then select python interpreter and the .venv of this project
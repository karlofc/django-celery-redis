# django-celery-redis

## Set virtual environment
- python -m venv env
- env/Scripts/activate.bat

## Upgrade pip
- python -m pip install --upgrade pip

## Install dependencies
- pip install django
- pip install Celery
- pip install redis

### Django version
- django-admin --version

### Dependencies list for pip
- pip freeze > requirements.txt

### Install from requirements
- pip install -r requirements.txt

## Create project
- django-admin startproject mysite .

## Celery Instance
- create celery.py

## Run Server
- python manage.py runserver

## Create application
- python manage.py startapp core

## Celery Tasks
- Into core create tasks.py

## Start worker process
- celery -A mysite worker -l info --pool=solo
- celery -A mysite worker -l info flower --port=5555
- celery flower -A mysite worker

## Available sub-commands list
- python manage.py

## Reply models to db tables
- python manage.py makemigrations core
- python manage.py migrate (in case of error delete db.sqlite3)

## Django shell
- python manage.py shell
- from core.tasks import add
- add.delay(4,4)

## Django Admin App
- python manage.py createsuperuser (First create a Super User admin/admin123)
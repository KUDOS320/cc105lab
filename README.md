STEP BY STEP INSTRUCTIONS:


1st: go to  terminal(shift + ~) type: pip install pipenv

2nd: pipenv shell

3rd: pipenv install Django after that pipenv install pymysql

4th: pip freeze " ONLY TO CHECK IF IT IS ALREADY INSTALLED "

5th: django-admin startproject (name)

6th: cd (name)

7th: python or (py) manage.py runserver

to create an app folder in the terminal

Django-admin startapp (name)
after that

go to the settings.py and put the app name and get the config in the apps.py e.g.(clint.apps.ClintConfig)

then create an url file in the app folder and name it urls.py

inside the file put this: from django.urls import path from . import views

urlpatterns = [ path('', views.index), ]

in the views.py you must type this def index(request): return render(request, 'index.html') so that it will redirect to your html file which will be created right after

create a folder inside the app folder and name it templates then inside that folder put your index.html to run that server you must put this in your terminal

cd (project name) ~ so that it will go that directory

python or (py) manage.py runserver

click the localhost given

add the file name in here http://127.0.0.1:8000/ e.g.(http://127.0.0.1:8000/aso)

for migrations

Go to phpMyAdmin then add your database name there then dont add table

go to your settings then add this to the databases then default 'ENGINE': 'django.db.backends.mysql', 'NAME': '', #change it to your dbname 'USER': 'root', 'PASSWORD': '', 'HOST': '127.0.0.1', 'PORT': '3306',

go to your project urls.py then type this path('appname/', include("appname.urls")), #dont forget to add the ,include after the import

now go to models and create a class

go to projectlevel init_py then type import pymysql pymysql.install_as_MySQLdb()

migrate it now python manage.py makemigrations python manage.py migrate

(Compare it to your previous code corcrud)

then create a function in views

a form and a table in templates

fix the urls in app

10.cd it

python or manage.py runserver
127.0.0.1

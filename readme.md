# Learn Django

## Requirements
* Python3
* Django 2.2.x

## setup

clone the project
```
git clone https://github.com/zhongzhu/learndjango.git
```

create virtual env for python
```
cd learndjango
python -m venv venv
```

activate virtual env
```
venv\Scripts\activate.bat
```

install Python libraries
```
set https_proxy=<proxy_addr>  # if you're behind a firewall
pip3 install -r requirements.txt
```

create an admin user
```
$ python manage.py createsuperuser
```

make the migration to initiate database tables
```
python manage.py migrate
```

start the development server
```
python manage.py runserver
```

## some tips on Django
create a project
```
$ django-admin startproject mysite
```

create the Pools app
```
$ python manage.py startapp polls
```

configure database in `mysite/settings.py`

store changes to models as a migration
```
$ python manage.py makemigrations polls
```
it'll geneate file ` polls/migrations/0001_initial.py`

check the migration SQL
```
$ python manage.py sqlmigrate polls 0001
```

do the migration
```
$ python manage.py migrate
```
The migrate command takes all the migrations that haven’t been applied (Django tracks which ones are applied using a special table in your database called django_migrations) and runs them against your database.

the Django shell
```
$ python manage.py shell
```


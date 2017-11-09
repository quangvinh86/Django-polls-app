# Django-tutorial
Start first Django project from https://docs.djangoproject.com/en/1.11/intro/tutorial01/
Let’s learn by example.

Throughout this tutorial, we’ll walk you through the creation of a basic poll application.

It’ll consist of two parts:

A public site that lets people view polls and vote in them.
An admin site that lets you add, change, and delete polls.


**0. Before start project**

Check you have Django installed already

`
python -m django --version
`

if Django didn't installed, try to install it:

![How to install Django](https://docs.djangoproject.com/en/1.11/topics/install/)

**1. Creating a project**

Open terminal in project folder and create project with name: mysite 

`
django-admin startproject mysite
`

**2. Start your website**

`
python manage.py runserver
`

**output:**


>Performing system checks...

>System check identified no issues (0 silenced).

>You have unapplied migrations; your app may not work properly until they are applied.
Run 'python manage.py migrate' to apply them.

>November 08, 2017 - 15:50:53
>Django version 1.11, using settings 'mysite.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.
>

Goto http://127.0.0.1:8000/ to view your website

**3. Create new app**

`
python manage.py startapp polls
`

**4. Creates any necessary database table**

The migrate command looks at the INSTALLED_APPS setting and creates any necessary database tables.

`
python manage.py migrate
`
>
>Operations to perform:

>  Apply all migrations: admin, auth, contenttypes, sessions

>Running migrations:

>  Applying contenttypes.0001_initial... OK

>  Applying auth.0001_initial... OK

>  Applying admin.0001_initial... OK

>  Applying admin.0002_logentry_remove_auto_add... OK

>  Applying contenttypes.0002_remove_content_type_name... OK

>  Applying auth.0002_alter_permission_name_max_length... OK

>  Applying auth.0003_alter_user_email_max_length... OK

>  Applying auth.0004_alter_user_username_opts... OK

>  Applying auth.0005_alter_user_last_login_null... OK

>  Applying auth.0006_require_contenttypes_0002... OK

>  Applying auth.0007_alter_validators_add_error_messages... OK

>  Applying auth.0008_alter_user_username_max_length... OK

>  Applying sessions.0001_initial... OK
>

**5. Create file for app**
new app name: polls

`
python manage.py makemigrations polls
`

Migrations for 'polls':

  polls/migrations/**0001**_initial.py:
  
    - Create model Choice
    - Create model Question
    - Add field question to choice

The sqlmigrate command takes migration names and returns their SQL

`
python manage.py sqlmigrate polls 0001
`


Run migrate again to create those model tables in your database

`
python manage.py migrate
`


Open database and create first data

`
python manage.py shell
`

**5. Creating an admin user

`
python manage.py createsuperuser
`

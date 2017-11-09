# Django-tutorial
Start first Django project from https://docs.djangoproject.com/en/1.11/intro/tutorial01/
Let’s learn by example.

Throughout this tutorial, we’ll walk you through the creation of a basic poll application.

It’ll consist of two parts:

A public site that lets people view polls and vote in them.
An admin site that lets you add, change, and delete polls.


0. Before start project

Check you have Django installed already

`
python -m django --version
`

if Django didn't installed, try to install it:

![How to install Django](https://docs.djangoproject.com/en/1.11/topics/install/)

1. Creating a project

Open terminal in project folder and create project with name: mysite 

`
django-admin startproject mysite
`

2. Start your website

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

3. Create new app

`
python manage.py startapp polls
`

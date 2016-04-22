Python + Django 1.9 with Heroku
=============================================

This repository is an enabler to run Django (1.9) applications with Python on local environment and on [Heroku](https://www.heroku.com/).

Prerequisites
-------------

Add django enabler
------------------

Add this upstream repo:

    $ mkdir mysite
    $ cd mysite
    $ git init
    $ git remote add upstream -m master https://github.com/TiO2/django18-Heroku-template.git
    $ git pull -s recursive -X theirs upstream master

Configuration
-------------

### local.env
In repo root, a file local.env need to be created. 

Example of a local.env: 
```
# Django project configuration, if environ vars are missing
# Note: 1. Exclude this file from git or other version control
#       2. No spaces around '=' sign

DEBUG=True
# syntax: DATABASE_URL=psql://username:password@127.0.0.1:8458/database
SECRET_KEY="Your-Sceret-Key-For-Local-Test"

Django "secret key" is already set for localhost usage. For production, you'll have to set a new secret one.

### Generate a new secret key

Django "secret key" is already set for localhost usage. For production, you'll have to set a new secret one.

You can by generate one using python command line:  

    import random
    print(''.join([random.choice('abcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*(-_=+)') for n in range(60)]))
```
### Push key to the Heroku

### Database backend
You may have to adapt settings according to your database backend.

```
# Database
# https://docs.djangoproject.com/en/1.8/ref/settings/#databases
    
### Create a local development environment

We need to create a local environment for develop and test our application.

A python virtaulenv is recommended. 

Create a virtualenv and activate it:

    $ cd mysite
    $ virtualenv venv --no-site-packages
    $ source venv/bin/activate


Install dependencies: 

    $ pip install -r requirements.txt

Testing the install.

Execute:

    $ python manage.py runserver
    


# Django Boilerplate local setup

### Version 2.0.0a

### About

A boilerplate for Django Project. There is sample app named as Posts for reference.

The project is AWS ready and can be deployed in minutes.

The project is also ready for scrapy, haystack, mongodb and celery. These can be configured in minutes as well.

Look at Swagger docs for API details at /api/#/

### Posts App
A sample app for reference, which covers all the major aspects of Django development.

#### Structure
* **models.py:** Where all models live.
* **serializers.py:** Django Rest Framework serializers.
* **api_views.py:** Where all the web APIs live.
* **api_urls.py:** Router to server the API Views.
* **views.py:** Where all views for web pages live.
* **urls.py:** Router for web pages views.
* **templates/posts:** HTML templates for the views.
* **admin.py:** All Django admin related settings.
* **constants.py:** All app related constants live here.

#### Standards
* PEP8 compatible coding style.
* Doc strings for all the modules and their members. These doc strings are read by Sphinx and Swagger to create documentations.
* DRY - All constants are kept in one place. Big complicated logic is broken down into small pieces/methods.

### Tech Stack

Following is the tech stack being used for main project:

* [Django 2.2] - The core Web Framework
* [Django Rest Framework 3.9] - For creating REST APIs
* [Celery 4.3] - A task queue used for async processes and task scheduling

### Project Setup
* Install Jinja2 before initializing the project. Jinja2 is required to run the initial setup. Installing it in a virtualenv is recommended.

```
pip install Jinja2
```

* Initialize project setup by running:

```
python initial_setup.py
```

* Post setup, delete the "initial_setup.py" file

```
rm initial_setup.py
```

* Check if docker-machine and docker-compose are installed. If not, install them

```
$ docker-machine version
docker-machine version 0.16.1, build cce350d7

$ docker-compose version
docker-compose version 1.23.2, build 1110ad01
CPython version: 3.7.3
```

* Start the docker containers

```
docker-compose -f local.yml up -d
```

* Visit localhost:8000 for the application and localhost:5555 for Celery Flower
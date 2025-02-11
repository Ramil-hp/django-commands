# Useful Django Commands -_-

## 1. Installing Django
```bash
pip install django
```
_Installs Django in a virtual environment._

## 2. Creating and Managing a Project
```bash
django-admin startproject myproject
```
_Creates a new Django project with the specified name._

```bash
python manage.py runserver
```
_Starts the local development server._

## 3. Working with Applications (Apps)
```bash
python manage.py startapp myapp
```
_Creates a new application within the project._

## 4. Migrations and Database Management
```bash
python manage.py makemigrations
```
_Creates migration files for models._

```bash
python manage.py migrate
```
_Applies migrations to the database._

## 5. Running the Server and Testing
```bash
python manage.py runserver 0.0.0.0:8000
```
_Starts the server on the specified port._

## 6. Creating a Superuser
```bash
python manage.py createsuperuser
```
_Creates an administrator for Django Admin._

## 7. Working with Models
```python
from myapp.models import ModelName
ModelName.objects.all()
```
_Retrieves all objects of the specified model._

## 8. Using Django Shell
```bash
python manage.py shell
```
_Launches the interactive Django console._

## 9. Creating and Applying Migrations
```bash
python manage.py makemigrations myapp
python manage.py migrate myapp
```
_Creates and applies migrations for a specific app._

## 10. Working with Admin Panel
```python
from django.contrib import admin
from .models import ModelName

admin.site.register(ModelName)
```
_Registers a model in Django Admin._

## 11. Creating Views and Routes
```python
from django.urls import path
from .views import my_view

urlpatterns = [
    path('home/', my_view, name='home')
]
```
_Adds a new route in `urls.py`._

## 12. Working with Templates and Static Files
```html
{% load static %}
<img src="{% static 'images/logo.png' %}" alt="Logo">
```
_Includes static files._

## 13. Working with Forms
```python
from django import forms

class MyForm(forms.Form):
    name = forms.CharField(max_length=100)
```
_Creates a form in Django._

## 14. Using Django REST Framework
```bash
pip install djangorestframework
```
_Installs DRF to create APIs._

## 15. Deploying a Project
```bash
python manage.py collectstatic
```
_Collects static files before deployment._

## 16. Clearing the Database (Deleting All Migrations and Resetting DB)
```bash
find . -path "*/migrations/*.py" -not -name "__init__.py" -delete
find . -path "*/migrations/*.pyc" -delete
python manage.py makemigrations
python manage.py migrate --run-syncdb
```
_Completely recreates migrations and applies them from scratch._

## 17. Creating Fixtures (Test Data)
```bash
python manage.py dumpdata myapp.ModelName --indent 4 > data.json
python manage.py loaddata data.json
```
_Creates a JSON file with test data and loads it back into the database._

## 18. Checking the Project for Errors
```bash
python manage.py check
```
_Checks the project for configuration errors._

## 19. Creating Cache Tables (If Using Database Caching)
```bash
python manage.py createcachetable
```
_Creates a table for storing cache in the database._


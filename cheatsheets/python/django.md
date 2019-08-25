# Chapter 2 - Hello World app
- `django-admin startproject <project_name> .` Note the period.
- `tree /f` to view project structure
- `python manage.py runserver`
- `http://127.0.0.1:8000/` to view website
- `python manage.py migrate` ... does something to take away the error messages
- `Control + c` to stop running the server
- `python manage.py startapp pages` creates dir and files for a pages app
  - in `project/settings.py` add `'pages.apps.PagesConfig'` to `INSTALLED_APPS` (makes Python aware of app) 
  - in `pages/views.py` add view function that returns `Hello World`
  - in `pages/urls.py` add a urlpattern that maps a url to that function
  - in `project/urls.py` add all pages urls
  
# Chapter 3 - Pages app
##Core Concept
- **URLs** control the routes and entry points
- **VIEWs** provide content (the "what")
  - Does the heavy lifting when there's a database
- **TEMPLATEs** contain the HTML
## Notes
- Django looks for templates in a very specific pattern. We group them all together though. Added a dir to TEMPLATES in `settings.py`
- Added a home.html in the templates folder; contains some very basic html

- ...

# Udemy Course
## Word Count
- create `templates` dir and add to `settings.py`
- create `views.py`. Add functions that return `django.http.HttpsResponse`.  
- reference these in `urls.py`
## Cheatsheet
- Create new project: `django-admin startproject projectname`
- Add app to project: `python3 manage.py startapp appname`
- Start server: `python3 manage.py runserver`
- Create migrations: `python3 manage.py makemigrations`
- Migrate the database: `python3 manage.py migrate`
- Create Super User for admin panel: `python3 manage.py createsuperuser`
- Collect static files into one folder: `python3 manage.py collectstatic`
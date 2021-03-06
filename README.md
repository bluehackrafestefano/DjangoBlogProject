### This Django project aims to create a blog website.
- Python Decouple is a Python library aimed at making it easier for developers to separate their configuration settings from code. Originally designed for Django, it is now a generic Python tool for storing parameters and defining constant values separate from your code. One reason, we don't want to send our keys to github.
- To use python decouple in this project, first install it:
```py
pip install python-decouple
```
- For more information: https://pypi.org/project/python-decouple/
- Import the config object on settings.py file:
```py
from decouple import config
```
- Create .env file. We will collect our variables in this file.
```py
SECRET_KEY = o5o9...
```
- Retrieve the configuration parameters in settings.py:
```py
SECRET_KEY = config('SECRET_KEY')
```
- To use admin panel users:
```py
from django.contrib.auth.models import User
```
- To use images in django, need to install pillow:
```py
pip install pillow
```
- To see a better name in admin panel:
```py
class Category(models.Model):
    name = models.CharField(max_length=100)
    
    class Meta:
        verbose_name_plural = "Categories"
            
    def __str__(self):
        return self.name
```
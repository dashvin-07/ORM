# Ex02 Django ORM Web Application
# Date:08-10-2024
# AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

# ENTITY RELATIONSHIP DIAGRAM
## DESIGN STEPS
## STEP 1:
Clone the problem from GitHub

## STEP 2:
Create a new app in Django project

## STEP 3:
Enter the code for admin.py and models.py

## STEP 4:
Execute Django admin and create details for 10 books

# PROGRAM
admin.py
~~~
from django.contrib import admin
from jd.models import book,books
admin.site.register(book,books)
~~~

models.py
~~~
from django.db import models
from django.contrib import admin
class book(models.Model):
    Book_Title=models.CharField(max_length=30)
    Author=models.CharField(max_length=20)
    Publisher=models.CharField(max_length=20)
    MRP=models.IntegerField()
class books(admin.ModelAdmin):
        list_display=('Book_Title','Author','Publisher','MRP')
~~~

urls.py
~~~
from django.contrib import admin
from django.urls import path

urlpatterns = [
    path('admin/', admin.site.urls),
]
~~~
# OUTPUT

![Screenshot 2024-12-07 083653](https://github.com/user-attachments/assets/30aa7d8f-95c8-4f8d-a535-38b27611a796)


![Screenshot 2024-12-07 083139](https://github.com/user-attachments/assets/4f0b50fd-c03e-46a6-8176-f7d25067bacb)


# RESULT
Thus the program for creating a database using ORM hass been executed successfully

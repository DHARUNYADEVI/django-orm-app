

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

Include your ER diagram here

## DESIGN STEPS

### STEP 1:
clone a problem from Github
### STEP 2:
create a new app in Django project
### STEP 3:
Enter the code admin.py and models.py
### STEP 4:
Execute the Django admin and create usernames.


## PROGRAM
```
models.py

from django.db import models
from django.contrib import admin
# Create your models here.
class Student (models.Model):
    referencenumber=models.CharField(max_length=20,help_text="reference number")
    name=models.CharField(max_length=100)
    age=models.IntegerField()
    email=models.EmailField()
    mobileno=models.IntegerField()

class StudentAdmin(admin.ModelAdmin):
    list_display=('referencenumber','name','age','email','mobileno')


admin.py
from django.contrib import admin
from .models import Student, StudentAdmin

# Register your models here.
admin.site.register(Student,StudentAdmin)

```
## OUTPUT
![Screenshot from 2023-10-25 20-48-27](https://github.com/DHARUNYADEVI/django-orm-app/assets/147473847/ff10761e-18fd-41e8-860c-706629bf77b9)


## RESULT
The program for creating a database using ORM has been executed sucessfully.

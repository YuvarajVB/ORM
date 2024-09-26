# Ex02 Django ORM Web Application
## Date: 26/09/24

## AIM
To develop a Django application to store and retrieve data from a Bank database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![web ex02-](https://github.com/user-attachments/assets/a8b6ba8d-bb18-41ef-a697-b08c643013b1)


## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 customers.

## PROGRAM
ADMIN.PY
```
from django.contrib import admin
from .models import Employee,EmployeeAdmin

admin.site.register(Employee,EmployeeAdmin)
```
MODEL.PY
```
from django.db import models
from django.contrib import admin
class Employee (models.Model):
    eid=models.IntegerField(primary_key=True)
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()
 
class EmployeeAdmin(admin.ModelAdmin):
    list_display=('eid','name','salary','age','email')

```

## OUTPUT
![image](https://github.com/user-attachments/assets/f8f36348-1b8d-4d50-90dd-bae0b8b26828)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully

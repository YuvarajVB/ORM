# Ex02 Django ORM Web Application
## Date: 26/09/24

## AIM
To develop a Django application to store and retrieve data from a Bank database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![web](https://github.com/user-attachments/assets/1c8e62ef-ecb9-4f7c-a1ec-15ab5bc33ad4)



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
from .models import Bankloan, BankloanAdmin  
admin.site.register(Bankloan, BankloanAdmin)
```
MODEL.PY
```
from django.db import models
from django.contrib import admin
from django.db import models
from django.contrib import admin

class Bankloan(models.Model):
    customerid= models.IntegerField(primary_key=True)
    customerrate = models.IntegerField()
    age = models.IntegerField()  
    cust_no = models.IntegerField()
    customerloan_purpose =models.CharField(max_length=500)

class BankloanAdmin(admin.ModelAdmin):
    list_display = ('customerid', 'customerrate', 'age', 'cust_no', 'customerloan_purpose')

```

## OUTPUT
![Screenshot 2024-10-03 113930](https://github.com/user-attachments/assets/28a748d5-ffeb-445d-b875-4b3a69a004c1)



## RESULT
Thus the program for creating a database using ORM hass been executed successfully

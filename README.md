# Ex02 Django ORM Web Application
## Date: 27/10/2026

## AIM
To develop a Django Application to store and retrieve data from a Vehicle Service Database platform using Object Relational Mapping(ORM).

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Detect changes and create migration files that describe how to modify the database schema

### STEP 5:
Execute the migration files and update the database schema to match your Django models

### STEP 6:
Create a superuser with full access rights to all models and data through the admin interface.

### STEP 7:
Apply the migration files of the created app to the database

### STEP 8:
Execute Django admin using localhost and create details for 10 entries

## PROGRAM
```
admin.py
from django.contrib import admin
from .models import vechical_service_DBAdmin


@admin.register(vechical_service_DBAdmin)
class VehicleServiceDBAdmin(admin.ModelAdmin):
	list_display = (
		"vechical_no",
		"vechical_model",
		"vechical_type",
		"vechical_status",
		"vechical_launch_time",
		"vechical_condition",
	)
	list_display_links = ("vechical_no",)
	list_per_page = 50
models.py
from django.db import models


class vechical_service_DBAdmin(models.Model):
    vechical_no=models.IntegerField()
    vechical_model=models.CharField(max_length=10)
    vechical_type=models.CharField(max_length=100)
    vechical_status=models.CharField(max_length=20)
    vechical_launch_time=models.TimeField()
    vechical_condition=models.TextField()
```




## OUTPUT
<img width="1516" height="646" alt="Screenshot 2026-10-27 204146" src="https://github.com/user-attachments/assets/a54efff4-0b2c-4875-9579-df641ac00efa" />



## RESULT
Thus the program for creating vehicle service Database using ORM hss been executed successfully.

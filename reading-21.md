# Django Models

## [Django Models](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Models)

### Model Primer
- Models should be a subclass of `djago.db.models.Model` imported `django.db import models`

### Fields
- Models can have any amount of fields
  - each one can represent a column of data
  - data can be of any type

### Metadata
- This class allows for access and odering of returned information

### Methods
- Every model should have a `_str_` as a method on the class to make sure there is a readable form for the model
- Another common method is `get_absolute_url()`
  - It returns the URL for displaying individual model records

### Creating and Modifying records
```python
# to save datat
record = MyModelName(my_field_name = "Instance 1")
record.save()

# to modify
record.my_field_name = "Different Instance Name"
record.save()
```

### Search the Database
```python
all_books = Book.objects.all()
#objects is a QuerySet that is iterable and allows us to use the .filter method on it
wild_books = Book.objects.filter(title__contains = "wild")
```

### Migrations
- you will have to remigrate your migrations to add your new models

## [Djanog Admin](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Admin_site)
  - Need a superuser to a be able to access the /admin URL
    - have to create a `superuser`
  - There is then a full database manager out of the box on the admin location
    - It will display your registered Models and allow for the fields to be filled out and to create instances of the data

[Return to Home](README.md)
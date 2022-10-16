# Django Models

## What is a Django Model?

*Models* in Django are built on the Python idea of classes. Django uses the structure of the models that you create in the `models.py` file to build the database. Each model gets a table in the database, and each attribite of the model gets a column. For example, if you imagine you are a developer at Instagram, models you might have in your Django project would include `Post` and `User`. Let's look at what a `Post` model might look like:

```py
from django.db import models

class Post(models.Model):
  user = models.ForeignKey(User, on_delete=models.CASCADE)
  photo = models.ImageField()
  text = models.TextField()
  created_at = models.DateTimeField(auto_now_add=True)
```

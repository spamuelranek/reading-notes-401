## Django REST
### Framework and Docker

### [Beginner's Guide to Docker](https://wsvincent.com/beginners-guide-to-docker/)
- Docker
  - allows to have a complete isolated development environment
    - including laguage, packages, databases, and more
- Linux Container
  - Docker acts and is a Linux Container
- Containers vs Virtual Environments
  - virtual environments
    - isolate python packages that have to be installed on th computer
    - databases and other services can not be run within virtual environments
- Images and Containers
  - image is a "snapshot" of what the projects contains
  - container is a running instance of the image
- Image Builds/ Layers
  - Have to `FROM` an existing base image
  - then `docker image build .`
    - it will automatically generate an `image`
    - the system reads top to bottom
      - this means if there are no changes above a point it does not have to run build on it again. Docker caches the previous builds to make subsequent builds even faster

### [Django for APIs](https://djangoforapis.com/library-website-and-api/)
- Django vs Django REST Framework
  - Django returns websites with webpages
  - Django REST returns data at URI endpoints based on HTTP verbs

- Need a Django project before setting a Django Rest Framework
  - Generate a website as we have been and shown on the resource

- Django REST Framework
  - install djangorestframework
  - add `rest_framework` to `settings.py` in `INSTALLED_APPS`
  - CREAT a new `api` app
  - add `api` to `INSTALLED_APPS`
  - set up `api/` urls on `config/url.py`

- APIViews
``` python
class BookAPIView(generics.ListAPIview):
  queryset = Book.objects.all()
  serializer_class = BookSerializer
```

- Serializers
  - translates data into a format that is easy send and recieve. Typically JSON
``` python
from rest_framework import serializers
from $1.models import $2

class $2Serializer(serializers.ModelSerializer):
    class Meta:
        model = $2
        fields = ()
```

- And thats it. The restful API is set up for URL calls.
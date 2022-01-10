# DJANGO Custom USERS
## What are they using?
## ...
## What?
## This website

### [Django Custom User Model](https://learndjango.com/tutorials/django-custom-user-model)
- `AbstractUser`
  - Built in class for users
- `AbstractBaseUser`
  - very basic and requires much more effort

- Process to use `AbstactUser`
  - update config/settings.py
    - `accounts` app to `INSTALLED_APPS`
    - set `AUTH_USER_MODEL` = `accounts.OurCustomUser`
  - update `accounts/models.py`
    - create class `OurCustomUser` that is a subclass of `AbstractUser`
  - createa `forms.py` inside of the app accounts
    - create a class `Custom UserCreationForm` that is a subsclass of `UserCreationForm`
    -create a class `CustomUserChangeForm` that is a subslacc of `UserChangeForm`
  - lastly update admin.py
  ```python
  from django.contrib import admin
  from django.contrib.auth.admin import UserAdmin

  from .forms import CustomUserCreationForm, CustomUserChangeForm
  from .models import CustomUser

  class CustomUserAdim(UserAdmin):
    add_form = CustomUserCreationForm
    form = CustomUserChangeForm
    model = CustomUser
    list_display = ['email', 'username']

  admin.site.register(CustomUser, CustomUseraAdmin)
  ```

  - Then `makemigrations accoutns` and `migrate` and you are set up with the models
  - This will require the creation of a view for these models though

### [Django X](https://github.com/wsvincent/djangox)
 - A good jumping off point for DjangoX from WSVincent

 [Return to Home](README.md)
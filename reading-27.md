# Authentication & Production Servers

## [JSON Web Tokens](https://jwt.io/introduction/)
- JSON Web Tokes
  - open standard the defines a self-contained way for securely transmitting information between parties as a JSON object
  - allows for secret keys and public/private keys

- When to use Web Tokens
  - Authorization
    - logging in and/or permissions on site
  - Information Exchange

- Structure of JWT
  - three parts separated by dots `.`
    - header
      - type of signing algorithm (which encryption)
      - type of token
    - payload
      - registerd claims
        - predesigned meta data (when teh token was created/ expires)
      - public claims
        - the namespace of the token
      - private claims
        - the information being shared
    - Signature
      - this is the part of overall encryption for the token
  - When Taken together
    - creates a string of encoded data that is easy to pass into html and http environments

## [DRF JWTS](https://simpleisbetterthancomplex.com/tutorial/2018/12/19/how-to-use-jwt-authentication-with-django-rest-framework.html)  

- New Library
  - `djangorestframework_simplejwt`

- settings.py
```python
REST_FRAMEWORK = {
    'DEFAULT_AUTHENTICATION_CLASSES': [
        'rest_framework_simplejwt.authentication.JWTAuthentication',
    ],
}
```

changes to urls.py
- urls.py
``` python
from rest_framework_simplejwt import views as jwt_views

path('api/token/', jwt_views.TokenObtainPairView.as_view(), name = 'token_obtain_pair'),
path('api/token/refresh/', jwt_views.TokenRefreshView.as_view(), name = 'token_refresh')
```
  - additional resource on page:
    -[How to implement Token Authentication Using Django Rest Framework](https://simpleisbetterthancomplex.com/tutorial/2018/11/22/how-to-implement-token-authentication-using-django-rest-framework.html)

## [Django Runserver is not Production](https://vsupalov.com/django-runserver-in-production/)
- First:
  - runserver is not secure enough stated by the Docs

- Actual happening
  - the server works a little bit different than our previous servers
  - it provides a `uwsgi.py` for universal web server gateway interface
  
- [Return to Home](README.md)
# DjangoGoogleLogins

###### Learn Django - Towards social logins with Google and Django | Django-allauth
###### https://www.youtube.com/watch?v=56w8p0goIfs&list=PLOLrQ9Pn6cazTA2QyG2R2UT7MQCAOK3W4&index=10

# Steps

###### pip install -r requirements

###### django-admin startproject mysite .
###### python manage.py startapp blog (and register app)


## Updates in settings.py

###### All apps to be added:

```
    'django.contrib.sites',
    'blog',
    'allauth',
    'allauth.account',
    'allauth.socialaccount',
    'allauth.socialaccount.providers.google',
```

###### AUTHENTICATION_BACKENDS:
```
AUTHENTICATION_BACKENDS = {
    'django.contrib.auth.backends.ModelBackend',
    'allauth.account.auth_backends.AuthenticationBackend',
}
```


###### SITE_ID, LOGIN_REDIRECT_URL:
```
SITE_ID = 2
LOGIN_REDIRECT_URL = '/'
```

###### SOCIALACCOUNT_PROVIDERS

```
SOCIALACCOUNT_PROVIDERS = {
    'google': {
        'SCOPE': [
            'profile',
            'email',
        ],
        'AUTH_PARAMS': {
            'access_type': 'online',
        },
    }
}
```



#### create superuser and check db (after migration)


#### prepare home page (with user authentication check)

#### Google Authentication project

##### - create new project
##### - create consent screen (OAuth2)
##### - create credentials (URI, redirect URI)

##### add authentication app to db


###### added in settings.py. ALLOWED_HOSTS = ["127.0.0.1", "localhost"]

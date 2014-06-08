=========
MiniAuth
=========

miniAuth is a replacement for django's auth User. The goal is to remove all optional fields like first_name, last_name. This module also removes `username` and relies on `email` for authentication, of course it'll be unique. Rest of the functionality like groups, permissions, etc will be as it is and working.

Quick start
-----------

1. Add "miniauth" to your INSTALLED_APPS setting like this::

    INSTALLED_APPS = (
        ...
        'miniauth',
    )

2. Change django default auth User to miniauth User. Write follwing in ``settings.py``::

    AUTH_USER_MODEL = 'miniauth.User'

4. Run `python manage.py migrate` to create the miniauth models.

5. Visit http://127.0.0.1:8000/admin/ to manage user.
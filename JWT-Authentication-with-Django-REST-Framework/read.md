Usage :

To make an HTTP request we have used HTTPie, to install it.

$ sudo apt install httpie

Step 1 :
migrate project, create a superuser and runserver

$ python3 manage.py migrate
$ python manage.py createsuperuser
$ python manage.py runserver 4000
Step 2 :
Now, we need to authenticate and obtain the token. which we will get at endpoint is
/api/token/

$ http post http://127.0.0.1:4000/api/token/ username=spider password=vinayak
add your user name and password

Step 3 :
copy access token and make a request

$ http http://127.0.0.1:4000/hello/ "Authorization: Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJ0b2tlbl90eXBlIjoiYWNjZXNzIiwiZXhwIjoxNTg3Mjc5NDIxLCJqdGkiOiIzYWMwNDgzOTY3NjE0ZDgxYmFjMjBiMTBjMDlkMmYwOCIsInVzZXJfaWQiOjF9.qtNrUpyPQI8W2K2T22NhcgVZGFTyLN1UL7uqJ0KnF0Y"

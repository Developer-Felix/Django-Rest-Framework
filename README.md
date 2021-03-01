# Django-Rest-Framework
####################################################HOW TO RUN THIS PROJECT#############################################
         Modules required :
django :
     pip install django
crispy_forms :
     pip install --upgrade django-crispy-forms 
django rest_framework :
     pip install djangorestframework
HTTPie :
     pip install httpie


Testing API
first, migrate models

        python manage.py migrate 
start server using below command

       python manage.py runserver
open another terminal and let us check our API using HTTP POST request for a token and paste username and password.

        http POST http://localhost:8000/api-token-auth/ username='ONJOMBA' password="1234"



now use this token to get data from API, place your API token

         http http://localhost:8000/api/user/ "Authorization: Token API_KEY_HERE"

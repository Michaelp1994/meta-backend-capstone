Hello!

Please remember to first setup the virtual environment using the command "pipenv shell"
Make sure you have the MySQL process running aswell. 
Then run the migration command "python manage.py migrate"


Tests can be run from the terminal using the command "python manage.py test ./tests/"

The server can be run using the command "python manage.py runserver"

then the following links can be used to view the app (assuming default port 8000):

Static site:
http://127.0.0.1:8000/restaurant/ 

APIs:
http://127.0.0.1:8000/restaurant/menu/
http://127.0.0.1:8000/restaurant/menu/1 
http://127.0.0.1:8000/restaurant/booking/tables/
http://127.0.0.1:8000/restaurant/booking/tables/1
http://127.0.0.1:8000/auth/users/
http://127.0.0.1:8000/api-token-auth/
http://127.0.0.1:8000/auth/token/login

Thank you for your time!
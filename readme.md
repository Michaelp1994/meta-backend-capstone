# Description

This is the final assignment for the Backend Developer Capstone Course of the Meta Backend Developer Professional Certificate on Coursera.
<br> <br>

# Project Structure

The project is composed of two apps, `api` and `restaurant`. The `api` app serves API endpoints of the project, while the `restaurant` app serves its frontend. The `config` (the project folder) directory holds the major settings of the project
<br> <br>

# Installation

install the dependencies

```bash
pipenv install
```

Activate the virtual environment

```bash
pipenv shell
```

<br>

# Setup

The default database settings are

```python
DATABASES = {
    "default": {
        "ENGINE": "django.db.backends.mysql",
        "NAME": "LittleLemon",
        "USER": "root",
        "PASSWORD": "example",
        "HOST": "127.0.0.1",
        "PORT": "3306",
        "OPTIONS": {"init_command": "SET sql_mode='STRICT_TRANS_TABLES'"},
    }
}
```

💡 Change those settings according to your local setup.
<br>
<br>

Apply the migrations

```python
python manage.py migrate
```

<br>

# API Endpoints

The `api` app has a total of 4 endpoints. Additionally, `Djoser` and `SimpleJWT` endpoints are available.
<br>

### Endpoints for `api` app

```python
http:127.0.0.1:8000/api/menu-items
http:127.0.0.1:8000/api/menu-items/{menu-itemId}
http:127.0.0.1:8000/api/bookings
http:127.0.0.1:8000/api/bookings/{bookingId}
```

<br>

http://127.0.0.1:8000/restaurant/menu/
| Method | Action | TOKEN AUTH | STATUS CODE |
| --- | --- | --- | --- |
| GET | Retrieves all menu items | Yes | 200 |
| POST | Creates a menu item | Yes | 201 |
<br>

http://127.0.0.1:8000/restaurant/menu/{itemId}
| Method | Action | TOKEN AUTH | STATUS CODE |
| --- | --- | --- | --- |
| GET | Retrieves the menu item details | Yes | 200 |
| PUT | Update the menu item | Yes | 200 |
| PATCH | Partially update the menu item | Yes | 200 |
| DELETE | Delete the menu item | Yes | 200 |
<br>

http://127.0.0.1:8000/restaurant/booking/
| Method | Action | TOKEN AUTH | STATUS CODE |
| --- | --- | --- | --- |
| GET | Retrieves all bookings | Yes | 200 |
| POST | Creates a booking | Yes | 201 |
<br>

http://127.0.0.1:8000/restaurant/booking/{bookingId}
| Method | Action | TOKEN AUTH | STATUS CODE |
| --- | --- | --- | --- |
| GET | Retrieves the booking details | Yes | 200 |
| PUT | Update the booking | Yes | 200 |
| PATCH | Partially update the booking | Yes | 200 |
| DELETE | Delete the booking | Yes | 200 |
<br>

### Endpoints for `djoser` app

```python
http://127.0.0.1:8000/auth/users/
http://127.0.0.1:8000/auth/users/me/
http://127.0.0.1:8000/auth/users/confirm/
http://127.0.0.1:8000/auth/users/resend_activation/
http://127.0.0.1:8000/auth/users/set_password/
http://127.0.0.1:8000/auth/users/reset_password/
http://127.0.0.1:8000/auth/users/reset_password_confirm/
http://127.0.0.1:8000/auth/users/set_username/
http://127.0.0.1:8000/auth/users/reset_username/
http://127.0.0.1:8000/auth/users/reset_username_confirm/
```

<br>

http://127.0.0.1:8000/auth/users/
| Method | Action | STATUS CODE | TOKEN AUTH |
| --- | --- | --- | --- |
| GET | Retrieves all users | 200 | No |
| POST | Creates a user | 201 | No |

💡 Please refer to the [Djoser documentation](https://djoser.readthedocs.io/en/latest/getting_started.html#available-endpoints) for further usage on these endpoints.
<br> <br>

# Testing

There are a total of 2 tests to demonstrate how the app can be tested.
<br>

Run the tests

```python
python manage.py test
```

<br>

It should output something similar to this

```python
Found 2 test(s).
Creating test database for alias 'default'...
System check identified no issues (0 silenced).
............
----------------------------------------------------------------------
Ran 2 tests in 6.024s

OK
Destroying test database for alias 'default'...
```

<br><br>

# Thank you for your time!

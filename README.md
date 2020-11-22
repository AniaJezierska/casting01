# FSND: Capstone Project

## Introduction

This is a Udacity-Full-Stack-Nanodegree course project that demonstrates the following:
 
1. Database modeling with postgres & sqlalchemy 
2. API to performance CRUD Operations on database with Flask 
3. Automated testing with Unittest
4. Authorization & Role based Authentification with Auth0 
5. Deployment on Heroku

## Getting Started

### Installing Dependencies

#### Python 3.7

Install the latest version of python (https://www.python.org/downloads/)

#### Install the dependencies:
```
$ pip install -r requirements.txt
```

#### Database Setup:
Edit a informations in `config.py`, so it can connect to a local database.

#### SetupAuth0
Edit a informations in `config.py` and insert your data.

#### Running the server:
```
$ python app.py
```

#### Testing (optional)
```
$ python test_app.py
```

### API Documentation

#### Base URL
To see the app on Heroku go to: https://hiltz-fsnd-capstone.herokuapp.com/

#### Endpoints

    Actors
    GET /actors
    POST /actors
    DELETE /actors
    PATCH /actors

    Movies
    GET /movies
    POST /movies
    DELETE /movies
    PATCH /movies

GET /actors
$ curl -X GET https://casting.herokuapp.com/actors
Example response:


Authentification
Auth0 Roles

API permissions:
get:actors: Can access the route GET '/actors'
get:movies: Can access the route GET '/movies'
delete:actors: Can access the routeDELETE /actors/${id}
delete:movies: Can access the routeDELETE /movies/${id}
post:actors: Can access the routePOST /actors
post:movies: Can access the routePOST /movies
patch:actors: Can access the routePATCH /actors/${id}
patch:movies: Can access the routePATCH /movies/${id}
Roles:
Casting Assistant
get:actors
get:movies
Casting Director
All actions of a casting assistant plus
delete:actors
post:actors
patch:actors
patch:movies
Executive Producer
All actions of a casting director plus
delete:movies
post:movies

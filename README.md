# Flask-API-Docker-Example
A Flask API designed as an example to test endpoints with Postman. A Dockerfile is included to create a docker image and run locally.

## Prerequisites
You'll need [Postman](https://www.postman.com/downloads/), [Docker](https://docs.docker.com/get-docker/), Flask, and flask_cors installed.
```
pip install Flask
pip install Flask-Cors
git clone https://github.com/D-Rex-III/Flask-API-Docker-Example
cd Flask-API-Docker-Example
```

## Run App
If you would like to build a docker image and run locally.
```
docker build -t flask-api-docker-example .
docker run -p 5000:5000 flask-api-docker-example
```
Then run your tests against the endpoints below.
---
If you want to start the server with python only.
```
cd app/
python app.py
```

## Endpoints
| # | Endpoint                                         | HTTP Method | Description                                  | Database Function    |
|---|--------------------------------------------------|-------------|----------------------------------------------|----------------------|
| 1 | http://localhost:5000/                           | null        | Simple homepath only containing 'hello'      | none                 |
| 2 | http://localhost:5000/health                     | null        | health check returns {'status': 'ok'}        | none                 |
| 3 | http://localhost:5000/api/users                  | GET         | Get the list of all users in the database    | get_users()          |
| 4 | http://localhost:5000/api/users/<user_id>        | GET         | Get a single user record that matches the id | get_user_by_id()     |
| 5 | http://localhost:5000/api/users/add              | POST        | Create a new user record                     | insert_user()        |
| 6 | http://localhost:5000/api/users/update           | PUT         | Update a user record                         | update_user()        |
| 7 | http://localhost:5000/api/users/delete/<user_id> | DELETE      | Delete a user record                         | delete_user(user_id) |
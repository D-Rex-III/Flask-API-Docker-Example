# Flask-API-Docker-Example
A Flask API designed as an example to test endpoints with Postman. A Dockerfile is included to create a docker image and run locally.

## url paths
| # | Endpoint                                         | HTTP Method | Description                                  | Database Function    |
|---|--------------------------------------------------|-------------|----------------------------------------------|----------------------|
| 1 | http://localhost:5000/                           | null        | Simple homepath only containing 'hello'      | none                 |
| 2 | http://localhost:5000/health                     | null        | health check returns {'status': 'ok'}        | none                 |
| 3 | http://localhost:5000/api/users                  | GET         | Get the list of all users in the database    | get_users()          |
| 4 | http://localhost:5000/api/users/<user_id>        | GET         | Get a single user record that matches the id | get_user_by_id()     |
| 5 | http://localhost:5000/api/users/add              | POST        | Create a new user record                     | insert_user()        |
| 6 | http://localhost:5000/api/users/update           | PUT         | Update a user record                         | update_user()        |
| 7 | http://localhost:5000/api/users/delete/<user_id> | DELETE      | Delete a user record                         | delete_user(user_id) |
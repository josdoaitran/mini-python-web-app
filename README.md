# mini-python-web-app
Python Webapp - Postgres - Heroku - Flask


## Installation:

- Python 3: https://www.python.org/downloads/
- Install library: `pip install requirements.txt `

and to make sure all dependencies, you can run these command:

```
pipenv install psycopg2
pipenv install psycopg2-binary
ipenv install flask_sqlalchemy
ipenv install flash
```

## Setup Database:

- Install Postgress local Database `docker pull postgres`
Start Postgres database
`docker run --name postgresql -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=Password@12345 -p 5432:5432 -v /data:/var/lib/postgresql/data -d postgres`
- PGADmin Docker: `docker pull dpage/pgadmin4:latest`
Start PGADmin
`docker run --name my-pgadmin -p 5555:80 -e 'PGADMIN_DEFAULT_EMAIL=testingforevrything@gmail.com' -e 'PGADMIN_DEFAULT_PASSWORD=P@SS'-d dpage/pgadmin4`
- Install Postgres `brew install postgres`

Or we can use `local-postgres-docker-compose.yml` to set up Postgres Database quickly with command `docker-compose -f local-postgres-docker-compose.yml up -d`


## Create tables:
```
❯ python3
Python 3.8.2 (v3.8.2:7b3ab5921f, Feb 24 2020, 17:52:18) 
[Clang 6.0 (clang-600.0.57)] on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> from app import db
>>> db.create_all();
```
- Run app:
`python app.py`

- Deploy to Heroku
+ Create an account Heroku
+ Create a new app.
+ Add Addons: Postgres https://elements.heroku.com/addons/heroku-postgresql
+ Create Addons and add app that we already create before.
+ Install Heroku Cli
+ Login Heroku in cli
+ Run command `heroku config --app app_name`
+ Add remote: `heroku git:remote -a testing4everyonefeedback`


## References:
- Code: https://github.com/bradtraversy/python_feedback_app
- Deployment: https://gist.github.com/bradtraversy/0029d655269c8a972df726ed0ac56b88
- Tutorial: https://www.youtube.com/watch?v=w25ea_I89iM

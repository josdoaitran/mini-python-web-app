# mini-python-web-app
Python Webapp - Postgres - Heroku - Flask


## Installation:

- Python 3
- Install pipenv: `sudo pip install pipenv`
- Python environment: `pipenv shell`
=> In the project, we should have `Pipfile` file
- Install flash by command `pipenv install flash`
- Install Postgress local Database `docker pull postgres`
Start Postgres database
`docker run --name postgresql -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=Password@12345 -p 5432:5432 -v /data:/var/lib/postgresql/data -d postgres`
- PGADmin Docker: `docker pull dpage/pgadmin4:latest`
Start PGADmin
`docker run --name my-pgadmin -p 5555:80 -e 'PGADMIN_DEFAULT_EMAIL=testingforevrything@gmail.com' -e 'PGADMIN_DEFAULT_PASSWORD=P@SS'-d dpage/pgadmin4`
- Install Postgres `brew install postgres`
- PostgreSQL Python Libraries by these commands:
  + `brew install libxml2 libxmlsec1 pkg-config`
  + `pipenv install psycopg2`
  + `pipenv install psycopg2-binary`
(If any error on MAC, run this command: `xcode-select --install`)
  + `pipenv install flask_sqlalchemy`

- Create tables:
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


## References:
- Code: https://github.com/bradtraversy/python_feedback_app
- Deployment: https://gist.github.com/bradtraversy/0029d655269c8a972df726ed0ac56b88
- Tutorial: https://www.youtube.com/watch?v=w25ea_I89iM

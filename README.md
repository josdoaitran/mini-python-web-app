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
`docker run --name postgresql -e POSTGRES_USER=myusername -e POSTGRES_PASSWORD=mypassword -p 5432:5432 -v /data:/var/lib/postgresql/data -d postgres`
- PGADmin Docker: `docker pull dpage/pgadmin4:latest`
Start PGADmin
`docker run --name my-pgadmin -p 8090:8080 -e 'PGADMIN_DEFAULT_EMAIL=user@domain.local' -e 'PGADMIN_DEFAULT_PASSWORD=postgresmaster'-d dpage/pgadmin4`
- Install Postgres `brew install postgres`
- PostgreSQL Python Libraries by these commands:
  + `brew install libxml2 libxmlsec1 pkg-config`
  + `pipenv install psycopg2`
  + `pipenv install psycopg2-binary`

(If any error on MAC, run this command:
  `xcode-select --install`
)


## References:
- Code: https://github.com/bradtraversy/python_feedback_app
- Deployment: https://gist.github.com/bradtraversy/0029d655269c8a972df726ed0ac56b88

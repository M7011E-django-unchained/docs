# Installation

Here comes information about what to do before installing and running the system and how to run it.

## Make sure docker is installed and running

If docker is not installed, it can be installed from [here](https://docs.docker.com/engine/install/).

## Create .env file in the same folder as the docker-compose.yml are 

`.env` file should look like this:

```env
DATABASE_URL = [your mongodb url]
PORT = 5000
NODE_ENV = production
DJANGO_API_PORT = 8000
DJANGO_API_TOKEN_VERIFICATION_URL = http://trading-api:8000/user/token/verify/
```

## Add db.sqlite3 file to the same folder as the docker-compose.yml are

Either start out with an fresh one or use one provided with some data. Beware, the data structure must be of correct version with the django project. In order to guarantee correct version, clone the [trading_api repo](https://github.com/M7011E-django-unchained/trading_api) and do the setup and simply run `python manage.py migrate` to get a fresh db-file.

## Run all software in one go

`docker compose up`

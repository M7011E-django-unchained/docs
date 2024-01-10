# Installation

Here comes information about what to do before installing and running the system and how to run it. **NOTE!** This installation is for production environment and pulls images directly from stable branches on github repositories and do not require the user to have all code locally on their own computer. 

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

There is a db-file provided in this folder but this contains some data for testing. In order to use a fresh db-file just clone the [trading_api repo](https://github.com/M7011E-django-unchained/trading_api) and do the setup and simply run `python manage.py createsuperuser` and follow the instruction, then run `python manage.py migrate` to get a fresh db-file containing one superuser which you created. Replace the provided db-file with your own and the system will use your data (presumably just a superuser) instead of the testdata.

## Run all software in one go

`docker compose up`

# Installation

Here comes information about what to do before installing and running the system and how to run it.

## Create .env file in the same folder as the docker-compose.yml containing

```env
DATABASE_URL = [your mongodb url]
PORT = 5000
NODE_ENV = production
DJANGO_API_PORT = 8000
DJANGO_API_TOKEN_VERIFICATION_URL = http://127.0.0.1:8000/user/token/verify/
```

## Run all software in one go

`docker-compose up`

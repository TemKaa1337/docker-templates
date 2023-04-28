to build and run: docker-compose up -d --build

to enter php:
- docker-compose exec php /bin/bash

to enter database: 
- docker-compose exec database /bin/bash
- psql -u postgres
- mysql -u user -p

to access webserver - http://127.0.0.1:8080/

to install Laravel:
1. docker-compose exec php /bin/bash
2. composer create-project laravel/laravel .

to set laravel database:
0. create database
1. set DB_CONNECTION
2. set DB_HOST (as database container name)
3. set DB_PORT
4. set DB_DATABASE
5. set DB_USERNAME
6. set DB_PASSWORD

to install symfony:
0. symfony new .
1. composer require symfony/maker-bundle
2. composer require symfony/orm-pack
3. add to env
- if postgres DATABASE_URL="mysql://user:password@database:3306/project?serverVersion=8.0"
- if mysql DATABASE_URL="postgresql://postgres:postgres@database:5432/project?serverVersion=15&charset=utf8"
4. if postgres call php bin/console doctrine:database:create
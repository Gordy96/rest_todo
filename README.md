to make it all work you need to execute:

`cd docker`

`docker-compose --env-file .env.dist build`

`docker-compose --env-file .env.dist up`

`docker exec docker_php_1 /bin/sh -c "composer install"`

`docker exec docker_php_1 /bin/sh -c "npm install"`

`docker exec docker_php_1 /bin/sh -c "npm run prod"`

`docker exec docker_php_1 /bin/sh -c "php bin/console doctrine:database:create"`

`docker exec docker_php_1 /bin/sh -c "php bin/console doctrine:migrations:migrate"`
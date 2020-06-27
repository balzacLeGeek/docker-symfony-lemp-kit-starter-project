#Docker / Symfony & LEMP Kit Starter Project
==================================
A Docker / Symfony 4 / LEMP environment ready for you

## Getting Started
It's simple:

1. Clone this repository `https://github.com/balzacLeGeek/docker-symfony-lemp-kit-starter-project.git`
2. Run `docker-compose up -d`
3. Create your symfony project using `docker-compose exec php-fpm symfony new --full my_project` or `docker-compose exec php-fpm composer create-project symfony/website-skeleton my_project_name`
4. Go to `http://localhost:8000`
 
## Access services outside the containers

Service|Address outside containers
------|---------|-----------
Webserver|[localhost:8000](http://localhost:8000)
PhpMyAdmin|**host:** `localhost`; **port:** `8080`

## Some useful commands

  * Start containers in the background: `docker-compose up -d`
  * Stop containers: `docker-compose stop`
  * Kill containers: `docker-compose kill`
  * View container logs: `docker-compose logs`
  * Execute command inside of container: `docker-compose exec SERVICE_NAME COMMAND` where `COMMAND` is whatever you want to run. Examples:
        * Shell into the PHP container, `docker-compose exec php-fpm bash`
        * Run symfony console, `docker-compose exec php-fpm bin/console`
        * Open a mysql shell, `docker-compose exec mysql mysql -uroot -pCHOSEN_ROOT_PASSWORD`
  * Change permissions:  `docker-compose exec -it php-fpm chown -R www-data:www-data /symfony/YOUR_FOLDER_NAME`

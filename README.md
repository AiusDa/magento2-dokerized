# MAGENTO 2 DOCKERIZED

## Intro

Welcome to my docker project for Magento Sites, feel free to use it as you wish, however I would appreciate recognition and feedback.

Stack:

- Apache 2.2
- PHP 7.1
- Mysql 5.7

Highlights:

- Tested for use with Magento 2.2
- Persistent database
- Easy to use

## Get Started

1. Create log files:
    - logs/apache/access.log
    - logs/apache/error.log
2. Create src folder
3. Create lib folder into db config:
    - config/mysql/lib
4. Clone .env-example and rename it as .env and set your env variables
5. Run: ```docker-compose build``` or ```docker-compose build --no-cache```
6. Install Magento into src folder:
    - If you have an existing Magento project clone it into src folder, then type into console:
    ```docker-compose run --rm composer install --ignore-platform-reqs```
    - Else type into console:
    ```docker-compose run --rm composer --ignore-platform-reqs create-project --repository-url=https://repo.magento.com/ magento/project-community-edition .```
7. Open in Broser your Magento URL and setup with the wizzard.
8. If you want run some ```magento``` command, you need prefix your command with: ```docker-compose run php php /var/www/html/magento <command>```

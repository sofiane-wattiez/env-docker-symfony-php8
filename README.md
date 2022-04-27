# ENV Docker [SYMFONY 6 + PHP 8.0.13]

**Warning :** I learn this tech actually, this is my first conf docker for dev environment.

###  Clone the repository :

* git hub : ```https://github.com/sofiane-wattiez/env-docker-symfony-php8.git```

* docker hub : ```https://hub.docker.com/repository/docker/swattiez/symfony6-php8```

* branch git : ```You have conf for php8.1.0 on 2nd branch```

### Run the docker-compose

  ```
  docker-compose build
  docker-compose up -d
  ```
  
  Connect into the PHP container
  
  ```docker exec -it bf6be9debe38 bash```
  
  ## Create your Symfony application and launch the web serv
  ```
  symfony new new-project --full
  cd new-project
  symfony serve -d
  ```
  
### Create an account (identical to your local session)
  ```
  adduser username
  chown username:username -R .
  ```
  
Your application is available at :  http://127.0.0.1:9000

If you need a database, modify the .env file like this example:

 ``` DATABASE_URL="postgresql://symfony:ChangeMe@database:5432/app?serverVersion=13&charset=utf8```
  
## Ready to use with

**This docker-compose provides you :**

* PHP-8.0.13-cli (Debian)
* Composer
* Symfony CLI
* common php extentions
* nodejs, npm, yarn
* postgres:13-alpine
* mailcatcher

# Requirements

Out of the container, this docker-compose is created for a Linux OS , use wsl2 if you used windows

* WSL2 with linux distrib (<font color="red">Only for Windows user</font>)
* Linux (Ubuntu)
* Docker
* Docker-compose

## Author

* **Sofiane Wattiez**

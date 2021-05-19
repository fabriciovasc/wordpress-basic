# WordPress basic
Simple Wordpress application with docker and docker-compose

## Getting started
These instructions will cover usage information and for the docker container

### Prerequisites
In order to run this container you'll need docker and docker-compose installed.

* [Windows](https://docs.docker.com/windows/started)
* [OS X](https://docs.docker.com/mac/started/)
* [Linux](https://docs.docker.com/linux/started/)

### Images
For the execution of the containers, the following images were used.

* [wordpress](https://hub.docker.com/_/wordpress)
* [mysql](https://hub.docker.com/_/mysql)
* [phpmyadmin/phpmyadmin](https://hub.docker.com/r/phpmyadmin/phpmyadmin)

### Usage

#### Create containers
> docker-compose up -d --build

    Creating network "wordpress-basic_wpsite" with the default driver
    Creating volume "wordpress-basic_db_data" with default driver
    Creating wordpress-basic_db_1 ... done
    Creating wordpress-basic_wordpress_1  ... done
    Creating wordpress-basic_phpmyadmin_1 ... done

#### Show containers
> docker ps

    CONTAINER ID   IMAGE                   COMMAND                  CREATED         STATUS         PORTS                                   NAMES
    68cf792db93e   phpmyadmin/phpmyadmin   "/docker-entrypoint.…"   5 seconds ago   Up 3 seconds   0.0.0.0:8080->80/tcp, :::8080->80/tcp   wordpress-basic_phpmyadmin_1
    100ba124e65f   wordpress:latest        "docker-entrypoint.s…"   5 seconds ago   Up 3 seconds   0.0.0.0:8000->80/tcp, :::8000->80/tcp   wordpress-basic_wordpress_1
    311be767137c   mysql:latest            "docker-entrypoint.s…"   5 seconds ago   Up 4 seconds   3306/tcp, 33060/tcp                     wordpress-basic_db_1

#### Install and show WordPress
As we can see, the wordpress container is in service, so it’s time to set it up. 
* [Click here to open local host Wordpress](http://localhost:8000)

#### Show phpMyAdmin
After installing wordpress, we can manage the database schemas with phpMyAdmin.
* [Click here to open local host phpMyAdmin](http://localhost:8080)

      User: root
      Password: password














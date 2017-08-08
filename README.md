# PHP Development stack
A docker config to enable me to quickly start a random php project. 

## Quickstart

### 0. Prerequisites

* [Docker](https://www.docker.com/products/overview)
* [Docker Compose](https://docs.docker.com/compose)

### 1. Download

```
git clone git@github.com:thomascrepain/php-development-stack.git
```

### 2. Set-up the environment variables

```
cd php-development-stack
cp .env.example .env
```

### 3. Start Docker

In the project root folder run:
```
docker-compose up
```

The app will be running at http://localhost

## Directory structure

    .
    ├── data        # Persistent data (e.g., database)
    ├── logs        # Logs of the app and all supporting services
    ├── docs        # Documentation files
    ├── public      # Public files (webroot)
    ├── services    # Supporting services (e.g., Docker containers) and their configs
    ├── src         # Source files
    ├── tests       # Automated tests
    ├── .env        # Environment variables 
    ├── LICENSE
    └── README.md

## Supporting services

This repo only uses official Docker images from Docker Hub. Any modifications to these images are available in `services/<image-name>/Dockerfile`.

### Nginx (stable-alpine)

The application is available at http://localhost

* [Nginx](https://www.nginx.com)
* [Nginx on Docker Hub](https://hub.docker.com/_/nginx/)

### PHP-FPM (7-fpm-alpine)

Installed:
```
* libmcrypt
* lybmcrypt-dev
* mysql-client
* icu-dev
* make
* gcc
* g++
* autoconf
* pdo_mysql
* iconv
* mcrypt
* intl
* opcache
* mbstring
```

* [PHP](http://php.net/)
* [PHP on Docker Hub](https://hub.docker.com/_/php/)

### MariaDB (latest)

The MariaDB server is for the host machine available at localhost:3306. This should be turned of in production or blocked by firewall.

* [MariaDB](https://mariadb.org/)
* [MariaDB on Docker Hub](https://hub.docker.com/_/mariadb/)

### Mailcatcher (latest)

An SMTP server is available for the application on port 1025. All emails send through this server are available at http://localhost:1080

* [Mailcatcher](https://mailcatcher.me/)
* [Mailcatcher on Docker Hub](https://hub.docker.com/r/sj26/mailcatcher/)

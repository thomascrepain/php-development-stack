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

### 4. Start Docker

In the project root folder run:
```
docker-compose up
```

The app will be running at http://localhost

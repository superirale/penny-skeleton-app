# Penny Classic Application
This is a first [penny](https://github.com/gianarb/penny) implementation.
"Classic" because it integrates [league/plates](https://github.com/thephpleague/plates) and help you to build a HTML application.

## Installation
```
git clone git@github.com:gianarb/penny-classic-app
cd penny-classic-app
composer install
npm install
grunt dev
```

## Built-in webserver

```
php -S 127.0.0.1:8080 -t public
```

it's ready! You can visit [127.0.0.1:8080](https://127.0.0.1:8080).

## Docker (NGINX/PHP-FPM)

**Attention**: This is a *development* environent due to how services are configured. If you want to use it in production
you have to: disable error reporting, persist logs, raise limits and fine tune your configurations.

This repository contains a `docker-compose.yml.dist` file which currently configures two containers, one
with the NGINX webserver and one with php-fpm. This file *must be renamed* into `docker-compose.yml` and modified
if you need something specific for your system like paths, ip addresses, ports and so on. Remember that the docker-compose.yml file
is ignored since this is very specific to the current installation.

### Crate your docker-compose.yml

```bash
cp docker-compose.yml.dist docker-compose.yml
# edit it for your specific needs
vi docker-compose.yml ```

### Build
Before starting you have to build penny-classic specific images, to do it issue a:

```bash
docker-compose build
```

### Up and running

```bash
docker-compose up -d
```

Now you can visit `http://127.0.0.10` - this address is configured in the `docker-compose.yml`

## Know how
This skeleton application not resolve ALL your problems and it's not perfect, this is a starting point and implementation example.
The penny's target is this! You are free to build your implementation, it made of experience and need.

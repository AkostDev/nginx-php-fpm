# Web Server with NGINX

## Installation

1. Clone this repository
2. Run `docker build -t nginx-php-fpm:latest . --no-cache`

## Example _docker-compose.yml_

```yaml
version: "3.1"
services:
  php-fpm:
    image: nginx-php-fpm:latest
    container_name: php-fpm
    restart: always
    ports:
      - "8000:80"
    volumes:
      - ./:/var/www/html
```
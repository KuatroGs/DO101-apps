FROM php:8.1-apache

RUN apt-get update && apt-get install -y apache2-utils

COPY . /var/www/html/

CMD ab -dSrk -c 20 -n 50000000 http://${SCALE_SERVICE_HOST}:${SCALE_SERVICE_PORT}/index.php

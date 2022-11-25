FROM php:8.1.2-fpm-alpine

EXPOSE 9000 8999

RUN docker-php-ext-install mysqli pdo pdo_mysql && docker-php-ext-enable mysqli pdo pdo_mysql

RUN apk update && apk add npm && apk add curl 

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer
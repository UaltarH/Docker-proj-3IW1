FROM php:8-fpm-alpine

EXPOSE 9000

RUN docker-php-ext-install mysqli && docker-php-ext-enable mysqli

RUN apk update && apk add composer --no-cache && apk add npm

RUN composer install && npm run build && php artisan migrate:fresh —seed 
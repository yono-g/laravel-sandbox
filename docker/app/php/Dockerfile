FROM php:7.4-fpm-alpine

RUN apk --no-cache add \
        postgresql-dev

RUN docker-php-ext-install \
    bcmath \
    pdo_pgsql

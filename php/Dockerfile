FROM php:7.4-fpm-alpine

COPY --from=composer:2.1 /usr/bin/composer /usr/bin/composer

RUN apk --update --no-cache add libzip-dev && \
docker-php-ext-install pdo_mysql zip bcmath 

COPY ./php/php.ini /usr/local/etc/php/php.ini
COPY ./php/php-fpm.d/www.conf /usr/local/etc/php-fpm.d/zzz-www.conf

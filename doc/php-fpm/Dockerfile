FROM php:8.0-fpm

RUN docker-php-ext-install pdo_mysql

COPY doc/php-fpm/php.ini-production /usr/local/etc/php/php.ini
COPY --chown=www-data:www-data src /var/www
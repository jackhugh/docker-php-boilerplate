FROM php:8.0-fpm

RUN docker-php-ext-install pdo_mysql

ARG UID
ARG GID

RUN usermod -u ${UID:-1000} www-data
RUN groupmod -g ${GID:-1000} www-data

COPY doc/php-fpm/php.ini-production /usr/local/etc/php/php.ini
COPY --chown=www-data:www-data src /var/www
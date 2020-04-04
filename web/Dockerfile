FROM php:7.2-apache

RUN apt-get update && apt-get install -y libpq-dev
RUN docker-php-ext-install \
    pdo_pgsql \
    && a2enmod \
   	rewrite

RUN pecl install xdebug \
    && docker-php-ext-enable xdebug

COPY ./xdebug.ini /usr/local/etc/php/conf.d/xdebug.ini

COPY ./dev.99-overrides.ini /usr/local/etc/php/conf.d/99-overrides.ini

RUN chmod -R 777 /var/www/
RUN chown -R www-data:www-data /var/www

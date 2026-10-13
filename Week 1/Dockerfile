FROM php:8.3-apache

WORKDIR /var/www/html

RUN apt update \
    && apt install git unzip \
    && pecl install xdebug \
    && docker-php-ext-enable xdebug

COPY . .

EXPOSE 80

CMD [“apache2ctl”, “-D”, “FOREGROUND”]
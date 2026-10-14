FROM php:8.3-apache

WORKDIR /var/www/html

COPY index.php .

RUN apt update \
    && apt install -y git unzip \
    && pecl install xdebug \
    && docker-php-ext-enable xdebug

COPY . .

EXPOSE 80

CMD ["apache2ctl", "-D", "FOREGROUND"]
FROM php:8.0-apache

RUN apt-get update && apt-get install -y\
    nano

RUN docker-php-ext-install pdo pdo_mysql
RUN docker-php-ext-enable pdo_mysql

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www/vig11

COPY . .



RUN a2enmod rewrite

RUN chmod -R 777 storage
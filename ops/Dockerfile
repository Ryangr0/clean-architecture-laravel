FROM php:7.3.10-apache

WORKDIR /app

RUN a2enmod rewrite

RUN docker-php-ext-install pdo pdo_mysql

COPY ./ops/apache/clean-architecture-laravel.conf /etc/apache2/sites-available/000-default.conf

COPY . /app

EXPOSE 80

ENTRYPOINT apache2-foreground

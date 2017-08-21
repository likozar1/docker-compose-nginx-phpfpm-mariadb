FROM php:7.1.5-fpm

RUN apt-get update
RUN apt-get install -y \
        libpng12-dev \
        libjpeg-dev \
        libfreetype6-dev

RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
        && docker-php-ext-install pdo \
                pdo_mysql \
                gd
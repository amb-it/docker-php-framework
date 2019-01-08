FROM php:fpm-alpine

RUN apk update && apk add  --no-cache \
    git \
    mysql-client \
    curl \
    mc \
    libzip-dev \
    libmcrypt \
    libmcrypt-dev \
    libxml2-dev \
    freetype \
    freetype-dev \
    libpng \
    libpng-dev \
    libjpeg-turbo \
    libjpeg-turbo-dev g++ make autoconf

RUN docker-php-ext-install zip pdo_mysql

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin/ --filename=composer

WORKDIR /var/www

CMD ["php-fpm"]

EXPOSE 9000
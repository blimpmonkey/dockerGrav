FROM php:7.1-fpm-alpine

RUN	apk update && apk upgrade

RUN apk add --update \
    zlib-dev \
    freetype-dev \
    libjpeg-turbo-dev \
    libpng-dev

# php extensions
RUN docker-php-ext-install \
    zip \
    gd

# Install modules
RUN apk add --update \
    git \
    curl

# Install Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
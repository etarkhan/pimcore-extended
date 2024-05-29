FROM composer
FROM php:8.0-apache

LABEL maintainer="Aref.Tarkhani@gmail.com"
LABEL build_date="2024-05-29"

RUN apt-get update \
        && apt-get install -y supervisor locales unzip zlib1g-dev libpng-dev libjpeg-dev libbz2-dev \
            libicu-dev libzip-dev zip fonts-roboto openssh-server sudo supervisor libssh2-1 libssh2-1-dev tzdata \
            cron rsyslog vim \
        && docker-php-ext-install zip gd mysqli exif bz2 pdo_mysql intl opcache \
        && rm -rf /var/lib/apt/lists/*

RUN a2enmod rewrite

RUN apt-get update && apt-get install -y libmagick++-dev imagemagick inkscape ffmpeg \
        && pecl install imagick \
        && docker-php-ext-enable imagick \
        && pecl install ssh2-1.3.1 \
        && docker-php-ext-enable ssh2 \
        && rm -rf /var/lib/apt/lists/* \
        && pecl install apcu \
        && docker-php-ext-enable apcu \
        && pecl install redis \
        && docker-php-ext-enable redis \
        && rm -rf /var/lib/apt/lists/*

RUN echo de_DE.UTF-8 UTF-8 >> /etc/locale.gen && \
        dpkg-reconfigure --frontend=noninteractive locales

CMD ["apache2-foreground"]
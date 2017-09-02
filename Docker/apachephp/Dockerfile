FROM php:5.6-apache

RUN apt-get update \
 && apt-get install -y \
      vim-nox \
      libpq-dev \
      libfreetype6-dev \
      libjpeg62-turbo-dev \
      libmcrypt-dev \
      libpng12-dev \
      libxml2-dev \
 && apt-get clean \
 && docker-php-ext-install -j$(nproc) iconv mcrypt pgsql pdo_pgsql \
 && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
 && docker-php-ext-install -j$(nproc) gd \
 && docker-php-ext-install -j$(nproc) gettext mbstring opcache pcntl shmop soap sockets sysvmsg wddx zip \
 && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

EXPOSE 80
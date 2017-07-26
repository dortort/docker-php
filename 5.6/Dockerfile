FROM php:5.6

RUN apt-get update \
  && apt-get install -y zlib1g-dev libicu-dev g++ \
  && rm -rf /var/lib/apt/lists/*

RUN docker-php-ext-configure intl \
  && docker-php-ext-install intl

RUN pecl install mongodb-1.1.9

RUN echo "extension=mongodb.so" > /usr/local/etc/php/conf.d/mongodb.ini

RUN echo '[Date]\ndate.timezone = "UTC"' > /usr/local/etc/php/conf.d/timezone.ini
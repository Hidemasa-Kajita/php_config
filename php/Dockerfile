FROM php:8.0-fpm

RUN apt-get update && apt-get install -y git

RUN git clone https://github.com/phpredis/phpredis.git /usr/src/php/ext/redis
RUN docker-php-ext-install mysqli redis

RUN mkdir /var/run/php-fpm
COPY conf/zzz-www.conf /usr/local/etc/php-fpm.d/zzz-www.conf

COPY conf/php.ini /usr/local/etc/php/conf.d/php.ini

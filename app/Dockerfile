FROM php:7.4-fpm-alpine3.10

RUN apk upgrade --update && \
  apk --no-cache add autoconf make g++ && \
  pecl install xdebug && \
  docker-php-ext-enable xdebug && \
  docker-php-ext-install pdo_mysql opcache

COPY app/override.ini /usr/local/etc/php/conf.d/overrides.ini

FROM php:7.3-fpm-alpine3.8

RUN apk upgrade --update && \
  apk --no-cache add icu-dev autoconf make g++ gcc && \
  pecl install -f xdebug-2.7.0beta1 && \
  docker-php-ext-enable xdebug && \
  docker-php-ext-install pdo_mysql

ADD override.ini /usr/local/etc/php/conf.d/overrides.ini

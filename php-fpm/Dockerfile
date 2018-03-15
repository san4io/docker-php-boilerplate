FROM php:fpm-alpine

RUN apk update \
    && apk upgrade \
    && apk add --no-cache bash shadow libxml2-dev curl-dev \
    && usermod -u 1000 www-data

RUN docker-php-ext-install zlib; exit 0 \
    && cp /usr/src/php/ext/zlib/config0.m4 /usr/src/php/ext/zlib/config.m4

RUN docker-php-ext-install opcache pdo_mysql tokenizer xml curl

WORKDIR /var/www

CMD ["php-fpm"]

EXPOSE 9000
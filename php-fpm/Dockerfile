FROM php:fpm-alpine

RUN apk update \
    && apk upgrade \
    && apk add --no-cache bash shadow \
    && usermod -u 1000 www-data

WORKDIR /var/www

CMD ["php-fpm"]

EXPOSE 9000
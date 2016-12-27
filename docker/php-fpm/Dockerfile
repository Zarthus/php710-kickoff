FROM php:7.1-fpm-alpine

MAINTAINER Vincent Composieux <vincent.composieux@gmail.com>
MAINTAINER Jos Ahrens <github@lynvie.com>

# RUN apk add --update \
#    php-fpm \
#    php-apcu \
#    php-curl \
#    php-gd \
#    php-iconv \
#    php-imagick \
#    php-json \
#    php-intl \
#    php-mcrypt \
#    php-mysql \
#    php-opcache \
#    php-openssl \
#    php-pdo \
#    php-pdo_mysql \
#    php-mysqli \
#    php-pdo_pg \
#    php-pgsql \
#    php-xml \
#    php-zlib

RUN rm -rf /var/cache/apk/* && rm -rf /tmp/*

ADD app.ini /etc/php7/fpm/conf.d/
ADD app.ini /etc/php7/cli/conf.d/

ADD app.pool.conf /etc/php7/fpm.d/

CMD ["php-fpm", "-F"]

EXPOSE 9000

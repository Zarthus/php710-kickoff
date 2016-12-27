FROM php:7.1-fpm-alpine

MAINTAINER Vincent Composieux <vincent.composieux@gmail.com>
MAINTAINER Jos Ahrens <github@lynvie.com>

# RUN apk add --update \
#    php7-fpm \
#    php7-apcu \
#    php7-curl \
#    php7-gd \
#    php7-iconv \
#    php7-imagick \
#    php7-json \
#    php7-intl \
#    php7-mcrypt \
#    php7-mysql \
#    php7-opcache \
#    php7-openssl \
#    php7-pdo \
#    php7-pdo_mysql \
#    php7-mysqli \
#    php7-pdo_pg \
#    php7-pgsql \
#    php7-xml \
#    php7-zlib

RUN rm -rf /var/cache/apk/* && rm -rf /tmp/*

ADD app.ini /etc/php7/fpm/conf.d/
ADD app.ini /etc/php7/cli/conf.d/

ADD app.pool.conf /etc/php7/fpm.d/

CMD ["php-fpm", "-F"]

EXPOSE 9000

FROM ubuntu:14.04

RUN apt-get update && apt-get install -y \
    pkg-config \
    libssl-dev \
    libsslcommon2-dev \
    php5-common \
    php5-cli \
    php5-fpm \
    php5-mcrypt \
    php5-intl \
    php5-dev \
    php-pear \
    php-apc

RUN pecl install mongo

ADD symfony.ini /etc/php5/fpm/conf.d/
ADD symfony.ini /etc/php5/cli/conf.d/

ADD symfony.pool.conf /etc/php5/fpm/pool.d/

CMD ["php5-fpm", "-F"]

EXPOSE 9000

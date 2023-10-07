FROM wordpress:php8.0

RUN pecl install redis && \
    docker-php-ext-enable redis

RUN apt-get update && apt-get install libxml-2.0

RUN docker-php-ext-install soap

COPY custom.ini $PHP_INI_DIR/conf.d/

USER www-data:www-data

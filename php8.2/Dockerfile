FROM wordpress:php8.2

RUN pecl install redis && \
    docker-php-ext-enable redis

RUN apt-get update && apt-get install -y libxml2-dev

RUN docker-php-ext-install soap

COPY custom.ini $PHP_INI_DIR/conf.d/

USER www-data:www-data

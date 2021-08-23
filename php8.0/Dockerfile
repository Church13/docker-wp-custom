FROM wordpress:php8.0

RUN pickle install redis && \
    docker-php-ext-enable redis

COPY custom.ini $PHP_INI_DIR/conf.d/

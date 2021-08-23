FROM wordpress:php8.0

RUN pecl install redis && \
    docker-php-ext-enable redis && \
    wp plugin install easy-wp-smtp --activate && \
    wp plugin install updraftplus --activate

COPY custom.ini $PHP_INI_DIR/conf.d/

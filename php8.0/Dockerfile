FROM wordpress:php8.0

RUN pecl install redis && \
    docker-php-ext-enable redis && \
    curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar && \
    chmod +x wp-cli.phar && \
    mv wp-cli.phar /usr/local/bin/wp

COPY custom.ini $PHP_INI_DIR/conf.d/

USER www-data:www-data

RUN wp plugin install easy-wp-smtp --activate && \
    wp plugin install updraftplus --activate

FROM php5.6.31-nginx1.12.1:latest 
RUN pecl install redis-3.1.0 \
    && pecl install xdebug \
    && docker-php-ext-enable redis xdebug
RUN wget https://getcomposer.org/composer.phar \
    && mv composer.phar /usr/local/bin/composer \
    && chmod +x /usr/local/bin/composer

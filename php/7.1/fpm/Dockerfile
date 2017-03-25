FROM php:7.1-fpm
# Install modules
RUN apt-get update && \
    apt-get install -y libpq-dev \
        libpq5 \
        php5-pgsql

RUN docker-php-ext-install pgsql \
        pdo \
        pdo_pgsql \
        bcmath

CMD ["php-fpm"]

FROM php:5.6-fpm
# Install modules
RUN apt-get update && apt-get install -y libpq-dev libpq5 php5-pgsql \
    && docker-php-ext-install pgsql pdo_pgsql

CMD ["php-fpm"]

FROM php:8.2.0alpha2-fpm

# Install system dependencies
RUN apt-get update && apt-get install -y \
    git \
    nodejs npm
# Install PHP extensions
RUN docker-php-ext-install pdo pdo_mysql
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

# CMD rm -rf vendor composer.lock;composer install;npm install & npm run dev;cp .env.example .env;php artisan key:generate;php artisan migrate;php artisan db:seed
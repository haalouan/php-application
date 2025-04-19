FROM php:8.1-fpm

RUN apt-get update && apt-get install -y \
    libpng-dev \
    libjpeg62-turbo-dev \
    libfreetype6-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install gd

# Install PDO and PDO_MySQL extension
RUN docker-php-ext-install pdo pdo_mysql

# Set the working directory
WORKDIR /var/www/html

# Expose port 80
EXPOSE 80
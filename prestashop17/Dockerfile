FROM php:8-apache

WORKDIR /var/www/project

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN apt-get update && apt-get install -y zip libzip-dev libpng-dev libmagickwand-dev libicu-dev cron

RUN pecl install imagick

RUN docker-php-ext-enable imagick

RUN docker-php-ext-install zip pdo_mysql mysqli bcmath gd intl

RUN a2enmod rewrite headers && service apache2 restart

COPY apache.conf /etc/apache2/sites-available/000-default.conf

COPY php.ini /usr/local/etc/php/php.ini

COPY crontab /etc/crontab

COPY entrypoint.sh /var/www/entrypoint.sh

ENTRYPOINT ["sh", "/var/www/entrypoint.sh"]

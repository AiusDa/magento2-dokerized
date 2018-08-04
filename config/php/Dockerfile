FROM php:7.1-apache-jessie
RUN apt-get update && apt-get install -y \
    zlib1g-dev \
    libicu-dev \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libmcrypt-dev \
    libpng12-dev \
    libbz2-dev \
    libxslt-dev
RUN docker-php-ext-install mcrypt \
    && docker-php-ext-install xsl \
    && docker-php-ext-install intl \
    && docker-php-ext-install pdo_mysql \
    && docker-php-ext-install soap \
    && docker-php-ext-install zip \
    && docker-php-ext-install bcmath
RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/
RUN docker-php-ext-install gd
RUN a2enmod rewrite

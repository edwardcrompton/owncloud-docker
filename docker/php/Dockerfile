FROM arm32v7/php:7.2-fpm
RUN apt-get update || apt-get update
RUN apt-get install -y openssl zip unzip
RUN apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng-dev
RUN apt-get install -y zlib1g-dev libicu-dev g++
RUN docker-php-ext-configure intl
RUN docker-php-ext-install -j$(nproc) intl zip gd pdo_mysql
#RUN docker-php-ext-install zip
#RUN docker-php-ext-install gd
#RUN docker-php-ext-install pdo_mysql
WORKDIR /app
RUN chown -R www-data:www-data /app


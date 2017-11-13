FROM php:7-fpm-alpine

# modules
RUN apk update \
    && apk add libmcrypt libmcrypt-dev \
       mysql-client \
       icu-dev make gcc g++ autoconf \
	&& docker-php-ext-install pdo_mysql \
	&& docker-php-ext-install iconv \
	&& docker-php-ext-install mcrypt \
	&& docker-php-ext-install intl \
	&& docker-php-ext-install opcache \
	&& docker-php-ext-install mbstring 

CMD ["php-fpm"]

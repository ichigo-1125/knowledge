FROM php:8.0.3-fpm

# computer environment
ENV TZ=UTC \
	LANG=ja_JP.UTF-8 \
	LANGUAGE=ja_JP:ja

# packages
RUN apt-get update && apt-get install -y \
	default-mysql-client

RUN docker-php-ext-install pdo_mysql mysqli

RUN cp /usr/share/zoneinfo/Asia/Tokyo /etc/localtime && \
	mkdir /var/run/php-fpm && \
	mkdir /var/log/php

WORKDIR /var/www/html

CMD ["php-fpm"]

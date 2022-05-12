# From official php image.
FROM php:8.0-fpm

RUN apt-get install -y --fix-missing php8.0 php8.0-curl php8.0-gd php8.0-mbstring \
    php8.0-zip php8.0-mysql php8.0-xml php8.0-fpm php8.0-imagick \
    php8.0-tidy php8.0-intl \
    php8.0-cli php8.0-common php8.0-cgi php8.0-xdebug \
    php-pear php8.0-gmp php8.0-bcmath php-soap php8.0-sqlite3    

# Install redis driver.
#RUN mkdir -p /usr/src/php/ext/redis; \
#    curl -fsSL --ipv4 https://github.com/phpredis/phpredis/archive/5.3.4.tar.gz | tar xvz -C "/usr/src/php/ext/redis" --strip 1; \
#    docker-php-ext-install redis
#